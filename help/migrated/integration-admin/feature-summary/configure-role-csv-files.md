---
jcr-language: en_us
title: Gestion des rôles personnalisés via des fichiers CSV
description: L’administrateur d’intégration peut ajouter un certain nombre de rôles personnalisés à son compte en bloc via CSV, et peut les attribuer à divers utilisateurs. Cette approche automatise le processus de création de rôles personnalisés.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---



# Gestion des rôles personnalisés via des fichiers CSV

L’administrateur d’intégration peut ajouter un certain nombre de rôles personnalisés à son compte en bloc via CSV, et peut les attribuer à divers utilisateurs. Cette approche automatise le processus de création de rôles personnalisés.

Vous pouvez configurer les rôles via les connecteurs Learning Manager FTP et Box.

Une fois connecté à votre compte de stockage Box ou ExaVault, l’administrateur d’intégration peut ajouter les fichiers .csv suivants dans le compte :

* role.csv
* user_role.csv

Pour commencer, téléchargez les fichiers .csv et modifiez les valeurs en fonction de vos besoins.

**role.csv**
[Exemple de fichier - role.csv](assets/role.csv) [Exemple de fichier : user_role.csv](assets/user-role.csv)

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nom de la colonne</b></p></td>
   <td>
    <p><b>Description</b></p></td>
   <td>
    <p><b>Exemples de valeurs</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Nom</p></td>
   <td>
    <p>Identifiez le rôle à affecter aux utilisateurs dans le fichier CSV.</p></td>
   <td>
    <p>Auteur commercial</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifiez le type d'accès (COMPLET, ÉCRIT, INSCRIPTION, RAPPORT, AUCUN) pour chaque type d'entité tel que COURS, CATALOGUE, etc.</p></td>
   <td>
    <p>COMPLET</p>
    <p>AUCUN</p>
    <p>ÉCRIRE | RAPPORT</p>
    <p>Les noms de colonne correspondent aux noms de type d’entité tels que Catalogue, Cours, Plan d’apprentissage, etc.</p>
    <p>Une colonne pour chaque type d’entité sera présente dans le fichier CSV. Les entités pour lesquelles aucune autorisation ne doit être donnée doivent être incluses avec une valeur NONE</p></td>
  </tr>
  <tr>
   <td>
    <p>Spécificateur d'étendue de catalogue</p></td>
   <td>
    <p>Un seul nom de catalogue ou une liste séparée par PIPE (|) de noms de catalogue qui déterminent la portée de ce rôle.</p></td>
   <td>
    <p>Catalogue de ventes | Catalogue général</p></td>
  </tr>
  <tr>
   <td>
    <p>Spécificateur d'étendue du groupe d'utilisateurs</p></td>
   <td>
    <p>Nom et valeur de l'attribut de groupe d'utilisateurs qui déterminent l'étendue des utilisateurs de ce rôle.</p>
    <p>Voir la section ci-dessous pour les portées.</p></td>
   <td>
    <p>location=Londres</p></td>
  </tr>
  <tr>
   <td>
    <p>Description</p></td>
   <td>
    <p>Description conviviale facultative pour aider à comprendre l’objectif du rôle et la référence ultérieure.</p></td>
   <td>
    <p>Accès complet de l’auteur aux objets d’apprentissage dans le catalogue des ventes</p></td>
  </tr>
 </tbody>
</table>

Toutes les colonnes, sauf Description, sont obligatoires.

## Définition de l’étendue des groupes d’utilisateurs {#definescopeofusergroups}

Vous pouvez spécifier des étendues pour des groupes d’utilisateurs pour différents types de groupes de la manière suivante :

