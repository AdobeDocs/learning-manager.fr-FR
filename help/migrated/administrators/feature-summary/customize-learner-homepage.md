---
jcr-language: en_us
title: Personnaliser la page d’accueil des élèves
description: Un administrateur peut personnaliser la page d’accueil de l’élève et la rendre plus moderne, basée sur le contenu et personnalisée pour un élève.
contentowner: saghosh
source-git-commit: 2dd741a9e0e49986df34bd415ea57f9e64f3b26a
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---



# Personnaliser la page d’accueil des élèves

## Présentation {#overview}

Un administrateur peut personnaliser la page d’accueil de l’élève et la rendre plus moderne, basée sur le contenu et personnalisée pour un élève.

L’approche personnalisée offre une manière widgetisée de créer une page d’accueil des élèves, que l’administrateur de l’organisation peut configurer dans l’interface utilisateur d’administration de manière WYSIWYG.

L’expérience est basée sur des recommandations de formation personnalisées issues d’un algorithme basé sur l’IA qui analyse le contenu tiers en fonction des compétences du secteur, intègre l’activité des pairs et les centres d’intérêt des élèves à l’aide de données explicites et implicites.

## Configuration de la page d’accueil de l’élève {#configurethelearnerhomepage}

Sur la **Branding** > **Page d’accueil de l’élève** , un administrateur peut personnaliser l&#39;expérience de la page d&#39;accueil d&#39;un élève, de sorte que lorsque l&#39;élève se connecte à l&#39;application de l&#39;élève, il voit un aspect complètement remanié.

Les administrateurs peuvent définir l’interface utilisateur (apparence) à partir de l’application d’administration (**Branding** > **Page d’accueil de l’élève** tab).

Les administrateurs peuvent passer en mode Widget immersif de l’interface utilisateur, personnaliser les widgets/fonctionnalités en conséquence, puis activer l’interface utilisateur immersive.

Le **Page d’accueil de l’élève** screen contient les sections suivantes :

## Option de disposition immersive {#immersivelayoutoption}

Pour afficher la mise en page d’une page immersive, activez l’option **Immersif**. Vous pouvez activer/désactiver cette option dans **Identité visuelle > Général**.

Dans les versions précédentes, les options de la page d’accueil des élèves se trouvaient dans Paramètres.

Voici les options que vous pouvez définir :

**Expérience de la page d’accueil :** Activer soit **Classique** ou **Immersif**. Si vous choisissez l’option Immersive, les options suivantes s’affichent :

* **Type de formation :** Choisissez l’une des options suivantes : **Industrie** ou **Aligné personnalisé**. Des formations personnalisées sont créées en interne. Les formations conformes au secteur d’activité comprennent du contenu standard provenant de fournisseurs tiers.

![](assets/select-homepage-experience.png)

*Définissez l’expérience de la page d’accueil en sélectionnant Secteur ou Aligné personnalisé*

L’option **Permettre à l’élève d’explorer les domaines d’intérêt** est disponible pour les expériences Classique et Immersive.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Si vous choisissez Personnalisé...</b></p></td>
   <td>
    <p><b>Si vous choisissez Correspondant au secteur...</b><br></p></td>
  </tr>
  <tr>
   <td>
    <p>Vous pouvez choisir au maximum un champ actif interne et externe.</p></td>
   <td>
    <p>Vous pouvez choisir au maximum cinq champs et au moins un champ. Par défaut, l’option <b>Profil </b>est sélectionné.</p></td>
  </tr>
 </tbody>
</table>

S’il y a moins de 1 000 élèves, l’ensemble du compte est considéré comme une seule étendue. Il s’agit spécifiquement du type de formation personnalisée. Si le compte compte compte moins de 1 000 utilisateurs, il considère le compte complet comme sa portée.

>[!NOTE]
>
>Case à cocher **Exploration des compétences** a été déplacé dans Paramètres > Général.

Cette option est activée et grisée si vous choisissez l’expérience immersive. Cette case à cocher est activée uniquement pour l’expérience classique.

![](assets/option-immersive.png)

*Sélection pour une expérience classique*

