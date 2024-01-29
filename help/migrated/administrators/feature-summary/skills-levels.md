---
description: Créer, attribuer et modifier des compétences et des niveaux.
jcr-language: en_us
title: Création et modification de compétences et de niveaux
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1718'
ht-degree: 0%

---



# Création et modification de compétences et de niveaux

Créer, attribuer et modifier des compétences et des niveaux.

La carte des compétences est un regroupement d’ensembles de compétences, de connaissances et de traits d’un employé au sein d’une organisation. Ces cartes de compétences aident les entreprises/organisations à définir ou à augmenter les attentes en matière de performance de leurs employés. Les compétences permettent aux employés d&#39;aligner leurs comportements sur les attentes de l&#39;organisation.

Adobe Learning Manager vous permet de mapper les performances des élèves en fonction de leurs compétences à l’aide de la carte des compétences. Une fois que les élèves ont terminé certains cours, ils peuvent connaître leur positionnement par rapport à chaque compétence en consultant les cartes de compétences.

L’objectif fondamental des compétences dans le LMS Learning Manager est de fournir à l’administrateur un outil qui aligne l’apprentissage sur les objectifs commerciaux.

## Ajouter une compétence {#addaskill}

En tant qu’administrateur, vous pouvez effectuer les opérations suivantes :

* Mappez un domaine à une compétence.
* Ajoutez plusieurs niveaux d’une compétence.
* Ajoutez un badge à un niveau.

Pour ajouter une compétence, procédez comme suit :

1. Dans le volet de gauche, cliquez sur **[!UICONTROL Compétences]**. Donnez un nom et une description à la compétence.

   ![](assets/add-skill-name-anddescription.png)

   *Ajouter le nom et la description d’une compétence*

1. Attribuez un domaine à la compétence. Lors de la création d’une compétence, vous pouvez la mapper avec les domaines de compétence les plus pertinents pris en charge par Learning Manager. Pour plus d’informations, voir [***Mapper les compétences avec les domaines***](/help/migrated/administrators/feature-summary/curation-skills.md).

   Commencez à saisir le domaine dans le champ et vous pouvez voir les recommandations. Choisissez l’option ou les options pertinentes pour la compétence.

   ![](assets/map-domain-with-skills.png)

   *Ajouter un domaine*

1. Attribuez les niveaux à la compétence. Pour ajouter un niveau, cliquez sur **[!UICONTROL Ajouter]**.

   Vous pouvez créer et affecter des compétences aux employés. Il y a différents niveaux de compétences et chaque niveau exige un certain nombre de crédits à gagner.

   Vous pouvez affecter un maximum de trois niveaux à une compétence. Le parcours d’apprentissage est celui qui consiste à inscrire des élèves à divers objets d’apprentissage, qui se traduisent ensuite par un certain nombre de crédits qui répondent aux exigences des différents niveaux d’une compétence.

   Une fois que ces objets d’apprentissage (LO) et niveaux ont été atteints, l’élève est désormais équipé pour effectuer des performances à un niveau plus productif qu’auparavant.

   ![](assets/add-skill-levels.png)

   *Ajouter des niveaux de compétence*

   Lorsque vous ajoutez une compétence, vous pouvez également affecter des décimales aux crédits. Les crédits sont affichés avec deux décimales maximum.

   La prise en charge des décimales est uniquement disponible en anglais.

1. Choisissez un badge pour le niveau. À partir de **[!UICONTROL Badge]** dans la liste déroulante, sélectionnez une image qui doit être utilisée comme badge pour ce niveau.
1. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

   Une fois la compétence créée, vous pouvez localiser la compétence nouvellement créée sur la page **[!UICONTROL Compétence]** page. Vous pouvez également voir les domaines et la brève description de la compétence. Vous pouvez également afficher les niveaux et les crédits qui ont été affectés à chaque niveau.

   ![](assets/list-of-skills.png)

   *Afficher la liste des compétences*

## Attribuer la compétence aux élèves {#assigntheskilltolearners}

Les administrateurs peuvent affecter les compétences aux élèves.

Une fois que vous avez créé vos compétences et que vous les avez enregistrées, elles sont répertoriées dans la page des compétences. Vous pouvez maintenant commencer à affecter ces compétences aux élèves comme suit :

1. Sur la **[!UICONTROL Compétence]** , cliquez sur l’hyperlien avec le nombre d’élèves inscrits à la compétence. Pour une compétence nouvellement créée, le nombre d’élèves pour tous les niveaux est égal à zéro.

   ![](assets/number-of-learnersenrolledtoaskill.png)

   *Afficher les élèves affectés à une compétence*

   Pour cet exemple, ajoutez des élèves pour le niveau 1. Cliquez sur l’hyperlien en regard de Niveau 1.

1. Dans la boîte de dialogue Élèves, cliquez sur **[!UICONTROL Ajouter des élèves]**.

   ![](assets/add-learners.png)

   *Ajouter des élèves*

1. Recherchez des élèves et ajoutez-les. Vous pouvez également ajouter des groupes d’utilisateurs.

   ![](assets/search-and-add-learners.png)

   *Rechercher et ajouter des élèves*

1. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

   Une fois que vous avez affecté des élèves, tous les élèves d&#39;un groupe d&#39;utilisateurs, le cas échéant, sont automatiquement inscrits à la compétence, par défaut. Vous pouvez faire en sorte que les élèves choisissent de ne pas s’inscrire automatiquement en cliquant sur le bouton **[!UICONTROL Inscription automatique]** bouton.

   ![](assets/turn-off-auto-enrollment.png)

   *Désactiver l’inscription automatique*

   Chaque élève peut s&#39;inscrire automatiquement ou peut être inscrit par l&#39;administrateur à un programme d&#39;apprentissage.

1. Après avoir cliqué **[!UICONTROL Fermer]**, vous pouvez voir le nombre total d’élèves qui ont été affectés à la compétence que vous aviez créée.

   Dans cet exemple, il y a deux élèves individuels et trois élèves dans un groupe d&#39;utilisateurs.

   ![](assets/learners-assignedtoaskill.png)

   *Nombre d’élèves affectés à une compétence*

## Attribuer la compétence à un cours {#assignskilltocourse}

Une fois que vous avez créé la compétence, un auteur peut créer un cours et attribuer la compétence au cours.

![](assets/assign-skill-to-acourse.png)

*Attribution de compétences à un cours*

Une fois que l’auteur a publié le cours, sur la page **[!UICONTROL Compétence]** , vous pouvez voir le nombre de cours associés à un niveau de compétence, qui est incrémenté lorsque vous affectez la compétence à un nouveau cours.

![](assets/skill-assigned-tothecourse.png)

*Nombre de cours associés à un niveau de compétence*

## Affecter une assistance à la tâche à la compétence {#assignajobaidtotheskill}

Les assistances à la tâche sont du contenu de formation auquel un élève peut accéder sans s’inscrire à un objet d’apprentissage spécifique comme un cours ou un programme d’apprentissage.

Lors de la création d’une assistance à la tâche, un auteur peut lui associer un niveau de compétence. La création d&#39;une assistance à la tâche sans compétence et son association à un cours avec une compétence ne relie pas la compétence à l&#39;assistance à la tâche.

![](assets/create-a-job-aid.png)

*Création d’une assistance à la tâche*

Sur la **[!UICONTROL Compétence]** , vous pouvez voir le nombre d&#39;assistances à la tâche associées à ce niveau de compétence.

![](assets/job-aid-assignedtotheskill.png)

*Nombre d&#39;assistances à la tâche d&#39;une compétence*

## Rechercher une compétence {#searchskill}

Recherchez une compétence en saisissant son nom et en la choisissant parmi les options disponibles. La recherche par frappe anticipée s’applique également ici.

Vous pouvez rechercher des compétences dans les deux **[!UICONTROL Actif]** et **[!UICONTROL Retraité]** de la page Compétences.

## Modifier une compétence {#editaskill}

Sur la **[!UICONTROL Compétence]** , cliquez sur la compétence que vous souhaitez modifier. Dans le panneau **[!UICONTROL Modifier la compétence]** , effectuez les modifications requises, par exemple,

* Ajout ou suppression d’un domaine de compétence.
* Modification du nom et de la description de la compétence.
* Ajouter un niveau de compétence ou modifier un niveau existant.
* Ajouter ou supprimer un badge pour une compétence.

Après avoir apporté les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

## Retrait d’une compétence {#retireaskill}

Pour retirer une compétence, sur la page **[!UICONTROL Compétence]** , sélectionnez la compétence que vous souhaitez retirer.

À partir de **[!UICONTROL Actions]** dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Retirer]**.

Lorsque vous retirez une compétence, celle-ci n’apparaît plus sur le cours.

Lorsqu&#39;une compétence est retirée, elle ne peut pas être associée à d&#39;autres cours ou assistances à la tâche, ni affectée à des élèves tant qu&#39;elle n&#39;est pas republiée. Les associations et les affectations existantes ne sont pas affectées par le retrait de la compétence.

## Republier une compétence {#republishaskill}

Une fois que vous avez retiré une compétence, la compétence retirée apparaît dans le panneau **[!UICONTROL Retraité]** onglet. L’onglet affiche la liste de toutes les compétences retirées.

Pour republier une compétence retirée, choisissez la compétence, puis choisissez l’une des **[!UICONTROL Actions]** , cliquez sur **[!UICONTROL Republier]**.

Cela restaure la compétence et vous pouvez la voir à nouveau dans le panneau **[!UICONTROL Actif]** onglet.

## Supprimer une compétence {#deleteaskill}

Vous ne pouvez supprimer qu’une compétence précédemment retirée.

Dans le panneau **[!UICONTROL Retraité]** , sélectionnez la compétence que vous souhaitez supprimer, puis dans le menu **[!UICONTROL Actions]** , cliquez sur **[!UICONTROL Supprimer]**.

Vous pouvez supprimer une compétence uniquement lorsqu’elle n’est associée à aucun élève, cours ou assistances à la tâche.

## Attribution de compétences aux instructeurs

