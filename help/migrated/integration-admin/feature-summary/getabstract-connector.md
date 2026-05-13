---
description: connecteur getAbstract dans Adobe Learning Manager
jcr-language: en_us
title: Connecteur getAbstract
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 1%

---


# connecteur getAbstract pour Adobe Learning Manager

## Introduction

Le **connecteur getAbstract** est conçu pour les entreprises clientes de [getAbstract.com](https://www.getabstract.com/). Cela permet aux élèves de découvrir et d’utiliser du contenu getAbstract directement via Adobe Learning Manager. Le connecteur permet également aux administrateurs d’importer les données d’engagement des utilisateurs et de suivre automatiquement les enregistrements d’achèvement des élèves.

Adobe Learning Manager souhaite offrir aux élèves des possibilités d’apprentissage continu et autonome axées sur le leadership et les compétences non techniques. Au lieu de développer tout le contenu en interne, l’administrateur connecte le compte getAbstract de l’organisation à Adobe Learning Manager à l’aide du connecteur getAbstract.

- Importe automatiquement du contenu getAbstract dans Adobe Learning Manager.
- Suit la consommation des cours et des parcours d’apprentissage par les élèves.

Cet article décrit les étapes à suivre pour configurer et gérer le connecteur getAbstract dans Adobe Learning Manager.

## Conditions préalables

- Assurez-vous que la fonctionnalité **Migration** est activée pour votre compte avant de configurer le connecteur.
- Obtenez l&#39;**ID client** et le **secret client** auprès de votre représentant de compte getAbstract. Ces informations d&#39;identification sont requises pour récupérer les métadonnées de cours et les données de consommation des utilisateurs.

## Configurer le connecteur getAbstract

Le connecteur getAbstract permet aux administrateurs Adobe Learning Manager d’améliorer l’expérience d’apprentissage en intégrant du contenu de haute qualité et organisé à partir de getAbstract.

Pour configurer le connecteur getAbstract :

1. Connectez-vous en tant qu’administrateur d’intégration.
2. Sélectionnez **getAbstract** sur la page d&#39;accueil.
3. Sélectionnez l&#39;une des options suivantes sur la vignette **Connecteur** :

   - **Prise en main** : présentation du connecteur.
   - **Connexion** : créez une connexion.
   - **Gérer les connexions** : affichez ou modifiez les connexions existantes.

   ![](assets/getabstract-connector1.png)
   _La vignette getAbstract présente trois options de configuration_

## Créer une connexion

Pour créer une connexion :

1. Sélectionnez **Se connecter**.

   ![](assets/getabstract-connector2.png)
   _Sélectionnez Se connecter sur la vignette getAbstract pour créer une nouvelle connexion_

2. Tapez un **nom de connexion**.
3. Saisissez l&#39;**ID client** et la **clé secrète client**.

   ![](assets/getabstract-connector3.png)
   _Tapez la connexion, l&#39;ID client et le secret client sur la page de connexion getAbstract_

4. Sélectionnez **Enregistrer** pour créer la connexion.

## Gérer le connecteur getAbstract

Avant d&#39;importer des données, vous devez configurer le connecteur et définir une planification de synchronisation. Une fois configuré, le connecteur extrait automatiquement les données d’utilisation, ce qui vous permet de surveiller la progression des élèves et d’inclure du contenu getAbstract dans les plans d’apprentissage et les rapports.

### Activer la connexion

Pour activer la connexion :

1. Sélectionnez **Gérer les connexions** sur la vignette **getAbstract**.

   ![](assets/getabstract-connector4.png)
   _Gérer les connexions pour configurer et planifier l&#39;importation de données_

2. Sélectionnez la connexion.
3. Sélectionnez **Configurer** dans le volet de navigation de gauche.
4. Sélectionnez **Activer la connexion**, puis **Enregistrer**.

   ![](assets/getabstract-connector5.png)
   _Activez la connexion pour importer les données de getAbstract vers Adobe Learning Manager_

### Modifier la connexion

Pour modifier la connexion :

1. Sélectionnez **Gérer les connexions** sur la vignette **getAbstract**.
2. Sélectionnez la connexion.
3. Sélectionnez **Configurer** dans le volet de navigation de gauche.
4. Sélectionnez **Modifier** pour mettre à jour l&#39;**ID client** et la **clé secrète client**.

   ![](assets/getabstract-connector6.png)
   _Modifier les informations d&#39;identification, y compris l&#39;ID client et le secret client_

5. Sélectionnez **Enregistrer**.

### Planification de la synchronisation

Pour planifier la synchronisation :

1. Sélectionnez **Gérer les connexions** sur la vignette **getAbstract**.
2. Sélectionnez la connexion.
3. Sélectionnez **Configurer** dans le volet de navigation de gauche.
4. Sélectionnez **Activer la planification** dans la section **Planification de la synchronisation**.

   ![](assets/getabstract-connector7.png)
   _Planifier l&#39;importation de données de getAbstract vers Adobe Learning Manager_

5. Sélectionnez la date et l&#39;heure de début en UTC.
6. Tapez le nombre de jours après lequel la synchronisation doit se répéter.
7. Sélectionnez **Enregistrer**.

Les paramètres de synchronisation sont enregistrés. Le connecteur s’exécute selon le planning et importe les données de getAbstract dans Adobe Learning Manager.

## Exécuter la synchronisation à la demande

L&#39;option **Synchronisation à la demande** vous permet d&#39;importer manuellement des données de getAbstract dans Adobe Learning Manager. Cela est utile lorsque vous souhaitez mettre à jour immédiatement les données d’activité des élèves, sans attendre la prochaine synchronisation planifiée.

Pour exécuter l’importation de données à la demande :

1. Sélectionnez **Gérer les connexions** sur la vignette **getAbstract**.
2. Sélectionnez la connexion.
3. Sélectionnez **Exécution à la demande** dans le volet de gauche.
4. Sélectionnez **Date de début**.

   ![](assets/getabstract-connector8.png)
   _Exécutez la demande à la demande pour l&#39;importation immédiate des données de getAbstract vers Adobe Learning Manager_

5. Sélectionnez l’une des options suivantes :

   - **Désactiver l&#39;accès à Adobe Learning Manager pendant l&#39;exécution** : recommandé si la synchronisation peut entraîner un temps d&#39;arrêt.
   - **Activer l&#39;accès à Adobe Learning Manager pendant l&#39;exécution** : recommandé pour éviter toute interruption des services.
6. Sélectionnez **Exécuter** pour importer toutes les données de la date de début à la date actuelle.

### Affichage de l’historique d’exécution

La page **État d&#39;exécution** répertorie toutes les exécutions de synchronisation dans l&#39;ordre. Si une exécution comporte des erreurs, une icône d’avertissement s’affiche. Vous pouvez vérifier le journal des erreurs, corriger le fichier CSV et réexécuter la dernière synchronisation si nécessaire.

Pour afficher l’historique d’exécution :

1. Sélectionnez **État d&#39;exécution** dans le volet de gauche.
2. Les colonnes suivantes s’affichent :
   - **Exécuter**
   - **Date de début**
   - **Durée**
   - **Type** (planifié ou à la demande)
   - **État** (En cours ou Terminé)

   ![](assets/getabstract-connector9.png)
   _Afficher l&#39;état d&#39;exécution des importations à la demande et planifiées_

>[!NOTE]
>
>Si vous supprimez et recréez une connexion, l’historique d’exécution des exécutions précédentes reste visible. Vous ne pouvez réexécuter que la dernière synchronisation.

### Conditions requises pour une synchronisation réussie

Pour garantir le bon fonctionnement de la synchronisation :

- Un fichier de flux utilisateur valide doit se trouver dans le dossier FTP getAbstract pour les dates de synchronisation spécifiées.
- Le fichier doit suivre le format de dénomination :
   - report_export_yyyy_MM_dd_HHmmss.xlsx ou,
   - report_export_yyyy_MM_dd.xlsx

Téléchargez un [exemple de fichier de flux utilisateur getAbstract](https://experienceleague.adobe.com/docs/learning-manager/assets/report-export-20170401175342.xlsx?lang=en) pour comprendre le format.
