---
description: Modifications d’API dans ALM
jcr-language: en_us
title: Modifications apportées aux API dans la version d’août 2026 de Adobe Learning Manager
source-git-commit: 857c94b5e9a7460d63a6dacc0beeddd41f362bf9
workflow-type: tm+mt
source-wordcount: '3354'
ht-degree: 3%

---


# Modifications apportées aux API dans la version d’août 2026 de Adobe Learning Manager

## API d’administration des groupes d’utilisateurs dans Adobe Learning Manager

Cette version ajoute trois nouveaux points d’entrée API publics de portée administrateur pour gérer par programme des groupes d’utilisateurs personnalisés. Vous pouvez créer, renommer et supprimer des groupes d’utilisateurs personnalisés sans utiliser l’application d’administration, ce qui vous permet d’automatiser la gestion des groupes dans le cadre de vos workflows d’identité ou d’approvisionnement.

Ces points de terminaison fonctionnent uniquement avec des groupes d’utilisateurs personnalisés. Les groupes gérés par le système, tels que le groupe Tous les utilisateurs et les groupes d’utilisateurs générés automatiquement, ont la valeur readOnly : true dans la réponse de l’API et ne peuvent pas être modifiés ou supprimés via ces points de terminaison.

Pour connaître les exigences d&#39;authentification d&#39;API, voir [Authentification d&#39;API Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Groupes d’utilisateurs points de terminaison d’API

Les trois points de terminaison nécessitent un jeton d’accès administrateur avec des autorisations d’écriture (ROLE_ADMIN).

| **Méthode** | **Chemin** | **Opération** | **Code de réussite** |
|---|---|---|---|
| POST | /primeapi/v2/userGroups | Création d’un groupe d’utilisateurs personnalisé | 201 Créés |
| PUT | /primeapi/v2/userGroups/{id} | Mise à jour du nom ou de la description d’un groupe | 200 OK |
| DELETE | /primeapi/v2/userGroups/{id} | Suppression d’un groupe d’utilisateurs personnalisé | 204 Aucun contenu |

## **En-têtes de demande courants**

Les trois points de terminaison nécessitent les en-têtes suivants.

