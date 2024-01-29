---
description: Création de plans d’apprentissage pour les administrateurs dans Learning Manager.
jcr-language: en_us
title: Plans d’apprentissage
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---


# Plans d’apprentissage

Création de plans d’apprentissage pour les administrateurs dans Learning Manager.

## Présentation {#overview}

Un plan d’apprentissage est un ensemble de règles qui inscrivent des élèves à des formations spécifiques en fonction de certains critères.

Un plan d’apprentissage permet à un administrateur d’attribuer automatiquement des cours, des programmes d’apprentissage ou des certifications en fonction de certains événements tels que l’intégration d’un nouvel employé ou le changement de désignation ou de lieu des employés.

Par exemple, lorsqu&#39;un employé rejoint une organisation, le programme d&#39;orientation des nouveaux employés lui est automatiquement affecté. De même, si un employé est promu à titre de gestionnaire, un nouveau programme d&#39;orientation des gestionnaires lui est automatiquement attribué.

Vous pouvez inscrire automatiquement des élèves à n&#39;importe quel cours et programme d&#39;apprentissage en fonction d&#39;un ensemble prédéfini d&#39;événements. Vous pouvez créer des parcours d’apprentissage pour les élèves en affectant automatiquement une activité d’apprentissage de suivi une fois qu’un élève a terminé une compétence, un cours ou un programme d’apprentissage.

## Créer des plans d’apprentissage {#createlearningplans}

Pour créer un plan d&#39;apprentissage, vous devez vous connecter en tant qu&#39;administrateur.

1. Dans le volet de gauche, cliquez sur **[!UICONTROL Plans d’apprentissage]**. S’il existe des événements existants, ils sont répertoriés sur la page. Toutefois, si vous configurez la fonction de plan d&#39;apprentissage pour la première fois, passez à l&#39;étape suivante.
1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Ajouter]**. Dans le panneau **[!UICONTROL Ajouter un plan d’apprentissage]** , saisissez le nom du plan d’apprentissage qu’un employé doit suivre.

   ![](assets/add-learning-plandialog.png)

1. Dans le panneau **[!UICONTROL Se produit lorsque]** dans la liste déroulante, sélectionnez l’événement requis. Les options déterminent quand un élève suit le cours. Après avoir sélectionné le type d’événement, sélectionnez la formation, les cours, le programme d’apprentissage ou la certification appropriés.

   **Remarque :** Les administrateurs et les auteurs peuvent créer des événements d’inscription automatique.

   Les événements sont les suivants :

   **1 - Nouvel élève ajouté :** Lorsqu’un nouvel utilisateur ou un employé rejoint l’organisation.

   ![](assets/new-learner-is-added.png)

   **2 - L’élève est ajouté à un groupe :** Lorsqu’un nouvel utilisateur ou un employé rejoint un groupe.  Saisissez et sélectionnez le groupe d’utilisateurs dans la liste déroulante, auquel cet événement est applicable. Vous pouvez choisir plusieurs groupes. En outre, vous pouvez attribuer cet événement à tous les membres existants de ces groupes en sélectionnant l’option.

   ![](assets/learner-gets-addedtoagroup.png)

   Ce plan d’apprentissage est spécialement conçu pour ***Personnalisé - Groupe*** utilisateurs. Saisissez le nom du groupe dans le champ et, à l’aide de la recherche par frappe anticipée, choisissez le ou les groupes.

   **3 - L’élève termine un objet d’apprentissage :** L’événement est déclenché lorsqu’un élève termine un objet d’apprentissage tel qu’un cours, un programme d’apprentissage, etc. Sélectionnez l’objet d’apprentissage pour lequel cet événement est applicable. Sélectionnez l’état d’achèvement de l’événement. Si vous le souhaitez, vous pouvez également choisir le groupe d’utilisateurs auquel cet élève appartient. Entrez le nombre de jours pendant lesquels cet événement est déclenché une fois l&#39;objet d&#39;apprentissage terminé. Sélectionnez l&#39;option si vous souhaitez affecter cet événement à des utilisateurs existants qui ont déjà terminé cet objet d&#39;apprentissage.

   ![](assets/learner-completealearningobject.png)

   **4 - L’élève atteint un niveau de compétence :** Saisissez le nom de la compétence et sélectionnez le niveau de compétence. Vous pouvez également choisir le groupe d’utilisateurs auquel cet élève appartient. Elle est facultative. Entrez le nombre de jours, après avoir atteint la compétence, pendant lesquels cet événement est déclenché. Sélectionnez l’option si vous souhaitez affecter cet événement à des élèves existants qui ont déjà acquis cette compétence.

   ![](assets/learner-achievesaskilllevel.png)

   En outre, définissez le nombre de jours après lesquels le plan d’apprentissage doit être attribué aux élèves.

   ![](assets/assign-learning.png)

   **5 - À une date précise :** Lorsque les événements doivent se produire à une date spécifique. Sélectionnez la date à laquelle l’événement doit être affecté. Sélectionnez les groupes d’utilisateurs pour lesquels l’événement doit être automatiquement affecté. Sélectionnez les instances à affecter et, éventuellement, saisissez après combien de jours l&#39;événement doit être déclenché.

   ![](assets/on-a-specific-date.png)

