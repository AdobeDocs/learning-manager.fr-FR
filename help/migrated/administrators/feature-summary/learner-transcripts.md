---
description: Télécharger le relevé de notes de l’élève et gérer les rapports à l’aide de Learning Manager.
jcr-language: en_us
title: Relevés de notes des élèves
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1910'
ht-degree: 0%

---



# Relevés de notes des élèves

Télécharger le relevé de notes de l’élève et gérer les rapports à l’aide de Learning Manager.

Adobe Learning Manager permet aux administrateurs d’une organisation de générer des relevés de notes associés aux élèves.

## Générer les relevés de notes des élèves {#generatelearnertranscripts}

1. Pour générer les relevés de notes des élèves, cliquez sur **[!UICONTROL Rapports]** dans le volet gauche de la connexion Administrateur.

   L’administrateur accède à l’onglet Rapports Excel dans le panneau **[!UICONTROL Rapports]** page.

1. Cliquez sur le lien **[!UICONTROL Relevés de notes des élèves]**.

   Le **[!UICONTROL Relevé de notes de l’élève]** la page historique s’affiche avec le message suivant : **Aucun relevé de notes des élèves n&#39;a encore été généré** ou une liste des téléchargements qui ont été déclenchés après l’implémentation de la page d’historique des relevés de notes d’apprentissage.

   <!--[](assets/learner-transcripts.png)-->

   Une boîte de dialogue Relevés de notes des élèves s’affiche. Choisissez la période pour laquelle vous souhaitez que le relevé de notes soit généré.

   >[!NOTE]
   >
   >Par défaut, la date de début est la date d&#39;inscription de l&#39;élève et la date de fin est toujours la date du jour. Vous ne pouvez modifier que la date de début à partir de laquelle vous avez besoin des données.

1. Choisissez les noms des élèves dans le menu **[!UICONTROL Sélectionner des élèves]** et cliquez sur **[!UICONTROL Générer].**
1. Vous pouvez choisir un seul élève ou des groupes d’élèves. Pour ajouter plusieurs élèves, cliquez sur **[!UICONTROL Ajouter plus d’élèves]**.

   ![](assets/add-learners-lt.png)

   *Ajouter d’autres élèves*

1. Vous pouvez choisir des catalogues spécifiques en activant la case à cocher. La transcription est téléchargée uniquement pour les catalogues spécifiés. Vous pouvez choisir des catalogues spécifiques en sélectionnant le catalogue dans le menu **[!UICONTROL Sélectionner des catalogues]** liste déroulante.

   ![](assets/select-catalogs-lt.png)

1. Lors de l’exportation des relevés de notes des élèves, une option est disponible : **[!UICONTROL Statut d’inscription]**. Cette liste déroulante contient les options suivantes :

   * Tout sélectionner
   * Terminé
   * En cours
   * Non commencé
   * Non inscrit

   ![](assets/add-enrollment-status-lt.png)

   *Sélectionner le catalogue*

1. Vous pouvez également télécharger des relevés de notes pour les élèves qui ont été supprimés d’un compte.

   Pour télécharger les relevés de notes des élèves des utilisateurs supprimés, cliquez sur le bouton **[!UICONTROL Options avancées]** et activez la case à cocher **[!UICONTROL Inclure les données des élèves supprimés]**.

   ![](assets/data-deleted-learners.png)

   *Télécharger les relevés de notes des élèves supprimés*

1. Vous pouvez choisir de télécharger les informations de niveau module dans le relevé de notes de l’élève en activant le paramètre **[!UICONTROL Activer les informations au niveau du module]** case à cocher. Dans ce cas, les noms des modules et le temps passé sur chaque module sont récupérés dans le cadre du relevé de notes si cette option est activée.
1. Vous pouvez choisir de télécharger les données de compétences et les fiches récapitulatives en activant l’option «**[!UICONTROL Inclure les données sur les compétences et les fiches récapitulatives]** case à cocher.

   Les transcriptions sont générées et téléchargées sur votre ordinateur sous forme de fichiers .csv lorsque les données de compétences ne sont pas incluses. Si la case à cocher Données de compétences est activée, des transcriptions sont générées et téléchargées sur les fichiers .xls.

## Générer le relevé de notes de l’élève en utilisant le copier-coller

La récupération des relevés de notes des élèves devient un processus fastidieux, car il ne peut être obtenu que pour un seul élève ou groupe d’utilisateurs à la fois. Ici, avec la fonctionnalité copier-coller, vous pouvez copier la liste des ID de messagerie des élèves et la coller en une seule fois.