```
Authorization: Bearer \<access-token\>
X-acap-user: \<user-id\>
X-acap-account: \<account-id\>
X-acap-caller-role: ROLE_ADMIN
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

### **Créer un groupe d&#39;utilisateurs**

```
POST /primeapi/v2/userGroups
```

Crée un nouveau groupe d&#39;utilisateurs personnalisé avec une liste initiale de membres. Le groupe est immédiatement disponible dans l’application d’administration.

#### **Corps de la demande**

```
{
  "name": "Marketing Team",
  "description": "Custom user group for marketing onboarding",
  "data": [
    { "type": "user", "id": "11282373" },
    { "type": "user", "id": "11282374" }
  ]
}
```

#### **Paramètres de demande**

| **Paramètre** | **Requis** | **Type** | **Description** |
|---------------|--------------|----------|-------------------------------------------------------------------------------------|
| name | Oui | chaîne | Nom complet du groupe. Ne doit pas être vide ni contenir uniquement des espaces. |
| description | Non | chaîne | Description facultative de l’objectif du groupe. |
| data | Oui | tableau | Liste initiale des membres. 1 élément minimum, 100 éléments maximum. |
| data[].type | Oui | chaîne | Doit être « utilisateur ». Aucun autre type de ressource n’est accepté. |
| data[].id | Oui | chaîne | Chaîne d’ID utilisateur numérique. L’utilisateur doit appartenir au compte et avoir le statut ACTIF. |

> **Remarque :** le tableau de données est utilisé uniquement lors de la création pour définir la liste de membres initiale. Pour ajouter ou supprimer des membres après la création, utilisez les points de terminaison d’appartenance de groupe d’utilisateurs existants.

#### **Réponse 201 Créée**

```
{
  "links": {
    "self": "https://<host>/primeapi/v2/userGroups"
  },
  "data": {
    "id": "2769204",
    "type": "userGroup",
    "attributes": {
      "dateCreated": "2026-06-04T14:19:53.000Z",
      "description": "Custom user group for marketing onboarding",
      "name": "Marketing Team",
      "readOnly": false,
      "userCount": 2
    }
  }
}
```

#### **Mot de POST des règles de validation**

| **#** | **Validation** | **Code d&#39;erreur** | **Déclencher** |
|-------|-------------------------------------------------------|----------------------------------------------------------|------------------------------------------------|
| 1 | nom présent et non vide | USERGROUP_CREATE_NAME_REQUIRED | Nom omis ou espace blanc uniquement |
| 2 | les données contiennent au moins 1 utilisateur | USERGROUP_CREATE_USERS_REQUIRED | tableau de données absentes ou vides |
| 3 | les données contiennent 100 utilisateurs ou moins | USERGROUP_USERS_MAX_LIMIT_EXCEEDED | Plus de 100 entrées dans les données[] |
| 4 | Tous les ID utilisateur sont des chaînes numériques | INVALID_USER_IDS | Chaîne non numérique trouvée dans data[].id |
| 5 | Tous les utilisateurs existent dans le compte et ont le statut ACTIF | INVALID_USER_IDS / USERGROUP_CREATE_USERS_NOT_IN_ACCOUNT | Utilisateur introuvable ou inactif |
| 6 | Le compte n’a pas atteint la limite de groupes personnalisés | 400 | Limite de niveau compte dépassée pour les groupes personnalisés |

### **Mettre à jour un groupe d&#39;utilisateurs**

```
PUT /primeapi/v2/userGroups/{id}
```

Met à jour le nom et/ou la description d’un groupe d’utilisateurs personnalisé existant. Ce point de terminaison ne peut pas ajouter ou supprimer des membres du groupe.

L’un ou l’autre champ peut être omis ; l’omission d’un champ ne modifie pas sa valeur actuelle. La transmission de la valeur NULL pour la description efface ce champ. La transmission d’une chaîne vide pour le nom est rejetée.

#### **Corps de la demande**

```json
{
  "name": "Updated Group Name",
  "description": "Updated description text"
}
```

#### **Paramètres de demande**

| **Paramètre** | **Requis** | **Type** | **Description** |
|---------------|--------------|----------|---------------------------------------------------------------------------|
| name | Oui | chaîne | Nouveau nom d’affichage. Ne doit pas être vide s’il est fourni. Ne rien modifier. |
| description | Non | chaîne | Nouvelle description. Transmettez la valeur NULL à effacer. Ne rien modifier. |

#### **Réponse 200 OK**

```
{
  "data": {
    "type": "userGroup",
    "id": "2767870",
    "attributes": {
      "name": "Updated Group Name",
      "description": "Updated description text",
      "readOnly": false,
      "state": "Active",
      "userCount": 3
    }
  }
}
```

#### **Mot de PUT des règles de validation**

| **#** | **Validation** | **Code d&#39;erreur** | **Déclencher** |
|-------|-------------------------------------|----------------------------------------|----------------------------------------------------------|
| 1 | les données sont nulles ou absentes | USERGROUP_UPDATE_USERS_NOT_ALLOWED | Données non nulles transmises par l&#39;appelant lors de la tentative de modification de l&#39;appartenance |
| 2 | le nom, s’il est fourni, n’est pas vide | USERGROUP_UPDATE_NAME_BLANK | nom envoyé en tant que chaîne contenant uniquement des espaces |
| 3 | Le groupe existe dans ce compte | INVALID_USER_GROUP_ID | Paramètre de chemin {id} inconnu |
| 4 | Le groupe n’est pas déjà supprimé | DELETED_USERGROUP | Le groupe a été précédemment supprimé |
| 5 | La lecture seule du groupe est false. | READ_ONLY_USERGROUP | Groupe géré par le système |
| 6 | Le groupe est un type personnalisé (non système). | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Type de groupe interne au système |

### **Supprimer un groupe d&#39;utilisateurs**

```
DELETE /primeapi/v2/userGroups/{id}
```

Marque le groupe d’utilisateurs personnalisé spécifié comme supprimé. L’enregistrement de groupe n’est pas définitivement supprimé : son état est défini sur SUPPRIMÉ, ce qui le rend invisible dans l’application d’administration et inéligible pour une utilisation dans les nouvelles configurations. Impossible de réutiliser l’ID de groupe.

#### **Exemple de demande**

```
DELETE /primeapi/v2/userGroups/2767870
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_ADMIN
```

#### **Réponse 204 Aucun Contenu**

Le corps de la réponse est vide.

> **Remarque :** le DELETE n&#39;est pas idempotent. L’envoi d’une deuxième demande de DELETE au même ID de groupe renvoie une erreur 400 avec le code DELETED_USERGROUP — et non 204. Considérez une réponse 400 DELETED_USERGROUP comme une confirmation que le groupe est déjà supprimé. La suppression en bloc n’est pas prise en charge ; chaque groupe nécessite une demande de DELETE distincte.

#### **Mot de DELETE des règles de validation**

| **#** | **Validation** | **Code d&#39;erreur** | **Déclencher** |
|-------|-------------------------------------|----------------------------------------|---------------------------------------------------|
| 1 | Le groupe existe dans ce compte | INVALID_USER_GROUP_ID | Paramètre de chemin {id} inconnu |
| 2 | Le groupe n’est pas déjà supprimé | DELETED_USERGROUP | Répéter le DELETE sur un groupe déjà dans l&#39;état DELETED |
| 3 | La lecture seule du groupe est false. | READ_ONLY_USERGROUP | Groupe géré par le système |
| 4 | Le groupe est un type personnalisé (non système). | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Type de groupe interne au système |

## API d’apprentissage externe dans Adobe Learning Manager

Cette version ajoute cinq nouveaux points d’entrée API de portée élève pour la fonctionnalité Apprentissage externe. Ces points de terminaison permettent aux élèves de créer, récupérer et mettre à jour des envois d&#39;apprentissage externes par programme, par exemple, à partir d&#39;une application mobile, d&#39;un système de RH intégré ou d&#39;un portail d&#39;apprentissage personnalisé.

Le workflow d’apprentissage externe via l’API reflète le workflow dans l’application de l’élève : un élève soumet les détails de la formation et un document de preuve facultatif, son responsable direct reçoit une notification pour examiner la soumission et, lors de l’approbation, l’enregistrement apparaît dans le relevé de notes de l’élève.

Les cinq points d’entrée ont une portée d’élève. Un élève ne peut accéder qu’à ses propres envois : l’API renvoie une erreur si un élève tente d’accéder aux données d’un autre élève.

Pour connaître les exigences d&#39;authentification d&#39;API, voir [Authentification d&#39;API Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Points de terminaison d’API d’apprentissage externe

Tous les points de terminaison nécessitent un jeton d’accès d’élève (ROLE_LEARNER).

| **Méthode** | **Chemin** | **Opération** | **Code de réussite** |
|------------|---------------------------------------|----------------------------------|------------------|
| GET | /primeapi/v2/externalLearningSettings | Récupérer la configuration du formulaire de compte | 200 OK |
| GET | /primeapi/v2/externalLearnings | Répertorier les envois de l&#39;appelant | 200 OK |
| GET | /primeapi/v2/externalLearnings/{id} | Récupérer une seule soumission | 200 OK |
| POST | /primeapi/v2/externalLearnings | Créer une nouvelle soumission | 201 Créés |
| PUT | /primeapi/v2/externalLearnings/{id} | Mise à jour d’une soumission en attente | 200 OK |

### En-têtes de requête courants

```
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_LEARNER
Accept: application/vnd.api+json
Content-Type: application/vnd.api+json (POST and PUT only)
```

### Cycle de vie du statut de la soumission

| **Statut** | **Définir par** | **Signification** | **L’élève peut-il effectuer la mise à jour ?** |
|------------|------------------|-----------------------------------------|-----------------------------|
| EN ATTENTE | Système lors de la création | En attente de révision par le responsable | Oui, par PUT |
| APPROUVÉ | Responsable | Accepté ; apparaît dans le relevé de notes de l’élève | Non - Retours PUT 409 |
| REJETÉ | Responsable | Refusé ; commentaire de révision joint | Non : créer une nouvelle soumission |

APPROUVÉ et REJETÉ sont des états finaux. Une soumission rejetée ne peut pas être rouverte ; l’élève doit créer une nouvelle soumission.

### Récupérer la configuration du formulaire de compte

```
GET /primeapi/v2/externalLearningSettings
```

Renvoie la configuration du formulaire au niveau du compte. Appelez ce point de terminaison avant de rendre un formulaire d’envoi. La réponse définit les champs à afficher, ceux qui sont obligatoires, leurs types de données et tous les champs personnalisés configurés par l’administrateur.

Vérifiez l’attribut activé de niveau supérieur avant de continuer. Si la valeur est false, la fonctionnalité Apprentissage externe n’est pas active pour ce compte et les points d’entrée d’envoi renvoient des erreurs.

#### Réponse 200 OK

```
{
  "data": {
    "id": "8627",
    "type": "externalLearningSettings",
    "attributes": {
      "enabled": true,
      "updatedAt": "2026-06-05T06:51:20.000Z",
      "coreFields": [
        { "id": "title", "type": "TEXT", "mandatory": true, "editable": false, "order": 0 },
        { "id": "description_notes", "type": "TEXT", "mandatory": false, "editable": true, "order": 1 },
        { "id": "date", "type": "TIMESTAMP", "mandatory": false, "editable": true, "order": 2 },
        { "id": "score", "type": "NUMBER", "mandatory": true, "editable": true, "order": 3 },
        { "id": "duration", "type": "TEXT", "mandatory": false, "editable": true, "order": 4 },
        { "id": "attachments", "type": "FILE_UPLOAD", "mandatory": true, "editable": true, "order": 5 }
      ],
      "customFields": [
        {
          "id": "960369b2-...",
          "type": "NUMBER",
          "mandatory": true,
          "order": 0,
          "label": { "en_US": "Employee Code" }
        },
        {
          "id": "3c6cc6d9-...",
          "type": "DROPDOWN",
          "mandatory": true,
          "order": 1,
          "label": { "en_US": "Department" },
          "options": [
            { "option_id": "opt_1", "label": { "en_US": "IT" } },
            { "option_id": "opt_2", "label": { "en_US": "HR" } },
            { "option_id": "opt_3", "label": { "en_US": "FIN" } }
          ]
        }
      ]
    }
  }
}
```

#### Référence du champ de base

| **ID de champ** | **Type** | **Valeur par défaut obligatoire** | **Notes** |
|-------------------|-------------|-----------------------|----------------------------------------------------------------------------------------------------------|
| titre | TEXTE | Oui | Nom de la formation. Toujours présent. Ne peut pas être désactivé par l&#39;administrateur. |
| description_notes | TEXTE | Non | Description ou notes en texte libre. |
| l’annonce | HORODATAGE | Non | Plage de dates. Valeur shape : { « start_date » : « <ISO-Z> », « end_date » : « <ISO-Z>&quot; }. Les deux valeurs peuvent être Null. |
| score | NOMBRE | Oui | Forme de la valeur : { « completed_score » : <number>, « max_score » : <number> }. Les deux valeurs doivent être numériques. |
| durée | TEXTE | Non | Chaîne libre, par exemple « 40 hours ». |
| pièces jointes | FILE_UPLOAD | Oui | Preuve d’accomplissement. **Non** transmis dans les champs[] — utilisez plutôt l&#39;attribut submissionUrl de niveau supérieur. |

Les champs personnalisés sont définis par l&#39;administrateur et renvoyés dans customFields[]. Leurs ID, types, indicateurs obligatoires, étiquettes et options de liste déroulante varient selon la configuration du compte.

### Lister les soumissions

```
GET /primeapi/v2/externalLearnings
```

Renvoie une liste paginée des propres envois de l’élève authentifié, triés par ordre décroissant (modifié en dernier).

#### **Paramètres de requête**

| **Paramètre** | **Par défaut** | **Maximum** | **Description** |
|---------------|-------------|-------------|-------------------------------------------------------------------------------------------------------|
| page[offset] | 0 | 5000 | Décalage d’enregistrement de base zéro. |
| page[limit] | 10 | 100 | Enregistrements par page. Les valeurs supérieures à 100 sont serrées silencieusement sur 100. |
| ls_qp_status | — | — | Filtrer par statut. Omettre pour tous les résultats. Valeurs valides : PENDING, APPROVED, REJECTED (non sensible à la casse). |

#### **Réponse 200 OK**

```
{
  "links": {
    "next": "/primeapi/v2/externalLearnings?page[offset]=10&page[limit]=10"
  },
  "data": [
    { "id": "1001", "type": "externalLearning", "attributes": { "status": "PENDING", ... } },
    { "id": "1002", "type": "externalLearning", "attributes": { "status": "APPROVED", ... } }
  ]
}
```

### Récupérer une soumission

```
GET /primeapi/v2/externalLearnings/{id}
```

Renvoie l’enregistrement complet d’une seule soumission appartenant à l’élève authentifié.

#### **Réponse 200 OK

```
{
  "data": {
    "id": "1001",
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "https://<cdn-url>/cert.pdf",
      "title": "Java Fundamentals Certification",
      "status": "PENDING",
      "creationSource": "LEARNER",
      "createdAt": "2026-04-14T08:30:00.000Z",
      "modifiedAt": "2026-04-16T11:45:00.000Z",
      "fields": [ "...resolved against live settings..." ]
    },
    "relationships": {
      "reviewerUser": { "data": null }
    }
  }
}
```

### Création d’une soumission

```
POST /primeapi/v2/externalLearnings
```

Crée une nouvelle soumission d’apprentissage externe à l’état EN ATTENTE. Tous les champs obligatoires définis dans les paramètres du compte doivent être inclus. Après la réussite d’un POST, le responsable de l’élève reçoit une notification sur la plateforme pour examiner l’envoi.

### **Chargement de fichier**

Le champ Pièces jointes est traité séparément des autres champs. Ne l&#39;incluez pas dans les champs[]. Au lieu de cela :

&#x200B;1. Obtenez une URL de téléchargement S3 présignée à partir du point de terminaison de téléchargement de fichiers ALM.

&#x200B;2. Chargez le fichier sur cette URL.

&#x200B;3. Transmettez l’URL obtenue en tant qu’attribut submissionUrl de niveau supérieur dans votre demande de POST.

#### **Corps de la demande**

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<pre-signed-upload-url>",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals Certification" },
        { "id": "description_notes", "type": "TEXT", "value": "Completed via online course platform." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": "2026-05-01T00:00:00.000Z", "end_date": "2026-05-15T00:00:00.000Z" } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 88, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "40 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1225" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_3" }
      ]
    }
  }
}
```

