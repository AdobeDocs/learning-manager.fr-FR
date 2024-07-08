---
jcr-language: en_us
title: Page d’accueil de l’élève
description: Une fois que l’administrateur a activé la disposition immersive, l’apprenant, après s’être connecté à l’application, est accueilli par une interface utilisateur entièrement remaniée.
contentowner: saghosh
exl-id: 71b495c7-a6c8-4e6e-9f00-ec93d7b483ad
source-git-commit: c4eb9a7c4fca73bc029f9afad1f3d48725779d30
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 40%

---

# Page d’accueil de l’élève

## Vue d’ensemble {#overview}

Une fois que l’administrateur a activé la disposition immersive, l’apprenant est accueilli avec une interface utilisateur complètement remaniée lors de la connexion à l’application.

>[!NOTE]
>
>Le navigateur IE11 ne prend pas en charge la disposition immersive.

## Nouvelle interface utilisateur de l’apprenant pour la disposition immersive

>[!IMPORTANT]
>
>La nouvelle interface utilisateur de l’apprenant sera publiée par étapes.

Nous avons actualisé l’interface utilisateur de l’apprenant avec un design plus élégant et mis à jour. La nouvelle interface utilisateur vise à fournir une expérience utilisateur cohérente sur les **[!UICONTROL pages de destination Accueil de]** l’apprenant, **[!UICONTROL Mon apprentissage]**, **[!UICONTROL Catalogue]** et **[!UICONTROL Aperçu du]** cours. Les nouveaux éléments visuels suivent les styles de conception actuels, ce qui rend le produit plus facile à utiliser et attrayant. Cette mise à jour inclut un nouveau générique, un panneau latéral et des widgets contemporains.

>[!NOTE]
>
>L’interface utilisateur remaniée s’applique uniquement à la disposition immersive. Le web/l’application mobile ne prend pas encore en charge ces modifications et les mettra à jour dans une prochaine version.

![](assets/old-ui.png)
_Ancienne interface utilisateur_

![](assets/home-page-new.jpg)
_Nouvelle interface utilisateur_

### Page d’accueil

La page d’accueil a un nouveau design avec un panneau latéral amélioré, un en-tête supérieur, des cartes de cours améliorées et des widgets.

![](assets/new-ui-homepage.png)
_Nouvelle page d’accueil_

### Page de catalogue

Les pages du catalogue ont un nouveau look avec des filtres organisés et des cartes de cours améliorées pour offrir une meilleure expérience utilisateur.

![](assets/catalog.jpg)
_Page de catalogue_

### Page de présentation du cours

La page d’aperçu du cours a une nouvelle apparence avec plus de détails sur le cours. Cette page aide les apprenants à obtenir toutes les informations dont ils ont besoin.

![](assets/course-overview.jpg)
_Page d’aperçu du cours_

### Cartes de cours

Les cartes de cours présentent également une mise en page redessinée pour afficher les détails plus efficacement. Les cartes de cours remaniées mettent en évidence les métadonnées pertinentes requises pour l’inscription. Ces métadonnées incluent les dates de publication ou d’échéance, les évaluations et les descriptions correctes, ainsi que leurs auteurs ou fournisseurs.

![](assets/old-course-cards.png)
_Ancienne carte de cours_

![](assets/new-course-card.jpg)
_Nouvelle carte de cours_

Pour les cours importés de LinkedIn **et de** la **plateforme Go1**, les fiches de cours afficheront les dates de publication originales de **LinkedIn** et **Go1**. Vous pouvez également afficher ces dates de publication spécifiques dans l’interface utilisateur.

### Barre latérale et barre de recherche

La barre latérale est mise à jour avec de nouveaux éléments de l’interface utilisateur pour une apparence plus soignée. La nouvelle barre de recherche n’a pas de bouton de recherche, ce qui lui donne un aspect plus propre. Les apprenants peuvent taper un mot-clé et appuyer sur Entrée pour lancer la recherche ou sélectionner les résultats sous la barre de recherche.

![](assets/side-bar.png)
_Barre latérale et barre de recherche_

### En-tête {#masthead}

