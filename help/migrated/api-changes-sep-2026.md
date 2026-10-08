---
description: Points d’entrée API publics destinés aux élèves pour la liste, la récupération, l’inscription et la suppression de parcours d’apprentissage personnalisés dans Adobe Learning Manager et points d’entrée API pour vérifier si un ou plusieurs objets d’apprentissage sont directement accessibles à un élève donné via un catalogue qui lui est attribué.
jcr-language: en_us
title: Modifications d’API en septembre 2026
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1374'
ht-degree: 3%
---

# Modifications apportées aux API dans la version de septembre 2026 de Adobe Learning Manager

## API de vérification de l’accès au catalogue pour les objets d’apprentissage

Déterminez si l’élève actuel a un accès direct au catalogue à un ou plusieurs objets d’apprentissage, indépendamment du fait qu’il ait atteint ce contenu via un parcours d’apprentissage ou une certification.

### Objectif de l’API

Lorsqu’un élève ouvre un parcours d’apprentissage ou une certification, il peut parcourir les cours individuels qu’il contient, même si un cours spécifique ne lui est pas directement attribué par le biais d’un catalogue. Cela prend en charge la découverte de contenu : les élèves peuvent explorer ce que contient un parcours d’apprentissage avant de décider de le poursuivre ou non.

Cependant, le fait de pouvoir afficher un cours de cette manière ne devrait pas signifier automatiquement que l’élève peut s’y inscrire. L’inscription doit dépendre de l’accès direct ou non de l’élève au catalogue de ce cours spécifique, et pas seulement un accès indirect via un parcours d’apprentissage conteneur.

Cette API vous permet de vérifier, pour un élève donné, si un ou plusieurs objets d&#39;apprentissage sont directement accessibles via un catalogue qui leur est attribué. Utilisez le résultat pour contrôler l&#39;interface utilisateur liée à l&#39;inscription, par exemple, en affichant une option d&#39;inscription uniquement lorsque l&#39;accès direct au catalogue est confirmé, tout en conservant la page du cours elle-même visible dans les deux cas.

### Point de terminaison

`GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs`

| Propriété | Valeur |
|---|---|
| **Portée** | Accès en lecture de l’élève |
| **Format de réponse** | application/vnd.api+json |

### Paramètres de requête

| Paramètre | Obligatoire | Type | Description |
|---|---|---|---|
| id | Oui | chaîne ou tableau | Un ou plusieurs ID d&#39;objets d&#39;apprentissage à vérifier. Accepte un ID unique ou une liste séparée par des virgules. Maximum de 10 ID par demande. |

### Exemple de requête

```
GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs?ids=course%3A2400159%2Ccourse%3A2400160%2Ccourse%3A2400161%2Ccourse%3A2400162
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

>[!NOTE]
>
>Les ID des objets d&#39;apprentissage doivent être codés en URL. Le signe deux-points d&#39;un ID tel que course:2400159 est codé en %3A et la virgule séparant plusieurs ID est codée en %2C.

### Exemple de réponse - 200 OK

```json
{
  "course:2400162": false,
  "course:2400161": false,
  "course:2400160": true,
  "course:2400159": true
}
```

| Valeur | Signification |
|---|---|
| vrai | L&#39;élève appelant a un accès direct au catalogue de cet objet d&#39;apprentissage. |
| faux | L’objet d’apprentissage n’est pas directement disponible pour l’élève appelant via un catalogue. L’élève peut toujours être en mesure de l’afficher s’il est accessible via un parcours d’apprentissage ou une certification auxquels il a accès. |

### Codes de réponse

| Statut | Signification |
|---|---|
| 200 | La demande a réussi. La réponse contient un résultat pour chaque ID demandé. |
| 400 | Erreur générique de requête incorrecte. Par exemple, plus de 10 identifiants ont été fournis ou un identifiant a été mal formé. |
| 401 | Il manque des informations d&#39;identification valides à la demande ou l&#39;accès a été refusé en raison d&#39;informations d&#39;identification non valides. |

### Exemple de réponse d’erreur

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "Either LO id is blank or not as per public api specification"
  }
}
```

### Utiliser cette API dans votre intégration

Un cas d’utilisation courant est une page de cours accessible par un élève en naviguant à partir d’un parcours d’apprentissage. Vous souhaitez que la page du cours elle-même reste accessible pour la découverte, tout en affichant l&#39;action **S&#39;inscrire** uniquement si l&#39;élève a un accès direct au catalogue de ce cours.

1. Lorsque la page du cours se charge, appelez ce point de terminaison avec l&#39;ID de l&#39;objet d&#39;apprentissage du cours.
2. Si la réponse renvoie la valeur true pour cet ID, affichez l&#39;option **S&#39;inscrire**.
3. Si la réponse renvoie la valeur false, conservez la page du cours visible, le titre, la description et les détails du cours, mais masquez l&#39;option **S&#39;inscrire**.

