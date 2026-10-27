---
description: Découvrez comment les webhooks d’achèvement Go1 aident Adobe Learning Manager à capturer les achèvements de cours, même lorsque les élèves ferment le navigateur prématurément
jcr-language: en_us
title: Suivi de l’achèvement Go1 avec webhooks
exl-id: 25c9c401-905f-4408-89ac-ac630a45a0c7
source-git-commit: aaea92d190b8ab22ce9f08c309faf5caa0b58a69
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%
---

# Suivi de l’achèvement Go1 avec webhooks

## Présentation

Adobe Learning Manager prend désormais en charge le suivi d’achèvement basé sur webhook pour le contenu Go1. Cette amélioration améliore la fiabilité de la synchronisation de l’achèvement des cours entre Go1 et Learning Manager. Les événements d’achèvement sont capturés même lorsque les élèves quittent le lecteur de cours juste après avoir terminé un cours.

Go1 utilise des webhooks pour envoyer des notifications d’achèvement de cours à Learning Manager chaque fois qu’un élève termine un cours Go1. Learning Manager reçoit et traite ces événements d’achèvement indépendamment de la session du navigateur de l’élève.

Go1 tente également de remettre le webhook jusqu’à ce que Learning Manager accuse réception de l’événement d’achèvement. Cela permet d’éviter les enregistrements d’apprentissage manqués ou incomplets.

## Problème résolu par cette amélioration

Auparavant, le suivi de l’achèvement dépendait de la communication entre le lecteur Go1 et Learning Manager pendant que la session de navigateur de l’élève restait active. Si un élève fermait la fenêtre du navigateur ou quittait le navigateur avant que l’état d’achèvement ne soit entièrement traité, l’enregistrement d’achèvement pouvait être perdu.

Résultat :

* Les terminaisons de cours peuvent ne pas apparaître dans les relevés de notes des élèves.
* Les administrateurs pouvaient trouver des écarts entre les réalisations réelles et enregistrées.
* Les événements d’achèvement manqués n’ont pas pu être récupérés automatiquement.

## Workflow d’événement

1. Un élève lance et termine un cours Go1.
1. Go1 enregistre l’achèvement.
1. Go1 envoie un webhook d’achèvement à Learning Manager.
1. Learning Manager valide et accepte l’événement d’achèvement.
1. Learning Manager met à jour l’état d’achèvement de l’élève.
1. Si Learning Manager n’accuse pas réception de l’événement, Go1 tente automatiquement de nouveau la remise.

## Foire aux questions

**Cette modification nécessite-t-elle une configuration administrateur** ?

Non, cette modification ne nécessite aucune configuration administrateur.

**Les cours Go1 existants sont-ils affectés** ?

Non, les cours Go1 existants ne sont pas affectés. L’amélioration améliore la synchronisation de l’achèvement pour le contenu Go1.

**Que se passe-t-il si un élève ferme le navigateur prématurément** ?

Go1 envoie le webhook d’achèvement indépendamment de la session du navigateur de l’élève. Même si l’élève quitte le lecteur de cours, Go1 tente à nouveau de le dispenser jusqu’à ce que Learning Manager accuse réception de l’événement d’achèvement.