#### Formes de valeur de champ

| **Type de champ** | **Forme de la valeur** | **Exemple** |
|----------------|---------------------------------------------------------|----------------------------------------------------------------|
| TEXTE | String | « Principes de base de Java » |
| NOMBRE | Objet avec score_atteint et score_max | { « completed_score » : 88, « max_score » : 100 } |
| HORODATAGE | Objet avec date_début et date_fin (ISO 8601 ou null) | { « start_date » : « 2026-05-01T00:00:00.000Z », « end_date » : null } |
| LISTE DÉROULANTE | chaîne option_id des paramètres du compte | « opt_3 » |
| FILE_UPLOAD | Non autorisé dans les champs[] — utilisez submissionUrl | — |

#### Mot de POST des règles de validation

| **#** | **Validation** | **Déclencher** |
|-------|-----------------------------------------------------------------|----------------------------------------------------------|
| 1 | L’apprentissage externe est activé pour le compte | Indicateur de fonctionnalité désactivé |
| 2 | Tous les champs obligatoires sont présents dans les champs[] | Champ obligatoire omis |
| 3 | Chaque forme d’ID, de type et de valeur de champ correspond aux paramètres du compte | Type incorrect ou objet de valeur mal formé |
| 4 | Type FILE_UPLOAD absent dans les champs[] | Pièce jointe envoyée dans les champs [] au lieu de submissionUrl |
| 5 | submissionUrl est une URL présignée S3 valide | URL CDN et URL non-S3 rejetées au moment de la création |
| 6 | submissionUrl présente lorsque attachments.mandatory a la valeur true | Les pièces jointes sont requises, mais l&#39;URL de soumission est manquante |

