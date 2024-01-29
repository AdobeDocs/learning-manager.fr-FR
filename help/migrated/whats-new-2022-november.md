---
title: Nouveautés de cette version (novembre 2022)
description: Découvrez les nouvelles fonctionnalités et améliorations d’Adobe Learning Manager
hidefromtoc: true
source-git-commit: 1da0911a4d0c2ae5cb01bbb2b7955675b0dfcdde
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 0%

---

# Nouveautés de cette version (novembre 2022)

<!--
IN-PROGRESS

<https://helpx.adobe.com/learning-manager/whats-new-nov-2022.html>
-->

## Configuration SSO multiple

Adobe Learning Manager prend actuellement en charge une méthode de connexion pour les utilisateurs internes et une méthode de connexion pour les utilisateurs externes. Cela crée des limitations dans les cas où les clients ont leurs employés et leurs propres clients et partenaires de distribution sur le même compte.

Dans le but de prendre en charge plusieurs types de groupes d’utilisateurs se connectant à la plateforme, Adobe Learning Manager prend désormais en charge plusieurs méthodes de connexion via plusieurs configurations SSO pour les utilisateurs internes et externes.

Pour plus d’informations, voir [Plusieurs connexions SSO](/help/migrated/administrators/feature-summary/multiple-sso-logins.md).

## Prise en charge des fonctionnalités hors connexion

Le portail natif d’Adobe Learning Manager prend désormais en charge l’accès hors connexion à un portail de formation.

Les élèves peuvent désormais découvrir et accéder au site de formation, consulter divers cours et contenus disponibles et décider de se connecter pour suivre les cours.

Cette fonctionnalité facilite la création d’un portail d’apprentissage orienté client, où les élèves peuvent parcourir divers cours sans être connectés au préalable.

Pour plus d’informations, voir [Expérience hors connexion pour les élèves](/help/migrated/administrators/feature-summary/non-logged-in-experience-learners.md).

## Améliorations apportées à la page Présentation de la formation

La page Présentation de la formation affiche désormais une interface utilisateur actualisée afin que les élèves bénéficient d&#39;une expérience améliorée lorsqu&#39;ils suivent un cours.

Autres améliorations :

* Ajoutez un signet à une formation.
* Recommandation de cours connexes.
* Informations sur le ou les parcours d’apprentissage pour les cours et les parcours d’apprentissage.
* Noms d’auteurs cliquables.
* Chemins de navigation pour une navigation plus facile.

## Améliorations apportées à la page Présentation de la formation

La page Présentation de la formation affiche désormais une interface utilisateur actualisée afin que les élèves bénéficient d&#39;une expérience améliorée lorsqu&#39;ils suivent un cours.

Autres améliorations :

* Ajoutez un signet à une formation.
* Recommandation de cours connexes.
* Informations sur le ou les parcours d’apprentissage pour les cours et les parcours d’apprentissage.
* Noms d’auteurs cliquables.
* Chemins de navigation pour une navigation plus facile.

## Page Profil de l’auteur

La page de profil de l’auteur affiche toutes les formations créées par un auteur particulier.

Les élèves peuvent facilement trouver des informations spécifiques à l’auteur et toutes les formations créées par l’auteur.

## Formations marquées d’un signet

Les élèves peuvent enregistrer (à l’aide du bouton Enregistrer) ou ajouter un signet à la formation pour eux à partir de la vignette du cours ou de la page de présentation. Tous les cours marqués d’un signet sont disponibles sur la page d’accueil de l’élève.

## Personnalisation du lecteur

Dans cette version, vous pouvez personnaliser le lecteur Fluidic pour qu&#39;il corresponde aux exigences de l&#39;identité visuelle d&#39;un cours.

Vous pouvez afficher et masquer divers paramètres et options de lecteur en fonction des exigences de contenu et accorder le contrôle aux élèves en fonction du type de contenu. Vous pouvez appliquer cette modification aux implémentations natives et sans tête.

Les différentes options que vous pouvez modifier sont les suivantes :

* Activation/désactivation de la table des matières
* Notes
* Langue
* Vitesse
* Légende
* Volume
* Commandes de lecture

## Emprunt d’identité de l’élève et du responsable

Les administrateurs peuvent lancer une session avec emprunt d’identité, ce qui leur permet de se connecter au nom de n’importe quel utilisateur de leur compte dans leur rôle d’élève et de responsable.

Pour plus d’informations, voir [Emprunt d’identité de l’élève et du responsable](/help/migrated/administrators/feature-summary/impersonation-learner-manager.md).

## Autres améliorations

