---
description: Tout sur le Gradebook du point de vue de l'élève
jcr-language: en_us
title: Classeur pour les élèves
source-git-commit: 0862e0d042fac74377b44c3387a72336ec625161
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---


# Classeur pour les élèves

## Commencer un cours avec un cahier de notes

Lorsque l&#39;annuaire de notes est activé et visible pour un cours dans Adobe Learning Manager, un onglet **Annuaire** apparaît sur la page de présentation du cours. Utilisez-le pour voir votre score pondéré pour chaque module, votre score global actuel et si vous avez réussi ou si vous devez encore terminer le cours.

![](assets/image_0008.png)

## Lorsque le classeur est disponible

L&#39;onglet **Carnet de notes** apparaît à côté des **modules**, des **notes** et des **discussions** dans le lecteur de cours lorsque votre auteur ou votre administrateur a activé la visibilité du carnet de notes pour le cours. Si l’onglet n’est pas visible, cela signifie que l’annuaire de notes n’a pas été activé pour ce cours ou que l’administrateur a désactivé la visibilité des élèves. Les scores peuvent toujours être enregistrés et visibles par votre administrateur.

Vous pouvez ouvrir l&#39;onglet **Gradebook** à tout moment pendant votre inscription :

![](assets/image_0009.png)

* **Avant de commencer :** après l&#39;inscription, la liste complète des modules pouvant être notés s&#39;affiche, avec leurs pourcentages de pondération, le nombre maximal de notes pour chacun et les critères de réussite définis par l&#39;auteur. Cela vous montre exactement comment le cours est noté avant de commencer.
* **En cours :** à mesure que vous terminez les modules et que les scores sont enregistrés, le journal de notation est mis à jour pour afficher vos scores jusqu&#39;à présent, aux côtés des modules qui n&#39;ont pas encore été tentés ou qui sont en attente de notation.
* **Après avoir terminé :** le cahier de notes affiche tous les scores du module final, le score total calculé du cours et un résultat **Réussi** dans l&#39;en-tête.

## Afficher le carnet de notes

* Dans **Mon apprentissage**, sélectionnez votre cours.
* Sélectionnez l&#39;onglet **Gradebook** dans la page du cours.

  L’en-tête du classeur indique :

  ![](assets/image_0010a.png)

* **Critères de réussite :** le score agrégé minimal et le nombre de modules requis
* Nombre de modules requis que vous avez terminés sur le total
* Votre **score total** actuel en pourcentage
* Statut actuel de votre cours : **Pas commencé**, **Achèvement en attente**, **Réussite** ou **Échec**

Le tableau de module sous l’en-tête affiche les colonnes suivantes pour chaque module :

| **Colonne** | **Ce qu&#39;il affiche** |
|------------|-------------------|
| **Module** | Nom et type du module |
| **Statut** | Votre statut d’achèvement ou de score pour ce module (voir référence du statut ci-dessous) |
| **Pondération** | Pourcentage de contribution de ce module à votre score global |
| **Score** | Votre score pour ce module (par exemple, 40/100) |
| **Contribution** | Le pourcentage de points réel que ce module a ajouté à votre score total jusqu&#39;à présent |

## Affichage du poids des modules à partir de l’onglet Modules

Vous pouvez également voir la pondération de chaque module à partir de l&#39;onglet **Modules** sans ouvrir le classeur.

Dans votre page de cours, sélectionnez l&#39;onglet **Modules**.

![](assets/image_0011.png)

L&#39;onglet **Modules** affiche le pourcentage de pondération pour chaque module et le nombre de modules requis pour terminer le cours.

## Scores de module avec plusieurs tentatives

Si un module autorise plusieurs tentatives, le score affiché dans votre classeur dépend de la façon dont l&#39;auteur du cours l&#39;a configuré :

