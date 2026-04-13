---
description: En savoir plus sur la méthode de connexion OIDC
jcr-language: en_us
title: Connexion à Adobe Learning Manager avec OpenID Connect
source-git-commit: 7c430e3fbb2716455310f2130d73af10ce2e56c7
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---


# Connexion à Adobe Learning Manager avec OpenID Connect (OIDC)

Découvrez comment fonctionne la connexion OpenID Connect dans Adobe Learning Manager pour les élèves, les auteurs et les administrateurs. Cet article traite de l&#39;expérience et non de la mise en œuvre.

## Comprendre la connexion à OpenID Connect

OpenID Connect (OIDC) est une méthode de connexion courante basée sur des normes web. De nombreuses organisations utilisent un fournisseur d’identité (par exemple, Okta, Google Workspace ou Microsoft Entra ID) pour les employés et les partenaires.

Lorsque votre organisation active OIDC pour Adobe Learning Manager :

* Vous vous connectez à l’aide de la page de connexion habituelle de votre organisation, et non d’un mot de passe s’appliquant uniquement à Adobe Learning Manager, sauf si votre organisation en décide autrement.
* Après votre authentification, Adobe Learning Manager reçoit les informations autorisées par votre organisation (telles que votre adresse e-mail et les attributs de votre profil) et vous propose l’expérience appropriée : élève, auteur, administrateur ou autres rôles pris en charge par votre compte.

OIDC est une alternative aux autres options de connexion que votre compte peut offrir, telles qu’Adobe ID ou l’authentification unique (SSO) basée sur SAML. Votre administrateur décide des méthodes disponibles.

## Pourquoi les organisations choisissent OpenID Connect

Les organisations choisissent souvent OIDC pour les raisons suivantes :

* Les utilisateurs bénéficient de la même expérience d’identité d’entreprise ou en ligne qu’ils utilisent pour d’autres applications.
* Les politiques de mot de passe, l’authentification multifacteur et le cycle de vie du compte sont gérés dans le fournisseur d’identité, de manière cohérente avec les autres applications d’entreprise.
* OIDC suit des modèles similaires à d’autres flux de connexion modernes du point de vue de l’utilisateur et de l’informatique, sans l’exchange de document plus lourd associé à certaines configurations SAML uniquement.

Votre expérience est toujours la même : accédez à Learning Manager, connectez-vous là où votre organisation vous l’a indiqué et accédez à l’application.

## Ce que vous voyez lorsque vous vous connectez

### Ouvrir Adobe Learning Manager

Vous pouvez utiliser :

* URL Adobe Learning Manager principale de votre environnement
* Domaine personnalisé configuré par votre organisation, le cas échéant
* Lien d’une page d’e-mail, d’invitation ou d’auto-inscription
* Un signet ou un lien profond vers un cours, une page de catalogue ou une ressource spécifique

Si votre compte utilise OIDC, le démarrage de la connexion redirige généralement votre navigateur vers le fournisseur d’identité de votre organisation.

### Se connecter avec votre organisation

Sur la page de votre fournisseur d’identité, saisissez vos informations d’identification et effectuez toutes les étapes supplémentaires requises par votre organisation, telles que l’authentification multifacteur. Cette étape se produit en dehors du formulaire de connexion de Adobe Learning Manager lorsque l’OIDC est la méthode utilisée. De votre point de vue, cela revient à vous connecter à votre compte d’entreprise ou d’établissement scolaire. Vous ne verrez peut-être pas de termes techniques tels que *OIDC* ou *OAuth* au cours de cette étape.

### Revenir à Adobe Learning Manager

Une fois connecté, votre navigateur vous renvoie à Adobe Learning Manager. Le produit alors:

