---
jcr-language: en_us
title: Création d’un rapport personnalisé dans Report Builder
description: Créez un rapport entièrement personnalisé dans le Report Builder Adobe Learning Manager en sélectionnant vos propres colonnes, filtres, paramètres de regroupement et en effectuant un tri à partir d’une zone de travail vide.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%

---


# Création d’un rapport personnalisé dans Report Builder

Créer à partir de zéro fonctionne mieux lorsque vous disposez d’une image claire des colonnes et de la sortie dont vous avez besoin et qu’aucun modèle existant ne correspond à votre cas d’utilisation. Si vous débutez avec Report Builder, pensez à commencer avec un modèle.

Dans cet exemple, vous identifierez les élèves de chaque responsable qui sont exposés au risque de suivre des cours de conformité.

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **Rapports**, puis **Report Builder**.
3. Sélectionnez l&#39;onglet **Rapports**, puis sélectionnez **Créer un rapport**.
4. Entrez un nom de rapport. Un nom est requis. Le cas échéant, saisissez une description.
   ![](assets/image011.png)
5. Dans le panneau de colonnes, sélectionnez les jeux de données suivants et développez-les :
a. Utilisateur
b. Objet d’apprentissage
c. État de conformité de l’utilisateur
6. Sélectionnez **+** à côté des colonnes suivantes que vous souhaitez inclure. Les colonnes sélectionnées apparaissent dans la zone de travail du rapport.
a. Utilisateur\Nom
b. Nom de l’utilisateur\du responsable
c. Objet d’apprentissage\Nom de l’objet d’apprentissage
d. État de conformité de l’utilisateur\% d’achèvement
e. État de conformité de l’utilisateur\Conformité %
!   [&#128279;](assets/image012.png)
7. Réorganisez les colonnes en les faisant glisser dans la zone de travail.
8. Pour renommer une colonne, entrez un nom dans le champ d&#39;alias de la colonne. L’alias apparaît comme l’en-tête de colonne dans le fichier téléchargé.
9. Sélectionnez **Enregistrer le rapport**.

## Télécharger le rapport

1. Sélectionnez **Actions** dans le coin supérieur droit.
   ![](assets/image013.png)
2. Sélectionnez Télécharger. Vous pouvez télécharger le rapport à partir de l’icône de notifications lorsqu’il est prêt.

Le rapport téléchargé dans l’extension de fichier .csv contient les colonnes suivantes :

1. name
2. managerName
3. name
4. completionPct
5. compliancePct

## Appliquer le regroupement, les filtres et le tri

### Filtre

Maintenant que vous avez téléchargé le rapport, appliquez un filtre avec completionPct OR compliancePct égal à 100.

1. Ouvrez le rapport et sélectionnez **Modifier** dans le coin supérieur droit.
2. Sélectionnez **Ajouter un filtre** et recherchez dans les colonnes où vous souhaitez appliquer les filtres.
   ![](assets/image014.png)
3. Sélectionnez **Ajouter**.
4. Combinez les filtres avec une logique ET/OU ; sélectionnez l’opérateur pour basculer entre les lignes de filtre.
   ![](assets/image015.png)
5. Sélectionnez **Enregistrer le rapport** et téléchargez le rapport.

Le rapport téléchargé contient des enregistrements où completionPct OU compliancePct est égal à 100.

### Regrouper par

Regrouper les enregistrements par responsable pour :

* Agréger les données des élèves par responsable
* Calculer les moyennes au niveau du responsable
* Compter les élèves sous chaque responsable

1. Ouvrez le rapport et sélectionnez **Modifier** dans le coin supérieur droit.
2. Sélectionnez **Regrouper par:Select** et sélectionnez la colonne **Nom du gestionnaire d&#39;utilisateurs**.
   ![](assets/image016.png)
3. Regroupez les colonnes suivantes :
a. User\Name
b. Objet d’apprentissage\Nom de l’objet d’apprentissage
4. Sélectionnez **Count** comme fonction d&#39;agrégation pour les colonnes.
   ![](assets/image017.png)
5. Répétez l’opération pour Objet d’apprentissage\Nom de l’objet d’apprentissage.
   ![](assets/image018.png)
6. Sélectionnez **Enregistrer le rapport** et téléchargez le rapport.

Le rapport téléchargé contient un résumé des performances de formation des élèves à l’attention du responsable. Elle affiche les taux moyens d’achèvement, les scores de conformité moyens et le nombre total d’élèves pour chaque responsable. Les données indiquent que tous les groupes suivent une formation universelle, tandis que les performances en matière de conformité varient considérablement entre les responsables.

### Trier

Triez le rapport par ordre décroissant en fonction du nombre d’élèves pour chaque responsable.

1. Ouvrez le rapport et sélectionnez **Modifier** dans le coin supérieur droit.
2. Sélectionnez **Ajouter un tri**.
3. Recherchez le nom d&#39;utilisateur et sélectionnez **Utilisateur\Nom**.
4. Sélectionnez **Descendant**.
   ![](assets/image019.png)
5. Sélectionnez **Ajouter**.
6. Sélectionnez **Enregistrer le rapport** et téléchargez le rapport.

Le rapport téléchargé contient le nombre d’élèves par responsable dans l’ordre décroissant.
