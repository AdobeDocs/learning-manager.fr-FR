---
description: L’API de rapport utilisateur incrémentiel permet aux administrateurs d’exporter uniquement les utilisateurs dont les données ont changé au cours d’une période spécifiée. Cela élimine la nécessité d’exporter l’intégralité des utilisateurs et permet une synchronisation plus efficace des enregistrements d’utilisateurs nouveaux ou mis à jour.
jcr-language: en_us
title: Rapport utilisateur incrémentiel (API de tâche)
source-git-commit: aad13507c56f0c2020a97e809edd9fa0b223479f
workflow-type: tm+mt
source-wordcount: '1576'
ht-degree: 1%

---


# Rapport utilisateur incrémentiel (API de tâche)

## Présentation

Le rapport d’utilisateur incrémentiel de Adobe Learning Manager est une nouvelle fonctionnalité d’API de tâche qui permet aux administrateurs et aux développeurs d’intégration d’exporter uniquement les utilisateurs dont les données ont été modifiées dans une fenêtre de date et d’heure spécifiée. Au lieu d’extraire à chaque fois la liste complète des utilisateurs, vous pouvez demander une tranche ciblée couvrant uniquement les utilisateurs nouveaux ou modifiés.

Ce document couvre :

- Pourquoi les rapports incrémentiels existent et quand les utiliser
- Fonctionnement de la fonctionnalité, y compris le modèle de suivi des modifications
- La nouvelle API de tâche pour les rapports utilisateur incrémentiels (payload, parameters, pagination)
- Comment gérer les grands comptes (plus de 5 00 000 utilisateurs)
- Champs suivis et non suivis
- Limites et non-objectifs

## Pourquoi utiliser la création de rapports incrémentiels

Cette section explique la motivation de la fonctionnalité et doit vous aider à décider si les exportations incrémentielles ou complètes correspondent le mieux à votre intégration.

## Problème avec les exportations de licences utilisateur complètes

L’exportation utilisateur complète actuelle (type de tâche generateUsers) renvoie chaque utilisateur d’un compte à chaque exécution. Pour les grands comptes d&#39;entreprise, cela crée deux problèmes importants :

| Client | Volume utilisateur |
|----------|-------------|
| Client A | 2,1 millions d’utilisateurs |
| Client B | 7 millions d’utilisateurs |
| Client C | Plus de 1 million d’utilisateurs |
| ID client | 7,7 millions d’utilisateurs (migration) |


* À ces échelles, le pipeline d’exportation s’exécute à environ 90 % de l’utilisation du processeur lors de la récupération, du traitement et du stockage des données.
* Les tableaux de bord en aval (PowerBI, Salesforce, intégrations personnalisées) réingèrent les enregistrements d’utilisateur inchangés à chaque exécution, ce qui fait perdre de la bande passante et du temps de traitement.
* Il est impossible de demander « quels utilisateurs ont changé depuis ma dernière exportation ? » à l’aide de l’API actuelle.

## Quand utiliser les rapports incrémentiels

Utilisez l’exportation incrémentielle lorsque vous devez garder un système externe synchronisé avec les données utilisateur Adobe Learning Manager. Cas d’utilisation typiques :

* Maintenir un tableau de bord d’entreprise (PowerBI, Tableau, SFDC) à jour avec les modifications de profil utilisateur.
* Alimentation des systèmes de gestion des identités en aval avec des modifications de rôle, d’état ou de métadonnées.
* Exécution nocturne ou horaire des pipelines de synchronisation delta au lieu de rechargements complets.
* Réduction de la charge d’API et des coûts de transfert de données pour les comptes comptant des millions d’utilisateurs.

Utilisez l’exportation complète (generateUsers) lorsque vous avez besoin d’une ligne de base faisant autorité, par exemple lors de la première configuration ou après un long intervalle entre les synchronisations.

| Mode d’exportation | Utiliser quand... |
|-------------|-----------|
| Exportation complète (generateUsers) | Données d’amorçage initiales ; comptes avec moins de 50 000 utilisateurs ; récupération après une fenêtre de synchronisation manquée. |
| Exportation incrémentielle (generateUserIncrementalReport) | Synchronisation delta régulière ; grands comptes ; pipelines ne nécessitant que des enregistrements modifiés |

