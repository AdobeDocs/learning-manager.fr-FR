---
description: Découvrez comment intégrer le connecteur Training Data Access à Adobe Learning Manager
jcr-language: en_us
title: Connecteur d'accès aux données de formation
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%

---


# Connecteur Training Data Access dans Adobe Learning Manager

## Introduction

Le **connecteur Training Data Access** vous permet de créer une expérience d&#39;apprentissage sans tête qui peut être autonome ou intégrée dans une interface personnalisée créée avec **Adobe Experience Manager (AEM) Sites**. Ce connecteur vous aide à récupérer et à afficher le contenu de formation à jour pour les élèves, avec des fonctionnalités de recherche et de filtrage.

>[!IMPORTANT]
>
>- Cette fonctionnalité est disponible uniquement si Adobe Learning Manager est vendu en tant que **module complémentaire** à Adobe Experience Manager.
>- Les données de cours récupérées via ce connecteur sont actualisées toutes les 24 heures
>- Ce connecteur n’est pas libre-service pour la création d’une expérience sans tête ou non connectée basée sur AEM. Veuillez contacter l’Adobe pour planifier l’approche adaptée à votre cas d’utilisation.

## Fonctionnement du logiciel

Une fois le connecteur activé, Adobe Learning Manager affiche un ensemble d’API publiques qui fournissent des métadonnées de formation telles que des cours, des parcours d’apprentissage et des certificats. Vous pouvez utiliser ces API pour créer un frontal personnalisé de marque qui affiche le contenu de la formation et prend en charge les fonctionnalités de recherche et de filtrage.

## Configuration du connecteur Training Data Access

Vous pouvez intégrer Adobe Learning Manager à votre système de stockage et de recherche de données pour transférer des métadonnées de formation vers AEM Sites ou d’autres expériences sans tête.

Pour configurer le connecteur :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Survolez la vignette **Accès aux données de formation** et sélectionnez **Se connecter**.

   ![](assets/training-data-access-connector1.png)
   _Sélectionnez Se connecter pour configurer le connecteur Training Data Access_

3. Tapez un **nom de connexion**.
4. Sélectionnez le **type d&#39;interface** :

   - **Learning Manager natif** : expérience de connexion standard, disponible par défaut.
   - **Interfaces sans en-tête** : option Premium qui expose les API publiques pour un front-end sans en-tête et sans connexion.

   ![](assets/training-data-access-connector2.png)
   _Tapez les informations requises pour la configuration du connecteur Training Data Access_

5. Sélectionnez **Se connecter**. Adobe Learning Manager génère automatiquement les **URL de base** et **URL CDN**. Vous utiliserez ces URL dans votre site ou application personnalisé(e) pour récupérer les données de formation.

>[!NOTE]
>
>Les clients de la formule Premium reçoivent une URL d’API différente de celle des clients standard.

## Exportation des métadonnées de formation

Pour exporter les métadonnées de formation :

1. Sélectionnez **Exporter les métadonnées de formation** sur la page du connecteur.
2. Sélectionnez **Activer l&#39;exportation des métadonnées de formation à l&#39;aide de cette connexion** pour commencer à transférer vos données de formation vers le système de recherche et d&#39;extraction.
3. Sélectionnez **Activer la planification** et définissez la date de début, l&#39;heure et l&#39;intervalle.

   ![](assets/training-data-access-connector3.png)
   _Planifier l&#39;exportation pour les métadonnées de formation_

4. Sélectionnez **Enregistrer**.

   - Cette opération télécharge automatiquement toutes les images de cours, de parcours d’apprentissage et de certificat sur le **CDN**.
   - Il exporte également les métadonnées associées vers votre système de recherche.

### Exportations à la demande

- **Exécuter les exportations à la demande** Accédez à **À la demande**, définissez la **Date de début** et sélectionnez **Exécuter** pour exécuter une exportation si nécessaire.
- **Vérifier l&#39;état d&#39;exécution :** affichez la progression de l&#39;exportation et l&#39;historique sur la page **État d&#39;exécution**.

## Création et publication du site web dans AEM

Pour afficher des données de formation sur un site Web sans en-tête ou basé sur AEM Sites :

1. **Installez le package AEM** à partir du [référentiel GitHub d&#39;Adobe](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0) (prérequis).
2. Utilisez l&#39;**URL de base**, l&#39;**URL CDN**, l&#39;**ID client**, le **secret client** et le **jeton d&#39;actualisation administrateur** pour créer une configuration dans AEM.
3. Créez le site à l’aide de composants AEM.
4. Publish du site pour les élèves.
5. Pour plus d&#39;informations sur la configuration, consultez [cet article](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/aem-sites/adobe-learning-manager-integration-aem) et [cet article](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/aem-sites/integrate-aem-learning-manager).

### Expérience des élèves

Une fois le site en ligne :

- Le site web affiche tous les **cours**, **parcours d’apprentissage** et **certificats** récupérés auprès de Adobe Learning Manager via le système de recherche.
- Les élèves qui **ne sont pas connectés** peuvent parcourir et afficher les détails du cours.
- Lorsqu&#39;un élève clique pour s&#39;inscrire à un cours, un parcours d&#39;apprentissage ou un certificat, il est invité à **se connecter** pour terminer l&#39;inscription et commencer la formation.

## Expérience hors connexion

L’expérience hors connexion vous permet de créer une expérience en temps réel pour les utilisateurs non connectés. Par exemple, une expérience hors connexion sert de page de destination pour les campagnes marketing visant à encourager les inscriptions.

L&#39;expérience hors connexion dans Adobe Learning Manager peut être configurée à l&#39;aide du connecteur **Training Data Access**. Le connecteur fournit les offres suivantes :

- Offre standard
- Offre Premium

### Offre standard

L’offre standard consiste à créer la version native de Adobe Learning Manager. Les utilisateurs peuvent créer une expérience sans tête de démonstration uniquement et non connectée. L’expérience de démonstration sans en-tête est non évolutive et ne doit pas être utilisée dans un environnement de production.

### Offre Premium

L&#39;offre Premium aide les utilisateurs à créer une interface sans en-tête configurée par le connecteur **Training Data Access**. Cela permet aux utilisateurs d’obtenir des données en temps réel sur le cours et les détails du parcours d’apprentissage tels que le nom, la description, l’auteur, les compétences, la durée, etc. Pour les scénarios d’apprentissage fusionnés, vous bénéficiez également de limites de places en temps réel, de places occupées, de limites de listes d’attente et de nombres de listes d’attente. Les clients peuvent utiliser ces API pour créer des fonctionnalités de recherche et de filtrage et un résumé complet du cours pour les élèves non connectés.

Les clients peuvent acheter une formule Premium pour créer cette expérience hors connexion hautement évolutive.

>[!NOTE]
>
>Veuillez contacter l’équipe de support ou le CSM pour acheter la formule Premium.

Une fois qu’un utilisateur a acheté une formule, l’équipe CSM active la formule Premium pour lui. À l&#39;aide du connecteur Training Data Access, les utilisateurs peuvent configurer une expérience hors connexion avec les fonctionnalités mentionnées précédemment.
