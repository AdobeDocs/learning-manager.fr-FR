---
jcr-language: en_us
title: Guide d’utilisation des webhooks
description: En savoir plus sur l’utilisation des webhooks, les bonnes pratiques et les limitations
contentowner: chandrum
exl-id: e6a63ffb-7fdd-46e4-b5e6-20ce36861cef
source-git-commit: 4b26eddf1285651a13ee9c71fdf677e8b92e6dc3
workflow-type: tm+mt
source-wordcount: '3369'
ht-degree: 1%

---

# Guide d’utilisation des webhooks

Les webhooks permettent aux applications web de communiquer entre elles automatiquement et en temps réel.

Contrairement aux API traditionnelles, qui attendent qu’un utilisateur demande des informations, les API en temps réel partagent des données dès qu’elles se produisent. Les webhooks agissent comme une API en temps réel et permettent de partager les données immédiatement chaque fois que l’événement spécifié se produit.

## Entités

Pour comprendre les événements de webhooks, nous devons d’abord connaître les entités concernées et les conditions de déclenchement de ces événements.

### Objets d’apprentissage

Les événements suivants sont pris en charge pour les objets d’apprentissage (Cours, Parcours d’apprentissage ou Certifications).

#### Brouillon

Chaque fois qu&#39;un objet d&#39;apprentissage est créé à partir de l&#39;interface utilisateur, il démarre en mode **Brouillon**. Cela signifie que l’objet d’apprentissage n’est pas encore publié et n’est pas disponible pour les élèves. L&#39;événement **LEARNING_OBJECT_DRAFT** est déclenché tant que l&#39;objet d&#39;apprentissage reste un brouillon. Toute mise à jour successive du brouillon déclenchera également cet événement.

#### Mise à jour 

Une fois l&#39;objet d&#39;apprentissage publié, son état passe de **Brouillon** à **Publié**. Pendant cette transition, le webhook génère l&#39;événement **LEARNING_OBJECT_MODIFICATION**, car l&#39;objet d&#39;apprentissage est en cours de modification de **Version préliminaire** à **Publié**. Toutes les modifications et mises à jour ultérieures de l’objet d’apprentissage déclenchent également un événement **LEARNING_OBJECT_MODIFICATION**.

L&#39;événement **LEARNING_OBJECT_MODIFICATION** est également déclenché lorsque l&#39;objet d&#39;apprentissage est retiré. Cette opération retirée marque les instances sous-jacentes comme étant mises à jour, car ces instances sont retirées une fois que l&#39;objet d&#39;apprentissage parent est dans l&#39;état retiré.

#### Supprimer

Lors de la suppression d&#39;un objet d&#39;apprentissage, l&#39;événement **LEARNING_OBJECT_DELETION** est généré. Cet événement indique que l’objet d’apprentissage a été supprimé et n’est plus accessible aux élèves.

En plus des événements en temps réel, les événements d&#39;objet d&#39;apprentissage ont également une contrepartie batch (non temps réel), qui est déclenchée dans le cadre de l&#39;événement **LEARNING_OBJECT_MODIFICATION_BATCH**. Cet événement se produit lors de la création ou de la modification d’un objet d’apprentissage via le workflow de migration. Étant donné que les opérations de brouillon et de suppression d&#39;objets d&#39;apprentissage ne sont pas prises en charge via la migration, il n&#39;existe aucun événement de brouillon ou de suppression correspondant pour ces actions.

### Instances d’objets d’apprentissage

Les événements suivants sont pris en charge pour les instances d’objets d’apprentissage.

#### Mise à jour 

Une fois qu&#39;une instance est créée, l&#39;événement **LEARNING_OBJECT_INSTANCE_MODIFICATION** est généré. Les instances d&#39;objets d&#39;apprentissage dans Adobe Learning Manager n&#39;ont pas l&#39;état **Version préliminaire**. Par conséquent, Adobe Learning Manager ne prend pas en charge un événement **LEARNING_OBJECT_INSTANCE_DRAFT**. Cet événement est généré chaque fois qu&#39;une instance est créée, modifiée ou retirée.

En plus d&#39;être généré lorsqu&#39;une instance est créée, mise à jour ou retirée, cet événement est également généré automatiquement lorsque son objet d&#39;apprentissage parent est marqué comme **Retiré**. En effet, lorsqu&#39;un objet d&#39;apprentissage est retiré, les instances sous-jacentes doivent également être marquées comme **retirées**.

