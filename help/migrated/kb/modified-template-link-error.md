---
jcr-language: en_us
title: Les liens de courrier électronique déclenchés à partir de modèles modifiés renvoient une erreur dans Learning Manager
description: Les liens de courrier électronique déclenchés à partir de modèles modifiés renvoient une erreur dans Adobe Learning Manager
contentowner: nluke
preview: true
exl-id: a8fa64e1-aeab-4cb5-9bb0-7cfdad0aa389
source-git-commit: 1529039e35d4190864e96826bfbea25dcad17c73
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 78%

---

# Les liens de courrier électronique déclenchés à partir de modèles modifiés renvoient une erreur dans Learning Manager

## Problème

Une erreur se produit après avoir cliqué sur un lien pour un e-mail automatique/e-mail de bienvenue/e-mail d’inscription.

**Erreur**

État HTTP 400 - Requête incorrecte

![](assets/email-404.png)

## Cause

Cela se produit généralement lorsque les modèles de courrier électronique sont personnalisés de manière incorrecte.

**Solution**

Pour éviter toute erreur liée à des liens rompus, qui peut apparaître en raison de la personnalisation, procédez comme suit :

1. Connectez-vous en tant qu’administrateur.
1. Dans le panneau de gauche, cliquez sur **[!UICONTROL Modèles de courrier électronique]**.

1. Accédez au modèle requis et cliquez dessus pour le modifier.

   La fenêtre **Aperçu du modèle** s’affiche.

   ![](assets/email-template.png)

   Notez les points suivants lorsque vous modifiez un modèle de courrier électronique :

   * Nous vous recommandons de modifier un modèle de courrier électronique depuis l’interface Learning Manager.
   * Copiez-collez le modèle modifié dans un fichier Bloc-notes/Word pour stocker une copie des modifications apportées.
   * Évitez de remplacer du texte dynamique dans le modèle, surligné en bleu. Par exemple, « **OrganizationName** », « **Learner** », « **cliquez ici** », « **CertificateName** », etc.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer les modifications appliquées au modèle.
1. Déclenchez le courrier électronique pour vérifier si les liens fonctionnent comme prévu.
1. Rétablissez les paramètres d&#39;origine en cliquant sur l&#39;option **Rétablir l&#39;original** pour le modèle modifié.
