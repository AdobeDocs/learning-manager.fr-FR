---
description: Lisez cet article pour apprendre à gérer les modules en tant qu’instructeur dans Learning Manager.
jcr-language: en_us
title: Modules
contentowner: shhivkum
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 0%

---



# Modules

Lisez cet article pour apprendre à gérer les modules en tant qu’instructeur dans Learning Manager.

## Afficher la présentation de la session {#viewsessionoverview}

1. Dans le volet de gauche, cliquez sur Session à venir.
1. Dans la liste de vos sessions à venir, sélectionnez la session dont vous souhaitez afficher les détails.

   L’application affiche la vue d’ensemble de la session avec des détails tels que le nom de la session, le lieu, les horaires, la limite d’inscription, la limite de liste d’attente, etc.

   ![](assets/upcomingsessions.png)
   *Afficher les sessions à venir*

## Configurer les détails de la session {#configuresessiondetails}

1. Dans le volet de gauche, cliquez sur Session à venir.
1. Sélectionnez la session à mettre à jour.
1. Cliquez sur Modifier dans le coin supérieur droit.

   ![](assets/sessiondetails.png)
   *Configurer les détails de la session*

1. Dans la page Présentation de la session, vous pouvez modifier les horaires, la date, le lieu, etc. de la session. Vous pouvez également modifier ou ajouter les détails de session suivants :

   * Spécifiez la limite d’inscription pour définir le nombre maximal d’élèves autorisés pour la session.
   * Spécifiez la limite de liste d’attente si vous souhaitez définir le nombre maximal d’élèves autorisés sur la liste d’attente pour la session.
   * Dans le champ Autoriser les envois, sélectionnez Oui pour permettre aux élèves d’envoyer des devoirs. Si vous sélectionnez Non, les élèves ne peuvent pas charger de soumissions d’affectation pour la session.

   ![](assets/editsessiondetails.png)
   *Modifier les détails de la session*

1. Cliquez sur Enregistrer.

   Vous ne pouvez pas modifier le champ Instructeur à partir de cette page.

## Charger des fichiers de ressources pour votre session {#uploadresourcefilesforyoursession}

En tant qu’instructeur, vous pouvez charger des fichiers de ressources tels que des fichiers d’affectation ou des présentations pour les modules, ou encore des fichiers d’activité pour le module. Utilisez le menu Ressources pour ajouter des fichiers de ressources pour votre module ou votre session.

1. Dans l’application Instructeur, cliquez sur Sessions à venir > Ressources.

   Vous pouvez afficher la page Ressources, qui contient déjà un lien vers les ressources que les auteurs ont peut-être chargées pour le cours associé à votre module. En outre, les instructeurs peuvent également charger des fichiers de ressources pour les modules.

1. Cliquez sur Ajouter.

   ![](assets/addresource.png)
   *Ajouter une ressource pour la session*

1. Accédez au fichier approprié sur votre ordinateur. Sélectionnez le fichier, puis cliquez sur Ouvrir.
1. Une fois le fichier chargé, vous pouvez le voir avec la date à laquelle il a été ajouté.

   Les élèves inscrits à ce module peuvent voir vos fichiers une fois qu&#39;ils ont été chargés, dans la section Ressources sous Cours.

   Pour supprimer un fichier de ressources, sélectionnez le ou les fichiers à supprimer. Cliquez sur Actions > Supprimer le fichier dans la page Ressources.

## Envoi de fichiers pour les modules d’activité {#filesubmissionforactivitymodules}

Le module d’activité prend en charge le workflow d’envoi de fichier. En tant qu’auteur, créez un module d’activité et sélectionnez  **[!UICONTROL Envoi de fichier]** option. Cela permet aux élèves d’envoyer un fichier.

Ces fichiers peuvent être approuvés/rejetés par les instructeurs du module. Le module n’est terminé qu’une fois que l’instructeur a approuvé l’envoi.

![](assets/activity-modules.png) ![](assets/approve-reject-option.png)
*Approuver ou rejeter des fichiers*

## Évaluer le module de liste de contrôle {#evaluate-checklist-module}

Une fois que l’élève a suivi le cours, l’instructeur voit le module de liste de contrôle sur la page Envois/listes de contrôle dans le panneau **Modules** section. Cette page contient tous les modules de liste de contrôle d&#39;activité ainsi que les modules d&#39;envoi d&#39;activité pour lesquels des révisions sont attendues. Pour chaque module, le nombre d&#39;élèves pour lesquels l&#39;évaluation est attendue s&#39;affiche.

