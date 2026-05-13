---
description: Découvrez comment intégrer le connecteur Adobe Commerce
jcr-language: en_us
title: Connecteur Adobe Commerce
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 4%

---


# Connecteur Adobe Commerce dans Adobe Learning Manager

## Connecteur Adobe Commerce

>[!NOTE]
>
>Cette fonctionnalité est disponible uniquement si Adobe Learning Manager est vendu en tant que **module complémentaire** à Adobe Experience Manager. Le connecteur peut également être activé pour les comptes **d&#39;essai**.

Adobe Learning Manager s’intègre à Adobe Commerce, une solution d’e-commerce extensible et évolutive qui vous permet de proposer des expériences commerciales multicanaux aux clients B2B et B2C. Utilisez le connecteur Adobe Commerce pour connecter Adobe Learning Manager à Adobe Commerce afin d’activer les fonctionnalités de formation payante et de commerce électronique dans votre plate-forme d’apprentissage.

Lorsque le connecteur est activé, Learning Manager envoie des données de formation à Adobe Commerce afin que les élèves puissent acheter des cours, des parcours d’apprentissage ou des certifications. Le connecteur collecte également des informations d’achat pour valider les transactions et accorder aux élèves l’accès à leur formation.

## Conditions préalables

Avant de configurer le connecteur Adobe Commerce, vérifiez les points suivants :

- Activez [RabbitMQ](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/start/overview) ou tout autre agent de messagerie.
- Activez les tâches [CRON](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/start/overview#cron_consumers_runner).

Pour les activer, modifiez les fichiers suivants :

- .magento.app.yaml
- .magento/services.yaml
- .magento.env.yaml

Autres exigences de configuration :

- Limite des options de remplacement à l’aide d’un module personnalisé. Cette étape est facultative, mais recommandée pour les jeux de données volumineux.
- Activez toutes les **API asynchrones**. Les jeux de données de formation volumineux sont exportés de manière asynchrone. Lorsque Learning Manager appelle les API Adobe Commerce, les demandes sont placées en file d’attente et traitées par un client qui crée des produits du côté commercial. Le traitement asynchrone doit être activé, car il n’est pas disponible par défaut dans Adobe Commerce.
- Ajoutez un **lien de retour** à Learning Manager sur la page de réussite du paiement dans Adobe Commerce.
   - Utilisez cette [URL de retour](https://learningmanager.adobe.com/app/learner#/postPayment) :
- Remplacez **indexation** de **À l&#39;enregistrement** par **Planifiée**. Voir la [Base de connaissances](https://experienceleague.adobe.com/en/support?support-tab=home#home) pour plus d&#39;informations.
- Appliquez les **correctifs** requis. Voir [Documentation sur l&#39;application des correctifs](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/start/overview) pour obtenir des instructions.
- Configurez **Fastly** pour Adobe Commerce sur l’infrastructure cloud (préparation et production). Voir [Configurer Fastly](https://devdocs.magento.com/cloud/cdn/configure-fastly.html) pour plus d&#39;informations.

## Configuration du connecteur

Pour configurer Adobe Commerce Connector :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Passez le curseur de la souris sur la vignette du connecteur **Adobe Commerce** et sélectionnez **Se connecter**.

   ![](assets/adobe-commerce-connector1.png)
   _Sélectionnez Se connecter pour configurer le connecteur Adobe Commerce_

3. Saisissez les informations suivantes :

   - Nom de la connexion
   - Jeton d’accès
   - URL ADOBE COMMERCE
   - Code boutique
4. Sélectionnez le type d’interface parmi les suivants :

   - Learning Manager natif
   - Personnalisé à l’aide d’AEM Sites

   ![](assets/adobe-commerce-connector2.png)
   _Tapez les détails requis pour la configuration d&#39;Adobe Commerce_

5. Sélectionnez **Se connecter**.

## Fixer le prix de la formation

Une fois la connexion activée :

- Les auteurs peuvent définir les prix des cours, des parcours d’apprentissage ou des certifications.
- Après la publication, les élèves peuvent acheter une formation via Adobe Learning Manager ou un site AEM personnalisé.

## Flux d’achat

### Adobe Learning Manager natif

- Les élèves se connectent à Adobe Learning Manager pour acheter un cours, un parcours d’apprentissage ou un certificat.
- Lorsque les élèves cliquent sur Acheter maintenant, ils sont redirigés vers Adobe Commerce pour finaliser le paiement.
- Après le paiement, les élèves sont invités à retourner dans Adobe Learning Manager pour commencer la formation.
- Les élèves doivent se connecter séparément à Adobe Commerce pour finaliser l’achat.
- Les élèves reçoivent des e-mails de confirmation d’achat de Learning Manager et d’Adobe Commerce. Les e-mails Adobe Commerce peuvent être activés ou désactivés selon les besoins.

### AEM Sites personnalisé

Lors de l’utilisation de sites AEM personnalisés :

- Les élèves peuvent parcourir et acheter des cours via le site AEM.
- Le site AEM utilise les métadonnées synchronisées depuis Adobe Learning Manager pour la recherche et l’affichage.
- Les utilisateurs connectés et invités peuvent parcourir. Cependant, seuls les utilisateurs connectés peuvent acheter.
- Après la connexion, les élèves peuvent ajouter des cours à leur panier, prévisualiser les détails et finaliser l’achat.

## Exportation de cours vers Adobe Commerce

### Planification de l’exportation

Pour planifier l’exportation :

1. Sélectionnez **Exporter les métadonnées de formation**, puis **Configurer la planification**.
2. Sélectionnez **Activer l&#39;exportation des métadonnées de formation avec cette connexion**.
3. Sélectionnez **Activer la planification** et définissez la **date de début**, l&#39;**heure** et l&#39;**intervalle**.

   ![](assets/adobe-commerce-connector3.png)
   _Activer l&#39;exportation planifiée_

4. Sélectionnez **Enregistrer**.

### Exportation à la demande

Une fois que les auteurs ont défini les prix de la formation, l’administrateur d’intégration doit exporter les données de formation :

1. Sélectionnez **Exporter les métadonnées de formation**, puis **À la demande**.
2. Sélectionnez la plage de dates.
3. Sélectionnez **Exécuter** pour exporter.

   ![](assets/adobe-commerce-connector4.png)
   _Créer une exportation à la demande_

4. En cas de réussite, les cours et les parcours d’apprentissage facturés sont déplacés vers Adobe Commerce pour être achetés.