### Mise à jour d’une soumission

```
PUT /primeapi/v2/externalLearnings/{id}
```

Met à jour une soumission EN ATTENTE existante. Seules les soumissions EN ATTENTE peuvent être mises à jour. Tenter de mettre en PUT une soumission APPROUVÉE ou REJETÉE renvoie une erreur 409.

**Ce point de terminaison utilise la sémantique de remplacement complet.** Fournissez le tableau de champs [] complet dans chaque demande de PUT, pas seulement les champs que vous modifiez. Les champs omis du tableau sont effacés.

#### Champs que l’élève peut mettre à jour

| **Champ/attribut** | **L’élève peut effectuer la mise à jour** | **Notes** |
|-----------------------|------------------------|----------------------------------------------------------------------------|
| champs[] | Oui | Remplacement complet : incluez tous les champs, pas seulement les champs modifiés |
| submissionUrl | Oui | Les URL CDN sont acceptées dans le PUT ; les URL présignées S3 sont requises uniquement dans le POST |
| reviewerUserId | Non | Défini par action du responsable ; en lecture seule pour l’élève |
| reviewedAt | Non | Défini par action du responsable ; en lecture seule pour l’élève |
| reviewerComment | Non | Défini par action du responsable ; en lecture seule pour l’élève |
| l&#39;état | Non | Contrôlé par le responsable : EN ATTENTE → APPROUVÉ ou REJETÉ |
| creationSource | Non | Envois créés par l’API Always LEARNER |
| createdAt | Non | Défini à la création ; immuable |

