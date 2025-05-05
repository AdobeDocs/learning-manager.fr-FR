---
jcr-language: en_us
title: Guide de déploiement Learning Manager
description: Learning Manager est un système de gestion de l’apprentissage (LMS) qui permet aux professionnels de la formation de fournir des supports d’apprentissage attrayants et suivis qui peuvent contribuer aux besoins ou aux objectifs d’une organisation. Learning Manager permet principalement aux formateurs ou aux responsables d’affecter des cours et d’autres objets d’apprentissage, dans un ordre spécifique, aux élèves.
contentowner: shhivkum
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '3246'
ht-degree: 72%

---



# Guide de déploiement Learning Manager

## Introduction {#introduction}

Learning Manager est un système de gestion de l’apprentissage (LMS) qui permet aux professionnels de la formation de fournir des supports d’apprentissage attrayants et suivis qui peuvent contribuer aux besoins ou aux objectifs d’une organisation. Learning Manager permet principalement aux formateurs ou responsables d’affecter des cours et autres objets d’apprentissage, dans un ordre spécifique. Cet outil offre également plusieurs fonctionnalités puissantes, dont un lecteur fluidique multiformat, la gamification, les badges, le tableau de bord des élèves facile à utiliser. Toutefois, pour tirer parti de toutes ces fonctionnalités, il est essentiel de configurer Learning Manager au préalable.

Ce guide fournit des instructions détaillées pour se familiariser avec Learning Manager. Ce document fournit également les informations de configuration et d’installation, en détail. Lisez ce qui suit pour bien démarrer avec Learning Manager.

## À qui est destiné ce guide ? {#whoisthisguideintendedfor}

En tant qu’utilisateur de Learning Manager, vous pouvez agir avec différents rôles d’administrateur, d’auteur, d’instructeur, de responsable ou d’élève. Ce guide s’adresse aux utilisateurs susceptibles d’être impliqués dans la configuration d’un LMS pour une organisation ou un client :

* **Administrateur informatique** : en tant qu’administrateur informatique, vous pouvez activer ou intégrer Learning Manager dans votre organisation. Un administrateur informatique peut également ajouter un ou plusieurs utilisateurs et jouer le rôle d’administrateur d’intégration ou d’administrateur qui intègre Learning Manager à des applications tierces.
* **Auteur** : en tant qu’auteur Learning Manager, vous pouvez créer du contenu d’apprentissage requis pour les besoins d’apprentissage d’une organisation. Un auteur est impliqué dans la création du contenu de base chargé dans Learning Manager.

* **Administrateur Learning Manager** : un administrateur Learning Manager effectue les activités de configuration et d’installation liées à l’application. Dans certaines entreprises, un administrateur informatique peut également jouer le rôle d’administrateur Learning Manager.

## Prise en main du déploiement de Learning Manager {#getstartedwithcaptivateprimedeployment}

Après avoir acheté Learning Manager, activez votre compte Learning Manager à l’aide de la clé de licence que vous avez reçue. Passez aux configurations suivantes, comme indiqué dans le visuel suivant :

![](assets/getting-started-withcaptivateprime.jpg)

## Configuration de votre site dans Learning Manager {#configureyoursiteincaptivateprime}

Avant de commencer à ajouter et à mettre en œuvre des objets d’apprentissage dans Learning Manager, quelques configurations clés sont requises. Commencez par configurer votre site en fonction de votre organisation. La configuration du site comprend les étapes suivantes :

* Configuration de l’identité visuelle et du logo pour votre entreprise
* Configuration des modèles de courrier électronique
* Configuration des paramètres de compte de base
* Configuration des paramètres de retour d&#39;informations
* Configuration des paramètres du tableau de bord des élèves

### Configuration de l’identité visuelle et du logo {#setupbrandingandlogo}

En tant qu’administrateur, vous pouvez définir l’identité visuelle et les thèmes en fonction des exigences de marque de votre organisation. Pour définir l’identité visuelle et les thèmes de votre site, procédez comme suit :

### Définition du logo et de la bannière : {#settingthelogoandbanner}

Utilisez les paramètres de logo et de bannière pour afficher le logo de votre entreprise dans Learning Manager. Configurez les options de marque pour définir le domaine de l’entreprise dans l’URL, afficher le nom de l’organisation et afficher les palettes de couleurs correspondant à la marque de l’entreprise. Pour configurer les paramètres d’identité visuelle :

