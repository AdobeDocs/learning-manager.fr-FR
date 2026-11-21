---
description: Découvrez comment activer les inscriptions multiples pour les cours adaptatifs, gérer les limites de places et les listes d’attente et comprendre les règles d’inscription dans les parcours d’apprentissage
jcr-language: en_us
title: Inscription multiple pour les cours adaptatifs
exl-id: e2a52964-fe9d-4a71-a020-68201f75f9f0
hide: true
source-git-commit: e056f1a655efd7c999856e2b54b28e676e67afc6
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Inscription multiple pour les cours adaptatifs

## Présentation

L&#39;inscription multiple permet à un élève de s&#39;inscrire simultanément à plusieurs instances d&#39;un même cours. Dans Adobe Learning Manager, vous pouvez désormais activer les inscriptions multiples pour les cours adaptatifs.

## A propos des inscriptions multiples à un cours adaptatif

Un cours adaptatif montre à chaque élève uniquement les modules qui correspondent à ses groupes d’utilisateurs. Lorsque la fonctionnalité multi-inscription est activée, un élève peut suivre plusieurs instances de ce cours, par exemple des sessions dans différents mois.

Les cours adaptatifs suivent les listes d’attente au niveau du module, pas au niveau de l’instance. Un élève peut être en cours sur certains modules et en liste d’attente sur d’autres en même temps. Par exemple, un cours comporte deux instances, chacune ayant une limite de places d&#39;une personne. Le premier élève s&#39;inscrit dans les deux instances et prend les deux places. Un deuxième élève qui s&#39;inscrit dans les deux instances est sur liste d&#39;attente dans les deux.

## Activer les inscriptions multiples pour un cours adaptatif

1. Se connecter à Adobe Learning Manager en tant qu’auteur.
2. Dans le volet de navigation de gauche, sélectionnez **Cours**. Ouvrez un cours adaptatif ou créez-en un.
3. Ajoutez les modules. Pour chaque module de contenu, sélectionnez **Ajouter des règles** pour définir les groupes d&#39;utilisateurs qui peuvent le voir et les groupes d&#39;utilisateurs pour lesquels il est obligatoire.
4. Sélectionnez **Enregistrer**. L’option d’inscription multiple devient disponible.
5. Activez l&#39;option **Multi-inscription**.
6. Créez les instances nécessaires. Pour les sessions de salle de classe et de classe virtuelle, définissez les limites de places.
7. Sélectionnez **Publish**.

Les élèves peuvent désormais s’inscrire à plusieurs instances du cours.

## Limite de places et comportement de liste d’attente

Les cours adaptatifs appliquent des limites de places pour chaque classe ou session de classe virtuelle. Un élève est inscrit immédiatement et n’est sur liste d’attente que pour les sessions qui sont complètes. L’élève peut démarrer tous les autres modules immédiatement.

| Condition | Résultat |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Toutes les sessions visibles ont des places disponibles | L’élève est inscrit avec un accès complet à tous les modules. |
| Une ou plusieurs sessions visibles sont saturées | L’élève est inscrit et sur liste d’attente uniquement pour les sessions complètes. |
| Vous ajoutez une session obligatoire sans places à un cours avec des élèves inscrits | L’élève est sur liste d’attente pour la nouvelle session. La progression existante et l’accès ne sont pas affectés. |
| Une modification de groupe d’utilisateurs supprime une session des modules visibles de l’élève | Adobe Learning Manager libère immédiatement le siège. |
| Un élève passe à une autre instance | Les modules terminés restent terminés. Les places sont utilisées uniquement pour les modules visibles que l’élève n’a pas terminés. |

## Règles d’inscription et d’achèvement pour les parcours d’apprentissage adaptatifs

Les auteurs peuvent désormais ajouter des cours adaptatifs aux parcours d’apprentissage adaptatif dans Adobe Learning Manager. L’inscription, la liste d’attente et l’achèvement suivent des règles qui combinent les paramètres de section et les paramètres de cours configurés par vos auteurs.

### Comment un parcours d’apprentissage adaptatif évalue un élève

Adobe Learning Manager évalue la visibilité au niveau de la section et du cours. La règle de section détermine si un élève doit voir une section et les cours adaptatifs qu’elle contient. Les règles du module dans chaque cours adaptatif décident ensuite si l’élève est inscrit au cours.

Les élèves seront automatiquement inscrits chaque fois qu&#39;il y aura un changement d&#39;URL en ce qui concerne le cours adaptatif dans Adaptive LP. De même, les élèves recevront des notifications d’inscription automatique et des e-mails.

### Règles d’évaluation de l’inscription

Lorsque vous inscrivez un élève à un parcours d’apprentissage adaptatif, Adobe Learning Manager vérifie le parcours dans l’ordre suivant :