## API de tâche pour le rapport de piste d’audit d’administrateur {#apiaudittrailreport}

### Objectif de l’API

Le rapport de piste d’audit de l’administrateur répertorie les modifications de configuration apportées à un
Compte Adobe Learning Manager. Par exemple, les modifications apportées aux notions de base, aux intégrations ou
Paramètres de compte avancés sur une période donnée. La génération du rapport de journal d’audit nécessite l’interrogation et l’agrégation des enregistrements de modification de configuration dans la plage de dates et les types de paramètres demandés. Selon la taille de la plage et le volume des modifications, cela peut dépasser les limites de temps d&#39;une requête HTTP synchrone, ce qui risque de provoquer des dépassements de délai du client ou de la passerelle.

Pour éviter cela, le rapport est généré de manière asynchrone via l’API de tâche générique :

1. **Créer un emploi.** L’administrateur soumet une demande en spécifiant le type de rapport, la plage de dates et les types de paramètres. L’API renvoie immédiatement un ID de tâche, sans attendre la compilation du rapport.

2. **Interrogation du travail.** L’administrateur récupère régulièrement le travail à l’aide de son ID pour vérifier son statut. Une fois la tâche terminée, la réponse contient le résultat ou une référence à celui-ci.

### URL de base et conventions

| Élément | Valeur |
|---|---|
| Chemin de base | `/primeapi/v2` |
| Type de contenu | `application/vnd.api+json;charset=UTF-8` (JSON:API) |
| Authentification | Jeton OAuth au porteur, portée d’un administrateur de compte |
| Contexte du compte | En-tête `x-acap-account` identifiant le compte de l&#39;administrateur appelant |
| Sondage | Aucun intervalle fixe n&#39;est appliqué ; interrogez le point de terminaison Obtenir le statut de la tâche jusqu&#39;à ce que `status` ne soit plus `QUEUED` ou `IN_PROGRESS` |

### ID

La tâche `id` renvoyée lors de la création d&#39;une tâche est une chaîne opaque (par exemple,
`4593`). Toujours transmettre la valeur `id` exacte que vous avez reçue de la création
réponse lors de l’interrogation du statut. Ne le construisez jamais ni ne l’analysez.

### Portées d’authentification

Chaque point de terminaison nécessite un jeton OAuth portant l’étendue suivante, et la
l’utilisateur appelant doit détenir le rôle d’administrateur de compte :

- `admin:write` créer une tâche de rapport (`ROLE_ADMIN` requis)
- `admin:read` a lu l&#39;état et le résultat d&#39;une tâche (`ROLE_ADMIN` requis)

Les demandes effectuées par un appelant qui ne détient pas `ROLE_ADMIN` sur le compte sont les suivantes :
rejeté ; voir [Gestion des erreurs](/help/migrated/api-changes-sep-2026.md#error-handling)

### Points de terminaison

#### Création d’une tâche de rapport de piste d’audit

`POST /primeapi/v2/jobs`

Crée une tâche asynchrone qui génère un rapport de journal d&#39;audit de modification de configuration
pour la plage de dates et les types de paramètres donnés. La réponse revient immédiatement
avec une ressource de tâche dans l&#39;état `QUEUED` ; le rapport lui-même est produit dans le
arrière-plan.

Portée : `admin:write`

| Paramètre | Dans | Obligatoire | Description |
|---|---|---|---|
| `jobType` | corps | Oui | Doit être `generateConfigChangeAuditReport` pour ce rapport |
| `payload.fromDate` | corps | Oui | Début de la fenêtre de rapport, ISO-8601 avec décalage, par exemple `2026-09-15T00:00:00.000+05:30` |
| `payload.toDate` | corps | Oui | Fin de la fenêtre de rapport, ISO-8601 avec décalage, par exemple `2026-09-23T23:59:59.000+05:30` |
| `payload.settingTypes` | corps | Oui | Tableau d&#39;une ou plusieurs catégories de paramètres à inclure ; les valeurs prises en charge sont `Basics`, `Integrations` et `Advanced` |

Exemple de corps de requête

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "payload": {
        "fromDate": "2026-09-15T00:00:00.000+05:30",
        "toDate": "2026-09-23T23:59:59.000+05:30",
        "settingTypes": ["Basics", "Integrations", "Advanced"]
      }
    }
  }
}
```

Réponse : `202 Created`. Le corps de la réponse est la ressource de travail dans sa version initiale
État `QUEUED`.

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "QUEUED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

>[!NOTE]
>
>Une fenêtre `fromDate`/`toDate` qui s&#39;étend sur une très grande plage de dates, ou que
>demande tous les types de paramètres pour un compte avec un long historique des modifications, peut
>le traitement prend plus de temps. Interrogation du point de terminaison Obtenir le statut de la tâche plutôt que
>en supposant que le rapport est prêt après un délai déterminé.

#### Obtenir le statut d’une tâche de rapport de piste d’audit

`GET /primeapi/v2/jobs/{id}`

Renvoie l’état actuel d’une tâche créée précédemment. Tant que le travail est
en cours d&#39;exécution, `attributes.status` est `QUEUED` ou `IN_PROGRESS` et
`attributes.result` est absent. Une fois le travail terminé, `attributes.status` est
soit `COMPLETED`, avec l&#39;emplacement du rapport dans `attributes.result`,
`FAILED`, avec détails d&#39;échec dans `attributes.error`.

Portée : `admin:read`

| Paramètre | Dans | Obligatoire | Description |
|---|---|---|---|
| `id` | chemin | Oui | ID de tâche renvoyé lors de la création de la tâche |

Exemple de réponse pendant l’exécution de la tâche

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "IN_PROGRESS",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

Exemple de réponse une fois la tâche terminée

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "COMPLETED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30",
      "dateCompleted": "2026-09-23T18:12:41.000+05:30",
      "result": {
        "downloadUrl": "https://learningmanager.adobe.com/primeapi/v2/jobs/4593/download",
        "expiresAt": "2026-09-24T18:12:41.000+05:30"
      }
    }
  }
}
```

