---
jcr-language: en_us
title: Accessibilité dans Adobe Learning Manager
description: Ce document décrit la prise en charge de l’accessibilité fournie par le système de gestion d’apprentissage d’Adobe Learning Manager pour les élèves présentant un handicap. Il fournit également aux utilisateurs des options de navigation et des fonctionnalités d’accessibilité sur la plate-forme.
contentowner: saghosh
source-git-commit: c4d06af2eee167677fef050a3f2885dfd4c91446
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 71%

---


# Accessibilité dans Adobe Learning Manager

Ce document décrit la prise en charge de l’accessibilité fournie par le système de gestion d’apprentissage d’Adobe Learning Manager pour les élèves présentant un handicap. Il fournit également aux utilisateurs des options de navigation et des fonctionnalités d’accessibilité sur la plate-forme.

Learning Manager suit les normes d’accessibilité WCAG 2.1 de niveau A et AA de W3C pour la plateforme.

Le rôle Élève de Adobe Learning Manager permet aux élèves de parcourir la plateforme et de tirer parti des fonctionnalités d’accessibilité clés suivantes :

* Lecteur d’écran
* Clavier
* Sous-titres
* Autres

## Prise en charge des lecteurs d’écran {#supportforscreenreaders}

Adobe Learning Manager prend en charge les lecteurs d’écran tels que NVDA, JAWS et Voice-over sur les ordinateurs de bureau, Talkback et Voice-over sur les appareils mobiles, qui permettent aux élèves de lire le texte sur la plateforme Learning Manager et de naviguer en conséquence.

Voici la combinaison lecteur d’écran et navigateur que nous prenons en charge sur ordinateur de bureau :

<table>
 <tbody>
  <tr>
   <td>
    <p style="text-align: left;"><b>Système d’exploitation</b></p></td>
   <td>
    <p style="text-align: left;"><b>Navigateur</b></p></td>
   <td>
    <p style="text-align: left;"><b>Lecteur d’écran</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Windows</p></td>
   <td>
    <p>Chrome</p></td>
   <td>
    <p>NVDA</p></td>
  </tr>
  <tr>
   <td>
    <p>Windows</p></td>
   <td>
    <p>Firefox</p></td>
   <td>
    <p>Jaws</p></td>
  </tr>
  <tr>
   <td>
    <p>macOS</p></td>
   <td>
    <p>Safari</p></td>
   <td>
    <p>VoiceOver</p></td>
  </tr>
  <tr>
   <td>
    <p>Android</p></td>
   <td>
    <p>Chrome</p></td>
   <td>
    <p>Talkback</p></td>
  </tr>
  <tr>
   <td>
    <p>iOS</p></td>
   <td>
    <p>Safari</p></td>
   <td>
    <p>VoiceOver</p></td>
  </tr>
 </tbody>
</table>

## Prise en charge de la navigation via le clavier {#supportforkeyboardnavigation}

Les élèves peuvent utiliser les touches standard pour parcourir les pages avec ou sans lecteur d’écran. Ils peuvent ainsi parcourir les éléments de la page et lire le contenu à l’aide d’un lecteur d’écran.

En outre, Learning Manager prend en charge les raccourcis clavier suivants :

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Fonctionnalité</b></p></td>
   <td>
    <p><b>Windows</b></p></td>
   <td>
    <p><b>macOS</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Ignorer la navigation</p></td>
   <td>
    <p>Alt+1</p></td>
   <td>
    <p>Option+1</p></td>
  </tr>
  <tr>
   <td>
    <p>Fonctionnalité<br></p></td>
   <td>
    <p>Windows<br></p></td>
   <td>
    <p>macOS<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Notification à l’utilisateur<br></p></td>
   <td>
    <p>Alt+2<br></p></td>
   <td>
    <p>Option+2<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Paramètres du profil<br></p></td>
   <td>
    <p>Alt + 3<br></p></td>
   <td>
    <p>Option+3<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Recherche globale<br></p></td>
   <td>
    <p>Alt+4<br></p></td>
   <td>
    <p>Option+4<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Ignorer la navigation<br></p></td>
   <td>
    <p>Alt+1<br></p></td>
   <td>
    <p>Option+1<br></p></td>
  </tr>
 </tbody>
</table>

## Commandes du lecteur

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Fonctionnalité</b></p></td>
   <td>
    <p><b>Windows</b></p></td>
   <td>
    <p><b>macOS</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Lecture/Pause</p></td>
   <td>
    <p>Alt+P</p></td>
   <td>
    <p>Option+P</p></td>
  </tr>
  <tr>
   <td>
    <p>Alt+V</p></td>
   <td>
    <p>Option+V</p></td>
   <td>
    <p>Volume</p></td>
  </tr>
  <tr>
   <td>
    <p>Alt+M</p></td>
   <td>
    <p>Option+M</p></td>
   <td>
    <p>Plein écran</p></td>
  </tr>
 </tbody>
</table>

## Autre prise en charge {#supportforcolorcontrast}

Le rôle Élève dans Learning Manager prend en charge plusieurs autres fonctionnalités d’accessibilité, notamment :

1. La structure sémantique des pages du rôle d’élève, y compris l’en-tête, le balisage de liste, les titres descriptifs, etc., est fournie.
1. La prise en charge du zoom du navigateur jusqu’à 200 % sans perte de contenu ou de fonctionnalité est maintenue pour le rôle d’élève.
1. Le contraste de couleur des éléments textuels et non textuels est conservé pour le rôle d’élève. Pour une meilleure expérience, utilisez le [thème dynamique](/help/migrated/administrators/feature-summary/themes.md).
1. Prise en charge des modèles de conception WAI ARIA de W3C pour maintenir la cohérence et les meilleures pratiques du secteur.

