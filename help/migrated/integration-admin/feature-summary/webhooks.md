---
jcr-language: en_us
title: Webhooks
description: Découvrez les webhooks pour envoyer des informations en temps réel, telles que les inscriptions aux cours, la création de cours et d’autres informations, à une URL spécifique
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '1633'
ht-degree: 0%

---

# Webhooks

Un webhook permet à une entité d’envoyer automatiquement des données en temps réel ou des notifications à une autre entité lorsqu’un événement spécifique se produit. Elle permettra à une application de fournir des informations à d&#39;autres applications sans les demander constamment. Par exemple, si un utilisateur termine un cours sur un système de gestion de l’apprentissage (LMS), un webhook peut automatiquement envoyer ces informations à une autre plate-forme, telle qu’un outil de gestion de la relation client ou de création de rapports. Les webhooks sont souvent utilisés dans les intégrations pour automatiser les processus et réduire le besoin de mises à jour manuelles entre les systèmes. Configurez les webhooks en fournissant une URL de rappel à laquelle vous enverriez les données.

## Webhooks et API

Les webhooks et les API aident les systèmes à communiquer entre eux, mais leur fonctionnement est différent. Avec les API, les informations sont partagées uniquement lorsque l’utilisateur en fait la demande. Par exemple, si un élève a besoin des données de progression du cours, il envoie une demande à l’API, qui fournit alors les informations. D’autre part, les webhooks envoient automatiquement des données immédiatement lorsqu’un événement se produit. Par exemple, si un élève termine un cours, il envoie immédiatement les données à l&#39;URL du processus d&#39;écoute sans aucune demande manuelle.

## Que sont les API en temps réel ?

Les API en temps réel permettent aux applications d’effectuer un exchange instantané des données lorsqu’un événement se produit. Contrairement aux API traditionnelles, qui attendent qu’un utilisateur demande des informations, les API en temps réel partagent des données dès qu’elles se produisent. Les webhooks agissent comme une API en temps réel et permettent de partager les données immédiatement chaque fois que l’événement spécifié se produit. L’API en temps réel garantit que ce transfert de données s’effectue immédiatement, sans qu’aucune demande manuelle ne soit nécessaire, ce qui permet aux systèmes de rester mis à jour instantanément.

## Événements de webhook

Les événements de webhook sont des actions spécifiques se produisant dans un système qui envoie automatiquement des données à une URL de processus d’écoute. Par exemple, lorsqu’un élève s’inscrit à un cours, un événement webhook est déclenché et envoie les détails d’inscription à l’URL du processus d’écoute.

Les événements de webhook sont classés en deux catégories :

* **Événements en temps réel** : les événements sont traités et envoyés en temps réel à une URL cible
* **Événements hors temps réel** : les événements sont traités par lots et envoyés à des heures spécifiées et non en temps réel

## URL du processus d’écoute

Une URL de processus d&#39;écoute est un point de terminaison ou une destination qui reçoit des informations de données lorsqu&#39;un événement se produit. Chaque fois qu&#39;un événement spécifique se produit, tel qu&#39;un utilisateur s&#39;inscrivant à un cours, le système envoie automatiquement les détails à cette URL sans aucune demande manuelle. L’URL du processus d’écoute est l’adresse à laquelle toutes ces mises à jour sont envoyées.
Le webhook envoie les informations pertinentes au format JSON. Voici un exemple de charge utile pour un événement déclenché dans Adobe Learning Manager :

```
{
  "accountId": 1010,
  "events": [
    {
      "eventId": "d5fb7071-10a9-46b2-9f9e-79dde346c052",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1727414643000,
      "eventInfo": "1727414643000-047210-84242-0",
      "data": {
        "userId": 4279332,
        "loId": "course:7374992",
        "loInstanceId": "course:7376092_10250977",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1727414643
      }
    }
  ]
}
```

## Création et gestion des webhooks - Administrateur de l’intégration

Suivez les étapes ci-dessous pour créer une intégration Webhooks dans Adobe Learning Manager :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur d&#39;intégration]**.
2. Sur la page d’accueil, sélectionnez **[!UICONTROL Webhooks]** > **[!UICONTROL Ajouter un webhook]**.

   ![](assets/create-webhook.png)
   _Ajouter un webhook_

