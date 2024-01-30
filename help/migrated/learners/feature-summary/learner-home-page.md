---
jcr-language: en_us
title: Page d’accueil de l’élève
description: Une fois que l’administrateur a activé la mise en page immersive, l’élève, après s’être connecté à l’application, est accueilli par une interface utilisateur complètement remaniée.
contentowner: saghosh
source-git-commit: 021a5eaa979be241faa2cf2b372731afc157ea9b
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 57%

---



# Page d’accueil de l’élève

## Vue d’ensemble {#overview}

Une fois que l’administrateur a activé la mise en page immersive, l’élève, après s’être connecté à l’application, est accueilli par une interface utilisateur complètement remaniée.

>[!NOTE]
>
>La disposition immersive n’est pas prise en charge par le navigateur IE11.

Selon qu’un widget a été activé ou non, l’élève voit les éléments suivants :

## En-tête {#masthead}

Comprend un carrousel d’images ou de vidéos avec une URL intégrée. Le [L’administrateur peut charger n’importe quelle image ou vidéo](../../administrators/feature-summary/announcements.md#masthead) ressource en tant qu’en-tête et définissez sa visibilité pour un groupe d’élèves.

![](assets/learner-masthead.png)

*Afficher l’en-tête*

## Liste Mon apprentissage {#mylearninglist}

Affiche la formation suivie par l’élève. Ces formations sont affichées sous la forme de cartes alignées horizontalement. Vous pouvez cliquer sur le bouton droit ou gauche pour parcourir les cours.

![](assets/learner-my-learning-list.png)

*Afficher la liste Mon apprentissage*

Vous pouvez également faire glisser vers la gauche et la droite pour naviguer dans la liste.

Pour reprendre un cours, cliquez sur **[!UICONTROL Continuer]** sur une carte, et le lecteur démarre.

L’apparence des icônes sur chaque carte de formation est activée/désactivée par l’administrateur via l’application d’administration (**Paramètres** > **Généralités** > **Activer les icônes des cartes de formation**).

**Ajouter à la liste Mon apprentissage**

Si vous survolez une fiche de cours dans les listes **Recommandé en fonction de vos centres d’intérêt** et **Recommandation sur la base de l’activité des pairs**, vous pouvez voir une option pour ajouter le cours à la **liste Mon apprentissage**. Cliquez sur **[!UICONTROL +]** sur la carte du cours et le cours sera ajouté au **Liste Mon apprentissage**.

![](assets/add-my-learning.png)

*Ajouter à la liste Mon apprentissage*

## Choix des niveaux de compétence {#chooseskilllevels}

En tant qu’élève, vous pouvez filtrer le catalogue de cours en fonction des niveaux suivants :

* Débutant
* Intermédiaire
* Avancé

Choisissez une option pour afficher le catalogue de cours en fonction de la sélection.

![](assets/skill-levels.png)

*Sélectionner des niveaux de compétence*

## Calendrier {#calendar}

Affiche vos sessions et formations planifiées. Parcourez le calendrier pour voir les formations des mois suivants.

![](assets/learner-calendar.png)

*Afficher le calendrier des sessions planifiées*

Le widget Calendrier offre les fonctionnalités suivantes. Vous pouvez afficher les éléments suivants :

* Formation par mois. Faites défiler vers la gauche ou la droite.
* Prochaine formation en salle de classe ou en classe virtuelle à laquelle vous pourrez vous inscrire.
* Prochaine formation en salle de classe ou en classe virtuelle à laquelle vous vous êtes inscrit(e).
* Formation en salle de classe ou en classe virtuelle approuvée par le responsable.

## Réseaux sociaux {#socialfeed}

![](assets/social-feed.png)

*Afficher le flux social*

Découvrez de quoi parlent les autres utilisateurs.

Le widget récapitule l’activité pour une période. Il :

* Affiche les utilisateurs actifs et les activités des utilisateurs présents dans votre portée ou votre groupe.
* Affiche les publications diffusées au cours des deux dernières semaines.

## Compétences de profil {#profileskills}

Les compétences de profil sont utilisées pour les recommandations de cours. Si l’administrateur affecte une compétence à un utilisateur ou un groupe d’utilisateurs, cette compétence est ajoutée aux compétences de profil de l’élève. Si l’élève ajoute une compétence à son profil, tous les niveaux de compétence sont ajoutés aux compétences de profil de l’élève. Lorsqu&#39;un élève place le curseur de la souris sur une compétence, il peut voir le nom de la compétence, la méthode d&#39;ajout de la compétence, le niveau, le pourcentage d&#39;achèvement de la compétence, et les crédits.

![](assets/profile-skills.png)
*Afficher les compétences de profil*

Si un élève s’inscrit à un cours, seules les compétences externes basées sur un score sont ajoutées aux compétences de profil. En outre, un élève peut rechercher, sélectionner et ajouter des compétences externes à son profil. Si un élève s’est connecté à l’application de l’élève pour la première fois et que ses compétences sont déjà présentes, les compétences apparaissent sur Mon profil.

## Recommandé en fonction de vos centres d’intérêt {#recommendationbasedonyourareaofinterest}

Affiche la formation en fonction de votre centre d’intérêt choisi. La recommandation est pilotée par un algorithme de machine learning.

![](assets/learner-recommendation.png)

*Afficher les cours recommandés*

Pour des recommandations plus ciblées, vous pouvez mettre à jour vos compétences en cliquant sur **Afficher/Mettre à jour**.

Une fois que vous aurez ajouté une compétence, les recommandations futures seront plus ciblées en fonction de vos préférences.

Si l’administrateur a désactivé l’option **Explorer les compétences**, vous pourrez ajouter un centre d’intérêt à vos compétences.

Les cours recommandés sont affichés sous forme de fiches. Lorsque vous placez le curseur de la souris sur une carte, vous pouvez voir plus de détails sur le cours.

La terminologie du produit est également prise en charge.

**Compétences correspondant au secteur d’industrie**

Si l’administrateur a activé l’option **Correspondant au secteur** dans l’application d’administration, vous pouvez afficher le graphique réseau des compétences.

Ces compétences ne peuvent être visualisées que lorsque l’administrateur définit le type de formation sur Correspondant au secteur.

Dans la visualisation Carte de compétence, vous pouvez rechercher une ou des compétences et les ajouter.

![](assets/learner-add-industry-skills.png)

*Visualisation de la carte de compétences*

Activer l’option **Afficher les compétences pour lesquelles des formations sont présentes dans mon compte**, si vous souhaitez afficher toutes les compétences présentes dans votre compte.

Après avoir ajouté une compétence, vous pouvez voir le graphique dirigé par la force avec la compétence sélectionnée comme sommet principal et les compétences associées comme sommets plus petits.

Les compétences que vous avez choisies apparaissent également dans la section **Compétences sélectionnées**.

![](assets/learner-add-industry-skills-1.png)

*Compétences sélectionnées*

Pour ajouter les compétences, cliquez sur **[!UICONTROL Ajouter]**.

## Recommandation sur la base de l’activité des pairs {#recommendationbasedonpeeractivity}

Affiche la formation en fonction de ce que vos homologues suivent. Ceci est aussi déclenché par un algorithme d’apprentissage automatique. Les recommandations sont basées sur la formation pour les élèves personnalisés et alignés sur le secteur.
