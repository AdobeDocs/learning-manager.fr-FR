---
jcr-language: en_us
title: Impossible d’acquérir une compétence après avoir suivi un cours
description: Même après avoir terminé un cours, un élève n’obtient pas de compétence. Les compétences attribuées à ce cours restent En cours pour l’élève.
contentowner: nluke
exl-id: d9c1e2a2-351d-4d6f-b2e6-f9e9278e6523
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 52%

---

# Impossible d’acquérir une compétence après avoir suivi un cours

## Problème

Même après avoir terminé un cours, un élève n’obtient pas de compétence. Les compétences attribuées à ce cours restent **En cours** pour l’élève.

## Cause

Ce problème se produit si les **crédits requis** pour acquérir cette compétence sont supérieurs aux **crédits acquis** par l’élève après avoir terminé le cours.

## Solution

Vérifiez les **crédits de compétence** et les **points** requis pour acquérir la compétence. Procédez comme suit :

1. Pour l’élève, générez un rapport **Relevé de notes de l’élève**.
1. Lors de la génération du relevé de notes de l&#39;élève, cliquez sur **[!UICONTROL Options avancées]** et cochez l&#39;option **[!UICONTROL Inclure les données de compétences et les fiches récapitulatives]**.

   ![](assets/advanced-options.png)

   *Sélectionnez l’option Inclure les données de compétences et les fiches récapitulatives*

1. Ouvrez le rapport Relevé de notes de l’élève téléchargé.
1. Accédez à la feuille **[!UICONTROL Relevé des compétences]**. Ici, vous pouvez afficher les **[!UICONTROL crédits requis]** et les **[!UICONTROL crédits acquis]** par l’élève.

   Dans l’exemple ci-dessous, les crédits requis pour acquérir la compétence pour un cours s’élèvent à 50. Mais l’élève n’a obtenu qu’un seul crédit.

   ![](assets/skill-transcript.png)

   *Afficher les crédits requis*

1. Pour vérifier les crédits qui sont attribués pour une compétence particulière, connectez-vous en tant qu’administrateur et accédez à **Compétences**, comme indiqué ci-dessous :

   ![](assets/skill.png)

   *Onglet Compétences de lancement*

1. Pour vérifier le nombre de crédits attribués à un cours, connectez-vous en tant qu’auteur et ouvrez le cours. Cliquez sur **[!UICONTROL Paramètres]** > **Compétences pédagogiques** comme indiqué ci-dessous :

   ![](assets/course-skills.png)

   *Afficher les compétences du cours*