La mise en page immersive est définie par défaut pour tous les nouveaux comptes. La mise en page est contrôlée par des widgets qu’un administrateur peut activer ou désactiver. En fonction du positionnement des widgets, cela se reflète sur la page d’accueil de l’élève.

Voici les widgets que vous pouvez activer/désactiver.

Vous pouvez ainsi prévisualiser l’interface utilisateur des élèves avant sa mise en ligne.

Pour les comptes existants, l’option **Immersif** sera **DÉSACTIVÉ**. Il est activé pour les nouveaux comptes avec Social et Ludification activés.

![](assets/immersive-layout-widgets.png)

*Aperçu de l’interface utilisateur de l’élève*

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Widget</b></p></td>
   <td>
    <p><b>Description</b></p></td>
  </tr>
  <tr>
   <td>
    <p>En-tête</p></td>
   <td>
    <p><b>Qu’est-ce qu’une en-tête et comment puis-je personnaliser l’en-tête des élèves ? </b><br></p>
    <p>C’est une bannière de bienvenue pour les élèves. La bannière peut être une image ou une vidéo. Vous pouvez cibler l’en-tête sur des groupes d’utilisateurs spécifiques et un élève peut afficher l’en-tête dès qu’il accède à la page d’accueil. Un groupe d’utilisateurs peut voir plusieurs heros images ou vidéos en fonction de la formule cible définie par l’administrateur. </p>
    <p>Voici comment un administrateur charge une bannière :</p>
    <ol>
     <li>Dans le panneau de gauche, cliquez sur <b>Annonce</b>.<br></li>
     <li>Dans le coin supérieur droit de la page, cliquez sur <b>Ajouter</b>.</li>
     <li>À partir de <b>Type </b>dans la liste déroulante, sélectionnez <b>En tant qu’en-tête</b>.</li>
     <li>Écrivez un message qui apparaîtra dans l’en-tête.</li>
     <li>Chargez une image ou une vidéo.</li>
     <li>Choisir le public cible. Sélectionnez un groupe d’utilisateurs ou une formation où l’en-tête sera affiché.</li>
     <li>Enregistrez l’annonce de l’en-tête.</li>
    </ol></td>
  </tr>
  <tr>
   <td>
    <p>Mon apprentissage</p></td>
   <td>
    <p>Affiche les objets d’apprentissage récemment visités par l’élève. </p></td>
  </tr>
  <tr>
   <td>
    <p>Calendrier</p></td>
   <td>
    <p>Affiche différentes formations en salle de classe et en salle de classe virtuelle à venir pour les élèves par mois. Celles auxquelles l’élève peut s’inscrire ou a déjà été inscrit s’affichent, y compris les formations approuvées par le responsable. </p></td>
  </tr>
  <tr>
   <td>
    <p>Ludification</p></td>
   <td>
    <p>Affiche le tableau des scores en fonction des activités d’apprentissage.</p></td>
  </tr>
  <tr>
   <td>
    <p>Apprentissage par les réseaux sociaux</p></td>
   <td>
    <p>Répertorie les activités et les publications des utilisateurs qui se trouvent dans la même portée d'utilisateur que l'élève. </p></td>
  </tr>
  <tr>
   <td>
    <p>Recommandé par l’organisation</p></td>
   <td>
    <p>Lorsqu’il est activé, ce widget recommande des formations à des groupes d’utilisateurs spécifiques. Chaque groupe d’utilisateurs peut cibler une ou plusieurs formations et le plan cible serait basé sur un calendrier. <br></p>
    <ul>
     <li>
      <p>Tout d’abord, l’administrateur <a href="announcements.md#recommendation">crée une annonce</a> de type <b>Comme recommandation</b> puis sélectionne la formation requise et utilise des groupes. Un élève appartenant à un groupe d’utilisateurs pourra voir la formation recommandée.</p></li>
     <li>
      <p>Deuxièmement, l’administrateur peut également décider si les recommandations entrent en vigueur immédiatement ou à une date spécifiée.</p></li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Recommandation fondée sur le domaine d'intérêt</p></td>
   <td>
    <p>Affiche les objets d’apprentissage en fonction de la zone d’intérêt choisie par l’élève. La recommandation est pilotée par un algorithme de machine learning.</p></td>
  </tr>
  <tr>
   <td>
    <p>Parcourir par catalogue<br></p></td>
   <td>
    <p>Affiche les catalogues sous forme de vignettes sur la page d’accueil. </p></td>
  </tr>
  <tr>
   <td>
    <p>Recommandation basée sur l’activité des pairs<br></p></td>
   <td>
    <p>Affiche la formation en fonction de ce que suivent les pairs d’un élève. Là encore, il est piloté par un algorithme de machine learning.</p></td>
  </tr>
 </tbody>
