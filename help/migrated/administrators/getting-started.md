---
description: Ce document fournit une approche recommandée pour installer et configurer Adobe Learning Manager. L’équipe Learning Manager recommande d’adopter une approche par étapes pour prendre en main l’application. Vous n’êtes pas obligé de suivre toutes les étapes dans un ordre spécifique.
jcr-language: en_us
title: Guide des meilleures pratiques pour configurer Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 71%

---



# Guide des meilleures pratiques pour configurer Learning Manager

Ce document fournit une approche recommandée pour installer et configurer Adobe Learning Manager. L’équipe Learning Manager recommande d’adopter une approche par étapes pour prendre en main l’application. Vous n’êtes pas obligé de suivre toutes les étapes dans un ordre spécifique.

Ces phases peuvent être effectuées par trois rôles différents, par une ou plusieurs personnes en fonction de la configuration de votre organisation. Les trois rôles sont les suivants :

1. **Administrateur informatique** - L’administrateur informatique effectue les activités d’activation ou d’intégration associées à l’application Learning Manager dans une organisation. L’administrateur informatique peut également ajouter un ou plusieurs utilisateurs et occuper le rôle d’administrateur d’intégration.
1. **Auteur** - L’auteur crée le contenu d’apprentissage requis pour les besoins d’apprentissage de l’organisation. L’auteur du contenu de formation ou d’apprentissage de votre organisation peut commencer à créer le contenu de base requis pour l’application Learning Manager.
1. **Administrateur Learning Manager** - L’administrateur de l’application Learning Manager effectue les activités de configuration et d’installation. Dans certaines entreprises, l’administrateur informatique peut également jouer le rôle d’administrateur de l’application Learning Manager.

Vous pouvez parcourir l&#39;infographie ci-dessous pour obtenir un aperçu des phases et des tâches correspondantes.

![](assets/learning-manager-getting-started.jpg)

À ce stade, on part du principe que votre entreprise a déjà reçu la clé de licence et que vous avez activé le compte Learning Manager. Comme cela est illustré dans l’infographie, les trois pistes fonctionnent comme suit :

## Étape 1 : configuration technique (administrateur informatique) {#phase1technicalsetupitadministrator}

Dans le Pôle 1, l’administrateur informatique de votre organisation peut passer au rôle d’administrateur d’intégration dans l’application Learning Manager et effectuer certaines activations et intégrations comme suit :

### Activer/Ajouter des champs actifs (Administrateur Learning Manager) {#enableaddactivefieldscaptivateprimeadministrator}

