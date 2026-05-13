---
description: Présentation de chaque connecteur pris en charge par ALM
jcr-language: en_us
title: Présentation des connecteurs compatibles ALM
contentowner: mmanuel
source-git-commit: fc9bf565de2f9491c793654645d2f2400ca49697
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 6%

---


# Connecteurs Adobe Learning Manager

## Introduction

Adobe Learning Manager (ALM) fournit une suite complète de connecteurs qui permettent une intégration transparente avec les applications tierces et les systèmes d’entreprise. Ces connecteurs servent de ponts entre votre système de gestion de l’apprentissage et les plates-formes externes, facilitant la synchronisation automatisée des données, la gestion des utilisateurs, l’importation de contenu et les exportations d’enregistrements d’apprentissage.

Ce document vous sert de guide de référence complet pour comprendre et sélectionner les connecteurs appropriés pour l’écosystème d’apprentissage de votre organisation. Que vous cherchiez à intégrer des systèmes de RH, des plateformes de commerce électronique, des outils de réunion virtuelle ou des solutions de veille stratégique.

Pour obtenir la liste complète des connecteurs pris en charge par Adobe Learning Manager, reportez-vous aux articles sur les connecteurs imbriqués juste en dessous de cet article dans la table des matières à gauche.

>[!NOTE]
>
>Cette fonctionnalité est partiellement disponible dans les environnements autorisés par FedRAMP. Voir [Disponibilité des fonctionnalités dans les environnements FedRAMP](/help/migrated/feature-availability-in-fedramp-authorized-environment.md) pour plus de détails.

>[!NOTE]
>
>Avec la version de novembre 2022 de Adobe Learning Manager, Zoom a abandonné l&#39;[authentification JWT d&#39;ici juin 2023](https://developers.zoom.us/docs/internal-apps/s2s-oauth/). En conséquence, le connecteur Zoom avec JWT continuera de fonctionner jusqu’à la date mentionnée. Toutefois, nous recommandons aux utilisateurs de créer une application OAuth de serveur à serveur pour remplacer la fonctionnalité dans leur compte. Par défaut, l’authentification OAuth Zoom est appliquée aux nouvelles connexions.

## Catégories de connecteurs

Les connecteurs Adobe Learning Manager peuvent être organisés en plusieurs catégories fonctionnelles en fonction de leur objectif principal et de leurs capacités d’intégration :

| Catégorie | Objectif | Exemples de connecteurs |
|---------|--------|-------------------|
| Transfert de données | Opérations d’exchange et de masse de données basées sur les fichiers | FTP, FTP personnalisé, Box |
| Salle de classe virtuelle | Intégration de la formation et des réunions en direct | Microsofts Teams, Zoom, Adobe Connect |
| Systèmes d’entreprise | Intégration des RH et des systèmes d’entreprise | Workday, Salesforce, ADFS |
| Plateformes de contenu | Intégration de contenu d’apprentissage externe | LinkedIn Learning, Harvard ManageMentor, getAbstract |
| Analytics et BI | Création de rapports et visualisation des données | Power BI, Accès aux données de formation |
| Authentification | Gestion des identités et sécurité | ADFS (capacités SSO) |
| e-commerce et marketing | Intégration des ventes et du marketing | Adobe Commerce, Marketo Engage |

## Connecteurs de transfert de données et de gestion de fichiers

Ces connecteurs facilitent l&#39;exchange automatisé des données par le biais de protocoles de transfert de fichiers, permettant des opérations en masse et la communication de système à système.

### Connecteur FTP Adobe Learning Manager

Le connecteur FTP permet aux entreprises d’automatiser la synchronisation des données entre Adobe Learning Manager et des systèmes externes à l’aide du protocole File Transfer Protocol, largement adopté. Ce connecteur prend en charge des variantes sécurisées, notamment SFTP (SSH File Transfer Protocol) et FTPS (FTP Secure) pour une sécurité renforcée.

