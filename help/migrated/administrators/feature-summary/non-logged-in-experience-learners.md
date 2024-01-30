---
title: Expérience hors connexion pour les élèves
description: Le portail natif d’Adobe Learning Manager prend en charge un mode d’accès non connecté au site de formation. Lorsque ce mode est activé, les élèves peuvent découvrir et accéder au site de formation et consulter divers cours et contenus disponibles. L’expérience hors connexion permet aux élèves de parcourir les cours sans être connectés à un portail.
source-git-commit: aef2dfe9d6f49dcccaf1f71b57ffa25a3075efe8
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 54%

---

# Expérience hors connexion pour les élèves

Le portail natif d’Adobe Learning Manager prend en charge un mode d’accès non connecté au site de formation. Lorsque ce mode est activé, les élèves peuvent découvrir et accéder au site de formation et consulter divers cours et contenus disponibles.

L’expérience hors connexion permet aux élèves de parcourir les cours sans être connectés à un portail.

Pour que la page d’accueil hors connexion soit activée, l’administrateur de l’intégration doit activer et configurer le [Connecteur de données de formation](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access).

La formation peut ensuite être exportée à partir du connecteur.

>[!NOTE]
>
>Assurez-vous que l’option Native Learning Manager est sélectionnée.

L’administrateur peut modifier et configurer la page d’accueil, qui est destinée aux utilisateurs non connectés.

## Lancer les options de la page d’accueil

Sur la page d’accueil d’Adobe Learning Manager, sélectionnez **Branding**. Ensuite, dans le volet de gauche, sélectionnez Page d’accueil non connectée.

![options de la page d’accueil](assets/non-logged-in-homepage.png)

*Sélectionnez l’option Page d’accueil non connectée*

## Ajouter une bannière

Ajoutez une bannière pour n’importe quelle annonce marketing ou présentez le sujet tendance du jour. Sélectionner **Ajouter une bannière**.

![bannière](assets/add-banner-image.png)

*Ajouter une bannière*

Accédez à l’emplacement de l’image à utiliser comme bannière. Fournissez ensuite un lien sous forme de bouton d’action sur l’image de bannière.

## Ajouter des catégories

Ce composant peut être utilisé pour filtrer le catalogue par balises, compétences et catalogue. Cette section contient un en-tête et une description pour chaque catégorie. Après avoir cliqué, l’utilisateur est redirigé vers la page du catalogue avec les filtres appliqués.

Sélectionner **[!UICONTROL Ajouter une catégorie]**. Saisissez ensuite les détails de la catégorie.

![ajouter une catégorie](assets/add-category.png)

*Ajout des catégories*

Enregistrez la catégorie. La catégorie est ajoutée à la section.

## Ajouter un catalogue

Ajoutez un catalogue pour les utilisateurs non connectés afin qu’ils puissent parcourir toutes les formations sur la plateforme.

![ajouter un catalogue](assets/add-catalog.png)

*Ajouter un catalogue*

Toutes les formations exportées seront présentes.

## Fonctionnalités non prises en charge

* Les assistances à la tâche ne seront pas exportées. Cependant, les élèves peuvent les voir après s’être connectés.
* Trier par dans le composant de catalogue.
* Paramètre d’affichage par défaut utilisé dans l’application d’administration (Paramètres > Général > Mode Liste).
* Évaluation par étoiles/efficacité.
* Paramètre d’icône de carte.
* Définition des compétences et des balises pertinentes.
* Vue de l&#39;application de l&#39;élève affichée dans le catalogue.
* Pages de présentation de la formation : cliquez sur la carte pour rediriger vers Inscription, après quoi un utilisateur est redirigé vers la page de présentation de la formation/page d’instance.
* Tous les catalogues activés seront présents. Tout élève n’ayant pas accès à un catalogue ne peut pas le voir ni y suivre la formation après s’être connecté.
