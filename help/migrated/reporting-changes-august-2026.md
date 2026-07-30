---
description: Ce document résume les modifications apportées aux rapports d’août 2026 dans Adobe Learning Manager. Elle couvre les colonnes nouvelles et mises à jour du relevé de notes de l'élève, de la formation, de l'inscription, de la liste d'attente, de la présence, de l'audit de contenu et des rapports utilisateur. Il explique également le comportement adaptatif du cours, la notation des classeurs, les enregistrements d’apprentissage externes, les rapports de crédit d’IA générale, le suivi de la certification racine, la normalisation des horodatages et les mises à jour des auteurs d’API.
jcr-language: en_us
title: Rapports sur les modifications de la version d’août 2026 de Adobe Learning Manager
source-git-commit: 5c32d300f6e66e154a5c993a0d9701254ac8b4ce
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 2%

---


# Rapports sur les modifications de la version d’août 2026 de Adobe Learning Manager

La version d’août 2026 de Adobe Learning Manager introduit des améliorations en matière de création de rapports dans les classeurs, l’apprentissage externe, l’utilisation des crédits Gen AI, etc. Cet article résume les nouvelles colonnes, les nouveaux rapports et les changements de comportement disponibles pour les administrateurs dans cette version.

## Quels sont les changements apportés

Les mises à jour des rapports couvrent huit domaines de fonctionnalités : notation du journal de notes, apprentissage externe, exportations incrémentielles d’utilisateurs, utilisation des crédits d’IA générative, suivi de la certification racine et alignement de l’horodatage du webhook. Les modifications concernent principalement les rapports suivants :

- Relevé de notes de l’élève (LT)
- Rapport des formations
- Rapport d’inscription
- Rapport de liste d’attente
- Rapport d’audit de contenu

La plupart des mises à jour introduisent de nouvelles colonnes. Certains ont introduit de nouveaux types de rapports. Quelques-uns ont modifié la façon dont les données existantes sont modélisées ou formatées.

<!--
## Adaptive course reporting changes

### Training report

Three new columns in the Training report support adaptive course behavior.

| **Column**               | **Description**                                          | **Supported Values**                                                   |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------|
| Adaptive Learning Object | Identifies whether a course is adaptive                  | true (adaptive), false (non-adaptive)                                  |
| Visibility User Groups   | Lists user groups that can view each module              | One or more user group names (for example, All Learners, UG-Australia) |
| Mandatory                | Indicates whether a module is mandatory for a user group | User group names for which the module is mandatory; blank = optional   |

You can combine **Visibility User Groups** and **Mandatory** to interpret adaptive completion rules directly in the report. For example, a module may be visible to **All Learners** but mandatory only for the **Administrator group**.


### Learner Transcript

A new **Previous Completions** column captures historical completion data when adaptive logic triggers recompletion.

| **Sub-field**         | **Description**                         |
|-----------------------|-----------------------------------------|
| completionRefreshDate | Timestamp when the completion was reset |
| completedDate         | Previous completion timestamp           |
| progressAtRefresh     | Learner progress before reset           |
| gradeAtRefresh        | Learner score at the time of reset      |

The Learner Transcript now supports multiple completion cycles. When a recompletion event occurs, for example, due to course updates or new mandatory modules, the previous completion moves to the **Previous Completions** column. The current completion remains in the standard transcript fields.

### Enrollment report

A new **Waitlisted** column indicates whether a learner is waitlisted in any module within a course.

| **Value** | **Meaning**                                             |
|-----------|---------------------------------------------------------|
| true      | The learner is waitlisted in one or more modules        |
| false     | Learner has confirmed enrollment in all visible modules |

### Waitlist report

Two new columns and an enhanced status-detail support module enable waitlist tracking at the module level.

| **Column**      | **Description**                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Module**      | Name of the module (classroom or virtual classroom session) where the learner is waitlisted. Appears after the Instance Status column. |
| **Module ID**   | Identifier of the module where the learner is waitlisted. Appears after the Module column.                                             |
| **Embedded In** | The learning path name and ID of any learning path that contains this course. Blank if the course is not part of a learning path.      |

