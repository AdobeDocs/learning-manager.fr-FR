---
title: Rôle personnalisé avec autorisations d'annonce étendues
jcr-language: en_us
description: Découvrez comment créer un rôle personnalisé dans Adobe Learning Manager qui autorise les annonces uniquement pour les catalogues et les groupes d'utilisateurs sélectionnés.
source-git-commit: 85eeebb33a67bf5528c88b26941345e00e98e0d3
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# Rôle personnalisé avec autorisations d&#39;annonce étendues

Les administrateurs peuvent créer des rôles personnalisés avec des autorisations d&#39;annonce limitées à des catalogues et des groupes d&#39;utilisateurs spécifiques. Cela permet de s&#39;assurer que les annonces sont ciblées, pertinentes et visibles uniquement par les élèves prévus. Les annonces limitées garantissent que les bons utilisateurs reçoivent les annonces pertinentes sans envoyer de détails à d&#39;autres personnes.

## Créer un rôle personnalisé avec une portée spécifique

L’administrateur peut créer un rôle personnalisé avec des autorisations d’annonce limitées à un catalogue et un groupe d’utilisateurs spécifiques.

Pour créer un rôle personnalisé avec une portée spécifique :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Utilisateurs]** dans le volet de navigation de gauche.

   ![](assets/select-uses-admin.png)
   _Attribuer des rôles personnalisés aux utilisateurs pour des autorisations et des responsabilités ciblées dans Adobe Learning Manager_

3. Sélectionnez Rôles personnalisés.
4. Sélectionnez Créer un rôle personnalisé.

   ![](assets/create-custom-roles.png)
   _Attribuez des rôles personnalisés aux utilisateurs pour personnaliser les autorisations et rationaliser le contrôle administratif pour des groupes d&#39;utilisateurs ou des catalogues spécifiques_

5. Saisissez le nom et la description du rôle personnalisé.
6. Sélectionnez Annonce sous Privilèges de compte.

   ![](assets/select-announcement.png)
   _Activez les autorisations d&#39;annonce sous Privilèges de compte pour permettre aux administrateurs personnalisés de gérer les communications ciblées dans la portée_

7. Sélectionnez Définir l’accès par catalogue sous Portée des privilèges de fonctionnalité et sélectionnez le catalogue.
8. Dans la même section, choisissez Définir l’accès par groupe d’utilisateurs et sélectionnez les
groupe d’utilisateurs.

   ![](assets/select-scope-announcement.png)
   _Définissez des portées de groupe d&#39;utilisateurs et de catalogue pour vous assurer que les administrateurs personnalisés peuvent gérer les autorisations et l&#39;accès uniquement dans les portées qui leur sont attribuées_

9. Sélectionnez et ajoutez l’utilisateur auquel vous souhaitez attribuer ce rôle personnalisé. Les utilisateurs affectés peuvent créer une annonce pour leur portée.

Un administrateur personnalisé peut créer des annonces limitées aux groupes d&#39;utilisateurs et aux catalogues qui lui sont attribués, ce qui garantit que les messages atteignent le bon public et empêche les notifications inutiles. Pour les notifications et les annonces par e-mail, les administrateurs peuvent ajouter des groupes d&#39;utilisateurs supplémentaires, mais seuls les utilisateurs faisant partie de la portée définie les recevront. Pour les annonces Recommandation et En-tête, vous pouvez uniquement sélectionner des groupes d&#39;utilisateurs dans la portée affectée.

## Créer une annonce pour la portée affectée

Un administrateur personnalisé peut créer des annonces limitées aux groupes d&#39;utilisateurs et aux catalogues qui lui sont attribués, ce qui garantit que les messages atteignent le bon public et empêche les notifications inutiles.

Pour créer une annonce pour la portée affectée :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur personnalisé.
2. Sélectionnez **[!UICONTROL Annonce]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Ajouter]**.

   ![](/help/migrated/assets/create-add-announcement.png)
   _Page Annonces dans Adobe Learning Manager, où les administrateurs peuvent créer et gérer des annonces pour des groupes d&#39;utilisateurs ciblés_

