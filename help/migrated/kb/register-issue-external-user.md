---
jcr-language: en_us
title: Inscription impossible en tant qu’utilisateur externe
description: Les élèves externes ne peuvent pas s’inscrire à un profil dans Adobe Learning Manager.
contentowner: nluke
exl-id: b1a9ecb6-75a8-44f7-b169-f77d7a4f6c2c
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 50%

---

# Inscription impossible en tant qu’utilisateur externe

## Problème

Les élèves externes ne peuvent pas s’inscrire à un profil.

## Erreur

Cet ID de messagerie est déjà enregistré. Veuillez utiliser une autre adresse électronique.

![](assets/cp-register-profile.png)

*Message d’erreur d’un e-mail déjà enregistré*

## Description

Dans certains cas, un utilisateur ne peut pas s’inscrire à un profil externe. L’utilisateur reçoit l’erreur ci-dessus lors de l’inscription.

## Cause

Ce problème se produit dans l’un des cas suivants :

* L’utilisateur est déjà inscrit à un autre profil externe.
* L’utilisateur est déjà un élève interne.
* L’utilisateur est dans un état supprimé.

## Résolution :

**Scénario 1:** L&#39;utilisateur est déjà inscrit à un autre profil externe.

1. Connectez-vous en tant qu’administrateur.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Externe]**.
1. Ouvrez le profil dont l’utilisateur fait déjà partie en cliquant sur Places utilisées

   ![](assets/cp-seats-used.png)

   *Ouvrir le profil de l&#39;utilisateur*

1. Sélectionnez l&#39;utilisateur, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Modifier le profil]**.

   ![](assets/cp-change-profile.png)

   *Modifier le profil de l&#39;utilisateur*

   Une fenêtre s’ouvre alors pour sélectionner un nouveau profil comme illustré ci-dessous.

   ![](assets/cp-select-profiles.png)

   *Sélectionner un profil utilisateur*

1. Une fois la sélection effectuée, cliquez sur **[!UICONTROL Modifier]**.

**Scénario 2:** L&#39;utilisateur est présent en tant qu&#39;élève interne.

1. Connectez-vous en tant qu’administrateur.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Interne]**.
1. Cliquez pour ouvrir un profil d’élève et cliquez sur l’icône Modifier.

   ![](assets/cp-internal-learner.png)

   *Ouvrir un profil d&#39;élève interne*

1. Modifiez l’adresse e-mail de l’élève ou ajoutez *_old* à l’adresse e-mail existante. L’adresse e-mail sera ainsi libérée.

   Par exemple, si l’adresse e-mail de l’élève est *<abc@adobe.com>,* remplacez-la par *<abc_old@adobe.com>*

1. Cliquez sur **Enregistrer** pour conserver les modifications apportées.

**Scénario 3** : L’utilisateur est dans un état supprimé.

1. Connectez-vous en tant qu’administrateur.
1. Sous **Gérer**, cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Nettoyage utilisateur]**.
1. Sélectionnez l’élève et cliquez sur l’icône Modifier.

   ![](assets/cp-deleted-learner.png)

   *Modifier l&#39;adresse e-mail de l&#39;utilisateur*

1. Modifiez l’adresse e-mail de l’élève ou ajoutez *_old* à l’adresse e-mail existante. L’adresse e-mail sera ainsi libérée.

   Par exemple, si l’adresse électronique de l’élève est **<abc@adobe.com>**, remplacez-la par **<abc_old@adobe.com>**.
