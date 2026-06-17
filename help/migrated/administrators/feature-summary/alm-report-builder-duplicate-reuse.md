---
jcr-language: en_us
title: Duplication et réutilisation d’un rapport dans Report Builder
description: Copiez un rapport existant dans le Report Builder Adobe Learning Manager pour créer une variante sans reconstruire à partir de zéro.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Duplication et réutilisation d’un rapport dans Report Builder

La duplication d’un rapport copie toutes ses colonnes, alias, paramètres de regroupement par groupe, agrégations, filtres et tri dans un nouveau rapport modifiable. Utilisez cette option lorsque vous souhaitez créer une version d’un rapport pour un catalogue, un groupe d’utilisateurs ou une période différents.

## Duplication d’un rapport

1. Ouvrez le rapport à dupliquer.
2. Sélectionnez **Actions** > **Dupliquer**. Une copie du rapport s&#39;ouvre en mode édition avec le nom « [nom du rapport d&#39;origine]-Copier ». Par exemple, Vue des performances structurées entre les responsables - Copier
3. Entrez un nouveau nom pour l&#39;état.
4. Effectuez toutes les modifications nécessaires, par exemple, mettre à jour les filtres, ajuster les colonnes ou modifier le tri.
5. Sélectionnez **Enregistrer le rapport**.

Le rapport dupliqué est enregistré dans votre onglet **Rapports** et est indépendant du rapport d&#39;origine.

## Duplication d’un modèle

Vous pouvez également dupliquer les modèles à partir de l&#39;onglet **Modèles**. La duplication d&#39;un modèle crée un nouveau rapport modifiable dans l&#39;onglet **Rapports**. Le modèle d’origine reste inchangé.

1. Sélectionnez l&#39;onglet **Modèles**.
2. Recherchez le modèle à copier.
3. Sélectionnez **Dupliquer**.
   ![](assets/image049.png)
4. Saisissez un nom, effectuez des réglages et sélectionnez **Enregistrer le rapport**.

## Bonnes pratiques

* Dupliquez un rapport bien testé comme base lorsque vous avez besoin de variations pour différentes équipes, différents catalogues ou différentes périodes. Cela est plus rapide que de construire à partir de zéro et garantit une structure cohérente.
* Renommez immédiatement la copie pour indiquer ce qui la rend différente de l’original, par exemple « Conformité par VP - APAC » plutôt que « Copie du rapport de conformité ».
* Après avoir dupliqué un modèle, mettez à jour le nom avant d&#39;apporter toute autre modification afin que le rapport soit identifiable dans l&#39;onglet **Rapports**.
