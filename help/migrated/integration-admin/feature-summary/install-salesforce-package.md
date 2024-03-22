---
jcr-language: en_us
title: Installation du package Salesforce
description: Learning Manager propose un package d’application Salesforce. Une fois le package installé et configuré dans SFDC, les vendeurs peuvent effectuer leurs activités de formation sur le portail SFDC. Cette application permet aux utilisateurs de SFDC d’explorer les nouvelles formations, de consulter les recommandations et de les utiliser directement dans le portail SFDC. Les utilisateurs reçoivent également les annonces envoyées par les administrateurs sous la forme d’en-têtes directement dans l’application dans le portail SFDC.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: 970c5f46d6af49bfcca09f88f3d0ece1168fe442
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 51%

---

# Installation du package Salesforce

## Vue d’ensemble

Learning Manager propose un package d’application Salesforce. Une fois le package installé et configuré dans SFDC, les vendeurs peuvent effectuer leurs activités de formation sur le portail SFDC. Cette application permet aux utilisateurs de SFDC d’explorer les nouvelles formations, de consulter les recommandations et de les utiliser directement dans le portail SFDC. Les utilisateurs reçoivent également les annonces envoyées par les administrateurs sous la forme d’en-têtes directement dans l’application dans le portail SFDC.

### Configuration dans l’application Learning Manager

1. Connectez-vous à votre compte d’administrateur Learning Manager en tant qu’administrateur d’intégration.
1. Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications fournies]**.
1. Cliquez sur **[!UICONTROL Salesforce]**.
1. Sur la page de l’application Salesforce, notez l’ID d’application (également appelé ID client) et le secret client mentionné dans la description.
1. Cliquez sur **[!UICONTROL Approuver]** et votre application doit être approuvée.
1. Cliquez sur **[!UICONTROL Ressources pour les développeurs]** > **[!UICONTROL Jetons d’accès pour le test et le développement]**.
1. Dans la section Obtenir le code OAuth, l’ID client et la portée doivent être définis sur - admin:read, admin:write. Cliquez sur **[!UICONTROL Envoyer]**.
1. Dans la section Obtenir le jeton d’actualisation, entrez l’ID client et le secret client. Cliquez sur **[!UICONTROL Envoyer]** et notez le jeton d’actualisation.

### Création d’un compte dans l’application Salesforce

1. Créez un compte sur la page d’inscription Salesforce. Vous devez créer un compte Salesforce dans l’édition pour développeurs ou entreprises.  [URL d’inscription du développeur](https://developer.salesforce.com/signup). Pour vous inscrire à Salesforce, veillez à utiliser l’ID de messagerie que vous avez utilisé pour Learning Manager.
1. Validez votre compte via l’e-mail de vérification.
1. Créez un mot de passe et connectez-vous à Salesforce.
1. Notez l’URL Salesforce après la connexion (par exemple, site.lightning.force.com).

### Installation du package Learning Manager

Si vous souhaitez installer le package, vous devez d’abord supprimer le pack existant dans Salesforce. Avant de procéder à la désinstallation, vous devez activer les paramètres, comme indiqué ci-dessous. L’application de ces paramètres est obligatoire, sinon vous ne pourrez pas installer le package.

![](assets/uninstall-package.png)

*Installation du package Learning Manager*

>[!NOTE]
>
>L’application Adobe Learning Manager est uniquement prise en charge dans la vue Salesforce Lightning.

1. Lancez l’outil  [URL du package Learning Manager](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP).
1. Dans le panneau **Connexion** page, cliquez sur **[!UICONTROL Utiliser un domaine personnalisé]**.

1. Saisissez l’URL du pack, puis cliquez sur **[!UICONTROL Continuer]**. L’option Installer pour les administrateurs uniquement doit être sélectionnée sur la page d’installation. Ne modifiez pas cette option.
1. Cliquez sur **Insgrand**. Une fois le pack installé, cliquez sur **[!UICONTROL Terminé]**. Vous êtes guidé vers la page Packages installés où vous pouvez voir le package Adobe Learning Manager installé.

1. Accédez au Lanceur d’applications (en regard de Configuration) et recherchez Adobe Learning Manager.
1. Pour configurer l’application, cliquez sur **[!UICONTROL Configurer]**.
1. Cliquez sur **[!UICONTROL Nouveau]** et ajoutez les détails suivants :

   * **Config :** entrez le nom de votre choix.
   * **ClientID**: entrez la valeur que vous avez obtenue à partir de la première section.
   * **ClientSecret :** Entrez la valeur obtenue à partir de la première section.
   * **RefreshToken :** Entrez la valeur obtenue à partir de la première section.
   * **LearningManagerBaseURL :** URL du site où Learning Manager est hébergé.
   * **Désactiver la redirection :** désactivez la redirection vers la page d’accueil de l’élève dans Learning Manager.

>[!NOTE]
>
>Vous ne pouvez créer qu’une seule configuration. Si vous essayez d’ajouter une autre configuration, un message d’erreur s’affiche. La configuration mappe le compte Salesforce au compte Élève.

### Ajout des paramètres du site distant

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Configuration]**.
1. Entrée **Recherche rapide**, recherchez Paramètres du site distant.
1. Cliquez sur **[!UICONTROL Nouveau site distant]**.
1. Saisissez les détails :

   1. **Nom du site distant :** entrez le nom de votre choix.
   1. **URL du site distance :** URL du site où Learning Manager est hébergé.

