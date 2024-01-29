---
jcr-language: en_us
title: Configuration des utilisateurs dans Learning Manager
contentowner: shhivkum
preview: true
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 0%

---



# Configuration des utilisateurs dans Learning Manager

## Utilisateurs internes et externes {#internalandexternalusers}

Dans tout système de gestion de l’apprentissage (LMS), y compris Learning Manager, la gestion des utilisateurs est un aspect important. Learning Manager vous permet de classer les utilisateurs en tant qu’utilisateurs internes et externes. Les utilisateurs internes sont les utilisateurs qui appartiennent à une organisation spécifique ou à un groupe. En règle générale, les utilisateurs d’une entreprise sont des utilisateurs internes. Ces utilisateurs ont des objets d’apprentissage spécifiques avec des échéances spécifiques, attribués par leurs responsables ou l’administrateur.

En revanche, les utilisateurs externes sont généralement des utilisateurs temporaires d’un compte Learning Manager spécifique. Ces utilisateurs peuvent accéder à des objets d’apprentissage spécifiques en cliquant sur un lien externe temporaire qu’ils reçoivent par e-mail. Les profils d’utilisateurs externes ont généralement une date d’expiration. Par exemple, une organisation qui effectue des certifications pour Java peut avoir n’importe quel utilisateur qui se connecte temporairement pour terminer les cours pertinents, puis tente la certification. Généralement, les formations en salle de classe et les cours destinés à des utilisateurs externes ont également une capacité limitée.

Lisez ce qui suit pour savoir comment ajouter des utilisateurs internes et des utilisateurs externes dans Learning Manager.

## Configuration d’utilisateurs externes {#setupexternalusers}

En tant qu’administrateur, vous pouvez ajouter des utilisateurs externes tels que des employés d’organisations partenaires à votre compte Learning Manager. Pour ajouter des utilisateurs externes :

1. À partir du **[!UICONTROL **Administrateur**]**page de connexion, cliquez sur **[!UICONTROL **Utilisateurs**]** dans le volet de navigation de gauche.
1. Dans le **[!UICONTROL **Utilisateurs**]**page, cliquez sur **[!UICONTROL **Externe**]** dans le volet de navigation de gauche. Le système affiche la page Utilisateurs externes avec une liste d’utilisateurs externes (le cas échéant).
1. Cliquez sur **[!UICONTROL **Ajouter**]** dans le coin supérieur droit de la page.

   ![](assets/set-up-external-users-step3.png)

1. Dans le **[!UICONTROL **Ajouter un utilisateur**]**boîte de dialogue contextuelle, les champs suivants sont obligatoires :

   * **[!UICONTROL **Nom du profil**:]**Spécifiez le nom du profil externe que vous créez.
   * **[!UICONTROL ** Adresse e-mail du responsable **:]** Spécifiez l’adresse e-mail du responsable pour l’utilisateur externe.
   * **[!UICONTROL ** Places attribuées **:]** Spécifiez le nombre d’élèves qui peuvent s’inscrire au cours.
   * **[!UICONTROL ** Expiration **:]** Spécifiez la date d&#39;expiration après laquelle un utilisateur externe ne peut plus enregistrer ou suivre le cours.

1. Cliquez sur **[!UICONTROL ** Paramètres avancés **.]**
1. Le cas échéant, définissez les options suivantes lors de la création d’un profil externe :

   * **[!UICONTROL ** Ajouter une image **:]** Glissez-déposez l’image souhaitée. Cette image s’affiche sur la page Élève pour les utilisateurs.
   * **[!UICONTROL ** Configuration requise pour la connexion **:]** Spécifiez le nombre de jours pendant lesquels l’utilisateur doit se connecter. Si l’utilisateur externe dépasse cette période de connexion, l’élève ne peut pas accéder à l’objet d’apprentissage ni l’utiliser.
   * **[!UICONTROL ** Domaines autorisés **:]** Spécifiez les domaines séparés par une virgule. Seuls les utilisateurs disposant des domaines spécifiés peuvent s’inscrire au compte.
   * **[!UICONTROL ** Vérification de l’adresse e-mail requise **:]** Activez cette case à cocher si vous souhaitez qu’un e-mail de vérification soit envoyé aux utilisateurs



1. Cliquez sur **[!UICONTROL Enregistrer.]**



   ![](assets/set-up-external-users-step7.png)

   Une boîte de dialogue contextuelle contenant l’URL s’affiche. Vous pouvez copier cette URL et l’envoyer aux utilisateurs externes. Par défaut, un e-mail avec cette URL est envoyé à l’utilisateur.

