---
title: Création et personnalisation de menus dans Experience Builder
description: Ce guide explique comment les administrateurs peuvent créer des menus dans Experience Builder dans Adobe Learning Manager. Apprenez à organiser les pages en menus, à personnaliser la mise en page des menus et à contrôler la visibilité des menus pour différents groupes d’utilisateurs.
jcr-language: en-us
source-git-commit: 85eeebb33a67bf5528c88b26941345e00e98e0d3
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---


# Création d’un menu

En tant qu’administrateur d’une société financière comptant deux équipes principales, les directeurs commerciaux et les directeurs de la réussite client (CSM), vous devez créer des menus distincts avec leurs pages respectives. Cela permet aux élèves de trouver facilement des cours pertinents pour leurs rôles dans leur propre menu.

Par défaut, les administrateurs peuvent voir le menu par défaut sur la page **[!UICONTROL Menu]**, qui ne peut pas être supprimée. Ce menu inclut toutes les pages intégrées actuellement visibles dans l’application de l’élève.

Pour créer un menu :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Menu]**, puis **[!UICONTROL Créer]**.

   ![](assets/select-create-menu.png)
   _Écran de menu affichant des options pour afficher, organiser et créer des menus personnalisés pour différents groupes d’élèves_

4. Saisissez le **[!UICONTROL nom du menu]** (par exemple, Formation sur le produit) et sélectionnez le groupe d&#39;utilisateurs dans l&#39;option **[!UICONTROL Visible pour]**.

   ![](assets/type-menu-name-and-users.png)
   _Écran Créer un menu, où les administrateurs peuvent saisir un nom de menu pour une utilisation interne et spécifier des groupes d&#39;utilisateurs pour contrôler la visibilité du menu_

5. Voici le type de pages disponibles dans le menu :
   * **[!UICONTROL Pages intégrées]** : il s’agit des pages par défaut fournies avec Adobe Learning Manager, telles que Accueil, Mon apprentissage et Catalogue. Les administrateurs ne peuvent pas supprimer les pages intégrées du menu. Ils peuvent masquer les pages du menu.
   * **[!UICONTROL Pages personnalisées]** : il s’agit de pages créées par l’administrateur à l’aide d’Experience Builder. Les pages personnalisées permettent aux organisations de concevoir des expériences de marque, spécifiques à des rôles ou basées sur des événements en ajoutant des widgets, des mises en page et des menus adaptés à différents groupes d’élèves.
6. Sélectionnez **[!UICONTROL Modifier]** en regard de **[!UICONTROL Page de destination]** pour mettre à jour la page de destination de l’élève.

   ![](assets/change-landing-page.png)
   _Écran de configuration du menu affichant l’option permettant de sélectionner des pages pour modifier la page de destination de l’interface de l’élève_

7. Choisissez la page personnalisée dans l&#39;option **[!UICONTROL Sélectionner des pages]**. Les administrateurs doivent pouvoir sélectionner uniquement les pages personnalisées publiées, et non celles à l’état de brouillon.

   ![](assets/select-custom-pages.png)
   _Écran de sélection de page, mettant en évidence l&#39;option permettant d&#39;inclure la page personnalisée pour les groupes d&#39;utilisateurs et de personnaliser l&#39;ordre des menus_

8. Faites glisser et déposez pour réorganiser les pages dans le menu.
9. Sélectionnez **[!UICONTROL Menu Aperçu]** pour afficher le menu avant de l&#39;enregistrer.
10. Sélectionnez **[!UICONTROL Enregistrer]**.

Le menu créé sera visible pour les élèves sélectionnés. Ils peuvent accéder aux pages personnalisées via leur interface utilisateur d’élève.

![](assets/preview-the-menu.png)
_L’interface utilisateur des élèves affiche la page personnalisée avec les modules de formation proposés et une navigation facile à partir du menu de la barre latérale_

## Création d’un sous-menu

Les administrateurs peuvent créer un sous-menu dans le menu et y ajouter des pages personnalisées. Les sous-menus n’ont pas de page de destination.

Pour créer un sous-menu :

1. Sélectionnez **[!UICONTROL Créer un sous-menu]** dans la page **[!UICONTROL Configuration de menu]**.

   ![](assets/create-submenu-option.png)
   _Pages de configuration de menu mettant en évidence l’option Créer un sous-menu pour créer des sous-menus pour les élèves_

2. Sélectionnez la langue et saisissez le titre du sous-menu.
3. Sélectionnez une icône à afficher en regard du sous-menu.
4. Sélectionnez **[!UICONTROL Ajouter une nouvelle langue]** pour créer le même sous-menu pour différentes langues. Par exemple, si vous ajoutez l’anglais et le français, les élèves dont la langue de l’interface est l’anglais sélectionnée verront le sous-menu Anglais, tandis que les élèves dont le français est sélectionné verront le sous-menu Français.

   ![](assets/create-submenu-prompt.png)
   _Invite de sous-menu affichant des options pour sélectionner le titre, la langue et l&#39;icône du sous-menu à afficher dans le menu_

5. Sélectionnez **[!UICONTROL Continuer]**.
6. Faites glisser et déposez les pages sous le sous-menu.

## Configuration de pages masquées

L&#39;option **[!UICONTROL Masquer les pages]** permet aux administrateurs de nettoyer l&#39;interface utilisateur des élèves en affichant moins de pages. Les administrateurs peuvent masquer des pages du menu afin que les élèves ne les voient pas dans l&#39;interface utilisateur des élèves, mais les élèves peuvent toujours accéder à ces pages par d&#39;autres moyens. Par exemple, la page Catalogue peut être masquée dans le menu, mais accessible via la page d’accueil de l’élève.

![](assets/select-hidden-pages.png)
_Écran de configuration du menu affichant les pages masquées telles que le catalogue, l’apprentissage par les réseaux sociaux, les compétences et les badges_

>[!NOTE]
>
>Les pages d’un sous-menu ne peuvent pas être masquées directement. Pour masquer une page, faites-la glisser en dehors du sous-menu, puis masquez-la.

## Étape suivante

Après avoir configuré des pages, des widgets et des menus, améliorez l’expérience globale de l’élève en ajoutant des personnalisations à l’aide de JavaScript et CSS.

