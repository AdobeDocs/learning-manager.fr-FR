---
description: Découvrez comment intégrer le connecteur Power BI à Adobe Learning Manager
jcr-language: en_us
title: Connecteur Power BI
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 4%

---


# Connecteur Power BI dans Adobe Learning Manager

## Introduction

Le connecteur Power BI vous permet d’intégrer Adobe Learning Manager à Microsoft Power BI (licence commerciale) afin que vous puissiez analyser, visualiser et partager vos données d’apprentissage.

Grâce à cette intégration, l’administrateur d’intégration peut exporter automatiquement des jeux de données dynamiques tels que les relevés de notes des élèves, les compétences des utilisateurs et les rapports d’activité xAPI directement vers un espace de travail Power BI sélectionné.

Une fois connecté, vous pouvez utiliser toutes les fonctionnalités de Power BI pour créer des tableaux de bord et des rapports personnalisés. Cela permet à votre organisation d&#39;obtenir des informations plus approfondies sur la progression des élèves, les compétences acquises et l&#39;efficacité de la formation, et de prendre des décisions éclairées basées sur des données d&#39;apprentissage en temps réel.

>[!NOTE]
>
>Adobe Learning Manager ne prend en charge l’intégration qu’avec la version commerciale de Microsoft Power BI. L’intégration à la version Government Cloud n’est pas prise en charge.

## Conditions préalables

- Seul le Power BI Microsoft avec une **licence commerciale** est pris en charge.
- Assurez-vous que vous êtes autorisé à créer des applications Power BI et des espaces de travail.
- Obtenez votre **nom de client**, votre **ID client d&#39;application**, votre **secret client d&#39;application** et votre **ID d&#39;espace de travail** (facultatif).

## Configuration du connecteur de Power BI

Pour connecter ALM à Power BI :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Passez le curseur de la souris sur la vignette du connecteur **Power BI** et sélectionnez **Connecter**.

   ![](assets/power-bi-connector1.png)
   _Sélectionnez Se connecter pour configurer le connecteur de Power BI_

3. Saisissez les informations suivantes :

   - ID du client
   - Secret du client
   - Nom du client
   - ID de l’espace de travail (facultatif)

   ![](assets/power-bi-connector2.png)
   _Tapez les informations requises pour configurer Power BI_

4. Sélectionnez **Se connecter**.

## Enregistrement de l’application de Power BI

Pour enregistrer l’application de Power BI :

