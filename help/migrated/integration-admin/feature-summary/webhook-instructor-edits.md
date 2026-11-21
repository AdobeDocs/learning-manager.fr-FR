---
description: Obtenez des événements de webhook dans Adobe Learning Manager lorsque les instructeurs modifient les détails de la session et maintenez les notifications des élèves et les systèmes connectés à jour.
jcr-language: en_us
title: Réception d’événements de webhook pour les modifications de session d’instructeur
exl-id: 6fa4b71b-a8f4-40a2-ab57-bb7f3016542c
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%
---

# Événements de webhook pour les modifications d’instance LO par les instructeurs

Adobe Learning Manager fournit des événements webhook qui informent les systèmes externes lorsqu’une instance d’objet d’apprentissage (LO), telle qu’une session d’un cours dirigé par un instructeur, est modifiée. Auparavant, ces événements étaient déclenchés uniquement lorsqu&#39;un administrateur ou un auteur modifiait une instance d&#39;objet d&#39;apprentissage. Les événements de webhook sont désormais également déclenchés lorsqu’un instructeur modifie les détails d’une session.

Vous pouvez utiliser ces événements pour que les systèmes externes, tels que les services de messagerie, les calendriers, les outils de création de rapports ou les plateformes d’analyse, restent à jour avec les modifications apportées aux instructeurs. Par exemple, vous pouvez informer les élèves lorsqu’une heure de session change.

Les modifications des instructeurs utilisent l&#39;événement de modification de l&#39;instance d&#39;objet d&#39;apprentissage existant, de sorte qu&#39;aucun nouveau type d&#39;événement n&#39;est introduit.

>[!NOTE]
>
>Les modifications d’instructeur déclenchent un webhook uniquement si un webhook actif s’abonne à l’événement de modification de l’instance d’objet d’apprentissage. Découvrez comment [créer et gérer des webhooks en tant qu’administrateur d’intégration](/help/migrated/integration-admin/feature-summary/webhooks.md#create-manage-webhooks).

## Modifications d’instructeur prises en charge

L’événement webhook est déclenché lorsqu’un instructeur modifie l’un des détails de session suivants :

* Horaires des sessions

* Crédits

* Fuseau horaire

* Salle

* Limite d’inscription

* Limite de liste d’attente

* Autoriser les soumissions

## Structure de la charge utile du webhook

Chaque demande de webhook contient la structure de niveau supérieur suivante :

```json
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

La même structure est utilisée quelle que soit la personne qui modifie l’instance d’objet d’apprentissage. La payload n’indique pas si un instructeur, un administrateur ou un auteur a effectué la modification.

Lorsqu’un instructeur modifie des détails d’une session, tels que le fuseau horaire, la limite d’inscription ou la limite de liste d’attente, le webhook envoie cet événement à l’URL du processus d’écoute. Utilisez l’événement pour récupérer les derniers détails de session et en informer les élèves ou mettre à jour vos systèmes externes.

## Récupérer les détails de la session mis à jour

L’événement webhook identifie l’instance d’objet d’apprentissage qui a été modifiée. Pour obtenir les détails de la session mis à jour, appelez l’API publique Learning Manager (API Prime) à l’aide de `loId` à partir de l’événement :

```http
GET /primeapi/v2/learningObjects/{loId}
```

Recherchez l&#39;instance correspondant à `loInstanceId` dans la réponse, puis comparez-la avec les données stockées dans votre système.

## Création d’intégrations avec des événements de webhook

Vous pouvez utiliser ces événements de webhook pour :

* Envoyer des notifications aux élèves par courrier électronique ou messagerie externe lorsque les détails de la session tels que la date, l&#39;heure, le fuseau horaire ou le lieu changent.

* Synchroniser les données de session avec des calendriers externes, des rapports ou des systèmes d&#39;analyse.

* Suivez les modifications de capacité lorsque la limite d’inscription ou la limite de liste d’attente d’une session est modifiée.

* Conserver les journaux d&#39;audit en enregistrant `eventId`, `timestamp` et `eventInfo` avec l&#39;objet d&#39;apprentissage et les identifiants d&#39;instance.

Au minimum, votre gestionnaire de webhook doit :

* Validez la payload et analysez `events[]`.

* Utilisez `eventName` pour identifier l&#39;événement de modification de l&#39;instance de l&#39;objet d&#39;apprentissage.

* Utilisez `loId` et `loInstanceId` pour localiser l&#39;enregistrement correspondant dans votre système et appelez l&#39;API publique pour récupérer les détails de la session actuelle.

* Utilisez `eventId` pour empêcher le traitement en double si le même événement est diffusé plusieurs fois.

Le même événement est envoyé pour les modifications apportées par les instructeurs, les administrateurs et les auteurs, de sorte que votre intégration peut le recevoir plus souvent qu’auparavant. Comparez les détails de session récupérés avec les données de votre système avant d’envoyer une notification. Les élèves sont ensuite avertis uniquement lorsque les détails pertinents changent.