1. Connectez-vous en tant que **[!UICONTROL Administrateur]** ou **[!UICONTROL Responsable]**.
1. Accéder à **[!UICONTROL Rapports]** en dessous de **[!UICONTROL Gérer]**, il charge le fichier **[!UICONTROL Activité de l’utilisateur]** page.
1. Cliquez sur **[!UICONTROL Rapports personnalisés]** dans le volet de gauche et sélectionnez **[!UICONTROL Relevés de notes des élèves]** dans la liste.
1. Sur la **[!UICONTROL Relevés de notes des élèves]** page, cliquez sur **[!UICONTROL Nouveau]** dans le coin supérieur gauche.
1. Sélectionner les dates préférées en cliquant sur à partir de **[!UICONTROL Sélectionner une plage de dates]** liste déroulante. Cliquez sur **[!UICONTROL ID de messagerie]** pour saisir la liste copiée des identifiants de messagerie uniques.

   ![](assets/cp-copy-paste-feature.png)

   *Copier-coller d’ID de messagerie*

1. Utilisation **[!UICONTROL Valider les ID de messagerie]** pour vérifier si l’id saisi est correct.

   ![](assets/cp-learnertran-gdpr.png)

   *Valider les ID de messagerie*

   Si l’ID de messagerie saisi est incorrect, il est mis en surbrillance en rouge avec un message de validation comme ci-dessus.

   **[!UICONTROL Générer]** Le bouton n’est disponible que si tous les ID de messagerie saisis sont corrects.

   ![](assets/cp-copy-paste-generate.png)

   *Générer les relevés de notes des élèves*

1. Cliquez sur **[!UICONTROL Générer]** pour générer les relevés de notes des élèves pour tous les ID de messagerie mentionnés. Vous recevrez un message de confirmation comme ci-dessous indiquant la génération du rapport.

   ![](assets/cp-copy-paste-gmessage.png)

   *Message de confirmation du rapport généré*

   La génération des relevés de notes des élèves peut être combinée pour les ID de messagerie saisis sous les deux **[!UICONTROL Utilisateurs]** et **[!UICONTROL ID de messagerie]** onglet.

## Historique des téléchargements de relevés de notes des élèves {#ltdownload}

Sur la **[!UICONTROL Relevé de notes de l’élève]** page de téléchargement, pour générer un rapport, lorsque vous cliquez sur le bouton **[!UICONTROL Nouveau]** , la boîte de dialogue Relevés de notes des élèves s’affiche.

![](assets/history-lt.png)

*Générer un rapport de tous les relevés de notes des élèves*

Cliquez sur **[!UICONTROL Options avancées]** et développez le panneau.

Choisissez les utilisateurs et le catalogue auquel ils appartiennent. Après **[!UICONTROL Générer]** , une boîte de dialogue s’affiche mentionnant le temps approximatif qui sera nécessaire pour télécharger le rapport. Pour générer le rapport, cliquez sur **[!UICONTROL Générer]**.

![](assets/download-learnertranscripts.png)

*Cliquez sur le bouton Générer.*

La transcription est générée en arrière-plan et vous pouvez continuer à effectuer vos tâches dans Learning Manager. Une fois la transcription générée, vous pouvez la télécharger à partir de la liste.

En tant qu’administrateur, vous pouvez afficher toutes les transcriptions générées par n’importe qui dans le système.

![](assets/download-history.png)

*Affichage de l’historique des téléchargements*

La liste de téléchargement affiche les attributs suivants :

* **Élèves :** Les élèves/groupes d&#39;élèves dont les relevés de notes doivent être téléchargés.
* **Données supplémentaires incluses :** Dépend des données supplémentaires que l’administrateur souhaite télécharger à partir de l’option Avancé du modèle Ajouter le relevé de notes de l’élève
* **Statut :** Téléchargé, en attente ou en cours.
* **De** et **Pour**: durée des transcriptions à télécharger.
* **Filtres appliqués :** Si vous avez appliqué les filtres pour le statut d’inscription.
* **Généré par :** L’ID utilisateur de l’utilisateur Learning Manager qui a demandé le téléchargement.
* **Statut :** Téléchargé, en attente ou en cours.

Vous pouvez annuler le téléchargement à tout moment. Si une tâche est annulée par l’administrateur, Learning Manager envoie une notification dans l’application à l’utilisateur qui a déclenché le relevé de notes de l’élève.

![](assets/queued-status.png)

*File d’attente de téléchargement du relevé de notes de l’élève*

