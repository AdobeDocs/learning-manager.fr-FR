---
title: Cycle de vie du compte d’administration Adobe Learning Manager
description: Ce document fournit un résumé complet des fonctionnalités de gestion, de configuration et de conformité des comptes de sécurité (ALM) de Adobe Learning Manager alignées sur les recommandations FedRAMP.
jcr-language: en-us
source-git-commit: 06051e44c0a6bc8ae60e44272ba088f2f6ff281f
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 0%

---


# recommandations de sécurité Adobe Learning Manager

## Quels paramètres de sécurité ne peuvent être gérés que par des administrateurs personnalisés ou des administrateurs d’intégration dans Adobe Learning Manager, et quelles sont leurs implications en matière de sécurité ?

Les deux types de comptes privilégiés de Adobe Learning Manager, Administrateur personnalisé et Administrateur d’intégration, disposent chacun d’un ensemble défini de paramètres de sécurité ayant des implications documentées.

### Administrateur personnalisé : ce qu’ils peuvent faire :

* Les rôles personnalisés sont configurés par l’administrateur complet dans Administrateur ALM > Utilisateurs > Rôles personnalisés. Un administrateur personnalisé peut avoir accès à une ou plusieurs des catégories d’autorisations suivantes : Privilèges de compte (annonces, ludification, compétences, gestion des utilisateurs), Privilèges de fonctionnalité (catalogues, rapports, balises) et Privilèges d’objet d’apprentissage (cours, certifications, parcours d’apprentissage).
* La portée est le paramètre le plus sensible en matière de sécurité : un rôle personnalisé peut être limité à des groupes d&#39;utilisateurs spécifiques et/ou à des catalogues spécifiques. Sans restriction de portée, un rôle personnalisé dispose effectivement d&#39;un accès à l&#39;échelle de la plate-forme à ses fonctionnalités accordées, ce qui se rapproche de l&#39;empreinte d&#39;un administrateur complet.
* Si un rôle personnalisé se voit accorder l’accès Paramètres sous Privilèges de compte, cet administrateur personnalisé peut modifier les méthodes de connexion, les paramètres de notification et les configurations au niveau du compte, un privilège à fort impact qui ne doit être accordé qu’avec une justification commerciale explicite.
* Un administrateur personnalisé disposant d’un accès aux paramètres et d’un accès aux entités Utilisateurs peut s’attribuer le rôle d’administrateur complet, ce qui revient à exercer un contrôle administratif total.

### Administrateur d’intégration : ce qu’il peut faire :

* Les administrateurs d’intégration gèrent les inscriptions d’applications OAuth 2.0 dans Administrateur d’intégration > Applications > S’inscrire. Ils sélectionnent l’une des six portées OAuth, allant de l’accès en lecture de l’élève à l’accès en lecture/écriture du rôle d’administrateur. La portée de lecture/écriture de l’administrateur accorde à l’application enregistrée les mêmes privilèges qu’un administrateur complet via l’API.
* Les administrateurs d’intégration configurent FTP, SFTP, Salesforce, Workday et d’autres connecteurs qui importent des enregistrements d’utilisateur, des attributions de rôle et des terminaisons de cours, et exportent des données de plateforme vers des systèmes externes.
* Portée OAuth pour les applications enregistrées : portée minimale requise. N’accordez jamais l’accès en lecture/écriture au rôle Administrateur sauf en cas de nécessité absolue.
* Les administrateurs d’intégration configurent des webhooks qui envoient des données d’événement ALM en temps réel (inscriptions, achèvements, changements de rôle) aux URL externes. Un point d’entrée webhook compromis ou mal configuré représente un risque d’exfiltration des données.
* Les administrateurs d’intégration peuvent configurer les intégrations LTI. Une fois activé, LTI ne peut pas être désactivé. Les identifiants LTI exposés permettent un accès non autorisé au contenu du cours à partir de plates-formes LMS externes.


## Quelles sont les valeurs par défaut sécurisées recommandées pour les comptes administratifs et privilégiés de niveau supérieur dans Adobe Learning Manager, et où sont-elles configurées ?

