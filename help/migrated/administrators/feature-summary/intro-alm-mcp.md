---
description: Étendez Adobe Learning Manager à Claude, ChatGPT Enterprise et aux agents personnalisés afin que les élèves puissent trouver des cours, suivre la progression et obtenir des réponses.
jcr-language: en_us
title: Serveur Adobe Learning Manager Model Context Protocol
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---

# Serveur Adobe Learning Manager Model Context Protocol

Le protocole MCP (Model Context Protocol) est une norme ouverte qui permet à un client AI de découvrir et d’appeler des outils externes. Le serveur Adobe Learning Manager MCP expose les outils d’apprentissage Adobe Learning Manager à tout client compatible MCP, tel qu’un agent d’entreprise personnalisé, Claude ou ChatGPT Enterprise. Les élèves accèdent à leur formation et à leur progression à partir du client qu’ils utilisent déjà, tandis que le contenu et les enregistrements d’apprentissage restent dans Adobe Learning Manager.

## Fonctionnement du logiciel

Un élève envoie une demande en langue naturelle à un client IA. Le client sélectionne l’outil d’élève le plus pertinent et appelle le serveur MCP avec le jeton d’accès OAuth de l’élève. Adobe Learning Manager exécute l’outil en tant qu’élève et renvoie le résultat, puis le client compose la réponse finale.

Chaque appel indique l’identité de l’élève. Un élève peut donc récupérer uniquement le contenu et les enregistrements auxquels il est déjà autorisé à accéder.

Le client AI appelle le serveur MCP, qui achemine chaque demande vers l’outil d’apprentissage correspondant.

## Capacités de l’élève

Les élèves travaillent en langage naturel dans le client d’IA qu’ils utilisent déjà. Le client interprète chaque demande, appelle l’outil d’élève Adobe Learning Manager approprié et renvoie une réponse en fonction de ce à quoi l’élève peut accéder. Les élèves peuvent :

* Découvrez les cours, certifications et parcours d’apprentissage qui leur sont proposés.
* Suivez leurs inscriptions, la progression et les échéances, y compris l&#39;apprentissage qui est sur le point d&#39;expirer.
* Obtenez des réponses basées sur le contenu d’apprentissage.
* Générez un parcours d’apprentissage personnalisé à partir de leurs objectifs et enregistrez-le.

Pour obtenir la liste complète, consultez la **référence des outils de l&#39;élève**.

## Formation des clients et des partenaires

>[!IMPORTANT]
>
>Les clients qui créent leurs propres agents d’entreprise peuvent également se connecter au serveur. Par exemple, une organisation partenaire peut offrir à ses propres clients l’accès à l’apprentissage par l’intermédiaire de son propre agent.

La formation des clients et des partenaires est une utilisation principale du serveur MCP. Les organisations qui créent leurs propres agents IA d’entreprise peuvent connecter ces agents aux outils d’apprentissage Adobe Learning Manager. Leurs clients et partenaires apprennent alors à l’intérieur de l’assistant qu’ils utilisent déjà, sans passer à un assistant d’apprentissage distinct.

Par exemple, Acme Inc. crée son propre assistant IA d’entreprise. Un partenaire Acme Inc. rend visite à l’assistant pour en savoir plus sur les produits Acme Inc. L’assistant se connecte au compte Adobe Learning Manager Acme Inc. via le serveur MCP et renvoie des réponses liées à l’apprentissage. Le partenaire ne quitte jamais l&#39;expérience Acme Inc.

Cette approche permet aux organisations :

* Proposez un apprentissage intégré à l’expérience d’IA existante d’un partenaire.
* Étendez les agents d’entreprise personnalisés avec les outils d’élève de Adobe Learning Manager.
* Intégrer l’apprentissage dans leurs propres workflows.
* Intégrer l’apprentissage à leur écosystème d’IA d’entreprise.

## Formation des employés

Les employés qui utilisent déjà un client d’IA, comme Claude, peuvent y obtenir leurs informations d’apprentissage. Par exemple, un employé peut vérifier l’apprentissage attribué, consulter les inscriptions, rechercher des cours sur une rubrique ou demander un parcours d’apprentissage, sans passer par Adobe Learning Manager. Pour obtenir des exemples de demande, découvrez les [exemples d’invite pour les élèves](/help/migrated/learners/feature-summary/sample-prompts-for-learners.md).

Cette approche permet aux employés :

* Restez dans les outils qu’ils utilisent déjà.
* Parvenir à leur apprentissage où qu’ils travaillent.
* Utilisez n’importe quel client AI compatible MCP comme point d’entrée vers Adobe Learning Manager.
* Récupérez les informations d’apprentissage sans modifier le contexte.

## Un serveur pour les deux publics

La formation des clients et des partenaires et la formation des employés utilisent les mêmes outils d’apprentissage et le même serveur. Seul le public change. Choisissez l’approche qui correspond à vos élèves.

| **Audience** | **Exemple** | **Emplacement des élèves** |
|----|----|----|
| Externe | Clients et partenaires | Agent IA d’entreprise de votre organisation |
| Interne | Employés | Un client IA d’entreprise, tel que Claude ou ChatGPT Enterprise |

## Configuration des rôles

La configuration est divisée en trois rôles.

* **Administrateur :** crée une application cliente MCP dans Adobe Learning Manager et la gère. En savoir plus sur la [configuration d&#39;un serveur MCP](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).
* **Administrateur du client IA :** ajoute le serveur au client IA d&#39;entreprise de l&#39;organisation, tel que Claude ou ChatGPT Enterprise.
* **Élève :** sélectionne **Connect** dans le client AI, authentifie la connexion et fournit les détails de son compte Adobe Learning Manager.

## Sécurité des demandes des élèves

Chaque élève authentifie la connexion et fournit les détails de son compte Adobe Learning Manager. Chaque demande s’exécute en tant qu’élève. Par conséquent, le client AI renvoie uniquement les informations auxquelles l’élève peut accéder dans Adobe Learning Manager. Le serveur n’accorde pas d’accès supplémentaire aux élèves.

## Limitations

* Le serveur MCP est disponible uniquement pour les comptes Adobe Learning Manager Ultimate.
* La disponibilité des outils dépend de ce que votre client AI prend en charge.
* Le serveur traite chaque demande comme nouvelle. Les conversations multi-tours ne fonctionnent que si votre client AI conserve le contexte de la conversation.
