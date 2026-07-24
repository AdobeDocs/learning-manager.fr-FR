---
jcr-language: en_us
title: Ajout et combinaison de filtres dans un rapport
description: Restreignez les données de rapport dans le Report Builder Adobe Learning Manager à l’aide de filtres uniques, de la logique ET/OU et de groupes de filtres imbriqués.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---


# Ajout et combinaison de filtres dans un rapport

## Présentation

Les filtres vous permettent d’étendre votre rapport aux enregistrements dont vous avez besoin. Vous pouvez appliquer un seul filtre, combiner plusieurs filtres avec une logique AND ou OR et créer des groupes imbriqués pour des conditions complexes.

## Ajout d’un filtre

Utilisez des filtres pour limiter votre rapport à un sous-ensemble spécifique de données au lieu de tout afficher.

Par exemple, vous pouvez vouloir comprendre le nombre d&#39;élèves inscrits à des cours au cours des 365 derniers jours. Dans ce cas, vous appliquez un filtre de date à la date d&#39;inscription pour inclure uniquement les activités récentes.

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Saisissez le nom et la description du rapport.
3. Sélectionnez les colonnes suivantes : <dataset>:<column name>

   * Inscription - Date d’inscription
   * Utilisateur - Nom

   ![](assets/report-builder-0024.png)

4. Dans la section Rapports, sélectionnez **Ajouter un filtre**.
5. Recherchez ou accédez au champ sur lequel vous souhaitez filtrer. Dans cet exemple, sélectionnez **Inscription - Date d&#39;inscription**.

   ![](assets/report-builder-0025.png)

6. Sélectionnez **Ajouter**.
7. Sélectionnez un opérateur. Les opérateurs disponibles dépendent du type de données du champ :

   * Champs de chaîne : contient, est égal à, commence par
   * Champs numériques - supérieur à, inférieur à, égal à, entre
   * Champs de date : est égal à, avant, après, entre les N derniers jours
   * Champs de liste (enum) : est dans, n’est pas dans

8. Dans ce cas, sélectionnez **l&#39;année dernière**.

   ![](assets/report-builder-0026.png)

9. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport téléchargé répertorie tous les utilisateurs qui se sont inscrits à un objet d’apprentissage au cours des 365 derniers jours.

## Ajout de plusieurs filtres avec logique ET/OU

Lorsque vous ajoutez un second filtre, la relation par défaut entre les filtres est AND ; les deux conditions doivent être vraies pour qu’une ligne apparaisse.

Par exemple, vous pouvez souhaiter identifier les élèves qui se sont inscrits aux cours au cours des 365 derniers jours ET qui rendent compte à un responsable spécifique. Dans ce cas, les deux conditions doivent être vraies, de sorte que les filtres sont combinés à l&#39;aide de la logique AND.

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Saisissez le nom et la description du rapport.
3. Sélectionnez les colonnes suivantes : <dataset>:<column name>

   * Utilisateur - Nom
   * Utilisateur - Nom du responsable
   * <span class="mark">Inscription - Date d&#39;inscription</span>

4. Regroupez par la colonne **Nom du gestionnaire d&#39;utilisateurs**.
5. Dans la section Filtre, sélectionnez les filtres suivants :

   * Inscription - Date d&#39;inscription i **s au cours de l&#39;année dernière**
   * Utilisateur : le nom du responsable **commence par** N
   * Utilisateur : le nom du responsable **n&#39;est pas vide**

     ![](assets/report-builder-0027.png)

6. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport téléchargé répertorie tous les utilisateurs qui se sont inscrits à un objet d&#39;apprentissage au cours des 365 derniers jours **et** rapports à un responsable dont le nom commence par N.

## Création de groupes de filtres imbriqués

Les groupes imbriqués vous permettent de créer des conditions avec plusieurs niveaux logiques, équivalents aux crochets d&#39;une formule. Par exemple : (Catalog = Safety OR Catalog = Hygiene) AND La date d’achèvement est dans les 90 derniers jours.

Utilisez des groupes de filtres imbriqués lorsque votre logique comprend une combinaison de conditions AND et OR qui doivent être évaluées ensemble.

Par exemple, utilisez la logique de filtre imbriquée pour identifier les inscriptions incomplètes où les élèves ont une progression inférieure à 50 % ou une formation en retard, en démontrant comment les conditions AND et OR fonctionnent ensemble.

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Saisissez le nom et la description du rapport.
3. Sélectionnez les colonnes suivantes : <dataset>:<column name>

   * Inscription - Statut
   * Inscription - Pourcentage de progression
   * Inscription - En retard

     ![](assets/report-builder-0028.png)

4. Dans la section **Filtre**, sélectionnez les filtres suivants :

   * Inscription -État **n&#39;est égal à aucun des** terminés.
   * Sélectionnez +.
   * Recherchez le pourcentage de progression de l’inscription.
   * Sélectionnez le filtre.
   * Sélectionnez **Ajouter comme groupe**.

     ![](assets/report-builder-0029.png)

5. Ajouter une inscription - Pourcentage de progression **inférieur à** 50.

   ![](assets/report-builder-0030.png)

6. Sélectionnez +.
7. Recherchez **Inscription en retard**.
8. Sélectionnez le filtre.
9. Sélectionnez **Ajouter comme groupe**.

   ![](assets/report-builder-0031.png)

10. Ajouter Inscription - En retard vaut TRUE.
11. Remplacez l’opérateur AND imbriqué par OR.

    ![](assets/report-builder-0032.png)

12. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport téléchargé répertorie toutes les inscriptions en cours ou non commencées, dont le pourcentage de progression est inférieur à 50 % ou en retard.
