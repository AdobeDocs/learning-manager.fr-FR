---
jcr-language: en_us
title: Installation du package Salesforce
description: Learning Manager propose un package d’application Salesforce. Une fois le package installé et configuré dans SFDC, les vendeurs peuvent effectuer leurs activités de formation sur le portail SFDC. Cette application permet aux utilisateurs de SFDC d’explorer les nouvelles formations, de consulter les recommandations et de les utiliser directement dans le portail SFDC. Les utilisateurs reçoivent également les annonces envoyées par les administrateurs sous forme d’en-têtes de mât directement dans l’application dans le portail SFDC.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: dffa765061b35d4559388e4120e51943768c8db8
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 47%

---

# Installation du package Salesforce

## Vue d’ensemble

Learning Manager propose un package d’application Salesforce. Une fois le package installé et configuré dans SFDC, les vendeurs peuvent effectuer leurs activités de formation sur le portail SFDC. Cette application permet aux utilisateurs de SFDC d’explorer les nouvelles formations, de consulter les recommandations et de les utiliser directement dans le portail SFDC. Les utilisateurs reçoivent également les annonces envoyées par les administrateurs sous forme d’en-têtes de mât directement dans l’application dans le portail SFDC.

### Configuration dans l’application Learning Manager

1. Connectez-vous à votre compte d’administrateur Learning Manager en tant qu’administrateur d’intégration.
1. Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications proposées]**.
1. Cliquez sur **[!UICONTROL Salesforce]**.
1. Sur la page de l’application Salesforce, notez l’ID d’application (également appelé ID client) et la clé secrète client mentionnées dans la description.
1. Cliquez sur **[!UICONTROL Approuver]** et votre application doit être approuvée.
1. Cliquez sur **[!UICONTROL Références]** pour les développeurs > **[!UICONTROL jetons d’accès à des fins de test et de développement]**.
1. Dans la section Get OAuth Code, l’ID client et l’étendue doivent être définis sur admin :read,admin :write. Cliquez sur **[!UICONTROL Envoyer]**.
1. Dans la section Obtenir le jeton d’actualisation, entrez l’ID client et le secret client. Cliquez sur **[!UICONTROL Envoyer]** , puis notez le jeton d’actualisation.

### Création d’un compte dans l’application Salesforce

