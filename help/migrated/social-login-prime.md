---
jcr-language: en_us
title: Connexion via les réseaux sociaux dans Learning Manager
description: Connexion via les réseaux sociaux dans Learning Manager
contentowner: saghosh
preview: true
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%
---


# Connexion via les réseaux sociaux dans Learning Manager

Vous pouvez utiliser vos identifiants Facebook, LinkedIn ou Twitter pour vous connecter à Learning Manager.

## Configuration de la connexion via les réseaux sociaux {#setupsociallogin}

1. Si vous souhaitez qu’il configure le compte, contactez votre gestionnaire de succès client.

   Sinon, suivez les étapes ci-dessous.

1. Recherchez le compte sur lequel vous souhaitez configurer la connexion via les réseaux sociaux.
1. Remplacez la connexion par SSO.
1. Cliquez sur Avancé. Spécifiez le fichier JSON suivant.

   ```
   \{"linkedIn":true,"microsoft":true,"twitter":true,"facebook":true,"editingAllowed":true
   ```

   S’il s’agit d’un fichier JSON incorrect, il y aura une exception.

   Cette fonctionnalité de connexion via les réseaux sociaux est uniquement utilisée pour les utilisateurs INTERNES.

