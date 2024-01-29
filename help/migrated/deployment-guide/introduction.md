---
jcr-language: en_us
title: Guide de déploiement de Learning Manager
description: Learning Manager est un système de gestion de l’apprentissage (LMS) qui permet aux professionnels de la formation de fournir des supports d’apprentissage attrayants et suivis qui peuvent contribuer aux besoins ou aux objectifs d’une organisation. Learning Manager permet principalement aux formateurs ou aux responsables d’affecter des cours et d’autres objets d’apprentissage, dans un ordre spécifique, aux élèves.
contentowner: shhivkum
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '3246'
ht-degree: 0%

---



# Guide de déploiement de Learning Manager

## Introduction {#introduction}

Learning Manager est un système de gestion de l’apprentissage (LMS) qui permet aux professionnels de la formation de fournir des supports d’apprentissage attrayants et suivis qui peuvent contribuer aux besoins ou aux objectifs d’une organisation. Learning Manager permet principalement aux formateurs ou aux responsables d’affecter des cours et d’autres objets d’apprentissage, dans un ordre spécifique, aux élèves. Cet outil offre également plusieurs fonctionnalités puissantes, notamment un lecteur fluidique multiformat, la ludification, les badges, un tableau de bord d&#39;élève facile à utiliser. Toutefois, pour tirer parti de toutes ces fonctionnalités, il est essentiel de configurer Learning Manager.

Ce guide fournit des instructions détaillées sur la façon de prendre en main Learning Manager. Ce document fournit également les informations de configuration et d’installation, en détail. Lisez ce qui suit pour savoir comment commencer à utiliser Learning Manager.

## À qui s&#39;adresse ce guide ? {#whoisthisguideintendedfor}

En tant qu’utilisateur de Learning Manager, vous pouvez porter le chapeau d’un administrateur, d’un auteur, d’un instructeur, d’un responsable ou d’un élève. Ce guide s’adresse aux utilisateurs susceptibles d’être impliqués dans la configuration d’un LMS pour une organisation ou un client :

* **Administrateur informatique** - En tant qu’administrateur informatique, vous pouvez activer ou intégrer Learning Manager dans votre organisation. Un administrateur informatique peut également ajouter un ou plusieurs utilisateurs et peut jouer le rôle d’administrateur d’intégration ou d’un administrateur qui intègre Learning Manager à des applications tierces.
* **Auteur** - En tant qu’auteur Learning Manager, vous pouvez créer du contenu d’apprentissage requis pour les besoins d’apprentissage d’une organisation. Un auteur est impliqué dans la création du contenu de base chargé dans Learning Manager.

* **Administrateur Learning Manager** - Un administrateur Learning Manager effectue les activités de configuration et d’installation liées à l’application. Dans certaines entreprises, un administrateur informatique peut également jouer le rôle d’administrateur Learning Manager.

## Prise en main du déploiement de Learning Manager {#getstartedwithcaptivateprimedeployment}

Après avoir acheté Learning Manager, activez votre compte Learning Manager à l’aide de la clé de licence que vous avez reçue. Passez aux configurations suivantes, comme indiqué dans le visuel suivant :

![](assets/getting-started-withcaptivateprime.jpg)

## Configuration de votre site dans Learning Manager {#configureyoursiteincaptivateprime}

Avant de commencer à ajouter et à mettre en œuvre des objets d’apprentissage dans Learning Manager, quelques configurations clés sont requises. Commencez par configurer votre site en fonction de votre organisation. La configuration du site comprend les étapes suivantes :

* Configuration de l’identité visuelle et du logo pour votre organisation
* Configuration des modèles de courrier électronique
* Configuration des paramètres de compte de base
* Configuration des paramètres de retour d’informations
* Configuration des paramètres du tableau de bord des élèves

### Configuration de l’identité visuelle et du logo {#setupbrandingandlogo}

En tant qu’administrateur, vous pouvez définir l’identité visuelle et les thèmes en fonction des exigences de marque de votre organisation. Pour définir l’identité visuelle et les thèmes de votre site, procédez comme suit :

### Définition du logo et de la bannière : {#settingthelogoandbanner}