Sur la page ci-dessous, vous pouvez voir les modules de type **Soumission** et **Liste de contrôle**. Pour cet exemple, nous allons utiliser le module Liste de contrôle.

![](assets/modules-list.png)
*Afficher la liste des modules*

Cliquez sur le module Liste de contrôle. Sur la **Liste de contrôle** , vous voyez les éléments suivants :

* Nom du module
* Nom du cours
* Instance à laquelle le cours appartient
* Critères de réussite définis par l’auteur
* Nombre de questions de la liste de contrôle

![](assets/checklist-page.png)
*Afficher la page de liste de contrôle*

Pour évaluer un élève, cliquez sur **[!UICONTROL Évaluer]** dans le **[!UICONTROL Liste de contrôle]** colonne. Vous pouvez également voir que l’état de la révision est **En attente**.

Évaluez l’élève et cliquez sur **[!UICONTROL Envoyer]**. En tant qu&#39;instructeur, vous devez répondre à toutes les questions d&#39;évaluation.

![](assets/checklist-evaluation-screen.png)
*Liste de contrôle pour l&#39;évaluation*

Selon les critères de réussite, le statut sera soit Échec, soit Réussite.

Une liste de contrôle, une fois évaluée, ne peut pas être réévaluée.

Un instructeur peut également afficher les réponses soumises par d’autres instructeurs du module.

Vous pouvez exporter les élèves au format csv en fonction du filtre de recherche appliqué.

Une fois que l’instructeur a évalué le cours à l’aide de la liste de contrôle, l’élève voit le statut du module comme **Réussite** et le statut du cours en tant que **Terminé** ou l&#39;état du module comme **Échec**, et statut du cours en tant que **Terminé**.

## Commentaires de l’instructeur pour le rejet d’une activité {#rejection-comments}

Un élève peut voir le commentaire d’un instructeur dans la notification envoyée pour rejet. L’élève peut ensuite renvoyer l’accord en fournissant plus d’informations sous forme de commentaires.

Voici le workflow :

1. Un auteur crée un cours avec un module d&#39;activité, affecte un instructeur, puis publie le cours.

1. Un élève suit le cours et, après l’avoir terminé, soumet un justificatif d’accomplissement.

   ![](assets/proof-of-completion.png)
   *Soumettre un justificatif d’accomplissement*

1. L’instructeur sélectionne ensuite le module d’activité qui lui est attribué. Dans la page Soumissions du module, l’instructeur clique sur **Modifier**. Il peut ensuite saisir les commentaires pour rejet et activer l’option Afficher le commentaire, afin que l’élève puisse afficher le commentaire dans la notification.

   ![](assets/enter-comments.png)
   *Saisir des commentaires d’achèvement*

1. L’instructeur peut cliquer sur **Rejeter**. Le statut de la soumission passe à **Marqué pour rejet**.

   ![](assets/marked-for-rejection.png)
   *Rejeter une soumission*

1. Après l’envoi, l’état passe à **Refusé**.

   ![](assets/rejected-status.png)
   *Afficher le statut de rejet*

1. L’élève reçoit désormais une notification indiquant que son envoi a été rejeté. Les commentaires de l’instructeur apparaissent également dans la notification.

   ![](assets/notification-of-rejection.png)
   *Réception d’une notification de rejet*

Pour tenir compte des modifications, l’Adobe a mis à jour le modèle de courrier électronique pour **Envoi refusé**.

## Ajouter des scores et des commentaires pour les modules d’activité {#addscoresandcommentsforactivitymodules}

Pour ajouter des scores et des commentaires pour les modules d&#39;activité qui ont été envoyés pour soumission, procédez comme suit :

1. Dans le volet de gauche, cliquez sur **[!UICONTROL Élève]**.

   ![](assets/learners.png)
   *Sélectionner un élève*

1. Dans la page de l’élève, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Modifier les scores et les commentaires]**.

   ![](assets/edit-scores-comments.png)
   *Ajouter des commentaires*

   Pour les élèves qui n’ont pas terminé le cours, le champ de saisie Score et commentaires ne s’affiche pas.

   ![](assets/editing-scores-andcomments.png)
   *Modifier les notes et les commentaires*

1. Cliquez sur **[!UICONTROL Enregistrer]**.
