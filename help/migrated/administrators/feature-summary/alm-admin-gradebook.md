---
description: Tout sur l’activation du Gradebook et sa visibilité pour les auteurs et les élèves
jcr-language: en_us
title: Classeur pour l’administrateur
source-git-commit: c6ad5527fa5156d1a681fa0f21fb259ac3ebf782
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 0%

---


# Activation de la visibilité de l’annuaire de notes pour votre compte

## Présentation

Avant que les auteurs puissent afficher le cahier de notes aux élèves dans un cours, un administrateur doit activer le paramètre de visibilité du cahier de notes au niveau du compte. Ce paramètre agit comme un commutateur principal : lorsqu&#39;il est désactivé, les élèves ne peuvent pas voir le cahier de notes dans un cours, quelle que soit la façon dont les cours individuels sont configurés.

## Ce que ce paramètre contrôle

Le paramètre **Visibilité du cahier de notes** dans **Paramètres** > **Général** détermine si les auteurs sont autorisés à exposer le cahier de notes aux élèves au niveau du cours.

| État du paramètre | Effet |
| --- | --- |
| Activé | Les auteurs peuvent contrôler la visibilité du journal de notes par cours à l&#39;aide de l&#39;option **Afficher le journal de notes aux élèves** dans l&#39;éditeur de cours. Les élèves voient l&#39;onglet **Gradebook** dans les cours où l&#39;auteur l&#39;a activé. |
| Désactivé | Les élèves ne peuvent pas voir le cahier de notes dans un cours. Si elle est désactivée, la configuration du cours n’aura pas le paramètre permettant d’afficher le cahier de notes pour les élèves. |


Cela signifie que le paramètre au niveau du compte et le paramètre au niveau du cours fonctionnent ensemble. Les deux doivent être activés pour qu’un élève puisse afficher le cahier de notes.

## Activer la visibilité des classeurs

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Dans le volet de navigation de gauche, sélectionnez **Paramètres**.
3. Sélectionnez **Général**.
4. Faites défiler jusqu&#39;à la section **Visibilité du Gradebook**.
5. Cochez la case **Activer l&#39;affichage Gradebook pour les élèves**.

   ![](assets/gradebook-admin-1.png)

Les auteurs peuvent désormais configurer la visibilité du cahier de notes par cours.

## Impact sur les workflows des auteurs

Lorsque ce paramètre au niveau du compte est activé, l&#39;option **Afficher le cahier de notes aux élèves** dans l&#39;éditeur de cours devient disponible. Les auteurs utilisent ce bouton pour décider, par cours, si les élèves peuvent voir l&#39;onglet **Gradebook**.

Lorsque ce paramètre au niveau du compte est désactivé :

* L&#39;option **Afficher le journal de notes aux élèves** dans l&#39;éditeur de cours peut toujours apparaître, mais toute configuration au niveau du cours est remplacée. Les élèves ne verront pas le cahier de notes.
* Les scores et les calculs pondérés du carnet de notes continuent d’être exécutés en arrière-plan à des fins de création de rapports par l’administrateur.
* Les administrateurs et les administrateurs personnalisés peuvent toujours télécharger les relevés de notes des élèves avec les données du carnet de notes.

>[!NOTE]
>
>La désactivation de ce paramètre au niveau du compte ne supprime aucune configuration ni note du journal de notes. Si vous l’activez à nouveau, tous les paramètres du carnet de notes de niveau cours précédemment configurés sont immédiatement restaurés.

## Interaction entre les deux paramètres

| Paramètre au niveau du compte | Paramètre au niveau du cours | Ce que l’élève voit |
| --- | --- | --- |
| Activé | Afficher le cahier de notes pour les élèves : **Activé** | Onglet **Gradebook** visible dans le lecteur de cours |
| Activé | Afficher le cahier de notes pour les élèves : **désactivé** | Aucun onglet Gradebook ; scores calculés en interne uniquement |

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
