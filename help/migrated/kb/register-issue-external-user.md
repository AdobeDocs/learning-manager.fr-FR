---
jcr-language: en_us
title: Impossible de s’inscrire en tant qu’utilisateur externe
description: Les élèves externes ne peuvent pas s’inscrire à un profil dans Adobe Learning Manager.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---



# Impossible de s’inscrire en tant qu’utilisateur externe

## Problème

Les élèves externes ne peuvent pas s&#39;inscrire à un profil.

## Erreur

L’ID de messagerie est déjà enregistré. Veuillez utiliser une autre adresse e-mail.

![](assets/cp-register-profile.png)

*Message d’erreur d’un e-mail déjà enregistré*

## Description

Dans certains cas, un utilisateur ne peut pas s’inscrire à un profil externe. L’utilisateur reçoit l’erreur ci-dessus lors de l’inscription.

## Cause

Ce problème se produit dans l’un des scénarios suivants :

* L’utilisateur est déjà inscrit à un autre profil externe.
* L’utilisateur est déjà un élève interne.
* L’utilisateur est dans un état supprimé.

## Résolution :

**Scénario 1 :** L’utilisateur est déjà inscrit à un autre profil externe.

1. Connectez-vous en tant qu’administrateur.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Externe]**.
1. Ouvrez le profil dont l’utilisateur fait déjà partie en cliquant sur Places utilisées.

   ![](assets/cp-seats-used.png)

   *Ouvrir le profil de l’utilisateur*

1. Sélectionnez l’utilisateur, puis cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Modifier le profil]**.

   ![](assets/cp-change-profile.png)

   *Modifier le profil de l’utilisateur*

   Cela ouvre une fenêtre pour sélectionner un nouveau profil comme ci-dessous.

   ![](assets/cp-select-profiles.png)

   *Sélectionner un profil utilisateur*

1. Une fois sélectionné, cliquez sur **[!UICONTROL Modifier]**.

**Scénario 2 :** L’utilisateur est présent en tant qu’élève interne.

1. Connectez-vous en tant qu’administrateur.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Interne]**.
1. Cliquez pour ouvrir un profil d’élève et cliquez sur l’icône Modifier.

   ![](assets/cp-internal-learner.png)

   *Ouverture d’un profil d’élève interne*

1. Modifier l’adresse e-mail de l’élève ou ajouter *_old* à l’adresse e-mail existante. L’adresse e-mail sera ainsi libérée.

   Par exemple, si l’adresse électronique de l’élève est *<abc@adobe.com>,* remplacer par *<abc_old@adobe.com>*

1. Cliquez sur **Enregistrer** pour conserver les modifications apportées.

**Scénario 3**: l’utilisateur est dans un état supprimé.

1. Connectez-vous en tant qu’administrateur.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Nettoyage de l’utilisateur]**.
1. Sélectionnez l’élève et cliquez sur l’icône Modifier.

   ![](assets/cp-deleted-learner.png)

   *Modifier l’adresse e-mail de l’utilisateur*

1. Modifier l’adresse e-mail de l’élève ou ajouter *_old* à l’adresse e-mail existante. L’adresse e-mail sera ainsi libérée.

   Par exemple, si l’adresse électronique de l’élève est **<abc@adobe.com>**, remplacez-le par **<abc_old@adobe.com>**.