## Rapport sur l’utilisateur complet actuel

(generateUsers) Cette section documente le rapport utilisateur d’API de tâche existant à titre de référence. Si vous le connaissez déjà, passez à la section suivante.

## Fonctionnement

Le rapport CSV de l’utilisateur actuel est soumis en tant que travail via l’API de travaux. Un pipeline Snaplogic récupère la tâche, exécute une requête MySQL sur la base de données du CAPTIVATE (tables user, usergroup, usergroup_user) et génère un fichier CSV.

## Filtres disponibles

La charge utile prend en charge trois filtres facultatifs :

* `expandMetadata` - Transmettez true pour exporter les métadonnées en tant que colonne distincte.
* `fetchActiveUsers` - Passe true pour exporter uniquement les utilisateurs actifs.
* `peerAccountId` - Pour générer le rapport d&#39;utilisateur pour un compte de pairs.

## Colonnes CSV

Le fichier CSV exporté contient les colonnes suivantes :

```
internalUserID, userEmail, customerDefinedUniqueUserId, name, managerEmail,

userType, state, excludedFromGamification, pointsEarned, profile, roles,

dateCreated, lastLoginDate, dateDeleted, uiLocale, contentLocale,

timeZoneCode, userSource, group, AF_location, AF_login, AF_externalaf,

lastSocialActivityDate
```

## Charge utile de la demande

Type de tâche : generateUsers. Rôle d’administrateur uniquement.

```
{

  "data": {

    "type": "job",

    "attributes": {

      "description": "<description of your choice>",

      "jobType": "generateUsers",

      "payload": {

        "expandMetadata": "<true to export metadata as separate column>",

        "fetchActiveUsers": "<true to export ACTIVE users only>",

        "peerAccountId": "<peerAccountId for peer account report>"

      }

    }

  }

}
```

## Limitations

* Aucun filtrage basé sur la date : chaque exécution exporte tous les utilisateurs.
* Impossible pour les grands comptes - épuisement des ressources de pipeline supérieur à ~1 million d&#39;utilisateurs.
* Aucune capacité incrémentielle ou delta.

## Rapport utilisateur incrémentiel (generateUserIncrementalReport)

Cette section décrit la nouvelle fonctionnalité : Rapport utilisateur incrémentiel.

## Qu’est-ce qu’une exportation incrémentielle ?

Une exportation incrémentielle renvoie uniquement les utilisateurs dont les données suivies ont été modifiées dans une fenêtre de date et d’heure de début et de fin spécifiée. Le serveur principal stocke un horodatage de la dernière modification pour les champs suivis de chaque utilisateur. Lorsque vous demandez un état pour une fenêtre donnée, seuls les utilisateurs dont la modification la plus récente se situe dans cette fenêtre sont inclus.

## Fonctionnement du modèle de suivi des modifications

Adobe Learning Manager conserve un horodatage de la dernière modification qui est mis à jour chaque fois qu’un champ suivi d’un utilisateur est modifié.

Lorsque vous demandez un rapport incrémentiel avec start_date_time et end_date_time, le système renvoie les utilisateurs dont l&#39;horodatage de la dernière modification est compris entre [start_date_time, end_date_time]. Si un utilisateur a été modifié à la fois pendant et après la fenêtre (c&#39;est-à-dire qu&#39;il a été modifié à nouveau après end_date_time), cet utilisateur n&#39;est pas inclus dans le rapport, car son horodatage modifié en dernier lieu se trouve désormais au-delà de la fenêtre.

>[!NOTE]
>
>Cela signifie qu’une exportation incrémentielle capture les utilisateurs dont la modification la plus récente se trouve dans la fenêtre spécifiée - tous les utilisateurs qui ont été touchés à un moment donné pendant la fenêtre.

## Champs suivis pour les modifications

Un utilisateur est inclus dans un rapport incrémentiel si l’un des champs suivants a été modifié :