Ajoutez un fichier CSV composé des compétences des instructeurs. Ces compétences sont ensuite ajoutées à la liste des compétences.

1. Dans le coin supérieur droit de l’écran, sélectionnez **[!UICONTROL Ajouter]** > **[!UICONTROL Attribution de compétences à un instructeur]**.
1. Chargez un fichier CSV. Les colonnes du fichier CSV sont les suivantes :

   * Nom de la compétence
   * Niveau de compétence
   * E-mail de l’instructeur ou UUID de l’instructeur

   Pour les comptes UUID, remplacez la colonne E-mail de l’instructeur par UUID de l’instructeur.

   Cliquez sur Enregistrer.

   ![Ajouter un fichier CSV de compétences d’instructeur](assets/instructor-skills.png)

   *Ajout de compétences d’instructeur à partir d’un fichier CSV*

1. Un message contextuel de confirmation s’affiche.

   Remarque : le message d’erreur suivant s’affiche si le fichier CSV comporte des champs incorrects.

   ![Message d’erreur si le fichier CSV contient des champs incorrects](assets/error-csv-upload.png)

   *Message d’erreur pour les champs incorrects*

### Page Compétences

Sur la page Compétences, une colonne intitulée Instructeurs indique le nombre d’instructeurs affectés à une compétence. Si vous cliquez sur le nombre d’instructeurs, une fenêtre contextuelle s’affiche, affichant les instructeurs affectés à la compétence.

![Compétences attribuées aux instructeurs](assets/instructor-skill-assigned.png)

*Page Compétences*

### Télécharger le fichier CSV d’affectation de compétences

1. Sur la page Compétences, cliquez sur **[!UICONTROL Ajouter]** > **[!UICONTROL Attribution de compétences à un instructeur]**.
1. Dans la boîte de dialogue, cliquez sur **[!UICONTROL Affectation ajoutée précédemment]**.
1. Le fichier CSV que vous avez chargé en dernier sera téléchargé.

>[!NOTE]
>
>Nous vous recommandons de télécharger d’abord le fichier CSV d’affectation de compétences, de le modifier, puis de charger le fichier.

## Foire aux questions {#frequentlyaskedquestions}

+++Comment puis-je supprimer un élève d’une compétence ?

Vous ne pouvez pas supprimer un élève d’une compétence. Vous pouvez toutefois ajouter de nouveaux élèves ou groupes d’utilisateurs à la compétence.
+++

+++Comment inscrire automatiquement des élèves à une compétence ?

La fonctionnalité d’inscription automatique est réservée aux groupes d’utilisateurs. Lorsque vous inscrivez un groupe d’utilisateurs, par exemple Tous les auteurs, à une compétence et l’enregistrez, l’inscription automatique est activée par défaut. Ainsi, tout nouvel ajout au groupe d’utilisateurs Tous les auteurs se voit également attribuer la compétence.

Si vous arrêtez l’inscription automatique pour ce niveau de compétence pour Tous les auteurs, les nouveaux utilisateurs qui sont ajoutés au groupe d’utilisateurs Tous les auteurs ne se voient pas attribuer la compétence.
+++

+++Comment redémarrer l’inscription automatique ?

Inscrivez à nouveau le même groupe d’utilisateurs au niveau de compétence pour lequel l’inscription automatique avait été interrompue.

Cela permet de redémarrer l’inscription automatique et les élèves qui ont été ajoutés au groupe lorsque cette fonctionnalité était désactivée se voient désormais attribuer la compétence.

En d’autres termes, chaque fois que vous réinscrivez un groupe d’utilisateurs pour démarrer l’inscription automatique, il actualise les membres du groupe d’utilisateurs et affecte la compétence à tous les membres actuels.
+++

+++Comment puis-je affecter une compétence à un cours ?

Voir la section [Attribution de compétences à un cours](skills-levels.md#assignskilltocourse) pour plus d&#39;informations sur la procédure.
+++

+++Comment modifier un niveau de compétence ?

Pour modifier un ou plusieurs niveaux d’une compétence, modifiez la compétence et modifiez les propriétés des niveaux existants.
+++

+++Comment puis-je activer les badges et les compétences afin qu’ils soient liés à l’achèvement du cours ?

Les compétences peuvent être liées à l&#39;achèvement du cours lors de la création d&#39;un cours en tant qu&#39;auteur. Dans la section Paramètres, vous pouvez définir les critères de compétence pour l’achèvement du cours.

![](assets/course-skills.png)

Pour activer les badges pour terminer le cours, dans la section **[!UICONTROL Instances]** de l’application d’auteur, activez le badge requis.
+++

+++ Un administrateur peut-il marquer un badge comme terminé même s’il indique « En cours » ?

Un administrateur peut marquer un objet d’apprentissage comme terminé. La compétence et les badges sont associés à l’objet d’apprentissage et ne peuvent pas être marqués **[!UICONTROL Terminé]** séparément.

Autrement dit, pour obtenir le badge, **vous devez terminer l’objet d’apprentissage associé**.
+++

### Plus comme ceci

* [Learning Manager Compétences et Adobe](https://elearning.adobe.com/2018/11/skills-captivate-prime/)
