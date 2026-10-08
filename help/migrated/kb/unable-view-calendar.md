---
jcr-language: en_us
title: Impossible d’afficher le calendrier
description: Lorsqu’un administrateur tente de modifier la date d’expiration d’un profil d’inscription externe et clique sur le calendrier pour modifier la date d’expiration, le calendrier ne s’affiche pas.
contentowner: saghosh
exl-id: 1b7e5594-714a-4a1d-9b8f-d481c1b48cb5
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 95%
---
# Impossible d’afficher le calendrier

## Problème

Vous ne pouvez pas afficher le calendrier lors de la modification de la date d’expiration d’un profil externe.

## Description

Lorsqu’un administrateur tente de modifier la date d’expiration d’un profil d’inscription externe et clique sur le calendrier pour modifier la date d’expiration, le calendrier ne s’affiche pas.

## Cause

Le problème se produit pour les raisons suivantes :

* Le niveau de zoom du navigateur est supérieur à 100 %.
* L’échelle et la disposition des paramètres d’affichage sont supérieures à 100 %.

## Résolution

### Navigateur

1. Lancez le navigateur.
1. Connectez-vous à Adobe Learning Manager.
1. Sur la barre d’adresses, cliquez sur l’icône de zoom.
1. Cliquez sur **[!UICONTROL Réinitialiser]**.
1. Modifier la date d’expiration du profil d’inscription.

### Paramètres d’affichage

1. Cliquez sur **[!UICONTROL Démarrer]** > **[!UICONTROL Paramètres]** > **[!UICONTROL Système]**.
1. Cliquez sur **[!UICONTROL Afficher]**.
1. Dans la section **[!UICONTROL Échelle et mise en page]**, utilisez la liste déroulante. Définissez les paramètres sur 100 %.

   ![](assets/scale-layout.png)

   *Modifier les paramètres d&#39;affichage*

1. Redémarrez l’ordinateur.
