---
jcr-language: en_us
title: Problèmes de connexion dans Learning Manager
description: Problèmes de connexion dans Adobe Learning Manager
contentowner: nluke
exl-id: 516c1a20-f185-4ace-a1e7-2cd89644863c
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 87%

---

# Problèmes de connexion dans Learning Manager

## Problème

Impossible de se connecter à Adobe Learning Manager.

## Erreur

Lorsque vous tentez de vous connecter à Adobe Learning Manager, le message d’erreur ci-dessous s’affiche :

![](assets/cp-error.png)

*Message d&#39;erreur pour une session expirée*

## Cause

Lorsqu’un utilisateur se connecte via SSO, il crée un cookie de session qui est stocké dans le navigateur. Cela permet également à l’utilisateur de se connecter à d’autres applications. La plupart des connexions SSO sont configurées pour se déconnecter après 24 heures. L’utilisateur doit s’authentifier à nouveau pour ouvrir une nouvelle session.

Dans certains cas, un utilisateur ne peut pas accéder au système en raison de cookies SSO obsolètes. Ces cookies sont transmis à Adobe Learning Manager pour authentification. La session ne se termine pas si un utilisateur n’a pas fermé le navigateur depuis un long moment ou s’il ne s’est pas déconnecté.

Adobe Learning Manager rejette ces cookies obsolètes, ce qui entraîne une erreur.

## Résolution

Si un cookie obsolète est rejeté par Adobe Learning Manager, essayez les options ci-dessous :

1. Effacez les cookies et la mémoire cache du navigateur. Pour plus d’informations, consultez ce [document](unable-log-in-learning-manager.md).

   Sinon, l’administrateur IDP peut forcer une déconnexion après un délai donné. Cette étape authentifie à nouveau l’utilisateur pour ouvrir une nouvelle session.

Il existe d’autres raisons pour lesquelles cette erreur se produit, mais le cas présenté ci-dessus est un scénario courant.

## Liens de référence :

[Microsoft : session d&#39;accès conditionnel dans une vie](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
