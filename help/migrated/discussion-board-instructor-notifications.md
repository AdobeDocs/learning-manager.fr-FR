---
description: Découvrez comment les instructeurs et les responsables de cohorte reçoivent des résumés par e-mail des activités du forum de discussion et comment gérer les paramètres et les abonnés avec les API
jcr-language: en_us
title: Notifications de l'instructeur du forum de discussion
exl-id: 370c9add-5572-4555-8a95-ddb470c230f4
source-git-commit: 650ec8159a4291189dfc38b03701b7b96932233d
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Notifications de l&#39;instructeur du forum de discussion

## Présentation

Les notifications des instructeurs du forum de discussion fournissent aux instructeurs, aux responsables de cohorte et aux administrateurs un résumé par e-mail des activités récentes sur les forums de discussion qu&#39;ils surveillent. Cela est utile pour les instructeurs qui gèrent plusieurs cohortes et participent à plusieurs tableaux en même temps.

Un gestionnaire de cohorte est la personne qui gère un groupe d&#39;élèves (une cohorte) qui suivent un cours ou un programme ensemble au même horaire.

Au lieu d’ouvrir chaque forum individuellement, les instructeurs reçoivent des alertes en temps réel dans l’application et un résumé par e-mail, à la fréquence que vous configurez, pour les forums auxquels ils sont abonnés. Vous gérez les abonnements aux forums et les paramètres de notification via l&#39;[`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence) et l&#39;[API des abonnés](api-changes-dec-2026.md#api-get-subscribers).

## Fonctionnalités clés