### Valeurs par défaut du compte Administrateur de niveau supérieur (configuré lors du premier provisionnement) :

* Méthode de connexion pour les utilisateurs internes : authentification unique (SSO) via SAML 2.0 : configurée dans Administrateur ALM > Paramètres > Méthodes de connexion. N’utilisez pas Adobe ID pour les employés ou les administrateurs.
* Validation en deux étapes (2FA) : appliquée à tous les utilisateurs : configurée dans Adobe Admin Console > Paramètres > Confidentialité et sécurité > Paramètres d’authentification.
* Durée maximale de la session : 8 heures (ou par politique d’organisation) : configurée dans Adobe Admin Console > Paramètres > Confidentialité et sécurité > Paramètres avancés.
* Temps d’inactivité max. : 30 minutes (ou par stratégie d’organisation) : même emplacement que ci-dessus.
* Suppression automatique des utilisateurs inactifs : activée avec une période de rétention définie par l’organisation (par exemple, 90 jours d’inactivité) : Administrateur ALM > Paramètres > Général.
* Expiration du profil utilisateur externe : défini sur chaque profil externe lors de la création - Administrateur ALM > Utilisateurs > Externe. Aucun profil externe indéfini.
* Restrictions d’accès IP : limitez-vous si possible aux plages d’adresses IP approuvées - Admin Console > Paramètres > Paramètres avancés.

### Rôle Administrateur personnalisé par défaut (configuré lors de la création de chaque rôle) :

* Portée OAuth pour les applications enregistrées : portée minimale requise. N’accordez jamais l’accès en lecture/écriture au rôle Administrateur sauf en cas de nécessité absolue.
* Portée du rôle personnalisé : se limite à des groupes d’utilisateurs et des catalogues spécifiques. Ne créez pas de rôles personnalisés avec une portée Tous les utilisateurs et Tous les catalogues, sauf si la fonction l’exige véritablement.
* Accès aux paramètres dans les rôles personnalisés : n’accordez pas cet accès, sauf si la fonction spécifique l’exige, compte tenu du risque de réaffectation des privilèges.

### Valeurs par défaut de l’administrateur d’intégration :

* Portée de l’API OAuth : sélectionnez la portée la plus restrictive qui répond aux exigences de l’intégration. N’accordez pas à l’administrateur l’accès en lecture/écriture aux applications nécessitant uniquement un accès en lecture à l’élève.
* Informations d’identification du connecteur, informations d’identification LTI et URL de webhook : ne les partagez jamais par e-mail ni ne les validez pour le contrôle de code source.

## Adobe Learning Manager offre-t-il aux administrateurs un moyen de comparer les paramètres de compte actuels aux paramètres sécurisés par défaut recommandés ?

Adobe Learning Manager ne dispose pas d’un tableau de bord de comparaison dédié qui affiche automatiquement les paramètres actuels en plus des valeurs sécurisées par défaut recommandées. Toutefois, trois fonctionnalités de plate-forme permettent aux administrateurs d&#39;auditer et de comparer les configurations actuelles manuellement ou par programme.

### Rapport de rôle personnalisé - attributions de rôle privilégiées actuelles :

Dans ALM, accédez à Admin > Utilisateurs > Rôles personnalisés et cliquez sur Télécharger (en haut à droite) pour exporter un fichier CSV de tous les rôles personnalisés, de leurs jeux d’autorisations et de leurs affectations d’étendue.

### API REST ALM - Récupération de la configuration programmatique :

* Le point de terminaison GET /account renvoie les données de configuration au niveau du compte au format JSON, accessibles à l’aide de la portée OAuth du rôle Administrateur. Les clients peuvent appeler ce point de terminaison par programme.
* Le point de terminaison GET /users (avec include=role filter) renvoie les attributions de rôle actuelles pour tous les utilisateurs, permettant ainsi la détection automatique des attributions de rôle inattendues. Utilisez l’API Jobs pour les exportations d’utilisateurs par lot.

## Les administrateurs peuvent-ils exporter les paramètres et configurations actuels relatifs à la sécurité depuis Adobe Learning Manager dans un format lisible par machine ?

