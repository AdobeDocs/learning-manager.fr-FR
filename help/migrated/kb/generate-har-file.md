---
description: Lisez ce qui suit pour savoir comment générer des fichiers HAR sur Google Chrome.
jcr-language: en_us
title: Génération d’un fichier HAR
contentowner: dvenkate
exl-id: 99fe78e8-b5e7-40a7-b9a5-efc2382de993
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 65%
---
# Génération d’un fichier HAR

Lisez ce qui suit pour savoir comment générer des fichiers HAR sur Google Chrome.

Pour générer un fichier HAR, procédez comme suit :

1. Ouvrez une fenêtre Google Chrome et ouvrez un nouvel onglet.
1. Ouvrez les outils de développement pour la page, cliquez avec le bouton droit de la souris et choisissez Inspecter.
1. Ouvrez l’onglet **[!UICONTROL Réseau]**. Assurez-vous que le bouton d’enregistrement rouge est actif. Activez la case à cocher **[!UICONTROL Conserver le journal]**.

   ![](assets/preserve-log-checkbox.png)

   *Cochez la case Conserver le journal dans l&#39;onglet Réseau*

1. Connectez-vous à [Learning Manager](https://learningmanager.adobe.com/acapindex.html) en utilisant vos informations d’identification et suivez le cours. Faites toutes les opérations qui engendreront le problème.
1. Dans les outils de développement, faites un clic droit et sélectionnez **Enregistrer tout au format HAR avec le contenu**.

   Dans certaines versions de Google Chrome, vous devrez peut-être sélectionner **[!UICONTROL Copier]** > **[!UICONTROL Copier tout au format HAR]**.

   ![](assets/copy-hra.png)

   *Copier tous les fichiers HAR*

1. Collez le contenu copié dans un fichier de bloc-notes. Enregistrez-le sur le bureau sous le nom de **logs.har** et envoyez-le par e-mail à l&#39;Adobe.
