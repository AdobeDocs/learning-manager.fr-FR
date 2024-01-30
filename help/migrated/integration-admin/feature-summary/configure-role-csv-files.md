---
jcr-language: en_us
title: Gérer des rôles personnalisés via les fichiers CSV
description: L’administrateur de l’intégration peut ajouter un certain nombre de rôles personnalisés à son compte en masse via un fichier CSV et les attribuer à différents utilisateurs. Cette approche automatise le processus de création des rôles personnalisés.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 86%

---



# Gérer des rôles personnalisés via les fichiers CSV

L’administrateur de l’intégration peut ajouter un certain nombre de rôles personnalisés à son compte en masse via un fichier CSV et les attribuer à différents utilisateurs. Cette approche automatise le processus de création des rôles personnalisés.

Vous pouvez configurer les rôles via les connecteurs Learning Manager FTP et Box.

Après vous être connecté à votre compte de stockage Box ou ExaVault, l’administrateur de l’intégration peut ajouter les fichiers CSV suivants dans le compte :

* role.csv
* user_role.csv

Pour commencer, téléchargez les fichiers CSV et modifiez les valeurs en fonction de vos besoins.

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
    <p><b>Exemple de valeurs</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Nom</p></td>
   <td>
    <p>Identifiez le rôle dans le fichier CSV à attribuer aux utilisateurs.</p></td>
   <td>
    <p>Auteur ventes</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifiez le type d'accès (COMPLET, ÉCRIT, INSCRIPTION, RAPPORT, AUCUN) pour chaque type d'entité tel que COURS, CATALOGUE, etc.</p></td>
   <td>
    <p>COMPLET</p>
    <p>AUCUN</p>
    <p>ÉCRITURE | RAPPORT</p>
    <p>Les noms des colonnes correspondront aux noms des types d’entités tels que Catalogue, Cours, Plan d’apprentissage, etc.</p>
    <p>Une colonne pour chaque type d’entité sera présente dans le fichier CSV. Les entités pour lesquelles aucune autorisation ne doit être donnée doivent être incluses avec une valeur AUCUNE</p></td>
  </tr>
  <tr>
   <td>
    <p>Spécificateur du champ d’application du catalogue</p></td>
   <td>
    <p>Nom unique de catalogue ou BARRE VERTICALE (|) liste séparée des noms de catalogue qui déterminent le champ d’application de ce rôle</p></td>
   <td>
    <p>Catalogue de vente | Catalogue général</p></td>
  </tr>
  <tr>
   <td>
    <p>Spécificateur d'étendue du groupe d'utilisateurs</p></td>
   <td>
    <p>Nom et valeur de l’attribut du groupe d’utilisateurs qui déterminent le champ d’application des utilisateurs de ce rôle.</p>
    <p>Voir la section ci-dessous pour obtenir les champs d’application.</p></td>
   <td>
    <p>location=London</p></td>
  </tr>
  <tr>
   <td>
    <p>Description</p></td>
   <td>
    <p>Description optionnelle conviviale pour aider à comprendre le but du rôle et les références ultérieures.</p></td>
   <td>
    <p>Accès complet à l’auteur aux Objets d’apprentissage dans le catalogue de vente</p></td>
  </tr>
 </tbody>
</table>

Toutes les colonnes sauf Description sont obligatoires.

## Définir le champ d’application des groupes d’utilisateurs {#definescopeofusergroups}

Vous pouvez spécifier les champs d’application des groupes d’utilisateurs pour divers types de groupes de la manière suivante :

