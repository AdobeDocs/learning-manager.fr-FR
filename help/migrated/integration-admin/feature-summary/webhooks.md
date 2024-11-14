---
jcr-language: en_us
title: Webhooks
description: Découvrez les webhooks pour envoyer des informations en temps réel, telles que les inscriptions aux cours, la création de cours et d’autres informations, à une URL spécifique
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: e4c3489db8207ead0416656161b918eba42f4582
workflow-type: tm+mt
source-wordcount: '765'
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
