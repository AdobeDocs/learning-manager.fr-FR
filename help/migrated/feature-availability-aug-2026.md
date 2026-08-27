---
description: Découvrez quelles applications prennent en charge les nouvelles fonctionnalités de Adobe Learning Manager pour la version d’août 2026, notamment les API, les appareils mobiles et les widgets AEM
jcr-language: en_us
title: Disponibilité des fonctionnalités dans la version d’août 2026 de Adobe Learning Manager
exl-id: e134937c-630d-4285-9181-2eca114717f6
source-git-commit: bb95f74b775d279e94fad319380d451446256636
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

---


# Disponibilité des fonctionnalités dans la version d’août 2026 de Adobe Learning Manager

## Objectif

Les clients d’entreprise qui créent ou étendent la plateforme par le biais de leur propre interface frontale (une mise en œuvre « sans interface utilisateur ») demandent régulièrement si une fonctionnalité nouvelle ou modifiée peut être réellement utilisée en dehors de l’interface utilisateur web standard, via l’API de l’élève, l’API de l’administrateur, le widget AEM ou une autre surface d’intégration.

Ce document fournit une réponse rapide et narrative pour chaque fonctionnalité livrée dans cette version. Pour chaque fonctionnalité, ce document identifie les surfaces d’application prises en charge, la disponibilité de l’intégration, la prise en charge de la migration et tout comportement de notification applicable.

## Disponibilité fonctionnalité par fonctionnalité

### Créateur d’e-mails basé sur des composants

Cela permettra à différents comptes qui s’inscrivent après la sortie de la fonctionnalité d’activer progressivement la migration de ces comptes de l’éditeur de messagerie existant vers un nouvel éditeur. Une fois activé, le client ne peut pas utiliser l’ancien éditeur de courrier électronique. (Pour activer les fonctionnalités, veuillez contacter CSM/Support).

* **Disponible sur :** application Administrateur. Les administrateurs et les auteurs configurent les mises en page et les modèles de courrier électronique ici.
* **Sans objet :** interface utilisateur destinée aux élèves, API sans tête et widget AEM, car les élèves reçoivent simplement les e-mails résultants par l&#39;intermédiaire de leur propre client de messagerie.
* **Notifications :**
  * Les notifications par e-mail continuent d’être envoyées aux élèves sur les clients de messagerie pris en charge.
  * Aucun nouveau comportement de notification sur la plateforme n’est introduit par cette fonctionnalité.

### Apprentissage externe

* **Disponible sur :** le Web natif, l&#39;API sans tête (élève), le Web mobile natif et l&#39;application Administrateur.
* **Pas encore disponible sur :** l&#39;application mobile native.
* **API de tâche :** non applicable.
* **Migration :** pas encore prise en charge.
* **Notifications :**
  * Les notifications sur la plateforme sont disponibles pour les élèves et les responsables lorsque des demandes d&#39;approbation d&#39;apprentissage externes sont soumises et lorsque les demandes sont approuvées ou rejetées.
  * Les notifications par e-mail ne sont actuellement pas disponibles pour ce workflow.

### Rapport utilisateur incrémentiel

* **Disponible sur :** API de tâche uniquement. Fournit une exportation incrémentielle (delta) des données utilisateur pour la création de rapports.
* **Non applicable :** interface utilisateur, autres surfaces API et outils de migration.

### Créateur de rapports

* **Disponible sur :** application Administrateur.
* **Pas encore disponible sur :** l&#39;API de tâche. Une exportation basée sur l’API de tâche est prévue pour une version ultérieure.
* **Migration :** non applicable.
* **Notifications :**
  * Les utilisateurs reçoivent des notifications sur la plateforme lorsque les téléchargements de rapports sont prêts ou lorsque la génération de rapports échoue.
  * Les notifications par e-mail ne s’appliquent pas.

### Dossiers de contenu hiérarchiques

* **Disponible sur :** l&#39;application administrateur et l&#39;application auteur.
* **Migration :** prise en charge.
* **API de tâche :** non applicable. Aucune surface d’API dédiée n’existe actuellement.

>[!NOTE]
>
>Les privilèges de rôle personnalisés s’appliquent uniquement au niveau du dossier racine/parent, et non à tous les dossiers de la hiérarchie.

### Agent d’informations

* **Disponible sur :** application Administrateur. Actuellement limité aux administrateurs complets uniquement (et non aux rôles personnalisés).
* **API d&#39;administration :** non disponible.
* **API de tâche/migration :** non applicable.

### Agent de parcours d’apprentissage

* **Disponible sur :** le Web natif et l&#39;API sans tête (élève).
* **Pas encore disponible sur :** le Web mobile natif, l&#39;application mobile native et le widget AEM.
* **API de tâche/migration :** non applicable.

### Assistant IA (élève)

* **Disponible sur :** le Web natif, l&#39;API sans tête (élève) et le Web mobile natif.
* **Pas encore disponible sur :** l&#39;application mobile native et le widget AEM.
* **API de tâche/migration :** non applicable.

>[!NOTE]
>
>Cette fonctionnalité doit être explicitement activée avant qu’elle n’apparaisse aux élèves.

### Hub en direct

* **Disponible sur :** le Web natif, l&#39;API sans tête (élève), le Web mobile natif et l&#39;application Administrateur.
* **API de tâche :** non applicable.
* **Migration :** non prise en charge actuellement.

### Administrateurs Personnalisés : Lire/Gérer D’Autres Rôles Personnalisés

* **Disponible sur :** application Administrateur. Permet aux administrateurs personnalisés d’afficher et de gérer d’autres rôles d’administrateur personnalisés.
* **API de tâche/migration :** non applicable. Aucune API dédiée pour le moment.

### Gradebook

* **Disponible sur :** le Web natif, l&#39;API sans tête (élève), le Web mobile natif, l&#39;application mobile native et l&#39;application administrateur.
* **Pas encore disponible sur :** widget AEM.
* **Migration :** non prise en charge actuellement.
* **Notifications :**
  * Aucune notification par e-mail.
  * Aucune notification sur la plateforme.

### Canaux

* **Disponible sur :** le Web natif et l&#39;application Administrateur. Actuellement en version Beta.
* **Pas encore disponible sur :** API sans tête (élève), Mobile Web, application mobile, widget AEM et API administrateur.
* **API de tâche/migration :** non applicable.
