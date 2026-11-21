---
title: Explorateur d’examens sécurisé
description: Activez l’intégration de l’Explorateur d’examens sécurisé au niveau du compte dans Adobe Learning Manager afin que les auteurs puissent demander un environnement de navigateur sécurisé pour les quiz natifs.
source-git-commit: 38dba6765ff013e446ab1f6098e9f1df0c24d0f9
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%
---

# Explorateur d’examens sécurisé

L’Explorateur d’examens sécurisé fournit un environnement sécurisé pour que les élèves puissent répondre à des questionnaires Adobe Learning Manager natifs en restreignant l’accès à d’autres navigateurs et applications pendant une évaluation.

Les administrateurs peuvent activer l’intégration du navigateur Safe Exam au niveau du compte et charger un fichier de configuration (.seb) pour définir les restrictions du quiz. Une fois l’intégration activée, les auteurs peuvent configurer des quiz individuels pour exiger l’utilisation de l’Explorateur d’examens sécurisé.

Cet article explique comment activer l’intégration du navigateur Safe Exam pour votre compte.

## Activer l&#39;intégration de Safe Exam Browser

Activez l’intégration du navigateur d’examen sécurisé pour rendre l’option disponible pour les auteurs lorsqu’ils configurent des quiz. Avant de commencer, assurez-vous que vous disposez du fichier Explorateur d’examens sécurisés pour votre compte.

Pour activer l&#39;intégration de Safe Exam Browser :

1. Connectez-vous à ALM en tant qu&#39;**administrateur**.
1. Sélectionnez **Paramètres** > **Général**.
1. Accédez à l&#39;**intégration de l&#39;Explorateur d&#39;examens sécurisé**.
1. Sélectionnez **Modifier**.

   Cela étend l&#39;**intégration de l&#39;Explorateur d&#39;examens sécurisé**.

1. Sélectionnez **Activer**.
1. Sélectionnez **Parcourir** et chargez le fichier Explorateur d&#39;examens sans échec à partir du système. Afficher la configuration [Configurer le fichier de navigateur d&#39;examen sécurisé](#configure-the-seb-file-for-macos) pour plus d&#39;informations.

   ![Paramètres d&#39;intégration de l&#39;Explorateur d&#39;examens sécurisé dans les paramètres généraux](assets/safe-exam-browser-integration-settings.png "Paramètres d&#39;intégration de l&#39;Explorateur d&#39;examens sécurisé dans les paramètres généraux")

1. Sélectionnez **Enregistrer**.

   L’Explorateur d’examens sans échec est désormais disponible pour que les auteurs puissent l’activer lors de la configuration des questionnaires pris en charge.

### Configuration du fichier .seb pour macOS {#configure-the-seb-file-for-macos}

Créez un fichier .seb à l’aide de l’outil de configuration SEB pour définir vos restrictions de quiz, vos paramètres de sécurité et vos applications autorisées. Avant d&#39;utiliser Safe Exam Browser (SEB), assurez-vous que le fichier .seb répond aux exigences suivantes :

1. Définissez le paramètre browserWindowWebView sur 3 (Entier) pour activer SEB.
1. Définissez startURL sur l’URL qui correspond à l’environnement cible.
1. Assurez-vous que le fichier .seb inclut les informations quitURL requises.