* Vous reconnaît en utilisant l’adresse e-mail et les informations de profil partagées par votre fournisseur d’identité, en fonction des paramètres de votre organisation
* Applique vos autorisations dans Adobe Learning Manager (élève, auteur, administrateur, administrateur d’intégration, etc.)
* Ouvre l’application ou la zone appropriée (par exemple, l’expérience de l’élève comparée aux expériences de l’administrateur ou de l’auteur), conformément à la façon dont Adobe Learning Manager attribue des rôles à votre compte

Si un problème se produit (par exemple, votre compte n’est pas provisionné ou votre organisation bloque l’accès), une erreur peut s’afficher ou vous ne pouvez pas continuer. Contactez votre équipe informatique interne ou votre administrateur Adobe Learning Manager.

## Utiliser d’autres options de connexion avec OpenID Connect

Adobe Learning Manager peut prendre en charge plusieurs méthodes de connexion sur un compte (plusieurs options d’authentification unique). Par exemple :

* Certains utilisateurs se connectent avec Adobe ID
* D’autres utilisent SAML SSO
* D’autres utilisent OIDC

Les options qui s’affichent dépendent de la configuration de votre compte. L’activation d’OIDC pour votre organisation ne supprime pas par elle-même les autres méthodes, sauf si vos administrateurs modifient cette configuration.

## Fonctionnalités et scénarios pris en charge

Les comportements suivants sont pris en charge lorsque votre organisation utilise OIDC avec Adobe Learning Manager, conformément à la façon dont les autres méthodes de connexion d’entreprise sont censées fonctionner.

### Tableau 1. Prise en charge d’OIDC dans des scénarios courants

| Zone | Ce que cela signifie pour vous |
| --- | --- |
| Utilisateurs internes et externes | Les employés et les utilisateurs externes invités (par exemple, les partenaires) peuvent utiliser OIDC lorsque votre administrateur l’active, y compris les flux qui partent de liens d’auto-inscription lorsque votre compte est configuré à cet effet. |
| Premier accès | Si vous y êtes autorisé par la politique, votre première connexion OIDC réussie peut créer ou lier votre utilisateur dans Adobe Learning Manager conformément aux règles de votre organisation, similaires aux autres options d’authentification unique. |
| Profil et attributs | Les informations telles que l’adresse e-mail et d’autres attributs peuvent être mises à jour à partir de votre fournisseur d’identité au fil du temps, de sorte que votre profil Adobe Learning Manager reste aligné sur le répertoire de votre organisation, dans les limites configurées par votre administrateur. |
| Liens profonds | Les liens pointant vers une page ou une ressource spécifique dans Learning Manager (pas seulement la page d’accueil) sont pris en charge. Vous pouvez accéder au contenu prévu après la connexion lorsque la configuration de votre organisation le permet. |
| Chemin de retour | Après l’authentification, vous pouvez revenir à l’endroit que vous tentiez d’atteindre (par exemple, la même URL de cours ou de catalogue que celle à partir de laquelle vous avez commencé), plutôt que de toujours vous poser sur une page d’accueil générique. |
| Domaine personnalisé | Si votre société utilise un nom d’hôte personnalisé pour Adobe Learning Manager, la connexion OIDC est également prise en charge dans ce contexte. |
| Mobile | La connexion sur les téléphones et les tablettes via des navigateurs ou des expériences pris en charge est prise en charge. |
| Publish vers Adobe Learning Manager (Prime) | Les workflows qui impliquent la publication de contenu dans Learning Manager à partir d’outils connectés restent pris en charge lorsque votre compte utilise OIDC, conformément à votre configuration d’intégration. |
| Connexion basée sur l’identifiant | Lorsque votre compte repose sur des identifiants stables (au-delà de l’e-mail uniquement) pour les comptes correspondants, ces flux sont pris en charge pour OIDC en fonction de la configuration de votre administrateur. |

Si un workflow spécifique ne fonctionne pas, la cause peut en être les paramètres du fournisseur d’identité, l’approvisionnement du compte ou l’attribution de rôle Adobe Learning Manager. Votre administrateur peut vérifier.

