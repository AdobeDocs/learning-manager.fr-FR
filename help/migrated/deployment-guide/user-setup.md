---
jcr-language: en_us
title: Configuration des utilisateurs dans Learning Manager
contentowner: shhivkum
preview: true
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 63%

---



# Configuration des utilisateurs dans Learning Manager

## Utilisateurs internes et externes {#internalandexternalusers}

La gestion des utilisateurs est un aspect important dans tout système de gestion de l’apprentissage (LMS), notamment dans Learning Manager. Learning Manager permet de classer les utilisateurs en tant qu’utilisateurs internes et externes. Les utilisateurs internes sont les utilisateurs d’une organisation ou d’un groupe spécifique. Les utilisateurs d’une entreprise sont généralement des utilisateurs internes. Ces utilisateurs ont des objets d’apprentissage spécifiques avec des échéances données qui sont attribués par leurs responsables ou l’administrateur.

En revanche, les utilisateurs externes sont généralement des utilisateurs provisoires d’un compte Learning Manager spécifique. Ces utilisateurs peuvent accéder à des objets d’apprentissage spécifiques en cliquant sur un lien externe temporaire reçu par e-mail. Les profils d’utilisateurs externes comprennent généralement une date d’expiration. Par exemple, dans une organisation qui effectue des certifications pour Java, tout utilisateur peut se connecter provisoirement pour suivre les cours pertinents, puis tenter la certification. Les cours et les formations en salle de classe s’adressent généralement à des utilisateurs externes et présentent également une capacité limitée.

Lisez ce qui suit pour découvrir comment ajouter des utilisateurs internes et externes dans Learning Manager.

## Configuration des utilisateurs externes {#setupexternalusers}

En tant qu’administrateur, vous pouvez ajouter des utilisateurs externes tels que des employés d’organisations partenaires à votre compte Learning Manager. Pour ajouter des utilisateurs externes :

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
1. Vous pouvez également définir les options suivantes lorsque vous créez un profil externe :

   * **[!UICONTROL ** Ajouter une image **:]** Glissez-déposez l’image souhaitée. Cette image s’affiche sur la page Élève pour les utilisateurs.
   * **[!UICONTROL ** Configuration requise pour la connexion **:]** Spécifiez le nombre de jours pendant lesquels l’utilisateur doit se connecter. Si l’utilisateur externe dépasse cette période de connexion, l’élève ne peut pas accéder à l’objet d’apprentissage ni suivre le cours.
   * **[!UICONTROL ** Domaines autorisés **:]** Spécifiez les domaines séparés par une virgule. Seuls les utilisateurs avec des domaines spécifiques peuvent s’inscrire au compte.
   * **[!UICONTROL ** Vérification de l’adresse e-mail requise **:]** Activez cette case à cocher si vous souhaitez qu’un e-mail de vérification soit envoyé aux utilisateurs



1. Cliquez sur **[!UICONTROL Enregistrer.]**



   ![](assets/set-up-external-users-step7.png)

   Une boîte de dialogue contextuelle indiquant l’URL s’affiche. Vous pouvez copier cette URL et l’envoyer aux utilisateurs externes. Un e-mail contenant cette URL est envoyé à l’utilisateur par défaut.

1. Lorsque vous ajoutez des profils externes, ils s’affichent dans la boîte de dialogue **[!UICONTROL ** Page Utilisateurs externes **(** Administrateur **>** Utilisateurs **>** Externe **).]** La limite de places, la date d’expiration et les exigences de connexion sont également affichées pour ces utilisateurs.
1. Pour modifier les paramètres d’un utilisateur externe à tout moment, cliquez sur le nom d’utilisateur. La boîte de dialogue **[!UICONTROL Modifier l’inscription externe]** s’affiche. Modifiez les paramètres, puis cliquez sur **[!UICONTROL ** Enregistrer **.]**
1. Vous pouvez également renvoyer l’e-mail de bienvenue ou copier l’URL à tout moment en cliquant sur les icônes e-mail/copier l’URL à côté du profil externe.

   ![](assets/set-up-external-users-step10.png)

