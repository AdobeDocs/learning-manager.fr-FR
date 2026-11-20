---
title: Sous-titres dans les sessions Live Hub
description: Découvrez comment les sous-titres affichent le contenu parlé en temps réel afin que les instructeurs et les élèves puissent suivre les sessions Live Hub.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 574ba5fd9ac9dc02130a39006574c9ca1ce6c1d1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 4%
---

# Familiarisation avec les sous-titres

Les sous-titres sont générés automatiquement lors d’une session Live Hub et sont mis à jour en continu lorsque les participants parlent. Les légendes s&#39;affichent dans une zone d&#39;affichage dédiée et dans la langue sélectionnée par l&#39;instructeur dans les **paramètres de la salle**.

Les instructeurs et les participants peuvent afficher les légendes. Chaque participant peut afficher ou masquer des sous-titres indépendamment sans affecter les paramètres de sous-titres des autres participants.

Seuls les instructeurs peuvent modifier la langue des sous-titres. Les participants peuvent uniquement afficher les sous-titres dans la langue choisie par les instructeurs. Les participants ne peuvent pas modifier la langue des sous-titres.

## Comment Live Hub détermine la langue des sous-titres

Live Hub sélectionne automatiquement la langue des sous-titres en fonction de l’ordre de priorité suivant :

1. **Langue du cours :** Live Hub utilise la langue du cours si elle est prise en charge pour les légendes. Pour un cours multilingue, si l&#39;instance de cours actuelle utilise une langue qui ne prend pas en charge les sous-titres, Live Hub sélectionne la langue de la première instance de cours qui prend en charge les sous-titres. Pour plus d&#39;informations, consultez [Langues prises en charge dans ALM](../../migrated/languages-supported.md).
1. **Langue du compte :** si la langue du cours n&#39;est pas prise en charge, Live Hub vérifie la langue du compte et l&#39;utilise si elle est prise en charge.

>[!NOTE]
>
>Si ni la langue du cours ni la langue du compte n’est prise en charge, Live Hub sélectionne l’anglais comme langue de légende. En outre, les sous-titres sont désactivés par défaut et doivent être activés manuellement.

## Langues prises en charge pour les sous-titres

Live Hub prend en charge les sous-titres dans les langues suivantes :

* Anglais
* Français
* Allemand
* Chinois
* Espagnol
* Italien
* Japonais
* Portugais
* Danois
* Néerlandais
* Finnois
* Turc
* Coréen
* Norvégien
* Suédois
* Russe

## Fonctionnement des sous-titres

Dans une session Live Hub, les sous-titres sont générés automatiquement. Les sous-titres s’affichent dans un panneau dédié et sont mis à jour en permanence pendant que les participants parlent. Les instructeurs et les élèves peuvent afficher les légendes.

Chaque participant peut afficher ou masquer les sous-titres selon ses préférences. La modification de ce paramètre n’affecte pas les autres participants.

![](assets/closed-captions-overview.png)
*Interface Live Hub affichant les sous-titres dans la session*

## Rôles et autorisations

La fonctionnalité de **sous-titres** est disponible pour les instructeurs et les élèves dans une session Live Hub. Les actions disponibles varient en fonction du rôle de l’utilisateur.

| **Instructeurs** | **Élèves** |
|---|---|
| [Afficher les sous-titres](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#display-closed-captions) | [Afficher les sous-titres](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#display-closed-captions) |
| [Modifier l’apparence des sous-titres](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#change-the-appearance-of-closed-captions) | [Modifier l’apparence des sous-titres](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#change-the-appearance-of-closed-captions) |
| [Sélectionner la langue des sous-titres](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#select-the-caption-language) | |