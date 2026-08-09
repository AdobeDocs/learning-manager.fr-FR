---
description: Une référence complète pour chaque propriété du schéma JSON du thème du compositeur de contenu, y compris les jetons de palette, les piles de polices, le rayon et les jetons d’espacement, les valeurs de rôle de texte, les propriétés des composants et le style d’évaluation.
jcr-language: en_us
title: Référence des propriétés JSON du thème du compositeur de contenu Adobe Learning Manager
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 5%

---


# Référence des propriétés JSON du thème du compositeur de contenu Adobe Learning Manager

Une référence complète pour chaque propriété dans un fichier JSON de thème du compositeur de contenu, avec des descriptions et des valeurs d’exemple.

Champs de niveau supérieur qui identifient et décrivent le thème.

## **Métadonnées**

| **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|--------------|----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| l&#39;identifiant | chaîne | Identificateur de thème unique. Minuscules, tirets uniquement, pas d’espaces ni de caractères spéciaux. Utilisé en interne pour référencer le thème. | « ardoise » |
| name | chaîne | Nom d&#39;affichage affiché dans le panneau Thèmes de cours. | « Ardoise » |
| version | chaîne | Numéro de version sémantique. Utilisez « 1.0.0 » pour les nouveaux thèmes. | &quot;1.0.0&quot; |
| description | chaîne | Brève description du caractère visuel du thème. | « Un thème chaleureux et faisant autorité avec un arrière-plan crème, des accents rouge Adobe et le système de polices Roboto Slab + Roboto » |
| auteur | chaîne | Nom du créateur du thème ou de l’équipe. | « Compositeur de contenu » |
| source | chaîne | Origine du thème. « expédié » pour les thèmes intégrés. « personnalisé » pour les thèmes créés par l’utilisateur. | « personnalisé » |
| isDefault | booléen | Indique si ce thème est automatiquement appliqué aux nouveaux cours. Définissez cette option sur false dans la plupart des cas. | faux |

## **foundation.palette**

Les sept jetons de couleur de base qui forment la base de couleur du thème. Toutes les valeurs d’éléments font référence à ces jetons à l’aide de var(—tokenName) plutôt que de valeurs hexadécimales codées en dur.

| **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|------------------|------------|---------------------------------------------------------------------------------------------------------------------------|-----------------|
| premier plan | couleur hexadécimale | Couleur de premier plan principale pour le texte, les icônes et les éléments de l’interface utilisateur placés sur l’arrière-plan. | #1A1A1A |
| arrière plan | couleur hexadécimale | Couleur de fond de la toile de fond du plat principal et de la diapositive. | #FAF7F2 |
| accentuer | couleur hexadécimale | Couleur d’accentuation de marque appliquée aux boutons, aux états sélectionnés, aux indicateurs de progression, aux en-têtes de leçon et aux mises en évidence interactives. | #E8001C |
| backgroundSubtle | couleur hexadécimale | Couleur d’arrière-plan secondaire pour les cartes, les panneaux, la navigation et les remplissages de composants. | #F0EBE1 |
| secondaire | couleur hexadécimale | Bordure, séparateur et couleur d’élément d’interface utilisateur inactive. | #D9D3C9 |
| textPrimary | couleur hexadécimale | Couleur de texte principale pour tout le contenu d’en-tête et de corps. | #1A1A1A |
| textInverse | couleur hexadécimale | Couleur du texte pour le contenu placé sur des arrière-plans sombres ou de couleur accentuée, tels que les libellés de bouton sur la couleur accentuée. | #FFFFFF |

## **foundation.fonts**

Deux piles de polices appliquées à tous les rôles de texte dans le thème. Référence dans les valeurs d’élément à l’aide de var(—font-heading) ou var(—font-body).

| **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|--------------|-------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| en-tête | chaîne de la pile de polices | Famille de polices pour les titres de leçon, les titres de rubrique et les titres d’affichage. Incluez des options de secours sécurisées pour le web. | « Roboto Slab, Géorgie, &#39;Times New Roman&#39;, empattement » |
| corps | chaîne de la pile de polices | Famille de polices pour le texte de paragraphe, les légendes, les questions de quiz et les étiquettes d’interface utilisateur. Incluez des options de secours sécurisées pour le web. | « Roboto, -apple-system, BlinkMacSystemFont, &#39;Segoe UI&#39;, sans-serif » |

