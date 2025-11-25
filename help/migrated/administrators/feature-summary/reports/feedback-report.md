---
description: Découvrez comment accéder au rapport de commentaires, le télécharger et l’interpréter dans Adobe Learning Manager. Comprendre les colonnes du rapport, les types de questions, les réponses du responsable et de l'élève, et comment les commentaires prennent en charge l'évaluation de la formation et l'amélioration continue.
jcr-language: en_us
title: Rapport de commentaires dans Adobe Learning Manager
source-git-commit: e0553621dd67338d2433bb1f82af43cacc2d8b8c
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 8%

---


# Rapport de commentaires

## Vue d’ensemble

Le rapport Retour d’informations dans Adobe Learning Manager collecte les niveaux 1 (Retour d’informations de l’élève) et 3 (Retour d’informations du responsable) une fois que les élèves ont terminé les objets d’apprentissage. Ce rapport présente un aperçu structuré des réponses subjectives et objectives des élèves et de leurs responsables.

Le rapport effectue le suivi des détails de l’élève tels que le nom, l’adresse e-mail, le nom du formulaire de retour d’informations, la version et la langue, et capture les réponses aux questions définies par l’administrateur. Elle enregistre également la sélection de l’élève pour chaque question (par exemple, Tout à fait d’accord, D’accord ou Pas d’accord).

## Objectif et avantages

* Fournit des informations exploitables pour améliorer la qualité du cours et l’efficacité globale de l’apprentissage.
* Affinez les méthodes de navigation, de stimulation et de livraison en fonction des commentaires directs des utilisateurs.

## Cas d’utilisation

* **Identifiez rapidement les problèmes de contenu** : les administrateurs peuvent détecter des évaluations faibles ou des commentaires négatifs répétés et mettre à jour les objets d’apprentissage sans attendre les tickets d’assistance ou les escalades.
* **Mesurer l&#39;efficacité de la formation** : les équipes peuvent comparer les retours d&#39;informations des élèves entre plusieurs cours ou versions pour comprendre quels objets d&#39;apprentissage sont performants et lesquels peuvent devoir être modifiés.
* **Suivre l&#39;engagement des élèves avec les formulaires de retour d&#39;informations** : les administrateurs peuvent voir combien d&#39;élèves répondent ou ignorent des questions, ce qui les aide à affiner les formulaires de retour d&#39;informations pour améliorer la qualité des réponses et les taux d&#39;achèvement.

## Comment télécharger le rapport de commentaires

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Rapports]** dans le menu de navigation de gauche.
   ![](assets/select-report.png)
   _La page d&#39;accueil de l&#39;administrateur affiche l&#39;option Rapports mise en évidence pour le téléchargement des rapports_

3. Sélectionnez **[!UICONTROL Rapports personnalisés]** dans Rapports, puis **[!UICONTROL Rapports Excel]**.
4. Sélectionnez **[!UICONTROL Rapport de commentaires]**.
   ![](assets/select-feedback-report.png)
   La section _Rapports personnalisés affiche l’option permettant de sélectionner Rapport de retour d’informations pour accéder aux données de retour d’informations des élèves et des responsables_

5. Sélectionnez **[!UICONTROL Toutes les formations]** ou **[!UICONTROL Formations sélectionnées]**, ainsi que la période. Si vous sélectionnez la deuxième option, vous pouvez ajouter jusqu’à 10 cours ou parcours d’apprentissage et générer leur rapport de retour d’informations. En outre, vous pouvez générer le rapport pour une durée maximale d’un an.
   ![](assets/feedback-report.png)
   _Configurez le rapport de retour d&#39;informations en sélectionnant l&#39;étendue de la formation, en définissant la période et en choisissant l&#39;option de traduction avant le téléchargement_

6. Sélectionnez la langue dans laquelle traduire le retour d&#39;informations L1. Les questions objectives et leurs réponses sont traduites dans la langue sélectionnée lorsque cette version linguistique est explicitement définie. Seules les questions subjectives explicitement définies dans la langue sélectionnée apparaissent dans le rapport.  Les réponses aux questions subjectives seront rédigées dans le langage de réponse d&#39;origine.
7. Sélectionnez **[!UICONTROL Télécharger]** pour télécharger le rapport.

