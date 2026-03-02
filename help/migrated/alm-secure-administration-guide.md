---
title: Adobe Learning Manager - Guide d’administration sécurisé
description: Ce guide décrit les paramètres de sécurité, les rôles et les meilleures pratiques pour gérer la sécurité administrative et le contrôle d’accès dans Adobe Learning Manager afin de garantir la conformité et la sécurité.
jcr-language: en-us
source-git-commit: 76a231b5d178a43a2e217d442481e6fd77f12390
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---


# Paramètres de sécurité administrative et implications en matière de sécurité

## Rôles administratifs ayant un impact sur la sécurité

Adobe Learning Manager utilise un modèle de contrôle d’accès basé sur les rôles (RBAC). Le tableau suivant mappe les niveaux de compte FedRAMP aux rôles ALM référencés dans ce document :

| Terme FedRAMP | Rôle ALM | Pertinence en matière de sécurité |
|-------------|---------|------------------|
| Compte d’administration de niveau supérieur | L’administrateur | Contrôle complet au niveau du compte. Accès exclusif à tous les paramètres de sécurité décrits dans ce document. C&#39;est le rôle auquel il est fait référence dans le présent guide lorsque l&#39;expression « compte administratif de niveau supérieur » est utilisée. |
| Compte privilégié (étendue) | Administrateur personnalisé | L&#39;accès administratif délégué s&#39;étendait à des fonctions, des groupes d&#39;utilisateurs ou des catalogues spécifiques. Impossible d’accéder aux paramètres de sécurité au niveau du compte, sauf autorisation explicite. |
| Compte privilégié (intégration) | Administrateur d’intégration | Gère les intégrations, les enregistrements d’API et les configurations de connecteur. Droits élevés étendus à la gestion de l’intégration. Impossible de modifier les autres paramètres de sécurité au niveau du compte. |

>[!NOTE]
>
>Seuls les utilisateurs auxquels ces rôles sont explicitement attribués peuvent modifier les paramètres administratifs ou de sécurité. Les paramètres décrits aux sections 3 à 7 sont accessibles exclusivement au rôle Administrateur, sauf indication contraire.

## Paramètres de connexion et d’authentification

Les paramètres de connexion et d’authentification contrôlent la façon dont tous les utilisateurs, y compris les administrateurs, accèdent à la plateforme ALM. Ces paramètres sont configurés exclusivement par le rôle Administrateur et ont un impact direct et significatif sur la sécurité de l’ensemble du compte.

### Configuration de la méthode de connexion

**Emplacement :** administrateur ALM > Paramètres > Méthodes de connexion

L’administrateur contrôle la méthode d’authentification utilisée pour tous les utilisateurs internes et externes. Les options sont les suivantes :

- **Adobe ID :** les utilisateurs s&#39;authentifient via leur compte d&#39;Adobe personnel. Géré par l’Adobe, pas par l’organisation.
- **Authentification unique (SSO) via SAML 2.0:** les utilisateurs s’authentifient via le fournisseur d’identité (IdP) de l’organisation. L’organisation contrôle entièrement l’authentification, l’authentification multifacteurs et la stratégie de session.
- **ID Learning Manager :** disponible pour les utilisateurs externes uniquement. Les utilisateurs créent un nom d’utilisateur et un mot de passe spécifiques à la plateforme.
- **Plusieurs configurations SSO :** jusqu’à 20 configurations SSO peuvent être ajoutées pour prendre en charge différents groupes d’utilisateurs, emplacements ou divisions organisationnelles