The Waitlist report has shifted from a course-level model to a module session–level model. A learner can now be enrolled in some modules and waitlisted in others. The report also supports waitlist tracking within Flex learning paths, where seat limits are enforced at the module level.

### LP Enrollment report

The Learning Path Enrollment report also receives a new **Remarks** column. When a learner is in a waitlisted state on any classroom or virtual classroom session within the courses that make up the learning path, the Remarks column shows **Waitlisted**. When all sessions are confirmed, the column is blank.

### Attendance report

The **Learner status** column now distinguishes between confirmed and waitlisted learners.

| **Value**  | **Meaning**                            |
|------------|----------------------------------------|
| Confirmed  | The learner has an allocated seat      |
| Waitlisted | The learner is pending seat allocation |

-->

## Modifications apportées aux rapports de l’annuaire de notes

### Relevé de notes de l&#39;élève

Une nouvelle colonne **Poids** représente la contribution de chaque module pouvant être noté au score global du cours.

| **Valeur** | **Description** |
|----------------------------------------------|------------------------------------------------------|
| Pourcentage numérique (par exemple, 20, 30, 50) | Contribution du module au score du cours |
| Vide | Le module n’est pas marquable (par exemple, PDF ou vidéos) |

### Rapport d’audit de contenu

Deux nouveaux événements capturent les modifications de configuration du journal de notes.

| **Événement** | **Déclenché lorsque** | **Données capturées** |
|-----------------------|-----------------------------------------------------------------|----------------------------------------------------------|
| Classeur mis à jour | L’annuaire est activé, désactivé ou modifié au niveau du cours | Modification de l&#39;état du classeur ; mises à jour de la configuration du classement |
| Poids du module mis à jour | Le poids attribué à un module est modifié | Identifiant du module ; valeur de pondération mise à jour |

Le relevé de notes de l’élève reflète la dernière pondération. Le rapport d’audit de contenu effectue le suivi des modifications historiques. Ensemble, ils vous donnent une image complète de la logique de notation actuelle et de son évolution.

## Modifications des rapports d’apprentissage externe

### Relevé de notes de l&#39;élève

Trois nouvelles colonnes sont ajoutées pour prendre en charge les enregistrements d’apprentissage externes.

| **Colonne** | **Description** |
|------------------------|-----------------------------------------------------------------------------------------------------|
| Nom de l’apprentissage externe | Nom de l’activité d’apprentissage externe soumise par l’élève |
| Champs personnalisés | Une colonne par champ personnalisé configuré pour l’apprentissage externe (texte, numérique, case à cocher ou liste déroulante) |
| Commentaire d’achèvement | Remarques du responsable saisies lors de l&#39;approbation ou du rejet |

**Remarque :** dans le relevé de notes de l&#39;élève (vue libre-service de l&#39;élève), l&#39;emplacement des colonnes diffère de celui du relevé de notes de l&#39;élève administrateur :

- **Nom de l&#39;apprentissage externe** est ajouté immédiatement après la colonne **Module** existante.

- **Le commentaire d&#39;achèvement** est ajouté immédiatement après la colonne **Remarques du réviseur** existante.

- Les colonnes de champ personnalisé (une par champ personnalisé configuré) sont ajoutées à la fin du relevé de notes.

Dans le relevé de notes de l’élève administrateur, toutes les nouvelles colonnes, y compris Nom de l’apprentissage externe et Commentaire d’achèvement, sont ajoutées à la fin, suivies des colonnes de champs personnalisés.

### Colonne Type dans le relevé de notes de l’élève

Les entrées d’apprentissage externe apparaissent désormais à côté des objets d’apprentissage existants (cours, parcours d’apprentissage, certifications) dans Administrator LT. La colonne **Type** inclut une nouvelle classification d&#39;apprentissage externe pour un filtrage facile.

Les données d’apprentissage externes sont transférées à la fois dans le relevé de notes de l’élève et dans Admin LT. Les champs de base tels que la date d&#39;achèvement, l&#39;état et le score sont mappés aux colonnes existantes. Les champs personnalisés sont ajoutés en tant que colonnes supplémentaires.

## Modifications incrémentielles du rapport utilisateur

