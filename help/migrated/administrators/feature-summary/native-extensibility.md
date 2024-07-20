---
title: Extensibilité native
description: Configurez des expériences personnalisées dans la version native de Adobe Learning Manager, ce qui vous permet de ne pas utiliser l’interface sans en-tête pour les cas moins complexes.
exl-id: 510bd00f-4f52-4705-817e-4ee73380ca90
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 48%

---

# Extensibilité native

Vous pouvez configurer des expériences personnalisées dans la version native d’Adobe Learning Manager, ce qui vous permet de ne pas utiliser d’approche headless pour les cas moins complexes. Vous pouvez également créer des applications personnalisées et les placer à différents points de la version native des flux de travail de l’élève, du responsable, de l’administrateur, de l’auteur ou de l’instructeur.

Adobe Learning Manager prend en charge 15 points d’invocation dans l’application pour l’administrateur, l’auteur, l’élève, le responsable et l’instructeur.

## Création d’une extension

1. En tant qu’administrateur, dans le panneau de gauche, sélectionnez **[!UICONTROL Extensions natives]**.
1. Sélectionnez Ajouter une extension.
1. Saisissez le nom de l&#39;extension dans le champ **[!UICONTROL Nom]**.
1. Saisissez la description de l&#39;extension dans le champ **[!UICONTROL Description]**.
1. Sélectionnez un point d’invocation. Dans Adobe Learning Manager, un point d’invocation est un emplacement où un lien ou un bouton peut être inséré dans une application personnalisée. Les points d’invocation suivants sont disponibles :

   Pour cet exemple, sélectionnez **[!UICONTROL Administrateur]**, **[!UICONTROL Auteur : cours]**, **[!UICONTROL Parcours d’apprentissage]** - **[!UICONTROL Instances]** - **[!UICONTROL Ligne d’instance]**.

   ![image d&#39;extension](assets/list-native-extensions.png)
   *Sélectionner le point d&#39;appel*

1. Saisissez l&#39;étiquette d&#39;extension qui apparaîtra sur l&#39;interface utilisateur dans le champ **[!UICONTROL Étiquette d&#39;extension]**.
1. Saisissez l’URL de votre choix pour héberger l’extension dans le champ **[!UICONTROL URL]**.
1. Dans la liste déroulante Ouvrir dans, indiquez si l’extension doit être lancée dans un nouvel onglet ou dans un nouvel onglet.
1. Sélectionnez la taille de la fenêtre modale. Les options sont disponibles si vous avez sélectionné le mode *Dans l&#39;application* à l&#39;étape précédente.

   Pour conserver l’accessibilité dans la fenêtre contextuelle, l’application d’extension doit être envoyée à l’événement une fois qu’elle se trouve sur le dernier élément pouvant recevoir le focus sur son site web, puis l’utilisateur sélectionne la touche TAB. Cela est nécessaire pour garder le focus dans la fenêtre contextuelle et prendre en charge l’accessibilité.

   ```
   window.parent.postMessage({*}
   
   { type: 'ALM_EXTENSION_APP', eventType: 'trapFocusInModal' }
   
   ,{}'');
   ```

1. Définissez l’étendue de l’extension. Les étendues suivantes sont disponibles :

   * **[!UICONTROL Tous les cours, parcours d’apprentissage et certifications]** : cette extension est activée pour tous les cours, parcours d’apprentissage et certifications. Avec les administrateurs, les auteurs peuvent la désactiver pour certains cours, parcours d’apprentissage et certifications.
   * **[!UICONTROL Cours, parcours d’apprentissage et certifications sélectionnés]** : cette extension est désactivée pour tous les cours, parcours d’apprentissage et certifications. Avec les administrateurs, les auteurs peuvent l’activer pour certains cours, parcours d’apprentissage et certifications.

1. Sélectionnez l’option **[!UICONTROL Activer]** pour activer l’extension. Une fois active, l’extension apparaît au point d’appel spécifié en fonction de l’étendue.
1. Sélectionnez **[!UICONTROL Enregistrer]** en haut à droite de la page pour créer l’extension.

## Accès à l’extension en tant qu’administrateur

1. En tant qu’administrateur, sélectionnez **[!UICONTROL Parcours d’apprentissage]** dans la barre d’outils de gauche.
1. Sélectionnez un cours > **[!UICONTROL Afficher le parcours d’apprentissage]**.
1. Sélectionnez **[!UICONTROL Instances]** dans le panneau de gauche.
1. Sélectionnez **[!UICONTROL Plus]** dans la section Instances. L’extension s’affiche dans la section Instances.

   ![image d&#39;instances](assets/instances-extension.png)
   *Sélectionner l&#39;extension*

   Lorsque vous sélectionnez l’extension, celle-ci apparaît dans la fenêtre modale.

## Accès à l’extension en tant qu’auteur

1. En tant qu’administrateur, sélectionnez **[!UICONTROL Parcours d’apprentissage]** dans la barre d’outils de gauche.
1. Sélectionnez un cours > **[!UICONTROL Afficher le parcours d’apprentissage]**.
1. Sélectionnez **[!UICONTROL Instances]** dans le panneau de gauche.
1. Sélectionnez **[!UICONTROL Plus]** dans la section Instances. L’extension s’affiche dans la section Instances.

   ![image d&#39;instances](assets/instances-extension.png)
   *Accéder à l&#39;extension en tant qu&#39;auteur*

   Lorsque vous sélectionnez l’extension, celle-ci apparaît dans la fenêtre modale.

## Affichage de l’ensemble des extensions

En tant qu’administrateur, vous pouvez afficher toutes les extensions sur la page Extensions natives. Pour afficher la liste, sélectionnez Extensions natives dans le panneau de gauche de l’application.

![afficher l&#39;image des extensions](assets/view-extensions.png)
*Afficher toutes les extensions*

## Activation ou désactivation d’une extension

En tant qu’auteur, sur la page Paramètres d’un cours, vous pouvez activer ou désactiver une extension pour un cours, une certification ou un parcours d’apprentissage.

![activer l&#39;image d&#39;extension](assets/activate-extension.png)
*Activer une extension*

## Partage d’une clé d’accès

Vous devez partager la clé d’accès si vous configurez une extension d’inscription.

Cela est important, car si cette clé n’est pas générée et partagée entre les utilisateurs, l’authentification de l’inscription échouera et les élèves ne pourront pas s’inscrire aux cours.

La clé d’accès doit être partagée pour l’inscription au cours ou au parcours d’apprentissage et aux certificats.

Dans l’onglet Paramètres, générez la clé.

![partager l&#39;image clé](assets/share-extension.png)
*Partager la clé d&#39;accès*

## Téléchargement du rapport d’extension

Il existe deux façons de télécharger ce rapport.

**Rapport de configuration d&#39;extension**

1. Dans la page Extensions natives, sélectionnez **[!UICONTROL Rapport de configuration de l’extension]**.

   ![signaler l&#39;image](assets/extension-config-report.png)
   *Télécharger le rapport d&#39;extension*

   Le rapport est généré.

1. Sélectionnez OK.

   ![génération de l&#39;image du rapport](assets/generating-report.png)
   *Génération du rapport*

   Le rapport contient les champs suivants :

   * Nom de l’extension
   * Point d’invocation
   * Étiquette
   * Ouvrir dans l’URL
   * Portée
   * Activation
   * ID unique d’objet d’apprentissage
   * ID de formation
   * Type de formation
   * Nom de la formation

**Page Rapports**

1. Dans **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]**, sélectionnez **[!UICONTROL Rapport de configuration d&#39;extension]**.

   ![image de page des rapports](assets/extension-report-page.png)
   *Téléchargez le rapport à partir de la page Rapports*

L&#39;état doit être compris entre **0 et 4294967295** lors de la configuration de l&#39;état d&#39;inscription.
