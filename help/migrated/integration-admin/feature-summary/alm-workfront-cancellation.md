---
description: Découvrez comment annuler et réactiver des sessions ILT et VILT dans Adobe Learning Manager en définissant l’état de la session dans les données de migration de Workfront
jcr-language: en_us
title: Annulation d’ALM Workfront
exl-id: 01500cf2-6e39-4ac3-84e2-823a5215f6cf
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '2112'
ht-degree: 1%
---

# Déclencheur d’annulation/de mise à jour ALM-Workfront

## Présentation

Adobe Learning Manager (Learning Manager) peut désormais annuler et réactiver les sessions dirigées par un instructeur et les sessions virtuelles dirigées par un instructeur (ILT/VILT) en fonction des modifications apportées dans Workfront. Si votre organisation planifie des sessions dans Workfront et les importe dans Learning Manager via la migration de Workfront à Learning Manager, vous pouvez définir l’état de chaque session sur Actif ou Annulé dans les données de migration. Learning Manager applique ensuite la modification comme si un administrateur avait annulé la session dans l’interface utilisateur.

L’annulation d’une session via la migration revient à l’annuler depuis l’interface utilisateur de Learning Manager. La seule différence délibérée est la réactivation, décrite dans [Réactiver une session annulée](#reactivate-a-cancelled-session).

### L’exigence

Les mises à jour d’une session, telles que la date et l’heure, l’instructeur, le lieu ou le lien et la capacité, passent déjà de Workfront à Learning Manager via la migration. Les annulations n’ont pas eu lieu. Lorsqu’une session était annulée dans Workfront, Learning Manager n’avait aucun moyen de le savoir, ce qui entraînait les problèmes suivants :

* Les élèves sont restés inscrits à une session qui ne s&#39;exécutait plus, ce qui a entraîné de la confusion et l&#39;absence d&#39;affichage.
* Les administrateurs devaient répéter l’annulation manuellement dans Learning Manager.
* Workfront et Learning Manager ne sont plus synchronisés, ce qui a sapé Workfront en tant que source fiable de planification.

### Fonctionnement du logiciel

1. Un gestionnaire de diffusion annule une session dans Workfront.
1. La ligne de session dans les données de migration inclut la nouvelle colonne d’état de session, définie sur Annulé.
1. Un administrateur système exécute la migration via l’API.
1. Learning Manager marque la session correspondante comme annulée et envoie les mêmes notifications qu’une annulation à partir de l’interface utilisateur.

>[!NOTE]
>
>Cette fonctionnalité étend le processus de migration existant plutôt que d’ajouter un deuxième chemin d’intégration en temps réel.

### Workflow de bout en bout

Le diagramme suivant montre comment une ligne de session passe de Workfront à Learning Manager.

![Organigramme montrant une ligne de session Workfront en cours de migration pour créer, mettre à jour ou annuler le workflow d’état de session correspondant](assets/alm-workfront-cancellation-visual1.png "Workfront vers Learning Manager")

## Cas d’utilisation

Les rôles suivants sont impliqués dans une annulation qui commence dans Workfront.

### Rôles impliqués

| Rôle | Description |
|---|---|
| Responsable de prestation | Planifie et gère le calendrier de formation dans Workfront, y compris l’annulation des sessions. Les responsables de prestation n&#39;utilisent pas l&#39;interface utilisateur de Learning Manager. La migration est le seul chemin par lequel leur annulation atteint Learning Manager. |
| Administrateur système | Exécute la migration via l’API. Ce rôle gère le pipeline Workfront vers Learning Manager et est distinct du gestionnaire de diffusion et de l’administrateur Learning Manager. |
| Administrateur | Gère les données de cours et de session dans l&#39;interface utilisateur de Learning Manager. Les administrateurs n’ont plus besoin d’annuler les sessions manuellement après avoir été informés d’un changement dans Workfront. |
| Auteur | Possède le contenu du cours et de la session dans l&#39;interface utilisateur de Learning Manager. |
| L’instructeur | Est affecté aux sessions. Les instructeurs voient l’état de session correct et sont avertis lorsqu’une session qu’ils donnent des instructions est annulée. |
| Gestion | Est inscrit à une session via Learning Manager. Les élèves sont rapidement informés lorsque leur session est annulée. |

### Scénarios courants

| Scénario | Ce que vous faites | Résultat |
|---|---|---|
| Une session est annulée dans Workfront, par exemple parce qu’une ressource n’est pas disponible ou qu’un fournisseur rencontre un problème. | Définissez l’état de la session sur Annulé dans la ligne de migration de la session et exécutez la migration. | La session est annulée dans Learning Manager et les personnes concernées en sont informées. |
| Les détails d’une session active changent dans Workfront. | Incluez les valeurs modifiées dans la ligne de migration. Définissez l’état de la session sur Actif ou laissez-le vide. | La session est mise à jour. Learning Manager envoie un e-mail de mise à jour de session. |
| Une session annulée est rétablie dans Workfront. | Définissez l’état de session sur Actif dans la ligne de migration et exécutez la migration. | La session devient active et peut être à nouveau modifiée et annulée. |
| Les détails mis à jour sont envoyés pour une session annulée sans définir l’état sur Actif. | Aucune action n’est requise de la part de l’utilisateur. | La session reste annulée, la ligne renvoie une erreur de validation et aucun détail n’est modifié. |
| Une ligne de migration n’inclut pas d’état de session. | Laissez la colonne vide ou omettez-la. | L’état actuel de la session dans Learning Manager reste inchangé. |

## Fonctionnalités clés

* **Colonne d&#39;état de session.** Le schéma de migration comprend un champ facultatif d’état de session qui prend en charge Actif et Annulé.
* **Annulation via la migration.** Lorsque l’état d’une ligne est Annulé, la session correspondante dans Learning Manager est annulée. Learning Manager utilise la même clé de correspondance que celle déjà utilisée par la migration pour créer et mettre à jour les sessions.
* **Aucun travail manuel dans Learning Manager.** Les administrateurs n’ont pas besoin d’annuler à nouveau la session dans l’interface utilisateur.
* **Même comportement que l&#39;annulation dans l&#39;interface utilisateur.** La gestion de l’inscription, la visibilité destinée aux élèves, les rapports, le journal d’audit et les notifications correspondent à une annulation à partir de l’interface utilisateur.
* **Réactivation.** Vous pouvez redéfinir une session annulée sur Actif en définissant l’état explicitement dans les données de migration.
* **Protection pour les sessions annulées.** La migration ne modifie pas les détails d’une session annulée, sauf si la ligne définit explicitement l’état sur Actif.
* **Rétrocompatibilité.** La colonne d’état est facultative, de sorte que les fichiers de migration existants continuent de fonctionner sans modifications.
* **Notifications complètes.** Les élèves, les instructeurs, les administrateurs, les auteurs et les responsables reçoivent les mêmes e-mails d’annulation qu’ils reçoivent pour une annulation à partir de l’interface utilisateur.

## États de session

Chaque session de Learning Manager présente l’un des deux états suivants :

| État | Signification |
|---|---|
| Actif | État par défaut. La session est en direct et les élèves peuvent s’y inscrire et y assister. |
| Annulé | La session est annulée. Les élèves inscrits, les administrateurs, les auteurs et les responsables sont informés, car ils font l’objet d’une annulation à partir de l’interface utilisateur. |

### Règles de transition des États pour la migration

Le tableau suivant indique ce qui se passe lorsqu&#39;une ligne de migration est traitée. Learning Manager identifie la session à l’aide de la clé correspondante que la migration utilise déjà pour la création et la mise à jour.

| État actuel dans Learning Manager | État de la session dans la ligne de migration | Résultat |
|---|---|---|
| La session n&#39;existe pas | Actif ou vide | La session est créée comme active. |
| Actif | Actif ou vide | La session reste active. Les valeurs modifiées dans la ligne sont appliquées. |
| Actif | Annulé | La session est annulée et des notifications sont envoyées. |
| Annulé | Annulé | La ligne est ignorée. Une session annulée ne peut plus être annulée. |
| Annulé | Actif | La session est réactivée. Les valeurs modifiées dans la ligne sont appliquées. |
| Annulé | Vide | La session reste annulée. Si la ligne a des valeurs modifiées, une erreur de validation est renvoyée et aucun détail n&#39;est modifié. |

### Règles pour la colonne d&#39;état de session

* La colonne est facultative sur chaque ligne.
* Lorsque la colonne est vide, la session passe à Active.
* Une session redevient active via la migration uniquement lorsque la colonne indique explicitement Actif.

Utilisez l’une des valeurs suivantes dans la colonne d’état de session :

* `state = Active`
* `state = Cancelled`

>[!NOTE]
>
>L’en-tête de colonne exact et les valeurs acceptées sont en cours de confirmation. Utilisez les noms spécifiés dans votre documentation de migration.

## Mises à jour des sessions annulées

Vous ne pouvez pas mettre à jour les détails d’une session annulée via la migration. Si une ligne d’une session annulée contient des valeurs modifiées et ne définit pas l’état sur Actif, Learning Manager renvoie une erreur de validation, laisse la session annulée et n’applique ni ne stocke les détails modifiés. Learning Manager n’envoie pas d’e-mail de session mise à jour pour la tentative.

### Annulation d’une session à l’aide de la migration

Utilisez cette procédure lorsqu’une session a été annulée dans Workfront et que vous souhaitez que Learning Manager reflète cette modification.

**Avant de commencer**

* La session existe déjà dans Learning Manager, importée via la migration de Workfront vers Learning Manager.
* Vous connaissez la clé correspondante utilisée par votre migration pour identifier la session.

1. Dans **Workfront**, annulez la session.
1. Dans le fichier CSV de session que vous utilisez pour la migration, recherchez la ligne de la session. Assurez-vous que la clé correspondante est la même que celle utilisée lors de la création de la session.
1. Dans la colonne État de la session, saisissez **Annulé**.
1. Exécutez la migration via l’API.
1. Dans Learning Manager, vérifiez que la session est annulée.

Learning Manager marque la session comme annulée, traite les élèves inscrits comme il le fait pour une annulation à partir de l’interface utilisateur et envoie les notifications d’annulation. Aucune action n’est requise dans l’interface utilisateur de Learning Manager.

>[!NOTE]
>
>Si la session est déjà annulée, Learning Manager ignore la ligne.

### Mise à jour d’une session active

Pour une session active, le comportement de mise à jour de migration existant reste disponible. Définissez l’état de la session sur Actif ou laissez-le vide et incluez les valeurs modifiées dans la ligne. Vous pouvez continuer à mettre à jour des détails tels que la date et l’heure, l’instructeur, l’emplacement ou le lien et la capacité via le pipeline de migration.

Actif conserve le comportement de création et de mise à jour existant. Annulé appelle la même annulation de session que celle fournie par l’interface utilisateur, via la migration CSV de session.

### Réactiver une session annulée

Une session annulée revient à l’état actif uniquement lorsque vous définissez explicitement l’état sur Actif. Vous pouvez réactiver une session via la migration ou en la modifiant dans l’interface utilisateur.

1. Dans le fichier CSV de la session, recherchez la ligne correspondant à la session annulée. Assurez-vous que la clé correspondante est la même que celle utilisée lors de la création de la session.
1. Dans la colonne État de session, saisissez Actif.
1. (Facultatif) Mettez à jour toutes les autres valeurs de la ligne que vous souhaitez modifier, telles que la date et l’heure, l’instructeur, l’emplacement, le lien ou la capacité.
1. Exécutez la migration via l’API.

La session devient active et ses détails peuvent être modifiés. Une session qui est réactivée par le biais de la migration ou de l’interface utilisateur peut être annulée à nouveau par l’un ou l’autre chemin.

>[!IMPORTANT]
>
>Si vous envoyez les détails d’une session mise à jour pour une session annulée sans définir l’état sur Actif, la session reste annulée et la ligne renvoie une erreur de validation.

## Notifications

Learning Manager envoie chaque e-mail qu’il envoie en cas d’annulation à partir de l’interface utilisateur lorsqu’une session est annulée via la migration. La couverture du destinataire n’est pas réduite et le contenu utilise le même modèle. Les destinataires ne peuvent donc pas savoir comment l’annulation a commencé.

Les destinataires, en fonction de la session, sont les suivants :

| Destinataire | Notification |
|---|---|
| Élèves | Les élèves inscrits à la session sont informés que la session est annulée. |
| Instructeurs | Les instructeurs affectés à la session sont informés de l’annulation. |
| Responsables | Les responsables reçoivent la notification d’annulation. |

### E-mails pour les sessions annulées

Une session annulée ne génère pas d’e-mails de mise à jour de session. Lorsqu’une session est annulée, les modifications apportées à la date et à l’heure, à l’instructeur, à l’emplacement ou au lien et à la capacité ne déclenchent pas l’e-mail mis à jour dans la session. Seules les notifications d’annulation et de réactivation s’appliquent à une session annulée.

## Considérations et limitations

* Étant donné que la fonctionnalité utilise la migration, une annulation effectuée dans Workfront atteint Learning Manager lorsque la migration s’exécute. L’annulation en temps réel basée sur un webhook n’est pas prise en charge.
* La migration ne peut pas modifier les détails d’une session annulée. Pour les modifier, définissez d’abord l’état sur Actif.
* La colonne d&#39;état de session est facultative. Les lignes qui l’omettent ne modifient jamais l’état d’une session.
* La fonctionnalité étend l’intégration de la migration existante. Il n’ajoute pas de deuxième chemin d’intégration en temps réel.
* Le calendrier ou le déclencheur de migration dépend de l’outil utilisé par votre entreprise pour l’exécuter. Ce guide ne définit pas de calendrier fixe.
* Les responsables de prestation travaillent uniquement dans Workfront. Ils n’ont pas besoin d’accéder à l’interface utilisateur de Learning Manager pour annuler une session.

## Mesures de succès

| Mesure | Target |
|---|---|
| Annulations que les administrateurs ou le service clientèle répliquent manuellement | Réduit à 0 dans un cycle de publication complet après le lancement. |
| Annulations de Workfront reflétées dans Learning Manager | 100 % des événements d’annulation traités au cours d’un cycle de migration. |
| Parité des notifications entre l’interface utilisateur et les annulations de migration | 0 écart dans la couverture des destinataires (administrateurs, auteurs, responsables et élèves) et 0 e-mail de mise à jour inutile pour les sessions annulées. |

## Dépannage

| Problème | Cause attendue ou possible | Action |
|---|---|---|
| Une session reste active après son annulation dans Workfront. | La migration n&#39;a pas encore traité l&#39;annulation ou la ligne de migration ne portait pas l&#39;état Annulé explicite. | Vérifiez l’entrée de migration et le résultat du traitement. |
| Les détails d’une session annulée ne changent pas. | Comportement attendu tant que la session reste annulée. | Réactivez la session en définissant l’état sur Actif, puis appliquez les modifications. |
| Aucun e-mail de session mise à jour n’est envoyé pour une session annulée. | Comportement attendu. Les e-mails de mise à jour ordinaires sont supprimés pour les sessions annulées. | Utilisez le cycle de vie d’annulation et de réactivation au lieu d’une mise à jour détaillée uniquement. |
| Une ligne d&#39;annulation est ignorée. | La session de correspondance dans Learning Manager est déjà annulée. | Aucune autre annulation n’est nécessaire. Réactivez d’abord la session si elle doit revenir à l’état actif. |
| Un destinataire a reçu le même e-mail d’annulation que pour une annulation d’interface utilisateur. | Comportement attendu. L’annulation de la migration est conçue pour correspondre à l’interface utilisateur. | Aucune action n’est requise. |
| Le comportement n’est pas clair lorsque l’état de la session est vide. | Les exigences de la source sont en conflit avec la gestion des états vides. | Confirmez le comportement de libération avant de vous fier à un état vide pour toute transition. |
