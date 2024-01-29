---
description: Lisez cet article pour savoir comment configurer les modèles de courrier électronique pour les événements liés à tous les objets d’apprentissage.
jcr-language: en_us
title: Modèles de courrier électronique
source-git-commit: fda58bc18bee6d21ee904a442884e4759587d053
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---



# Modèles de courrier électronique

Lisez cet article pour savoir comment configurer les modèles de courrier électronique pour les événements liés à tous les objets d’apprentissage.

L’application Learning Manager envoie des notifications par e-mail à plusieurs rôles d’utilisateurs en fonction des événements.

En tant qu&#39;auteur, vous pouvez personnaliser les modèles de courrier électronique en ajoutant ou modifiant le contenu et en envoyant des notifications aux utilisateurs pour divers événements déclenchés par les élèves, les responsables et les activités d&#39;auteur. Par exemple, vous pouvez envoyer un e-mail personnalisé chaque fois qu’un élève s’inscrit à votre cours. Lors de l’inscription, l’élève reçoit automatiquement l’e-mail spécifique au cours.

Vous pouvez également choisir de ne pas envoyer de notifications par courrier électronique pour certains événements en désactivant l’option de modèle de courrier électronique.

## Définition des notifications par e-mail {#settingemailnotifications}

1. Dans l’application d’auteur, cliquez sur l’objet d’apprentissage pour lequel vous souhaitez configurer le modèle de courrier électronique. Par exemple, Cours.
1. Dans la page Objet d’apprentissage, cliquez sur le cours, la certification ou le programme d’apprentissage que vous souhaitez configurer dans les paramètres de messagerie.
1. Dans la page de détails de l&#39;objet d&#39;apprentissage, cliquez sur Modèles de courrier électronique.

   La liste des modèles disponibles pour l&#39;objet d&#39;apprentissage que vous avez choisi s&#39;affiche.

   ![](assets/email-templates-forlearningprograms.png)
   *Liste des modèles*

1. Cliquez sur le nom de l’événement pour afficher le modèle en mode Aperçu.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Voir Aperçu du modèle*

   Vous pouvez personnaliser chaque modèle en cliquant sur le texte dans son corps. Vous pouvez insérer des variables dans le texte en cliquant sur les icônes appropriées, comme indiqué dans l’instantané. Passez le curseur de la souris sur chaque icône pour afficher les noms.

   ![](assets/insert-variable.png)
   *Insertion d’une variable*

   Les variables suivantes sont disponibles :

   * Nom LPN
   * LPCcompleteDeadline
   * LearnerName
   * E-mail de l’élève
   * CourseName
   * CourseDescription
   * CourseCompletionDeadline
   * CourseSkillDetails
   * CourseBadge

   Vous pouvez réinitialiser le contenu par défaut du message en cliquant sur le lien Revenir à l’original situé au-dessus du modèle.

   Comme vous le voyez en haut du modèle, vous pouvez le personnaliser pour plusieurs rôles (Responsable, Élève, etc.) selon le type de notification par e-mail.

1. Cliquez sur Enregistrer au bas de la page des modèles.
1. Dans la page Modèles de courrier électronique, cliquez sur le bouton bascule circulaire Oui/Non pour envoyer ou désactiver la notification.

![](assets/email-notification-e1437624109719.png)
*Activer ou désactiver la notification par e-mail*

Si le cercle du bouton de notification en regard de chaque nom d’événement est adjacent à Oui (avec une nuance bleue en arrière-plan), la notification est activée. S’il est dans l’ombre grise et que le cercle est adjacent à Non, la notification est désactivée.

Chaque fois que vous configurez un modèle de courrier électronique au niveau du cours, il est prioritaire sur les paramètres de niveau administrateur pour ce cours particulier.
