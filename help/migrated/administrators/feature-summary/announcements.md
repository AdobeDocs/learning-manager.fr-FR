---
jcr-language: en_us
title: Annonces
description: Une annonce est un message multimédia (texte, image ou vidéo) qu’un administrateur diffuse pour un ensemble défini d’utilisateurs.
exl-id: 313ac2c6-05c0-4941-8d71-9c664099bb5c
source-git-commit: 69ef7d1e27fac3db49cbb4b9f9403f74e146efb5
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 69%

---

# Annonces

Une annonce est un message multimédia (texte, image ou vidéo) qu’un administrateur diffuse pour un ensemble défini d’utilisateurs.

L&#39;administrateur peut diffuser des annonces aux élèves les informant de l&#39;occurrence d&#39;un événement ou d&#39;une activité. L’annonce peut être une combinaison de texte, d’images ou de vidéos. Vous pouvez lier des objets d’apprentissage, comme des cours, des programmes d’apprentissage et des certifications, à une annonce.

Il existe quatre types d&#39;annonces :

* Notification
* En-tête
* Recommandation
* Courrier électronique

## Notification {#notification}

1. En tant qu&#39;utilisateur administrateur, cliquez sur Annonces dans le volet de gauche.
1. Cliquez sur Ajouter dans l’angle supérieur droit de la page.
1. Dans la liste déroulante Type, sélectionnez l’option **Comme notification**.

![](assets/as-notofocation.png)

*Personnaliser la notification*

1. Dans le champ Message, ajoutez le message de l’annonce. Vous pouvez également ajouter une URL pour les annonces ici. Cependant, vous devez ajouter l’URL dans le formulaire HTML.

   Par exemple, `code <a href="http://www.w3schools.com" target="_blank">Visit W3Schools</a>.`

   Lorsque vous spécifiez une cible vide, lorsqu’un utilisateur clique sur l’URL de l’annonce, le lien s’ouvre dans un nouvel onglet. Si vous ne spécifiez pas de cible, le lien s’ouvre dans le même navigateur.

1. Ajoutez éventuellement des pièces jointes à l’annonce, telles que des images ou des fichiers vidéo.
1. Sélectionnez les groupes d’utilisateurs cibles ou les objets d’apprentissage cibles. Vous ne pouvez sélectionner qu’un seul de ces deux groupes pour une annonce.

   Commencez à saisir le nom de groupe d’utilisateurs dans la zone de texte, puis effectuez la sélection dans la liste déroulante. De même, sélectionnez la formation en saisissant le nom de l’objet dans la zone de texte.

1. Cliquez sur Paramètres avancés dans la boîte de dialogue. Vous pouvez réaliser les actions suivantes :

   * Modifiez cette annonce en annonce pense-bête en cochant la case Activer l’annonce pense-bête.
   * Sélectionnez le délai de livraison pour l’annonce.

1. Sélectionnez **[!UICONTROL À une date]** si vous souhaitez planifier une annonce pour une date ultérieure et cliquez sur la zone de texte adjacente. Une fenêtre contextuelle de calendrier s’affiche, dans laquelle vous pouvez sélectionner la date de début. Sélectionnez la date de fin en suivant les mêmes étapes.
1. Cliquez sur **[!UICONTROL Enregistrer]**.
1. Dans l’onglet Brouillons, cliquez sur l’icône des paramètres en regard d’une annonce, puis cliquez sur Envoyer.

Si la pièce jointe d’éléments multimédia est de grande taille, le chargement peut prendre du temps. Une fois que vous avez cliqué sur Enregistrer, une fenêtre contextuelle s’affiche avec un message pendant le traitement de votre téléchargement. Vous recevrez une notification après le chargement de la pièce jointe.

## En-tête {#masthead}

Lorsque vous sélectionnez cette option, tout fichier multimédia que vous sélectionnez s&#39;affiche comme en-tête sur la page d’accueil de l’élève. L&#39;en-tête sert d&#39;appel à l’action pour les élèves auxquels il est destiné.

![](assets/masthead-announcement.png)

*Personnaliser l&#39;en-tête*

