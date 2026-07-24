---
jcr-language: en_us
title: Prise en main de Report Builder
description: Report Builder fournit 15 modèles préconfigurés en lecture seule pour les besoins courants de création de rapports sur les données d’apprentissage, avec des colonnes, des filtres, des regroupements et des tris déjà configurés. Vous pouvez prévisualiser ces modèles ou les dupliquer pour créer des versions modifiables.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '3332'
ht-degree: 1%

---


# Prise en main de Report Builder

## Présentation

Report Builder comprend 15 modèles préconfigurés conçus pour les cas d’utilisation de création de rapports de données d’apprentissage les plus courants. Chaque modèle est une configuration de rapport prête à l’emploi avec des colonnes, des filtres, des paramètres de regroupement et des tris déjà appliqués. Les modèles sont en lecture seule. Vous pouvez les prévisualiser ou les dupliquer pour créer une copie modifiable.

## À propos des modèles

Les modèles sont des configurations de rapport prêtes à l’emploi fournies par Adobe Learning Manager. Chaque modèle est conçu pour un cas d’utilisation spécifique, tel que le suivi des inscriptions et de l’achèvement, les rapports de conformité ou les performances des instructeurs. Les modèles apparaissent sous l&#39;onglet **Modèles** dans le Report Builder. Chaque modèle est construit à partir d’un ou plusieurs jeux de données et produit un type de sortie spécifique. Pour personnaliser un modèle, sélectionnez **Dupliquer** pour créer une copie modifiable dans votre onglet **Rapports** tout en laissant l&#39;original inchangé.

## Catalogue de modèles

### Relevé de notes de l’utilisateur

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** terminer l&#39;historique d&#39;apprentissage pour chaque élève, en indiquant toutes les inscriptions, les statuts, les scores, les échéances et le temps passé sur tous les types d&#39;objets d&#39;apprentissage.

**À utiliser lorsque :** vous avez besoin d&#39;une exportation complète de l&#39;activité de l&#39;élève prête pour l&#39;audit pour les audits de conformité, les cas de support de l&#39;élève ou l&#39;intégration des données ALM dans un système externe.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** utilisateur, objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, nom d’utilisateur, adresse e-mail de l’utilisateur, nom du responsable, statut de l’utilisateur, nom de l’objet d’apprentissage, type d’objet d’apprentissage, date d’inscription, date d’achèvement, état, pourcentage de progression, score le plus élevé de l’utilisateur, échéance de l’achèvement, retard, temps passé (minutes)

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut

### Résumé de la progression de l’élève

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** suit la progression de chaque élève par rapport aux parcours d’apprentissage et aux cours attribués, y compris le mappage de la hiérarchie via l’ID LO parent.

**À utiliser lorsque :** vous souhaitez voir où en est chaque élève dans un parcours d’apprentissage :* qui est en cours, qui est en retard et qui risque de manquer une échéance.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** utilisateur, objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, nom d’utilisateur, adresse e-mail de l’utilisateur, nom du responsable, ID de l’objet d’apprentissage, nom de l’objet d’apprentissage, type d’objet d’apprentissage, ID de l’objet d’apprentissage parent, date d’inscription, date d’échéance, état, pourcentage de progression, retard, date de début, date d’achèvement

**Filtres appliqués :** date d’inscription au cours de l’année précédente ; type d’objet d’apprentissage = parcours ou cours d’apprentissage ; catalogue = catalogue par défaut

### Tableau de bord des élèves actifs

**Catégorie :** Engagement des élèves et utilisation de la plateforme

**Description :** résumé mensuel de l&#39;engagement de la plateforme par élève, montrant les cours suivis, les terminaisons et le temps total passé.

