---
description: Découvrez comment Content Composer gère la création et Adobe Learning Manager la livraison, le suivi et le reporting après la publication.
jcr-language: en_us
title: Fonctionnement conjoint de Content Composer et de Adobe Learning Manager
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---


# Fonctionnement conjoint de Adobe Learning Manager Content Composer et de Adobe Learning Manager

Le compositeur de contenu gère la création. Adobe Learning Manager gère la livraison, l’inscription, le suivi et la création de rapports. Les deux produits se connectent par le biais d’une étape de publication. Une fois que vous avez publié à partir du compositeur de contenu, le cours devient un module dans la bibliothèque de contenu ALM, où il peut être assemblé dans un cours et attribué aux élèves.

## Commandes du compositeur de contenu

- Structure de la leçon et de la rubrique

- Contenu du cours : texte, images, vidéos, composants et vérifications des connaissances

- Questionnaires de fin de leçon, y compris les types de questions et les options de réponse

- Thème visuel

- Critères d’achèvement et critères de réussite

- Version de SCORM utilisée pour la création de rapports

## Ce que Adobe Learning Manager contrôle

- Inscription des élèves et accès

- Métadonnées du module : durée, balises, ID uniques, expiration

- Assemblage de cours : combinaison des modules du compositeur de contenu avec d’autres contenus d’apprentissage

- Suivi des élèves, rapports et relevés de notes

- Contrôle de version du cours

- Notifications et rappels

## De la création du cours à l’achèvement de l’élève

1. **Créer le cours dans le compositeur de contenu** : créez votre cours dans le compositeur de contenu, y compris les leçons, les sujets, les thèmes, les quiz et les paramètres d&#39;achèvement. Configurez les paramètres du cours (critères d’achèvement, critères de réussite et notation du quiz) avant la publication.
Pour plus d&#39;informations, voir [Configurer les paramètres du cours](#settings).

2. **Publish vers Adobe Learning Manager :** une fois la création terminée, connectez Content Composer à votre compte ALM via les paramètres **Exporter** et publiez le cours. Content Composer envoie le cours à la bibliothèque de contenu ALM en tant que module compatible SCORM.
   ![Cours publié avec un en-tête, un logo et un thème de police personnalisés](../assets/49_published_course_custom_branding_header_updated.png)

3. **Configurer le module dans ALM :** une fois publié, le cours apparaît sous la forme d&#39;un module dans la bibliothèque de contenu ALM. Un auteur ALM configure les métadonnées du module (y compris la durée, les balises, les ID uniques et les paramètres d&#39;expiration) et ajoute le module à un cours ALM avec d&#39;autres contenus d&#39;apprentissage.
   ![Champs de métadonnées de module et de critères d&#39;achèvement](../assets/50_alm_add_content_composer_module_metadata_updated.png)

>[!NOTE]
>
>Si vous définissez des critères d’achèvement et de réussite dans Adobe Learning Manager (ALM), ces paramètres ont priorité sur ceux définis dans le compositeur de contenu.

4.**Publish du cours ALM :** un auteur ALM assemble le module dans un cours ALM, ajoute des images et des paramètres de cours, puis le publie. Ce n’est qu’après cette étape que les élèves peuvent être inscrits.

Pour plus d&#39;informations, voir [Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-author).
![ Bibliothèque de contenu dans Adobe Learning Manager, affichant les modules publiés et de traitement](../assets/51_alm_content_library_list_view_updated.png)

Pour plus d&#39;informations, voir [Création de cours en tant qu&#39;auteur sur ALM](https://experienceleague.adobe.com/en/docs/learning-manager/using/authors/courses).

5.**Les élèves terminent le cours :** les élèves accèdent au cours via Adobe Learning Manager, lancent le module Compositeur de contenu, suivent des leçons et répondent à des questionnaires, et reçoivent des scores en fonction des critères d’achèvement et de réussite que vous avez configurés à l’étape 1.

Pour plus d&#39;informations, voir [Accéder au cours en tant qu&#39;élève](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-learner).

&#x200B;6. Enregistrements ALM de la progression de l’élève : l’état d’achèvement, les scores du quiz et les données de l’élève sont enregistrés dans ALM et mis à disposition via les relevés de notes des élèves et les rapports administratifs.

7.**Mettez à jour le cours à l&#39;aide du contrôle de version** : lorsque vous mettez à jour le contenu dans le compositeur de contenu et que vous le republiez, ALM crée une nouvelle version du module. Les auteurs ALM peuvent mettre à jour les cours existants pour utiliser la dernière version.
