---
jcr-language: en_us
title: Intégration de Learning Manager à Slack
description: Intégration de Learning Manager à Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 44%

---



# Intégration de Learning Manager à Slack

Nous avons **supprimé** **Slack** en tant que connecteur dans Learning Manager. Vous n’aurez plus accès au connecteur de Slack.

En tant qu’utilisateur Slack, vous pouvez installer l’application Adobe Learning Manager depuis le répertoire d’applications Slack dans vos équipes Slack et explorer le contenu Learning Manager directement dans Slack. Vous pouvez interagir avec Primebot pour rechercher de nouveaux cours, afficher des recommandations et être informé des échéances à venir dans Learning Manager. Vous pouvez également vous inscrire et accéder directement à votre apprentissage dans Slack.

L’application Learning Manager pour Slack n’est pas prise en charge dans une instance Azure de Learning Manager.

## Installation de l’application Adobe Learning Manager {#installingadobecaptivateprimeapp}

En tant qu’élève, vous pouvez installer l’application CP Prime dans votre compte Slack. Pour installer l’application dans votre compte Slack, ouvrez le répertoire d’applications et recherchez Learning Manager. Téléchargez et installez l’application. Si l’application n’est pas approuvée dans votre compte, contactez votre administrateur d’intégration pour obtenir son approbation. Si elle est déjà approuvée, vous pourrez vous connecter.

## Approbation de la connexion de l’élève en tant qu’administrateur d’intégration {#approvinglearnersigninasanintegrationadmin}

En tant qu’administrateur d’intégration, pour approuver l’autorisation d’un élève à utiliser l’application Prime sur le Slack, procédez comme suit.

1. Sélectionnez **[!UICONTROL Applications]** dans le volet de gauche et cliquez sur l’onglet **[!UICONTROL Applications fournies]**.

   ![](assets/featuredapps.jpg)

1. Cliquez sur la vignette **[!UICONTROL Slack]**, la page d’intégration Slack s’ouvre. Cliquez sur **[!UICONTROL Approuver]** en haut à droite pour approuver l&#39;application.

   ![](assets/approval.png)

1. Revenez à la page **[!UICONTROL Applications]**. Une fois approuvé, Slack devrait apparaître dans l&#39;onglet **[!UICONTROL Applications externes]**.
1. Les élèves peuvent désormais se connecter à leur compte Prime via Slack.

## Fonctionnalités de Primebot {#primebotfunctionalities}

Vous pouvez maintenant commencer à interagir avec le Primebot. Les fonctionnalités du bot sont les suivantes.

1 - Commande

&#42;/prime&#42; peut être utilisé pour des requêtes ponctuelles et précises concernant votre compte Adobe Learning Manager.

Les sous-commandes disponibles sont :

/prime find `<query>` - rechercher des cours, des certifications, etc.

/prime recommend : affichage de recommandations

/prime deadlines : affichage des dates d’échéance passées et à venir

/prime enrollments : affichage des inscriptions

/prime skills : affichage des compétences

/prime notifications : affichage des notifications

/prime catalogs : affichage des catalogues

/prime invite : [l’administrateur uniquement] invite les utilisateurs du Slack de l’équipe actuelle à tester primebot

/prime profile : affichage de profils

/prime logout : déconnexion de votre compte Prime dans cette équipe Slack

/prime help : affichage des messages d’aide

2 - Recommander

Vous pouvez essayer une phrase telle que `show my recommendations` pour obtenir une liste personnalisée de cours, de certifications et de programmes d’apprentissage recommandés à partir de votre compte Adobe Learning Manager.

3 - Rechercher

Vous pouvez essayer des expressions telles que `search for machine learning` ou `search for artificial intelligence`. Vous pouvez spécifier le type d’objet d’apprentissage à l’aide d’expressions telles que `search for machine learning certifications`, `search for artificial intelligence courses` ou `search for adobe photoshop job aids`. Vous pouvez également effectuer une recherche dans un catalogue en utilisant des expressions telles que `search for machine learning in Lynda catalog`.

4 - Délais

Utilisez une expression comme `show my deadlines` pour obtenir une liste des échéances en retard et à venir à partir de votre compte Adobe Learning Manager. Vous pouvez filtrer les échéances passées ou à venir avec des expressions telles que `show my overdue deadlines` ou `show my upcoming deadlines`.