| Méthode de connexion | Implication en matière de sécurité | Recommandation |
|-------------|---------------------|----------------|
| **Adobe ID** | L’organisation n’a aucun contrôle sur la stratégie de mot de passe, l’AMF ou la récupération de compte. Un compte personnel d’Adobe compromis donne accès à la plateforme ALM. | **NON RECOMMANDÉ** pour les utilisateurs administratifs ou internes. À utiliser uniquement lorsque l’authentification unique n’est pas disponible. |
| **SSO (SAML 2.0 / Federated ID)** | L’authentification est entièrement contrôlée par le fournisseur d’identité de l’organisation. L’authentification multifacteur, les expirations de session et les politiques d’accès conditionnel sont appliquées au niveau de l’IdP. Révocation immédiate au départ de l’utilisateur. | **RECOMMANDÉ** pour tous les utilisateurs et administrateurs internes. Fournit le plus haut niveau de contrôle organisationnel. |
| **ID Learning Manager** | Les utilisateurs gèrent eux-mêmes les mots de passe en dehors de l’infrastructure d’identité de l’entreprise. Impossible d’appliquer l’authentification multifacteur via ALM. La complexité du mot de passe dépend du comportement de l’utilisateur. | Acceptable pour les utilisateurs externes uniquement. Ne convient pas aux employés ni aux administrateurs. |

>[!CAUTION]
>
>Si la méthode de connexion est définie sur Adobe ID pour les utilisateurs internes, l’organisation ne peut plus appliquer l’authentification à plusieurs facteurs, contrôler la complexité des mots de passe ou révoquer immédiatement l’accès lorsqu’un utilisateur quitte l’application. Cela augmente considérablement le risque d’accès non autorisé.

Voir [Rôles personnalisés](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) pour plus d&#39;informations.

### Authentification multifacteur (MFA)

**Emplacement :** Adobe Admin Console > Paramètres > Confidentialité et sécurité > Paramètres d&#39;authentification

L&#39;application MFA pour les utilisateurs d&#39;**Adobe ID** et du **Enterprise ID** est configurée par l&#39;**administrateur système** dans Adobe Admin Console, et non dans l&#39;application ALM elle-même.  Pour les utilisateurs de **Federated ID/SSO**, l’authentification multifacteur est appliquée au fournisseur d’identité de l’organisation.

- **2FA imposé :** les utilisateurs ne peuvent pas désactiver la validation en deux étapes. Offre une protection efficace contre le vol d’informations d’identification et le phishing.
- **2FA facultatif :** les utilisateurs peuvent choisir d&#39;activer ou non la validation en deux étapes. Une posture de sécurité nettement plus faible.
- **MFA non configuré :** seuls les mots de passe protègent l&#39;accès. Risque élevé, en particulier pour les comptes administratifs.

>[!IMPORTANT]
>
>Les comptes administratifs sans AMF imposée présentent un risque beaucoup plus élevé d’accès non autorisé. Une identification d’administrateur compromise sans MFA accorde un contrôle total sur le compte, y compris la possibilité de modifier tous les paramètres de sécurité.

### Durée de la session et délai d&#39;inactivité

**Emplacement :** Adobe Admin Console > Paramètres > Confidentialité et sécurité > Paramètres avancés

L&#39;**administrateur système** configure la durée de vie maximale de la session active et le délai d&#39;expiration de la session inactive pour l&#39;organisation. Ces paramètres s’appliquent à tous les utilisateurs, y compris les administrateurs.

- **Durée max de la session :** force la réauthentification après une période définie, quelle que soit l&#39;activité. Limite la fenêtre d’opportunité si une session est compromise.
- **Temps d&#39;inactivité max. :** met fin aux sessions qui ont été inactives pendant une période définie. Protège contre les sessions authentifiées sans assistance sur les appareils partagés ou déverrouillés.

## Attribution de rôles et paramètres d’étendue des privilèges

Les paramètres d’attribution de rôle et de portée de privilège déterminent qui a un accès administratif dans ALM et ce qu’il peut faire. Il s’agit des paramètres de sécurité les plus performants de la plateforme. Seul le rôle Administrateur peut créer, attribuer, modifier ou révoquer des rôles administratifs.

### Attribution de rôle administratif