* **Meilleur score :** Le meilleur score de toute tentative est affiché. Un score plus faible lors d’une tentative ultérieure ne réduit pas votre score enregistré.
* **Dernière :** le score de votre tentative la plus récente est toujours affiché. Un score plus faible lors d’une tentative ultérieure remplace le score précédent.

## Comprendre l’état de votre module

Chaque module du classeur affiche l’un des statuts suivants :

![](assets/image_0012.png)

| **Statut** | **Signification** |
|------------|-------------------|
| **Terminé** | Module terminé et score enregistré |
| **En cours** | Module démarré mais pas encore terminé |
| **Non démarré** | Module non encore ouvert |
| **Échec** | Le module a obtenu un score qui n’a pas atteint le seuil de réussite du module |
| **Révision en attente** | Module terminé mais en attente d’un score de la part d’un instructeur ou d’un administrateur |
| **Pas de pondération** | Le type de module ne prend pas en charge l&#39;évaluation (PDF, vidéo et similaire) ; ne contribue pas à l&#39;agrégation |

## Mode de calcul du score total

Votre score global est la somme de la contribution pondérée de chaque module noté :

(Score obtenu ÷ Score maximum) × % de pondération = Contribution du module

La colonne **Contribution** du classeur indique la contribution de chaque module à votre agrégat actuel. Les modules marqués **Pas de pondération** sont exclus de ce calcul.

L&#39;échelle de notation n&#39;a pas besoin d&#39;être la même pour tous les modules. Un module obtenu une note de 100 et un module obtenu une note de 10 contribuent tous deux correctement. La formule normalise chacune d&#39;elles avant d&#39;appliquer la pondération.

## Afficher et signaler les scores du carnet de notes

Les administrateurs de Adobe Learning Manager peuvent afficher les scores pondérés du carnet de notes de tous les élèves inscrits à un cours, analyser les performances de chaque élève par module, télécharger un relevé de notes filtré et suivre les modifications de la configuration du carnet de notes dans le rapport Piste d&#39;audit de contenu.

## Affichage du carnet de notes d’un cours

Lorsque l&#39;option Gradebook est activée pour un cours, une nouvelle section **Retour d&#39;informations L2 - Gradebook** apparaît dans la navigation de gauche sous **Rapports** lorsque vous ouvrez le cours.

* Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
* Dans le volet de navigation de gauche, sélectionnez **Cours** et ouvrez le cours que vous souhaitez réviser.
* Dans la navigation de cours, sous **Rapports**, sélectionnez **Retour d&#39;informations L2 - Classebook**. La page **Classeur de commentaires actifs** s&#39;ouvre.

![](assets/image_0013.png)

On peut y voir :

1. Critères de réussite du cours (nombre minimal de modules requis et score agrégé minimal)
2. Une ligne de filtre pour afficher les élèves par grade : **Réussite**, **Échec** ou **En attente d’achèvement**
3. Formule du score global : Score global = Σ (Score obtenu ÷ Score maximum) × Pondération, pour chaque module
4. Une liste d&#39;élèves montrant le **score total** de chaque élève et son score pour chaque module évaluable
5. Une liste déroulante d&#39;instances permettant de basculer entre les instances de cours lorsqu&#39;un cours a plusieurs instances

Les élèves qui n’ont pas encore tenté de modules avec score affichent des tirets dans les colonnes de score. Les modules qui ne prennent pas en charge la notation, le PDF, la vidéo, l&#39;audio et autres n&#39;apparaissent pas en tant que colonnes de notation.

## Afficher les scores d’un élève individuel

Dans le **Classeur de commentaires actifs**, sélectionnez le nom d&#39;un élève.

![](assets/image_0014.png)

La vue individuelle de l’élève affiche :

1. Nom, adresse électronique et statut de l’élève (**Achèvement en attente**, **Réussite** ou **Échec**)
2. Score global et nombre de modules requis terminés par l’élève
3. Une table de module montrant : le nom du module, son type, s&#39;il est requis, le statut, la pondération, le score obtenu et la contribution à l&#39;agrégat

