---
description: Découvrez comment Adobe Learning Manager marque les élèves comme participants lorsqu’ils regardent un enregistrement de session Adobe Connect, sans mises à jour manuelles
jcr-language: en_us
title: Suivi de l’assiduité via les vues d’enregistrement Adobe Connect
exl-id: f4cb951e-3cb1-4caf-b6b8-aec86b32f782
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 1%
---

# Suivi de l’assiduité via les vues d’enregistrement Adobe Connect

## Présentation

Adobe Learning Manager peut suivre l’assiduité aux sessions de classe virtuelle Adobe Connect grâce aux vues d’enregistrement. Lorsqu’un élève manque une session en direct mais regarde l’enregistrement sur Adobe Connect assez longtemps, Learning Manager marque l’élève comme ayant assisté à la session. L’élève termine ensuite le module de session et peut aller jusqu’à l’objet d’apprentissage auquel la session appartient.

Avant cette fonctionnalité, Learning Manager n’avait aucun moyen d’enregistrer l’assiduité des élèves qui regardaient un enregistrement Connect. Un élève qui avait manqué une session en direct n&#39;a pas pu la terminer et un instructeur a dû intervenir et marquer l&#39;assiduité manuellement. Cette fonctionnalité supprime cette étape manuelle. Adobe Connect indique qui a regardé quel enregistrement et pendant combien de temps, et Learning Manager compare la durée de visionnage avec les critères d’achèvement définis pour le compte.

Une fois que l’élève répond aux critères d’achèvement de la session enregistrée, les élèves sont marqués dans l’application d’administration.

L’ID de messagerie de l’élève doit être le même dans Adobe Learning Manager et Adobe Connect, car Adobe Learning Manager le redirige vers Adobe Connect à l’aide du même ID de messagerie.
La fréquence de synchronisation par défaut et l’intervalle le plus court que l’administrateur d’intégration peut définir sont d’une heure.


## Qui fait quoi

| Rôle | Ce qu&#39;ils font |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Gestion | Ouvre l’enregistrement de la session et le regarde après avoir manqué la session en direct. |
| L’instructeur | Démarre l’enregistrement pendant la session en direct. Un enregistrement et une transcription existent donc. |
| Administrateur d’intégration | Configure le compte Adobe Connect utilisé par la synchronisation de l’assiduité et définit la planification de la synchronisation, ou l’active ou la désactive. |
| Auteur ou gestionnaire de diffusion | Planifie les sessions de classe virtuelle et, pour les programmes de plusieurs jours, réutilise une salle persistante sur plusieurs jours. |
| Adobe Connect | Capture l’e-mail de chaque élève et l’heure de visionnage des enregistrements, et expose la liste des visionneuses d’enregistrements via une API. |

Chaque rôle joue un rôle distinct dans la gestion de l’assiduité basée sur l’enregistrement.

## Glossaire

| Terme | Signification |
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| Session de classe virtuelle | Une session de classe virtuelle hébergée sur Adobe Connect. |
| Formation virtuelle dirigée par un instructeur | Formation dispensée par un instructeur via des sessions de classe virtuelle. |
| Objet d’apprentissage | Un cours, par exemple, qui contient le module de session. |
| Salle persistante | Salle Adobe Connect pouvant être réutilisée pour plusieurs sessions, par exemple le jour 1, le jour 2 et le jour 3. |
| Critères de validation | Pourcentage de l’enregistrement qu’un élève doit regarder pour être marqué comme terminé pour le module. |

## Cas d’utilisation

### Un élève manque une session en direct

Un élève ne peut pas participer à la session de classe virtuelle en direct. Par la suite, l’élève ouvre la session dans Learning Manager et regarde l’enregistrement. Une fois que le temps de visionnage répond aux critères d’achèvement, Learning Manager marque l’élève comme ayant participé et l’élève termine le module sans demander de l’aide à l’instructeur.

### Un élève qui ne regarde que partiellement

Un élève ouvre l’enregistrement mais regarde moins que le partage requis. Les critères d’achèvement ne sont pas remplis, donc Learning Manager ne marque pas l’élève comme ayant participé.

### Sessions de plusieurs jours sur une salle persistante

Un auteur ou un responsable de prestation planifie des sessions pour les jours 1, 2 et 3 dans la même salle Connect persistante. Ils peuvent voir et réutiliser le nom de la salle sans se connecter à Adobe Connect.

## Fonctionnalités clés