Utilisez les paramètres de logo et de bannière pour afficher le logo de votre entreprise dans Learning Manager. Configurez les options de marque pour définir le domaine de l’entreprise dans l’URL, afficher le nom de l’organisation et afficher les palettes de couleurs correspondant à la marque de l’entreprise. Pour configurer les paramètres de branding :

* Connectez-vous à votre compte Learning Manager en tant qu’administrateur.
* Dans le volet de gauche, cliquez sur **Branding**.
* Sur la page Identité visuelle, vous pouvez configurer les options suivantes en cliquant sur **Modifier** en regard de l’option que vous souhaitez modifier :

   * **Nom de l’organisation** : La valeur que vous spécifiez ici détermine le nom qui apparaît sur la bannière sur chaque page de votre site.
   * **Sous-domaine**: cette valeur détermine l’URL de votre site.
   * **Style de logo**: l’image de ce champ apparaît sous la forme du logo dans le coin supérieur droit de chaque page. Ici, vous pouvez choisir d’afficher uniquement le logo, ou le nom de votre organisation, ou le logo et le nom de l’organisation.

![](assets/setting-the-themesforyoursite.png)

>[!NOTE]
>
>Vous pouvez uniquement configurer le nom et le logo à l’aide de l’identité visuelle. Vous ne pouvez pas modifier la position du logo ou de l’image.

***Learning Manager prend en charge les formats de fichier suivants pour les images de logo : .png, .jpeg, .jpg, .gif, .bmp***

### Définition des thèmes pour votre site {#settingthethemesforyoursite}

Learning Manager vous permet de modifier l’apparence de votre site à l’aide de thèmes. L’application fournit les thèmes de couleur suivants que vous pouvez choisir :

* Prime par défaut
* Cailloux
* Carnaval
* Automne
* Ciel hivernal

Vous pouvez choisir l’une des gammes de couleurs pour l’aligner avec l’image de marque de votre entreprise.

1. Dans le volet de navigation de gauche Learning Manager, cliquez sur **[!UICONTROL Branding]**.
1. Dans le panneau **Thèmes** section, cliquez sur **[!UICONTROL Modifier]**. L’application vous permet de choisir un nouveau thème. Lorsque vous sélectionnez un thème, vous pouvez immédiatement voir les palettes de couleurs utilisées pour les éléments clés de l’interface.

   ![](assets/setting-the-themesforyoursite.png)

1. De plus, vous pouvez modifier le **Couleur de la barre supérieure**, **Couleur accentuée**, et le **Luminosité de la barre latérale**.  Vous pouvez utiliser vos propres couleurs de marque pour ces éléments d’interface clés.
1. Pour rétablir les valeurs sur la palette de couleurs par défaut de votre thème, cliquez sur **[!UICONTROL Réinitialiser le thème]**. Les couleurs des éléments clés de l’interface utilisateur sont définies sur les options par défaut pour le thème choisi.
1. Après avoir choisi le thème, cliquez sur **[!UICONTROL Afficher les conseils]** pour afficher les libellés ou les conseils dans l’aperçu.

   ![](assets/setting-the-themesforyoursite-step5.png)

   Remarquez un diaporama avec plusieurs images dans le **Thèmes** section. Ce diaporama vous permet de prévisualiser instantanément le thème ou le jeu de couleurs. Vous pouvez prévisualiser instantanément les pages sélectionnées, telles que la page d’accueil, le tableau de bord de l’élève, etc.

1. Si vous souhaitez prévisualiser les modifications dans un navigateur, cliquez sur **[!UICONTROL Aperçu en direct]**. Une fenêtre contextuelle Aperçu du thème en direct apparaît, dans laquelle vous pouvez modifier la palette de couleurs ou continuer avec les options par défaut. Pour prévisualiser vos options dans un navigateur, cliquez sur **[!UICONTROL Aperçu]** dans cette fenêtre contextuelle.

   ![](assets/setting-the-themesforyoursite-step6.png)

1. Les options choisies sont appliquées temporairement à votre site. Si vous souhaitez enregistrer le thème et les paramètres de couleur sélectionnés, cliquez sur **[!UICONTROL Appliquer]**.
1. Après avoir sélectionné et appliqué un thème, cliquez sur ****[!UICONTROL Enregistrer]**** pour enregistrer votre choix.