#### Corps de la demande

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<cdn-url>/cert-v2.pdf",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals — Updated" },
        { "id": "description_notes", "type": "TEXT", "value": "Updated notes." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": null, "end_date": null } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 92, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "42 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1227" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_2" }
      ]
    }
  }
}
```

## API pour ID de certification pertinent pour l’élève et ID de certification racine dans LT

Lorsqu&#39;une certification récurrente est renouvelée, Adobe Learning Manager crée une nouvelle version de la certification et y inscrit automatiquement les élèves actifs. Si votre intégration demande des données de certification directement plutôt que de compter sur l&#39;expérience de l&#39;élève Adobe Learning Manager, vous pouvez utiliser cette API pour déterminer exactement quelle version d&#39;une certification récurrente est pertinente pour un élève spécifique à tout moment.

### Objectif de l’API

Les certifications récurrentes génèrent un nouvel ID de certification à chaque renouvellement. Dans l’expérience d’élève Adobe Learning Manager native, seule la version adaptée à chaque élève est affichée. Les anciennes versions sont masquées automatiquement lorsqu’un élève passe à une nouvelle version.

Si votre intégration récupère les données de certification indépendamment, par exemple pour afficher les informations de certification sur un portail externe, il se peut qu’elle n’applique pas automatiquement ce filtrage. Sans cela, un élève pourrait voir chaque version historique d’une certification récurrente, y compris celles qui ne le concernent plus, sans indication sur laquelle agir.

Cette API a comblé cette lacune. Étant donné l&#39;ID de certification racine, il renvoie la version de certification spécifique qui s&#39;applique à un élève donné, en tenant compte de son historique d&#39;inscription et de toutes les récurrences.

### Comprendre la périodicité de la certification

Lorsqu’une certification est configurée pour se reproduire, chaque renouvellement crée une nouvelle version de certification avec son propre ID unique. Toutes les versions remontent à un seul **ID de certification racine**, l&#39;ID de la certification d&#39;origine lors de sa création.

Par exemple, une certification qui se répète tous les mois peut produire une séquence de versions dans le temps, où chaque nouvelle version est générée automatiquement lorsque l&#39;intervalle de périodicité est atteint. Les élèves qui sont activement inscrits lorsqu&#39;une périodicité se produit sont automatiquement inscrits à la nouvelle version.

Étant donné que chaque version a un ID distinct, la version pertinente d’un élève dépend de son calendrier d’inscription individuel :

- Un élève qui s&#39;est inscrit avant une périodicité et a terminé sa certification avant la périodicité suivante aura parcouru plusieurs versions au fil du temps.

- Un élève qui s&#39;inscrit au cours d&#39;un cycle de périodicité est inscrit directement dans la version en cours au moment de son inscription.

### Détermination de la version de certification appropriée

Utilisez l&#39;API de version de certification pour identifier la version d&#39;une certification récurrente pertinente pour un élève spécifique.

Fournissez l&#39;**ID de certification racine** comme entrée. L’API évalue l’historique d’inscription de l’élève et renvoie la version appropriée en fonction des règles suivantes :

| **État de l’élève** | **Ce que l&#39;API retourne** |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| L’élève n’est pas encore inscrit à la certification | Dernière version disponible de la certification |
| L’élève est actuellement inscrit | Version spécifique à laquelle l’élève est actuellement inscrit, en tenant compte de toutes les récurrences survenues depuis son inscription initiale |

Cela signifie que deux élèves qui interrogent le même ID de certification racine en même temps peuvent recevoir des résultats différents, en fonction de l&#39;historique d&#39;inscription individuel de chaque élève.

**Remarque** : il peut y avoir une brève fenêtre au cours d&#39;une périodicité, pendant la création de la nouvelle version et la migration des inscriptions, pendant laquelle l&#39;API peut retourner la version qui est sur le point d&#39;être remplacée plutôt que la nouvelle version créée.

**Exemple**

Considérez une certification qui se répète tous les mois, où quatre versions ont été créées au fil du temps en raison de récurrences successives :

- Un élève qui s&#39;est inscrit à la première version et qui a progressé à chaque périodicité à mesure qu&#39;elle se produisait reviendra à la version dans laquelle il est actuellement actif, qui reflète son propre historique d&#39;achèvement et de périodicité, pas nécessairement la toute dernière version qui existe.

- Un élève qui n’est pas encore inscrit du tout reviendra à la version la plus récemment créée, car il s’agit de la version à laquelle les nouvelles inscriptions doivent adhérer.

Cela permet à l’intégration d’orienter toujours un élève vers la version de certification qui le concerne, plutôt que d’afficher chaque version historique ou de deviner laquelle s’applique.

### Référence des API

**Obtenir la certification applicable pour une certification racine**

```
GET /primeapi/v2/learningObjects/{loId}/applicableCertification
```

Résout la version de certification qui s’applique à l’élève actuel, en fonction de l’ID d’une certification racine. Pour les élèves inscrits, cette option renvoie la version dans laquelle ils sont actuellement inscrits. Pour les élèves qui ne sont pas inscrits, cette option renvoie la dernière version active.

| **Propriété** | **Valeur** |
|----------------------------------------------------------|--------------------------|
| **Portée** | Accès en lecture de l’élève |
| **Limite de taux (appels d’élève standard)** | 70 demandes par minute |
| **Limite de taux (identifiants d’API élevés ou de niveau administrateur)** | 500 demandes par heure |
| **Format de réponse** | application/vnd.api+json |

**Remarque** : cette API renvoie des informations de version pour un seul élève à la fois. Elle ne renvoie pas la liste de toutes les versions d’une certification.

**Paramètres de chemin**

| **Paramètre** | **Requis** | **Type** | **Description** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| loId | Oui | chaîne | L’ID de l’objet d’apprentissage, en particulier la certification racine, pour lequel la version applicable est demandée. Ceci est soumis à des autorisations d’accès standard. |

**Paramètres de requête**

| **Paramètre** | **Requis** | **Type** | **Description** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclure | Non | chaîne | Une liste de modèles associés à inclure dans la réponse, séparés par des virgules, en plus de la certification résolue, tels que les sous-objets d’apprentissage ou l’inscription. Utilise la même syntaxe include que les autres points de terminaison d&#39;objets d&#39;apprentissage Adobe Learning Manager. |

**Exemple de requête**

```
GET /primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