</table>

Une fois les modifications enregistrées, la page d’accueil de l’élève reflète toutes les modifications.

Lorsque l’élève se connecte à l’application de l’élève via un navigateur, il peut voir la disposition immersive suivante :

<table>
 <tbody>
  <tr>
   <td>
    <p><strong>Page d’accueil</strong></p><img src="assets/home-page1.png"></td>
   <td>
    <p><strong>Liste Mon apprentissage</strong></p><img src="assets/learning-list.jpg"></td>
   <td>
    <p><strong>Afficher le catalogue</strong></p><img src="assets/catalog-new.jpg"></td>
  </tr>
 </tbody>
</table>

*Affichage de la mise en page immersive pour différentes sections sur la page d’accueil*

## Option de mise en page classique {#classiclayoutoption}

La disposition de l’interface utilisateur qui a toujours existé jusqu’à présent est désormais appelée Disposition classique. Lorsque vous choisissez cette option, la page d’accueil de l’élève revient à la mise en page classique.

![](assets/classic-layout.png)

*Aperçu de la mise en page classique*

## Configuration des paramètres de recommandation {#configurerecommendationsettings}

Activé **Branding** > **Généralités**, vous pouvez configurer les portées des recommandations pour les élèves internes et externes et permettre aux élèves de choisir des compétences sur la page d’accueil de l’élève.

Sur la **Généralités** , vous disposez des options suivantes :

<table>
 <tbody>
  <tr>
   <td>
    <p>Nom de l’organisation</p></td>
   <td>
    <p>Nom de l’organisation à laquelle l’élève appartient.</p></td>
  </tr>
  <tr>
   <td>
    <p>Sous-domaine</p></td>
   <td>
    <p>Sous-domaine de l’organisation.</p></td>
  </tr>
  <tr>
   <td>
    <p>Style de logo</p></td>
   <td>
    <p>Voici comment votre logo et le nom de votre société apparaîtront sur Learning Manager.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Thèmes</p></td>
   <td>
    <p>Thème appliqué à Learning Manager.</p></td>
  </tr>
  <tr>
   <td>
    <p>Personnaliser</p></td>
   <td>
    <p>Adobe Learning Manager vous permet de personnaliser votre compte afin d’améliorer l’expérience de vos utilisateurs.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Page d’accueil de l’élève</p></td>
   <td>
    <p>Choisissez l’une des options suivantes : <b>Classique </b>ou <b>Immersif</b>. Si vous choisissez Immersive, d’autres options apparaissent.</p></td>
  </tr>
  <tr>
   <td>
    <p>Type de formation<br></p></td>
   <td>
    <p>Choisissez l’une des options suivantes : <b>Personnalisé </b>ou <b>Correspondant au secteur</b>. S’il y a moins de 1 000 élèves, l’ensemble du compte est considéré comme une seule étendue. La recommandation est basée sur tous les élèves.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Définition de la portée de la recommandation<br></p></td>
   <td>
    <p>Sélectionnez un ou plusieurs champs actifs. Pour <b>Personnalisé</b>, vous pouvez choisir au maximum un champ actif. Pour <b>Correspondant au secteur</b>, vous pouvez choisir au maximum cinq champs actifs.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Permettre à l’élève d’explorer les domaines d’intérêt</p></td>
   <td>
    <p>Uniquement pour l’expérience classique. Choisir <b>Oui </b>ou <b>Non</b>.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Inviter les utilisateurs à sélectionner des centres d’intérêt (compétences) <br></p></td>
   <td>
    <p>Uniquement pour l’expérience immersive. Choisir <b>Oui</b> ou <b>Non</b>. <br></p></td>
  </tr>
 </tbody>
</table>
