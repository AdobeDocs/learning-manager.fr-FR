---
description: En savoir plus sur la configuration des paramètres avancés dans Adobe Learning Manager
jcr-language: en_us
title: Paramètres avancés dans Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 34%

---


# Paramètres avancés dans Adobe Learning Manager

## Étiquettes de catalogue

Les étiquettes de catalogue dans Adobe Learning Manager sont utilisées pour baliser les objets d’apprentissage (cours, certifications, parcours d’apprentissage, etc.) avec des champs et des valeurs spécifiques. Ces étiquettes vous aident, vous et les auteurs, à classer et organiser efficacement le contenu, ce qui permet un meilleur filtrage, suivi et création de rapports.

Voir [Étiquettes de catalogue dans Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md) pour plus d&#39;informations.


>[!NOTE]
>
>* Libellés obligatoires : vous pouvez choisir de rendre les libellés de catalogue obligatoires pour les auteurs lors de la création du cours.
>* Flux de production des auteurs : les auteurs doivent ajouter des étiquettes de conformité lors de la création ou de la modification des cours pour garantir une catégorisation correcte.

## Dossier de contenu

Les dossiers de contenu vous permettent d’organiser et de gérer le contenu en créant des dossiers privés ou publics. Cette fonctionnalité garantit que le contenu est accessible uniquement à des auteurs ou des groupes spécifiques, offrant un meilleur contrôle sur la visibilité et la gestion du contenu.

**Points clés :**

Un dossier est un référentiel de contenu, qui est un sous-ensemble de la bibliothèque de contenu complète disponible dans un compte avec les propriétés suivantes :

* Vous seul (l’administrateur) pouvez créer, modifier ou supprimer un dossier.
* Vous pouvez contrôler l&#39;accès aux dossiers dans le cadre de la définition des rôles uniquement pour les administrateurs personnalisés.
* Le contenu doit toujours être associé à au moins un dossier. Pour commencer, tout le contenu sera associé au dossier public, qui peut être modifié par la suite.
* Le contenu peut être associé à plusieurs dossiers au moment de la création, ce qui est également possible par une opération de copie.
* Tous les noms de dossier doivent être uniques au sein du compte, faute de quoi une erreur s’affichera lors de la désignation d’un dossier.

Les dossiers contrôlent uniquement la visibilité du contenu et ne créent pas de copies de celui-ci. Par conséquent, la modification du contenu sera répercutée dans tous les dossiers associés.

**Dossier public**

Un dossier public est toujours présent dans un compte et tout le contenu sera initialement inclus dans ce dossier. Par la suite, les auteurs peuvent déplacer du contenu de ce dossier vers d’autres dossiers. Un dossier public possède les propriétés suivantes :

* Par défaut, tout le contenu associé à ce dossier sera accessible à tous les types d’auteurs.
* Tout contenu faisant partie d’un dossier public ne peut faire partie d’aucun autre dossier. L’inverse est également vrai.

Ce dossier ne peut pas faire partie de la définition de rôle configurable. Par conséquent, le fait de ne pas avoir de dossier public dans la définition de rôle configurable ne restreint pas l’accès à un dossier public.

**Dossier privé**

Tout dossier que vous créez est un dossier privé.

**Ajouter un dossier de contenu**

Pour ajouter un dossier de contenu, procédez comme suit :

1. Sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Dossier de contenu]**.
2. Sélectionnez **[!UICONTROL Ajouter]** pour créer un dossier.
3. Saisissez le nom et la description du dossier à créer.

   ![Texte optionnel](assets/advanced-settings-picture1.png)

4. Sélectionnez **[!UICONTROL Enregistrer]** pour créer le dossier.

**Opérations de dossier**

* **[!UICONTROL Ajouter un dossier]** : pour ajouter un dossier, sélectionnez le dossier, puis **[!UICONTROL Ajouter]** dans le coin supérieur droit de l&#39;écran.
* **[!UICONTROL Supprimer un dossier]** : pour supprimer un dossier, sélectionnez le dossier à supprimer, sélectionnez le menu **[!UICONTROL Actions]**, puis **[!UICONTROL Supprimer le dossier]**.

## Lieux de salles de classe

Créez et gérez une bibliothèque d’emplacements de salle de classe physique ou virtuelle. Ces emplacements peuvent être utilisés par les auteurs et les administrateurs pour configurer des événements de formation dirigée par un instructeur (ILT). Cette fonctionnalité garantit que les détails de la salle de classe, tels que les limites de places et les informations de localisation, sont préconfigurés et facilement accessibles.

Voir [Ajouter des emplacements de salle de classe dans Adobe Learning Manager](/help/migrated/administrators/feature-summary/classroom.md) pour plus d&#39;informations.

## Rapports

Cette section vous permet de configurer les tableaux de bord Conformité et Réussite du groupe.

![Texte optionnel](assets/advanced-settings-picture2.png)

Pour plus d’informations, voir les sections suivantes :

* [Tableau de bord Conformité](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Tableau de bord de réussite du groupe](/help/migrated/administrators/feature-summary/group-success-dashboard.md)