```
curl -X GET --header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://<host>/primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs'
```

**Remarque** : la valeur loId doit être codée en URL. Le signe deux-points dans un ID de certification tel que certification:167658 est codé en tant que %3A.

**Exemple de réponse 200 OK**

La réponse utilise la même structure qu’une réponse d’objet d’apprentissage standard, renvoyant la certification résolue.

**Important :** le champ d&#39;ID dans la réponse est l&#39;ID de la certification **résolu**, la version spécifique applicable à cet élève. Il sera généralement différent de l’ID de certification racine que vous avez transmis en tant que loId, puisque l’objectif de cette API est de traduire un ID racine dans la version actuelle correcte.

```
{
  "data": {
    "id": "string",
    "type": "string",
    "attributes": {
      "authorNames": [
        "string"
      ],
      "bannerUrl": "string",
      "catalogs": [
        ...
      ]
    }
  }
}
```

**Codes de réponse**

| **Statut** | **Signification** |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 200 | La certification applicable a été résolue avec succès et est renvoyée en réponse. |
| 400 | Le loId fourni n’est pas une certification ou n’est pas une certification racine. Transmettez l’ID de la certification d’origine, et non une version périodique, en tant que loId. |
| 401 / 403 | Il manque des informations d&#39;identification valides à la demande ou les informations d&#39;identification ne disposent pas de l&#39;accès requis. |
| 404 | Aucune certification active n&#39;a pu être résolue pour cette certification racine. Par exemple, parce que chaque version de la chaîne a été retirée ou supprimée, ou parce que la certification n&#39;a aucune référence de certification racine enregistrée. Un 404 peut également se produire si une version est résolue avec succès, mais que l’élève appelant n’y a pas accès au catalogue. |
| 500 | Une erreur de serveur inattendue s&#39;est produite lors de la résolution de la certification. Relancez la demande. Si l’erreur persiste, contactez le support technique. |