**Emplacement :** Administrateur ALM > Utilisateurs > Interne > Actions > Attribuer un rôle/Supprimer un rôle

L&#39;**administrateur** peut accorder ou révoquer les rôles suivants :

- **Administrateur :** accès complet au niveau du compte
- **Auteur :** accès à la création de contenu
- **Administrateur personnalisé :** accès administratif limité (voir Section 4.2)
- **Administrateur d&#39;intégration :** intégration et accès à l&#39;API (voir Section 7)

| Paramètre/Action | Implication en matière de sécurité | Pratique recommandée |
|---|---|---|
| **Octroi du rôle d&#39;administrateur** | Contrôle total du compte. Un utilisateur disposant de ce rôle peut modifier tous les paramètres de ce document, y compris reconfigurer l’authentification et révoquer l’accès d’autres administrateurs. | Attribuez uniquement à un nombre minimum d’utilisateurs avec un besoin professionnel vérifié. Tenir à jour une liste documentée de tous les détenteurs de rôle d’administrateur. |
| **Échec de la révocation des rôles au départ** | Les utilisateurs quittés conservent l&#39;accès aux fonctions administratives. Risque d’accès non autorisé, d’exfiltration de données ou de sabotage. | Supprimez immédiatement les rôles lorsque les responsabilités administratives ou professionnelles d’un utilisateur changent. Effectuez des examens d’accès périodiques. |
| **Attribution excessive de rôles généraux** | Un accès administratif étendu augmente l’impact potentiel d’un compte compromis et réduit la responsabilité des actions administratives. | Appliquer le principe du moindre privilège. Privilégiez les rôles étendus (par exemple, Administrateur personnalisé) lorsque cela est possible. |

### Configuration personnalisée du rôle d’administration

**Emplacement :** administrateur ALM > Utilisateurs > Rôles personnalisés > Créer un rôle

Appliquez le principe du **privilège minimum**. Utilisez les rôles **Administrateur personnalisé** pour déléguer des fonctions spécifiques (voir Section 4.2).

L&#39;**administrateur** peut créer des rôles personnalisés qui accordent un sous-ensemble défini d&#39;autorisations administratives. Les rôles personnalisés peuvent être définis en fonction de groupes d&#39;utilisateurs, de catalogues ou d&#39;ensembles de fonctionnalités spécifiques, ce qui limite la portée des accès administratifs délégués.

**Les catégories d&#39;autorisations disponibles sont les suivantes :**

