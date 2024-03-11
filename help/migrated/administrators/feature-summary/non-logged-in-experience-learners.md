---
title: Expérience hors connexion pour les élèves
description: Le portail natif d’Adobe Learning Manager prend en charge un mode d’accès non connecté au site de formation. Lorsque ce mode est activé, les élèves peuvent découvrir et accéder au site de formation et consulter divers cours et contenus disponibles. L’expérience hors connexion permet aux élèves de parcourir les cours sans être connectés à un portail.
exl-id: 12260cca-d2d2-4e7c-991d-9b09690d4c0a
source-git-commit: 1d36ad7f4b50d76f73eb1d24313ada78264e6ad3
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 41%

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

## API des élèves

Adobe Learning Manager - Les API des élèves vous permettent de créer une expérience d’apprentissage personnalisée pour vos utilisateurs. L’utilisation de ces API nécessite un jeton utilisateur valide et doit être utilisée uniquement dans le cadre des workflows où il y a un élève entièrement licencié/inscrit.

>[!IMPORTANT]
>
>Ils ne doivent pas être utilisés tels quels pour tout type de récupération de données afin de prendre en charge des utilisateurs/utilisateurs partagés non connectés ou tout autre cas de ce type. Pour créer une expérience sans tête ou AEM sans connexion, contactez-nous. Nous vous proposerons la bonne approche en fonction de vos besoins.

Les cas d’utilisation non enregistrés nécessitent une manipulation spéciale.

**Si vous avez des questions sur l&#39;utilisation appropriée de ces API, contactez l&#39;équipe en charge de l&#39;architecture de la solution et assurez-vous qu&#39;un architecte de solution a validé une solution avant de la déployer**.

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
