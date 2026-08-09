---
description: Découvrez comment le compositeur de contenu gère les mises à jour de cours dans Adobe Learning Manager, comment la republication crée une nouvelle version de module et comment les auteurs ALM mettent à jour les cours existants pour utiliser la dernière version.
jcr-language: en_us
title: Contrôle de version de module dans Adobe Learning Manager
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---


# Contrôle de version de module dans Adobe Learning Manager

Les documents sources changent au fil du temps - une politique est révisée, un MON obtient une nouvelle version, une présentation est mise à jour. Le compositeur de contenu et ALM gèrent une actualisation en tant que changement de version et non en tant que modification sur place. Les cours publiés précédemment continuent donc à fonctionner pendant que vous mettez à jour le module sous-jacent.

Lorsque vous republiez, Adobe Learning Manager charge le module existant en tant que nouvelle version dans la bibliothèque de contenu, en incrémentant le numéro de version du module d’une unité.

1. Dans le compositeur de contenu, mettez à jour les fichiers source et régénérez les leçons affectées (voir Mettre à jour un cours lorsque la source change), puis republiez.

2. La publication de la mise à jour ne remplace pas le module existant. Elle ajoute une nouvelle version à côté dans la bibliothèque de contenu ALM.

3. Un auteur ALM doit explicitement mettre à jour chaque cours ALM qui utilise le module pour pointer vers la nouvelle version ; les cours existants continuent de référencer la version avec laquelle ils ont été créés jusqu&#39;à ce qu&#39;un auteur ALM effectue cette modification.

4. Les élèves qui ont déjà terminé le cours sous la version précédente conservent leur enregistrement d’achèvement existant. La nouvelle version s’applique aux élèves inscrits après la mise à jour du cours ALM.

Passez en revue les leçons régénérées dans le compositeur de contenu avant de publier à nouveau. La régénération peut ajuster du texte, des images ou des questions de quiz précédemment modifiés dans les leçons affectées.
