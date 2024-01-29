---
description: Découvrez comment télécharger le relevé de notes d’un élève en fonction des utilisateurs, des objets d’apprentissage ou des compétences dans Learning Manager.
jcr-language: en_us
title: Relevés de notes des élèves
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 0%

---



# Relevés de notes des élèves

Découvrez comment télécharger le relevé de notes d’un élève en fonction des utilisateurs, des objets d’apprentissage ou des compétences dans Learning Manager.

Adobe Learning Manager permet aux responsables d’une organisation de générer des relevés de notes associés aux élèves.

## Générer les relevés de notes des élèves {#generatelearnertranscripts}

1. Pour générer les relevés de notes des élèves, cliquez sur **[!UICONTROL Rapports]** dans le volet gauche de la connexion à Manager.
1. Cliquez sur **[!UICONTROL Mes rapports]** sur la page.
1. Cliquez sur **[!UICONTROL Relevés de notes des élèves]** lien.

   ![](assets/learner-transcripts.png)

   *Créer des rapports pour les relevés de notes des élèves*

1. Une boîte de dialogue Relevés de notes des élèves s’affiche. Choisissez la période pour laquelle vous souhaitez que le relevé de notes soit généré.

   >[!NOTE]
   >
   >Par défaut, la date de début est la date d&#39;inscription de l&#39;élève et la date de fin est toujours la date du jour. Vous ne pouvez modifier que la date de début à partir de laquelle vous avez besoin des données.

1. Choisissez les noms des élèves dans le champ Sélectionner des élèves, puis cliquez sur **[!UICONTROL Générer]**.

Vous pouvez choisir un seul élève ou des groupes d’élèves. Pour ajouter plusieurs élèves, cliquez sur Ajouter plus d’élèves.

Les transcriptions sont générées et téléchargées sur votre ordinateur sous forme de fichiers .xls. Chaque fichier .xls excel comporte sept feuilles, dont les détails sont mentionnés ci-dessous :

## Télécharger le relevé de notes de l’élève en fonction du fuseau horaire {#lt-timezone}

Comme un administrateur, un responsable peut également choisir les colonnes à exporter. En outre, un responsable peut télécharger le relevé de notes de l’élève en fonction du fuseau horaire qu’il a sélectionné dans les paramètres du profil.

Si le responsable active cette option, le fuseau horaire est sélectionné à partir de celui défini dans la page des paramètres du profil, comme indiqué ci-dessous.

>[!NOTE]
>
>Pour un nouveau responsable, la case à cocher Fuseau horaire est désactivée.

![](assets/image030.png)

*Télécharger les relevés de notes des élèves pour un fuseau horaire*

## Contenu du fichier Relevé de notes de l’élève {#learnertranscriptfilecontent}

Un fichier typique de relevé de notes d&#39;élève se compose de six feuilles Excel dans un seul fichier. Les feuilles de relevé de notes de l’élève donnent un aperçu global des données, y compris le nombre d’élèves impliqués par cours, leurs compétences, le pourcentage d’achèvement en fonction du cours ou de l’élève et un tableau de bord de conformité. Voici les tableaux de bord disponibles dans les relevés de notes des élèves :

**Relevé de notes de l’élève**

Dans la feuille Excel du relevé de notes de l&#39;élève, ainsi que les détails du profil de l&#39;élève, des détails sur la consommation des objets d&#39;apprentissage sont fournis, tels que la date d&#39;inscription, la date de début, le niveau atteint, le score du quiz obtenu, etc. Si les cours font partie d’un programme d’apprentissage, ils sont répertoriés séparément des détails de consommation des cours individuels.

**1 - Tableau de bord Activité d’apprentissage**