3. Saisissez le **[!UICONTROL nom]** et la **[!UICONTROL description]** du webhook.
4. Tapez l&#39;URL du processus d&#39;écoute en tant que **[!UICONTROL URL cible]** où vous souhaitez transmettre les données d&#39;événement.
5. Sélectionnez l’une des méthodes d’authentification :
L’authentification dans Webhooks est une méthode de sécurité permettant de s’assurer que les données envoyées à une URL de processus d’écoute proviennent d’une source approuvée.
   * **[!UICONTROL Aucun]** : aucune authentification requise.
   * **[!UICONTROL De base]** : il s&#39;agit d&#39;une authentification basée sur les informations d&#39;identification. Saisissez le nom d’utilisateur et le mot de passe.
   * **[!UICONTROL Signature]** : le système crée une signature spéciale et l’ajoute aux données du webhook. Le serveur de réception vérifie ce code pour s&#39;assurer que les données sont réelles et n&#39;ont pas été modifiées. Générez une signature et utilisez-la pour l’authentification. Téléchargez la signature au format JSON.
6. Sélectionnez les événements Webhook dans la liste déroulante **[!UICONTROL Déclencher des événements]**.

   >[!NOTE]
   >
   >Vous pouvez également tester les webhooks en sélectionnant l’option Tester les webhooks dans la page Ajouter un webhook.

7. Sélectionnez l’option **[!UICONTROL État d’activation]** pour activer le webhook. Une fois cette option activée, les données sont transmises chaque fois que les événements sélectionnés se produisent.

>[!NOTE]
>
>Vous pouvez créer et gérer jusqu’à 5 webhooks.

### Modifier les webhooks - Administrateur de l’intégration

Procédez comme suit pour modifier des webhooks à partir de Adobe Learning Manager :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur d&#39;intégration]**.
2. Sélectionnez **[!UICONTROL Webhooks]** sur la page d’accueil.
3. Sélectionnez le webhook que vous souhaitez modifier.

   ![](assets/edit-webhook.png)
   _Modifier le webhook_
4. Sélectionnez **[!UICONTROL Modifier]** pour modifier les détails du webhook et sélectionnez **[!UICONTROL Enregistrer]**.

### Suppression des webhooks - Administrateur de l’intégration

Procédez comme suit pour modifier des webhooks à partir de Adobe Learning Manager :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur d&#39;intégration]**.
2. Sélectionnez **[!UICONTROL Webhooks]** sur la page d’accueil.
3. Sélectionnez le webhook à supprimer.
4. Sélectionnez **[!UICONTROL Supprimer]** pour supprimer les webhooks.

![](assets/delete-webhooks.png)
_Supprimer le webhook_

### Retrait des webhooks - Administrateur de l’intégration

Procédez comme suit pour retirer les webhooks :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur d&#39;intégration]**.
2. Sélectionnez **[!UICONTROL Webhooks]** sur la page d’accueil.
3. Sélectionnez le webhook que vous souhaitez modifier.
4. Sélectionnez **[!UICONTROL Modifier]** et désactivez **[!UICONTROL État d’activation]** pour retirer le webhook.

![](assets/retire-webhook.png)
_Retrait du webhook_

## Webhooks pour les alternatives {#webhooks-for-alternates}

ALM fournit des événements de webhook dédiés pour des achèvements alternatifs afin de prendre en charge l’automatisation, les intégrations et la synchronisation avec des systèmes externes.

Ces événements permettent aux consommateurs externes de faire une distinction fiable entre les achèvements directs et les achèvements accordés par le biais de relations alternatives.

### Présentation

Lorsqu’un élève termine un cours via un autre ou une autre relation, ALM déclenche un événement webhook distinct du webhook d’achèvement de cours standard. Cela garantit que les intégrations peuvent répondre différemment aux autres finalisations si nécessaire.

Les événements de webhook sont également déclenchés en cas d’achèvement rétroactif ou d’inachèvement rétroactif, couvrant les mises à jour historiques ainsi que les modifications de relation.

### Comportement d’événement Webhook

* Un événement webhook distinct est déclenché lorsqu’un élève reçoit l’événement Terminé via un autre statut pour un cours cible.
* L’événement est généré lorsque l’élève termine un cours source configuré qui satisfait la cible via une autre relation.
* Ce webhook n’est pas déclenché pour les terminaisons de cours directes.
* Lorsque l’achèvement rétroactif ou l’inachèvement rétroactif est activé, des événements webhook sont émis pour chaque élève affecté et chaque cours cible.

### Détails de la payload du webhook

La payload du webhook d’achèvement secondaire inclut les attributs clés suivants :

* **ID d’élève**
Identifie l’élève qui a reçu l’autre achèvement.
* **Cours source**
Cours ou parcours d’apprentissage que l’élève a suivi directement.
* **Cours cible**
Cours marqué comme terminé via la relation de remplacement.
* **Méthode d&#39;achèvement**
Indique que la méthode d&#39;achèvement est alternative.
* **Date d’achèvement**
Dérivé de la date de fin du cours source.
* **Type de relation**
Spécifie si la relation est alternative.