* Nom du groupe d’utilisateurs tel quel (par exemple, Tous les auteurs, Mon groupe personnalisé)
* Attribut et valeur de feuille (par exemple, Department=HR)
* Groupes de profils d&#39;auto-inscription (self_registration=profilename)
* Groupes de profils d&#39;inscription externe (ext_registration=profilename)
* L&#39;équipe de subordonnés directs d&#39;un responsable (manager_direct=`<emailid>`)
* Organisation complète d’un responsable (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nom de colonne</b></p></td>
   <td>
    <p><b>Description</b></p></td>
   <td>
    <p><b>Commentaire</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Id</p></td>
   <td>
    <p>ID de messagerie de l’utilisateur auquel un rôle configurable doit être attribué.</p></td>
   <td>
    <p>Si un rôle configurable est déjà attribué à l’utilisateur, il est remplacé par un nouveau rôle spécifié dans le fichier CSV. Aucune erreur n’est signalée.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Nom du rôle configurable à affecter à l’utilisateur</p></td>
   <td>
    <p>Le nom du rôle doit être un rôle existant tel que spécifié dans le fichier CSV. Les rôles créés par l’administrateur via l’interface utilisateur peuvent être utilisés ici.</p></td>
  </tr>
 </tbody>
</table>

**Fonctionnalités étendues**

Chaque fois qu’une autorisation complète est attribuée pour l’une des fonctionnalités suivantes (fonctionnalités au niveau du compte), la portée du groupe d’utilisateurs et la portée du catalogue sont automatiquement considérées comme COMPLÈTES, car l’utilisateur ne peut pas avoir un accès limité à ces fonctionnalités.

Si des noms de catalogue ou des noms de groupe d’utilisateurs sont fournis dans le fichier CSV, ils sont remplacés avec l’autorisation COMPLÈTE.

* Annonce
* Compétences
* Ludification
* Utilisateurs
* Plans d’apprentissage
* Modèles de courrier électronique

## Ajout des fichiers CSV de rôle dans le compte {#addtherolecsvsintheaccount}

Dans votre compte Box, choisissez **Importer > utilisateur > interne**, puis téléchargez les fichiers role.csv et user_role.csv.

* Les fichiers CSV de rôle personnalisé doivent être copiés dans le dossier « import->user->internal->user_role »
* Le fichier CSV des utilisateurs doit être copié dans le dossier « import->user->internal »

Les deux fichiers CSV doivent être chargés uniquement via Box ou FTP et ne peuvent pas être chargés via l’interface utilisateur.

>[!NOTE]
>
>Le fichier CSV Utilisateurs est obligatoire, mais les fichiers CSV Rôle personnalisé sont facultatifs. Tous les fichiers présents sont traités, et les autres sont ignorés.

Les rôles personnalisés créés à l’aide du fichier csv ne sont pas visibles par les administrateurs dans l’interface utilisateur. Ces rôles ne seront pas liés ou affectés par les rôles créés (ou à créer ultérieurement) par l’interface utilisateur.

Les rôles personnalisés qui ont été créés par un fichier CSV peuvent être entièrement gérés via le fichier CSV lui-même. Cela inclut l’ajout, la modification et la suppression de rôles.

Les rôles attribués peuvent être révoqués en supprimant les entrées d’affectation du fichier csv user_role. Toutefois, les affectations effectuées via l’interface utilisateur d’administration ne sont pas affectées par ce paramètre.

Pour attribuer et révoquer un rôle personnalisé, mettez à jour les fichiers csv.

## Synchronisation des rôles personnalisés {#synchronizationofcustomroles}

Une fois que l’administrateur d’intégration a chargé les fichiers CSV basés sur les rôles dans le stockage Connecteur, il peut activer la synchronisation avec les fichiers CSV. Chaque fois qu’un rôle personnalisé est mis à jour, ajouté ou supprimé dans les fichiers CSV, l’administrateur peut synchroniser les informations dans les fichiers et actualiser la liste des rôles.

Dans la page Prise en main du panneau Administrateur, cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Sources de données]**.

Dans la section Paramètres de synchronisation, activez l’option **[!UICONTROL Activer la synchronisation automatique]**.

![](assets/sync-settings.png)

*Sélectionnez l’option Activer la synchronisation automatique*

Lorsque vous sélectionnez cette option, vous pouvez planifier l’heure de synchronisation à l’heure exacte que vous spécifiez dans le champ Heure de synchronisation. Si vous spécifiez l’heure de synchronisation à 00h00, les rôles personnalisés sont mis à jour tous les jours à l’heure exacte spécifiée.

Si vous souhaitez synchroniser les données à la demande, cliquez sur **[!UICONTROL Synchroniser maintenant]**.

## Contraintes lors de la configuration des rôles {#constraintswhileconfiguringroles}

Quel que soit le compte, le nom d’un rôle doit être unique. Par conséquent, un rôle créé via l’interface utilisateur ou le fichier CSV ne doit pas avoir le même nom qu’un autre rôle déjà créé par l’interface utilisateur ou le fichier CSV.

Sur des lignes similaires, à partir de l’interface utilisateur d’administration, un utilisateur ne peut pas se voir attribuer un rôle configurable créé via CSV, car ces rôles ne seront pas disponibles.

Cependant, le fichier CSV d’affectation d’utilisateur peut être utilisé pour attribuer des rôles créés par l’interface utilisateur.
