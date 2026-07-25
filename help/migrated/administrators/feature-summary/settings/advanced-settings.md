---
description: En savoir plus sur la configuration des paramètres avancés dans Adobe Learning Manager
jcr-language: en_us
title: Paramètres avancés dans Adobe Learning Manager
exl-id: 7047c89f-5f1c-4e0a-a908-20ef0eb9667d
source-git-commit: 29302e039dfd8b8cc0c5fc20b46dc2403ce6c45b
workflow-type: tm+mt
source-wordcount: '2391'
ht-degree: 1%

---

# Paramètres avancés dans Adobe Learning Manager

## Étiquettes de catalogue

Les étiquettes de catalogue dans Adobe Learning Manager sont utilisées pour baliser les objets d’apprentissage (cours, certifications, parcours d’apprentissage, etc.) avec des champs et des valeurs spécifiques. Ces étiquettes vous aident, vous et les auteurs, à classer et organiser efficacement le contenu, ce qui permet un meilleur filtrage, suivi et création de rapports.

Voir [Étiquettes de catalogue dans Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md) pour plus d&#39;informations.


>[!NOTE]
>
>* Libellés obligatoires : vous pouvez choisir de rendre les libellés de catalogue obligatoires pour les auteurs lors de la création du cours.
>* Flux de production des auteurs : les auteurs doivent ajouter des étiquettes de conformité lors de la création ou de la modification des cours pour garantir une catégorisation correcte.

## Dossier de contenu

Les dossiers de contenu dans Adobe Learning Manager contrôlent les auteurs qui peuvent voir et accéder au contenu dans la bibliothèque de contenu. Grâce aux dossiers de contenu hiérarchisés, les administrateurs peuvent organiser de grandes bibliothèques de contenu en jusqu’à trois niveaux de dossiers privés imbriqués, ce qui facilite la recherche, la gestion et la réutilisation du contenu au sein de votre organisation.

### Qu’est-ce qu’un dossier de contenu ?

Un dossier de contenu est un conteneur qui regroupe le contenu associé et détermine qui peut y accéder. Chaque fichier de contenu dans Adobe Learning Manager appartient à tout moment à au moins un dossier.

Il existe deux types de dossiers de contenu :

**Dossier public** présent dans chaque compte par défaut. Le dossier public possède les propriétés suivantes :

* Tous les auteurs du compte peuvent accéder au contenu du dossier public.
* Le contenu du dossier public ne peut pas se trouver dans un dossier privé. L&#39;inverse est également vrai. Le contenu d’un dossier privé ne peut pas se trouver dans le dossier public.
* Le dossier public ne fait pas partie de la configuration de l’accès basé sur les rôles. Le fait de restreindre un rôle personnalisé à des dossiers privés spécifiques ne restreint pas l’accès au dossier public.

**Dossiers privés** - créés par les administrateurs. Les dossiers privés prennent en charge une hiérarchie à trois niveaux et leur accès est contrôlé par la configuration des rôles.

**Comprendre les niveaux de hiérarchie des dossiers**

Les dossiers de contenu privés prennent en charge jusqu’à trois niveaux d’imbrication :

* **Dossiers de niveau 1** : dossiers de niveau supérieur à la racine de votre bibliothèque de contenu

* **Dossiers de niveau 2** : sous-dossiers imbriqués dans un dossier de niveau 1

* **Dossiers de niveau 3** : sous-dossiers imbriqués dans un dossier de niveau 2

Cette structure permet aux organisations de refléter l’organisation du contenu réel, par rubrique, type de diffusion, audience ou équipe, plutôt que de gérer des milliers de fichiers dans une liste plate.

>[!NOTE]
>
>Seuls les administrateurs peuvent créer, modifier ou supprimer des dossiers à n’importe quel niveau. Les auteurs et les utilisateurs personnalisés interagissent avec la hiérarchie, mais ne peuvent pas la modifier. En outre, les administrateurs personnalisés ayant accès à n’importe quel dossier racine peuvent créer, modifier ou supprimer des dossiers sous ce dossier racine.


