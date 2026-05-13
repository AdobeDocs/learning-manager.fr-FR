---
description: Découvrez comment intégrer le connecteur ADFS à Adobe Learning Manager
jcr-language: en_us
title: Connecteur ADFS
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 3%

---


# Connecteur ADFS dans Adobe Learning Manager

## Introduction

Le connecteur ADFS dans Adobe Learning Manager vous permet d’intégrer Microsoft Azure Active Directory à l’aide des services ADFS (Active Directory Federation Services). Cette intégration permet la synchronisation automatique des données utilisateur d’Azure AD vers Learning Manager. Grâce à des fonctionnalités telles que le mappage des attributs, le filtrage des utilisateurs et les importations planifiées, le connecteur permet de rationaliser la gestion des utilisateurs et garantit que les données des élèves restent précises et à jour. Elle est particulièrement utile pour les organisations qui s’appuient sur ADFS pour la gestion centralisée des identités et des accès.

## Conditions préalables

Avant de configurer le connecteur ADFS dans Adobe Learning Manager, effectuez les étapes suivantes dans Azure Portal :

- Enregistrement d’une application
- Génération d’un secret client
- Définir les autorisations d’API

### Enregistrement d’une application dans Azure

Pour enregistrer une application dans Azure :

1. Connectez-vous au [portail Azure](https://portal.azure.com/).
2. Accédez à **Azure Active Directory**.
3. Sélectionnez **Ajouter**, puis **Inscription d&#39;application**.
4. Saisissez un nom pour votre application et sélectionnez **S&#39;inscrire**.

### Génération d’un secret client

Pour créer un secret client :

1. Dans l&#39;application nouvellement enregistrée, accédez à **Certificats et secrets**.
2. Sélectionnez **Nouveau secret client**.
3. Ajoutez une description et définissez l&#39;expiration sur **24 mois**.
4. Enregistrez la **valeur de secret du client** dans un emplacement sécurisé.

### Définir les autorisations d’API

Pour ajouter une autorisation d’API :

1. Sélectionnez **Autorisations API**, puis **Ajouter une autorisation**.
2. Sélectionnez **Microsoft Graph**, puis **Autorisations de l&#39;application**.
3. Recherchez et sélectionnez les autorisations suivantes :

   - **Directory.Read.All** - Lire les données du répertoire
   - **User.Read.All** - Lire les profils complets de tous les utilisateurs
4. Sélectionnez **Ajouter des autorisations**.
5. Accordez le **consentement de l&#39;administrateur** pour les autorisations.

## Configuration du connecteur ADFS dans Learning Manager

Vous pouvez configurer le connecteur ADFS dans Adobe Learning Manager pour importer les données utilisateur à partir d’ADFS, exporter les compétences des utilisateurs vers ADFS et planifier des synchronisations automatisées pour maintenir les deux systèmes à jour.

Pour configurer le connecteur ADFS :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Survolez la vignette du connecteur **ADFS**.
3. Sélectionnez **Se connecter**.

   ![](assets/adfs-connector1.png)
   _Sélectionnez Se connecter pour configurer le connecteur ADFS_

### Saisir les détails de la connexion

Sur la page de configuration ADFS :

1. Saisissez les informations suivantes :

   - Nom de la connexion
   - ID du client
   - Secret du client

   ![](assets/adfs-connector2.png)
   _Tapez les détails de configuration pour connecter ADFS_

2. Sélectionnez **Se connecter**.
3. Adobe Learning Manager récupérera et remplira automatiquement l&#39;**ID du locataire** et le **domaine principal** à partir de votre portail Azure.

## Importation d’utilisateurs à partir d’ADFS

### Attributs de mappage

- Les administrateurs d’intégration peuvent mapper les attributs ADFS aux attributs regroupables correspondants dans Adobe Learning Manager.
- Ce mappage est une configuration unique qui est réutilisée pour toutes les importations utilisateur suivantes.
- Vous pouvez modifier le mappage d’attributs à tout moment si nécessaire.

### Importation automatisée d’utilisateurs

- Adobe Learning Manager extrait automatiquement les données utilisateur d’ADFS à intervalles réguliers.
- Cela permet de garder les enregistrements d’utilisateur synchronisés entre les systèmes.

### Filtrage des utilisateurs

- Les administrateurs peuvent appliquer des filtres pour limiter les utilisateurs importés.
- Par exemple, n’importez que les utilisateurs sous des responsables ou des services spécifiques.