* Nom du groupe d’utilisateurs tel quel (par exemple, Tous les auteurs, Mon groupe personnalisé)
* Attribut et valeur de la feuille (par exemple, Department=HR)
* Groupes de profils d’auto-inscription (self_registration=profilename)
* Groupes de profils d’inscription externe (self_registration=profilename)
* L&#39;équipe de subordonnés directs d&#39;un responsable (manager_direct=`<emailid>`)
* Organisation complète d’un responsable (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nom de la colonne</b></p></td>
   <td>
    <p><b>Description</b></p></td>
   <td>
    <p><b>Commentaire</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Id</p></td>
   <td>
    <p>ID de courrier électronique de l’utilisateur auquel un rôle configurable doit être attribué.</p></td>
   <td>
    <p>Si l’utilisateur a déjà un rôle configurable affecté, le rôle est remplacé par un nouveau rôle spécifié dans le fichier CSV. Aucune erreur n’est signalée.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Nom du rôle configurable à attribuer à l’utilisateur</p></td>
   <td>
    <p>Le nom du rôle doit être un rôle existant tel que spécifié dans le fichier CSV. Les rôles créés par l’administrateur via l’interface utilisateur peuvent être utilisés ici.</p></td>
  </tr>
 </tbody>
</table>

**Caractéristiques complètes de champs d’application**

Lorsqu’une autorisation complète est attribuée à l’une des fonctionnalités suivantes (fonctionnalités au niveau du compte), le champ d’application du groupe d’utilisateurs et le champ d’application du catalogue sont automatiquement considérées comme COMPLETS, l’utilisateur ne pouvant pas avoir un accès limité à ces fonctionnalités.

Si des noms de catalogue ou des noms de groupes d’utilisateurs sont fournis dans le fichier CSV, ils sont remplacés par une autorisation de type COMPLET.

* Annonces
* Compétences
* Ludification
* Utilisateurs
* Plans d’apprentissage
* Modèles de courriers électroniques

## Ajouter les fichiers CSV du rôle dans le compte {#addtherolecsvsintheaccount}

Dans votre compte Box, sélectionnez **Importer > utilisateur > interne**, et téléchargez les fichiers role.csv et user_role.csv.

* Les fichiers CSV de rôle personnalisé doivent être copiés dans le dossier « import->user->internal->user_role »
* Le fichier CSV des utilisateurs doit être copié dans le dossier « import->user->internal »

Les deux fichiers CSV doivent être téléchargés via Box ou FTP uniquement et ne peuvent pas être téléchargés via l’interface utilisateur.

>[!NOTE]
>
>Le fichier CSV Utilisateurs est obligatoire, mais les fichiers CSV Rôle personnalisé sont facultatifs. Tous les fichiers présents sont traités et les autres sont ignorés.

Les rôles personnalisés créés à l’aide du fichier CSV ne sont pas visibles par les administrateurs de l’interface utilisateur. Ces rôles ne seront pas associés ni attribués par les rôles créés (ou à créer ultérieurement) par l’interface utilisateur.

Les rôles personnalisés qui ont été créés par un fichier CSV peuvent être entièrement gérés via le fichier CSV lui-même. Cela inclut l’ajout, la modification et la suppression de rôles.

Les rôles attribués peuvent être révoqués en supprimant les entrées d’attribution du fichier CSV user_role. Cependant, les attributions effectuées via l’interface utilisateur d’administration ne sont pas concernées.

Pour attribuer et révoquer un rôle personnalisé, mettez à jour les fichiers CSV.

## Synchronisation des rôles personnalisés {#synchronizationofcustomroles}

Une fois que l’administrateur d’intégration a téléchargé les fichiers CSV basés sur les rôles dans le stockage Connector, il peut activer la synchronisation avec les fichiers CSV. Chaque fois qu’un rôle personnalisé est mis à jour, ajouté ou supprimé dans les fichiers CSV, l’administrateur peut synchroniser les informations des fichiers et mettre à jour la liste des rôles.

Dans la page Prise en main du panneau Administrateur, cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Sources de données]**.

Dans la section Paramètres de synchronisation, activez l’option **[!UICONTROL Activer la synchronisation automatique]**.

![](assets/sync-settings.png)

*Sélectionnez l’option Activer la synchronisation automatique*

Lorsque vous sélectionnez cette option, vous pouvez programmer l’heure de synchronisation à l’heure exacte indiquée dans le champ Heure de synchronisation. Si vous indiquez 00:00 comme heure de synchronisation, les rôles personnalisés sont chaque jour mis à jour à l’heure exacte spécifiée.

Si vous souhaitez synchroniser les données à la demande, cliquez sur **[!UICONTROL Synchroniser maintenant]**.

## Contraintes lors de la configuration des rôles {#constraintswhileconfiguringroles}

Dans tous les cas, le nom d’un rôle doit être unique. Par conséquent, un rôle créé via l’interface utilisateur ou un fichier CSV ne doit pas avoir le même nom qu’un autre rôle déjà créé via l’interface utilisateur ou un fichier CSV.

Sur des lignes similaires, à partir de l’interface utilisateur de l’administrateur, un utilisateur ne peut pas se voir attribuer un rôle configurable créé via un fichier CSV car ces rôles ne seront pas disponibles.

Toutefois, le fichier CSV de l’attribution aux utilisateurs peut être utilisé pour affecter les rôles créés par l’interface utilisateur.