## Suspension du profil utilisateur externe {#pausetheexternaluserprofile}

Après avoir ajouté un groupe d’utilisateurs externes à Learning Manager, vous pouvez également suspendre le processus d’inscription des utilisateurs externes. Lorsque vous mettez en pause, le processus d&#39;enregistrement des utilisateurs externes est bloqué. Toutefois, ce processus fonctionne uniquement lorsque les utilisateurs ne se sont pas encore enregistrés en acceptant l&#39;invitation.

Pour suspendre les groupes d’utilisateurs externes, cliquez sur **[!UICONTROL **Actions**]**dans le coin supérieur droit de la page et choisissez **[!UICONTROL Pause]**.

## Reprise d’un profil utilisateur externe {#resumeexternaluserprofile}

A tout moment, vous pouvez toujours révoquer le blocage (pause) en sélectionnant une option reprendre. Cliquez sur **[!UICONTROL **Actions**]** dans le coin supérieur droit de la page et choisissez **[!UICONTROL Reprendre]**.

**[!UICONTROL États d&#39;utilisateur externe]** 

Dans Learning Manager, les états suivants s’appliquent aux utilisateurs externes :

* **État inactif** - Dans ce cas, l’enregistrement des utilisateurs externes a expiré. Les administrateurs définissent la date d’expiration pour les utilisateurs externes lorsqu’ils les ajoutent au flux de production d’ajout de l’utilisateur.
* **État actif** - Dans cet état, les utilisateurs externes peuvent s’enregistrer dans l’application Learning Manager, mais aussi se connecter à l’application.
* **Suspension :** dans cet état, le processus d’enregistrement des utilisateurs externes est bloqué. Toutefois, les utilisateurs existants peuvent toujours se connecter.

## Configuration des utilisateurs internes {#setupinternalusers}

En tant qu’administrateur, vous pouvez configurer des utilisateurs pour votre entreprise ou organisation. Ces utilisateurs sont également appelés utilisateurs internes. Les utilisateurs internes peuvent se connecter à l’application via l’authentification unique ou leur identifiant Adobe ID. Ces utilisateurs peuvent ensuite accéder aux objets d’apprentissage et les suivre selon leurs besoins. Il existe trois manières de configurer des utilisateurs internes pour une organisation :

* Ajout d’utilisateurs en bloc à l’aide d’un fichier CSV
* Ajout d’utilisateurs via l’auto-inscription
* Ajout d’un utilisateur interne unique



## Ajout d’utilisateurs à l’aide d’un fichier CSV {#addingusersusingacsvfile}

Cette méthode permet d’ajouter des utilisateurs internes si le nombre d’utilisateurs est important. Lorsque vous utilisez un fichier CSV pour ajouter des utilisateurs pour la première fois, vous devez mapper le contenu des données CSV aux libellés de l’application. Lorsque vous ajoutez de nouveaux utilisateurs ou mettez à jour les données utilisateur ultérieurement, le même mappage est conservé. Pour ajouter des utilisateurs internes en bloc :

1. Sur la **[!UICONTROL Accueil de l’administrateur]** page, cliquez sur **[!UICONTROL **Utilisateurs**]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL ** Ajouter **>** Chargement d’un fichier CSV **.]**
1. Dans la boîte de dialogue contextuelle, cliquez sur **[!UICONTROL ** Importer **.]**
1. Accédez à l’emplacement où vous avez enregistré votre fichier CSV. Cliquez sur **[!UICONTROL Ouvrir]**.
1. Importez le fichier CSV et mappez son contenu avec les libellés de l’application. Cette étape s’applique uniquement lorsque vous chargez le fichier CSV pour la première fois.
1. Cliquez sur **[!UICONTROL **Enregistrer**]**pour enregistrer le mappage.
1. Cliquez sur **[!UICONTROL **Ajouter**]**pour télécharger le fichier CSV déjà mappé aux données de l’application.

### Considérations à prendre en compte lors de la création du fichier CSV pour le chargement : {#considerationswhencreatingthecsvfileforupload}