## **foundation.spacing**

Jetons d’espacement horizontal et vertical utilisés comme ligne de base. Les composants sont mis à l’échelle à partir de ceux-ci en utilisant les multiplicateurs horizontalSpacingScale et verticalSpacingScale.

| **Chemin** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|---------------|----------|-------------------------------------|-----------------|
| horizontal.xs | valeur px | Plus petite unité d’espacement horizontal | 4px |
| horizontal.s | valeur px | Petite unité d&#39;espacement horizontale | 8px |
| horizontal.m | valeur px | Unité d&#39;espacement horizontale moyenne | 12px |
| horizontal.l | valeur px | Grande unité d&#39;espacement horizontale | 16px |
| horizontal.xl | valeur px | Extra-grande unité d&#39;espacement horizontal | 24px |
| vertical.xs | valeur px | Plus petite unité d’espacement vertical | 4px |
| vertical.s | valeur px | Petite unité d&#39;espacement vertical | 8px |
| vertical.m | valeur px | Unité d&#39;espacement vertical moyenne | 16px |
| vertical.l | valeur px | Grande unité d&#39;espacement vertical | 24px |
| vertical.xl | valeur px | Extra-grande unité d&#39;espacement vertical | 32px |

## **foundation.radius**

Jetons de rayon de bordure contrôlant l’arrondi des coins pour les composants et les cartes.

| **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|--------------|----------|---------------------------------------------------------|-----------------|
| aucune | valeur px | Pas d’arrondi : angles pointus. Toujours « 0px ». | 0px |
| s | valeur px | Petit rayon pour un arrondi subtil. | 4px |
| m | valeur px | Rayon moyen pour l’arrondi standard des cartes et des composants. | 8px |
| l | valeur px | Grand rayon pour un arrondi important. | 16px |
| complet | valeur px | Forme de pilule complète ou de cercle. Toujours « 9999px ». | 9999px |

## **foundation.logo**

| **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|--------------|----------------|----------------------------------------------------------------------------------------------|-----------------|
| logo | chaîne ou null | URL ou chemin d&#39;accès au fichier pour l&#39;image du logo affichée dans l&#39;en-tête du cours. Définissez cette option sur Null pour l’absence de logo. | null |

## **elements.text**

Propriétés typographiques pour chaque rôle de texte nommé dans le cours. Tous les rôles partagent le même ensemble de propriétés.

### **Rôles de texte**

| **Rôle** | **Appliqué à** |
|--------------|------------------------------------------------------------------------------|
| lessonTitle | Titre principal sur une diapositive d’ouverture de leçon |
| topicTitle | En-tête en haut de chaque diapositive de rubrique |
| blockHeading | Intitulés dans les composants de contenu tels que les en-têtes d’accordéon et les titres de carte |
| sous-titre | Titres secondaires dans une diapositive de rubrique |
| question | Texte de la question de vérification du quiz et des connaissances |
| légende | Légendes sous les images et les blocs multimédias |
| paragraphe | Corps de texte dans les diapositives de contenu |
| buttonLabel | Texte sur les boutons et les éléments d’appel à l’action |

### **Propriétés de texte partagées**

Les propriétés suivantes s’appliquent à chaque rôle de texte répertorié ci-dessus.

