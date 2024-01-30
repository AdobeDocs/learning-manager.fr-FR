---
jcr-language: en_us
title: Activer le contrôle complet du catalogue partagé
description: Activer le contrôle total du catalogue partagé dans Adobe Learning Manager
contentowner: saghosh
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 89%

---



# Activer le contrôle complet du catalogue partagé

## Créer un catalogue {#createcatalog}

En tant qu’administrateur, vous pouvez créer un catalogue de cours, de programmes d’apprentissage, d’assistances à la tâche et de certifications.

Pour plus d’informations, voir [Catalogues](/help/migrated/administrators/feature-summary/catalogs.md).

## Partager le catalogue {#sharecatalog}

Vous pouvez partager des catalogues avec les utilisateurs internes de l’entreprise ou avec tous les utilisateurs externes. Toutefois, le partage est exclusif. En d&#39;autres termes, un catalogue partagé en interne ne peut pas être partagé avec les groupes externes et vice versa.

Les cours, programmes d&#39;apprentissage, aides en ligne et les certifications sont les éléments de formation pris en charge pour le catalogue partagé.

Pour plus d’informations, voir [Partager des catalogues](/help/migrated/administrators/feature-summary/catalogs.md).

## Activer le contrôle complet du catalogue partagé {#fullcontrol}

Vous pouvez accorder un accès complet à votre catalogue aux comptes externes. L’administrateur du compte peut alors accepter le catalogue et peut en conséquence ajouter ou supprimer un/des apprentissage(s) ou des modules.

Pour autoriser le contrôle complet sur un compte externe,

1. Après avoir ajouté un/des apprentissage(s) à un catalogue, vous devez partager le catalogue avec des utilisateurs externes.
1. Dans la boîte de dialogue Compte externe, ajoutez le sous-domaine et l’ID de messagerie de l’administrateur de l’organisation externe.
1. Dans l’option Contrôle du catalogue, activez le bouton pour permettre un contrôle complet du catalogue par les utilisateurs externes.

   ![](assets/catalog-control.png)

   *Autoriser le contrôle total du catalogue partagé*

   Lorsque vous autorisez le contrôle complet du catalogue, l’administrateur de l’organisation externe accepte la demande autorisant les modifications du catalogue. L’auteur de l’organisation externe peut alors modifier les cours ou ajouter des modules.

   Voir les sections ci-dessous pour plus d’informations.

## Administrateur d’organisation externe {#administratorofexternalorganization}

Une fois que l’administrateur de l’organisation précédente a activé le contrôle complet du catalogue, l’administrateur de l’organisation externe accepte la demande, accepte le catalogue et l’affiche.

1. Cliquez sur l’icône de notification pour afficher la notification d’acceptation du catalogue.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Pour accepter l’invitation pour le catalogue, cliquez sur Accepter.
1. Dans la liste des catalogues, si vous lancez le catalogue qui a été partagé avec vous, vous pouvez voir un message indiquant que le catalogue dispose désormais d’un contrôle complet.

   ![](assets/catalog-details.png)

   *Afficher les détails du catalogue*

1. Vous pouvez modifier le nom du catalogue et sa description.

## Partager le catalogue pour un programme d’apprentissage, une certification et des assistances de tâche {#sharecatalogforlearningprogramcertificationandjobaids}

À l’instar du contrôle complet du catalogue pour les cours, l’administrateur peut également accorder un contrôle complet du catalogue pour les éléments suivants :

* Programmes d’apprentissage
* Certifications
* Assistances à la tâche

## Réinitialiser le cours {#resetcourse}

1. Sur la carte du catalogue dont le lien est rompu, cliquez sur **[!UICONTROL Réinitialiser le cours]**.

<!-- ![](assets/reset-course.png)-->

1. Vous voyez un message d’alerte après avoir cliqué sur le bouton Réinitialiser. Réinitialisation du cours :

   * Supprime tout le contenu nouvellement ajouté du catalogue.
   * Met à jour le catalogue en synchronisation avec le catalogue partagé d’origine.
   * Restaure la relation avec l’objet d’apprentissage parent.

   La réinitialisation du catalogue est irréversible. Vous ne pouvez pas annuler les modifications que vous avez apportées au catalogue.

1. Pour accepter les modifications, cliquez sur Oui.
1. Dans le catalogue de cours, vous pouvez constater que le catalogue ne contient plus le message *Lien rompu*.

   Lorsque vous affichez les détails du catalogue, vous pouvez constater que le catalogue est maintenant restauré dans son état d’origine.

## Ajouter à nouveau un objet d’apprentissage {#readdalearningobject}

Si vous avez supprimé un cours, un programme d’apprentissage, une certification ou une assistance à la tâche par inadvertance, vous pouvez le/la restaurer.

Pour restaurer un objet d’apprentissage supprimé, cliquez sur Ajouter à nouveau.

Cette action inverse l’action et restaure l’objet d’apprentissage dans la vue catalogue.

![](assets/re-add-button.png)

*Ajouter à nouveau un objet d’apprentissage*

Après avoir cliqué sur le bouton Ajouter à nouveau, un message de confirmation s’affiche pour indiquer que l’objet d’apprentissage a bien été ajouté au catalogue.

## Organisation externe {#externalorganization}

Une fois que l’administrateur du compte externe a accepté le catalogue, l’auteur peut désormais ajouter des cours et des programmes d’apprentissage.

1. En tant qu’utilisateur, vous recevez une notification indiquant que le catalogue est désormais disponible dans votre compte.
1. Pour voir la liste des cours, cliquez sur **[!UICONTROL Cours]** dans le volet de navigation de gauche. Vous pouvez afficher tous les cours créés par vous et partagés avec vous.
1. Pour voir les détails du cours, cliquez sur **[!UICONTROL Afficher les cours]** sur la carte de cours.

   <!--![](assets/view-course.png)-->

1. Sur la page des détails du cours, vous pouvez voir des informations sur le cours et les modules partagés. Pour ajouter un module, cliquez sur Ajouter des modules. Lorsque vous ajoutez des modules aux modules existants, les nouveaux modules apparaissent à la suite des modules existants. Vous pouvez toujours réorganiser les modules.
1. Après avoir ajouté les modules, cliquez sur Republier.

   Après avoir republié les modules, le message *Lien rompu* s’affiche sur la carte de catalogue.

   Comme vous avez mis à jour le catalogue d’origine avec de nouveaux modules, la relation existante avec le cours acquis n’existe plus.

   L’objet d’apprentissage ne sera pas synchronisé avec le compte source car le contenu de l’objet d’apprentissage a été modifié.

   <!--![](assets/link-broken.png)-->

Après avoir ajouté et republié le module, si vous pensez avoir ajouté ou supprimé un cours par inadvertance dans le catalogue précédemment, vous pouvez réinitialiser le module et rétablir son état d&#39;origine lorsqu&#39;il a été partagé pour la première fois avec un contrôle total.
