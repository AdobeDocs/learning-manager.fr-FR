---
jcr-language: en_us
title: Application Learning Manager pour Salesforce
description: Salesforce est l’une des solutions CRM les plus populaires auprès des équipes commerciales et marketing. En utilisant l’application Learning Manager d’Adobe dans Salesforce, vous pouvez permettre à ses utilisateurs d’accéder à tout leur contenu d’apprentissage directement à partir de leur interface Salesforce. Les utilisateurs peuvent accéder au contenu d’apprentissage qui leur est attribué, tel que les cours, les programmes d’apprentissage, les assistances à la tâche, etc., à partir de Salesforce. Les utilisateurs peuvent également recevoir des notifications sur leurs inscriptions et des annonces de la part de l’administrateur.
contentowner: jayakarr
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---



# Application Learning Manager pour Salesforce

## Présentation {#overview}

Salesforce™ est l’une des solutions CRM les plus populaires auprès des équipes commerciales et marketing. En utilisant l’application Learning Manager d’Adobe dans Salesforce, vous pouvez permettre à ses utilisateurs d’accéder à tout leur contenu d’apprentissage directement à partir de leur interface Salesforce. Les utilisateurs peuvent accéder au contenu d’apprentissage qui leur est attribué, tel que les cours, les programmes d’apprentissage, les assistances à la tâche, etc., à partir de Salesforce. Les utilisateurs peuvent également recevoir des notifications sur leurs inscriptions et des annonces de la part de l’administrateur.

Pour le moment, l’application Salesforce n’est pas disponible, car l’approbation est en attente de Salesforce App Exchange. Si vous souhaitez obtenir un aperçu de la version bêta de l’application, contactez votre gestionnaire de compte ou l’équipe d’assistance Learning Manager.

## Installation et configuration {#installationandsetup}

Découvrez comment installer et configurer l’application Learning Manager pour Salesforce en suivant les étapes ci-dessous.

### Conditions préalables {#prerequisites}

1. L’administrateur d’intégration de votre organisation doit approuver l’application Salesforce. Cette application se trouve dans la section Applications fournies de l’application Learning Manager pour le rôle d’administrateur d’intégration.
1. Accès au compte Salesforce de votre organisation, sur lequel l’application doit être installée. En règle générale, l’administrateur Salesforce de votre organisation est la personne qui installe ces applications. Si vous êtes administrateur d’intégration de Learning Manager et ne disposez pas du compte Salesforce, contactez l’administrateur Salesforce de votre organisation.

### Étapes d’installation {#installationsteps}

1. Demandez à votre gestionnaire de compte ou gestionnaire de succès client d’activer votre compte pour l’utilisation de cette application en fournissant votre ID de compte Learning Manager. Demandez également au CSM le package pouvant être installé de l’application Élève Learning Manager pour Salesforce.

1. Connectez-vous à votre compte Learning Manager en tant qu’administrateur d’intégration et vérifiez que l’application Salesforce est activée pour votre compte.

1. Pour installer l’application Learning Manager dans votre compte Salesforce, utilisez le package installable fourni par votre gestionnaire de compte ou gestionnaire de succès client. Vous devez disposer de droits d’administrateur pour le compte Salesforce sur lequel vous avez l’intention d’installer cette application.

1. Choisissez l’option appropriée pour vous comme indiqué dans l’instantané et cliquez sur **[!UICONTROL Installer]**.

   ![](assets/install-options.png)

   *Sélectionnez l’option Installer pour les administrateurs uniquement*

   Si vous optez pour **Installer pour des profils spécifiques**, choisissez un ou plusieurs profils dans la liste.

1. Cliquez sur **[!UICONTROL Continuer]** dans la fenêtre contextuelle qui s’affiche pour confirmer l’accès tiers.

   Un message s’affiche pour confirmer que l’application a été correctement installée. Cliquez sur **Terminé**.

## Ajout d’un composant de notification à la page d’accueil {#addnotificationcomponenttothehomepage}

L’équipe de Learning Manager recommande à l’administrateur Salesforce d’ajouter également le composant de notifications Learning Manager à la mise en page de la page d’accueil. Ce composant permet aux utilisateurs de Salesforce d’obtenir des notifications sur les affectations et d’autres annonces de Learning Manager, même lorsqu’elles ne se trouvent pas dans le contexte de l’application de l’élève.

Pour ajouter le composant de notification Learning Manager à la mise en page de la page d’accueil, procédez comme suit :

1. Cliquez sur **[!UICONTROL Configuration]** dans le coin supérieur droit. L’option Mises en page de la page d’accueil s’affiche dans le volet de gauche comme illustré dans l’instantané ci-dessous.

   ![](assets/homepage-component.png)

   *Sélectionnez Mises en page d’accueil.*

1. Choisissez la disposition de votre choix et cliquez sur **[!UICONTROL Modifier]**.
1. Sélectionnez l’option de notification d’Adobe Learning Manager qui apparaît sur la page et cliquez sur **[!UICONTROL Suivant]**.
1. Choisissez l’ordre des composants qui apparaissent dans le volet de gauche, prévisualisez, puis cliquez sur **[!UICONTROL Enregistrer]**.

Pour savoir comment se connecter à l’application Learning Manager et l’utiliser dans Salesforce en tant qu’élève, consultez la section [Contenu de l’aide de l’application Salesforce](../../learners/feature-summary/sfdc-app.md).