1. Pour tous les événements, vous pouvez sélectionner l’instance dans le panneau **[!UICONTROL Instance]** liste déroulante. Vous pouvez également sélectionner des instances de l’apprentissage attribué pour n’importe quel événement.

   ![](assets/choose-instance.png)

   Dans Learning Manager, un plan d’apprentissage crée sa propre instance, Auto. Lorsque vous choisissez un groupe, par exemple Tous les élèves, tous les élèves du plan d&#39;apprentissage sont inscrits par défaut à l&#39;instance Auto.

   Lorsque vous enregistrez le plan d’apprentissage, l’instance Auto apparaît comme une option dans le panneau **[!UICONTROL Sélectionner une instance]** liste déroulante dans la section Élèves d’un cours.

1. Pour enregistrer le plan d’apprentissage, cliquez sur **[!UICONTROL Enregistrer]**.

## Se désinscrire de la formation {#unenroll-training}

Lors de l’ajout d’un plan d’apprentissage, un administrateur peut désinscrire des utilisateurs de formations spécifiques en fonction de certains déclencheurs.

Dans l’application d’administration, cliquez sur **[!UICONTROL Plans d’apprentissage]** > **[!UICONTROL Ajouter]**.

Les sections suivantes représentent les déclencheurs où l’option **[!UICONTROL Se désinscrire de la formation]** a été ajouté.

## L’élève est supprimé d’un groupe {#learnergetsremovedfromagroup}

1. Ajoutez un ou plusieurs groupes d’utilisateurs. Si plusieurs groupes sont sélectionnés, le plan est déclenché lorsqu’un élève est supprimé de l’un des groupes mentionnés.
1. Choisir l’action en tant que **[!UICONTROL Se désinscrire de la formation]**.

   1. L’administrateur peut choisir les formations desquelles l’utilisateur sera désinscrit lorsqu’il sera supprimé du groupe d’utilisateurs.
   1. L’instance et la date d’achèvement ne s’appliqueront pas à ce scénario.

![](assets/image038.png)

## L’élève termine une formation {#learnercompletesatraining}

1. Ajoutez un ou plusieurs groupes d’utilisateurs. Si plusieurs groupes sont sélectionnés, le plan est déclenché lorsqu’un élève termine la formation spécifiée.
1. Choisir l’action en tant que **[!UICONTROL Se désinscrire de la formation]**.

   1. L’administrateur peut choisir les formations desquelles l’utilisateur sera désinscrit lorsqu’il sera ajouté au groupe d’utilisateurs.
   1. L’instance et la date d’achèvement ne s’appliqueront pas à ce cas.

![](assets/image040.png)

## L’élève est ajouté à un groupe {#learnergetsaddedtoagroup}

1. Ajoutez un ou plusieurs groupes d’utilisateurs. Si plusieurs groupes sont sélectionnés, le plan est déclenché lorsqu’un élève est ajouté à l’un des groupes mentionnés.
1. Sélectionnez l’action Se désinscrire de la formation.

   1. L’administrateur peut choisir les formations desquelles l’utilisateur sera désinscrit lorsqu’il sera ajouté au groupe d’utilisateurs.
   1. L’instance et la date d’achèvement ne s’appliqueront pas à ce cas.

![](assets/image043.png)

## L’élève atteint un niveau de compétence {#learnerachievesaskilllevel}