Lorsque vous créez le fichier CSV pour charger des utilisateurs internes, voici certains des champs obligatoires pour lesquels vous devez saisir des données : Nom de l’employé, Adresse électronique de l’employé, Profil ou désignation de l’employé et Hiérarchie du responsable.

Le nom et l’adresse e-mail de chaque employé peuvent être mappés directement aux données de l’application. Notez que vous devez indiquer en tant qu’adresse e-mail du responsable une adresse e-mail qui est spécifiée dans le fichier CSV. Vous pouvez définir l’ID du responsable lors de la création du fichier CSV ou indiquer l’ID de messagerie qui correspond à l’ID du responsable lors du chargement du fichier CSV.

***Avant d’ajouter un ID en tant qu’ID de responsable d’un employé, assurez-vous que le responsable est ajouté en tant qu’employé dans le fichier CSV.***

***Assurez-vous qu’il n’y a pas d’espace supplémentaire entre les entrées pour télécharger le fichier CSV avec succès.***

Consultez un exemple de capture d’écran d’un fichier CSV ici :

![](assets/considerations-whencreatingthecsvfileforupload.png)

Pour télécharger un exemple de fichier CSV, téléchargez `<give link to zip file>`.

<!--Zip file reference, no source file-->

### Configuration de l’utilisateur racine {#settinguprootuser}

Automatisation de l’importation en bloc d’utilisateurs.

## Ajout d’utilisateurs via l’auto-inscription {#addingusersthroughselfregistration}

Outre l’ajout d’utilisateurs internes en bloc, vous pouvez ajouter des utilisateurs par auto-inscription. L’auto-inscription permet aux employés de s’inscrire eux-mêmes en tant qu’élèves à votre compte Learning Manager. Lorsque vous créez un profil d’auto-inscription, une URL unique est créée. Partagez cette URL avec l’employé pour lui permettre de s’inscrire à Learning Manager.

1. Sur la page **[!UICONTROL d’accueil de l’administrateur]**, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL ** Ajouter **>** Auto-inscription **.]**

   ![](assets/adding-users-throughself-registration-step2.png)

1. Dans la boîte de dialogue contextuelle **[!UICONTROL Ajouter un utilisateur]**, indiquez le nom de l’employé dans le champ **[!UICONTROL Nom du profil]**.
1. Dans le panneau **[!UICONTROL Nom du responsable]** saisissez le nom du responsable de l&#39;employé.
1. Vous pouvez éventuellement ajouter la photo de profil de l’employé à l’aide du champ **[!UICONTROL Ajouter une image]**.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/adding-users-throughself-registration-step6.png)

   Le système affiche une autre boîte de dialogue contextuelle indiquant que le profil a été créé avec succès. Une URL unique est également générée dans cette boîte de dialogue.

1. Partagez cette URL avec l’employé pour lui permettre de s’inscrire en tant qu’élève.

   ![](assets/adding-users-throughself-registration-step7.png)

## Ajout d’utilisateurs uniques dans Learning Manager {#addsingleusersincaptivateprime}

L’ajout d’utilisateurs uniques est la troisième méthode permettant d’ajouter des utilisateurs internes à votre compte. Cette procédure est idéale si vous souhaitez ajouter quelques utilisateurs. Pour ajouter un utilisateur unique :

1. Sur la page **[!UICONTROL d’accueil de l’administrateur]**, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de navigation de gauche.
1. Cliquez sur **[!UICONTROL ** Ajouter **>** Utilisateur unique **.]**



1. Dans la boîte de dialogue contextuelle Ajouter un utilisateur, indiquez les détails suivants pour les utilisateurs :

   * **[!UICONTROL Nom]** **[!UICONTROL :]** Spécifiez le nom de l&#39;employé ou de l&#39;utilisateur interne. Ce champ est obligatoire.

   * **[!UICONTROL E-mail]** **[!UICONTROL :]** Indiquez l’ID de messagerie de l’employé. Ce champ est obligatoire.

   * **[!UICONTROL Profil]** **[!UICONTROL :]** Indiquez la désignation ou la fonction de l&#39;employé.

   * **[!UICONTROL ** Nom du responsable **:]** Spécifiez le nom du responsable. Le responsable doit déjà être ajouté dans la base de données spécifiée ici.
   * **[!UICONTROL ** DOJ **:]** Indiquez la date d&#39;embauche de l&#39;employé.
   * **[!UICONTROL **Emplacement**:]**Indiquez l&#39;emplacement de l&#39;employé. Par exemple, si votre organisation compte plusieurs sites géographiques, spécifiez le site de l’employé.



   ![](assets/add-single-usersincaptivateprime-step3.png)