1. Lorsque vous ajoutez des profils externes, ils s’affichent dans la boîte de dialogue **[!UICONTROL ** Page Utilisateurs externes **(** Administrateur **>** Utilisateurs **>** Externe **).]** La limite de places, la date d’expiration et les exigences de connexion sont également affichées pour ces utilisateurs.
1. Pour modifier les paramètres d’un utilisateur externe à tout moment, cliquez sur son nom d’utilisateur. Le **[!UICONTROL Modifier l&#39;inscription externe]** s’affiche. Modifiez les paramètres, puis cliquez sur **[!UICONTROL ** Enregistrer **.]**
1. Vous pouvez également renvoyer l’e-mail de bienvenue ou copier l’URL à tout moment en cliquant sur les icônes d’e-mail/de copie d’URL en regard du profil externe.

   ![](assets/set-up-external-users-step10.png)

## Suspendre le profil de l’utilisateur externe {#pausetheexternaluserprofile}

Après avoir ajouté un groupe d’utilisateurs externes à Learning Manager, vous pouvez également suspendre le processus d’inscription des utilisateurs externes. Lorsque vous interrompez, le processus d’enregistrement des utilisateurs externes est bloqué. Cependant, ce processus ne fonctionne que lorsque les utilisateurs ne se sont pas encore inscrits en acceptant l’invitation.

Pour suspendre les groupes d’utilisateurs externes, cliquez sur **[!UICONTROL **Actions**]**dans le coin supérieur droit de la page et choisissez **[!UICONTROL Pause]**.

## Reprendre le profil utilisateur externe {#resumeexternaluserprofile}

À tout moment, vous pouvez toujours révoquer le blocage (pause) en choisissant une option de reprise. Cliquez sur **[!UICONTROL **Actions**]** dans le coin supérieur droit de la page et choisissez **[!UICONTROL Reprendre]**.

**[!UICONTROL États des utilisateurs externes]**

Dans Learning Manager, les états suivants s’appliquent aux utilisateurs externes :

* **État inactif** - Dans ce cas, l’enregistrement des utilisateurs externes a expiré. Les administrateurs définissent la date d’expiration pour les utilisateurs externes lors de leur ajout via le workflow d’ajout d’utilisateurs.
* **État actif** - Dans cet état, les utilisateurs externes peuvent s’enregistrer dans l’application Learning Manager, mais aussi se connecter à l’application.
* **Pause** - Dans cet état, le processus d’enregistrement des utilisateurs externes est bloqué. Cependant, les utilisateurs existants peuvent continuer à se connecter.

## Configuration des utilisateurs internes {#setupinternalusers}

En tant qu’administrateur, vous pouvez configurer des utilisateurs pour votre entreprise ou organisation. Ces utilisateurs sont également appelés utilisateurs internes. Les utilisateurs internes peuvent se connecter à l’application à l’aide de l’authentification unique ou d’Adobe ID. Ces utilisateurs peuvent ensuite accéder aux objets d’apprentissage et les utiliser selon leurs besoins. Pour configurer des utilisateurs internes pour une organisation, il existe trois façons possibles :

* Ajout d’utilisateurs par lot à l’aide d’un fichier CSV
* Ajout d’utilisateurs via l’auto-inscription
* Ajout d’un utilisateur interne unique



## Ajout d’utilisateurs à l’aide d’un fichier CSV {#addingusersusingacsvfile}

Vous pouvez choisir cette méthode pour ajouter des utilisateurs internes si le nombre d’utilisateurs est important. Lorsque vous utilisez un fichier CSV pour ajouter des utilisateurs pour la première fois, vous devez mapper le contenu des données CSV aux étiquettes de l’application. Par la suite, lorsque vous ajoutez de nouveaux utilisateurs ou mettez à jour les données utilisateur, le même mappage est conservé. Pour ajouter des utilisateurs internes en bloc :

1. Sur la **[!UICONTROL Accueil de l’administrateur]** page, cliquez sur **[!UICONTROL **Utilisateurs**]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL ** Ajouter **>** Chargement d’un fichier CSV **.]**
1. Dans la boîte de dialogue contextuelle, cliquez sur **[!UICONTROL ** Importer **.]**
1. Accédez à l’emplacement où vous avez enregistré votre fichier CSV. Cliquez sur **[!UICONTROL Ouvrir]**.
1. Importez le fichier CSV et mappez son contenu avec les libellés de l’application. Cette étape s’applique uniquement lorsque vous chargez le fichier CSV pour la première fois.
1. Cliquez sur **[!UICONTROL **Enregistrer**]**pour enregistrer le mappage.
1. Cliquez sur **[!UICONTROL **Ajouter**]**pour télécharger le fichier CSV déjà mappé aux données de l’application.

