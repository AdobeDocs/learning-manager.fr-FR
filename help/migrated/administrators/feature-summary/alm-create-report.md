---
jcr-language: en_us
title: Création d’un rapport personnalisé dans Report Builder
description: Créez un rapport entièrement personnalisé dans le Report Builder Adobe Learning Manager en sélectionnant vos propres colonnes, filtres, paramètres de regroupement et en effectuant un tri à partir d’une zone de travail vide.
contentowner: mmanuel
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 6c26277dfbd20374e57273f8371b360ee770a0df
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 1%
---

# Création d’un rapport personnalisé dans Report Builder

## Présentation

Créer à partir de zéro fonctionne mieux lorsque vous disposez d’une image claire des colonnes et de la sortie dont vous avez besoin et qu’aucun modèle existant ne correspond à votre cas d’utilisation. Si vous débutez avec Report Builder, pensez à commencer avec un modèle.

## Création d’un rapport personnalisé

Dans cet exemple, vous identifierez les élèves de chaque responsable qui sont exposés au risque de suivre des cours de conformité.

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **Rapports**, puis **Report Builder**.
3. Sélectionnez l&#39;onglet **Rapports**, puis sélectionnez **Créer un rapport**.
4. Entrez un nom de rapport. Un nom est requis. Le cas échéant, saisissez une description.

   ![](assets/report-builder-0013.png)

5. Dans le panneau de colonnes, sélectionnez les jeux de données suivants et développez-les :

   * Utilisateur
   * Objet d’apprentissage
   * État de conformité de l’utilisateur

6. Sélectionnez **+** à côté des colonnes suivantes que vous souhaitez inclure. Les colonnes sélectionnées apparaissent dans la zone de travail du rapport.

   * Nom d’utilisateur
   * Nom de l’utilisateur et du responsable
   * Objet d’apprentissage - Nom de l’objet d’apprentissage
   * État de conformité de l’utilisateur - % d’achèvement
   * État de conformité de l’utilisateur - % de conformité

   ![](assets/report-builder-0014.png)

7. Réorganisez les colonnes en les faisant glisser dans la zone de travail.
8. Pour renommer une colonne, saisissez un nom dans le champ **Alias** de la colonne. Si vous spécifiez un alias, il est utilisé comme en-tête de colonne. Si vous ne spécifiez pas d&#39;alias, l&#39;en-tête de colonne par défaut inclut le nom du jeu de données. Par exemple, le nom du jeu de données Objet d’apprentissage s’affiche sous la forme Objet d’apprentissage - Nom.

   **En-têtes de colonne**

   Report Builder inclut le nom du jeu de données dans les en-têtes de colonne par défaut pour aider à distinguer les colonnes avec des noms similaires dans les jeux de données. Par exemple, si vous sélectionnez Nom dans le jeu de données Objet d’apprentissage, l’en-tête de colonne apparaît sous la forme Objet d’apprentissage - Nom.

   Si vous spécifiez un alias personnalisé pour une colonne, Report Builder utilise l&#39;alias au lieu de l&#39;en-tête de colonne par défaut.

   **Impact sur les rapports existants**

   Après la mise à niveau, les rapports existants qui utilisent des noms de colonne par défaut sans alias personnalisé affichent les en-têtes de colonne mis à jour. Par exemple, le nom du jeu de données de l’objet d’apprentissage passe de Nom à Objet d’apprentissage - Nom.

   Les données de rapport, les filtres et les planifications ne sont pas affectés.

   Si vous utilisez la sortie de rapport dans des scripts, des feuilles de calcul, des tableaux de bord BI ou des intégrations qui référencent des colonnes par en-tête, vérifiez vos systèmes en aval et mettez à jour les références aux en-têtes de colonnes précédents selon vos besoins.

   Pour conserver un en-tête de colonne spécifique, définissez un alias personnalisé pour la colonne.

9. Sélectionnez **Enregistrer le rapport**.

## Télécharger le rapport

1. Sélectionnez **Actions** dans le coin supérieur droit.

   ![](assets/report-builder-0015.png)

2. Sélectionnez **Télécharger**. Vous pouvez télécharger le rapport à partir de l’icône de notifications lorsqu’il est prêt.

Le rapport téléchargé (csv) contient les colonnes suivantes :

* name
* managerName
* name
* completionPct
* compliancePct

## Appliquer le regroupement, les filtres et le tri

### Filtre

Maintenant que vous avez téléchargé le rapport, appliquez un filtre avec completionPct OR compliancePct égal à 100.

1. Ouvrez le rapport et sélectionnez **Modifier** dans le coin supérieur droit.
2. Sélectionnez **Ajouter un filtre** et recherchez dans les colonnes où vous souhaitez appliquer les filtres.

   ![](assets/report-builder-0016.png)

3. Sélectionnez **Ajouter**.
4. Combinez les filtres avec une logique ET/OU ; sélectionnez l’opérateur pour basculer entre les lignes de filtre.

   ![](assets/report-builder-0017.png)

5. Sélectionnez **Enregistrer le rapport** et téléchargez le rapport.

Le rapport téléchargé contient des enregistrements où completionPct OU compliancePct est égal à 100.

### Regrouper par

Regrouper les enregistrements par responsable pour :

* Agréger les données des élèves par responsable
* Calculer les moyennes au niveau du responsable
* Compter les élèves sous chaque responsable

1. Ouvrez le rapport et sélectionnez **Modifier** dans le coin supérieur droit.
2. Sélectionnez **Regrouper par:Select** et sélectionnez la colonne **Nom du gestionnaire d&#39;utilisateurs**.

   ![](assets/report-builder-0018.png)

3. Regroupez les colonnes suivantes :

   * User-Name
   * Objet d’apprentissage - Nom de l’objet d’apprentissage

4. Sélectionnez **Count** comme fonction d&#39;agrégation pour les colonnes.

   ![](assets/report-builder-0019.png)

   **En-têtes de colonne pour les colonnes agrégées :**

   Lorsque vous appliquez une fonction d&#39;agrégation, l&#39;en-tête de colonne par défaut inclut la fonction d&#39;agrégation. Par exemple, lorsque vous appliquez **Nombre** à **Objet d’apprentissage - ID**, l’en-tête de colonne s’affiche comme **Nombre** de **Objet d’apprentissage - ID**. Si vous avez spécifié un alias personnalisé, celui-ci reste inchangé.

5. Répétez l’opération pour Objet d’apprentissage - Nom de l’objet d’apprentissage.

   ![](assets/report-builder-0020.png)

6. Sélectionnez **Enregistrer le rapport** et téléchargez le rapport.

Le rapport téléchargé contient un résumé des performances de formation des élèves à l’attention du responsable. Elle affiche les taux moyens d’achèvement, les scores de conformité moyens et le nombre total d’élèves pour chaque responsable. Les données indiquent que tous les groupes suivent une formation universelle, tandis que les performances en matière de conformité varient considérablement entre les responsables.

### Trier

Triez le rapport par ordre décroissant en fonction du nombre d’élèves pour chaque responsable.

1. Ouvrez le rapport et sélectionnez **Modifier** dans le coin supérieur droit.
2. Sélectionnez **Ajouter un tri**.
3. Recherchez le nom d&#39;utilisateur et sélectionnez **Nom-utilisateur**.
4. Sélectionnez **Descendant**.

   ![](assets/report-builder-0021.png)

5. Sélectionnez **Ajouter**.
6. Sélectionnez **Enregistrer le rapport** et téléchargez le rapport.

Le rapport téléchargé contient le nombre d’élèves par responsable dans l’ordre décroissant.
