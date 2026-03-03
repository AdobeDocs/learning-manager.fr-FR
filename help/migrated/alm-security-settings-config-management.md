---
title: Adobe Learning Manager - gestion des paramètres de sécurité et de la configuration
description: Ce document décrit les types de comptes administratifs de Adobe Learning Manager, les paramètres de sécurité, les paramètres par défaut sécurisés recommandés, les fonctionnalités d’API, les fonctionnalités d’exportation, les méthodes de comparaison des configurations, les méthodes de publication et l’historique des versions. Il fournit des conseils détaillés sur le fonctionnement des comptes privilégiés, leurs implications en matière de sécurité et la prise en charge de la gestion de la configuration sur l’ensemble de la plateforme.
jcr-language: en-us
exl-id: a2e34104-c417-407f-af85-9f3f4b2a9fcb
source-git-commit: 8b4ac7a99a9bf0cbeaa4ed07fd979deb7130302d
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Gestion des paramètres de sécurité et de configuration

Ce guide fournit des réponses détaillées aux recommandations FedRAMP (FRR-RSC-03 à FRR-RSC-08) pour Adobe Learning Manager (ALM). Il décrit les bonnes pratiques en matière de sécurité, les valeurs par défaut sécurisées recommandées et les outils d’audit, d’exportation et de gestion des paramètres de compte privilégié. Ce document est destiné aux administrateurs et aux équipes de conformité afin de garantir une configuration et une gestion sécurisées des comptes ALM.

Il met également en évidence les domaines dans lesquels ALM répond ou répond partiellement aux normes FedRAMP, avec des références à la documentation et aux ressources disponibles sur Adobe Experience League.

+++Quels paramètres de sécurité ne peuvent être gérés que par des administrateurs personnalisés ou des administrateurs d’intégration dans Adobe Learning Manager, et quelles sont leurs implications en matière de sécurité ?

Les deux types de comptes privilégiés de Adobe Learning Manager : Administrateur personnalisé et Administrateur d’intégration. Chacun dispose d’un ensemble défini de paramètres pertinents pour la sécurité avec des implications documentées.

**Administrateur personnalisé : ce qu&#39;il peut faire** :

* Les rôles personnalisés sont configurés par l’administrateur complet dans Administrateur ALM > Utilisateurs > Rôles personnalisés. Un administrateur personnalisé peut avoir accès à une ou plusieurs des catégories d’autorisations suivantes : Privilèges de compte (annonces, ludification, compétences, gestion des utilisateurs), Privilèges de fonctionnalité (catalogues, rapports, balises) et Privilèges d’objet d’apprentissage (cours, certifications, parcours d’apprentissage).
* La portée est le paramètre le plus sensible en matière de sécurité : un rôle personnalisé peut être limité à des groupes d&#39;utilisateurs spécifiques et/ou à des catalogues spécifiques. Sans restriction de portée, un rôle personnalisé dispose effectivement d&#39;un accès à l&#39;échelle de la plate-forme à ses fonctionnalités accordées, ce qui se rapproche de l&#39;empreinte d&#39;un administrateur complet.
* Si un rôle personnalisé se voit accorder l’accès Paramètres sous Privilèges de compte, cet administrateur personnalisé peut modifier les méthodes de connexion, les paramètres de notification et les configurations au niveau du compte, un privilège à fort impact qui ne doit être accordé qu’avec une justification commerciale explicite.

**Administrateur d&#39;intégration : opérations possibles** :

* Les administrateurs d’intégration gèrent les inscriptions d’applications OAuth 2.0 dans Administrateur d’intégration > Applications > S’inscrire. Ils sélectionnent l’une des six portées OAuth, allant de l’accès en lecture de l’élève à l’accès en lecture/écriture du rôle d’administrateur. La portée de lecture/écriture de l’administrateur accorde à l’application enregistrée les mêmes privilèges qu’un administrateur complet via l’API.
* Les administrateurs d’intégration configurent FTP, SFTP, Salesforce, Workday et d’autres connecteurs qui importent des enregistrements d’utilisateur, des attributions de rôle et des terminaisons de cours, et exportent des données de plateforme vers des systèmes externes.
* Les administrateurs d’intégration configurent des webhooks qui envoient des données d’événement ALM en temps réel (inscriptions, achèvements, changements de rôle) aux URL externes. Un point d’entrée webhook compromis ou mal configuré représente un risque d’exfiltration des données.
* Les administrateurs d’intégration peuvent configurer les intégrations LTI. Une fois activé, LTI ne peut pas être désactivé.

