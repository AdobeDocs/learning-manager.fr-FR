---
jcr-language: en_us
title: Forum aux questions pour les administrateurs
description: Forum aux questions pour les administrateurs Adobe Learning Manager
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 55%

---



# Forum aux questions pour les administrateurs

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Découvrez les questions fréquentes sur Learning Manager concernant le rôle d'administrateur. </p></td>
  </tr>
 </tbody>
</table>

+++ Puis-je ajouter des utilisateurs en bloc ? Comment ?

Oui, vous pouvez ajouter plusieurs utilisateurs simultanément à l’aide de la fonction de téléchargement CSV. Cliquez sur  [ici](/help/migrated/administrators/add-users-in-bulk.md) pour plus d’informations.

+++

+++J’ai mal saisi l’ID de messagerie lors de la création de la connexion de mes élèves, comment puis-je le corriger ?

Pour corriger les identifiants de connexion utilisateur, vous devez importer un fichier CSV dans Learning Manager. Un exemple de fichier CSV est joint au bas de cette page pour référence. Étant donné que l’adresse est considérée comme un identifiant unique pour une personne, elle ne peut plus être modifiée. Procédez comme suit :

1. Ajoutez le même utilisateur avec l’ID d’e-mail correct dans le fichier CSV et assurez-vous qu’il reste en tant que responsable des autres utilisateurs en ajoutant son ID d’e-mail à la colonne « Adresse électronique du responsable de l’employé » dans l’exemple de fichier CSV.
1. Ajoutez d’autres utilisateurs dans votre compte au fichier CSV, y compris vous-même.
1. Importez ce fichier sur l’application Administrateur Learning Manager -> Utilisateurs -> Ajouter -> Importer un fichier CSV
1. Lorsque vous y êtes invité dans la boîte de dialogue, mappez tous les champs avec les colonnes correspondantes au format CSV.
1. Cliquez sur Enregistrer.

Les utilisateurs doivent être ajoutés sur la page Élèves.