### Règles de dénomination des dossiers

Les noms de dossier doivent être uniques au sein du même niveau et se trouver dans le même dossier parent. Plus précisément :

| **Scénario** | **Autorisé ?** |
|----------------------------------------------------------------------------------------------|--------------------------|
| Deux dossiers de niveau 1 portant le même nom | Non |
| Deux dossiers de niveau 2 sous le même dossier de niveau 1 avec le même nom | Non |
| Deux dossiers de niveau 2 sous différents dossiers de niveau 1 avec le même nom | Oui |
| Un dossier de niveau 2 et un dossier de niveau 3 portant le même nom | Oui. Les niveaux sont distincts |
| Un dossier de niveau 3 et un autre dossier de niveau 3 sous le même dossier de niveau 2 avec le même nom | Non |


### Affichage des chemins de dossier

La bibliothèque de contenu affiche le chemin complet de chaque fichier de contenu. Par exemple, **Programmes de formation** / **Intégration** / **Ressources SCORM**. Ce chemin montre l’emplacement complet du contenu.

Si un fichier existe dans plusieurs dossiers, tous les chemins apparaissent séparés par des virgules. Si un chemin est long, il est tronqué depuis le début avec une ellipse (...), et le nom du dossier le plus profond est toujours affiché.

### Accès aux dossiers basé sur les rôles

L&#39;accès aux dossiers privés est attribué au **niveau 1 uniquement**. Lorsqu’un rôle personnalisé se voit accorder l’accès à un dossier de niveau 1, cet accès se répercute automatiquement sur tous les sous-dossiers de niveau 2 et de niveau 3 qu’il contient. Il n’existe pas d’option permettant d’accorder l’accès au niveau du sous-dossier indépendamment.

Le tableau suivant décrit ce que chaque rôle peut faire avec la hiérarchie des dossiers.

| **Rôle** | **Ce qu&#39;ils peuvent faire** |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| L’administrateur | Créer, renommer et supprimer des dossiers privés de niveau 1, de niveau 2 et de niveau 3 ; configurer l’accès aux dossiers de niveau 1 pour les rôles personnalisés |
| Administrateur personnalisé | Gérer les dossiers dans les branches accessibles de niveau 1, en fonction des privilèges qui leur sont attribués |
| Auteur | Parcourir les dossiers, filtrer le contenu par dossier, ajouter du contenu aux dossiers, copier et déplacer du contenu entre les dossiers, sélectionner du contenu lors de l&#39;ajout de modules à un cours |
| Auteur personnalisé | Identique à l’auteur, mais limité aux dossiers accessibles via les privilèges de niveau 1 qui leur sont attribués |

### Limites de la structure des dossiers

| **Limite** | **Valeur** |
|---------------------------------------|-----------|
| Dossiers de niveau 1 par compte | Aucune limite |
| Sous-dossiers de niveau 2 par dossier de niveau 1 | 25 |
| Sous-dossiers de niveau 3 par dossier de niveau 2 | 25 |
| Profondeur de dossier maximale | 3 niveaux |


### Comportement de sélection de dossier

Lorsque vous sélectionnez un dossier, par exemple, lors du filtrage ou de la suppression, la sélection se propage en cascade dans la hiérarchie comme suit :

* La sélection d&#39;un dossier de **niveau 1** sélectionne automatiquement tous les dossiers de niveau 2 et de niveau 3 situés en dessous.

* La sélection d&#39;un **dossier de niveau 2** sélectionne automatiquement tous les dossiers de niveau 3 situés en dessous. Les autres dossiers de niveau 2 du même dossier de niveau 1 ne sont pas sélectionnés.

* La sélection d&#39;un dossier de **niveau 3** sélectionne uniquement ce dossier. Aucun autre dossier n’est sélectionné.

