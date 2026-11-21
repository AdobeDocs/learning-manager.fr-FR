---
description: Ajoutez le serveur Adobe Learning Manager MCP à votre client IA d’entreprise, tel que Claude ou ChatGPT Enterprise, afin que les élèves puissent s’y connecter
jcr-language: en_us
title: Ajout de Adobe Learning Manager à votre client IA d’entreprise
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---

# Ajout de Adobe Learning Manager à votre client IA d’entreprise

Vous avez besoin de droits d’administrateur dans votre client AI. Obtenez d’abord l’URL du point de terminaison MCP, l’ID client et la clé secrète de votre administrateur Adobe Learning Manager. Afficher **Configurer un serveur Model Context Protocol** pour plus de détails.

## Ajouter le connecteur

1. Connectez-vous à votre client IA d’entreprise en tant qu’administrateur.
2. Ouvrez les paramètres administrateur pour les connecteurs.
3. Ajoutez un connecteur personnalisé utilisant le protocole Model Context Protocol.
4. Entrez l’URL du point de terminaison Adobe Learning Manager MCP.
5. Entrez l’ID client et la clé secrète de votre administrateur Adobe Learning Manager.
6. Enregistrez le connecteur.
7. Mettez le connecteur à la disposition de vos élèves.

>[!NOTE]
>
>Les interfaces clientes de l’IA changent souvent. Si ces étapes ne correspondent pas à votre client, consultez la documentation du fournisseur de votre client IA pour ajouter un connecteur distant.

## Dépannage

**Les élèves ne voient pas le connecteur.** Confirmez que le connecteur est activé pour l’espace de travail ou le groupe de l’élève.

**L’autorisation échoue lorsqu’un élève sélectionne Se connecter.** Vérifiez que l&#39;ID client et la clé secrète correspondent aux valeurs de la page **Informations d&#39;identification du client** du serveur dans Adobe Learning Manager.