### Schéma de la ressource

#### Attributs de la tâche

| Champ | Type | Description |
|---|---|---|
| `id` | chaîne | ID de tâche opaque |
| `jobType` | chaîne | `generateConfigChangeAuditReport` pour ce rapport |
| `status` | chaîne | `QUEUED`, `IN_PROGRESS`, `COMPLETED` ou `FAILED` |
| `dateCreated` | chaîne (ISO-8601) | Date de création de la tâche |
| `dateCompleted` | chaîne (ISO-8601) | Une fois le travail terminé, présenter une fois `status` est `COMPLETED` ou `FAILED` |
| `payload` | objet | Paramètres de requête avec lesquels la tâche a été créée (incorporés, voir ci-dessous) |
| `result` | objet | Où télécharger le rapport terminé ; présent uniquement lorsque `status` est `COMPLETED` (intégré - voir ci-dessous) |
| `error` | objet | Détails de l&#39;échec ; présents uniquement lorsque `status` est `FAILED` |

#### Charge utile (intégrée, dans la demande de création)

| Champ | Description |
|---|---|
| `fromDate` | Au début de la fenêtre de rapport |
| `toDate` | Fin de la fenêtre de rapport |
| `settingTypes` | Définition des catégories incluses dans le rapport : `Basics`, `Integrations`, `Advanced` |

#### Résultat (incorporé, dans une tâche terminée)

| Champ | Description |
|---|---|
| `downloadUrl` | URL signée à partir de laquelle le rapport généré peut être téléchargé |
| `expiresAt` | Lorsque `downloadUrl` cesse d&#39;être valide, demandez une nouvelle vérification de l&#39;état pour obtenir un nouveau lien après cette heure |

### Gestion des erreurs {#audit-trail-report-error-handling}

Les codes suivants s’appliquent à ces points de terminaison :

| état HTTP | Code d’erreur | Quand cela se produit |
|---|---|---|
| 400 | `BAD_REQUEST` | `toDate` est antérieur à `fromDate`, `settingTypes` est vide ou contient une valeur non prise en charge, ou une date n&#39;est pas valide selon la norme ISO-8601 - Créer un point de terminaison uniquement |
| 401 | `UNAUTHORIZED_ACCESS` | Le jeton est manquant, non valide ou expiré |
| 403 | `FORBIDDEN` | L&#39;appelant ne détient pas `ROLE_ADMIN` sur le compte |
| 400 | `OBJECT_DOESNT_EXIST` | Get by id : le travail n&#39;existe pas ou l&#39;identifiant est incorrect. Les deux cas sont regroupés dans la même réponse |

Exemple de réponse d’erreur

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "toDate must be on or after fromDate"
  }
}
```

### Utiliser cette API dans votre intégration

Un cas d’utilisation courant est une action « Télécharger la piste d’audit » destinée aux administrateurs dans le
écran paramètres du compte.

1. Lorsque l’administrateur sélectionne une plage de dates et un ou plusieurs types de paramètres et
confirme, appelez le point de terminaison create-job avec ces valeurs.
2. Stockez la tâche renvoyée `id` et interrogez le point de terminaison Obtenir le statut de la tâche à un
intervalle raisonnable (par exemple, toutes les quelques secondes).
3. Tant que `status` est `QUEUED` ou `IN_PROGRESS`, continuez à afficher un état de progression
dans l’interface utilisateur.
4. Lorsque `status` devient `COMPLETED`, utilisez `result.downloadUrl` pour laisser le
l&#39;administrateur télécharge le rapport avant le passage de `expiresAt`.
5. Lorsque `status` devient `FAILED`, faites défiler `error` vers l&#39;administrateur et laissez-le
réessayez.
