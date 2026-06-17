---
jcr-language: en_us
title: Suivi de l’engagement par groupe d’utilisateurs dans Report Builder
description: Créez un rapport dans le Report Builder Adobe Learning Manager qui affiche le temps total passé et les inscriptions par groupe d’utilisateurs, regroupés par mois.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Suivi de l’engagement par groupe d’utilisateurs dans Report Builder

Ce rapport aide les responsables de la formation et les administrateurs L&amp;D à identifier les groupes d’utilisateurs les plus actifs et à déterminer les tendances de l’engagement mois après mois. Il utilise les ensembles de données **Groupe d&#39;utilisateurs de champ actif** et **Inscription** avec les fonctions de groupe par et d&#39;agrégation pour produire une ligne de résumé par groupe d&#39;utilisateurs par mois.

## Créer le rapport d’engagement par groupe d’utilisateurs

1. Lancez **Report Builder** et sélectionnez **Créer un rapport**.
2. Tapez un nom, par exemple _Engagement par MoM de groupe d&#39;utilisateurs_.
3. Dans le panneau **Sélectionner des colonnes**, développez **Groupe d&#39;utilisateurs Active Field** et sélectionnez **+** en regard de **Nom du groupe d&#39;utilisateurs**. La colonne apparaît dans le panneau **Colonnes sélectionnées**.
4. Développez **Inscription** et sélectionnez **+** en regard de **Date d&#39;inscription**.
5. Sélectionnez **+** en regard de **Temps passé**. Sélectionnez l&#39;icône **Modifier** (crayon) et saisissez l&#39;alias _Temps total passé_.
6. Développez **Objet d&#39;apprentissage** et sélectionnez **+** en regard de **Nombre d&#39;utilisateurs inscrits**. Sélectionnez l&#39;icône Modifier et saisissez l&#39;alias _Total des inscriptions_.
7. Sélectionnez **Regrouper par : sélectionnez** en haut du panneau **Colonnes sélectionnées**.
8. Choisissez **Inscription - Date d&#39;inscription** et définissez la granularité sur **Mois**. Sélectionnez **Groupe d&#39;utilisateurs de champs actifs - Nom du groupe d&#39;utilisateurs**. Les deux s&#39;affichent sous forme de balises : **Inscription - Date d&#39;inscription (mois)** et **Groupe d&#39;utilisateurs du champ actif - Nom du groupe d&#39;utilisateurs**.
9. Sur la ligne **Inscription - Temps passé**, sélectionnez **Agréger par** et choisissez **Somme**.
10. Dans la ligne **Objet d’apprentissage - Nombre d’utilisateurs inscrits**, sélectionnez **Agréger par** et choisissez **Nombre**.
   ![](assets/image038.jpg)
11. Sélectionnez **Ajouter un filtre**. Choisissez **Inscription - Date d&#39;inscription**, puis sélectionnez une plage relative telle que **3 derniers mois**, ou entrez une plage de dates spécifique.
12. Sélectionnez **+ Ajouter le tri**. Trier par **Inscription - Date d&#39;inscription** croissante, puis ajouter un tri secondaire sur **Temps total passé** décroissant.
13. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport contiendra une ligne par groupe d&#39;utilisateurs et par mois, indiquant le temps total passé et le nombre total d&#39;inscriptions pour cette période.

