---
jcr-language: en_us
title: L’utilisateur est automatiquement supprimé dans Learning Manager
description: Un utilisateur est supprimé de Learning Manager, mais l’administrateur n’a jamais effectué une telle action.
contentowner: nluke
exl-id: 9e293da3-bcbf-4798-b391-aef53ef8d946
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 61%

---

# L’utilisateur est automatiquement supprimé dans Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problème

Un utilisateur est supprimé de Learning Manager, mais l’administrateur n’a jamais effectué une telle action.

## Cause

Dans Adobe Learning Manager, une option permet de supprimer un utilisateur s’il ne s’est pas connecté au système depuis un certain temps.

## Comment modifier/appliquer le paramètre ?

### Pour les élèves internes

1. Connectez-vous en tant qu’**administrateur**.
1. Sous **Configurer**, cliquez sur **Paramètres** > **Général**.
1. Dans la page Paramètres généraux, recherchez l’option **Supprimer automatiquement les utilisateurs internes**.
1. Cliquez sur **[!UICONTROL Modifier]** pour saisir le nombre de jours dans le champ, afin de supprimer automatiquement un élève s&#39;il n&#39;a pas accédé au système.

   ![](assets/cp-autodelete-internal.png)

   *Modifier le nombre de jours*

>[!NOTE]
>
>   Laissez le champ vide si vous ne souhaitez pas supprimer automatiquement des utilisateurs.


1. Cliquez sur **[!UICONTROL Enregistrer]** pour conserver les paramètres définis.

### Pour les élèves externes :

1. Connectez-vous en tant qu’**administrateur**.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Externe]**.
1. Cliquez sur le nom d’un utilisateur externe pour lequel le paramètre doit être appliqué.

   La fenêtre **Modifier un profil d’inscription externe** s’ouvre.

1. Cliquez sur **[!UICONTROL Paramètres avancés]** dans le coin inférieur gauche.

   ![](assets/cp-autodelete-external.png)

   *Sélectionnez l&#39;option Paramètres avancés*

1. Dans le champ **Exigence de connexion**, entrez le nombre de jours pendant lesquels supprimer automatiquement un élève s&#39;il n&#39;a pas accédé au système.
1. Cliquez sur **[!UICONTROL Enregistrer]** pour conserver les paramètres définis.
