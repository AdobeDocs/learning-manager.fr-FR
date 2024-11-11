---
jcr-language: en_us
title: Webhooks
description: Découvrez les webhooks pour envoyer des informations en temps réel, telles que les inscriptions aux cours, la création de cours et d’autres informations, à une URL spécifique
contentowner: chandrum
source-git-commit: e4b0526e11083d116bf4ca4b0816892e0e8f0f9d
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 1%

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

## Événements en temps réel

| S.No | Événements de webhook | Description |
|---|---|---|
| 1 | CI_STATS | Déclenché en cas de modification de la disponibilité des places ou de la liste d&#39;attente pour une instance de cours. |
| 2 | COURSE_ENROLLMENT | Déclenché lorsqu’un élève s’inscrit à un cours. |
| 3 | COURSE_COMPLETED | Déclenché lorsqu’un élève termine un cours. |
| 4 | LEARNING_PATH_ENROLLMENT | Déclenché lorsqu’un élève s’inscrit à un parcours d’apprentissage. |
| 5 | LEARNING_PATH_COMPLETED | Déclenché lorsqu’un élève termine un parcours d’apprentissage. |
| 6 | CERTIFICATION_ENROLLMENT | Déclenché lorsqu’un élève s’inscrit à une certification. |
| 7 | CERTIFICATION_COMPLETED | Déclenché lorsqu’un élève termine une certification. |
| 8 | COURSE_UNENROLLMENT | Déclenché lorsqu’un élève se désinscrit d’un cours. |
| 9 | LEARNING_PATH_UNENROLLMENT | Déclenché lorsqu’un élève se désinscrit d’un parcours d’apprentissage. |
| 10 | CERTIFICATION_UNENROLLMENT | Déclenché lorsqu’un élève se désinscrit d’une certification. |
| 11 | LEARNING_OBJECT_DRAFT | Déclenché lors de la création d’un objet d’apprentissage à l’état de brouillon. |
| 12 | LEARNING_OBJECT_DELETION | Déclenché lors de la suppression d’un objet d’apprentissage. |
| 13 | LEARNING_OBJECT_MODIFICATION | Déclenché lors de la modification d’un objet d’apprentissage. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Déclenché lors de la création ou de la modification d’une instance d’objet d’apprentissage.<div><b>Remarque :</b> il est recommandé d&#39;utiliser des instances de cours uniquement après la publication du cours.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Déclenché lors de la suppression d’une instance d’objet d’apprentissage. |

## Événements hors temps réel

| S.No | Événements de webhook | Description |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme inscrit des élèves à un cours. |
| 2 | COURSE_COMPLETED_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme marque un cours comme terminé. |
| 3 | LEARNING_PATH_ENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme inscrit des élèves à un parcours d’apprentissage. |
| 4 | LEARNING_PATH_COMPLETED_BATCH | Déclenché lorsqu’un administrateur/responsable marque un parcours d’apprentissage comme terminé. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme inscrit des élèves à une certification. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme marque une certification comme terminée. |
| 7 | LEARNER_PROGRESS | Suit la progression d’un élève lorsqu’un module est terminé. |
| 8 | COURSE_UNENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme désinscrit des élèves d’un cours. |
| 9 | LEARNING_PATH_UNENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme désinscrit des élèves d’un parcours d’apprentissage. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme désinscrit des élèves d’une certification. |
| 11 | LEARNING_OBJECT_MODIFICATION_BATCH | Déclenché lors de la modification d’un objet d’apprentissage via le workflow de migration. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Déclenché lors de la création ou de la modification d’une instance d’objet d’apprentissage via le workflow de migration. |

## Bonnes pratiques pour les webhooks

Les webhooks permettent la communication en temps réel basée sur des événements entre les services. Cependant, une implémentation incorrecte peut entraîner des événements perdus, une lenteur des performances du système ou des risques de sécurité. Vous trouverez ci-dessous les bonnes pratiques pour mettre en œuvre des webhooks, en mettant l’accent sur la tolérance aux pannes, la fiabilité et la sécurité.

### Tolérance aux pannes

La tolérance aux pannes du système de webhook ALM fournit des recommandations aux abonnés pour gérer les problèmes potentiels, tels que la perte d’événements, les événements en double et la remise en panne.

Le délai d’expiration de la connexion ALM est configuré sur 10 secondes et celui du socket sur 5 secondes. On s&#39;attend à ce que le client accuse réception du message dès qu&#39;il le reçoit. Cela permet de s&#39;assurer que le client n&#39;accuse pas de retard lors du traitement des messages. Dans le cas où un traitement en aval prend du temps, le client doit toujours accuser réception de l’événement instantanément, puis gérer le traitement en aval à sa fin.

#### Conservation des données

Les événements sont conservés pendant 7 jours. Si elles ne sont pas traitées dans ce délai, elles sont définitivement perdues. Si la récupération a lieu le dernier jour et qu’un délai supplémentaire est nécessaire, le système ne prolonge pas la période de rétention.
Si des événements sont produits plus rapidement qu’ils ne sont consommés, certains événements peuvent être perdus. Bien que cela soit rare, les abonnés doivent surveiller pour éviter que cela ne devienne un problème à long terme.

#### Webhooks désactivés

Lorsqu’un abonné ne répond pas aux événements de webhook, le système ALM tente à nouveau de créer des webhooks à l’aide d’une annulation exponentielle pour éviter de submerger l’abonné.

