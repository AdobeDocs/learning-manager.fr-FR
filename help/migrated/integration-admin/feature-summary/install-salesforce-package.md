---
jcr-language: en_us
title: Installation du package Salesforce
description: Learning Manager propose un package d’application Salesforce. Une fois le package installé et configuré dans SFDC, les vendeurs peuvent effectuer leurs activités de formation sur le portail SFDC. Cette application permet aux utilisateurs de SFDC d’explorer les nouvelles formations, de consulter les recommandations et de les utiliser directement dans le portail SFDC. Les utilisateurs reçoivent également les annonces envoyées par les administrateurs sous la forme d’en-têtes directement dans l’application dans le portail SFDC.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: fb946ae98dce45156e2f4c1cf992319405403ea9
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 47%

---

# Installation du package Salesforce

## Vue d’ensemble

Learning Manager propose un package d’application Salesforce. Une fois le package installé et configuré dans SFDC, les vendeurs peuvent effectuer leurs activités de formation sur le portail SFDC. Cette application permet aux utilisateurs de SFDC d’explorer les nouvelles formations, de consulter les recommandations et de les utiliser directement dans le portail SFDC. Les utilisateurs reçoivent également les annonces envoyées par les administrateurs sous la forme d’en-têtes directement dans l’application dans le portail SFDC.

### Configuration dans l’application Learning Manager

