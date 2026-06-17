---
jcr-language: en_us
title: Limitations du Report Builder dans Adobe Learning Manager
description: Découvrez les Reports Builder qui ne sont pas pris en charge dans cette version afin de pouvoir planifier votre approche de création de rapports en conséquence.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Limitations du Report Builder dans Adobe Learning Manager

Report Builder couvre un large éventail de besoins de création de rapports personnalisés, mais certains types de rapports, ensembles de données et configurations ne sont pas pris en charge dans cette version. Cette section répertorie les limitations connues et suggère des solutions de contournement, le cas échéant.

## Certifications récurrentes

Certaines requêtes impliquant des certifications récurrentes ne fonctionnent pas correctement dans le Report Builder de cette version. Si votre rapport implique des cycles de certification récurrents, tels que le suivi d’une réinscription ou d’une réexécution sur plusieurs périodes de certification, utilisez plutôt les rapports de certification existants dans Adobe Learning Manager.

## Jeux de données et types de rapports non pris en charge

Les éléments suivants ne sont pas disponibles dans Report Builder dans cette version :

* **Données de résultats commerciaux** : Report Builder ne prend pas en charge les intégrations BYOD (Bring Your Own Data). Les rapports qui combinent des données professionnelles externes avec des données LMS ne sont pas pris en charge.
* **Rapports d&#39;audit** : les journaux d&#39;audit système et d&#39;activité de l&#39;administrateur ne peuvent pas être intégrés dans le Report Builder. Utilisez les rapports d’audit existants dans la vue Administrateur pour ces données.
* **Rapports incrémentiels** : le Report Builder génère des rapports d&#39;instantanés complets à chaque fois. Les rapports incrémentiels qui ne renvoient que les enregistrements modifiés depuis le dernier téléchargement ne sont pas pris en charge. Pour les données incrémentielles, utilisez l’API de tâche.

## Limitations du rapport de tendance

### Une seule colonne de date par rapport de tendance

Un seul rapport de tendances ne peut être regroupé que par une seule colonne basée sur la date. Vous ne pouvez pas combiner deux tendances différentes basées sur la date dans le même rapport.

Par exemple, vous pouvez créer :

* Rapport affichant les **inscriptions par mois** (regroupées par date d&#39;inscription)
* Un rapport distinct montrant les **achèvements par mois** (regroupés par date d&#39;achèvement)

Vous ne pouvez pas créer un seul rapport qui affiche le mois d’inscription et le mois d’achèvement dans des colonnes de tendance distinctes. Pour obtenir les deux, créez deux rapports distincts et analysez-les côte à côte.

### Les tendances reflètent les données actuelles, pas les instantanés historiques

Les rapports de tendances dans Report Builder sont fondés sur les données ponctuelles actuelles et non sur des instantanés historiques. Le rapport reflète l&#39;état des enregistrements tels qu&#39;ils existent aujourd&#39;hui, distribués dans leurs champs de date.

Cela signifie :

* Un élève inscrit en janvier mais désinscrit ultérieurement peut ne pas apparaître dans la tendance d&#39;inscription de janvier
* Un groupe d’utilisateurs qui a été réorganisé ne reflétera pas son appartenance historique des derniers mois
* Les enregistrements supprimés peuvent ne pas apparaître dans la tendance pour la période pendant laquelle ils étaient actifs

Utilisez les rapports de tendances pour l&#39;analyse directionnelle. Pour obtenir un historique précis ou à des fins d’audit, utilisez les rapports fixes existants ou les exportations d’API de tâche.