| **Propriété** | **Type** | **Valeurs acceptées** | **Description** |
|--------------------|-----------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| fontFamily | Var CSS ou pile de polices | var(—font-heading), var(—font-body) ou une chaîne de pile de polices complète | Famille de polices pour ce rôle de texte. |
| fontSize | valeur px | Toute valeur de pixel | Taille de la police. |
| fontWeight | chaîne | « bold » ou « normal » uniquement - les valeurs numériques ne sont pas prises en charge | Épaisseur de la police. |
| fontStyle | chaîne | « normal » ou « italique » | Style de police. |
| couleur | CSS var ou hex | Tout jeton de palette via var(—tokenName) ou une valeur hexadécimale directe | Couleur du texte. |
| textAlign | chaîne | « gauche », « centre » ou « droite » | Alignement horizontal du texte. |
| letterSpacing | chaîne | « normal », une valeur px ou une valeur em | Espace entre les caractères. |
| lineHeight | chaîne | Un pourcentage ou une valeur sans unité | Height de ligne. |
| textDecoration | chaîne | « aucun », « souligné » ou « texte barré » | Décoration du texte. |
| textTransform | chaîne | « none », « uppercase », « lowercase » ou « capitalize » | Transformation de la casse du texte. |
| paddingInlineStart | valeur px | Toute valeur de pixel | Remplissage à gauche appliqué au bloc de texte. |
| paragraphSpacing | valeur px | Toute valeur de pixel | Espace ajouté sous chaque paragraphe du bloc de texte. |

### **Valeurs de rôle de texte - Thème d&#39;ardoise**

| **Rôle** | **fontFamily** | **fontSize** | **fontWeight** | **fontStyle** | **couleur** | **textAlign** | **LetterSpacing** | **lineHeight** | **textTransform** |
|--------------|---------------------|--------------|----------------|---------------|--------------------|---------------|-------------------|----------------|-------------------|
| lessonTitle | var(—font-heading) | 48px | gras | normal | var(—textPrimary) | centrer | -0,01em | 130% | aucune |
| topicTitle | var(—font-heading) | 40px | normal | normal | var(—textPrimary) | gauche | 0 | 135% | aucune |
| blockHeading | var(—font-heading) | 24px | gras | normal | var(—textPrimary) | gauche | 0 | 140% | aucune |
| sous-titre | var(—font-body) | 20px | gras | normal | var(—textPrimary) | gauche | 0,01 cadratin | 150% | aucune |
| question | var(—font-heading) | 24px | normal | normal | var(—textPrimary) | gauche | 0 | 150% | aucune |
| légende | var(—font-body) | 13px | normal | normal | var(—textPrimary) | gauche | 0,02 cadratin | 170% | aucune |
| paragraphe | var(—font-body) | 16px | normal | normal | var(—textPrimary) | gauche | 0,01 cadratin | 190% | aucune |
| buttonLabel | var(—font-body) | 14px | gras | normal | var(—textInverse) | centrer | 0,06 cadratin | 125% | majuscules |

## **éléments - surfaces structurelles**

Propriétés qui contrôlent l&#39;arrière-plan et la bordure des surfaces de disposition fixes du cours.

| **Élément** | **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|--------------|--------------|-------------------|---------------------------------------------------|----------------------------|
| canevas | arrière plan | CSS var | Couleur d’arrière-plan de la zone de travail du plat principal | var(—background) |
| en-tête | arrière plan | CSS var | Couleur d’arrière-plan de la barre d’en-tête du cours | var(—background) |
| en-tête | bordure | Chaîne de bordure CSS | Bordure inférieure de la barre d’en-tête du cours | 1 px solid var(—secondary) |
| footer | arrière plan | CSS var | Couleur d&#39;arrière-plan de la barre de pied de page du cours | var(—background) |
| footer | bordure | Chaîne de bordure CSS | Bordure supérieure de la barre de pied de page du cours | 1 px solid var(—secondary) |
| lessonHeader | arrière plan | CSS var | Couleur d&#39;arrière-plan de la zone d&#39;en-tête du titre de la leçon | var(—accent) |
| rubrique | arrière plan | CSS var | Couleur d’arrière-plan de chaque diapositive de rubrique | var(—background) |
| rubrique | bordure | Chaîne de bordure CSS | Bordure autour du conteneur de diapositives de rubrique | 1 px solid var(—secondary) |
| navigation | arrière plan | CSS var | Couleur d&#39;arrière-plan du panneau de navigation de la leçon | var(—backgroundSubtle) |
| navigation | bordure | Chaîne de bordure CSS | Bordure dans le panneau de navigation de la leçon | 1 px solid var(—secondary) |
| bouton | arrière plan | CSS var | Couleur d’arrière-plan des boutons d’action principaux | var(—accent) |
| pagination | arrière plan | CSS var | Couleur d’arrière-plan de la commande de pagination | var(—backgroundSubtle) |

