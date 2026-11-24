---
description: Enregistrez le serveur Adobe Learning Manager MCP en tant que connecteur dans votre client d’IA d’entreprise, afin que les élèves de votre organisation puissent se connecter et interroger leur apprentissage.
jcr-language: en_us
title: Ajout de Adobe Learning Manager à votre client IA d’entreprise
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%
---

# Ajout de Adobe Learning Manager à votre client IA d’entreprise

## Présentation

Vous avez besoin de droits d’administrateur dans votre client AI. Avant de commencer, demandez l’URL du point de terminaison MCP, l’ID client et la clé secrète à votre administrateur Adobe Learning Manager. En savoir plus sur la [configuration d&#39;un serveur Model Context Protocol](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).

## Ajouter le connecteur

1. Connectez-vous à votre client IA d’entreprise en tant qu’administrateur.
2. Ouvrez les paramètres Administrateur pour les connecteurs.
3. Ajoutez un connecteur personnalisé utilisant le protocole Model Context Protocol.
4. Entrez l’URL du point de terminaison Adobe Learning Manager MCP.
5. Entrez l’ID client et la clé secrète de votre administrateur Adobe Learning Manager.
6. Enregistrez le connecteur.
7. Mettez le connecteur à la disposition de vos élèves.

>[!NOTE]
>
>Les interfaces clientes de l’IA changent fréquemment. Si ces étapes ne correspondent pas à votre client, consultez la documentation du fournisseur de votre client AI pour ajouter un connecteur distant.

## Dépannage

**Les élèves ne voient pas le connecteur.**
Confirmez que le connecteur est activé pour l’espace de travail ou le groupe de l’élève.

**L&#39;autorisation échoue lorsqu&#39;un élève sélectionne Se connecter.**
Vérifiez que l&#39;ID client et la clé secrète correspondent aux valeurs de la page **Informations d&#39;identification du client** du serveur dans Adobe Learning Manager.