1. Connectez-vous à votre compte d’administrateur Learning Manager en tant qu’administrateur d’intégration.
1. Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications phares]**.
1. Cliquez sur **[!UICONTROL Salesforce]**.
1. Sur la page de l’application Salesforce, notez l’ID d’application (également appelé ID client) et le secret client mentionné dans la description.
1. Cliquez sur **[!UICONTROL Approuver]** et votre application doit être approuvée.
1. Cliquez sur **[!UICONTROL Ressources pour les développeurs]** > **[!UICONTROL Jetons d&#39;accès pour le test et le développement]**.
1. Dans la section Obtenir le code OAuth, l’ID client et la portée doivent être définis sur - admin:read, admin:write. Cliquez sur **[!UICONTROL Envoyer]**.
1. Dans la section Obtenir le jeton d’actualisation, entrez l’ID client et le secret client. Cliquez sur **[!UICONTROL Envoyer]** et notez le jeton d’actualisation.

### Création d’un compte dans l’application Salesforce

1. Créez un compte sur la page d’inscription Salesforce. Vous devez créer un compte Salesforce dans l’édition pour développeurs ou entreprises.  [URL d&#39;inscription du développeur](https://developer.salesforce.com/signup). Pour vous inscrire à Salesforce, veillez à utiliser l’ID de messagerie que vous avez utilisé pour Learning Manager.
1. Validez votre compte via l’e-mail de vérification.
1. Créez un mot de passe et connectez-vous à Salesforce.
1. Notez l’URL Salesforce après la connexion (par exemple, site.lightning.force.com).

### Installation du package Learning Manager

Si vous souhaitez installer le package, vous devez d’abord supprimer le pack existant dans Salesforce. Avant de procéder à la désinstallation, vous devez activer les paramètres, comme indiqué ci-dessous. L’application de ces paramètres est obligatoire, sinon vous ne pourrez pas installer le package.

![](assets/uninstall-package.png)

*Installer le package Learning Manager*

>[!NOTE]
>
>L’application Adobe Learning Manager est uniquement prise en charge dans la vue Salesforce Lightning.

1. Lancez l&#39;[URL du package Learning Manager](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP).
1. Dans la page **Connexion**, cliquez sur **[!UICONTROL Utiliser un domaine personnalisé]**.

1. Entrez l&#39;URL du package et cliquez sur **[!UICONTROL Continuer]**. L’option Installer pour les administrateurs uniquement doit être sélectionnée sur la page d’installation. Ne modifiez pas cette option.
1. Cliquez sur **Inshaut**. Une fois le package installé, cliquez sur **[!UICONTROL Terminé]**. Vous êtes guidé vers la page Packages installés où vous pouvez voir le package Adobe Learning Manager installé.

1. Accédez au Lanceur d’applications (en regard de Configuration) et recherchez Adobe Learning Manager.
1. Pour configurer l&#39;application, cliquez sur **[!UICONTROL Configurer]**.
1. Cliquez sur **[!UICONTROL Nouveau]** et ajoutez les détails suivants :

   * **Config :** entrez le nom de votre choix.
   * **ClientID** : entrez la valeur que vous avez obtenue dans la première section.
   * **ClientSecret:** Entrez la valeur que vous avez obtenue à partir de la première section.
   * **RefreshToken:** Entrez la valeur que vous avez obtenue à partir de la première section.
   * **LearningManagerBaseURL :** URL du site où Learning Manager est hébergé.
   * **Désactiver la redirection :** désactivez la redirection vers la page d’accueil de l’élève dans Learning Manager.

>[!NOTE]
>
>Vous ne pouvez créer qu’une seule configuration. Si vous essayez d’ajouter une autre configuration, un message d’erreur s’affiche. La configuration mappe le compte Salesforce au compte Élève.

### Ajout des paramètres du site distant

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Configuration]**.
1. Dans **Recherche rapide**, recherchez Paramètres du site distant.
1. Cliquez sur **[!UICONTROL Nouveau site distant]**.
1. Saisissez les détails :

   1. **Nom du site distant :** entrez le nom de votre choix.
   1. **URL du site distance :** URL du site où Learning Manager est hébergé.

1. Lancez Learning Manager.

### Ajouter le domaine d’Adobe aux URL approuvées Salesforce

Pour ajouter le domaine d’Adobe aux URL approuvées, procédez comme suit :

1. Dans la console Salesforce, accédez à **[!UICONTROL Configuration]** > **[!UICONTROL Recherche rapide]**.
1. Recherchez **[!UICONTROL URL approuvées]** et sélectionnez **[!UICONTROL Nouvelle URL approuvée]**.
1. Saisissez un nom dans le champ **[!UICONTROL Nom de l&#39;API]**.
1. Saisissez `*.adobe.com` dans le champ URL.
1. Cochez toutes les cases des **directives CSP** et enregistrez les modifications.
1. Modifier le jeton d’actualisation de l’application Salesforce et l’enregistrer.
1. Relancez l’application Salesforce.

### Activez les notifications pour l’application Learning Manager

1. Dans le coin supérieur droit, cliquez sur **Configuration**.
1. Recherchez Notifications personnalisées.
1. Cliquez sur **[!UICONTROL Nouveau]**.
1. Saisissez les détails suivants :

   1. **Nom de la notification personnalisée :** LearningManagerNotification
   1. **Nom de l’API :** LearningManagerNotification

1. Sélectionnez **Bureau** et **Mobile** comme canaux pris en charge.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
1. Pour activer les notifications Push sur les appareils mobiles, procédez comme suit :

   1. Installez l’application mobile Salesforce sur votre téléphone mobile.
   1. Connectez-vous à l’application à l’aide de vos informations d’identification.
   1. Accédez à **Configuration** > **Paramètres de remise des notifications**.
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

*Attribuer un profil à un élève*

Lors de l’ajout d’un élève, vous devez lui attribuer un profil spécifique. Accédez ensuite à ce profil et accordez l’accès requis.

Pour que les élèves puissent afficher l’application Learning Manager, vous devez l’activer pour tous les élèves.

L’étape suivante consiste à fournir l’autorisation d’accéder à l’application Learning Manager.

![](assets/permission-set.png)

*Ajouter des autorisations pour accéder à l&#39;application Learning Manager*

Lorsque vous installez le pack, un nouveau jeu d&#39;autorisations est créé, **Utilisateur Adobe Learning Manager**. Accédez au jeu d’autorisations, puis ajoutez les utilisateurs.

Sélectionnez les utilisateurs et attribuez les autorisations en conséquence. Les élèves peuvent désormais accéder à l’application Learning Manager.

Ensuite, sélectionnez un profil, par exemple Profil standard d’un utilisateur, puis cliquez sur le profil. Cliquez sur **[!UICONTROL Modifier]** et dans la section **Paramètres d&#39;application personnalisés**, activez la case à cocher **Adobe Learning Manager**. Cela rend l’application accessible à l’utilisateur.

Dans la section **Paramètres d’onglet personnalisés**, dans la liste déroulante **Page d’accueil de l’élève**, sélectionnez l’option **[!UICONTROL Par défaut sur]**.

Vous devez rendre l’application visible à tous les profils.

Cliquez sur **[!UICONTROL Enregistrer]** pour que les élèves appartenant à tous les profils accèdent à l’application Learning Manager.
