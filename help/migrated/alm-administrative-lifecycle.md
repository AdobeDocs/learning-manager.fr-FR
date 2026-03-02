---
title: Cycle de vie du compte d’administration Adobe Learning Manager
description: Ce document fournit des conseils complets sur la gestion sécurisée des comptes administratifs de niveau supérieur dans Adobe Learning Manager (ALM) afin de respecter la conformité FedRAMP et les meilleures pratiques de sécurité.
jcr-language: en-us
source-git-commit: db3ed4dc44da75b418e923999bdf3776bf81b11f
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---


# Types de comptes d’administration dans Adobe Learning Manager

## Mappage de rôle ALM

Dans Adobe Learning Manager, le compte administratif de niveau supérieur est le rôle Administrateur. Il s&#39;agit du rôle auquel il est fait référence chaque fois que ce guide utilise le terme FedRAMP « compte administratif de niveau supérieur ». Les administrateurs personnalisés et les administrateurs d’intégration sont traités comme des comptes privilégiés (étendus).

Le tableau ci-dessous met en correspondance les niveaux de compte FedRAMP avec les rôles spécifiques utilisés dans Adobe Learning Manager :

| Terme FedRAMP | Nom du rôle ALM | Description |
|--------------------------------------|----------------------------|-------------|
| Compte d’administration de niveau supérieur | L’administrateur | Rôle de privilèges les plus élevés dans ALM. Contrôle total des utilisateurs, des rôles, du contenu d’apprentissage, des rapports, des intégrations et de toutes les configurations système. Mappe directement à la définition du compte administratif de niveau supérieur FedRAMP. |
| Compte privilégié (étendue) | Administrateur personnalisé | Sous-ensemble défini d’autorisations d’administrateur dont la portée s’étend à des fonctions spécifiques (par exemple, création de rapports, gestion de catalogue). Ne dispose pas du contrôle complet au niveau du compte. |
| Compte privilégié (intégration) | Administrateur d’intégration | Gère les intégrations et l’accès basé sur les API entre ALM et les systèmes externes. Privilèges élevés limités à la gestion de l’intégration. |


Adobe Learning Manager utilise un modèle de contrôle d’accès basé sur les rôles (RBAC) pour gérer les accès administratifs. Les rôles administratifs sont attribués uniquement par les administrateurs autorisés.

Voir [Rôles personnalisés dans Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) pour plus d&#39;informations

## Types d’identité et authentification recommandée

Adobe Admin Console prend en charge trois types d’identité pour les comptes administrateur. Le choix du type d’identité a des conséquences directes sur la sécurité :

| Type d’identité | Description | Recommandation de sécurité |
|---------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Adobe ID (ID personnel) | Type par défaut ; géré par Adobe. N&#39;importe qui peut en créer un. | NON RECOMMANDÉ pour les administrateurs. L’organisation n’a aucun contrôle sur ce type de compte. |
| Enterprise ID | Compte appartenant à l’organisation géré par un administrateur système Admin Console. | Acceptable si le Federated ID/SSO n’est pas disponible. Appliquer 2FA. |
| Federated ID (SSO) | Propriété de l’organisation ; intégrée à SAML 2.0 SSO. L’organisation contrôle entièrement l’authentification. | RECOMMANDÉ. S’authentifie via l’IdP de l’organisation ; prend en charge l’application MFA au niveau du fournisseur d’identité. |

Pour plus d’informations, voir les sections suivantes :

