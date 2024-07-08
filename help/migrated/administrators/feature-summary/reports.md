---
description: Découvrez les rapports liés au rôle d’administrateur dans l’application Learning Manager.
jcr-language: en_us
title: Rapports
contentowner: manochan
exl-id: 31b176b7-4b8f-4851-a0c5-4eee58bceb41
source-git-commit: 7be69e68f3b8970e090c8eccd25771cd2e5e99f1
workflow-type: tm+mt
source-wordcount: '7132'
ht-degree: 57%

---

# Rapports

Découvrez les rapports liés au rôle d’administrateur dans l’application Learning Manager.

Adobe Learning Manager vous permet de créer différents rapports pour suivre, surveiller et contrôler les activités des élèves. Les activités des élèves font l’objet d’un suivi et sont capturées automatiquement dans la base de données. Les rapports Responsable et Administrateur sont générés à partir de la base de données.

## Vue d’ensemble {#overview}

Le processus de génération des rapports est similaire pour Administrateur et pour Responsable. Les responsables peuvent afficher les rapports correspondant à leurs subordonnés tandis que les administrateurs peuvent afficher tous les rapports à l’échelle de l’entreprise.

Les rapports sont regroupés dans un tableau de bord. Un rapport se trouve toujours dans un tableau de bord. Un **[!UICONTROL tableau de bord]** par défaut existe par défaut dans la page des rapports. Tout rapport supplémentaire de votre part entre dans ce tableau de bord par défaut. Pour ajouter des rapports à des tableaux de bord individuels, utilisez la flèche déroulante et choisissez **[!UICONTROL Ajouter un rapport]**. Pour plus d’informations sur la création des tableaux de bord, consultez la section Tableaux de bord sur cette page.

## Types de rapports {#typesofreports}

Adobe Learning Manager prend en charge les quatre principaux types de rapports tels que Accomplissement, Temps passé, Compétences et Efficacité. Vous pouvez utiliser les types de rapports suivants pour générer des rapports de 300+ variations :

* Statistiques de fourniture des cours aux élèves
* Rapport sur l’efficacité des cours
* Rapport basé sur les compétences de l’élève
* Statistiques d’inscription aux programmes d’apprentissage des élèves
* Temps d’apprentissage des élèves
* Nombre d’élèves
* Fin de certification

## Tableaux de bord Activités des utilisateurs {#useractivitydashboards}

Consultez un résumé de toutes les activités utilisateur sur la plate-forme au fil du temps. Configurez les groupes d’utilisateurs et appliquez des filtres.

Le tableau de bord d’activité des utilisateurs affiche l’activité des utilisateurs dans le compte. Les trois rapports répertoriés sont les suivants :

* **Utilisateurs enregistrés :** Ce rapport fournit des informations sur le nombre d’utilisateurs enregistrés dans votre compte semaine après semaine. Pour les comptes disposant d’une licence Unités mensuelles actives, le rapport affiche les unités MAU à la place.

* **Rapport Visites d’utilisateurs :** Ce rapport fournit des informations sur le nombre d’utilisateurs accédant à la plateforme au quotidien. Un rapport mensuel est également disponible.

* **Rapport Temps d’apprentissage passé :** ce rapport fournit des informations sur le temps d’apprentissage passé sur la plateforme au jour le jour. Un rapport mensuel est également disponible.

### Utilisateurs enregistrés {#registeredusers}

Learning Manager consigne le nombre d’utilisateurs enregistrés dans le système chaque semaine. Les administrateurs peuvent consulter ce rapport pour connaître le nombre d’utilisateurs enregistrés ce jour de la semaine. Une fois consigné pour une semaine, le nombre d’utilisateurs enregistrés ne change pas. Par conséquent, le nombre d’utilisateurs enregistrés historiques n’est pas lié à l’ensemble actuel d’élèves dans le système.

Ce rapport fournit des informations sur le nombre d’utilisateurs enregistrés dans votre compte chaque semaine.

Pour les comptes disposant d’une licence Unités mensuelles actives, le rapport affiche les unités MAU à la place.

![](assets/registered-usersreport.png)
*Rapport Utilisateurs enregistrés*

***Pour les comptes Unités avec accès mensuel :***

**Rapport sur les utilisateurs actifs mensuels**

Ce rapport indique le nombre d’élèves actifs chaque mois dans la plate-forme d’apprentissage. L’utilisateur est considéré comme actif pour le mois s’il exécute l’une des actions d’apprentissage mentionnées ici. Il en va de même pour le décompte des unités actives mensuelles.

Une fois comptabilisé et consigné pour un mois, le nombre d’utilisateurs actifs mensuels ne change pas. Par conséquent, le nombre d’utilisateurs historiques affichés n’est pas lié à l’ensemble actuel d’élèves dans le système.

### Visites d’utilisateurs {#uservisits}

Ce rapport affiche le nombre total d’élèves accédant au système au cours d’une période de jour ou de mois. Parcourir la plate-forme d’apprentissage sans suivre de cours signifie quand même « accéder » à la plate-forme d’apprentissage. Cela permet à l’administrateur de connaître le nombre total d’utilisateurs accédant au système. Le premier jour du mois, Learning Manager crée un enregistrement du nombre total d’utilisateurs accédant à la plate-forme au cours du mois précédent. Il capture également des informations sur le groupe d’utilisateurs de ces utilisateurs.

Seuls les groupes d’utilisateurs configurés par l’administrateur sont enregistrés. Cela permet aux administrateurs d’appliquer également un filtre sur les groupes d’utilisateurs pour les données mensuelles historiques. Notez que si la configuration des groupes d’utilisateurs est modifiée et que Learning Manager n’a pas enregistré de données pour ce groupe d’utilisateurs au cours des mois précédents, Learning Manager ne peut pas afficher les données de ce groupe d’utilisateurs nouvellement configuré pour les mois précédents.

Ce rapport répertorie les utilisateurs qui accèdent à la plate-forme avec tous les formats tels que le Web, l’application mobile, les solutions personnalisées sans interface utilisateur, etc. Le graphique d’utilisation de l’application de l’appareil mentionne spécifiquement uniquement les utilisateurs accédant à la plate-forme à l’aide de l’application de l’appareil Learning Manager. Cela permet aux administrateurs d’identifier l’utilisation de l’application mobile dans leur compte.

![](assets/user-visit-report.png)
*Rapport Visite utilisateur*

### Rapport sur le temps d’apprentissage {#learningtimespentreport}

Ici, vous pouvez voir des diagrammes hiérarchiques à deux axes qui affichent le temps d’apprentissage total passé par tous les élèves sur une période de 12 mois. Le deuxième axe représente le temps médian consacré à l’apprentissage d’un élève.

Le temps passé pour différents objets d’apprentissage, notamment les programmes d’apprentissage et les certifications, est calculé pour les éléments suivants :

* Cours en auto-apprentissage avec contenu statique et interactif
* Cours d’activité avec URL.
* Sessions de fin de semaine avec l’indicateur de fin de semaine activé.
* Session de connexion VC où la présence est automatiquement marquée.
* Le temps passé pour différents objets d’apprentissage, notamment les programmes d’apprentissage et les certifications
* Instructions xAPI pour un cours d’activité xAPI.

Vous pouvez exporter le graphique sous la forme d’une feuille de calcul Excel.

Un filtre permettant de choisir la configuration du groupe d’utilisateurs est fourni, permettant de visualiser les données selon différents groupes d’utilisateurs.

Le filtre de date et de groupe d’utilisateurs sélectionné est appliqué à tous les graphiques pertinents du tableau de bord.

