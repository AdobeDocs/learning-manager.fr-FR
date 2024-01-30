---
jcr-language: en_us
title: Impossible d’acquérir une compétence après avoir suivi un cours
description: Même après avoir terminé un cours, un élève n’obtient pas de compétence. Les compétences attribuées à ce cours restent En cours pour l’élève.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 52%

---



# Impossible d’acquérir une compétence après avoir suivi un cours

## Problème

Même après avoir terminé un cours, un élève n’obtient pas de compétence. Les compétences attribuées à ce cours restent les suivantes : **En cours** pour l’élève.

## Cause

Ce problème se produit si **Crédits requis** pour atteindre cette compétence, il est plus important que **Crédits gagnés** par l’élève après avoir terminé le cours.

## Solution

Vérifier la **Crédits de compétences** et **Point** informations requises pour acquérir la compétence. Procédez comme suit :

1. Pour l’élève, générez un rapport **Relevé de notes de l’élève**.
1. Lors de la génération du relevé de notes de l’élève, cliquez sur **[!UICONTROL Options avancées]** et cochez l’option **[!UICONTROL Inclure les données sur les compétences et les fiches récapitulatives]**.

   ![](assets/advanced-options.png)

   *Sélectionnez l’option Inclure les données de compétences et les fiches récapitulatives*

1. Ouvrez le rapport Relevé de notes de l’élève téléchargé.
1. Accédez à la feuille **[!UICONTROL Relevé des compétences]**. Ici, vous pouvez voir le **[!UICONTROL Crédits requis]** et **[!UICONTROL Crédits gagnés]** par l’élève.

   Dans l’exemple ci-dessous, les crédits requis pour acquérir la compétence pour un cours s’élèvent à 50. Mais l’élève n’a obtenu qu’un seul crédit.

   ![](assets/skill-transcript.png)

   *Afficher les crédits requis*

1. Pour vérifier les crédits qui sont attribués pour une compétence particulière, connectez-vous en tant qu’administrateur et accédez à **Compétences**, comme indiqué ci-dessous :

   ![](assets/skill.png)

   *Lancer l’onglet Compétences*

1. Pour vérifier le nombre de crédits attribués à un cours, connectez-vous en tant qu’auteur et ouvrez le cours. Cliquez sur **[!UICONTROL Paramètres]** > **Compétences du cours** comme indiqué ci-dessous :

   ![](assets/course-skills.png)

   *Afficher les compétences du cours*