1. Cliquez sur **[!UICONTROL Ajouter]**.
1. Le système affiche un message indiquant que l’utilisateur a été ajouté avec succès. L’utilisateur reçoit un lien de vérification dans l’ID de messagerie spécifié. L’utilisateur peut cliquer sur ce lien pour activer son compte et accéder à Learning Manager.

   ![](assets/add-single-usersincaptivateprime-step5.png)

## Gestion des groupes d’utilisateurs dans Learning Manager {#managingusergroupsincaptivateprime}

Le groupe d’utilisateurs n’est rien d’autre qu’un ensemble d’utilisateurs appartenant à une catégorie définie. En tant qu&#39;administrateur, vous pouvez utiliser des groupes d&#39;utilisateurs pour sélectionner rapidement des élèves en fonction de leurs attributs. En outre, vous pouvez attribuer rapidement des logos ou des catalogues au groupe d’utilisateurs et générer des rapports personnalisés sur leur progression.

Il existe deux types de groupes d’utilisateurs dans Learning Manager : Personnalisé et Généré automatiquement. Lorsque vous ajoutez des élèves à votre compte, certains groupes par défaut sont automatiquement créés en fonction des rôles et des propriétés des utilisateurs de votre compte. Ces groupes sont générés automatiquement. Par exemple, un groupe comprenant tous les élèves ou tous les auteurs.

***Vous ne pouvez pas modifier le nom et la description des groupes générés automatiquement.***

Pour afficher les groupes d’utilisateurs générés automatiquement dans Learning Manager, dans le volet de gauche, cliquez sur **[!UICONTROL Généré automatiquement]**. L’application affiche une liste de tous les groupes d’utilisateurs générés automatiquement qui sont disponibles pour votre compte.

Vous pouvez également créer des groupes personnalisés avec une liste sélectionnée d’utilisateurs dans Learning Manager. Les groupes personnalisés vous permettent de spécifier un nom, une description et les attributs du groupe d’utilisateurs. Les groupes personnalisés que vous créez dans Learning Manager sont dynamiques par nature. En d’autres termes, si de nouveaux utilisateurs sont ajoutés avec des attributs similaires, ils sont automatiquement ajoutés à ces groupes d’utilisateurs.

## Création de groupes d’utilisateurs personnalisés {#createcustomusergroups}

1. Dans la page d’accueil de l’administrateur Learning Manager, cliquez sur **[!UICONTROL Utilisateurs]**.
1. Dans la page Groupes d’utilisateurs personnalisés, cliquez sur **[!UICONTROL **Ajouter**]**dans le coin supérieur droit de la page.

   Le système affiche la boîte de dialogue **[!UICONTROL Ajouter un groupe d’utilisateurs]**.

   ![](assets/creating-custom-usergroups.png)

1. Indiquez le nom et la description de votre groupe d’utilisateurs. Le groupe Dev-Users inclut par exemple les utilisateurs de l’équipe de développement du produit.
1. Ajoutez des utilisateurs au groupe d’utilisateurs personnalisé en saisissant le nom d’utilisateur ou le profil de l’utilisateur dans le champ **[!UICONTROL ** Ajouter des utilisateurs **champ.]**
1. Pour ajouter d’autres utilisateurs au groupe personnalisé, cliquez sur **[!UICONTROL ** Ajouter plus d’utilisateurs **.]**
1. Après avoir ajouté tous les utilisateurs, cliquez sur **[!UICONTROL Enregistrer]**pour enregistrer le groupe d’utilisateurs personnalisé.

