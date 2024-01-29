---
jcr-language: en_us
title: Attribution par défaut des rôles d’instructeur aux groupes d’utilisateurs dans Learning Manager
description: Attribution par défaut des rôles d’instructeur aux groupes d’utilisateurs dans Learning Manager
contentowner: nluke
preview: true
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---



# Attribution par défaut des rôles d’instructeur aux groupes d’utilisateurs dans Learning Manager

## Problème

Le rôle d’instructeur est attribué à tous les utilisateurs affectés à une session.

## Description

Dans certains cas, une session peut nécessiter plusieurs instructeurs ou un administrateur/auteur affecte un groupe d’utilisateurs à une session. Le rôle d’instructeur est ainsi attribué à tous les utilisateurs du groupe d’utilisateurs.

## Cause

Comme les rôles ne peuvent pas être embranchés lors de l’affectation en bloc d’utilisateurs dans un groupe d’utilisateurs, le rôle d’instructeur est attribué à tous les utilisateurs.

## Solution

Créez des groupes d’utilisateurs personnalisés pour filtrer les rôles d’utilisateurs attribués à une session. Pour supprimer les rôles d’instructeur attribués dans un groupe d’utilisateurs, effectuez les étapes suivantes :

1. Connectez-vous en tant qu’administrateur. Dans le panneau de gauche, cliquez sur **[!UICONTROL Modèles de courrier électronique]**.
1. Pour éviter les déclencheurs d’e-mail pour les modifications à apporter, cliquez sur **[!UICONTROL Tout désactiver]**.

   ![](assets/instructor-disable-all.png)

1. Accéder à **Utilisateurs** > **Groupe d’utilisateurs**. Cliquez sur **[!UICONTROL Ajouter]**.

   ![](assets/instructor-usergroups.png)

1. Créez un groupe d’utilisateurs personnalisé dans la fenêtre Ajouter un groupe d’utilisateurs comme suit :

   * Saisissez un nom pour le groupe personnalisé dans le champ **[!UICONTROL Nom]** champ.
   * Sous **[!UICONTROL Inclure les élèves]** , ajoutez le groupe d’utilisateurs pour lequel vous souhaitez filtrer les instructeurs.
   * Sous **[!UICONTROL Exclure des élèves]** , ajoutez les utilisateurs pour lesquels vous souhaitez conserver le rôle d’instructeur.

   ![](assets/instructor-add-ug.png)

   Les étapes ci-dessus créent une liste d’utilisateurs à ajouter dans le jeu d’inclusion et suppriment des utilisateurs spécifiques (instructeurs) mentionnés dans le jeu d’exclusion.

1. Cliquez sur **[!UICONTROL Enregistrer]** les modifications apportées.
1. Recherchez le groupe d’utilisateurs personnalisé créé en accédant à **[!UICONTROL Utilisateurs]** > **[!UICONTROL Interne]**.

   ![](assets/instructor-custom-ug.png)

1. Cochez la case pour sélectionner tous les utilisateurs du groupe.

   ![](assets/instructor-bulk-ug.png)

1. Cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Supprimer le rôle]** > **[!UICONTROL Supprimer un instructeur]**.

Assurez-vous que tous les déclencheurs d’e-mail désactivés à l’étape 2 sont réactivés une fois l’opération terminée.
