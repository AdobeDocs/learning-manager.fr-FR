---
jcr-language: en_us
title: Annonce
description: Une annonce est un message multimédia (texte, image ou vidéo) qu’un administrateur diffuse pour un ensemble défini d’utilisateurs.
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1018'
ht-degree: 0%

---



# Annonce

Une annonce est un message multimédia (texte, image ou vidéo) qu’un administrateur diffuse pour un ensemble défini d’utilisateurs.

L&#39;administrateur peut diffuser des annonces aux élèves les informant de l&#39;occurrence d&#39;un événement ou d&#39;une activité. L’annonce peut être une combinaison de texte, d’images ou de vidéos. Vous pouvez lier des objets d&#39;apprentissage tels que des cours, des programmes d&#39;apprentissage et des certifications à une annonce.

Il existe quatre types d&#39;annonces :

* Notification
* En-tête
* Recommandation
* E-mail

## Notification {#notification}

1. En tant qu&#39;utilisateur administrateur, cliquez sur Annonces dans le volet de gauche.
1. Cliquez sur Ajouter dans le coin supérieur droit de la page.
1. Dans la liste déroulante Type, sélectionnez l’option **Notification As**.
1. Dans le champ Message, ajoutez le message pour l’annonce. Vous pouvez également ajouter une URL pour les annonces ici. Cependant, vous devez ajouter l’URL dans le formulaire par HTML.

   Par exemple,  `code <a href="http://www.w3schools.com" target="_blank">Visit W3Schools</a>.`

   Lorsque vous spécifiez la cible comme vide, puis lorsqu’un utilisateur clique sur l’URL de l’annonce, le lien s’ouvre dans un nouvel onglet. Si vous ne spécifiez pas la cible, le lien s’ouvre dans le même navigateur.

1. Ajoutez éventuellement des pièces jointes telles que des images ou des fichiers vidéo pour l’annonce.
1. Choisissez les groupes d’utilisateurs cibles ou les objets d’apprentissage cibles. Vous ne pouvez choisir qu’une seule option pour une annonce.

   Commencez à saisir le nom du groupe d’utilisateurs dans la zone de texte et faites votre choix dans la liste déroulante. De même, choisissez la formation en saisissant le nom de l’objet dans la zone de texte.

1. Cliquez sur Paramètres avancés dans la boîte de dialogue. Vous pouvez effectuer les actions suivantes :

   * Convertissez cette annonce en annonce pense-bête en cochant la case Activer l&#39;annonce pense-bête.
   * Sélectionnez le délai de livraison de l&#39;annonce.

1. Sélectionner **[!UICONTROL À une date]** si vous souhaitez planifier une annonce pour une date ultérieure et cliquez sur la zone de texte adjacente. Une fenêtre contextuelle de calendrier s’affiche, dans laquelle vous pouvez choisir la date de début. Choisissez la date de fin en suivant les mêmes étapes.
1. Cliquez sur **[!UICONTROL Enregistrer]**.
1. Dans l’onglet Brouillons, cliquez sur l’icône des paramètres en regard d’une annonce, puis cliquez sur Envoyer.

Si la pièce jointe multimédia est de grande taille, le téléchargement peut prendre un certain temps. Une fois que vous avez cliqué sur Enregistrer, une fenêtre contextuelle s’affiche avec un message pendant le traitement de votre téléchargement. Vous recevrez une notification une fois la pièce jointe téléchargée.

## En-tête {#masthead}

Lorsque vous choisissez cette option, tout fichier multimédia que vous choisissez est proposé comme en-tête sur la page d’accueil de l’élève. L’en-tête sert d’appel à l’action pour les élèves auxquels il est destiné.

![](assets/masthead-announcement.png)

*Personnalisation de l’en-tête*

1. Parcourez et choisissez une image qui représentera l’en-tête. La taille recommandée est de 1 280 x 360 px.
1. Choisissez les paramètres régionaux auxquels vous souhaitez ajouter un en-tête. Pour chaque langue, vous devez choisir une ressource d’en-tête.
1. Dans le panneau **[!UICONTROL Bouton d’action]** ajoutez une url afin que les élèves soient redirigés vers l&#39;url lorsqu&#39;ils cliquent sur le bouton de l&#39;en-tête. Il s’agit d’un champ facultatif.
1. Choisissez les groupes d’utilisateurs cibles ou les objets d’apprentissage cibles. Vous ne pouvez choisir qu’une seule option pour une annonce.

   Commencez à saisir le nom du groupe d’utilisateurs dans la zone de texte et faites votre choix dans la liste déroulante. De même, choisissez la formation en saisissant le nom de l’objet dans la zone de texte.