Outre les champs actifs fournis par les utilisateurs lors de l’inscription, l’administrateur peut ajouter davantage de champs actifs. L’administrateur peut également activer ou désactiver les champs d’utilisateur. Les valeurs de ces champs actifs sont générées à partir des métadonnées de diverses sources de données associées aux comptes d’utilisateurs. Reportez-vous à [Aide sur les champs actifs](feature-summary/add-users-user-groups.md#active-fields) pour plus d’informations.

### Authentification unique (SSO) {#singlesignonsso}

Vous pouvez accéder à l’application Learning Manager en utilisant un ID Adobe ou l’authentification unique. L’authentification unique est un mécanisme permettant à un utilisateur de s’authentifier une fois et d’accéder à plusieurs applications de nombreuses fois. Cette configuration n’est pas obligatoire pour l’entreprise. Si votre entreprise possède un fournisseur d’authentification unique basée sur SAML 2.0, vous pouvez l’utiliser pour configurer l’application Learning Manager. La configuration doit être effectuée au niveau de l’entreprise et de l’application Learning Manager. Si vous choisissez d’utiliser l’authentification unique, contactez l’assistance d’Adobe pour obtenir les instructions de configuration. Reportez-vous à [Aide sur les paramètres](feature-summary/settings.md) pour plus d’informations.

### Importation en bloc d’utilisateurs {#bulkimportofusers}

Si votre entreprise compte un nombre élevé d’utilisateurs, vous pouvez tous les importer en bloc dans l’application Learning Manager à l’aide d’un fichier CSV. Avant d’effectuer cette tâche, nous vous suggérons d’exporter la liste des utilisateurs de l’application de RH de votre organisation au format .CSV. Même si vous n’effectuez pas d’importation en bloc des utilisateurs à ce stade, vous pouvez vous familiariser avec le format CSV. Pour commencer le processus d’importation dans Learning Manager, vous devez télécharger le fichier .CSV et mapper les champs de données de l’application avec les colonnes CSV de votre organisation. Reportez-vous à [Aide sur l’importation en bloc](add-users-in-bulk.md) pour plus d’informations.

### Intégration avec le connecteur FTP {#ftpconnectorintegration}

Si vous avez continuellement besoin d’ajouter et de supprimer des employés au sein de votre entreprise, vous pouvez automatiser l’importation en bloc d’utilisateurs à l’aide du connecteur FTP. Après avoir établi une connexion, vous pouvez charger un fichier CSV et mapper les attributs de celui-ci avec les champs correspondants de Learning Manager. Vous pouvez planifier le processus d’importation automatique, mais aussi effectuer une synchronisation ponctuelle en fonction des besoins. Reportez-vous à [Aide du connecteur FTP](../integration-admin/feature-summary/connectors.md#ftpconnector) pour plus d’informations.

### Intégration avec le connecteur Salesforce {#salesforceconnectorintegration}

Si vous disposez d’un compte Salesforce dans votre entreprise, vous pouvez automatiser le processus d’importation de tous les utilisateurs Salesforce dans l’application Learning Manager. Si vous souhaitez utiliser cette fonctionnalité, vous pouvez utiliser le connecteur Salesforce pour intégrer Learning Manager avec le compte Salesforce et automatiser la synchronisation des données. Utilisez la fonctionnalité de planification automatique pour effectuer régulièrement une importation automatisée des utilisateurs. Vous pouvez également effectuer une synchronisation quotidiennement. Reportez-vous à [l’aide relative au connecteur Salesforce](../integration-admin/feature-summary/connectors.md#sfconnector) pour plus d’informations.

### Intégration avec Adobe Connect {#adobeconnectintegration}

Si vous utilisez Adobe Connect dans votre entreprise, vous pouvez l’intégrer à l’application Adobe Learning Manager afin d’offrir une expérience utilisateur conviviale aux élèves. Cette intégration permet aux élèves d’accéder à des classes virtuelles directement dans l’application Learning Manager en un seul clic, sans avoir à se reconnecter à Adobe Connect. Grâce à cette fonctionnalité, les élèves peuvent également utiliser des sessions de classe virtuelle enregistrées dans l’application Learning Manager. Pour effectuer l’intégration, commencez par intégrer les paramètres. Accédez à **Paramètres > Adobe Connect > Configurer maintenant** pour définir l’URL et les informations de connexion d’Adobe Connect et effectuer l’intégration de celui-ci. Reportez-vous à [l’aide relative à l’intégration avec Adobe Connect](feature-summary/adobeconnect-integration.md) pour plus d’informations.

### Enregistrement de l’application Salesforce {#salesforceappregistration}

Pour une expérience utilisateur conviviale, les élèves peuvent accéder à l’application Learning Manager directement dans leurs comptes Salesforce. Les élèves peuvent accéder au contenu d’apprentissage qui leur a été affecté (cours, programmes d’apprentissage, assistances à la tâche, etc.) depuis l’application Salesforce. Les utilisateurs peuvent également accéder aux notifications et annonces de l’application Learning Manager dans Salesforce. Pour utiliser cette fonctionnalité, vous devez enregistrer l’application Salesforce dans l’application Learning Manager. Reportez-vous à [l’aide relative à l’application Salesforce](../integration-admin/feature-summary/sfdc-app.md) pour les instructions d’installation et d’utilisation.

## Étape 2 : configuration du site (administrateur Learning Manager) {#phase2siteconfigurationcaptivateprimeadministrator}

L’administrateur de l’application Learning Manager au sein de votre entreprise doit installer ou configurer certaines fonctionnalités pour que vous puissiez commencer à les mettre en œuvre pour vos élèves.

### Identité visuelle {#branding}

Une organisation peut souhaiter afficher le logo de l’entreprise dans l’application Learning Manager, avoir son propre domaine dans l’URL, afficher le nom de l’organisation et afficher des palettes de couleurs correspondant à la marque d’une organisation. Learning Manager offre toutes ces options aux organisations. Si vous souhaitez personnaliser les paramètres et utiliser votre propre identité visuelle, cliquez sur la section Identité visuelle de la marque dans le volet de gauche. Cliquez sur Modifier en regard de toutes ces options et personnalisez celles-ci en fonction de vos besoins. Reportez-vous à [Aide sur le branding et les thèmes](feature-summary/themes.md) pour plus d’informations.

### Ajout d’utilisateurs/de groupes d’utilisateurs {#addusersusergroups}

Les élèves étant les principaux utilisateurs de votre contenu d’apprentissage, ajouter des utilisateurs au système de gestion de l’apprentissage (LMS) constitue la première étape. Ajoutez des utilisateurs à l’application Learning Manager, puis affectez-leur des rôles. Vous pouvez ajouter des utilisateurs de l’une des manières suivantes :

#### Ajout d’utilisateurs (internes) {#addusersinternal}

* **En tant qu’utilisateur unique** : ajouter des utilisateurs uniques dans l’application Learning Manager vous permet de faire des essais avec quelques-uns d’entre eux avant de les ajouter en bloc. En outre, cette option est utile lorsque vous souhaitez ajouter d’autres utilisateurs uniques en fonction des besoins, après l’importation en bloc d’utilisateurs.
* **Auto-inscription** - Cette option permet aux administrateurs d’autoriser leurs employés à s’inscrire à Learning Manager.
* **Importation en bloc** (avec le chargement CSV) : cette option vous permet d’importer des utilisateurs par lot dans l’application Learning Manager. Comme condition préalable, vous devez tenir la liste des utilisateurs prête au format CSV avant d’utiliser cette fonctionnalité.

#### Ajout d’utilisateurs (profils externes) {#addusersexternalprofiles}

* Par inscription externe : cette option vous permet d’inscrire à l’application des membres de services externes ou des employés externes à votre entreprise.

#### Ajout de groupes d’utilisateurs {#addusergroups}

L’application Learning Manager génère des groupes d’utilisateurs par défaut basés sur des attributs similaires. Outre les groupes par défaut, vous pouvez générer des groupes d’utilisateurs personnalisés basés sur des paramètres tels que la désignation et l’emplacement. Ces groupes peuvent ensuite être utilisés dans la fonctionnalité de ludification, les rapports, etc. Reportez-vous à [l’aide relative à l’ajout d’utilisateurs](feature-summary/add-users-user-groups.md) pour plus d’informations.

### Affecter des rôles {#assignroles}

Lorsque les utilisateurs sont ajoutés à Learning Manager, l’administrateur peut commencer à affecter les rôles d’auteur, d’administrateur ou d’administrateur d’intégration à des utilisateurs selon les besoins de votre entreprise. Pour attribuer des rôles aux utilisateurs, dans la connexion Administrateur, vous pouvez cliquer sur **[!UICONTROL Utilisateurs]**  dans le volet de gauche, cochez la case en regard de chaque nom d’utilisateur, puis cliquez sur **[!UICONTROL Actions]** liste déroulante pour choisir le rôle que vous souhaitez attribuer. Les rôles de responsable sont attribués aux utilisateurs par Adobe Learning Manager en fonction des rôles/privilèges mentionnés par votre organisation dans le fichier CSV. Vous pouvez également modifier les rôles des utilisateurs en tant que responsables à l’aide du workflow Modifier les utilisateurs. Reportez-vous à [l’aide relative à l’ajout d’utilisateurs](feature-summary/add-users-user-groups.md) pour plus d’informations.

### Modèles de notification {#notificationtemplates}

Les notifications peuvent être utiles aux utilisateurs d’un LMS pour connaître l’état de leur compte ou pour être informés des événements/activités en cours. Lorsque les utilisateurs créent un cours, configurent des fonctionnalités ou suivent un cours, divers événements se produisent et déclenchent l’envoi de notifications aux élèves, à leurs responsables, aux administrateurs ou aux auteurs. Learning Manager fournit divers modèles de notification par courrier électronique dans l’application. En tant qu’administrateur, vous pouvez les personnaliser en fonction des besoins de votre entreprise. Pour créer des notifications par courrier électronique, choisissez **Modèles de courriers électroniques** dans le volet de gauche, puis cliquez sur le nom du modèle. Reportez-vous à [l’aide relative aux modèles de courriers électroniques](feature-summary/email-templates.md) pour plus d’informations.

**Désactivation des notifications par courrier électronique (recommandé)**

Par défaut, les notifications sont activées dans l’application Learning Manager. Vous pouvez désactiver les notifications à ce stade si vous ne voulez pas en envoyer aux employés de l’entreprise pour l’instant.

### Badges {#badges}

Les badges sont une mesure de l’accomplissement que vos collaborateurs peuvent obtenir à l’issue d’un cours. Les professionnels à travers le monde utilisent ces badges en tant que représentation de l’acquisition d’une compétence particulière ou de l’achèvement d’un apprentissage. Vous pouvez créer un ensemble de badges que vous pourrez ensuite affecter aux élèves lorsqu’ils terminent un contenu d’apprentissage. Pour commencer à créer des badges, cliquez sur la fonctionnalité **[!UICONTROL Badges]** dans le volet de gauche. Reportez-vous à  [Aide sur les badges](feature-summary/badges.md) pour plus d’informations.

### Retour d’informations {#feedback}

Les retours d’informations constituent l’un des aspects les plus importants d’un LMS pour mesurer la progression des élèves et s’assurer de la bonne qualité du contenu d’apprentissage. Learning Manager propose deux types de retour d’informations aux utilisateurs.

* Les retours d’informations L1 sont fournis par les élèves à l’issue d’un cours.
* Le retour d&#39;informations L3 correspond au retour d&#39;informations donné par les responsables aux élèves en fonction de l&#39;impact du cours sur le comportement des élèves et sur leurs activités quotidiennes.

L’utilisation de cette fonctionnalité est facultative. Les administrateurs peuvent personnaliser les modèles de retour d’informations en fonction des besoins de l’entreprise. Pour utiliser cette fonctionnalité, l’administrateur doit activer les retours d’informations L1 et L3 au niveau d’une instance de cours. Pour configurer les retours d’informations, sélectionnez un cours, cliquez sur Paramètres par défaut de l’instance dans le volet de gauche et activez l’option de retour d’informations. Reportez-vous à [l’aide relative aux retours d’informations](feature-summary/courses.md) pour plus d’informations.

### Ludification {#gamification}

Maintenir les élèves motivés pendant qu’ils utilisent le contenu d’apprentissage est l’un des principaux défis rencontrés par les entreprises. La ludification augmente le taux d’achèvement des cours en incitant les élèves à atteindre leurs objectifs grâce à des techniques de jeu. Les élèves peuvent rivaliser avec leurs collègues pour marquer des points pour diverses activités d’apprentissage et atteindre les niveaux bronze, argent, or et platine. Les administrateurs peuvent activer/désactiver chaque tâche et modifier l’attribution des points aux tâches. Learning Manager propose la fonctionnalité de ludification avec des paramètres par défaut. Vous pouvez commencer par utiliser cette fonctionnalité avec les paramètres par défaut pendant un certain temps, puis choisir de la personnaliser. Configurer/modifier les paramètres de cette fonctionnalité est facultatif. Si vous avez un spécialiste dans votre entreprise, nous vous recommandons de configurer les paramètres avant de l’utiliser. Reportez-vous à [l&#39;aide relative à la ludification](feature-summary/gamification.md) pour plus d’informations.

### Création d’objets d’apprentissage {#createlearningobjects}

Il s’agit de l’étape logique où les trois pistes (les pistes 1, 2 et 3) se rejoignent et où vous prenez le relais pour gérer la suite.

À ce stade, après avoir créé des modules et des cours, vous pouvez commencer à créer des objets d’apprentissage de niveau supérieur tels que des certifications, des programmes d’apprentissage ou des assistances à la tâche. Avant de créer des objets d’apprentissage, vérifiez que vous avez déjà ajouté des utilisateurs dans l’application Learning Manager et créé des modules et des cours.

#### Création de certifications {#createcertifications}

Une certification est un justificatif d’achèvement d’un contenu d’apprentissage ou une preuve d’accomplissement destinée aux élèves, sur une base ponctuelle ou selon un calendrier récurrent. Il est possible d’accroître la propension des élèves à s’inscrire à des contenus d’apprentissage en leur fournissant une certification à l’issue d’un cours. En tant qu’administrateur, vous pouvez créer un programme de certification hébergé en interne ou piloté par un tiers. En cas de certification interne, définissez les cours qu’un participant doit terminer pour obtenir la certification. Avant de créer la certification, vérifiez que vous avez des cours disponibles dans le compte. Reportez-vous à  [Aide sur la certification](feature-summary/certifications.md) pour plus d&#39;informations sur la création de certifications.

#### Création d’assistances à la tâche {#createjobaids}

Les assistances à la tâche sont un référentiel de contenu de formation accessible aux élèves sans aucun critère d&#39;inscription ou d&#39;achèvement. Les élèves peuvent se reporter à ces assistances à la tâche dans le cadre de leur travail afin d’obtenir de l’aide pour effectuer une activité ou une tâche quelconque au sein de l’entreprise. Même s’il n’est pas obligatoire d’utiliser les assistances à la tâche dans le cadre de la création d’un cours, l’équipe Learning Manager estime qu’en créer constitue une bonne pratique et vous recommande de le faire. Reportez-vous à  [Aide sur les assistances à la tâche](../authors/feature-summary/job-aids.md) pour plus d&#39;informations sur la création d&#39;assistances à la tâche.

#### Création de programmes d’apprentissage {#createlearningprograms}

Les programmes d’apprentissage sont des ensembles de cours uniquement destinés à réaliser les objectifs spécifiques des élèves. Avant de créer des programmes d&#39;apprentissage, assurez-vous d&#39;avoir déjà créé certains cours ou de disposer de cours existants dans votre compte.  Même s’il est facultatif pour une organisation d’utiliser cette fonctionnalité, l’équipe de Learning Manager vous recommande de l’utiliser pour inculquer une formation ciblée à vos employés. Pour commencer à utiliser les programmes d’apprentissage, cliquez sur Programmes d’apprentissage dans le volet de gauche, sélectionnez un ensemble de cours dans le catalogue et lancez la publication. Reportez-vous à [Aide des programmes d’apprentissage](feature-summary/learning-programs.md) pour obtenir des instructions spécifiques.

### Création de catalogues {#createcatalogs}

Vous pouvez utiliser les catalogues pour créer du contenu ciblé ou pour classer du contenu comme destiné à un ensemble spécifique d’élèves. Dans Learning Manager, un catalogue est un ensemble d’objets d’apprentissage tels que des cours, des certifications et des programmes d’apprentissage. Vous pouvez sélectionner les objets d’apprentissage de votre choix lors de la création de catalogues. Vérifiez que vous avez déjà créé un ensemble de cours, de certifications ou de programmes d’apprentissage avant de créer des catalogues. Vous pouvez créer des catalogues personnalisés avec un jeu d’objets d’apprentissage si vous souhaitez les affecter à des groupes d’utilisateurs internes ou externes. Reportez-vous à  [Aide des catalogues](feature-summary/catalogs.md) pour plus d’informations sur les catalogues.

### Activation des notifications par courrier électronique et de l’accès utilisateur {#turnonemailnotificationsuseraccess}

À ce stade, vous pouvez activer les notifications par e-mail pour les utilisateurs de vos applications et également activer l’accès utilisateur.

## Étape 3 : création de cours (Auteur) {#phase3authoringcoursesauthor}

Les développeurs ou auteurs de contenu de votre organisation peuvent commencer à créer le contenu d’apprentissage. Il est obligatoire de créer des modules et des cours car ils forment la base de tout votre contenu d’apprentissage dans l’application Learning Manager.

### Création de modules {#createmodules}

Les modules sont les éléments de base de l’application Learning Manager. Pour organiser votre contenu d’apprentissage, commencez à créer des modules en tant qu’auteur. Learning Manager vous permet de choisir parmi l’un des quatre types de module de cours (classe, auto-apprentissage, activité et classe virtuelle). Reportez-vous à  [Aide sur les modules](../authors/how-to-choose-modules.md) pour savoir quel type de module de cours est le mieux adapté aux besoins de votre organisation.

### Création de cours {#createcourses}

Les administrateurs peuvent jouer le rôle d’auteur dans l’application Learning Manager et créer des cours. Dans l’application Learning Manager, le cours constitue l’unité de base, avec un jeu de modules qui peuvent être affectés à un élève. Les élèves utilisent les cours. Vous pouvez créer un cours en choisissant les modules que vous avez créés précédemment, associer les compétences que vous voulez que les élèves acquièrent dans le cadre du cours, associer des niveaux, des crédits et des badges au cours, sélectionner les assistances à la tâche, les prérequis et les ressources de votre choix, et enfin publier le cours. Vous pouvez également créer plusieurs instances d’un cours afin de pouvoir les affecter à des élèves situés dans différents fuseaux horaires, définir une planification, etc. Reportez-vous à  [Aide des cours](../authors/feature-summary/courses.md)pour plus d&#39;informations sur la création d&#39;un cours.

### Création d’objets d’apprentissage {#Createlearningobjects-1}

Il s’agit de l’étape logique où les trois pistes (les pistes 1, 2 et 3) se rejoignent et où vous prenez le relais pour gérer la suite.

À ce stade, après avoir créé des modules et des cours, vous pouvez commencer à créer des objets d’apprentissage de niveau supérieur tels que des certifications, des programmes d’apprentissage ou des assistances à la tâche. Avant de créer des objets d’apprentissage, vérifiez que vous avez déjà ajouté des utilisateurs dans l’application Learning Manager et créé des modules et des cours.

#### Création de certifications {#Createcertifications-1}

Une certification est un justificatif d’achèvement d’un contenu d’apprentissage ou une preuve d’accomplissement destinée aux élèves, sur une base ponctuelle ou selon un calendrier récurrent. Il est possible d’accroître la propension des élèves à s’inscrire à des contenus d’apprentissage en leur fournissant une certification à l’issue d’un cours. En tant qu’administrateur, vous pouvez créer un programme de certification hébergé en interne ou piloté par un tiers. En cas de certification interne, définissez les cours qu’un participant doit terminer pour obtenir la certification. Avant de créer la certification, vérifiez que vous avez des cours disponibles dans le compte. Reportez-vous à  [Aide sur la certification](feature-summary/certifications.md) pour plus d&#39;informations sur la création de certifications.

#### Création d’assistances à la tâche {#CreateJobaids-1}

Les assistances à la tâche sont un référentiel de contenu de formation accessible aux élèves sans aucun critère d&#39;inscription ou d&#39;achèvement. Les élèves peuvent se reporter à ces assistances à la tâche dans le cadre de leur travail afin d’obtenir de l’aide pour effectuer une activité ou une tâche quelconque au sein de l’entreprise. Même s’il n’est pas obligatoire d’utiliser les assistances à la tâche dans le cadre de la création d’un cours, l’équipe Learning Manager estime qu’en créer constitue une bonne pratique et vous recommande de le faire. Reportez-vous à  [Aide sur les assistances à la tâche](../authors/feature-summary/job-aids.md) pour plus d&#39;informations sur la création d&#39;assistances à la tâche.

#### Création de programmes d’apprentissage {#Createlearningprograms-1}

Les programmes d’apprentissage sont des ensembles de cours uniquement destinés à réaliser les objectifs spécifiques des élèves. Avant de créer des programmes d&#39;apprentissage, assurez-vous d&#39;avoir déjà créé certains cours ou de disposer de cours existants dans votre compte.  Même s’il est facultatif pour une organisation d’utiliser cette fonctionnalité, l’équipe de Learning Manager vous recommande de l’utiliser pour inculquer une formation ciblée à vos employés. Pour commencer à utiliser les programmes d’apprentissage, cliquez sur Programmes d’apprentissage dans le volet de gauche, sélectionnez un ensemble de cours dans le catalogue et lancez la publication. Reportez-vous à [Aide des programmes d’apprentissage](feature-summary/learning-programs.md) pour obtenir des instructions spécifiques.

## Étape 4 : gestion de votre système LMS (administrateur Learning Manager) {#phase4managingyourlmscaptivateprimeadministrator}

### Annonces {#announcements}

Les annonces sont utiles pour diffuser des informations importantes à tous les élèves d’un compte en une seule fois. Dans l’application Learning Manager, une annonce est un message multimédia (texte, image ou vidéo) qu’un administrateur peut créer et diffuser à destination d’un ensemble défini de groupes d’utilisateurs et d’objets d’apprentissage. Vous pouvez envoyer les annonces instantanément ou les planifier pour qu’elles se déclenchent automatiquement à une date spécifique. Si vous souhaitez utiliser cette fonctionnalité dans l’application Learning Manager, sélectionnez Annonces dans le volet de gauche et cliquez sur Ajouter pour créer des annonces. Reportez-vous à [Aide sur les annonces](feature-summary/announcements.md) pour plus d’informations.

### Inscription des utilisateurs {#userenrollment}

L’inscription des utilisateurs constitue une étape importante pour une application LMS. À ce stade, vous pouvez commencer à inscrire les élèves à différents objets d’apprentissage de l’application Learning Manager. Vous pouvez inscrire les élèves manuellement ou de manière automatisée en utilisant les plans d’apprentissage.

#### Inscription manuelle {#manualenrollment}

* **Auto-inscription -** Si vous activez cette option lors de la création d’un objet d’apprentissage, les élèves peuvent s’inscrire aux objets d’apprentissage.
* **Approbation du responsable** - Si vous choisissez cette option dans le type d&#39;inscription lors de la création d&#39;un cours, les responsables doivent approuver l&#39;inscription des élèves.
* **Nomination du responsable** - Si vous choisissez ce type d&#39;inscription lors de la création du cours, ces cours doivent être nommés par les responsables.
* **Inscription administrateur** - Dans ce cas, l’administrateur peut inscrire certains élèves en fonction des exigences de l’organisation.

Reportez-vous à [Aide à l’inscription des utilisateurs](feature-summary/courses.md)pour plus d’informations.

Pour inscrire manuellement des élèves à des objets d’apprentissage, vous pouvez procéder de l’une des quatre manières suivantes :

### Inscription automatisée {#automatedenrollment}

Automatisez l’inscription des élèves aux objets d’apprentissage, à l’aide des plans d’apprentissage.

#### Plans d’apprentissage (basés sur des déclencheurs) {#learningplansbasedontriggers}

Vous pouvez utiliser les plans d’apprentissage pour affecter automatiquement des cours, des programmes d’apprentissage ou des certifications aux élèves en fonction de certains événements. Par exemple,

* Un nouvel utilisateur est ajouté.
* Un utilisateur change de groupe d’utilisateurs.
* Un élève achève un objet d’apprentissage.
* Un utilisateur achève une compétence.

Reportez-vous à [Aide sur les plans d’apprentissage](feature-summary/learning-plans.md)  pour plus d’informations.

### Création de rapports {#createreports}

À ce stade, vous pouvez commencer à créer différents types de rapport et à gérer ceux-ci.

Adobe Learning Manager permet de créer différents rapports pour suivre, surveiller et contrôler les activités des élèves. Vous pouvez utiliser les trois types de fonctions de génération de rapports suivants :

* **Tableau de bord Rapports** - Créez des rapports de synthèse pour obtenir des informations exploitables sur la consommation de contenu d’apprentissage par vos élèves, en fonction de diverses catégories telles que les groupes d’utilisateurs, l’efficacité, le temps des élèves sur les cours, etc.
* **Relevés de notes des élèves** - Créez des rapports centrés sur les élèves avec un historique complet des élèves du jour de l’inscription à la date du jour.
* **Rapports de cours** - Créer des statistiques de consommation de cours des élèves à partir de cours individuels. Vous pouvez également créer des rapports de quiz au niveau du cours.

Reportez-vous à  [Aide sur les rapports](feature-summary/reports.md) pour plus d&#39;informations sur le processus de génération de rapports.

Pour toute autre information relative à l’utilisation des fonctionnalités de l’application Learning Manager, reportez-vous à [Aide de Learning Manager](../topics.md) selon chaque rôle.
