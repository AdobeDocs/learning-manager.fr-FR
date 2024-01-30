---
jcr-language: en_us
title: Le module est marqué comme incomplet à la fin du cours dans Adobe Learning Manager.
description: Même lorsqu’un élève a terminé un cours dans Adobe Learning Manager, le module est marqué comme incomplet.
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 53%

---



# Le module est marqué comme incomplet à la fin du cours dans Adobe Learning Manager.

## Problème

Même lorsqu’un élève a terminé un cours dans Adobe Learning Manager, le module est marqué comme incomplet.

## Cause

SCORM 2004 définit les critères de réussite et d&#39;achèvement et envoie les relevés pour les deux documents séparément.

Par exemple, supposons qu’un contenu soit défini avec un **Critères d’achèvement** sur 100 % des vues de diapositive et **Critères de réussite** défini sur « Quiz réussi ».

Un élève termine le cours, mais il échoue au quiz. Dans ce cas, la progression est de 100 %, mais le module est marqué comme incomplet, car l’élève ne répond pas aux **Critères de réussite**.

## Solution

Le problème est lié aux **Préférences** de rapport définies pour le projet. L’auteur doit vérifier les critères définis pour l’achèvement et le succès du cours.

Si des modifications sont nécessaires, l’auteur peut les effectuer à l’aide d’un outil de création de contenu, tel qu’Adobe Captivate Classic. L’auteur peut ensuite mettre à jour le module en conséquence.

![](assets/scorm.png)

*Afficher les préférences de création de rapports classiques du Captivate*