- **Droits de compte :** accès aux configurations à l&#39;échelle du système telles que les annonces, la ludification, les compétences et la gestion des utilisateurs.
- **Droits de fonctionnalité (principal) :** accès aux catalogues, rapports et balises.
- **Droits de fonctionnalité (objets d&#39;apprentissage) :** accès aux cours, certifications, parcours d&#39;apprentissage et assistances à la tâche.
- **Portée :** limitez le rôle à des groupes d&#39;utilisateurs et/ou des catalogues spécifiques.

| Décision de configuration | Implication en matière de sécurité | Pratique recommandée |
|---|---|---|
| **Création d&#39;un rôle personnalisé trop large** | Un rôle personnalisé avec des privilèges excessifs offre peu d’avantages en termes de sécurité par rapport au rôle d’administrateur complet et augmente le rayon d’impact d’un compte compromis. | Définissez l’étendue des rôles personnalisés sur le jeu minimal d’autorisations nécessaires pour la fonction spécifique. Préférez les rôles de portée catalogue et de portée utilisateur. |
| **Octroi de l&#39;accès aux paramètres à un administrateur personnalisé** | Les administrateurs personnalisés avec un accès aux Paramètres peuvent modifier les méthodes de connexion, les paramètres de notification et d’autres configurations au niveau du compte. | Accordez uniquement aux paramètres l’accès aux rôles personnalisés lorsqu’ils sont explicitement requis. Contrôlez régulièrement les rôles personnalisés qui disposent de ce privilège. |
| **Impossible d&#39;auditer les attributions de rôles personnalisées** | Les rôles personnalisés non documentés ou non révisés peuvent s’accumuler au fil du temps, entraînant un détournement de privilèges. | Téléchargez régulièrement le rapport de rôle personnalisé (**Utilisateurs > Rôles personnalisés > Télécharger**) et passez en revue toutes les attributions de rôle personnalisé actives. |

## Configuration des utilisateurs et paramètres de gestion des accès

Les paramètres de provisionnement des utilisateurs contrôlent la façon dont les utilisateurs sont ajoutés à la plateforme, la durée pendant laquelle ils restent actifs et le moment où leurs données sont supprimées. Ces paramètres sont configurés exclusivement par le rôle Administrateur et ont des implications directes en termes de sécurité pour l’exposition des données et le contrôle d’accès.

| Paramètre | Emplacement | Implication en matière de sécurité | Valeur par défaut recommandée |
|---|---|---|---|
| **Suppression automatique des utilisateurs inactifs** | Administrateur ALM > Paramètres > Général | Sans suppression automatique, les comptes inactifs s’accumulent. Les comptes dormants sont souvent la cible d’accès non autorisé, car ils peuvent ne pas être surveillés. | Activer. Définissez une période de rétention conforme à la politique de l’entreprise (par exemple, 90 jours d’inactivité). |
| **Expiration du profil utilisateur externe** | Administrateur ALM > Utilisateurs > Externe > Ajouter un profil | Les profils d’utilisateurs externes sans date d’expiration restent accessibles indéfiniment. Les partenaires ou les sous-traitants qui n’ont plus besoin d’accès conservent un point d’entrée actif. | Définissez une date d’expiration pour chaque profil utilisateur externe au moment de la création. |
| **Commandes de lien d&#39;auto-inscription** | Administrateur ALM > Utilisateurs > Interne > Ajouter > Auto-inscription | Un lien d’auto-inscription permet à tout utilisateur disposant de l’URL de créer un compte d’élève. S’il n’est pas géré, cela peut entraîner l’accès à la plate-forme d’utilisateurs non autorisés ou inattendus. | Générez des liens d’auto-inscription uniquement si nécessaire. Désactivez ou révoquez rapidement les liens inutilisés. |
| **Pause/reprise du profil externe** | Administrateur ALM > Utilisateurs > Externe > Actions > Pause | Suspendre un profil externe empêche les nouveaux utilisateurs de s’enregistrer, mais n’affecte pas ceux déjà enregistrés. Si vous ne parvenez pas à suspendre les profils externes inactifs, des enregistrements inattendus risquent de se produire. | Suspendre les profils externes lorsque l’enregistrement n’est plus nécessaire. Supprimez les profils qui sont définitivement inactifs. |
| **Suppression et purge des utilisateurs** | Administrateur ALM > Utilisateurs > Interne > Actions > Supprimer / Nettoyage utilisateur > Purger | Les utilisateurs supprimés sont désactivés, mais leurs données sont conservées. La purge supprime définitivement toutes les données utilisateur. Si les utilisateurs supprimés ne sont pas purgés, ils peuvent conserver leurs dossiers d’apprentissage sensibles et leurs informations personnelles au-delà de la période de rétention requise. | Videz les enregistrements utilisateur conformément aux politiques de conservation et de confidentialité des données de l’entreprise. La purge est irréversible. |

>[!IMPORTANT]
>
>La purge est permanente et irréversible. Tous les enregistrements d&#39;apprentissage, les données d&#39;inscription et les informations utilisateur sont supprimés. Si un utilisateur purgé est référencé dans des configurations de connecteur, ces connecteurs seront désactivés. Confirmez soigneusement la sélection avant d’exécuter une purge.

## Paramètres de création de rapports et d’accès aux données

Les paramètres de création de rapports et d’accès aux données déterminent quels utilisateurs peuvent afficher, générer et exporter les données de la plateforme. Une mauvaise configuration de ces paramètres peut entraîner la divulgation d’informations sensibles d’ordre personnel, organisationnel ou liées à la conformité.

| Paramètre | Emplacement | Implication en matière de sécurité | Valeur par défaut recommandée |
|---|---|---|---|
| **Octroi d&#39;accès aux rapports pour les rôles personnalisés** | Administrateur ALM > Utilisateurs > Rôles personnalisés > Privilèges de fonctionnalité > Rapports | Les rapports peuvent contenir des informations d’identification personnelle (PII), les données d’achèvement du cours, les scores d’évaluation et la progression de l’élève. L’accès aux fonctionnalités de création de rapports doit être limité aux utilisateurs ayant un besoin professionnel vérifié. | Accordez l’accès aux rapports uniquement aux rôles ayant un besoin spécifique et documenté. Utilisez l’accès en lecture seule lorsque l’accès en écriture n’est pas requis. |
| **Étendue du rapport Contrôle total ou Lecture seule** | Administrateur ALM > Utilisateurs > Rôles personnalisés > Rapport récapitulatif du compte | Le rapport Contrôle total sur le résumé du compte accorde la visibilité d’administrateur personnalisée à tous les groupes d’utilisateurs et catalogues, quelle que soit la portée de leur rôle. Cela peut exposer des données en dehors de la portée prévue d’un rôle d’administrateur étendu. | Accordez le contrôle total sur le rapport récapitulatif du compte uniquement aux rôles qui nécessitent véritablement une visibilité sur les rapports à l’échelle de l’organisation. |
| **Accès aux rapports xAPI et par e-mail** | Administrateur ALM > Utilisateurs > Rôles personnalisés | Les rapports xAPI et les rapports par e-mail sont disponibles uniquement pour le rôle Administrateur complet. Ces rapports peuvent contenir des données comportementales et de communication détaillées. L’accès est restreint par la conception. | N’essayez pas de déléguer l’accès aux rapports xAPI ou e-mail via des rôles personnalisés. Il s’agit d’un programme conçu pour être géré uniquement par un administrateur. |
| **Données utilisateur exportées** | Administrateur ALM > Utilisateurs > Interne > Exporter les données utilisateur | La fonction Exporter les données utilisateur génère un fichier téléchargeable contenant tous les enregistrements utilisateur internes. Ces données doivent être traitées conformément aux politiques de sécurité et de confidentialité de l’entreprise. | Limiter la capacité d&#39;exportation au personnel autorisé. Traiter les données exportées comme sensibles. Ne pas stocker ou transmettre en dehors des systèmes approuvés. |

## Paramètres d’intégration et d’accès API

Les paramètres d’intégration et d’accès API contrôlent la façon dont les systèmes externes se connectent à Adobe Learning Manager. Ces paramètres étendent l’accès au-delà de l’interface utilisateur ALM et, s’ils sont mal configurés, peuvent exposer les données et les fonctionnalités de la plate-forme à des systèmes non autorisés.  Les paramètres d’intégration sont gérés par le rôle Administrateur d’intégration. Le rôle d’administrateur complet conserve la possibilité de réviser, d’approuver et de révoquer les applications enregistrées.

| Paramètre | Emplacement | Implication en matière de sécurité | Valeur par défaut recommandée |
|---|---|---|---|
| **Inscription d&#39;application API** | Administrateur de l’intégration > Applications > S’inscrire | L’enregistrement d’une application crée des informations d’identification OAuth 2.0 (ID client et secret) qui peuvent être utilisées pour accéder aux données et aux fonctions ALM par programmation. Les portées OAuth trop larges (par exemple, lecture/écriture du rôle Administrateur) accordent un accès complet à l’API d’administration. | Octroyez les portées OAuth minimales requises. Révisez et révoquez régulièrement les inscriptions d’applications inutilisées ou héritées. Traitez les informations d’identification du client comme des secrets sensibles. |
| **Portée de l’application OAuth** | Administrateur de l’intégration > Applications > S’inscrire > Domaines | Les portées OAuth disponibles vont de l’accès en lecture à l’élève à l’accès en lecture/écriture à l’administrateur. La lecture/écriture du rôle d’administrateur permet à une application de modifier toutes les données qu’un administrateur peut modifier, y compris les rôles d’utilisateur et les paramètres de sécurité. | Utilisez la portée OAuth la plus restrictive qui répond aux exigences de l’intégration. N’accordez jamais l’accès en lecture/écriture au rôle Administrateur sauf en cas de nécessité absolue. |
| **Configuration du connecteur (FTP, Salesforce, HRIS, etc.)** | Administrateur de l’intégration > Connecteurs | Les connecteurs permettent l’importation et l’exportation automatisées des données utilisateur, des compétences et des achèvements de cours. Les connecteurs mal configurés peuvent importer des données utilisateur incorrectes, attribuer des rôles inattendus ou exporter des données sensibles vers des destinations non autorisées. | Passez régulièrement en revue toutes les configurations de connecteur actives. S’assurer que les sources de données et les destinations sont autorisées. Désactivez les connecteurs qui ne sont plus utilisés. |
| **Configuration du webhook** | Administrateur de l’intégration > Webhooks | Les webhooks envoient des données d’événement ALM en temps réel (inscriptions, achèvements, modifications de l’utilisateur) à une URL externe spécifiée. Un point d’entrée webhook mal configuré ou compromis peut entraîner l’exfiltration de données ou l’exposition d’événements d’élève sensibles. | Enregistrez uniquement les URL de webhook vérifiées et approuvées par l’organisation. Passez régulièrement en revue les configurations de webhook actives. Supprimez immédiatement les webhooks inactifs ou non reconnus. |
| **Configuration de l&#39;intégration LTI** | Administrateur d’intégration > Intégrations LTI | L’intégration LTI permet à ALM d’agir en tant que fournisseur ou consommateur LTI, permettant ainsi aux plateformes LMS externes d’accéder aux cours ALM. Une fois activé, LTI ne peut pas être désactivé. Les informations d’identification LTI affichées peuvent autoriser un accès non autorisé au contenu du cours. | Activez LTI uniquement lorsqu’une exigence d’intégration vérifiée existe. Traitez les informations d’identification LTI comme sensibles. Partagez les informations d’identification uniquement avec les administrateurs LMS autorisés. |

## Responsabilités de configuration administrative et responsabilité partagée

Les paramètres administratifs de Adobe Learning Manager sont configurables par les clients et font partie des contrôles de sécurité gérés par le client dans le cadre du modèle de responsabilité partagée d’Adobe.

| Responsabilités de l&#39;Adobe | Responsabilités du client |
|---|---|
| Fonctionnement sécurisé de la plateforme ALM et de l’infrastructure sous-jacente. | Configuration de tous les rôles et autorisations administratifs. |
| Application du modèle de contrôle d&#39;accès basé sur les rôles (RBAC). | Sélection et application des méthodes de connexion et de l’authentification multifacteurs appropriées. |

Des informations supplémentaires sur les pratiques de sécurité de Adobe Learning Manager sont disponibles dans :

**Référence :** [Présentation de la sécurité Adobe Learning Manager (mot de PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Maintenance des documents

Ce document peut être mis à jour régulièrement pour refléter les modifications apportées aux fonctionnalités de Adobe Learning Manager ou aux consignes de sécurité. La version et la date de la dernière mise à jour sont conservées dans les métadonnées du document et dans le package d’autorisation FedRAMP. Les clients doivent consulter la version accessible au public de Adobe Experience League pour s’assurer qu’ils utilisent les conseils les plus récents.