### Journal d’audit des e-mails

Les administrateurs peuvent désormais accéder à tous les journaux d’e-mail envoyés depuis le système via un rapport de journal d’audit d’e-mail.

Ce journal capture toutes les données liées aux e-mails envoyés au cours des 30 derniers jours et est actualisé chaque jour. En outre, le rapport contient des informations, par exemple, l’état de remise, l’expéditeur, le destinataire, l’objet et les métadonnées de contenu.

Téléchargez le rapport à partir de Rapports > Rapports personnalisés > Rapports Excel > Rapport par e-mails. Une notification s’affiche pour vous permettre de télécharger le rapport.

Ce rapport se compose des champs suivants :

* Heure de déclenchement de l’e-mail (fuseau horaire UTC)
* Heure d’état du dernier événement (fuseau horaire UTC)
* État de livraison
* Adresse e-mail du destinataire
* ID utilisateur de l’expéditeur
* Objet du courrier électronique
* Type d’entité
* Nom de l’entité
* ID d’entité

### Notification d’élève sur liste d’attente

Lorsqu’un auteur ajoute une nouvelle instance, il peut déclencher un e-mail pour informer les élèves inscrits sur liste d’attente d’autres instances. Les élèves reçoivent un e-mail de modification.

### Modèles d’e-mail au niveau de l’instance

Vous pouvez personnaliser les e-mails pour chaque instance d’une formation.

Chaque fois que l’auteur ou l’administrateur est autorisé à ajouter une nouvelle instance, le modèle d’une instance individuelle peut être modifié.

Par exemple, si un cours a différents types d’audience, vous pouvez modifier le modèle de courrier électronique en conséquence.

![modèles de courrier électronique](assets/email-template.png)

La priorité du modèle est répertoriée ci-dessous :

1. Modèle au niveau de l’instance
2. Modèle au niveau de la formation
3. Modèle de compte

### Commentaires de l’instructeur lors de l’acceptation des envois

Les instructeurs peuvent désormais ajouter des commentaires tout en acceptant les envois des élèves. Une fois l’envoi approuvé par l’instructeur, l’élève reçoit une notification par e-mail et une notification dans l’application (si cette option est activée). Les commentaires liés à l’envoi sont présents dans les relevés de notes des élèves pour l’administrateur et l’élève.

### Améliorations liées à la recherche

L’historique des recherches récentes d’un élève s’affiche afin qu’il puisse afficher toutes les recherches précédentes.

Les résultats de la recherche sont désormais cohérents pour tous les apprentissages formels et informels (apprentissage social). Les résultats incluent la formation, l’apprentissage social et les correspondances de marché de contenu.

La recherche est plus ciblée et plus ciblée, ce qui vous permet d’afficher les résultats de la recherche à trois endroits : apprentissage formel, apprentissage social et marché de contenus.

![recherche](assets/search-image.png)

#### Recherche basée sur les expressions

Dans cette version d’Adobe Learning Manager, nous avons remplacé la recherche Typeahead par la recherche basée sur les expressions.

#### Recherches récentes

Un élève peut afficher ses recherches récentes dans la session en cours uniquement.

### Catalogue de cours gratuits sur le marché de contenu

Un catalogue gratuit de 50 cours gratuits, de haute qualité et soigneusement sélectionnés est désormais disponible sur la place de marché de contenu pour les élèves.

### Prise en charge de l’indonésien

Le bahasa indonésien est désormais ajouté en tant que langue d’interface dans les applications de l’élève et du responsable.

### Champ Auteur obligatoire

Lors de la création d’un cours, le champ Auteur est obligatoire.

### Modifications apportées au Marché de contenus

* Les comptes d’évaluation nouvellement créés répertorient un nouveau catalogue de 50 cours gratuits sur le Marché de contenus, qui sont disponibles pour les utilisateurs.
* Un élève peut désormais voir le nombre de résultats de recherche et lier des liens intégrés pour la redirection vers le Marché de contenus.

### Modifications immersives mobiles

Dans cette version, les utilisateurs Web immersifs mobiles peuvent effectuer les tâches répertoriées ci-dessous :

* Créer - Publications de sondage
* Modifier le post - tous les types, RTE
* Flux de production d’e-commerce.
* Prévisualiser un module : les élèves auront la fonctionnalité Aperçu du module dans Immersif mobile. Cette modification permettra aux élèves de prévisualiser le module avant de s&#39;inscrire à un cours.
* Copiez une URL.
* Supprimer un forum.

### Modifications du connecteur de zoom