* Connectez-vous à votre compte Learning Manager en tant qu’administrateur.
* Dans le volet de gauche, cliquez sur **Identité visuelle**.
* Sur la page Identité visuelle, vous pouvez configurer les options suivantes en cliquant sur **Modifier** en regard de l’option que vous souhaitez modifier :

   * **Nom de l&#39;organisation** : la valeur que vous spécifiez ici détermine le nom qui apparaît sur la bannière sur chaque page de votre site.
   * **Sous-domaine** : cette valeur détermine l&#39;URL de votre site.
   * **Style de logo** : l&#39;image dans ce champ apparaît sous la forme du logo dans le coin supérieur droit de chaque page. Ici, vous pouvez choisir d’afficher uniquement le logo, ou le nom de votre organisation, ou le logo et le nom de l’organisation.

![](assets/setting-the-themesforyoursite.png)

>[!NOTE]
>
>Vous pouvez uniquement configurer le nom et le logo à l’aide de l’identité visuelle. Vous ne pouvez pas modifier la position du logo ou de l’image.

***Learning Manager prend en charge les formats de fichiers suivants pour les images de logo : .png, .jpeg, .jpg, .gif, .bmp***

### Définition des thèmes pour votre site {#settingthethemesforyoursite}

Learning Manager permet de modifier l’apparence de votre site à l’aide de Thèmes. L’application fournit les thèmes de couleur suivants que vous pouvez choisir :

* Le calque Prime par défaut
* Galets
* Carnaval
* Automne
* Ciel d&#39;hiver

Vous pouvez choisir l’une des gammes de couleurs pour vous aligner avec l’identité visuelle de votre entreprise.

1. Dans le volet de navigation de gauche de Learning Manager, cliquez sur **[!UICONTROL Identité visuelle]**.
1. Dans la section **Thèmes**, cliquez sur **[!UICONTROL Modifier]**. L’application vous permet de choisir un nouveau thème. Lorsque vous sélectionnez un thème, vous pouvez immédiatement voir les palettes de couleurs utilisées pour les éléments d’interface clés.

   ![](assets/setting-the-themesforyoursite.png)

1. De plus, vous pouvez modifier la **couleur de la barre supérieure**, la **couleur d&#39;accentuation** et la **luminosité de la barre latérale**.  Vous pouvez utiliser vos propres couleurs de marque pour ces éléments d’interface clés.
1. Pour réinitialiser les valeurs sur la palette de couleurs par défaut de votre thème, cliquez sur **[!UICONTROL Réinitialiser le thème]**. Les couleurs des éléments clés de l’interface utilisateur sont définies sur les options par défaut pour le thème sélectionné.
1. Après avoir choisi le thème, cliquez sur **[!UICONTROL Afficher les conseils]** pour afficher les étiquettes ou les conseils dans l’aperçu.

   ![](assets/setting-the-themesforyoursite-step5.png)

   Remarquez un diaporama avec plusieurs images dans la section **Thèmes**. Ce diaporama vous permet de prévisualiser instantanément le thème ou le jeu de couleurs. Vous pouvez prévisualiser instantanément les pages sélectionnées, telles que la page d’accueil, le tableau de bord de l’élève, etc.

1. Si vous souhaitez prévisualiser les modifications dans un navigateur, cliquez sur **[!UICONTROL Aperçu en direct]**. Une fenêtre contextuelle Aperçu du thème en direct s’affiche, dans laquelle vous pouvez modifier la palette de couleurs ou continuer avec les options par défaut. Pour prévisualiser vos options dans un navigateur, cliquez sur **[!UICONTROL Aperçu]** dans cette fenêtre contextuelle.

   ![](assets/setting-the-themesforyoursite-step6.png)

1. Les options sélectionnées sont appliquées temporairement à votre site. Si vous souhaitez enregistrer le thème et les paramètres de couleur sélectionnés, cliquez sur **[!UICONTROL Appliquer]**.
1. Après avoir sélectionné et appliqué un thème, cliquez sur **&#x200B;**&#x200B;[!UICONTROL Enregistrer]&#x200B;**&#x200B;** pour sauvegarder votre choix.

## Configurer des modèles de courrier électronique {#configureemailtemplates}

