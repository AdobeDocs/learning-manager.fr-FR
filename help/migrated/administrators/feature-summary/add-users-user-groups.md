---
description: Découvrez comment ajouter des utilisateurs ou des groupes d’utilisateurs dans l’application Learning Manager.
jcr-language: en_us
title: Ajout d’utilisateurs et création de groupes d’utilisateurs
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3913'
ht-degree: 0%

---



# Ajout d’utilisateurs et création de groupes d’utilisateurs

Découvrez comment ajouter des utilisateurs ou des groupes d’utilisateurs dans l’application Learning Manager.

<!--![](assets/user-mgmt-new.png)-->

## Présentation {#overview}

Dans Adobe Learning Manager, vous pouvez assumer les rôles suivants :

* **Administrateur :** Un administrateur définit la stratégie de formation pour l’organisation. Un administrateur peut ajouter des élèves, rechercher les compétences requises pour les élèves, gérer et affecter des cours, créer des plans d&#39;apprentissage, des certifications et des programmes d&#39;apprentissage, et gérer des rapports pour l&#39;ensemble de l&#39;organisation.
* **Auteur :** Les auteurs sont des concepteurs pédagogiques et des créateurs de contenu. Un auteur peut ajouter des modules et des cours à Learning Manager.
* **Responsable :** Un responsable gère les activités d’apprentissage d’une équipe. Un responsable peut désigner des membres de l’équipe pour suivre un cours, approuver les demandes des membres de l’équipe et fournir un retour d’informations sur les performances des membres de leur équipe après la fin de la formation. Les responsables peuvent également afficher des rapports pour leur équipe afin de suivre leurs performances.
* **Élève :** Les élèves peuvent accéder aux cours, aux programmes d’apprentissage et aux certifications qui leur sont attribués. Les élèves peuvent également parcourir tous les cours disponibles à l&#39;aide d&#39;un catalogue et s&#39;inscrire eux-mêmes à des cours, des programmes d&#39;apprentissage ou des certifications.

En tant qu’administrateur, vous pouvez ajouter des utilisateurs de trois façons :

* Interne
* Externe
* Groupes d’utilisateurs

## Ajouter un seul utilisateur {#addasingleuser}

Pour ajouter des utilisateurs,

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
1. Sur la page d’accueil, cliquez sur **[!UICONTROL Ajouter des utilisateurs]**. Sur cette page, vous pouvez ajouter un ou plusieurs utilisateurs à la fois à l’aide d’un fichier CSV. Vous pouvez également créer un lien d&#39;auto-inscription pour les employés internes ou créer un profil d&#39;élève externe.
1. Pour ajouter un seul utilisateur, cliquez sur **[!UICONTROL Ajouter]** dans le coin supérieur droit et sélectionnez l’option **[!UICONTROL Utilisateur unique]**.

   ![](assets/single-user.png)
   *Ajout d’un utilisateur interne unique*

1. Sur la **[!UICONTROL Ajouter un utilisateur]** , saisissez les détails de l’élève. Pour le champ **[!UICONTROL Nom du responsable]**, sélectionnez le nom d’un utilisateur existant dans le système.

   ![](assets/manager.png)
   *Boîte de dialogue Ajouter un utilisateur*

1. Pour ajouter le nouvel utilisateur dans Learning Manager, cliquez sur **[!UICONTROL Ajouter]**. Une fois l’utilisateur ajouté, il reçoit un e-mail de vérification. L’élève active ensuite le compte et commence à utiliser Learning Manager. Ce workflow est utile si vous devez ajouter un nombre limité d’élèves à votre compte Learning Manager. Mais si vous prévoyez d&#39;inscrire tous les employés d&#39;une grande organisation, vous pouvez les ajouter en une seule tentative. Pour plus d’informations, voir la section suivante.

## Ajout d’utilisateurs par lot {#addusersinbulk}

En règle générale, la plupart des organisations utilisent un système de gestion des ressources humaines (HRMS), qui conserve tous les enregistrements des employés, tels que la désignation, l&#39;emplacement, la date de l&#39;intégration ou la hiérarchie des employés. Vous pouvez exporter ces données au format CSV. Pour importer un fichier CSV, procédez comme suit :

1. Cliquez sur **[!UICONTROL Ajouter]** dans le coin supérieur droit, puis sélectionnez l’option **[!UICONTROL Chargement d’un fichier CSV]**.

   ![](assets/upload-a-csv.png)
   *Chargement d’un fichier CSV pour ajouter des utilisateurs en bloc*