**Exemple de réponse à l&#39;erreur**

```
{
  "meta": {
    "error": "string",
    "detail": "string"
  }
}
```

**Remarque :** cette API résout la version pour un élève par appel. Elle ne renvoie pas la liste de toutes les versions qui existent pour une certification racine.

**Points importants**

- **Certifications non récurrentes : I** si le loId que vous passez est une certification qui n&#39;est pas configurée pour se répéter, l&#39;API renvoie cette certification elle-même.

- **Versions intermédiaires ignorées : I** si l&#39;inscription active d&#39;un élève est passée directement d&#39;une version antérieure à une version ultérieure sans inscription active entre, l&#39;API résout toujours correctement la version actuelle de l&#39;élève. La présence de versions intermédiaires avec lesquelles l’élève n’a pas collaboré activement n’affecte pas la résolution.

- **Certifications supprimées ou retirées :** une version de certification qui a été supprimée est entièrement exclue de la résolution. Une certification retirée peut toujours être considérée en fonction de son état ; si vous comptez sur une version spécifique restant résoluble, confirmez son état actuel plutôt que de supposer que la suppression à elle seule la supprime de la considération.

- **La résolution est déterministe :** si les données d&#39;inscription d&#39;un élève sont dans un état incohérent (par exemple, plusieurs inscriptions sont marquées comme actuelles), l&#39;API résout vers la dernière version créée plutôt que de renvoyer un résultat imprévisible ou une erreur.

