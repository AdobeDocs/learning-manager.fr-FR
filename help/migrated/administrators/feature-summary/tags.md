---
description: Découvrez comment gérer les balises dans Learning Manager.
jcr-language: en_us
title: Balises
contentowner: dvenkate
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---



# Balises

Les administrateurs peuvent désormais gérer les balises dans Learning Manager. Utilisez un meilleur balisage et une base de données gérable pour aider les élèves à mieux rechercher et à accéder rapidement aux résultats de recherche appropriés. Vous pouvez gérer les balises redondantes, mal orthographiées et non pertinentes à l’aide de cette fonction. Vous pouvez également ajouter, modifier, supprimer, ajouter ou remplacer des balises.

La liste des objets d’apprentissage associés à la balise peut être affichée en cliquant sur le nombre indiqué en regard de chaque balise. La liste affiche le nombre de cours, de programmes d&#39;apprentissage, de certificats, d&#39;assistances à la tâche et de groupes de contenus. Cliquez sur l’une de ces options pour afficher la liste.

Vous pouvez trier les balises en fonction de leur utilisation ou de leur ordre alphabétique à l’aide de la commande **[!UICONTROL Trier par]** option.

## Ajouter/Supprimer/Modifier des balises {#adddeleteedittags}

1. En tant qu’administrateur, dans le volet de navigation de gauche, cliquez sur **[!UICONTROL Balises]**. Le **[!UICONTROL Tag Management]** la page s’ouvre.
1. Pour ajouter une nouvelle balise, cliquez sur **[!UICONTROL Ajouter]**. Le bouton Ajouter est disponible dans le coin supérieur droit de la page. S’il n’existe aucune balise existante, le **[!UICONTROL Ajouter]** sera également disponible au milieu du **[!UICONTROL Tag Management]** page.

   Lors de l’ajout de plusieurs balises, séparez-les à l’aide des balises (,) ou (;). Un nom de balise peut contenir jusqu’à 50 caractères.

1. Pour supprimer une balise existante, sélectionnez-la en cochant la case. Vous pouvez sélectionner plusieurs balises jusqu’à cinquante à supprimer à la fois. Pour supprimer, procédez comme suit :

   * Sélectionnez les balises à supprimer > ouvrez le panneau **[!UICONTROL Action]** menu déroulant > sélectionner **[!UICONTROL Supprimer]**.

1. Une seule balise peut être modifiée à la fois. Pour modifier une balise, procédez comme suit :

   * Sélectionnez la balise à modifier > ouvrir le **[!UICONTROL Actions]**menu déroulant > cliquez sur **[!UICONTROL Modifier]**.

   Le **[!UICONTROL Modifier la balise]** s’affiche. Entrez le nouveau nom de balise et cliquez sur **[!UICONTROL Enregistrer]**.

   Si le nom de balise que vous avez entré existe déjà, Adobe Learning Manager affiche un message d’avertissement. Il ne peut pas y avoir deux balises portant le même nom.

## Remplacer les balises {#replacetags}

1. Sélectionnez les balises à remplacer. Vous pouvez sélectionner jusqu’à 50 balises à la fois. Ouvrez le panneau **[!UICONTROL Actions]** menu déroulant et sélectionnez **[!UICONTROL Remplacer]**.
1. Le **[!UICONTROL Remplacer les balises]** s’affiche avec les balises sélectionnées.

1. Dans le panneau **[!UICONTROL Nom des balises remplacées]** , saisissez le nom de la nouvelle balise par laquelle vous souhaitez remplacer les balises sélectionnées. Vous pouvez les remplacer par une balise existante dans la liste déroulante ou ajouter une nouvelle balise.

   Un point-virgule ou une virgule ne peut pas faire partie du nom de la balise.  Notez que les balises sans point-virgule et l’affichage des messages d’erreur lors de l’utilisation de telles balises dans le cadre de certains objets d’apprentissage ne sont pas traités pour les scénarios de migration.

1. Cliquez sur **[!UICONTROL Remplacer]**.

## Ajouter des balises {#appendtags}

Dans le cas d’une opération d’ajout de balises, la balise nouvelle/existante est ajoutée à toutes les listes d’objets d’apprentissage et de groupes de contenus associés aux balises sélectionnées.

1. Sélectionnez les balises à ajouter. Vous pouvez sélectionner jusqu’à 50 balises à la fois. Ouvrez le menu déroulant Actions et sélectionnez **[!UICONTROL Ajouter]**.
1. Le  **[!UICONTROL Ajouter des balises]** s’affiche avec les balises sélectionnées.
1. Vous pouvez ajouter une balise supplémentaire à tous les apprentissages avec les balises sélectionnées en saisissant le nom de la balise **[!UICONTROL Nouvelle balise]** ou dans la liste déroulante des balises existantes. La nouvelle balise sera ajoutée à tous les éléments d’apprentissage associés dans Learning Manager.

   Un point-virgule ou une virgule ne peut pas faire partie du nom de la balise. S’il est utilisé, Prime affichera un message d’erreur. Notez que les balises sans point-virgule et l’affichage des messages d’erreur lors de l’utilisation de telles balises dans le cadre de certains objets d’apprentissage ne sont pas traités pour les scénarios de migration.

1. Cliquez sur **[!UICONTROL Ajouter]**.

## Paramètres {#settings}

En tant qu’administrateur, vous pouvez autoriser l’auteur à créer des balises en cliquant sur l’option Paramètres.

![](assets/unknown-1.jpeg)

*Page Paramètres pour la création d’une balise*

* Lorsqu’un utilisateur est autorisé à créer des balises et sélectionne des balises existantes actuellement non valides,

  Un message d’erreur s’affiche, suggérant que la balise sélectionnée n’est plus valide. Les nouvelles balises seront créées en supprimant les caractères non pris en charge. Dans ce cas, l’auteur doit être en mesure de voir ses anciennes balises être remplacées par de nouvelles balises avant d’enregistrer.

* Si l’utilisateur ne dispose pas des autorisations nécessaires pour créer de nouvelles balises, un message d’erreur s’affiche pour indiquer que la balise sélectionnée n’est plus valide. Les auteurs peuvent contacter les administrateurs pour modifier les balises non valides.

  Les auteurs ne peuvent pas créer ou enregistrer de balises non valides. Ils peuvent supprimer les balises non valides et ajouter toute autre balise valide existante, puis continuer.
