---
jcr-language: en_us
title: Examen des performances de l’instructeur avec Report Builder
description: Créez un rapport dans le Report Builder Adobe Learning Manager qui affiche les sessions enseignées, le nombre total d’inscriptions et les achèvements par instructeur.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---


# Examen des performances de l’instructeur avec Report Builder

Ce rapport aide les responsables de la formation à identifier les instructeurs les plus actifs, le nombre d’élèves qu’ils atteignent et le nombre d’élèves qui terminent les cours qu’ils dispensent.

## Création d’un rapport d’efficacité de l’instructeur

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Tapez un nom tel que _Efficacité de l&#39;instructeur_.
3. Ajoutez **Noms des instructeurs** à partir du jeu de données **Session de module**.
4. Ajoutez **ID de session de module** à partir du jeu de données **Session de module**. Vous allez agréger cela pour compter les sessions.
5. Ajoutez **État** à partir du jeu de données **Transcription du module**. Vous utiliserez la commande count if pour compter les terminaisons.
6. Sélectionnez **Regrouper par** sur **Noms des instructeurs**.
7. Appliquez **Count** à **ID de session de module**. Tapez l&#39;alias _Nombre total de sessions_.
8. Appliquez **Nombre si** à **État** et sélectionnez **Terminé**. Tapez l&#39;alias _Nombre total de finalisations_.
9. Pour afficher également le nombre total d&#39;inscriptions, ajoutez **État** une seconde fois. Appliquer **Nombre si** à **Pas commencé**. Tapez l&#39;alias _Total des inscriptions_.
   ![](assets/image035.png)
10. Filtrez **Noms des instructeurs** pour qu&#39;ils ne soient pas vides.
   ![](assets/image036.jpg)
11. Triez par **Total des achèvements** en descendant pour faire apparaître en premier les instructeurs les plus performants.
   ![](assets/image037.png)
12. Sélectionnez Enregistrer le rapport et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport téléchargé résume l&#39;efficacité des instructeurs en comparant le nombre total de sessions de formation, les achèvements de l&#39;élève et les inscriptions non commencées pour chaque instructeur, ce qui permet d&#39;évaluer l&#39;engagement, les performances à l&#39;achèvement et les besoins potentiels de suivi de formation.

## Bonnes pratiques

* Utilisez des étiquettes de catalogue pour limiter les rapports des instructeurs à une entité, un lieu ou un programme spécifique\. Cela est plus précis que le filtrage par nom de catalogue uniquement.
* Ajoutez un filtre de date, tel que **Date d&#39;inscription** au cours des 90 derniers jours, pour étendre le rapport à une période récente plutôt qu&#39;à des données historiques.
* Triez-les selon une mesure significative, telle que **Total des achèvements**, plutôt que par nom d&#39;instructeur, afin que les différences de performances soient immédiatement visibles.