#### Supprimer

Lorsqu&#39;une instance est supprimée, l&#39;événement **LEARNING_OBJECT_INSTANCE_DELETION** est généré. Cet événement s&#39;applique uniquement aux instances de cours qui contiennent des modules d&#39;auto-apprentissage, car Adobe Learning Manager permet uniquement aux administrateurs de supprimer les instances de cours dont le type de module est d&#39;auto-apprentissage. Adobe Learning Manager ne prend pas en charge les suppressions explicites pour les autres types de modules de cours non destinés aux instances de parcours d’apprentissage ou de certification.

L&#39;instance de l&#39;objet d&#39;apprentissage a également un homologue en temps non réel, exposé dans le cadre de l&#39;événement **LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH**. Cet événement est déclenché lors de la création ou de la modification d&#39;une instance d&#39;objet d&#39;apprentissage par le biais du flux de migration. Les opérations de brouillon ou de suppression pour les instances d&#39;objets d&#39;apprentissage n&#39;étant pas prises en charge lors de la migration, les événements de brouillon ou de suppression correspondants ne sont pas disponibles.

### Inscription

Une fois qu&#39;un élève a effectué une action d&#39;inscription, un événement d&#39;inscription en temps réel est déclenché. Selon le type d’objet d’apprentissage, l’événement d’inscription en temps réel peut appartenir à l’une des catégories suivantes :

* COURSE_ENROLLMENT
* LEARNING_PATH_ENROLLMENT
* CERTIFICATION_ENROLLMENT

Les événements d&#39;inscription ont des contreparties de lot en plus de ces événements en temps réel. Chaque fois qu’une inscription est déclenchée par un administrateur, un responsable ou une plateforme, des événements d’inscription en temps non réel sont déclenchés. En fonction du type d’objet d’apprentissage, l’événement d’inscription par lots peut être l’un des suivants :

* COURSE_ENROLLMENT_BATCH
* LEARNING_PATH_ENROLLMENT_BATCH
* CERTIFICATION_ENROLLMENT_BATCH

### Désinscription

Lorsqu’un élève effectue une action de désinscription, un événement de désinscription en temps réel est déclenché. Selon le type d’objet d’apprentissage, l’événement de désinscription en temps réel peut appartenir à l’une des catégories suivantes :

* COURSE_UNENROLLMENT
* LEARNING_PATH_UNENROLLMENT
* CERTIFICATION_UNENROLLMENT

En plus de ces événements, il existe également des événements de désinscription par lots. Chaque fois qu’une désinscription est marquée par un administrateur, un responsable ou une plateforme, des événements de désinscription en temps non réel sont déclenchés. En fonction du type d’objet d’apprentissage, l’événement de désinscription par lots peut être l’un des suivants :

* COURSE_UNENROLLMENT_BATCH
* LEARNING_PATH_UNENROLLMENT_BATCH
* CERTIFICATION_UNENROLLMENT_BATCH

### Accomplissement

L’événement d’achèvement en temps réel est déclenché chaque fois qu’un élève termine un objet d’apprentissage. En fonction du type d’objet d’apprentissage, l’événement d’achèvement en temps réel peut appartenir à l’une des catégories suivantes :

* COURSE_COMPLETED
* LEARNING_PATH_COMPLETED
* CERTIFICATION_COMPLETED

En plus de ces événements en temps réel, il existe également des événements d’achèvement de lot. Par exemple, lorsqu’un administrateur, un responsable ou une plateforme marque un objet d’apprentissage comme terminé, les événements d’achèvement en temps non réel sont déclenchés. En fonction du type d’objet d’apprentissage, l’événement d’achèvement par lots peut appartenir à l’une des catégories suivantes :

* COURSE_COMPLETED_BATCH
* LEARNING_PATH_COMPLETED_BATCH
* CERTIFICATION_COMPLETED_BATCH

### Progression de l’élève

Chaque fois qu&#39;un élève s&#39;inscrit à un objet d&#39;apprentissage et commence le module, sa progression est suivie. Ces données sont incluses dans l&#39;événement **LEARNER_PROGRESS**. L’événement peut être retardé de 15 minutes maximum, car le suivi de la progression repose sur une logique d’agrégation complexe, qui n’est pas en temps réel.

### Statistiques CI