Le type d’application JWT sera obsolète en juin 2023. Nous vous recommandons de créer des applications OAuth ou OAuth de serveur à serveur pour remplacer les fonctionnalités d’une application JWT dans votre compte.

### Rapport de ludification

Dans cette version, vous avez accès à un rapport qui affiche divers cours dans lesquels la ludification a été activée.

### Importation des préférences de langue via CSV

Lors de l’importation d’un fichier CSV, le fichier CSV contient les champs Interface Language, Content Language et Time Zone.

L’administrateur peut également exporter le rapport, qui contient les mêmes champs que ci-dessus.

* Langue de l’interface
* Langue du contenu
* Fuseau horaire

Outre les administrateurs, un administrateur personnalisé peut également exporter ce rapport.

![rapport de langue](assets/language-report.png)

#### Impact sur la localisation

* Les noms de colonne ne peuvent pas être localisés et doivent être tels quels (Interface Language, Content Language, Timezone).
* Les codes de paramètres régionaux ne sont pas sensibles à la casse.
* Bien qu’il n’y ait aucune restriction quant à la saisie du code de pays, vous pouvez spécifier uniquement le code de langue. Par exemple, « it_IT » et « it » sont valides.
* S’il y a une différence dans le rapport en raison d’un code de paramètres régionaux incorrect, le traitement csv continue, comme d’habitude, et il n’a aucune incidence sur les autres enregistrements dans le fichier csv. La préférence de paramètres régionaux de l’utilisateur avec des paramètres régionaux incorrects n’est pas mise à jour. Le reste des données est mis à jour.

## Modifications et améliorations apportées aux API

### Connecteurs VC

Si un ID de messagerie d&#39;administrateur est utilisé pour configurer le connecteur VC, cet administrateur particulier doit avoir l&#39;autorisation pour les éléments suivants :

* Création d’une réunion
* Mise à jour d’une réunion
* Récupération du rapport de présence

Lors de la création ou de la mise à jour de la réunion VC, les instructeurs doivent METTRE FIN à la réunion dans les 30 minutes suivant l’heure de fin prévue de la réunion.

### Signet

Les API suivantes sont ajoutées pour ajouter un signet à un cours sur la page Présentation de la formation :

* Obtenir tous les signets : `primeapi/v2/bookmarks`
* Créer un signet : `primeapi/v2/learningObjects/{id}/bookmark`
* Supprimer un signet : `primeapi/v2/learningObjects/{id}/bookmark`

### Prise en charge des métadonnées et du contenu multilingues via la migration

Pour tous les types de formation pris en charge dans la plateforme (cours, parcours d’apprentissage, modules, certifications et assistances à la tâche), la migration multilingue peut désormais être prise en charge via des fichiers CSV en utilisant des colonnes supplémentaires pour d’autres langues.

#### Conditions préalables

Créez le projet de migration en tant qu’administrateur d’intégration, puis partagez l’ID de projet de migration avec l’équipe d’assistance ALM afin que l’indicateur multilingue puisse être activé à partir du serveur principal.

#### Portée des objets de migration multilingue

* Module
* Cours
* Version du module
* Certification
* Programme d’apprentissage
* Assistance à la tâche
* Version de l’assistance à la tâche

#### Spécification CSV

Adobe Learning Manager vous fournit un ensemble de spécifications CSV standard pour la migration multilingue. Il est recommandé de parcourir ces spécifications CSV avant de commencer le processus de migration. L’administrateur d’intégration de votre organisation peut analyser les formats de données existants et les mapper pour qu’ils correspondent aux éléments de modèle CSV fournis par Learning Manager.

#### Modifications avec prise en charge multilingue

* La colonne module_version n’est pas prise en charge dans module_version.csv et course_module.csv.
* Impossible de mettre à jour module_version dans la même exécution (dans la même exécution, le module ne peut pas être migré avec deux versions avec le même module).
* La mise à jour du contenu ou des métadonnées est considérée comme une mise à jour de version de module à partir de module_version.csv.
* Impossible de prendre en charge la mise à jour de Job_Aid_Version via job_aid_version.csv

### Révoquer les jetons d’authentification et les cookies

Une application LMS sans en-tête reçoit refresh_token lors de la première connexion. Par la suite, refresh_token est utilisé pour générer access_token pour que ses applications clientes effectuent des appels API. De même, la lecture de contenu utilise le point de terminaison oauth pour générer un cookie pour gérer la lecture, ce qui implique plusieurs fichiers de contenu et des appels d’api appelés par ces fichiers à l’aide d’un cookie. Le cookie généré par oauth a la même validité que le jeton access_token, qui est de sept jours. Une fois le cookie généré, il n&#39;y a aucun moyen de l&#39;effacer, contrairement à la déconnexion typique de l&#39;application web. Le cookie Oauth et le cookie de l’application web sont deux cookies différents et ne se connaissent pas.