Le processus de nouvelle tentative démarre avec un intervalle initial de 5 secondes. Si l&#39;abonné ne répond pas, le temps d&#39;attente double pour atteindre 10, 20, 40 et 80 secondes, et peut augmenter jusqu&#39;à un maximum de 5 minutes. Une fois qu&#39;il atteint 5 minutes, le système continuera à réessayer toutes les 5 minutes jusqu&#39;à la fin de la période de rétention de 7 jours. Si l’abonné ne répond toujours pas pendant toute cette période, le webhook est automatiquement désactivé. Un e-mail de rappel sera envoyé à l’abonné à intervalles réguliers.

#### Dupliquer les événements

Si un abonné met plus de 5 secondes à répondre après le traitement d&#39;un événement, le système peut essayer de traiter à nouveau le même événement. Il est recommandé d’utiliser des ID d’événement pour suivre les événements déjà traités. En outre, si le webhook se bloque après l’envoi de l’événement mais avant l’enregistrement de son traitement, le même groupe d’événements peut être retenté. Il est recommandé d’utiliser des ID de lot ou des ID d’événement individuels pour reconnaître et ignorer les doublons.

#### Événements hors service

ALM tente de conserver les événements dans l&#39;ordre correct, mais il arrive que des événements ne soient pas distribués dans l&#39;ordre, en particulier entre des événements en temps réel et non en temps réel.

Si un administrateur inscrit plusieurs élèves à la fois à un cours, les événements d&#39;inscription sont marqués comme non en temps réel. Toutefois, si un élève termine le cours rapidement, cet événement d&#39;achèvement est marqué comme étant en temps réel et peut être diffusé avant les événements d&#39;inscription.

#### Recommandation pour la tolérance aux pannes

Pour éviter ces erreurs, les abonnés doivent surveiller activement les événements de webhook et configurer des alertes pour les problèmes tels que les événements manqués, les livraisons en double ou les séquences désordonnées.

## Consignes spécifiques aux événements de webhook

1. Si vous obtenez d’abord un événement LEARNER_PROGRESS, ignorez ensuite les événements répertoriés ci-dessous :

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEARNING_PATH_ENROLLMENT
   * LEARNING_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Ignorez l’événement LEARNER_PROGRESS s’il survient après les événements suivants :

   * COURSE_COMPLETED
   * COURSE_COMPLETED_BATCH
   * LEARNING_PATH_COMPLETED
   * LEARNING_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Utilisez le champ d’horodatage pour déterminer s’il faut ignorer ou traiter l’événement, à l’exception de l’événement LEARNER_PROGRESS.


## Exemples de charges pour les événements

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "01234567-0458-4450-b5dd-6bc1edr4560",
      "eventName": "CI_STATS",
      "timestamp": 1725604147,
      "eventInfo": "1725604145-LoSt",
      "data": {
        "loInstanceId": "course:1234567_123456775",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "29123ec1-4576-4ec5-a057-3a6dr45t9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:1234567_1234567",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725524713
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "29572ec1-4576-4ec5-a057-3wsd43r59d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:12345678_123456788",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725524713
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345671",
        "loInstanceId": "course:1234567_12345674",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725523818,
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 112345678,
        "loId": "course:12345678",
        "loInstanceId": "course:1234567_12345678",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725523818,
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "96ed0791-338f-4c4c-83bc-9fwfr4564965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 11234567,
        "loId": "learningProgram:123456",
        "loInstanceId": "learningProgram:12345_134567",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604248
      }
    }
  ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "96edft791-338f-4c4c-83bc-9f7erf94965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12347",
        "loInstanceId": "learningProgram:12345_12345",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604248
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "e207104e-d554-4027-944b-08fty6fdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 11080928,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604380,
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "e207104e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604380,
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8bdfr76-148e-4128-80e9-b89123456755",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:123456_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604672
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8b2ee776-148e-4128-80e9-12345678",
      "eventName": "CERTIFICATION_ENROLLMENT_BATCH",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 123456788,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604672
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1245678",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604740
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:134567",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604740
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "dd04d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": 1725604552,
      "eventInfo": "1725604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12345678,
        "loInstanceId": "course:1234567_11234567",
        "dateStarted": 1725604380,
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3417817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 12345671,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3417817-8cb8-40ea-a441-8123e45724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 123456781,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d123456d1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 12345678,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
       
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 1234567,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:1234567_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1712349f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": 1725519188,
      "eventInfo": "1725519188000-040344-48604-0",
      "data": {
        "loId": "course:12345671",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "023456-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": 1725605296,
      "eventInfo": "1234567800-040656-662792-0",
      "data": {
        "loId": "course:1234567",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "22345668-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456000-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
        "loType": "learningProgram"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "2234567068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456700-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
        "loType": "learningProgram"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b131da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": 1725603298,
      "eventInfo": "1723456000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:12345678",
        "loType": "course"
        
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b23458-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": 1725603298,
      "eventInfo": "112345000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:1234568",
        "loType": "course"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234560-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": 1725605491,
      "eventInfo": "17223456700-040657-236307-0",
      "data": {
        "loInstanceId": "course:1234567_14453849",
        "loId": "course:1234567",
        "loType": "course"

      }
    }
  ]
}
```

+++

