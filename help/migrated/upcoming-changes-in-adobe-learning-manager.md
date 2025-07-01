---
title: Changements à venir dans Adobe Learning Manager
description: Découvrez les nouvelles fonctionnalités, améliorations et mises à jour importantes qui seront bientôt disponibles sur Adobe Learning Manager. Tenez-vous informé des changements afin de pouvoir planifier et tirer le meilleur parti des dernières améliorations.
source-git-commit: 97c52c188612b7ad7233a13bd90bcb174fdc60bc
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 2%

---


# Changements à venir dans Adobe Learning Manager

Nous sommes ravis de vous faire part de plusieurs mises à jour importantes à venir dans Adobe Learning Manager pour les prochaines versions. Ces améliorations visent à rationaliser les workflows d’administration, à améliorer la précision des rapports de données et à renforcer les contrôles basés sur les rôles.

Ces changements sont conçus pour réduire l’effort manuel, prendre en charge l’automatisation et améliorer la gouvernance des opérations de formation.

## Capturer les terminaisons marquées par un instructeur dans le relevé de notes de l’élève (M44)

### Audience

Propriétaires administrateur et automatisation

### Vue d’ensemble

Dans Adobe Learning Manager, lors de l’utilisation des relevés de notes incrémentiels de l’élève (LT) pour les workflows d’automatisation, les terminaisons marquées par un instructeur effectuées après la date de la session ne sont pas capturées. L’horodatage d’achèvement reflète l’heure de fin de session d’origine (et non l’heure à laquelle l’instructeur a marqué l’achèvement). Étant donné que ces mises à jour ne sont pas incluses dans la fenêtre de modification d’une journée utilisée pour la génération LT incrémentielle, les données de présence et d’achèvement des élèves sont exclues des rapports, ce qui entraîne des rapports en aval inexacts ou incomplets et des écarts de conformité potentiels.

### Quels sont les changements apportés 

Les rapports Relevés de notes de l’élève incluent les terminaisons marquées par les instructeurs après la date de la session. Cela permet de s’assurer que toute marque d’assiduité retardée est correctement reflétée dans l’exportation du relevé de notes.

Les états de présence tels que « Terminé avec succès/échec » apparaîtront automatiquement dans les exportations LT incrémentielles.

### Nouveautés

* Nouvelle colonne : Marquer la date de fin (fuseau horaire UTC).
* La source d’achèvement est disponible au niveau du module.
* Compatible avec les rapports LT basés sur le connecteur ou générés par l’API du travail.

![](assets/capture-instructor.png)

**Action requise**

* Si l&#39;automatisation dépend de la position des colonnes, assurez-vous que la logique tient compte de la nouvelle colonne.
* Si vous utilisez des noms de colonnes, aucune modification n’est requise.
* Les finitions modernisées (importations manuelles) ne sont pas incluses.

## Liens de téléchargement dans le rapport Assistances à la tâche (M44)

### Audience

Administrateur, administrateur personnalisé et propriétaires d’automatisation

### Vue d’ensemble

Le rapport Assistances à la tâche comprend un lien de téléchargement direct pour chaque assistance à la tâche, permettant un accès rapide à partir du rapport lui-même.

### Nouveautés

Une nouvelle colonne, **[!UICONTROL Lien d&#39;assistance à la tâche]**, a été ajoutée à la troisième position dans le rapport. Il renvoie directement à l’assistance à la tâche s’il s’agit d’un fichier ou s’il affiche l’URL externe fournie par l’auteur.

Les utilisateurs disposant d’un accès (administrateur/auteurs et rôles personnalisés) peuvent télécharger l’assistance à la tâche à l’aide de ce lien.

![](assets/download-links-for-job-aid.png)

### Action requise

* Examinez les workflows automatisés à l’aide des rapports d’assistances à la tâche (à l’aide de l’API Jobs).
* Si le script est basé sur la position des colonnes, mettez à jour les scripts en conséquence.
* Aucune action n’est nécessaire si vous utilisez des noms de colonnes.

## Colonnes ID utilisateur interne et E-mail du responsable ajoutées au rapport utilisateur (M44)

### Audience

Les administrateurs (et les administrateurs personnalisés) qui utilisent le **[!UICONTROL rapport utilisateur]** (**[!UICONTROL Administrateur]** > **[!UICONTROL Utilisateurs]** > **[!UICONTROL Interne]** > **[!UICONTROL Exporter les données utilisateur]**) téléchargé à partir de l&#39;interface utilisateur de l&#39;administrateur.

### Vue d’ensemble

Pour faciliter l&#39;identification des utilisateurs et les workflows d&#39;intégration, deux colonnes, **[!UICONTROL ID utilisateur interne]** et **[!UICONTROL E-mail du responsable]**, ont été ajoutées au rapport Utilisateur, exportées via l&#39;interface utilisateur.

### Nouveautés

Le rapport Utilisateur inclut l’ID utilisateur interne d’un utilisateur et l’adresse e-mail de son responsable, pour les mapper de manière unique entre différents outils ou points de terminaison d’API.

### Action requise

* Si vous utilisez ce rapport dans des flux automatisés, cette colonne nouvellement ajoutée doit être prise en charge dans l&#39;automatisation.
* Aucune modification n’est nécessaire si les workflows ne sont pas affectés.

## Autorisations d’annonce étendues pour les administrateurs personnalisés (M44)

### Audience

Administrateurs personnalisés

### Vue d’ensemble

Les administrateurs personnalisés peuvent créer des annonces uniquement pour les groupes d&#39;utilisateurs ou les catalogues dans leur portée définie.

### Nouveautés

* Les règles d&#39;étendue permettent aux administrateurs personnalisés de créer des annonces pour des groupes d&#39;utilisateurs ou des catalogues spécifiques uniquement.
* Lors de la définition d&#39;un rôle personnalisé, les administrateurs peuvent attribuer des autorisations d&#39;annonce avec une portée sur les groupes d&#39;utilisateurs ou les catalogues.
* Les administrateurs personnalisés sont limités à la création d&#39;annonces dans leur portée donnée.
* Le rapport d’annonce de notification pour les administrateurs personnalisés affichera les élèves uniquement dans la portée qui leur est attribuée.

### Action requise

* Le format du rapport restera inchangé. Si des administrateurs personnalisés le téléchargent à partir de l’interface utilisateur, le contenu du rapport est soumis à leur portée.
* Aucune modification n’est nécessaire si ce rapport n’est utilisé dans aucun workflow automatisé ou en aval.