## Configuration des modèles de courrier électronique {#configureemailtemplates}

En tant qu’administrateur, votre prochaine étape consistera à configurer des modèles de courrier électronique pour divers événements. Vous pouvez activer, désactiver et modifier les modèles de courrier électronique à envoyer aux utilisateurs. Il existe trois catégories principales de modèles de courrier électronique :

* Modèles d’e-mail généraux : ces e-mails sont déclenchés pour les événements génériques. Par exemple, une notification de bienvenue lorsqu’un utilisateur se connecte pour la première fois.
* Modèles de courrier électronique associés à un objet ou une activité d’apprentissage : ces courriers électroniques sont envoyés aux élèves, aux auteurs ou aux responsables chaque fois qu’il y a une activité d’apprentissage. Par exemple, les e-mails déclenchés après l’inscription au cours, la participation à la classe, la fin du cours, etc.
* Rappels et mises à jour : ces e-mails sont déclenchés lorsque les utilisateurs ont besoin de mises à jour ou de rappels pour un événement. Par exemple, un élève reçoit un rappel pour un cours à venir ou un administrateur reçoit une notification par e-mail pour un rapport partagé.

Vous pouvez activer et configurer n’importe laquelle de ces notifications par e-mail à partir du tableau de bord Administrateur. Pour savoir comment définir des modèles de courrier électronique, procédez comme suit :

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL ** Modèles de courrier électronique **.]**
1. Cliquez sur l’un des onglets suivants :**[!UICONTROL ** Généralités **/** Activité d’apprentissage **/** Rappels et mises à jour **.]** Par exemple, supposons que vous cliquiez sur **[!UICONTROL ** Activité d’apprentissage **.]**
1. Cliquez sur le bouton bascule pour l’activité pour laquelle vous souhaitez déclencher un e-mail. Dans cet exemple, supposons que vous cliquiez sur **[!UICONTROL ** Programme d’apprentissage - Inscrit par l’administrateur/le responsable **.]**

   ![](assets/configure-email-templates-step3.png)

   Le système affiche le message contextuel « Activé avec succès ». Désormais, chaque fois qu’un responsable ou un administrateur inscrit un élève à un cours, celui-ci reçoit un courrier électronique de ce compte Learning Manager.

1. Vous pouvez modifier le modèle de courrier électronique par défaut. Pour ce faire, cliquez sur l’événement. Dans cet exemple, cliquez sur **[!UICONTROL Programme d’apprentissage - Inscrit par l’administrateur/le responsable.]**
1. Dans le panneau **[!UICONTROL Aperçu du modèle]** dans la boîte de dialogue contextuelle, notez qu’il existe deux onglets : [!UICONTROL Élève] et [!UICONTROL Responsable].

   ![](assets/configure-email-templates-step5.png)

   Pour chacun de ces onglets, cliquez sur le corps de l’e-mail pour modifier le contenu. Pour enregistrer les modifications apportées au modèle de courrier électronique, cliquez sur **[!UICONTROL Enregistrer]**.

   Désormais, chaque fois qu’un élève est inscrit à un cours par le responsable ou l’administrateur, l’élève et son responsable reçoivent une notification par e-mail.

   ***Remarque : les modifications s’appliquent uniquement au modèle d’e-mail associé à l’événement sélectionné.***

1. Notez que vous n’avez pas pu modifier l’URL du compte ou la signature dans le modèle d’e-mail. Pour modifier le **[!UICONTROL URL du compte]** ou **[!UICONTROL Signature]**, cliquez sur le bouton **[!UICONTROL Paramètres]** onglet. Dans cet onglet, vous pouvez modifier la bannière d’e-mail, la signature électronique, l’URL du compte.

   Le lien URL du compte s’affiche dans tous les e-mails, juste avant la signature. Entrez votre URL préférée et cliquez sur **[!UICONTROL Enregistrer]**. Cette URL est uniquement visible par les utilisateurs internes.

   Pour la bannière d’e-mail, vous pouvez modifier la couleur de la bannière en sélectionnant  **[!UICONTROL ** Arrière-plan de la bannière **.]** Vous pouvez également utiliser une image personnalisée comme bannière en sélectionnant **[!UICONTROL Image personnalisée]** option. Cliquez sur  **[!UICONTROL Enregistrer]** après avoir apporté les modifications.

   ***Remarque : la taille d’image personnalisée de la bannière d’e-mail doit être de 1 240 x 200 px. Les images dont la taille est supérieure à la taille recommandée sont recadrées.***

   ***Learning Manager prend uniquement en charge les types de fichiers .jpg, .jpeg et .png pour les bannières d’e-mail.***

   ![](assets/configure-email-templates-step6.png)