1. Accédez à [Enregistrer l&#39;application Power BI](https://app.powerbi.com/embedsetup).
2. Sélectionnez **Intégrer pour votre organisation** et connectez-vous à votre compte Microsoft.
3. Saisissez un nom pour votre application.
4. Sélectionnez **Application web côté serveur** sous **Type d&#39;application**.
5. Dans la section **URL de redirection**, sélectionnez **Utiliser une URL personnalisée** et saisissez [cette URL](https://learningmanager.adobe.com/ctr/app/azure/_callback) : (remplacez le domaine si nécessaire pour votre environnement.)
6. Dans le champ **URL d&#39;accueil**, saisissez [cette URL](https://learningmanager.adobe.com/).
7. Dans la section **Autorisations**, sélectionnez **Lire tous les ensembles de données** et **Lire et écrire tous les ensembles de données**.
8. Contactez votre administrateur de Power BI pour obtenir le **nom du client**.
9. Si vous n’avez pas d’ID d’espace de travail, créez-en un dans Power BI (Power BI Pro est requis) et copiez l’ID à partir de l’URL.
10. Sélectionnez **Enregistrer l&#39;application** et enregistrez l&#39;**ID de client** et le **secret du client** pour une utilisation ultérieure.

>[!NOTE]
>
>Si vous devez réautoriser la connexion ultérieurement, créez une nouvelle application de Power BI et utilisez l’URL de redirection appropriée pour votre environnement.

## Exportation de rapports vers Power BI

Après avoir configuré la connexion, vous pouvez exporter ces rapports :

- **Relevés de notes de l&#39;élève**
- **Compétences des utilisateurs**
- **Rapports d&#39;activité xAPI**
- **Rapports unifiés** (combinaison de plusieurs rapports)

### Relevé de notes de l&#39;élève

#### Planification des exportations

1. Sélectionnez **Relevés de notes des élèves** dans le panneau de gauche.
2. Sélectionnez **Activer la planification** sur la page Exporter.
3. Sélectionnez **date de début** et **heure**.
4. Définissez l&#39;**intervalle** pour la fréquence à laquelle l&#39;exportation doit se répéter (quotidiennement, hebdomadairement, etc.).

   ![](assets/power-bi-connector3.png)
   _Activer l&#39;exportation de la planification pour le relevé de notes de l&#39;élève_

5. Sélectionnez **Enregistrer**.

#### Exportation sur demande

- Vous pouvez générer des rapports manuellement en spécifiant la **date de début** et en exécutant une exportation à la demande.
- Le rapport contiendra des données allant de la date spécifiée jusqu&#39;à aujourd&#39;hui.

### Compétences des utilisateurs

#### Planification des exportations

1. Sélectionnez **Compétences d&#39;utilisateur** dans le panneau de gauche.
2. Sélectionnez **Activer la planification** sur la page Exporter.
3. Sélectionnez **date de début** et **heure**.
4. Définissez l&#39;**intervalle** pour la fréquence à laquelle l&#39;exportation doit se répéter (quotidiennement, hebdomadairement, etc.).

   ![](assets/power-bi-connector4.png)
   _Activer l&#39;exportation planifiée du rapport des compétences des utilisateurs_

5. Sélectionnez **Enregistrer**.

#### Exportation sur demande

- Vous pouvez générer des rapports manuellement en spécifiant la **date de début** et en exécutant une exportation à la demande.
- Le rapport contiendra des données allant de la date spécifiée jusqu&#39;à aujourd&#39;hui.

### Gestion des rapports d’activité xAPI

Les **instructions xAPI** peuvent également être exportées vers Power BI.

#### Configuration des exportations xAPI

1. Sélectionnez **Exporter le rapport d&#39;activité xAPI**.
2. Sélectionnez **Configuration** dans le volet de gauche.

   - Renseignez les champs de chemin JSON pour qu’ils correspondent à vos colonnes CSV.
   - Sélectionnez **Ajouter** pour inclure d&#39;autres chemins.
   - Utilisez **Modifier** pour mettre à jour les champs.
3. Sélectionnez **Enregistrer**.

#### Planification des exportations

1. Sélectionnez **Configurer la planification**.
2. Sélectionnez **Activer l&#39;exportation des instructions xAPI à l&#39;aide de cette connexion**.
3. Définissez la **date de début**, l&#39;**heure** et l&#39;**intervalle**.
4. Sélectionnez **Enregistrer**.

#### Exportation à la demande

1. Sélectionnez **À la demande**.
2. Spécifiez la **date de début**.
3. Sélectionnez **Exécuter**.

>[!NOTE]
>
>Si certaines instructions xAPI dans le magasin d’enregistrements d’apprentissage (LRS) ne disposent pas de chemins JSON configurés, leurs valeurs apparaissent comme N/A dans le Power BI.

#### Afficher l’état d’exécution

- Utilisez l&#39;**état d&#39;exécution** pour afficher l&#39;historique des exportations, y compris l&#39;heure de début, la durée et l&#39;état.
- Une icône d’avertissement indique les exécutions ayant échoué. Cliquez sur le lien pour télécharger les rapports d’erreur au format .CSV.

### Rapports unifiés

**Les rapports unifiés** combinent les données de :

- Relevé de notes de l&#39;élève
- Ludification
- Rapport de commentaires
- Connexion/Accès
- Compétence de l’utilisateur
- Rapport d’utilisateur
- Rapport de formation

Cela vous aide à créer des tableaux de bord plus puissants en fusionnant des données dans Power BI.

#### Création d’une configuration de rapport unifiée

1. Sélectionnez **Rapports unifiés**, puis **Configuration**.
2. Saisissez un nom unique dans le champ **Nom de l&#39;ensemble de données**.
3. Sélectionnez un ou plusieurs rapports à inclure dans ce jeu de données sous **Sélectionner des rapports pour l&#39;exportation de données**.

   - Relevé de notes de l&#39;élève
   - Connexion/Accès
   - Rapport de formation
   - Ludification
   - Compétence de l’utilisateur
   - Rapport de commentaires
   - Rapport d’utilisateur
4. Utilisez le champ **Ajouter des filtres de groupe d&#39;utilisateurs** pour sélectionner les données des groupes d&#39;utilisateurs que vous souhaitez exporter. Par défaut, **Tous les utilisateurs** est sélectionné.
5. Utilisez le champ **Ajouter des filtres de catalogue de contenu** pour filtrer les rapports par catalogue de contenu.
6. Le tableau de filtres indique les rapports qui prennent en charge les filtres **Groupe d&#39;utilisateurs**, **Catalogue** ou **Heure**.

   ![](assets/power-bi-connector5.png)
   _Créer une configuration pour les rapports unifiés_

7. Après avoir sélectionné des rapports et des filtres, sélectionnez **Enregistrer** en haut à droite.

#### Filtrer les relevés de notes des élèves par statut

- **Tous :** tous les enregistrements de la période
- **Terminé :** seules les activités d&#39;apprentissage terminées
- **En cours :** activités en cours uniquement
- **Pas commencé :** exclut les enregistrements non encore démarrés
- **Désinscrit :** inclut les enregistrements désinscrits

## Télécharger des modèles de Power BI

Adobe fournit des modèles de Power BI prêts à l’emploi pour vous aider à démarrer rapidement.

- Téléchargez des modèles, importez vos rapports et personnalisez-les selon vos besoins.
- Utilisez des modèles pour créer des tableaux de bord attrayants sans repartir de zéro.

## Paramètres liés au parcours d’apprentissage

L’affichage des **parcours d’apprentissage** dans vos rapports dépend de vos paramètres d’administration :

- **Connexions existantes :**

   - Si **Parcours d’apprentissage** est désactivé, aucune ligne ou colonne associée n’est incluse.
   - Si cette option est activée, le rapport inclut le parcours d’apprentissage (niveau supérieur) pour les élèves inscrits.

- **Nouvelles connexions :**

   - Si le parcours d’apprentissage est désactivé, les colonnes affichent :

      - **Parcours intégré :** nom du programme d’apprentissage.
      - **ID du parcours intégré :** ID pour le programme d’apprentissage.
      - **ID de cours intégré :** ID de cours dans le parcours d’apprentissage.
   - Si cette option est activée, la colonne **Type** utilise le parcours d’apprentissage (niveau supérieur), le cas échéant.
   - Pour les nouvelles connexions, les modifications s’appliquent après 30 jours.

### Où voir vos données **

Toutes les données exportées apparaissent sous forme de jeux de données sous votre compte Power BI. Utilisez-les pour créer des tableaux de bord et des visualisations personnalisés.