4. Sélectionnez le **[!UICONTROL Type d&#39;annonce]** dans le menu déroulant.
a. **[!UICONTROL En tant que notification]**
b. **[!UICONTROL En tant qu&#39;en-tête]**
c. **[!UICONTROL Comme recommandation]**
d. **[!UICONTROL Comme e-mail]**
5. Sélectionnez **[!UICONTROL En Tant Qu&#39;En-Tête]**.
6. Sélectionnez la langue et chargez une image pour l’en-tête.
7. Ajoutez éventuellement une URL pour le bouton d’action.

   ![](/help/migrated/assets/announcement-screen.png)
   _Écran Créer une annonce permettant aux administrateurs de définir le type d&#39;annonce, de télécharger des pièces jointes et d&#39;ajouter des boutons d&#39;action_

   La portée affectée est présélectionnée dans la section **[!UICONTROL Portée]** et ne peut pas être modifiée par les administrateurs personnalisés.

   >[!NOTE]
   >
   >**[!UICONTROL Pour les notifications]** et les annonces **[!UICONTROL par e-mail]**, ils peuvent inclure des groupes d&#39;utilisateurs et des catalogues supplémentaires si ceux-ci chevauchent leur portée attribuée.

8. Sélectionnez **[!UICONTROL Enregistrer]**.

Seuls les élèves relevant de la portée de l’administrateur personnalisé pourront afficher l’annonce. Consultez cet [article](/help/migrated/administrators/feature-summary/announcements.md) pour apprendre à créer plusieurs types d&#39;annonces.

## Réinitialiser l’étendue par les administrateurs personnalisés

Les administrateurs personnalisés peuvent réinitialiser la portée de leurs annonces publiées si un administrateur a modifié la portée de celles-ci. Une fois la portée réinitialisée, la portée mise à jour sera appliquée à l’annonce et seuls les élèves de la nouvelle portée pourront voir l’annonce.

Pour réinitialiser l’étendue :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur personnalisé.
2. Sélectionnez **[!UICONTROL Annonce]** dans le volet de navigation de gauche.
3. Sélectionnez l&#39;onglet **[!UICONTROL Publié]**.
4. Sélectionnez une annonce, puis cliquez sur l’icône des paramètres.
5. Sélectionnez **[!UICONTROL Modifier]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Écran d’annonce affichant les annonces publiées avec les options Modifier, Publier et autres_

6. Sélectionnez **Réinitialiser**.

   ![](/help/migrated/assets/reset-the-scope.png)
   _Annonce affichant une notification de modification de la portée, avec une option permettant aux administrateurs personnalisés de réinitialiser et de mettre à jour la sélection de la portée pour refléter les nouvelles autorisations d&#39;accès_

La portée sera mise à jour et seuls les utilisateurs de la portée mise à jour pourront afficher l&#39;annonce.

## Modifier l’annonce via l’interface utilisateur de l’administrateur

Les administrateurs peuvent modifier et gérer toutes les annonces créées par les administrateurs personnalisés. Si un administrateur tente de modifier une annonce créée par un administrateur personnalisé avec une portée spécifique, un message d&#39;avertissement s&#39;affiche sur l&#39;annonce indiquant **[!UICONTROL Supprimer]** la portée. L&#39;administrateur peut supprimer l&#39;étendue pour rendre l&#39;annonce disponible pour tout le monde. Dans ce cas, l&#39;administrateur personnalisé reçoit un avertissement indiquant que la portée de l&#39;annonce a été modifiée.

Pour modifier l&#39;annonce via l&#39;interface utilisateur de l&#39;administrateur :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Annonce]** dans le volet de navigation de gauche.
3. Sélectionnez l&#39;onglet **[!UICONTROL Publié]**.
4. Sélectionnez une annonce, puis cliquez sur l’icône des paramètres.
5. Sélectionnez **[!UICONTROL Modifier]**.

   ![](/help/migrated/assets/select-edit-published-announcement.png)
   _Écran d’annonce affichant les annonces publiées avec les options Modifier, Publier et autres_

6. Sélectionnez **[!UICONTROL Supprimer]**.

   ![](/help/migrated/assets/remove-the-scope.png)
   _Écran d&#39;annonce indiquant que la portée doit être supprimée pour permettre aux administrateurs de modifier les annonces créées pour les groupes d&#39;utilisateurs dont la portée est limitée_

L’administrateur peut modifier l’annonce après avoir supprimé l’étendue.