1. Vous pouvez également choisir d’activer les e-mails du responsable facultatifs. Si vous sélectionnez **[!UICONTROL Activer]** , chaque fois qu&#39;un rapport direct reçoit un e-mail de ce compte Prime, le responsable est également inclus dans la liste de diffusion.

   ***Remarque : les paramètres de cet onglet s’appliquent à tous les modèles, globalement.***

### Configuration de modèles de courrier électronique pour un objet d’apprentissage {#configureemailtemplatesforalearningobject}

En plus de définir des modèles de courrier électronique au niveau global, en tant qu’administrateur, vous pouvez également configurer des modèles de courrier électronique pour un objet d’apprentissage spécifique. Dans ce cas, toutes les modifications que vous apportez au modèle de courrier électronique s’appliquent uniquement à cet objet d’apprentissage.

Cette option est également disponible pour les auteurs, lorsqu’ils configurent un objet d’apprentissage.

Pour configurer des modèles de courrier électronique pour un objet d’apprentissage :

1. Cliquez sur le cours, le programme d’apprentissage ou la certification pour lesquels vous souhaitez configurer le modèle de courrier électronique.
1. Dans le volet de gauche, cliquez sur **[!UICONTROL ** Modèles de courrier électronique **.]** Le système affiche un ****[!UICONTROL Aperçu du modèle]**** boîte de dialogue contextuelle.
1. Modifiez l’objet ou le corps du modèle de courrier électronique, puis cliquez sur **[!UICONTROL **Enregistrer**]**pour appliquer les modifications.
1. Pour annuler les modifications, cliquez sur **[!UICONTROL ** Rétablir l’original **.]**

### Empêcher les utilisateurs de recevoir des e-mails {#restrictusersfromreceivingemails}

En tant qu’administrateur, vous pouvez sélectionner les personnes qui recevront les e-mails de Learning Manager et celles qui ne les recevront pas. Pour ce faire, utilisez la commande ****[!UICONTROL Utilisateur restreint]**** option sous le ****[!UICONTROL Paramètres]** **tab. Les utilisateurs peuvent être ajoutés à cette liste en utilisant leur nom, leur ID de messagerie ou leur ID d’utilisateur unique. Les utilisateurs répertoriés sous cette option ne pourront pas recevoir de communication par e-mail de Learning Manager.

## Configuration des paramètres de votre compte {#configureyouraccountsettings}

Learning Manager vous permet de configurer certains paramètres de compte, tels que les paramètres de base, les paramètres de retour d’informations, les paramètres généraux et les paramètres du tableau de bord de l’élève. Les procédures suivantes vous expliquent comment configurer chacun de ces paramètres :

### Configuration des paramètres de base {#configurebasicsettings}

1. Dans la page d’accueil de Learning Manager, cliquez sur ****[!UICONTROL Paramètres]****. Par défaut, le système affiche la page Informations de base, avec les champs de langue et d’emplacement par défaut.
1. Cliquez sur ****[!UICONTROL Modifier]**** dans le coin supérieur droit de la page pour modifier les informations de base.
1. Configurez les options suivantes :

   * **Pays**: Sélectionnez le pays dans ce champ déroulant.
   * **Fuseau horaire**: définissez le fuseau horaire approprié pour votre emplacement.
   * **Paramètres régionaux**: sélectionnez la langue de votre choix. Si vous modifiez la langue dans ce champ, la modification est appliquée à tous les utilisateurs qui utilisent cette application. Cependant, individuellement, chaque utilisateur peut modifier la langue de préférence.
   * **L&#39;exercice commence à partir de**: Sélectionnez le mois de début de l’exercice financier de votre organisation.



   ![](assets/configure-basic-settings-step3.png)