#### Fonctionnalités clés :

- Chargez et téléchargez des fichiers entre Adobe Learning Manager et des serveurs distants.
- Exchange automatisé des données pour les informations utilisateur et les dossiers de formation.
- Prise en charge des protocoles de transfert de fichiers sécurisés (SFTP, FTPS).
- Traitement par lots de gros volumes de données.

Pour plus d&#39;informations, voir [Connecteur FTP](/help/migrated/integration-admin/feature-summary/ftp-connector.md).

### Connecteur FTP personnalisé

Le connecteur FTP personnalisé offre des fonctionnalités de transfert de fichiers plus sophistiquées, prenant en charge les formats de données structurées et les exchanges d’instruction xAPI. Ce connecteur est conçu pour les organisations nécessitant un contrôle plus précis de leurs processus d&#39;exchange des données.

#### Fonctionnalités clés :

- Importez et exportez des données utilisateur via des fichiers CSV structurés.
- Gérer les enregistrements d’apprentissage et les instructions xAPI.
- Traitement automatisé des fichiers à partir des dossiers FTP désignés.
- Fonctionnalités de sécurité améliorées pour le transfert de données sensibles.

Pour plus d&#39;informations, voir [Connecteur FTP personnalisé](/help/migrated/integration-admin/feature-summary/custom-ftp-connector.md).

### Connecteur Box

Le connecteur Box exploite la plateforme de stockage cloud de Box pour faciliter la synchronisation transparente des données entre les systèmes externes et Adobe Learning Manager. Ce connecteur est particulièrement utile pour les organisations qui utilisent déjà Box pour la gestion de fichiers.

#### Fonctionnalités clés :

- Stockage et synchronisation de fichiers dans le cloud.
- Traitement automatisé des données CSV.
- Intégration avec les workflows Box existants.
- Mises à jour des données en temps réel à partir des dossiers désignés.

## Connecteurs de salle de classe virtuelle et de réunion

Ces connecteurs intègrent Adobe Learning Manager à des plateformes de vidéoconférence et de réunion virtuelle populaires, permettant ainsi la prestation transparente de sessions de formation en direct.

Pour plus d&#39;informations, voir [Connecteur Box](/help/migrated/integration-admin/feature-summary/box-connector.md).

### Connecteur Microsoft Teams

Le connecteur de Microsofts Teams transforme Adobe Learning Manager en une solution complète de classe virtuelle en l’intégrant directement aux fonctionnalités de réunion des équipes. Ce connecteur est essentiel pour les organisations qui utilisent l’écosystème Microsoft 365.

#### Fonctionnalités clés :

- Planifiez des sessions de classe virtuelle directement depuis Adobe Learning Manager.
- Création et gestion automatiques des réunions Teams.
- Accès transparent des élèves sans liens de réunion distincts.

Pour plus d&#39;informations, voir [Connecteur MS Teams](/help/migrated/integration-admin/feature-summary/install-microsoft-teams-connector.md).

### Connecteur Zoom

Le connecteur Zoom permet aux organisations d’exploiter les puissantes fonctionnalités de vidéoconférence de Zoom directement dans leur environnement Adobe Learning Manager, offrant une expérience transparente pour les instructeurs et les élèves.

#### Fonctionnalités clés :

- Planification directe de réunions Zoom à partir de Adobe Learning Manager.
- Génération et distribution automatisées de liens de réunion.
- Surveillance de l’assiduité en temps réel.
- Intégration de la lecture et de la gestion des enregistrements.
- Prise en charge de la salle de réunion pour les sessions interactives.

Pour plus d&#39;informations, voir [Connecteur Zoom](/help/migrated/integration-admin/feature-summary/zoom-connector.md).

### Connecteur Adobe Connect

Le connecteur Adobe Connect s’intègre parfaitement à la plateforme de classe virtuelle d’Adobe, offrant des fonctionnalités avancées pour des expériences d’apprentissage en ligne interactives.

