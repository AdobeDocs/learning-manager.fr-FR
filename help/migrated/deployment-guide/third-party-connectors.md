---
description: Découvrez comment intégrer Salesforce à Learning Manager à l’aide de connecteurs, comment intégrer FTP à Learning Manager et charger un fichier CSV automatiquement à l’aide du connecteur FTP.
jcr-language: en_us
title: Connecteurs Learning Manager
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '6293'
ht-degree: 72%

---



# Connecteurs Learning Manager

Découvrez comment intégrer Salesforce à Learning Manager à l’aide de connecteurs, comment intégrer FTP à Learning Manager et charger un fichier CSV automatiquement à l’aide du connecteur FTP.

Les entreprises disposent d’autres applications et systèmes devant éventuellement être intégrés à Learning Manager. Les connecteurs sont des utilitaires qui facilitent l’exécution d’intégrations basées sur des données, telles que l’importation de données dans Learning Manager à partir de systèmes externes ou l’exportation de données vers des systèmes externes à partir de Learning Manager. Dans la version de juillet 2016, les connecteurs permettent uniquement d’importer en bloc des utilisateurs pour Learning Manager à partir de systèmes externes.

Learning Manager fournit des connecteurs Salesforce et FTP. À l’aide du connecteur Salesforce, les administrateurs d’intégration d’une entreprise peuvent intégrer leurs applications Salesforce à Learning Manager. En tant qu’intégrateur, vous pouvez également utiliser le connecteur FTP pour importer automatiquement un groupe d’utilisateurs dans l’application de votre entreprise.

Learning Manager fournit également les connecteurs Lynda, GetAbstract et Harvard Management System qui permettent aux élèves d’accéder aux cours de Lynda.com, GetAbstract et Harvard ManageMentor et de les suivre.

Lisez ce qui suit pour savoir comment configurer et utiliser chacun de ces connecteurs dans Learning Manager.

![](assets/connectorslist.jpg)

## Connecteur Salesforce {#sfconnector}

Le connecteur Salesforce connecte les comptes Learning Manager et Salesforce pour automatiser la synchronisation des données. Les fonctionnalités du connecteur Salesforce sont les suivantes :

### Attributs de mappage

L’administrateur d’intégration peut choisir les colonnes Salesforce et les mapper à des attributs compatibles avec des groupes de Learning Manager correspondants. Il s’agit d’une opération unique. Une fois le mappage terminé, le même mappage est utilisé lors des prochaines importations de l’utilisateur. Il peut être reconfiguré si l’administrateur souhaite avoir un mappage différent pour importer des utilisateurs.

### Importation automatisée d’utilisateurs

L’importation des utilisateurs permet à l’administrateur de Learning Manager de récupérer les détails des employés à partir de Salesforce et de les importer dans Learning Manager automatiquement. Cette automatisation évite l’effort manuel lié à la création d’un fichier CSV et à son chargement dans Learning Manager.

### Planification automatique

L’utilisation de la fonctionnalité de planification automatique avec la fonctionnalité d’importation automatisée d’utilisateur peut être efficace. L’administrateur de Learning Manager peut configurer une planification en fonction des besoins de l’organisation. Les utilisateurs de l’application Learning Manager peuvent être à jour en fonction de la planification. La synchronisation peut être exécutée de façon quotidienne dans l’application Learning Manager.

### Filtrage des utilisateurs

L’administrateur de Learning Manager peut appliquer un filtrage sur les utilisateurs avant de les importer. Par exemple, l’administrateur de Learning Manager peut choisir d’importer tous les utilisateurs sous un ou plusieurs responsables spécifiques dans la hiérarchie.

## Configurer le connecteur Salesforce {#configuresalesforceconnector}

Découvrez le processus d’intégration de Learning Manager à Salesforce.

### Prérequis {#prerequisites}