| Ordre | Vérifier | Résultat |
|-----------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Visibilité de la section | Adobe Learning Manager vérifie l&#39;inscription à un cours uniquement si sa section est visible par l&#39;élève. |
| 2 | Éligibilité au cours | Si le cours n’a pas de module obligatoire pour l’élève, celui-ci n’est pas inscrit au cours. Le cours n’est pas pris en compte dans l’achèvement du parcours d’apprentissage. |
| 3 | Sections sans cours éligible | Si une section contient uniquement des cours adaptatifs et que l’élève n’est éligible pour aucun d’entre eux, Adobe Learning Manager ignore la section. |
| 4 | Inscription au parcours d’apprentissage | Si aucune des sections obligatoires ne s’applique à l’élève, celui-ci n’est pas inscrit au parcours d’apprentissage. |

Si l’élève est déjà inscrit à une instance du cours qui appartient à l’instance du parcours d’apprentissage, Adobe Learning Manager utilise cette inscription.

Après l’inscription, les règles suivantes s’appliquent :

* Un élève qui a ignoré un cours initialement en raison de la visibilité peut être inscrit automatiquement si le cours adaptatif est visible en raison des modifications ultérieures de la visibilité/règle obligatoire.
* Un changement de groupe d&#39;utilisateurs ou un changement de cours peut désinscrire un élève d&#39;un cours adaptatif. Si aucun contenu obligatoire n’est conservé dans le parcours, l’élève est désinscrit du parcours.
* Pour les modifications de section, l’élève ne recevra pas de notification d’inscription automatique ni d’e-mail. Lors du rechargement de la page, l’élève peut voir les modifications.

### Comportement de liste d’attente dans les parcours d’apprentissage adaptatifs

La liste d’attente fonctionne au niveau de la session, pas au niveau de l’instance. Cela s’applique également aux cours adaptatifs dans les parcours d’apprentissage.

| Scénario | Comportement |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Aucun cours adaptatif du parcours ne comporte de module de salle de classe ou de salle de classe virtuelle | Aucune liste d’attente ne s’applique. |
| Un cours adaptatif comporte un module de salle de classe ou de classe virtuelle et aucune instance n’est sélectionnée | Le cours est défini par défaut sur **Aucune instance**. L’élève peut s’inscrire dans n’importe quelle instance et est sur liste d’attente uniquement dans les sessions qui sont complètes. |
| Une instance est sélectionnée avant l’inscription | L’élève est inscrit à cette instance et est sur liste d’attente uniquement pour les sessions qui sont complètes. |

Pour gérer les élèves inscrits sur liste d&#39;attente, ouvrez le cours adaptatif et sélectionnez l&#39;onglet **Élèves** > **Liste d&#39;attente**. Pour un cours adaptatif dans un parcours d’apprentissage flexible et un parcours d’apprentissage adaptatif, les élèves inscrits sur liste d’attente apparaissent uniquement sur l’onglet **Liste d’attente** du cours et non sous le parcours d’apprentissage.

### Actualisation de l’achèvement et comportement de restauration

Adobe Learning Manager ne révoque pas automatiquement l’achèvement lorsque des groupes d’utilisateurs ou des règles changent. Un élève terminé reste terminé jusqu’à ce que vous actualisiez l’achèvement.

* Exécutez **Actualiser l’achèvement** sur le parcours d’apprentissage. Vous ne pouvez pas actualiser un cours adaptatif seul pour les élèves qui le suivent tout au long du parcours.

* Chaque cours adaptatif est recalculé en premier, en fonction des modules obligatoires actuels de l’élève. Le parcours d’apprentissage est ensuite recalculé en fonction des sections obligatoires actuelles et des états de cours actualisés.

* Si le cours ou le parcours n’est plus terminé, l’état de l’élève passe à En cours. L&#39;achèvement original reste sur le relevé de notes de l&#39;élève en tant qu&#39;enregistrement historique.

* Une restauration d’achèvement recherche les cours adaptatifs dont les modules ont été modifiés en raison d’une modification de groupe d’utilisateurs ou d’une republication. Il recalcule ces cours, puis le parcours d’apprentissage. L&#39;état de la tâche affiche **Réussite** une fois la restauration terminée.

La liste d’attente est suivie au niveau du module. Un élève peut être mis en liste d’attente sur une session complète dans plusieurs instances. Par exemple, un cours comporte deux instances avec une limite de places d&#39;une unité chacune. Le premier élève s&#39;inscrit dans les deux instances et prend les deux places. Un deuxième élève qui s&#39;inscrit dans les deux instances apparaît sur l&#39;onglet **Liste d&#39;attente** de chaque instance.

### Attribuer des places aux élèves inscrits sur liste d’attente

Lorsqu’un élève se désinscrit, qu’un auteur augmente une limite de places ou qu’un élève change d’instance, Adobe Learning Manager efface la liste d’attente dans l’ordre de la date d’inscription. Vous pouvez également allouer des places manuellement.

1. Ouvrez le cours adapté.
2. Sélectionnez l&#39;onglet **Élèves** > **Liste d&#39;attente**.
3. Cochez la case en regard de chaque élève pour lequel vous souhaitez allouer des places.
4. Sélectionnez **Allouer Des Places**.

Adobe Learning Manager efface chaque élève sélectionné de la liste d&#39;attente de toutes les sessions sur liste d&#39;attente en même temps, et pas seulement de la session que vous consultez. Le système suppose que vous avez organisé le siège pour l’élève.