| Fonctionnalité | Ce qu’il fait |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Présence automatique | Marque un élève comme ayant participé à une session de classe virtuelle basée sur Connect lorsqu’il regarde l’enregistrement suffisamment longtemps pour atteindre la limite de seuil prescrite. |
| Temps de visionnage à partir de Connect | Utilise l’adresse e-mail de l’élève et enregistre le temps de visionnage capturé par Adobe Connect. |
| Seuil des critères d’achèvement | Marque l’élève comme terminé pour le module lorsque le temps de veille atteint le pourcentage défini dans les critères d’achèvement. |
| Durée de visionnage réelle uniquement | Compte le temps qu’un élève a réellement regardé. Faire glisser la barre de recherche n’ajoute pas de temps de visionnage. |
| Synchronisation planifiée | Exécute un pipeline principal selon une planification contrôlée par l’administrateur de l’intégration et peut être activé ou désactivé. |
| Visibilité persistante de la salle | Affiche le nom de la salle Connect au niveau de l&#39;instance afin que les auteurs puissent réutiliser une salle persistante sur plusieurs jours. |

## Fonctionnement du suivi des présences

*D’un élève ouvrant l’enregistrement vers Learning Manager marquant le module comme terminé.*

### Flux de bout en bout

1. L’instructeur anime la session de classe virtuelle en direct sur Adobe Connect et démarre l’enregistrement. L&#39;enregistrement et la transcription deviennent disponibles après la session.

1. Un élève qui a manqué la session sélectionne l’enregistrement pour l’afficher. Adobe Connect effectue un suivi automatique de la vue.

1. Adobe Connect capture l’adresse e-mail de l’élève et le temps qu’il a réellement passé à regarder.

1. Dans la planification configurée, un pipeline SnapLogic principal appelle l’API Adobe Connect et extrait la liste des visionneuses d’enregistrement pour un cadre de temps donné. Le pipeline utilise le compte Adobe Connect configuré dans l’administrateur d’intégration.

1. Learning Manager mappe chaque visionneuse au cours et module correspondants.

1. Learning Manager compare le temps de visionnage total de l’élève avec les critères d’achèvement.

1. Si le temps de visionnage répond aux critères, Learning Manager marque l’élève comme ayant terminé le module. En arrière-plan, Learning Manager enregistre cela en renseignant le fichier CSV de niveau de cours de l’utilisateur.

>[!NOTE]
>
>Adobe Connect ne transmet pas les données à Learning Manager. Learning Manager l’affiche au niveau de l’instance Adobe Connect, par exemple « ces cinq utilisateurs ont regardé ces six enregistrements au cours des dernières 24 heures ». La présence est donc mise à jour après l’exécution du pipeline suivant, et non au moment où l’élève termine de regarder.

### Critères d’achèvement et durée de visionnage

L’élève doit consulter au moins le pourcentage de l’enregistrement défini par les critères d’achèvement. Gardez ces règles à l’esprit :

* Le pourcentage s’applique à la durée de l’enregistrement et non à la durée de la session planifiée. Si une session de 15 minutes est enregistrée pendant seulement 5 minutes, le temps requis est basé sur les 5 minutes. Adobe Connect fournit la durée d’enregistrement.

* Le pourcentage est défini côté Learning Manager. Il s’agit d’un paramètre commun à l’ensemble du compte, et non d’un paramètre pour chaque instance. Le même type de paramètre s’applique déjà aux sessions en direct, par exemple une participation de 80 %.

* Adobe Connect enregistre la durée de visionnage réelle par l’élève. Le fait de sauter à la barre de recherche ne compte pas et Learning Manager traite le temps de visionnage que Connect passe.

| Critères de validation | Longueur d’enregistrement | Temps de visionnage nécessaire | Résultat |
|-------------------------|------------------------------------|-----------------------|-------------------------------------------------------------|
| 50% | 5 minutes | 2,5 minutes | Marqué comme terminé une fois que 2,5 minutes ont été visionnées. |
| 50% | 5 minutes (la séance a duré 15 minutes) | 2,5 minutes | D’après l’enregistrement de 5 minutes, et non la session de 15 minutes. |
| 0% | Tout | Aucune au-delà de l’ouverture | L’ouverture de l’enregistrement suffit. |

### Fenêtre d’éligibilité

Learning Manager applique l’assiduité basée sur l’enregistrement uniquement jusqu’à la date d’achèvement de l’objet d’apprentissage. Si l’objet d’apprentissage n’a pas de date d’achèvement, Learning Manager utilise la date d’achèvement de l’objet d’apprentissage parent.

### Planification de la synchronisation