**Références** :

* [Rôles personnalisés | Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/admin/custom-role)
* [Gestion des rôles personnalisés via CSV | Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/configure-role-csv-files)
* [Manuel du développeur d’applications | Adobe Learning Manager][https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual]
* [Connecteurs Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/connectors)

+++

+++Quelles sont les valeurs par défaut sécurisées recommandées pour les comptes administratifs et privilégiés de niveau supérieur dans Adobe Learning Manager, et où sont-elles configurées ?

Les documents Adobe Learning Manager recommandent des valeurs par défaut sécurisées spécifiques pour le rôle Administrateur et les types de comptes privilégiés.

* **Valeurs par défaut du compte Administrateur de niveau supérieur (configuré lors du premier provisionnement)** :

* Méthode de connexion pour les utilisateurs internes : authentification unique (SSO) via SAML 2.0 : configurée dans Administrateur ALM > Paramètres > Méthodes de connexion. N’utilisez pas Adobe ID pour les employés ou les administrateurs.
* Validation en deux étapes (2FA) : appliquée à tous les utilisateurs : configurée dans Adobe Admin Console > Paramètres > Confidentialité et sécurité > Paramètres d’authentification.
* Durée maximale de la session : 8 heures (ou par politique d’organisation) : configurée dans Adobe Admin Console > Paramètres > Confidentialité et sécurité > Paramètres avancés.
* Temps d’inactivité max. : 30 minutes (ou par stratégie d’organisation) : même emplacement que ci-dessus.
* Suppression automatique des utilisateurs inactifs : activée avec une période de rétention définie par l’organisation (par exemple, 90 jours d’inactivité) : Administrateur ALM > Paramètres > Général.
* Expiration du profil utilisateur externe : défini sur chaque profil externe lors de la création : Administrateur ALM > Utilisateurs > Externe. Aucun profil externe indéfini.
* Restrictions d’accès IP : limitez-vous si possible aux plages d’adresses IP approuvées : Admin Console > Paramètres > Paramètres avancés.

**Rôle Administrateur personnalisé par défaut (configuré lors de la création de chaque rôle)** :

* Portée OAuth pour les applications enregistrées : portée minimale requise. N’accordez jamais l’accès en lecture/écriture au rôle Administrateur sauf en cas de nécessité absolue.
* Portée du rôle personnalisé : se limite à des groupes d’utilisateurs et des catalogues spécifiques. Ne créez pas de rôles personnalisés avec une portée Tous les utilisateurs et Tous les catalogues, sauf si la fonction l’exige véritablement.
* Accès aux paramètres dans les rôles personnalisés : n’accordez pas cet accès, sauf si la fonction spécifique l’exige, compte tenu du risque de réaffectation des privilèges.

**Valeurs par défaut de l&#39;administrateur d&#39;intégration** :

* Portée de l’API OAuth : sélectionnez la portée la plus restrictive qui répond aux exigences de l’intégration. N’accordez pas à l’administrateur l’accès en lecture/écriture aux applications nécessitant uniquement un accès en lecture à l’élève.
* Informations d’identification du connecteur, informations d’identification LTI et URL de webhook : ne les partagez jamais par e-mail ni ne les validez pour le contrôle de code source.

**Références** :

* [Paramètres | Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/admin/custom-role)
* [Authentification et mots de passe sécurisés des utilisateurs | Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/authentication-settings.html)
* [Rôles personnalisés | Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/admin/custom-role)

+++

+++Adobe Learning Manager offre-t-il aux administrateurs un moyen de comparer les paramètres de compte actuels aux paramètres sécurisés par défaut recommandés ?

Adobe Learning Manager ne dispose pas d’un tableau de bord de comparaison dédié qui affiche automatiquement les paramètres actuels en plus des valeurs sécurisées par défaut recommandées.

**Rapport de rôle personnalisé : attributions de rôle privilégiées actuelles** :

* Dans ALM, accédez à Admin > Utilisateurs > Rôles personnalisés et cliquez sur Télécharger (en haut à droite) pour exporter un fichier CSV de tous les rôles personnalisés, de leurs jeux d’autorisations et de leurs affectations d’étendue.
* Comparez cette exportation aux valeurs par défaut recommandées dans la section 8 du document FRR-RSC-02, en vérifiant spécifiquement si un rôle personnalisé a un accès Paramètres, une portée Tous les utilisateurs ou une portée Tous les catalogues sans justification documentée.

