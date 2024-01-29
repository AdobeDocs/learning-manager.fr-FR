---
description: Découvrez comment créer des certifications, inscrire des élèves et modifier des certifications publiées.
jcr-language: en_us
title: Certifications
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---



# Certifications

Découvrez comment créer des certifications, inscrire des élèves et modifier des certifications publiées.

Certifiez vos élèves de manière ponctuelle ou sur une période récurrente à l’aide de cette fonctionnalité. Seuls les administrateurs peuvent définir des certifications pour les élèves.

En tant qu’administrateur, vous pouvez créer un programme de certification hébergé en interne ou dirigé par un tiers. En cas de certification interne, définissez les cours qu’un élève doit suivre pour obtenir sa certification. Publiez le programme, puis attribuez-le aux élèves.

## Création d’une certification {#createacertification}

1. Cliquez sur **[!UICONTROL Certification]** dans le volet de gauche.\
   Une page s’affiche avec une liste de tous les brouillons et l’état de publication des certifications.

1. Afficher les certifications dans différents modes :

   1. Cliquez sur **[!UICONTROL Brouillon]** pour afficher toutes les certifications qui sont à l&#39;état de brouillon. Vous devez terminer leur création.
   1. Cliquez sur **[!UICONTROL Publié]** pour afficher toutes les certifications que vous avez publiées.
   1. Cliquez sur **[!UICONTROL Tous]** pour afficher les certifications dans tous les états.
   1. Triez et affichez la liste des certifications par ordre croissant, décroissant ou selon la date à laquelle vous les avez mises à jour.

1. Cliquez sur **[!UICONTROL Ajouter]**.

   Une nouvelle page de certification s’affiche.

![](assets/add-new-certification.png)

*Afficher la page pour ajouter une certification*

1. Ajoutez le nom et la description du certificat.

<table>
 <tbody>
  <tr>
   <th>Champ</th>
   <th>Description</th>
  </tr>
  <tr>
   <td>Jours avant la fin</td>
   <td>Date limite de certification. Entrez une valeur numérique.</td>
  </tr>
  <tr>
   <td>Type</td>
   <td>
    <p>Type de certification :</p>
    <ul>
     <li><b>Récurrent</b>- Choisissez cette option si la certification doit avoir lieu après chaque année, deux ans ou trois ans.</li>
     <li><b>Perpétuel</b>- Choisissez cette option si la certification doit être une exigence unique.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Réaffectation</td>
   <td>Choisissez si vous souhaitez que le certificat soit réaffecté en fonction de la date d’achèvement ou de la date d’inscription.<br></td>
  </tr>
  <tr>
   <td>Validité (en mois) <br></td>
   <td>Spécifiez la durée de validité de la certification.</td>
  </tr>
  <tr>
   <td>Séquencement des cours<br></td>
   <td>Décidez si les élèves doivent suivre les cours de manière ordonnée ou non ordonnée.<br></td>
  </tr>
  <tr>
   <td>Désinscription<br></td>
   <td>Activez ou désactivez l’option permettant aux élèves de se désinscrire.</td>
  </tr>
  <tr>
   <td>Émetteur de la certification<br></td>
   <td>
    <p>Choisir <b>Interne</b> s’il appartient à votre organisation, ou choisissez <b>Externe</b> pour les certifications d’organisations externes.</p>
    <p>Lorsque vous choisissez <b>Certification externe</b>, vous voyez deux autres options...</p>
    <ul>
     <li>Identique à la date d’approbation<br></li>
     <li>Envoyé par l’élève<br></li>
    </ul>
    <p>Les élèves peuvent spécifier la date d'achèvement correcte pour les certifications externes. Dans les versions précédentes, la date d'achèvement était définie par défaut par Prime, en fonction de la date d'approbation du responsable. La date d’achèvement indiquée par l’élève doit être postérieure à la date de création du certificat<span>.</span></p></td>
  </tr>
  <tr>
   <td>Durée</td>
   <td>Si vous avez choisi Certification externe, spécifiez la durée en minutes.</td>
  </tr>
  <tr>
   <td>Balises</td>
   <td>Entrez les balises à associer au certificat. Les balises sont utiles pour rechercher le certificat.</td>
  </tr>
  <tr>
   <td>Sélectionner des catalogues<br></td>
   <td>Choisissez le catalogue dont le certificat fait partie.</td>
  </tr>
 </tbody>
</table>

Choisir les cours à ajouter à la certification à partir de **[!UICONTROL Cours]** > **[!UICONTROL Catalogue]** onglet.

Passez le curseur de la souris sur chaque vignette de cours, cliquez sur + pour les ajouter à la certification. Cliquez sur **[!UICONTROL Aperçu]** pour afficher le cours en tant qu’élève avant de l’ajouter.