L&#39;événement en temps réel **CI_STATS** est déclenché chaque fois qu&#39;il y a un changement dans la disponibilité du siège ou de la liste d&#39;attente pour une instance de cours. Ces données sont capturées uniquement au niveau de l’instance. En outre, cet événement est déclenché pour les cours et non pour d’autres parcours d’apprentissage ou certifications, car la disponibilité des places et des listes d’attente sont des attributs spécifiques à un cours et à son instance.

## Ordre des événements

Adobe Learning Manager veille à ce que les événements soient classés pour chaque compte. Cependant, il peut y avoir des différences dans la corrélation des messages entre les événements d’inscription ou d’achèvement et de progression. Cela se produit car l’événement de progression de l’élève peut être retardé de 15 minutes maximum, car le suivi de la progression repose sur une logique d’agrégation complexe, qui n’est pas en temps réel. En outre, les événements de progression proviennent de différentes sources de données, de sorte que leur ordre ne peut pas être garanti en relation avec les événements d’inscription et d’achèvement. Par conséquent, Adobe Learning Manager fournit les meilleures pratiques aux clients lors de l’écoute de ces événements.

Si l’événement d’achèvement se produit avant l’événement de progression de l’élève, le client peut ignorer cet événement. En effet, l’événement de progression de l’élève peut être retardé de 15 minutes maximum, tandis que l’événement d’achèvement peut être déclenché avant la réception de l’événement de progression. Étant donné que la réception d’un événement d’achèvement indique que l’objet d’apprentissage est terminé, cela signifie que la progression a atteint 100 %.

Dans les rares cas où l’événement d’inscription survient après l’événement de progression de l’élève, le client peut ignorer l’événement d’inscription. En effet, la progression ne peut être suivie qu’une fois que l’élève s’est inscrit à l’objet d’apprentissage. En d’autres termes, la réception d’un événement de progression indique que l’objet d’apprentissage a été démarré, ce qui ne se produit qu’après une inscription réussie.

## Evénements en temps réel et événements par lots

Certains événements ont des contreparties en temps réel et en temps non réel, comme mentionné ci-dessus. Des questions peuvent se poser quant au moment où vous devez vous abonner à des événements en temps réel et à celui où vous devez vous abonner à des événements en dehors de ce temps. Les instructions suivantes peuvent être suivies en fonction des entités décrites ci-dessus.

### Événements en temps réel

| S.No | Événements de webhook | Description |
|---|---|---|
| 1 | CI_STATS | Déclenché en cas de modification de la disponibilité des places ou de la liste d&#39;attente pour une instance de cours. |
| 2 | COURSE_ENROLLMENT | Déclenché lorsqu’un élève s’inscrit à un cours. |
| 3 | COURSE_COMPLETED | Déclenché lorsqu’un élève termine un cours. |
| 4 | LEARNING_PATH_ENROLLMENT | Déclenché lorsqu’un élève s’inscrit à un parcours d’apprentissage. |
| 5 | LEARNING_PATH_COMPLETED | Déclenché lorsqu’un élève termine un parcours d’apprentissage. |
| 6 | CERTIFICATION_ENROLLMENT | Déclenché lorsqu’un élève s’inscrit à une certification. |
| 7 | CERTIFICATION_COMPLETED | Déclenché lorsqu’un élève termine une certification. |
| 8 | COURSE_UNENROLLMENT | Déclenché lorsqu’un élève se désinscrit d’un cours. |
| 9 | LEARNING_PATH_UNENROLLMENT | Déclenché lorsqu’un élève se désinscrit d’un parcours d’apprentissage. |
| 10 | CERTIFICATION_UNENROLLMENT | Déclenché lorsqu’un élève se désinscrit d’une certification. |
| 11 | LEARNING_OBJECT_DRAFT | Déclenché lors de la création d’un objet d’apprentissage à l’état de brouillon. |
| 12 | LEARNING_OBJECT_DELETION | Déclenché lors de la suppression d’un objet d’apprentissage. |
| 13 | LEARNING_OBJECT_MODIFICATION | Déclenché lors de la modification d’un objet d’apprentissage. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Déclenché lors de la création ou de la modification d’une instance d’objet d’apprentissage.<div><b>Remarque :</b> il est recommandé d&#39;utiliser des instances de cours uniquement après la publication du cours.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Déclenché lors de la suppression d’une instance d’objet d’apprentissage. |

### Événements hors temps réel