1. Spécifiez la compétence à acquérir.
1. Ajoutez un ou plusieurs groupes d’utilisateurs. Si plusieurs groupes sont sélectionnés, le plan est déclenché lorsqu’un élève acquiert la compétence sélectionnée.

![](assets/image045.png)

## À une date spécifique {#onaspecificdate}

1. Sélectionnez la date à laquelle les élèves doivent être désinscrits.
1. Ajoutez un ou plusieurs groupes d’utilisateurs. Si plusieurs groupes sont sélectionnés, le plan est déclenché à la date spécifiée et désinscrit les utilisateurs, qui font partie des groupes sélectionnés.
1. Sélectionnez l’action Se désinscrire de la formation.

   1. L’administrateur peut choisir les formations desquelles l’utilisateur sera désinscrit lorsqu’il sera désinscrit à la date spécifiée.
   1. L’instance et la date d’achèvement ne s’appliqueront pas à ce cas.

![](assets/image047.png)

## Modifier un plan d’apprentissage {#editalearningplan}

Après avoir créé un plan d&#39;apprentissage, l&#39;administrateur peut modifier/mettre à jour le plan d&#39;apprentissage à tout moment. Pour Modifier, cliquez sur le nom du plan d&#39;apprentissage et modifiez les valeurs dans le champ **[!UICONTROL Modifier le plan d’apprentissage]** la boîte de dialogue contextuelle qui s’affiche. Cliquez sur **[!UICONTROL Enregistrer]**.

## Activation d’un plan d’apprentissage {#enablealearningplan}

Par défaut, tous les nouveaux plans d’apprentissage que vous avez créés sont désactivés. Vous devez activer un plan pour qu’un élève soit affecté à. Lorsque vous activez la case à cocher **[!UICONTROL Élèves actuels]**, l’événement est activé par lui-même.

Pour activer un plan d’apprentissage :

1. Dans la liste des plans d’apprentissage, choisissez le plan que vous souhaitez activer.

   ![](assets/list-of-learningplans.png)

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Activer]**. Cela active le plan d’apprentissage.

## Supprimer un plan d’apprentissage {#deletealearningplan}

Pour supprimer un plan d’apprentissage :

1. Dans la liste des plans d’apprentissage, choisissez le plan que vous souhaitez supprimer.
1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Supprimer]**.

## Désactiver un plan d’apprentissage {#disablealearningplan}

Pour désactiver un plan d’apprentissage :

1. Cliquez sur l’onglet **[!UICONTROL Activé]**.
1. Dans la liste des plans d’apprentissage, choisissez le plan que vous souhaitez désactiver.
1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Désactiver]**. Le plan est alors déplacé vers la page **[!UICONTROL Désactivé]** onglet.

## Filtrage d’un plan d’apprentissage {#filteralearningplan}

Vous pouvez filtrer les plans d’apprentissage en fonction du type d’événement utilisé lors de la création d’un plan d’apprentissage. Cliquez sur **[!UICONTROL Type]** et choisissez une option pour afficher les plans d’apprentissage qui correspondent à la sélection.

![](assets/filter-a-learningplan.png)

## Foire aux questions {#frequentlyaskedquestions}

1. Comment configurer Learning Manager pour configurer les inscriptions automatiques pour l’intégration des nouvelles recrues ?

   Dans le panneau **[!UICONTROL Se produit lorsque]** dans la liste déroulante, sélectionnez l’option **[!UICONTROL Nouvel élève ajouté]**. Attribuez ensuite les objets d’apprentissage, l’instance et la date d’achèvement à l’élève. Les administrateurs et les auteurs peuvent créer des événements d’inscription automatique. Activez l’événement après l’avoir créé.

1. Comment configurer un plan d’apprentissage/une inscription automatique pour les cours en salle de classe et en salle de classe virtuelle ?

   Il est recommandé de configurer l&#39;instance de cours avec les détails de session requis. Ensuite, configurez un plan d’apprentissage et mappez-le à l’instance de cours, qui a déjà été créée.

1. Comment afficher la liste des élèves inscrits à un plan d’apprentissage spécifique ?

   Une fois l’instance Auto créée, cliquez sur **[!UICONTROL Cours]** > **[!UICONTROL Élèves]**, puis sélectionnez l&#39;instance requise dans le menu **[!UICONTROL Instance]** liste déroulante.
