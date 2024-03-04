---
jcr-language: en_us
title: Importation de compétences à partir de sources externes
description: Importez des compétences à partir de fournisseurs de contenu, tels que LinkedIn et Go1, à l’aide des connecteurs respectifs.  Les compétences importées seront ajoutées aux compétences définies par l’administrateur dans Learning Manager et seront disponibles pour les auteurs pendant le processus de création du cours.
contentowner: saghosh
source-git-commit: fc77dad8f39d6d29c8ec74eb5ba137bf12ab7f8c
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# Importation de compétences à partir de sources externes

Importez des compétences à partir de fournisseurs de contenu, tels que LinkedIn et Go1, à l’aide des connecteurs respectifs. Cette amélioration fait partie de l&#39;objectif visant à renforcer la capacité de Learning Manager à s&#39;intégrer à des systèmes externes de gestion des compétences et des nuages. Les compétences importées seront ajoutées aux compétences définies par l’administrateur dans Learning Manager et seront disponibles pour les auteurs pendant le processus de création du cours. Des améliorations ont également été apportées à la fonctionnalité de recherche de compétences sur toute la plateforme afin de fournir une meilleure expérience de recherche lorsque le compte a un grand nombre de compétences.

## Configuration de l’importation de compétences

Suivez les étapes de la procédure pour activer l’importation de compétences dans le compte.

1. Dans l’application d’administration, sélectionnez **Paramètres** dans le volet de gauche.
1. Sélectionner **Généralités**.
1. Dans le panneau **Importation des compétences** section, sélectionner **Activer**. Si cette option est activée, vous pouvez choisir une source externe à importer **Compétences**. Les compétences des ressources d’apprentissage existantes seront importées dans le référentiel de compétences une seule fois lors de l’exécution initiale. Pour toutes les importations ultérieures de ressources d’apprentissage, les compétences seront importées dans le référentiel de compétences uniquement pour les éléments nouvellement importés.
1. Sélectionnez un fournisseur de contenu dans la liste déroulante.

## Workflow d’administration de l’intégration

L’administrateur d’intégration charge les fichiers CSV (compétence, niveau de compétence et cours), puis migre les cours vers le compte. Par exemple, une fois que l’administrateur a sélectionné LinkedIn Learning, l’administrateur d’intégration peut planifier une activité dans laquelle les compétences et les niveaux sont importés dans Adobe Learning Manager.

## Exportation des compétences

En tant qu’administrateur,

1. Sélectionner **Compétences** dans le volet de gauche.
1. Sélectionnez la source de n’importe quelle compétence. Vous pouvez afficher les cours, les assistances à la tâche, les élèves inscrits et les instructeurs du cours.

### Modification d’une compétence

Sélectionnez une compétence. Dans le panneau **Modifier une compétence** dans la fenêtre contextuelle, vous ne pouvez pas modifier le nom et la description de la compétence. Vous pouvez toutefois ajouter des domaines de compétence et un badge pour la compétence.