## **éléments - propriétés du composant partagé**

Ces propriétés apparaissent sur tous les composants de bloc de contenu : paragraphBlock, videoBlock, imageGrid, accordéon, carrousel, flipCard et timeline.

| **Propriété** | **Type** | **Description** |
|------------------------|-------------------|---------------------------------------------------------------------------------------------------|
| arrière plan | CSS var ou color | Arrière-plan externe du bloc de composant. Généralement « transparent ». |
| cardBackgroundColor | CSS var ou color | Remplissage en arrière-plan de cartes individuelles au sein du composant. |
| cardBorder | Chaîne de bordure CSS | Bordure appliquée à chaque carte. Caractères CSS complets, par exemple « 1px solid var(—secondary) ». |
| cardShadowOffset | chaîne | Décalage X et Y de l’ombre portée de la carte, par exemple « 0px 2px 6px ». |
| cardShadowColor | CSS var ou color | Couleur de l’ombre portée de la carte. |
| cardShadowOpacity | chaîne de pourcentage | Opacité de l’ombre portée de la carte. Définissez sur « 0 % » pour supprimer l’ombre. |
| horizontalSpacingScale | chaîne numérique | Multiplicateur appliqué aux jetons d’espacement horizontal pour ce composant. « 1 » utilise l’espacement par défaut. |
| verticalSpacingScale | chaîne numérique | Multiplicateur appliqué aux jetons d’espacement vertical pour ce composant. « 1 » utilise l’espacement par défaut. |
| radiusScale | chaîne numérique | Multiplicateur appliqué aux jetons de rayon pour ce composant. « 1 » utilise le rayon par défaut. |
| nestedAccentColor | CSS var ou color | Couleur d’accentuation pour les éléments imbriqués dans le composant. S’applique uniquement à paragraphBlock. |

### **Valeurs de composant partagées - Thème Slate**

| **Composant** | **cardBackgroundColor** | **cardBorder** | **cardShadowOpacity** |
|----------------|-----------------------------|----------------------------|---------------------------|
| paragraphBlock | var(—backgroundSubtle) | 1 px solid var(—secondary) | 8% |
| videoBlock | var(—backgroundSubtle) | 1 px solid var(—secondary) | 8% |
| imageGrid | var(—backgroundSubtle) | 1 px solid var(—accent) | 8% |
| accordéon | var(—backgroundSubtle) | 1 px solid var(—secondary) | 8% |
| carrousel | var(—backgroundSubtle) | 1 px solid var(—secondary) | 8% |
| flipCard | var(—backgroundSubtle) | 1 px solid var(—secondary) | 8% |
| chronologie | var(—backgroundSubtle) | 1 px solid var(—secondary) | 8% |

## **éléments - propriétés spécifiques au composant**

Propriétés uniques à chaque type de composant.

| **Composant** | **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|----------------|--------------------------|----------|------------------------------------------------------------------|-------------------------|
| paragraphBlock | nestedAccentColor | CSS var | Couleur d’accentuation pour les éléments imbriqués dans le bloc de paragraphe | var(—accent) |
| flipCard | cardFrontBackgroundColor | CSS var | Couleur d&#39;arrière-plan de la face avant de la carte à clef | var(—backgroundSubtle) |
| flipCard | cardBackBackgroundColor | CSS var | Couleur d’arrière-plan de la face arrière de la carte de visite : couleur de révélation | var(—accent) |
| flipCard | arrowColor | CSS var | Couleur de l’icône en forme de flèche de l’indicateur de symétrie | var(—textInverse) |
| onglets | activeBg | CSS var | Couleur d’arrière-plan de l’onglet actuellement sélectionné | var(—accent) |
| onglets | inactiveBg | CSS var | Couleur d’arrière-plan des onglets non sélectionnés | var(—backgroundSubtle) |
| onglets | containerBg | CSS var | Couleur d’arrière-plan du conteneur de barres d’onglets | var(—backgroundSubtle) |
| chronologie | trackColor | CSS var | Couleur de la ligne de connexion entre les nœuds du montage | var(—secondary) |
| chronologie | progressCompletedBg | CSS var | Couleur de remplissage des marques de progression du montage terminées | var(—accent) |
| chronologie | progressCurrentBorder | CSS var | Couleur de bordure de l’indicateur de progression du montage actuel | var(—accent) |
| chronologie | progressUnreachBg | CSS var | Couleur de remplissage des marques de montage non encore atteinte | var(—secondary) |
| chronologie | progressUnreachBorder | CSS var | Couleur de bordure des marques de montage non encore atteinte | var(—backgroundSubtle) |

