---
jcr-language: en_us
title: Personnalisation d’un modèle de Report Builder dupliqué
description: Modifiez une copie d’un modèle de Report Builder Adobe Learning Manager pour qu’elle corresponde à vos besoins spécifiques en matière de colonnes, de filtres et de tri.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---


# Personnalisation d’un modèle de Report Builder dupliqué

Après avoir dupliqué un modèle, vous pouvez ajouter ou supprimer des colonnes, mettre à jour les filtres, renommer les colonnes et ajuster le tri avant d’enregistrer et de télécharger\. Cet article couvre chaque étape de personnalisation\.

Avant de commencer, dupliquez un modèle de l&#39;onglet **Modèles**.

## Ajout et suppression de colonnes

1. Dans la vue d’édition, recherchez l’ensemble de données contenant la colonne que vous souhaitez ajouter.
2. Sélectionnez **+** en regard du nom de la colonne. La colonne apparaît dans la zone de travail du rapport.
3. Pour ajouter la même colonne plusieurs fois, par exemple, pour compter deux valeurs d’état différentes. Sélectionnez à nouveau **+** pour cette colonne.
4. Pour supprimer une colonne, sélectionnez-la dans la zone de travail, puis cliquez sur l’icône de suppression.

## Réorganisation et changement de nom des colonnes

1. Faites glisser une colonne vers la position souhaitée dans la zone de travail. L’ordre dans la zone de travail correspond à l’ordre des colonnes dans le fichier téléchargé.
2. Pour renommer une colonne, sélectionnez son champ d’alias et saisissez le nom que vous souhaitez voir apparaître en tant qu’en-tête de colonne dans le rapport.

## Mettre à jour les filtres

1. Pour modifier une valeur de filtre existante, sélectionnez la ligne de filtre, modifiez la valeur, puis confirmez.
2. Pour ajouter un nouveau filtre, sélectionnez **Ajouter un filtre**.
3. Choisissez le champ sur lequel vous souhaitez filtrer.
4. Sélectionnez un opérateur. Les opérateurs disponibles dépendent du type de données du champ.
5. Saisissez ou sélectionnez une valeur :
   * Pour les champs de chaîne, tapez pour effectuer une recherche et une sélection parmi les suggestions.
   * Pour les champs de liste, sélectionnez une ou plusieurs valeurs dans le sélecteur.
   * Dans les champs de date, saisissez une date ou choisissez une plage relative telle que les 90 derniers jours.
6. Pour supprimer un filtre, sélectionnez l’icône de suppression sur cette ligne de filtre.

## Mettre à jour le tri

1. Cliquez sur l’icône de tri de la colonne à trier.
2. Sélectionnez **Croissant** ou **Décroissant**.
3. Pour trier sur des colonnes supplémentaires, répétez l’opération pour chaque colonne. La première colonne triée est la colonne principale ; des tris supplémentaires s’appliquent au sein des colonnes.

>[!TIP]
>
>Appliquez toujours au moins un tri. Sans tri, l’ordre des lignes peut différer selon le téléchargement d’un même rapport.

## Enregistrement et téléchargement

1. Sélectionnez Enregistrer pour enregistrer vos modifications dans l&#39;onglet **Rapports**.
2. Sélectionnez **Télécharger** pour générer le rapport. Vous recevrez une notification dans l’application lorsque le fichier sera prêt.
