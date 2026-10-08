---
description: Découvrez comment télécharger des fichiers source dans le compositeur de contenu, restreindre la sortie AI à votre contenu et mettre à jour les fichiers source lorsque le matériau change.
jcr-language: en_us
title: Gestion des fichiers source
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%
---

# Gestion des fichiers source

**Gérer les sources** vous permet de contrôler le contenu que le compositeur de contenu utilise pour générer votre cours. Ajoutez vos propres documents à un cours, puis choisissez de restreindre l&#39;IA à ce seul contenu ou de la laisser compléter votre matériau avec ses propres connaissances. Si vous n&#39;ajoutez aucun document, le compositeur de contenu génère le cours en utilisant les connaissances existantes du modèle IA.

## Génération d&#39;un cours à l&#39;aide du matériau source

1. Sélectionnez **Gérer les sources** ou **Ajouter des fichiers** dans le panneau de conversation ou la barre d&#39;outils.
   ![](../assets/5_brief_manage_sources_prompt_updated.png)

2. Faites glisser un fichier dans la boîte de dialogue ou sélectionnez **+ Ajouter des fichiers sources** pour parcourir. Vous pouvez ajouter plusieurs fichiers source.
   ![](../assets/6_manage_sources_no_files_added_updated.png)

3. Sélectionnez **Restreindre la sortie au contenu dans les fichiers**. Cela permet au compositeur de contenu d&#39;utiliser uniquement le contenu source pour générer le cours. Si cette option est désélectionnée, le compositeur de contenu utilise également le Web pour créer un cours.
   ![](../assets/7_manage_sources_file_uploading_restrict_output_updated.png)

Format pris en charge :

| **Format** | **Taille maximale** |
|-------------------------|--------------|
| PDF | 100 Mo |
| Markdown (.md) | 100 Mo |
| PowerPoint (.ppt/.pptx) | 100 Mo |
| MS Word (.doc/.docx) | 100 Mo |
| Fichier texte (.txt) | 100 Mo |

Sélectionnez **Continuer** pour générer l&#39;aperçu du cours.

### Générer sans matériau source

Effectuez les étapes ci-dessous pour générer l&#39;outline du cours, lorsque vous n&#39;avez pas de fichier source comme document de référence.

1. Sélectionnez **Gérer les sources**. La boîte de dialogue **Gérer les sources** s&#39;ouvre.

2. Sélectionnez **Je n&#39;ai aucun matériau source - Générer le cours sans fichiers source** pour permettre à l&#39;IA de générer du contenu à partir de ses connaissances générales. Lorsque cette option n&#39;est pas sélectionnée et que les fichiers sont chargés, l&#39;IA restreint le contenu généré à vos documents chargés uniquement.![](../assets/8_manage_sources_no_source_material_option_updated.png)

3. Sélectionnez **Continuer** pour générer l&#39;aperçu du cours.

### Mettre à jour un cours lorsque le matériau source change

Les documents sources peuvent être obsolètes une fois qu&#39;un cours a déjà été généré : une politique est révisée, un SOP obtient une nouvelle version ou une présentation est mise à jour. Utilisez ce workflow pour remettre le cours en ligne avec le matériau actuel.

1. Sélectionnez **Gérer les sources** dans le panneau de conversation ou la barre d&#39;outils pour rouvrir la boîte de dialogue.

2. Ajoutez les nouveaux fichiers ou les fichiers révisés en utilisant **+ Ajouter des fichiers sources**.

3. Supprimez ou remplacez tous les fichiers obsolètes afin que la liste source ne reflète que le matériau actuel.

4. Sélectionnez Continuer pour enregistrer la liste source mise à jour.

5. Régénérez les leçons concernées dans le compositeur de contenu, passez en revue les modifications, puis republiez le cours. La republication envoie la mise à jour à Adobe Learning Manager en tant que nouvelle version de module. Reportez-vous à la section Contrôle de version de module dans ALM.

### Confirmer le téléchargement du fichier

![](../assets/9_manage_sources_file_ingested_confirmation_updated.png)

Une fois qu’un fichier est joint, l’icône de fichier dans la barre d’outils affiche un nombre de badges. L&#39;assistant confirme le téléchargement et offre un raccourci de **génération de contour**. Sélectionnez-le ou sélectionnez **Générer le contour** dans la barre d&#39;outils supérieure.