[Exemple de fichier CSV.csv Learning Manager](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Comment configurer les alertes ?

Dans Adobe Learning Manager version 1.0, vous pouvez créer des notifications. Refer  [question sur les notifications](/help/migrated/administrators/feature-summary/user-notifications.md) pour plus d’informations.

+++

+++Comment ajouter des certificats pour les cours ?

Adobe Learning Manager ne fournit pas de certificats pour les cours. Cependant, l&#39;administrateur peut créer des badges pour chaque cours en cliquant sur l&#39;onglet Badges dans le panneau de gauche. Lorsqu’un administrateur inscrit des élèves à un cours, il peut également associer un badge.

+++

+++Comment importer des signatures pour les certificats ?

Dans Adobe Learning Manager, il n’existe aucune fonction pour importer des signatures pour la certification ou le badge.

+++

+++Puis-je configurer un calendrier pour les cours ? Comment ?

Dans la version 1.0 d’Adobe Learning Manager, nous n’avons pas prévu la possibilité de configurer un calendrier pour les cours.

+++

+++Comment inscrire directement les élèves inscrits sur liste d’attente ?

Pour tout cours en salle de classe, lorsque les places sont limitées, les élèves sont mis en liste d’attente dans leur ordre d’inscription. Pour tous les cours en salle de classe, les administrateurs peuvent sélectionner des élèves en liste d’attente et attribuer des places indépendamment du nombre limite de places. Les élèves sont inscrits au cours dès l’attribution de la place par l’administrateur.

1. Cliquez sur Cours dans le volet de gauche après avoir ouvert une session en tant qu’administrateur.
1. Dans la liste des cours disponibles, cliquez sur le nom d’un cours en salle de classe de votre choix. Une nouvelle page apparaît avec des informations détaillées sur le cours.
1. Cliquez sur Liste d’attente dans le volet de gauche de la page des détails du cours. Une liste de tous les élèves en liste d’attente s’affiche sur la page.
1. Sélectionnez les élèves, puis cliquez sur l’option Attribuer des places pour inscrire les élèves directement aux cours, indépendamment du nombre limite de places.

Pour plus d’informations, voir  [liste d’attente et assiduité](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) fonctionnalité.

+++

+++Comment enregistrer l’assiduité pour les élèves du module de salle de classe ?

Oui, vous pouvez enregistrer l’assiduité en suivant les étapes ci-dessous :

1. Cliquez sur Cours dans le volet de gauche après avoir ouvert une session en tant qu’administrateur.
1. Dans la liste des cours disponibles, cliquez sur le nom du cours à partir de n’importe quel module de salle de classe/cours de votre choix. Une nouvelle page apparaît avec des informations détaillées sur le cours.
1. Sélectionnez les stagiaires, puis cliquez sur Enregistrer pour enregistrer la fin du cours.

S’il existe plusieurs modules dans un cours et que l’élève a terminé uniquement l’un d’entre eux, vous pouvez sélectionner un seul module et cliquez sur Enregistrer pour marquer la réalisation pour cet élève. Si l’élève a terminé tous les modules d’un cours, vous pouvez cliquer sur l’option Tout sélectionner, puis cliquer sur Enregistrer.

Pour plus d’informations, voir  [liste d’attente et assiduité](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) fonctionnalité.

+++

+++Comment puis-je inclure l’option Retour d’informations L3 ?

Vous pouvez ajouter Retour d’informations L3 lorsque vous inscrivez des élèves aux cours. Pour ajouter une question au retour d’informations L3, procédez comme suit :

1. Cliquez sur Cours dans le volet de gauche après vous être connecté en tant qu’administrateur. Les listes de tous les cours s&#39;affichent sur la page de droite.
1. Cliquez sur la vignette du cours pour lequel vous souhaitez ajouter un retour d&#39;informations L3
1. Cliquez sur la valeur d’instance par défaut dans le volet de gauche.
1. Cliquez sur le cercle du bouton bascule en regard de L3 - Retour d’informations sur le changement de comportement pour le sélectionner.
1. Ajoutez une question de retour d’informations L3 dans la zone de texte située sous la question L3.

+++

+++Comment puis-je rechercher la nomination du responsable pour un cours nommé par le responsable ?

En tant qu’administrateur, vous pouvez rechercher la nomination du responsable pour les cours en suivant les étapes ci-dessous :

1. Cliquez sur Cours dans le volet de gauche.
1. Placez le curseur de la souris sur un cours nommé par le responsable et cliquez sur **[!UICONTROL Rechercher la nomination du responsable]**.

1. Dans la liste des occurrences, cliquez sur **[!UICONTROL Responsables désignés]** lien suivi de **[!UICONTROL Ajouter des responsables]** lien.

1. Ajoutez le nom du responsable, le nombre de places attribué et cliquez sur la coche pour enregistrer les modifications.

Lors de la création des cours, l’auteur choisit le type de cours en tant que Nommé par le responsable.

+++

+++Comment puis-je inscrire un élève à un cours particulier ?

Suivez les étapes ci-dessous pour inscrire des élèves à des cours :

1. Cliquez sur Cours dans le volet de gauche après vous être connecté en tant qu’administrateur. La liste de tous les cours s&#39;affiche sur la page de droite.
1. Choisissez le cours auquel vous souhaitez ajouter des élèves, puis placez le pointeur de la souris au-dessus.
1. Cliquez sur Inscrire des élèves et ajoutez le nom des élèves. **Remarque :** Vous pouvez ajouter un ou plusieurs élèves à la fois.

+++

+++Comment affecter des élèves à une compétence particulière ?

Affectez des élèves à des compétences en suivant les étapes ci-dessous :

1. Cliquez sur **[!UICONTROL Compétences]** dans le volet de gauche après vous être connecté en tant qu’administrateur.
1. Sélectionnez une ou plusieurs compétences en cochant les cases en regard de chaque compétence, puis cliquez sur **[!UICONTROL Actions]** dans le coin supérieur droit de la page.
1. Cliquez sur Affecter à des utilisateurs.
1. Commencez à saisir le nom de l’utilisateur, faites votre choix dans la liste déroulante et cliquez sur **[!UICONTROL Enregistrer]**.

   >[!NOTE]
   >
   >Vous pouvez inscrire plusieurs élèves pour des compétences en cliquant sur Ajouter plus d’utilisateurs et en répétant la 4e étape.

+++

+++Comment créer une session de programme d’apprentissage ?

Pour créer un programme d’apprentissage, suivez les étapes ci-dessous :

1. Cliquez sur Programme d’apprentissage dans le volet de gauche. La page Programmes d’apprentissage s’affiche avec une liste des programmes d’apprentissage existants.
1. Cliquez sur Ajouter dans l’angle supérieur droit de la page.\
   Saisissez le nom du programme, la présentation, la description et cliquez sur Enregistrer.
1. Cliquez sur Cours dans le volet de gauche.
1. Ajoutez un ou plusieurs cours en cliquant sur + sur chaque vignette de cours.

   >[!NOTE]
   >
   >Vous devez publier le programme d’apprentissage avant d’inscrire des élèves ou une instance.

1. Cliquez sur Instances dans le volet de gauche, puis cliquez sur **[!UICONTROL Ajouter de nouvelles instances]** dans le coin droit de la page pour inclure les détails de l&#39;instance.

Pour plus d’informations sur les programmes d’apprentissage, voir  [Fonctionnalité Programmes d’apprentissage.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Comment modifier ou personnaliser les rapports pour tous les rôles ?

Cliquez sur la flèche déroulante dans l’angle supérieur droit de chaque rapport pour modifier des rapports. Cliquez sur Enregistrer après avoir effectué les modifications et affichez le rapport modifié.

+++

+++Comment modifier les cours, les programmes d’apprentissage et le profil de l’entreprise ?

Vous pouvez modifier des cours ou des programmes d’apprentissage, même une fois que vous les avez publiés. Pour plus d’informations, voir  [Cours](/help/migrated/administrators/feature-summary/courses.md) et  [programmes d’apprentissage](/help/migrated/administrators/feature-summary/learning-programs.md) Contenu de l’aide.

Pour modifier le profil de la société, cliquez sur **[!UICONTROL Paramètres]** dans le volet de gauche et cliquez sur **[!UICONTROL Modifier]** dans le coin supérieur droit de la page.

+++

+++Comment puis-je rechercher les cours ?

Cliquez sur Cours dans le volet de gauche après avoir ouvert une session en tant qu’administrateur. Une liste de tous les cours disponibles s’affiche.

Vous pouvez rechercher vos cours de deux manières :

1. Cliquez sur l’icône Rechercher affichée dans l’angle supérieur droit. Un champ de recherche s’affiche. Saisissez le nom du cours ou n’importe quel mot-clé associé à votre cours pour le localiser.
1. En filtrant la liste des cours à l’aide des filtres.

Vous pouvez filtrer les cours par état (Tous, Publié et Retiré) en cliquant sur chacune de ces options. Vous pouvez également effectuer une recherche en fonction des compétences en cliquant sur Compétences et en sélectionnant chacune d&#39;elles.

En fonction de votre choix, vous pouvez afficher la liste de cours filtrée et sélectionner les cours requis.

+++

+++Puis-je modifier les thèmes de l’application ? Comment ?

Oui, vous pouvez modifier les thèmes et l’identité visuelle de l’application Learning Manager selon les besoins de votre organisation. Un ensemble de cinq images représentatives vous donne un aperçu de vos modifications de thèmes chromatiques avant de les appliquer à votre application. Consultez ces images en cliquant sur les symboles &lt; et > à gauche et à droite des images à prévisualiser.

Cliquez sur **[!UICONTROL Branding]** dans le volet de gauche, pour mettre à jour le nom de votre organisation, modifiez le sous-domaine, les styles et les thèmes du journal. Cliquez sur **[!UICONTROL Modifier]** adjacentes à chacune de ces rubriques pour modifier le contenu.

Reportez-vous à  [Aide sur les thèmes de couleur et l’image de marque](/help/migrated/administrators/feature-summary/themes.md) pour plus d’informations.

+++

+++Comment configurer les badges pour les cours ?

1. Cliquez sur Badges dans le volet de gauche après vous être connecté en tant qu’administrateur.
1. Cliquez sur Ajouter dans le coin supérieur droit de la page qui s’affiche.
1. Ajoutez un nom de badge.
1. Téléchargez le badge en cliquant sur Charger un badge et cliquez sur Enregistrer.

+++

+++Comment puis-je configurer des points de ludification pour les cours ?

Vous pouvez configurer les points de ludification pour les participants en suivant les étapes ci-dessous :

1. Cliquez sur Ludification après vous être connecté en tant qu’administrateur. Une page s’affiche contenant une liste de niveaux Bronze, Argent, Or et Platine et les points requis à obtenir correspondant à chaque niveau. La liste des tâches et les points correspondants sont disponibles.
1. Cliquez sur l’icône Modifier en regard de chaque tâche pour configurer ou modifier les points.

Refer  [Fonction de ludification](/help/migrated/administrators/feature-summary/gamification.md) pour plus d’informations.

+++

+++Comment créer des rapports pour les responsables et les élèves ?

Vous pouvez créer des rapports en suivant les étapes ci-dessous :

1. Cliquez sur Rapports dans le volet de gauche. La page Synthèse des rapports s’affiche.
1. Sur la page Rapports, cliquez sur **[!UICONTROL Ajouter]** dans le coin supérieur droit.

   **[!UICONTROL Ajouter un rapport]** s’affiche.

1. Renseignez tous les champs obligatoires, puis cliquez sur Enregistrer.

Seuls les administrateurs et les responsables peuvent créer ou afficher des rapports. Reportez-vous à [fonctionnalité Rapports](/help/migrated/administrators/feature-summary/reports.md) pour plus d’informations.

+++

+++Comment passer aux rôles d’élève, de responsable et d’auteur ?

Vous pouvez passer votre connexion de compte à d’autres rôles tels qu’Élève, Responsable et Auteur sans quitter la session de votre compte.

1. Cliquez sur la flèche déroulante en regard de votre photo de profil dans l’angle supérieur droit de la page.\
   Un menu contextuel s’affiche.
1. Sélectionnez chaque rôle disponible pour avoir accès aux comptes de rôle respectifs.

+++

+++Comment inclure des notifications pour les utilisateurs ?

Les responsables, les auteurs et les élèves peuvent voir les notifications en fonction des activités de cours. L’administrateur peut activer ou désactiver les notifications pour tous les utilisateurs en suivant les étapes ci-dessous :

1. Cliquez sur Modèles de courrier électronique dans le volet de gauche et sélectionnez Général, Inscriptions des utilisateurs, Terminaisons et Commentaires.
1. Parmi les événements répertoriés ci-dessous, cliquez sur les boutons bascule Non/Oui en regard de **chaque **événement et choisissez Oui pour activer la notification. Cliquez sur Non pour désactiver l’envoi de notifications pour un événement particulier.

+++

+++Comment puis-je autoriser l’inscription externe pour les cours ?

Adobe Learning Manager vous donne la possibilité d’inscrire des membres de services externes ou des collaborateurs externes à votre organisation dans l’application.

1. Cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de gauche.
1. Cliquez sur **[!UICONTROL Externe]** dans le volet de gauche.
1. Cliquez sur **[!UICONTROL Ajouter]** dans le coin supérieur droit de la page.

   La boîte de dialogue Ajouter un utilisateur s’affiche.

1. Ajoutez le nom du profil, l’adresse électronique du responsable, le nombre de places attribuées et les informations sur l’expiration. Vous pouvez également ajouter une image au profil externe.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

L’administrateur peut copier l’URL d’enregistrement et l’envoyer au groupe d’inscriptions externes. Les utilisateurs externes peuvent s’enregistrer, se connecter à l’application Learning Manager et accéder à leurs cours.

+++

+++Comment ajouter un questionnaire pour le retour d’informations L1 ?

Créez un questionnaire de retour d’informations qui peut être utilisé par les élèves une fois les cours terminés. Trois exemples de questions sont disponibles par défaut. Suivez les étapes ci-dessous pour créer le questionnaire.

1. Cliquez sur Retour d’informations dans le volet de gauche. Une fenêtre de questionnaire de retour d’informations s’affiche.
1. Cliquez sur **[!UICONTROL Modifier]** pour ajouter/modifier le questionnaire.

Vous pouvez ajouter un jeu de questions et choisir de ne pas les afficher si vous n’en avez pas besoin. Cliquez sur la case à cocher pour activer/désactiver une question particulière.

+++

+++Comment configurer les compétences et les niveaux ?

1. Cliquez sur Compétences dans le volet gauche de la fenêtre Administrateur.
1. Cliquez sur Ajouter pour ajouter de nouvelles compétences.
1. Ajoutez le nom de la compétence, une description et les crédits correspondants pour chaque niveau.

   Par défaut, un seul niveau avec 0 (zéro) crédit sera disponible pour chaque compétence.

1. Cliquez sur [!UICONTROL **Ajouter un niveau**] pour ajouter un nouveau niveau à chaque compétence et cliquez sur Enregistrer. Vous pouvez ajouter jusqu’à 5 niveaux.

Une fois la compétence enregistrée, vous ne pouvez plus supprimer les niveaux d’une compétence. L’administrateur peut également affecter des élèves à une compétence et un niveau spécifiques.

+++

+++Comment configurer le système de facturation pour les cours de mon organisation ?

1. Cliquez sur [!UICONTROL **Facturation**] dans le volet de gauche.

   Les informations de facturation s’affichent sur la page.

1. Cliquez sur le bouton [!UICONTROL **S’abonner**] onglet.
1. Saisissez le nombre de packs que vous souhaitez commander dans le champ Packs, et cliquez sur Passer une commande dans l’angle supérieur droit de la page.

   Choisissez le nombre de packs en fonction du nombre d’élèves dans votre organisation et passez votre commande. Dans le cas d’un processus piloté par bon de commande, écrivez-nous à l’adresse  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Entrez vos coordonnées, sélectionnez le type de carte de crédit, saisissez les détails de votre carte de crédit et cliquez sur le bouton Terminer ma commande.

Refer [Gestion de la facturation](/help/migrated/administrators/feature-summary/billing-management.md) pour plus d’informations.

+++

+++ Puis-je personnaliser la conception du certificat ? Comment ?

Dans Adobe Learning Manager, vous pouvez reconnaître les élèves en émettant des badges. Reportez-vous à la section Fonctionnalité Badges pour plus d’informations.  Reportez-vous également à la fonctionnalité Certification.

+++

+++Comment configurer le profil de mon entreprise ?

1. Après vous être connecté en tant qu’administrateur, cliquez sur **[!UICONTROL Informations sur la société]** dans le volet de gauche.
1. Ajoutez le profil de la société, le sous-domaine, le logo en cliquant sur chacune de ces options dans la page.

+++

+++Comment ajouter des cours ?

Pour ajouter des cours, vous devez basculer votre rôle sur Auteur. Vous pouvez uniquement afficher la liste des cours disponibles en fonction de leur état en tant que **[!UICONTROL Terminé]**, **[!UICONTROL Publié]**, et **[!UICONTROL Retraité]**.

Pour afficher les cours, cliquez sur **[!UICONTROL Cours]** dans le volet de gauche. Refer  [Création de cours](/help/migrated/administrators/feature-summary/courses.md)pour plus d’informations

+++

+++Comment ajouter différents rôles à l’application ?

Pour ajouter des utilisateurs, suivez les étapes ci-dessous :

1. Cliquez sur Utilisateurs dans le volet de gauche après vous être connecté en tant qu’administrateur. Vous pouvez également ajouter des utilisateurs en cliquant sur Prise en main dans le volet de gauche de la fenêtre, puis en cliquant sur Ajouter des utilisateurs.
1. Pour ajouter de nouveaux utilisateurs, cliquez sur Ajouter dans l’angle supérieur droit de la page.

Par défaut, tous les nouveaux utilisateurs ont un rôle d’élève. Vous pouvez attribuer des rôles d’administrateur ou d’auteur aux élèves en cliquant sur **[!UICONTROL Actions]** dans le coin supérieur droit de la page et en choisissant **[!UICONTROL Attribuer un rôle]** > **[!UICONTROL Créer un auteur]** ou **[!UICONTROL Rendre administrateur]**.

Refer  [Ajouter de nouveaux utilisateurs](/help/migrated/administrators/feature-summary/add-users-user-groups.md) pour obtenir des informations détaillées sur l’ajout d’élèves, d’auteurs et d’administrateurs.

+++

+++Comment modifier une image d’arrière-plan pour un élève ?

Contactez l’équipe d’assistance Learning Manager.

+++

+++Où puis-je trouver mon ID de compte Learning Manager ?

Vous pouvez obtenir l’ID de compte à partir du navigateur dans lequel Learning Manager est ouvert.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++
