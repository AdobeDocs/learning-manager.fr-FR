---
description: Créez, attribuez et modifiez des compétences et niveaux.
jcr-language: en_us
title: Création et modification de compétences et niveaux
contentowner: manochan
exl-id: b1461900-43e8-4e9d-bef1-a55c44d3bc8b
source-git-commit: b882c22da029cdc4c8bcc4ab1b6d861f06f83f0f
workflow-type: tm+mt
source-wordcount: '1721'
ht-degree: 79%

---

# Création et modification de compétences et niveaux

Créez, attribuez et modifiez des compétences et niveaux.

Une carte de compétences est un regroupement d’ensembles de compétences, de connaissances et de caractéristiques d’un employé dans une organisation. Ces cartes de compétences aident les entreprises/organisations à définir ou augmenter leurs attentes en termes de performance de leurs employés. Les compétences permettent aux employés d’aligner leurs comportements sur les attentes de leur entreprise.

Adobe Learning Manager vous permet de déterminer les performances des élèves en fonction de leurs compétences à l’aide de la carte des compétences. Une fois que les élèves ont terminé certains cours, ils peuvent connaître leur positionnement par rapport à chaque compétence en consultant les cartes de compétences.

Le but fondamental des compétences dans le système de gestion d’apprentissage (LMS) Learning Manager est de fournir à l’administrateur un outil qui adapte l’apprentissage aux objectifs de l’entreprise.

## Ajout d’une compétence {#addaskill}

En tant qu’administrateur, vous pouvez réaliser les actions suivantes :

* Mapper une compétence à un domaine
* Ajouter plusieurs niveaux à une compétence
* Ajouter un badge à un niveau

Pour ajouter une compétence, suivez les étapes ci-dessous :

1. Dans le volet de gauche, sélectionnez **[!UICONTROL Compétences]** > **[!UICONTROL Ajouter]** > **[!UICONTROL Ajouter des compétences]**. Donnez un nom et une description à la compétence.

   ![](assets/add-skill-name-anddescription.png)

   *Ajouter le nom et la description d’une compétence*

1. Attribuez un domaine à la compétence. Lors de la création d’une compétence, vous pouvez la mapper avec les domaines de compétence les plus pertinents pris en charge par Learning Manager. Pour plus d’informations, voir [***Mappage de compétences avec les domaines***](/help/migrated/administrators/feature-summary/curation-skills.md).

   Commencez à saisir le domaine dans le champ et les recommandations s’affichent. Sélectionnez l’option ou les options adaptées à la compétence.

   ![](assets/map-domain-with-skills.png)

   *Ajouter un domaine*

1. Attribuez les niveaux à la compétence. Pour ajouter un niveau, cliquez sur **[!UICONTROL Ajouter]**.

   Vous pouvez créer et attribuer des compétences aux employés. Il existe différents niveaux de compétences et chaque niveau nécessite un certain nombre de crédits.

   Vous pouvez attribuer un maximum de trois niveaux à une compétence. Le cursus d’apprentissage consiste à inscrire les élèves à divers objets d’apprentissage, qui se traduisent ensuite par un certain nombre de crédits répondant aux exigences des différents niveaux d’une compétence.

   Une fois que ces objets d’apprentissage et niveaux ont été atteints, l’élève est à présent capable d’augmenter sa productivité.

   ![](assets/add-skill-levels.png)

   *Ajouter des niveaux de compétence*

   Lorsque vous ajoutez une compétence, vous pouvez également attribuer des décimales aux crédits. Les crédits sont affichés jusqu’à deux décimales.

   La prise en charge des décimales n’est disponible qu’en anglais.

1. Sélectionnez un badge pour le niveau. Dans la liste déroulante **[!UICONTROL Badge]**, sélectionnez une image qui doit être utilisée comme badge pour ce niveau.
1. Cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications.

   Une fois la compétence créée, vous pouvez la localiser dans la page **[!UICONTROL Compétence]**. Vous pouvez également y consulter les domaines et la description rapide de la compétence. Vous pouvez également afficher les niveaux et les crédits attribués à chaque niveau.

   ![](assets/list-of-skills.png)

   *Afficher la liste des compétences*

## Attribution de la compétence aux élèves {#assigntheskilltolearners}

Les administrateurs peuvent attribuer des compétences aux élèves.

Une fois que vos compétences sont créées et enregistrées, elles sont répertoriées dans la page Compétences. Vous pouvez maintenant commencer à attribuer ces compétences aux élèves de la façon suivante :

1. Sur la page **[!UICONTROL Compétence]**, cliquez sur le lien hypertexte indiquant le nombre d’élèves inscrits à la compétence. Pour une nouvelle compétence, le nombre d’élèves est égal à zéro pour tous les niveaux.

   ![](assets/number-of-learnersenrolledtoaskill.png)

   *Afficher les élèves affectés à une compétence*

   Pour cet exemple, ajoutez des élèves au niveau 1. Cliquez sur le lien hypertexte adjacent au niveau 1.