* [Types d’identité](https://helpx.adobe.com/enterprise/using/admin-console.html)
* [Authentification et mots de passe sécurisés des utilisateurs](https://helpx.adobe.com/enterprise/using/authentication-settings.html)

## Attribution de rôles et contrôle d’accès

L&#39;accès aux comptes administratifs dans Adobe Learning Manager est contrôlé par l&#39;[attribution de rôles](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) explicite par un administrateur existant. Les principales caractéristiques d’un accès administratif sécurisé sont les suivantes :

* Les rôles administratifs sont attribués uniquement par les administrateurs autorisés.
* L’accès est basé sur les rôles et sa portée dépend des autorisations attribuées.
* Il incombe aux organisations de limiter l’accès administratif aux utilisateurs ayant des besoins commerciaux légitimes.

L’Adobe recommande aux clients de passer régulièrement en revue l’accès administratif pour s’assurer du respect du principe du moindre privilège.

## Appliquer l’authentification multifacteur (MFA)

L’Adobe recommande vivement aux administrateurs d’appliquer la vérification en deux étapes (2FA) à l’échelle de l’organisation. L’authentification multifacteur s’applique aux utilisateurs de Enterprise ID et d’Adobe ID. L’authentification multifacteur doit être appliquée aux utilisateurs du Federated ID auprès du fournisseur d’identité de leur organisation.

Pour appliquer 2FA dans Adobe Admin Console :

1. Connectez-vous à Adobe Admin Console.
2. Accédez à Paramètres > Confidentialité et sécurité > Paramètres d’authentification.
3. Activez la validation en deux étapes et sélectionnez l’option Appliquer pour empêcher les utilisateurs de la désactiver.
4. Configurez éventuellement les restrictions d’accès basées sur IP et les paramètres de session avancés (Durée max. de la session / Temps max. d’inactivité).

>[!IMPORTANT]
>
>L’Adobe recommande d’appliquer la 2FA et de ne pas la laisser facultative pour les utilisateurs. L’application de la 2FA peut prendre jusqu’à 24 heures. Pour les utilisateurs de Federated ID, appliquez l’authentification multifacteur auprès de votre fournisseur d’identité.

Voir [Authentification sécurisée des utilisateurs pour plus d&#39;informations](https://helpx.adobe.com/enterprise/using/authentication-settings.html).


## Se connecter en tant qu’administrateur

Les [administrateurs](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-admin) ALM se connectent directement à la plateforme ALM à l’aide des informations d’identification de l’organisation gérées par le Admin Console.

### Attribution d’un rôle d’administrateur

Au sein de la plateforme ALM, les administrateurs configurent l’accès administratif en créant et en gérant des rôles, en attribuant des autorisations aux utilisateurs et en définissant la portée des autorisations en fonction des responsabilités opérationnelles.

Pour attribuer le rôle Administrateur dans ALM :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur existant.
2. Accédez à Utilisateurs > Interne.
3. Recherchez ou sélectionnez l’utilisateur cible.
4. Sélectionnez Actions > Attribuer un rôle > Rendre administrateur.

Les rôles administratifs personnalisés permettent aux clients de déléguer des tâches administratives tout en conservant un contrôle centralisé sur les privilèges au niveau du compte. Les administrateurs personnalisés peuvent être limités à des groupes d’utilisateurs ou des catalogues spécifiques.

Voir [Ajouter des utilisateurs et des groupes d&#39;utilisateurs](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) pour plus d&#39;informations.

## Configuration des méthodes de connexion et de l’authentification unique

Les administrateurs ALM contrôlent les méthodes de connexion disponibles pour tous les utilisateurs via Paramètres > Méthodes de connexion, une configuration importante pour la sécurité :

* **Utilisateurs internes** : définissez le mode de connexion sur Adobe ID ou Authentification unique (SSO). L’authentification unique via SAML 2.0 est fortement recommandée.
* **Utilisateurs externes** : définissez le mode de connexion sur Adobe ID, SSO ou ID Learning Manager. Alignez la méthode sélectionnée sur la politique de sécurité de votre organisation.

L’Adobe recommande d’utiliser l’authentification unique Federated ID/SAML 2.0 comme méthode de connexion pour tous les utilisateurs internes. Cela garantit que l’authentification est entièrement contrôlée par le fournisseur d’identité de votre organisation, permettant une application centralisée de l’authentification multifacteurs et une révocation immédiate du compte lors du départ de l’utilisateur.

Voir [Paramètres](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/settings) pour plus d&#39;informations.

## Valeurs par défaut sécurisées recommandées pour le provisionnement

Lorsqu’un compte ALM est configuré pour la première fois, l’Adobe recommande de vérifier les paramètres par défaut suivants avant d’accorder un accès opérationnel à un utilisateur administrateur :

| Paramètre | Valeurs par défaut sécurisées recommandées | Où configurer |
|------------------------------|------------------------------------------------------------------|-------------------------------------------------|
| Méthode de connexion — utilisateurs internes | Authentification unique (SSO)/Federated ID | ALM > Paramètres > Méthodes de connexion |
| Validation en deux étapes (2FA) | Appliqué (facultatif pour tout utilisateur) | Admin Console > Paramètres > Confidentialité et sécurité |
| Durée max de session | 8 heures ou par stratégie d’organisation | Admin Console > Paramètres > Paramètres avancés |
| Temps d’inactivité max. | Politique de 30 minutes ou par organisation | Admin Console > Paramètres > Paramètres avancés |
| Portée du rôle d’administrateur | Privilèges moindres ; utiliser des rôles d’administrateur personnalisés si possible | ALM > Utilisateurs > Rôles personnalisés |
| Expiration de l’utilisateur externe | Définition d’une date d’expiration pour chaque profil utilisateur externe | ALM > Utilisateurs > Externes |

### Liste de contrôle de configuration initiale pour les nouveaux administrateurs

Lors de la configuration d’un nouveau compte administrateur de niveau supérieur, effectuez les opérations suivantes avant d’accorder l’accès opérationnel :

* Confirmez que le type d’identité est Enterprise ID ou Federated ID, et non Adobe ID personnel.
* Appliquez 2FA au niveau du Admin Console (Paramètres > Paramètres d’authentification).
* Si ce n’est pas déjà fait, configurez l’authentification unique/le Federated ID.
* Définissez les options Durée max de session et Temps d’inactivité max. dans le Admin Console > Paramètres > Paramètres avancés.
* Limiter l’étendue du rôle d’administrateur : attribuez uniquement les autorisations nécessaires aux responsabilités de l’utilisateur.
* Vérifiez que le compte administrateur est lié à une adresse e-mail d’organisation contrôlée par votre équipe informatique.
* Documentez le compte dans le registre d’accès privilégié de votre organisation.

## Fonctionnement des comptes administratifs

### Tâches administratives quotidiennes

Les comptes administratifs sont utilisés pour effectuer des tâches opérationnelles quotidiennes, notamment :

* **Gestion du cycle de vie des utilisateurs** : création d&#39;utilisateurs, mise à jour de profils et modification des rôles.
* **Gestion du contenu d&#39;apprentissage** : gestion des cours, des programmes d&#39;apprentissage, des certifications et des catalogues.
* **Reporting et analyses** : génération et révision de rapports sur la progression des élèves et l’utilisation de la plateforme.
* **Intégrations et configuration système** : gestion des connecteurs, de l&#39;accès basé sur l&#39;API et des paramètres au niveau du système.

Les administrateurs doivent suivre les politiques de contrôle d’accès interne et de gestion des modifications de leur organisation lorsqu’ils effectuent des actions administratives.

Consultez la [Foire aux questions pour les administrateurs Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/frequently-asked-questions-for-administrators)


### Hiérarchie des rôles et délégation

Adobe Admin Console utilise une structure d’administration hiérarchique. Les administrateurs système peuvent déléguer des responsabilités à des rôles dotés de privilèges inférieurs afin de réduire la surface d’attaque du compte administrateur de niveau supérieur :

* Administrateur de produit : gère l’accès à des produits Adobe spécifiques (par exemple, Adobe Learning Manager).
* Administrateur de profil de produit : gère l’appartenance des utilisateurs à des profils de produit spécifiques.
* Administrateur du groupe d’utilisateurs : gère l’appartenance au groupe d’utilisateurs.
* Administrateur personnalisé ALM : administrateur étendu dans ALM avec des autorisations configurables par catalogue et groupe d’utilisateurs.

### Pratiques de gouvernance en cours

Les pratiques suivantes doivent être suivies par les organisations gérant des comptes d’administrateur ALM de manière continue :

* **Examen périodique des accès** : auditez régulièrement la liste des administrateurs système en Admin Console (Utilisateurs > Administrateurs) et des administrateurs ALM (Utilisateurs > Internes) pour vous assurer que seul le personnel actuellement autorisé assume ces rôles.
* **Surveillance du journal d&#39;audit** : le journal d&#39;audit du Admin Console enregistre toutes les modifications apportées par les administrateurs. Les administrateurs système bénéficient d’une visibilité totale. Vérifiez régulièrement le journal pour détecter toute modification non autorisée.
* **Accès permanent minimum** : évitez d’utiliser des comptes d’administrateur de niveau supérieur pour les tâches de routine. Réservez l’accès administrateur complet aux tâches qui l’exigent spécifiquement.
* **Sécurité de la session** : configurez la durée maximale de la session et le temps d&#39;inactivité maximal dans le Admin Console > Paramètres > Paramètres avancés pour limiter l&#39;exposition des sessions sans assistance.

Voir [Présentation du portail Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html) pour plus d&#39;informations.

### Gestion des comptes utilisateur sous contrôle administrateur

Les administrateurs ALM gèrent les comptes utilisateur internes et externes. Les opérations liées à la sûreté comprennent :

* Suppression automatique des utilisateurs : dans Paramètres, les administrateurs peuvent configurer les utilisateurs internes inactifs pour qu’ils soient automatiquement supprimés après un nombre spécifié de jours, réduisant ainsi le risque de compte inactif.
* Expiration pour les utilisateurs externes : les administrateurs définissent une date d’expiration lors de la création de profils d’utilisateurs externes. Les comptes expirés sont automatiquement déplacés vers un état inactif.
* Suppression d’utilisateurs : les administrateurs peuvent supprimer manuellement des utilisateurs via Utilisateurs > Interne > Actions > Supprimer un utilisateur.
* Purge des utilisateurs : après la suppression, les administrateurs peuvent purger définitivement les enregistrements des utilisateurs pour se conformer aux politiques de conservation des données et empêcher tout accès non autorisé aux données utilisateur obsolètes.

Pour plus d’informations, voir les sections suivantes :

* [Ajouter un utilisateur et des groupes d’utilisateurs](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups)
* [Purger les utilisateurs](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/purge-users)

## Déclassement des comptes administratifs

L’accès administratif doit être supprimé lorsqu’il n’est plus nécessaire. Les comptes administratifs de déclassement peuvent comprendre :

* Révocation des rôles administratifs des utilisateurs.
* Réduction des privilèges lorsque l’accès administratif complet n’est plus nécessaire.
* Suppression d’utilisateurs du système, le cas échéant.

Un examen régulier et la suppression des accès administratifs superflus permettent de conserver un accès moins privilégié.

### Suppression des droits d’administrateur système (Admin Console)

Lorsqu’un administrateur système quitte l’organisation ou change de rôle, les privilèges doivent être révoqués rapidement :

1. Connectez-vous à Adobe Admin Console en tant qu’administrateur système.
2. Accédez à Utilisateurs > Administrateurs.
3. Sélectionnez l’administrateur à supprimer.
4. Cliquez sur l’icône Plus d’options (...) > Modifier l’administrateur, puis supprimez le rôle Administrateur système. OU sélectionnez Supprimer l’utilisateur pour supprimer entièrement l’utilisateur de l’organisation.
5. Si l’administrateur avait d’autres rôles (Administrateur de produit, Administrateur de support, etc.), révoquez-les également.

>[!IMPORTANT]
>
>Si l’administrateur sortant est le titulaire du contrat de l’organisation, le rôle de titulaire du contrat doit être transféré à une autre personne avant de pouvoir le supprimer. Contactez l’assistance de l’Adobe si nécessaire.

Pour plus d’informations, voir les sections suivantes :

* [Création, mise à jour ou suppression de comptes utilisateur dans le Admin Console](https://helpx.adobe.com/enterprise/using/manage-users-individually.html)
* [Comment quitter le compte appartenant à votre organisation](https://helpx.adobe.com/enterprise/using/leave-organization.html)

### Supprimer le rôle d’administrateur ALM

Pour révoquer l’accès administrateur ALM sans supprimer le compte de l’utilisateur (par exemple, lorsque la personne reste un élève) :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Accédez à Utilisateurs > Interne.
3. Recherchez et sélectionnez l’utilisateur.
4. Sélectionnez Actions > Supprimer le rôle > Supprimer l’administrateur.

L’utilisateur revient au rôle Élève. Leur historique d’apprentissage et leurs inscriptions aux cours sont conservés.

Voir [Ajouter un utilisateur et des groupes d&#39;utilisateurs](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) pour plus d&#39;informations.

### Suppression et purge d’utilisateurs

Lorsqu’un utilisateur quitte entièrement l’organisation et que son compte doit être supprimé de la plateforme :

* Supprimez l’utilisateur : Utilisateurs > Interne > sélectionnez un utilisateur > Actions > Supprimer l’utilisateur. Cela désactive le compte et supprime l’accès actif.
* Purger l’utilisateur : après la suppression, accédez à Utilisateurs > Nettoyage de l’utilisateur, sélectionnez le mois de la suppression, sélectionnez l’utilisateur et choisissez Actions > Purger l’utilisateur. La purge supprime définitivement tous les enregistrements d’utilisateur.

Voir [Purger les utilisateurs](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/purge-users) pour plus d&#39;informations.


## Sécurité et responsabilité partagée

Adobe Learning Manager fonctionne selon un modèle de responsabilité partagée :

* L’Adobe est responsable de la sécurisation de la plate-forme et de l’infrastructure ALM sous-jacentes.
* Les clients sont responsables de la gestion des accès administratifs, des attributions de rôles et des activités du cycle de vie des utilisateurs dans leur compte ALM.

Des informations supplémentaires sur les pratiques de sécurité de Adobe Learning Manager sont disponibles dans [Présentation de la sécurité de Adobe Learning Manager (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Maintenance des documents

Ce document peut être mis à jour régulièrement pour refléter les modifications apportées aux fonctionnalités de Adobe Learning Manager ou les bonnes pratiques administratives. La version et la date de la dernière mise à jour sont conservées dans les métadonnées du document et dans le package d’autorisation FedRAMP. Les clients doivent consulter la version accessible au public de Adobe Experience League pour s’assurer qu’ils utilisent les conseils les plus récents.

## Couverture renforcée des capacités de sécurité

### SCG-ENH-CMP

Adobe tient à jour des processus documentés d’inventaire, de propriété et de gestion du cycle de vie des composants pour assurer une configuration et une conformité contrôlées entre les composants système.

### SCG-ENH-API

L’Adobe applique des contrôles de sécurité d’API standardisés, notamment l’authentification, l’autorisation et la surveillance, avec une gouvernance documentée et des garanties de plate-forme.

### SCG-ENH-MRG

Adobe applique des processus de gestion des modifications et des fusions, y compris des contrôles de révision et d&#39;approbation, pour préserver l&#39;intégrité du système et réduire les risques liés au déploiement.

### SCG-ENH-VRH

L’Adobe suit un processus défini de gestion et de correction des vulnérabilités couvrant l’identification, la hiérarchisation, le suivi et la résolution en temps opportun.
