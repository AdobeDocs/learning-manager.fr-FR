---
jcr-language: en_us
title: Impossible de publier sur le domaine Learning Manager EU
description: Impossible de publier d’Adobe Captivate vers le domaine Adobe Learning Manager EU dans Adobe Learning Manager.
contentowner: nluke
exl-id: fb8ae1af-9902-4901-8263-fb3ebff98fbc
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 83%

---

# Impossible de publier sur le domaine Learning Manager EU {#unable-to-publish-to-learning-manager-eu-domain}

## Problème

Impossible de publier d’Adobe Captivate vers le domaine Adobe Learning Manager EU.

## Erreur

Aucun compte trouvé

## Description

Il existe des scénarios où les auteurs tentent de publier un cours d’Adobe Captivate à Adobe Learning Manager. Cependant, ils ne peuvent pas le faire car ils voient un message d’erreur « Aucun compte trouvé ».

## Cause

Ce problème se produit car Adobe Captivate est par défaut configuré pour publier du contenu dans le domaine américain d’Adobe Learning Manager.

## Résolution:

À noter :

* Si cette option est ouverte, fermez l’application Adobe Captivate.
* Vous devez disposer d’un accès administrateur sur votre ordinateur pour effectuer les étapes ci-dessous. Si vous n’avez pas d’accès administrateur, contactez votre équipe informatique pour obtenir de l’aide.

Procédez comme suit :

1. Accédez au répertoire d’installation d’Adobe Captivate.

   Par exemple, `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 est la version du Captivate. Diffère si vous utilisez une autre version d’Adobe Captivate).

1. Copiez le fichier de configuration **AdobeCaptivate.ini** sur votre ordinateur.

   ![](assets/cp-captivate.ini.png)
   *Afficher le fichier de configuration*

1. Ouvrez le fichier copié depuis votre ordinateur sur un Bloc-notes.
1. Remplacez la valeur de LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` par LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *Afficher PrimeBaseURL*

1. Enregistrez les modifications apportées au Bloc-notes.
1. Copiez le fichier enregistré que vous avez modifié et collez-le à nouveau dans le chemin d’accès du fichier. Remplacer le fichier original dans `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. Une fois terminé, lancez Adobe Captivate et essayez de publier sur Adobe Learning Manager.
