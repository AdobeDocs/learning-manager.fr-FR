---
description: Téléchargez le relevé de notes de l’élève et gérez les rapports à l’aide de Learning Manager.
jcr-language: en_us
title: Relevés de notes de l'élève
contentowner: jayakarr
exl-id: f88ad02c-6d36-41e7-9d83-0ebc70d98d63
source-git-commit: de57d96488851c31c380b34672767a803379842e
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 66%

---

# Relevés de notes de l&#39;élève

Téléchargez le relevé de notes de l’élève et gérez les rapports à l’aide de Learning Manager.

Adobe Learning Manager permet aux administrateurs d&#39;une organisation de générer des relevés liés aux élèves.

## Générer les relevés de notes des élèves {#generatelearnertranscripts}

1. Pour générer les relevés de notes des élèves, cliquez sur **[!UICONTROL Rapports]** dans le volet gauche de la connexion Administrateur.

   L&#39;administrateur accède à l&#39;onglet **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapports Excel]** dans la page **[!UICONTROL Rapports]**.

1. Cliquez sur le lien **[!UICONTROL Relevés de notes des élèves]**.

   La page d&#39;historique **[!UICONTROL Relevé de notes de l&#39;élève]** s&#39;affiche avec le message **Aucun relevé de notes de l&#39;élève n&#39;a encore été généré** ou une liste de téléchargements qui ont été déclenchés après l&#39;implémentation de la page d&#39;historique Relevés de notes de l&#39;élève.

   <!--[](assets/learner-transcripts.png)-->

   Une boîte de dialogue concernant les relevés de notes des stagiaires s&#39;affiche. Sélectionnez la plage de dates pour laquelle vous souhaitez générer le relevé de notes.

   >[!NOTE]
   >
   >Par défaut, la date de début est la date d&#39;inscription de l&#39;élève et la date de fin est toujours la date du jour. Vous pouvez modifier la date de départ uniquement à partir du moment où vous avez besoin des données.

1. Choisissez les noms des élèves dans le champ **[!UICONTROL Sélectionner des élèves]**, puis cliquez sur **[!UICONTROL Générer].**
1. Vous pouvez sélectionner un élève ou un groupe d’élèves. Cliquez **[!UICONTROL Ajouter des élèves]** pour en ajouter davantage.

   ![](assets/add-learners-lt.png)

   *Ajouter d’autres élèves*

1. Vous pouvez choisir des catalogues spécifiques en activant la case à cocher. Le relevé de notes est uniquement téléchargé pour les catalogues spécifiés. Vous pouvez choisir des catalogues spécifiques en sélectionnant le catalogue dans la liste déroulante **[!UICONTROL Sélectionner des catalogues]**.

   ![](assets/select-catalogs-lt.png)

1. Lors de l&#39;exportation des relevés de notes des élèves, il existe une option, **[!UICONTROL État d&#39;inscription]**. Cette liste déroulante contient les options suivantes :

   * Tout sélectionner
   * Terminé
   * En cours
   * Non démarré
   * Non inscrit

   ![](assets/add-enrollment-status-lt.png)

   *Sélectionner le catalogue*

1. Vous pouvez également télécharger des relevés de notes pour les élèves qui ont été supprimés d’un compte.

   Pour télécharger les relevés de notes des élèves supprimés, cliquez sur la flèche **[!UICONTROL Options avancées]** et activez la case à cocher **[!UICONTROL Inclure les données des élèves supprimés]**.

   ![](assets/data-deleted-learners.png)

   *Télécharger les relevés de notes des élèves supprimés*

1. Vous pouvez choisir de télécharger les informations au niveau du module dans le relevé de notes de l&#39;élève en activant la case à cocher « **[!UICONTROL Activer les informations au niveau du module]** ». Dans ce cas, les noms des modules et le temps passé sur chaque module sont récupérés dans le cadre du relevé de notes si cette option est activée.
1. Vous pouvez choisir de télécharger les données de compétences et les fiches récapitulatives en activant la case à cocher « **[!UICONTROL Inclure les données de compétences et les fiches récapitulatives]** ».

   Les transcriptions sont générées et téléchargées sur votre ordinateur sous forme de fichiers .zip lorsque les données de compétences ne sont pas incluses. Si la case Données de compétences est sélectionnée, les relevés de notes sont générés et téléchargés sous forme de fichiers .xls.

## Générer le relevé de notes de l’élève à l’aide du copier-coller