>[!NOTE]
>
>Pour les rapports **[!UICONTROL Visites d&#39;utilisateurs]** et **[!UICONTROL Temps d&#39;apprentissage]**, les données par défaut affichées (lorsqu&#39;aucun groupe d&#39;utilisateurs n&#39;est configuré) s&#39;appliqueront à l&#39;ensemble du compte.

## Tableau de bord de contenu de formation {#trainingcontentdashboard}

Le tableau de bord de contenu de formation fournit des informations sur les formations disponibles sur la plate-forme. Vous pouvez consulter les formations très demandées ou suivre toutes les formations disponibles.

### Rapport des formations {#trainingsreport}

Ce rapport fournit des informations sur le nombre total de formations disponibles sur la plate-forme (à l’état publié) au cours d’un mois. Il donne une indication du nombre de formations proposées au fil du temps.

![](assets/training-report.png)
*Rapport d’entraînement*

### Rapport des formations actives {#activetrainingsreport}

Ce rapport fournit des informations sur les formations actives sur la période sélectionnée. Les formations actives sont des formations qui sont inscrites, affichées dans le lecteur ou terminées à cet instant.

Pour les formations actives, les données de tous les groupes internes de l’utilisateur racine (avec rôle de responsable) seront disponibles pour la sélection lorsqu’aucune configuration de groupe d’utilisateurs n’est effectuée. Outre les groupes d’utilisateurs racine, vous pouvez configurer 10 autres groupes d’utilisateurs si nécessaire.

![](assets/active-trainingsreport.png)
*Rapport Formations actives*

>[!NOTE]
>
>Les données ne s’affichent pas comme prévu lorsque **[!UICONTROL les filtres Tous les utilisateurs]** et **[!UICONTROL 12 mois]** sont sélectionnés, mais les données s’affichent lorsque vous sélectionnez **[!UICONTROL Tous les groupes] d’utilisateurs internes.**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Référence</b></p></td>
   <td>
    <p><b>Mesure</b></p></td>
   <td>
    <p><b>Description</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Taux au début (%)</p></td>
   <td>
    <p>Rapport entre le nombre d’élèves ayant commencé le cours et le nombre d’inscriptions.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Taux d’achèvement (%)</p></td>
   <td>
    <p>Rapport entre le nombre total d’utilisateurs ayant suivi le cours et le nombre total d’utilisateurs ayant commencé le cours.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Retour d’informations de l’élève</p></td>
   <td>
    <p>Moyenne de toutes les réponses des retours d’informations L1 reçues, sur une échelle de 1 à 10, arrondie à l'entier le plus proche.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Retour d’informations du responsable</p></td>
   <td>
    <p>Moyenne de toutes les réponses des retours d’informations L3 reçues, sur une échelle de 1 à 5, arrondie à l'entier le plus proche.<br></p></td>
  </tr>
 </tbody>
</table>

Le rapport de formation comporte deux colonnes supplémentaires :

1. Nombre moyen d’étoiles d’un cours.
1. Nombre d’apprenants qui ont évalué le cours.
1. Chemin incorporé
1. ID du parcours intégré
1. ID de cours incorporé

>[!NOTE]
>
>Les filtres appliqués n’affectent pas le taux au début, le taux d’achèvement, le retour d’informations de l’élève et le retour d’informations du responsable. Les filtres affectent uniquement l’inscription, les vues et les achèvements.

>[!NOTE]
>
>Pour les deux rapports (Contenu de formation, Activité de l&#39;utilisateur), vous pouvez configurer un maximum de 10 groupes d’utilisateurs. Le traitement et la mise à disposition des filtres nouvellement configurés peuvent prendre jusqu’à 24 heures.

## Tableaux de bord récapitulatifs des apprentissages {#dashboards}

### Générer les rapports de tableau de bord

>[!INFO]
>
>Dans cette formation, vous apprendrez à générer des rapports de tableau de bord à partir de la base de données.<br><br>[![bouton](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R3B5NPDN&amp;mv=display&amp;mv2=display#/course/8318854)</br></br>


Si vous ne parvenez pas à lancer la formation, écrivez à <almacademy@adobe.com>.

Consultez un rapport récapitulatif de toutes les activités d’apprentissage de la plateforme. Sur cette page, vous pouvez voir les informations récapitulatives suivantes pour l’équipe et les profils externes de l’utilisateur racine sélectionné. Une période peut également être sélectionnée :

* Résumé de l’apprentissage sous forme d’inscriptions, de vues et d’achèvements
* Principales compétences
* Résumé de la conformité

![](assets/summary-charts.png)
*Graphiques synthétiques*

S’il existe des gestionnaires internes au niveau racine, ils seront affichés les uns après les autres.

Tous les profils externes seront répertoriés après les profils internes (utilisateurs internes de niveau racine).

Si un profil externe a un gestionnaire, la hiérarchie du gestionnaire sera affichée dans la liste déroulante Afficher les **[!UICONTROL données pour]** . L’utilisateur sera répertorié dans la hiérarchie du gestionnaire dans toutes les pages de détails (résumé de l’apprentissage, conformité et état des compétences)

Si ce n’est pas le cas, tous les détails individuels de l’utilisateur seront affichés dans la liste.

Pour afficher des détails plus granulaires sur les inscriptions des différentes équipes internes, cliquez sur **[!UICONTROL Détails]** du résumé de formation.

![](assets/learning-sunnarydetails.png)
*Détails du résumé de formation*

Lorsque vous cliquez sur une inscription, vous pouvez voir les élèves pour chaque responsable et l’inscription à laquelle les objets d’apprentissage. Vous pouvez également voir les détails de progression et d’achèvement de chaque apprenant.

![](assets/learners-for-a-manager.png)
*Apprenants affectés à un responsable*

Cliquez sur une équipe et exportez son rapport sous la forme d’un fichier .csv. Un administrateur peut exporter le rapport pour n’importe quel groupe d’utilisateurs ou utilisateur individuel en sélectionnant le groupe d’utilisateurs ou l’utilisateur individuel, puis exporter des détails à partir de la **[!UICONTROL liste déroulante Action]** .

En outre, vous pouvez voir une vue de graphique à barres des compétences en cours et qui ont été atteintes. Vous pouvez ajouter/supprimer des compétences que vous souhaitez afficher dans le graphique.

![](assets/skill-status-stackedbarchart.png)
*Graphique à barres empilées État des compétences*

### Tableau de bord Conformité

**Adobe Learning Manager** offre un tableau de bord de conformité à tous les administrateurs et gestionnaires. Les administrateurs peuvent créer un tableau de bord de conformité et le partager avec les responsables. Les gestionnaires pourront afficher le tableau de bord nouvellement partagé sur leur application et pourront facilement suivre la conformité des membres de leur équipe pour une formation particulière. Le tableau de bord de conformité permet aux administrateurs de classer les cours de conformité personnalisés dans des catégories spécifiques (par exemple, ventes, marketing et juridique). Les catégories de conformité personnalisées sont optimisées par **[!UICONTROL des étiquettes]** de catalogue.

![](assets/compliance-dashboard-admin.png)

_Tableau de bord de conformité – Vue Administrateur_

Les administrateurs peuvent également vérifier l’état de conformité de l’équipe de chaque responsable en sélectionnant **[!UICONTROL Accéder au tableau de bord]** de conformité. Les administrateurs peuvent partager un ensemble de formations avec les responsables individuellement ou en groupe. Cela aide les gestionnaires à suivre facilement la conformité de leurs coéquipiers pour la formation spécifiée.

#### Processus d’administration

##### Création d’étiquettes de conformité personnalisées

Une étiquette de conformité est un type d’étiquette de catalogue qui classe les cours/cursus d’apprentissage/certifications comme type de conformité.
Pour créer une étiquette de conformité personnalisée, procédez comme suit :

1. Dans l’application Administrateur, accédez à **[!UICONTROL Paramètres]** > **[!UICONTROL Général]**.
1. Sélectionnez **[!UICONTROL l’option Type de conformité]** personnalisée pour activer l’étiquette de conformité personnalisée.


   ![](assets/custom-compliance.png)
   _Activer la conformité personnalisée_

   >[!NOTE]
   >
   >Cette nouvelle étiquette de catalogue a été introduite pour classer les cours, les parcours d’apprentissage et les certifications en tant que type de conformité. Pour activer l’option **[!UICONTROL Type de conformité]** personnalisée, vous devez d’abord activer l’option Afficher l’étiquette **** du catalogue sur la même page.

1. Accédez à **[!UICONTROL Paramètres]** > **[!UICONTROL Étiquette]** du catalogue et sélectionnez le type ]**de**[!UICONTROL  conformité.
1. Saisissez les valeurs (par exemple, Juridique, Ventes) dans la zone de **[!UICONTROL texte Valeur]** et sélectionnez **[!UICONTROL Ajouter une valeur]**.

   ![](assets/custom-compliance-values.png)
   _Ajouter des valeurs pour Conformité personnalisée_

1. Sélectionnez **[!UICONTROL Enregistrer]**.

>[!NOTE]
>
>L’auteur doit ajouter ces étiquettes de conformité lors de la création/modification des cours dans son application. Voir [Ajouter des étiquettes de conformité à un cours/cursus de formation/certification](/help/migrated/authors/feature-summary/courses.md#add-compliance-labels-to-courselearning-pathcertification).

##### Création et partage d’un tableau de bord de conformité

Pour créer et partager un tableau de bord de conformité, procédez comme suit :

1. Accédez à **[!UICONTROL Rapports]** > **[!UICONTROL résumé]** des apprentissages.
1. Dans la **[!UICONTROL section Tableau de bord de]** conformité, sélectionnez **[!UICONTROL Partagé avec les responsables]**.
1. Sélectionnez **[!UICONTROL Partager le tableau de bord]** et sélectionnez les étiquettes créées dans le **[!UICONTROL menu déroulant Conformité]** personnalisée.


   ![](assets/compliance-type.png)
   _Sélectionner le type de conformité_

1. Tapez et sélectionnez le nom du responsable dans la zone de **[!UICONTROL texte Partager avec]** .
1. Sélectionnez **[!UICONTROL Partager]** pour envoyer le tableau de bord au gestionnaire sélectionné.

>[!NOTE]
>
>Le partage du nouveau tableau de bord remplacera le tableau de bord existant dans l’application du gestionnaire sélectionné. Les responsables pourront afficher le tableau de bord nouvellement partagé par les administrateurs.

<!--In the final visualization, you can check the compliance status of learners, and take appropriate action.

Also, an Admin can view individual training data in the **[!UICONTROL Compliance Dashboard]**.

For instance, the Administrator has identified three trainings to track compliance. Learning Manager provides the compliance snapshot for all three trainings at once.

Now an Admin can click on any training and quickly view the compliance for the selected training.

![](assets/compliance-dashboard.png)
*View Compliance dashboard*

You can also see the compliance status for each internal team.

Click the link **[!UICONTROL Compliance Status Details]** on the bottom of the visualization. 

You can see that, for a team, the number of learners in the team are violating or honoring the learning compliance.

![](assets/compliance-statusofateam.png)
*Compliance status of a team*

### Share training with managers

Learning Manager offers compliance dashboard to all Administrators and Managers. Managers find it very useful to track compliance of their team members for a particular training. At the same time, Administrators would like all Managers to add compliance trainings to their dashboard and track it. 

In Learning Manager, the **[!UICONTROL Share with Managers]** workflow allows Administrators to share training with Managers, so that they can get added to a manager's Compliance Dashboard. Thus, Managers do not need to take any action and can start tracking compliance immediately. 

An Administrator can share a set of training courses with managers individually or with a group. This sharing can help a manager easily track the compliance of his/her team for the specified training.

The Administrator can "push" a default list of compliance training to be viewed in the manager's compliance dashboard.

### Share training

1. In **[!UICONTROL Reports]** > **[!UICONTROL Learning Summary]**, scroll down, and click the tab **[!UICONTROL Share with Managers]**. 

   ![](assets/share-with-managers.png)
   *Share training with managers*

1. To add training or multiple training, click **[!UICONTROL Share more]**.   

1. In the **[!UICONTROL Share with Managers]** dialog, choose the training(s) and the manager(s).

   ![](assets/select-training.png)
   *Select training to share with managers*

1. Click **[!UICONTROL Share]**.

The training is now shared with the specified manager.

### View training

In the list of shared training, click **[!UICONTROL View]**. You can view the training that is assigned to a manager or some managers.

### Withdraw training

1. To withdraw training from a manager, click **[!UICONTROL Withdraw]**.  

1. Click **[!UICONTROL Proceed]**. This withdraws previously shared training from the Manager's compliance dashboard.-->

## Rapports personnalisés

Les administrateurs peuvent générer des rapports spécifiques à l’aide du modèle personnalisé disponible dans la **[!UICONTROL section Rapports]** .

### Rapports échantillon {#samplereports}

L’onglet **[!UICONTROL Exemples de rapports]** affiche certains rapports indicatifs basés sur des exemples de points de données. Consultez ces rapports pour avoir une idée des différents types de rapports comportant de nombreuses fonctionnalités et pouvant être générés en utilisant les données de votre compte.

### Rapports de tableau de bord {#dashboardreports}

Un tableau de bord est une série de rapports. Les rapports peuvent être regroupés dans un tableau de bord selon votre choix. Pour afficher tous les panoramas que vous avez créés, cliquez sur cet onglet de panorama. Dans la liste déroulante Afficher le **[!UICONTROL tableau de bord]** , vous pouvez sélectionner le tableau par défaut ou un tableau de bord que vous avez créé.

### Rapports Excel {#excelreports}

L’onglet **[!UICONTROL Rapports Excel]** vous permet d’exporter des rapports au format de fichier XLS.

Vous pouvez télécharger les types de rapport suivants :

* Rapports de cours
* Relevés de notes des élèves
* Rapport des annonces
* Rapport des assistances à la tâche
* Piste d’audit de contenu
* Piste d’audit de l’utilisateur
* Rapport de connexion/d’accès
* Transcriptions de ludification
* Piste d’audit de ludification

### Relevés de notes de l&#39;élève {#learnertranscripts}

Les relevés de notes des élèves dans les rapports Excel affichent les colonnes Crédits requis et Crédits gagnés sous forme de nombres décimaux.

### Rapports de cours {#coursereports}

En tant qu’administrateur, vous pouvez télécharger des rapports pour les cours. Procédez comme suit :

1. Ouvrez **[!UICONTROL des rapports]** > **[!UICONTROL des rapports]** personnalisés > **[!UICONTROL des rapports]** Excel > **[!UICONTROL des rapports de]** cours.
1. La boîte de dialogue **[!UICONTROL Rapport de cours]** s’affiche. Sélectionnez le cours dont vous souhaitez récupérer le rapport et cliquez sur **[!UICONTROL Afficher]**.

   ![](assets/course-reports.png)
   *Rapports de cours*

1. Vous êtes redirigé vers la page du cours. Vous pouvez exporter le score du quiz par utilisateur et par question en fonction de chaque inscription en choisissant le type d’inscription spécifique.
1. Sélectionnez **[!UICONTROL Exporter le score du quiz]** pour exporter le rapport. La boîte de dialogue **[!UICONTROL Génération d’une demande de rapport]** s’affiche. Cliquez sur **[!UICONTROL OK]** pour confirmer.

   ![](assets/generating-reportrequest.png)
   *Génération de la demande de rapport*

   >[!NOTE]
   >
   >Un rapport de scores de questionnaires contiendra les détails des scores pour chaque tentative si l’option de multiples tentatives est configurée pour le module.

### Relevés de notes des élèves {#LearnerTranscripts-1}

Adobe Learning Manager permet aux administrateurs d’une organisation de générer des récapitulatifs liés aux stagiaires. Le rapport Relevé de notes de l’élève comprend les éléments suivants :

1. Relevé de notes de l’élève : tableau de bord Activité d’apprentissage
1. Compétence : Tableau de bord des compétences
1. Tableau de bord Conformité

Les relevés de notes des élèves dans les rapports Excel affichent les colonnes Crédits requis et Crédits gagnés sous forme de nombres décimaux.

Pour plus d’informations sur la génération de rapports de relevés de notes de l’apprenant et plus d’informations, consultez [Relevés de notes de l’élève](learner-transcripts.md).

### Rapports des annonces {#announcementsreports}

En tant qu’administrateur, vous pouvez générer un rapport de toutes les annonces que vous envoyez. Le rapport comporte les informations suivantes :

* Type d’annonce
* Nom de l’annonce
* Date de l’annonce
* État de l’annonce
* Nom de l’élève

Pour télécharger un rapport, suivez l’une de ces étapes :

1. Ouvrez **[!UICONTROL les rapports]** > **[!UICONTROL les rapports]** personnalisés > **[!UICONTROL les rapports]** Excel > **[!UICONTROL le rapport]** Annonces. La boîte de dialogue **[!UICONTROL Génération d’une demande de rapport]** s’ouvre. Cliquez sur OK.
1. [!UICONTROL **Communications**] > [!UICONTROL **actions >**] [!UICONTROL **rapport**] d’exportation.

   ![](assets/announcements.png)
   *Rapport d’annonces*

1. Vous pouvez extraire un rapport pour une annonce spécifique en cliquant sur **[!UICONTROL Exporter le rapport]** sous l’icône de paramètres.

   ![](assets/announcements-specific-report.png)
   *Rapport pour des annonces spécifiques*

### Rapport des assistances à la tâche {#jobaidsreport}

Les assistances à la tâche constituent du contenu de formation auquel un élève peut accéder sans s’inscrire à un objet d’apprentissage spécifique comme un cours ou un programme d’apprentissage. Les administrateurs peuvent extraire et télécharger un rapport sur les assistances à la tâche.

Le rapport extrait comprend les informations suivantes :

* Nom
* Type d’assistance à la tâche
* État de l’assistance à la tâche (publiée ou retirée)
* Date d’inscription
* Date de fin
* Date de téléchargement
* Nom de l’élève
* Nom du responsable
* Créé par

Pour télécharger un rapport, effectuez l’une des opérations suivantes :

* Ouvrez  **[!UICONTROL des rapports]** > **[!UICONTROL des rapports]** personnalisés > **[!UICONTROL des rapports]** Excel > **[!UICONTROL des rapports]** Aide à la tâche. La boîte de dialogue **[!UICONTROL Génération d’une demande de rapport]** s’affiche. Cliquez sur **[!UICONTROL OK]**.
* Ouvrez l’aide **[!UICONTROL >****les actions]** > **[!UICONTROL exporter le rapport]**.

![](assets/job-aids.png)
*Rapport Aides à la tâche*

* Vous pouvez également extraire un rapport pour une assistance à la tâche spécifique en cliquant sur **[!UICONTROL Exporter le rapport]** sous l’icône des paramètres.

![](assets/job-aid-specific-download.png)
*Rapport pour une aide à la tâche spécifique*

### Rapport des assistances à la tâche

Après avoir sélectionné **[!UICONTROL le rapport]** Aides à la tâche dans la liste, deux options s’affichent :

![rapport](assets/job-aids-new.png)
*sur les aides à la tâche Télécharger le rapport d’inscription des aides à la tâche aux États-Unis*

**Toutes les aides** à la tâche : Si le nombre d’aides à la tâche dans le compte est inférieur à 10 millions, le rapport généré contiendra des informations sur l’inscription de toutes les aides à la tâche. Il s’agira de la sélection par défaut. Si le nombre de lignes dépasse 10 millions, une erreur s’affiche et vous devez sélectionner manuellement les outils de travail requis.

**Aides à la tâche sélectionnées** : Si vous sélectionnez cette option, vous pouvez entrer les aides à la tâche pour lesquelles vous souhaitez générer le rapport. Vous pouvez sélectionner au maximum 10 aides à la tâche. Adobe Learning Manager vérifie si le nombre d’aides à la tâche dépasse 10 millions.

![Rapport Aides à la tâche S’inscrire](assets/job-aids-2-new.png)
*Sélectionner une aide à la tâche*

**Rapport sur les aides à la tâche**

Si vous sélectionnez cette option, les détails de toutes les assistances à la tâche du système, ainsi que leurs métadonnées et formations, sont téléchargés.

Le rapport téléchargé se compose des champs suivants :

* Nom de l’assistance à la tâche
* Langue(s)
* ID
* Type
* Durée (minutes)
* État
* Date de publication (fuseau horaire UTC)
* Créé par nom
* Créé par courrier électronique
* Créé par ID unique utilisateur
* Catalogue(s)
* Parcours d’apprentissage
* Cours
* Balise(s)
* Compétence(s)

**Rapport d’inscription des utilisateurs d’aides à la tâche**

Le rapport d’inscription contient des détails sur l’inscription des utilisateurs et d’autres informations.

Le rapport téléchargé se compose des champs suivants :

* Nom de l’assistance à la tâche
* Type
* État
* Date d’inscription (fuseau horaire UTC)
* Date de réalisation (fuseau horaire UTC)
* Date de téléchargement (fuseau horaire UTC)
* Nom de l’élève
* Courrier électronique
* ID utilisateur unique
* Nom du responsable
* Adresse électronique du responsable
* ID utilisateur unique de responsable
* Affecté par nom
* Affecté par courrier électronique
* Affecté par ID utilisateur unique
* Créé par nom
* Créé par courrier électronique
* Créé par ID unique utilisateur
* Code tâche
* Nouveau champ
* Profil

### Rapports de piste d’audit de contenu {#contentaudittrailreports}

Utilisez le **[!UICONTROL générateur de rapports Content Audit Trail]** pour générer un rapport de toutes les modifications et modifications apportées à un cours au cours de sa vie dans le système. Le rapport généré récupère les informations suivantes.

* ID d’objet
* Nom d’objet
* Type d’objet
* Type de modification
* Description
* ID de l’objet référencé
* Nom de l’objet référencé
* Modifié par le nom d’utilisateur
* ID utilisateur de l’auteur de la modification
* Date de modification (fuseau horaire UTC)

Dans la **colonne Type de** modification, vous obtiendrez les informations suivantes :

| Type de modification | Description |
| --- | --- |
| Créer | Cours créé |
| Certification Ajouter | Certification ajoutée au catalogue |
| Suppression de certification | Certification supprimée du catalogue |
| Ajout de contenu | Contenu ajouté au module |
| Ajout de cours | Cours ajouté au cursus de formation |
| Suppression de cours | Cours supprimé du cursus de formation |
| Ajouter une étiquette personnalisée | Étiquette personnalisée ajoutée au catalogue |
| Suppression d’étiquette personnalisée | Étiquette personnalisée supprimée du catalogue |
| Supprimer | Catalogue supprimé |
| Ajout d’une aide à la tâche | Aide à la tâche ajoutée au catalogue |
| Suppression de l’aide à la tâche | Aide à la tâche supprimée du catalogue |
| Ajout d’un cursus de formation | Cursus de formation ajouté au catalogue |
| Suppression du cursus de formation | Cursus de formation supprimé du catalogue |
| Ajout du contenu du module | Module ajouté au cours (section Contenu) |
| Suppression du contenu du module | Module supprimé du cours (section Contenu) |
| Publié | Cours ou cursus de formation publié et ajouté au catalogue par défaut |
| Republié | Cours réédité |
| Ajout de ressource | Ressource ajoutée au cours |
| Suppression de ressource | Ressource supprimée du cours |
| Retiré | Cours retiré |
| Ajouter un catalogue partagé | Catalogue partagé vers Catalogue |
| Suppression du catalogue partagé | Partage de catalogue supprimé du catalogue |
| Mise à jour du catalogue partagé | Etat de partage de catalogue : actif |
| Mise à jour  | Cours ou cursus de formation mis à jour |
| Ajout d’un groupe d’utilisateurs | Groupe d’utilisateurs ajouté au catalogue |
| Suppression d’un groupe d’utilisateurs | Groupe d’utilisateurs supprimé du catalogue |

Les informations relatives aux métadonnées ne sont pas récupérées dans le rapport généré.

Pour générer un rapport d’audit de piste de cours, procédez comme suit.

1. Sélectionnez **[!UICONTROL Rapport]** > **[!UICONTROL rapports]** Excel > **[!UICONTROL Piste d’audit de cours]**. La boîte de dialogue **[!UICONTROL Piste d’audit de contenu]** s’affiche.

   ![](assets/course-audit-trial.png)
   *Piste d’audit de cours*

1. Sélectionnez le cours, le programme d’apprentissage et la certification dont vous souhaitez télécharger le rapport. Si ces informations ne sont pas spécifiées, tous les rapports sont téléchargés par défaut.
1. Sélectionnez une plage de dates pour le rapport et cliquez sur **[!UICONTROL Générer]**.
1. Le rapport est généré et vous serez averti que le rapport d’audit de contenu est prêt. Vous pouvez télécharger le rapport.

### Rapports de piste d’audit d’utilisateur {#useraudittrailreports}

La piste d’audit utilisateur capture le cycle de vie des utilisateurs, des groupes d’utilisateurs et des profils d’auto-inscription. Elle indique tout ajout et toute suppression d’utilisateur ainsi que tout changement de responsable. La création et la suppression des profils d’auto-inscription sont enregistrées. Vous pouvez également suspendre et reprendre le processus d’auto-inscription.

Vous pouvez utiliser les fonctions Ajouter, Activer, Désactiver, Suspendre ou Reprendre pour les profils externes, et les fonctions Ajouter, Supprimer, Suspendre ou Reprendre pour le processus d’auto-inscription. Les téléchargements de fichier CSV sont également consignés.

1. Sélectionnez  **[!UICONTROL Rapport > Rapport Excel > Piste]** utilisateur. La boîte de dialogue Journal d’audit utilisateur s’affiche.
1. La boîte de dialogue Piste d’audit d’utilisateur s’affiche. Choisissez la plage de dates dans le menu contextuel. Vous pouvez choisir de générer le rapport pour la semaine passée ou le mois passé. Vous pouvez également sélectionner une date personnalisée.

   ![](assets/user-audit-trail.png)
   *Suivi utilisateur*

1. Cliquez sur **[!UICONTROL Générer]** pour générer le rapport.

La boîte de dialogue **[!UICONTROL Rapport de piste d’audit d’utilisateur]** contient deux filtres.

**Filtre de rage de date :** Sélectionnez la plage de dates pour laquelle vous souhaitez générer le rapport. Trois options s’offrent à vous :

* La semaine dernière
* Le mois dernier
* Date personnalisée

Sélectionner le filtre Apprenants : Search pour un utilisateur ou un groupe d’utilisateurs.

Le rapport exporté contient les données des utilisateurs qui répondent aux deux critères de recherche spécifiés.

![](assets/user-audit-trail.png)
*Suivi utilisateur*

>[!NOTE]
>
>Lorsqu’une compétence est attribuée ou supprimée, elle peut être suivie dans le rapport d’audit de l’utilisateur.

### Rapport de configuration des extensions

Ce rapport fournit des informations sur les détails de configuration de toutes les extensions natives ajoutées, y compris leur état d’activation. Découvrez comment télécharger le rapport d’extension, voir [Télécharger le rapport](native-extensibility.md#download-extension-report) d’extension.

### Rapport d’activité xAPI

Ce rapport fournit les données de toutes les instructions xAPI enregistrées et générées au cours des modules d’activité xAPI.

Pour télécharger ce rapport, procédez comme suit :

1. Sélectionnez  **[!UICONTROL Rapport > rapport Excel > rapport]** d’activité xAPI. La boîte de dialogue Rapport d’activité xAPI s’affiche.
1. Choisissez la plage de dates dans le menu contextuel. Vous pouvez choisir de générer le rapport pour la semaine passée ou le mois passé. Vous pouvez également sélectionner une date personnalisée.
1. Sélectionnez les apprenants et l’activité dans le menu déroulant.
1. Sélectionnez **[!UICONTROL Générer]** pour générer le rapport.

### Rapports de ludification {#gamification}

Les administrateurs peuvent télécharger une transcription de ludification au format CSV. Vous pouvez télécharger le rapport pour un utilisateur individuel ou pour des groupes d’utilisateurs. Le nom d’utilisateur, l’adresse e-mail de l’utilisateur, l’UUID de l’utilisateur, le nombre total de points marqués, la répartition des points collectés, le nom des groupes dans lesquels l’utilisateur joue, le nom du gestionnaire et les valeurs de champ actif sont tous extraits dans le rapport. Les administrateurs peuvent utiliser ce rapport pour évaluer et comprendre le classement des utilisateurs dans une entreprise ou pour un groupe spécifique.

1. Sélectionnez Rapport > Rapport Excel > Rapport Gamification.

   ![](assets/gamification.png)
   *Rapport de gamification*

1. La boîte de dialogue Transcriptions de ludification s’affiche. Sélectionnez des élèves à l’aide de leur nom, profil, groupes d’utilisateur, ID d’adresse électronique ou UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Boîte de dialogue des transcriptions de gamification*

1. Cliquez sur  **[!UICONTROL Générer]** pour générer le rapport.

   Après avoir généré le rapport d’un élève, vous devez être en mesure d’exporter les informations de niveau actuel et obtenu pour tous les utilisateurs (internes, externes ou supprimés) du compte. Vous pouvez également vérifier les dates auxquelles certains niveaux ont été atteints par un élève :

   * Date d’atteinte du niveau Bronze
   * Date d’atteinte du niveau Argent
   * Date d’atteinte du niveau Or
   * Date d’atteinte du niveau Platine

   Ces colonnes contiennent les dates auxquelles le niveau a été atteint pour la toute première fois. La colonne **[!UICONTROL Niveau]** actuel affiche le niveau actuel de l’élève.

   Lorsque l’administrateur réinitialise la ludification, tous les points de l’élève sont réinitialisés en conséquence.

### Rapport Gamification Audit Trail {#gamification-audit-trail}

Ce rapport contient l’historique et les raisons des points de gamification gagnés par les apprenants pour chaque règle.

### Télécharger le rapport

1. Sélectionnez l’URL de piste d’audit de Gamification.
1. Dans la fenêtre contextuelle Journal d’audit **** de gamification, sélectionnez la plage de dates.
1. Sélectionnez **Générer**.

Le rapport est téléchargé au format CSV. Le fichier contient les colonnes suivantes :

* Nom
* E-mail/UUID,
* Statut
* Action
* Aiguillage
* Points d’équilibre
* Règle/Tâche
* Sous-tâche de règle/tâche,
* Détails de la règle/de la tâche
* Type
* Nom
* Nom de l’instanceDate d’obtention (fuseau horaire UTC)
* Heure de début de la règle/de la tâche
* Heure de fin de la règle/de la tâche

### Rapport d’inscription et de désinscription {#enrollmentandunenrollmentreport}

Les administrateurs et les gestionnaires peuvent extraire un rapport des apprenants qui ont été inscrits et désinscrits. En tant qu’administrateur, vous pouvez afficher tout élève, administrateur ou responsable qui a été inscrit ou désinscrit d’une instance d’un cours, d’un programme d’apprentissage ou d’une certification et exporter le rapport. En tant que responsable, vous ne pouvez récupérer qu’un rapport des membres de votre équipe. En tant que gestionnaire, vous ne pouvez pas voir les élèves supprimés ou votre propre nom dans l’application du gestionnaire en tant qu’élève inscrit ou non inscrit.

Pour télécharger un rapport, procédez comme suit : Ouvrez le **[!UICONTROL rapport]** Cours/Programme d’apprentissage/Certification ]**>**[!UICONTROL  les apprenants ]**>**[!UICONTROL  Action ]**>**[!UICONTROL  Exporter.

![](assets/unenrollment.png)
*Rapport de désinscription*

### Rapport de commentaires {#feedback-report}

En tant qu’administrateur, vous pouvez désormais récupérer le retour d’informations de l’élève (L1) et le retour d’informations du responsable (L3) pour des formations sélectionnées sur une période donnée.

Vous pouvez exporter les données à partir de l’interface utilisateur ou via le connecteur PowerBI pour une analyse plus approfondie.

Les rapports de commentaires L1 et L3 offrent une option pour télécharger un rapport de rétroaction consolidé pour les réponses L1 et L3 pour les formations sélectionnées pour une période d’un an **ou pour un** maximum de 10 formations sélectionnées pour n’importe quelle plage de dates.

Connectez-vous en tant qu’administrateur, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]**, puis dans la liste des rapports, cliquez sur **[!UICONTROL Rapport]** de commentaires.

![](assets/download-feedbackreport.png)
*Télécharger le rapport de retour d’information*

En cliquant sur télécharger, après avoir sélectionné les filtres, vous recevrez une notification pour télécharger le rapport au format CSV.

Le rapport téléchargé contiendra des détails tels que le nom et le type de formation, le nom de l’instance, le nom et l’adresse e-mail de l’apprenant, le type de commentaire : L1 ou L3, les dates des commentaires soumis pour les nouvelles données.

Pour les données existantes antérieures à la mise en œuvre de cette fonctionnalité, la date d’achèvement de LO sera affichée, la date d’achèvement de LO, la question de commentaire L1 Texte réel autorythmé et le texte de la salle de classe dans différentes colonnes, les réponses respectives des commentaires L1, le nom et l’adresse électronique du responsable, la valeur des commentaires L3 et la date d’envoi, les champs actifs.

Vous pouvez également exporter les données de l’interface utilisateur ou vers Power BI, qui prend en charge toutes les formations pour n’importe quelle plage de dates pour une analyse plus approfondie

### Rapport des formations {#training-report}

Learning Manager prend en charge le rapport de formation qui permet aux administrateurs de télécharger les détails de la formation et ses métadonnées associées telles que l’auteur, la date de publication, les compétences, les étiquettes de catalogue, etc.

Dans l’application Admin, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports]** personnalisés > **[!UICONTROL Rapports]** Excel > **[!UICONTROL Rapport]** Formations.

Vous pouvez télécharger des rapports pour les éléments suivants :

* Formations sélectionnées (10 maximum) : sélectionne une ou plusieurs formations (jusqu’à 10) dans n’importe quel catalogue
* Formations des catalogues sélectionnés (5 maximum) : (la sélection du catalogue contiendra jusqu’à cinq catalogues)
* Toutes les formations : (toutes les formations dans le compte)

![](assets/download-trainingreport.png)
*Télécharger le rapport de formation*

Dans la section Options avancées, les options suivantes sont disponibles :

* Inclure les descriptions de cours dans le programme d’apprentissage et la certification
* Inclure les informations de niveau de module

Après avoir sélectionné les filtres et cliqué sur Télécharger, vous recevrez une notification pour télécharger le rapport au format CSV.

Le rapport contiendra les champs suivants :

*Nom du catalogue, Type de formation, ID de formation, ID unique de formation, Nom de la formation, Sous-formations, Modules, Durée de la formation ou du module, Format, État de la formation, Compétences, Auteur, Date de dernière publication, Date de la dernière réalisation, Nombre d’inscriptions aux instructeurs, Nombre commencé, Nombre d’achèvements, Note L1 moyenne, Note L2 moyenne, Note L3 moyenne, Réponses L1 reçues, Réponses L2 reçues, Réponses L3 reçues, Étiquettes et balises de catalogue.*

![](assets/more-options.png)
*Options supplémentaires*

### Rapport récapitulatif de la session {#session-summary-report}

Le rapport récapitulatif de session contient toutes les sessions planifiées pour un élève à une date spécifiée.

Cela permet à l’administrateur d’exporter tous les détails des sessions virtuelles et de classe correspondant à la plage de dates donnée. L’administrateur peut également exporter le rapport de session en ce qui concerne des formations ou des instructeurs spécifiques.

Cela aidera également l’administrateur à comprendre les sessions planifiées sur une base mensuelle et à identifier le calendrier des instructeurs et les sessions déjà livrées.

En tant qu’administrateur, cliquez sur **[!UICONTROL Rapports]** personnalisés > **[!UICONTROL Rapport récapitulatif de]** session.

Dans la boîte de dialogue qui suit, sélectionnez la plage de dates et la formation ou l’instructeur pour obtenir un récapitulatif.

![](assets/session-summary-report.png)
*Rapport récapitulatif de la session*

Le fichier CSV téléchargé contient les champs suivants :

* Date et heure de début
* Date et heure de fin

* Nom du module
* Durée de la session (en minutes)
* Nombre de sièges
* Lieu
* Nom d’instance
* Nom du cours
* ID du cours
* Nom de l’instructeur
* E-mail de l&#39;instructeur
* Nombre d’inscriptions
* Type de session
* Limite de liste d’attente
* Nombre d’utilisateurs en liste d’attente
* E-mails des utilisateurs en liste d’attente
* Informations sur le lieu
* Région de l’emplacement

### Rapport sur l’utilisation de l’instructeur

Ce rapport capture le temps (en minutes) passé chaque jour par un instructeur pour enseigner les sessions qui lui sont assignées. Le rapport peut être téléchargé pendant une période de trois mois à compter de la date de début sélectionnée.

Pour télécharger le rapport, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports]** personnalisés > **[!UICONTROL Rapport]** d’utilisation d’Instructor.

Sélectionnez un ou plusieurs instructeurs et la plage de dates.

![Télécharger le rapport](assets/utilization-report.png)
*d’utilisation de l’instructeur Télécharger le rapport d’utilisation de l’instructeur*

Le rapport téléchargé contient les champs suivants :

* Nom du formateur
* ID de l’instructeur
* Niveau de compétence
* Dates sous forme de colonnes. Si le formateur est utilisé à une date donnée, le nombre de sessions apparaît. Si l’instructeur n’est pas utilisé un jour, la valeur affiche zéro.

Le rapport contient des enregistrements sur trois mois à partir du mois sélectionné.

Pour récupérer les enregistrements de tous les instructeurs, laissez le champ Instructeur vide.

Un administrateur personnalisé autorisé à générer des rapports peut également récupérer ce rapport.

### Rapport de piste d’audit d’utilisateur

Ce rapport capture des informations sur les apprenants qui ont changé d’instance, « d’instance » à « à instance », commutées par heure, date, etc.

Sélectionnez les élèves ou un groupe d’utilisateurs.

Pour télécharger le rapport, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports]** personnalisés > **[!UICONTROL Rapport]** de piste d’audit utilisateur.

![Télécharger le rapport de piste d’audit de l’utilisateur](assets/user-audit-report.png)

*Télécharger le rapport de piste d’audit de l’utilisateur*

### Rapport du plan d’apprentissage

Ce rapport contient des détails sur tous les plans d’apprentissage d’un compte, par exemple, les groupes d’utilisateurs associés, le statut et les informations de déclencheur.

Le rapport contient les éléments suivants :

* Nom du plan d’apprentissage
* Type (se produit lorsque)
* Formation (terminée)
* Compétence (atteinte)
* Date (à la date)
* Action
* Statut, créé par
* Date de création
* Date de dernière modification
* Groupe d’utilisateurs (s’applique à)
* Groupe d’utilisateurs (ajouter à)
* Inscrire après
* Type(s) d’élément d’apprentissage
* Élément(s) d’apprentissage
* Instance(s) d’élément d’apprentissage
* Élément d’apprentissage
* Date d’achèvement
* Rappel des éléments d’apprentissage
* Scope-Catalog
* Scope-Usergroup

## Inscription aux courriers électroniques {#emailsubscriptions}

Vous pouvez obtenir vos rapports favoris par courrier électronique en vous abonnant.

### Configuration des abonnements aux courriers électroniques

>[!INFO]
>
>Dans cette formation, vous apprendrez à configurer des abonnements par e-mail pour les rapports de tableau de bord.<br><br>[![bouton](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=PLHRQ62N&amp;mv=display&amp;mv2=display#/course/8318927)</br></br>


Si vous ne parvenez pas à lancer la formation, écrivez à <almacademy@adobe.com>.

Dans **[!UICONTROL la page Rapports]** , cliquez sur l’onglet  **[!UICONTROL Abonnement]** . La page Abonnement aux rapports s’affiche.

Pour sélectionner le nom du rapport dans la liste déroulante, commencez à taper le nom du rapport dans le champ Rapports. Sélectionnez la fréquence du courrier électronique dans la liste déroulante. Vous pouvez ajouter l’objet du courrier électronique et fournir un autre ID de courrier électronique.

Vous pouvez modifier et supprimer des abonnements.

## Rapports historiques

Les rapports historiques dans Adobe Learning Manager (ALM) font référence aux rapports qui capturent les données et les activités historiques au sein de la plateforme d’apprentissage. Ces rapports fournissent des informations sur les activités passées des apprenants, le contenu de la formation, les performances des groupes d’utilisateurs et d’autres données pertinentes. Les rapports historiques permettent aux administrateurs de suivre, de surveiller et d’analyser les progrès et l’efficacité des initiatives d’apprentissage au fil du temps.

### Rapports d’accès aux cours

Les rapports d’accès aux cours fournissent des informations sur la nouvelle visite de chaque cours.

Pour télécharger ce rapport, procédez comme suit :

1. Accédez à **[!UICONTROL Rapports]** > **[!UICONTROL Rapports]** personnalisés > **[!UICONTROL Rapports]** historiques.
1. Sélectionnez Rapport **[!UICONTROL d’accès au cours]**. La boîte de dialogue Génération de la demande de rapport s’ouvre.
1. Sélectionnez l’année et le trimestre dans le menu déroulant.
1. Sélectionnez **[!UICONTROL Générer]**.

### Rapports de connexion/accès

Les rapports de connexion/accès fournissent des informations sur les connexions et les accès des utilisateurs. Vous pouvez générer un rapport contenant trois mois de données simultanément.

Pour télécharger ce rapport, procédez comme suit :

1. Accédez à **[!UICONTROL Rapports]** > **[!UICONTROL Rapports]** personnalisés > **[!UICONTROL Rapports]** historiques.
1. Sélectionnez Rapport **[!UICONTROL de connexion/accès]**. La boîte de dialogue Génération de la demande de rapport s’ouvre.
1. Sélectionnez l’année et le trimestre dans le menu déroulant.
1. Sélectionnez **[!UICONTROL Générer]**.

## Création d’un tableau de bord {#createadashboard}

1. Pour commencer à créer vos propres panoramas, cliquez sur Ajouter un tableau de bord sur le côté droit de la page.

   ![](assets/add-dashboards.png)
   *Ajouter des tableaux de bord*

1. Indiquez le nom et la description du tableau de bord.
1. Si vous souhaitez partager le tableau de bord avec un gestionnaire, sélectionnez-le dans **[!UICONTROL le champ Partager avec]** . Vous pouvez utiliser tous les critères de sélection habituels pour cette opération.
1. Cliquez sur **[!UICONTROL Enregistrer].**

Vous pouvez afficher le tableau récemment créé dans l’onglet **[!UICONTROL Rapports de tableau de bord]**.

Pour ajouter des rapports à votre panorama, cliquez sur la liste déroulante située dans le coin supérieur droit de votre fenêtre et cliquez sur **[!UICONTROL Ajouter un rapport]**. Le rapport créé selon cette procédure est associé à votre tableau de bord.

>[!NOTE]
>
>Les rapports que vous créez en cliquant sur Ajouter dans le coin supérieur droit de la page Rapports sont ajoutés à votre tableau de bord par défaut.

## Tableaux de bord partagés {#shareddashboards}

Les tableaux partagés sont une série de rapports qui ont été partagés avec vous par d’autres utilisateurs au sein de votre entreprise. Tous les rapports que vous ajoutez à un tableau partagé sont automatiquement partagés avec les autres utilisateurs ayant accès à ce tableau.

Vous pouvez partager le panorama en procédant de deux manières :

* En saisissant dans **[!UICONTROL le champ Partager avec]** les utilisateurs avec lesquels le tableau de bord est partagé.
* Choisissez Modifier un tableau dans la liste déroulante et saisissez les détails de l’utilisateur avec lequel partager le tableau de bord.

>[!NOTE]
>
>Un responsable peut uniquement afficher les rapports des membres de son équipe à partir d’un tableau de bord partagé.

## Téléchargements {#downloads}

La feuille exportée des rapports de tableau de bord fournit des informations détaillées au lieu du résumé du rapport. Le rapport téléchargé suit le format d’un relevé de notes d’élève.

## Création de rapports {#report}

1. Cliquez sur Rapports dans le volet de gauche. La page Synthèse des rapports s’affiche.

   >[!NOTE]
   >
   >Par défaut, au moins trois exemples de rapport s’affichent dans l’onglet des exemples du tableau de bord. Les exemples de rapport servent uniquement à offrir un exemple de création et de modification possible.

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Ajouter]**.
1. Dans la boîte de dialogue **[!UICONTROL Ajouter un rapport]**, dans la liste déroulante Type, vous pouvez choisir l’un des rapports prédéfinis ou sélectionner **[!UICONTROL Personnalisé]**. Si vous sélectionnez un rapport prédéfini, vous pouvez voir que le formulaire est pré-rempli. Vous pouvez modifier certains champs et cliquer sur **[!UICONTROL Enregistrer]**. Cela ajoute le rapport à votre tableau de bord par défaut.

   ![](assets/create-report.png)
   *Créer un rapport*

   Dans **[!UICONTROL Type de rapport]**, vous pouvez choisir un ensemble prédéfini de rapports ou des valeurs personnalisées. Vous pouvez afficher les rapports suivants en tant que partie d’un ensemble prédéfini de rapports :

   * Compétences attribuées et obtenues
   * Cours inscrits et terminés
   * Efficacité des cours
   * Programmes d’apprentissage inscrits et terminés
   * Temps passé à apprendre par cours
   * Temps passé à apprendre par trimestre
   * Fin de certification

1. Choisissez **[!UICONTROL l’axe Y]** pour votre rapport depuis les options du menu déroulant. Pour certains des critères sélectionnés, vous pouvez choisir un ou plusieurs états dans les options États. Par exemple, pour un critère principal de statistiques d’inscription à un cours, les états peuvent être Terminé, Incomplet et Inscrit. Les données de plage principale sont représentées sous forme de graphiques à barres dans le rapport.

   ![](assets/axes-for-reports.png)
   *Axes pour les rapports*

1. Choisissez la plage/les critères secondaires de **[!UICONTROL l’axe Y]** pour votre rapport parmi les options de la liste déroulante. Par exemple, pour une option d’inscription de programme d’apprentissage, choisissez un ou plusieurs états dans la liste déroulante États. Les données de plage secondaire sont représentées sous forme de graphiques linéaires.
1. Choisissez les critères X**-axis** appropriés pour votre rapport dans les options déroulantes. Si l’axe X est sélectionné en tant que date, une option de regroupement de votre critère d’axe X par Jour, Mois, Trimestre et Année est disponible.
1. Dans la section Intervalle de temps, choisissez l’option appropriée dans la liste déroulante. Les options disponibles sont :

   * 30 derniers jours
   * Trimestre
   * Année
   * QTD (90 derniers jours)
   * YTD (365 derniers jours)
   * Plage de dates. Indiquez des valeurs dans les champs de données **[!UICONTROL De]** et **[!UICONTROL À]**.

   ![](assets/time-filter-for-report.png)

1. **Section Filtres**

   Les filtres s’affichent dans la boîte de dialogue Ajouter un rapport en bas en fonction des types de rapports que vous avez sélectionnés. Certains de ces filtres principaux sont mentionnés ci-dessous.

   * **Responsable :** vous pouvez sélectionner l’un des responsables en fonction de la hiérarchie. Pour certains responsables, il peut exister des responsables subordonnés ainsi que plusieurs employés supervisés par chaque responsable subordonné.
   * **Profil :** choisissez la désignation de votre employé. Il est plus pratique d’afficher les rapports des employés selon leur profil/désignation. Par exemple, informaticien ou ingénieur.
   * **Groupe d’utilisateurs :** sélectionnez le groupe d’utilisateurs à partir duquel vous souhaitez filtrer les rapports. Learning Manager récupère les groupes d’utilisateurs définis pour votre compte depuis la fonction Utilisateurs.
   * **Contenu :** vous pouvez filtrer votre rapport par rapport à un cours en le sélectionnant dans la liste déroulante.

   Élargissez cette section et choisissez les filtres requis.

   ![](assets/choose-filters.png)
   *Choisir les filtres*

1. Cliquez sur **[!UICONTROL Enregistrer]** pour terminer la création d’un rapport.

   ![](assets/sample-report.png)
   *Exemple de rapport*

## Modification d’un rapport {#editareport}

Dans le rapport, cliquez sur la flèche déroulante et sélectionnez l’option **[!UICONTROL Modifier le rapport]**.

![](assets/edit-a-report-1.png)
*Modification d’un rapport*

Apportez les modifications requises au rapport. Cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer les modifications.

## Déplacer un rapport vers un tableau de bord {#moveareporttoadashboard}

Choisissez cette option pour déplacer le rapport actuel vers un tableau de bord existant. Pour déplacer le rapport, cliquez sur l’option **[!UICONTROL Déplacer vers le tableau de bord]**.

![](assets/move-a-report.png)
*Déplacement d’un rapport vers un tableau de bord*

Choisissez le tableau de bord vers lequel vous souhaitez déplacer le rapport et cliquez sur **[!UICONTROL Déplacer]**.

## Création d’une copie d’un rapport {#createacopyofareport}

Pour créer une copie du rapport, sélectionnez l’option **[!UICONTROL Créer une copie]**.

![](assets/copy-a-report.png)
*Création d’une copie d’un rapport*

Choisissez le tableau vers lequel vous souhaitez copier le rapport. Pour démarrer la copie, cliquez sur **[!UICONTROL Copier]**.

## Suppression d’un rapport {#deleteareport}

Pour supprimer un rapport, sélectionnez l’option **[!UICONTROL Supprimer le rapport]**. Une fois le rapport supprimé, vous ne pouvez pas le restaurer. L’opération est irréversible. Procédez avec prudence lors de la suppression d’un rapport.

![](assets/delete-a-report.png)
*Suppression d’un rapport*

## Téléchargement d’un rapport {#downloadareport}

Pour télécharger le report, sélectionnez l’option **[!UICONTROL Télécharger le rapport.]**.

![](assets/download-a-report.png)
*Téléchargement d’un rapport*

## Redimensionnement d’un rapport {#resizeareport}

Vous pouvez redimensionner vos rapports aux formats 1 × 1 (moyen) et 1 × 2 (grand). Cela vous donne un meilleur aperçu de vos rapports. En outre, vous pouvez facilement effectuer un panoramique et un zoom sur ces rapports.

## Filtres {#filters}

Les filtres s’affichent dans la boîte de dialogue **[!UICONTROL Ajouter un rapport]** en bas de la page en fonction des types de rapport que vous avez sélectionnés. Certains de ces filtres principaux sont mentionnés ci-dessous.

**Responsable :** vous pouvez sélectionner l’un des responsables en fonction de la hiérarchie. Pour certains responsables, il peut exister des responsables subordonnés ainsi que plusieurs employés supervisés par chaque responsable subordonné.

**Profil :** choisissez la désignation de votre employé. Il est plus pratique d’afficher les rapports des employés selon leur profil/désignation. Par exemple, informaticien ou ingénieur.

**Groupe d&#39;utilisateurs** Choisissez le groupe d&#39;utilisateurs à partir duquel vous souhaitez filtrer les rapports. Learning Manager récupère les groupes d’utilisateurs définis pour votre compte depuis la fonction Utilisateurs.

**Cours** Vous pouvez filtrer votre rapport en fonction de n’importe quel cours en les choisissant dans la liste déroulante.

![](assets/sample-report-admin.png)
*Filtrage d’un rapport*

Au-dessus de la légende du graphique, vous pouvez afficher une case de zoom. Placez-y le pointeur de la souris, cliquez et faites glisser la barre transversale sur n’importe quelle partie de la zone de zoom à agrandir.

Vous pouvez afficher les valeurs de l’axe Y secondaire sous forme de ligne à travers le graphique à barres. Par exemple, dans l’exemple ci-dessus, vous pouvez voir les valeurs de l’efficacité dans une ligne grise à travers le graphique.

## Rapports de groupes d’utilisateurs {#user-group-reporting}

Suivez la manière dont les groupes d’utilisateurs, tels que des services, des partenaires externes et des rôles se comportent en comparaison d’autres groupes d’utilisateurs ou par rapport à d’autres objectifs pédagogiques.

### Groupes d’utilisateurs {#usergroups}

Pour générer des rapports basés sur des groupes d’utilisateurs, choisissez **[!UICONTROL Groupe d’utilisateurs]** sur l’axe X dans la liste des options déroulantes, comme indiqué dans la capture d’écran ci-dessous.

![](assets/user-group-reports.png)
*Rapports de groupe d’utilisateurs*

Pour choisir un groupe d’utilisateurs, saisissez le nom du groupe. Vous pouvez voir les groupes suggérés qui s’affichent en fonction de la chaîne que vous saisissez. Une fois que vous voyez une liste de groupes, choisissez le groupe d’utilisateurs requis.

Vous pouvez également choisir plusieurs groupes d’utilisateurs à l’aide de la recherche par frappe anticipée.

Une fois que vous avez enregistré et généré le rapport, si vous avez sélectionné plusieurs groupes d’utilisateurs, le rapport est généré avec tous les groupes d’utilisateurs représentés dans le graphique à barres à côté des autres sur l’axe des x.

Ce rapport de groupe d’utilisateurs vous permet de comparer la performance d’un(e) service/division/rôle par rapport à l’autre pour leurs progrès en termes de formation.

### Attributs personnalisés de groupes d&#39;utilisateurs/utilisateur {#customusergroupsuserattributes}

Vous pouvez également créer des groupes d&#39;utilisateurs personnalisés à l&#39;aide de la fonction Ajouter des utilisateurs/un groupe d’utilisateurs dans Learning Manager. Après avoir créé des groupes d’utilisateurs, vous pouvez générer des rapports pour ces groupes d’utilisateurs personnalisés à l’aide d’une liste d’attributs, tels que l’emplacement ou la succursale.

Sur l’axe x, choisissez l’option d’attribut utilisateur et sélectionnez l’attribut dans la **liste déroulante de sélection** située à côté. Pour créer un rapport de groupe d’utilisateurs personnalisé basé sur ces attributs, vous devez également choisir le groupe d’utilisateurs approprié dans le filtre.

## Affichage des rapports {#viewingreports}

Dans la page Rapports, vous pouvez afficher tous les rapports. Vous pouvez réduire chaque rapport en cliquant sur l’icône moins (-) dans l’angle supérieur droit de chaque rapport. Cliquez sur l’icône (+) pour afficher de nouveau votre rapport.

## Affichage rapide avec différentes dates {#quickviewwithdifferentdates}

Vous pouvez modifier la valeur/plage de dates de tout rapport et afficher rapidement une date différente sans modifier ni enregistrer le rapport. Cliquez sur l’icône Modifier (comme illustré par une flèche dans l’instantané ci-dessous) en regard de la plage de dates, telle que QTD, dernière année. Pour confirmer la modification, choisissez la nouvelle valeur dans le menu déroulant et cliquez sur la coche. Vous pouvez annuler la modification en cliquant sur le symbole X.

>[!NOTE]
>
>Les valeurs de date que vous utilisez pour afficher le rapport sont temporaires. Cette vue du rapport n’est pas téléchargée lorsque vous sélectionnez l’option de téléchargement. Il ne s’agit que d’une vue temporaire.

![](assets/learner-count-report.png)
*Afficher le nombre d’apprenants*

## Affichage rapide avec différents responsables {#quickviewwithdifferentmanagers}

Si vous supervisez plusieurs responsables, vous pouvez afficher rapidement les rapports de chaque responsable. Sélectionnez un nom de responsable dans la liste déroulante pour afficher un rapport unique pour chaque responsable.

>[!NOTE]
>
>Les valeurs de responsable que vous utilisez pour afficher le rapport sont temporaires. Cette vue de rapport n’est pas téléchargée lorsque vous sélectionnez l’option de téléchargement. Il ne s’agit que d’une vue temporaire.

## Affichage des rapports sur les cours {#viewcoursereports}

### Génération de rapports de cours

>[!INFO]
>
>Dans cette formation, vous apprendrez à exporter des rapports de cours et à configurer des abonnements par courrier électronique pour ces rapports.<br><br>[![bouton](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=R726NKNM&amp;mv=display&amp;mv2=display#/course/8318904)</br></br>


Si vous ne parvenez pas à lancer la formation, écrivez à <almacademy@adobe.com>.

Vous pouvez afficher les rapports spécifiques de chaque cours en procédant comme suit :

1. Cliquez sur **[!UICONTROL le lien Afficher les rapports]** de cours dans l’onglet Mes tableaux de bord de la page Rapports.\
   Une boîte de dialogue contextuelle s’affiche. Un champ de saisie de texte apparaît où vous pouvez entrer le cours requis et les noms de cours suggérés apparaissent dans la liste déroulante. Sélectionnez le cours dans la liste affichée.

   ![](assets/view-course-report-300x117.png)

   *Affichage des rapports sur les cours*

1. Sélectionnez le cours de votre choix dans la liste déroulante, puis cliquez sur Afficher.
1. Vous êtes redirigé vers la page de résultats de score du quiz du cours sélectionné pour afficher le rapport de ce cours.

**Modifier un rapport/Déplacer vers un tableau de bord/Créer une copie/Supprimer un rapport/Redimensionner**

Cliquez sur la flèche déroulante dans l’angle supérieur droit de chaque rapport pour afficher des options telles que Modifier un rapport/Déplacer vers un tableau de bord/Créer une copie/Supprimer un rapport/Redimensionner.

![](assets/edit-options-dashboard-300x126.png)

*Modifier/Déplacer vers le panorama/Créer un Copier/Supprimer/Redimensionner les rapports*

**[!UICONTROL Modifier]** Pour revenir aux valeurs initiales lors de la modification des données, cliquez sur Réinitialiser. Cliquez sur Enregistrer après avoir modifié les valeurs.

**[!UICONTROL Déplacer vers le tableau de bord]** Vous pouvez déplacer le rapport actif vers un autre tableau de bord, choisi dans la liste des tableaux de bord.

**[!UICONTROL Créer une copie]** Vous pouvez copier le rapport sur le même tableau de bord ou sur un autre, choisi dans la liste des tableaux de bord.

**[!UICONTROL Supprimer]** Cliquez sur Supprimer pour supprimer le rapport. Un message d’avertissement/de confirmation s’affiche avant de pouvoir supprimer le rapport.

**[!UICONTROL Redimensionner]** Vous pouvez redimensionner les rapports en tailles 1×1 (moyenne) et 2×2 (grande).

## Générer et consulter des rapports pour un compte d’homologue {#generateandviewreportsforpeeraccount}

En tant qu’administrateur, outre la génération des rapports pour votre compte, vous pouvez également générer et afficher des rapports pour les comptes d’homologue que vous avez définis.

Après avoir créé un compte de pair avec un autre utilisateur, vous pouvez afficher les rapports correspondants à partir de la page **[!UICONTROL Rapports]**. Lorsque vous créez un rapport, le champ **[!UICONTROL Sélectionner un compte]** s’affiche. Dans la liste déroulante qui répertorie tous les comptes de pairs auxquels vous êtes associé, sélectionnez le compte pour lequel vous souhaitez afficher les rapports partagés.

Lors de la création d’un compte d’homologue, si vous n’avez pas sélectionné l’option Partager un catalogue, vous ne pouvez pas afficher ce compte dans cette liste.

![](assets/acc1-jpg.png)
*Gérer les rapports pour le compte homologue*

1. Sélectionnez les axes X et Y et la date du rapport.
1. Remarquez que le bouton Catalogues partagés du champ de filtres est activé automatiquement. Cela est obligatoire. Si le catalogue partagé n’est pas activé, cela signifie que vous ne pouvez pas générer ni afficher de rapports pour le compte d’homologue.
1. Dans la liste déroulante située sous Catalogue partagé, sélectionnez le catalogue partagé pour lequel vous souhaitez afficher le rapport.
1. Cliquez sur [!UICONTROL **Enregistrer**].

   ![](assets/acc2.png)
   *Sélectionner le catalogue partagé pour le compte homologue*

1. Après avoir cliqué sur **[!UICONTROL Enregistrer]**, vous pouvez afficher la représentation graphique de vos rapports dans votre tableau de bord par défaut. Depuis ce tableau de bord, vous pouvez filtrer davantage le rapport en fonction du responsable pour le compte d’homologue spécifique.
1. Si vous apportez des modifications au catalogue, les modifications sont immédiatement prises en compte dans les rapports et le tableau de bord générés par l’homologue. Toutefois, si l’homologue modifie le catalogue, les modifications ne s’affichent pas automatiquement dans votre tableau de bord.
1. Si vous souhaitez que votre tableau de bord soit mis à jour automatiquement, votre homologue doit vous envoyer une nouvelle requête d’homologue.

   >[!NOTE]
   >
   >Les responsables ne peuvent pas afficher les rapports d’homologue.

## Forum aux questions {#frequentlyaskedquestions}

+++Comment partager un tableau de bord personnalisé avec un responsable ?

Lors de la création d’un tableau de bord, entrez le nom et une description. Pour partager un tableau de bord avec un responsable, entrez le nom du responsable dans le champ **[!UICONTROL Partager avec]**.

![](assets/share-dashboard-manager.png)
*Partage d’un tableau de bord*
+++