## Configuration des paramètres de retour d’informations {#configurefeedbacksettings}

Learning Manager vous permet de recueillir les commentaires des élèves sur un cours. Il est également possible de recueillir des commentaires sur les élèves à l’aide de Learning Manager. Pour demander des commentaires, vous devez d&#39;abord configurer les types de commentaires L1 et L3.

Le retour d’informations L3 est le retour d’informations d’un responsable sur un élève. Vous pouvez utiliser ce type de retour d’informations pour suivre les performances des élèves au fil du temps. Le retour d’informations L1 est le retour d’informations qu’un élève fournit sur un cours. Ce type de commentaires permet à un administrateur de recueillir des commentaires directs sur un cours.

En tant qu’administrateur, vous pouvez configurer les paramètres de retour d’informations de manière globale. Pour ce faire, procédez comme suit :

1. Dans la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL Paramètres]**.
1. Dans le volet de gauche, cliquez sur **[!UICONTROL Généralités]**.
1. Pour configurer le retour d&#39;informations L1, cliquez sur le bouton **[!UICONTROL Retour d&#39;informations L1]** onglet. Les options permettant de configurer une question obligatoire et plusieurs questions facultatives s’affichent. Ce sont les questions qu’un élève consulte lorsqu’il fournit des commentaires après avoir suivi un cours. Les questions sont rédigées sous forme d’instructions afin que les élèves puissent sélectionner leur réponse sur une échelle de 1 à 5.

   La première partie du retour d&#39;informations L1 est une question obligatoire sur la façon dont un élève doit recommander ce cours à un ami ou à un collègue.

   ***Remarque : vous ne pouvez pas modifier la question obligatoire.***

   ![](assets/configure-feedbacksettings-step3.png)

1. Pour configurer les autres questions de votre questionnaire de retour, cliquez sur les questions dans la section ****[!UICONTROL Cours en auto-apprentissage]**** ou ****[!UICONTROL Cours en salle de classe]****. Lorsque vous cliquez sur une question, le système vous permet de modifier les questions par défaut.



   ![](assets/configure-feedbacksettings-step4.png)

1. Vous pouvez soit activer ou désactiver les questions par défaut, soit modifier complètement les questions par défaut en fonction de vos besoins. Par exemple, vous pouvez supprimer la question par défaut « Le sujet de formation était pertinent pour moi. » et ajouter remplacer la question par « J’ai trouvé la formation utile et pertinente. »
1. Après avoir finalisé les questions pour les élèves, vous pouvez configurer les paramètres de rappel. Par défaut, il existe un rappel existant, dans lequel l’application envoie des rappels automatiques aux élèves une fois le cours terminé avec succès. Ce rappel est également configuré pour se répéter toutes les deux semaines jusqu’à ce que l’élève réponde. Vous pouvez modifier le rappel existant en cliquant dessus ou ajouter un nouveau rappel.

   ![](assets/configure-feedbacksettings-step6.png)

1. Configurez les paramètres de rappel en complétant les options suivantes :

   * **Quand envoyer ?**: Indiquez si vous souhaitez envoyer la demande de retour d’informations à la fin du cours ou après la fin du cours.
   * **Jours après la fin**: Spécifiez le nombre de jours après lequel vous souhaitez envoyer la demande de retour d&#39;informations. Ce champ est visible uniquement s’il est sélectionné ****[!UICONTROL Après la fin du cours]****.

   * **Périodicité**: indiquez si vous souhaitez envoyer un rappel de retour d’informations tous les jours, toutes les semaines ou tous les mois. Vous pouvez également spécifier le nombre de semaines pendant lesquelles vous souhaitez envoyer le rappel.

1. Cliquez sur la coche pour enregistrer vos paramètres de rappel.
1. Une fois tous les paramètres de retour terminés, cliquez sur **[!UICONTROL **Enregistrer**]** dans le coin supérieur droit de la page.

## Configurer les retours L3 : {#configurel3feedback}

