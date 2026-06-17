---
jcr-language: en_us
title: Tri des colonnes du rapport dans le Report Builder
description: Appliquez un tri sur une ou plusieurs colonnes dans le Report Builder Adobe Learning Manager pour contrôler l’ordre des lignes de vos rapports téléchargés.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Tri des colonnes du rapport dans le Report Builder

Le tri détermine l’ordre des lignes dans le fichier de rapport téléchargé\. Appliquez le tri chaque fois que la cohérence de la sortie est importante.

## Ajout d’un tri

Dans cet exemple, vous découvrirez les cours qui ont le plus d’achèvements.

1. Lancez Report Builder et sélectionnez **Créer un rapport**.
2. Saisissez le nom et la description du rapport.
3. Sélectionnez les colonnes suivantes : `<dataset>:<column name>`
a. Objet d’apprentissage - Nom de l’objet d’apprentissage
b. Objet d’apprentissage - État de l’objet d’apprentissage
c. Objet d’apprentissage - Nombre d’achèvements
4. Dans la section Tri, sélectionnez **Ajouter un tri**.
5. Sélectionnez **Objet d’apprentissage - Nombre d’achèvements**.
6. Sélectionnez un ordre de tri **croissant** ou **décroissant**.
   ![](assets/image032.jpg)
7. Sélectionnez **Ajouter**.
8. Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport.

Le rapport téléchargé répertorie tous les enregistrements, triés par le nombre de cours terminés.

## Ajout d’un tri sur plusieurs colonnes

Dans cet exemple, vous allez générer un rapport pour mesurer les performances de tous les responsables.

Pour trier sur plusieurs colonnes :

1. Lancez **Report Builder** et sélectionnez **Créer un rapport**.
2. Saisissez le nom et la description du rapport.
3. Sélectionnez les colonnes suivantes : `<dataset>:<column name>`
a. Utilisateur - Nom
b. Utilisateur - Nom du responsable
c. Transcription du module - État
d. Transcription du module - Pourcentage de progression
4. Ajouter les agrégats suivants :
a. Regrouper par utilisateur - Nom du responsable
b. Nombre d’utilisateurs distincts - Nom
c. Count If=COMPLETED Module Transcript - État
d. Relevé de notes moyen du module - Pourcentage de progression
   ![](assets/image033.png)
5. Dans la section **Trier**, ajoutez le tri multicolonne suivant :
a. Transcription du module - État : Décroissant
b. Utilisateur - Nom du responsable : croissant
   ![](assets/image034.jpg)
6. Sélectionnez Enregistrer le rapport et sélectionnez Actions > Télécharger pour télécharger le rapport.

Le rapport téléchargé fournit un résumé des performances à l’échelle du responsable, montrant le nombre d’élèves, le nombre d’inscriptions en fonction du statut et les pourcentages de progression moyens. Il met en évidence les niveaux de participation et les progrès de la formation dans les différents groupes de gestionnaires.
