---
title: Guide de dépannage pour Live Hub (Beta)
description: Messages d’erreur et notifications courants que vous pouvez rencontrer au cours d’une session Live Hub, leurs causes et les étapes à suivre pour les résoudre.
source-git-commit: 43d4a9fb47d94ef541984a1c1fb9c70ba4e3f61d
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 2%

---


# Guide de dépannage pour Live Hub (Beta)

Au cours d’une session Live Hub, les instructeurs peuvent rencontrer des messages d’erreur ou des notifications qui empêchent certaines actions de se dérouler comme prévu. Cet article décrit les erreurs courantes rencontrées par les instructeurs, leurs causes possibles et les étapes à suivre pour les résoudre.

## Problèmes de connexion

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Une erreur s’est produite. Veuillez essayer de nouveau. | Une erreur générale de connectivité ou de session se produit, par exemple, lors de la jonction ou de l’interaction avec une session et la demande échoue en raison d’une instabilité du réseau, d’une session ALM expirée ou d’un état de navigateur conflictuel, tel que plusieurs onglets ouverts à la même réunion. | <ul><li>Vérifiez votre connexion réseau et assurez-vous de la stabilité de la bande passante sans interférence VPN/proxy.</li><li>Confirmez que vous êtes connecté à ALM avec une session valide : déconnectez-vous et reconnectez-vous si votre session a peut-être expiré.</li><li>Évitez de participer à la même réunion à partir de plusieurs onglets en même temps.</li><li>Essayez une fenêtre privée/privée ou videz le cache de votre navigateur si le problème persiste.</li><li>Actualiser la page : la plupart des erreurs passagères se résolvent après un rechargement ; si elles se reproduisent, contactez le support.</li></ul> |

## Problèmes liés à l’onglet Quiz

Les messages ci-dessous peuvent apparaître lorsqu’un instructeur crée ou lance un quiz qui ne répond pas aux exigences requises pour le lancer.

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Saisissez une question pour continuer. | Un instructeur tente de lancer un quiz sans saisir le texte de la question. | Saisissez la question, fournissez les options de réponse, sélectionnez la bonne réponse, puis lancez le quiz pour les participants. |
| Les options de réponse ne peuvent pas être laissées vides. | Un instructeur saisit le texte de la question, mais ne saisit pas les options de réponse ou laisse une ou plusieurs options de réponse vides. | Saisissez la question, fournissez les options de réponse, sélectionnez la bonne réponse, puis lancez le quiz pour les participants. |
| Marquez la bonne réponse. | Un instructeur saisit les options de question et de réponse, mais ne sélectionne pas l’option de réponse correcte. | Saisissez la question, fournissez les options de réponse, sélectionnez la bonne réponse, puis lancez le quiz pour les participants. |

## Problèmes liés à l’onglet Sondage

Les messages ci-dessous peuvent apparaître lorsqu’un instructeur duplique, supprime ou réinitialise un sondage.

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Impossible de dupliquer le sondage. Veuillez essayer de nouveau. | Un instructeur duplique un sondage existant et le doublon n’est pas créé. | Fermez le panneau Sondages et questionnaires et essayez à nouveau de dupliquer le sondage. |
| Impossible de supprimer tous les sondages. Veuillez essayer de nouveau. | Un instructeur supprime tous les sondages à la fois à l’aide de la commande Tout supprimer, et la suppression en bloc échoue ou ne se termine que partiellement. | Fermez le panneau Sondages et questionnaires et réessayez de supprimer les sondages à l’aide de la commande Supprimer tous les sondages. |
| Impossible de supprimer le sondage. Veuillez essayer de nouveau. | Un instructeur supprime un seul sondage et la suppression ne se termine pas. | Fermez le panneau Sondages et questionnaires et réessayez de supprimer le sondage. |
| Impossible de réinitialiser le sondage. Veuillez essayer de nouveau. | Un instructeur réinitialise un sondage précédemment exécuté afin qu’il puisse être réutilisé, et la réinitialisation ne se termine pas. | Fermez le panneau Sondages et questionnaires et réessayez de réinitialiser le sondage. |

