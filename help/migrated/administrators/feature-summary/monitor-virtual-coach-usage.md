---
jcr-language: en_us
title: Surveillance de l’utilisation du Virtual Coach
description: Surveillez comment Virtual Coach est utilisé par votre compte.
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 2%

---


# Surveillance de l’utilisation du Virtual Coach

Affichez les données d’utilisation de Virtual Coach, suivez la consommation de crédit de l’utilisateur actif mensuel (MAU) et accédez aux rapports de performances des élèves dans Adobe Learning Manager.

## Activer Virtual Coach pour votre compte

Virtual Coach est disponible en tant que module complémentaire pour Adobe Learning Manager. Après l’achat, la mise en service génère une clé d’activation qui est envoyée par e-mail à l’administrateur du compte.

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Accédez à la page **Facturation** à partir du navigateur de gauche.
3. Dans la section **Virtual Coach**, saisissez la clé d&#39;activation que vous avez reçue par courrier électronique.
4. Sélectionnez **Appliquer**. Virtual Coach est activé pour votre compte.
   ![](assets/virtual-coach-037.png)

Une fois activée, vous recevrez une notification dans l’application confirmant que la fonctionnalité est en ligne. Quatre exemples de scénarios de jeu de rôle sont ajoutés automatiquement à la bibliothèque de contenu afin que les auteurs puissent commencer immédiatement.

>[!NOTE]
>
>La clé d’activation est générée automatiquement lors de l’approvisionnement et partagée par e-mail. Si vous ne disposez pas de la clé d’activation, contactez votre gestionnaire de succès client (CSM) Adobe Learning Manager.

## Afficher votre solde créditeur MAU

Les crédits MAU (Monthly Active User) comptent le nombre d’élèves uniques qui utilisent Virtual Coach chaque mois.

1. Accédez à la page **Facturation**.
2. Dans la section **Virtual Coach**, sélectionnez **Afficher les détails d&#39;utilisation**.
3. Utilisez la liste déroulante **Sélectionner une période** pour choisir la période que vous souhaitez réviser.
   ![](assets/virtual-coach-038.png)

   La table **Utilisation globale** indique :

   a. **Disponible :** total des crédits MAU achetés\
   b. **Utilisé(s) :** crédits consommés à ce jour\
   c. **Restant :** crédits disponibles pour le reste de la période du contrat

   La table **Utilisation mensuelle** affiche le nombre d&#39;élèves actifs uniques par mois civil.

4. Sélectionnez **Télécharger le rapport détaillé** pour exporter les données d&#39;utilisation complètes.

## Mode d’utilisation des crédits MAU

Un crédit MAU est consommé lorsqu’un élève termine une session d’entraîneur virtuel au cours d’un mois civil. Les sessions supplémentaires du même élève le même mois ne consomment pas de crédits supplémentaires.

| Scénario | MAU consommés |
|----------|--------------|
| Un élève termine 5 sessions en janvier | 1 |
| Le même élève utilise Virtual Coach en janvier et février | 2 (1 par mois) |
| 100 élèves terminent chacun une session en janvier | 100 |

_Les crédits MAU sont comptabilisés par élève unique par mois civil, quel que soit le nombre de sessions terminées par chaque élève._

Les crédits non utilisés à la fin de la période contractuelle sont périmés et ne sont pas reportés.

### Exemple 1 : élève unique, plusieurs sessions

Scénario : Sarah termine cinq sessions d&#39;entraîneur virtuel en janvier.

* Sessions en janvier : 5
* MAU consommés : 1
* Pourquoi : Sarah est comptabilisée comme une seule utilisatrice unique pour le mois de janvier, quel que soit le nombre de fois qu&#39;elle s&#39;entraîne.

### Exemple 2 : même élève, plusieurs mois

Scénario : Sarah utilise Virtual Coach en janvier et février.

* Sessions en janvier : 3
* Sessions en février : 2
* MAU consommés : 2 (1 pour janvier + 1 pour février)
* Pourquoi : chaque mois calendaire compte séparément.

### Exemple 3 : plusieurs élèves, même mois

Scénario : 100 représentants commerciaux réalisent chacun une session d’entraîneur virtuel en janvier.

* Nombre total de sessions : 100
* MAU consommés : 100
* Pourquoi : chaque élève unique compte comme un MAU pour ce mois.

### Exemple 4 : Exercice en équipe au fil du temps

Scénario : Votre équipe de 50 personnes utilise Virtual Coach tout au long de l&#39;année.

| Mois | Élèves actifs | MAU consommés ce mois-ci | MAU cumulés |
|------|----------------|--------------------------|-----------------|
| janvier | 0 | 0 | 0 |
| février | 5 (5 personnes ne se sont pas entraînées) | 5 | 5 |
| Mars | 0 (les 50 gains pratiqués) | 0 | 45 |
| Avril | 0 | 0 | 75 |

## Afficher les rapports Virtual Coach

La section **Gérer** > section **Rapports** > page **Rapports IA** fournit des données d’utilisation et de performances pour toutes les activités de l’entraîneur virtuel dans votre organisation. Deux rapports sont disponibles sous l&#39;intitulé **Virtual Coach**.

Tous les rapports sont exportés au format CSV. La génération du rapport peut prendre plusieurs minutes, en fonction de la taille des données.

### Résumé de l’utilisation de l’élève

Contient les données d’utilisation mensuelles pour tous les élèves. Utilisez ce rapport pour suivre le nombre d’élèves qui utilisent Virtual Coach chaque mois, surveiller la consommation de crédit MAU et identifier les tendances d’engagement au fil du temps.

### Détails de la session

Contient des données de niveau session pour tous les élèves des 90 derniers jours. Utilisez ce rapport pour examiner les scores de session, la couverture de rubrique et les mesures de style individuels dans votre population d’élèves, et pour identifier les lacunes en matière de compétences qui peuvent nécessiter une formation ou un contenu supplémentaire.

## Accéder à un rapport et le télécharger

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **Rapports** dans le volet de navigation de gauche.
3. Sélectionnez **Rapports IA**.
4. Sous la section **Coach virtuel**, sélectionnez le rapport que vous souhaitez télécharger, **Résumé de l&#39;utilisation de l&#39;élève** ou **Détails de la session**.
   ![](assets/virtual-coach-039.png)
5. Sélectionnez la plage de dates lorsque vous y êtes invité, puis sélectionnez **Continuer**.
6. Le rapport se télécharge automatiquement au format CSV.