>[!NOTE]
>
>Lorsque vous sélectionnez un sous-dossier sans sélectionner son parent, le dossier parent n’affiche pas d’indicateur de sélection partielle ou mixte. C&#39;est intentionnel. Car un dossier parent peut lui-même contenir du contenu, pas seulement des sous-dossiers. La sélection d’un dossier parent signifie « inclure tout le contenu de ce dossier et de tout ce qui se trouve en dessous ». Un indicateur partiel suggère que le contenu propre au dossier parent est partiellement inclus, ce qui serait trompeur. Si vous souhaitez filtrer uniquement par sous-dossier spécifique, sélectionnez directement ce sous-dossier. Si vous souhaitez que tout le contenu se trouve dans un dossier parent et ses sous-dossiers, sélectionnez le dossier parent.

### Quand utiliser une structure de dossiers hiérarchique

Les dossiers de contenu hiérarchisés sont particulièrement utiles lorsque votre entreprise gère de nombreux fichiers de contenu et a besoin d’une façon structurée de parcourir, de réutiliser et de contrôler l’accès à ces fichiers.

Les scénarios courants sont les suivants :

* **Bibliothèques de contenu volumineuses** : lorsque vous disposez de milliers de fichiers de contenu, une hiérarchie à trois niveaux permet aux auteurs d’accéder directement à ce dont ils ont besoin, plutôt que de faire défiler une liste plate.

* **Plusieurs équipes ou projets** : les dossiers de niveau 1 peuvent séparer les zones d’équipe ou de projet ; les dossiers de niveau 2 peuvent être organisés par type de livraison ; les dossiers de niveau 3 peuvent contenir des ressources individuelles.

* **Séparation du contenu basée sur les rôles** : lorsque différentes équipes d’auteurs doivent accéder uniquement au contenu pertinent pour leur travail, l’affectation d’accès au dossier de niveau 1 conserve le contenu privé de chaque équipe.

### Cas d’utilisation réels de dossiers de contenu hiérarchique

**Cas d’utilisation 1- Formation à la conformité avec un contenu spécifique à la juridiction**

Une organisation internationale organise des formations obligatoires sur la conformité dans plusieurs régions. Chaque région dispose de modules de base qui s’appliquent à tous, ainsi que d’addenda juridiques spécifiques à chaque juridiction, tels que les réglementations sur la confidentialité des données, le droit du travail local, les exigences de divulgation financière, qui varient selon le pays ou la région.

Sans dossiers hiérarchisés, tous les actifs de conformité sont regroupés dans une liste plate, ce qui rend difficile pour les équipes de contenu régionales de savoir quels fichiers appartiennent à quel programme ou à quelle juridiction.

Avec une structure à trois niveaux :

* Niveau 1 : Formation sur la conformité

* Niveau 2 : EMEA / APAC / Amériques (un sous-dossier par région)

* Niveau 3 : modules ou ressources spécifiques par région (PDF de la réglementation de la confidentialité, jeux de politiques locales, fichiers d’évaluation)

Dans le cas d’auteurs régionaux, étant un rôle personnalisé, seul le dossier de niveau 1 peut être sélectionné lors de la création du rôle personnalisé. La sélection du dossier de niveau 2 n’est pas une option. Ils peuvent uniquement trouver, mettre à jour et réutiliser les ressources correspondant à leur juridiction sans voir ou modifier accidentellement le contenu d’une autre région.

**Cas d’utilisation 2- Programme d’intégration à grande échelle avec de nombreux rôles**

Une organisation intègre des milliers d’employés par an dans le cadre de plusieurs rôles distincts : contributeurs individuels, responsables, sous-traitants et spécialistes techniques. Chaque rôle possède son propre parcours d’intégration avec un contenu de base partagé et des modules spécifiques aux rôles.

Avec une structure à trois niveaux :

* Niveau 1 : Intégration

