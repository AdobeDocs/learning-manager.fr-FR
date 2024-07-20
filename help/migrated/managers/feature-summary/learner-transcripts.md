---
description: Découvrez comment télécharger le relevé de notes d’un élève en fonction des utilisateurs, des objets d’apprentissage ou des compétences dans Learning Manager.
jcr-language: en_us
title: Relevés de notes de l'élève
exl-id: 8204aa1e-0e0d-4d9e-9dc0-6260667bf4e7
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 85%

---

# Relevés de notes de l&#39;élève

Découvrez comment télécharger le relevé de notes d’un élève en fonction des utilisateurs, des objets d’apprentissage ou des compétences dans Learning Manager.

Adobe Learning Manager permet aux responsables d&#39;une organisation de générer des récapitulatifs liés aux élèves.

## Générer les relevés de notes des élèves {#generatelearnertranscripts}

1. Pour générer les relevés de notes des élèves, cliquez sur **[!UICONTROL Rapports]** dans le volet gauche de la connexion au responsable.
1. Cliquez sur l&#39;onglet **[!UICONTROL Mes rapports]** sur la page.
1. Cliquez sur le lien **[!UICONTROL Relevés de notes des élèves]**.

   ![](assets/learner-transcripts.png)

   *Créer des rapports pour les relevés de notes des élèves*

1. Une boîte de dialogue concernant les relevés de notes des stagiaires s&#39;affiche. Sélectionnez la plage de dates pour laquelle vous souhaitez générer le relevé de notes.

   >[!NOTE]
   >
   >Par défaut, la date de début est la date d&#39;inscription de l&#39;élève et la date de fin est toujours la date du jour. Vous pouvez modifier la date de départ uniquement à partir du moment où vous avez besoin des données.

1. Choisissez les noms des élèves dans le champ Sélectionner les élèves, puis cliquez sur **[!UICONTROL Générer]**.

Vous pouvez sélectionner un élève ou un groupe d’élèves. Cliquez Ajouter des élèves pour en ajouter davantage.

Les relevés de notes sont générés et téléchargés sur votre ordinateur en tant que fichiers .xls standard. Chaque fichier .xls excel comporte sept feuilles, dont les détails sont mentionnés ci-dessous :

## Télécharger le relevé de notes de l’élève en fonction du fuseau horaire {#lt-timezone}

Comme un administrateur, un responsable peut également choisir les colonnes à exporter. En outre, un responsable peut télécharger le relevé de notes de l’élève en fonction du fuseau horaire qu’il a sélectionné dans les paramètres du profil.

Si le responsable active cette option, le fuseau horaire est sélectionné à partir de celui défini dans la page des paramètres du profil, comme indiqué ci-dessous.

>[!NOTE]
>
>Pour un nouveau responsable, la case à cocher Fuseau horaire est désactivée.

![](assets/image030.png)

*Télécharger les relevés de notes des élèves pour un fuseau horaire*

## Contenu du fichier Relevé de notes des élèves {#learnertranscriptfilecontent}

Un fichier typique de relevé de notes de l’élève se compose de six feuilles Excel dans un seul fichier. Les feuilles du relevé de notes de l’élève offrent un aperçu général des données, notamment le nombre d’élèves inscrits dans chaque cours, leurs compétences, leur pourcentage d’achèvement par cours ou par élève et un tableau de bord de conformité. Les tableaux de bord suivants sont disponibles dans les relevés de notes des élèves :

**Relevé de notes de l’élève**

Dans la feuille Excel du relevé de notes de l’élève se trouvent des détails d’utilisation des objets d’apprentissage, comme sa date d’inscription, sa date de début, sa note obtenue, son score au quiz etc., en plus des informations relatives au profil de l’élève. Si des cours font partie d’un programme d’apprentissage, ils sont répertoriés séparément des détails de suivi des cours individuels.

**1- Tableau de bord Activité d’apprentissage**