* Vous pouvez abonner des utilisateurs Adobe Learning Manager actifs à des forums de discussion sélectionnés en utilisant l&#39;API des abonnés ([`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users), étendue `admin:write`). Un utilisateur doit avoir accès au forum lorsque des notifications sont envoyées.
* Les utilisateurs reçoivent des notifications en temps réel dans l’application pour les types d’événements activés et un résumé d’e-mail regroupé par forum. Les types d&#39;événements sont contrôlés par les paramètres au niveau du compte (`notifyNewPost`, `notifyComment` et `notifyReply`) dans l&#39;API [`boardSubscriptionSettings`](api-changes-dec-2026.md#api-sequence).
* La fenêtre de résumé correspond à la période dont l’activité est collectée dans un seul e-mail de résumé. Vous la définissez au niveau du compte avec l&#39;attribut `digestFrequencyHours`, de 1 à 168 heures (par exemple, 24 heures pour un résumé quotidien). Cela s’applique à tous les utilisateurs du compte.
* Vous pouvez abonner des utilisateurs par ID utilisateur ou adresse e-mail, et vous pouvez ajouter plusieurs utilisateurs dans une seule demande ([abonnements groupés](api-changes-dec-2026.md#bulk-subscriptions)). Les utilisateurs sont d’abord créés dans Learning Manager de la manière habituelle.
* L’e-mail de résumé répertorie chaque nouvelle publication, commentaire et réponse pour les types d’événements activés, avec le nom du forum, le nom et l’adresse e-mail de l’auteur, ainsi qu’un lien direct. Elle affiche également un décompte des mises à jour effectuées depuis le début de la période de résumé.
* L&#39;API `boardSubscriptionSettings` et l&#39;API des abonnés sont des API publiques. Vous pouvez donc gérer les paramètres et les abonnements sans interface utilisateur (intégrations pilotées par API).

## Cas d’utilisation

Les cas d’utilisation suivants montrent comment les notifications de l’instructeur aident :

| Cas d’utilisation | Aide apportée par la notification |
|---|---|
| Surveiller plusieurs cohortes | Un instructeur responsable de plusieurs cohortes peut recevoir une activité résumée des conseils associés à ces cohortes. |
| Examiner l’engagement de l’élève | Un gestionnaire de cohorte peut surveiller les nouvelles contributions et identifier les discussions actives sans vérifier chaque conseil séparément. |
| Suivi des conversations de suivi | Les commentaires et les réponses inclus dans le résumé aident les instructeurs à identifier les discussions qui peuvent nécessiter des conseils ou une modération. |

## Considérations importantes

* Un utilisateur doit pouvoir accéder à un forum lorsqu’une notification est envoyée. L’accès est vérifié à nouveau au moment de la livraison, pas seulement lorsque l’utilisateur est abonné. Si un abonné perd l&#39;accès à un forum, l&#39;abonnement est conservé mais les notifications pour ce forum sont ignorées.
* Le résumé étant envoyé sous la forme d’un e-mail unique, un forum occupé peut le rendre très long. Par exemple, une cohorte d&#39;environ 40 apprenants pourrait publier plusieurs centaines de commentaires en six heures.
* Si vos forums sont très actifs, utilisez une fréquence de résumé plus courte, par exemple toutes les six heures, afin que chaque e-mail reste gérable. Définissez la fréquence avec `digestFrequencyHours` dans l&#39;API [`boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings).
* Le nombre de publications dans le résumé d’e-mail est limité à 20 par tableau et par résumé. Le même plafond s&#39;applique indépendamment aux commentaires (20) et aux réponses (20) par forum. Seules les listes affichées sont tronquées ; le nombre de titres/sous-titres reflète toujours l’activité réelle non tronquée de la fenêtre.
* Le nombre d&#39;abonnés est plafonné à 200 par carte.
* Étant donné que le contenu est envoyé directement dans l’e-mail plutôt que sous forme de pièce jointe, le corps de l’e-mail a également une taille limite.

## Modèle d’abonnement, autorisations et éligibilité

* Un abonné est un utilisateur qui reçoit des notifications d&#39;un forum. Un abonnement à un forum est indépendant de la relation de suivi existante avec l’utilisateur du forum.
* Toute personne qui s’authentifie avec OAuth et possède les portées `admin:read` et `admin:write` peut utiliser les paramètres d’abonnement et les API des abonnés. `admin:read` vous permet de répertorier les abonnés et de lire les paramètres. `admin:write` vous permet d&#39;ajouter ou de supprimer des abonnés et de modifier les paramètres.
* Vous pouvez abonner n’importe quel utilisateur Learning Manager, mais l’utilisateur doit exister, être actif et avoir accès au forum pour recevoir des notifications. L’accès est revérifié lorsque les notifications et les résumés sont envoyés.
* Si un utilisateur perd l’accès, la livraison est ignorée pour ce forum et l’abonnement est conservé. La livraison reprend si l’accès est rétabli.
* Vous pouvez ajouter plusieurs utilisateurs à un forum en une seule demande (abonnements groupés). Si un utilisateur est déjà abonné, la demande aboutit toujours et aucun doublon n’est créé. Voir [Abonnements en bloc](api-changes-dec-2026.md#bulk-subscriptions) pour le format de la demande, la réponse multi-statuts 207 et les cas d’échec.

## Contenu du résumé

### Événements inclus

Le résumé inclut les nouvelles publications, les nouveaux commentaires et les nouvelles réponses lorsque le paramètre correspondant est `true` dans l&#39;API [`boardSubscriptionSettings` &#x200B;](api-changes-dec-2026.md#api-create-settings) : `notifyNewPost`, `notifyComment` et `notifyReply`. Vous les avez définies avec `POST` ou `PATCH /boardSubscriptionSettings`. Tous les paramètres sont `false` par défaut.

### Événements exclus

Le résumé exclut les événements dont le paramètre correspondant dans l&#39;API [`boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings) (par exemple, `notifyComment`) est `false`. Aucun résumé n’est envoyé lorsqu’il n’y a aucune activité éligible.

### Exemple de mise en page de l’e-mail de résumé

Un e-mail de résumé est envoyé pour chaque forum abonné ayant eu une activité éligible. Il est structuré comme suit :

* **Ligne récapitulative :** l&#39;e-mail s&#39;ouvre avec le nombre total de mises à jour sur le forum (par exemple, sept mises à jour) et une ventilation par type (par exemple, nouveaux posts et commentaires), ainsi que l&#39;heure à partir de laquelle l&#39;activité est comptée.
* **Section Tableau :** l&#39;activité est regroupée sous le nom du tableau. Chaque publication est répertoriée en dessous.
* **Détails de l&#39;élément :** chaque publication, commentaire ou réponse affiche le nom et l&#39;adresse e-mail de l&#39;utilisateur qui l&#39;a créé, ainsi qu&#39;un lien vers l&#39;élément.
* **Liens :** la sélection d&#39;un lien ouvre directement la publication, le commentaire ou la réponse. Le destinataire doit être connecté pour que le lien s’ouvre.
* **Commentaires et réponses :** ils apparaissent dans le même e-mail que les publications, de sorte que les instructeurs peuvent voir les conversations de suivi ainsi que les nouvelles rubriques.

## Configuration des notifications

### Configuration des paramètres à l’aide des API

Vous gérez les notifications via deux API publiques : l&#39;[`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence), qui s&#39;applique au niveau du compte, et l&#39;[API des abonnés](api-changes-dec-2026.md#api-get-subscribers), qui s&#39;applique par forum. Les deux utilisent les portées OAuth `admin:read` et `admin:write`. Appelez-les dans cet ordre :

1. Définissez les paramètres au niveau du compte avec [`POST /boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings).
1. Modifiez les paramètres ultérieurement, si nécessaire, avec [`PATCH /boardSubscriptionSettings`](api-changes-dec-2026.md#api-update-settings).
1. Récupérez les paramètres au niveau du compte avec [`GET /boardSubscriptionSettings`](api-changes-dec-2026.md#api-get-settings).
1. Répertoriez les utilisateurs abonnés à un forum avec [`GET /boards/{id}/subscribers`](api-changes-dec-2026.md#api-get-subscribers).
1. Abonner des utilisateurs à un forum avec [`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users).
1. Désabonner un utilisateur d&#39;un forum avec [`DELETE /boards/{id}/subscribers/{userId}`](api-changes-dec-2026.md#api-unsubscribe-user).

Utilisez l&#39;API `boardSubscriptionSettings` pour définir la fréquence du résumé en heures et activer ou désactiver les publications, les commentaires et les réponses pour le résumé. Par exemple, un compte avec une fréquence de résumé de 1 heure reçoit un e-mail de résumé toutes les heures. Tous les paramètres d&#39;événement sont `false` par défaut.

### Gestion des abonnés

Utilisez l’API des abonnés pour choisir les utilisateurs actifs de Learning Manager qui sont abonnés à tel ou tel forum. Un abonnement est distinct de la relation de suivi de conseil d’administration existante. Un utilisateur doit avoir une visibilité sur un forum pour recevoir ses notifications, ce qui signifie que l’utilisateur doit être connecté. La perte de visibilité supprime la diffusion, mais ne supprime pas l’abonnement.

### Activer la fonctionnalité

Pour activer les notifications des instructeurs, créez les paramètres au niveau du compte, puis abonnez les utilisateurs à des forums, comme décrit dans [Modifications d’API en novembre 2026](api-changes-dec-2026.md). Après cela, le système collecte les nouveaux posts, commentaires et réponses créés pendant l&#39;intervalle configuré. À la fin de l&#39;intervalle, les abonnés reçoivent une notification résumée couvrant l&#39;activité éligible sur les forums souscrits.

En savoir plus sur les modifications d&#39;API dans [Modifications d&#39;API en décembre 2026](api-changes-dec-2026.md).
