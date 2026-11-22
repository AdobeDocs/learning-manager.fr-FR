---
description: Permettez aux élèves de découvrir les cours, de suivre la progression et d’obtenir des réponses à partir du contenu Adobe Learning Manager dans Claude, ChatGPT Enterprise et les agents personnalisés.
jcr-language: en_us
title: Serveur Adobe Learning Manager Model Context Protocol
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: f6dc1e97076edf812862b80a6ed5931989c660da
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%
---

# Serveur Adobe Learning Manager Model Context Protocol

## Présentation

Le protocole MCP (Model Context Protocol) est un moyen standard pour un client AI de se connecter aux outils. Le serveur MCP Adobe Learning Manager permet aux élèves de suivre leur formation là où ils travaillent déjà. Cela expose les outils de l’élève Adobe Learning Manager à tout client d’IA qui prend en charge MCP, tel qu’un agent d’entreprise personnalisé, Claude ou ChatGPT. Les élèves peuvent ensuite accéder à leurs formations et progresser depuis le même client, tandis que le contenu reste dans Adobe Learning Manager.

## Capacités de l’élève

Les élèves travaillent en langage naturel dans le client d’IA qu’ils utilisent déjà. Le client interprète chaque demande, appelle l’outil d’élève Adobe Learning Manager approprié et renvoie une réponse en fonction de ce à quoi l’élève peut accéder. Les élèves peuvent :

* Découvrez les cours, certifications et parcours d’apprentissage qui leur sont proposés.
* Suivez leurs inscriptions, la progression et les échéances, y compris l&#39;apprentissage qui est sur le point d&#39;expirer.
* Obtenez des réponses basées sur le contenu d’apprentissage.
* Générez un parcours d’apprentissage personnalisé à partir de leurs objectifs et enregistrez-le.
Pour obtenir la liste complète, consultez la **référence des outils de l&#39;élève**.

Le client AI appelle le serveur MCP, qui achemine chaque demande vers l’outil d’apprentissage correspondant.

Pour obtenir la liste complète, consultez la **référence des outils de l&#39;élève**.

## Formation des clients et des partenaires

La formation des clients et des partenaires est une utilisation principale du serveur MCP. Les organisations qui créent leurs propres agents IA d’entreprise peuvent connecter ces agents aux outils d’apprentissage Adobe Learning Manager. Leurs clients et partenaires apprennent alors à l’intérieur de l’assistant qu’ils utilisent déjà, sans passer à un assistant d’apprentissage distinct.

Par exemple, Acme Inc. crée son propre assistant IA d’entreprise. Un partenaire d&#39;Acme Inc. visite l&#39;environnement de Tech Corp pour en apprendre davantage sur les produits de Tech Corp. L’assistant d’Acme se connecte à son compte Adobe Learning Manager via le serveur MCP et renvoie des réponses liées à l’apprentissage, de sorte que le partenaire ne quitte jamais l’expérience Acme.

Cette approche permet aux organisations :

* Proposer un apprentissage dans le cadre de l’expérience d’IA existante d’un partenaire.
* Laissez les agents d’entreprise personnalisés utiliser les outils d’apprentissage Adobe Learning Manager.
* Intégrer l’apprentissage dans leurs propres workflows.
* Intégrer l’apprentissage à leur écosystème d’IA d’entreprise.

## Formation des employés

Les employés qui utilisent déjà un client d’IA, comme Claude, peuvent y obtenir leurs informations d’apprentissage. Par exemple, un employé peut vérifier l’apprentissage attribué, consulter les inscriptions, rechercher des cours sur une rubrique ou demander un parcours d’apprentissage, sans passer par Adobe Learning Manager. Pour des exemples de demandes, voir [exemples d’invites pour les élèves](https://word-edit.officeapps.live.com/docs/sample-prompts-adobe-learning-manager-learners).

Cette approche permet aux employés :

* Restez dans les outils qu’ils utilisent déjà.
* Parvenir à leur apprentissage où qu’ils travaillent.
* Utilisez n’importe quel client AI prenant en charge MCP comme point d’entrée vers Adobe Learning Manager.
* Obtenez des informations d’apprentissage sans modifier le contexte.

## Un serveur pour les deux publics

La formation des clients et des partenaires et la formation des employés utilisent les mêmes outils d’apprentissage et le même serveur. Seul le public change. Choisissez l’approche qui correspond à vos élèves.

| **Audience** | **Exemple** | **Emplacement des élèves** |
|----|----|----|
| Externe | Clients et partenaires | Agent IA d’entreprise de votre organisation |
| Interne | Employés | Un client IA d’entreprise, tel que Claude ou ChatGPT Enterprise |

## Configuration des rôles

La configuration est répartie entre trois rôles.

* **Administrateur :** crée une application cliente MCP dans Adobe Learning Manager et la gère. Voir [configurer un serveur MCP](https://word-edit.officeapps.live.com/docs/configure-model-context-protocol-server-adobe-learning-manager).
* **Administrateur du client IA :** ajoute le serveur au client IA d&#39;entreprise de l&#39;organisation, tel que Claude ou ChatGPT Enterprise.
* **Élève :** sélectionne **Connect** dans le client AI, authentifie la connexion et fournit les détails de son compte Adobe Learning Manager.

## Sécurité des demandes des élèves

Chaque élève authentifie la connexion et fournit les détails de son compte Adobe Learning Manager. La demande s’exécute en tant qu’élève. Le client AI renvoie donc uniquement les informations auxquelles l’élève peut accéder dans Adobe Learning Manager. Le serveur ne donne pas aux élèves un accès supplémentaire.

## Limitations de MCP dans cette mise à jour

* La disponibilité des outils dépend de ce que votre client AI prend en charge.
* Chaque demande est traitée comme nouvelle. Les conversations multi-tours ne fonctionnent que si votre client AI conserve le contexte de la conversation.
