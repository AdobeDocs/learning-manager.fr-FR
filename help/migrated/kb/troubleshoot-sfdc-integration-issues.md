---
jcr-language: en_us
title: Résolution des problèmes d’intégration de Salesforce (SFDC) avec Adobe Learning Manager
description: Résolvez les problèmes courants d’intégration de Salesforce (SFDC) à Adobe Learning Manager (ALM), notamment les échecs d’exportation, les problèmes d’autorisation de champ dans les objets personnalisés SFDC et les notes importantes sur la compatibilité SFDC-ALM.
contentowner: saghosh
source-git-commit: cedb4acc89e7d972a4752e10c4fb6930c4633f6a
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Résolution des problèmes d’intégration de Salesforce (SFDC) avec Adobe Learning Manager

## Dépannage des échecs d’exportation SFDC (aucune exportation pendant 2 à 3 heures ou plus)

Si l&#39;exportation SFDC ne s&#39;est pas terminée correctement pendant plus de **2-3 heures**, suivez les étapes ci-dessous pour identifier et comprendre le problème.

1. Accédez à la page **Accueil Salesforce**.
2. Dans la zone de recherche **Recherche rapide**, saisissez **`Bulk Data Load Jobs`** et ouvrez-la.
3. La page affiche les tâches de chargement de données en bloc pour les **7 derniers jours**.
4. Recherchez des travaux associés aux **objets Adobe Learning Manager (ALM)**.
5. Cliquez sur la tâche spécifique sur laquelle vous souhaitez enquêter.
6. Faites défiler la page des détails du travail jusqu&#39;en **bas** pour afficher le **message d&#39;erreur** et des détails supplémentaires.

Dans de nombreux cas, la cause première est l&#39;insuffisance des autorisations au niveau des champs dans SFDC **.** Le nom du champ défaillant peut ressembler à :

- `cp_Module_ID`
- ou d&#39;autres champs `cp_...` liés aux objets personnalisés ALM.

Si de tels champs apparaissent dans l’erreur, passez à la section suivante.

## Octroi d’autorisations de champ sur les champs d’objet personnalisés ALM dans SFDC

Utilisez la fonctionnalité **Accessibilité des champs** pour résoudre les problèmes d&#39;autorisation sur des champs spécifiques (par exemple, `cp_Module_ID`).

### Étapes

1. Accédez à la page **Accueil Salesforce**.
2. Dans la zone de recherche **Recherche rapide**, saisissez **`Field Accessibility`** et ouvrez-la.
3. Dans la liste des objets, sélectionnez le **type de rapport/objet** pertinent.
   - Exemple : `cp_LearnerTranscript_xxxx_xxxx` pour le rapport Relevé de notes de l’élève (LT).
4. Sur la page suivante, sélectionnez **« Afficher par champs »**.
5. Dans la liste déroulante **champ**, sélectionnez le champ qui s&#39;est affiché dans l&#39;erreur d&#39;exportation
   - Exemple : `cp_Module_ID`.
6. Dans la matrice d&#39;accès, cliquez sur l&#39;entrée **« Masqué »** pour le profil **Administrateur système** (et d&#39;autres profils pertinents, si nécessaire).
7. À la page suivante :
   - Activez **« Visible »** le cas échéant.
   - Cliquez sur **Enregistrer** en bas de la page.
8. Après l’enregistrement, vous revenez à la vue d’accessibilité des champs. Le champ doit maintenant s&#39;afficher en tant que **« Modifiable »** pour **Administrateur système** (et tous les autres profils que vous avez mis à jour).

## Répétez l’opération pour tous les champs concernés et recommencez l’exportation

1. **Répétez** les étapes d&#39;accessibilité des champs de la section 2 pour **chaque champ** signalé comme présentant des problèmes d&#39;autorisation dans les **tâches de chargement de données en bloc**.
2. Une fois que tous les champs problématiques ont une visibilité et des autorisations de modification correctes :
   - Revenez à **Adobe Learning Manager**.
   - Dans la configuration **Connecteur SFDC**, **réessayez l&#39;exportation**.


## Remarques importantes et limitations

Gardez ces spécificités SFDC-ALM à l’esprit lors de la conception ou du dépannage des intégrations.

### Aucune création automatique d’objet/de champ dans SFDC

- Le connecteur **SFDC ne crée pas de nouveaux objets ou champs dans Salesforce**.
- Si un **nouveau champ est ajouté dans ALM** et que vous souhaitez qu’il apparaisse dans SFDC :
   - **Créez manuellement le champ personnalisé correspondant** dans SFDC.
   - **Mappez** le champ personnalisé SFDC au **champ ALM approprié** dans la configuration du connecteur.
   - Assurez-vous que le nouveau champ dispose des **autorisations appropriées** au niveau des champs (utilisez la section 2).

### URL de rappel pour les comptes ALM avec des domaines personnalisés

- Si le compte ALM utilise un **domaine personnalisé**, l&#39;équipe d&#39;ingénieurs doit **ajouter ce domaine personnalisé** à la **liste autorisée d&#39;URL de rappel** pour l&#39;application de production OAuth du connecteur SFDC.
- Cela se fait via une **demande Jira** à l&#39;équipe d&#39;ingénierie.
- Sans cela, le flux OAuth du connecteur peut échouer.

### Limitation de fuseau horaire (UTC uniquement)

- Si l’organisation SFDC utilise un **fuseau horaire autre que UTC**, les données d’achèvement et d’inscription de **peuvent être manquantes** pendant la synchronisation.
- Raison : ALM **ne prend actuellement en charge que le fuseau horaire UTC** pour l&#39;intégration SFDC.
- Référence interne : PAPI-24525 est levé pour prendre en charge des fuseaux horaires supplémentaires.

### Limitation du type de données de filtre (liste déroulante ou liste de contrôle)

- ALM prend en charge l&#39;importation de **filtres SFDC créés avec des champs de liste déroulante**.
- ALM **ne prend pas en charge** les filtres basés sur les champs de liste de contrôle/case à cocher à sélections multiples.
- Raison : ALM **ne prend en charge que les types de données de chaîne** pour les filtres SFDC.
