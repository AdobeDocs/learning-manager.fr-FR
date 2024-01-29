---
jcr-language: en_us
title: Impossible d’afficher les élèves dans un cours
description: L’onglet Élèves d’un cours n’affiche aucun élève inscrit à Adobe Learning Manager. Toutefois, si vous générez un rapport, vous pouvez afficher les élèves inscrits dans le rapport.
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

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

Vous pouvez vérifier ces informations dans le rapport Relevé de notes de l’apprentissage. Pour générer un relevé de notes de l’élève, procédez comme suit :

1. Connectez-vous en tant qu’administrateur.
1. Cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Relevé de notes de l’élève]**.

1. Entrez le nom de l’attribut **[!UICONTROL Élève]** et spécifiez les **[!UICONTROL Date]** plage.
1. Développer la section **[!UICONTROL Options avancées]** et sélectionnez l’option **[!UICONTROL Activer les informations au niveau du module]**.
1. Cliquez sur **[!UICONTROL Générer]**.

   Dans le relevé de notes de l’élève, vous pouvez afficher l’objet d’apprentissage par lequel l’élève est inscrit.
