---
jcr-language: en_us
title: Impossible d’afficher le calendrier
description: Lorsqu’un administrateur tente de modifier la date d’expiration d’un profil d’inscription externe et clique sur le calendrier pour modifier la date d’expiration, le calendrier ne s’affiche pas.
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---



# Impossible d’afficher le calendrier

## Problème

Vous ne pouvez pas afficher le calendrier lors de la modification de la date d’expiration d’un profil externe.

## Description

Lorsqu’un administrateur tente de modifier la date d’expiration d’un profil d’inscription externe et clique sur le calendrier pour modifier la date d’expiration, le calendrier ne s’affiche pas.

## Cause

Le problème se produit pour les raisons suivantes :

* Le niveau de zoom du navigateur est supérieur à 100 %.
* L’échelle et la disposition dans les paramètres d’affichage sont supérieures à 100 %.

## Résolution

### Navigateur

1. Lancez le navigateur.
1. Connectez-vous à Adobe Learning Manager.
1. Dans la barre d’adresses, cliquez sur l’icône de zoom.
1. Cliquez sur **[!UICONTROL Réinitialiser]**.
1. Modifiez la date d’expiration du profil d’inscription.

### Paramètres d’affichage

1. Cliquez sur **[!UICONTROL Début]** > **[!UICONTROL Paramètres]** > **[!UICONTROL Système]**.
1. Cliquez sur **[!UICONTROL Affichage]**.
1. Sous le **[!UICONTROL Échelle et disposition]** , utilisez la liste déroulante. Définissez les paramètres sur 100 %.

   ![](assets/scale-layout.png)

   *Modification des paramètres d’affichage*

1. Redémarrez l’ordinateur.
