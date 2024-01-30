---
jcr-language: en_us
title: Configuration système
description: Configuration requise pour Adobe Learning Manager
contentowner: dvenkate
source-git-commit: 1b90528ec5675c67dcc9b8d86f2a5b8b82f7f5e4
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 65%

---


# Configuration requise pour Adobe Learning Manager

## Windows {#windows}

Microsoft Windows 7, 8, 10 (versions 64 bits uniquement).

## macOS {#macos}

macOS X 10.12, 10.13, 10.14, 10.15

## Mémoire RAM

8 Go de RAM.

## Affichage

Résolution minimale prise en charge : 1024 x 720.

## Espace disque

5 Go minimum d’espace disque disponible.

## Enregistrement

* Microphone requis pour l’enregistrement audio.
* Webcam requise pour l’enregistrement vidéo.

## Divers

Connexion Internet active et compte d’élève Adobe Learning Manager requis pour utiliser l’application.

## Spécification de navigateur

La page d’accueil avec mise en page immersive n’est pas prise en charge dans le navigateur IE 11.

* Google Chrome version 43 et ultérieure.
* Dernières versions d’Edge, de Safari (version 13 et ultérieure), et de Firefox.
* Internet Explorer version 11 et ultérieure

## Taille recommandée des images {#recommendedsizeofimages}

* En-tête : 1 280 x 360 px.
* Image sur la carte du catalogue : 280 x 100 px
* Taille de la carte de formation : 300 x 240 px
* Bannière pour réseaux sociaux : 1600 x 240 px

## Ordinateur

### Système d’exploitation

Windows 10 et 11, macOS X 10.12, 10.13, 10.14, 10.15

### Processeur

Intel® CoreTM i5 ou plus rapide.

### Mémoire RAM

8 Go minimum requis.

### Résolution de l’écran

1366 x 768 pixels

### Espace disque

5 Go minimum d’espace disque disponible.

### Enregistrement

Un microphone est nécessaire pour l’enregistrement audio ; une webcam est nécessaire pour l’enregistrement vidéo.

## Application mobile

### Périphériques

* iOS : deux dernières versions majeures.
* Android : deux dernières versions majeures.

### Navigateurs

* Chrome sous Android.
* Safari sous iOS.

### Vitesse du réseau

* 1 Mbit/s

### Unité centrale, mémoire (min) des périphériques

* Qualcomm® Snapdragon™ 695 5G ou équivalent, 6 Go de mémoire

### Espace disque/scanner de code QR requis

* 250 Mo

>[!NOTE]
>
>Le navigateur mobile prend uniquement en charge le rôle d’élève dans **disposition immersive**.

>[!NOTE]
>
>L’application mobile Learning Manager prend uniquement en charge le rôle d’élève.

## Taille maximale du contenu {#maximumcontentsize}

La taille de fichier maximale pouvant être téléchargée est de 600 Mo.

>[!NOTE]
>
>Si la taille du fichier *user.csv* dépasse 100 Mo, l’importation de ce fichier peut entraîner un comportement inattendu de la part du navigateur. Le problème se produit car la mémoire du navigateur est insuffisante.

Nous vous recommandons d’importer des fichiers de grande taille *user.csv* à l’aide du workflow automatisé Box/Exavault. Pour en savoir plus, voir [Migration de fichiers](/help/migrated/integration-admin/feature-summary/migration-manual.md).


## Format de contenu pris en charge

### Téléchargement de modules {#moduleupload}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Type de contenu</b></p></td>
   <td>
    <p><b>Extensions</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Documents</p></td>
   <td>
    <p>« pdf », « docx », « doc », « xls », « xlsx »</p></td>
  </tr>
  <tr>
   <td>
    <p>Présentations PowerPoint</p></td>
   <td>
    <p>« pptx », « ppt »</p></td>
  </tr>
  <tr>
   <td>
    <p>Vidéos</p></td>
   <td>
    <p>« mp4 », « wmv », « 3gp », « 3g2 », « 3gp2 », « asf », « avi », « f4v », « h264 », « mpe », « mpeg », « mpg », « mpg2 », « m4v », « mov », « wmv »</p></td>
  </tr>
  <tr>
   <td>
    <p>SCORM 1.2</p></td>
   <td>
    <p>« zip »</p></td>
  </tr>
  <tr>
   <td>
    <p>SCORM 2004</p></td>
   <td>
    <p>« zip »</p></td>
  </tr>
  <tr>
   <td>
    <p>CAPI</p></td>
   <td>
    <p>« zip »</p></td>
  </tr>
  <tr>
   <td>
    <p>AICC</p></td>
   <td>
    <p>« zip »</p></td>
  </tr>
  <tr>
   <td>
    <p>Audio</p></td>
   <td>
    <p>« mp3 », « wav », « aac », « m4a », « wma », « vorbis », « pcm », « eac3 », « amr », « ac3 »</p></td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p><strong>Badges</strong></p></td>
   <td>
    <p>« png », « jpg », « jpeg », « gif »</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Photo de profil utilisateur</strong></p></td>
   <td>
    <p>« png », « jpg », « jpeg », « gif »</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Logo de société</strong></p></td>
   <td>
    <p>« png », « jpg », « jpeg », « bmp », « gif »</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Téléchargement de certifications</strong></p></td>
   <td>
    <p> « png », « jpg », « jpeg », « pdf », « doc », « docx », « gif »</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Ressources / pièces jointes de cours</strong></p></td>
   <td>
    <p> Tous les formats de fichiers</p></td>
  </tr>
 </tbody>