1. Dans la boîte de dialogue Élèves, cliquez sur **[!UICONTROL Ajouter des élèves]**.

   ![](assets/add-learners.png)

   *Ajout d’élèves*

1. Recherchez des élèves et ajoutez-les. Vous pouvez également ajouter des groupes d’utilisateurs.

   ![](assets/search-and-add-learners.png)

   *Rechercher et ajouter des élèves*

1. Cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications.

   Une fois que vous avez attribué les élèves, tous les élèves d’un groupe d’utilisateurs, le cas échéant, sont automatiquement inscrits à la compétence, par défaut. Vous pouvez forcer les élèves à se désinscrire de l’inscription automatique en cliquant sur le bouton **[!UICONTROL Inscription automatique]**.

   ![](assets/turn-off-auto-enrollment.png)

   *Désactiver l’inscription automatique*

   Chaque élève peut s&#39;inscrire automatiquement ou peut être inscrit par l&#39;administrateur à un programme d&#39;apprentissage.

1. Après avoir cliqué sur **[!UICONTROL Fermer]**, vous pouvez voir le nombre total d’élèves attribués à la compétence que vous avez créée.

   Dans cet exemple, il y a deux élèves individuels et trois élèves appartenant à un groupe d’utilisateurs.

   ![](assets/learners-assignedtoaskill.png)

   *Nombre d’élèves affectés à une compétence*

## Attribution de la compétence à un cours {#assignskilltocourse}

Une fois que vous avez créé la compétence, un auteur peut créer un cours et lui attribuer la compétence.

![](assets/assign-skill-to-acourse.png)

*Attribution de compétences à un cours*

Après la publication du cours par l’auteur, sur la page **[!UICONTROL Compétences]**, vous pouvez voir le nombre de cours associés à un niveau de compétence ; ce nombre augmente lorsque vous attribuez la compétence à un nouveau cours.

![](assets/skill-assigned-tothecourse.png)

*Nombre de cours associés à un niveau de compétence*

## Attribution d’une assistance à la tâche à la compétence {#assignajobaidtotheskill}

Les assistances à la tâche constituent du contenu de formation auquel un élève peut accéder sans s’inscrire à un objet d’apprentissage spécifique comme un cours ou un programme d’apprentissage.

Lors de la création d’une assistance à la tâche, un auteur peut y associer un niveau de compétence. La création d’une assistance à la tâche sans compétence et son association à un cours comprenant une compétence ne lie pas la compétence à l’assistance à la tâche.

![](assets/create-a-job-aid.png)

*Création d’une assistance à la tâche*

Sur la page **[!UICONTROL Compétence]**, vous pouvez voir le nombre d’assistances à la tâche associées à ce niveau de compétence.

![](assets/job-aid-assignedtotheskill.png)

*Nombre d&#39;assistances à la tâche d&#39;une compétence*

## Recherche d’une compétence {#searchskill}

Recherchez une compétence en saisissant son nom et en la sélectionnant parmi les options présentes. La recherche par frappe anticipée s’applique également ici.

Vous pouvez rechercher des compétences dans les sections **[!UICONTROL Active]** et **[!UICONTROL Retirée]** de la page Compétences.

## Modification d’une compétence {#editaskill}

Sur la page **[!UICONTROL Compétence]**, cliquez sur la compétence que vous souhaitez modifier. Dans le panneau **[!UICONTROL Modifier la compétence]** , effectuez les modifications requises, par exemple,

* Ajout ou suppression d’un domaine de compétence
* Modification du nom et de la description de la compétence
* Ajout d’un niveau de compétence ou modification d’un niveau existant
* Ajout ou suppression d’un badge à une compétence

Après avoir effectué les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

## Retrait d’une compétence {#retireaskill}

Pour retirer une compétence, sur la page **[!UICONTROL Compétence]**, sélectionnez la compétence que vous souhaitez retirer.

Dans le menu **[!UICONTROL Actions]**, situé dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Retirer]**.

Lorsque vous retirez une compétence, celle-ci n’apparaît plus dans le cours.

Lorsqu’une compétence est retirée, elle ne peut plus être associée à des cours ou à des assistances à la tâche, ni être attribuée à des élèves jusqu’à ce qu’elle soit republiée. Les associations et attributions existantes ne sont pas modifiées par le retrait de la compétence.

## Republication d’une compétence {#republishaskill}

Une fois que vous avez retiré une compétence, celle-ci apparaît dans l’onglet **[!UICONTROL Retirée]**. L’onglet affiche la liste de toutes les compétences retirées.