| S.No | Événements de webhook | Description |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme inscrit des élèves à un cours. |
| 2 | COURSE_COMPLETED_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme marque un cours comme terminé. |
| 3 | LEARNING_PATH_ENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme inscrit des élèves à un parcours d’apprentissage. |
| 4 | LEARNING_PATH_COMPLETED_BATCH | Déclenché lorsqu’un administrateur/responsable marque un parcours d’apprentissage comme terminé. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme inscrit des élèves à une certification. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme marque une certification comme terminée. |
| 7 | LEARNER_PROGRESS | Suit la progression d’un élève lorsqu’un module est terminé. |
| 8 | COURSE_UNENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/gestionnaire/plateforme désinscrit des élèves d’un cours. |
| 9 | LEARNING_PATH_UNENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme désinscrit des élèves d’un parcours d’apprentissage. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Déclenché lorsqu’un administrateur/responsable/plateforme désinscrit des élèves d’une certification. |
| 11 | LEARNING_OBJECT_MODIFICATION_BATCH | Déclenché lors de la modification d’un objet d’apprentissage via le workflow de migration. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Déclenché lors de la création ou de la modification d’une instance d’objet d’apprentissage via le workflow de migration. |

### Objets d’apprentissage et ses instances

* Abonnez-vous à des événements en temps réel chaque fois que vous souhaitez écouter les modifications apportées aux objets d’apprentissage par le biais d’actions de l’interface utilisateur par des rôles tels qu’administrateur, auteur, etc.
* Abonnez-vous à des événements en temps non réel ou par lots chaque fois que vous souhaitez écouter les modifications apportées aux objets d’apprentissage par le biais des processus de migration.

### Inscription, désinscription et achèvement

* Abonnez-vous à des événements en temps réel chaque fois que vous souhaitez écouter les inscriptions, les désinscriptions ou les achèvements effectués par les élèves.
* Abonnez-vous à des événements en temps non réel ou par lots chaque fois que vous souhaitez écouter les inscriptions, les désinscriptions ou les achèvements marqués par l’administrateur, le responsable, la plateforme, etc.

### Progression de l’élève

* Abonnez-vous à l’événement chaque fois que vous souhaitez écouter les modifications de progression d’un élève.

>[!NOTE]
>
>Dans les scénarios ci-dessus (inscription, désinscription, achèvement et progression), les combinaisons d&#39;attributs constituées de userId et loInstanceId peuvent identifier un enregistrement de manière unique.

### État de l’instance de cours

* Abonnez-vous à l&#39;événement **CI_STATS** en temps réel chaque fois que vous souhaitez écouter les changements de disponibilité des places ou des listes d&#39;attente.

## Payload d’événement de webhook

