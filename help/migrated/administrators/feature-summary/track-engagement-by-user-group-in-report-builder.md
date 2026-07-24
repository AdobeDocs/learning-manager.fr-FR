---
jcr-language: en_us
title: Suivi de l’engagement par groupe d’utilisateurs dans Report Builder
description: Créez un rapport dans le Report Builder Adobe Learning Manager qui affiche le temps total passé et les inscriptions par groupe d’utilisateurs, regroupés par mois.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Suivi de l’engagement par groupe d’utilisateurs dans Report Builder

Ce rapport aide les responsables de la formation et les administrateurs L&amp;D à identifier les groupes d’utilisateurs les plus actifs et à déterminer les tendances de l’engagement mois après mois. Il utilise les ensembles de données **Groupe d&#39;utilisateurs de champ actif** et **Inscription** avec les fonctions de groupe par et d&#39;agrégation pour produire une ligne de résumé par groupe d&#39;utilisateurs par mois.

## Créer le rapport d’engagement par groupe d’utilisateurs

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Sélectionnez **Créer un rapport**. Saisissez un nom, par exemple Engagement par MoM de groupe d’utilisateurs.
3. Dans le panneau **Sélectionner des colonnes**, développez **Groupe d&#39;utilisateurs Active Field** et sélectionnez **+** en regard de **Nom du groupe d&#39;utilisateurs**. La colonne apparaît dans le panneau **Colonnes sélectionnées**.
4. Développez **Inscription** et sélectionnez **+** en regard de **Date d&#39;inscription**.
5. Sélectionnez **+** en regard de **Temps passé**. Sélectionnez l&#39;icône **modifier** (crayon) et entrez l&#39;alias Temps total passé.
6. Développez **Objet d&#39;apprentissage** et sélectionnez **+** en regard de **Nombre d&#39;utilisateurs inscrits**. Sélectionnez l&#39;icône **modifier** et saisissez l&#39;alias Total des inscriptions.
7. Sélectionnez **Regrouper par : sélectionnez** en haut du panneau **Colonnes sélectionnées**.
8. Choisissez **Inscription - Date d&#39;inscription** et définissez la granularité sur **Mois**. Sélectionnez **Groupe d&#39;utilisateurs de champs actifs - Nom du groupe d&#39;utilisateurs**. Les deux s’affichent sous la forme de balises Inscription - Date d’inscription (mois) et Groupe d’utilisateurs du champ actif - Nom du groupe d’utilisateurs.
9. Sur la ligne **Inscription - Temps passé**, sélectionnez **Agréger par** et choisissez **Somme**.
10. Dans la ligne **Objet d’apprentissage - Nombre d’utilisateurs inscrits**, sélectionnez **Agréger par** et choisissez **Nombre**.

    ![](assets/report-builder-0040.png)

11. Sélectionnez **Ajouter un filtre**. Choisissez **Inscription - Date d&#39;inscription**, sélectionnez une plage relative telle que **3 derniers mois** ou entrez une plage de dates spécifique.
12. Sélectionnez **+ Ajouter le tri**. Trier par **Inscription - Date d&#39;inscription** croissante, puis ajouter un tri secondaire sur **Temps total passé** décroissant.
13. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport contiendra une ligne par groupe d&#39;utilisateurs et par mois, indiquant le temps total passé et le nombre total d&#39;inscriptions pour cette période.
