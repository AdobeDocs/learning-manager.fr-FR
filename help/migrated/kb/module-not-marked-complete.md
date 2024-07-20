---
jcr-language: en_us
title: Le module est marqué comme incomplet à la fin du cours dans Adobe Learning Manager.
description: Même lorsqu’un élève a terminé un cours dans Adobe Learning Manager, le module est marqué comme incomplet.
contentowner: nluke
exl-id: c0f14f2e-733a-4b4f-a2c2-4c0b33a15fa1
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 53%

---

# Le module est marqué comme incomplet à la fin du cours dans Adobe Learning Manager.

## Problème

Même lorsqu’un élève a terminé un cours dans Adobe Learning Manager, le module est marqué comme incomplet.

## Cause

SCORM 2004 définit les critères de réussite et d&#39;achèvement et envoie les relevés pour les deux documents séparément.

Par exemple, imaginons un contenu dont les **critères d’achèvement** correspondent à des vues de diapositive à 100 % et dont les **critères de réussite** sont définis sur « Quiz réussi ».

Un élève termine le cours, mais il échoue au quiz. Dans ce cas, la progression est de 100 %, mais le module est marqué comme incomplet, car l&#39;élève ne satisfait pas aux **critères de réussite**.

## Solution

Le problème est lié aux **Préférences** de rapport définies pour le projet. L’auteur doit vérifier les critères définis pour l’achèvement et le succès du cours.

Si des modifications sont nécessaires, l’auteur peut les effectuer à l’aide d’un outil de création de contenu, tel qu’Adobe Captivate Classic. L’auteur peut ensuite mettre à jour le module en conséquence.

![](assets/scorm.png)

*Afficher les préférences de création de rapports classiques du Captivate*