Pour republier une compétence retirée, sélectionnez la compétence, puis dans le menu **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Republier]**.

Cette action restaure la compétence et vous pouvez à nouveau la trouver dans l’onglet **[!UICONTROL Active]**.

## Suppression d’une compétence {#deleteaskill}

Vous pouvez uniquement supprimer une compétence qui a été retirée.

Dans l’onglet **[!UICONTROL Retiré]**, sélectionnez la compétence que vous souhaitez supprimer, puis dans le menu **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Supprimer]**.

Vous pouvez uniquement supprimer une compétence lorsqu’elle n’est associée à aucun élève, cours ou assistance à la tâche.

## Attribuer des compétences aux instructeurs

Ajoutez un fichier CSV qui contient les compétences des instructeurs. Ces compétences sont ensuite ajoutées à la liste des compétences.

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

La page Compétences comporte une colonne intitulée Instructeurs qui indique le nombre d’instructeurs associés à une compétence. Si vous cliquez sur le nombre d’instructeurs, une fenêtre contextuelle s’affiche, affichant les instructeurs affectés à la compétence.

![Compétences attribuées aux instructeurs](assets/instructor-skill-assigned.png)

*Page Compétences*

### Télécharger le fichier CSV d’affectation de compétences

1. Sur la page Compétences, cliquez sur **[!UICONTROL Ajouter]** > **[!UICONTROL Attribution de compétences à un instructeur]**.
1. Dans la boîte de dialogue, cliquez sur **[!UICONTROL Affectation ajoutée précédemment]**.
1. Le fichier CSV que vous avez chargé en dernier sera téléchargé.

>[!NOTE]
>
>Nous vous recommandons de télécharger d’abord le fichier CSV d’attribution de compétences, de le modifier, puis de charger le fichier.

## Forum aux questions {#frequentlyaskedquestions}

+++Comment puis-je supprimer un élève d’une compétence ?

Vous ne pouvez pas retirer un élève d’une compétence. Vous pouvez cependant ajouter de nouveaux élèves ou groupes d’utilisateurs à la compétence.
+++

+++Comment inscrire automatiquement des élèves à une compétence ?

La fonction d’inscription automatique est réservée aux groupes d’utilisateurs. L’inscription automatique est activée par défaut lorsque vous inscrivez un groupe d’utilisateurs, comme par exemple, Tous les auteurs, à une compétence et que vous l’enregistrez. Ainsi, la compétence sera attribuée à tout nouvel utilisateur ajouté au groupe d’utilisateurs Tous les auteurs.

Si vous désactivez l’inscription automatique à ce niveau de compétence pour Tous les auteurs, la compétence ne sera pas attribuée aux nouveaux utilisateurs ajoutés à ce groupe d’utilisateurs.
+++

+++Comment redémarrer l’inscription automatique ?

Inscrivez à nouveau le même groupe d’utilisateurs au niveau de compétence pour lequel l’inscription automatique a été désactivée.

Cette opération réactive l’inscription automatique et les élèves qui ont été ajoutés au groupe lorsque cette fonction était désactivée se voient désormais attribuer la compétence.

Autrement dit, à chaque fois que vous réactivez l’inscription automatique pour un groupe d’utilisateurs, les membres du groupe d’utilisateurs sont réactualisés et la compétence est attribuée à tous les membres actuels.
+++

+++Comment puis-je affecter une compétence à un cours ?

Voir la section [Attribution d’une compétence à un cours](skills-levels.md#assignskilltocourse) pour obtenir plus d’informations sur la procédure.
+++

+++Comment modifier un niveau de compétence ?

Pour modifier un ou plusieurs niveaux dans une compétence, modifiez cette dernière et modifiez les propriétés des niveaux existants.
+++

+++Comment puis-je activer les badges et les compétences afin qu’ils soient liés à l’achèvement du cours ?

Les compétences peuvent être liées à l’achèvement d’un cours lors de la création de ce cours par un auteur. Dans la section Paramètres, vous pouvez définir les critères de compétence pour l’achèvement du cours.

![](assets/course-skills.png)

Pour activer des badges pour l’achèvement du cours, dans la section **[!UICONTROL Instances]** de l’application d’auteur, activez le badge requis.
+++

+++ Un administrateur peut-il marquer un badge comme terminé même s’il indique « En cours » ?

Un administrateur peut marquer un objet d’apprentissage comme terminé. Les compétences et les badges sont associés à l’objet d’apprentissage et ne peuvent pas être marqués comme **[!UICONTROL Terminés]** séparément.

En d’autres termes, pour obtenir le badge, **un élève doit terminer l’objet d’apprentissage associé**.
+++

### Articles connexes

* [Learning Manager Compétences et Adobe](https://elearning.adobe.com/2018/11/skills-captivate-prime/)