La table de module comprend tous les modules avec et sans score. Les modules pouvant être notés montrent leur score et leur contribution. Les modules non marquables affichent des tirets dans les colonnes Score et Contribution.

## Modules de score

Le comportement de score pour les administrateurs et les instructeurs est inchangé par rapport au workflow actuel :

* **Les modules SCORM, AICC, xAPI et de quiz natif** sont notés automatiquement lorsque le contenu sous-jacent signale un score.
* **Les sessions de salle de classe, les sessions de classe virtuelle et les modules d&#39;activité** sont notés par les instructeurs ou les administrateurs à partir de la page **Présence et notation**.

## Télécharger le relevé de notes de l’élève pour un cours

Vous pouvez télécharger un relevé de notes de l’élève filtré pour ce cours directement à partir de la page du cahier de notes de l’une des deux façons suivantes :

* Dans le **Carnet de notes de retour d&#39;informations actif**, sélectionnez **Télécharger le relevé de notes de l&#39;élève** dans le coin supérieur droit de la page.
* Sur la page d&#39;accueil de l&#39;administrateur, sélectionnez **Rapports**, puis **Rapports personnalisés**. Sélectionnez **Relevés de notes des élèves** dans la liste des rapports disponibles.

Voir Signaler les modifications dans la version pour plus d’informations.

## Événements de piste d’audit de contenu

La piste d’audit de contenu capture deux événements de configuration spécifiques au journal de notes :

| **Événement** | **Lorsqu&#39;il apparaît** |
|-----------|---------------------|
| **Classeur mis à jour** | Lorsqu&#39;un auteur active ou désactive l&#39;annuaire de notes d&#39;un cours |
| **Poids Du Module Mis À Jour** | Lorsqu&#39;un auteur modifie le pourcentage pondéré d&#39;un module |

Voir Signaler les modifications dans la version pour plus d’informations.

Utilisez ces entrées pour suivre les personnes qui ont modifié la configuration du classeur et quand, en particulier dans les environnements où plusieurs auteurs collaborent sur le même cours.

## Dépannage

**La section Retour d&#39;informations L2 - Classebook n&#39;apparaît pas dans la navigation de cours**

L&#39;auteur du cours doit activer le Gradebook lors de la création du cours. Confirmez que l&#39;auteur a activé l&#39;annuaire de notes pour la création du cours. Si le cours a été créé avant que l&#39;annuaire de notes ne soit disponible, il ne peut pas être ajouté rétroactivement. Une nouvelle version du cours est requise.

**Le score total d’un élève est de 0 malgré les modules terminés**

Confirmez que le cours comporte au moins un module évaluable avec une valeur de pondération affectée. Si tous les modules terminés par l’élève ne peuvent pas être notés (PDF, vidéo, audio), aucun score global n’est calculé. Vérifiez également que les modules ayant obtenu un score ne sont pas toujours à l&#39;état **Révision en attente**. Les modules non notés sont exclus de l’agrégation jusqu’à ce qu’un instructeur attribue un score.

**La colonne Pondération est manquante dans le relevé de notes de l&#39;élève téléchargé**

Cette colonne s&#39;affiche uniquement lorsque l&#39;historique des notes est activé et qu&#39;au moins un module a une valeur de pondération enregistrée. Confirmez que l&#39;auteur a activé le classeur et enregistré les valeurs de pondération totalisant 100 %.

**Un élève a terminé tous les modules requis, mais affiche Achèvement en attente**

Un ou plusieurs modules peuvent toujours être en attente d&#39;un score d&#39;un instructeur ou d&#39;un administrateur (**Révision en attente**). Le cours ne peut pas être terminé tant que tous les modules requis n’ont pas été à la fois terminés et que le score n’est pas enregistré. Entrez le score exceptionnel de **Présence et notation** pour effacer l&#39;état en attente.