1. Recherchez et choisissez une image qui représentera l&#39;en-tête. La taille recommandée est 1 280 x 360 px.
1. Choisissez la langue à laquelle vous souhaitez ajouter un en-tête. Pour chaque langue, vous devez choisir un en-tête.
1. Dans le champ **[!UICONTROL Bouton d&#39;action]**, ajoutez une URL afin de rediriger les élèves vers celle-ci lorsqu&#39;ils cliquent sur le bouton dans l&#39;en-tête. Il s’agit d’un champ facultatif.
1. Sélectionnez les groupes d’utilisateurs cibles ou les objets d’apprentissage cibles. Vous ne pouvez sélectionner qu’un seul de ces deux groupes pour une annonce.

   Commencez à saisir le nom de groupe d’utilisateurs dans la zone de texte, puis effectuez la sélection dans la liste déroulante. De même, sélectionnez la formation en saisissant le nom de l’objet dans la zone de texte.

1. Dans la section **[!UICONTROL Paramètres avancés]**, vous disposez des options suivantes :

   * Cliquez sur **[!UICONTROL Immédiatement]** si vous souhaitez que l&#39;annonce soit publiée immédiatement.
   * Cliquez sur **[!UICONTROL Jamais]** si vous ne souhaitez pas que votre annonce expire.
   * Sélectionnez les dates de **[!UICONTROL début]** et de **[!UICONTROL fin]** pour l&#39;annonce.

   ![](assets/advanced-settings.png)

   *Définir l&#39;heure d&#39;affichage de l&#39;en-tête*

**Existe-t-il une limite au nombre d&#39;annonces En-tête en direct ?**

Vous ne verrez que les 10 annonces En-tête les plus récentes.

## Recommandation {#recommendation}

Lorsque vous sélectionnez cette option, toutes les formations que vous choisissez sont recommandées aux groupes d’utilisateurs spécifiés. Les recommandations sont basées sur un algorithme de machine learning.

![](assets/recommendation-announcement.png)

*Sélectionnez la formation recommandée à afficher pour un élève*

1. Sélectionnez la formation que vous souhaitez recommander aux élèves. Vous pouvez ajouter jusqu’à 10 formations.

   Les élèves ne verront que les formations non inscrites dans Recommandation par organisation. Selon la visibilité du catalogue, l’élève a accès à la formation.

1. Sélectionnez les groupes d’utilisateurs cibles ou les objets d’apprentissage cibles. Vous ne pouvez sélectionner qu’un seul de ces deux groupes pour une annonce.

   Commencez à saisir le nom de groupe d’utilisateurs dans la zone de texte, puis effectuez la sélection dans la liste déroulante. De même, sélectionnez la formation en saisissant le nom de l’objet dans la zone de texte.

1. La section Paramètres avancés propose les options suivantes :

   * Cliquez sur **[!UICONTROL Immédiatement]** si vous souhaitez que l&#39;annonce soit publiée immédiatement.
   * Cliquez sur **[!UICONTROL Jamais]** si vous ne souhaitez pas que votre annonce expire.
   * Sélectionnez les dates de **[!UICONTROL début]** et de **[!UICONTROL fin]** pour l&#39;annonce.

   <!--![](assets/advanced-settings.png)-->

Lorsque vous cliquez sur **[!UICONTROL Enregistrer]**, vous pouvez soit publier immédiatement l’annonce, soit la publier ultérieurement. L&#39;annonce, jusqu&#39;alors, restera à l&#39;état de brouillon.

* Les en-têtes/recommandations ne déclenche aucune notification.
* Les en-têtes/recommandations n’apparaissent pas dans le rapport d’annonces.

## Liste Brouillon, Planifié et Envoyé {#draftscheduledandsentlist}

Dans la connexion Administrateur, vous pouvez afficher toutes les annonces dans trois onglets tels que Brouillons, Planifié et Envoyé.

<!--![](assets/three-tabs-announcement1.png)-->

### Brouillon {#draft}

Dans l&#39;onglet Brouillons, vous pouvez afficher toutes les annonces créées par un administrateur mais pas encore diffusées ou pas encore programmées pour la diffusion.

Par défaut, toutes les annonces sont définies pour une diffusion immédiate. Si vous sélectionnez l’option Paramètres > Envoyer pour une annonce non planifiée, celle-ci est alors diffusée immédiatement. Pour planifier une diffusion d’annonce, vous devez sélectionner les dates de début et de fin dans les paramètres avancés.

### Planifié {#scheduled}

Dans l’onglet Planifié, vous pouvez afficher toutes les annonces planifiées pour la diffusion à une date ultérieure.

### Envoyés {#sent}

Dans l’onglet Envoyé, vous pouvez afficher toutes les annonces déjà diffusées.

## E-mail

Utilisez cette option pour envoyer des courriers électroniques ad hoc ciblés aux élèves d&#39;un groupe d&#39;utilisateurs sélectionné ou aux élèves inscrits à une formation spécifique.

![L&#39;administrateur crée une annonce par e-mail](assets/email-announcement-admin.png)

*Envoyer des courriers électroniques ad hoc ciblés aux élèves*

*L&#39;administrateur crée une annonce par e-mail*

1. Sélectionnez **[!UICONTROL Saisir comme adresse électronique]**.
1. Saisissez l’objet et le contenu du message.
1. Dans la section Cible, vous pouvez :

   * Sélectionner un groupe d’utilisateurs OU
   * Sélectionner un cours. Si le cours comporte plusieurs instances, vous pouvez sélectionner l’instance requise.

1. Cliquez sur **[!UICONTROL Enregistrer]**.