#### Fonctionnalités clés :

- Fonctionnalités interactives avancées (sondages, quiz, présentations).
- Outils de partage d’écran et de présentation de haute qualité.
- Enregistrement et lecture complets des sessions.
- Expérience de classe virtuelle optimisée pour les appareils mobiles.

Pour plus d&#39;informations, voir [Connecteur Adobe Connect](/help/migrated/integration-admin/feature-summary/adobe-connect-connector.md).

## Connecteurs d’intégration de système d’entreprise

Ces connecteurs permettent à Adobe Learning Manager de s’intégrer aux principaux systèmes de l’entreprise, facilitant ainsi la gestion automatisée des utilisateurs et la synchronisation des données organisationnelles.

### Connecteur Workday

Le connecteur Workday crée un pont transparent entre votre système de RH et votre plateforme de gestion de l’apprentissage, garantissant ainsi que les dossiers des employés, les structures organisationnelles et les attributions de rôles restent synchronisés entre les deux systèmes.

#### Fonctionnalités clés :

- Provisionnement automatisé des utilisateurs à partir de Workday.
- Synchronisation des données des employés en temps réel.
- Mappage de la hiérarchie organisationnelle.
- Automatisation des affectations d’apprentissage basées sur les rôles.

Pour plus d&#39;informations, voir [Connecteur Workday](/help/migrated/integration-admin/feature-summary/workday-connector.md).

### Connecteur Salesforce

Le connecteur Salesforce permet aux entreprises d’intégrer leur système de gestion de la relation client à des initiatives d’apprentissage, créant ainsi des opportunités de formation commerciale, d’éducation des clients et de suivi des performances.

#### Fonctionnalités clés :

- Importation automatisée des utilisateurs à partir de Salesforce.
- Mappage des champs de données personnalisés.
- Exportation d’un enregistrement d’apprentissage vers Salesforce.
- Corrélation entre les performances des ventes et l’achèvement de la formation.
- Gestion du programme d’éducation des clients.

Pour plus d&#39;informations, voir [Connecteur Salesforce](/help/migrated/integration-admin/feature-summary/salesforce-connector.md).

### Connecteur ADFS (Active Directory Federation Services)

Le connecteur ADFS permet aux organisations de mettre en œuvre une authentification et une autorisation de niveau entreprise, permettant aux utilisateurs d’accéder à Adobe Learning Manager à l’aide de leurs identifiants Active Directory existants.

#### Fonctionnalités clés :

- Implémentation de l’authentification unique (SSO)
- Conformité de la sécurité de l’entreprise
- Authentification utilisateur transparente

Pour plus d&#39;informations, voir [Connecteur ADFS](/help/migrated/integration-admin/feature-summary/adfs-connector.md).

## Connecteurs de plate-forme de contenu et d’apprentissage

Ces connecteurs étendent votre catalogue d’apprentissage en intégrant des bibliothèques de contenu externes et des plateformes d’apprentissage spécialisées.

### Connecteur LinkedIn Learning

Le connecteur LinkedIn Learning donne accès à la vaste bibliothèque de cours de développement professionnel LinkedIn, ce qui permet aux organisations de compléter leur formation interne avec du contenu externe de référence.

#### Fonctionnalités clés :

- Accès au catalogue complet des cours de LinkedIn Learning.
- Découverte et importation automatisées de cours.
- Suivi de la progression des élèves dans Adobe Learning Manager.

Pour plus d&#39;informations, voir [Connecteur LinkedIn](/help/migrated/integration-admin/feature-summary/linkedin-learning-connector.md).

### Connecteur Harvard ManageMentor

Le connecteur Harvard ManageMentor permet d&#39;intégrer des contenus de formation en leadership et en gestion de classe mondiale directement dans votre environnement Adobe Learning Manager, donnant ainsi accès aux célèbres ressources éducatives de la Harvard Business School.

