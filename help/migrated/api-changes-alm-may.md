---
description: Modifications d’API dans ALM
jcr-language: en_us
title: Modifications apportées aux API dans la version d’avril
source-git-commit: 7d3314f9293e1ad7e4ff4f6e537e19c82f7416e9
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# Modifications apportées aux API dans la version de mai 2026

## Amélioration de l’API GET /learningObjects

L’API GET /learningObjects inclut désormais un nouvel attribut startDate dans la ressource learningObjectInstance lorsque la relation d’instances est incluse.

**Point de terminaison**
GET /learningObjects/{id}?include=instances

**Modifier**
Un nouveau champ, startDate, a été ajouté sous :
included[].attributes.startDate

**Description**
startDate représente la date et l&#39;heure de début planifiées d&#39;une instance d&#39;objet d&#39;apprentissage.

**Exemple**
https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course:13209797?include=instances
Réponse de l’échantillon (tronquée)

```
{
  "id": "course:13209797_16226533",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2026-05-20T04:35:46.000Z",
    "isAET": false,
    "isDefault": true,
    "isFlexible": false,
    "startDate": "2026-10-06T18:29:59.000Z",
    "state": "Active",
    "timeZoneCode": "IST"
  }
}
```

**Notes**

* Le champ est renvoyé uniquement pour les instances d’objets d’apprentissage applicables.
* La valeur est renvoyée au format date-heure UTC ISO 8601.
* Les intégrations existantes restent rétrocompatibles.
