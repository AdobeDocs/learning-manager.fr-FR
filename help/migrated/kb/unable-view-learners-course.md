---
jcr-language: en_us
title: Impossible d’afficher les élèves dans un cours
description: L’onglet Élèves d’un cours n’affiche aucun élève inscrit à Adobe Learning Manager. Toutefois, si vous générez un rapport, vous pouvez afficher les élèves inscrits dans le rapport.
contentowner: saghosh
exl-id: 2ea54347-fa6b-493e-b73c-d350efb2aaaf
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 58%

---

# Impossible d’afficher les élèves dans un cours

## Problème

Vous ne pouvez pas afficher les élèves inscrits à un cours.

## Description

L’onglet Élèves d’un cours n’affiche aucun élève inscrit. Toutefois, si vous générez un rapport, vous pouvez afficher les élèves inscrits dans le rapport.

![](assets/no-learners.png)

*Aucun élève affiché*

## Cause

Si un élève est inscrit par le biais d’un objet d’apprentissage supérieur (programme d’apprentissage ou certification), l’élève sera visible sur l’onglet Élève de l’objet d’apprentissage supérieur. L’élève ne pourra pas être recherché sous l’onglet Élèves du cours.

**Comment afficher l’objet d’apprentissage supérieur auquel l’élève est inscrit ?**

Vous pouvez vérifier ces informations dans le rapport Relevés de notes de l’apprentissage. Pour générer un relevé de notes des élèves, procédez comme suit :

1. Connectez-vous en tant qu’administrateur.
1. Cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Relevé de notes de l’élève]**.

1. Entrez le nom de l&#39;**[!UICONTROL élève]** et spécifiez la plage **[!UICONTROL Date]**.
1. Développez la section **[!UICONTROL Options avancées]** et sélectionnez l’option **[!UICONTROL Activer les informations de niveau de module]**.
1. Cliquez sur **[!UICONTROL Générer]**.

   Dans la transcription de l’apprenant, vous pouvez afficher l’objet d’apprentissage par le biais duquel l’élève est inscrit.
