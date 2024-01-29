---
jcr-language: en_us
title: Page d’accueil de l’élève
description: Une fois que l’administrateur a activé la mise en page immersive, l’élève, après s’être connecté à l’application, est accueilli par une interface utilisateur complètement remaniée.
contentowner: saghosh
source-git-commit: 021a5eaa979be241faa2cf2b372731afc157ea9b
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---



# Page d’accueil de l’élève

## Présentation {#overview}

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

Si vous survolez une carte de cours dans le panneau **Recommandé en fonction de vos centres d’intérêt** et **Recommandé en fonction des listes d&#39;activités des pairs**, vous pouvez voir une option pour ajouter le cours à la **Liste Mon apprentissage**. Cliquez sur **[!UICONTROL +]** sur la carte du cours et le cours sera ajouté au **Liste Mon apprentissage**.

![](assets/add-my-learning.png)

*Ajouter à la liste Mon apprentissage*

## Choisir les niveaux de compétence {#chooseskilllevels}

En tant qu’élève, vous pouvez filtrer le catalogue de cours en fonction de ces niveaux :

* Débutant
* Intermédiaire
* Avancé

Choisissez une option et vous pouvez ensuite voir le catalogue de cours en fonction de la sélection.

![](assets/skill-levels.png)

*Sélectionner des niveaux de compétence*

## Calendrier {#calendar}

Affiche vos sessions et formations planifiées. Parcourez le calendrier pour voir les formations des mois suivants.

![](assets/learner-calendar.png)

*Afficher le calendrier des sessions planifiées*

Le widget Calendrier offre les fonctionnalités suivantes. Vous pouvez afficher :

* Formation par mois. Faites défiler vers la gauche ou la droite.
* Prochaine formation en classe ou en classe virtuelle à laquelle vous pourrez vous inscrire.
* Prochaine formation en salle de classe ou en classe virtuelle à laquelle vous êtes inscrit(e).
* Formation en salle de classe ou en classe virtuelle approuvée par le responsable.

## Flux social {#socialfeed}

![](assets/social-feed.png)

*Afficher le flux social*

Découvrez de quoi parlent les autres utilisateurs.

Le widget récapitule l’activité pour une période. Il :

* Affiche les utilisateurs actifs et leurs activités des utilisateurs qui se trouvent dans votre portée ou votre groupe.
* Affiche les publications effectuées au cours des deux dernières semaines.

## Compétences de profil {#profileskills}

Les compétences de profil sont utilisées pour les recommandations de cours. Si l’administrateur affecte une compétence à un utilisateur ou à un groupe d’utilisateurs, la compétence est ajoutée aux compétences de profil de l’élève. Si l’élève ajoute une compétence à son profil, tous les niveaux de compétence sont ajoutés aux compétences de profil de l’élève. Lorsqu’un élève passe le curseur de la souris sur une compétence, il peut voir le nom de la compétence, la méthode d’ajout de la compétence, le niveau, le pourcentage d’achèvement de la compétence et les crédits.

![](assets/profile-skills.png)
*Afficher les compétences de profil*

Si un élève s’inscrit à un cours, seules les compétences externes basées sur un score sont ajoutées aux compétences de profil. En outre, un élève peut rechercher, sélectionner et ajouter des compétences externes à son profil. Si un élève s’est connecté à l’application de l’élève pour la première fois et que ses compétences sont déjà présentes, les compétences apparaissent sur Mon profil.

## Recommandation en fonction de votre centre d’intérêt {#recommendationbasedonyourareaofinterest}

Affiche la formation en fonction du centre d’intérêt choisi. La recommandation est pilotée par un algorithme de machine learning.

![](assets/learner-recommendation.png)

*Afficher les cours recommandés*

Pour des recommandations plus ciblées, vous pouvez mettre à jour vos compétences en cliquant sur **Afficher/Mettre à jour**.

Une fois que vous avez ajouté une compétence, les recommandations futures seront plus ciblées et ciblées en fonction de vos préférences.

Si l’administrateur a désactivé l’option **Découvrir les compétences**, vous serez en mesure d’ajouter de l’intérêt à vos compétences.

Les cours recommandés sont affichés sous forme de cartes. Lorsque vous placez le curseur de la souris sur une carte, vous pouvez voir plus de détails sur le cours.

La terminologie du produit est également prise en charge.

**Compétences alignées sur le secteur**

Si l’administrateur a activé cette option, vous pouvez afficher le graphique réseau des compétences **Correspondant au secteur** dans l’application d’administration.

Ces compétences ne peuvent être affichées que lorsque l’administrateur définit le type de formation sur Correspondant au secteur.

Dans la visualisation de la carte de compétences, vous pouvez rechercher une ou plusieurs compétences et les ajouter.

![](assets/learner-add-industry-skills.png)

*Visualisation de la carte de compétences*

Activer l’option **Afficher les compétences pour lesquelles des formations sont présentes dans mon compte**, si vous souhaitez afficher toutes les compétences présentes dans votre compte.

Après avoir ajouté une compétence, vous pouvez voir le graphique dirigé vers la force avec la compétence sélectionnée comme sommet principal et les compétences associées comme sommets plus petits.

Les compétences que vous avez choisies s’affichent également dans le panneau **Compétences sélectionnées** section.

![](assets/learner-add-industry-skills-1.png)

*Compétences sélectionnées*

Pour ajouter les compétences, cliquez sur **[!UICONTROL Ajouter]**.

## Recommandation basée sur l’activité des pairs {#recommendationbasedonpeeractivity}

Affiche la formation en fonction de ce que vos homologues suivent. Là encore, il est piloté par un algorithme de machine learning. Les recommandations sont basées sur la formation pour les élèves personnalisés et alignés sur le secteur.