1. Dans le panneau **[!UICONTROL Paramètres avancés]** , vous disposez des options suivantes :

   * Cliquez sur **[!UICONTROL Immédiatement]** si vous voulez que l&#39;annonce soit publiée immédiatement.
   * Cliquez sur **[!UICONTROL Jamais]** si vous ne souhaitez pas que votre annonce expire.
   * Sélectionnez l’option **[!UICONTROL Début]** et **[!UICONTROL Fin]** dates de l&#39;annonce.

   ![](assets/advanced-settings.png)

   *Définition de la durée d’affichage d’un en-tête*

**Le nombre d&#39;annonces En-tête en direct est-il limité ?**

Vous ne verrez que les 10 annonces En-tête les plus récentes.

## Recommandation {#recommendation}

Lorsque vous choisissez cette option, toute formation que vous choisissez est recommandée aux groupes d’utilisateurs spécifiés. Les recommandations sont basées sur un algorithme de machine learning.

![](assets/recommendation-announcement.png)

*Sélectionner la formation recommandée à afficher à un élève*

1. Choisissez la formation que vous souhaitez recommander aux élèves. Vous pouvez ajouter jusqu’à 10 formations.

   Les élèves ne verront que les formations non inscrites dans Recommandation par organisation. Selon la visibilité du catalogue, l’élève a accès à la formation.

1. Choisissez les groupes d’utilisateurs cibles ou les objets d’apprentissage cibles. Vous ne pouvez choisir qu’une seule option pour une annonce.

   Commencez à saisir le nom du groupe d’utilisateurs dans la zone de texte et faites votre choix dans la liste déroulante. De même, choisissez la formation en saisissant le nom de l’objet dans la zone de texte.

1. Dans la section Paramètres avancés, vous disposez des options suivantes :

   * Cliquez sur **[!UICONTROL Immédiatement]** si vous voulez que l&#39;annonce soit publiée immédiatement.
   * Cliquez sur **[!UICONTROL Jamais]** si vous ne souhaitez pas que votre annonce expire.
   * Sélectionnez l’option **[!UICONTROL Début]** et **[!UICONTROL Fin]** dates de l&#39;annonce.

   <!--![](assets/advanced-settings.png)-->

Lorsque vous cliquez sur **[!UICONTROL Enregistrer]**, vous pouvez publier l’annonce immédiatement ou plus tard. D&#39;ici là, l&#39;annonce sera à l&#39;état de brouillon.

* Les en-têtes/Recommendations ne déclenchent aucune notification.
* Les en-têtes/Recommendations n&#39;apparaissent pas dans le rapport des annonces.

## Brouillon, liste planifiée et liste envoyée {#draftscheduledandsentlist}

Dans la connexion Administrateur, vous pouvez afficher toutes les annonces dans trois onglets tels que Brouillons, Planifié et Envoyé.

<!--![](assets/three-tabs-announcement1.png)-->

### Brouillon {#draft}

Dans l&#39;onglet Brouillons, vous pouvez afficher toutes les annonces créées par un administrateur mais pas encore diffusées ou pas encore programmées pour la diffusion.

Par défaut, toutes les annonces sont définies pour une diffusion immédiate. Si vous choisissez paramètres > option d&#39;envoi pour une annonce non planifiée, elle est immédiatement diffusée. Pour planifier une diffusion d’annonce , vous devez choisir les dates de début et de fin dans les paramètres avancés.

### Planifié {#scheduled}

Dans l&#39;onglet Programmé, vous pouvez afficher toutes les annonces programmées pour être diffusées à une date ultérieure.

### Envoyé {#sent}

Dans l&#39;onglet Envoyé, vous pouvez afficher toutes les annonces déjà diffusées.

## En tant qu’e-mail

Utilisez cette option pour envoyer des courriers électroniques ad hoc ciblés aux élèves d&#39;un groupe d&#39;utilisateurs sélectionné ou aux élèves inscrits à une formation spécifique.

![L’administrateur crée une annonce par e-mail](assets/email-announcement-admin.png)

*Envoyer des courriers électroniques ad hoc ciblés aux élèves*

*L’administrateur crée une annonce par e-mail*

1. Sélectionner **[!UICONTROL Saisir comme adresse e-mail]**.
1. Saisissez l’objet et le corps du message.
1. Dans la section Cible, vous pouvez :

   * Sélectionner un groupe d’utilisateurs OU
   * Sélectionnez un cours. Si le cours comporte plusieurs instances, vous pouvez sélectionner l&#39;instance requise.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