## Que contient le rapport de commentaires ?

Voici les colonnes par défaut du rapport au niveau du compte :

| Colonne | Description |
|----|----|
| Type de retour d’informations | Indique si le retour d’informations provient de l’élève (L1) ou du responsable (L3) |
| Nom d’utilisateur | Nom de l’élève qui a suivi la formation |
| Courrier électronique de l’utilisateur | Adresse électronique de l’élève |
| ID de formation | Un identifiant unique généré par le système attribué à chaque objet d’apprentissage (cours, certification ou parcours d’apprentissage) |
| Nom de la formation | Nom de l’élément d’apprentissage pour lequel le retour d’informations est envoyé |
| Instance de formation | Nom de l’instance de la formation (pour les cours à instances multiples) |
| Type de formation | Type de formation (cours, certification, parcours d’apprentissage) |
| Type de formulaire de retour d’informations | Type/catégorie du formulaire de retour d’informations utilisé (par exemple, cours fusionnés, cours en auto-apprentissage et cours en salle de classe) |
| Nom du formulaire de retour d’informations | Nom du formulaire de retour d’informations |
| Version du retour d’informations | Numéro de version du formulaire de retour d’informations |
| Responsable actuel | Nom du responsable de l’élève |
| E-mail du responsable actuel | Adresse électronique du responsable de l’élève |
| Date de fin | Date à laquelle l’élève a terminé la formation |
| Date du retour d’informations | Date à laquelle l’élève a envoyé le retour d’informations |
| Langue d&#39;origine du retour d&#39;informations L1 | Langue dans laquelle l’élève a initialement soumis le retour d’informations L1 |
| Question 1 sur l&#39;échelle de Likert L3 | Mesure les performances de l’élève après la formation à l’aide d’une échelle de notation |
| Réponse de l’échelle de Likert L3 1 | Réponse du responsable à cette question à échelle de Likert |
| Question de texte libre L3 1 | Question en texte libre ajoutée au formulaire de retour d’informations L3 pour les responsables ; peut être configurée comme facultative ou obligatoire |
| Réponse de texte libre L3 1 | La réponse du responsable à cette question de texte libre |

Les colonnes suivantes apparaissent dans le rapport au niveau du compte en fonction des quatre types de questions ajoutées au formulaire de retour d’informations :

| Colonne | Description |
|---|---|
| Efficacité du cours | La question prédéfinie d’efficacité de cours affichée dans le formulaire |
| Réponse sur l’efficacité du cours | Réponse de l’élève à la question sur l’efficacité du cours |
| Question NPS 1 | Première question sur le Net Promoter Score |
| Plage NPS 1 | Échelle d’évaluation utilisée (par exemple, de 0 à 10) |
| Réponse NPS 1 | Évaluation de l’élève pour NPS Question 1 |
| Question Likert 1 | Première question à échelle de Likert |
| Réponse de Likert 1 | Réponse à la question 1 de Likert |
| Question textuelle 1 | Première question ouverte/de texte du formulaire |
| Réponse textuelle 1 | Réponse de l’élève à la question textuelle 1 |


>[!NOTE]
>
>Le rapport au niveau du compte inclut également tous les champs actifs configurés pour les élèves.

Les colonnes suivantes apparaissent dans le rapport au niveau de l’objet d’apprentissage :

| Colonne | Description |
|---|---|
| Gestion | Nom de l’élève |
| Courrier électronique | Adresse e-mail de l’élève |
| Nom du formulaire de retour d’informations | Nom du formulaire de retour d’informations |
| Version du retour d’informations | Numéro de version du formulaire de retour d’informations |
| Langue de l’élève | Langue sélectionnée par l’élève |

>[!NOTE]
>
>Le rapport de niveau Objet d’apprentissage inclut également les questions ajoutées au formulaire de retour d’informations. Chaque question s’affiche sous la forme d’un en-tête de colonne et les réponses de l’élève à ces questions sont affichées dans les lignes correspondantes ci-dessous.