1. Créez un compte sur la page d’inscription Salesforce. Vous devez créer un compte Salesforce dans l’édition développeur ou enterprise.  [URL](https://developer.salesforce.com/signup) d’inscription des développeurs. Assurez-vous que vous devez utiliser l’ID de messagerie pour vous inscrire à Salesforce que vous avez utilisé pour Learning Manager.
1. Validez votre compte via l’e-mail de vérification.
1. Créez un mot de passe et connectez-vous à Salesforce.
1. Notez l’URL de Salesforce après la connexion (par exemple, site.lightning.force.com

### Installation du package Learning Manager

Si vous souhaitez installer le package, vous devez d’abord supprimer le pack existant dans Salesforce. Avant de procéder à la désinstallation, vous devez activer les paramètres, comme indiqué ci-dessous. L’application de ces paramètres est obligatoire, sinon vous ne pourrez pas installer le package.

![](assets/uninstall-package.png)

*Installer le package Learning Manager*

>[!NOTE]
>
>L’application Adobe Learning Manager est uniquement prise en charge dans la vue Lightning de Salesforce.

1. Launch l’URL](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP) du [package Learning Manager.
1. Dans la page Connexion **, cliquez sur**[!UICONTROL  Utiliser le **domaine]** personnalisé.

1. Saisissez l’URL du package et cliquez sur **[!UICONTROL Continuer]**. L’option Installation pour les administrateurs uniquement doit être sélectionnée sur la page d’installation. Ne modifiez pas cette option.
1. Cliquez sur **Inshaut**. Une fois le package installé, cliquez sur **[!UICONTROL Terminé]**. Vous êtes guidé vers la page Packages installés où vous pouvez voir le package Adobe Learning Manager installé.

1. Accédez au Lanceur d’applications (en regard de Configuration) et recherchez Adobe Learning Manager.
1. Pour configurer l’application, cliquez sur **[!UICONTROL Configurer]**.
1. Cliquez sur **[!UICONTROL Nouveau]** et ajoutez les détails suivants :

   * **Config :** entrez le nom de votre choix.
   * **ClientID** : saisissez la valeur que vous avez obtenue dans la première section.
   * **ClientSecret :** saisissez la valeur que vous avez obtenue dans la première section.
   * **RefreshToken :** saisissez la valeur que vous avez obtenue dans la première section.
   * **LearningManagerBaseURL :** URL du site où est hébergé Learning Manager.
   * **Désactiver la redirection :** désactivez la redirection vers la page d’accueil de l’élève dans Learning Manager.

>[!NOTE]
>
>Vous pouvez créer une seule configuration. Si vous essayez d’ajouter une autre configuration, un message d’erreur s’affiche. La configuration mappe le compte Salesforce au compte Élève.

### Ajout des paramètres du site distant

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Configuration]**.
1. Dans **la recherche** rapide, recherchez Paramètres du site distant.
1. Cliquez sur **[!UICONTROL Nouveau site]** distant.
1. Saisissez les détails :

   1. **Nom du site distant :** entrez le nom de votre choix.
   1. **URL du site distance :** URL du site où Learning Manager est hébergé.

1. Lancez Learning Manager.

### Ajout du domaine Adobe à Salesforce URL approuvées

Pour ajouter le domaine Adobe aux URL approuvées, procédez comme suit :

1. Dans la console Salesforce, accédez à **[!UICONTROL Configuration]** > **[!UICONTROL Recherche]** rapide.
1. Search pour **[!UICONTROL URL approuvées]** et sélectionnez **[!UICONTROL Nouvelle URL]** approuvée.
1. Saisissez un nom dans le champ Nom de ]**l’API**[!UICONTROL .
1. Ajoutez l’URL en tant que `{}.adobe.com{*}`fichier .
1. Cochez toutes les cases des directives **CSP** et enregistrez les modifications.
1. Modifiez le jeton d’actualisation de l’application Salesforce et enregistrez-le.
1. Relancez l’application Salesforce.

### Activez les notifications pour l’application Learning Manager

1. Dans le coin supérieur droit, cliquez sur **Configuration**.
1. Recherchez Notifications personnalisées.
1. Cliquez sur **[!UICONTROL Nouveau]**.
1. Saisissez les détails suivants :

   1. **Nom de notification personnalisé :** LearningManagerNotification
   1. **Nom de l’API :** LearningManagerNotification

1. Sélectionnez Bureau **** et **Mobile** comme canaux pris en charge.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
1. Pour activer les notifications Push sur les appareils mobiles, procédez comme suit :

   1. Installez l’application mobile Salesforce sur votre téléphone mobile.
   1. Connectez-vous à l’application à l’aide de vos informations d’identification.
   1. Accédez à **Configuration** > **paramètres** de remise de notification.
   1. Ajoutez Salesforce pour iOS et Android.

### Désinstaller Learning Manager de Salesforce

1. Dans l’application Salesforce, accédez à Package installés.
1. Cliquez sur **[!UICONTROL Désinstaller]**.

## Configuration de Learning Manager pour les utilisateurs Salesforce

L’application Learning Manager est également disponible pour les utilisateurs qui sont présents dans n’importe quel compte Salesforce. L’administrateur Salesforce peut ajouter des utilisateurs en fonction des profils. Les profils Salesforce sont similaires à ce qu’ils sont dans Learning Manager. Par exemple, Administrateur, Administrateur d’intégration, Instructeur, etc. L’administrateur Salesforce peut également créer un profil personnalisé.

### Profil

En tant qu’administrateur Salesforce, vous pouvez affecter les profils aux utilisateurs ou créer un profil personnalisé.

>[!NOTE]
>
>Les utilisateurs doivent être présents dans Salesforce et Learning Manager.

![](assets/create-profile.png)

*Attribuer un profil à un apprenant*

Lorsque vous ajoutez un élève, vous devez lui attribuer un profil spécifique. Accédez ensuite à ce profil et accordez l’accès requis.

Pour que les apprenants puissent afficher l’application Gestionnaire de formation, vous devez activer l’application pour tous les élèves.

L’étape suivante consiste à fournir l’autorisation d’accéder à l’application Learning Manager.

![](assets/permission-set.png)

*Ajouter des autorisations pour accéder à l’application Gestionnaire de la formation*

Lorsque vous installez le package, un nouveau jeu d’autorisations est créé **Adobe utilisateur** Learning Manager. Accédez au jeu d’autorisations, puis ajoutez les utilisateurs.

Sélectionnez les utilisateurs et attribuez les autorisations en conséquence. Les élèves peuvent désormais accéder à l’application Learning Manager.

Ensuite, sélectionnez un profil, par exemple Profil standard d’un utilisateur, puis cliquez sur le profil. Cliquez sur **[!UICONTROL Modifier]** et, dans la section Paramètres d’application **personnalisés** , activez la case **à cocher Adobe Gestionnaire** de formation. Cela rend l’application accessible à l’utilisateur.

Dans la section **Paramètres d’onglet personnalisés**, dans la liste déroulante **Page d’accueil de l’élève**, sélectionnez l’option **[!UICONTROL Par défaut sur]**.

Vous devez rendre l’application visible à tous les profils.

Cliquez sur **[!UICONTROL Enregistrer]** et les apprenants appartenant à tous les profils accéderont à l’application Learning Manager.