L’administrateur d’intégration contrôle la fréquence d’exécution du pipeline. La planification peut être horaire ou hebdomadaire, entre autres intervalles, et l’administrateur d’intégration peut l’activer ou le désactiver. Le même compte Adobe Connect est utilisé à chaque exécution.

### Modifications

* Lorsqu’un utilisateur ajoute la salle persistante créée pour le jour 1, Learning Manager lui donne accès à cette salle. Ils peuvent ensuite ajouter la même salle à des sessions les autres jours.
* Learning Manager affiche le nom de la salle de classe Connect au niveau de l’instance, dans les détails de la session à côté de l’**URL de salle de classe virtuelle**.
* Pour l’instance par défaut, Learning Manager affiche la salle configurée lors de la création du cours.

### Limitations et considérations

* La présence n’est pas en temps réel, car Learning Manager extrait les données d’un planning.
* La fonctionnalité couvre uniquement les sessions de classe virtuelle basées sur Connect.
* Un enregistrement doit exister. L’instructeur doit donc lancer l’enregistrement pendant la session en direct.
* Les élèves sont mis en correspondance via l’adresse e-mail saisie par Adobe Connect.
* Faire glisser la barre de recherche n’ajoute pas de temps de visionnage.
* L’assiduité basée sur l’enregistrement s’arrête à la date d’achèvement de l’objet d’apprentissage ou de l’objet d’apprentissage parent.

### Points à retenir

* Le temps de visionnage doit être supérieur ou égal au pourcentage prescrit (par exemple, 50 % de 5 minutes correspond à 2,5 minutes). Le temps de visionnage ne s’additionne pas si l’élève regarde la session de manière répétée mais reste en deçà du temps de visionnage prescrit. Cependant, la durée de visionnage s’additionne même si l’élève regarde la session à différents moments dans des parties et répond aux critères de seuil. Par exemple, si un élève regarde une minute de la session le jour 1, puis une autre minute 1,5 minute de la session le jour suivant à partir du point où il est parti, le temps de veille s’additionne. Cela se produit du côté d’Adobe Connect.

* Les critères d’achèvement peuvent être configurés au niveau du cours et du compte. L’effet est identique à la participation à la session en direct.

* La fréquence de synchronisation par défaut et l’intervalle le plus court que l’administrateur d’intégration peut définir sont d’une heure.

* L’ID de messagerie de l’élève doit être le même dans Adobe Learning Manager et Adobe Connect, car Adobe Learning Manager le redirige vers Adobe Connect à l’aide du même ID de messagerie.

### FAQ

**Q. L’élève doit-il assister à la session en direct ?**
**A.** Non. Un élève qui manque la session en direct peut toujours être marqué comme ayant participé en regardant l’enregistrement suffisamment longtemps.

**Q. Quelle partie de l’enregistrement l’élève doit-il regarder ?**
**A.** Pourcentage dans les critères d&#39;achèvement, appliqué à la durée d&#39;enregistrement. Par exemple, à 50 %, un enregistrement de 5 minutes nécessite au moins 2,5 minutes de temps de visionnage.

**Q. Le fait de sauter l’enregistrement en avant compte-t-il ?**
**A.** Non. Adobe Connect enregistre le temps que l’élève a réellement regardé. Faire glisser la barre de recherche ne compte donc pas.

**Q. L’assiduité est-elle marquée dès que l’élève a terminé de regarder ?**
**A.** Non. Learning Manager extrait les données de la visionneuse d’Adobe Connect selon un calendrier, de sorte que l’assiduité est mise à jour après l’exécution du pipeline suivant.

**Q. Adobe Connect envoie-t-il les données à Learning Manager ?**
**A.** Non. Learning Manager l’extrait. Il s’agit d’un mécanisme de traction au niveau de l’instance Adobe Connect, pas d’un mécanisme de poussée.

**Q. Comment Learning Manager sait-il quel élève a regardé ?**
**A.** Adobe Connect capture l’adresse e-mail de l’élève et l’heure de visionnage de l’enregistrement. Learning Manager mappe cela au cours et au module.

**Q. Qui contrôle la fréquence d’exécution de la synchronisation ?**
**A.** L’administrateur d’intégration définit la planification et peut l’activer ou la désactiver.

**Q. Le pourcentage d’achèvement est-il défini pour chaque instance ?**
**A.** Non. Il s’agit d’un paramètre courant dans l’ensemble du compte.

**Q. Les sessions de plusieurs jours peuvent-elles partager une salle Connect ?**
**A.** Oui. Les auteurs peuvent réutiliser la salle persistante créée pour le jour 1 sur les sessions pour d’autres jours, et le nom de la salle apparaît au niveau de l’instance dans Learning Manager.
