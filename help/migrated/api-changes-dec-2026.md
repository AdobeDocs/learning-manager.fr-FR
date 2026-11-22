---
description: Découvrez comment utiliser les paramètres d’abonnement au forum et les API des abonnés pour configurer les e-mails de résumé et gérer les abonnés au forum
jcr-language: en_us
title: Modifications apportées aux API en novembre 2026
exl-id: 9b2d3856-810c-4352-bf18-667f698d4d70
source-git-commit: 4234f3cc3b9d77a7f9d197d2df2160ec62edd6d6
workflow-type: tm+mt
source-wordcount: '5724'
ht-degree: 4%
---

# Modifications apportées aux API en décembre 2026

## API pour les notifications des instructeurs des forums de discussion {#api-discussion-board-instructors}

Cet article décrit les nouvelles API qui prennent en charge les notifications des instructeurs des forums de discussion. Utilisez-les pour abonner des instructeurs et des gestionnaires de cohorte à des forums de discussion et pour contrôler quelle activité apparaît dans leurs courriels de résumé.

### Séquence API {#api-sequence}

Les API se répartissent en deux groupes. L&#39;API `boardSubscriptionSettings` fonctionne au niveau du compte. L’API des abonnés fonctionne au niveau du forum. Utilisez les API dans cette séquence :

