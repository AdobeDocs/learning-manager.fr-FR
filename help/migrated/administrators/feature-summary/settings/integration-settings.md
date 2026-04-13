---
description: En savoir plus sur la façon dont les paramètres d’intégration connectent Adobe Learning Manager à des solutions tierces
jcr-language: en_us
title: Paramètres d’intégration dans Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 4%

---


# Paramètres d’intégration dans Adobe Learning Manager

## Méthodes de connexion

Adobe Learning Manager propose plusieurs méthodes de connexion pour garantir un accès sécurisé et flexible aux utilisateurs internes et externes. Les administrateurs peuvent configurer ces méthodes de connexion en fonction des exigences organisationnelles.

Les méthodes de connexion disponibles sont les suivantes :

* Identifiant Adobe Learning Manager
* ID Adobe
* Single Sign-On

### Utilisateurs internes

La section Utilisateurs internes vous permet de configurer des options de connexion spécifiquement pour les utilisateurs internes. Les utilisateurs internes peuvent accéder au compte à l’aide d’Adobe ID ou de l’authentification unique (SSO).

**Adobe ID:**

* Les utilisateurs internes peuvent se connecter à l’aide de leurs informations d’identification Adobe ID.
* Convient aux organisations qui utilisent déjà les services Adobe.

**Authentification unique (SSO) :**

* Permet l’authentification unique pour les utilisateurs internes d’utiliser le fournisseur d’identité (IdP) de l’organisation.
* Prend en charge l’authentification basée sur SAML 2.0 pour des expériences de connexion transparentes.

Pour autoriser les connexions SSO pour les utilisateurs internes, sélectionnez Activer plusieurs connexions SSO pour la connexion et commencez à configurer l’authentification unique.

Le champ **[!UICONTROL SSO active]** dans Adobe Learning Manager est utilisé pour mapper les configurations d’authentification unique (SSO) à des attributs ou des groupes d’utilisateurs spécifiques. Vous pouvez configurer ce champ pour activer plusieurs configurations SSO pour les utilisateurs internes en fonction de leur organisation, de leur emplacement ou d’autres critères.

### Utilisateurs externes

La section Utilisateurs externes de Adobe Learning Manager vous permet de gérer les élèves externes, tels que les partenaires ou les agences, qui ont besoin d’un accès limité au compte Adobe Learning Manager. Cette section fournit des outils pour créer des profils d&#39;inscription, gérer des groupes d&#39;utilisateurs externes et configurer des paramètres spécifiques aux élèves externes.

Les utilisateurs externes peuvent se connecter à l’aide des méthodes suivantes :

* Adobe ID : les utilisateurs externes peuvent se connecter à l’aide de leurs informations d’identification Adobe ID.
* Authentification unique (SSO) : les utilisateurs externes peuvent se connecter via SSO si elle est configurée par l’administrateur.
* ID Adobe Learning Manager : les utilisateurs externes peuvent créer un nom d’utilisateur et un mot de passe Learning Manager pour accéder à la plateforme.

**Points clés :**

* Vous pouvez activer une ou plusieurs méthodes de connexion pour les utilisateurs externes.
* Si l’ID Adobe Learning Manager est sélectionné, les utilisateurs externes doivent créer leurs propres informations d’identification.
* L’authentification unique peut être configurée pour les utilisateurs externes en fonction des besoins organisationnels.

### Configuration de l’authentification unique dans Adobe Learning Manager

Adobe Learning Manager prend en charge l’authentification unique (SSO) pour permettre aux utilisateurs de s’authentifier une fois et d’accéder à plusieurs applications. Les administrateurs peuvent configurer l’authentification unique pour les utilisateurs internes et externes à l’aide de fournisseurs basés sur SAML 2.0.

Voir [Connexions SSO dans Adobe Learning Manager](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) pour plus d&#39;informations.

>[!NOTE]
>
>* Vous pouvez ajouter jusque’à 20 configurations SSO (authentification unique) à un compte.
>* Contactez le support technique de l’Adobe pour obtenir de l’aide avec les fournisseurs d’authentification unique basés sur SAML 2.0.

## Sources de données

Les sources de données vous permettent, ou permettent aux administrateurs d’intégration, d’intégrer des systèmes externes pour importer et synchroniser les données utilisateur et d’apprentissage. Cette fonctionnalité garantit une gestion et une synchronisation transparentes des données avec des systèmes tels que HRMS, Salesforce, FTP et autres.

**Exemples de types de sources de données**

* **Connecteurs FTP** : les sources de données FTP permettent aux organisations de charger des fichiers de données utilisateur directement dans Adobe Learning Manager via des protocoles de transfert de fichiers sécurisés. Ces connexions sont particulièrement utiles pour les importations par lots d&#39;informations utilisateur, les inscriptions de cours et d&#39;autres opérations de données en bloc.
* **Intégrations tierces** : Adobe Learning Manager prend en charge l’intégration avec divers systèmes d’entreprise via des connecteurs préconfigurés. Ces intégrations peuvent inclure des systèmes de gestion des RH, des plateformes de gestion de la relation client et d&#39;autres systèmes de gestion de l&#39;apprentissage.
*** l’intégration de Salesforce ** : le connecteur Salesforce permet la synchronisation directe des données utilisateur, des informations sur les cours et des enregistrements d’apprentissage entre Salesforce et Adobe Learning Manager.

Voir [Connecteurs dans Adobe Learning Manager](/help/migrated/integration-admin/feature-summary/connectors.md) pour plus d&#39;informations.

## Comptes de pairs

Les comptes de pairs dans Adobe Learning Manager vous permettent de partager les places achetées et d’afficher des rapports sur les comptes associés. Cette fonctionnalité est utile pour les organisations qui doivent collaborer ou partager des ressources entre différents comptes.

Voir [Comptes de pairs](/help/migrated/administrators/feature-summary/peer-account.md) dans Adobe Learning Manager pour plus d&#39;informations.





