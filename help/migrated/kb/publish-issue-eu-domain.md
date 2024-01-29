---
jcr-language: en_us
title: Impossible de publier sur le domaine Learning Manager EU
description: Impossible de publier d’Adobe Captivate vers le domaine UE d’Adobe Learning Manager dans Adobe Learning Manager.
contentowner: nluke
source-git-commit: 69ac8f8ce5a0c077f31569571f9d9fbf16ecb943
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---



# Impossible de publier sur le domaine Learning Manager EU {#unable-to-publish-to-learning-manager-eu-domain}

## Problème

Impossible de publier d’Adobe Captivate vers le domaine Adobe Learning Manager EU.

## Erreur

Aucun compte trouvé

## Description

Il existe des scénarios où les auteurs tentent de publier un cours d’Adobe Captivate vers Adobe Learning Manager. Cependant, ils ne peuvent pas le faire car ils voient un message d’erreur « Aucun compte trouvé ».

## Cause

Ce problème se produit car Adobe Captivate est par défaut configuré pour publier du contenu dans le domaine américain d’Adobe Learning Manager.

## Résolution :

Points à noter :

* Le cas échéant, fermez l’application Adobe Captivate.
* Vous devez disposer d’un accès administrateur sur votre ordinateur pour effectuer les étapes ci-dessous. Si vous n’avez pas d’accès administrateur, contactez votre équipe informatique pour obtenir de l’aide.

Effectuez les étapes ci-dessous :

1. Accédez au répertoire d’installation d’Adobe Captivate.

   Par exemple,  `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 est la version du Captivate. Diffère si vous utilisez une autre version d’Adobe Captivate).

1. Copie du fichier de configuration **AdobeCaptivate.ini** sur votre bureau.

   ![](assets/cp-captivate.ini.png)
   *Affichage du fichier de configuration*

1. Ouvrez le fichier copié à partir de votre bureau sur un Bloc-notes.
1. Modifiez la valeur de LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` to LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *Afficher PrimeBaseURL*

1. Enregistrez les modifications apportées au Bloc-notes.
1. Copiez le fichier enregistré que vous avez modifié et collez-le à nouveau dans le chemin d’accès au fichier. Remplacer le fichier d’origine dans  `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. Une fois terminé, lancez Adobe Captivate et essayez de publier sur Adobe Learning Manager.
