---
description: Découvrez comment intégrer le connecteur Zoom à Adobe Learning Manager
jcr-language: en_us
title: Connecteur Zoom
contentowner: mmanuel
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%
---

# Connecteur de zoom dans Adobe Learning Manager

## Introduction

Le Connecteur Zoom de Adobe Learning Manager permet une intégration transparente avec Zoom pour offrir des sessions de classe virtuelle en direct. Grâce à cette intégration, les instructeurs peuvent organiser des réunions Zoom directement à partir de Learning Manager, inscrire des élèves et suivre les données de présence et d’achèvement. Les élèves reçoivent des invitations automatiques et peuvent participer aux sessions via leur compte Adobe Learning Manager. Après la session, les données de présence et de performances sont synchronisées avec Adobe Learning Manager pour la création de rapports et le suivi.

## Configuration du connecteur Zoom

Pour configurer le Connecteur de zoom :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur d’intégration.
2. Survolez la vignette **Zoom**.

   ![](assets/zoom-connector1.png)
   _Configuration du Connecteur de zoom dans Adobe Learning Manager_

3. Sélectionnez **Se connecter**. La page de configuration du connecteur Zoom s’ouvre.
4. Saisissez les détails de compte suivants dans les champs respectifs. Vous pouvez obtenir ces informations d’identification auprès de votre administrateur de compte Zoom :

   * Nom de la connexion
   * ID de compte Zoom
   * ID du client
   * Secret du client
   * Adresse e-mail du super administrateur

   ![](assets/zoom-connector2.png)
   _Tapez les détails de configuration pour configurer le connecteur de zoom_

5. Sélectionnez **Se connecter** pour établir l&#39;intégration.

>[!NOTE]
>
>Lors de l&#39;activation du connecteur, les **élèves doivent utiliser la même adresse e-mail** pour leurs comptes Zoom et Adobe Learning Manager afin de s&#39;assurer que les données utilisateur sont correctement synchronisées.

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

Pour utiliser le Connecteur Zoom avec Adobe Learning Manager, vous devez créer une application OAuth Zoom de serveur à serveur et configurer les portées requises.

### Portées OAuth requises

Lors de la création de l’application dans Zoom, assurez-vous que les portées suivantes sont sélectionnées :

| Ce que vous voulez | Rechercher ce mot-clé | Puis choisir |
|---|---|---|
| Afficher toutes les réunions d’utilisateurs | réunion | `meeting:read:meeting:admin, meeting:read:list_meetings:admin` |
| Afficher/gérer toutes les réunions d’utilisateurs | réunion | `meeting:update:meeting:admin, meeting:delete:meeting:admin, meeting:write:meeting:admin` |
| Afficher les données du rapport | rapport | `report:read:meeting:admin, report:read:user:admin` (Choisissez celui qui correspond à votre point de terminaison.) |
| Afficher toutes les informations utilisateur | l&#39;interface | `user:read:user:admin, user:read:list_users:admin` |
| Gérer les utilisateurs et les utilisatrices | l&#39;interface | `user:update:user:admin, user:write:user:admin` |
| Ajout d’un participant à une réunion | inscrit | `meeting:write:registrant:admin` |
| Répertorier tous les participants à la réunion | inscrit | `meeting:read:list_registrants:admin` |
| Réunions de sous-comptes | réunion + rechercher :master | `meeting:write:meeting:master` |
| Rapport sur les participants à la réunion | participant | `report:read:list_meeting_participants:admin` |

