---
description: Ce document fournit une approche recommandée aux organisations pour configurer Adobe Learning Manager. L’équipe Learning Manager suggère une approche par étapes pour commencer à utiliser l’application. Il n’est pas obligatoire de suivre toutes les phases dans une séquence spécifique.
jcr-language: en_us
title: Guide des bonnes pratiques pour configurer Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 0%

---



# Guide des bonnes pratiques pour configurer Learning Manager

Ce document fournit une approche recommandée aux organisations pour configurer Adobe Learning Manager. L’équipe Learning Manager suggère une approche par étapes pour commencer à utiliser l’application. Il n’est pas obligatoire de suivre toutes les phases dans une séquence spécifique.

Ces phases peuvent être effectuées par trois rôles différents, par une ou plusieurs personnes en fonction de la configuration de votre organisation. Les trois rôles sont les suivants :

1. **Administrateur informatique** - L’administrateur informatique effectue les activités d’activation ou d’intégration associées à l’application Learning Manager dans une organisation. L’administrateur informatique peut également ajouter un ou plusieurs utilisateurs et jouer le rôle d’administrateur d’intégration.
1. **Auteur** - L’auteur crée le contenu d’apprentissage requis pour les besoins d’apprentissage de l’organisation. L’auteur du contenu de formation ou d’apprentissage de votre organisation peut commencer à créer le contenu de base requis pour l’application Learning Manager.
1. **Administrateur Learning Manager** - L’administrateur de l’application Learning Manager effectue les activités de configuration et d’installation. Dans certaines entreprises, l’administrateur informatique peut également jouer un rôle d’administrateur de l’application Learning Manager.

Vous pouvez parcourir l&#39;infographie ci-dessous pour obtenir un aperçu des phases et des tâches correspondantes.

![](assets/learning-manager-getting-started.jpg)

À ce stade, nous supposons que votre organisation a déjà reçu la clé de licence et que vous avez activé le compte Learning Manager. Comme mentionné dans l&#39;infographie, les trois pistes sont expliquées comme suit :

## Phase 1 - Configuration technique (administrateur informatique) {#phase1technicalsetupitadministrator}

Dans le Pôle 1, l’administrateur informatique de votre organisation peut passer au rôle d’administrateur d’intégration dans l’application Learning Manager et effectuer certaines activations et intégrations comme suit :

### Activer/ajouter des champs actifs (administrateur Learning Manager) {#enableaddactivefieldscaptivateprimeadministrator}

