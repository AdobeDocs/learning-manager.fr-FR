---
jcr-language: en_us
title: Report Builder - Foire aux questions
description: Obtenez des réponses aux questions fréquemment posées sur Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---


# Report Builder - Foire aux questions


**Quelle est la différence entre un modèle et un rapport ?**

Les modèles sont des configurations de rapport prédéfinies fournies par Adobe Learning Manager. Ils sont conçus pour les cas d’utilisation courants, prêts à être téléchargés immédiatement et en lecture seule. Vous ne pouvez pas les modifier. Les rapports sont vos propres configurations enregistrées. Vous pouvez les créer en créant de toutes pièces ou en dupliquant un modèle et en modifiant la copie. Les rapports apparaissent dans l&#39;onglet **Rapports** ; les modèles apparaissent dans l&#39;onglet **Modèles**.

**Puis-je modifier un modèle directement ?**

Non. Les modèles sont en lecture seule. Pour personnaliser un modèle, sélectionnez **Dupliquer** pour créer une copie modifiable. Vos modifications sont enregistrées en tant que nouveau rapport dans l&#39;onglet **Rapports** et n&#39;affectent pas le modèle d&#39;origine.

Des lignes en double apparaissent lorsqu&#39;un champ des données a une relation un-à-plusieurs avec l&#39;enregistrement principal. Les causes courantes comprennent les sessions avec plusieurs instructeurs (une ligne par instructeur par session) et les objets d&#39;apprentissage avec plusieurs auteurs. Pour résoudre ce problème, ajoutez le champ qui a plusieurs valeurs, telles que **Noms des instructeurs** ou **Nom de l’auteur**, en tant que colonne.

**Pourquoi l&#39;ordre des lignes change-t-il entre deux téléchargements du même rapport ?**

La génération de rapports utilise un système de requêtes distribué. Sans tri explicite, l&#39;ordre des lignes dépend du nœud de requête qui renvoie les résultats en premier, ce qui peut différer entre les exécutions. Appliquez au moins un tri à votre rapport pour garantir une sortie cohérente entre les téléchargements.

**Pourquoi les dates sont-elles affichées en UTC ?**

Le Report Builder renvoie des valeurs de date en UTC dans cette version. Le fuseau horaire configuré de votre compte sera appliqué aux champs de date dans une prochaine version. Lors de l’analyse des données basées sur la date, tenez compte du décalage UTC pertinent pour le fuseau horaire principal de votre compte.

**Combien de temps faut-il pour que les nouvelles données d’inscription ou d’achèvement apparaissent ?**

Le Report Builder extrait les données de la base de données de Adobe Learning Manager, dont la latence maximale est d’environ 15 minutes à partir du moment où un événement se produit dans le système. Si vous venez d’enregistrer une inscription ou d’achever un projet et qu’elle n’apparaît pas dans votre rapport, attendez au moins 15 minutes et téléchargez à nouveau.

**Existe-t-il une limite de lignes ou de colonnes dans un rapport ?**

Les rapports sont limités à environ 1 million de lignes. Le nombre de colonnes dans cette version n&#39;est pas limité. Si votre rapport nécessite plus d’un million de lignes, appliquez des filtres pour en limiter l’étendue.

**Puis-je extraire des données de Report Builder via une API ou une automatisation ?**

L’accès automatisé des API aux rapports de Report Builder est prévu pour une prochaine version. Dans la version actuelle, les rapports sont téléchargés manuellement via l’interface utilisateur de Report Builder ou reçus de manière planifiée via la fonction d’abonnement.