Dans le cadre de la payload de réponse Webhooks, Adobe Learning Manager émet les attributs requis pour identifier de manière unique une entité. Celles-ci seront émises dans le même format et selon les normes utilisées par l’API publique, afin de garantir la synchronisation des données du webhook avec les données de l’API publique. Affichez [Exemples de charges](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#sample-payloads-for-the-events) pour voir les charges des différents événements.

## Utilisation de webhooks pour créer une base de données externe ou un service de notification

L’un des cas d’utilisation pour lesquels les webhooks peuvent être utiles est la création d’une base de données du côté du client. Adobe Learning Manager possède sa propre base de données et son propre schéma, mais les clients n’y ont pas accès.

La question est la suivante : comment les clients peuvent-ils créer une base de données en utilisant des événements de webhooks ?

Étant donné que Adobe Learning Manager n’expose pas directement les enregistrements de table et le schéma, les clients peuvent compter sur la solution Webhooks pour créer une base de données externe en utilisant les événements pour la remplir. Dans cette version, nous fournissons des événements pour les objets d&#39;apprentissage, les instances d&#39;objets d&#39;apprentissage, l&#39;inscription, la désinscription, l&#39;achèvement, la progression et les statistiques des instances de cours.

### Création d&#39;une base de données à partir d&#39;événements d&#39;objets d&#39;apprentissage

Les événements d&#39;objet d&#39;apprentissage affichent `loId` et `loType` pour identifier une entité. Toutefois, ces attributs ne suffisent pas à créer une base de données d’objets d’apprentissage externes. Les clients auront besoin de champs supplémentaires pour décrire davantage l’objet d’apprentissage.
Il existe deux approches pour récupérer les données supplémentaires :

#### Générer un rapport de données de formation pour récupérer toutes les données

Cette approche doit être utilisée lorsque les objets d’apprentissage sont créés en bloc via des workflows tels que la migration. L&#39;objectif ici est de générer le rapport **[!UICONTROL Données de formation]** avec tous les objets d&#39;apprentissage assimilés dans le cadre du workflow de migration. Pour optimiser le processus d’importation, il est recommandé de définir l’heure de début de l’exportation sur l’heure de déclenchement de la migration. Ainsi, seuls les objets d’apprentissage importés via la migration seront exportés dans le rapport, car les données historiques seront déjà disponibles dans la base de données du client.

#### Interrogez les informations à partir du GET d’API public /learningObjects - Portée de l’administrateur

Cette approche doit être utilisée lorsque les objets d’apprentissage sont créés via des workflows en temps réel. Le client doit avoir sa propre couche de mise en cache pour traiter par lots les objets d&#39;apprentissage émis via les événements, puis interroger l&#39;API `GET /learningObjects` en transmettant ces ID d&#39;objets d&#39;apprentissage. La raison d’être d’une couche de mise en cache est de s’assurer que les limites de débit de l’API publique ne sont pas dépassées. Actuellement, nous avons des limites de débit d’administration définies à 500 demandes par heure pour ` GET /learningObject` API. Si cette limite est dépassée, le service API public répond avec un message **Nombre de demandes HTTP 429 trop élevé**.

### Création d&#39;une base de données à partir d&#39;une instance d&#39;objet d&#39;apprentissage et d&#39;événements CI_STATS

L’événement Instance d’objet d’apprentissage émet les attributs `loInstanceId`, `loId` et `loType` pour les cours et les parcours d’apprentissage. De même, l&#39;événement **CI_STATS** s&#39;applique uniquement aux cours, car `seatLimit`, `seatAvailability`, `waitListLimit`, `waitlistAvailability`, etc., s&#39;appliquent uniquement aux cours.

Dans certains cas, des données d’instance supplémentaires telles que le nom de l’instance, l’état, etc., sont requises. Pour récupérer des données d&#39;instance supplémentaires, l&#39;approche suivante doit être suivie :

#### Interrogation des informations à partir de public-api GET /learningobjects - portée d’administration

Les clients peuvent utiliser l&#39;API `GET /learningObjects` comme indiqué ci-dessus, ainsi que les instances incluses pour récupérer les informations sur les instances. Ils doivent toujours suivre l&#39;approche mentionnée dans la [section](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#query-the-information-from-the-public-api-get-learningobjects-admin-scope) pour s&#39;assurer que les limites de taux ne sont pas dépassées.


>[!NOTE]
>
>1. Les certifications n’ont pas le concept d’instances dans ALM.
>2. Il n&#39;est pas nécessaire de récupérer des données supplémentaires pour CI_STATS, car les mêmes informations auraient déjà été récupérées dans le cadre des événements d&#39;instance d&#39;objet d&#39;apprentissage.

### Création d&#39;une base de données à partir d&#39;événements d&#39;inscription, de désinscription, d&#39;achèvement et de progression

L’inscription, la désinscription, l’achèvement et la progression des élèves sont émis sous la forme d’événements distincts dans Adobe Learning Manager. L&#39;élève est identifié par l&#39;attribut `userId`. Cependant, il peut exister certains scénarios dans lesquels des informations supplémentaires sur l’élève, telles que le nom, l’adresse e-mail, etc., sont requises pour les workflows en aval du côté client. Pour récupérer ces données, les clients peuvent suivre l’approche décrite ci-dessous :

#### Exporter le rapport d’utilisateur à partir de l’administrateur ou des connecteurs

Cette approche doit être suivie chaque fois que des workflows en bloc sont impliqués, tels que l’inscription en bloc, la désinscription en bloc, etc. Le rapport d’utilisateur de Adobe Learning Manager contient toutes les informations relatives à un utilisateur. En corrélant le `userId` obtenu à partir de l’événement webhook, les clients peuvent consulter ce rapport (qui peut être exposé côté client en tant que point de terminaison de base de données, de cache ou d’API) pour récupérer des détails supplémentaires tels que le nom, l’adresse e-mail, l’UUID, etc. Cette approche peut être utilisée pour synchroniser les utilisateurs sur une base hebdomadaire ou quotidienne.

#### Requête d’informations à partir du GET d’API public /des utilisateurs - Portée d’administration

Cette approche peut être suivie lorsque les utilisateurs ne sont pas disponibles dans le rapport ci-dessus. La combinaison des approches 1 et 2 garantit que tous les utilisateurs existants qui ont été créés dans le passé peuvent être couverts par le **[!UICONTROL rapport d&#39;utilisateur]**, tandis que les utilisateurs nouvellement créés peuvent toujours être récupérés à partir de l&#39;API. Si le **[!UICONTROL Rapport d&#39;utilisateur]** ne dispose pas des données, le client peut envoyer les ID utilisateur en tant qu&#39;arguments d&#39;entrée à l&#39;API `GET /users` pour récupérer les informations utilisateur. Ces informations doivent être mises en cache du côté client pour éviter des appels répétés de l’API publique pour le même ensemble d’utilisateurs. Veuillez noter que les limites de taux d’administration sont actuellement définies sur 500 demandes par heure pour les API GET /users. Toute demande dépassant cette limite entraînera une réponse **HTTP 429 Trop de demandes**.

## Tolérance aux pannes

La tolérance aux pannes du système de webhook ALM fournit des recommandations aux abonnés pour gérer les problèmes potentiels, tels que la perte d’événements, les événements en double et la remise en panne.

Le délai d’expiration de la connexion ALM est configuré sur 10 secondes et celui du socket sur 5 secondes. On s&#39;attend à ce que le client accuse réception du message dès qu&#39;il le reçoit. Cela permet de s&#39;assurer que le client n&#39;accuse pas de retard lors du traitement des messages. Dans le cas où un traitement en aval prend du temps, le client doit toujours accuser réception de l’événement instantanément, puis gérer le traitement en aval à sa fin.

### Conservation des données

Les événements sont conservés pendant 7 jours. Si elles ne sont pas traitées dans ce délai, elles sont définitivement perdues. Si la récupération a lieu le dernier jour et qu’un délai supplémentaire est nécessaire, le système ne prolonge pas la période de rétention.
Si des événements sont produits plus rapidement qu’ils ne sont consommés, certains événements peuvent être perdus. Bien que cela soit rare, les abonnés doivent surveiller pour éviter que cela ne devienne un problème à long terme.

### Webhooks désactivés

Lorsqu’un abonné ne répond pas aux événements de webhook, le système ALM tente à nouveau de créer des webhooks à l’aide d’une annulation exponentielle pour éviter de submerger l’abonné.

Le processus de nouvelle tentative démarre avec un intervalle initial de 5 secondes. Si l&#39;abonné ne répond pas, le temps d&#39;attente double pour atteindre 10, 20, 40 et 80 secondes, et peut augmenter jusqu&#39;à un maximum de 5 minutes. Une fois qu&#39;il atteint 5 minutes, le système continuera à réessayer toutes les 5 minutes jusqu&#39;à la fin de la période de rétention de 7 jours. Si l’abonné ne répond toujours pas pendant toute cette période, le webhook est automatiquement désactivé. Un e-mail de rappel sera envoyé à l’abonné à intervalles réguliers.

### Duplication d’événements

Si un abonné met plus de 5 secondes à répondre après le traitement d&#39;un événement, le système peut essayer de traiter à nouveau le même événement. Il est recommandé d’utiliser des ID d’événement pour suivre les événements déjà traités. En outre, si le webhook se bloque après l’envoi de l’événement mais avant l’enregistrement de son traitement, le même groupe d’événements peut être retenté. Il est recommandé d’utiliser des ID de lot ou des ID d’événement individuels pour reconnaître et ignorer les doublons.

### Recommandation pour la tolérance aux pannes

Pour éviter ces erreurs, les abonnés doivent surveiller activement les événements de webhook et configurer des alertes pour les problèmes tels que les événements manqués, les livraisons en double ou les séquences désordonnées.

## Consignes spécifiques aux événements de webhook

1. Si vous obtenez d’abord un événement LEARNER_PROGRESS, ignorez ensuite les événements répertoriés ci-dessous :

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEARNING_PATH_ENROLLMENT
   * LEARNING_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Ignorez l’événement LEARNER_PROGRESS s’il survient après les événements suivants :

   * COURSE_COMPLETED
   * COURSE_COMPLETED_BATCH
   * LEARNING_PATH_COMPLETED
   * LEARNING_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Utilisez le champ d’horodatage pour déterminer s’il faut ignorer ou traiter l’événement, à l’exception de l’événement LEARNER_PROGRESS.

## Webhooks Événements bonnes pratiques de consommation

* La solution de webhook est utilisée pour gérer les systèmes à haut débit où la vitesse et une faible latence sont essentielles. Par conséquent, le client doit s&#39;assurer que l&#39;événement est accusé de réception dès sa réception. Même si un traitement supplémentaire est nécessaire du côté du client (tel que la récupération de données à partir de rapports, de l&#39;API ou l&#39;exécution d&#39;autres actions), l&#39;accusé de réception doit être envoyé dès la réception de l&#39;événement, et il appartient au client de traiter l&#39;événement ultérieurement.
* Ne pas accuser réception de l’événement dès que possible pourrait avoir un impact sur la nature en temps réel des événements, car les événements suivants ne seront émis qu’une fois l’accusé de réception précédent reçu.
* Les clients peuvent répondre avec un code d&#39;état HTTP 202 Accepté pour confirmer que l&#39;événement a été accepté.

## Limitations

* Les assistances à la tâche ne sont pas prises en compte pour les événements Webhook dans la catégorie des objets d’apprentissage, car elles sont généralement utilisées pour aider les élèves à terminer d’autres objets d’apprentissage.
* Un retrait d’instance d’objet d’apprentissage sera considéré comme un événement de mise à jour. Il n&#39;y aurait pas d&#39;événement de suppression pour une instance, car elle ne peut être retirée que, et non supprimée.
* Les modifications de session seront capturées dans le cadre de l’événement de mise à jour de l’instance. Cela s’applique uniquement aux cours. Il n’y aura pas de propagation ascendante à partir des entités de niveau inférieur pour les instances de parcours d’apprentissage ou de certification.
* Si un parcours d’apprentissage contient un cours et qu’un élève termine le cours via le parcours d’apprentissage, deux événements **LearnerProgress** sont générés : un pour le cours et un pour le parcours d’apprentissage.
* Certains workflows calculent les attributs des objets d’apprentissage, tels que la durée et le type de livraison, de manière asynchrone. Par conséquent, les événements pour ces objets d’apprentissage seront générés une fois le traitement de la tâche cron terminé.
* Si un cours est inscrit par le biais d’un programme d’apprentissage ou d’une certification parent, les événements d’inscription, de désinscription et d’achèvement se déclencheront uniquement pour le programme d’apprentissage ou la certification parent. Ces événements ne se déclenchent pas pour le cours enfant, car l’inscription s’est produite indirectement.
* Les webhooks ne sont pris en charge que pour les comptes avec le statut **[!UICONTROL ACTIF]**. Ils ne sont pas disponibles pour les comptes **[!UICONTROL VERSION D&#39;ESSAI]** ou **[!UICONTROL INACTIFS]**.

## Exemples de charges pour les événements

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345-0458-4450-b5dd-6bc1ef4f8b50",
      "eventName": "CI_STATS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456785-LoSt",
      "data": {
        "loInstanceId": "course:12345678_14448475",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345c1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c2345c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12345823000-040363-12018-0",
      "data": {
        "userId": 11080928,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c23458c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
    ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234567",
        "loInstanceId": "learningProgram:1234567_109139",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12340791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234557",
        "loInstanceId": "learningProgram:1234557_109139",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123404e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12344e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234e776-148e-4128-80e9-b896a460b655",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12344672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123472ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234524713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:123456798",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123454768000-040654-756257-0",
      "data": {
        "userId": 123456728,
        "loId": "certification:123418",
        "loInstanceId": "certification:134518_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123453bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "d1234d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12380928,
        "loInstanceId": "course:7232090_10423047",
        "dateStarted": "2024-11-08T03:49:52.000Z",
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3237817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1345506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f2317817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "17235506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "823df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e23f878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7232766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235507900000-040304-1065-0",
      "data": {
        "userId": 12311591,
        "loId": "certification:123199",
        "loInstanceId": "certification:123199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7202766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1735507900000-040304-1065-0",
      "data": {
        "userId": 12511591,
        "loId": "certification:139199",
        "loInstanceId": "certification:139199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345da9f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234519188000-040344-48604-0",
      "data": {
        "loId": "course:1234091",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234a690-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605296000-040656-662792-0",
      "data": {
        "loId": "course:12319716",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "223e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "1234e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1231da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12d16e90-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605491000-040657-236307-0",
      "data": {
        "loInstanceId": "course:12319674_14453849",
        "loId": "course:12319674",
        "loType": "course"
      }
    }
  ]
}
```

+++