Pour les scénarios d’inachèvement rétroactifs, les événements de webhook indiquent qu’un autre achèvement existant a été révoqué.

### Considérations relatives à l’intégration

Les systèmes externes peuvent utiliser ces événements de webhook pour :

* Mettre à jour les enregistrements d’élève
* Synchronisation de l’état d’achèvement
* Déclencher des notifications ou des workflows en aval
* Gestion des pistes d’audit à des fins de conformité

Les utilisateurs de webhook doivent faire une distinction explicite entre les achèvements directs et alternatifs.

Les compléments alternatifs n&#39;accordent pas de récompenses de compétences, de badges et de ludification. Le retour d&#39;informations doit être traité en conséquence dans les systèmes en aval.

## Webhooks pour les parcours d’apprentissage adaptatifs

### Introduction

Adobe Learning Manager fournit des **événements webhook** qui informent les systèmes externes chaque fois que l’état d’achèvement d’un **parcours d’apprentissage (programme d’apprentissage)** est actualisé. Cela vous permet de synchroniser les systèmes en aval (tels que les plateformes de RH, de création de rapports ou d&#39;analyse) chaque fois que l&#39;enregistrement d&#39;achèvement d&#39;un élève est annulé ou recalculé.

Deux nouveaux types d’événements de webhook sont disponibles :

**LEARNING_PATH_COMPLETION_ROLLBACK** : déclenché lorsqu’un **élève** actualise l’état d’achèvement d’un parcours d’apprentissage pour lui-même.

**LEARNING_PATH_COMPLETION_ROLLBACK_BATCH** : déclenché lorsqu’un **administrateur** actualise l’état d’achèvement d’un parcours d’apprentissage pour **un ou plusieurs élèves** (par exemple, via des opérations en bloc).

Ces événements utilisent une **structure de charge utile commune** et peuvent être utilisés par votre point de terminaison webhook pour mettre à jour ou retraiter les données d’achèvement de votre côté.

### Structure de charge utile commune

Chaque demande de webhook contient la structure de niveau supérieur suivante :

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "757b9d58-048c-4ae2-9fff-35f9def7ef29",
      "eventName": "LEARNING_PATH_COMPLETION_ROLLBACK",
      "timestamp": "2026-01-20T05:48:10.000Z",
      "eventInfo": "1768888090000-197513-137581-0",
      "data": {
        "userId": 13446697,
        "loId": "learningProgram:157165",
        "loInstanceId": "learningProgram:157165_148769",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2026-01-20T05:44:05.000Z"
      }
    }
  ]
}
```

La **même structure** est utilisée pour les deux types d&#39;événements ; seuls eventName et les valeurs dans les données (par exemple, userId, loId, enrollmentSource) diffèrent.

#### Exemple : actualisation initiée par l’élève

Lorsqu’un élève actualise l’état d’achèvement de son propre parcours d’apprentissage, le webhook envoie un événement LEARNING_PATH_COMPLETION_ROLLBACK :

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "757b9d58-048c-4ae2-9fff-35f9def7ef29",
      "eventName": "LEARNING_PATH_COMPLETION_ROLLBACK",
      "timestamp": "2026-01-20T05:48:10.000Z",
      "eventInfo": "1768888090000-197513-137581-0",
      "data": {
        "userId": 13446697,
        "loId": "learningProgram:157165",
        "loInstanceId": "learningProgram:157165_148769",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2026-01-20T05:44:05.000Z"
      }
    }
  ]
}
```

Utilisez cet événement pour **recalculer ou réinitialiser les données d&#39;achèvement des élèves** dans vos systèmes externes lorsque l&#39;élève demande explicitement une actualisation.

#### Exemple : actualisation par lots initiée par l’administrateur

