---
description: Recherchez ce que les élèves peuvent faire avec le serveur Adobe Learning Manager Model Context Protocol et quels outils prennent en charge chaque fonctionnalité.
jcr-language: en_us
title: Outils d'élève pour le serveur Model Context Protocol
exl-id: 4509b984-d0ba-4b7e-a0bb-803aa235fd1e
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---

# Outils d&#39;élève pour le serveur Model Context Protocol

## Présentation

Chaque fonctionnalité s’exécute en tant qu’élève connecté, une fois qu’il se connecte. Une demande renvoie uniquement ce à quoi l’élève peut accéder dans Adobe Learning Manager. En savoir plus sur la [connexion de votre client AI](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md).

## Capacités de l’élève

| **Capacité** | **Ce que les élèves peuvent faire** | **Exemple de requête** |
|----|----|----|
| Rechercher du contenu d’apprentissage | Trouver des cours, des certifications et des parcours d’apprentissage | Quels sont les cours de leadership disponibles ? |
| Afficher les inscriptions | Vérifier les inscriptions et la formation requise | Lequel de mes cours est sur le point d’expirer ? |
| Poser des questions d’apprentissage | Obtenir des réponses à partir du contenu d’apprentissage | Que signifie la gestion des risques de la chaîne d’approvisionnement dans FedRAMP ? |
| Générer des parcours d’apprentissage | Créer des parcours d’apprentissage personnalisés | Aidez-moi à trouver des cours pour perfectionner mes compétences en gestion de projet. |
| Enregistrer les parcours d’apprentissage | Enregistrer les parcours d’apprentissage générés | Enregistrez ce parcours d’apprentissage. |

## Outils MCP pris en charge

Le serveur MCP Adobe Learning Manager expose les outils d’élève suivants.

| **Nom de l&#39;outil** | **Description** |
|----|----|
| search_learning_items | Recherchez dans le catalogue des cours, des parcours d’apprentissage, des certifications, des instructions, des badges, des compétences, des catalogues et des balises. Filtrez par état d’élève, compétence, balise, catalogue, format de livraison, prix et langue. Pour les questions relatives au sujet, utilisez answer_learning_content_question. Exemple : « Cours Python pour débutants ». |
| list_my_learning_enrollments | Répertoriez les cours, parcours d’apprentissage, certifications et assistances à la tâche auxquels l’élève est inscrit, en cours et terminés, avec l’état, la progression et l’échéance. Filtrer par type d&#39;objet d&#39;apprentissage ou état d&#39;achèvement. Les résultats affichent d’abord les inscriptions les plus récentes. Exemple : « Qu’est-ce qui est attendu bientôt ? » |
| get_learning_object | Obtenez les détails complets d’un cours, d’un parcours d’apprentissage, d’une certification ou d’une assistance à la tâche par ID, avec éventuellement des instances, des compétences et des objets de sous-apprentissage. Obtenez l’ID de search_learning_items ou list_my_learning_enrollments. |
| get_my_learning_profile | Obtenez le profil de l’élève, y compris les détails du compte et du responsable. Pour les inscriptions et la progression, utilisez list_my_learning_enrollments. |
| answer_learning_content_question | Répondre aux questions sur le contenu d’apprentissage, en s’appuyant sur le matériau d’apprentissage et en citant les objets d’apprentissage sources. Résumez un objet d’apprentissage ou comparez-en deux côte à côte pour la couverture, la profondeur, les conditions préalables et le public. Pour rechercher ou répertorier du contenu, utilisez search_learning_items ou list_my_learning_enrollments. Exemple : « Expliquez TCP/UDP comme traité dans mon cours de mise en réseau. » |
| custom_learning_path | Recommandez des cours qui correspondent aux objectifs, aux sujets et aux besoins d’un élève. Enregistrez un chemin d’accès approuvé vers le compte de l’élève. Répertoriez les chemins enregistrés ou obtenez les détails et les cours d’un chemin par ID. |

>[!IMPORTANT]
>
>Les noms des outils sont affichés à titre de référence et peuvent varier en fonction de la mise en œuvre du client.
