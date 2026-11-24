---
description: Enregistrez le serveur Adobe Learning Manager MCP en tant que connecteur personnalisé dans votre propre compte Claude et authentifiez-vous pour interroger votre apprentissage.
jcr-language: en_us
title: Ajouter Adobe Learning Manager à Claude en tant qu’élève
exl-id: 31c00b29-4919-48b7-9993-ed3ac358ba5e
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%
---

# Ajouter Adobe Learning Manager à Claude en tant qu’élève

## Présentation

Utilisez ces étapes uniquement si votre organisation n’a pas encore ajouté le connecteur pour vous. Si un connecteur Adobe Learning Manager apparaît dans Claude, sélectionnez **Connecter** à la place.

## Ajouter le connecteur dans Claude

1. Dans Claude, accédez à **Personnaliser** > **Connecteurs**.
2. Sélectionnez **Ajouter** (**+**), puis sélectionnez **Ajouter un connecteur personnalisé**.
3. Entrez un **nom**, tel que Adobe Learning Manager.
4. Entrez l&#39;URL du point de terminaison MCP dans **URL du serveur MCP distant**.
5. Sélectionnez **Continuer**.
6. Sous **Authentification**, conservez **Connexion**.
7. Sous **Client OAuth**, sélectionnez **Utiliser votre propre client OAuth**.
8. Entrez l&#39;ID client dans **ID client**.
9. Entrez la clé secrète dans **Clé secrète du client**.
10. Sélectionnez **Ajouter**.
11. Connectez-vous à Adobe Learning Manager lorsque la page de connexion s’ouvre.

Une fois connecté, le connecteur s’affiche comme connecté. Posez une question sur votre apprentissage. Pour des idées, découvrez les [exemples d’invite pour les élèves](/help/migrated/learners/feature-summary/sample-prompts-for-learners.md).

>[!IMPORTANT]
>
>Claude labellise le champ Secret client comme facultatif, mais Adobe Learning Manager l’exige. Si vous laissez le champ vide ou si vous saisissez une valeur incorrecte, la connexion échoue et un message **Échec de l’autorisation** s’affiche.

>[!NOTE]
>
>Vos demandes s’exécutent avec vos propres autorisations. Claude ne peut voir que ce que vous pouvez voir dans Adobe Learning Manager.

## Utiliser un autre compte Adobe Learning Manager

Si votre navigateur a déjà une session Adobe Learning Manager active, Claude se connecte à ce compte sans demander d’informations d’identification. Pour vous connecter en tant qu’utilisateur différent, déconnectez-vous d’abord de Adobe Learning Manager ou utilisez une fenêtre de navigateur privée.

## Autres clients IA

Pour ChatGPT ou un autre client, les étapes diffèrent. Consultez la documentation de votre client AI pour ajouter un connecteur personnalisé et utilisez les mêmes trois valeurs de votre administrateur.

## Dépannage

**La connexion affiche un message de redirection non enregistré.**
Votre administrateur doit ajouter le domaine Claude à **Rediriger les domaines** pour le serveur. Demandez à votre administrateur d&#39;ajouter <https://claude.ai> et réessayez.

**Claude affirme que l&#39;autorisation a échoué.**
Vérifiez si la clé secrète contient des espaces superflus ou une valeur incorrecte. Copiez-le à nouveau à partir de votre administrateur, supprimez le connecteur et ajoutez-le à nouveau.

**Vous vous êtes connecté avec le mauvais utilisateur.**
Déconnectez le connecteur, déconnectez-vous de Adobe Learning Manager et reconnectez-vous dans une fenêtre de navigateur privée.

**Claude vous demande de vous reconnecter.**
Votre session a expiré ou votre accès a été révoqué. Sélectionnez **Se connecter** pour vous reconnecter.