Adobe Learning Manager prend en charge l’exportation des données de configuration relatives à la sécurité par plusieurs mécanismes. Aucune exportation individuelle ne produit un instantané complet de tous les paramètres de sécurité en une seule fois, mais les exportations suivantes couvrent collectivement l’ensemble de la portée des données pertinentes pour la sécurité.

### Journal d’audit du Admin Console — Exportation au format CSV de toutes les authentifications et modifications de rôle :

* Dans Adobe Admin Console, accédez à **Données > Journaux > Journal d’audit**, appliquez des filtres selon vos besoins, puis cliquez sur **Exporter en CSV**
* Le fichier CSV exporté enregistre chaque action administrative, y compris : les modifications d’application 2FA, les modifications de limite de session, les attributions et les suppressions de rôles d’administrateur, les suppressions d’utilisateurs et les modifications de droits d’accès au produit, le tout avec des horodatages et l’identité des acteurs.
* Les données sont conservées pendant 90 jours. Les utilisateurs de Global Admin Console peuvent exporter des journaux dans toutes les organisations.

### API REST ALM - Exportation au format JSON des attributions de rôle actuelles et de la configuration du compte :

* `GET /account` — renvoie les paramètres au niveau du compte au format JSON, y compris les données de configuration de connexion active et les métadonnées du compte.
* `GET /users?include=role` — renvoie tous les utilisateurs avec leurs rôles actuellement attribués dans JSON.
* `GET /userGroups` — renvoie tous les groupes d&#39;utilisateurs et leur appartenance, pertinents pour l&#39;audit de la portée du rôle personnalisé.
* Toutes les réponses API sont au format JSON (`vnd.api+json`). L’authentification utilise OAuth 2.0 avec une portée de lecture/écriture du rôle Administrateur.

### Exportation CSV de rôle personnalisé - définitions de rôle privilégiées actuelles :

* L’administrateur ALM > Utilisateurs > Rôles personnalisés > Télécharger exporte un fichier CSV de toutes les définitions de rôle personnalisé, de leurs catégories d’autorisations et des attributions de portée.
* Cette exportation peut être utilisée comme instantané lisible par ordinateur de la configuration actuelle du compte privilégié.

### API des tâches : données d’utilisateur et de rôle en bloc :

* L’API des tâches ALM prend en charge la génération à la demande de rapports utilisateur (y compris les attributions de rôles) au format CSV. Ils peuvent être programmés et utilisés par des outils de conformité externe ou SIEM.