1. Lancez Learning Manager.

### Activez les notifications pour l’application Learning Manager

1. Dans le coin supérieur droit, cliquez sur **Configuration**.
1. Recherchez Notifications personnalisées.
1. Cliquez sur **[!UICONTROL Nouveau]**.
1. Saisissez les détails suivants :

   1. **Nom de la notification personnalisée :** LearningManagerNotification
   1. **Nom de l’API :** LearningManagerNotification

1. Sélectionner les deux **Poste de travail** et **Mobile** comme canaux pris en charge.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
1. Pour activer les notifications Push sur les appareils mobiles, procédez comme suit :

   1. Installez l’application mobile Salesforce sur votre téléphone mobile.
   1. Connectez-vous à l’application à l’aide de vos informations d’identification.
   1. Accéder à **Configuration** > **Paramètres de remise des notifications**.
   1. Ajoutez Salesforce pour iOS et Android.

### Désinstaller Learning Manager de Salesforce

1. Dans l’application Salesforce, accédez à Packages installés.
1. Cliquez sur **[!UICONTROL Désinstaller]**.

## Configuration de Learning Manager pour les utilisateurs Salesforce

L’application Learning Manager est également disponible pour les utilisateurs qui sont présents dans n’importe quel compte Salesforce. L’administrateur Salesforce peut ajouter des utilisateurs en fonction des profils. Les profils Salesforce sont similaires à ce qu’ils sont dans Learning Manager. Par exemple, Administrateur, Administrateur d’intégration, Instructeur, etc. L’administrateur Salesforce peut également créer un profil personnalisé.

### Profil

En tant qu’administrateur Salesforce, vous pouvez affecter les profils aux utilisateurs ou créer un profil personnalisé.

>[!NOTE]
>
>Les utilisateurs doivent être présents à la fois dans Salesforce et dans Learning Manager.

![](assets/create-profile.png)

*Attribution d’un profil à un élève*

Lors de l’ajout d’un élève, vous devez lui attribuer un profil spécifique. Accédez ensuite à ce profil et accordez l’accès requis.

Pour que les élèves puissent afficher l’application Learning Manager, vous devez l’activer pour tous les élèves.

L’étape suivante consiste à fournir l’autorisation d’accéder à l’application Learning Manager.

![](assets/permission-set.png)

*Ajouter des autorisations pour accéder à l’application Learning Manager*

Lorsque vous installez le pack, un nouveau jeu d’autorisations est créé. **Utilisateur Adobe Learning Manager**. Accédez au jeu d’autorisations, puis ajoutez les utilisateurs.

Sélectionnez les utilisateurs et attribuez les autorisations en conséquence. Les élèves peuvent désormais accéder à l’application Learning Manager.

Ensuite, sélectionnez un profil, par exemple Profil standard d’un utilisateur, puis cliquez sur le profil. Cliquez sur **[!UICONTROL Modifier]** et dans le **Paramètres d’application personnalisés** section, activez la case à cocher **Adobe Learning Manager**. Cela rend l’application accessible à l’utilisateur.

Dans la section **Paramètres d’onglet personnalisés**, dans la liste déroulante **Page d’accueil de l’élève**, sélectionnez l’option **[!UICONTROL Par défaut sur]**.

Vous devez rendre l’application visible à tous les profils.

Cliquez sur **[!UICONTROL Enregistrer]** et les élèves appartenant à tous les profils accéderont à l’application Learning Manager.