#### Fonctionnalités clés :

- Accès au contenu Premium de la Harvard Business School.
- Modules de développement de la gestion et du leadership.
- Importation et organisation transparentes du contenu.

Pour plus d&#39;informations, voir [Connecteur Harvard ManageMentor](/help/migrated/integration-admin/feature-summary/harvard-managementor-connector.md).

### getAbstract Connector

Le connecteur getAbstract permet d’accéder à des résumés concis de livres de gestion et à des informations professionnelles, ce qui permet aux organisations d’offrir un apprentissage continu grâce à des formats de contenu assimilables.

#### Fonctionnalités clés :

- Accès aux résumés et informations des livres d’entreprise.
- Suivi et reporting des données d’utilisation.
- Création automatisée des enregistrements d’achèvement.

Pour plus d&#39;informations, voir [connecteur getAbstract](/help/migrated/integration-admin/feature-summary/getabstract-connector.md).

## Connecteurs Business Intelligence et Analytics

Ces connecteurs offrent des fonctionnalités avancées de création de rapports, de visualisation de données et de veille stratégique en intégrant des données d’apprentissage à des plateformes d’analyse externes.

### Connecteur Power BI

Le connecteur de Power BI transforme vos données d’apprentissage en informations professionnelles exploitables en synchronisant automatiquement les métriques d’apprentissage avec la puissante plate-forme de veille stratégique de Microsoft.

#### Fonctionnalités clés :

- Synchronisation des données d’apprentissage en temps réel.
- Création et gestion de tableaux de bord personnalisés.
- Visualisation avancée des données et création de rapports.
- Intégration du relevé de notes de l’élève et du rapport de compétences.

Pour plus d’informations, voir [Connecteur Power BI](/help/migrated/integration-admin/feature-summary/power-bi-connector.md).

### Connecteur d&#39;accès aux données de formation

Le connecteur Training Data Access permet aux organisations de créer des interfaces d’apprentissage personnalisées et des expériences d’apprentissage sans tête en fournissant un accès API aux données de formation et aux informations sur les cours.

**Fonctionnalités clés :**

- Accès API public aux données de cours et de parcours d’apprentissage.
- Prise en charge du développement d’interfaces utilisateur personnalisées.
- Création d’une expérience d’apprentissage sans tête.
- Fonctions avancées de recherche et de filtrage.

Pour plus d&#39;informations, voir [Connecteur Training Data Access](/help/migrated/integration-admin/feature-summary/training-data-access-connector.md).

## Connecteurs e-commerce et marketing

Ces connecteurs permettent la monétisation du contenu d’apprentissage et l’intégration avec les plateformes d’automatisation du marketing.

### Connecteur Adobe Commerce

Le connecteur Adobe Commerce transforme Adobe Learning Manager en une plate-forme complète d’apprentissage et de commerce, permettant aux organisations de vendre des cours, des certifications et des programmes de formation grâce à une expérience d’e-commerce entièrement intégrée.

**Fonctionnalités clés :**

- Intégration transparente de la plateforme d’e-commerce.
- Catalogue de cours et gestion des prix.
- Traitement et inscription automatisés des paiements.

Pour plus d&#39;informations, voir [Connecteur Adobe Commerce](/help/migrated/integration-admin/feature-summary/adobe-commerce-connector.md).

### Connecteur Marketo Engage

Le connecteur Marketo Engage crée de puissantes synergies entre les activités d’apprentissage et les campagnes marketing, permettant aux organisations de tirer parti de l’engagement éducatif pour le développement des prospects et du client.

#### Fonctionnalités clés :

- Création et mises à jour automatisées des prospects.
- Suivi des activités d’apprentissage pour les informations marketing.
- Déclencheurs d’événement d’inscription à un cours et d’achèvement.

Pour plus d&#39;informations, voir [Connecteur Marketo Engage](/help/migrated/integration-admin/feature-summary/marketo-engage-connector.md).