</table>

## Spécifications de hauteur et de largeur pour le téléchargement d’éléments {#heightandwidthspecificationforuploadingelements}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Éléments</b></p></td>
   <td>
    <p><b>Taille</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Badge sur le tableau des réussites de l’élève</p></td>
   <td>
    <p>40 x 40 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Badge étendu sur l’application de l’élève</p></td>
   <td>
    <p>90x90 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Photo de profil utilisateur sur le tableau des réussites de l’élève</p></td>
   <td>
    <p>100x100 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Photo de profil utilisateur sur le menu déroulant de déconnexion</p></td>
   <td>
    <p>42x42 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Logo de société dans l’en-tête</p></td>
   <td>
    <p>45 pixels de hauteur, la largeur est calculée en conséquence.</p></td>
  </tr>
  <tr>
   <td>
    <p>Logo de l’entreprise sur la page d’accueil de Learning Manager</p></td>
   <td>
    <p>100 pixels de hauteur, la largeur est calculée en conséquence.</p></td>
  </tr>
 </tbody>
</table>

## Accessibilité

### Navigateurs et lecteurs d’écran pris en charge

Les combinaisons suivantes sont prises en charge :

* Chrome + NVDA
* Edge + Narrateur
* Mac Safari + VoiceOver

### Prise en charge du mode immersif mobile

Les éléments suivants sont pris en charge :

* Android + Talkback
* iOS + VoiceOver

## Exigences réseau {#networkrequirements}

Assurez-vous que les domaines tiers suivants sont ajoutés à la liste blanche si vous êtes connecté à un réseau comportant des restrictions.

* &#42;.adobe.com
* &#42;.boltdns.net
* &#42;.brightcove.com
* &#42;.amazon.com
* &#42;.adobedtm.com
* &#42;.typekit.net
* &#42;.demdex.net
* &#42;.brightcove.net
* &#42;.zencdn.net
* &#42;.cloudflare.com
* bam.nr-data.net
* &#42;.akamaihd.net


### Cas étendus spécifiques {#specificextendedcases}

<table>
 <tbody>
  <tr>
   <th>Fonctionnalité</th>
   <th>Services utilisés</th>
  </tr>
  <tr>
   <td>Connecteur FTP</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a></td>
  </tr>
  <tr>
   <td>Migration</td>
   <td><a href="https://www.box.com/" target="_blank">www.box.com</a><br><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a></td>
  </tr>
  <tr>
   <td>Connecteur Lynda</td>
   <td><a href="https://www.box.com/" target="_blank">www.box.com</a><br><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://www.lynda.com/" target="_blank">www.lynda.com</a></td>
  </tr>
  <tr>
   <td>Connecteur Harvard ManageMentor</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://myhbp.org" target="_blank">www.myhbp.org</a></td>
  </tr>
  <tr>
   <td>Connecteur getAbstract</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://www.getabstract.com/en/" target="_blank">www.getabstract.com  </a></td>
  </tr>
  <tr>
   <td>Connecteur Box</td>
   <td>Box Zones situées à Francfort</td>
  </tr>
  <tr>
   <td>Connecteur Mini Orange</td>
   <td>Mini Orange</td>
  </tr>
  <tr>
   <td>Connecteur Workday</td>
   <td>Workday</td>
  </tr>
  <tr>
   <td>Connecteur Blue Jeans<br></td>
   <td>Blue Jeans</td>
  </tr>
  <tr>
   <td>Microsoft Power BI</td>
   <td>Licence commerciale de Power BI prise en charge uniquement.</td>
  </tr>
 </tbody>
</table>

## Présentation technique {#technicaloverview}

[Présentation technique de Learning Manager](assets/learning-manager-technicaloverview.pdf)
