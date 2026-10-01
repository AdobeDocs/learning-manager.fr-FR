---
description: Découvrez comment les administrateurs de Learning Manager activent Virtual Coach, surveillent l’utilisation des crédits MAU et téléchargent les rapports de performance des élèves
jcr-language: en_us
title: Gérer l’utilisation et la facturation du Virtual Coach
exl-id: 1f8f6465-51c3-4670-a1c7-9a7dfb091452
source-git-commit: 449f25df93867bf4d5ec11af057f8da7c405a09f
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%
---

# Gérer l’utilisation et la facturation du Virtual Coach

Activez Virtual Coach, surveillez la consommation de crédit de l’utilisateur actif mensuel (MAU) et téléchargez les rapports de performance des élèves en tant qu’administrateur Adobe Learning Manager.

## Activer Virtual Coach pour votre compte {#activatevirtualcoach}

Virtual Coach est disponible en tant que module complémentaire pour Adobe Learning Manager. Après l’achat, la mise en service génère une clé d’activation qui est envoyée par e-mail à l’administrateur du compte.

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Accédez à la page **Facturation** à partir du navigateur de gauche.
3. Dans la section **Virtual Coach**, saisissez la clé d&#39;activation que vous avez reçue par courrier électronique.

   ![](/help/migrated/administrators/feature-summary/assets/virtual_coach12.png)
   *Entrez votre clé d&#39;activation dans la section Virtual Coach de la page de facturation pour activer la fonctionnalité.*

4. Sélectionnez **Appliquer**. Virtual Coach est activé pour votre compte.

Une fois activée, vous recevez une notification dans l’application confirmant que la fonctionnalité est en ligne. Quatre exemples de scénarios de jeu de rôle sont ajoutés automatiquement à la **bibliothèque de contenu** afin que les auteurs puissent commencer immédiatement.

>[!NOTE]
>
>La clé d’activation est générée automatiquement lors de l’approvisionnement et partagée par e-mail. Si vous ne disposez pas de la clé d’activation, contactez votre gestionnaire de succès client Adobe Learning Manager.

## Afficher le solde créditeur MAU

Les crédits MAU (Monthly Active User) comptent le nombre d’élèves uniques qui utilisent Virtual Coach chaque mois.

1. Accédez à la page **Facturation**.
2. Dans la section **Virtual Coach**, sélectionnez **Afficher les détails d&#39;utilisation**.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach22.png)

3. Utilisez la liste déroulante **Sélectionner une période** pour choisir la période que vous souhaitez réviser.

   La table **Utilisation globale** indique :

   - **Disponible** : total des crédits MAU achetés.
   - **Utilisé** : crédits consommés à ce jour.
   - **Restant** : crédits disponibles pour le reste de la période du contrat.

   La table **Utilisation mensuelle** affiche le nombre d&#39;élèves actifs uniques par mois civil.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach23.png)

4. Sélectionnez **Télécharger le rapport détaillé** pour exporter les données d&#39;utilisation complètes.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach-report-mau-billing-5.png)

## Mode d’utilisation des crédits MAU

Un crédit MAU est consommé lorsqu’un élève lance une session d’entraîneur virtuel au cours d’un mois civil. Les sessions supplémentaires du même élève le même mois ne consomment pas de crédits supplémentaires. Les crédits inutilisés à la fin de la période du contrat expirent et ne sont pas reportés.

| Scénario | MAU consommés |
|---|---|
| Un élève termine 5 sessions en janvier | 1 |
| Le même élève utilise Virtual Coach en janvier et février | 2 (1 par mois) |
| 100 élèves terminent chacun une session en janvier | 100 |

*Les crédits MAU sont comptabilisés par élève unique par mois civil, quel que soit le nombre de sessions lancées par chaque élève.*

**Exemple : élève unique, plusieurs sessions.** Sarah lance cinq sessions d&#39;entraîneurs virtuels en janvier. Elle est comptabilisée comme un seul utilisateur unique pour le mois, donc 1 MAU est consommé quel que soit le nombre de fois qu&#39;elle pratique.

**Exemple : même élève, plusieurs mois.** Sarah utilise Virtual Coach en janvier (3 sessions) et en février (2 sessions). Chaque mois civil compte séparément, donc 2 MAU sont consommés : 1 pour janvier et 1 pour février.

**Exemple : plusieurs élèves le même mois.** 100 représentants commerciaux lancent chacun une session de Coach virtuel en janvier. Chaque élève unique compte comme une MAU pour ce mois, donc 100 MAU sont consommés.

**Exemple : entraînement en équipe au fil du temps.** Votre équipe de 50 personnes utilise Virtual Coach tout au long de l&#39;année. Dans un mois où seulement cinq sur les 50 s’entraînent, cinq MAU sont consommés pour ce mois ; dans un mois où les 50 s’entraînent à nouveau, 0 MAU supplémentaire au-delà de ce qui a déjà été consommé pour les élèves qui reviennent ce mois-là, puisque chaque élève n’est compté qu’une fois par mois civil, quel que soit le nombre de fois qu’il s’entraîne en son sein.

Pour en savoir plus sur les rapports Virtual Coach, accédez à [Rapports Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/virtual-coach-reports.md).
