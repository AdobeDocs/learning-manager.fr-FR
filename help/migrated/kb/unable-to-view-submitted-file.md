---
jcr-language: en_us
title: Impossible d’afficher les envois de fichiers dans Adobe Learning Manager
description: Les instructeurs ne peuvent pas afficher les fichiers que les élèves ont chargés dans le module d’activité d’envoi.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 50%

---



# Impossible d’afficher les envois de fichiers dans Adobe Learning Manager

## Le problème

Un instructeur ne peut pas afficher les envois de fichiers chargées par un élève.

## Description

Les instructeurs ne peuvent pas afficher les fichiers que les élèves ont chargés dans le **module d&#39;activité d’envoi**.

Par exemple, un élève s&#39;était inscrit pour une instance nommée **Instance de test** d’un cours, comme indiqué ci-dessous :

![](assets/test-instance.png)

*Afficher l’instance*

L’élève ouvre ensuite le cours et charge un fichier dans le module Activité.

Lorsque l&#39;instructeur tente d&#39;approuver l’envoi, il n&#39;est pas en mesure de le faire.

![](assets/activity.png)

*Chargement d’un fichier dans le module Activité*

## Cause

S’il n’y a pas d’instructeur dans l’instance de cours dans laquelle l’élève est inscrit, le problème apparaît.

## Résolution

Pour vérifier si un instructeur est ajouté à l’instance de cours, procédez comme suit :

1. Accédez aux paramètres du cours.
1. Dans le panneau **Gérer** section, cliquez sur **[!UICONTROL Instances].**
1. Dans l’instance où l’élève est inscrit, cliquez sur **[!UICONTROL Sessions]**.

   ![](assets/check-instructor.png)

   *Sélectionnez Sessions dans l’instance*

   Aucun instructeur n’est affecté à cette session.

1. Cliquez sur **[!UICONTROL Modifier]**. Ajoutez l’instructeur qui approuve l’envoi du fichier.

   ![](assets/assign-instructor.png)

   *Ajouter l’instructeur*
1. Enregistrez les modifications.