**API REST ALM : récupération de configuration programmatique** :

* Le point de terminaison GET /account renvoie les données de configuration au niveau du compte au format JSON, accessibles à l’aide de la portée OAuth du rôle Administrateur. Les clients peuvent appeler ce point de terminaison par programme et différencier la réponse par rapport à une ligne de base dérivée des valeurs par défaut recommandées dans la section 8 du document FRR-RSC-02.
* Le point de terminaison GET /users (avec include=role filter) renvoie les attributions de rôle actuelles pour tous les utilisateurs, permettant ainsi la détection automatique des attributions de rôle inattendues.

>[!NOTE]
>
>Adobe Learning Manager n’offre pas d’interface utilisateur native de comparaison côte à côte. Les clients nécessitant un contrôle de conformité automatisé de la configuration doivent intégrer l’API REST ALM à leur outil existant.

**Référence**

* [Manuel du développeur d’applications | Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual)

+++

+++Les administrateurs peuvent-ils exporter les paramètres et configurations actuels relatifs à la sécurité depuis Adobe Learning Manager dans un format lisible par machine ?

Adobe Learning Manager prend en charge l’exportation des données de configuration relatives à la sécurité par plusieurs mécanismes. Aucune exportation individuelle ne produit un instantané complet de tous les paramètres de sécurité en une seule fois, mais les exportations suivantes couvrent collectivement l’ensemble de la portée des données pertinentes pour la sécurité.

**API REST ALM : exportation au format JSON des attributions de rôle actuelles et de la configuration du compte** :

* GET /account : renvoie les paramètres au niveau du compte dans JSON, y compris les données de configuration de connexion active et les métadonnées du compte.
* GET /users?include=role : renvoie tous les utilisateurs avec leurs rôles actuellement attribués dans JSON.
* GET /userGroups : renvoie tous les groupes d&#39;utilisateurs et leur appartenance, pertinents pour l&#39;audit de la portée du rôle personnalisé.
* Toutes les réponses API sont au format JSON (vnd.api+json). L’authentification utilise OAuth 2.0 avec une portée de lecture/écriture du rôle Administrateur.

**Exportation CSV de rôle personnalisé : définitions de rôle privilégiées actuelles** :

* L’administrateur ALM > Utilisateurs > Rôles personnalisés > Télécharger exporte un fichier CSV de toutes les définitions de rôle personnalisé, de leurs catégories d’autorisations et des attributions de portée.
* Cette exportation peut être utilisée comme instantané lisible par ordinateur de la configuration actuelle du compte privilégié.
**

**API des tâches : données d&#39;utilisateur et de rôle en bloc** :

* L’API des tâches ALM prend en charge la génération à la demande de rapports utilisateur (y compris les attributions de rôles) au format CSV. Ils peuvent être programmés et utilisés par des outils de conformité externe ou SIEM.

**Référence**

* [Manuel du développeur d’applications | Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual)

+++

+++Adobe Learning Manager fournit-il une API qui permet d’afficher et d’ajuster par programmation les paramètres relatifs à la sécurité ?

Adobe Learning Manager fournit une API REST v2 complète qui permet l’affichage et l’ajustement par programmation des paramètres de sécurité à l’aide de l’authentification OAuth 2.0. Voici les fonctionnalités d’API spécifiques relatives aux paramètres de sécurité :

**Authentification et étendue** :

* Les applications sont enregistrées par l’administrateur d’intégration sous Administration de l’intégration > Applications > Enregistrer. L’ID client et le secret OAuth 2.0 sont émis par application.
* Six portées sont disponibles. Pour la gestion des paramètres de sécurité, un accès en lecture/écriture au rôle Administrateur est requis. Cela accorde à l’application le même accès qu’un administrateur complet via l’API.
* Les jetons d’accès sont obtenus via le code d’autorisation OAuth standard ou le flux d’informations d’identification du client. URL de base : https://learningmanager.adobe.com/primeapi/v2/

**Gestion des utilisateurs et des rôles via l&#39;API** :

* GET /users : récupérer tous les utilisateurs et leurs rôles actuels
* POST /users : provisionner de nouveaux utilisateurs par programme
* PATCH /users/{id} : mettre à jour les attributs utilisateur, y compris les attributions de rôle
* DELETE /users/{id} : désactiver un compte utilisateur
* POST /users/{id}/purge : purge définitivement un utilisateur et tous les enregistrements associés