Les retours L3 contiennent les questions qui sont envoyées au responsable d’un élève une fois qu’il a terminé un cours. Le retour d’informations L3 permet à un administrateur de suivre les modifications du comportement ou des compétences d’un élève au fil du temps. Pour configurer ces commentaires, sur la page Commentaires, cliquez sur le bouton ****[!UICONTROL Retour d&#39;informations L3]**** onglet. Vous voyez une question par défaut. Le responsable doit répondre à cette question à l’aide d’une échelle de notation à cinq points.

![](assets/configure-l3-feedback.png)

Comme pour le retour d&#39;informations L1, vous pouvez configurer les rappels pour le retour d&#39;informations L3. Vous pouvez soit modifier le rappel existant, soit ajouter un nouveau rappel de retour d’informations.

Après avoir finalisé la question de retour d’informations et les paramètres de rappel, cliquez sur ****[!UICONTROL Enregistrer]**** pour appliquer vos paramètres.

## Configuration des commentaires au niveau de l’instance {#configurefeedbackataninstancelevel}

La procédure précédente décrivait les étapes à suivre pour configurer les paramètres de retour d’informations au niveau global. Autrement dit, les paramètres sont appliqués à tous les cours. En plus de ces questions globales, en tant qu’administrateur ou auteur, vous pouvez configurer des questions de retour d’informations L1 et L3 supplémentaires au niveau de l’instance.

Pour configurer les paramètres de retour d’informations au niveau d’une instance :

1. Sur la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL Cours]**.
1. Passez le curseur de la souris sur le cours où vous souhaitez configurer les paramètres de retour d’informations. Cliquez sur [!UICONTROL **Afficher le cours**.]

   ![](assets/configure-feedbackataninstancelevel.png)

1. Dans la page de détails du cours, cliquez sur **[!UICONTROL Valeurs par défaut de l’instance]** dans la section Configurer.
1. Dans le panneau [!UICONTROL **Langue**] dans la liste déroulante, sélectionnez la langue dans laquelle vous souhaitez que le questionnaire de retour d’informations s’affiche.
1. Activez les retours de réaction L1 si vous souhaitez demander des retours aux élèves. Vous pouvez ajouter jusqu’à deux questions dans cette section. Les élèves peuvent fournir des réponses descriptives à ces questions.
1. Sélectionnez l’option **[!UICONTROL Rendre obligatoire]** case à cocher si vous souhaitez rendre l&#39;une ou l&#39;autre ou les deux questions obligatoires.
1. Sélectionnez l’option **[!UICONTROL Afficher le questionnaire immédiatement après la fin du cours]** si vous souhaitez que les élèves consultent le questionnaire de retour d’informations immédiatement après avoir terminé le cours.

   ![](assets/configure-feedbackataninstancelevel-step7.png)

1. Pour configurer le retour d’informations L3 sur le changement de comportement au niveau d’une instance : ****[!UICONTROL Activer]**** le retour d&#39;informations L3. L’application affiche une question prédéfinie obligatoire et une question vide dans laquelle vous pouvez saisir une question de votre choix.
1. Pour la question prédéfinie sur l’amélioration de l’élève après avoir suivi le cours, la réponse est au format Échelle de Likert. En d’autres termes, les responsables doivent choisir une option sur une échelle allant de Plutôt d’accord à Plutôt pas d’accord.
1. Spécifiez la deuxième question pour le responsable. Les responsables peuvent fournir une réponse descriptive à cette question.
1. Sélectionnez l’option ****[!UICONTROL Rendre obligatoire]**** case à cocher si vous souhaitez rendre la deuxième question obligatoire.

   ![](assets/configure-feedbackataninstancelevel-step11.png)

1. Éventuellement, configurez les paramètres de rappel au niveau de l’instance. Si vous ne configurez pas les paramètres de rappel ici, les paramètres de rappel globaux sont automatiquement affectés.
1. Après avoir finalisé les questions de retour d’informations et les paramètres de rappel, cliquez sur **[!UICONTROL **Enregistrer**]**pour appliquer vos paramètres.

   ***Remarque : les paramètres de retour d’informations ne s’appliquent pas aux certifications.***