1. Le fichier CSV que vous chargez se compose des champs, comme indiqué ci-dessous :

   ![](assets/csv.png)
   *Structure du fichier CSV*

   Vous devez gérer un fichier CSV maître et effectuer tous les ajouts et suppressions sur le fichier CSV maître. Le fichier CSV maître contient les champs suivants :

   * nom &#42;
   * e-mail &#42;
   * profil
   * manager

   (&#42;) Champ obligatoire.

1. Après avoir cliqué sur l’option **[!UICONTROL Chargement d’un fichier CSV]**, la boîte de dialogue suivante s’affiche.

   ![](assets/upload-a-csv-dialog.png)
   *Boîte de dialogue Charger un fichier CSV*

1. Choisissez le fichier CSV ou faites-le glisser. Après avoir choisi le fichier, mappez les champs de données avec ceux du fichier CSV. Cliquez sur la liste déroulante requise et choisissez le champ approprié.

   ![](assets/map-data-fields.png)
   *Champs de mappage dans le fichier CSV*

1. Pour commencer à importer les utilisateurs, cliquez sur **[!UICONTROL Enregistrer]**. Un message de confirmation s’affiche.

   ![](assets/save-csv.png)
   *Message de confirmation indiquant que le chargement du fichier CSV a réussi*

1. Les nouveaux utilisateurs sont maintenant ajoutés à votre compte Learning Manager d’Adobe. Pour sélectionner les nouveaux utilisateurs, cochez la case en regard des noms afin que tout le monde soit sélectionné.

   ![](assets/select-new-users.png)
   *Nouveaux utilisateurs ajoutés*

>[!NOTE]
>
>Pour plus d’informations, voir la FAQ, [Ajout d’utilisateurs par lot](../add-users-in-bulk.md).

Après avoir sélectionné les utilisateurs, vous pouvez effectuer les opérations suivantes :

## Enregistrement d’un utilisateur {#registerauser}

L’utilisateur étant sélectionné, cliquez sur **[!UICONTROL Actions]** dans le coin supérieur droit et cliquez sur **[!UICONTROL S&#39;inscrire]**.

Les utilisateurs sélectionnés reçoivent un e-mail de bienvenue. Si les élèves ont déjà un Adobe ID, ils peuvent cliquer sur ce lien. S’ils n’ont pas d’Adobe ID existant, ils peuvent cliquer sur le lien Bienvenue pour créer un Adobe ID et le lier à leur compte Learning Manager.

## Attribution d’un rôle {#assignarole}

Après avoir ajouté des élèves au compte Adobe Learning Manager, si vous souhaitez modifier leurs rôles, cliquez sur Actions dans le coin supérieur droit de la page. Choisir l’option **[!UICONTROL Attribuer un rôle]**. Ici, vous pouvez décider de donner un accès d’auteur ou d’administrateur à l’élève. Une fois que vous avez attribué un rôle, cet élève dispose d’un accès d’auteur au compte et peut ajouter des modules et créer des cours.

![](assets/assign-a-role.png)
*Attribution d’un rôle à un utilisateur*

## Supprimer un rôle {#removearole}

Vous pouvez également supprimer l’accès Auteur ou Administrateur pour les utilisateurs. Sélectionnez un ou plusieurs élèves, puis cliquez sur **[!UICONTROL Actions]**, puis sélectionnez **[!UICONTROL Supprimer le rôle]**. Choisissez une option, par exemple : **[!UICONTROL Supprimer l’auteur]**, et l’accès d’auteur est révoqué pour cet élève.

>[!NOTE]
>
>Vous ne pouvez pas attribuer manuellement un rôle de responsable à une personne du système. Ils ont automatiquement accès au tableau de bord du responsable lorsqu’un ou plusieurs employés y sont ajoutés.

## Suppression d’un utilisateur {#deleteauser}

Pour supprimer un utilisateur, cliquez **[!UICONTROL Actions]**, puis choisissez **[!UICONTROL Supprimer l’utilisateur]**. Dans la boîte de dialogue de confirmation, cliquez sur **[!UICONTROL Oui]**, et l’élève est supprimé.

![](assets/delete-a-role.png)
*Message de confirmation pour supprimer un utilisateur*

## Modification d’un utilisateur {#editauser}

Dans la liste des utilisateurs, choisissez un utilisateur, puis cliquez sur l’utilisateur. Dans les détails de l’utilisateur, cliquez sur le bouton **[!UICONTROL Modifier]** ( ![](assets/edit-pen.png)). Sur la **[!UICONTROL Modifier l’utilisateur]** , apportez les modifications nécessaires et, pour enregistrer les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

![](assets/edit-user.png)
*Boîte de dialogue Modifier l’utilisateur*

## Workflows pour les champs actifs et les valeurs de champ actif préservant la sensibilité à la casse

Dans cette version, Learning Manager préserve la sensibilité à la casse de l’attribut utilisateur et de sa valeur. **Par exemple**, la sensibilité à la casse d&#39;un attribut utilisateur est &#39;location&#39; et sa valeur &#39;PARIS&#39; sera préservée et affichée de la même manière. En cas de problème, l’administrateur peut désormais modifier le nom et les valeurs de l’attribut pour corriger toute erreur de sensibilité à la casse.

Pour ce faire, l’administrateur peut visiter le site **[!UICONTROL Application d’administration]** > **[!UICONTROL Utilisateurs]** > **[!UICONTROL Groupes d’utilisateurs]** et en cliquant sur le nom du groupe.

L’administrateur peut ajouter et mettre à jour les valeurs d’attribut autorisées pour un élève via l’interface utilisateur.

Types de champs actifs :

* Regroupable : les élèves sont regroupés sur la base des valeurs.
* Reportable : les groupes d’utilisateurs de rapport sont créés en fonction des champs actifs.
* Exportable : les champs seront affichés dans le rapport de groupe d’utilisateurs exporté.

## Création d’un lien d’auto-inscription {#createaselfregistrationlink}

Vous pouvez également permettre aux employés de votre organisation de s’inscrire en tant qu’élèves dans l’Adobe du compte Learning Manager, sans nécessiter votre aide en tant qu’administrateur. L’administrateur peut créer un lien d’auto-inscription et le partager avec les employés, qui peuvent ensuite s’inscrire à Learning Manager à l’aide de leurs identifiants d’Adobe.

Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Ajouter]**, puis choisissez **[!UICONTROL Auto-inscription]**.

![](assets/self-registration.png)
*Créer un lien pour s’inscrire automatiquement en tant qu’élève*

Le **[!UICONTROL Ajouter un profil d&#39;auto-inscription]** s’affiche. Nommez ce profil. Ajoutez ensuite le nom du responsable. Il est important de savoir que le responsable doit déjà être un élève inscrit dans Learning Manager.

![](assets/add-self-registrationprofile.png)
*Ajouter un profil pour l’auto-inscription*

Après avoir cliqué **[!UICONTROL Enregistrer]**, une URL est générée, que vous pouvez partager avec les élèves, afin qu’ils puissent cliquer sur l’URL et s’inscrire eux-mêmes.

## Inscription d’élèves externes {#enrollexternallearners}

Dans Adobe Learning Manager, vous pouvez également créer des liens d’inscription pour les partenaires externes ou les agences ayant un accès limité à votre compte et leur fournir du matériel d’apprentissage.

Il existe quelques différences entre les enregistrements internes et externes.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Utilisateurs internes</b></p></td>
   <td>
    <p><b>Utilisateurs externes</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Connectez-vous à l’aide des informations d’identification Adobe ID ou SSO.</p></td>
   <td>
    <p>Connectez-vous à l’aide de n’importe quel ID de messagerie.</p></td>
  </tr>
  <tr>
   <td>
    <p>La ludification est disponible.</p></td>
   <td>
    <p>La ludification n’est pas disponible.</p></td>
  </tr>
  <tr>
   <td>
    <p>Les hiérarchies d’élèves sont disponibles.</p></td>
   <td>
    <p>Les hiérarchies d’élèves ne sont pas disponibles.</p></td>
  </tr>
 </tbody>
</table>

Pour inscrire des utilisateurs externes, procédez comme suit :

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL Externe]**.

   ![](assets/click-external.png)

   *Inscription d’utilisateurs externes*

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Ajouter]**.
1. Sur la **[!UICONTROL Ajouter un profil d&#39;inscription externe]** , ajoutez les détails suivants :

   * Nom du profil de l’organisation partenaire.
   * Adresse e-mail du responsable de l’organisation partenaire.
   * Limite de places pour l’inscription externe de ce partenaire.
   * Date d’expiration pour définir une date limite afin de ne plus autoriser de nouvelles inscriptions pour ce groupe. Après la date d’expiration, seuls les utilisateurs enregistrés existants peuvent accéder à cette formation.

   ![](assets/map-data-fields-2.png)

   *Boîte de dialogue Ajouter un profil d’inscription externe*

   * Dans le panneau **[!UICONTROL Paramètres avancés]** dans la section, saisissez les informations suivantes :

      * **[!UICONTROL Configuration requise pour la connexion]:** Spécifiez une valeur en jours. Les élèves sont supprimés s’ils ne se connectent pas pendant la durée ci-dessus.
      * **[!UICONTROL Domaines autorisés]:** Liste séparée par des virgules des noms de domaine d’e-mail autorisés.
      * **[!UICONTROL Vérification de l’adresse e-mail requise]:** Sélectionnez cette option pour rendre la vérification par e-mail obligatoire pour un élève.

   ![](assets/email-verificationrequired.png)

   *Saisissez les détails dans la section Paramètres avancés*

1. Après avoir cliqué **[!UICONTROL Enregistrer]**, vous pouvez voir le message de confirmation suivant. Vous devez partager l’URL avec votre partenaire externe.

   ![](assets/save-and-share-urlwithexternalusers.png)

## Activation d’un profil externe {#enableanexternalprofile}

Une fois qu’un profil externe a été créé, vous devez activer son statut. Dans la liste des profils externes, choisissez le profil requis, puis cliquez sur le bouton d’état.

![](assets/choose-required-profiles.png)
*Activation d’un profil externe*

Cela active le lien Inscription externe. Un e-mail de bienvenue est automatiquement envoyé au partenaire. Vous pouvez également copier le lien et le partager avec eux en cliquant sur l’icône Copier l’URL (), ou vous pouvez renvoyer l’e-mail de bienvenue à l’organisation partenaire en cliquant sur l’icône Courrier ().

Le responsable partenaire peut partager le lien avec les employés qui doivent suivre la formation dans PrLearning Manager. Lorsqu’ils cliquent sur le lien, ils peuvent s’inscrire eux-mêmes après avoir renseigné quelques détails pour créer leur profil sur Learning Manager. Ces utilisateurs n’apparaîtront pas dans l’onglet Élèves avec les employés internes. Vous pouvez voir leurs noms sous la rubrique **[!UICONTROL Élèves externes]** onglet.

## Suspendre un profil externe {#pause}

Après avoir ajouté un groupe d’utilisateurs externes à Learning Manager, vous pouvez également suspendre le processus d’inscription des utilisateurs externes. Lorsque vous interrompez, le processus d’inscription des utilisateurs externes est bloqué. Cependant, ce processus ne fonctionne que lorsque les utilisateurs ne se sont pas encore inscrits en acceptant l’invitation.

Pour suspendre les groupes d’utilisateurs externes, choisissez un ou plusieurs groupes, cliquez sur **[!UICONTROL Actions]** dans le coin supérieur droit de la page, puis cliquez sur **[!UICONTROL Pause]**.

## Reprendre un profil externe {#resumeanexternalprofile}

À tout moment, vous pouvez toujours révoquer l’état suspendu d’un partenaire externe et reprendre les services normaux. Cliquez sur **[!UICONTROL Actions]** dans le coin supérieur droit de la page et choisissez **[!UICONTROL Reprendre]**.

Les états suivants s’appliquent aux utilisateurs externes :

* **État inactif** - Dans cet état, l’inscription des utilisateurs externes a expiré. Les administrateurs définissent la date d’expiration pour les utilisateurs externes lors de leur ajout via le workflow d’ajout d’utilisateurs.
* **État actif** - Dans cet état, les utilisateurs externes peuvent s’enregistrer dans l’application Learning Manager et se connecter à l’application.
* **Pause** - Dans cet état, le processus d’enregistrement des utilisateurs externes est bloqué. Cependant, les utilisateurs existants peuvent continuer à se connecter.

## Vérifier les places utilisées {#checkusedseats}

Dans la liste des profils externes, cliquez sur **[!UICONTROL Places utilisées]**. Vous pouvez afficher le nombre d’élèves qui ont été ajoutés dans l’organisation partenaire.

![](assets/seats-used.png)
*Vérifier les places utilisées*

## Suppression d’un utilisateur {#Deleteauser-1}

Choisissez un utilisateur, puis cliquez sur dans le coin supérieur droit. **[!UICONTROL Actions]** > **[!UICONTROL Supprimer l’utilisateur]**.

## Modifier le profil {#changeprofile}

Pour déplacer un utilisateur vers un autre profil externe, choisissez un utilisateur, puis cliquez sur dans le coin supérieur droit **[!UICONTROL Actions]** > **[!UICONTROL Modifier le profil]**. Dans la liste des profils, choisissez un profil, puis cliquez sur **[!UICONTROL Modifier]**.

## Attribution d’un rôle {#Assignarole-1}

Choisissez un utilisateur, puis cliquez sur dans le coin supérieur droit. **[!UICONTROL Actions]** > **[!UICONTROL Attribuer un rôle]** > **Créer`<role>`**. L’utilisateur obtient un nouveau rôle.

## Supprimer un rôle {#Removearole-1}

Choisissez un utilisateur, puis cliquez sur dans le coin supérieur droit. **[!UICONTROL Actions]** > **[!UICONTROL Supprimer le rôle]** > **Supprimer`<role>`**. Le rôle sélectionné est supprimé de la liste des rôles qui ont été attribués à l’utilisateur.

## Création de groupes d’utilisateurs {#createusergroups}

Un groupe d’utilisateurs est un ensemble d’utilisateurs associés à une catégorie. Les groupes d&#39;utilisateurs aident les administrateurs à sélectionner les élèves de leur organisation en fonction de leurs attributs, puis à leur attribuer du contenu d&#39;apprentissage. En outre, ces groupes d’utilisateurs permettent aux administrateurs d’attribuer des logos et des catalogues personnalisés aux élèves et d’afficher des rapports personnalisés sur leur progression.

Pour accéder aux groupes d’utilisateurs, dans le volet de navigation de gauche, cliquez sur **[!UICONTROL Groupes d’utilisateurs]**.

![](assets/user-groups.png)
*Création de groupes d’utilisateurs*

Il existe deux types de groupes dans Adobe Learning Manager : Personnalisé et Généré automatiquement. Lorsque vous ajoutez des élèves à votre compte, certains groupes sont automatiquement créés en fonction de leurs propriétés communes.

Pour afficher les groupes créés automatiquement, cliquez sur l’onglet **[!UICONTROL Généré automatiquement]**.

![](assets/auto-generated.png)
*Afficher les groupes générés automatiquement*

Vous pouvez voir qu’il existe différents groupes, comme Tous les utilisateurs internes, Tous les responsables, des groupes basés sur le centre de coûts, basés sur le service et basés sur les équipes des responsables.

En plus des groupes générés automatiquement, vous pouvez créer des groupes personnalisés. Pour ajouter un nouveau groupe personnalisé, dans le coin supérieur droit, cliquez sur **[!UICONTROL Ajouter]**.

1. Saisissez le nom et la description du groupe.
1. Saisissez le nom d’utilisateur ou le profil dans le champ de recherche lors de la saisie et sélectionnez, dans la liste déroulante, les utilisateurs à ajouter.
1. Pour ajouter d’autres élèves, cliquez sur **[!UICONTROL Ajouter plus d’utilisateurs].**
1. Pour créer le groupe d’utilisateurs, cliquez sur **[!UICONTROL Enregistrer]**.

Ce groupe personnalisé est maintenant créé et ajouté au profil. Les groupes d’utilisateurs que vous créez sont de nature dynamique. Si de nouveaux utilisateurs sont ajoutés avec des attributs similaires, ils sont automatiquement ajoutés au groupe d’utilisateurs.

## Exclusion de groupes d’utilisateurs

Vous souhaiterez parfois exclure un petit groupe d’utilisateurs d’un grand groupe d’utilisateurs. Cette opération est nécessaire pour inscrire cet ensemble spécifique d’utilisateurs à des formations via des plans d’apprentissage ou pour configurer la visibilité correcte des catalogues. Dans cette version de Learning Manager, vous pouvez exclure des élèves ou des groupes d’utilisateurs lorsque vous créez un groupe d’utilisateurs personnalisé. Dans la boîte de dialogue Ajouter un groupe d’utilisateurs, la section Exclure des élèves vous permet de le faire.

![](assets/exclude-user-groups.png)
*Exclure des groupes d’utilisateurs*

Par exemple, si vous souhaitez configurer un plan d’apprentissage de sorte que tous les utilisateurs appartenant à l’emplacement = Californie, sauf Store-5 (situé en Californie), soient inscrits.

## Paramètres avancés {#advancedsettings}

## Sources de données {#datasources}

Vous pouvez utiliser cette fonctionnalité lorsque vous souhaitez importer/synchroniser les utilisateurs ou les données d’apprentissage de la base de données de votre organisation dans l’application Learning Manager. Vous pouvez également définir la fréquence de cette synchronisation.

Cliquez sur **[!UICONTROL Sources de données]** dans le volet gauche sous **[!UICONTROL Avancé]** section.

![](assets/data-sources-add-users.png)

*Sources de données pour importer ou synchroniser des utilisateurs*

Choisissez le type de source de données dans le menu **[!UICONTROL Source]** dans la liste déroulante, sélectionnez la fréquence de mise à jour et cliquez sur **[!UICONTROL Synchroniser maintenant]** si vous devez synchroniser immédiatement ou cliquez sur **[!UICONTROL Enregistrer].** Les types de source de données sont SFDC, FTP, etc. pour les utilisateurs internes.

Vous pouvez ajouter plusieurs sources de données.

## Champs actifs {#activefields}

Cette fonctionnalité permet aux administrateurs d’ajouter des champs actifs en plus de ceux fournis lors de l’inscription des utilisateurs.

Cliquez sur **Champs actifs** disponible dans la page utilisateurs internes. Les élèves peuvent uniquement choisir parmi les valeurs données dans les valeurs personnalisées.

![](assets/active-fields.png)
*Champs actifs*

### Configurer les champs {#configurefields}

**Utilisateurs internes**

Vous pouvez ajouter une valeur personnalisée pour les champs utilisateur pour les utilisateurs internes.

Pour ajouter des valeurs personnalisées, procédez comme suit :

1. Cliquez sur  **[!UICONTROL Modifier les valeurs]** pour un utilisateur interne.

   ![](assets/modify-values.png)
   *Modification des valeurs pour les utilisateurs internes*

1. Le **Valeurs du champ personnalisé** s’affiche.

   ![](assets/values-in-customfields.png)
   *Valeurs dans la boîte de dialogue Champs personnalisés*

1. Sélectionnez la valeur à ajouter dans le menu **[!UICONTROL Sélectionner un champ]** menu déroulant.
1. Saisissez les nouvelles valeurs dans le champ **[!UICONTROL Nouvelle valeur]** champ.
1. Cliquez sur **[!UICONTROL Terminé]**.
1. Cliquez sur Enregistrer dans le coin supérieur droit pour **[!UICONTROL Enregistrer]** modifications.

**Utilisateurs externes**

Ajoutez des valeurs personnalisées similaires à celles des utilisateurs internes.

![](assets/modify-values-forexternalusers.png)
*Modification des valeurs pour les utilisateurs externes*

### Paramètres {#settings}

**Affichage de l’utilisateur**

Si l’option **Afficher uniquement les champs non remplis lors de la connexion de l’élève** Si est activé, l’utilisateur ne voit les champs vides qu’au moment de la connexion.

![](assets/settings-tab.png)
*Afficher les champs non remplis*

Avec cette option, un administrateur peut décider s’il souhaite afficher les champs ou les masquer une fois qu’ils ont été renseignés.

## Restreindre les champs actifs dans les rapports {#restrictactivefields}

Learning Manager 27.7 introduit deux nouvelles options : **[!UICONTROL Déclarable]** et **[!UICONTROL Exportable]**, pour les champs actifs.

![](assets/options-in-activefields.png)
*Options dans les champs actifs*

Pour les champs CSV et les champs ajoutés manuellement, si un champ actif est marqué comme **[!UICONTROL Déclarable]**, le champ actif peut être recherché dans un filtre à l’intérieur d’un rapport de tableau de bord.

![](assets/filters-in-a-dashboardreport.png)
*Filtres dans un rapport de tableau de bord*

Si un champ actif est marqué comme **[!UICONTROL Exportable]**, puis le Champ actif apparaît dans le fichier Excel lors du téléchargement d’un rapport Excel.

Ces options apparaissent pour les champs actifs internes et externes.

Vous pouvez uniquement supprimer un champ actif personnalisé.

## Affichage de l’utilisateur

Vous pouvez masquer l’intégralité de la page « Finaliser votre profil » aux élèves. La page ne s’affiche pas une fois l’élève connecté.

Notez que le comportement par défaut existant ne change pas. Il s’agit d’une fonctionnalité facultative désormais disponible pour les administrateurs.

Activez les options ci-dessous :

![](assets/user-display.png)
*Section Affichage de l’utilisateur*

## Prise en charge des champs CSV manuels par les connecteurs FTP et Box {#import-connector}

Souvent, les utilisateurs souhaitent que les champs Actifs soient fournis manuellement lorsqu’un élève se connecte à Learning Manager. Cela est actuellement possible dans Learning Manager, lorsque l’utilisateur importe un fichier CSV manuellement.

Le fichier CSV ne peut pas contenir tous les champs actifs. Pour tous les champs actifs qui ne sont pas mis à jour dans le fichier CSV chargé, l’utilisateur doit saisir les données de ces champs actifs.

Actuellement, tous les champs actifs doivent être mappés à un champ du fichier CSV source.

Il arrive qu’un utilisateur ne souhaite pas mapper un champ Actif à un champ spécifié dans le fichier CSV. Dans ce cas, l’utilisateur peut mapper le champ Actif à la valeur **[!UICONTROL PointImportFromSource]**. Sélectionnez cette valeur dans la liste déroulante, lors de l’importation d’utilisateurs à partir de connecteurs FTP et Box.

## Rôles personnalisés {#customroles}

Ajoutez n’importe quel champ de votre choix à vos informations utilisateur et cliquez sur **[!UICONTROL Enregistrer]**. Après avoir ajouté les champs, vous pouvez également vérifier les disponibilités des champs dans le panneau **[!UICONTROL Modifier les utilisateurs]** boîte de dialogue.

Après avoir ajouté les champs, vous pouvez remarquer que les champs marqués d’une coche sont issus d’une source de données ou d’un fichier CSV, comme indiqué dans l’instantané ci-dessous. L’administrateur peut modifier ces champs sources en les activant ou en les désactivant.

**Valeurs des champs actifs dans Learning Manager**

Les valeurs des champs actifs sont récupérées de la manière suivante :

1. L’application Learning Manager importe les métadonnées des sources de données associées à votre compte.
1. Métadonnées capturées à partir du fichier CSV importé manuellement.
1. Les élèves remplissent les métadonnées lors de leur connexion
1. L’administrateur saisit les données des utilisateurs.

>[!NOTE]
>
>L’application Learning Manager crée automatiquement des groupes d’utilisateurs à partir de ces métadonnées.

**Ajouter une valeur personnalisée**

Vous pouvez ajouter une valeur personnalisée pour les champs utilisateur dans les champs Utilisateur interne et Utilisateur externe.

Pour ajouter des valeurs personnalisées, procédez comme suit :

Des champs personnalisés peuvent être ajoutés et supprimés, ils s’appliquent à tous les utilisateurs. Les champs CSV peuvent être activés ou désactivés. Ils n’entrent en vigueur que lorsque vous chargez un fichier CSV après avoir effectué les modifications dans les champs Actifs. Tous les champs actifs internes s’appliquent à tous les types d’utilisateurs internes. Les champs externes s’appliquent uniquement aux utilisateurs externes. Si un champ personnalisé est présent dans le fichier CSV, il est converti automatiquement en champ CSV lors du chargement suivant et est activé.

## Valeurs des champs CSV {#valuesforcsvfields}

Les utilisateurs ne peuvent choisir parmi les champs prédéfinis pour les champs CSV que si l’option **[!UICONTROL Restreindre la sélection]** case à cocher activée.

![](assets/value-field-for-csv.png)
*Case à cocher Restreindre la sélection*

## Importer les journaux {#importlogs}

Dans cet espace, vous pouvez afficher l’historique d’importation CSV des utilisateurs ajoutés par l’administrateur à l’aide de la fonction d’importation en bloc. Vous pouvez également cliquer sur **Ajouter** dans le coin supérieur droit de la page pour ajouter des utilisateurs à l’aide de la fonction de chargement CSV.

## Champs actifs à plusieurs valeurs

Avec cette fonctionnalité, vous pouvez avoir plusieurs champs pour un champ actif. Dans un compte, il peut y avoir au maximum trois champs actifs à valeurs multiples. Les champs actifs à plusieurs valeurs sont disponibles pour les utilisateurs externes et internes.

Une fois que vous avez marqué un champ actif comme à plusieurs valeurs, vous ne pouvez pas le reconvertir en champ à valeur unique. Cette opération est irréversible.

Un champ à valeur unique existant ne peut pas être marqué comme champ à plusieurs valeurs.

Pour créer un champ actif à plusieurs valeurs, procédez comme suit :

1. Ajoutez un champ actif.

   ![Ajouter un champ actif](assets/add-active-field.png)
   *Ajouter un champ actif*

1. Cliquez sur Ajouter.
1. Dans l’onglet Paramètres, marquez le nouveau champ comme à plusieurs valeurs.

   ![Marquer comme à plusieurs valeurs](assets/mark-multi-valued.png)
   *Marquer comme à plusieurs valeurs*

   Il y a une autre case à cocher, **[!UICONTROL Configurable par l’élève]**, qui si elle est désactivée, l’élève ne pourra pas voir le champ sur la page Profil.

1. Ajoutez les valeurs à l’aide d’un fichier CSV ou en cliquant sur Modifier les valeurs.

   ![Ajouter des valeurs](assets/add-values.png)
   *Ajouter des valeurs*

1. Cliquez sur [!UICONTROL **Terminé**].

>[!NOTE]
>
>Une fois que le groupe d’utilisateurs est créé et que le champ est renseigné, les valeurs multiples ne peuvent pas être converties en valeurs uniques, et inversement.

### Ajouter un champ actif à plusieurs valeurs via CSV

Procédez comme suit :

1. Créez un fichier CSV avec les nouveaux champs actifs sous forme de colonnes (valeurs séparées par des virgules ou valeurs uniques).
1. Importez le fichier CSV.
1. Marquez les champs comme à plusieurs valeurs dans la boîte de dialogue Valeurs dans les champs personnalisés.
1. Importez à nouveau le fichier CSV.

Le fichier CSV doit avoir une colonne portant le même nom qu’un champ actif marqué comme à plusieurs valeurs.

Le fichier CSV contient les champs suivants :

* **[!UICONTROL Utilisateur]**: groupes d’utilisateurs créés en tant que rôles.
* **[!UICONTROL Rôles]**: champ actif à plusieurs valeurs avec des valeurs.

Si le fichier CSV est rechargé avec de nouvelles valeurs ou des valeurs supprimées, les champs actifs et les groupes sont également mis à jour en conséquence.

### Rapports

Tous les états incluent les champs actifs à plusieurs valeurs et leurs valeurs.

L’administrateur peut ajouter des champs actifs générés automatiquement et configurer les rapports d’activité et de formation des utilisateurs.

Le rapport Relevé de notes de l’élève contient tous les champs actifs et les valeurs séparées par des virgules. L’administrateur peut ensuite filtrer les données en conséquence.

## Foire aux questions {#faq}

+++Comment enregistrer des utilisateurs dans Learning Manager ?

Après avoir ajouté un utilisateur et lui avoir attribué un rôle, vous pouvez l’enregistrer en procédant comme suit :

1. L’utilisateur ou les utilisateurs étant sélectionnés, cliquez sur **[!UICONTROL Actions]** dans le coin supérieur droit, puis cliquez sur **[!UICONTROL S&#39;inscrire]**.

1. Dans la fenêtre contextuelle, cliquez sur **[!UICONTROL Oui]**.

Le ou les utilisateurs sélectionnés reçoivent un e-mail de bienvenue. Si les élèves ont déjà un Adobe ID, ils peuvent cliquer sur ce lien. S’ils n’ont pas d’Adobe ID existant, ils peuvent cliquer sur le lien Bienvenue pour créer un Adobe ID et le lier à leur compte Learning Manager.

Les élèves doivent obligatoirement cliquer sur l’un de ces liens dans l’e-mail, car cela aide Learning Manager à vérifier le compte de l’élève.

+++

+++Comment modifier les données utilisateur ?

Pour modifier un utilisateur, procédez comme suit :

1. Dans la liste des utilisateurs, cliquez sur l’utilisateur pour lequel vous souhaitez modifier les données.
1. Cliquez sur l’icône de crayon, comme indiqué ci-dessous.

![](assets/edit-user-data.png)

Dans le panneau **[!UICONTROL Modifier l’utilisateur]** , mettez les champs à jour en conséquence. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

+++

+++Comment suspendre et reprendre un utilisateur externe dans Learning Manager ?

Dans la liste des utilisateurs externes, sélectionnez l’utilisateur que vous souhaitez supprimer. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Pause]**.

Pour plus d’informations, voir [Suspendre un profil externe](add-users-user-groups.md#pause).

Après avoir suspendu un profil, le profil externe affiche l’état comme ***Suspendu***.

+++

+++Comment envoyer un e-mail de bienvenue à un profil externe nouvellement créé ?

Lors de l’ajout d’un utilisateur externe, dans la section **[!UICONTROL Ajouter un profil d&#39;inscription externe]** , saisissez l’adresse e-mail du responsable externe. Lorsque vous cliquez sur Enregistrer, un e-mail de bienvenue est également envoyé à l’adresse e-mail que vous avez spécifiée. Si vous souhaitez envoyer à nouveau l’e-mail de bienvenue, cliquez sur l’icône d’enveloppe, comme indiqué ci-dessous :

![](assets/send-welcome-mail.png)

+++

+++Comment créer des groupes d’utilisateurs personnalisés ?

Cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Groupes d’utilisateurs]** et sur la page Groupes d’utilisateurs, cliquez sur **[!UICONTROL Ajouter]**. Dans la boîte de dialogue Ajouter un groupe d’utilisateurs, ajoutez les utilisateurs individuellement et en équipe.

![](assets/custom-user-group.png)

+++

+++Comment désactiver les champs actifs déjà remplis ?

Si vous souhaitez que les élèves voient uniquement les champs actifs qui ne sont pas remplis par eux, suivez les étapes ci-dessous :

1. Cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Champs actifs]**.

1. Cliquez sur **[!UICONTROL Paramètres]** et activez l’option **[!UICONTROL Afficher uniquement les champs non remplis lors de la connexion de l’élève]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

+++

+++Comment empêcher les élèves de saisir des valeurs aléatoires dans les champs actifs ?

Vous pouvez restreindre la sélection pour les élèves afin qu&#39;ils puissent uniquement sélectionner les valeurs prédéfinies et ne pas saisir de valeurs aléatoires. Procédez comme suit :

1. Cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Champs actifs]**.
1. Dans la section **[!UICONTROL Configurer les champs]**, cliquez sur **[!UICONTROL Modifier les valeurs]**.

1. Activer l’option **[!UICONTROL Restreindre la sélection]**.
1. Cliquez sur **[!UICONTROL Terminé]**.

+++

+++Comment différencier les champs actifs CSV et les champs actifs personnalisés ?

Vous pouvez uniquement activer ou désactiver les champs actifs CSV, mais vous ne pouvez pas les supprimer. En revanche, vous ne pouvez pas activer ou désactiver les champs actifs personnalisés.

+++