## **elements.assessment**

Propriétés des composants de quiz et de vérification des connaissances.

| **Propriété** | **Type** | **Description** | **Valeur d&#39;ardoise** |
|----------------------------|----------------|------------------------------------------------------------------------------|-------------------------|
| arrière plan | CSS var | Contexte extérieur du bloc d&#39;évaluation | transparent |
| optionTextColor | CSS var | Couleur du texte des libellés des options de réponse | var(—textPrimary) |
| optionIndicatorColor | CSS var | Couleur du bouton radio ou de l’indicateur de case à cocher | var(—accent) |
| optionSelectedColor | CSS var | Couleur appliquée à l’indicateur d’option sélectionné | var(—accent) |
| optionCheckmarkColor | CSS var | Couleur de la coche affichée sur une option sélectionnée | var(—textInverse) |
| optionBackgroundColor | CSS var | Couleur d’arrière-plan de chaque option de réponse | var(—background) |
| optionHoverBackgroundColor | CSS var | Couleur d’arrière-plan d’une option de réponse au survol | var(—backgroundSubtle) |
| buttonBackgroundColor | CSS var | Couleur d’arrière-plan du bouton Envoyer ou Vérifier la réponse | var(—accent) |
| buttonTextColor | CSS var | Couleur du texte de l’étiquette du bouton de réponse Envoyer ou Vérifier | var(—textInverse) |
| buttonHoverBackgroundColor | CSS var | Couleur d’arrière-plan du bouton au survol | var(—accent) |
| feedbackCorrectColor | couleur hexadécimale | Couleur d’arrière-plan du panneau de commentaires des réponses correctes | #D7F7E1 |
| feedbackIncorrectColor | couleur hexadécimale | Couleur d’arrière-plan du panneau de retour d’informations incorrect | #FFEBE8 |
| feedbackTextColor | couleur hexadécimale | Couleur du texte dans le panneau de commentaires | #111111 |
| optionBorderCorrectColor | couleur hexadécimale | Couleur de la bordure sur l’option de réponse correcte une fois la réponse révélée | #079355 |
| optionBorderIncorrectColor | couleur hexadécimale | Couleur de la bordure d’une option sélectionnée incorrectement une fois la réponse affichée | #D73220 |
| horizontalSpacingScale | chaîne numérique | Multiplicateur pour l&#39;espacement horizontal au sein du composant d&#39;évaluation | &quot;1&quot; |
| verticalSpacingScale | chaîne numérique | Multiplicateur pour l&#39;espacement vertical dans le composant d&#39;évaluation | &quot;1&quot; |
| radiusScale | chaîne numérique | Multiplicateur du rayon de bordure dans le composant d&#39;évaluation | &quot;1&quot; |

## **Référence du jeton de palette var()**

Utilisez ces expressions var() dans les valeurs d’éléments pour référencer des jetons de palette. La mise à jour d’un jeton de palette met automatiquement à jour chaque élément qui l’utilise.

| **Expression** | **Références** |
|-------------------------|-------------------------------------|
| var(—foreground) | foundation.palette.foreground |
| var(—background) | foundation.palette.background |
| var(—accent) | foundation.palette.accent |
| var(—backgroundSubtle) | foundation.palette.backgroundSubtle |
| var(—secondary) | foundation.palette.secondary |
| var(—textPrimary) | foundation.palette.textPrimary |
| var(—textInverse) | foundation.palette.textInverse |
| var(—font-heading) | foundation.fonts.heading |
| var(—font-body) | foundation.fonts.body |

## Exemple d’un thème json

