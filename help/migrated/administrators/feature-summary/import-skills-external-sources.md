---
jcr-language: en_us
title: Importation de compétences à partir de sources externes
description: Importez des compétences à partir de fournisseurs de contenu, tels que LinkedIn et Go1, à l’aide des connecteurs respectifs.  Les compétences importées seront ajoutées aux compétences définies par l’administrateur dans Learning Manager et seront disponibles pour les auteurs pendant le processus de création du cours.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: 260b413b7bb739dc57504df57a6bd2d6a35df161
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Importation de compétences à partir de sources externes

Importez des compétences à partir de fournisseurs de contenu, tels que LinkedIn et Go1, à l’aide des connecteurs respectifs. Cette amélioration fait partie de l&#39;objectif visant à renforcer la capacité de Learning Manager à s&#39;intégrer à des systèmes externes de gestion des compétences et des nuages. Les compétences importées seront ajoutées aux compétences définies par l’administrateur dans Learning Manager et seront disponibles pour les auteurs pendant le processus de création du cours. Des améliorations ont également été apportées à la fonctionnalité de recherche de compétences sur toute la plateforme afin de fournir une meilleure expérience de recherche lorsque le compte a un grand nombre de compétences.

## Configuration de l’importation de compétences

Suivez les étapes de la procédure pour activer l’importation de compétences dans le compte.

1. Dans l&#39;application Administration, sélectionnez **Paramètres** dans le volet de gauche.
1. Sélectionnez **Général**.
1. Dans la section **Importation de compétences**, sélectionnez **Activer**. Si cette option est activée, vous pouvez choisir une source externe pour importer les compétences. Une fois activées, pour toutes les importations suivantes de ressources d’apprentissage, les compétences seront importées dans le référentiel de compétences pour les éléments nouvellement importés. Les compétences des ressources d’apprentissage existantes peuvent être importées dans le référentiel de compétences une seule fois. Pour exécuter cette exécution initiale, contactez votre CSM.
1. Sélectionnez un fournisseur de contenu dans la liste déroulante.

En tant qu’administrateur, vous ne pouvez importer des compétences qu’à partir d’une seule source de compétences.

### Niveau de compétence par défaut

Le niveau de compétence par défaut est un et le crédit est de 10 après la migration des compétences. Un administrateur ultérieur peut modifier le crédit.

Vous ne pouvez pas modifier le nom de la compétence, la description et ajouter des niveaux aux compétences externes. Vous pouvez toutefois ajouter un domaine, des badges et modifier des crédits.

### Compétences et crédits de cours par défaut

Après avoir importé des compétences, elles sont ajoutées aux ressources d’apprentissage importées à partir de la source qui a été sélectionnée en tant que source de compétences. Par exemple, si votre source de compétences était LinkedIn Learning, toutes les ressources d’apprentissage importées à partir de LinkedIn Learning auront les compétences qu’elle fournit. Lorsqu’elles sont importées dans les ressources d’apprentissage, chaque ressource d’apprentissage donne une valeur par défaut de 10 crédits.

#### Rapports

La colonne **Source** avec des valeurs - Interne, LinkedIn Learning, Go1, qui indique la source de l’importation des compétences.

Les compétences récemment ajoutées figureront en tête de liste.

Sur la page des paramètres du cours, la colonne **Attribué par** contient des valeurs, Interne et Fournisseur de contenu.


## Workflow d’administration de l’intégration

L’administrateur d’intégration charge les fichiers CSV (compétence, niveau de compétence et cours), puis migre les cours vers le compte. Par exemple, une fois que l’administrateur a sélectionné LinkedIn Learning, l’administrateur de l’intégration peut planifier une activité dans laquelle les compétences et les niveaux sont importés dans Adobe Learning Manager.

## Exportation des compétences

En tant qu’administrateur,

1. Sélectionnez **Compétences** dans le volet de gauche.
1. Sélectionnez la source de n’importe quelle compétence. Vous pouvez afficher les cours, les assistances à la tâche, les élèves inscrits et les instructeurs du cours.

### Modification d’une compétence

Sélectionnez une compétence. Dans la fenêtre contextuelle **Modifier une compétence**, vous ne pouvez pas modifier le nom et la description de la compétence. Vous pouvez toutefois ajouter des domaines de compétence et un badge pour la compétence.
