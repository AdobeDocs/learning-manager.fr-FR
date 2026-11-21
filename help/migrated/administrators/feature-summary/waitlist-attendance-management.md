---
jcr-language: en_us
title: Gestion de l’assiduité et de la liste d’attente
description: Les administrateurs peuvent gérer l’assiduité et les listes d’attente des cours pour les élèves.
contentowner: manochan
exl-id: 257ed196-d6a7-4d6c-bd90-33d658f6ba55
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 38dba6765ff013e446ab1f6098e9f1df0c24d0f9
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 38%
---
# Gestion de l’assiduité et de la liste d’attente

Les administrateurs peuvent gérer l’assiduité et les listes d’attente des cours pour les élèves.

## Gestion de la liste d’attente {#waitlistmanagement}

Les élèves sont sur liste d&#39;attente pour un cours en salle de classe lorsque les places sont limitées, en fonction de l&#39;ordre de leur inscription. Lorsque toutes les places réservées à un groupe d’utilisateurs sont remplies, les membres supplémentaires de ce groupe sont placés sur la liste d’attente du groupe. Les élèves en dehors des groupes d&#39;utilisateurs sont placés sur la **liste d&#39;attente ouverte**.

Les administrateurs peuvent consulter la liste d’attente et gérer les élèves inscrits sur liste d’attente. Adobe Learning Manager peut également promouvoir automatiquement les élèves inscrits sur liste d’attente lorsqu’une place devient disponible.

Pour gérer les élèves inscrits sur liste d’attente :

1. Sélectionnez **Cours** dans le volet de gauche.
1. Sélectionnez le nom d’un cours en salle de classe dans les cours disponibles.

   Une nouvelle page apparaît avec des informations détaillées sur le cours.

1. Sélectionnez **Liste d&#39;attente** dans le volet gauche de la page de détails du cours.

   La page de liste d&#39;attente s&#39;ouvre avec l&#39;**état de liste d&#39;attente** suivant :

   * **Limite de places :** nombre total de places disponibles pour la session.
   * **Remplie :** nombre de places actuellement occupées.
   * **Dans la liste d&#39;attente :** nombre d&#39;élèves en attente d&#39;inscription.

1. Sélectionnez les onglets suivants dans la page **Liste d&#39;attente** :

   1. **Liste d&#39;attente par groupe d&#39;utilisateurs** : répertorie les élèves sur liste d&#39;attente sous chaque groupe d&#39;utilisateurs.

   >[!NOTE]
   >
   >Cet onglet apparaît uniquement si le paramètre **Inscription de groupe** est activé.

   1. **Ouvrir la liste d&#39;attente** : répertorie les élèves inscrits sur liste d&#39;attente qui ne sont réservés pour aucun groupe d&#39;utilisateurs.

   ![Page de liste d&#39;attente affichant l&#39;onglet Liste d&#39;attente par groupe d&#39;utilisateurs](assets/waitlist-by-user-group-tab.png "Page de liste d&#39;attente affichant l&#39;onglet Liste d&#39;attente par groupe d&#39;utilisateurs")

1. En regard d’un élève, sélectionnez l’une des actions suivantes :

   | **Action** | **Description** |
   |---|---|
   | **Confirmer** | Inscrit l’élève sur liste d’attente dans la session et le supprime de la liste d’attente. |
   | **Se désinscrire** | Supprime l’élève de la liste d’attente et met à jour les positions des autres élèves inscrits sur liste d’attente. |

## Gestion de l’assiduité {#attendancemanagement}

Cette fonction s’applique uniquement aux cours en salle de classe et en salle de classe virtuelle. Vous pouvez enregistrer l’assiduité en suivant les étapes ci-dessous :

1. Cliquez sur Cours dans le volet de gauche après avoir ouvert une session en tant qu’administrateur.
1. Dans la liste des cours disponibles, cliquez sur le nom d’un module/cours en salle de classe de votre choix. Une nouvelle page apparaît avec des informations détaillées sur le cours.
1. Cliquez sur l’onglet Assiduité, sélectionnez les élèves, puis cliquez sur Enregistrer pour noter l’assiduité.

>[!NOTE]
>
>S’il existe plusieurs modules dans un cours et que l’élève n’a terminé qu’un seul d’entre eux, vous pouvez sélectionner un seul module et cliquer sur Enregistrer. Si l’élève a terminé tous les modules d’un cours, vous pouvez cliquer sur l’option Tout sélectionner, puis cliquer sur Enregistrer.

L’assiduité à une session de classe virtuelle basée sur Adobe Connect est marquée automatiquement 2 à 3 heures après la session. L’achèvement d’un cours en salle de classe virtuelle par un élève est marqué uniquement une fois l’assiduité marquée.