* Niveau 2 : Rôle (Contributeur individuel / Responsable / Entrepreneur / Spécialiste technique)

* Niveau 3 : Type de module (packages SCORM / platines ILT / guides d&#39;activité / évaluations)

Les auteurs qui créent des cours pour chaque rôle accèdent directement au niveau 2 et recherchent les fichiers exacts pour ce suivi. Lorsqu&#39;un module est réutilisé entre des rôles, comme une vidéo sur les valeurs d&#39;une entreprise, il peut être copié ou lié dans plusieurs dossiers sans créer de doublons. Le contenu reste à source unique, mais apparaît dans toutes les branches pertinentes.

**Cas d’utilisation 3 - Bibliothèque de compétences techniques à volume élevé avec plusieurs équipes de contenu**

Une entreprise technologique tient à jour une bibliothèque interne de formation aux compétences avec des milliers de fichiers de contenu dans les gammes de produits, l’infrastructure cloud, les outils de développement, la sécurité et l’ingénierie des données. Plusieurs équipes d’auteurs contribuent, chacune étant responsable d’un domaine de produits. Les modules de cours peuvent exécuter de 40 à 60 fichiers par cours.

Sans hiérarchie, les milliers de fichiers sont regroupés dans une poignée de dossiers de niveau supérieur et les auteurs de différentes équipes choisissent souvent la mauvaise version du fichier ou écrasent accidentellement les ressources partagées.

Avec une structure à trois niveaux :

* Niveau 1 : Domaine de produits (Cloud / Outils de développement / Sécurité / Ingénierie des données)

* Niveau 2 : Nom du cours

* Niveau 3 : Type de ressource (vidéos / PDF / SCORM / Quizzes)

Chaque équipe produit a uniquement accès à son dossier de niveau 1. Trouver un quiz spécifique pour un cours spécifique signifie naviguer vers exactement le bon dossier de niveau 3 plutôt que de rechercher parmi des milliers de fichiers. Lorsque l&#39;équipe de sécurité met à jour un package SCORM, elle sait qu&#39;il réside dans Sécurité > [Nom du cours] > SCORM et qu&#39;elle ne peut pas atterrir accidentellement dans la branche d&#39;une autre équipe.

### Gestion des dossiers de contenu en tant qu’administrateur

En tant qu’administrateur dans Adobe Learning Manager, vous créez et gérez la hiérarchie des dossiers de contenu, contrôlez les rôles personnalisés qui ont accès à des dossiers spécifiques et gérez les noms de dossier et les suppressions. Les auteurs peuvent ajouter du contenu aux dossiers et organiser le contenu dans la hiérarchie, mais seuls les administrateurs peuvent créer, renommer ou supprimer des dossiers.

#### Créer un dossier de contenu

>[!NOTE]
>
>Deux dossiers au même niveau sous le même parent ne peuvent pas partager un nom. Le même nom est autorisé dans différentes branches ou à différents niveaux.

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Dans le volet de navigation de gauche, sélectionnez **Configurer** > **Paramètres**.
3. Dans la section **Avancé**, sélectionnez **Dossier de contenu**.
4. Sélectionnez **Ajouter** dans le coin supérieur droit de la page. La boîte de dialogue **Ajouter un nouveau dossier** s&#39;ouvre.
5. Saisissez un nom et une description facultative pour le dossier.
6. Sélectionnez **Enregistrer**. Le dossier est créé et apparaît dans la liste des dossiers.


#### Création d’un sous-dossier

1. Sur la page **Dossier de contenu**, recherchez le dossier parent.
2. Sélectionnez l&#39;option **Créer un sous-dossier** en regard du nom du dossier.
3. Saisissez un nom et une description facultative pour le sous-dossier.
4. Sélectionnez **Enregistrer**. Le sous-dossier apparaît en retrait sous son parent dans la liste des dossiers.

>[!NOTE]
>
>Chaque dossier peut contenir jusqu’à 25 sous-dossiers directs. Le niveau 3 correspond à la profondeur maximale. Vous ne pouvez pas créer de sous-dossier dans un dossier de niveau 3.

#### Renommer un dossier

1. Sur la page **Dossier de contenu**, sélectionnez le dossier que vous souhaitez renommer. Le dossier s’ouvre en mode édition.
2. Mettez à jour le nom du dossier et, si nécessaire, la description.
3. Sélectionnez **Enregistrer**. Le dossier est enregistré sous le nouveau nom.

#### Supprimer un dossier

Avant de supprimer, tenez compte des règles suivantes :

* Vous pouvez supprimer un dossier vide à n’importe quel niveau.
* Seuls les dossiers vides peuvent être supprimés. Les dossiers qui contiennent du contenu ne peuvent pas être supprimés, que le contenu soit lié à d’autres dossiers ou non.
* La suppression d’un dossier parent supprime tous ses sous-dossiers. La sélection d’un dossier parent sélectionne automatiquement tous ses enfants.

#### Supprimer le dossier parent

1. Sur la page **Dossier de contenu**, cochez la case en regard de chaque dossier que vous souhaitez supprimer.
2. Sélectionnez **Actions** > **Supprimer le dossier** dans le coin supérieur droit de la page.
3. Confirmez la suppression lorsque vous y êtes invité. Tous les sous-dossiers à l’intérieur des dossiers parents sont également supprimés.

#### Suppression d’un sous-dossier

1. Sur la page **Dossier de contenu**, cochez la case en regard du sous-dossier que vous souhaitez supprimer.
2. Sélectionnez **Actions** > **Supprimer le dossier** dans le coin supérieur droit de la page.
3. Confirmez la suppression lorsque vous y êtes invité. Le sous-dossier est supprimé.

>[!CAUTION]
>
>La suppression d’un dossier est définitive. Assurez-vous que tout le contenu du dossier a été déplacé vers un autre emplacement avant de confirmer.


#### Configuration de l’accès aux dossiers pour les rôles personnalisés

Vous pouvez restreindre les rôles personnalisés à des dossiers de niveau 1 spécifiques afin que les administrateurs personnalisés et les auteurs ayant ces rôles ne voient que le contenu qui les concerne.

L&#39;accès est défini au niveau du dossier **Niveau 1 uniquement**. Lorsque vous accordez à un rôle personnalisé l’accès à un dossier de niveau 1, ce rôle accède automatiquement à tous les sous-dossiers de niveau 2 et de niveau 3 qu’il contient. Vous ne pouvez pas attribuer l’accès au niveau du sous-dossier indépendamment.

1. Dans la navigation de gauche, sélectionnez **Utilisateurs** > **Rôles personnalisés**.
2. Ouvrez le rôle personnalisé que vous souhaitez configurer ou créez-en un nouveau.
3. Sous **Droits de compte**, recherchez la section **Dossiers de contenu**.
4. Sélectionnez **Dossiers sélectionnés**.
5. Sélectionnez les dossiers de niveau 1 auxquels ce rôle doit avoir accès.
6. Sélectionnez **OK**.

Les utilisateurs ayant ce rôle ne voient que le contenu des dossiers Niveau 1 sélectionnés et de leurs sous-dossiers. Le contenu d’autres dossiers privés et du dossier public reste inaccessible.

#### Bonnes pratiques

Les pratiques suivantes vous aident à créer une structure de dossiers qui évolue bien et reste facile à parcourir.

1. **Planifiez votre structure avant de créer des dossiers.** Une fois le contenu organisé selon une hiérarchie, la restructuration nécessite le déplacement de grands volumes de contenu. Choisissez des catégories de niveau 1, telles que les gammes de produits, les services ou les programmes de formation, avant de commencer.

2. **Utilisez trois niveaux pour des regroupements significatifs.** Une tendance commune est la suivante : Niveau 1 pour un domaine ou un programme général, Niveau 2 pour le type ou l’équipe de prestation, Niveau 3 pour les ressources individuelles. Par exemple :

   * Niveau 1 : formation commerciale

   * Niveau 2 : Modules individualisés

   * Niveau 3 : Ressources du PDF

3. **Les noms doivent être courts, descriptifs et uniques dans leur parent.** Évitez les noms génériques tels que « Module 1 » ou « Contenu ». Utilisez des identifiants adaptés aux auteurs qui parcourent la bibliothèque.

4. **Attribuer un accès au rôle personnalisé au niveau 1 uniquement.** L&#39;accès se propageant automatiquement en cascade, l&#39;affectation au niveau 1 est suffisante et simplifie la gestion de l&#39;accès. Vous n’avez pas besoin de mettre à jour l’accès lorsque vous ajoutez des sous-dossiers de niveau 2 ou 3.

5. **Déplacer le contenu avant de supprimer les dossiers.** Si un dossier contient du contenu qui n’est lié à aucun autre emplacement, la suppression est bloquée. Prenez l’habitude de vérifier le contenu des dossiers avant de les supprimer.


<!--

**Key points:**

A folder is a repository of content, which is a subset of the entire content library available in an account with the following properties:

* Only you (administrator) can create, edit, or delete a folder.
* You can control access to folders as part of defining roles only for custom administrators.
* Content must at all times be associated with at least one folder. To start with, all content will be associated with the public folder, which can later be changed.
* Content can be associated with multiple folders at the time of creation, which will also be possible by a copy operation
* All folder names must be unique within the account, otherwise there will be an error in naming a folder.

Folders only control visibility of content and don't create copies of content. Therefore, editing content will reflect in all the associated folders.

**Public folder**

A public folder is always present in an account and initially, all content will be part of this folder. Later, authors can move content out of this folder into other folders. A public folder has the following properties:

* All content associated with this folder will be accessible to all types of authors, by default.
* Any content that is a part of a public folder, cannot be part of any other folder. The converse also holds true.

This folder cannot be part of configurable role definition. Consequently, not having a public folder in configurable role definition doesn't restrict access to a public folder.

**Private folder**

Any folder created by you is a private folder.

**Add a content folder**

To add a content folder, follow the steps:

1. Select **[!UICONTROL Settings]** > **[!UICONTROL Content Folder]**.
2. Select **[!UICONTROL Add]** to create a new folder.
3. Type the name and description of the folder to be created.
 
    ![alt text](assets/advanced-settings-picture1.png)

4. Select **[!UICONTROL Save]** to create the folder.

**Folder operations**

* **[!UICONTROL Add a folder]**: To add a folder, select the folder, and then select **[!UICONTROL Add]** on the upper-right corner of the screen.
* **[!UICONTROL Delete a folder]**: To delete a folder, select the folder to delete, select the **[!UICONTROL Actions]** menu, and then select **[!UICONTROL Delete Folder]**.
-->

## Lieux de salles de classe

Créez et gérez une bibliothèque d’emplacements de salle de classe physique ou virtuelle. Ces emplacements peuvent être utilisés par les auteurs et les administrateurs pour configurer des événements de formation dirigée par un instructeur (ILT). Cette fonctionnalité garantit que les détails de la salle de classe, tels que les limites de places et les informations de localisation, sont préconfigurés et facilement accessibles.

Voir [Ajouter des emplacements de salle de classe dans Adobe Learning Manager](/help/migrated/administrators/feature-summary/classroom.md) pour plus d&#39;informations.

## Rapports

Cette section vous permet de configurer les tableaux de bord Conformité et Réussite du groupe.

![Texte optionnel](assets/advanced-settings-picture2.png)

Pour plus d’informations, voir les sections suivantes :

* [Tableau de bord Conformité](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Tableau de bord de réussite du groupe](/help/migrated/administrators/feature-summary/group-success-dashboard.md)