Vous pouvez **annuler** le téléchargement à tout moment. Si une tâche est annulée, Learning Manager envoie une notification dans l’application à l’utilisateur qui a annulé la tâche.

## Données des élèves supprimés {#dataofdeletedlearners}

Vous pouvez inclure les données des élèves supprimés dans la liste Relevé de notes de l’élève. Dans la boîte de dialogue Relevés de notes des élèves, activez l’option **[!UICONTROL Inclure les données des élèves supprimés]**.

Après avoir activé l’option et cliqué sur **[!UICONTROL Générer]**, les fonctionnalités de données des élèves supprimés dans la page de téléchargement du relevé de notes de l’élève, comme indiqué ci-dessous :

![](assets/deleted-learnersondownloadpage.png)

*Afficher les données des élèves supprimés*

## Personnalisation des colonnes {#customize-columns-lt}

Un administrateur peut personnaliser les colonnes exportées dans un rapport de relevé de notes de l’élève. Les administrateurs, les administrateurs personnalisés et les responsables peuvent configurer les colonnes avant d’exporter le rapport.

Sur la **[!UICONTROL Relevés de notes des élèves]** , cliquez sur **[!UICONTROL Options avancées]**. Dans le panneau **[!UICONTROL Configurer le format d’exportation]** , choisissez les colonnes à exporter.

![](assets/image024.png)

*Personnalisation des colonnes à exporter*

La personnalisation est autorisée uniquement lorsqu’un utilisateur télécharge le relevé de notes de l’élève au format .CSV. Lors du téléchargement au format .XLSX, la sélection des préférences de colonne ne sera pas respectée et toutes les colonnes par défaut seront exportées.

## Contenu du fichier de relevé de notes de l’élève {#learnertranscriptfilecontent}

Un fichier typique de relevé de notes d&#39;élève se compose de six feuilles Excel dans un seul fichier. Les feuilles de relevé de notes de l&#39;élève donnent un aperçu global des données, y compris le nombre d&#39;élèves impliqués par cours, leurs compétences, le pourcentage d&#39;achèvement en fonction du cours ou de l&#39;élève et un tableau de bord de conformité. Voici les tableaux de bord disponibles dans les relevés de notes des élèves :

**Relevé de notes de l’élève**

Dans la feuille Excel du relevé de notes de l&#39;élève, ainsi que les détails du profil de l&#39;élève, des détails sur la consommation des objets d&#39;apprentissage sont fournis, tels que la date d&#39;inscription, la date de début, le niveau atteint et le score du quiz obtenu. Si les cours font partie d’un programme d’apprentissage, ils sont répertoriés séparément des détails de consommation des cours individuels.

**1- Tableau de bord Activité d’apprentissage**

Dans ce tableau de bord spécifique à l’objet d’apprentissage, vous pouvez afficher le nombre d’élèves par cours, programme d’apprentissage ou certification. Vous pouvez afficher la feuille de progression pour les élèves d&#39;un objet d&#39;apprentissage particulier. Cette feuille affiche des données telles que le nombre d&#39;élèves ayant terminé le cours ou le programme d&#39;apprentissage, les élèves en cours et les dates d&#39;échéance des élèves.

La progression des utilisateurs pour le cours spécifique est calculée en fonction des champs de saisie dans lesquels vous spécifiez les seuils d&#39;échéance et de pourcentage de progression. Par exemple, si vous spécifiez 7 jours et 70 % comme valeurs dans votre champ de saisie, la progression du cours pour les cours dont la durée est de 7 jours et pour les cours dont la progression est supérieure à 70 % s&#39;affiche. Vous pouvez également modifier la période dans cette feuille, où les données modifiées s&#39;affichent automatiquement dans ce tableau de bord.

**2 - Tableau de bord Activité d’apprentissage**

Ce tableau de bord d&#39;apprentissage affiche les données d&#39;un utilisateur spécifique. À partir de ce tableau de bord, vous pouvez voir les cours, programmes d’apprentissage ou certifications auxquels un utilisateur particulier s’est inscrit. Le tableau affiche également des données sur les objets d’apprentissage terminés par l’utilisateur, les objets d’apprentissage en cours et les échéances à venir pour l’utilisateur.

La progression de l’utilisateur pour chaque cours est calculée en fonction des entrées que vous spécifiez. Autrement dit, les valeurs de date d&#39;échéance et de pourcentage d&#39;avancement. Par exemple, si vous spécifiez 7 jours et 70 % comme valeurs dans votre champ de saisie, la progression de l&#39;utilisateur pour les différents cours qui doivent être suivis dans 7 jours et pour les cours dont la progression est supérieure à 70 % s&#39;affiche.

