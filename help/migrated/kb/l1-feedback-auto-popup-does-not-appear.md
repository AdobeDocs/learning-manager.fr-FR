---
jcr-language: en_us
title: La fenêtre contextuelle automatique de retour d’informations L1 ne s’affiche pas
description: Comment résoudre l’erreur « La fenêtre contextuelle automatique de retour d’informations L1 n’apparaît pas »
contentowner: saghosh
exl-id: 47edcd7f-e332-4a75-a025-fd07737d0b70
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 76%

---

# La fenêtre contextuelle automatique de retour d’informations L1 ne s’affiche pas

## Le problème 

La fenêtre contextuelle automatique de retour d’informations L1 ne s’affiche pas pour un élève une fois le cours terminé.

## Cause

Il peut arriver qu’un élève ne reçoive pas de retour d’informations L1 après avoir terminé un cours spécifique ou qu’il reçoive un message comme indiqué ci-dessous :

![](assets/l1-feedback.png)

*Impossible de recevoir le retour d&#39;informations L1*

Cela peut se produire pour les raisons suivantes :

1. Le retour d’informations n’est pas défini pour s’afficher une fois le cours terminé.
1. Les rappels sont désactivés.
1. Un rappel est planifié pour s’afficher après un certain temps.

## Résolution

1. Assurez-vous que l&#39;option « Afficher le questionnaire immédiatement après la fin du cours » est activée dans **Cours** > **Instances** > **Retour d&#39;informations L1**.
   <!--![](assets/l1-feedback.png)-->
1. En tant qu’administrateur, accédez à **Paramètres > Retour d’informations**. Vérifiez quand le rappel est planifié. S’il est planifié **Dès la fin du cours**, remplacez l’option par **À l’issue du cours**.
1. Activez les modèles de courrier électronique suivants : **Modèles de courrier électronique > Rappels et mises à jour > Demander le retour d&#39;informations de l&#39;élève pour le cours**. Si l’option est désactivée, activez-la, puis testez-la.
1. Si les étapes ci-dessus ne fonctionnent pas, supprimez le rappel présent dans **Administrateur > Paramètres > Retour d’informations**. Créez-en un pour « À l’issue du cours » et définissez la périodicité en fonction des besoins.