En plus des champs actifs fournis par les utilisateurs lors de l’inscription, l’administrateur peut ajouter d’autres champs actifs. L’administrateur peut également activer/désactiver les champs utilisateur. Les valeurs de ces champs actifs sont générées à partir des métadonnées de diverses sources de données associées aux comptes utilisateur. Reportez-vous à [Aide sur les champs actifs](feature-summary/add-users-user-groups.md#active-fields) pour plus d’informations.

### Authentification unique (SSO) {#singlesignonsso}

Vous pouvez accéder à l’application Learning Manager à l’aide d’Adobe ID ou de l’authentification unique. L’authentification unique est un mécanisme qui permet à un utilisateur de s’authentifier une fois et d’accéder à plusieurs applications à la fois. Cette configuration n’est pas obligatoire pour l’organisation. Si votre organisation dispose d’un fournisseur d’authentification unique basé sur SAML 2.0, vous pouvez l’utiliser pour configurer l’application Learning Manager. La configuration est requise au niveau de votre organisation et de l’application Learning Manager. Si vous choisissez d’utiliser l’authentification unique, contactez le support Adobe pour recevoir des instructions de configuration. Reportez-vous à [Aide sur les paramètres](feature-summary/settings.md) pour plus d’informations.

### Importation en bloc d’utilisateurs {#bulkimportofusers}

Lorsque le volume d’utilisateurs est élevé dans votre organisation, vous pouvez importer tous les utilisateurs en bloc dans l’application Learning Manager à l’aide d’un fichier CSV. Avant d’effectuer cette tâche, nous vous suggérons d’exporter la liste des utilisateurs de l’application de RH de votre organisation au format .CSV. Même si vous n’importez pas les utilisateurs en masse à ce stade, vous pouvez vous familiariser avec le format CSV. Pour commencer le processus d’importation dans Learning Manager, vous devez télécharger le fichier .CSV et mapper les champs de données de l’application avec les colonnes CSV de votre organisation. Reportez-vous à [Aide sur l’importation en bloc](add-users-in-bulk.md) pour plus d’informations.

### Intégration du connecteur FTP {#ftpconnectorintegration}

Si vous êtes confronté à l’ajout ou au retrait continu d’employés dans votre organisation, vous pouvez choisir d’automatiser l’importation en bloc d’utilisateurs à l’aide du connecteur FTP. Vous devez d’abord établir une connexion, puis vous pouvez charger un fichier CSV et mapper les attributs du fichier CSV avec les champs Learning Manager correspondants. Vous pouvez planifier le processus d’importation automatique et également le synchroniser au besoin. Reportez-vous à [Aide du connecteur FTP](../integration-admin/feature-summary/connectors.md#ftpconnector) pour plus d’informations.

### Intégration du connecteur Salesforce {#salesforceconnectorintegration}

Si votre organisation dispose d’un compte Salesforce, vous pouvez automatiser le processus d’importation de tous les utilisateurs de Salesforce dans l’application Learning Manager. Si vous souhaitez utiliser cette fonctionnalité, vous pouvez utiliser le connecteur Salesforce pour intégrer Learning Manager au compte Salesforce et automatiser la synchronisation des données. Utilisez la fonction de planification automatique pour effectuer régulièrement l’importation automatique des utilisateurs. Vous pouvez également effectuer une synchronisation quotidienne. Reportez-vous à [Aide du connecteur Salesforce](../integration-admin/feature-summary/connectors.md#sfconnector) pour plus d’informations.

### Intégration d’Adobe Connect {#adobeconnectintegration}

Si vous utilisez Adobe Connect dans votre organisation, vous pouvez l’intégrer à l’application Adobe Learning Manager pour offrir une expérience utilisateur transparente aux élèves. L’intégration permet à vos élèves d’accéder aux classes virtuelles directement dans l’application Learning Manager en un seul clic, sans avoir à se reconnecter à Adobe Connect. Grâce à cette fonctionnalité, vos élèves peuvent également utiliser les sessions de classe virtuelle enregistrées dans l’application Learning Manager. Pour l’intégrer, intégrez d’abord les paramètres. Utilisation **Paramètres > Adobe Connect > Configurer maintenant** pour fournir l’URL de connexion et les informations de connexion et les intégrer. Reportez-vous à [Aide sur l’intégration d’Adobe Connect](feature-summary/adobeconnect-integration.md) pour plus d’informations.

### Inscription à l’application Salesforce {#salesforceappregistration}

Les élèves de votre entreprise peuvent bénéficier d’une expérience transparente de l’accès à l’application Learning Manager directement dans leurs comptes Salesforce. Les élèves peuvent accéder au contenu d’apprentissage qui leur est attribué, tel que les cours, les programmes d’apprentissage et les assistances à la tâche, à partir de l’application Salesforce. Les utilisateurs peuvent également accéder aux notifications et aux annonces à partir de l’application Learning Manager dans Salesforce. Pour utiliser cette fonctionnalité, vous devez enregistrer l’application proposée Salesforce dans l’application Learning Manager. Reportez-vous à [Aide de l’application Salesforce](../integration-admin/feature-summary/sfdc-app.md) pour en savoir plus sur l’installation et les instructions d’utilisation.

## Phase 2 - Configuration du site (administrateur de Learning Manager) {#phase2siteconfigurationcaptivateprimeadministrator}

L’administrateur de l’application Learning Manager de votre organisation doit configurer ou configurer certaines fonctionnalités avant de commencer à les implémenter pour vos élèves.

### Branding {#branding}

Une organisation peut souhaiter afficher le logo de l’entreprise dans l’application Learning Manager, avoir son propre domaine dans l’URL, afficher le nom de l’organisation et afficher des palettes de couleurs correspondant à la marque d’une organisation. Learning Manager permet aux organisations d’utiliser toutes ces fonctionnalités. Pour personnaliser les paramètres et utiliser votre propre branding, cliquez sur la section Branding dans le volet de gauche. Cliquez sur Modifier en regard de toutes ces options et personnalisez-les selon vos besoins. Reportez-vous à [Aide sur le branding et les thèmes](feature-summary/themes.md) pour plus d’informations.

### Ajouter des utilisateurs/groupes d’utilisateurs {#addusersusergroups}

Les élèves étant les principaux utilisateurs de votre contenu d’apprentissage, l’ajout d’utilisateurs dans le système de gestion de l’apprentissage est l’étape principale. Ajouter des utilisateurs à l’application Learning Manager et leur attribuer des rôles. Vous pouvez ajouter des utilisateurs de l’une des manières suivantes :

#### Ajouter des utilisateurs (interne) {#addusersinternal}

* **En tant qu’utilisateur unique** - L’ajout d’utilisateurs uniques dans l’application Learning Manager vous permet d’essayer certains utilisateurs avant de les ajouter en bloc. En outre, cette option est utile lorsque vous souhaitez ajouter d’autres utilisateurs uniques en fonction des besoins, après l’importation en bloc d’utilisateurs.
* **Auto-inscription** - Cette option permet aux administrateurs d’autoriser leurs employés à s’inscrire à Learning Manager.
* **Importation en bloc** (avec le chargement CSV) : cette option vous permet d’importer des utilisateurs par lot dans l’application Learning Manager. Comme condition préalable, vous devez tenir la liste des utilisateurs prête au format CSV avant d’utiliser cette fonctionnalité.

#### Ajout d’utilisateurs (profils externes) {#addusersexternalprofiles}

* Inscription externe : à l’aide de cette option, vous pouvez inscrire des membres de service externes ou des employés externes de votre organisation à l’application.

#### Ajouter des groupes d’utilisateurs {#addusergroups}

L’application Learning Manager génère des groupes d’utilisateurs par défaut en fonction d’attributs similaires. En plus des groupes par défaut, vous pouvez générer des groupes d’utilisateurs personnalisés en fonction de paramètres tels que la désignation, l’emplacement, afin de pouvoir utiliser ces groupes dans la ludification et les rapports, entre autres. Reportez-vous à [Aide pour l’ajout d’utilisateurs](feature-summary/add-users-user-groups.md) pour plus d’informations.

### Attribution de rôles {#assignroles}

Une fois les utilisateurs ajoutés à Learning Manager, l’administrateur peut commencer à affecter des rôles d’auteur, d’administrateur ou d’administrateur d’intégration aux utilisateurs en fonction des exigences de l’organisation. Pour attribuer des rôles aux utilisateurs, dans la connexion Administrateur, vous pouvez cliquer sur **[!UICONTROL Utilisateurs]**  dans le volet de gauche, cochez la case en regard de chaque nom d’utilisateur, puis cliquez sur **[!UICONTROL Actions]** liste déroulante pour choisir le rôle que vous souhaitez attribuer. Les rôles de responsable sont attribués aux utilisateurs par Adobe Learning Manager en fonction des rôles/privilèges mentionnés par votre organisation dans le fichier CSV. Vous pouvez également modifier les rôles des utilisateurs en tant que responsables à l’aide du workflow Modifier les utilisateurs. Reportez-vous à [Aide pour l’ajout d’utilisateurs](feature-summary/add-users-user-groups.md) pour plus d’informations.

### Modèles de notification {#notificationtemplates}

Les notifications peuvent être utiles aux utilisateurs d’un système de gestion de l’apprentissage pour connaître leur statut ou être informés des événements/activités. Lors de la création de cours, de la configuration des fonctionnalités ou de l’utilisation des cours, les utilisateurs passent par plusieurs événements qui déclenchent des notifications aux élèves, à leurs responsables, administrateurs ou auteurs. Learning Manager fournit divers modèles de notification par e-mail dans l’application. En tant qu’administrateur, vous pouvez les personnaliser en fonction des besoins de votre organisation. Pour créer des notifications par e-mail, choisissez **Modèles de courrier électronique** dans le volet de gauche et cliquez sur le nom du modèle. Reportez-vous à [Aide sur les modèles de courrier électronique](feature-summary/email-templates.md) pour plus d’informations

**Désactiver les notifications par e-mail (recommandé)**

Par défaut, les notifications sont activées dans l’application Learning Manager. Vous pouvez désactiver les notifications à ce stade, si vous ne souhaitez pas informer vos employés de l’organisation.

### Badges {#badges}

Les badges sont une mesure de la réussite que votre employé peut gagner à la fin d’un cours. Les professionnels du monde entier utilisent ces badges comme une représentation d&#39;une compétence particulière ou d&#39;une réussite d&#39;apprentissage. Vous pouvez créer une collection de badges afin de pouvoir les attribuer aux élèves une fois le contenu d’apprentissage terminé. Pour commencer à créer des badges, cliquez sur **[!UICONTROL Badges]** dans le volet de gauche. Reportez-vous à  [Aide sur les badges](feature-summary/badges.md) pour plus d’informations.

### Commentaires {#feedback}

Le retour d’informations est l’un des facteurs importants d’un LMS pour mesurer les progrès d’apprentissage des élèves et garantir la qualité du contenu d’apprentissage. Learning Manager propose deux types d’options de retour d’informations aux utilisateurs.

* Le retour d’informations L1 est le retour d’informations donné par les élèves après avoir terminé le cours.
* Le retour d&#39;informations L3 correspond au retour d&#39;informations donné par les responsables aux élèves en fonction de l&#39;impact du cours sur le comportement des élèves et sur leurs activités quotidiennes.

Cette fonctionnalité est facultative pour les organisations. Les administrateurs peuvent personnaliser les modèles de retour d’informations en fonction des exigences de votre organisation. Pour utiliser cette fonctionnalité, l&#39;administrateur doit activer les options de retour d&#39;informations L1 et L3 au niveau de l&#39;instance de cours. Pour configurer le retour d’informations, choisissez un cours, cliquez sur Valeurs par défaut de l’instance dans le volet de gauche et activez l’option Retour d’informations. Reportez-vous à [Aide sur les commentaires](feature-summary/courses.md) pour plus d’informations.

### Ludification {#gamification}

Maintenir l&#39;engagement des élèves pendant qu&#39;ils consomment le contenu est l&#39;un des défis auxquels sont confrontées les organisations. La ludification augmente le taux d&#39;achèvement des cours en engageant et en motivant les élèves à atteindre leurs objectifs, à l&#39;aide de techniques de jeu. Les élèves peuvent rivaliser avec leurs collègues pour obtenir des points pour diverses activités d&#39;apprentissage et atteindre des niveaux de bronze, d&#39;argent, d&#39;or et de platine. Les administrateurs peuvent activer/désactiver chaque tâche de ludification et modifier l’attribution de points aux tâches. Learning Manager fournit la fonctionnalité de ludification avec certains paramètres par défaut. Vous pouvez commencer à utiliser la fonctionnalité avec les paramètres par défaut pendant un certain temps, puis choisir de la personnaliser. La configuration/modification des paramètres de cette fonctionnalité est facultative. Si votre organisation dispose d’un expert en la matière, nous vous recommandons de configurer les paramètres avant de l’utiliser. Reportez-vous à [Aide sur la ludification](feature-summary/gamification.md) pour plus d’informations.

### Création d’objets d’apprentissage {#createlearningobjects}

Il s’agit de l’étape logique où les trois pistes (piste 1, piste 2 et piste 3) convergent pour que vous puissiez passer à l’action suivante.

À ce stade, après avoir créé des modules et des cours, vous pouvez commencer à créer des objets d’apprentissage de niveau supérieur tels que des certifications, des programmes d’apprentissage ou des assistances à la tâche pour continuer. Avant de commencer à créer des objets d’apprentissage, assurez-vous d’avoir déjà ajouté des utilisateurs dans l’application Learning Manager, créé des modules et des cours.

#### Création de certifications {#createcertifications}

La certification est une preuve d’achèvement d’un contenu d’apprentissage ou une preuve de réussite pour les élèves, à titre unique ou périodique. L’inscription des élèves au contenu d’apprentissage peut être augmentée en fournissant une certification aux élèves à la fin du cours. En tant qu’administrateur, vous pouvez créer un programme de certification hébergé en interne ou géré par un tiers. Dans la certification interne, définissez les cours qu’un élève doit suivre pour obtenir sa certification. Avant de créer la certification, assurez-vous que certains cours sont disponibles dans le compte. Reportez-vous à  [Aide sur la certification](feature-summary/certifications.md) pour plus d&#39;informations sur la création de certifications.

#### Créer des assistances à la tâche {#createjobaids}

Les assistances à la tâche sont un référentiel de contenu de formation accessible aux élèves sans aucun critère d&#39;inscription ou d&#39;achèvement. Les élèves peuvent se référer à ces assistances à la tâche pendant qu&#39;ils sont sur la tâche pour obtenir de l&#39;aide pour effectuer une activité ou une tâche dans une organisation. Même s&#39;il n&#39;est pas obligatoire d&#39;utiliser des assistances à la tâche dans le cadre de la création de cours, l&#39;équipe Learning Manager vous recommande de créer des assistances à la tâche comme meilleure pratique pour votre organisation. Reportez-vous à  [Aide sur les assistances à la tâche](../authors/feature-summary/job-aids.md) pour plus d&#39;informations sur la création d&#39;assistances à la tâche.

#### Création de programmes d’apprentissage {#createlearningprograms}

Les programmes d’apprentissage sont un ensemble de cours conçus de manière unique pour répondre à des objectifs d’apprentissage spécifiques. Avant de créer des programmes d&#39;apprentissage, assurez-vous d&#39;avoir déjà créé certains cours ou de disposer de cours existants dans votre compte.  Même s’il est facultatif pour une organisation d’utiliser cette fonctionnalité, l’équipe de Learning Manager vous recommande de l’utiliser pour inculquer une formation ciblée à vos employés. Pour commencer à utiliser les programmes d’apprentissage, cliquez sur Programmes d’apprentissage dans le volet de gauche, choisissez un ensemble de cours dans le catalogue et publiez-les. Reportez-vous à [Aide des programmes d’apprentissage](feature-summary/learning-programs.md) pour obtenir des instructions spécifiques.

### Création de catalogues {#createcatalogs}

Vous pouvez utiliser les catalogues d&#39;une organisation pour créer un contenu ciblé ou pour classifier le contenu selon un ensemble défini d&#39;élèves. Dans Learning Manager, un catalogue est une collection d’objets d’apprentissage tels que des cours, des certifications ou des programmes d’apprentissage. Vous pouvez choisir les objets d’apprentissage de votre choix lors de la création de catalogues. Assurez-vous d’avoir déjà créé un ensemble de cours, de certifications ou de programmes d’apprentissage avant de créer les catalogues. Vous pouvez créer des catalogues personnalisés avec un ensemble d&#39;objets d&#39;apprentissage si vous souhaitez les affecter à des groupes d&#39;utilisateurs internes ou externes. Reportez-vous à  [Aide des catalogues](feature-summary/catalogs.md) pour plus d’informations sur les catalogues.

### Activer les notifications par e-mail/l’accès utilisateur {#turnonemailnotificationsuseraccess}

À ce stade, vous pouvez activer les notifications par e-mail pour les utilisateurs de vos applications et également activer l’accès utilisateur.

## Phase 3 - Cours de création (Auteur) {#phase3authoringcoursesauthor}

Les développeurs ou auteurs de contenu de votre organisation peuvent commencer à créer le contenu d’apprentissage. Il est obligatoire de créer des modules et des cours car ils forment la base de tout votre contenu d’apprentissage dans l’application Learning Manager.

### Création de modules {#createmodules}

Les modules sont les composantes de base de l’application Learning Manager. Pour organiser votre contenu d’apprentissage, commencez à créer des modules en tant qu’auteur. Learning Manager vous permet de choisir l’un des quatre types de modules de cours, tels que salle de classe, auto-apprentissage, Activité et salle de classe virtuelle. Reportez-vous à  [Aide sur les modules](../authors/how-to-choose-modules.md) pour savoir quel type de module de cours est le mieux adapté aux besoins de votre organisation.

### Création de cours {#createcourses}

Les administrateurs peuvent assumer un rôle d’auteur dans l’application Learning Manager et créer des cours. Dans l’application Learning Manager, un cours est une unité de base avec un ensemble de modules, qui peut être attribuée à l’élève. Les élèves suivent les cours. Vous pouvez commencer à créer des cours en choisissant les modules que vous avez créés précédemment, associer les compétences que vous souhaitez que les élèves acquièrent à partir du cours, associer des niveaux, des crédits et des badges à un cours, sélectionner des assistances à la tâche, des conditions préalables et des ressources en fonction de votre choix et publier le cours. Vous pouvez également créer plusieurs instances d&#39;un cours afin de pouvoir affecter les instances de cours à plusieurs élèves dans différents fuseaux horaires, calendriers, etc. Reportez-vous à  [Aide des cours](../authors/feature-summary/courses.md)pour plus d&#39;informations sur la création d&#39;un cours.

### Création d’objets d’apprentissage {#Createlearningobjects-1}

Il s’agit de l’étape logique où les trois pistes (piste 1, piste 2 et piste 3) convergent pour que vous puissiez passer à l’action suivante.

À ce stade, après avoir créé des modules et des cours, vous pouvez commencer à créer des objets d’apprentissage de niveau supérieur tels que des certifications, des programmes d’apprentissage ou des assistances à la tâche pour continuer. Avant de commencer à créer des objets d’apprentissage, assurez-vous d’avoir déjà ajouté des utilisateurs dans l’application Learning Manager, créé des modules et des cours.

#### Création de certifications {#Createcertifications-1}

La certification est une preuve d’achèvement d’un contenu d’apprentissage ou une preuve de réussite pour les élèves, à titre unique ou périodique. L’inscription des élèves au contenu d’apprentissage peut être augmentée en fournissant une certification aux élèves à la fin du cours. En tant qu’administrateur, vous pouvez créer un programme de certification hébergé en interne ou géré par un tiers. Dans la certification interne, définissez les cours qu’un élève doit suivre pour obtenir sa certification. Avant de créer la certification, assurez-vous que certains cours sont disponibles dans le compte. Reportez-vous à  [Aide sur la certification](feature-summary/certifications.md) pour plus d&#39;informations sur la création de certifications.

#### Créer des assistances à la tâche {#CreateJobaids-1}

Les assistances à la tâche sont un référentiel de contenu de formation accessible aux élèves sans aucun critère d&#39;inscription ou d&#39;achèvement. Les élèves peuvent se référer à ces assistances à la tâche pendant qu&#39;ils sont sur la tâche pour obtenir de l&#39;aide pour effectuer une activité ou une tâche dans une organisation. Même s&#39;il n&#39;est pas obligatoire d&#39;utiliser des assistances à la tâche dans le cadre de la création de cours, l&#39;équipe Learning Manager vous recommande de créer des assistances à la tâche comme meilleure pratique pour votre organisation. Reportez-vous à  [Aide sur les assistances à la tâche](../authors/feature-summary/job-aids.md) pour plus d&#39;informations sur la création d&#39;assistances à la tâche.

#### Création de programmes d’apprentissage {#Createlearningprograms-1}

Les programmes d’apprentissage sont un ensemble de cours conçus de manière unique pour répondre à des objectifs d’apprentissage spécifiques. Avant de créer des programmes d&#39;apprentissage, assurez-vous d&#39;avoir déjà créé certains cours ou de disposer de cours existants dans votre compte.  Même s’il est facultatif pour une organisation d’utiliser cette fonctionnalité, l’équipe de Learning Manager vous recommande de l’utiliser pour inculquer une formation ciblée à vos employés. Pour commencer à utiliser les programmes d’apprentissage, cliquez sur Programmes d’apprentissage dans le volet de gauche, choisissez un ensemble de cours dans le catalogue et publiez-les. Reportez-vous à [Aide des programmes d’apprentissage](feature-summary/learning-programs.md) pour obtenir des instructions spécifiques.

## Phase 4 - Gestion de votre système de gestion de l’apprentissage (administrateur Learning Manager) {#phase4managingyourlmscaptivateprimeadministrator}

### Annonce {#announcements}

Les annonces sont utiles à l&#39;organisation pour diffuser toutes les informations importantes à tous les élèves d&#39;un compte en même temps. Dans l&#39;application Learning Manager, une annonce est un message multimédia (texte, image ou vidéo) qu&#39;un administrateur peut créer et diffuser à un ensemble défini de groupes d&#39;utilisateurs et d&#39;objets d&#39;apprentissage. Vous pouvez envoyer des annonces instantanément ou les planifier pour qu&#39;elles se déclenchent automatiquement à une date spécifique. Si vous souhaitez utiliser cette fonctionnalité dans l&#39;application Learning Manager, choisissez Annonces dans le volet de gauche et cliquez sur Ajouter pour créer des annonces. Reportez-vous à [Aide sur les annonces](feature-summary/announcements.md) pour plus d’informations.

### Inscription d’utilisateur {#userenrollment}

L’inscription des utilisateurs est une étape importante pour une application LMS. À ce stade, vous pouvez commencer à inscrire les élèves à divers objets d’apprentissage de l’application Learning Manager. Vous pouvez inscrire des élèves manuellement ou de manière automatisée, à l&#39;aide de plans d&#39;apprentissage.

#### Inscription manuelle {#manualenrollment}

* **Auto-inscription -** Si vous activez cette option lors de la création d’un objet d’apprentissage, les élèves peuvent s’inscrire aux objets d’apprentissage.
* **Approbation du responsable** - Si vous choisissez cette option dans le type d&#39;inscription lors de la création d&#39;un cours, les responsables doivent approuver l&#39;inscription des élèves.
* **Nomination du responsable** - Si vous choisissez ce type d&#39;inscription lors de la création du cours, ces cours doivent être nommés par les responsables.
* **Inscription administrateur** - Dans ce cas, l’administrateur peut inscrire certains élèves en fonction des exigences de l’organisation.

Reportez-vous à [Aide à l’inscription des utilisateurs](feature-summary/courses.md)pour plus d’informations.

Inscrivez des élèves à des objets d&#39;apprentissage manuellement en utilisant les quatre méthodes suivantes :

### Inscription automatisée {#automatedenrollment}

Automatisez l’inscription des élèves aux objets d’apprentissage, à l’aide des plans d’apprentissage.

#### Plans d’apprentissage (en fonction des déclencheurs) {#learningplansbasedontriggers}

Vous pouvez utiliser des plans d&#39;apprentissage pour affecter automatiquement des cours, des programmes d&#39;apprentissage ou des certifications aux élèves, en fonction de l&#39;occurrence de certains événements. Par exemple,

* Un nouvel utilisateur est ajouté
* L’utilisateur modifie le groupe d’utilisateurs
* L’élève termine un objet d’apprentissage
* L’utilisateur remplit une compétence

Reportez-vous à [Aide sur les plans d’apprentissage](feature-summary/learning-plans.md)  pour plus d’informations.

### Création de rapports {#createreports}

À ce stade, vous pouvez commencer à créer et à gérer différents types de rapports.

Adobe Learning Manager vous permet de créer divers rapports pour suivre, surveiller et contrôler les activités des élèves. Vous pouvez utiliser les trois types de fonctions de génération de rapports suivants :

* **Tableau de bord Rapports** - Créez des rapports de synthèse pour obtenir des informations exploitables sur la consommation de contenu d’apprentissage par vos élèves, en fonction de diverses catégories telles que les groupes d’utilisateurs, l’efficacité, le temps des élèves sur les cours, etc.
* **Relevés de notes des élèves** - Créez des rapports centrés sur les élèves avec un historique complet des élèves du jour de l’inscription à la date du jour.
* **Rapports de cours** - Créer des statistiques de consommation de cours des élèves à partir de cours individuels. Vous pouvez également créer des rapports de quiz au niveau du cours.

Reportez-vous à  [Aide sur les rapports](feature-summary/reports.md) pour plus d&#39;informations sur le processus de génération de rapports.

Pour toute autre information relative à l’utilisation des fonctionnalités de l’application Learning Manager, reportez-vous à [Aide de Learning Manager](../topics.md) selon chaque rôle.
