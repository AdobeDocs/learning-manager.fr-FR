---
jcr-language: en_us
title: Problèmes liés au retrait d’un programme d’apprentissage
description: Problèmes liés au retrait d’un programme d’apprentissage dans Adobe Learning Manager
contentowner: nluke
exl-id: 706cafe3-2650-4837-9dee-e381a4a711f9
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 55%

---

# Problèmes liés au retrait d’un programme d’apprentissage

## Problème

Un programme d’apprentissage est automatiquement retiré.

## Cause

Dans certaines situations, un programme d’apprentissage est retiré sans qu’un administrateur/auteur ait explicitement demandé ce retrait.

Ce problème vient du fait qu’un programme d’apprentissage représente un ensemble de cours. Les formations de niveau supérieur sont retirées si l’un de leurs cours contient une instance qui a été retirée, ou si l’instance du cours est retirée.

## Résolution

Pour vérifier le cours contenant une instance qui a été retirée, procédez comme suit :

1. Connectez-vous en tant qu’administrateur et lancez le programme d’apprentissage correspondant.

1. Cliquez sur **[!UICONTROL Instances]** > **CCours**. La page répertorie tous les cours qui font partie de ce programme d’apprentissage. Vous pourrez voir le cours qui contient une instance retirée.

   ![](assets/retired-instance.png)

   *Afficher la liste de tous les cours*

1. Une fois que vous avez déterminé quelle instance de cours a été retirée, cliquez sur **[!UICONTROL Cours]** > **[!UICONTROL Ouvrir le cours]**.

1. Cliquez sur **[!UICONTROL Instances]**. Sur l&#39;instance retirée, cliquez sur **[!UICONTROL Modifier]**, puis modifiez la date d&#39;achèvement en choisissant une date ultérieure à laquelle vous souhaitez retirer l&#39;instance.

   ![](assets/completion-date.png)

   *Modifier la date d&#39;achèvement d&#39;un cours*

1. Lorsque vous avez terminé, cliquez sur la liste déroulante comme indiqué dans l’image ci-dessous. Cliquez ensuite sur **[!UICONTROL Rouvrir l’instance]**.

   ![](assets/re-open-instance.png)

   *Rouvrir l&#39;instance d&#39;un cours*

1. Consultez le programme d’apprentissage correspondant. Cliquez sur **[!UICONTROL Instances]** et exécutez l’étape précédente pour rouvrir l’instance du programme d’apprentissage.