**À utiliser quand :** vous souhaitez identifier vos élèves les plus et les moins engagés au cours de l’année écoulée et voir les tendances de l’engagement mois après mois.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** utilisateur, transcription (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, Nom d’utilisateur, Adresse e-mail de l’utilisateur, Nom du responsable, Statut de l’utilisateur, Date du dernier accès (mois), Cours uniques consultés, Inscriptions terminées, Temps total passé (minutes)

**Filtres appliqués :** date du dernier accès de l&#39;utilisateur au cours de l&#39;année précédente ; statut de l&#39;utilisateur = Actif ; catalogue = Catalogue par défaut

**Regrouper par :** champs utilisateur + mois de la date du dernier accès

**Agrégats :** nombre unique sur l&#39;ID d&#39;objet d&#39;apprentissage (cours uniques consultés), nombre si état = Terminé (inscriptions terminées), somme du temps passé (temps total passé)

### Rapport sur les élèves inactifs

**Catégorie :** Engagement des élèves et utilisation de la plateforme

**Description :** identifie les utilisateurs actifs sans accès à la plateforme au cours de l&#39;année écoulée, en indiquant leurs dernières dates d&#39;inscription et d&#39;achèvement.

**À utiliser lorsque :** vous devez rechercher des comptes dormants pour des campagnes de réengagement, des examens de licence ou un nettoyage de compte.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** utilisateur, transcription (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, Nom d’utilisateur, Adresse e-mail de l’utilisateur, Nom du responsable, Date de création de l’utilisateur, Date de dernier accès de l’utilisateur, Date de la dernière inscription, Date de la dernière fin

**Filtres appliqués :** date du dernier accès de l&#39;utilisateur NON comprise dans l&#39;année précédente ; statut de l&#39;utilisateur = Actif ; catalogue = Catalogue par défaut

**Regrouper par :** ID utilisateur, nom d’utilisateur, adresse e-mail de l’utilisateur, nom du responsable, date de création de l’utilisateur, date de dernier accès de l’utilisateur

**Agrégats :** max. à la date d&#39;inscription (date de la dernière inscription), max. à la date d&#39;achèvement (date de la dernière inscription)

### Adoption d’un nouvel élève

**Catégorie :** Engagement des élèves et utilisation de la plateforme

**Description :** assure le suivi de l&#39;engagement d&#39;intégration des utilisateurs créés l&#39;année dernière, par exemple, les premières inscriptions, les résultats et le nombre total de cours consultés.

**À utiliser lorsque :** vous souhaitez mesurer la vitesse à laquelle les nouveaux utilisateurs passent de la création du compte à leur première inscription et à l&#39;achèvement, une mesure de santé clé pour l&#39;intégration.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** utilisateur, transcription (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, Nom d’utilisateur, Adresse e-mail de l’utilisateur, Nom du responsable, Date de création de l’utilisateur, Date de dernier accès de l’utilisateur, Date de première inscription, Date de première fin, Nombre total de cours consultés, Cours terminés

**Filtres appliqués :** date de création de l&#39;utilisateur au cours de l&#39;année précédente ; statut de l&#39;utilisateur = Actif ; catalogue = Catalogue par défaut

>[!NOTE]
>
>Ce modèle utilise une jointure gauche entre les jeux de données Utilisateur et Transcription afin que les utilisateurs avec zéro inscription apparaissent toujours dans le rapport. Cela permet d’identifier les nouveaux utilisateurs qui n’ont pas encore commencé leur parcours d’apprentissage.

**Regrouper par :** ID utilisateur, nom d’utilisateur, adresse e-mail de l’utilisateur, nom du responsable, date de création de l’utilisateur, date de dernier accès de l’utilisateur

**Agrégats :** min à la date d&#39;inscription (première date d&#39;inscription), min à la date d&#39;achèvement (première date d&#39;achèvement), nombre unique sur l&#39;ID d&#39;objet d&#39;apprentissage (nombre total de cours consultés), nombre si le statut = Terminé (cours terminés)

### Apprentissage par groupe d’utilisateurs

**Catégorie :** Utilisateurs, groupes et structure de l’organisation

**Description :** compare les activités d&#39;apprentissage entre les segments de l&#39;organisation : élèves actifs, cours consultés, achèvements et temps passé par groupe.

**À utiliser lorsque :** vous souhaitez comparer l&#39;engagement entre les services, les fonctions ou tout groupe d&#39;utilisateurs sur le terrain actif.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** groupe d&#39;utilisateurs (champ actif), relevé de notes (objet d&#39;apprentissage)

**Colonnes clés :** ID de groupe d&#39;utilisateurs, Nom du groupe d&#39;utilisateurs, Nombre de membres, Élèves actifs, Nombre total de cours uniques consultés, Inscriptions terminées, Temps total passé (minutes)

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut ; nom du groupe d&#39;utilisateurs (champ actif) = profil (champ actif)

**Regrouper par :** ID de groupe d&#39;utilisateurs, nom de groupe d&#39;utilisateurs, nombre de membres

**Agrégats :** nombre unique sur l&#39;ID utilisateur (élèves actifs), nombre unique sur l&#39;ID d&#39;objet d&#39;apprentissage (nombre total de cours uniques consultés), nombre si état = Terminé (inscriptions terminées), somme du temps passé (temps total passé)

### Apprentissage par emplacement

**Catégorie :** Utilisateurs, groupes et structure de l’organisation

**Description :** compare les activités d&#39;apprentissage entre les emplacements géographiques : élèves actifs, cours suivis, achèvements et temps passé par emplacement.

**À utiliser lorsque :** vous devez évaluer la santé de l&#39;apprentissage entre les régions sans découpage manuel des données. Utile pour les organisations mondiales avec des élèves répartis géographiquement.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** groupe d&#39;utilisateurs (champ actif), relevé de notes (objet d&#39;apprentissage)

**Colonnes clés :** ID de groupe d&#39;utilisateurs, Nom du groupe d&#39;utilisateurs, Nombre de membres, Élèves actifs, Nombre total de cours uniques consultés, Inscriptions terminées, Temps total passé (minutes)

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut ; le nom du groupe d&#39;utilisateurs (champ actif) contient « Emplacement »

**Regrouper par :** ID de groupe d&#39;utilisateurs, nom de groupe d&#39;utilisateurs, nombre de membres

**Agrégats :** nombre unique sur l&#39;ID utilisateur (élèves actifs), nombre unique sur l&#39;ID d&#39;objet d&#39;apprentissage (nombre total de cours uniques consultés), nombre si état = Terminé (inscriptions terminées), somme du temps passé (temps total passé)

### Formation par le responsable

**Catégorie :** Utilisateurs, groupes et structure de l’organisation

**Description :** résume les performances d&#39;apprentissage de la hiérarchie d&#39;équipe complète de chaque responsable : élèves actifs, achèvements et temps passé.

**À utiliser lorsque :** vous souhaitez comparer l&#39;engagement de l&#39;équipe entre les responsables et identifier les équipes ayant un faible taux d&#39;achèvement ou un temps passé par rapport à la taille de l&#39;équipe.

**Publics concernés :** formation des employés, activation commerciale.

**Jeux de données utilisés :** groupe d’utilisateurs (équipe), transcription (objet d’apprentissage)

**Colonnes clés :** ID du responsable, nom du responsable, adresse e-mail du responsable, nombre de membres (équipe complète), élèves actifs, nombre total de cours uniques consultés, inscriptions terminées, temps total passé (minutes)

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut

**Regrouper par :** ID du propriétaire (ID du responsable), nom du propriétaire, adresse électronique du propriétaire, nombre de membres

**Agrégats :** nombre unique sur l&#39;ID utilisateur (élèves actifs), nombre unique sur l&#39;ID d&#39;objet d&#39;apprentissage (nombre total de cours uniques consultés), nombre si état = Terminé (inscriptions terminées), somme du temps passé (temps total passé)

>[!NOTE]
>
>Ce modèle utilise le jeu de données Groupe d’utilisateurs (équipe), qui capture la hiérarchie complète de l’équipe sous chaque responsable. Aucun filtre de groupe d’utilisateurs supplémentaire n’est nécessaire.

### Résumé de l’inscription

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** le nombre d&#39;inscriptions au niveau du cours réparties par statut - Terminé, En cours et Non commencé - pour chaque objet d&#39;apprentissage.

**À utiliser quand :** vous souhaitez obtenir un aperçu rapide de l&#39;entonnoir d&#39;inscription pour chaque cours : combien d&#39;élèves ont commencé, combien sont en cours et combien ont terminé.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** ID de l’objet d’apprentissage, nom de l’objet d’apprentissage, type d’objet d’apprentissage, état de l’objet d’apprentissage, nombre total d’élèves inscrits, inscriptions terminées, inscriptions en cours, inscriptions non commencées

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut

**Regrouper par :** ID, nom, type, état de l&#39;objet d&#39;apprentissage

**Agrégats :** nombre unique sur l&#39;ID utilisateur (nombre total d&#39;élèves inscrits), nombre si état = Terminé, nombre si état = En cours, nombre si état = Non commencé

### Analyse de la tendance des inscriptions

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** nombre d&#39;inscriptions et d&#39;achèvements d&#39;un mois sur l&#39;autre par objet d&#39;apprentissage, montrant comment la participation des élèves évolue au fil du temps.

**À utiliser lorsque :** vous souhaitez voir quand le nombre d&#39;inscriptions augmente et diminue pour chaque cours et si les inscriptions suivent le même mois.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** nom de l’objet d’apprentissage, type d’objet d’apprentissage, date d’inscription (mois), nombre total d’élèves inscrits, inscriptions terminées

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut

**Regrouper par :** nom de l&#39;objet d&#39;apprentissage, type d&#39;objet d&#39;apprentissage, mois de la date d&#39;inscription

**Agrégats :** nombre unique sur l&#39;ID utilisateur (nombre total d&#39;élèves inscrits), nombre si état = Terminé (inscriptions terminées)

### Rapport d’achèvement du cours

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** répartition de l&#39;achèvement par cours avec nombre d&#39;états, date de la dernière fin, progression moyenne et temps moyen passé.

**À utiliser lorsque :** vous souhaitez identifier un contenu peu performant : des cours avec une inscription élevée mais une faible achèvement, ou des cours où la progression moyenne est faible (indiquant une baisse précoce).

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** ID de l’objet d’apprentissage, nom de l’objet d’apprentissage, type d’objet d’apprentissage, état de l’objet d’apprentissage, nombre total d’élèves inscrits, inscriptions terminées, inscriptions en cours, inscriptions non commencées, date de la dernière fin, pourcentage moyen de progression, temps moyen passé (minutes)

**Filtres appliqués :** date d&#39;inscription au cours de l&#39;année précédente ; catalogue = catalogue par défaut

**Regrouper par :** ID, nom, type, état de l&#39;objet d&#39;apprentissage

**Agrégats :** Nombre unique sur l&#39;ID utilisateur, Nombre si état = Terminé/En cours/Non commencé, Max. à la date d&#39;achèvement, Moyenne sur le pourcentage de progression, Moyenne sur le temps passé

### Tableau de bord Tendance d&#39;achèvement

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** le nombre d&#39;achèvements mensuels par objet d&#39;apprentissage, avec le temps moyen passé et la progression, s&#39;étend uniquement aux inscriptions terminées.

**À utiliser lorsque :** vous souhaitez suivre l&#39;évolution des taux d&#39;achèvement mois après mois et savoir si les élèves qui terminent le cours le font minutieusement ou à la hâte.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** nom de l’objet d’apprentissage, type d’objet d’apprentissage, date d’achèvement (mois), nombre total d’élèves terminés, temps moyen passé (minutes), progression moyenne %

**Filtres appliqués :** date d&#39;achèvement au cours de l&#39;année dernière ; état = Terminé ; catalogue = Catalogue par défaut

**Regrouper par :** nom de l’objet d’apprentissage, type d’objet d’apprentissage, mois de la date d’achèvement

**Agrégats :** décompte unique sur l&#39;ID utilisateur (nombre total d&#39;élèves terminés), moyenne sur le temps passé, moyenne sur le pourcentage de progression

>[!NOTE]
>
>Ce modèle est filtré sur le statut Terminé avant le regroupement, ce qui garantit que seuls les enregistrements ayant une date de fin valide sont inclus et que les dates nulles ne faussent pas la tendance mensuelle.

### Délai d’achèvement

**Catégorie :** Transcriptions, Achèvement Et Suivi De La Progression

**Description :** mesure le temps réel passé à terminer chaque cours, en moyenne, minimum et maximum, par rapport à la durée prévue.

**À utiliser lorsque :** vous souhaitez identifier les cours où les élèves prennent beaucoup plus de temps ou moins de temps que prévu pour les terminer, ce qui peut indiquer des problèmes de longueur du contenu ou de difficulté.

**Publics concernés :** formation des clients, formation des partenaires, formation des employés, accompagnement commercial.

**Jeux de données utilisés :** objet d’apprentissage, transcription (objet d’apprentissage)

**Colonnes clés :** ID de l’objet d’apprentissage, nom de l’objet d’apprentissage, type d’objet d’apprentissage, durée (minutes, conception), nombre total d’élèves terminés, temps moyen passé (minutes), temps min passé (minutes), temps max. passé (minutes)

**Filtres appliqués :** date d&#39;achèvement au cours de l&#39;année dernière ; état = Terminé ; catalogue = Catalogue par défaut

**Regrouper par :** ID d&#39;objet d&#39;apprentissage, nom, type, durée (minutes)

**Agrégats :** comptage unique sur l&#39;ID utilisateur, moyenne/min/max sur le temps passé

**Remarque :** la durée (la longueur de cours prévue) est incluse dans l&#39;option Regrouper par afin qu&#39;elle apparaisse sur la même ligne que le temps réel passé, ce qui permet une comparaison directe sans champ calculé. Un écart important entre le temps min et max passé suggère des expériences d’apprentissage incohérentes.

### Affectations d’apprentissage en retard

**Catégorie :** Conformité et certification

**Description :** répertorie les utilisateurs actifs avec des inscriptions obligatoires en retard, en indiquant l&#39;échéance, le statut actuel et la progression pour chacun d&#39;eux.

**À utiliser lorsque :** vous avez besoin d&#39;une liste activable d&#39;élèves non conformes pour passer aux responsables ou déclencher des workflows de réinscription.

**Publics concernés :** formation des partenaires, formation des employés, aide à la vente.

**Jeux de données utilisés :** utilisateur, groupe d’utilisateurs (champ actif), objet d’apprentissage, relevé de notes (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, nom d&#39;utilisateur, adresse e-mail de l&#39;utilisateur, nom du responsable, nom du groupe d&#39;utilisateurs (champ actif), ID de l&#39;objet d&#39;apprentissage, nom de l&#39;objet d&#39;apprentissage, type d&#39;objet d&#39;apprentissage, date d&#39;inscription, échéance de l&#39;achèvement, état, pourcentage de progression, en retard

**Filtres appliqués :** En retard = Oui ; État = En cours OU Non commencé ; Échéance au cours de l’année précédente ; Catalogue = Catalogue par défaut ; État utilisateur = Actif ; Nom du groupe d’utilisateurs (champ actif) = Profil (champ actif)

**Aucun groupe par appliqué** La sortie est d&#39;une ligne par inscription en retard, ce qui préserve l&#39;intégralité des détails de l&#39;élève et du cours pour la réaffectation.

>[!NOTE]
>
>Le filtre Statut (En cours OU Non commencé) sert de mesure de sécurité pour exclure tout enregistrement incorrectement marqué comme en retard bien qu&#39;il soit terminé.

### Statut de formation obligatoire

**Catégorie :** Conformité et certification

**Description :** vue de conformité complète de toutes les inscriptions avec une échéance d&#39;achèvement, avec tous les statuts inclus, pas seulement en retard.

**À utiliser lorsque :** vous avez besoin d&#39;un tableau complet de la conformité plutôt que de simples violations, par exemple, pour signaler les taux globaux d&#39;achèvement de la formation obligatoire aux responsables.

**Publics concernés :** formation des employés, activation commerciale.

**Jeux de données utilisés :** utilisateur, groupe d’utilisateurs (champ actif), objet d’apprentissage, relevé de notes (objet d’apprentissage)

**Colonnes clés :** ID utilisateur, nom d’utilisateur, adresse e-mail de l’utilisateur, nom du responsable, nom du groupe d’utilisateurs (champ actif), ID de l’objet d’apprentissage, nom de l’objet d’apprentissage, type d’objet d’apprentissage, date d’inscription, échéance de l’achèvement, date d’achèvement, état, pourcentage d’avancement, en retard

**Filtres appliqués :** l&#39;échéance d&#39;achèvement n&#39;est pas vide ; date d&#39;inscription au cours de l&#39;année dernière ; catalogue = catalogue par défaut ; état de l&#39;utilisateur = actif ; nom du groupe d&#39;utilisateurs (champ actif) = profil (champ actif)

**Aucun groupe par appliqué** Tous les statuts inclus (terminé, en cours, non commencé, en retard), donnant une image complète de la conformité.

**Remarque :** le filtrage sur « La date limite d&#39;achèvement n&#39;est pas vide » est la logique clé qui identifie systématiquement la formation obligatoire pour tous les types de cours, quelle que soit la configuration du statut obligatoire.

## Référence rapide de modèle

| **#** | **Nom du modèle** | **Catégorie** | **Enseignement interne** | **Éducation externe (client/partenaire)** |
|--------|------------------------------|-------------------------------------|------------------|-------------------------------------|
| 1 | Relevé de notes de l’utilisateur | Transcriptions, achèvement et progression | ✓ | ✓ |
| 2 | Résumé de la progression de l’élève | Transcriptions, achèvement et progression | ✓ | ✓ |
| 3 | Tableau de bord des élèves actifs | Engagement de l’élève et utilisation de la plateforme | ✓ | ✓ |
| 4 | Rapport sur les élèves inactifs | Engagement de l’élève et utilisation de la plateforme | ✓ | ✓ |
| 5 | Adoption d’un nouvel élève | Engagement de l’élève et utilisation de la plateforme | ✓ | ✓ |
| 6 | Apprentissage par groupe d’utilisateurs | Utilisateurs, groupes et structure de l’organisation | ✓ | ✓ |
| 7 | Apprentissage par emplacement | Utilisateurs, groupes et structure de l’organisation | ✓ | ✓ |
| 8 | Formation par le responsable | Utilisateurs, groupes et structure de l’organisation | ✓ | ✗ |
| 9 | Résumé de l’inscription | Transcriptions, achèvement et progression | ✓ | ✓ |
| 10 | Analyse de la tendance des inscriptions | Transcriptions, achèvement et progression | ✓ | ✓ |
| 11 | Rapport d’achèvement du cours | Transcriptions, achèvement et progression | ✓ | ✓ |
| 12 | Tableau de bord Tendance d&#39;achèvement | Transcriptions, achèvement et progression | ✓ | ✓ |
| 13 | Délai d’achèvement | Transcriptions, achèvement et progression | ✓ | ✓ |
| 14 | Affectations d’apprentissage en retard | Conformité et certification | ✓ | ✓ |
| 15 | Statut de formation obligatoire | Conformité et certification | ✓ | ✗ |

## Utilisation d’un modèle de Report Builder

Démarrez rapidement dans le Report Builder Adobe Learning Manager en personnalisant un modèle prédéfini pour les cas d’utilisation courants de création de rapports.

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **Rapports** dans le volet de gauche, puis **Report Builder**.

3. Sélectionnez l&#39;onglet **Modèles**.
4. Parcourez les modèles disponibles. Chaque modèle est nommé en fonction de son cas d’utilisation.

   ![](assets/report-builder-0004.png)

5. Sélectionnez un nom de modèle pour ouvrir son aperçu en lecture seule. Pour cet exemple, sélectionnez le modèle **Conformité % pour l&#39;équipe de l&#39;utilisateur**. Vérifiez les colonnes, les filtres appliqués et l’ordre de tri.
6. Sélectionnez **Dupliquer**.

   ![](assets/report-builder-0005.png)

Lorsque vous dupliquez un modèle, Report Builder ouvre une copie modifiable avec la configuration existante du modèle préchargée. Le nom, la description, les colonnes, les filtres et le tri du rapport peuvent être modifiés avant l’enregistrement.

## Nommer et décrire le rapport

1. Dans le champ **Nom**, remplacez le nom par défaut (par exemple, *copie du % de conformité pour l&#39;équipe de l&#39;utilisateur*) par un nom unique pour votre rapport. Un nom est requis.
2. Dans le champ **Description**, saisissez un court résumé de ce que contient le rapport. Cela aide les autres administrateurs à comprendre l’objectif du rapport lorsqu’ils le consultent ou le modifient.

## Ajout et configuration de colonnes

La section **Colonnes** comporte deux panneaux : **Sélectionner des colonnes** à gauche et **Sélectionner des colonnes** à droite.

### Ajout d’une colonne

1. Dans le panneau **Sélectionner des colonnes**, développez un jeu de données en sélectionnant son nom. Par exemple, **Catalogue** ou **Groupe d&#39;utilisateurs sur le terrain actif**.
2. Sélectionnez l&#39;icône **+** en regard de la colonne que vous souhaitez ajouter. La colonne apparaît dans le panneau **Colonnes sélectionnées** à droite.

   ![](assets/report-builder-0006.png)

3. Pour ajouter la même colonne plusieurs fois. Par exemple, pour appliquer deux agrégats différents au même champ. Sélectionnez à nouveau **+** pour cette colonne.

### Réorganiser les colonnes

Faites glisser la poignée à gauche de n&#39;importe quelle ligne de colonne dans le panneau **Colonnes sélectionnées** pour la déplacer vers une autre position. L’ordre des colonnes dans le panneau correspond à celui du rapport téléchargé.

### Renommer une colonne

1. Sélectionnez l&#39;icône **modifier** (crayon) sur une ligne de colonne.

   ![](assets/report-builder-0007.png)

2. Entrez un alias. L’alias s’affiche comme en-tête de colonne dans le rapport téléchargé au lieu du nom de champ par défaut.

   ![](assets/report-builder-0008.png)

### Suppression d’une colonne

Sélectionnez l&#39;icône **x** sur une ligne de colonne pour la supprimer du rapport.

## Appliquer le regroupement par

La commande **Regrouper par** apparaît en haut du panneau **Colonnes sélectionnées**.

1. Sélectionnez **Regrouper par : sélectionnez**.

   ![](assets/report-builder-0009.png)

2. Sélectionnez les colonnes à regrouper. Vous pouvez en sélectionner plusieurs. Dans la capture d&#39;écran, le rapport est regroupé par Nom du groupe d&#39;utilisateurs (équipe) et Nom du propriétaire du groupe d&#39;utilisateurs (équipe).
3. Chaque colonne groupe par sélectionnée apparaît sous la balise sous le contrôle **Groupe par**. Pour supprimer une colonne de groupe par, sélectionnez **x** sur sa balise.

>[!NOTE]
>
>Lorsque l&#39;option Regrouper par est appliquée, une fonction d&#39;agrégation doit être appliquée à chaque colonne qui n&#39;est pas une colonne Regrouper par. Une colonne sans agrégat provoque une erreur.

### Application d&#39;un agrégat à une colonne

1. Sur toute colonne sans regroupement dans le panneau **Colonnes sélectionnées**, sélectionnez **Agréger par**.
2. Choisissez une fonction dans la liste déroulante. Dans la capture d&#39;écran, **Nombre d&#39;objets d&#39;apprentissage** utilise **Nombre distinct**, alias count_of_courses.

   ![](assets/report-builder-0010.png)

Fonctions d&#39;agrégation disponibles :

| **Fonction** | **Éléments renvoyés** |
|--------------------|---------------------------------------------|
| **Nombre** | Nombre total de lignes dans le groupe |
| **Comptage Distinct** | Nombre de valeurs uniques dans le groupe |
| **Compter Si** | Nombre de lignes correspondant à une valeur que vous spécifiez |
| **Somme** | Total d’un champ numérique dans le groupe |
| **Min** | Valeur la plus faible du groupe |
| **Max** | Valeur la plus élevée du groupe |
| **Moyenne** | Valeur moyenne dans le groupe |

## Appliquer des filtres

La section **Filtres** se trouve sous la section **Colonnes**. Les filtres limitent les lignes qui apparaissent dans le rapport.

1. Pour ajouter un filtre, sélectionnez l’icône **+** à droite de la section Filtres.
2. Sélectionnez le champ sur lequel filtrer.

   ![](assets/report-builder-0011.png)

3. Sélectionnez un opérateur et saisissez ou choisissez une valeur.

Pour modifier un filtre existant, sélectionnez l&#39;icône **crayon** sur la ligne de filtre. Pour ajouter un groupe de filtres imbriqués, sélectionnez l’icône **+** avec des crochets à droite d’une ligne de filtre.

## **Configurer le tri**

La section **Tri** se trouve sous la section **Filtres**.

1. Sélectionnez **+ Ajouter le tri** pour ajouter un tri.
2. Choisissez la colonne à trier et sélectionnez **Croissant** ou **Décroissant**.

   ![](assets/report-builder-0012.png)

3. Répétez l’opération pour ajouter des tris secondaires. Faites glisser la poignée à gauche de chaque ligne de tri pour modifier la priorité.

>[!TIP]
>
>Appliquez toujours au moins un tri. Sans tri, l’ordre des lignes peut différer selon le téléchargement d’un même rapport.

## Enregistrer le rapport

Sélectionnez **Enregistrer le rapport** dans le coin supérieur droit. Le rapport est enregistré dans votre onglet **Rapports** et est prêt à être téléchargé.

## Bonnes pratiques

* Utilisez des alias sur chaque colonne afin que le rapport téléchargé comporte des en-têtes significatifs au lieu de noms de champ tels que Objet d’apprentissage - ID d’objet d’apprentissage.
* Utilisez **Count Distinct** au lieu de **Count** lorsque vous souhaitez des enregistrements uniques, par exemple, des cours distincts par catalogue plutôt que des lignes de total.

* Appliquez le tri avant l’enregistrement, en particulier pour les rapports que vous partagerez ou auxquels vous vous abonnerez.
* Gardez la description à jour. D’autres administrateurs s’y fient pour comprendre la portée du rapport sans l’ouvrir.