## Configuration des paramètres généraux {#configuregeneralsettings}

Les paramètres généraux dans Learning Manager permettent aux administrateurs de configurer des paramètres génériques qui affectent d’autres fonctionnalités de l’application. Par exemple, vous pouvez utiliser des paramètres généraux pour spécifier si l’efficacité du cours peut être rendue visible aux élèves. Pour configurer les paramètres généraux :

1. Dans la page d’accueil de Learning Manager, cliquez sur ****[!UICONTROL Paramètres]****.
1. Dans le volet de gauche, cliquez sur ****[!UICONTROL Généralités]****.
1. Dans la page Paramètres généraux, vous pouvez configurer les options suivantes :

   Pour toutes ces options, la fonction affectée par chaque option est variable. Si nécessaire, nous pouvons fournir des liens croisés vers chacune des fonctionnalités détaillées.

   * **Afficher l&#39;efficacité du cours**: Activez cette option si vous souhaitez que les élèves voient l’efficacité d’un cours sur le titre du cours.
   * **Option de réinitialisation du module**: activez cette option si vous souhaitez donner aux élèves la possibilité de réinitialiser un module. Les élèves peuvent ensuite réinitialiser leurs modules s&#39;ils ont échoué ou s&#39;ils ont partiellement terminé le module et veulent recommencer.
   * **Modération du cours**: Activez cette option si vous souhaitez que les modifications apportées à un cours soient approuvées par un administrateur avant que les modifications ne soient visibles par les élèves.
   * **Forum de discussion**: activez cette option si vous souhaitez que les élèves consultent les forums de discussion des cours et y participent. Si vous activez l’option **Forum de discussion** cochez cette case, les élèves et les instructeurs peuvent publier des commentaires pour les cours. Toutefois, si les paramètres de niveau de cours indiquent que cette fonctionnalité n’est pas sélectionnée, les paramètres de niveau de cours ont priorité sur les paramètres d’administrateur.

   * **Option Découvrir les compétences**: activez cette option si vous souhaitez que les élèves explorent les compétences des pairs et du leadership.
   * **ID uniques d’objets d’apprentissage**: activez cette option si vous souhaitez donner aux auteurs la possibilité d&#39;ajouter des ID uniques aux objets d&#39;apprentissage.
   * **Afficher la liste des catalogues**: activez cette option si vous souhaitez que les élèves voient tous les catalogues disponibles. Cette option aide les élèves à affiner leur liste d’objets d’apprentissage.



   ![](assets/configure-generalsettings-step3.png)

## Configuration des paramètres du tableau de bord des élèves {#configurelearnerdashboardsettings}

Le tableau de bord des élèves dans Learning Manager permet aux élèves d’afficher leurs cours obligatoires et recommandés en dehors de leurs réalisations, compétences et annonces. Les administrateurs peuvent décider de la manière dont ce tableau de bord des élèves doit apparaître, en configurant les paramètres du tableau de bord des élèves. Ces paramètres permettent aux administrateurs de définir les widgets sur la page Élève. Ces paramètres spécifient également comment et où les widgets sont placés sur le tableau de bord des élèves. En tant qu’administrateur, vous pouvez prévisualiser la mise en page du tableau de bord des élèves avant d’appliquer les paramètres.

1. Dans la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL Paramètres]**.
1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL ** Tableau de bord des élèves **.]**
1. Sélectionnez les widgets que vous souhaitez activer. Si vous désélectionnez un widget, celui-ci est immédiatement supprimé de l’aperçu. Les élèves ne peuvent pas voir ce widget dans leur tableau de bord.
1. Cliquez sur ****[!UICONTROL Enregistrer]**** pour appliquer les paramètres.

   ![](assets/configure-learnerdashboardsettings-step4.png)

1. Pour appliquer les paramètres par défaut, cliquez sur **[!UICONTROL Restaurer les paramètres par défaut.]** Dans ce cas, tous les widgets sauf **[!UICONTROL Bienvenue et annonces autocollantes]** sont visibles.

   ***Même après avoir activé les paramètres du tableau de bord des élèves, ces derniers peuvent modifier et déplacer les widgets dans leurs tableaux de bord respectifs.***