Donc, pour effacer le cookie, nous avons introduit un nouveau point de terminaison, qui révoque refresh_token, cookie, et cookie et refresh token.

**Détails**

**Point de terminaison**

`POST oauth/o/revoke`

**Paramètres de requête**

* `cookie=true|false` - indique que le cookie doit être révoqué
* `refresh_token=true|false` - indique que refresh

**Corps de la demande**

Corps requis pour la révocation de refresh_token ou (refresh_token et cookie)

```
{
      "client_id": <>,
      "client_secret": <>,
      "refresh_token": <>
}
Body required for revoking oauth cookie only
{
      "access_token": <>
}
```

### API rendues publiques

Dans cette version, nous avons rendu certaines API publiques.

| API | Type | Description |
|---|---|---|
| /social/search | GET | Recherche dans les réseaux sociaux. |
| /announcements | GET | Obtenez des informations détaillées sur l’annonce dans l’en-tête attribué à l’élève. |
| /announcements/`{id}` | GET | Obtenez des informations détaillées sur l’annonce dans l’en-tête attribué à l’élève. |
| /learningObjects/`{id}`/loResources/{loResourcesId} | GET | Chargez l&#39;URL du fichier pour loResource de resourceType « Activity » où l&#39;envoi de fichier est requis. |
| /jobAid/`{jobAidId}`/jobAidDownloaded | GET | Définissez le rapport de téléchargement de l’assistance à la tâche. |
| /bulkimport/startrun | POST | Exécutez l’importation en bloc. |
| /bulkimport/cansync | GET | Synchronisation de l’importation en bloc. |
| /search | GET | DELETEMEBOB |
| /uploadInfo | GET | Obtenez des informations relatives à la mise à jour du contenu. |
| /uploadSigner | GET | Obtenez la signature du contenu to_sign. |
| /avatar | POST | Met à jour l’image de l’avatar de l’élève avec une nouvelle image. |
| /avatar | DELETE | Supprime l’image d’avatar de l’élève. |

### Application Salesforce

Le **Ignorer les LO de niveau supérieur** doit être activée dans l’application Salesforce afin que tous les cours, programmes d’apprentissage et certificats puissent être affichés en même temps.

### API pour la personnalisation du lecteur

Dans cette version, nous avons fourni des API pour personnaliser un lecteur. Vous pouvez :

* Démarrez ou chargez le lecteur.
* Accédez à un module particulier.
* Activer/désactiver la table des matières.
* Changer de langue.
* Fermez le lecteur.
* Lecture, pause, avance, retour, recherche, modification du volume ou de la vitesse.
* Capturez les événements émis par le lecteur.

### Afficher la position d’un élève sur la liste d’attente

Le GET /enrollments/{id}L’API /waitlistPosition sous l’API LO récupère la position d’un utilisateur sur la liste d’attente pour une inscription spécifiée.

### Soumission de la date d’achèvement dans les certifications externes

L’API /primeapi/v2/learningObjects/certification:xxxxx aura l’attribut « completionDateSameAsApprovalDate » pour indiquer que l’option « Date d’achèvement de la certification » est activée pour l’élève ou désactivée dans le certificat avec l’indicateur True/False.

### Données d’aperçu Get LO

Le GET /preview/learningObjects/{id} L’API est ajoutée pour obtenir des informations d’aperçu sur un objet d’apprentissage.

### Déplacement d’utilisateurs externes dans des profils

Le `PUT primeapi/v2/externalProfiles/{currentep}/users/{userid}?` l&#39;appel permet de déplacer un utilisateur vers un autre profil externe en spécifiant un nouvel ID externalProfile.

### Ajout d’utilisateurs à des profils externes

Le `POST /externalProfiles/{id}/users` ajoute des utilisateurs externes dans le profil externe.

## Notes de mise à jour

Pour plus d’informations sur les versions actuelles et précédentes de l’application web et de l’application pour appareil Learning Manager, consultez la section [Notes de mise à jour](/help/migrated/release-note/release-notes.md).

## Correctifs de bogues

Pour voir les bogues corrigés dans cette mise à jour, reportez-vous à la section [Liste des problèmes résolus](release-note/release-notes.md#bugs-fixed-in-this-release).

## Configuration requise

[Configuration requise pour Learning Manager](/help/migrated/system-requirements.md)