Comporte un carrousel de vidéos ou d’images avec une URL intégrée. L’administrateur [peut télécharger n’importe quelle image ou ressource vidéo](../../administrators/feature-summary/announcements.md#masthead) en tant qu’en-tête de mât et définir sa visibilité pour un groupe d’apprenants.

![](assets/learner-masthead.png)

*Afficher le générique*

### Liste Mon apprentissage {#mylearninglist}

Affiche la formation suivie par l’apprenant. Ces entraînements sont affichés sous forme de cartes alignées horizontalement. Vous pouvez cliquer sur le bouton droit ou gauche pour parcourir les cours.

![](assets/learner-my-learning-list.png)

*Afficher ma liste d’apprentissage*

Vous pouvez également balayer vers la gauche et la droite pour naviguer dans la liste.

Pour reprendre un cours, cliquez sur **[!UICONTROL Continuer]** sur une carte et le lecteur se lance.

L’affichage des icônes sur chaque carte de formation est activé/désactivé par l’administrateur via l’application Admin (**Paramètres** > **Général** > **Activer les icônes** de cartes de formation).

**Ajouter à la liste Mon apprentissage**

Si vous survolez une fiche de cours dans les listes **Recommandé en fonction de vos centres d’intérêt** et **Recommandation sur la base de l’activité des pairs**, vous pouvez voir une option pour ajouter le cours à la **liste Mon apprentissage**. Cliquez sur **[!UICONTROL +]** sur la carte du cours et le cours sera ajouté à Ma liste **d’apprentissage**.

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

## Widget du tableau de bord de conformité

Le widget du tableau de bord de conformité permet aux apprenants de filtrer les cours/cursus d’apprentissage/certifications dont les échéances sont à venir à l’aide de l’étiquette Conformité. Cette fonctionnalité est disponible sur toutes les applications pour apprenants, y compris l’application ALM Teams, AEM, l’application mobile, l’application immersive et l’application SF.

![](assets/compliance-status-learner.png)
_Widget du tableau de bord de conformité_

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

Si un élève s’inscrit à un cours, seules les compétences externes basées sur un score sont ajoutées aux compétences de profil. En outre, un apprenant peut rechercher, sélectionner et ajouter des compétences externes à son profil. Si un apprenant s’est connecté à l’application de l’apprenant pour la première fois et si ses compétences sont déjà présentes, les compétences apparaissent sur Mon profil.

## Recommandé en fonction de vos centres d’intérêt {#recommendationbasedonyourareaofinterest}

Affiche la formation en fonction de votre centre d’intérêt choisi. La recommandation est pilotée par un algorithme d’apprentissage automatique.

![](assets/learner-recommendation.png)

*Afficher les cours recommandés*

Pour des recommandations plus ciblées, vous pouvez mettre à jour vos compétences en cliquant sur **Afficher/Mettre à jour**.

Une fois que vous aurez ajouté une compétence, les recommandations futures seront plus ciblées en fonction de vos préférences.

Si l’administrateur a désactivé l’option **Explorer les compétences**, vous pourrez ajouter un centre d’intérêt à vos compétences.

Les cours recommandés sont affichés sous forme de fiches. Lorsque vous survolez une carte avec la souris, vous pouvez voir plus de détails sur le parcours.

La terminologie du produit est également prise en charge.

**Compétences correspondant au secteur d’industrie**

Si l’administrateur a activé l’option **Correspondant au secteur** dans l’application d’administration, vous pouvez afficher le graphique réseau des compétences.

Ces compétences ne peuvent être visualisées que lorsque l’administrateur définit le type de formation sur Correspondant au secteur.

Dans la visualisation Carte de compétence, vous pouvez rechercher une ou des compétences et les ajouter.

![](assets/learner-add-industry-skills.png)

*Visualisation de la carte des compétences*

Activez l’option **Afficher les compétences pour lesquelles des formations sont présentes dans mon compte**, si vous souhaitez afficher toutes les compétences qui se trouvent dans votre compte.

Après avoir ajouté une compétence, vous pouvez voir le graphique dirigé par la force avec la compétence sélectionnée comme sommet principal et les compétences associées comme sommets plus petits.

Les compétences que vous avez choisies apparaissent également dans la section **Compétences sélectionnées**.

![](assets/learner-add-industry-skills-1.png)

*Compétences sélectionnées*

Pour ajouter les compétences, cliquez sur **[!UICONTROL Ajouter]**.

## Recommandation sur la base de l’activité des pairs {#recommendationbasedonpeeractivity}

Affiche la formation en fonction des résultats suivis par vos pairs. Ceci est aussi déclenché par un algorithme d’apprentissage automatique. Les recommandations sont basées sur la formation des apprenants personnalisés et alignés sur l’industrie.
