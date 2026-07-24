---
jcr-language: en_us
title: Examen des performances de l’instructeur avec Report Builder
description: Créez un rapport dans le Report Builder Adobe Learning Manager qui affiche les sessions enseignées, le nombre total d’inscriptions et les achèvements par instructeur.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# Examen des performances de l’instructeur avec Report Builder

## Présentation

Ce rapport aide les responsables de la formation à identifier les instructeurs les plus actifs, le nombre d’élèves qu’ils atteignent et le nombre d’élèves qui terminent les cours qu’ils dispensent.

## Création d’un rapport d’efficacité de l’instructeur

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Tapez un nom tel que **Efficacité de l&#39;instructeur**.
3. Ajoutez **Noms des instructeurs** à partir du jeu de données **Module**.
4. Ajoutez **ID de module** à partir du jeu de données **Module**. Vous allez agréger cela pour compter les sessions.
5. Ajoutez **État** à partir du jeu de données **Transcription du module**. Vous utiliserez la commande count if pour compter les terminaisons.
6. Sélectionnez **Regrouper par** sur **Noms des instructeurs**.
7. Appliquez **Count** à **ID de module**. Tapez l&#39;alias Nombre total de sessions.
8. Appliquer **Nombre si** à **État**, sélectionnez Terminé. Tapez l&#39;alias **Nombre total de finalisations**.
9. Pour afficher également le nombre total d&#39;inscriptions, ajoutez **État** une seconde fois. Appliquer **Nombre si** à Non démarré. Tapez l&#39;alias Total des inscriptions.

   ![](assets/report-builder-0037.png)

10. Filtrez **Noms des instructeurs** pour qu&#39;ils ne soient pas vides.

    ![](assets/report-builder-0038.png)

11. Triez par **Total des achèvements** en descendant pour faire apparaître en premier les instructeurs les plus performants.

    ![](assets/report-builder-0039.png)

12. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport téléchargé résume l&#39;efficacité des instructeurs en comparant le nombre total de sessions de formation, les achèvements de l&#39;élève et les inscriptions non commencées pour chaque instructeur, ce qui permet d&#39;évaluer l&#39;engagement, les performances à l&#39;achèvement et les besoins potentiels de suivi de formation.

## Bonnes pratiques

* Utilisez des étiquettes de catalogue pour limiter les rapports des instructeurs à une entité, un emplacement ou un programme spécifique. Cela est plus précis que le filtrage par nom de catalogue uniquement.
* Ajoutez un filtre de date, tel que **Date d&#39;inscription** au cours des 90 derniers jours, pour étendre le rapport à une période récente plutôt qu&#39;à des données historiques.
* Triez-les selon une mesure significative, telle que **Total des achèvements** plutôt que par nom d&#39;instructeur, afin que les différences de performances soient immédiatement visibles.