### Considérations à prendre en compte lors de la création du fichier CSV pour le téléchargement : {#considerationswhencreatingthecsvfileforupload}

Lorsque vous créez le fichier CSV pour charger des utilisateurs internes, voici certains des champs obligatoires pour lesquels vous devez saisir des données : Nom de l’employé, Adresse électronique de l’employé, Profil ou désignation de l’employé et Hiérarchie du responsable.

Le nom et l’adresse e-mail de chaque employé peuvent être mappés directement aux données de l’application. Notez que vous devez spécifier un e-mail qui est spécifié dans le fichier CSV, en tant qu’e-mail du responsable. Vous pouvez soit définir l’ID du responsable lors de la création du fichier CSV, soit spécifier l’ID de messagerie qui correspond à l’ID du responsable lors du téléchargement du fichier CSV.

***Avant d’ajouter un ID en tant qu’ID de responsable d’un employé, assurez-vous que le responsable est ajouté en tant qu’employé dans le fichier CSV.***

***Assurez-vous qu’il n’y a pas d’espace supplémentaire entre les entrées pour télécharger le fichier CSV avec succès.***

Consultez un exemple d’instantané d’un fichier CSV ici :

![](assets/considerations-whencreatingthecsvfileforupload.png)

Pour télécharger un exemple de fichier CSV, téléchargez `<give link to zip file>`.

<!--Zip file reference, no source file-->

### Configuration de l’utilisateur racine {#settinguprootuser}

Automatisation de l’importation en bloc d’utilisateurs.

## Ajout d’utilisateurs via l’auto-inscription {#addingusersthroughselfregistration}

Outre l’ajout d’utilisateurs internes en bloc, vous pouvez également ajouter des utilisateurs par auto-inscription. Vous pouvez utiliser l’auto-inscription pour permettre aux employés de s’inscrire en tant qu’élèves à votre compte Learning Manager. Lorsque vous créez un profil d’auto-inscription, une URL unique est créée. Partagez cette URL avec l’employé pour lui permettre de s’inscrire dans Learning Manager.

1. Sur la **[!UICONTROL Accueil de l’administrateur]** page, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL ** Ajouter **>** Auto-inscription **.]**

   ![](assets/adding-users-throughself-registration-step2.png)

1. Dans le panneau **[!UICONTROL Ajouter un utilisateur]** dans la boîte de dialogue contextuelle, spécifiez le nom de l&#39;employé dans le champ **[!UICONTROL Nom du profil]** champ.
1. Dans le panneau **[!UICONTROL Nom du responsable]** saisissez le nom du responsable de l&#39;employé.
1. Vous pouvez éventuellement ajouter la photo de profil de l&#39;employé à l&#39;aide de la boîte de dialogue **[!UICONTROL Ajouter une image]** champ.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/adding-users-throughself-registration-step6.png)

   Le système affiche une autre boîte de dialogue contextuelle avec un message indiquant que le profil a été créé avec succès. Cette boîte de dialogue génère également une URL unique.

1. Partagez cette URL avec l’employé pour lui permettre de s’inscrire en tant qu’élève.

   ![](assets/adding-users-throughself-registration-step7.png)

## Ajout d’utilisateurs uniques dans Learning Manager {#addsingleusersincaptivateprime}

L’ajout d’utilisateurs uniques est la troisième méthode par laquelle vous pouvez ajouter des utilisateurs internes à votre compte. Lorsque vous souhaitez ajouter quelques utilisateurs, cette procédure est idéale. Pour ajouter un seul utilisateur :

1. Sur la **[!UICONTROL Accueil de l’administrateur]** page, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL ** Ajouter **>** Utilisateur unique **.]**