Un nouveau modèle d’exportation incrémentielle vous permet d’exporter uniquement les utilisateurs dont les données ont été modifiées au cours d’une période donnée, au lieu de générer des exportations de données complètes à chaque fois.

| **Mode d&#39;exportation** | **Comportement** |
|--------------------|-----------------------------------------------------------------|
| Exportation complète | Retourne tous les utilisateurs du compte |
| Exportation incrémentielle | Retourne uniquement les utilisateurs avec des modifications dans la plage de dates spécifiée |

Pour utiliser l&#39;exportation incrémentielle, filtrez par **à partir de la date** et **à la date** pour définir la fenêtre de modification. Les rapports des utilisateurs sont désormais générés à l’aide d’un pipeline de plateforme de données, et la sortie est retournée par blocs pour prendre en charge les comptes volumineux.

## Rapports de crédit Gen AI

Un nouveau tableau de bord de crédit et deux rapports offrent aux administrateurs une visibilité sur la consommation de crédit Gen AI.

### Tableau de bord des crédits

Le tableau de bord présente les mesures suivantes au niveau du compte.

| **Métrique** | **Description** |
|-------------------|---------------------------------------------------|
| Crédits achetés | Total des crédits provisionnés pour le compte |
| Crédits utilisés | Crédits consommés via les fonctionnalités optimisées par l’IA |
| Crédits restants | Crédits disponibles après consommation |
| Utilisation par fonctionnalité | Consommation de crédit divisée par fonction d’IA individuelle |

### Nouveaux rapports

| **Rapport** | **Description** |
|----------------------|---------------------------------------------------------------------------------------------|
| Rapport d’utilisation mensuel | Résume la consommation de crédits par mois, fonction et crédits consommés |
| Rapport de journal d’audit | Fournit des détails au niveau de l’utilisateur : identifiant utilisateur, nom de la fonctionnalité, crédits consommés et horodatage |

## Autres changements comportementaux

### Certification racine : ID de formation racine

Une nouvelle colonne **ID de formation racine** est ajoutée à la fin du **relevé de notes de l’élève administrateur** et du **relevé de notes de l’élève** (vue en libre-service de l’élève). Il capture l&#39;identifiant unique qui lie toutes les récurrences d&#39;une certification à une seule entité racine. Cela permet d&#39;associer toutes les instances récurrentes d&#39;une certification à un seul ID racine pour le suivi et le filtrage.

### Normalisation de l’horodatage du webhook et du relevé de notes de l’élève

Les horodatages des webhooks sont désormais alignés sur le formatage du relevé de notes de l’élève. La valeur en secondes de chaque champ de date et d’heure de l’**objet de données** d’une payload de webhook est désormais définie sur 00, ce qui fournit une granularité de niveau minute cohérente avec les rapports de relevé de notes de l’élève. Cela élimine le besoin de normaliser les formats d’horodatage lors de la comparaison des données de webhook avec les données du relevé de notes de l’élève.

### Informations sur l’auteur dans la réponse de l’API pour les cours partagés

Lorsqu&#39;un cours est partagé d&#39;un compte Adobe Learning Manager à un autre via le partage de catalogue, la réponse de l&#39;objet d&#39;apprentissage (LO) de l&#39;API renvoie désormais uniquement les détails de l&#39;auteur d&#39;origine à partir du compte source. Auparavant, l’administrateur du compte acceptant apparaissait comme auteur du cours dans la réponse de l’API pour son compte

Cette modification affecte uniquement les comptes d’homologues (de réception). Lorsque vous interrogez le point de terminaison détaillé LO pour un cours partagé dans un compte de réception, le champ authorNames reflète désormais l&#39;auteur d&#39;origine du compte source, et non l&#39;administrateur du compte de réception.

La façon dont les détails de l’auteur apparaissent lors de l’interrogation de l’objet d’apprentissage dans le compte source reste inchangée.

**Remarque :** si votre intégration repose sur le champ authorNames dans la réponse de l&#39;API LO pour les cours partagés, vérifiez que les données d&#39;auteur mises à jour ne rompent pas la logique en aval qui supposait que le nom d&#39;administrateur du compte destinataire apparaîtrait dans ce champ.