Dans ce tableau de bord spécifique à l’objet d’apprentissage, vous pouvez afficher le nombre d’élèves par cours, programme d’apprentissage ou certification. Vous pouvez afficher la feuille de progression pour les élèves d&#39;un objet d&#39;apprentissage particulier. Cette feuille affiche des données telles que le nombre d&#39;élèves ayant terminé le cours ou le programme d&#39;apprentissage, les élèves en cours et les dates d&#39;échéance des élèves.

La progression des utilisateurs pour le cours spécifique est calculée en fonction des champs de saisie dans lesquels vous spécifiez les seuils d&#39;échéance et de pourcentage de progression. Par exemple, si vous spécifiez 7 jours et 70 % comme valeurs dans votre champ de saisie, la progression du cours pour les cours dont la durée est de 7 jours et pour les cours dont la progression est supérieure à 70 % s&#39;affiche. Vous pouvez également modifier la période dans cette feuille, où les données modifiées s&#39;affichent automatiquement dans ce tableau de bord.

**2 - Tableau de bord Activité d’apprentissage**

Ce tableau de bord d&#39;apprentissage affiche les données d&#39;un utilisateur spécifique. À partir de ce tableau de bord, vous pouvez voir les cours, programmes d’apprentissage ou certifications auxquels un utilisateur particulier s’est inscrit. Le tableau affiche également des données sur les objets d’apprentissage terminés par l’utilisateur, les objets d’apprentissage en cours et les échéances à venir pour l’utilisateur.

La progression de l’utilisateur pour chaque cours est calculée en fonction des entrées que vous spécifiez. Autrement dit, les valeurs de date d&#39;échéance et de pourcentage d&#39;avancement. Par exemple, si vous spécifiez 7 jours et 70 % comme valeurs dans votre champ de saisie, la progression de l&#39;utilisateur pour les différents cours qui doivent être suivis dans 7 jours et pour les cours dont la progression est supérieure à 70 % s&#39;affiche.

**Compétence**

Dans la feuille de compétences, le nom de la compétence, le niveau de compétence, les crédits requis, les crédits acquis, le pourcentage d’achèvement et d’autres détails du profil sont fournis. Un exemple de feuille d&#39;excellence des compétences est fourni ci-dessous à titre de référence.

**Tableau de bord Compétence**

Dans ce tableau de bord, vous pouvez voir si votre organisation est équipée sur diverses compétences. Pour une compétence spécifique, vous pouvez vérifier le nombre d’utilisateurs d’une organisation qui sont censés avoir cette compétence par rapport au nombre qui ont réellement la compétence. Ce tableau de bord spécifie également les utilisateurs qui devront peut-être actualiser leurs compétences. Cette valeur est calculée en fonction de la saisie que vous saisissez dans le champ Saisie. Par exemple, si vous saisissez 50 jours, le tableau de bord fournit des données sur les utilisateurs qui peuvent avoir besoin d’actualiser leurs compétences après 50 jours.

Ce tableau de bord de compétences est plus spécifique à l’utilisateur. Vous pouvez filtrer un utilisateur spécifique ou plusieurs utilisateurs et afficher leur niveau de compétence sous forme de tableau de bord. Cette feuille peut aider les responsables et les administrateurs à suivre le niveau de compétence de chaque élève par rapport au niveau de compétence attendu. Le tableau de bord des compétences met également en lumière les élèves qui doivent actualiser leurs compétences. La liste d&#39;actualisation des élèves est calculée en fonction du nombre de jours que vous saisissez dans le champ de saisie.

**Tableau de bord Conformité**

Le tableau de bord de conformité se compose de deux parties : rapport de conformité par utilisateur et rapport de conformité par formation. Pour le rapport basé sur l’utilisateur, vous pouvez utiliser le tableau de bord Conformité pour suivre les utilisateurs qui ont des échéances à venir pour des initiatives de conformité importantes. Pour le rapport basé sur la formation, vous pouvez filtrer par programme d’apprentissage ou certification.

Pour les deux rapports de conformité, filtrez par date d&#39;échéance pour afficher les données appropriées.
