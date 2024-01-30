---
jcr-language: en_us
title: Intégration d'Adobe Connect
description: Les auteurs peuvent créer des cours d'une classe virtuelle avec Adobe Connect pendant le processus de création de cours. Pour activer Adobe Connect pour votre compte Learning Manager, vous devez contacter l'administrateur de votre entreprise.
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 70%

---



# Intégration d&#39;Adobe Connect

Les administrateurs d’une organisation peuvent configurer les paramètres du compte Learning Manager pour activer l’intégration d’Adobe Connect.

## Configurer Adobe Connect {#configureadobeconnect}

1. Dans une session administrateur, cliquez **[!UICONTROL Paramétrages]** dans le volet de gauche pour visualiser les informations de base sur votre entreprise. Cliquez sur **[!UICONTROL Adobe Connect]** dans le volet de gauche.

   ![](assets/left-pane.png)

   *Sélectionnez Adobe Connect dans le volet de gauche.*

1. Cliquez sur **[!UICONTROL Configurer maintenant]** lien entrant **[!UICONTROL Configuration d’Adobe Connect]** section.

   <!--![](assets/configure-now-connect.png)-->

1. Fournissez le nom de domaine et les informations de connexion d’Adobe Connect de votre société.

   ![](assets/adobeconnect-config.png)

   *Ajouter un nom de domaine et des informations d’identification*

   Exemple d’URL Adobe Connect : mycompany.adobeconnect.com\
   Vous devez fournir l’ID de messagerie de l’administrateur du compte Connect d’Adobe.

   Seuls les comptes Connect hébergés par Adobe sont pris en charge dans Learning Manager. Example : ’.adobeconnect.com’.

1. Cliquez sur **[!UICONTROL Intégrer].**

   Après l’authentification de l’ID de messagerie, Learning Manager affiche le message comme Connect a été intégré avec succès. Vous pouvez commencer à visualiser automatiquement vos cours de classe virtuelle à l’aide d’Adobe Connect.

   L’administrateur de compte Adobe Connect doit accepter les termes et conditions d’utilisation d’Adobe Connect. Si cela n’est pas accepté, votre authentification de connexion peut échouer. Après avoir créé le compte Adobe Connect, connectez-vous au compte une fois. Lors de la première connexion, une page affichant les termes et conditions s’affiche.

   <!--![](assets/mail-confirmation.png)-->

## Ajouter des informations relatives à la session de classe virtuelle {#addvirtualclassroomsessioninformation}

Si l’auteur d’un cours de classe virtuelle n’a pas fourni les informations de session, l’administrateur peut inclure les détails de la session.

Dans Connexion administrateur, cliquez sur le nom du cours de classe virtuelle (VC). Cliquez sur **[!UICONTROL Instances]** dans le volet de gauche et cliquez sur **[!UICONTROL Détails de la session]**.  Cliquez sur l’icône Modifier dans le coin droit de la page Détails de la session pour ajouter les informations de session.

![](assets/session-creation-admin.png)

*Ajout d’informations sur les sessions de classe virtuelle*

Grâce à l’intégration d’Adobe Learning Manager et d’Adobe Connect pour la création de modules ou sessions de classe virtuelle, votre compte Connect doit prendre en charge les salles de réunion avec un nombre de salles et d’utilisateurs simultanés adapté à votre scénario d’utilisation. Ces salles de réunion sont utilisées pour héberger des modules de classe virtuelle Learning Manager. Une nouvelle salle de réunion Connect est créée de manière dynamique par Learning Manager pour chaque module ou session de classe virtuelle dans Learning Manager.

Vous devez acheter Adobe Connect séparément d’Adobe Learning Manager.

## Participation des élèves {#learnersattendance}

Si l’hôte du cours de classe virtuelle n’assiste pas à la session, la participation n’est pas enregistrée automatiquement pour les élèves qui ont participé à la session. Dans de tels scénarios, l’administrateur peut enregistrer manuellement la présence.

Cliquez sur le cours de classe virtuelle, cliquez sur Présence dans le volet gauche de la page suivante et enregistrez la présence.
