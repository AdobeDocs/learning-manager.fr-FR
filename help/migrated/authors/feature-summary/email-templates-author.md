---
description: Lisez cet article pour savoir comment configurer les modèles de courrier électronique pour les événements liés à tous les objets d’apprentissage.
jcr-language: en_us
title: Modèles de courriers électroniques
exl-id: 3b17f889-52be-4073-ab91-7c76dd79f1d2
source-git-commit: 6862dc1958a34a369f0e0e7218f28151a47beb3b
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 72%

---

# Modèles de courriers électroniques

Lisez cet article pour savoir comment configurer les modèles de courrier électronique pour les événements liés à tous les objets d’apprentissage.

L’application Learning Manager envoie des notifications par courrier électronique à plusieurs rôles utilisateurs sur la base d’événements.

En tant qu’auteur, vous pouvez personnaliser les modèles de courrier électronique en ajoutant ou en modifiant le contenu et en envoyant des notifications aux utilisateurs pour les différents événements déclenchés par les activités des élèves, des responsables et des auteurs. Vous pouvez, par exemple, envoyer un courrier électronique personnalisé à chaque fois qu’un élève s’inscrit à votre cours. Lors de l’inscription, l’élève reçoit automatiquement le courrier électronique spécifique au cours.

Vous pouvez également choisir de ne pas envoyer de notifications par courrier électronique pour certains événements en désactivant l’option de modèle de courrier électronique.

## Configuration des notifications par e-mail {#settingemailnotifications}

1. Dans l’application d’auteur, sélectionnez l’objet d’apprentissage pour lequel vous souhaitez configurer le modèle de courrier électronique. Par exemple, Cours.

1. Dans la page Objet d’apprentissage, cliquez sur le cours, la certification ou le programme d’apprentissage pour configurer les paramètres de courrier électronique.

1. Dans la page de détails de l’objet d’apprentissage, sélectionnez **Modèles de courrier électronique** > **Tous les modèles**. Des modèles de courrier électronique sont disponibles pour **Instance par défaut** et **Cours actuel**. Vous pouvez basculer entre eux à l’aide de la liste déroulante dans le coin supérieur droit.

   Vous pouvez afficher la liste des modèles disponibles pour l’objet d’apprentissage que vous avez sélectionné.

   ![](assets/email-templates-forlearningprograms.png)
   *Liste des modèles*

1. Cliquez sur le nom de l’événement pour visualiser le modèle en mode Aperçu.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Voir Aperçu du modèle*

   Vous pouvez personnaliser chaque modèle en cliquant sur le texte du corps du modèle. Vous pouvez insérer des variables dans le texte en cliquant sur les icônes appropriées comme indiqué dans l’instantané. Placez le pointeur au-dessus de chaque icône pour afficher les noms.

   ![](assets/insert-variable.png)
   *Insertion d’une variable*

   Les variables suivantes sont disponibles :

   * LPName
   * LPCompletionDeadline
   * LearnerName
   * LearnerEmail
   * CourseName
   * CourseDescription
   * CourseCompletionDeadline
   * CourseSkillDetails
   * CourseBadge

   Vous pouvez réinitialiser le contenu par défaut du message en cliquant sur le lien Rétablir l’original situé au-dessus du modèle.

   Comme vous le voyez en haut du modèle, vous pouvez le personnaliser pour plusieurs rôles (Responsable, Élève, etc.) selon le type de notification par e-mail.

1. Cliquez sur Enregistrer au bas de la page des modèles.
1. Dans la page de modèles de courrier électronique, cliquez sur le bouton bascule circulaire Oui/Non pour envoyer ou désactiver la notification.

![](assets/email-notification-e1437624109719.png)
*Activer ou désactiver la notification par e-mail*

Si le cercle dans le bouton de notification en regard de chaque nom d’événement est adjacent à Oui (avec un arrière-plan de nuance bleue), la notification est activée. Si l’arrière-plan est de nuance grise et le cercle est adjacent à Non, la notification est désactivée.

À chaque fois que vous configurez un modèle de courrier électronique au niveau du cours, il est prioritaire sur les paramètres de niveau administrateur pour le cours en question.

## Paramètres du modèle d’e-mail

L’auteur peut configurer les éléments suivants dans les paramètres du modèle de courrier électronique :

* **Bannière d’e-mail**: permet de modifier la bannière de l’e-mail.

* **Signature électronique**: permet d’ajouter ou de modifier la signature électronique.
