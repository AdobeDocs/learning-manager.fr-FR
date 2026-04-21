---
description: En savoir plus sur les relevés de notes des élèves
jcr-language: en_us
title: Modifications apportées aux relevés de notes des élèves
exl-id: 295c4e1f-c3c7-4f97-83c3-1234f3d47546
source-git-commit: 048e550320932b683cf6bbcdc0b4d0fdf4e84905
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Modifications apportées aux relevés de notes des élèves dans la version d’avril

## Colonne Méthode d’achèvement

La colonne **Méthode d&#39;achèvement** indique comment chaque enregistrement du relevé de notes de l&#39;élève de l&#39;administrateur a été terminé.

**Valeurs :**

1. **Direct** (pour les terminaisons directes)
2. **Variante** (pour les réalisations obtenues via d&#39;autres relations)
3. **Remplacement révoqué** (lorsque toutes les autres fins de production sont révoquées en raison d&#39;une inachèvement rétroactive et de la suppression de la relation)

>[!NOTE]
>
>Cette colonne n’est pas visible dans le LT de l’élève ; elle est uniquement disponible dans le LT de l’administrateur à des fins de reporting et de suivi.

**Impact** : permet aux administrateurs de bénéficier de pistes d&#39;audit claires, d&#39;un suivi de la conformité et de la transparence concernant la manière dont un cours a été terminé.

## Autre suivi de l’achèvement dans les relevés de notes des élèves

Les autres achèvements permettent aux élèves de recevoir un crédit d’achèvement pour un cours ou un parcours d’apprentissage cible lorsqu’ils ont terminé un cours ou un parcours source équivalent, en fonction des relations établies.

Dans le relevé de notes de l&#39;élève, les autres achèvements ont un impact sur trois colonnes existantes : **État**, **Date d&#39;achèvement** et **Source d&#39;achèvement**.

- **État** : l’état peut être **Terminé** même si l’élève n’a pas directement terminé le cours ou le parcours cible en raison d’une autre achèvement. Les autres états (**Non démarré**, **En cours**, **Non inscrit**) ne sont pas affectés.
- **Date d&#39;achèvement** : pour une autre achèvement, la date est héritée du cours ou du chemin source. Si l’élève termine directement la cible ultérieurement, la date est mise à jour pour refléter l’achèvement direct.
- **Source d&#39;achèvement** : capture le ou les ID de formation du ou des cours ou parcours source qui ont fourni l&#39;autre achèvement. Les sources actives multiples sont répertoriées sous forme d’ID séparés par des virgules. Si les sources sont révoquées, seules les sources actives restent. Lorsque plusieurs sources existent, la date de fin la plus ancienne est utilisée.

**Impact** : les autres achèvements réduisent le rapprochement manuel, automatisent le suivi de la progression dans les parcours d’apprentissage et les certifications, et prennent en charge les exigences de conformité.

>[!NOTE]
>
>Les relevés de notes des élèves n&#39;affichent pas la colonne **Méthode d&#39;achèvement**. Cette colonne est disponible uniquement dans le relevé de notes de l’élève administrateur.

## Logique de la date d&#39;achèvement pour les suppléants

La colonne **Date d&#39;achèvement** du relevé de notes de l&#39;élève est utilisée pour les achèvements directs et alternatifs.

- Pour d’autres achèvements, la date reflète la date à laquelle l’élève a terminé le cours ou le parcours source.
- Si l’élève termine directement la cible ultérieurement, la date d’achèvement est mise à jour en fonction de la date d’achèvement directe.
- Aucune nouvelle colonne n&#39;est introduite pour les autres dates d&#39;achèvement.
- Si plusieurs origines proposent une autre date de fin, la date de fin active la plus ancienne est utilisée.
- Si une source est révoquée (avec l&#39;option d&#39;inachèvement rétroactif activée), la date est mise à jour vers la source active la plus récente suivante ou est effacée s&#39;il ne reste aucune source active.

**Impact** : garantit un suivi historique précis et un reporting cohérent, même lorsque les relations alternatives évoluent au fil du temps.

## Autres déclarations de production révoquées

Les autres achèvements révoqués se produisent lorsque toutes les relations source pour un cours ou un parcours d’apprentissage cible sont supprimées, à condition que l’inachèvement rétroactif soit activé.

### Conditions de déclenchement

- L’inachèvement rétroactif doit être activé au niveau du compte.
- La révocation ne se produit que lorsque **toutes** relations de source actives sont supprimées.
- S&#39;il reste au moins une source, l&#39;autre achèvement persiste et la colonne source d&#39;achèvement est mise à jour en conséquence.

### Impact sur le relevé de notes de l’élève

- **État** : si toutes les autres finalisations sont révoquées et qu&#39;il n&#39;y a pas d&#39;achèvement direct, le statut est mis à jour (par exemple, de **Terminé** à **Non commencé** ou **En cours**).
- **Date d&#39;achèvement** : effacée s&#39;il ne reste aucune source active et s&#39;il n&#39;y a pas d&#39;achèvement direct.
- **Source d&#39;achèvement** : mise à jour pour supprimer les sources révoquées ; effacé si toutes les sources sont révoquées.

Si l’élève a une fin directe, la révocation d’autres sources n’affecte pas l’état d’achèvement ou la date d’achèvement.

>[!NOTE]
>
>Si plusieurs sources ont fourni une autre fin de production et que seules certaines sont révoquées, le relevé de notes reflète les sources actives restantes et leur date d&#39;achèvement la plus ancienne. Si toutes les sources sont révoquées et qu’il n’y a pas d’achèvement direct, l’élève perd l’état d’achèvement pour la cible.

## Rapport amélioré pour les remarques des réviseurs de listes de contrôle

Cette modification s’applique uniformément à toutes les sources LT d’administration (exportations d’interface utilisateur, rapports d’API de tâche et connecteurs, le cas échéant). LT exporté par connecteur affichera les remarques du réviseur dans une colonne dédiée à la fin (pour les connecteurs qui n’exposaient pas précédemment le commentaire de soumission), ce qui garantit que les intégrations en aval peuvent distinguer le retour du réviseur des autres commentaires.

>[!NOTE]
>
>Pour les relevés de notes des élèves, la colonne précédemment intitulée **Commentaire de soumission** est désormais renommée **Remarques du réviseur** et remplie avec le commentaire du réviseur de la liste de contrôle lorsqu&#39;elle est activée.

## Amélioration du calcul du temps d’apprentissage

Le rapport Relevé de notes de l’élève utilise désormais une logique raffinée pour distinguer les périodes d’apprentissage actives et inactives en fonction de l’activité de l’utilisateur et du focus de l’onglet du navigateur.

**Impact** : fournit une mesure plus précise de l&#39;engagement des élèves, en prenant en charge les rapports et analyses de conformité.