| Champ | Notes |
|---|---|
| userEmail | Adresse e-mail de l’utilisateur |
| name | Prénom de l’utilisateur |
| managerId | La table utilisateur stocke managerId. Si le managerId change, le champ est marqué comme étant modifié. Si seule l’adresse e-mail du responsable change (même managerId), ce champ n’est PAS considéré comme modifié. |
| type | Classification interne ou externe des utilisateurs |
| l&#39;état | Actif ou supprimé |
| profile | Affectation de profil utilisateur |
| Rôles | Ajouts ou suppressions de rôles |
| uiLocale | Paramètres régionaux de l’interface utilisateur |
| contentLocale | Paramètres régionaux du contenu |
| timeZoneCode | Fuseau horaire de l’utilisateur |
| Champs actifs (AF_*) | Tous les champs actifs configurés, par exemple AF_location, AF_login |
| métadonnées | Tous les champs de métadonnées configurés |

## Champs non suivis pour les modifications

Les champs suivants apparaissent dans la sortie CSV, mais ne déclenchent pas l’inclusion dans une exportation incrémentielle lorsqu’ils sont modifiés :

* excludeFromGamification
* pointsEarned
* lastLoginDate
* dateDeleted
* dateCreated
* userSource
* lastSocialActivityDate

## Format de sortie

Le rapport CSV incrémentiel a les mêmes colonnes et le même format que le rapport CSV de l’utilisateur complet. Toutes les colonnes apparaissent dans le même ordre, y compris toutes les colonnes de champs actifs et de métadonnées, indépendamment des champs modifiés pour les utilisateurs exportés.

>[!NOTE]
>
>Si un nouveau champ actif est ajouté ou qu’un champ existant est supprimé, tous les utilisateurs affectés par cette modification apparaîtront lors de la prochaine exportation incrémentielle. Les nouvelles colonnes des nouveaux champs actifs sont ajoutées à la fin du rapport afin que les intégrations existantes liées à la position des colonnes ne soient pas rompues.

## Nouvelle API de tâche pour le rapport utilisateur incrémentiel

Le rapport utilisateur incrémentiel utilise l’API de tâche pour générer un fichier CSV contenant les utilisateurs dont les données suivies ont changé dans la fenêtre de date et d’heure spécifiée. Pour les jeux de résultats volumineux, utilisez le même modèle de pagination décrit plus loin dans ce document : soumettez la même fenêtre de date dans chaque demande et passez le dernier ID utilisateur reçu dans la réponse précédente en tant que fromUserId pour récupérer le bloc suivant.

## Type de tâche

Type de tâche : generateUserIncrementalReport

## Charge utile de la demande

```
{

    "data": {

        "type": "job",

        "attributes": {

            "description": "description of your choice",

            "jobType": "generateUserIncrementalReport",

            "payload":{

                 "fullExport": <Pass true to export all users. If fullExport is true, fromDate and toDate are ignored>,

                 "expandMetadata": <Pass true to export metadata as separate columns>,

                 "fromDate": <Start of the change window in ISO format, for example 2020-01-01T18:30:00.000Z>,

                 "toDate": <End of the change window in ISO format, for example 2020-01-31T18:30:00.000Z>,

                 "fromUserId": <For paginated requests, pass the last userId received in the previous response>

            }

        }

   }

}
```

## Paramètres de charge utile

| Paramètre | Type | Description |
|---|---|---|
| fromDate | Chaîne (ISO 8601) | Requis pour l’exportation incrémentielle. Au début de la fenêtre de modification. Utiliser le format ISO 8601. |
| toDate | Chaîne (ISO 8601) | Requis pour l’exportation incrémentielle. Fin de la fenêtre de modification. Utiliser le format ISO 8601. |
| fromUserId | String | Facultatif. Pour les demandes paginées, transmettez le dernier ID utilisateur reçu dans la réponse précédente en tant que fromUserId. Omettez ce paramètre pour la première demande. |
| expandMetadata | Booléen | Facultatif. Si la valeur est True, les métadonnées sont exportées sous forme de colonnes distinctes. |

