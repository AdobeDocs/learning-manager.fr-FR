---
jcr-language: en_us
title: La fenêtre contextuelle automatique de retour d’informations L1 ne s’affiche pas
description: Comment résoudre l’erreur « La fenêtre contextuelle automatique de retour d’informations L1 n’apparaît pas »
contentowner: saghosh
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---



# La fenêtre contextuelle automatique de retour d’informations L1 ne s’affiche pas

## Problème

La fenêtre contextuelle automatique de retour d’informations L1 ne s’affiche pas pour un élève après avoir terminé le cours.

## Cause

Parfois, il peut arriver qu’un élève ne reçoive pas le retour d’informations L1 après avoir terminé un cours particulier ou qu’il reçoive un message comme indiqué ci-dessous :

![](assets/l1-feedback.png)

*Impossible de recevoir le retour d&#39;informations L1*

Cela peut se produire pour les raisons suivantes :

1. Les commentaires ne sont pas configurés pour s’afficher une fois le cours terminé.
1. Les rappels sont désactivés.
1. Un rappel est planifié pour s’afficher après un certain temps.

## Résolution

1. Assurez-vous que l’option « Afficher le questionnaire immédiatement après la fin du cours » est activée dans **Cours** > **Instances** > **Retour d&#39;informations L1**.
   <!--![](assets/l1-feedback.png)-->
1. En tant qu’administrateur, accédez à **Paramètres > Retour d’informations**. Vérifiez quand le rappel est planifié. Au cas où il est prévu **Après** achèvement, remplacer l’option par **En cours** achèvement.
1. Activez les modèles de courrier électronique suivants : **Modèles de courrier électronique > Rappels et mises à jour > Demander le retour d’informations de l’élève pour le cours**. Si l’option est désactivée, activez-la, puis testez-la.
1. Si les étapes ci-dessus ne fonctionnent pas, supprimez le rappel présent dans **Administrateur > Paramètres > Retour d’informations**. Créez-en un pour « À l’issue du cours » et définissez la périodicité en fonction des besoins.
