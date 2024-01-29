---
description: Adobe Learning Manager prend en charge plusieurs méthodes de connexion via plusieurs configurations SSO pour les utilisateurs internes et externes.
title: Plusieurs connexions SSO
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 0%

---


# Plusieurs connexions SSO {#multiple-sso-logins}

Un administrateur peut configurer plusieurs méthodes de connexion pour les utilisateurs internes et externes. Adobe Learning Manager prend en charge plusieurs connexions SSO qui aideront les administrateurs à configurer la méthode de connexion en fonction de leurs besoins et cas d’utilisation.

L’objectif est de permettre aux administrateurs de configurer différentes SSO pour différents groupes d’utilisateurs en fonction de leur emplacement, de leur organisation, etc.

Jusqu’à 20 configurations SSO peuvent être ajoutées à un compte. Ils peuvent être utilisés pour configurer l’authentification unique pour les utilisateurs internes et externes.

>[!NOTE]
>
>Lors de l’activation de l’authentification unique multiple, vous pouvez choisir des valeurs ou des groupes d’utilisateurs dans le profil d’auto-inscription. Lors du choix d’une valeur, un groupe d’utilisateurs sans utilisateur est créé. Un tel groupe d’utilisateurs n’a aucun utilisateur. Lorsque le fichier CSV suivant sera importé, ce groupe d’utilisateurs sera supprimé.

## Activer plusieurs connexions SSO

Pour activer plusieurs connexions SSO, sélectionnez **Paramètres** > **Méthodes de connexion**.

Sur la page de configuration, cochez la case « Activer l’authentification unique (SSO) multiple » pour les utilisateurs internes ou externes.

Lorsque l’authentification unique multiple est activée, la méthode de connexion sélectionnée pour « Méthode de connexion par défaut » devient le type de connexion par défaut pour les groupes/profils d’utilisateurs qui ne sont liés à aucune configuration d’authentification unique. La connexion par défaut peut être Adobe ID, SSO ou ID ALM (utilisateurs externes).

Pour configurer une authentification unique, procédez comme suit :

1. Cliquez sur Configurer l’authentification unique (SSO).
1. Cliquez sur Ajouter une nouvelle configuration SSO.
1. Dans la boîte de dialogue Configuration de l’authentification unique, ajoutez les éléments suivants :

   * Entrez le nom de l’authentification unique.
   * Sélectionnez le type d’authentification unique initiée par l’IDP ou initiée par le SP.

      * Si vous avez sélectionné Initié par le FI, saisissez l’URL du FI. Il s’agit de l’URL qui sera l’identifiant unique de votre application et des informations fournies par votre fournisseur de services IDP. Il s’agit de l’URL vers laquelle tous les utilisateurs d’Adobe Learning Manager seront redirigés après s’être connectés.
      * Chargez le fichier XML de métadonnées IDP à partir de votre fournisseur IDP. Ce fichier contient des informations sur le fournisseur d’identité qui permettent à Adobe Learning Manager d’accepter les assertions SAML qu’il contient
      * Si vous avez sélectionné Initié SP, saisissez l’ID d’entité. L’ID d’entité est une URL fournie par le fournisseur de services (SP).
      * Entrez l’URL de connexion SP. Cette URL est utilisée par les utilisateurs pour se connecter à l’application.

1. La configuration SSO est ajoutée à la liste.

## Configuration de l’authentification unique pour les utilisateurs internes

### Utilisateurs d’un fichier CSV

Procédez comme suit :

1. Importez le fichier CSV contenant les champs actifs et leurs valeurs.
1. Cliquez sur Paramètres > Méthodes de connexion.
1. Cochez la case Activer l’authentification unique (SSO) multiple pour la connexion.
1. Mappez les configurations SSO aux valeurs du champ actif.
1. Enregistrez les paramètres. Importez à nouveau le fichier CSV.

### Utilisateur unique

Procédez comme suit :

1. Cliquez sur Paramètres > Méthodes de connexion.
1. Cochez la case Activer l’authentification unique (SSO) multiple pour la connexion.
1. Sélectionnez un champ actif pour une authentification unique.
1. Liez les configurations SSO aux valeurs du champ.
1. Enregistrez les paramètres. Ajoutez un utilisateur unique et attribuez une valeur au champ actif.

### Utilisateurs auto-inscrits

Procédez comme suit :

1. Cliquez sur Paramètres > Méthodes de connexion.
1. Cochez la case Activer l’authentification unique (SSO) multiple pour la connexion.
1. Liez les configurations SSO aux valeurs du champ.
1. Enregistrez les paramètres. Ajoutez un utilisateur unique et attribuez une valeur au champ actif.
1. Ajoutez un profil d’auto-inscription.
1. Sélectionnez une valeur pour le champ SSO configuré.

Après avoir enregistré les paramètres du profil, l’URL copiée redirige les utilisateurs vers l’authentification unique liée à la valeur choisie pour le profil.

### Configuration de l’authentification unique pour les utilisateurs externes

Procédez comme suit :

1. Créez un profil externe.
1. Cliquez sur Paramètres > Méthodes de connexion.
1. Cochez la case Activer l’authentification unique (SSO) multiple pour la connexion.
1. Liez la configuration SSO au profil externe créé.
1. Enregistrez les paramètres.

Après avoir enregistré les paramètres du profil, une fois enregistrée, l’URL du profil externe copiée redirige les utilisateurs vers l’authentification unique liée au profil.

## Foire aux questions

+++ Qui peut activer plusieurs connexions SSO pour les utilisateurs ?

L’administrateur et l’administrateur personnalisé peuvent activer plusieurs connexions SSO.
+++

+++ Puis-je utiliser un champ actif à valeur unique existant ou nouveau ?

Oui, vous pouvez utiliser un champ actif à valeur unique existant ou nouveau pour configurer plusieurs connexions SSO.
+++

+++Si des champs sont désactivés dans un fichier CSV, la configuration de plusieurs connexions SSO échouera-t-elle ?

Non, cela n’affectera pas la configuration des connexions SSO. Les utilisateurs seront redirigés vers une authentification unique déjà configurée.
+++

+++ Un administrateur peut-il ajouter de nouvelles valeurs au champ actif de la page lors de la configuration de l’authentification unique multiple ?

Oui, un administrateur peut ajouter de nouvelles valeurs aux champs actifs.
+++

+++ Puis-je désactiver ou supprimer des champs liés à l’authentification unique ?

Oui, vous pouvez désactiver ou supprimer des champs liés à l’authentification unique jusqu’à ce que vous dissociiez les champs de la page de configuration de l’authentification unique.
+++
