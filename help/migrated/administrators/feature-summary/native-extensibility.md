---
title: Extensibilité native
description: Configurez des expériences personnalisées dans la version native d’Adobe Learning Manager, ce qui vous permet de ne pas utiliser l’interface sans en-tête pour les cas moins complexes.
source-git-commit: 86c80607e2f50e6abf6d64fd7a916ef5b024b837
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
1. Saisissez le nom de l’extension dans le champ **[!UICONTROL Nom]** champ.
1. Saisissez la description de l’extension dans le champ **[!UICONTROL Description]** champ.
1. Sélectionnez un point d’invocation. Dans Adobe Learning Manager, un point d’invocation est un emplacement où un lien ou un bouton peut être inséré dans une application personnalisée. Les points d’invocation suivants sont disponibles :

   Pour cet exemple, sélectionnez **[!UICONTROL Administrateur]**, **[!UICONTROL Auteur : Cours]**, **[!UICONTROL Parcours d’apprentissage]** - **[!UICONTROL Instances]** - **[!UICONTROL Ligne d’instance]**.

   ![image d’extension](assets/list-native-extensions.png)
   *Sélectionner le point d’appel*

1. Saisissez l’étiquette d’extension qui apparaîtra sur l’interface utilisateur dans le champ **[!UICONTROL Libellé d’extension]** champ.
1. Saisissez l’URL de votre choix pour héberger l’extension dans le champ **[!UICONTROL URL]**.
1. Dans la liste déroulante Ouvrir dans, indiquez si l’extension doit être lancée dans un nouvel onglet ou dans un nouvel onglet.
1. Sélectionnez la taille de la fenêtre modale. Les options sont disponibles si vous avez sélectionné *Dans l’application* modale à l’étape précédente.

   Pour conserver l’accessibilité dans la fenêtre contextuelle, l’application d’extension doit être envoyée à l’événement une fois qu’elle se trouve sur le dernier élément pouvant recevoir le focus sur son site web, puis l’utilisateur sélectionne la touche TAB. Cela est nécessaire pour garder le focus dans la fenêtre contextuelle et prendre en charge l’accessibilité.

   ```
   window.parent.postMessage({*}
   
   { type: 'ALM_EXTENSION_APP', eventType: 'trapFocusInModal' }
   
   ,{}'');
   ```

1. Définissez l’étendue de l’extension. Les étendues suivantes sont disponibles :

   * **[!UICONTROL Tous les cours, cursus et certifications]**: cette extension est activée pour tous les cours, parcours d’apprentissage et certifications. Avec les administrateurs, les auteurs peuvent la désactiver pour certains cours, parcours d’apprentissage et certifications.
   * **[!UICONTROL Cours, parcours d’apprentissage et certifications sélectionnés]**: cette extension est désactivée pour tous les cours, parcours d’apprentissage et certifications. Avec les administrateurs, les auteurs peuvent l’activer pour certains cours, parcours d’apprentissage et certifications.

1. Sélectionnez l’option **[!UICONTROL Activer]** pour activer l’extension. Une fois active, l’extension apparaît au point d’appel spécifié en fonction de l’étendue.
1. Sélectionnez **[!UICONTROL Enregistrer]** en haut à droite de la page pour créer l’extension.

## Accès à l’extension en tant qu’administrateur

1. En tant qu’administrateur, sélectionnez **[!UICONTROL Parcours d’apprentissage]** dans la barre d’outils de gauche.
1. Sélectionnez un cours > **[!UICONTROL Afficher le parcours d’apprentissage]**.
1. Sélectionnez **[!UICONTROL Instances]** dans le panneau de gauche.
1. Sélectionnez **[!UICONTROL Plus]** dans la section Instances. L’extension s’affiche dans la section Instances.

   ![image d’instances](assets/instances-extension.png)
   *Sélectionner l’extension*

   Lorsque vous sélectionnez l’extension, celle-ci apparaît dans la fenêtre modale.

## Accès à l’extension en tant qu’auteur

1. En tant qu’administrateur, sélectionnez **[!UICONTROL Parcours d’apprentissage]** dans la barre d’outils de gauche.
1. Sélectionnez un cours > **[!UICONTROL Afficher le parcours d’apprentissage]**.
1. Sélectionnez **[!UICONTROL Instances]** dans le panneau de gauche.
1. Sélectionnez **[!UICONTROL Plus]** dans la section Instances. L’extension s’affiche dans la section Instances.

   ![image d’instances](assets/instances-extension.png)
   *Accéder à l’extension en tant qu’auteur*

   Lorsque vous sélectionnez l’extension, celle-ci apparaît dans la fenêtre modale.

## Affichage de l’ensemble des extensions

En tant qu’administrateur, vous pouvez afficher toutes les extensions sur la page Extensions natives. Pour afficher la liste, sélectionnez Extensions natives dans le panneau de gauche de l’application.

![afficher l’image des extensions](assets/view-extensions.png)
*Voir toutes les extensions*

## Activation ou désactivation d’une extension

En tant qu’auteur, sur la page Paramètres d’un cours, vous pouvez activer ou désactiver une extension pour un cours, une certification ou un parcours d’apprentissage.

![activer l’image de l’extension](assets/activate-extension.png)
*Activation d’une extension*

## Partage d’une clé d’accès

Vous devez partager la clé d’accès si vous configurez une extension d’inscription.

Cela est important, car si cette clé n’est pas générée et partagée entre les utilisateurs, l’authentification de l’inscription échouera et les élèves ne pourront pas s’inscrire aux cours.

La clé d’accès doit être partagée pour l’inscription au cours ou au parcours d’apprentissage et aux certificats.

Dans l’onglet Paramètres, générez la clé.

![partager l’image clé](assets/share-extension.png)
*Partage de la clé d’accès*

## Téléchargement du rapport d’extension

Il existe deux façons de télécharger ce rapport.

**Rapport de configuration de l’extension**

1. Dans la page Extensions natives, sélectionnez **[!UICONTROL Rapport de configuration de l’extension]**.

   ![image du rapport](assets/extension-config-report.png)
   *Télécharger le rapport d’extension*

   Le rapport est généré.

1. Sélectionnez OK.

   ![génération de l’image du rapport](assets/generating-report.png)
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

1. Entrée **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]**, sélectionnez **[!UICONTROL Rapport de configuration de l’extension]**.

   ![image de la page rapports](assets/extension-report-page.png)
   *Téléchargement du rapport à partir de la page Rapports*

L’état doit être compris dans la plage **0 - 4294967295**, lors de la configuration de l’état d’inscription.