La récupération des relevés de notes de l’élève devient un processus fastidieux, car il ne peut être obtenu que pour un seul élève ou un seul groupe d’utilisateurs à la fois. Ici, avec la fonction copier-coller, vous pouvez copier la liste des identifiants de messagerie des élèves et la coller en une seule fois.

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur]** ou **[!UICONTROL responsable]**.
1. Accédez à **[!UICONTROL Rapports]** sous **[!UICONTROL Gérer]**. La page **[!UICONTROL Activité de l&#39;utilisateur]** est chargée.
1. Cliquez sur **[!UICONTROL Rapports personnalisés]** dans le volet de gauche et sélectionnez **[!UICONTROL Relevés de notes des élèves]** dans la liste.
1. Sur la page **[!UICONTROL Relevés de notes des élèves]**, cliquez sur le bouton **[!UICONTROL Générer]** dans le coin supérieur gauche.
1. Sélectionnez les dates préférées en cliquant dans la liste déroulante **[!UICONTROL Sélectionner une plage de dates]**. Cliquez sur l&#39;onglet **[!UICONTROL ID de messagerie]** pour entrer la liste copiée des ID de messagerie uniques.

   ![](assets/cp-copy-paste-feature.png)

   *Copier-coller des ID de messagerie*

1. Utilisez **[!UICONTROL Valider les ID de messagerie]** pour vérifier si l&#39;ID saisi est correct.

   ![](assets/cp-learnertran-gdpr.png)

   *Valider les ID de messagerie*

   Si l’ID de messagerie saisi est incorrect, il est mis en surbrillance en rouge avec un message de validation comme ci-dessus.

   Le bouton **[!UICONTROL Générer]** ne sera pas disponible à moins que tous les ID de messagerie saisis ne soient corrects.

   ![](assets/cp-copy-paste-generate.png)

   *Générer les relevés de notes des élèves*

1. Cliquez sur le bouton **[!UICONTROL Générer]** pour générer les relevés de notes des élèves pour tous les ID de messagerie mentionnés. Vous recevrez un message de confirmation comme ci-dessous indiquant la génération du rapport.

   ![](assets/cp-copy-paste-gmessage.png)

   *Message de confirmation du rapport en cours de génération*

   La génération des relevés de notes des élèves peut être combinée pour les ID de messagerie saisis sous les onglets **[!UICONTROL Utilisateurs]** et **[!UICONTROL ID de messagerie]**.

## Historique des téléchargements des relevés de notes des élèves {#ltdownload}

Sur la page de téléchargement **[!UICONTROL Relevé de notes de l&#39;élève]**, pour générer un rapport, lorsque vous cliquez sur le bouton **[!UICONTROL Générer]**, la boîte de dialogue Relevés de notes de l&#39;élève s&#39;affiche.

![](assets/history-lt.png)

*Générer un rapport de tous les relevés de notes des élèves*

Cliquez sur **[!UICONTROL Options avancées]** et développez le panneau.

Choisissez les utilisateurs et le catalogue auquel ils appartiennent. Après avoir cliqué sur le bouton **[!UICONTROL Générer]**, une boîte de dialogue indiquant le temps de téléchargement approximatif du rapport s’affiche. Pour générer le rapport, cliquez sur **[!UICONTROL Générer]**.

![](assets/download-learnertranscripts.png)

*Sélectionnez le bouton Générer*

Le relevé est généré en arrière-plan et vous pouvez poursuivre vos tâches dans Learning Manager. Une fois le relevé généré, vous pouvez le télécharger dans la liste.

En tant qu’administrateur, vous pouvez afficher toutes les transcriptions générées par n’importe qui dans le système.

![](assets/download-history.png)

*Afficher l&#39;historique des téléchargements*

La liste de téléchargements affiche les attributs suivants :

* **Élèves :** les élèves/groupes d&#39;élèves dont les relevés de notes doivent être téléchargés.
* **Données supplémentaires incluses :** dépend des données supplémentaires que l’administrateur souhaite télécharger depuis l’option Avancé dans le module Ajouter un relevé de notes de l’élève.
* **État :** téléchargé, en file d&#39;attente ou en cours.
* **De** et **À** : durée des relevés à télécharger.
* **Filtres appliqués :** spécifie si vous avez appliqué les filtres pour le statut de l&#39;inscription.
* **Généré par :** l’ID utilisateur de l’utilisateur Learning Manager qui a demandé le téléchargement.
* **État :** téléchargé, en file d&#39;attente ou en cours.

Vous pouvez annuler le téléchargement à tout moment. Si une tâche est annulée par l’administrateur, Learning Manager envoie une notification dans l’application à l’utilisateur qui a déclenché le relevé de notes de l’élève.

![](assets/queued-status.png)

*File d’attente de téléchargement du relevé de notes de l’élève*

Vous pouvez **annuler** le téléchargement à tout moment. Si une tâche est annulée, Learning Manager envoie une notification dans l’application à l’utilisateur qui a annulé la tâche.

## Données des élèves supprimés {#dataofdeletedlearners}

Vous pouvez inclure les données des élèves supprimés dans la liste des relevés de notes des élèves. Dans la boîte de dialogue Relevés de notes des élèves, activez l&#39;option **[!UICONTROL Inclure les données des élèves supprimés]**.

Après avoir activé l’option et cliqué sur **[!UICONTROL Générer]**, les données des élèves supprimés apparaissent dans la page de téléchargement des relevés de notes des élèves, comme illustré ci-dessous :

![](assets/deleted-learnersondownloadpage.png)

*Afficher les données des élèves supprimés*

## Personnalisation des colonnes {#customize-columns-lt}

Un administrateur peut personnaliser les colonnes exportées dans un rapport de relevé de notes de l’élève. Les administrateurs, les administrateurs personnalisés et les responsables peuvent configurer les colonnes avant d’exporter le rapport.

Dans la boîte de dialogue **[!UICONTROL Relevés de notes des élèves]**, cliquez sur **[!UICONTROL Options avancées]**. Dans la section **[!UICONTROL Configurer le format d&#39;exportation]**, choisissez les colonnes que vous souhaitez exporter.

![](assets/image024.png)

*Personnaliser les colonnes à exporter*

La personnalisation n’est autorisée que lorsqu’un utilisateur télécharge le relevé de notes de l’élève au format .CSV. Si le relevé est téléchargé au format .XLSX, la sélection des préférences de colonne ne sera pas respectée, et toutes les colonnes par défaut seront exportées.

## Contenu du fichier Relevé de notes des élèves {#learnertranscriptfilecontent}

Un fichier typique de relevé de notes de l’élève se compose de six feuilles Excel dans un seul fichier. Les feuilles de relevé de notes de l&#39;élève donnent un aperçu global des données, y compris le nombre d&#39;élèves impliqués par cours, leurs compétences, le pourcentage d&#39;achèvement en fonction du cours ou de l&#39;élève et un tableau de bord de conformité. Les tableaux de bord suivants sont disponibles dans les relevés de notes des élèves :

**Relevé de notes de l’élève**

Dans la feuille Excel du relevé de notes de l’élève se trouvent des détails d’utilisation des objets d’apprentissage, comme sa date d’inscription, sa date de début, sa note obtenue et son score au quiz, en plus des informations relatives au profil de l’élève. Si les cours font partie d’un programme d’apprentissage, ils sont répertoriés séparément des détails de consommation des cours individuels.

**1- Tableau de bord Activité d’apprentissage**

Dans ce tableau de bord spécifique aux objets d’apprentissage, vous pouvez afficher le nombre d’élèves inscrits à chaque cours, programme d’apprentissage ou certification. Vous pouvez afficher la fiche de progression des élèves suivant un objet d’apprentissage en particulier. Cette fiche présente des données telles que le nombre d’élèves ayant terminé le cours ou le programme d’apprentissage, les élèves en cours d’apprentissage et les échéances des élèves.

La progression des utilisateurs pour le cours en question est calculée en fonction des champs de saisie dans lesquels vous spécifiez la date d’échéance et les seuils de pourcentage de progression. Par exemple, si vous spécifiez 7 jours et 70 % en tant que valeurs dans le champ de saisie, la progression s’affiche pour les cours dont la date d’échéance est dans 7 jours et ceux dont la progression est supérieure à 70%. Vous pouvez également modifier la période dans cette feuille. Les données modifiées s’affichent automatiquement dans ce tableau de bord.

**2- Tableau de bord Activité d’apprentissage**

Ce tableau de bord d’apprentissage affiche les données d’un utilisateur en particulier. Il vous permet de voir les cours, programmes d’apprentissage ou certifications auxquels s’est inscrit un utilisateur spécifique. Le tableau affiche également des données sur les objets d’apprentissage que cet utilisateur a terminés, les objets d’apprentissage en cours et les échéances à venir pour cet utilisateur.

La progression des utilisateurs pour chaque cours est calculée en fonction des informations saisies, à savoir les valeurs de date d’échéance et de pourcentage de progression. Par exemple, si vous spécifiez 7 jours et 70 % en tant que valeurs dans le champ de saisie, la progression de l’utilisateur s’affiche pour les cours dont la date d’échéance est dans 7 jours et ceux dont la progression est supérieure à 70%.

**Compétence**

La feuille Compétences indique le nom des compétences, leur niveau, les crédits requis et acquis, le pourcentage d’achèvement et d’autres informations de profil. Un exemple de capture d’écran de la feuille Excel des compétences est fourni ci-dessous pour référence.

![](assets/skills-learner-transcript.png)

*Exemple de feuille Excel de compétences*

**1- Tableau de bord Compétence**

Dans ce tableau de bord, vous pouvez vérifier si votre entreprise dispose de diverses compétences. Vous pouvez comparer le nombre d’utilisateurs dans une entreprise qui sont censés posséder une compétence spécifique par rapport au nombre d’utilisateurs qui la possèdent réellement. Ce tableau de bord indique également les utilisateurs qui doivent actualiser leurs compétences. Cette valeur est calculée en fonction des informations que vous saisissez dans le champ de saisie. Par exemple, si vous entrez 50 jours, le tableau de bord vous permet d’accéder aux informations sur les utilisateurs qui doivent actualiser leurs compétences dans 50 jours.

**2- Tableau de bord Compétence**

Ce tableau de bord des compétences est davantage axé sur l’utilisateur. Il permet de filtrer un utilisateur spécifique ou plusieurs utilisateurs et de voir leur niveau de compétence sous forme de tableau de bord. Cette fiche peut aider les responsables et les administrateurs à suivre les compétences effectives de chaque élève par rapport aux compétences attendues de celui-ci. Le tableau de bord Compétence permet également de savoir quels élèves ont besoin de se perfectionner. La liste d’actualisation des compétences des élèves est calculée en fonction du nombre de jours que vous entrez dans le champ de saisie.

**Tableau de bord Conformité**

Ce tableau de bord se compose de deux parties : un rapport de conformité par utilisateur et un rapport de conformité par formation. Pour le rapport basé sur l’utilisateur, vous pouvez utiliser le tableau de bord Conformité pour suivre les utilisateurs ayant des échéances proches pour des initiatives de conformité importantes. Pour le rapport basé sur la formation, vous pouvez filtrer par programme d’apprentissage ou par certification.

Pour ces deux rapports de conformité, filtrez par échéance pour afficher les données adéquates.

### Colonnes d’heure et de date dans le relevé de notes {#datetime}

Pour les valeurs des colonnes suivantes, les minutes sont arrondies à la minute la plus proche et les secondes à 00 :

* Date d’inscription (fuseau horaire UTC)
* Date de début (fuseau horaire UTC)
* Date d’achèvement (fuseau horaire UTC)

![](assets/time-columns-in-thetranscript.png)

*Colonnes d&#39;heure et de date sur la feuille Excel*

### Colonnes de durée et d’ID du module dans le relevé de notes {#moduledurationandidcolumnsinthetranscript}

Le relevé de notes de l&#39;élève affiche également les colonnes **[!UICONTROL Durée du module]** et **[!UICONTROL ID]**.

![](assets/lt-id-duration.png)

*Colonnes de durée et d’ID de module dans le relevé de notes*

### AUTRES colonnes dans le relevé {#ModuledurationandIDcolumnsinthetranscript-1}

| **Colonne** | **Description** |
|---|---|
| Après | Nombre d’élèves qui ont acquis la compétence avant le nombre (valeur) de jours saisi qui doivent être actualisés |
| Compétence | Noms des compétences attribuées aux élèves |
| Nom du responsable | Nom du responsable dont les données d’engagement des compétences des subordonnés doivent être affichées dans le tableau de résumé des compétences |
| Libellés de ligne | Nom de l’élève avec la liste des compétences assingées |
| Nombre de compétences que chaque utilisateur doit posséder | Nombre de compétences assignées à l’élève |
| Nombre de compétences dont dispose chaque utilisateur | Nombre de compétences acquises par l’élève |
| Nombre de compétences nécessitant une actualisation | Nombre d’élèves dont la compétence doit être actualisée |
| Pourcentage de conformité | Pourcentage de progression de la compétence assignée |
| Chemin incorporé | Ces lignes affichent le nom du programme d’apprentissage intégré. |
| ID du parcours intégré | Ces lignes affichent les ID du programme d’apprentissage intégré |
| Langue du chemin incorporé | Ces lignes affichent la langue dans laquelle le programme d’apprentissage a été créé. |