Récupération de la configuration du compte :

* GET /account : renvoie la configuration au niveau du compte, y compris les données des paramètres de compte au format JSON, y compris les champs tels que complianceLabelDefaultID, showComplianceLabel et custom_injections.

+++

+++Adobe Learning Manager publie-t-il ses conseils de configuration sécurisée dans un format lisible par machine tel qu’OSCAL, JSON ou YAML ?

Adobe Learning Manager ne publie pas actuellement son Guide de configuration sécurisée dans un format lisible par machine. Les conseils de [FRR-RSC-01](/help/migrated/alm-administrative-lifecycle.md) et [FRR-RSC-02](/help/migrated/alm-secure-administration-guide.md) sont publiés sous forme de documentation lisible par l’homme sur Adobe Experience League dans des formats de document HTMLS et téléchargeables.

Il n’existe aucune définition de composant OSCAL, ligne de base YAML ou fichier de stratégie JSON publiquement disponible codant les valeurs par défaut sécurisées recommandées pour Adobe Learning Manager.

Les clients qui ont besoin de comparer automatiquement les paramètres actuels avec les lignes de base recommandées doivent utiliser l&#39;[API REST ALM](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/developer-manual) pour récupérer les données de configuration actuelles au format JSON.

+++

+++Le Guide de configuration sécurisée de Adobe Learning Manager est-il accessible au public sans connexion ni accès spécial ?

**Éléments accessibles au public** :

* [FRR-RSC-01 : Guide de l&#39;administrateur sécurisé](/help/migrated/alm-administrative-lifecycle.md) : conseils sur le cycle de vie complet pour les comptes administratifs de niveau supérieur.
* [FRR-RSC-02 : Paramètres et implications de sécurité administrative](/help/migrated/alm-secure-administration-guide.md) : tous les paramètres pertinents pour la sécurité, leurs implications et les valeurs par défaut recommandées.
* FRR-RSC-03-10 (le présent document) — Réponses aux questions et réponses aux huit recommandations de FedRAMP.

+++

+++Adobe Learning Manager fournit-il un contrôle de version et un historique des versions qui permettent aux agences de suivre les modifications apportées aux paramètres de sécurité et aux paramètres par défaut recommandés au fil du temps ?

Adobe Learning Manager conserve un historique des versions détaillé et accessible au public pour chaque mise à jour de produit. Les modifications relatives à la sécurité des paramètres d’administration, des fonctionnalités d’authentification, des points de terminaison d’API et des fonctionnalités de gestion des rôles sont documentées dans chaque version.

**Notes de mise à jour ALM : numérotées, historique cumulatif des modifications** :

* Adobe publie des notes de mise à jour numérotées pour chaque mise à jour de Adobe Learning Manager (par exemple, Mise à jour 100, Mise à jour 99). Ils sont publiés sur l’Experience League et documentent toutes les nouvelles fonctionnalités, les modifications apportées aux paramètres existants, les ajouts et suppressions d’API, les modifications de connecteur et les fonctionnalités obsolètes.
* Chaque note de mise à jour comprend une section dédiée aux modifications d’API, qui répertorie les nouveaux points de terminaison, les champs de réponse modifiés et les dépréciations, en lien direct avec les fonctionnalités de configuration relatives à la sécurité.

**Nouvelles pages : résumés des fonctionnalités par version** :

* Chaque version majeure dispose d’une page « Nouveautés » dédiée qui documente les nouvelles fonctionnalités de sécurité en contexte. Par exemple, les notes de mise à jour incluent des modifications apportées à la gestion des autorisations de rôle personnalisé, l’ajout de la visibilité des autorisations créées par CSV pour les rôles personnalisés et des modifications de limitation du taux d’API.

**Liste des API obsolètes : enregistrement faisant autorité des capacités d’API supprimées** s :

* L’Adobe conserve une page Dépréciations d’API dédiée répertoriant tous les points d’entrée API ALM obsolètes et supprimés avec la version publiée dans laquelle chaque dépréciation s’est produite.

**Références** :

* [Notes de mise à jour de Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/introduction/release-notes)
* [Nouveautés de Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/introduction/whats-new-july-2024)
* [Dépréciations d’API dans Adobe Learning Manager](https://experienceleague.adobe.com/fr/docs/learning-manager/using/introduction/api-deprecations-list)

+++
