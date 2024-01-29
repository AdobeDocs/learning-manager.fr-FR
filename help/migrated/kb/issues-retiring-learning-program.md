---
jcr-language: en_us
title: Problèmes liés au retrait d’un programme d’apprentissage
description: Problèmes liés au retrait d’un programme d’apprentissage dans Adobe Learning Manager
contentowner: nluke
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---



# Problèmes liés au retrait d’un programme d’apprentissage

## Problème

Un programme d’apprentissage est automatiquement retiré.

## Cause

Dans certaines situations, un programme d’apprentissage a été retiré sans qu’un administrateur/auteur ait explicitement mis hors service le programme d’apprentissage.

Ce problème se produit car un programme d’apprentissage est un ensemble de cours. Les formations de niveau supérieur sont retirées si l’un de leurs cours contient une instance retirée ou si l’instance de cours est retirée.

## Résolution

Pour vérifier le cours qui contient une instance retirée, procédez comme suit :

1. Connectez-vous en tant qu’administrateur et lancez le programme d’apprentissage correspondant.

1. Cliquez sur **[!UICONTROL Instances]** > **Ccours**. La page répertorie tous les cours qui font partie de ce programme d’apprentissage. Vous pourrez voir le cours qui contient une instance retirée.

   ![](assets/retired-instance.png)

   *Afficher la liste de tous les cours*

1. Une fois que vous avez déterminé l’instance de cours qui a été retirée, cliquez sur **[!UICONTROL Cours]** > **[!UICONTROL Ouvrir le cours]**.

1. Cliquez sur **[!UICONTROL Instances]**. Sur l&#39;instance retirée, cliquez sur **[!UICONTROL Modifier]** puis modifiez la date d&#39;achèvement en choisissant une date ultérieure à laquelle vous souhaitez que l&#39;instance soit retirée.

   ![](assets/completion-date.png)

   *Modifier la date d&#39;achèvement d&#39;un cours*

1. Une fois l’opération terminée, cliquez sur la liste déroulante comme indiqué dans l’image ci-dessous. Cliquez ensuite sur **[!UICONTROL Rouvrir l’instance]**.

   ![](assets/re-open-instance.png)

   *Rouvrir l&#39;instance d&#39;un cours*

1. Consultez le programme d’apprentissage correspondant. Cliquez sur **[!UICONTROL Instances]** et exécutez l’étape précédente pour rouvrir l’instance du programme d’apprentissage.