Assurez-vous de disposer de l’URL de votre organisation Salesforce. Par exemple, si le nom de votre organisation est **myorg**, l’URL Salesforce peut être [ https://myorg.salesforce.com.](https://myorg.salesforce.com/) Il s’agit de la seule opération requise pour connecter le compte Salesforce à Learning Manager.

Veillez également à disposer des informations d’identification appropriées pour vous connecter au compte.

## Créer une connexion {#createaconnection}

1. Dans la page d’accueil de Learning Manager, placez le curseur de la souris au-dessus de l’icône Salesforce. Un menu s’affiche. Cliquez sur l’élément **[!UICONTROL Connecter]** dans le menu.

   ![](assets/mouserover-salesforce.png)

1. Une boîte de dialogue s’affiche vous invitant à entrer l’URL de l’organisation. Cliquez sur **[!UICONTROL Se connecter]** après avoir fourni l&#39;URL.
1. En cas de réussite de la connexion, la page de présentation s’affiche.

## Attribut de mappage {#mapattributes}

Une fois la connexion établie, vous pouvez mapper les colonnes Salesforce aux attributs correspondants de Learning Manager. Cette étape est obligatoire.

1. Sur la gauche de la page de mappage, vous pouvez voir les colonnes de Learning Manager et sur la droite, les colonnes Salesforce. Sélectionnez le nom de colonne approprié qui correspond au nom de colonne de Learning Manager.

   ![](assets/sfdc-map-columns.png)

   Les données de la colonne Learning Manager affichées sur le côté gauche sont extraites des champs actifs. Le champ **responsable** doit nécessairement être mappé à un champ d&#39;adresse e-mail de type. Le mappage de toutes les colonnes est obligatoire pour que le connecteur puisse être utilisé.

1. Cliquez sur **[!UICONTROL Enregistrer]** après avoir terminé le mappage.
1. Le connecteur est maintenant prêt à l’emploi. Le compte qui a été configuré s’affiche comme une source de données dans l’application de l’administrateur pour que l’administrateur programme l’importation ou pour une synchronisation à la demande.

## Utilisation du connecteur Salesforce {#usingsalesforceconnector}

Le connecteur Salesforce se connecte à Salesforce.com pour récupérer les utilisateurs selon la configuration et les ajouter à Learning Manager.

## Connecteur FTP Learning Manager {#ftpconnector}

À l’aide du connecteur FTP, vous pouvez intégrer Learning Manager à des systèmes externes arbitraires pour automatiser la synchronisation des données. Les systèmes externes doivent pouvoir exporter des données au format CSV et les placer dans le dossier approprié du compte FTP de Learning Manager. Les fonctionnalités du connecteur FTP sont les suivantes :

Vous pouvez également utiliser le connecteur Box pour la migration de données, l’importation d’utilisateurs et l’exportation de données. Pour plus d’informations, voir [Connecteur Box.](third-party-connectors.md#main-pars_header_302653946)

## Importation de données {#dataimport}

L’importation des utilisateurs permet à l’administrateur de Learning Manager de récupérer les détails des employés à partir de Salesforce et de les importer dans Learning Manager automatiquement. Grâce à cette fonction, vous pouvez intégrer plusieurs systèmes en plaçant le fichier CSV généré par ces systèmes dans les dossiers appropriés des comptes FTP. Learning Manager choisit les fichiers CSV, les fusionne et importe les données en fonction de la planification. Reportez-vous à la fonctionnalité de planification pour plus d’informations.

**Attributs de mappage**

L’administrateur d’intégration peut sélectionner les colonnes du fichier CSV et les mapper aux attributs compatibles avec les groupes de Learning Manager. Ce mappage est une opération unique. Une fois le mappage terminé, le même mappage est utilisé lors des importations suivantes des utilisateurs. Le mappage peut être reconfiguré si l’administrateur souhaite un mappage différent pour l’importation des utilisateurs.

## Exporter des données {#exportdata}

Vous pouvez désormais exporter des compétences d’utilisateur vers un emplacement FTP à des fins d’intégration avec un système tiers.

## Planification {#scheduling}

L’administrateur peut définir des tâches de planification en fonction des besoins de l’organisation et les utilisateurs de l’application Learning Manager sont à jour selon la planification. De même, l’administrateur d’intégration peut planifier l’exportation des compétences en temps opportun à des fins d’intégration avec un système tiers. La synchronisation peut être exécutée de façon quotidienne dans l’application Learning Manager.

## Configuration du connecteur FTP Learning Manager {#configurecaptivateprimeftpconnector}

Découvrez le processus d’intégration de Learning Manager au connecteur FTP.

### Création d’une connexion {#Createaconnection-1}

1. Dans la page d’accueil de Learning Manager, placez le curseur de la souris au-dessus de l’icône Salesforce. Un menu s’affiche. Cliquez sur l’élément **[!UICONTROL Connecter]** dans le menu.

   ![](assets/mouseover-ftpconnector.png)

1. Une boîte de dialogue s’affiche vous invitant à entrer l’ID de messagerie. Indiquez l’ID de messagerie de la personne responsable de la gestion du compte FTP de Learning Manager pour l’organisation. Cliquez sur **[!UICONTROL Se connecter]** après avoir fourni l&#39;ID de messagerie.
1. Learning Manager vous envoie un courrier électronique invitant l’utilisateur à réinitialiser le mot de passe avant d’accéder au FTP pour la première fois. L’utilisateur doit réinitialiser le mot de passe et l’utiliser pour accéder au compte FTP Learning Manager.

   Un seul compte FTP Learning Manager peut être créé pour un compte Learning Manager donné.

   Dans la page de présentation, vous pouvez spécifier le nom de connexion pour votre intégration. Sélectionnez les mesures à prendre parmi les options suivantes :

   * Importer les utilisateurs internes
   * Exporter les compétences des utilisateurs : configurer un calendrier
   * Exporter les compétences des utilisateurs : sur demande

   ![](assets/connectors-overview.png)

## Importation

+++Utilisateur interne

L’option d’importation d’utilisateur interne vous permet de planifier la génération du rapport d’importation d’utilisateur automatiquement. Les rapports générés vous sont envoyés au format CSV.

+++

+++Attributs de mappage

Une fois la connexion établie, vous pouvez associer les colonnes des fichiers CSV qui seront placés dans le dossier FTP aux attributs correspondants de Learning Manager. Cette étape est obligatoire.

1. Sur la gauche de la page Attributs de mappage, vous pouvez voir les colonnes attendues de Learning Manager et sur la droite, les noms des colonnes du fichier CSV. À droite, vous pouvez initialement voir une zone de sélection vide. Importez n&#39;importe quel modèle CSV en cliquant sur **Choisir un fichier**.
1. Les étapes ci-dessus permettent de compléter la liste déroulante de sélection de droite avec tous les noms de colonnes du fichier CSV. Sélectionnez le nom de colonne approprié qui correspond au nom de colonne de Learning Manager.

   *Le champ du gestionnaire doit obligatoirement être mappé à un champ d’adresse électronique. Le mappage de toutes les colonnes est obligatoire pour que le connecteur puisse être utilisé.*

1. Cliquez sur **[!UICONTROL Enregistrer]** après avoir terminé le mappage.

   Le connecteur est maintenant prêt à l’emploi. Le compte que vous venez de configurer s’affiche désormais en tant que source de données dans l’application d’administrateur pour que l’administrateur programme l’importation ou pour une synchronisation à la demande.



+++

+++Utilisation du connecteur FTP Learning Manager

1. Les fichiers CSV de systèmes externes doivent être placés à l’emplacement suivant :

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Remarque :** dans la version de juillet 2016, seule l&#39;importation d&#39;utilisateurs est autorisée. Par conséquent, pour utiliser le connecteur FTP, vous devez vous assurer que les fichiers CSV sont placés dans le dossier suivant :

   `code Home/import/user/internal/*.csv`

1. Le connecteur FTP extrait toutes les lignes des fichiers CSV. Il est donc important que la ligne correspondant à un utilisateur dans un fichier CSV n’apparaisse dans aucun autre fichier CSV.
1. Tous les fichiers CSV doivent contenir les colonnes spécifiées dans le mappage.
1. Tous les fichiers CSV requis doivent être présents dans le dossier avant le début du processus.

Lors de l’importation des utilisateurs dans Learning Manager, l’administrateur doit également déterminer la gestion des utilisateurs dans Learning Manager. Reportez-vous à l&#39;[Aide sur la gestion des utilisateurs](../integration-admin/feature-summary/migration-manual.md#usermanagement) pour en savoir plus.

+++

## Exportation

+++Compétences

Il existe deux options pour exporter les rapports de compétences des utilisateurs.

**[!UICONTROL Compétences d&#39;utilisateur - À la demande]** : vous pouvez spécifier la date de début et exporter le rapport à l&#39;aide de l&#39;option. Le rapport sera extrait à partir de la date entrée jusqu&#39;à présent.

![](assets/user-skills-on-demand.png)

**[!UICONTROL Compétences des utilisateurs : Configurer]** : cette option vous permet de planifier l’extraction du rapport. Cochez la case Activer le calendrier et précisez la date et l’heure de début. Vous pouvez également spécifier l’intervalle auquel vous souhaitez que le rapport soit généré et envoyé.

![](assets/user-skills-configure.png)

+++

Pour ouvrir le dossier d’exportation dans lequel les fichiers exportés seront placés à votre emplacement FTP, ouvrez le lien vers le dossier FTP fourni dans la page Compétences de l’utilisateur comme indiqué ci-dessous.

![](assets/ftp-folder.png)

Les fichiers exportés automatiquement seront présents à l&#39;emplacement **Accueil/Exportation/&#42;Emplacement_FTP&#42;**

Les fichiers exportés automatiquement seront disponibles avec le titre **skill_results_&#42;date du &#42;_au_&#42;date du&#42;.csv**

![](assets/exported-csvs.png)

## Connecteur Lynda {#lyndaconnector}

Le connecteur Lynda peut être utilisé par les clients professionnels de Lynda.com qui souhaitent que leurs élèves découvrent et suivent les cours de Lynda dans Learning Manager. Il est possible de configurer le connecteur pour récupérer les cours de Lynda.com à intervalle régulier avec votre clé API. Une fois qu’un cours est créé dans Learning Manager, les utilisateurs peuvent le rechercher et le suivre. La progression des élèves peut alors être suivie dans Learning Manager.

### Configurer le connecteur Lynda {#configurethelyndaconnector}

1. Dans le tableau de bord intégré de l’administrateur, cliquez sur Lynda.

   Vous verrez la mosaïque contenant trois options : Prise en main, Connexion et Gérer les connexions.

1. Si vous configurez le connecteur Lynda pour la première fois, cliquez sur Connexion.

   Vous devez configurer le compte FTP Exavault avant de configurer ce connecteur.

1. À partir de la page de connexion, indiquez un nom pour votre connecteur. Saisissez l’Appkey et la clé secrète de votre connexion.

   Vous devez contacter votre fournisseur pour obtenir l’Appkey et la clé secrète.

1. Cliquez sur Enregistrer.

   La configuration est enregistrée et la connexion Lynda pour votre compte est ajoutée. Vous pouvez désormais cliquer sur Gérer les connexions à partir de la page d’accueil et modifier votre configuration à tout moment.

1. Si vous avez déjà créé une connexion, cliquez sur Gérer les connexions pour afficher l’ensemble de vos connexions.

   La fonction de migration doit être activée pour votre compte avant de configurer le connecteur.

1. Cliquez sur la connexion à modifier.
1. Dans le volet de gauche, cliquez sur Configurer. Effectuez l’une des opérations suivantes :

   * Affichez ou modifiez les détails de votre compte et la planification de la synchronisation à partir de cette fenêtre. Vous devez cocher la case Activer la connexion si vous souhaitez activer ce compte.
   * Cliquez sur Modifier pour modifier vos informations d’identification. Cliquez sur Réinitialiser pour annuler les modifications apportées à ce champ.
   * Cliquez sur Activer la planification pour planifier la synchronisation. Vous pouvez saisir l’heure et la date de début, puis saisir la fréquence de la synchronisation en nombre de jours. Par exemple, vous pouvez décider d’effectuer la synchronisation tous les 3 jours.

   Cliquez sur Enregistrer pour enregistrer vos modifications.

   ![](assets/lynda.png)

1. Dans le volet de gauche, cliquez sur Exécution sur demande. Cette option vous permet d’importer les flux utilisateur et d’autres données pertinentes de Lynda. Entrez la date de début de l’exécution sur demande, et cliquez sur Exécuter pour exécuter la synchronisation. Toutes les données comprises entre la date de début et la date en cours sont importées.

   * Vous pouvez cliquer sur Désactiver l’accès à Learning Manager lors de l’exécution lorsque l’application subit un temps d’arrêt au cours de la synchronisation.
   * Si vous cliquez sur Activer l’accès à Learning Manager lors de l’exécution, aucune interruption de service ne se produit lors de la synchronisation.

   ![](assets/lynda-ondemand.png)

1. Vous pouvez également cliquer sur État d’exécution dans le volet de gauche à tout moment pour afficher le résumé de toutes les exécutions pour ce connecteur, dans l’ordre chronologique. Vous pouvez afficher la date de début et la durée de la synchronisation, le type de synchronisation (s’il s’agit de synchronisation sur demande) et l’état de la synchronisation (si la synchronisation est en cours ou terminée).

   Lorsque vous supprimez et recréez une connexion, les exécutions précédentes du connecteur se produisent de nouveau. Vous pouvez afficher toutes les exécutions antérieures à la suppression de la connexion.

   Vous pouvez exécuter de nouveau la dernière synchronisation uniquement.

   ![](assets/lynda-executionstatus.png)

## Connecteur getAbstract {#getabstractconnector}

Le connecteur getAbstract peut être utilisé par les clients professionnels de getAbstract.com qui souhaitent que leurs élèves découvrent et lisent les résumés de getAbstract. Il est possible de configurer le connecteur pour récupérer les données d’utilisation à intervalle régulier, en se basant sur les enregistrements d’achèvements des élèves créés dans Learning Manager. Lisez ce qui suit pour savoir comment configurer ce connecteur dans Learning Manager.

### Configurer le connecteur getAbstract {#configurethegetabstractconnector}

1. Dans le tableau de bord intégré de l’administrateur, cliquez sur getAbstract.

   Depuis la mosaïque, vous verrez trois options : Prise en main, Connexion et Gérer les connexions.

1. Si vous configurez le connecteur getAbstract pour la première fois, cliquez sur Connexion.

   Vous devez configurer le compte FTP Exavault avant de configurer ce connecteur.

   Assurez-vous que vous partagez ces informations d’identification FTP avec votre fournisseur de contenu pour accéder aux flux.

1. Saisissez un nom pour votre connexion dans le champ Nom de la connexion.

   Saisissez les clés appropriées dans les champs ID client et Secret client. Vous serez peut-être amené à contacter votre fournisseur pour obtenir les clés appropriées pour ce connecteur.

   Des clés sont nécessaires pour obtenir les métadonnées des cours suivis par le client.

1. Si vous avez déjà établi une connexion, sur la page d’accueil, cliquez sur getAbstract > Gérer les connexions pour afficher et modifier la configuration existante.

   La fonction de migration doit être activée pour votre compte avant de configurer le connecteur.

1. Cliquez sur la connexion dont vous souhaitez consulter ou modifier la configuration.

   ![](assets/getabstractschedulepage.png)

1. Dans le volet de gauche, cliquez sur Configurer. Effectuez l’une des opérations suivantes :

   * Affichez ou modifiez les détails de votre compte et la planification de la synchronisation à partir de cette fenêtre. Vous devez cocher la case Activer la connexion si vous souhaitez activer ce compte.
   * Cliquez sur Modifier pour modifier vos informations d’identification. Cliquez sur Réinitialiser pour annuler les modifications apportées à ce champ.
   * Cliquez sur Activer la planification pour planifier la synchronisation. Vous pouvez saisir l’heure et la date de début, puis saisir la fréquence de la synchronisation en nombre de jours. Par exemple, vous pouvez décider d’effectuer la synchronisation tous les 3 jours.

1. Cliquez sur Enregistrer.

   La configuration est enregistrée et la connexion getAbstract pour votre compte est ajoutée.

1. Dans le volet de gauche, cliquez sur Exécution sur demande. Cette option vous permet d’importer les flux utilisateur et d’autres données pertinentes de getAbstract. Entrez la date de début de l’exécution sur demande, et cliquez sur Exécuter pour exécuter la synchronisation. Toutes les données comprises entre la date de début et la date en cours sont importées.

   * Vous pouvez cliquer sur Désactiver l’accès à Learning Manager lors de l’exécution lorsque l’application subit un temps d’arrêt au cours de la synchronisation.
   * Si vous cliquez sur Activer l’accès à Learning Manager lors de l’exécution, aucune interruption de service ne se produit lors de la synchronisation.

1. Vous pouvez également cliquer sur État d’exécution dans le volet de gauche à tout moment pour afficher le résumé de toutes les exécutions pour ce connecteur, dans l’ordre chronologique. Vous pouvez afficher la date de début et la durée de la synchronisation, le type de synchronisation (s’il s’agit de synchronisation sur demande) et l’état de la synchronisation (si la synchronisation est en cours ou terminée).

   Lorsque vous supprimez et recréez une connexion, les exécutions précédentes du connecteur se produisent de nouveau. Vous pouvez afficher toutes les exécutions antérieures à la suppression de la connexion.

   Vous pouvez exécuter de nouveau la dernière synchronisation uniquement.

   Pour garantir le fonctionnement de tout type de synchronisation, vous devez vous assurer que le flux utilisateur est présent dans le dossier FTP getAbstract pour les dates spécifiées dans la synchronisation.

   Consultez la feuille Excel suivante. Il s’agit d’un exemple de fichier de flux utilisateur getAbstract. Le nom du fichier doit suivre le format **&#x200B; report_export_yyyy_MM_dd_HHmmss.xlsx** ou **report_export_yyyy_MM_dd.xlsx**.
   [Exemple de feuille Excel de flux utilisateur getAbstract](assets/report-export-20170401175342.xlsx)

## Connecteur Harvard ManageMentor {#hmmconnector}

Le connecteur Harvard ManageMentor peut être utilisé par les clients professionnels de Harvard ManageMentor qui aimeraient que leurs élèves découvrent et suivent les cours de Harvard ManageMentor. Ce connecteur aide à créer des cours dans Learning Manager et peut être configuré pour récupérer les données de progression des élèves à intervalle régulier. Procédez comme suit pour configurer ce connecteur :

### Configurer le connecteur Harvard ManageMentor {#configuretheharvardmanagermentorconnector}

1. Dans le tableau de bord intégré de l’administrateur, cliquez sur Harvard ManageMentor.

   Depuis la mosaïque, vous verrez trois options : Prise en main, Connexion et Gérer les connexions.

1. Si vous configurez le connecteur Harvard ManageMentor pour la première fois, cliquez sur Connexion.

   Vous devez également configurer le compte FTP Exavault avant de configurer ce connecteur.

   Assurez-vous que vous partagez ces informations d’identification FTP avec votre fournisseur de contenu pour accéder aux flux.

1. Saisissez un nom pour votre connexion dans le champ Nom de la connexion. Cliquez sur Connexion pour enregistrer cette connexion.
1. Si vous avez déjà établi une connexion, sur la page d’accueil, cliquez sur Harvard ManageMentor > Gérer les connexions. Cliquez sur la connexion à modifier pour modifier votre configuration existante.

   La fonction de migration doit être activée pour votre compte avant de configurer le connecteur.

   ![](assets/hmm.png)

1. Dans le volet de gauche, cliquez sur Configurer. Effectuez l’une des opérations suivantes :

   * Affichez ou modifiez les détails de votre compte et la planification de la synchronisation à partir de cette fenêtre. Vous devez cocher la case Activer la connexion si vous souhaitez activer ce compte.
   * Cliquez sur Activer la planification pour planifier la synchronisation. Vous pouvez saisir l’heure et la date de début, puis saisir la fréquence de la synchronisation en nombre de jours. Par exemple, vous pouvez décider d’effectuer la synchronisation tous les 3 jours.

1. Dans le volet de gauche, cliquez sur Exécution sur demande. Cette option vous permet d’importer les flux utilisateur et d’autres données pertinentes de Harvard ManageMentor. Entrez la date de début de l’exécution sur demande, et cliquez sur Exécuter pour exécuter la synchronisation. Toutes les données comprises entre la date de début et la date en cours sont importées pour cette connexion.

   * Vous pouvez cliquer sur Désactiver l’accès à Learning Manager lors de l’exécution lorsque l’application subit un temps d’arrêt au cours de la synchronisation.
   * Si vous cliquez sur Activer l’accès à Learning Manager lors de l’exécution, aucune interruption de service ne se produit lors de la synchronisation.

   Si vous voulez automatiser la synchronisation à intervalle régulier, indiquez le nombre de jours dans le champ Nombre de jours avant répétition. La synchronisation garantit que votre compte est mis à jour avec la dernière version des extraits et des résumés de Harvard ManageMentor.

1. Vous pouvez également cliquer sur État d’exécution dans le volet de gauche à tout moment pour afficher le résumé de toutes les exécutions pour ce connecteur, dans l’ordre chronologique. Vous pouvez afficher la date de début et la durée de la synchronisation, le type de synchronisation (s’il s’agit de synchronisation sur demande) et l’état de la synchronisation (si la synchronisation est en cours ou terminée).

   Lorsque vous supprimez et recréez une connexion, les exécutions précédentes du connecteur se produisent de nouveau. Vous pouvez afficher toutes les exécutions antérieures à la suppression de la connexion.

   Vous pouvez exécuter de nouveau la dernière synchronisation uniquement.

   Pour que la synchronisation soit effectuée correctement, vous devez vous assurer qu’au moins un des fichiers suivants est présent dans le dossier FTP Harvard ManageMentor :

   hmm12_metadata.xlsx : ce fichier contient les métadonnées de cours pour le connecteur Harvard ManageMentor. Assurez-vous que vous respectez la convention de dénomination lorsque vous chargez le fichier.

   client_hmm12_20150125.xlsx : il s’agit du flux utilisateur du connecteur Harvard ManageMentor. La convention de dénomination de fichier que vous devez respecter est **client_hmm12_aaaaMMjj.xlsx.**

   Voir les exemples suivants de fichiers de flux utilisateur et de flux de cours :
   [Fichier de métadonnées de cours pour le connecteur Harvard ManageMentor](assets/hmm12-metadata.xlsx) [Flux utilisateur pour le connecteur Harvard ManageMentor](assets/client-hmm12-20170304.xlsx)

## Connecteur Workday {#workdayconnector}

À l’aide du connecteur Workday, vous pouvez intégrer Learning Manager à un locataire Workday pour automatiser la synchronisation des données.

### Importation

#### Attributs de mappage

L’administrateur d’intégration peut choisir les colonnes Salesforce et les mapper à des attributs compatibles avec des groupes de Learning Manager. Il s’agit d’un effort unique. Une fois le mappage terminé, le même mappage est utilisé lors des prochaines importations de l’utilisateur. Il peut être reconfiguré si l’administrateur souhaite avoir un mappage différent pour importer des utilisateurs.

#### Importation automatisée d’utilisateurs

L’importation des utilisateurs permet à l’administrateur de Learning Manager de récupérer les détails des employés à partir de Salesforce et de les importer dans Learning Manager automatiquement.

#### Filtrage des utilisateurs

L’administrateur de Learning Manager peut appliquer un filtrage sur les utilisateurs avant de les importer. Par exemple, l’administrateur de Learning Manager peut choisir d’importer tous les utilisateurs sous un ou plusieurs responsables spécifiques dans la hiérarchie.

## Exportation

L’exportation des compétences d’utilisateur permet aux utilisateurs d’exporter automatiquement les compétences d’utilisateur vers Workday.

Les compétences de plusieurs comptes Learning Manager ne peuvent pas être exportées simultanément à l’aide du même compte Workday.

## Planification {#Scheduling-1}

L’administrateur peut définir des tâches de planification en fonction des besoins de l’organisation et les utilisateurs de l’application Learning Manager sont à jour selon la planification. De même, l’administrateur d’intégration peut planifier l’exportation des compétences en temps opportun à des fins d’intégration avec un système tiers. La synchronisation peut être exécutée de façon quotidienne dans l’application Learning Manager.

## Configuration du connecteur Workday {#configureworkdayconnector}

**Condition requise :** demandez à l’administrateur Workday de votre entreprise de créer un ISU (Integration System User, utilisateur système d’intégration) avec des autorisations comme défini dans le document ISU_Permissions. Téléchargez une copie à partir du lien ci-dessous.
[Téléchargez une copie de la sécurité de l&#39;utilisateur du système d&#39;intégration (ISU).](assets/isu-permissions-v1.pdf) Découvrez le processus d’intégration de Learning Manager au connecteur Workday.

1. Dans la page d’accueil de Learning Manager, placez le curseur de la souris sur la vignette Workday. Un menu s’affiche. Cliquez sur l’élément **[!UICONTROL Connecter]** dans le menu.

   ![](assets/workday-tile.png)

1. Une boîte de dialogue s’affiche et vous invite à saisir les informations d’identification correspondant à la nouvelle connexion. Voici les champs que vous devez renseigner avant d’établir la connexion.

   * Nom de la connexion : fournissez le nom de votre choix pour la connexion.
   * URL hôte : l’administrateur d’intégration peut obtenir les détails de l’URL hôte auprès de l’administrateur Workday correspondant.
   * Client : le client est interne à votre société. Votre administrateur Workday doit vous fournir les détails du locataire.
   * Nom d’utilisateur et mot de passe : l’administrateur Workday crée un utilisateur ISU (Integrated System User) avec les privilèges de sécurité requis et le partage avec l’administrateur d’intégration.

   Remarque : Learning Manager utilise la version 28.1 de l’API Workday.

   ![](assets/configure-connector.png)

1. Cliquez sur le bouton Connexion après avoir saisi les informations dans tous les champs pertinents.

   Vous pouvez également disposer de plusieurs connexions Workday synchronisées à votre compte Learning Manager.

Dans la page de présentation, vous pouvez spécifier le nom de connexion pour votre intégration. Sélectionnez les mesures à prendre parmi les options suivantes :

* Importer les utilisateurs internes
* Exporter les compétences des utilisateurs : configurer un calendrier
* Exporter les compétences des utilisateurs : sur demande

![](assets/overview.png)

## Importation

### Attributs de mappage {#MapAttributes-1}

Vous pouvez utiliser le connecteur Workday pour intégrer Learning Manager et Workday afin d’automatiser la synchronisation des données. Vous pouvez importer tous les utilisateurs actifs de Workday vers Learning Manager. Les utilisateurs peuvent être importés depuis diverses sources de données, notamment FTP et Salesforce.

Les attributs de l’utilisateur de Learning Manager et Workday doivent être mappés avant d’importer des utilisateurs. Dans la page de présentation, utilisez l’option Utilisateurs internes sous Importer pour fournir des attributs de mappage.

Entrez les informations d’identification d’Adobe Learning Manager dans la colonne Adobe Learning Manager. Utilisez les menus déroulants pour sélectionner les informations d’identification appropriées pour les colonnes sous Workday.

Actuellement, Learning Manager prend en charge l’importation de 44 attributs utilisateur à partir de Workday. Ajoutez des attributs supplémentaires à l’aide des champs actifs de Learning Manager.

![](assets/map-attributes.png)

Workday comporte quatre niveaux hiérarchiques, tandis que Learning Manager en comporte deux. Les quatre niveaux dans Workday sont la catégorie de profil de compétence, le profil de compétence, la catégorie d’élément de compétence et l’élément de compétence. Votre nom de compétence et le niveau de Learning Manager seront mappés dans Workday sous l’élément de compétence.

+++Liste des attributs Workday pris en charge

wd:User_ID\
wd:Worker_ID\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Nom_Formaté\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Nom_Formaté\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Formatted_Address\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Formatted_Phone\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number\
wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Gender_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID\
wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID\
wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$\
wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Formatted_Address\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Status_Data.wd:Active\
wd:Employment_Data.wd:Worker_Status_Data.wd:Active_Status_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retired\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Terminated\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$\
wd:Qualification_Data.wd:Education.0.wd:School_Name\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company\
wd:Management_Chain_Data.wd:Worker_Superonto_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID

+++

## Exportation

Vous pouvez exporter toutes les compétences terminées par un utilisateur de Learning Manager vers Workday. Notez que seules toutes les compétences actives sont exportées et Learning Manager n’exporte pas les compétences retirées. Vous pouvez également connecter plusieurs comptes Learning Manager au même connecteur Workday. Si les noms de compétence sont identiques dans deux comptes Learning Manager, ils sont mappés à la même compétence dans Workday. Il est conseillé de mettre à jour les noms de compétence dans tous les comptes Learning Manager avant de mettre à jour la compétence dans Workday au cas où deux comptes Learning Manager utiliseraient le même compte Workday.

+++Compétences de l’utilisateur - Configuration

Cette option vous permet de planifier l’extraction du rapport. Assurez-vous que la case Activer l’exportation des compétences d’utilisateur à l’aide de cette connexion est sélectionnée. Cochez la case Activer le calendrier et précisez la date et l’heure de début. Vous pouvez également spécifier l’intervalle auquel vous souhaitez que le rapport soit généré et envoyé. Sélectionnez la case Activer la planification et indiquez la date de début, la durée et la répétition après le numéro « n » de jours. Une fois terminé, cliquez sur Enregistrer.

![](assets/configure-schedule.png)

+++

+++Compétences des utilisateurs - À la demande

Vous pouvez spécifier la date de début et exporter le rapport à l’aide de l’option. Le rapport sera extrait à partir de la date saisie jusqu’à la date du jour. Saisissez la date à partir de laquelle vous souhaitez commencer à générer le rapport et cliquez sur Exécuter.

![](assets/on-demand-report.png)

+++

+++Compétences de l’utilisateur - Statut d’exécution

Ici, vous pouvez consulter le résumé de toutes les tâches et accéder à leur rapport d’état. vous pouvez télécharger des rapports d’erreurs en cliquant sur le lien de rapport d’erreurs.

![](assets/execution-status.png)

+++

## Connecteur miniOrange {#miniorangeconnector}

À l’aide du connecteur miniOrange, vous pouvez intégrer Learning Manager à un locataire miniOrange pour automatiser la synchronisation des données.

### Importation

#### Attributs de mappage

L’administrateur d’intégration peut choisir des attributs miniOrange et les mapper à des attributs compatibles avec des groupes de Learning Manager. Il s’agit d’un effort unique. Une fois le mappage terminé, le même mappage est utilisé lors des prochaines importations de l’utilisateur. Il peut être reconfiguré si l’administrateur souhaite avoir un mappage différent pour importer des utilisateurs.

#### Importation automatisée d’utilisateurs

L’importation des utilisateurs permet à l’administrateur de Learning Manager de récupérer les détails des employés à partir de miniOrange et de les importer dans Learning Manager automatiquement.

#### Filtrage des utilisateurs

L’administrateur de Learning Manager peut appliquer un filtrage sur les utilisateurs avant de les importer. Par exemple, l’administrateur de Learning Manager peut choisir d’importer tous les utilisateurs sous un ou plusieurs responsables spécifiques dans la hiérarchie.

Pour configurer   miniOrange   , veuillez contacter l’équipe CSM Learning Manager.

## Configurer le connecteur miniOrange {#configureminiorangeconnector}

1. Dans la page d’accueil de Learning Manager, placez le curseur de la souris sur la mini-vignette/carte orange. Un menu s’affiche. Cliquez sur l&#39;option **[!UICONTROL Connexion]** dans le menu.

   ![](assets/miniorange-tile.png)

1. Cliquez sur Connexion pour établir une nouvelle connexion. La page du connecteur miniOrange s’affiche. Saisissez les détails de votre compte que vous souhaitez mapper.

   ![](assets/establish-connection.png)

1. Si vous souhaitez importer un utilisateur miniOrnage directement en tant qu’utilisateur interne Learning Manager, utilisez l’option **[!UICONTROL Importer les utilisateurs internes]**.

   ![](assets/import-users.png)

1. Dans la page de mappage, à gauche   sur le côté, vous pouvez voir les colonnes de Learning Manager et à droite   côté, vous pouvez voir les colonnes miniOrange. Sélectionnez le nom de colonne approprié qui correspond au nom de colonne de Learning Manager.

   ![](assets/map-attributes.png)

1. Pour afficher et modifier la source de données, en tant qu’administrateur, cliquez sur **[!UICONTROL Paramètres > Source de données]**.

   La source miniOrange établie serait répertoriée. Si vous devez modifier le filtre, cliquez sur **[!UICONTROL Modifier]**.

   ![](assets/data-source.png)

1. Vous recevrez une notification une fois l’importation effectuée. Pour afficher ou modifier le journal des importations, cliquez sur **[!UICONTROL Utilisateurs > Journal des importations.]**

### Suppression d’une connexion {#deleteaconnection}

Procédez comme suit pour supprimer une connexion mini-Orange établie.

## Connecteur BlueJeans {#bluejeansconnector}

Vous pouvez désormais intégrer Learning Manager au connecteur BlueJeans et utiliser BlueJeans pour héberger des classes. BlueJeans vous permet de lancer des conférences téléphoniques audio et vidéo, des conversations vidéo et des webinaires.

Suivez les étapes ci-dessous pour configurer et utiliser le connecteur.

1. Dans la page d’accueil de Learning Manager , passez le curseur de la souris sur la vignette ou la carte BlueJeans. Un menu s’affiche. Cliquez sur l&#39;option **[!UICONTROL Se connecter]** dans le menu.

   ![](assets/miniorange.png)

1. La page du connecteur BlueJeans s’ouvre. Saisissez les détails de votre compte dans les champs respectifs pour intégrer Learning Manager et BlueJeans afin de synchroniser le flux utilisateur. Vous pouvez obtenir ces détails auprès de l’administrateur de votre compte BlueJeans.

   ![](assets/bluejeans-connecotrpage.png)

   En tant qu’élève, lors de l’activation du connecteur, utilisez le même ID de messagerie que celui utilisé pour votre compte Learning Manager afin de permettre aux flux utilisateurs d’être redirigés vers Learning Manager.

1. Une fois la connexion établie, en tant qu’auteur, créez un cours de classe virtuelle avec BlueJeans comme système de conférence.

   ![](assets/conferencing-systems.png)

1. Les administrateurs, les responsables et les élèves peuvent inscrire des élèves au cours créé. Lors de l’inscription, l’élève reçoit un courrier électronique. L’élève peut se connecter à son compte Learning Manager pour voir les détails du programme et suivre le cours.
1. Une fois le cours terminé, le rapport d’achèvement est envoyé à Learning Manager. L’administrateur peut consulter le rapport d’achèvement afin de vérifier l’assiduité et le score des élèves.

   ![](assets/-attendence-and-scoringreport.png)

## Connecteur Box {#boxconnector}

À l’aide du connecteur BOX, vous pouvez intégrer Learning Manager à des systèmes externes de votre choix pour automatiser la synchronisation des données. Les systèmes externes doivent pouvoir exporter des données au format CSV et les placer dans le dossier approprié du compte Box de Learning Manager. Les fonctionnalités du connecteur Box sont les suivantes :

Vous pouvez également utiliser le connecteur FTP pour la migration de données, l’importation d’utilisateurs et l’exportation de données. Pour plus d’informations, consultez [Connecteur FTP Learning Manager.](third-party-connectors.md#main-pars_header_1427405935)

## Importation de données {#DataImport-1}

L’importation des utilisateurs permet à l’administrateur de Learning Manager de récupérer les détails des employés à partir de Salesforce et de les importer dans Learning Manager automatiquement. Grâce à cette fonction, vous pouvez intégrer plusieurs systèmes en plaçant le fichier CSV généré par ces systèmes dans les dossiers appropriés des comptes Box. Learning Manager choisit les fichiers CSV, les fusionne et importe les données en fonction de la planification. Reportez-vous à la fonctionnalité de planification pour plus d’informations.

**Attributs de mappage**

L’administrateur d’intégration peut sélectionner les colonnes du fichier CSV et les mapper aux attributs compatibles avec les groupes de Learning Manager. Ce mappage est un effort unique. Une fois le mappage terminé, le même mappage est utilisé lors des importations suivantes des utilisateurs. Le mappage peut être reconfiguré si l’administrateur souhaite un mappage différent pour l’importation des utilisateurs.

## Exportation de données {#dataexport}

Vous pouvez désormais exporter des compétences d’utilisateur vers un emplacement Box à des fins d’intégration avec un système tiers.

## Planification de rapports {#schedulereports}

L’administrateur peut définir des tâches de planification en fonction des besoins de l’organisation et les utilisateurs de l’application Learning Manager sont à jour selon la planification. De même, l’administrateur d’intégration peut planifier l’exportation des compétences en temps opportun à des fins d’intégration avec un système tiers. La synchronisation peut être exécutée de façon quotidienne dans l’application Learning Manager.

## Configuration du connecteur Box {#configureboxconnector}

Découvrez le processus d’intégration de Learning Manager au connecteur Box.

1. Dans la page d’accueil de Learning Manager, placez le curseur de la souris sur la vignette/carte Box. Un menu s’affiche. Cliquez sur l’élément Connecter dans le menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

1. Une boîte de dialogue s’affiche vous invitant à entrer l’ID de messagerie. Indiquez l’ID de messagerie de la personne responsable de la gestion du compte Box de Learning Manager pour l’organisation. Cliquez sur Connecter après avoir renseigné l’ID de messagerie.

1. Learning Manager vous envoie un courrier électronique invitant l’utilisateur à réinitialiser le mot de passe avant d’accéder au Box pour la première fois. L’utilisateur doit réinitialiser le mot de passe et l’utiliser pour accéder au compte Box de Learning Manager.

   Un seul compte Box Learning Manager peut être créé pour un compte Learning Manager donné.

   Dans la page de présentation, vous pouvez spécifier le nom de connexion pour votre intégration. Sélectionnez les mesures à prendre parmi les options suivantes :

   * Importer les utilisateurs internes
   * Exporter les compétences des utilisateurs : configurer un calendrier
   * Exporter les compétences des utilisateurs : sur demande

## Importation

+++Utilisateur interne

L’option d’importation d’utilisateur interne vous permet de planifier la génération du rapport d’importation d’utilisateur automatiquement. Les rapports générés vous sont envoyés au format CSV.

+++

+++Attributs Map

Une fois la connexion établie, vous pouvez mapper les colonnes des fichiers CSV qui seront placés dans le dossier Box aux attributs correspondants de Learning Manager. Cette étape est obligatoire.

1. Dans la page Attributs de mappage, à gauche   sur le côté, vous pouvez voir les colonnes attendues de Learning Manager et à droite   Vous pouvez voir les noms des colonnes CSV. À droite, vous pouvez initialement voir une zone de sélection vide. Importez n’importe quel modèle CSV en cliquant sur Sélectionner un fichier.

1. Les étapes ci-dessus permettent de compléter la liste déroulante de sélection de droite avec tous les noms de colonnes du fichier CSV. Sélectionnez le nom de colonne approprié qui correspond au nom de colonne de Learning Manager.

   *Le champ du gestionnaire doit obligatoirement être mappé à un champ d’adresse électronique. Le mappage de toutes les colonnes est obligatoire pour que le connecteur puisse être utilisé.*

1. Cliquez sur Enregistrer après avoir terminé le mappage.

   Le connecteur est maintenant prêt à l’emploi. Le compte que vous venez de configurer s’affiche désormais en tant que source de données dans l’application d’administrateur pour que l’administrateur programme l’importation ou pour une synchronisation à la demande.

+++

+++Utilisation du connecteur Box de Learning Manager

1. Les fichiers CSV de systèmes externes doivent être placés à l’emplacement suivant :

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Remarque :** dans la version de juillet 2016, seule l&#39;importation d&#39;utilisateurs est autorisée. Par conséquent, pour utiliser le connecteur Box, vous devez vous assurer que les fichiers CSV sont placés dans le dossier suivant :\
   `code Home/import/user/internal/*.csv`

1. Le connecteur Box prend toutes les lignes des fichiers CSV. Il est donc important que la ligne correspondant à un utilisateur dans un fichier CSV n’apparaisse dans aucun autre fichier CSV.
1. Tous les fichiers CSV doivent contenir les colonnes spécifiées dans le mappage.
1. Tous les fichiers CSV requis doivent être présents dans le dossier avant le début du processus.

Lors de l’importation des utilisateurs dans Learning Manager, l’administrateur doit également déterminer la gestion des utilisateurs dans Learning Manager. Reportez-vous à l&#39;[Aide sur la gestion des utilisateurs](../integration-admin/feature-summary/migration-manual.md#usermanagement) pour en savoir plus.

+++

## Exportation

+++Compétences

Il existe deux options pour exporter les rapports de compétences des utilisateurs.

Compétences des utilisateurs - À la demande : vous pouvez spécifier la date de début et exporter le rapport à l’aide de l’option. Le rapport sera extrait à partir de la date entrée jusqu’à présent

**[!UICONTROL Compétences des utilisateurs : Configurer]** : cette option vous permet de planifier l’extraction du rapport. Cochez la case Activer le calendrier et précisez la date et l’heure de début. Vous pouvez également spécifier l’intervalle auquel vous souhaitez que le rapport soit généré et envoyé.

+++

Pour ouvrir le dossier d’exportation dans lequel les fichiers exportés seront placés dans votre emplacement Box, ouvrez le lien vers le dossier Box fourni dans la page Compétences de l’utilisateur, comme indiqué ci-dessous.

Les fichiers exportés automatiquement seront présents à l&#39;emplacement **Accueil/Exportation/&#42;Emplacement_Box&#42;**

Les fichiers exportés automatiquement seront disponibles avec le titre **skill_results_&#42;date du &#42;_au_&#42;date du&#42;.csv**

Les autorisations d’accès et le contenu du dossier Box partagé par l’équipe Learning Manager doivent être gérés par le client.  Notez également que le contenu du dossier sera physiquement stocké dans la région de Francfort.

## Connecteur LinkedInLearning {#linkedinlearningconnector}

Le connecteur LinkedInLearning peut être utilisé par les clients professionnels de LinkedIn.com qui souhaitent que leurs élèves découvrent et suivent les cours de LinkedIn dans Learning Manager. Il est possible de configurer le connecteur pour récupérer les cours avec votre clé API. Une fois qu’un cours est créé dans Learning Manager, les utilisateurs peuvent le rechercher et le suivre. La progression des élèves peut alors être suivie dans Learning Manager.

### Configuration du connecteur LinkedIn {#configurelinkedinconnector}

1. Dans le tableau de bord intégré de l’administrateur, cliquez sur LinkedInLearning.

   Vous verrez la mosaïque contenant trois options : Prise en main, Connexion et Gérer les connexions.

1. Si vous configurez le connecteur LinkedInLearning pour la première fois, cliquez sur Se connecter.

   Vous devez configurer le compte FTP Exavault avant de configurer ce connecteur.

1. À partir de la page de connexion, indiquez un nom pour votre connecteur. Saisissez l’Appkey et la clé secrète de votre connexion.

   Vous devez contacter votre fournisseur pour obtenir la clé d’application et la clé secrète .

1. Cliquez sur Enregistrer.

   La configuration est enregistrée et la connexion LinkedInLearning pour votre compte est ajoutée. Vous pouvez désormais cliquer sur Gérer les connexions à partir de la page d’accueil et modifier votre configuration à tout moment.

1. Si vous avez déjà créé une connexion, cliquez sur Gérer les connexions pour afficher l’ensemble de vos connexions.

   La fonction de migration doit être activée pour votre compte avant de configurer le connecteur.

1. Cliquez sur la connexion à modifier.
1. Dans le volet de gauche, cliquez sur Configurer. Effectuez l’une des opérations suivantes :

   * Affichez ou modifiez les détails de votre compte et la planification de la synchronisation à partir de cette fenêtre. Vous devez cocher la case Activer la connexion si vous souhaitez activer ce compte.
   * Cliquez sur Modifier pour modifier vos informations d’identification. Cliquez sur Réinitialiser pour annuler les modifications apportées à ce champ.
   * Cliquez sur Activer la planification pour planifier la synchronisation. Vous pouvez saisir l’heure et la date de début, puis saisir la fréquence de la synchronisation en nombre de jours. Par exemple, vous pouvez décider d’effectuer la synchronisation tous les 3 jours.

   Cliquez sur Enregistrer pour enregistrer vos modifications.

1. Dans le volet de gauche, cliquez sur Exécution sur demande. Cette option vous permet d’importer les flux utilisateur et d’autres données pertinentes de LinkedIn. Saisissez la date de début de l&#39;exécution à la demande, puis cliquez sur Exécuter pour exécuter la synchronisation. Toutes les données comprises entre la date de début et la date en cours sont importées.

   * Vous pouvez cliquer sur Désactiver l’accès à Learning Manager lors de l’exécution lorsque l’application subit un temps d’arrêt au cours de la synchronisation.
   * Si vous cliquez sur Activer l’accès à Learning Manager lors de l’exécution, aucune interruption de service ne se produit lors de la synchronisation.

1. Vous pouvez également cliquer sur État d’exécution dans le volet de gauche à tout moment pour afficher le résumé de toutes les exécutions pour ce connecteur, dans l’ordre chronologique. Vous pouvez afficher la date de début et la durée de la synchronisation, le type de synchronisation (s’il s’agit de synchronisation sur demande) et l’état de la synchronisation (si la synchronisation est en cours ou terminée).

   Lorsque vous supprimez et recréez une connexion, les exécutions précédentes du connecteur se produisent de nouveau. Vous pouvez afficher toutes les exécutions antérieures à la suppression de la connexion.

   Vous pouvez exécuter de nouveau la dernière synchronisation uniquement.

