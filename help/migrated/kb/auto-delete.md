---
jcr-language: en_us
title: L’utilisateur est automatiquement supprimé dans Learning Manager
description: Un utilisateur est supprimé de Learning Manager, mais l’administrateur n’a jamais effectué une telle action.
contentowner: nluke
source-git-commit: 3242a293fc4b2707044e11c342c984cbfb2fc434
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 55%

---



# L’utilisateur est automatiquement supprimé dans Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problème

A **utilisateur** est supprimé de Learning Manager, mais l’administrateur n’a jamais effectué une telle action.

## Cause

Dans Adobe Learning Manager, une option permet de supprimer un utilisateur s’il ne s’est pas connecté au système depuis un certain temps.

## Comment modifier/appliquer le paramètre ?

### Pour les élèves internes

1. Connectez-vous en tant qu’**administrateur**.
1. Sous **Configurer**, cliquez sur **Paramètres** > **Généralités**.
1. Dans la page Paramètres généraux, recherchez l’option **Supprimer automatiquement les utilisateurs internes**.
1. Cliquez sur **[!UICONTROL Modifier]** pour saisir le nombre de jours dans le champ, pour supprimer automatiquement un élève s’il n’a pas accédé au système.

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

1. Cliquez sur **[!UICONTROL Paramètres avancés]** en bas à gauche.

   ![](assets/cp-autodelete-external.png)

   *Sélectionnez l’option Paramètres avancés*

1. Dans le panneau **Configuration requise pour la connexion** champ, saisissez le nombre de jours pendant lesquels supprimer automatiquement un élève s’il n’a pas accédé au système.
1. Cliquez sur **[!UICONTROL Enregistrer]** pour conserver les paramètres définis.