**Compétence**

Dans la feuille des compétences, le nom de la compétence, le niveau de compétence, les crédits requis, les crédits acquis, le pourcentage d’achèvement et d’autres détails du profil sont fournis. Un exemple de feuille d&#39;excellence des compétences est fourni ci-dessous à titre de référence.

![](assets/skills-learner-transcript.png)

*Exemple de feuille Excel de compétences*

**1- Tableau de bord Compétence**

Dans ce tableau de bord, vous pouvez voir si votre organisation est équipée sur diverses compétences. Pour une compétence spécifique, vous pouvez vérifier le nombre d’utilisateurs d’une organisation qui sont censés avoir cette compétence par rapport au nombre d’utilisateurs qui ont réellement cette compétence. Ce tableau de bord spécifie également les utilisateurs qui doivent actualiser leurs compétences. Cette valeur est calculée en fonction de la saisie que vous saisissez dans le champ Saisie. Par exemple, si vous saisissez 50 jours, le tableau de bord fournit des données sur les utilisateurs dont les compétences doivent être actualisées après 50 jours.

**2- Tableau de bord Compétence**

Ce tableau de bord de compétences est plus spécifique à l’utilisateur. Vous pouvez filtrer un utilisateur spécifique ou plusieurs utilisateurs et afficher leur niveau de compétence sous forme de tableau de bord. Cette feuille peut aider les responsables et les administrateurs à suivre le niveau de compétence de chaque élève par rapport au niveau de compétence attendu. Le tableau de bord des compétences met également en lumière les élèves qui doivent actualiser leurs compétences. La liste d&#39;actualisation des élèves est calculée en fonction du nombre de jours que vous saisissez dans le champ de saisie.

**Tableau de bord Conformité**

Le tableau de bord de conformité se compose de deux parties : rapport de conformité par utilisateur et rapport de conformité par formation. Pour le rapport basé sur l’utilisateur, vous pouvez utiliser le tableau de bord Conformité pour suivre les utilisateurs qui ont des échéances à venir pour des initiatives de conformité importantes. Pour le rapport basé sur la formation, vous pouvez filtrer par programme d’apprentissage ou certification.

Pour les deux rapports de conformité, filtrez par date d&#39;échéance pour afficher les données appropriées.

### Colonnes d’heure et de date dans le relevé de notes {#datetime}

Les valeurs des colonnes suivantes ont des minutes arrondies à la minute la plus proche et des secondes à 00 :

* Date d’inscription (fuseau horaire UTC)
* Date de début (fuseau horaire UTC)
* Date d’achèvement (fuseau horaire UTC)

![](assets/time-columns-in-thetranscript.png)

*Colonnes d&#39;heure et de date de la feuille Excel*

### Colonnes de durée et d’ID du module dans le relevé de notes {#moduledurationandidcolumnsinthetranscript}

Le relevé de notes de l’élève affiche également les colonnes - **[!UICONTROL Durée du module]** et **[!UICONTROL ID]**.

![](assets/lt-id-duration.png)

*Colonnes de durée et d’ID du module dans le relevé de notes*

### AUTRES colonnes du relevé de notes {#ModuledurationandIDcolumnsinthetranscript-1}

| **Colonne** | **Description** |
|---|---|
| Après | Nombre d’élèves qui ont acquis la compétence avant le nombre (valeur) de jours saisi qui doit être actualisé |
| Compétence | Noms des compétences attribuées aux élèves |
| Nom du responsable | Nom du responsable dont les données d’engagement des compétences des subordonnés doivent être affichées dans le tableau de résumé des compétences |
| Libellés de ligne | Nom de l’élève avec la liste des compétences attribuées |
| Nombre de compétences que chaque utilisateur doit posséder | Nombre de compétences attribuées à l’élève |
| Nombre de compétences dont dispose chaque utilisateur | Nombre de compétences acquises par l’élève |
| Nombre de compétences nécessitant une actualisation | Nombre d’élèves dont la compétence doit être actualisée |
| Pourcentage de conformité | Pourcentage de progression de la compétence assignée |
| Chemin incorporé | Ces lignes affichent le nom du programme d’apprentissage intégré. |
| ID du chemin incorporé | Ces lignes affichent les ID du programme d’apprentissage intégré |
| Langue du chemin incorporé | Ces lignes affichent la langue dans laquelle le programme d’apprentissage a été créé. |