En tant qu’administrateur, votre prochaine étape consistera à configurer des modèles de courrier électronique pour divers événements. Vous pouvez activer, désactiver et modifier les modèles de courrier électronique à envoyer aux utilisateurs. Il existe trois catégories principales de modèles de courrier électronique :

* Modèles de courrier électronique généraux : Ces courriers électroniques sont déclenchés pour les événements génériques. Par exemple, une notification de bienvenue lorsqu’un utilisateur se connecte pour la première fois.
* Modèles de courrier électronique associés à un objet ou une activité d’apprentissage : Ces courriers électroniques sont envoyés aux élèves, aux auteurs ou aux responsables chaque fois qu’il y a une activité d’apprentissage. Par exemple, les courriers électroniques déclenchés après l’inscription au cours, la participation à la classe, la fin du cours, etc.
* Rappels et mises à jour : Ces courriers électroniques sont déclenchés lorsque les utilisateurs ont besoin de mises à jour ou de rappels pour tout événement. Par exemple, un élève reçoit un rappel pour un cours à venir ou un administrateur reçoit une notification par e-mail pour un rapport partagé.

Vous pouvez activer et configurer n’importe laquelle de ces notifications par e-mail à partir du tableau de bord Administrateur. Pour savoir comment définir des modèles de courrier électronique, procédez comme suit :

