---
description: Découvrez comment le widget Conformité des élèves répertorie chaque instance inscrite à un cours auquel plusieurs élèves ont une échéance, et comment l’API la prend en charge
jcr-language: en_us
title: Les cours auxquels plusieurs élèves sont inscrits s’afficheront dans le widget Conformité des élèves
exl-id: 6484c815-ecae-4a75-ba10-ef42e4ff50a6
source-git-commit: d762bc8f199b703169878acbb52d0d7e3e0d6973
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%
---

# Cours auxquels plusieurs élèves sont inscrits dans le widget Conformité des élèves

Dans Adobe Learning Manager, un élève peut être inscrit à plusieurs instances du même cours. Le widget Conformité des élèves répertorie désormais chaque instance inscrite avec une échéance, de sorte que les élèves voient chaque date d&#39;échéance au lieu de seulement l&#39;instance principale.

## Modifications apportées aux cours avec inscriptions multiples

Avant cette modification, le widget Conformité affichait uniquement l’instance principale d’un cours auquel plusieurs élèves étaient inscrits. Un élève inscrit dans plusieurs instances ne pouvait pas voir les échéances des autres dans le widget.

Désormais, le widget Conformité affiche chaque instance qui remplit toutes ces conditions :

* L’élève est inscrit à l’instance.
* L&#39;instance a une échéance.
* L’élève n’a pas terminé l’instance.

Chaque entrée affiche le nom de l’instance, afin que les élèves puissent distinguer les instances du même cours. Lorsqu’un élève sélectionne une entrée, Adobe Learning Manager ouvre directement cette instance.

Par exemple, un élève termine un cours de formation initiale. Un administrateur inscrit ensuite l’élève aux éditions de septembre, octobre et novembre du même cours, avec une date limite pour chacune. Le widget Conformité répertorie les trois éditions.

Le widget compte chaque instance séparément dans chaque catégorie de conformité : **En retard**, **Échéance à venir dans les 30 prochains jours** et **En cours**.

## Instances qui apparaissent dans le widget Conformité

Le tableau suivant décrit comment le widget traite chaque situation d’inscription.

| Situation d’inscription | Apparaît dans le widget | Notes |
|--------------------------------------------------|-----------------------------------|---------------------------------------|
| Inscrit, l&#39;instance a une échéance, non terminée | Oui | Affiché avec le nom de l’instance |
| Inscrit, l&#39;instance n&#39;a pas d&#39;échéance | Non | Seules les instances avec une échéance apparaissent |
| Instance terminée | Non | Une instance terminée n&#39;est pas répertoriée |
| Terminé dans toutes les instances inscrites | Non | Le cours n&#39;apparaît plus |
| Une instance avec une échéance et une autre sans échéance | Seule l’instance avec une échéance |                                       |
| Une seule instance inscrite | Oui | Le widget affiche cette instance |

Voir [Prise en charge des API pour les instances multi-inscrites dans l&#39;application de l&#39;élève](/help/migrated/api-changes-dec-2026.md#multi-enrolled-compliance-widget) pour plus d&#39;informations sur les API.
