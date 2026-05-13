---
description: Découvrez comment intégrer Harvard ManageMentor à Adobe Learning Manager
jcr-language: en_us
title: Connecteur Harvard ManageMentor
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 1%

---


# Connecteur Harvard ManageMentor dans Adobe Learning Manager

## Introduction

Le **connecteur Harvard ManageMentor** est conçu pour les entreprises clientes qui utilisent Harvard ManageMentor. Il permet aux élèves de découvrir et d’accéder aux cours Harvard ManageMentor directement depuis Adobe Learning Manager. Une fois connecté, le système peut récupérer les données de progression des élèves régulièrement et créer des cours dans Adobe Learning Manager en fonction des métadonnées importées.

Cet article explique comment configurer et utiliser le connecteur Harvard ManageMentor dans Adobe Learning Manager.

Grâce à cette intégration, les administrateurs d’intégration peuvent connecter le compte Harvard ManageMentor de la société à Adobe Learning Manager pour importer automatiquement les cours et suivre la progression des élèves, sans créer de nouveau contenu de formation à partir de zéro.

## Prérequis

Assurez-vous que la fonctionnalité **Migration** est activée pour votre compte avant de configurer le connecteur.

## Configuration du connecteur

Utilisez le connecteur Harvard ManageMentor pour importer des cours de Harvard ManageMentor dans Adobe Learning Manager. Après avoir connecté votre compte, vous pouvez importer les détails du cours et suivre la progression des élèves.

Pour configurer le connecteur :

1. Connectez-vous en tant qu’administrateur d’intégration.
2. Sélectionnez **Harvard ManageMentor** sur la page d&#39;accueil.
3. Sélectionnez l’une des options suivantes sur la mosaïque du connecteur :
   - **Prise en main**
   - **Connexion**
   - **Gérer les connexions**

   ![](assets/harvard-managementor-connector1.png)
   _La vignette Harvard ManageMentor affiche trois options de configuration_

## Créer une connexion

Pour créer une connexion :

1. Sélectionnez **Se connecter** sur la vignette **Harvard ManageMentor**.

   ![](assets/harvard-managementor-connector2.png)
   _Sélectionnez Se connecter pour créer une nouvelle connexion Harvard ManageMentor_

2. Saisissez la connexion dans le champ **Nom de la connexion**.
3. Sélectionnez **Se connecter** pour créer la connexion.

   ![](assets/harvard-managementor-connector3.png)
   _Saisissez le nom dans le champ Nom de connexion_

## Gérer la connexion

Après avoir configuré le connecteur Harvard ManageMentor, vous pouvez gérer votre connexion dans Adobe Learning Manager. Vous pouvez modifier les paramètres de synchronisation et exécuter les synchronisations manuellement ou selon une planification.

### Activer la connexion

Pour activer la connexion :

1. Sélectionnez **Gérer les connexions** sur la vignette **Harvard ManageMentor**.

   ![](assets/harvard-managementor-connector4.png)
   _Gérer les connexions pour configurer et planifier l&#39;importation de données_

2. Sélectionnez la connexion.
3. Sélectionnez **Configurer** dans le volet de navigation de gauche.
4. Sélectionnez **Activer la connexion**, puis **Enregistrer**.

   ![](assets/harvard-managementor-connector5.png)
   _Activez le connecteur Harvard ManageMentor pour importer les données_

### Planification de la synchronisation

Pour planifier la synchronisation :

1. Sélectionnez **Gérer les connexions** sur la vignette **Harvard ManageMentor**.
2. Sélectionnez la connexion.
3. Sélectionnez **Configurer** dans le volet de navigation de gauche.
4. Sélectionnez **Activer la planification** dans la section **Planification de la synchronisation**.

   ![](assets/harvard-managementor-connector6.png)
   _Planifiez l&#39;importation de données de Harvard ManageMentor vers Adobe Learning Manager_

5. Sélectionnez la date et l&#39;heure de début en UTC.
6. Tapez le nombre de jours après lequel la synchronisation doit se répéter.
7. Sélectionnez **Enregistrer**.

Les paramètres de synchronisation sont enregistrés. Le connecteur fonctionnera selon le planning et importera les données de Harvard ManageMentor dans Adobe Learning Manager.

## Exécuter la synchronisation à la demande

L&#39;option **Synchronisation à la demande** vous permet d&#39;importer manuellement des données de Harvard ManageMentor dans Adobe Learning Manager. Cela est utile lorsque vous souhaitez mettre à jour immédiatement les données d’activité des élèves, sans attendre la prochaine synchronisation planifiée.

Pour exécuter l’importation de données à la demande :

1. Sélectionnez **Gérer les connexions** sur la vignette **Harvard ManageMentor**.
2. Sélectionnez la connexion.
3. Sélectionnez **Exécution à la demande** dans le volet de gauche.
4. Sélectionnez **Date de début**.

   ![](assets/harvard-managementor-connector7.png)
   _Exécutez la demande à la demande pour l&#39;importation immédiate des données de Harvard ManageMentor vers Adobe Learning Manager_

5. Sélectionnez l’une des options suivantes :

   - **Désactiver l&#39;accès à Adobe Learning Manager pendant l&#39;exécution** : recommandé si la synchronisation peut entraîner un temps d&#39;arrêt.
   - **Activer l&#39;accès à Adobe Learning Manager pendant l&#39;exécution** : recommandé pour éviter toute interruption des services.
6. Sélectionnez **Exécuter** pour importer toutes les données de la date de début à la date actuelle.

### Affichage de l’historique d’exécution

La page Statut d’exécution répertorie toutes les exécutions de synchronisation dans l’ordre. Si une exécution comporte des erreurs, une icône d’avertissement s’affiche. Si nécessaire, vous pouvez vérifier le journal des erreurs, corriger le fichier CSV et réexécuter la dernière synchronisation.

Pour afficher l’historique d’exécution :

1. Sélectionnez **État d&#39;exécution** dans le volet de gauche.
2. Les colonnes suivantes s’affichent :
   - **Exécuter**
   - **Date de début**
   - **Durée**
   - **Type** (planifié ou à la demande)
   - **État** (En cours ou Terminé)

   ![](assets/harvard-managementor-connector8.png)
   _Afficher l&#39;état d&#39;exécution des importations à la demande et planifiées_

>[!NOTE]
>
>Si vous supprimez et recréez une connexion, l’historique d’exécution des exécutions précédentes reste visible. Vous ne pouvez réexécuter que la dernière synchronisation.

### Configuration requise pour la synchronisation

Assurez-vous que les fichiers suivants sont présents dans le dossier Harvard ManageMentor FTP :

- **hmm12_metadata.csv** Ce fichier contient des métadonnées de cours. Respectez le format de dénomination de fichier correct.
- **client_hmm12_yyyyMMdd.csv** Ce fichier est le flux de l’utilisateur. Le format de la date doit correspondre à aaaaMMjj.

**Fichiers d’exemple**

- [Fichier de métadonnées de cours pour le connecteur Harvard ManageMentor](https://experienceleague.adobe.com/docs/learning-manager/assets/hmm12-metadata.csv?lang=en)
- [Fichier de flux utilisateur pour le connecteur Harvard ManageMentor](https://experienceleague.adobe.com/docs/learning-manager/assets/client-hmm12-20170304.csv?lang=en)
