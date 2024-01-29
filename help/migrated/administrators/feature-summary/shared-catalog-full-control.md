---
jcr-language: en_us
title: Activer le contrôle total du catalogue partagé
description: Activer le contrôle total du catalogue partagé dans Adobe Learning Manager
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---



# Activer le contrôle total du catalogue partagé

## Créer un catalogue {#createcatalog}

En tant qu’administrateur, vous pouvez créer un catalogue de cours, de programmes d’apprentissage, d’assistances à la tâche et de certifications.

Pour plus d’informations, voir [Catalogues](/help/migrated/administrators/feature-summary/catalogs.md).

## Partager le catalogue {#sharecatalog}

Vous pouvez partager les catalogues avec les utilisateurs internes d’une organisation ou avec des utilisateurs externes. Cependant, le partage est exclusif. En d’autres termes, un catalogue partagé en interne ne peut pas être partagé avec des groupes externes et vice versa.

Les cours, les programmes d’apprentissage, les assistances à la tâche et les certifications sont les objets d’apprentissage pris en charge pour le catalogue partagé.

Pour plus d’informations, voir [Partage de catalogues](/help/migrated/administrators/feature-summary/catalogs.md).

## Activer le contrôle total du catalogue partagé {#fullcontrol}

Vous pouvez accorder un accès complet à votre catalogue aux comptes externes. L’administrateur du compte peut alors accepter le catalogue et ajouter ou supprimer des apprentissages ou des modules en conséquence.

Pour accorder le contrôle total à un compte externe,

1. Après avoir ajouté des formations à un catalogue, vous devez partager le catalogue avec des utilisateurs externes.
1. Dans la boîte de dialogue Compte externe, ajoutez le sous-domaine et l’ID de messagerie de l’administrateur de l’organisation externe.
1. Dans l&#39;option Contrôle du catalogue, basculez le bouton pour permettre le contrôle total du catalogue pour les utilisateurs externes.

   ![](assets/catalog-control.png)

   *Autoriser le contrôle total du catalogue partagé*

   Lorsque vous autorisez le contrôle complet du catalogue, l’administrateur de l’organisation externe accepte la demande d’autorisation de modifications du catalogue. L’auteur de l’organisation externe peut ensuite modifier les cours ou ajouter des modules.

   Voir les sections ci-dessous pour plus d’informations.

## Administrateur d’une organisation externe {#administratorofexternalorganization}

Une fois que l’administrateur de l’organisation précédente a activé le contrôle total du catalogue, l’administrateur de l’organisation externe accepte la demande, accepte le catalogue et l’affiche.

1. Cliquez sur l’icône de notification pour afficher la notification d’acceptation du catalogue.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Pour accepter l’invitation pour le catalogue, cliquez sur Accepter.
1. Dans la liste des catalogues, si vous lancez le catalogue qui a été partagé avec vous, un message vous informe que le catalogue a désormais le contrôle total.

   ![](assets/catalog-details.png)

   *Afficher les détails du catalogue*

1. Vous pouvez modifier le nom du catalogue et la description.

## Partager le catalogue pour le programme d’apprentissage, la certification et les assistances à la tâche {#sharecatalogforlearningprogramcertificationandjobaids}

Comme pour le contrôle de catalogue complet des cours, l&#39;administrateur peut également accorder le contrôle de catalogue complet pour les éléments suivants :

* Programmes d’apprentissage
* Certifications
* Assistances à la tâche

## Réinitialiser le cours {#resetcourse}

1. Sur la carte du catalogue dont le lien est rompu, cliquez sur **[!UICONTROL Réinitialiser le cours]**.

<!-- ![](assets/reset-course.png)-->

1. Un message d’alerte s’affiche lorsque vous cliquez sur le bouton Réinitialiser. Réinitialisation du cours :

   * Supprime tout le contenu nouvellement ajouté du catalogue.
   * Met à jour le catalogue synchronisé avec le catalogue partagé d’origine.
   * Restaure la relation avec l’objet d’apprentissage parent.

   La réinitialisation du catalogue est irréversible. Vous ne pouvez pas annuler les modifications que vous avez apportées au catalogue.

1. Pour accepter les modifications, cliquez sur Oui.
1. Sur le Catalogue de cours, vous pouvez voir que le catalogue ne contient pas le message *Lien rompu* plus.

   Lorsque vous affichez les détails du catalogue, vous pouvez voir que le catalogue est maintenant restauré à son état d’origine.

## Ajout d’un nouvel objet d’apprentissage {#readdalearningobject}

Si vous avez supprimé un cours, un programme d’apprentissage, une certification ou une assistance à la tâche par inadvertance, vous pouvez le restaurer.

Pour restaurer un objet d&#39;apprentissage supprimé, cliquez sur Ajouter à nouveau.

Cette action annule l’action et restaure l’objet d’apprentissage dans la vue du catalogue.

![](assets/re-add-button.png)

*Ajouter à nouveau un objet d’apprentissage*

Après avoir cliqué sur le bouton Rajouter, un message de confirmation s’affiche pour confirmer que l’objet d’apprentissage a été ajouté avec succès au catalogue.

## Organisation externe {#externalorganization}

Une fois que l’administrateur du compte externe a accepté le catalogue, l’auteur peut désormais ajouter des cours et des programmes d’apprentissage.

1. En tant qu’utilisateur, vous recevez une notification indiquant que le catalogue est désormais disponible dans votre compte.
1. Pour afficher la liste des cours, cliquez sur **[!UICONTROL Cours]** dans le volet de navigation de gauche. Vous pouvez voir tous les cours que vous avez créés et partagés avec vous.
1. Pour afficher les détails du cours, cliquez sur **[!UICONTROL Afficher le cours]** sur la carte du cours.

   <!--![](assets/view-course.png)-->

1. Dans la page de détails du cours, vous pouvez voir des informations sur le cours et les modules partagés. Pour ajouter un module, cliquez sur Ajouter des modules. Lorsque vous ajoutez des modules aux modules existants, les nouveaux modules apparaissent à la fin des modules existants. Vous pouvez toujours réorganiser les modules.
1. Après avoir ajouté les modules, cliquez sur Republier.

   Après avoir republié les modules, un message s’affiche sur la carte du catalogue *Lien rompu*.

   Étant donné que vous avez mis à jour le catalogue d&#39;origine avec de nouveaux modules, la relation existante avec le cours acquis n&#39;existe plus.

   L&#39;objet d&#39;apprentissage ne sera plus synchronisé avec le compte source, car son contenu a été modifié.

   <!--![](assets/link-broken.png)-->

Après avoir ajouté et republié le module, si vous pensez avoir ajouté ou supprimé un cours par inadvertance dans le catalogue précédemment, vous pouvez réinitialiser le module et rétablir son état d&#39;origine lorsqu&#39;il a été partagé pour la première fois avec un contrôle total.
