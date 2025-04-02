---
description: Les administrateurs peuvent lancer une session avec emprunt d’identité, ce qui leur permet de se connecter au nom de n’importe quel utilisateur de leur compte dans leurs rôles d’élève et de responsable.
jcr-language: en_us
title: Emprunt d’identité de l’élève et du responsable
contentowner: saghosh
exl-id: 0306f255-283f-43b9-9494-11b3dc3765da
source-git-commit: f44f44ab34acc42edb79d66588ad986d629734ff
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 59%

---

# Emprunt d’identité de l’élève et du responsable {#impersonation-of-learner-and-manager}

Dans les grandes organisations, le personnel du service clientèle a besoin d’une fonctionnalité d’emprunt d’identité pour déboguer les problèmes rencontrés par les élèves.

Grâce à cette possibilité d’emprunter l’identité d’autres utilisateurs, les administrateurs peuvent identifier et effectuer toutes les activités effectuées par les élèves et les responsables de leur organisation.

>[!NOTE]
>
>Les administrateurs personnalisés ne peuvent pas emprunter l’identité des utilisateurs ; seuls les administrateurs peuvent le faire.

## Fonctionnement du logiciel

Les administrateurs peuvent rechercher un utilisateur (interne ou externe), puis emprunter son identité. L’administrateur est ensuite redirigé vers la page de l’utilisateur (application de gestionnaire, le cas échéant, ou autre application d’élève), puis il déconnecte l’administrateur de sa session. L’administrateur est ensuite redirigé vers la page Compléter votre profil, au cas où l’identité de l’utilisateur a été empruntée par l’administrateur.

Voici ce que vous devez garder à l’esprit lorsque vous empruntez l’identité d’un utilisateur :

* Tous les administrateurs voient cette fonctionnalité par défaut.
* Seuls les utilisateurs actifs du compte peuvent se voir emprunter leur identité.
* Un administrateur ne peut pas emprunter sa propre identité.
* Un administrateur personnalisé qui a accès à la page Utilisateurs peut emprunter l’identité des utilisateurs.
* Un administrateur/administrateur personnalisé ne peut emprunter une identité que pendant 60 minutes.
* Un administrateur personnalisé disposant d’un accès en lecture seule ne peut pas emprunter l’identité des utilisateurs.

## Emprunter l’identité d’un utilisateur

Pour emprunter l’identité d’un utilisateur, suivez les étapes ci-dessous :

1. Connectez-vous à l’application en tant qu’administrateur.
1. Sélectionnez Profil > Emprunter l’identité de l’utilisateur.

   Vous ne pouvez emprunter l’identité que d’un seul utilisateur à la fois.

1. Recherchez un utilisateur (interne/externe) dans la zone de recherche présente dans la fenêtre modale. Vous ne pouvez emprunter l’identité que d’un seul utilisateur à la fois. Sélectionnez Continuer.

   Vous pouvez également effectuer une recherche avec l’adresse e-mail de l’utilisateur, l’UUID, etc.

1. Un message s’affiche avec la confirmation que vous emprunterez l’identité d’un utilisateur.

   Sélectionnez Continuer.

   Un message de confirmation, « Mode de personnification : Vous êtes connecté en tant que « nom d’utilisateur (adresse e-mail de l’utilisateur) ». « Déconnexion » apparaît sur l’en-tête de la page.

**Une session empruntée dure 60 minutes.**

Lors du passage à un rôle d’élève ou de responsable, un message s’affiche indiquant que l’administrateur est en mode d’emprunt d’identité de l’utilisateur.

## Rapport sur les connexions et accès

La connexion et l’accès d’un administrateur sont capturés dans le rapport de connexion et d’accès. Un enregistrement est créé dans le rapport pour chaque utilisateur représenté par l’administrateur.

Les colonnes qui font partie de cette fonction sont les suivantes :

* Identité empruntée par le nom d’utilisateur
* Identité empruntée par l’adresse électronique de l’utilisateur

Ces colonnes sont ajoutées à la fin du rapport.

Chaque connexion est comptée séparément dans le rapport.

## Éléments non pris en charge

* Emprunt d’identité des composants AEM.
* Emprunt d’identité dans l’application mobile.
* Emprunt d’identité en immersif mobile.
* Emprunt d’identité d’applications immersives. S’applique uniquement aux applications ALM.

## Forum aux questions

+++Puis-je me connecter à Adobe Learning Manager même lorsque mon identité est empruntée ?

Oui, la connexion d’un utilisateur est indépendante de l’emprunt d’identité.
+++

+++ Les événements d’emprunt d’identité sont-ils comptabilisés de manière unique ?

Oui, chaque accès/visite de connexion par l’administrateur pendant l’emprunt d’identité sera compté séparément.
+++

+++Quel est le délai d’expiration de l’emprunt d’identité ?

Il est de 60 minutes. Si un utilisateur qui emprunte l’identité ferme la fenêtre du navigateur, puis accède à une URL principale dans les 60 minutes, l’activité d’emprunt d’identité se poursuit et le message de bannière doit s’afficher.
+++