**Remarque** : un équivalent de portée administrateur de cette API n&#39;est pas disponible actuellement et est en cours d&#39;évaluation pour une prochaine version.

### Utiliser cette API dans votre intégration

Un cas d’utilisation courant est une page ou un portail externe qui répertorie les certifications auxquelles un élève peut accéder. Plutôt que de créer un lien direct vers un ID de certification spécifique, qui peut devenir obsolète après une périodicité. Créez un lien à l’aide de l’ID de certification racine et résolvez la version correcte au moment où l’élève la sélectionne.

&#x200B;1. Stockez ou référencez des certifications dans votre intégration à l&#39;aide de l&#39;**ID de certification racine**, l&#39;ID de la certification telle qu&#39;elle a été créée au départ, avant toute périodicité.

&#x200B;2. Lorsqu’un élève sélectionne une certification pour l’afficher ou l’utiliser, appelez GET /primeapi/v2/learningObjects/{loId}/applicableCertification, en transmettant l’ID de certification racine loId.

&#x200B;3. Utilisez la version de certification renvoyée dans la réponse pour diriger l’élève vers la destination correcte, qu’il s’agisse d’une action d’inscription ou d’une vue de la progression actuelle.

Cela garantit que les élèves obtiennent toujours la version de la certification qui correspond à leur inscription et à leur progression réelles, même si la certification se reproduit au fil du temps et génère de nouvelles versions.

## Rapport : ID de formation racine dans le relevé de notes de l’élève

La colonne **ID de formation racine** est disponible par défaut dans le relevé de notes de l&#39;élève pour tous les comptes.

| **Type de ligne** | **Valeur de l&#39;ID de formation racine** |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| Certification configurée pour se répéter | ID de certification racine auquel cette version renvoie |
| Certification non configurée pour se répéter | La même valeur que l’ID de formation pour cette ligne |
| Cours intégré à une certification | ID de certification racine de la certification parent, et non le propre ID du cours |
| Cours ou parcours d’apprentissage qui ne fait partie d’aucune certification | La même valeur que l’ID de formation ou l’ID de cours intégré pour cette ligne |

**Remarque** : pour les comptes très volumineux avec un volume élevé de certifications, les valeurs d&#39;ID de formation racine dans le relevé de notes de l&#39;élève sont résolues par lots. Cela ne modifie pas l’exactitude des données, mais la génération de transcriptions très volumineuses peut prendre plus de temps.

Cette colonne vous permet de regrouper et de générer des rapports sur l&#39;historique complet d&#39;un élève pour chaque version d&#39;une certification périodique, plutôt que de traiter chaque périodicité comme un enregistrement indépendant et sans rapport. Chaque périodicité apparaît toujours comme sa propre ligne dans le relevé de notes de l&#39;élève. La colonne ID de formation racine identifie simplement les lignes appartenant à la même certification sous-jacente.

**Remarque :** utilisez la colonne ID de formation racine pour suivre l&#39;historique complet de participation d&#39;un élève tout au long d&#39;une certification récurrente.

