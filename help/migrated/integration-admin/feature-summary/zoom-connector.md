---
description: Découvrez comment intégrer le connecteur Zoom à Adobe Learning Manager
jcr-language: en_us
title: Connecteur Zoom
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 1%

---


# Connecteur Zoom dans Adobe Learning Manager

## Introduction

Le connecteur Zoom de Adobe Learning Manager permet une intégration transparente avec Zoom pour offrir des sessions de classe virtuelle en direct. Grâce à cette intégration, les instructeurs peuvent organiser des réunions Zoom directement à partir de Learning Manager, inscrire des élèves et suivre les données de présence et d’achèvement. Les élèves reçoivent des invitations automatiques et peuvent participer aux sessions via leur compte Adobe Learning Manager. Après la session, les données de présence et de performances sont synchronisées avec Adobe Learning Manager pour la création de rapports et le suivi.

## Configuration du connecteur Zoom

Pour configurer le connecteur de zoom :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Survolez la vignette **Zoom**.

   ![](assets/zoom-connector1.png)
   _Configurer le connecteur Zoom dans Adobe Learning Manager_

3. Sélectionnez **Se connecter**. La page de configuration du connecteur Zoom s’ouvre.
4. Saisissez les détails de compte suivants dans les champs respectifs. Vous pouvez obtenir ces informations d’identification auprès de votre administrateur de compte Zoom :

   * Nom de la connexion
   * ID de compte Zoom
   * ID du client
   * Secret du client
   * Adresse e-mail du super administrateur

   ![](assets/zoom-connector2.png)
   _Tapez les détails de configuration pour configurer le connecteur Zoom_

5. Sélectionnez **Se connecter** pour établir l&#39;intégration.

>[!NOTE]
>
>Lors de l&#39;activation du connecteur, **les élèves doivent utiliser la même adresse e-mail** pour leurs comptes Zoom et Adobe Learning Manager afin de s&#39;assurer que les données utilisateur sont correctement synchronisées.

## Création de cours Zoom

Une fois la connexion établie :

1. Connectez-vous en tant qu&#39;**auteur** et créez un nouveau cours de classe virtuelle.
2. Sélectionnez **Zoom** comme système de conférence lors de la création du cours.
3. Affectez des élèves au cours via des administrateurs, des responsables ou par le biais d’une auto-inscription.
4. Lors de l’inscription, les élèves reçoivent un e-mail avec les détails du cours.
5. Les élèves peuvent se connecter à leur compte Adobe Learning Manager pour accéder au cours et rejoindre la session Zoom.

## Suivi de l’assiduité et de l’achèvement

Après la fin de la session virtuelle :

* Adobe Learning Manager reçoit automatiquement l’état d’achèvement de Zoom.
* Les administrateurs peuvent afficher les rapports de présence et de score dans Adobe Learning Manager pour suivre la participation et les performances des élèves.

## Création d’une application OAuth Zoom de serveur à serveur

Pour utiliser le connecteur Zoom avec Adobe Learning Manager, vous devez créer une application OAuth Zoom de serveur à serveur et configurer les portées requises.

### Portées OAuth requises

Lors de la création de l’application dans Zoom, assurez-vous que les portées suivantes sont sélectionnées :

| Description de l&#39;étendue | Portée du zoom |
|---|---|
| Afficher toutes les réunions d’utilisateurs | administrateur:read:de réunion |
| Afficher et gérer toutes les réunions d’utilisateurs | administrateur:write:de réunion |
| Afficher les données du rapport | report:read:admin |
| Afficher toutes les informations utilisateur | utilisateur:read:administrateur |
| Gérer les utilisateurs et les utilisatrices | utilisateur:write:administrateur |
| Ajout d’un participant à une réunion | participant à la réunion:write:inscription : administrateur |
| Répertorier tous les participants à la réunion | meeting:read:list_registrants:admin |
| Gestion des réunions de sous-comptes | meeting:write:meeting:master |
| Afficher le rapport sur les participants à la réunion | report:read:list_meeting_participants:admin |
