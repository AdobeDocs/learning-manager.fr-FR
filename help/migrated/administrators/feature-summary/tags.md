---
description: Découvrez comment gérer les balises dans Learning Manager
jcr-language: en_us
title: Balises
contentowner: dvenkate
exl-id: ea39d2a2-3d2b-43ae-8f8d-b97420b9d008
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 63%

---

# Balises

Les administrateurs peuvent désormais gérer les balises dans Learning Manager. Utilisez un meilleur balisage et une base de données gérable pour faciliter les recherches pour les élèves et obtenir des résultats de recherche appropriés plus rapidement. Vous pouvez gérer les balises redondantes, mal orthographiées et non pertinentes à l’aide de cette fonctionnalité. Vous pouvez également ajouter, modifier, supprimer, associer ou remplacer des balises.

La liste des objets d’apprentissage associés à la balise peut être affichée en cliquant sur le numéro fourni à côté de chaque balise. La liste affiche le numéro de cours, de programmes d’apprentissage, de certificats, d’assistances à la tâche et de groupes de contenu. Cliquez sur l’une de ces options pour afficher la liste.

Vous pouvez trier les balises en fonction de leur utilisation ou par ordre alphabétique à l’aide de l’option **[!UICONTROL Trier par]**.

## Présentation des balises

Cette formation vous apprendra à ajouter, modifier, remplacer, ajouter et supprimer des balises. Vous apprendrez également à modifier les paramètres d’autorisation et à utiliser les filtres de balise.

[![bouton](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318920)

Si vous ne pouvez pas lancer la formation, écrivez à <almacademy@adobe.com>.

## Ajout/Suppression/Modification de balises {#adddeleteedittags}

1. En tant qu’administrateur, sur le panneau de navigation gauche, cliquez sur **[!UICONTROL Balises]**. La page **[!UICONTROL Gestion des balises]** s’ouvre.
1. Pour ajouter une nouvelle balise, cliquez sur **[!UICONTROL Ajouter]**. Le bouton Ajouter est disponible en haut à droite de la page. S’il n’y a pas de balises existantes, le bouton **[!UICONTROL Ajouter]** s’affiche également au milieu de la page **[!UICONTROL Gestion des balises]**.

   Lors de l’ajout de plusieurs balises, séparez-les à l’aide de (,) ou de (;). Un nom de balise peut contenir un maximum de 50 caractères.

1. Pour supprimer une balise existante, sélectionnez la balise en cliquant sur la case à cocher. Vous pouvez sélectionner plusieurs balises jusqu’à cinquante à supprimer à la fois. Pour les supprimer, procédez comme suit :

   * Sélectionnez les balises à supprimer > ouvrez le menu déroulant **[!UICONTROL Action]** > sélectionnez **[!UICONTROL Supprimer]**.

1. Vous ne pouvez modifier qu’une seule balise à la fois. Pour modifier une balise, procédez comme suit :

   * Sélectionnez la balise à modifier > ouvrez le menu déroulant **[!UICONTROL Actions]**cliquez sur **[!UICONTROL Modifier]**.

   La boîte de dialogue **[!UICONTROL Modifier une balise]** s’affiche. Saisissez le nom de la nouvelle balise et cliquez sur **[!UICONTROL Enregistrer]**.

   Si le nom de balise saisi existe déjà, Adobe Learning Manager affiche un message d’avertissement. Deux balises ne peuvent pas porter le même nom.

## Remplacement des balises {#replacetags}

1. Sélectionnez les balises que vous voulez remplacer. Vous pouvez sélectionner jusqu’à 50 balises à la fois. Ouvrez le menu déroulant **[!UICONTROL Actions]** et sélectionnez **[!UICONTROL Remplacer]**.
1. La boîte de dialogue **[!UICONTROL Remplacer les balises]** apparaît et affiche les balises sélectionnées.

1. Dans l’option **[!UICONTROL Nom pour les balises remplacées]**, saisissez le nom de la nouvelle balise par laquelle vous souhaitez remplacer les balises sélectionnées. Vous pouvez les remplacer par une balise existante dans le menu déroulant ou ajouter une nouvelle balise.

   Un point-virgule ou une virgule ne peut pas faire partie du nom de la balise.  Notez que les balises sans point-virgule et l’affichage de messages d’erreur lors de l’utilisation de ces balises dans certains objets d’apprentissage ne seront pas traités pour les scénarios de migration.

1. Cliquez sur **[!UICONTROL Remplacer]**.

## Association de balises {#appendtags}

Dans le cas d’une opération d’ajout de balises, la balise nouvelle/existante est ajoutée à toutes les listes d’objets d’apprentissage et de groupes de contenus associés aux balises sélectionnées.

1. Sélectionnez les balises que vous voulez associer. Vous pouvez sélectionner jusqu’à 50 balises à la fois. Ouvrez le menu déroulant Actions et sélectionnez **[!UICONTROL Ajouter]**.
1. La boîte de dialogue **[!UICONTROL Ajouter des balises]** s&#39;affiche et indique les balises sélectionnées.
1. Vous pouvez associer une balise supplémentaire à tous les éléments d’apprentissage avec les balises sélectionnées en saisissant le nom de la **[!UICONTROL nouvelle balise]** ou dans la liste déroulante des balises existantes. La nouvelle balise sera associée à tous les éléments d’apprentissage dans Learning Manager.

   Les points-virgules ou les virgules ne peuvent pas faire partie du nom de balise. S’ils sont utilisés, Prime affichera un message d’erreur. Notez que les balises sans point-virgule et l’affichage de messages d’erreur lors de l’utilisation de ces balises dans certains objets d’apprentissage ne seront pas traités pour les scénarios de migration.

1. Cliquez sur **[!UICONTROL Associer]**.

## Paramètres {#settings}

En tant qu’administrateur, vous pouvez autoriser l’auteur à créer des balises en cliquant sur l’option Paramètres.

![](assets/unknown-1.jpeg)

*Page Paramètres pour la création d&#39;une balise*

* Lorsqu’un utilisateur est autorisé à créer des balises et sélectionne des balises existantes actuellement non valides,

  Un message d’erreur s’affiche, suggérant que la balise sélectionnée n’est plus valide. Les nouvelles balises seront créées en supprimant les caractères non pris en charge. Dans ce cas, l’auteur doit s’assurer que ses anciennes balises ont bien été modifiées avant de les enregistrer.

* Si l’utilisateur ne dispose pas des autorisations nécessaires pour créer de nouvelles balises, un message d’erreur s’affiche pour indiquer que la balise sélectionnée n’est plus valide. Les auteurs peuvent contacter l’administrateur pour modifier les balises non valides.

  Les auteurs ne peuvent pas créer ou enregistrer de balises non valides. Ils peuvent supprimer les balises non valides et ajouter toute autre balise valide existante, puis continuer.
