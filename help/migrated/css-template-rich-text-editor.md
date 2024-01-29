---
jcr-language: en_us
title: Modèle CSS pour l’éditeur de texte enrichi
description: Modèle CSS pour l’éditeur de texte enrichi
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---



# Modèle CSS pour l’éditeur de texte enrichi

## Pourquoi la feuille de style CSS est-elle requise ?

Le texte enrichi est composé d’un balisage de HTML. Le rendu du balisage tel quel entraînera l’application du style par défaut par le navigateur. Souvent, cela ne correspond pas aux directives de style de l’entreprise. Une feuille de style CSS est requise pour respecter les directives.

## Style par défaut

La feuille de style CSS jointe contient le style appliqué par Learning Manager. Le style est modifié en fonction de la majorité des cas d’utilisation. Téléchargez le fichier CSS joint et importez-le dans votre application web en fonction de vos conventions et de votre système de build. Les classes CSS définies sont des espaces de noms sous la classe ql-editor et elles n’interfèrent pas avec vos styles existants.

## Personnalisation des styles

Le style par défaut peut ne pas répondre aux besoins de tous. Les personnalisations peuvent être effectuées en remplaçant la feuille de style CSS fournie. Tout le style est enveloppé sous ql-editor en tant que sélecteurs descendants. Les classes suivantes sont utilisées :

* **Retrait**: li.ql-indent-$number. $number varie de 1 à 9
* **taille**: ql-size-small, ql-size-large, ql-size-énorme
* **alignement**: ql-align-center, ql-align-validate, ql-align-right
* **couleur**: ql-color-$color. $color = blanc, rouge, orange, jaune, vert, bleu, violet
* **arrière plan**: ql-bg-$color. $color = noir, rouge, orange, jaune, vert, bleu, violet
* **balises html**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Fichier CSS à utiliser pour la personnalisation.](assets/ql-headless.css)
