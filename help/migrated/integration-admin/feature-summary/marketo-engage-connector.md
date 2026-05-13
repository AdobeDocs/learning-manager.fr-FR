---
description: Découvrez comment intégrer le connecteur de Marketo Engage à Adobe Learning Manager
jcr-language: en_us
title: Connecteur Marketo Engage
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 3%

---


# Connecteur Marketo Engage dans Adobe Learning Manager

## Introduction

Le connecteur de Marketo Engage permet à Adobe Learning Manager de s’intégrer de manière transparente à Marketo Engage, une plateforme d’automatisation du marketing. Cette intégration aide les spécialistes du marketing à suivre et à agir sur les données de comportement des élèves de Adobe Learning Manager en les synchronisant avec la base de données Marketo.

Le connecteur de Marketo Engage permet une synchronisation transparente des données entre les deux systèmes et permet aux spécialistes du marketing d’utiliser les données d’activité d’apprentissage pour créer des campagnes marketing ciblées.

Le connecteur de Marketo Engage vous permet de :

- Ajouter ou mettre à jour automatiquement les prospects dans la base de données du Marketo Engage lorsque des utilisateurs sont ajoutés à Adobe Learning Manager.
- Synchronisez les comportements d’apprentissage des utilisateurs tels que les inscriptions aux cours, les achèvements, les affectations de compétences et les achèvements de compétences en tant qu’objets personnalisés dans Marketo.
- Créez des campagnes dynamiques dans Marketo en utilisant ces données, en tirant parti de fonctionnalités telles que les **listes dynamiques**.

Cette intégration aide les spécialistes du marketing à cibler les publics en fonction de leur parcours d’apprentissage dans Adobe Learning Manager.

## Fonctionnalités clés

- Création et mises à jour automatisées de prospects en fonction des utilisateurs Adobe Learning Manager.
- Exportez l’activité d’apprentissage (inscriptions, achèvements, compétences acquises) sous forme d’objets personnalisés vers Marketo.
- Planifiez ou déclenchez des exportations à la demande.
- Prise en charge des rapports unifiés, notamment :
   - Rapport d’utilisateur
   - Relevés de notes
   - Rapport sur les compétences des utilisateurs

## Conditions préalables

Avant l’intégration, assurez-vous que votre compte Marketo prend en charge la création de schémas via les API.

Vous aurez besoin des détails suivants pour créer la connexion :

- **Nom de la connexion**
- **ID client**
- **Clé secrète du client**
- **Domaine du Marketo Engage**

>[!NOTE]
>
>Vous pouvez obtenir l&#39;ID client et le secret client à partir de l&#39;application de Marketo Engage sous **LaunchPoint**, et le domaine à partir de la section **Services Web**.

## Configuration du connecteur

Pour configurer le connecteur du Marketo Engage :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Passez le curseur de la souris sur la vignette **Marketo Engage** et sélectionnez **Se connecter**.

   ![](assets/marketo-engage-connector1.png)
   _Sélectionnez Se connecter pour configurer le connecteur de Marketo Engage_

3. Saisissez les informations d’identification requises.

   - Nom de la connexion
   - ID du client
   - Secret du client
   - Domaine Marketo Engage

   ![](assets/marketo-engage-connector2.png)
   _Saisissez les informations requises pour le connecteur Marketo Engage_

4. Sélectionnez **Se connecter** pour établir la connexion.

## Événements et déclencheurs de campagne

Vous pouvez déclencher des exportations de données vers Marketo Engage en fonction des événements suivants :

- Un nouvel utilisateur est ajouté à Adobe Learning Manager.
- Un utilisateur est inscrit à un cours.
- Un utilisateur termine un cours.
- Un utilisateur est inscrit à une compétence.
- Un utilisateur remplit une compétence.

Ces événements peuvent être exportés **à la demande** ou **de manière planifiée**.

## Mappage de colonnes

Marketo utilise deux bases de données :

- **Base de données de prospects** : pour les enregistrements d&#39;utilisateur (prospects)
- **Base de données d&#39;objets personnalisée** : pour les enregistrements d&#39;activités et d&#39;événements personnalisés

Pour mapper des champs entre Adobe Learning Manager et Marketo :

1. Les champs **Rapport utilisateur** de Adobe Learning Manager sont affichés dans une colonne.
2. Les **champs Marketo** correspondants sont répertoriés dans la colonne adjacente.
3. Mappez les champs appropriés de Learning Manager vers Marketo pour créer et mettre à jour des prospects.
4. Après le mappage, tous les utilisateurs exportés apparaissent comme des prospects dans la base de données des prospects Marketo.

Les rapports exportés dans la section **Objets personnalisés Marketo** portent le préfixe « cp_ ».

## Exportation prise en charge

Vous pouvez exporter les événements utilisateur suivants vers votre instance de Marketo Engage :

- Nouvel utilisateur ajouté
- Métadonnées utilisateur mises à jour
- Activité de l’utilisateur mise à jour
- Inscription aux formations
- Auto-inscription
- Achèvement des compétences

Ces exportations aident à stimuler l’engagement et à personnaliser les campagnes de sensibilisation en utilisant les données des activités d’apprentissage.