Dans ce tableau de bord spécifique aux objets d’apprentissage, vous pouvez afficher le nombre d’élèves inscrits à chaque cours, programme d’apprentissage ou certification. Vous pouvez afficher la fiche de progression des élèves suivant un objet d’apprentissage en particulier. Cette fiche présente des données telles que le nombre d’élèves ayant terminé le cours ou le programme d’apprentissage, les élèves en cours d’apprentissage et les échéances des élèves.

La progression des utilisateurs pour le cours en question est calculée en fonction des champs de saisie dans lesquels vous spécifiez la date d’échéance et les seuils de pourcentage de progression. Par exemple, si vous spécifiez 7 jours et 70 % en tant que valeurs dans le champ de saisie, la progression s’affiche pour les cours dont la date d’échéance est dans 7 jours et ceux dont la progression est supérieure à 70%. Vous pouvez également modifier la période dans cette feuille. Les données modifiées s’affichent automatiquement dans ce tableau de bord.

**2- Tableau de bord Activité d’apprentissage**

Ce tableau de bord d’apprentissage affiche les données d’un utilisateur en particulier. Il vous permet de voir les cours, programmes d’apprentissage ou certifications auxquels s’est inscrit un utilisateur spécifique. Le tableau affiche également des données sur les objets d’apprentissage que cet utilisateur a terminés, les objets d’apprentissage en cours et les échéances à venir pour cet utilisateur.

La progression des utilisateurs pour chaque cours est calculée en fonction des informations saisies, à savoir les valeurs de date d’échéance et de pourcentage de progression. Par exemple, si vous spécifiez 7 jours et 70 % en tant que valeurs dans le champ de saisie, la progression de l’utilisateur s’affiche pour les cours dont la date d’échéance est dans 7 jours et ceux dont la progression est supérieure à 70%.

**Compétence**

La feuille Compétences indique le nom des compétences, leur niveau, les crédits requis et acquis, le pourcentage d’achèvement et d’autres informations de profil. Un exemple de capture d’écran de la feuille Excel des compétences est fourni ci-dessous pour référence.

**Tableau de bord Compétence**

Dans ce tableau de bord, vous pouvez vérifier si votre entreprise dispose de diverses compétences. Vous pouvez comparer le nombre d’utilisateurs dans une entreprise qui sont censés posséder une compétence spécifique par rapport au nombre d’utilisateurs qui la possèdent réellement. Ce tableau de bord indique également les utilisateurs qui peuvent avoir besoin d’actualiser leurs compétences. Cette valeur est calculée en fonction des informations que vous saisissez dans le champ de saisie. Par exemple, si vous entrez 50 jours, le tableau de bord vous permet d’accéder aux informations sur les utilisateurs qui peuvent avoir besoin d’actualiser leurs compétences dans 50 jours.

Ce tableau de bord des compétences est davantage axé sur l’utilisateur. Il permet de filtrer un utilisateur spécifique ou plusieurs utilisateurs et de voir leur niveau de compétence sous forme de tableau de bord. Cette fiche peut aider les responsables et les administrateurs à suivre les compétences effectives de chaque élève par rapport aux compétences attendues de celui-ci. Le tableau de bord Compétence permet également de savoir quels élèves ont besoin de se perfectionner. La liste d’actualisation des compétences des élèves est calculée en fonction du nombre de jours que vous entrez dans le champ de saisie.

**Tableau de bord Conformité**

Ce tableau de bord se compose de deux parties : un rapport de conformité par utilisateur et un rapport de conformité par formation. Pour le rapport basé sur l’utilisateur, vous pouvez utiliser le tableau de bord Conformité pour suivre les utilisateurs ayant des échéances proches pour des initiatives de conformité importantes. Pour le rapport basé sur la formation, vous pouvez filtrer par programme d’apprentissage ou par certification.

Pour ces deux rapports de conformité, filtrez par échéance pour afficher les données adéquates.