1. Cliquez sur **[!UICONTROL Curriculum]** pour afficher/vérifier la liste des cours que vous avez ajoutés.
1. Cliquez sur **[!UICONTROL Publier]**.

## Mappage des instances de cours pour les certifications {#courseinstancemappingforcertifications}

Pour mapper le cours et l&#39;instance pour les certifications :

1. Cliquez sur Certifications dans le volet de gauche.
1. Dans la liste des certifications, sélectionnez Afficher la certification de la certification là où vous souhaitez mapper le cours et l’instance.
1. Dans le volet de gauche, cliquez sur Cours. Les cours de la certification s’affichent. Cliquez sur Modifier.
1. Passez le curseur de la souris sur le cours où vous souhaitez définir le mappage d&#39;instance, sélectionnez Mappage d&#39;instance de cours.
1. Dans la fenêtre contextuelle qui s’affiche, sélectionnez l’instance du cours à dispenser pour la certification que vous avez choisie.
1. Cliquez sur Enregistrer.

Un administrateur peut ajouter des cours de type salle de classe et salle de classe virtuelle à un programme d&#39;apprentissage. La session que l&#39;auteur a donnée lors de la création du cours devient l&#39;instance par défaut. Lorsqu&#39;un administrateur ajoute des cours à un programme d&#39;apprentissage, il est mappé par défaut à l&#39;instance par défaut de tous les cours, mais il peut modifier le mappage d&#39;instance. Le nombre de cours ajoutés à un programme d’apprentissage est également visible dans la page des instances, comme indiqué ci-dessous.

## Activer le contrôle de catalogue complet {#catalog}

Comme accorder la licence complète [contrôle de catalogue pour les apprentissages ou les modules](shared-catalog-full-control.md), vous pouvez également activer le contrôle de catalogue complet pour les certifications.

## Inscription ou désinscription d’élèves à la certification {#enrollorunenrolllearnerstothecertification}

Pour plus d&#39;informations sur l&#39;inscription des élèves et les étapes à suivre, voir [Inscription des élèves](courses.md#main-pars_header_1058138132).

## Désinscription pour les élèves {#unenrollmentforlearners}

Lors de la création des certifications, l’administrateur a la possibilité de sélectionner si les élèves peuvent se désinscrire de la certification. Si l’administrateur sélectionne l’option, l’élève peut se désinscrire.

![](assets/unenrollment.png)

*Choisir de désinscrire des élèves*

## Marquer comme terminé {#markcompletion}

Les administrateurs peuvent marquer une certification comme terminée à l’aide de l’option qui leur est disponible. Pour marquer l’achèvement d’une certification, procédez comme suit.

1. Ouvrir **[!UICONTROL Certification]** > **[!UICONTROL Élèves]**.

   La page Élèves s’ouvre avec la liste des élèves inscrits.

1. Sélectionnez un/plusieurs/tous les élèves pour marquer la certification comme terminée à l’aide de la case à cocher disponible pour chaque élève.
1. Cliquez sur  **[!UICONTROL Action]** > **[!UICONTROL Marquer comme terminé.]**

   Notez que si une certification comporte plusieurs cours, tous les cours seront marqués comme terminés.

## Cours obligatoires pour la certification externe {#mandatory}

Dans les versions antérieures de Learning Manager, l’achèvement du cours d’un élève en certification externe n’était pas obligatoire pour obtenir un certificat.

Vous pouvez désormais rendre les cours obligatoires en activant l’option **[!UICONTROL Définition des cours obligatoires comme étant obligatoires pour l’obtention de la certification]** dans l’onglet Curriculum lors de la modification de la certification.

## Modification d’une certification publiée {#editingapublishedcertification}

Une certification peut être modifiée par un administrateur à un état publié. À ce stade, l’administrateur peut modifier toutes les sections d’une certification et la republier.

Pour modifier une certification publiée, cliquez sur la carte de certification, puis sur **[!UICONTROL Modifier]** dans le coin supérieur droit de la page.

Lors de la modification des sections d’une certification, si vous devez quitter la page, vous devez republier la certification. Une boîte de dialogue de confirmation vous demande de publier à nouveau la certification.

## Abonnement {#subscription}

Un administrateur peut récupérer le score du quiz et les rapports d’état des élèves. Ils peuvent définir la fréquence du rapport, l’objet de l’e-mail et l’ID d’e-mail des destinataires. Selon la fréquence définie, le destinataire reçoit un e-mail avec le rapport joint.

![](assets/report-subscription.jpeg)

*Définition de la fréquence des rapports et d’autres propriétés*
