---
jcr-language: en_us
title: Création d’un rapport de tendances dans Report Builder
description: Suivez les tendances d’apprentissage d’un mois à l’autre ou d’une semaine à la semaine dans le Report Builder Adobe Learning Manager à l’aide des agrégateurs de tendances dans les champs de date.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---


# Création d’un rapport de tendances dans Report Builder

Les rapports de tendance montrent comment les mesures, telles que le nombre de cours, le nombre d&#39;inscriptions ou les achèvements, changent au fil du temps. Vous pouvez choisir une colonne de date et une granularité de tendance (jour, semaine ou mois), et le Report Builder regroupe les données par période.

## Signification des données de tendance

Les rapports de tendance dans Report Builder reflètent **un instantané des données, regroupées par date**. Ils ne montrent pas l&#39;état historique des données à chaque date passée.

Par exemple, une tendance d&#39;inscription mensuelle affiche le nombre d&#39;inscriptions qui existent aujourd&#39;hui, réparties sur les mois au cours desquels elles ont été créées. Si un élève s&#39;est inscrit en janvier puis s&#39;est désinscrit par la suite, cet enregistrement d&#39;inscription peut ne plus apparaître. Le rapport reflète l&#39;état actuel des dossiers, pas ce qui était vrai en janvier.

Il s&#39;agit d&#39;une distinction importante à des fins de vérification. Si vous avez besoin de données historiques ponctuelles, utilisez ce rapport pour une analyse directionnelle des tendances plutôt que pour des enregistrements historiques précis.

## Création d’un rapport de tendance sur le nombre de cours

Ce rapport indique le nombre de cours ajoutés au compte d’un mois à l’autre.

1. Sélectionnez **Rapports** > **Report Builder**, puis sélectionnez l’onglet **Rapports**.
2. Sélectionnez **Créer un rapport**. Tapez un nom tel que Nombre de cours MoM.
3. Ajoutez **l&#39;ID d&#39;objet d&#39;apprentissage** à partir du jeu de données **Objet d&#39;apprentissage**.
4. Ajoutez la **date de création** à partir de l&#39;ensemble de données de l&#39;**objet d&#39;apprentissage**.
   ![](assets/image039.png)
5. Appliquer **Regrouper par** à la **date de création**. Définissez la granularité de la tendance sur **Mois**.
   ![](assets/image040.png)
6. Appliquez **Count** à **l&#39;ID d&#39;objet d&#39;apprentissage**. Entrez l&#39;alias Nombre de cours.
   ![](assets/image041.png)
7. Triez par **Date de création** par ordre croissant pour afficher la tendance par ordre chronologique.
   ![](assets/image042.png)
8. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le fichier téléchargé se compose d’une tendance mensuelle de l’activité de création de cours, indiquant le nombre de cours créés au fil du temps. Il permet de suivre les modèles de production des cours, les pics, les déclins et la croissance globale du contenu.

## Création d&#39;un rapport de tendance des achèvements par catalogue

Ce rapport affiche les totaux d&#39;achèvement mensuels par catalogue sur une période définie.

1. Sélectionnez **Rapports** > **Report Builder**, puis sélectionnez l’onglet **Rapports**.
2. Sélectionnez **Créer un rapport**. Tapez un nom tel que Fin de catalogue MoM.
3. Ajoutez **Nom du catalogue** à partir du jeu de données **Catalog**.
4. Ajoutez **Date de fin** à partir du jeu de données **Transcription du module**.
5. Ajoutez **ID d&#39;objet d&#39;apprentissage** à partir de l&#39;ensemble de données **Objet d&#39;apprentissage** pour compter les terminaisons.
6. Appliquer **Regrouper par** sur **Nom du catalogue**. Appliquez également **Regrouper par** à la **date de fin** avec une granularité de **mois**.
   ![](assets/image_043.png)
7. Appliquez **Count** à **l&#39;ID d&#39;objet d&#39;apprentissage**. Entrez l&#39;alias Total des fins de production.
8. Ajoutez un filtre : **Le catalogue** est dans Safety, POS, Delivery (ou les catalogues pertinents pour votre compte).
9. Ajoutez un filtre : **La date d&#39;achèvement** tombe dans l&#39;année dernière.
   ![](assets/image044.png)
10. Trier par **Date de fin** croissante.
   ![](assets/image_045.png)
11. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

## Bonnes pratiques

* Utilisez **Date d&#39;achèvement** pour les tendances d&#39;achèvement et **Date d&#39;inscription** pour les tendances d&#39;inscription. L’utilisation d’un champ de date incorrect produit des résultats trompeurs.
* Ajoutez un filtre de date pour limiter la tendance à une fenêtre significative, par exemple, les 12 derniers mois pour une tendance mensuelle ou les 8 dernières semaines pour une tendance hebdomadaire.
* Attribuez à votre rapport de tendances un libellé indiquant la granularité et la plage de dates dans le nom, par exemple, « Fin de catalogue MoM - 3 derniers mois », pour qu’il soit clair lorsque vous l’afficherez ultérieurement.