```
{
  "id": "slate",
  "name": "Slate",
  "version": "1.0.0",
  "description": "A warm, authoritative theme with cream background, Adobe red accents, and the Roboto Slab + Roboto type system",
  "author": "Content Composer",
  "source": "custom",
  "isDefault": false,
  "foundation": {
    "palette": {
      "foreground": "#1A1A1A",
      "background": "#FAF7F2",
      "accent": "#E8001C",
      "backgroundSubtle": "#F0EBE1",
      "secondary": "#D9D3C9",
      "textPrimary": "#1A1A1A",
      "textInverse": "#FFFFFF"
    },
    "fonts": {
      "heading": "Roboto Slab, Georgia, 'Times New Roman', serif",
      "body": "Roboto, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    },
    "spacing": {
      "horizontal": {
        "xs": "4px",
        "s": "8px",
        "m": "12px",
        "l": "16px",
        "xl": "24px"
      },
      "vertical": {
        "xs": "4px",
        "s": "8px",
        "m": "16px",
        "l": "24px",
        "xl": "32px"
      }
    },
    "radius": {
      "none": "0px",
      "s": "4px",
      "m": "8px",
      "l": "16px",
      "full": "9999px"
    },
    "logo": null
  },
  "elements": {
    "text": {
      "lessonTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "48px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "center",
        "letterSpacing": "-0.01em",
        "lineHeight": "130%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "topicTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "40px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "135%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "blockHeading": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "140%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "subheading": {
        "fontFamily": "var(--font-body)",
        "fontSize": "20px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "question": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "caption": {
        "fontFamily": "var(--font-body)",
        "fontSize": "13px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.02em",
        "lineHeight": "170%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "paragraph": {
        "fontFamily": "var(--font-body)",
        "fontSize": "16px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "190%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "buttonLabel": {
        "fontFamily": "var(--font-body)",
        "fontSize": "14px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textInverse)",
        "textAlign": "center",
        "letterSpacing": "0.06em",
        "lineHeight": "125%",
        "textDecoration": "none",
        "textTransform": "uppercase",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      }
    },
    "canvas": {
      "background": "var(--background)"
    },
    "header": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "footer": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "lessonHeader": {
      "background": "var(--accent)"
    },
    "topic": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "navigation": {
      "background": "var(--backgroundSubtle)",
      "border": "1px solid var(--secondary)"
    },
    "button": {
      "background": "var(--accent)"
    },
    "pagination": {
      "background": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "paragraphBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "nestedAccentColor": "var(--accent)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageBlock": {
      "background": "transparent",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "videoBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageGrid": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--accent)",
      "cardShadowOffset": "0px 2px 8px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "accordion": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "carousel": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "flipCard": {
      "background": "transparent",
      "cardFrontBackgroundColor": "var(--backgroundSubtle)",
      "cardBackBackgroundColor": "var(--accent)",
      "arrowColor": "var(--textInverse)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "tabs": {
      "background": "transparent",
      "activeBg": "var(--accent)",
      "inactiveBg": "var(--backgroundSubtle)",
      "containerBg": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "timeline": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "trackColor": "var(--secondary)",
      "progressCompletedBg": "var(--accent)",
      "progressCurrentBorder": "var(--accent)",
      "progressUnreachedBg": "var(--secondary)",
      "progressUnreachedBorder": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "assessment": {
      "background": "transparent",
      "optionTextColor": "var(--textPrimary)",
      "optionIndicatorColor": "var(--accent)",
      "optionSelectedColor": "var(--accent)",
      "optionCheckmarkColor": "var(--textInverse)",
      "optionBackgroundColor": "var(--background)",
      "optionHoverBackgroundColor": "var(--backgroundSubtle)",
      "buttonBackgroundColor": "var(--accent)",
      "buttonTextColor": "var(--textInverse)",
      "buttonHoverBackgroundColor": "var(--accent)",
      "feedbackCorrectColor": "#D7F7E1",
      "feedbackIncorrectColor": "#FFEBE8",
      "feedbackTextColor": "#111111",
      "optionBorderCorrectColor": "#079355",
      "optionBorderIncorrectColor": "#D73220",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    }
  }
}
```