Pour une exportation incrémentielle, passez `fromDate` et `toDate` pour définir la fenêtre de modification. Si le jeu de résultats est supérieur à un bloc, poursuivez la pagination en envoyant les mêmes `fromDate` et `toDate` et en transmettant le dernier `userId` de la réponse précédente en tant que `fromUserId`. Si fullExport a la valeur true, la fenêtre de date est ignorée et l’API génère une exportation utilisateur complète.

## Gestion des grands comptes (plus de 500 k utilisateurs)

Les rapports des utilisateurs sont générés à l’aide d’un pipeline de plateforme de données et la sortie est retournée par blocs pour prendre en charge les comptes volumineux. Si une exportation incrémentielle couvre plus de 500 000 utilisateurs, le rapport est paginé.

## Modèle de pagination

Pour récupérer toutes les pages d’une exportation incrémentielle volumineuse, transmettez les mêmes startDateTime et endDateTime dans chaque demande, ainsi que l’ID utilisateur du dernier utilisateur reçu dans le segment précédent à partir de l’ID utilisateur. L’API renvoie le prochain ensemble de 500 000 utilisateurs maximum avec un ID utilisateur supérieur à l’ID transmis par l’utilisateur.

## Workflow de pagination

Étape 1 : soumettez la première demande sans fromUserId.

```
// First request – no fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z"

  }

}
```

Étape 2 : recevez le premier bloc (jusqu’à 500 000 utilisateurs). Notez le dernier ID utilisateur dans la réponse.

Étape 3 : soumettez la demande suivante, en passant la même fenêtre de date et le dernier ID utilisateur de la réponse précédente que fromUserId.

```
// Subsequent request – pass last userId from previous response as fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z",

    "fromUserId": "<last userId from previous response>"

  }

}
```

Étape 4 : répétez l’opération jusqu’à ce qu’une réponse renvoie moins de 500 000 enregistrements, indiquant que vous avez atteint la dernière page.

| Requête | fromUserId, paramètre |
|---|---|
| Première page | Ignorer de l’ID utilisateur |
| Deuxième page | Transmettez le dernier ID utilisateur de la première page comme fromUserId. |
| Troisième page | Transmettez le dernier ID utilisateur de la deuxième page en tant que fromUserId. |
| ... (continuer) | ... |
| Dernière page | La réponse contient moins de 500 000 enregistrements |

>[!NOTE]
>
>Assurez-vous que vos `startDateTime` et `endDateTime` restent identiques dans toutes les demandes paginées pour une seule exécution d’exportation. La modification de la fenêtre de date au milieu de la pagination produira des résultats incohérents.

## Limitations

La portée du rapport utilisateur incrémentiel est intentionnelle. Les fonctionnalités suivantes ne sont pas couvertes :

* Pas un rapport d’audit de l’utilisateur : il ne répertorie pas les champs spécifiques modifiés.
* Aucune comparaison entre anciennes et nouvelles valeurs : le rapport affiche uniquement les valeurs de champ actuelles.
* Aucun horodatage par modification : l’heure des modifications individuelles des champs n’est pas affichée.
* Aucune indication du nombre de modifications : un utilisateur modifié une fois et un utilisateur modifié dix fois apparaissent de manière identique dans l’exportation.
* Le format de rapport existant reste inchangé : la structure des colonnes du fichier CSV est identique à celle du rapport complet de l’utilisateur.

## Intégration du connecteur

Le rapport utilisateur incrémentiel est conçu pour être utilisé dans les connecteurs Adobe Learning Manager (PowerBI, Salesforce et autres) en tant que remplacement compensé pour le rapport utilisateur complet dans les pipelines de synchronisation régulière. Cela permet aux connecteurs qui utilisent actuellement generateUsers de migrer vers le modèle incrémentiel sans apporter de modifications au schéma de données en aval.

Les connecteurs peuvent utiliser le rapport incrémentiel pour la synchronisation delta et revenir au rapport complet pour les données d’amorçage ou la récupération.