## Problèmes de téléchargement de contenu

Le message ci-dessous peut apparaître lorsqu’un instructeur charge un fichier de référence que l’assistant AI utilise pour répondre aux questions.

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Impossible de traiter le fichier. Veuillez essayer de nouveau. | Un instructeur charge un fichier corrompu, vide ou protégé par mot de passe qui ne peut pas être traité. | Convertissez le fichier dans un format pris en charge (PDF ou PPT) et chargez-le à nouveau. |

## Problèmes de toast de téléchargement de contenu

Les messages ci-dessous apparaissent sous forme de notifications toast lorsqu’un instructeur charge un fichier de référence que l’assistant AI utilisera et que le fichier échoue à une vérification de validation spécifique.

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Impossible de traiter le fichier. Vérifiez le fichier et réessayez. | Un instructeur charge un fichier corrompu. | Vérifiez le format du fichier et convertissez-le dans un format pris en charge (PDF ou PPT), puis rechargez-le. |
| Le fichier est protégé par un mot de passe. Supprimez le mot de passe et chargez à nouveau le fichier. | Un instructeur charge un fichier protégé par mot de passe. | Supprimez la protection par mot de passe du fichier, puis rechargez-le. |
| Le fichier n’a aucun contenu à traiter. Chargez un fichier contenant du texte. | Un instructeur charge un fichier qui n’a aucun contenu à traiter par l’assistant IA. | Chargez un fichier contenant du texte. |
| « FileName.pdf » dépasse la limite de 1 Mo. | Un instructeur charge un fichier de PDF dont la taille dépasse la limite de 1 Mo. | Compressez ou réduisez la taille du fichier du PDF à moins de 1 Mo, puis rechargez-le. |
| « FileName.pptx » dépasse la limite de 3 Mo. | Un instructeur charge un fichier PPT dont la taille dépasse la limite de 3 Mo. | Compressez ou réduisez la taille du fichier PPT à moins de 3 Mo, puis rechargez-le. |

## Problèmes de session en petits groupes

Les messages ci-dessous peuvent apparaître lorsqu’un instructeur tente de démarrer une session en petits groupes.

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Impossible de démarrer l&#39;interruption — la connexion est interrompue. Veuillez réessayer une fois reconnecté. | Un instructeur tente de démarrer les salles d’atelier alors que sa connexion est actuellement interrompue ou en cours de reconnexion. | Attendez que votre connexion se stabilise (un indicateur de reconnexion est présent), puis redémarrez les salles de réunion. |
| Impossible de démarrer l&#39;éclatement. Veuillez essayer de nouveau. | Un instructeur commence les salles de petits groupes et la demande de démarrage échoue. | Réessayez de démarrer les salles de réunion. Si le problème persiste, fermez le panneau Répartitions et réessayez. |
| Impossible de générer le résumé. | Cela peut se produire dans les situations suivantes : <ul><li>Aucun utilisateur ne s’est exprimé pendant la session, il n’y a donc pas de contenu audio à résumer.</li><li>La discussion dure moins de 60 secondes.</li></ul> | Assurez-vous que les participants parlent activement pendant au moins 60 secondes pendant la session avant de générer le résumé. Si le problème persiste, attendez un moment et réessayez. |

## Problèmes de toast de génération de réponses

Le message ci-dessous peut apparaître lorsqu’un instructeur demande à l’assistant IA de générer une réponse à la question d’un participant dans la conversation.

| Message d’erreur | Scénario | Suggestions pour surmonter l’erreur |
|---|---|---|
| Cela n&#39;a pas été abordé au cours de la séance. | Un élève pose une question qui n’est pas traitée dans la référence de contenu téléchargée. Il s’agit d’un comportement attendu, et non d’une erreur. | Répondez à la question manuellement. |
