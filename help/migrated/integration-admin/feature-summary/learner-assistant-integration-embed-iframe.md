---
description: Découvrez comment intégrer l’assistant d’élève dans votre application à l’aide d’un iframe, y compris la configuration et la gestion des événements
jcr-language: en_us
title: Intégrer l’assistant d’élève en intégrant iFrame
source-git-commit: 1549a4592b7a930631dcff6b2e75ec3a3d4f5592
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 2%

---


# Intégration de l’assistant d’élève à l’aide d’un iframe

## Présentation

Les utilisateurs de Adobe Learning Manager (ALM) peuvent intégrer l&#39;**assistant Élève** directement dans leurs propres applications destinées aux élèves (par exemple, des portails personnalisés, des systèmes de gestion de l&#39;apprentissage frontaux, des centres d&#39;apprentissage, etc.) utilisation d&#39;un HTML standard `<iframe>`.

Lorsqu’il est intégré via iFrame, l’assistant Élève donne accès à toutes les fonctionnalités de l’assistant, notamment :

* Orchestrator
* Agent de réponse
* Agent de connaissances
* Agent de parcours d’apprentissage

>[!IMPORTANT]
>
>L’incorporation d’iFrame donne à votre application un accès complet aux agents sous-jacents de l’assistant Élève. Cependant, votre application (l’« application parent ») est responsable de la gestion des événements émis par l’assistant. Par exemple, lorsqu&#39;un élève clique sur une citation ou sur un lien de cours dans la réponse de l&#39;assistant, l&#39;assistant émet un événement. Votre application parent doit gérer cet événement et effectuer la navigation réelle. L’assistant d’élève ne navigue pas au nom de votre application.

## Conditions préalables

Avant de commencer, assurez-vous d’avoir :

* Un client ALM avec l’assistant Élève activé. Configurez les catalogues requis à partir de la page des paramètres de l’administrateur.
* Un jeton d’accès valide pour authentifier la session de l’élève (ou de l’administrateur). Pour générer un jeton d’accès, suivez les instructions de la page [Authentification à l’aide d’OAuth 2.0](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20). La page comprend les étapes requises pour s’authentifier et générer le jeton d’accès nécessaire pour continuer.
* Possibilité d&#39;incorporer un `<iframe>` dans votre application et de communiquer avec lui via l&#39;API postMessage du navigateur.
* Propriété du code frontal de l’application parent, car votre application doit écouter et répondre aux messages de l’iFrame intégré.

## Paramètres de configuration de l’assistant d’apprentissage

| Nom du paramètre | Valeur | Description |
|---|---|---|
| hostName | learningmanager.adobe.com | Spécifie le domaine hôte de l&#39;application. |
| accessToken | token123 (jeton d’accès réel) | Jeton utilisé pour authentifier et autoriser la session utilisateur. |

## Initialiser iFrame

Transmettez la configuration à l’assistant de l’élève via l’API postMessage, à l’aide d’une poignée de main de configuration iFrame intégrée.

1. L&#39;application parent incorpore l&#39;Assistant d&#39;apprentissage en tant que `<iframe>`.
2. Si aucune configuration basée sur l’URL n’est trouvée, l’assistant d’apprentissage envoie un événement ALM_CHAT_REQUEST_CONFIG à l’application parent.
3. L&#39;application parente répond avec un événement ALM_CHAT_CONFIG contenant la payload de configuration. Par exemple :

   ```json
   {
     "hostName": "learningmanager.adobe.com",
     "accessToken": "token123",
     "openByDefault": false,
     "isAdmin": false
   }
   ```

4. Une fois l’initialisation réussie, l’assistant de l’élève effectue le rendu et est prêt à être utilisé.

## Résumé des événements iFrame

L&#39;assistant de l&#39;élève et l&#39;application parent communiquent par le biais d&#39;événements postMessage dans les deux sens.

### Événements sortants (iFrame de l’assistant de l’élève vers l’application parent)

| Nom de l&#39;événement | Description | Paramètres transmis |
|---|---|---|
| ALM_CHAT_OPENED | Déclenché à l’ouverture de la conversation. | -- |
| ALM_CHAT_CLOSED | Déclenché lorsque la conversation est fermée. | -- |
| ALM_CHAT_LO_REDIRECT | Accédez à la page de présentation personnalisée du parcours d’apprentissage. | loId, loType, instanceId |
| ALM_CHAT_URL_REDIRECT | Déclenché lorsqu’un lien externe est cliqué dans le message de conversation. | url |
| ALM_CHAT_REQUEST_CONFIG | Demande la configuration à partir de l’application parent. | -- |
| ALM_CHAT_WAITING_FOR_REPLY | Indique que l&#39;assistant traite une demande ou attend une réponse. | isWaitingForReply |
| ALM_CHAT_PERSONALIZED_PATH_CREATED | Déclenché lorsqu’un parcours d’apprentissage est enregistré. | -- |

### Événements entrants (application parente vers l’assistant de l’élève)

| Nom de l&#39;événement | Description | Charge utile |
|---|---|---|
| ALM_CHAT_CONFIG | Envoie la charge utile de configuration requise pour initialiser l&#39;assistant. | Objet de configuration |
| ALM_CHAT_OPEN | Ouvre l’assistant Élève. | Aucune |
| ALM_CHAT_CLOSE | Ferme l’assistant d’élève. | Aucune |
| ASK_AI_ASSISTANT_QUERY | Ouvre la fenêtre de conversation et envoie une requête à l’assistant. | { query : « Question text » } |

## Exigences de gestion des événements dans l’application parent

L’incorporation de l’assistant d’élève via iFrame ne en fait pas un widget entièrement autonome. Votre application parente doit activement écouter les événements sortants et prendre les mesures appropriées. Au minimum, votre application doit :

* Écoutez ALM_CHAT_REQUEST_CONFIG et répondez avec ALM_CHAT_CONFIG afin que l’assistant puisse s’initialiser.
* Gérer ALM_CHAT_LO_REDIRECT : lorsqu’un élève clique sur une citation ou une source dans la réponse de l’assistant, votre application reçoit les loId, loType et instanceId, et est responsable de l’orientation de l’élève vers le cours ou l’objet d’apprentissage correct.
* Gérer ALM_CHAT_URL_REDIRECT : lorsqu’un élève clique sur un lien externe dans un message de conversation, votre application reçoit l’URL et est responsable de son ouverture ou de sa navigation (par exemple, dans un nouvel onglet).
* Suivez éventuellement ALM_CHAT_OPENED / ALM_CHAT_CLOSED / ALM_CHAT_WAITING_FOR_REPLY pour refléter l&#39;état de l&#39;assistant dans votre propre interface utilisateur (par exemple, en affichant un indicateur de chargement alors que isWaitingForReply a la valeur true).
* Vous pouvez également utiliser ALM_CHAT_OPEN / ALM_CHAT_CLOSE / ASK_AI_ASSISTANT_QUERY pour contrôler l’assistant par programme. Par exemple, ouvrez l&#39;assistant et préremplissez une requête à partir d&#39;un bouton **Aide** ailleurs dans votre application.

## Besoin d’aide ?

Contactez votre chargé de réussite client Adobe pour configurer une procédure pas à pas technique.