Voir [Adobe Learning Manager- Manuel du développeur d&#39;applications](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual) pour plus d&#39;informations.

## Adobe Learning Manager fournit-il une API qui permet d’afficher et d’ajuster par programmation les paramètres relatifs à la sécurité ?

Adobe Learning Manager fournit une API REST v2 complète qui permet l’affichage et l’ajustement par programmation des paramètres de sécurité à l’aide de l’authentification OAuth 2.0. Voici les fonctionnalités d’API spécifiques relatives aux paramètres de sécurité :

### Authentification et portée

* Les applications sont enregistrées par l&#39;administrateur d&#39;intégration sous **Administrateur d&#39;intégration > Applications > S&#39;inscrire**. L’ID client et le secret OAuth 2.0 sont émis par application.
* Six portées sont disponibles. Pour la gestion des paramètres de sécurité, un accès en lecture/écriture **au rôle** administrateur est requis. Cela accorde à l’application le même accès qu’un administrateur complet via l’API.
* Les jetons d’accès sont obtenus via le code d’autorisation OAuth standard ou le flux d’informations d’identification du client.\
  **URL de base :**\
  `https://learningmanager.adobe.com/primeapi/v2/`

### Gestion des utilisateurs et des rôles via l’API

* `GET /users` — récupérer tous les utilisateurs et leurs rôles actuels
* `POST /users` — provisionner de nouveaux utilisateurs par programme
* `PATCH /users/{id}` — mettre à jour les attributs utilisateur, y compris les attributions de rôle
* `DELETE /users/{id}` — désactiver un compte d&#39;utilisateur
* `POST /users/{id}/purge` — purger définitivement un utilisateur et tous les enregistrements associés

### Récupération de la configuration du compte

* `GET /account` — renvoie la configuration au niveau du compte, y compris les données des paramètres de compte au format JSON, y compris les champs tels que :
   * `complianceLabelDefaultID`
   * `showComplianceLabel`
   * `custom_injections`

### API User Management d’Adobe (couche Admin Console)

* L’API de gestion des utilisateurs d’Adobe (UMAPI) fournit un accès par programme aux opérations du Admin Console :
   * Approvisionnement des utilisateurs
   * Attribution de droits sur les produits
   * Attribution du rôle d’administrateur système au niveau de l’organisation
* UMAPI est une interface distincte de l’API REST ALM et fonctionne au niveau de l’organisation de l’Adobe. Utilisez-le pour automatiser les attributions de rôle de Admin Console et le provisionnement des utilisateurs.

## Adobe Learning Manager publie-t-il ses conseils de configuration sécurisée (valeurs par défaut recommandées) dans un format lisible par machine tel qu’OSCAL, JSON ou YAML ?

Adobe Learning Manager ne publie pas actuellement son Guide de configuration sécurisée dans un format lisible par machine.

## Le Guide de configuration sécurisée de Adobe Learning Manager est-il accessible au public sans connexion ni accès spécial ?

Oui. Le Guide de configuration sécurisée de Adobe Learning Manager est accessible au public sur Adobe Experience League. Aucun compte, connexion ou licence n’est requis pour y accéder.

Éléments accessibles au public :

* FRR-RSC-01 : Guide d’administration sécurisée : guide sur le cycle de vie complet pour les comptes administratifs de niveau supérieur.
* FRR-RSC-02 : Paramètres et implications de sécurité administrative : tous les paramètres pertinents pour la sécurité, leurs implications et les valeurs par défaut recommandées.

## Adobe Learning Manager fournit-il un contrôle de version et un historique des versions qui permettent aux agences de suivre les modifications apportées aux paramètres de sécurité et aux paramètres par défaut recommandés au fil du temps ?

Adobe Learning Manager conserve un historique des versions détaillé et accessible au public pour chaque mise à jour de produit. Les modifications relatives à la sécurité des paramètres d’administration, des fonctionnalités d’authentification, des points de terminaison d’API et des fonctionnalités de gestion des rôles sont documentées dans chaque version.

### Notes de mise à jour ALM : historique des modifications cumulées et numérotées

* Adobe publie des notes de mise à jour numérotées pour chaque mise à jour de Adobe Learning Manager (par exemple, *Mise à jour 100*, *Mise à jour 99*).
* Ceux-ci sont publiés sur **Experience League** et le document :
   * Nouvelles fonctionnalités
   * Modifications apportées aux paramètres existants
   * Ajouts et suppressions d’API
   * Modifications apportées au connecteur
   * Fonctionnalités obsolètes
* Chaque note de mise à jour comprend une section dédiée aux **modifications d’API**, répertoriant :
   * Nouveaux points de terminaison
   * Champs de réponse modifiés
   * Dépréciations
   * Ils concernent directement les capacités de configuration relatives à la sécurité.

### Pages « Nouveautés » — Récapitulatifs des fonctionnalités par version

* Chaque version majeure dispose d&#39;une page **« Nouveautés »** dédiée documentant les nouvelles fonctionnalités de sécurité en contexte.
* Voici quelques exemples de mises à jour de sécurité documentées :
   * Modifications apportées à la gestion des autorisations de rôle personnalisé
   * Ajout de visibilité des autorisations créées au format CSV pour les rôles personnalisés
   * Modifications de la limitation du taux d’API

### Liste des API obsolètes : enregistrement faisant autorité des fonctionnalités API supprimées

* L&#39;Adobe conserve une page dédiée **Dépréciations d&#39;API** répertoriant tous les points d&#39;entrée d&#39;API ALM obsolètes et supprimés, y compris la version dans laquelle chaque dépréciation s&#39;est produite.
* Voici quelques exemples de dépréciations liées à la sécurité :
   * Modifications apportées au comportement de tri et de remplacement du point de terminaison `GET /users`
   * Notification, filtre de date de rapport