Lorsqu’un administrateur effectue une actualisation des terminaisons pour un ou plusieurs élèves (par exemple, en corrigeant les terminaisons historiques pour un groupe), le webhook émet un événement LEARNING_PATH_COMPLETION_ROLLBACK_BATCH :

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "757b9d58-048c-4ae2-9fff-35f9def7ef29",
      "eventName": "LEARNING_PATH_COMPLETION_ROLLBACK_BATCH",
      "timestamp": "2026-01-20T05:48:10.000Z",
      "eventInfo": "1768888090000-197513-137581-0",
      "data": {
        "userId": 13446698,
        "loId": "learningProgram:157166",
        "loInstanceId": "learningProgram:157166_148770",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2026-01-21T05:44:05.000Z"
      }
    }
  ]
}
```

Dans les opérations par lots, votre point de terminaison webhook peut recevoir **plusieurs objets d’événement dans une seule demande**, à raison d’un par élève dont l’achèvement a été actualisé. Votre intégration doit se répéter sur le tableau d’événements et traiter chaque événement indépendamment.

### Comment utiliser ces événements dans les intégrations

Vous pouvez utiliser ces événements de webhook pour :

**Synchroniser les enregistrements d&#39;achèvement** avec des systèmes externes LMS/LRS, HR ou de reporting lorsqu&#39;un achèvement est annulé ou recalculé.

**Déclencher des workflows en aval** tels que des réaffectations, des notifications ou le recalcul de certifications et de badges.

**Conserver les journaux d’audit** en consignant l’eventId, l’horodatage et l’eventInfo avec les identifiants de l’élève et du parcours d’apprentissage.

Au minimum, votre gestionnaire de webhook doit :

Validez la payload et analysez les événements[].
Utilisez eventName pour déterminer si la modification a été **initiée par l&#39;élève** ou **initiée par l&#39;administrateur/le lot**.

Utilisez userId, loId et loInstanceId pour localiser et mettre à jour l’enregistrement correspondant dans votre système.
Utilisez l’ID d’événement pour éviter tout traitement en double si le même événement est diffusé plusieurs fois.

## Webhooks pour l’ajout et la suppression d’appartenances à un groupe d’utilisateurs

Deux nouveaux types d’événements de webhook affichent les statuts finaux :

* RÉPONSE:ASYNCAPI_USERGROUP_USER_ADDED
* RÉPONSE:ASYNCAPI_USERGROUP_USER_REMOVED

### Exemple de charge utile

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5",
      "eventName": "RESPONSE:ASYNCAPI_USERGROUP_USER_REMOVED",
      "timestamp": "2026-03-18T13:38:12.000Z",
      "eventInfo": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5",
      "data": {
        "status": "SUCCESS",
        "request": {
          "metadata": { "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" },
          "data": [ { "type": "user", "id": "13446641" } ]
        }
      }
    }
  ]
}
```

### Eléments clés

* `accountId` identifie le compte ALM.
* `events` est un tableau d&#39;objets d&#39;événement.
* `eventId` correspond à l&#39;identificateur de demande asynchrone d&#39;origine.
* `eventName` indique une opération d&#39;ajout ou de suppression.
* `timestamp` affiche l&#39;heure d&#39;achèvement.
* `data.status` signale actuellement « SUCCESS » pour les lots réussis.
* `data.request` contient la demande exacte que vous avez envoyée.

Votre intégration devrait principalement désactiver `eventId` (ou `metadata.event_id`) et `status`.

### Exemples

#### Ajout d’utilisateurs de manière asynchrone

**Étape 1. Effectuer l&#39;appel asynchrone**

POST /primeapi/v2/async/userGroups/12345/users

```
{
  "metadata": {
    "event_id": "sync-2026-03-30T10:15:00Z-ug-12345",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

**Étape 2. Lire la réponse immédiate**

```
{ "event_id": "sync-2026-03-30T10:15:00Z-ug-12345" }
```

Vous pouvez maintenant marquer cette tâche comme envoyée dans votre système.

**Étape 3. Gérer le webhook**

Exemple de rappel de webhook :

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "sync-2026-03-30T10:15:00Z-ug-12345",
      "eventName": "RESPONSE:ASYNCAPI_USERGROUP_USER_ADDED",
      "timestamp": "2026-03-30T10:15:43.000Z",
      "data": {
        "status": "SUCCESS",
        "request": {
          "metadata": {
            "event_id": "sync-2026-03-30T10:15:00Z-ug-12345",
            "sourceSystem": "HRIS",
            "batchId": "hr_2026_03_30_0001"
          },
          "data": [
            { "type": "user", "id": "11101219" },
            { "type": "user", "id": "11101220" }
          ]
        }
      }
    }
  ]
}
```

Un consommateur type :

* Recherchez la tâche interne.
* Vérifiez éventuellement l&#39;appartenance à l&#39;aide de GET /userGroups/{id}/users.
* Marquer la tâche comme terminée.

#### Suppression d’utilisateurs de manière asynchrone

La suppression est symétrique, à l’aide d’un DELETE possédant la même structure de corps.

```
{
  "metadata": {
    "event_id": "sync-2026-03-30T11:00:00Z-ug-12345",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0002"
  },
  "data": [ { "type": "user", "id": "11101219" } ]
}
```

Réponse immédiate :

```
{ "event_id": "sync-2026-03-30T11:00:00Z-ug-12345" }
```

Par la suite, un webhook RESPONSE:ASYNCAPI_USERGROUP_USER_REMOVED arrive avec le même eventId.

Pour plus d&#39;informations, consultez [API publique asynchrone pour l&#39;appartenance à un groupe d&#39;utilisateurs](/help/migrated/api-changes-alm.md#asynchronous-public-apis-for-user-group-membership).