Pour plus d’informations, voir :

* [Rapport de conformité d’accessibilité pour un élève](https://www.adobe.com/fr/accessibility/compliance/adobe-captivate-prime-web-2019-learner-portal-acr.html)
* [Rapport de conformité d&#39;accessibilité pour tous les rôles](https://www.adobe.com/fr/accessibility/compliance/adobe-captivate-prime-web-2019-acr.html)

## Workflows principaux de Learning Manager (rôle Élève) {#captivateprimetopworkflowslearnerrole}

Voyons comment les fonctionnalités d’accessibilité vous aident à naviguer dans certaines fonctionnalités clés pour les élèves dans Learning Manager.

Utilisez la touche `kbd Tab` pour naviguer dans les éléments de la page. Utilisez la touche `kbd Shift + Tab` pour inverser le sens de la navigation. La mise en évidence du clavier est indiquée par un contour bleu affiché autour d’un élément. Un lecteur d’écran doit lire le texte de l’élément mis en évidence.

## Rechercher une formation dans Learning Manager {#searchforatrainingincaptivateprime}

1. Utilisez ces repères pour naviguer et atteindre la zone de recherche en haut à droite de la page d’accueil.
1. Saisissez du texte à l’aide du clavier. Les résultats de la recherche apparaîtront.
1. Utilisez les flèches du clavier `kbd Up/Down` pour parcourir les résultats ou appuyez sur `kbd ENTER` pour afficher tous les résultats.

1. Une fois la formation identifiée, appuyez sur `kbd ENTER` pour accéder à la page de formation.

## Suivre une formation dans Adobe Learning Manager {#consumeatraininginadobecaptivateprime}

1. Une fois qu&#39;une formation est identifiée, utilisez `kbd Tab` ou `kbd Shift + Tab` pour accéder au bouton S&#39;inscrire/Démarrer. Le statut du bouton dépend de votre statut d’inscription pour cette formation.

1. Appuyez sur `kbd ENTER` pour commencer la formation.
1. Voici les commandes qui apparaissent quel que soit le type de contenu :

   * Table des matières
   * Notes
   * Bouton Lecture/Pause
   * Plein écran
   * Bouton Fermer
   * Paramètres
   * Libellé du nom du module

1. Voici les commandes qui apparaissent en fonction du type de contenu :

   * VIDÉO : commandes Avance, Arrière, Curseur.
   * CONTENU DU DOCUMENT - Numéro de page, Page précédente, Page suivante, Zoom avant, Zoom arrière.
   * eLEARNING : bouton Sous-titres.

1. Appuyez sur les commandes clavier `kbd Tab` ou `kbd Shift + Tab` pour parcourir les commandes et appuyez sur `kbd ENTER` pour activer/désactiver un contrôle.

1. Pour le type DOCUMENT, utilisez les commandes fléchées comme `kbd UP/DOWN` pour faire défiler le document.

## Prise en charge de l’accessibilité pour des besoins spécifiques

Examinons les fonctionnalités d’accessibilité que les élèves peuvent utiliser en fonction de leurs besoins spécifiques.

### Utilisateurs sourds ou malentendants

* Utilisez les sous-titres pour sourds et malentendants disponibles dans le contenu créé à l’aide de l’outil de création Adobe Captivate.
* Pour les vidéos, les auteurs peuvent encoder les vidéos avec du texte de sous-titre pour sourds et malentendants. Ces vidéos contiennent des sous-titres pour sourds et malentendants intégrés et peuvent être visionnés par les élèves.
* Learning Manager permet de charger des fichiers WebVTT de sous-titres pour le contenu vidéo. Pour plus d&#39;informations, voir [*Charger un fichier WebVTT pour le sous-titrage*](authors/feature-summary/content-library.md#webvtt).

### Utilisateurs aveugles ou malvoyants

* Utilisez les raccourcis clavier et les commandes standard pour parcourir la page.
* Utilisez des lecteurs d’écran, comme ceux mentionnés plus haut, pour lire les informations sur la page Web.
* Utilisez des loupes pour zoomer sur l’écran et améliorer la lisibilité, et zoomez jusqu’à 200 % dans le navigateur pour lire le contenu.

### Utilisateurs ayant des difficultés à percevoir les couleurs

Le rôle Élève d’Adobe Learning Manager s’efforce de fournir aux utilisateurs une interface claire et lisible conformément aux normes WCAG 2.1.

Pour une meilleure expérience sur la page de l’élève, utilisez le [thème dynamique](/help/migrated/administrators/feature-summary/themes.md).

### Utilisateurs ayant une mobilité et une portée limitées

Adobe Learning Manager continue de se concentrer sur l’accessibilité et prévoit d’améliorer les capacités actuelles afin de permettre aux élèves du système de mieux parcourir le rôle « Élève ».

### Prise en charge des sous-titres pour sourds et malentendants pour les vidéos

Lors de la création d’un cours, les auteurs peuvent charger des fichiers webVTT avec les fichiers vidéo. Les élèves peuvent alors afficher les sous-titres lorsqu’ils regardent les vidéos.

## Améliorations de la future version {#whatwillbeaddressedinafuturerelease}

* Prise en charge des sous-titres pour sourds et malentendants pour les vidéos. Les auteurs devraient avoir la possibilité de télécharger des fichiers SRT avec les fichiers vidéo. Les élèves devraient pouvoir afficher des sous-titres pour sourds et malentendants pour les vidéos.