## Fonctionnement des rôles après la connexion

Adobe Learning Manager détermine ce que vous pouvez faire à partir des rôles et des autorisations de votre compte, et non à partir du protocole OIDC lui-même. L’OIDC détermine uniquement qui vous êtes à la satisfaction de votre fournisseur d’identité et ce que votre organisation partage avec Adobe Learning Manager.

* Les élèves voient généralement les formations, les catalogues et les plans d’apprentissage.
* Les auteurs peuvent créer ou organiser du contenu.
* Les administrateurs gèrent les utilisateurs, la configuration et les rapports.

Si vous vous trouvez dans la mauvaise zone ou si vous ne disposez pas des droits d’accès requis, demandez à votre administrateur Adobe Learning Manager de vérifier votre profil et votre appartenance au groupe.

## Dépannage des problèmes courants

### Tableau 2. Résolution des problèmes de connexion OIDC

| Le problème | Éléments à essayer |
| --- | --- |
| Boucle de redirection ou page vierge | Effacez les cookies de l’URL de Learning Manager et de votre fournisseur d’identité, essayez un autre navigateur ou essayez une fenêtre privée. Si le problème persiste, contactez le service informatique. Les proxys d’entreprise ou les stratégies de session du fournisseur d’identité interfèrent parfois. |
| « Accès refusé » ou similaire après la connexion au fournisseur d’identité | Votre fournisseur d’identité vous a accepté, mais Adobe Learning Manager peut ne pas avoir d’utilisateur correspondant ou votre compte peut ne pas avoir de licence ou de rôle. Contactez votre administrateur Adobe Learning Manager. |
| Langue ou détails de profil incorrects | Le mappage d’attributs est contrôlé par votre organisation. Demandez à votre administrateur si les attributs de répertoire doivent piloter les champs de paramètres régionaux ou de profil. |
| Le lien profond a ouvert la page d’accueil au lieu de la ressource | Le comportement des chemins de retour et des liens profonds peut dépendre de la manière dont le lien a été partagé et de votre session. Relancez le lien après une connexion complète ou demandez à votre administrateur si le format du lien est pris en charge pour les utilisateurs externes. |

## Ce que les administrateurs doivent savoir

Si vous configurez Adobe Learning Manager pour votre organisation, l’OIDC est configuré avec l’enregistrement d’application de votre fournisseur d’identité : les identifiants client, les points de terminaison pour l’autorisation, les jetons, les informations utilisateur et l’URL de redirection que Adobe Learning Manager utilise pour terminer la connexion. Ces valeurs proviennent de la documentation de votre fournisseur d’identité. Les paramètres doivent correspondre entre votre fournisseur d’identité et Learning Manager afin que les utilisateurs puissent voir une redirection et un retour fluides.

Les utilisateurs finaux n’ont pas besoin de gérer ces valeurs. Ils ont uniquement besoin de l’URL (ou du domaine personnalisé) Learning Manager correcte et, le cas échéant, des liens d’invitation ou d’auto-inscription de votre équipe.

## Résumé

* OIDC permet aux utilisateurs de se connecter à Adobe Learning Manager via le fournisseur d’identité standard de leur organisation, avec un flux de redirection et de retour familier.
* Une fois connecté, Adobe Learning Manager utilise l’adresse e-mail et les attributs partagés pour identifier l’utilisateur et appliquer des rôles (élève, auteur, administrateur, etc.).
* L’auto-inscription, plusieurs options SSO, les mises à jour d’attributs, le provisionnement pour la première fois des utilisateurs, les liens profonds, le chemin de retour, les domaines personnalisés, les applications mobiles, Publish vers Adobe Learning Manager et la correspondance basée sur les identifiants sont pris en charge en fonction de la configuration de votre compte.
* D’autres méthodes de connexion (telles qu’Adobe ID ou SAML) restent disponibles lorsque vos administrateurs les maintiennent activées.