1. Dans la boîte de dialogue contextuelle Ajouter un utilisateur, spécifiez les détails suivants pour les utilisateurs :

   * **[!UICONTROL Nom]** **[!UICONTROL :]** Spécifiez le nom de l&#39;employé ou de l&#39;utilisateur interne. Ce champ est obligatoire.

   * **[!UICONTROL E-mail]** **[!UICONTROL :]** Indiquez l’ID de messagerie de l’employé. Ce champ est obligatoire.

   * **[!UICONTROL Profil]** **[!UICONTROL :]** Indiquez la désignation ou la fonction de l&#39;employé.

   * **[!UICONTROL ** Nom du responsable **:]** Spécifiez le nom du responsable. Le responsable doit déjà être ajouté dans la base de données à spécifier ici.
   * **[!UICONTROL ** DOJ **:]** Indiquez la date d&#39;embauche de l&#39;employé.
   * **[!UICONTROL **Emplacement**:]**Indiquez l&#39;emplacement de l&#39;employé. Par exemple, si votre organisation se trouve dans plusieurs lieux géographiques, spécifiez le lieu où se trouve l&#39;employé.



   ![](assets/add-single-usersincaptivateprime-step3.png)

1. Cliquez sur **[!UICONTROL Ajouter]**.
1. Le système affiche un message indiquant que l’utilisateur a été ajouté avec succès. L’utilisateur reçoit un lien de vérification dans l’ID de messagerie spécifié. L’utilisateur peut cliquer sur ce lien pour activer son compte et commencer à accéder à Learning Manager.

   ![](assets/add-single-usersincaptivateprime-step5.png)

## Gestion des groupes d’utilisateurs dans Learning Manager {#managingusergroupsincaptivateprime}

Le groupe d’utilisateurs n’est rien d’autre qu’un ensemble d’utilisateurs appartenant à une catégorie définie. En tant qu&#39;administrateur, vous pouvez utiliser des groupes d&#39;utilisateurs pour sélectionner rapidement des élèves en fonction de leurs attributs. En outre, vous pouvez attribuer rapidement des logos ou des catalogues au groupe d’utilisateurs et générer des rapports personnalisés sur leur progression.

Il existe deux types de groupes d’utilisateurs dans Learning Manager : Personnalisé et Généré automatiquement. Lorsque vous ajoutez des élèves à votre compte, certains groupes par défaut sont automatiquement créés en fonction des rôles et des propriétés des utilisateurs de votre compte. Ces groupes sont générés automatiquement. Par exemple, un groupe avec tous les élèves ou tous les auteurs.

***Vous ne pouvez pas modifier le nom et la description des groupes générés automatiquement.***

Pour afficher les groupes d’utilisateurs générés automatiquement dans Learning Manager, dans le volet de gauche, cliquez sur **[!UICONTROL Généré automatiquement]**. L’application affiche une liste de tous les groupes d’utilisateurs générés automatiquement qui sont disponibles pour votre compte.

Vous pouvez également créer des groupes personnalisés avec une liste sélectionnée d’utilisateurs dans Learning Manager. Les groupes personnalisés vous permettent de spécifier un nom, une description et les attributs du groupe d’utilisateurs. Les groupes personnalisés que vous créez dans Learning Manager sont dynamiques par nature. En d’autres termes, si de nouveaux utilisateurs sont ajoutés avec des attributs similaires, ils sont automatiquement ajoutés à ces groupes d’utilisateurs.

## Création de groupes d’utilisateurs personnalisés {#createcustomusergroups}

1. Dans la page d’accueil de l’administrateur Learning Manager, cliquez sur **[!UICONTROL Utilisateurs]**.
1. Dans la page Groupes d’utilisateurs personnalisés, cliquez sur **[!UICONTROL **Ajouter**]**dans le coin supérieur droit de la page.

   Le système affiche le **[!UICONTROL Ajouter un groupe d’utilisateurs]** boîte de dialogue.

   ![](assets/creating-custom-usergroups.png)

1. Spécifiez le nom et la description de votre groupe d’utilisateurs. Par exemple, Dev-Users qui inclut des utilisateurs de l’équipe de développement du produit.
1. Ajoutez des utilisateurs au groupe d’utilisateurs personnalisé en saisissant le nom d’utilisateur ou le profil de l’utilisateur dans le champ **[!UICONTROL ** Ajouter des utilisateurs **champ.]**
1. Pour ajouter d’autres utilisateurs au groupe personnalisé, cliquez sur **[!UICONTROL ** Ajouter plus d’utilisateurs **.]**
1. Après avoir ajouté tous les utilisateurs, cliquez sur **[!UICONTROL Enregistrer]**pour enregistrer le groupe d’utilisateurs personnalisé.