| Étape | API | Objectif | Portée |
|---|---|---|---|
| 1 | [`POST /boardSubscriptionSettings`](#api-create-settings) | Définissez les paramètres au niveau du compte. | `admin:write` |
| 2 | [`PATCH /boardSubscriptionSettings`](#api-update-settings) | Mettez à jour les paramètres au niveau du compte. | `admin:write` |
| 3 | [`GET /boardSubscriptionSettings`](#api-get-settings) | Récupérez les paramètres au niveau du compte. | `admin:read` |
| 4 | [`GET /boards/{id}/subscribers`](#api-get-subscribers) | Obtenir la liste des utilisateurs abonnés à un forum. | `admin:read` |
| 5 | [`POST /boards/{id}/subscribers`](#api-subscribe-users) | Abonnement d’utilisateurs à un forum. | `admin:write` |
| 6 | [`DELETE /boards/{id}/subscribers/{userId}`](#api-unsubscribe-user) | Désabonner un utilisateur d&#39;un forum. | `admin:write` |

### Authentification et autorisations

Toute personne qui s’authentifie avec OAuth et possède les portées `admin:read` et `admin:write` peut appeler ces API. Les API utilisent les portées OAuth suivantes :

* `admin:read` : liste des abonnés et paramètres de notification de lecture (`GET` demandes).
* `admin:write` : créez ou modifiez les paramètres de notification, et ajoutez ou supprimez des abonnés (`POST`, `PATCH` et `DELETE` demandes).

>[!NOTE]
>
>L’accès au forum est vérifié à nouveau lors de l’envoi d’une notification. Si un abonné perd l&#39;accès à un forum, la livraison est ignorée pour ce forum, mais l&#39;abonnement est conservé. La livraison reprend si l’accès est rétabli.

### Limites et considérations

* Le nombre d’abonnés pouvant être ajoutés est plafonné.
* Le résumé est envoyé sous la forme d’un e-mail unique sans pagination, et la taille du corps de l’e-mail est limitée. Pour les forums très actifs, choisissez une fréquence de résumé qui permet de gérer chaque e-mail, par exemple toutes les 6 heures.
* Les liens de résumé ouvrent la publication, le commentaire ou la réponse uniquement pour les utilisateurs connectés.

## API pour créer des paramètres au niveau du compte {#api-create-settings}

### Objectif de l’API {#purpose-create-settings}

Utilisez cette API pour définir les paramètres au niveau du compte pour les notifications d’abonnement aux forums pour la première fois. Les paramètres contrôlent la façon dont les résumés des notifications sont générés dans le compte :

* Quels événements du forum de discussion génèrent des notifications.
* Fréquence d’envoi des e-mails de résumé.
* Indique si les publications, les commentaires, les réponses et les votes sont inclus.

Pour modifier les paramètres ultérieurement, utilisez [`PATCH /boardSubscriptionSettings`](#api-update-settings).

### Point de terminaison {#endpoint-create-settings}

```http
POST /primeapi/v2/boardSubscriptionSettings
```

| Propriété | Valeur |
|---|---|
| Portée | `admin:write` |
| Format de la demande | `application/vnd.api+json;charset=UTF-8` |
| Format de réponse | `application/vnd.api+json;charset=UTF-8` |

### Corps de la demande {#request-body-create-settings}

Envoyez les paramètres en tant qu&#39;attributs d&#39;une ressource `boardSubscriptionSettings`.

| Champ | Type | Description |
|---|---|---|
| `notifyNewPost` | booléen | Indique si les abonnés sont avertis lorsqu’une nouvelle publication est ajoutée à un forum. |
| `notifyComment` | booléen | Indique si les abonnés sont avertis lorsqu’un commentaire est ajouté à une publication. |
| `notifyReply` | booléen | Indique si les abonnés sont avertis lorsqu’une réponse est ajoutée à un commentaire. |
| `digestFrequencyHours` | entier | Fréquence d’envoi, en heures, de l’e-mail de résumé. Les valeurs valides sont comprises entre 1 et 168 (une semaine). Par exemple, 24 envoie un résumé quotidien et 168 un résumé hebdomadaire. |

### Exemple de requête {#example-request-create-settings}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyNewPost": true,
      "notifyComment": true,
      "notifyReply": true,
      "digestFrequencyHours": 24
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Exemple de réponse - 201 Créé {#example-response-create-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Codes de réponse {#response-codes-create-settings}

| Statut | Signification |
|---|---|
| 201 | La demande a réussi. Les paramètres au niveau du compte ont été créés. |
| 400 | Erreur générique de requête incorrecte. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |

## API pour mettre à jour les paramètres au niveau du compte {#api-update-settings}

### Objectif de l’API {#purpose-update-settings}

Utilisez cette API pour mettre à jour les paramètres de compte que vous avez créés avec [`POST /boardSubscriptionSettings`](#api-create-settings). Par exemple, modifiez la fréquence du résumé ou activez ou désactivez un type d’événement.

### Point de terminaison {#endpoint-update-settings}

```http
PATCH /primeapi/v2/boardSubscriptionSettings
```

| Propriété | Valeur |
|---|---|
| Portée | `admin:write` |
| Format de la demande | `application/vnd.api+json;charset=UTF-8` |
| Format de réponse | `application/vnd.api+json;charset=UTF-8` |

### Corps de la demande {#request-body-update-settings}

Envoyez les attributs que vous souhaitez modifier, au même format que l’API de création : `notifyNewPost`, `notifyComment`, `notifyReply` et `digestFrequencyHours`. Les attributs que vous n’envoyez pas conservent leurs valeurs actuelles. Pour obtenir la description de chaque attribut, consultez [API pour créer des paramètres au niveau du compte](#api-create-settings).

### Exemple de requête {#example-request-update-settings}

```bash
curl -X PATCH \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyReply": true,
      "digestFrequencyHours": 12
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Exemple de réponse - 200 OK {#example-response-update-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 12,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Codes de réponse {#response-codes-update-settings}

| Statut | Signification |
|---|---|
| 200 | La demande a réussi. Les paramètres au niveau du compte ont été mis à jour et la réponse contient les paramètres actuels. |
| 400 | Erreur générique de requête incorrecte. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |

## API pour récupérer les paramètres au niveau du compte {#api-get-settings}

### Objectif de l’API {#purpose-get-settings}

Lorsque les utilisateurs s’abonnent à un forum, Adobe Learning Manager peut les informer de l’activité dans ce forum par le biais d’e-mails de résumé. Les paramètres au niveau du compte déterminent les types d’activités qui déclenchent une notification et la fréquence d’envoi du résumé.

Cette API vous permet de récupérer ces paramètres. Utilisez-le pour afficher la configuration de notification actuelle dans votre application ou pour vérifier les paramètres avant de créer des fonctionnalités qui en dépendent.

### Point de terminaison {#endpoint-get-settings}

```http
GET /primeapi/v2/boardSubscriptionSettings
```

| Propriété | Valeur |
|---|---|
| Portée | `admin:read` |
| Format de réponse | `application/vnd.api+json;charset=UTF-8` |

### Exemple de requête {#example-request-get-settings}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Exemple de réponse - 200 OK {#example-response-get-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Schéma de la ressource {#resource-schema-get-settings}

**`boardSubscriptionSettings`attributs**

| Champ | Type | Description |
|---|---|---|
| `notifyNewPost` | booléen | Indique si les abonnés sont avertis lorsqu’une nouvelle publication est ajoutée à un forum. |
| `notifyComment` | booléen | Indique si les abonnés sont avertis lorsqu’un commentaire est ajouté à une publication. |
| `notifyReply` | booléen | Indique si les abonnés sont avertis lorsqu’une réponse est ajoutée à un commentaire. |
| `digestFrequencyHours` | entier | Fréquence d’envoi, en heures, de l’e-mail de résumé. Les valeurs valides sont comprises entre 1 et 168 (une semaine). Utilisez cette valeur pour indiquer aux utilisateurs la fréquence à laquelle l’e-mail de résumé doit être envoyé. Par exemple, affichez « Quotidien » lorsque la valeur est 24 et « Hebdomadaire » lorsque la valeur est 168. |

### Codes de réponse {#response-codes-get-settings}

| Statut | Signification |
|---|---|
| 200 | La demande a réussi. La réponse contient les paramètres d’abonnement au forum au niveau du compte. |
| 400 | Erreur générique de requête incorrecte. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |

### Utiliser cette API dans votre intégration {#integration-get-settings}

Un cas d’utilisation courant est un écran de préférences de notification qui montre comment les e-mails d’abonnement au forum sont configurés pour le compte.

1. Lorsque l&#39;écran des préférences de notification de votre application se charge, appelez `GET /boardSubscriptionSettings`.
1. Afficher les types d’activité qui déclenchent une notification et la fréquence d’envoi de l’e-mail de résumé, en utilisant les valeurs de la réponse.

## API pour récupérer les abonnés au forum {#api-get-subscribers}

### Objectif de l’API {#purpose-get-subscribers}

Récupérez la liste des utilisateurs qui sont abonnés à un forum spécifique. Les utilisateurs qui sont abonnés à un forum sont informés des nouvelles activités qu’il contient. Cette API renvoie les utilisateurs qui sont actuellement abonnés à un forum donné, ainsi que des détails sur le moment et l’auteur de la création de chaque abonnement.

Utilisez cette API pour afficher une liste d&#39;abonnés dans votre application, pour vérifier qui reçoit les mises à jour d&#39;une carte ou pour synchroniser les données d&#39;abonnement d&#39;une carte avec un système externe.

La réponse est paginée. Utilisez les paramètres de requête `page[offset]` et `page[limit]` pour vous déplacer dans les listes d&#39;abonnés volumineuses. Les données renvoyées sont soumises aux autorisations de l’utilisateur appelant sur le forum demandé.

### Point de terminaison {#endpoint-get-subscribers}

```http
GET /primeapi/v2/boards/{id}/subscribers
```

| Propriété | Valeur |
|---|---|
| Portée | `admin:read` |
| Format de réponse | `application/vnd.api+json;charset=UTF-8` |

### Paramètres {#parameters-get-subscribers}

| Paramètre | Dans | Obligatoire | Par défaut | Description |
|---|---|---|---|---|
| `id` | chemin | Oui | Sans objet | ID du forum dont vous souhaitez récupérer les abonnés. L&#39;accès est soumis aux autorisations de l&#39;appelant sur le forum. |
| `page[offset]` | requête | Non | 0 | Position de départ des enregistrements à renvoyer. |
| `page[limit]` | requête | Non | 10 | Nombre d&#39;abonnés à retourner par page. La valeur maximale autorisée est 200. |

### Exemple de requête {#example-request-get-subscribers}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers?page[offset]=0&page[limit]=50'
```

### Exemple de réponse - 200 OK {#example-response-get-subscribers}

```json
{
  "data": [
    {
      "id": "1234:5678",
      "type": "boardSubscriber",
      "attributes": {
        "boardId": 1234,
        "dateSubscribed": 1757000000000,
        "subscribedByUserId": 5678,
        "user": {
          "id": "5678",
          "name": "Jane Doe",
          "email": "jane.doe@example.com",
          "avatarUrl": "https://example.com/avatars/5678.png",
          "bio": "Learning enthusiast",
          "contentLocale": "en-US",
          "uiLocale": "en-US",
          "timeZoneCode": "PST",
          "userType": "INTERNAL",
          "state": "ACTIVE",
          "profile": "Learner",
          "roles": ["Learner"],
          "gamificationEnabled": true,
          "pointsEarned": 120,
          "pointsRedeemed": 20,
          "enrollOnClick": true,
          "preferredResolution": "720p",
          "lastLoginDate": "2026-09-23T18:12:04.000Z"
        }
      }
    }
  ]
}
```

### Schéma de la ressource {#resource-schema-get-subscribers}

La réponse inclut une nouvelle ressource, `boardSubscriber`. Ses attributs sont `boardId`, `dateSubscribed`, `subscribedByUserId` et `user`. L&#39;objet utilisateur incorporé contient des informations sur l&#39;abonné telles que l&#39;ID utilisateur, le nom, l&#39;adresse e-mail, le profil et les rôles, ainsi que d&#39;autres métadonnées utilisateur.

**`boardSubscriber`attributs**

| Champ | Type | Description |
|---|---|---|
| `id` | chaîne | ID d’abonnement opaque. |
| `type` | chaîne | Type de ressource. |
| `boardId` | Nombre | ID du forum auquel l’utilisateur est abonné. |
| `dateSubscribed` | Nombre | Horodatage de l’inscription de l’utilisateur au forum. |
| `subscribedByUserId` | Nombre | ID de l’utilisateur qui a créé l’abonnement. |
| `user` | objet | Détails de l’utilisateur abonné (intégré, voir ci-dessous). |

**`user`(intégré, à l&#39;intérieur d&#39;un abonné)**

| Champ | Type | Description |
|---|---|---|
| `id` | chaîne | ID utilisateur opaque. |
| `name` | chaîne | Nom complet de l’utilisateur. |
| `email` | chaîne | Adresse électronique de l’utilisateur. |
| `avatarUrl` | chaîne | URL de la photo de profil de l’utilisateur. |
| `bio` | chaîne | Courte biographie de l&#39;utilisateur. |
| `binUserId` | chaîne | Identifiant interne de l’utilisateur. |
| `userUniqueId` | chaîne | Identifiant unique de l’utilisateur dans le compte. |
| `userType` | chaîne | Type d’utilisateur, par exemple, interne ou externe. |
| `state` | chaîne | État actuel du compte utilisateur. |
| `profile` | chaîne | Profil attribué à l’utilisateur. |
| `roles` | tableau de chaînes | Rôles détenus par l’utilisateur. |
| `contentLocale` | chaîne | Paramètres régionaux dans lesquels l’utilisateur préfère afficher le contenu. |
| `uiLocale` | chaîne | Paramètres régionaux utilisés pour l’interface utilisateur. |
| `timeZoneCode` | chaîne | Fuseau horaire configuré pour l’utilisateur. |
| `preferredResolution` | chaîne | Résolution vidéo préférée de l’utilisateur. |
| `enrollOnClick` | booléen | Indique si l’utilisateur est inscrit automatiquement lors de la sélection d’un objet d’apprentissage. |
| `gamificationEnabled` | booléen | Indique si la ludification est activée pour l’utilisateur. |
| `pointsEarned` | Nombre | Total des points de ludification gagnés par l&#39;utilisateur. |
| `pointsRedeemed` | Nombre | Total des points de ludification récupérés par l&#39;utilisateur. |
| `lastLoginDate` | chaîne | Date et heure de la dernière connexion de l’utilisateur. |
| `fields` | objet | Champs utilisateur personnalisés et leurs valeurs. |
| `metadata` | objet | Métadonnées supplémentaires associées à l’utilisateur. |

### Codes de réponse {#response-codes-get-subscribers}

| Statut | Signification |
|---|---|
| 200 | La demande a réussi. La réponse contient les abonnés du forum. |
| 400 | Erreur générique de requête incorrecte. Par exemple, l’ID de tableau ou une valeur de pagination est incorrect. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |

### Utiliser cette API dans votre intégration {#integration-get-subscribers}

Un cas d’utilisation courant est une vue administrateur ou modérateur qui affiche toutes les personnes qui reçoivent des mises à jour pour un forum.

1. Lorsque la vue se charge, appelez ce point de terminaison avec l&#39;ID de tableau et une valeur `page[limit]` adaptée à votre disposition (jusqu&#39;à 200).
1. Affichez les valeurs `user.name`, `user.email` et `dateSubscribed` pour chaque abonné.
1. Si le nombre d&#39;enregistrements renvoyés est égal à `page[limit]`, il se peut qu&#39;il y ait davantage d&#39;abonnés. Rappelez le point de terminaison, en augmentant `page[offset]` de la taille de la page, jusqu&#39;à ce qu&#39;une page renvoie moins d&#39;enregistrements que demandé.

## API pour abonner des utilisateurs à un forum {#api-subscribe-users}

### Objectif de l’API {#purpose-subscribe-users}

Abonnez un ou plusieurs utilisateurs à un forum de discussion afin qu&#39;ils reçoivent des e-mails de résumé pour celui-ci. Identifiez les utilisateurs par ID utilisateur, par adresse e-mail (résolue en ID utilisateur au sein du compte) ou les deux. Vous pouvez ajouter plusieurs utilisateurs dans une seule demande. Voir [Abonnements en bloc](#bulk-subscriptions).

### Point de terminaison {#endpoint-subscribe-users}

```http
POST /primeapi/v2/boards/{id}/subscribers
```

| Propriété | Valeur |
|---|---|
| Portée | `admin:write` |
| Format de la demande | `application/vnd.api+json;charset=UTF-8` |
| Format de réponse | `application/vnd.api+json;charset=UTF-8` |

### Paramètres {#parameters-subscribe-users}

| Paramètre | Dans | Obligatoire | Description |
|---|---|---|---|
| `id` | chemin | Oui | ID du forum auquel abonner les utilisateurs. |

### Corps de la demande {#request-body-subscribe-users}

Envoyez les utilisateurs en tant qu&#39;attributs d&#39;une ressource `boardSubscriberBulkRequest`. Au moins l&#39;un des `userIds` ou `emails` est requis.

| Champ | Type | Description |
|---|---|---|
| `data.attributes.userIds` | tableau de nombres | ID des utilisateurs à abonner. |
| `data.attributes.emails` | tableau de chaînes | Adresses e-mail des utilisateurs à abonner. Chaque adresse est résolue en un ID utilisateur dans le compte. |

### Exemple de requête {#example-request-subscribe-users}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriberBulkRequest",
    "attributes": {
      "userIds": [
        1234,
        5678
      ],
      "emails": [
        "abc@xyz.com"
      ]
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1010/subscribers'
```

### Exemple de réponse - 207 Multi-Status {#example-response-subscribe-users}

```json
{
  "added": [
    {
      "userId": "12345",
      "status": "SUCCESS"
    }
  ],
  "failed": [
    {
      "userId": "78910",
      "errorCode": "NO_BOARD_ACCESS"
    }
  ]
}
```

**Attributs de réponse**

| Champ | Type | Description |
|---|---|---|
| `added` | tableau | Utilisateurs qui ont été abonnés. Chaque entrée a un `userId` et un `status`. Les utilisateurs déjà abonnés sont également signalés ici comme des réussites. |
| `failed` | tableau | Utilisateurs qui n&#39;ont pas pu être abonnés. Chaque entrée a un `userId` et un `errorCode`, par exemple `NO_BOARD_ACCESS`. |

### Codes de réponse {#response-codes-subscribe-users}

| Statut | Signification |
|---|---|
| 207 | Multi-état. La demande a été traitée et la réponse répertorie le résultat pour chaque utilisateur dans `added` et `failed`. |
| 400 | Erreur générique de requête incorrecte. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |
| 404 | La ressource demandée, comme le tableau, n&#39;a pas été trouvée. |
| 409 | Le forum étant inactif, supprimé ou retiré, la demande est rejetée dans son intégralité. |

### Abonnements en masse {#bulk-subscriptions}

Utilisez l&#39;abonnement groupé pour ajouter plusieurs utilisateurs à un forum de discussion dans une seule demande. L’abonnement en bloc permet de réduire le nombre d’appels API dont vous avez besoin pour gérer les abonnés. Il est utile lorsque :

* Un instructeur gère plusieurs cohortes.
* Un gestionnaire de cohorte doit avoir accès à de nombreux forums de discussion.
* Un système externe synchronise les abonnements aux cartes par lots.
* Plusieurs instructeurs doivent être inscrits lors de la création de la cohorte.

#### Comportement d’ajout en bloc

Une demande en bloc peut contenir des ID utilisateur, des adresses e-mail ou une combinaison des deux. Chaque utilisateur est traité indépendamment.

#### Comportement impuissant

L’ajout en bloc est idempotent. Si un utilisateur est déjà abonné au forum, la demande aboutit, aucun abonnement en double n’est créé et l’abonnement existant reste inchangé. Cela permet aux clients de réessayer les demandes en toute sécurité.

#### Succès partiel

Certains utilisateurs peuvent être abonnés tandis que d’autres ne parviennent pas à se valider. L&#39;opération n&#39;échoue pas car un ou plusieurs utilisateurs ne sont pas valides.

| Casse | Résultat |
|---|---|
| L’utilisateur existe et a accès au forum | Succès |
| L’utilisateur est déjà abonné | Succès |
| L’utilisateur n’a pas accès au forum | Échec (`NO_BOARD_ACCESS`) |
| L’utilisateur n’existe pas | Échec |
| L’utilisateur est inactif | Échec |
| L’utilisateur a été supprimé | Échec |

#### Format de réponse

L&#39;abonnement en bloc renvoie le statut multiple HTTP 207 avec un résultat `added` et un résultat `failed` pour chaque utilisateur, comme dans l&#39;[exemple de réponse](#example-response-subscribe-users).

#### Échecs de validation courants

* **L&#39;utilisateur n&#39;a pas accès au forum.** Si un utilisateur n&#39;a pas de visibilité sur le forum, `NO_BOARD_ACCESS` est renvoyé pour cet utilisateur. Les autres utilisateurs continuent d’être traités normalement.
* **Le forum est inactif, supprimé ou retiré.** Si le forum n’est pas éligible pour les abonnements, la demande est rejetée avec le conflit HTTP 409.
* **L&#39;utilisateur n&#39;est pas valide.** Si un compte utilisateur n’existe pas, est inactif ou a été supprimé, l’opération renvoie une entrée d’échec pour cet utilisateur.

## API pour désabonner un utilisateur d’un forum {#api-unsubscribe-user}

### Objectif de l’API {#purpose-unsubscribe-user}

Désabonner un utilisateur d&#39;un forum de discussion. Une fois l’abonnement supprimé, l’utilisateur ne reçoit plus de notifications ni d’e-mails de résumé pour ce forum.

### Point de terminaison {#endpoint-unsubscribe-user}

```http
DELETE /primeapi/v2/boards/{id}/subscribers/{userId}
```

| Propriété | Valeur |
|---|---|
| Portée | `admin:write` |
| Format de réponse | `application/vnd.api+json;charset=UTF-8` |

### Paramètres {#parameters-unsubscribe-user}

| Paramètre | Dans | Obligatoire | Description |
|---|---|---|---|
| `id` | chemin | Oui | ID du forum. |
| `userId` | chemin | Oui | ID de l’utilisateur auquel se désabonner. |

### Exemple de requête {#example-request-unsubscribe-user}

```bash
curl -X DELETE \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers/5678'
```

### Exemple de réponse - 204 Aucun contenu {#example-response-unsubscribe-user}

La réponse n&#39;a pas de corps.

### Codes de réponse {#response-codes-unsubscribe-user}

| Statut | Signification |
|---|---|
| 204 | La demande a réussi. L&#39;utilisateur a été désabonné du forum. |
| 400 | Erreur générique de requête incorrecte. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |
| 404 | La ressource demandée, telle que le forum ou l&#39;abonnement, n&#39;a pas été trouvée. |

## Commande d’API de signet et gestion du contenu retiré {#bookmark-api-ordering-retired-content}

### Objectif de l’API

Les élèves mettent en signet les formations qu&#39;ils souhaitent revoir. Avant cette modification, les API de signets renvoyaient les signets sans ordre particulier. Les intégrations, en particulier les implémentations sans en-tête, ne pouvaient pas afficher d’abord les signets les plus récemment enregistrés. Les élèves ayant de nombreux signets devaient faire défiler les éléments plus anciens pour trouver les plus récents.

Les signets des objets d&#39;apprentissage retirés restaient également dans la liste. La sélection de l’un d’eux a entraîné une erreur « Page introuvable ».

Cette modification améliore les API de signets de deux manières :

* Les signets sont renvoyés dans l’ordre chronologique, du plus récent au plus récent.
* Les signets vers les objets d&#39;apprentissage retirés ne sont plus renvoyés.

Aucun nouveau point de terminaison, paramètre ou attribut de réponse n’est introduit. Les intégrations existantes continuent de fonctionner sans modifications.

### URL de base et conventions

Les API de signet utilisent le chemin et les conventions de base suivants :

| Élément | Valeur |
|---|---|
| Chemin de base | `/primeapi/v2` |
| Type de contenu | `application/vnd.api+json` |
| Authentification | Jeton OAuth avec accès en lecture à l’élève |
| Ordre par défaut | Signet le plus récent en premier |
| Nouveaux paramètres | Aucune |
| Structure de réponse | Inchangé |

### Points de terminaison

#### Points de terminaison renvoyant des signets

Les points de terminaison suivants renvoient les signets dans le nouvel ordre :

| Point de terminaison | Retours |
|---|---|
| `GET /primeapi/v2/learningObjects?filter.bookmarks=true` | Objets d’apprentissage que l’élève a marqués d’un signet |
| `GET /primeapi/v2/bookmarks` | Signets de l’élève |

#### Obtenir les objets d’apprentissage marqués d’un signet dans l’ordre

`GET /primeapi/v2/learningObjects?filter.bookmarks=true`

<!-- Content Review by Claude: Please confirm the endpoint list. The dev-to-QE hand-off confirms ordering for GET /learningObjects?filter.bookmarks=true. The PRD (ALMER-442) also lists GET /primeapi/v2/bookmarks. Please also confirm the OAuth scope. -->

Renvoie les objets d&#39;apprentissage que l&#39;élève appelant a marqués d&#39;un signet. L’élément avec signet le plus récent est le premier et le plus ancien est le dernier.

**Portée :** accès en lecture de l&#39;élève

Le point de terminaison accepte le paramètre de requête suivant :

| Paramètre | Dans | Obligatoire | Description |
|---|---|---|---|
| `filter.bookmarks` | requête | Oui | Définissez sur `true` pour renvoyer uniquement les objets d’apprentissage que l’élève a marqués d’un signet |

**Exemple de requête**

```http
GET /primeapi/v2/learningObjects?filter.bookmarks=true
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

**Exemple de réponse OK 200**

L’élève a marqué un signet comme suit : Prise en main d’Adobe Analytics en premier, Création de projets d’espace de travail en second et Segmentation avancée dans Adobe Analytics en dernier. La réponse les répertorie du plus récent au plus ancien. Les autres attributs sont omis par souci de concision.

```json
{
  "data": [
    {
      "id": "course:2400162",
      "type": "learningObject",
      "attributes": {
        "name": "Advanced Segmentation in Adobe Analytics"
      }
    },
    {
      "id": "course:2400160",
      "type": "learningObject",
      "attributes": {
        "name": "Building Workspace Projects"
      }
    },
    {
      "id": "course:2400159",
      "type": "learningObject",
      "attributes": {
        "name": "Getting Started with Adobe Analytics"
      }
    }
  ]
}
```

>[!NOTE]
>
>Le nouvel ordre est le comportement par défaut et s’applique à tous les comptes.

### Ordre des signets

#### Ordre des signets

Les signets sont triés par date d’enregistrement par l’élève, du plus récent au plus ancien. Par exemple, si un élève met en signet le cours A, puis le cours B, puis le cours C, la réponse répertorie le cours C en premier, le cours B en second et le cours A en dernier.

Si un objet d’apprentissage marqué d’un signet apparaissant à la 10e position, par exemple, n’est pas enregistré et est ensuite marqué d’un signet à nouveau, il apparaîtra comme étant récent et en premier dans la liste.

Les intégrations qui triaient précédemment les signets sur le client peuvent supprimer cette logique et afficher les résultats dans l’ordre renvoyé.

### Gestion du contenu retiré

#### Gestion des objets d&#39;apprentissage retirés

Les signets vers les objets d&#39;apprentissage retirés ne sont pas renvoyés dans la réponse, que l&#39;élève soit inscrit ou non à l&#39;objet d&#39;apprentissage.

Les objets d’apprentissage retirés qui sont marqués d’un signet ne s’affichent pas sauf si l’élève y est inscrit.

Les élèves ne voient plus les signets qui entraînent une erreur « Page introuvable ». Le signet est masqué dans les résultats et non supprimé.

### Compatibilité

Cette modification ne rompt pas les consommateurs d’API existants :

* Les points de terminaison et leurs paramètres restent inchangés.
* La structure de la réponse reste inchangée et aucun attribut n’est ajouté ou supprimé.
* Seul l’ordre des résultats et l’exclusion des objets d’apprentissage retirés diffèrent du comportement précédent.

### Utiliser cette API dans votre intégration

Un cas d’utilisation courant est une liste « Enregistré pour plus tard » dans une expérience d’élève sans en-tête. Vous souhaitez que les élèves voient d’abord leurs signets les plus récents, sans liens vers du contenu retiré.

1. Appelez `GET /primeapi/v2/learningObjects?filter.bookmarks=true` lorsque l’élève ouvre la liste.
2. Affichez les objets d’apprentissage dans l’ordre renvoyé. Le premier élément est le dernier élément marqué d&#39;un signet.
3. Supprimez tout filtrage de tri côté client ou de contenu retiré que vous avez ajouté comme solution de contournement.
4. Afficher le nombre de signets en utilisant le nombre d’éléments de la réponse. Les signets vers les objets d&#39;apprentissage retirés ne sont plus inclus.

### Prise en charge d’API pour les instances multi-inscrites dans le widget Conformité des élèves dans l’application Élève {#api-multienrolled-instances-lc-widget}

L’API publique prend en charge ce comportement via un paramètre de requête facultatif sur le point d’entrée des inscriptions existantes. Si vous omettez le paramètre, l’API renvoie les mêmes résultats qu’auparavant, de sorte que les intégrations existantes, y compris les implémentations sans en-tête, continuent de fonctionner sans modification.

**Point de terminaison**

GET /primeapi/v2/enrollments

**Paramètre de requête**

includeMultiInstanceEnrollments (facultatif)

**Requête**

https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&filter.loTypes=course&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&sort=dateEnrolled

**Valeur**

vrai. False par défaut.

**Corps de la réponse**

{

« links » : {

« self » : « [https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnrolled&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true) »,

« next » : « [https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnrolled&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true&amp;page\[cursor\]=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjOjOjOjEwLCJsZWFybmluZ1B2dyYcn0i} »](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&page%5bcursor%5d=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWFybmluZ1Byb2dyYW0iOjAsImNlcnRpZmljYXRpb24iOjB9)

},

« data » : \[

{

« id »: « course:15067_30122_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« completionDeadline » : « 2026-02-24T10:50:45.000Z »,

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:15067 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:15067_30122 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:15067_30122_41715_1_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:1108800_1997400_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « SELF_ENROLL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:1108800 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:1108800_1997400 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:1108800_1997400_2174574_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:2027668_3707328_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:2027668 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:2027668_3707328 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:2027668_3707328_2665897_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:2030067_3709862_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:2030067 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:2030067_3709862 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:2030067_3709862_2668467_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:3081896_5749155_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:3081896 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:3081896_5749155 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:3081896_5749155_3737554_0_3400468 »,

« type »: « learningObjectResourceGrade »

},

{

« id »: « course:3081896_5749155_3737555_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:2037893_3717940_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:2037893 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:2037893_3717940 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:2037893_3717940_3676856_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:3049434_5713130_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« completionDeadline » : « 2020-05-05T18:29:59.000Z »,

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:3049434 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:3049434_5713130 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:3049434_5713130_3693595_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:2001397_3679403_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:2001397 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:2001397_3679403 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:2001397_3679403_2635974_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:2037862_3717900_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« enrollmentSource »: « MGR_APPROVAL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « APPROBATION_EN_ATTENTE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:2037862 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:2037862_3717900 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:2037862_3717900_3676816_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

},

{

« id »: « course:2037837_3717863_3400468 »,

« type »: « learningObjectInstanceEnenrollment »,

« attributes » : {

« completionDeadline » : « 2020-02-29T18:29:59.000Z »,

« enrollmentSource »: « SELF_ENROLL »,

« hasPassed » : false,

« progressPercent » : 0,

« score » : 0,

« state »: « AUTRE »

},

« relations » : {

« learner » : {

« data » : {

« id »: « 3400468 »,

« type »: « utilisateur »

}

},

« learningObject » : {

« data » : {

« id »: « course:2037837 »,

« type »: « learningObject »

}

},

« loInstance » : {

« data » : {

« id »: « course:2037837_3717863 »,

« type »: « learningObjectInstance »

}

},

« loResourceGrades » : {

« data » : \[

{

« id »: « course:2037837_3717863_3597363_0_3400468 »,

« type »: « learningObjectResourceGrade »

}

\]

}

}

}

\]

}

## Date du dernier accès pour l’inscription au parcours d’apprentissage {#api-last-access-date-lp-enrollment}

Adobe Learning Manager vous permet de stocker des métadonnées personnalisées, telles qu’une date de dernier accès, lors d’une inscription à un parcours d’apprentissage. Vous définissez et lisez les métadonnées via l’API. Cela vous permet de suivre l’accès limité dans le temps aux parcours d’apprentissage que vous attribuez.

## À propos des métadonnées d’inscription au parcours d’apprentissage

Vous pouvez déjà définir une date de dernier accès pour une inscription à un cours via l’API. Cette date contrôle la durée pendant laquelle un élève peut accéder au cours. Les inscriptions au parcours d’apprentissage prennent désormais en charge un champ de métadonnées générique, ce qui vous permet de stocker une date de dernier accès ou toute autre valeur que vous souhaitez suivre.

Vous n’avez pas besoin d’activer le champ ou d’envoyer un en-tête spécial. Le champ est vide tant que vous ne l’avez pas défini.

>[!NOTE]
>
>Les métadonnées sont destinées à votre propre suivi. Adobe Learning Manager ne le met pas à jour lorsque les élèves ouvrent un parcours d’apprentissage ou ses cours, et il ne contrôle pas l’accès au parcours d’apprentissage. Elle n’est pas propagée non plus aux cours du chemin. Chaque cours conserve sa propre date de dernier accès, de sorte que les cours du même parcours peuvent avoir des dates différentes. Continuez à gérer séparément l’expiration de l’accès au niveau du cours.

### Règles de métadonnées {#metadata-rules}

* La valeur doit être un objet JSON. Une chaîne, un nombre, une Booléen ou un tableau renvoie une erreur 400 avec le message `metadata must be a JSON object`.
* Vous pouvez utiliser n’importe quelle clé. Adobe Learning Manager ne valide pas les clés ou les valeurs, et n’applique pas de format de date. Les exemples de cet article utilisent des millisecondes d&#39;époque, le même format que les dates de cours.
* Une demande de PATCH remplace l’objet de métadonnées entier. Il ne fusionne pas avec les valeurs existantes. Par conséquent, les clés que vous omettez sont supprimées.
* Le paramètre `"metadata": null` efface toutes les métadonnées et renvoie 200.
* Une demande avec un objet `attributes` vide ou sans clé `metadata` ne modifie pas les métadonnées stockées.
* Lorsqu&#39;aucune métadonnée n&#39;est définie ou après que vous l&#39;avez effacée, la clé `metadata` n&#39;est pas dans la réponse.

## Définition des métadonnées d’une inscription existante

Utiliser un jeton d’administration.

Envoyez une demande de PATCH au point de terminaison suivant, où `{enrollmentId}` correspond à l’ID d’inscription au parcours d’apprentissage au format `learningProgram:<lpId><instanceId><userId>` :

```
PATCH /primeapi/v2/users/{userId}/enrollments/{enrollmentId}
```

Utiliser ce corps de requête :

```json
{
  "data": {
    "id": "<enrollmentId>",
    "type": "learningObjectInstanceEnrollment",
    "attributes": {
      "metadata": {
        "lastAccessDate": 1745337600000
      }
    }
  }
}
```

### Définition des métadonnées lors de l’inscription d’un élève

Utiliser un jeton d’administration.

Envoyez une demande de POST avec le parcours d’apprentissage et les ID d’instance. Incluez un objet `metadata` facultatif dans le corps de la demande.

```
POST /primeapi/v2/users/{userId}/enrollments?loId=<lpId>&loInstanceId=<instanceId>
```

* Si `metadata` n&#39;est pas un objet JSON, la demande renvoie 400 et l&#39;utilisateur n&#39;est pas inscrit.
* Si l’utilisateur est déjà inscrit, la demande renvoie 200 et ne change rien. Pour modifier les métadonnées d’une inscription existante, utilisez la demande du PATCH.
* La réponse n’inclut pas les métadonnées. Envoyez une demande de GET pour le lire.

### Récupération des métadonnées

Vous pouvez récupérer les métadonnées avec un jeton d’administrateur ou d’élève. Les demandes diffèrent par type de jeton.

| Jeton | Obtenir une inscription | Lister les inscriptions au parcours d’apprentissage |
|---|---|---|
| Administrateur | `GET /primeapi/v2/users/{userId}/enrollments/{enrollmentId}` | `GET /primeapi/v2/users/{userId}/enrollments?filter.loTypes=learningProgram` |
| Gestion | `GET /primeapi/v2/enrollments/{enrollmentId}`<br>`GET /primeapi/v2/learningObjects/{id}?include=enrollment` | `GET /primeapi/v2/enrollments?filter.loTypes=learningProgram` |

>[!NOTE]
>
>Le paramètre `include=enrollment` fonctionne uniquement avec un jeton d&#39;élève. Il n’est pas pris en charge pour le rôle d’administrateur.

La réponse renvoie l&#39;objet `metadata` avec l&#39;inscription au parcours d&#39;apprentissage.

### Utilisation de métadonnées dans des portails sans en-tête et externes

Les portails externes et les intégrations utilisent les mêmes appels API. Utilisez la demande qui correspond au jeton utilisé par votre portail.

* **Afficher la valeur dans votre portail :** Envoyez la demande de GET pour votre type de jeton à partir du tableau ci-dessus et lisez l&#39;objet `metadata` à partir de la réponse.
* **Mettez à jour la valeur à partir d&#39;un système externe, tel qu&#39;une plateforme commerciale :** envoyez la demande du PATCH avec un jeton d&#39;administration.

## API de tâche : exportation des rapports de Report Builder avec generateCustomReport {#api-job-report-builder-exports}

La version de décembre 2026 de Adobe Learning Manager ajoute un nouveau type de tâche, `generateCustomReport`, à l’API de tâche. Utilisez-le pour exporter automatiquement tout rapport que vous avez créé dans Report Builder en transmettant l’ID de rapport.

Associé au nouveau jeu de données de quiz L2 dans Report Builder, vous pouvez désormais :

* Exportez les données de quiz au niveau des questions (L2) entre plusieurs cours et modules dans un seul rapport, au lieu d&#39;exécuter `generateQuizReport` une fois pour chaque cours.
* Automatisez les exportations récurrentes, par exemple une exportation incrémentielle quotidienne vers votre entrepôt de données ou votre outil de veille stratégique.

Les types de travaux existants, y compris `generateQuizReport`, sont inchangés.

### Avant de commencer

* Vous devez être administrateur. Le type de tâche `generateCustomReport` n&#39;est pas disponible pour les autres rôles.
* Commencez par créer et enregistrer le rapport dans Report Builder. Pour les données de quiz L2, générez le rapport à partir du jeu de données du quiz L2 et incluez les champs de niveau question dont vous avez besoin, tels que le texte de la question, la réponse de l&#39;élève, le score, le nombre de tentatives et la date de réponse.
* Notez l’ID du rapport. Vous le transmettez dans la demande en tant que `reportId`.

### Création d’une offre d’emploi

**Point de terminaison**

```
POST /primeapi/v2/jobs
```

**Corps de la demande**

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "description": "Daily L2 quiz export",
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      }
    }
  }
}
```

**Attributs**

| Attribut | Obligatoire | Description |
|---|---|---|
| `jobType` | Oui | Doit être `generateCustomReport`. |
| `payload.reportId` | Oui | ID du rapport de Report Builder enregistré, sous forme de chaîne. Doit être un entier positif, transmis sous forme de chaîne, par exemple `"1478"`. L’envoi d’un nombre, d’un 0, d’une valeur négative, décimale ou vide renvoie une erreur. |
| `description` | Non | Une description de votre choix pour le poste. |
| `callbackUrl` | Non | URL à appeler une fois la tâche terminée. Fonctionne de la même manière que pour les autres types de tâches. |
| `payload.filters` | Non | Voir la section ci-dessous. |

### Remplacer le filtre de date (facultatif) {#override-date-filter}

```json
"payload": {
  "reportId": "1478",
  "filters": [
    { "columnName": "L2 Quiz - Response - Timestamp", "operator": "gte", "val": "2026-11-15T00:00:00.000Z" }
  ]
}
```

* Il remplace le filtre de date d&#39;enregistrement du rapport pour cette exécution uniquement. L&#39;exportation couvre `val` (inclus) jusqu&#39;à l&#39;exécution de la tâche.
* `columnName` utilise le format `<Dataset name> - <Field name>`. Il doit correspondre à un filtre de date qui existe déjà dans le rapport. Elle ne respecte pas la casse, mais l’espacement et les tirets doivent correspondre exactement.
* `operator` est facultatif et seul `gte` est autorisé.
* `val` est une heure UTC ISO 8601 au cours des 7 derniers jours. Les temps sont tronqués à la seconde.
* Vous pouvez remplacer plusieurs colonnes. Une liste vide signifie que les filtres enregistrés sont utilisés.
* Cas d’utilisation : une exportation incrémentielle quotidienne qui commence là où la précédente s’est terminée.

### Erreurs renvoyées lors de la création d’une tâche

| Cause | Message |
|---|---|
| `reportId` manquant | `reportId is required` |
| `reportId` n&#39;est pas une chaîne d&#39;entier positive | `reportId must be a positive integer string` |
| Date non au format ISO | `filters.val must be in ISO format, e.g. 2020-01-01T18:30:00.000Z` |
| Date antérieure à 7 jours ou ultérieure | `filters.val must be within the last 7 days` |
| Opérateur autre que `gte` | `filters.operator must be gte` |
| Même colonne donnée deux fois | `Duplicate filter column: <column>` |
| La colonne n&#39;est pas un filtre dans le rapport | `Unsupported custom report filter column: <column>` |
| Une tâche pour le même rapport est toujours en cours d&#39;exécution | `There exists an similar job with id = <jobId> which has not finished yet` |

Seuls les problèmes liés à la définition de rapport enregistrée sont détectés lors de l’exécution de la tâche. Dans ce cas, l&#39;état de la tâche devient `Failed` et aucune raison n&#39;est renvoyée.

### Exigences en matière de rapports

Le travail échoue avec un message d’erreur si le rapport ne répond pas aux conditions suivantes :

* La définition du rapport inclut un filtre de date relative, par exemple, les 7 derniers jours.
* Chaque filtre de date du rapport doit couvrir 7 jours ou moins, et non un seul.
* Les plages de dates fixes, avec des dates de début et de fin définies, ne sont pas prises en charge et la tâche échoue.
* Un rapport sans filtre de date échoue. Cela inclut les rapports créés sur des jeux de données qui n’ont pas de champ de date.

>[!NOTE]
>
>La demande du POST est validée immédiatement. Une demande non valide est rejetée avec HTTP 400, et la raison est dans `source.info`.

### Vérifier l’état de la tâche et télécharger le rapport

**Point de terminaison**

```
GET /primeapi/v2/jobs/{jobId}
```

La réponse utilise la même structure que les autres types de tâche. Une fois la tâche terminée, `status.code` est `Completed` et `status.data.s3Url` contient le lien de téléchargement.

```json
{
  "data": {
    "type": "job",
    "id": "12345",
    "attributes": {
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      },
      "status": {
        "code": "Completed",
        "data": {
          "s3Url": "valid for 7 days"
        }
      }
    }
  }
}
```

L’API renvoie `Submitted`, `Completed` et `Failed`. Le fichier est un fichier CSV unique nommé `report.csv`.

>[!NOTE]
>
>L’URL de téléchargement est valide pendant sept jours. Téléchargez le fichier dès que le travail est terminé.

>[!IMPORTANT]
>
>Toute personne disposant du lien peut télécharger le fichier sans se connecter. Gérez le lien comme vous le feriez pour les données qu’il contient.

**Exemple de tâche ayant échoué**

```json
"status": { "code": "Failed" }
```

### Limites

Une seule tâche `generateCustomReport` peut être exécutée à la fois pour un rapport. Une deuxième demande est rejetée jusqu’à ce que la première soit terminée.

### Sortie du rapport de quiz L2

Lorsque vous générez un rapport à partir du jeu de données de quiz L2 dans Report Builder et que vous l&#39;exportez avec `generateCustomReport`, la sortie présente les caractéristiques suivantes :

* La sortie est un fichier CSV unique nommé `report.csv`. Le module est une colonne du fichier. Si vous sélectionnez un cours, le rapport ne renvoie que les modules du quiz.
* Chaque ligne représente la réponse d’un élève à une question en une seule tentative.
* Les données sont actualisées à intervalle de Report Builder standard (environ toutes les 15 minutes).
* Les valeurs de date et d’heure se trouvent dans le fuseau horaire de votre compte. L&#39;en-tête de colonne affiche le fuseau horaire, par exemple, `L2 Quiz - Response - Timestamp (America/Argentina/Salta)`.

### Champs du jeu de données de quiz L2

| Catégorie | Champs |
|---|---|
| Gestion | ID utilisateur |
| Cours | ID de cours, ID d’instance de cours, Nom du cours |
| Module | ID du module, Nom du module, Version du module |
| Question | ID de la question, Texte de la question, Réponse correcte, Type d’interaction |
| Réponse | Réponse Réponse, Score Atteint, Score Maximum Possible, Est Correct, Horodatage De La Réponse |
| Tentative | Nombre de tentatives |

>[!NOTE]
>
>Le jeu de données de quiz L2 n&#39;est pas lié à d&#39;autres jeux de données de Report Builder. Le nom de l’élève, l’adresse électronique, le responsable et les attributs personnalisés ne sont pas disponibles dans ce rapport. Pour faire correspondre une ligne à un élève, utilisez l’ID utilisateur.

Vous pouvez également exporter des rapports créés sur d&#39;autres jeux de données de Report Builder avec `generateCustomReport`. Les champs disponibles dans la sortie dépendent du jeu de données.

## API pour la création et la gestion du connecteur Zoom

Utilisez ces API pour gérer les connexions Zoom dans Adobe Learning Manager. Vous pouvez récupérer des connexions existantes, enregistrer des informations d’identification Zoom, créer ou mettre à jour des connexions, configurer des autorisations d’accès pour des groupes d’utilisateurs et des rôles personnalisés, et activer ou désactiver une connexion.

### Configuration des API de connecteur Zoom

La configuration et la gestion d’un connecteur Zoom nécessitent quatre appels API. Définissez-les dans l’ordre suivant :

| Étape | API | Ce qu’il fait |
|---|---|---|
| 1 | `POST /ctr/authcred/uuid/20012` | Enregistre les informations d’identification du zoom. |
| 2 | `POST /ctr/app/esconnect` | Crée la connexion Zoom ou met à jour une connexion existante. |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Définit les groupes d&#39;utilisateurs et les rôles personnalisés qui peuvent utiliser la connexion. |
| 4 | `POST /ctr/xtsas/{connectionId}/enable` | Active ou désactive la connexion. |

>[!NOTE]
>
>Ces API utilisent la session d’administration de l’intégration connectée. Ils n’utilisent pas de clé API ni de jeton OAuth.

### URL de base et conventions

Les API de connecteur Zoom utilisent les conventions suivantes :

| Élément | Valeur |
|---|---|
| Adresse URL de base | `https://learningmanagerstage1.adobe.com` |
| Type de contenu | `application/json` |
| Authentification | Session d’un administrateur d’intégration connecté |
| En-têtes requis | `content-type`, `accept`, `x-acap-caller-role: ROLE_INTEGRATIONADMIN`, `x-csrf-token` et `Cookie` |
| UUID du catalogue d’intégration pour Zoom | `20012` |
| Limite de connexion | 50 connexions Zoom |

La valeur `x-csrf-token` est incorporée dans le HTML de la page d&#39;administration de l&#39;intégration en tant que `csrfToken`. L&#39;en-tête `Cookie` contient les cookies de session de l&#39;administrateur connecté.

### Avant de commencer

- Connectez-vous en tant qu’administrateur d’intégration.
- Créez une application OAuth Zoom de serveur à serveur. Notez son ID client, son secret client et son ID de compte. Vous avez également besoin de l’adresse e-mail du super administrateur Zoom.
- Appeler `GET /ctr/xtsas/canCreateAccount/25`. Cela renvoie `true` si vous pouvez créer une autre connexion Zoom.

### Étape 1 : enregistrement des informations d’identification du zoom {#save-credentials}

Appelez cette API avant de créer ou de mettre à jour une connexion. Il stocke les informations d’identification utilisées par le connecteur pour se connecter à Zoom.

```
POST /ctr/authcred/uuid/20012
```

Pour mettre à jour une connexion existante, ajoutez le paramètre de requête `connectionId` :

```
POST /ctr/authcred/uuid/20012?connectionId={connectionId}
```

Le corps de la demande correspond aux informations d’identification du texte JSON. Il s’agit d’une chaîne JSON qui contient du JSON, et non un objet imbriqué. Incluez les guillemets extérieurs.

| Clé | Description |
|---|---|
| `clientId` | ID client de l’application Zoom. |
| `clientSecret` | Secret client de l’application Zoom. Cette valeur est sensible. |
| `accountId` | ID du compte Zoom. |
| `superAdmin` | Adresse e-mail du super administrateur Zoom. |

Exemple de corps de requête :

```
"{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}"
```

Exemple de réponse `200 OK` :

```json
{
  "code": 0,
  "description": "Success"
}
```

`code: 0` signifie que les informations d&#39;identification ont été enregistrées.

### Étape 2 : Créer ou mettre à jour la connexion Zoom {#create-connection}

Cette API crée une connexion Zoom. Le même point de terminaison met également à jour une connexion existante.

```
POST /ctr/app/esconnect
```

Le corps de la demande comporte les champs suivants :

| Champ | Obligatoire | Description |
|---|---|---|
| `UUID` | Oui | UUID du catalogue d’intégration. Utilisez `20012` pour le zoom. |
| `listOfConnections` | Oui | Les connexions à créer. Envoyez un élément. |
| `listOfConnections[].name` | Oui | Nom d&#39;affichage du connecteur, par exemple `Zoom_Partner_X`. |
| `listOfConnections[].tag` | Oui | Envoyez une chaîne vide (`""`) lorsque vous créez un connecteur. Ignorez-le lorsque vous en mettez à jour un. |
| `listOfConnections[].credentialsJson` | Oui | Informations d’identification au format texte JSON. Utilisez la même chaîne que celle envoyée à l’étape 1. |
| `listOfConnections[].schedules` | Oui | Planification de la synchronisation. Envoyer `objectUUID` 10002, `priority` 1 et `type` 1. |
| `listOfConnections[].id` | Mise à jour uniquement | ID de la connexion à mettre à jour, par exemple `3474737`. |

Exemple de corps de requête :

```json
{
  "UUID": 20012,
  "listOfConnections": [
    {
      "name": "Zoom_Example",
      "tag": "",
      "credentialsJson": "{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}",
      "schedules": [
        { "objectUUID": 10002, "priority": 1, "type": 1 }
      ]
    }
  ]
}
```

Exemple de réponse `200 OK` :

```json
[3474737]
```

La réponse est un tableau JSON qui contient l’ID de la nouvelle connexion. Utilisez cet ID lors des étapes 3 et 4 et lors de tout appel de suivi.

### Création et mise à jour comparées

| Différence | Créer | Mise à jour |
|---|---|---|
| `listOfConnections[].id` | Non envoyé | ID de connexion |
| `listOfConnections[].tag` | `""` | Non envoyé |
| Appel d’informations d’identification à l’étape 1 | `POST /ctr/authcred/uuid/20012` | `POST /ctr/authcred/uuid/20012?connectionId={id}` |

### Étape 3 : définir qui peut utiliser la connexion {#set-access}

Cette API définit les groupes d&#39;utilisateurs et les rôles personnalisés qui peuvent utiliser la connexion.

```
PUT /ctr/xtsa/{connectionId}/access
```

Le chemin utilise le singulier `xtsa` pour une connexion. Le pluriel `xtsas` correspond à la collection de connexions.

Le corps de la requête est un tableau JSON. Chaque élément accorde l’accès à un groupe d’utilisateurs ou à un rôle personnalisé.

| Champ | Obligatoire | Description |
|---|---|---|
| `accessType` | Oui | `USER_GROUP` ou `CUSTOM_ROLE`. |
| `accessId` | Oui | ID du groupe d’utilisateurs ou du rôle personnalisé, sous la forme d’une chaîne. |

Exemple de corps de requête :

```json
[
  { "accessType": "USER_GROUP", "accessId": "<groupId>" },
  { "accessType": "CUSTOM_ROLE", "accessId": "<roleId>" }
]
```

L&#39;API retourne `204 No Content` sans corps lorsque la liste d&#39;accès est enregistrée.

>[!NOTE]
>
>La demande remplace toute la liste d’accès. Ça ne s&#39;y ajoute pas. Tout ce qui n&#39;est pas dans le corps perd l&#39;accès. Pour supprimer tous les accès, envoyez un tableau vide (`[]`).

### Étape 4 : activer ou désactiver la connexion {#enable-disable}

Cette API active ou désactive une connexion. Utilisez-le après avoir créé la connexion, chaque fois que vous devez modifier son état.

```
POST /ctr/xtsas/{connectionId}/enable
```

Le chemin utilise le pluriel `xtsas`, comme la liste et les appels de suppression. L&#39;appel d&#39;accès à l&#39;étape 3 utilise le singulier `xtsa`.

| Paramètre Path | Type | Description |
|---|---|---|
| `connectionId` | Nombre | ID de la connexion. Il s&#39;agit du `id` renvoyé par `GET /ctr/xtsas` et de l&#39;ID renvoyé à l&#39;étape 2. |

Le corps de la demande comporte les champs suivants :

| Champ | Type | Obligatoire | Description |
|---|---|---|---|
| `objectUUID` | Nombre | Oui | Objet de synchronisation de la connexion. Utilisez `10002`, la même valeur que celle que vous avez envoyée dans `schedules[].objectUUID` à l&#39;étape 2. |
| `operation` | Nombre | Oui | Envoyer `1`. |
| `val` | Booléen | Oui | Nouvel état de la connexion. Envoyer `false` pour désactiver la connexion. Envoyer `true` pour l&#39;activer. |

Exemple de corps de requête pour désactiver une connexion :

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": false
}
```

Exemple de corps de requête pour activer une connexion :

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": true
}
```

Exemple de requête pour désactiver une connexion :

```bash
curl -X POST 'https://learningmanagerstage1.adobe.com/ctr/xtsas/<connectionId>/enable' \
  -H 'accept: application/json' \
  -H 'content-type: application/json' \
  -H 'x-acap-caller-role: ROLE_INTEGRATIONADMIN' \
  -H 'x-csrf-token: <CSRF_TOKEN>' \
  -H 'Cookie: <SESSION_COOKIES>' \
  --data '{"objectUUID":10002,"operation":1,"val":false}'
```

Pour confirmer le nouvel état, appelez `GET /ctr/xtsas`, recherchez la connexion par `id` et vérifiez son indicateur `enabled`.

>[!NOTE]
>
>L&#39;en-tête `x-acap-caller-role` doit correspondre au rôle du profil actif. Pour ces API, utilisez `ROLE_INTEGRATIONADMIN`.

### Gérer la connexion après l’avoir créée

Vous pouvez utiliser les appels suivants avec l’ID de connexion :

| Objectif | Appeler |
|---|---|
| Activation ou désactivation d’une connexion | `POST /ctr/xtsas/{connectionId}/enable` |
| Lire la liste d’accès d’une connexion | `GET /ctr/xtsa/{connectionId}/access` |
| Accès en lecture pour toutes les connexions Zoom | `GET /ctr/xtsas/access?UUID=20012` |
| Répertoriez toutes les connexions. Les connexions Zoom ont `extsysRefId` 25. | `GET /ctr/xtsas` |
| Afficher une connexion | `GET /ctr/app/connection/{id}/object/10002` |
| Suppression définitive d’une connexion | `DELETE /ctr/xtsas/{id}` |

>[!NOTE]
>
>L&#39;appel d&#39;affichage renvoie le secret client en texte clair. Traitez le secret du client comme étant sensible et faites-le pivoter s’il est exposé. Ne validez pas et ne partagez pas les cookies de session, les jetons CSRF ou les informations d’identification, y compris dans les fichiers HAR et les commandes cURL copiées.

### Utiliser ces API dans votre intégration

La configuration automatisée d’un connecteur Zoom pour un nouveau compte ou partenaire est un cas d’utilisation courant.

1. Appelez `GET /ctr/xtsas/canCreateAccount/25` pour confirmer que vous pouvez créer une autre connexion.
2. Appelez `POST /ctr/authcred/uuid/20012` avec les informations d&#39;identification du zoom.
3. Appelez `POST /ctr/app/esconnect` avec le nom de connecteur, la même chaîne d&#39;informations d&#39;identification et la planification de la synchronisation. Lisez l’ID de connexion de la réponse.
4. Appelez `PUT /ctr/xtsa/{connectionId}/access` avec les groupes d&#39;utilisateurs et les rôles personnalisés qui peuvent utiliser la connexion.
5. Appelez `POST /ctr/xtsas/{connectionId}/enable` avec `val` défini sur `true` ou `false` pour activer ou désactiver la connexion. Appelez ensuite `GET /ctr/xtsas` et vérifiez l&#39;indicateur `enabled` pour confirmer l&#39;état.
6. Pour modifier les informations d’identification ultérieurement, répétez les étapes 2 et 3 avec l’ID de connexion.


