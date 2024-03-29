---
description: Lisez ce qui suit pour savoir comment générer des fichiers HAR sur Google Chrome.
jcr-language: en_us
title: Génération d’un fichier HAR
contentowner: dvenkate
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 57%

---



# Génération d’un fichier HAR

Lisez ce qui suit pour savoir comment générer des fichiers HAR sur Google Chrome.

Pour générer un fichier HAR, procédez comme suit :

1. Ouvrez une fenêtre Google Chrome et ouvrez un nouvel onglet.
1. Ouvrez les outils de développement pour la page, cliquez avec le bouton droit de la souris et choisissez Inspecter.
1. Ouvrez l’onglet **[!UICONTROL Réseau]**. Assurez-vous que le bouton d’enregistrement rouge est actif. Activer le **[!UICONTROL Conserver le journal]** case.

   ![](assets/preserve-log-checkbox.png)

   *Cochez la case Conserver le journal dans l’onglet Réseau*

1. Connectez-vous à [Learning Manager](https://learningmanager.adobe.com/acapindex.html) en utilisant vos informations d’identification et suivez le cours. Faites toutes les opérations qui engendreront le problème.
1. Dans les outils de développement, cliquez avec le bouton droit de la souris et sélectionnez **Enregistrer tout au format HAR avec le contenu**.

   Dans certaines versions de Google Chrome, vous devrez peut-être sélectionner **[!UICONTROL Copier]** > **[!UICONTROL Tout copier au format HAR]**.

   ![](assets/copy-hra.png)

   *Copier tous les fichiers HAR*

1. Collez le contenu copié dans un fichier de bloc-notes. Enregistrer sur le bureau sous **logs.har** et envoyez-le par e-mail à l’Adobe.