1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL **&#x200B; Modèles de courrier électronique &#x200B;**.]**
1. Cliquez sur l&#39;un des onglets suivants :**[!UICONTROL ** Général **/** Activité d&#39;apprentissage **/** Rappels et mises à jour **.]** Par exemple, supposons que vous cliquiez sur **[!UICONTROL **&#x200B; Activité d’apprentissage &#x200B;**.]**
1. Cliquez sur le bouton bascule pour l’activité pour laquelle vous souhaitez déclencher un courrier électronique. Dans cet exemple, supposons que vous cliquiez sur **[!UICONTROL **&#x200B; Programme d’apprentissage - Inscrit par l’administrateur/le responsable &#x200B;**.]**

   ![](assets/configure-email-templates-step3.png)

   Le système affiche le message contextuel « Activé avec succès ». Désormais, chaque fois qu’un responsable ou un administrateur inscrit un élève à un cours, celui-ci reçoit un e-mail de ce compte Learning Manager.

1. Vous pouvez modifier le modèle de courrier électronique par défaut. Pour ce faire, cliquez sur l’événement. Dans cet exemple, cliquez sur **[!UICONTROL Programme d’apprentissage - Inscrit par l’administrateur/le responsable.]**
1. Dans la boîte de dialogue contextuelle **[!UICONTROL Aperçu du modèle]**, notez que deux onglets sont disponibles : [!UICONTROL Élève] et [!UICONTROL Responsable].

   ![](assets/configure-email-templates-step5.png)

   Pour chacun de ces onglets, cliquez sur le corps du courrier électronique pour modifier le contenu. Pour enregistrer les modifications apportées au modèle de courrier électronique, cliquez sur **[!UICONTROL Enregistrer]**.

   Désormais, chaque fois qu’un élève est inscrit à un cours par le responsable ou l’administrateur, l’élève et son responsable reçoivent une notification par e-mail.

   ***Remarque : les modifications s’appliquent uniquement au modèle d’e-mail associé à l’événement sélectionné.***

1. Notez que vous n’avez pas pu modifier l’URL du compte ou la signature dans le modèle de courrier électronique. Pour modifier l’**[!UICONTROL URL du compte]** ou la **[!UICONTROL Signature]**, cliquez sur l’onglet **[!UICONTROL Paramètres]**. Dans cet onglet, vous pouvez modifier la bannière de l’e-mail, la signature de l’e-mail, l’URL du compte.

   Le lien de l’URL de compte s’affiche dans tous les courriers électroniques, juste avant la signature. Saisissez vos URL préférées et cliquez sur **[!UICONTROL Enregistrer]**. Cette URL est uniquement visible par les utilisateurs internes.

   Pour la bannière de l’e-mail, vous pouvez modifier la couleur de la bannière en sélectionnant **[!UICONTROL **&#x200B; Arrière-plan de la bannière &#x200B;**.] **&#x200B; Vous pouvez également utiliser une image personnalisée comme bannière en sélectionnant l&#39;option &#x200B;** [!UICONTROL Image personnalisée]&#x200B;**. Cliquez sur &#x200B;** [!UICONTROL Enregistrer]** après avoir apporté les modifications.

   ***Remarque : la taille d’image personnalisée de la bannière d’e-mail doit être de 1 240 x 200 px. Les images supérieures à la taille recommandée sont recadrées.***

   ***Learning Manager prend uniquement en charge les types de fichiers .jpg, .jpeg et .png pour les bannières d’e-mail.***

   ![](assets/configure-email-templates-step6.png)

1. Vous pouvez également choisir d’activer l’option Messages électroniques du responsable facultatifs. Si vous cochez la case **[!UICONTROL Activer]**, chaque fois qu&#39;un rapport direct reçoit un e-mail de ce compte Prime, le responsable est également inclus dans la liste de diffusion.

   ***Remarque : les paramètres de cet onglet s&#39;appliquent à tous les modèles, globalement.***

### Configuration de modèles de courrier électronique pour un objet d’apprentissage {#configureemailtemplatesforalearningobject}

En plus de définir des modèles de courrier électronique au niveau global, en tant qu’administrateur, vous pouvez également configurer des modèles de courrier électronique pour un objet d’apprentissage spécifique. Dans ce cas, toutes les modifications que vous apportez au modèle de courrier électronique s’appliquent uniquement à cet objet d’apprentissage.

Cette option est également disponible pour les auteurs, lorsqu’ils configurent un objet d’apprentissage.

Pour configurer des modèles de courrier électronique pour un objet d’apprentissage :

1. Cliquez sur le cours, le programme d’apprentissage ou la certification pour lesquels vous souhaitez configurer le modèle de courrier électronique.
1. Dans le volet de gauche, cliquez sur **[!UICONTROL **&#x200B; Modèles de courrier électronique &#x200B;**.] **&#x200B; Le système affiche une boîte de dialogue contextuelle &#x200B;**&#x200B;**[!UICONTROL Aperçu du modèle]**&#x200B;**.
1. Modifiez l&#39;objet ou le corps du modèle de courrier électronique, puis cliquez sur **[!UICONTROL **Enregistrer**]**&#x200B;pour appliquer les modifications.
1. Pour annuler les modifications, cliquez sur **[!UICONTROL **&#x200B; Revenir à l&#39;original &#x200B;**.]**

### Empêcher les utilisateurs de recevoir des courriers électroniques {#restrictusersfromreceivingemails}

En tant qu’administrateur, vous pouvez déterminer quels utilisateurs doivent recevoir ou non les e-mails de Learning Manager. Pour ce faire, utilisez l&#39;option **&#x200B;**[!UICONTROL Utilisateur restreint]**&#x200B;** sous l&#39;onglet **Paramètres **[!UICONTROL **]**. Des utilisateurs peuvent être ajoutés à cette liste à l’aide de leur nom, leur identifiant de messagerie ou leur identifiant utilisateur unique. Les utilisateurs répertoriés sous cette option n’auront accès à aucune communication électronique issue de Learning Manager.

## Configurer vos paramètres de compte {#configureyouraccountsettings}

Learning Manager permet de configurer certains paramètres de compte, tels que les paramètres de base, les paramètres de retour d’informations, les paramètres généraux et les paramètres du tableau de bord de l’élève. Les procédures suivantes vous expliquent comment configurer chacun de ces paramètres :

### Configuration des paramètres de base {#configurebasicsettings}

1. Dans la page d’accueil de Learning Manager, cliquez sur **&#x200B;**&#x200B;[!UICONTROL Paramètres]&#x200B;**&#x200B;**. Par défaut, le système affiche la page Informations de base, avec les champs de langue et d’emplacement par défaut.
1. Cliquez sur **&#x200B;**&#x200B;[!UICONTROL Modifier]&#x200B;**&#x200B;** dans le coin supérieur droit de la page pour modifier les informations de base.
1. Configurez les options suivantes :

   * **Pays** : Sélectionnez le pays dans ce champ déroulant.
   * **Fuseau horaire** : Définissez le fuseau horaire approprié pour votre emplacement.
   * **Paramètres régionaux** : Sélectionnez la langue de votre choix. Si vous modifiez la langue dans ce champ, la modification est appliquée à tous les utilisateurs qui utilisent cette application. Cependant, individuellement, chaque utilisateur peut modifier la langue de préférence.
   * **L&#39;exercice commence en** : Sélectionnez le mois de début de l’exercice pour votre organisation.



   ![](assets/configure-basic-settings-step3.png)

## Configuration des paramètres de retour d’informations {#configurefeedbacksettings}

Learning Manager permet de recueillir des retours d’informations des élèves concernant un cours. Il est également possible de recueillir des retours d’informations sur les élèves qui utilisent Learning Manager. Pour obtenir des retours d’informations, vous devez d’abord configurer les types de retours L1 et L3.

Les retours L3 sont les retours d’informations qu’un responsable fournit au sujet d’un élève. Vous pouvez utiliser ce type de retour d’informations pour suivre les performances des élèves au fil du temps. Les retours L1 sont les retours d’informations qu’un élève fournit au sujet d’un cours. Ce type de retours permet à un administrateur de recueillir des commentaires directs sur un cours.

En tant qu’administrateur, vous pouvez configurer les paramètres de retours d’informations de manière globale. Pour ce faire, procédez comme suit :

1. Dans la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL Paramètres]**.
1. Dans le volet de gauche, cliquez sur **[!UICONTROL Général]**.
1. Pour configurer le retour d&#39;informations L1, cliquez sur l&#39;onglet **[!UICONTROL Retour L1]**. Vous voyez les options permettant de configurer une question obligatoire et plusieurs questions facultatives. Il s’agit des questions qu’un élève consulte pendant qu’il fournit des retours après avoir suivi un cours. Les questions sont rédigées sous forme d’instructions afin que les élèves puissent sélectionner leur réponse sur une échelle de 1 à 5.

   La première partie du retour d&#39;informations L1 est une question obligatoire sur la façon dont un élève doit recommander ce cours à un ami ou à un collègue.

   ***Remarque : vous ne pouvez pas modifier la question obligatoire.***

   ![](assets/configure-feedbacksettings-step3.png)

1. Pour configurer les autres questions de votre questionnaire de retour, cliquez sur les questions dans les **&#x200B;**&#x200B;[!UICONTROL Cours en auto-apprentissage]&#x200B;**&#x200B;** ou **&#x200B;**&#x200B;[!UICONTROL Cours en classe]&#x200B;**&#x200B;**. Lorsque vous cliquez sur une question, le système vous permet de modifier les questions par défaut.



   ![](assets/configure-feedbacksettings-step4.png)

1. Vous pouvez soit activer ou désactiver les questions par défaut, soit modifier complètement les questions par défaut en fonction de vos besoins. Par exemple, vous pouvez supprimer la question par défaut « Le sujet de formation était pertinent pour moi. » et ajouter remplacer la question par « J’ai trouvé la formation utile et pertinente. »
1. Après avoir finalisé les questions pour les élèves, vous pouvez configurer les paramètres de rappel. Par défaut, il y a un rappel existant, dans lequel l’application envoie des rappels automatiques aux élèves une fois le cours terminé. Ce rappel est également configuré pour se répéter toutes les deux semaines jusqu’à ce que l’élève réponde. Vous pouvez soit modifier le rappel existant en cliquant dessus, soit ajouter un nouveau rappel.

   ![](assets/configure-feedbacksettings-step6.png)

1. Configurez les paramètres de rappel en complétant les options suivantes :

   * **Quand envoyer** : Indiquez si vous souhaitez envoyer la demande de retour d’informations à la fin du cours ou après la fin du cours.
   * **Jours après la fin** : Précisez le nombre de jours après lesquels vous souhaitez envoyer la demande de retour. Ce champ est visible uniquement si **&#x200B;**&#x200B;[!UICONTROL Après la fin du cours]&#x200B;**&#x200B;** est sélectionné.

   * **Période de récurrence** : Indiquez si vous souhaitez envoyer un rappel de retour d’informations tous les jours, toutes les semaines ou tous les mois. Vous pouvez également spécifier le nombre de semaines pendant lesquelles vous souhaitez envoyer le rappel.

1. Cliquez sur la coche pour enregistrer les paramètres de rappel.
1. Après avoir finalisé tous les paramètres de retour d&#39;informations, cliquez sur **[!UICONTROL **Enregistrer**]**&#x200B;dans le coin supérieur droit de la page.

## Configurer les retours L3 : {#configurel3feedback}

Les retours L3 contiennent les questions qui sont envoyées au responsable d’un élève une fois qu’il a terminé un cours. Le retour d’informations L3 permet à un administrateur de suivre les modifications du comportement ou des compétences d’un élève au fil du temps. Pour configurer ces retours, sur la page Retours d’informations, cliquez sur l’onglet **&#x200B;**&#x200B;[!UICONTROL Retour L3]&#x200B;**&#x200B;**. Vous voyez une question par défaut. Le responsable doit répondre à cette question à l’aide d’une échelle de notation à cinq points.

![](assets/configure-l3-feedback.png)

Tout comme les retours L1, vous pouvez configurer les rappels pour les retours L3. Vous pouvez soit modifier le rappel existant, soit ajouter un nouveau rappel de retour d’informations.

Une fois que vous avez terminé la question de retour et les paramètres de rappel, cliquez sur **&#x200B;**&#x200B;[!UICONTROL Enregistrer]&#x200B;**&#x200B;** pour appliquer vos paramètres.

## Configuration des retours d’informations au niveau d’une instance {#configurefeedbackataninstancelevel}

La procédure précédente décrit les étapes à suivre pour configurer les paramètres de retour d’informations au niveau global. Autrement dit, les paramètres sont appliqués à tous les cours. En plus de ces questions globales, en tant qu’administrateur ou auteur, vous pouvez configurer des questions de retour L1 et L3 supplémentaires au niveau de l’instance.

Pour configurer les paramètres de retour d’informations au niveau d’une instance :

1. Sur la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL Cours]**.
1. Survolez le cours où vous souhaitez configurer les paramètres de retour d’informations. Cliquez Sur [!UICONTROL **Afficher Le Cours**.]

   ![](assets/configure-feedbackataninstancelevel.png)

1. Dans la page de détails du cours, cliquez sur **[!UICONTROL Valeurs par défaut de l&#39;instance]** dans la section Configurer.
1. Dans la liste déroulante [!UICONTROL **Langue**], sélectionnez la langue dans laquelle vous souhaitez afficher le questionnaire de retour d&#39;informations.
1. Activez l’option Retour de réaction L1 si vous souhaitez demander des retours aux élèves. Vous pouvez ajouter jusqu’à deux questions dans cette section. Les élèves peuvent fournir des réponses descriptives à ces questions.
1. Cochez la case **[!UICONTROL Rendre obligatoire]** si vous souhaitez rendre l&#39;une ou l&#39;autre ou les deux questions obligatoires.
1. Sélectionnez **[!UICONTROL Afficher le questionnaire immédiatement après la fin du cours]** si vous souhaitez que les élèves consultent le questionnaire de retour d’informations immédiatement après avoir terminé le cours.

   ![](assets/configure-feedbackataninstancelevel-step7.png)

1. Pour configurer le retour d&#39;informations L3 sur le changement de comportement au niveau d&#39;une instance, **&#x200B;**&#x200B;[!UICONTROL Activez]&#x200B;**&#x200B;** le retour d&#39;informations L3. L’application affiche une question prédéfinie et obligatoire et une question vide dans laquelle vous pouvez saisir une question de votre choix.
1. Pour la question prédéfinie sur l’amélioration de l’élève après avoir suivi le cours, la réponse est au format Échelle de Likert. C&#39;est-à-dire que les responsables doivent choisir une option sur une échelle allant de Plutôt d’accord à Plutôt pas d’accord.
1. Précisez la deuxième question pour le responsable. Les responsables peuvent fournir une réponse descriptive à cette question.
1. Cochez la case **&#x200B;**&#x200B;[!UICONTROL Rendre obligatoire]&#x200B;**&#x200B;** si vous souhaitez rendre la deuxième question obligatoire.

   ![](assets/configure-feedbackataninstancelevel-step11.png)

1. Vous pouvez éventuellement configurer les paramètres de rappel au niveau de l’instance. Si vous ne configurez pas les paramètres de rappel ici, les paramètres de rappel globaux sont automatiquement attribués.
1. Après avoir terminé les questions de retour d&#39;informations et les paramètres de rappel, cliquez sur **[!UICONTROL **Enregistrer**]**&#x200B;pour appliquer vos paramètres.

   ***Remarque : les paramètres de retour d&#39;informations ne s&#39;appliquent pas aux certifications.***

## Configuration des paramètres généraux {#configuregeneralsettings}

Les paramètres généraux dans Learning Manager permettent aux administrateurs de configurer des paramètres génériques qui affectent d’autres fonctionnalités de l’application. Par exemple, vous pouvez utiliser des paramètres généraux pour spécifier si l’efficacité du cours peut être rendue visible aux élèves. Pour configurer les paramètres généraux :

1. Dans la page d’accueil de Learning Manager, cliquez sur **&#x200B;**&#x200B;[!UICONTROL Paramètres]&#x200B;**&#x200B;**.
1. Dans le volet de gauche, cliquez sur **&#x200B;**&#x200B;[!UICONTROL Général]&#x200B;**&#x200B;**.
1. Dans la page Paramètres généraux, vous pouvez configurer les options suivantes :

   Pour toutes ces options, la fonction affectée par chaque option est variable. Si nécessaire, nous pouvons fournir des liens croisés vers chaque fonctionnalité détaillée.

   * **Afficher l&#39;efficacité du cours** : Activez cette option si vous souhaitez que les élèves voient l’efficacité d’un cours sur le titre du cours.
   * **Option de réinitialisation du module** : Activez cette option si vous souhaitez donner aux apprenants la possibilité de réinitialiser un module. Les élèves peuvent réinitialiser leurs modules s’ils ont échoué ou s’ils ont partiellement terminé le module et souhaitent recommencer.
   * **Modération du cours** : Activez cette option si vous souhaitez que les modifications apportées à un cours soient approuvées par un administrateur avant que les modifications ne soient visibles par les apprenants.
   * **Forum de discussion** : Activez cette option si vous souhaitez que les élèves consultent les forums de discussion des cours et y participent. Si vous activez la case à cocher **Forum de discussion**, les élèves et les instructeurs peuvent publier des commentaires pour les cours. Cependant, si les paramètres de niveau de cours indiquent que cette fonctionnalité n’est pas sélectionnée, ces paramètres sont prioritaires par rapport aux paramètres de l’administrateur.

   * **Option Découvrir les compétences** : Activez cette option si vous souhaitez que les élèves explorent les compétences des pairs et du leadership.
   * **ID uniques d’objets d’apprentissage** : Activez cette option si vous souhaitez donner aux auteurs la possibilité d’ajouter des ID uniques aux objets d’apprentissage.
   * **Afficher la liste des catalogues** : Activez cette option si vous souhaitez que les élèves voient tous les catalogues disponibles. Cette option aide les élèves à affiner leur liste d’objets d’apprentissage.



   ![](assets/configure-generalsettings-step3.png)

## Configuration des paramètres du tableau de bord des élèves {#configurelearnerdashboardsettings}

Le tableau de bord des élèves de Learning Manager permet aux élèves d’afficher les cours obligatoires et recommandés, outre leurs réussites, compétences et annonces. Les administrateurs peuvent décider de l’affichage de ce tableau de bord des élèves en configurant les paramètres du tableau de bord des élèves. Ces paramètres permettent aux administrateurs de définir les widgets sur la page des élèves Ces paramètres spécifient également comment et où les widgets sont placés sur le tableau de bord des élèves. En tant qu’administrateur, vous pouvez prévisualiser la mise en page du tableau de bord des élèves avant d’appliquer les paramètres.

1. Dans la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL Paramètres]**.
1. Dans le volet de navigation de gauche, cliquez sur **[!UICONTROL **&#x200B; Tableau de bord des élèves &#x200B;**.]**
1. Sélectionnez les widgets que vous souhaitez activer. Si vous désélectionnez un widget, celui-ci est immédiatement supprimé de l’aperçu. Les élèves ne peuvent pas voir ce widget dans leur tableau de bord.
1. Cliquez sur **&#x200B;**&#x200B;[!UICONTROL Enregistrer]&#x200B;**&#x200B;** pour appliquer les paramètres.

   ![](assets/configure-learnerdashboardsettings-step4.png)

1. Pour appliquer les paramètres par défaut, cliquez sur **[!UICONTROL Restaurer les paramètres par défaut.]** Dans ce cas, tous les widgets sauf **[!UICONTROL Bienvenue et Annonces pense-bête]** sont visibles.

   ***Même après avoir activé les paramètres du tableau de bord des élèves, ces derniers peuvent modifier et déplacer les widgets dans leurs tableaux de bord respectifs.***

