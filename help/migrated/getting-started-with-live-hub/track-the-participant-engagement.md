---
title: Suivi de l’engagement des participants
description: Découvrez comment les instructeurs utilisent l’indicateur d’engagement des participants en temps réel dans Live Hub pour surveiller la mise au point du navigateur, l’activité de conversation et la participation aux sondages.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 5d89078fff50bbd3be1a2d01085efd568b8e0130
workflow-type: tm+mt
source-wordcount: '1408'
ht-degree: 0%
---

# Suivi de l’engagement des participants

L’engagement des participants dans le hub en direct offre aux instructeurs une vue en temps réel de l’engagement des élèves ou des participants au cours d’une session en direct. Il combine la mise au point du navigateur, l’activité de chat et la participation aux sondages dans un seul niveau d’engagement, affiché sous la forme d’un indicateur vert, jaune ou rouge. Utilisez-le pour repérer les trempettes et ajuster votre livraison en temps réel.

L’engagement du participant affiche le niveau d’engagement moyen de tous les élèves dans la salle principale à un moment donné. Le niveau est actualisé dès qu’un élève rejoint la session.

L’engagement du participant est calculé et affiché uniquement pendant une session en direct.

>[!NOTE]
>
> Seuls les instructeurs peuvent voir l’engagement du participant. Les élèves n&#39;y ont pas accès.

## Comprendre les calculs du niveau d’engagement

Le score d’engagement du participant vous aide à surveiller l’attention de l’élève en temps réel pendant une session en direct. Ce badge d&#39;engagement en haut de l&#39;écran affiche le niveau d&#39;engagement global comme **Faible**, **Moyen** ou **Élevé**, ce qui vous permet d&#39;ajuster l&#39;organisation de votre session et d&#39;encourager la participation si nécessaire.

L’indicateur est visible uniquement par les instructeurs dans la salle principale.

![Indicateur de niveau d’engagement](assets/engagement-level-indicator.png)
*L’interface Live Hub affiche l’engagement du participant dans le coin supérieur droit.*

## Comment le score d’engagement est-il calculé ?

Chaque élève ou participant a un score d’engagement compris entre 0 et 100, en fonction des facteurs suivants :

- **Attention portée à la session** : lorsqu&#39;un élève ou un participant garde la fenêtre de session active, son niveau d&#39;engagement est Élevé par défaut. S’ils passent à une autre fenêtre ou à un autre onglet du navigateur, leur niveau d’engagement passe à Faible, sauf s’ils continuent à participer aux activités de la session.
- **Participation à la session** : les activités telles que parler, partager un écran, envoyer des messages de chat, répondre à des sondages ou à des questionnaires, dessiner sur le tableau blanc, lever une main, envoyer des réactions et cliquer au sein de la session augmentent le score d&#39;engagement.

### Modification des scores d’engagement

Le score d’engagement de l’élève change tout au long d’une session en direct en fonction de son attention et de sa participation. Les conditions suivantes affectent la façon dont le score d’engagement est calculé :

- **Durée de l’activité** : la plupart des activités de participation augmentent temporairement le score d’engagement, leur contribution diminuant progressivement sur environ cinq minutes. Par exemple, si un élève parle pendant une session, puis passe à une autre fenêtre, son score d’engagement diminue progressivement plutôt que immédiatement
- **Partage d’écran** : le score d’engagement reste à 100 lorsqu’un élève ou un participant partage son écran.
- **Activités simultanées** : lorsqu’un élève ou un participant exécute plusieurs activités simultanément, seule l’activité présentant la valeur d’engagement la plus élevée est prise en compte. Les scores des activités individuelles ne sont pas combinés, ce qui garantit que le score de l’engagement ne dépasse pas 100.
- **Plusieurs appareils** : si un élève ou un participant rejoint la session à partir de plusieurs appareils, le score d’engagement le plus élevé entre ces appareils est pris en compte.

## Score global de l’engagement

Le badge d’engagement du participant affiche le niveau d’engagement global en fonction du score d’engagement moyen de tous les élèves dans la salle principale, arrondi au nombre entier le plus proche.

Les conditions suivantes s’appliquent lors du calcul du score d’engagement global :
- **Instructeurs et robots d’enregistrement** : les instructeurs et les robots d’enregistrement sont exclus du calcul du score d’engagement global. Les robots d&#39;enregistrement n&#39;apparaissent pas dans la liste des participants.
- **Salles de réunion** : les élèves ou les participants dans les salles de réunion ne sont pas inclus dans le score global de l’engagement. Lorsque les élèves passent de la salle principale à une salle de réunion, leurs scores d&#39;engagement individuels sont réinitialisés et recalculés dans les une à deux minutes qui suivent.
- **Nouveaux élèves** : le score d’engagement du participant devient disponible environ une minute après avoir rejoint la session. Tant que le score n’est pas disponible, l’élève ou le participant est exclu du calcul du score global de l’engagement.
- **Salle principale vide** : lorsqu’aucun élève ou participant n’est présent dans la salle principale, le badge affiche l’engagement du participant sans niveau d’engagement.

## Identification des niveaux d’engagement et des indicateurs

Le badge d’engagement du participant affiche l’un des niveaux d’engagement suivants en fonction du score global de l’engagement. Vous pouvez utiliser ces niveaux pour surveiller l’attention de l’élève et ajuster la prestation de la session selon vos besoins.  Voici ce que signifie chaque niveau :

| **Niveau d&#39;engagement** | **Score** | **Description** |
|----|----|----|
| Elevé | 61 à 100 | Les élèves participent activement à la session. |
| Moyen | 31 à 60 | Les élèves montrent des interactions occasionnelles avec une participation modérée. |
| Faible | 0 à 30 | Les élèves montrent peu ou pas d&#39;interaction ou une mise au point réduite pendant la session. |

>[!NOTE]
>
> - Le score de l’engagement indique l’attention portée aux participants pendant une session. Il ne mesure pas les résultats d’apprentissage ou le rendement.
> 
> - Les scores d’engagement sont calculés toutes les minutes. Les modifications peuvent prendre jusqu’à deux minutes pour apparaître dans la pastille d’engagement.

## Forum aux questions

+++ Le score de l’engagement détecte-t-il si un participant regarde activement la session ?

Non. Le score d’engagement est calculé en fonction de l’activation ou non de la fenêtre de session et des activités du participant, telles que parler, envoyer des messages instantanés et répondre aux sondages. Il n’utilise pas la vidéo en caméra, le suivi des yeux ou le statut muet du microphone pour mesurer l’engagement.

+++

+++ Que se passe-t-il lorsqu’un participant quitte la fenêtre de session ?

Lorsqu’un participant bascule vers un autre onglet, une autre fenêtre ou une autre application du navigateur, la fenêtre de session n’est plus considérée comme active. Même si la fenêtre de session reste visible, elle est considérée comme inactive lorsqu’une autre fenêtre est active.

+++

+++ Toutes les activités de participation contribuent-elles de manière égale au score d’engagement ?

Parler, partager un écran, envoyer des messages de chat, répondre à des sondages ou à des questionnaires, dessiner sur le tableau blanc, lever la main et envoyer des réactions contribuent également au score de fiançailles. Cliquer au sein de la session contribue légèrement moins.

+++

+++ Comment le score de l’engagement change-t-il après une activité de participation ?

La contribution de la plupart des activités de participation diminue graduellement en environ cinq minutes. Par exemple, si un participant passe à une autre fenêtre, puis parle, son score d’engagement passe à 100 lors de la mise à jour suivante. Au cours des minutes suivantes, le score diminue progressivement à 80, 60, 40 et 20, où il reste jusqu’à ce que le participant revienne à la fenêtre de session ou participe à nouveau.

Un participant qui garde la fenêtre de session active conserve un niveau d’engagement élevé.

+++

+++ Les participants des salles de réunion sont-ils inclus dans le score global de l’engagement ?

Non. Seuls les participants de la salle principale sont inclus dans le calcul du score global de l’engagement. Le badge d’engagement ne s’affiche pas lorsqu’un instructeur se trouve dans une salle de réunion.

+++

+++ Pourquoi le score d’engagement global diminue-t-il après la fin des salles de réunion ?

Lorsque les participants passent des salles de petits groupes à la salle principale, leur score d&#39;engagement individuel est réinitialisé et recalculé dans un délai d&#39;une à deux minutes. Cela peut temporairement diminuer le score d’engagement global.

+++

+++ Comment le score d’engagement est-il calculé lorsqu’un participant rejoint l’équipe à partir de plusieurs appareils ?

Si un participant rejoint la session à partir de plusieurs appareils, le score d’engagement le plus élevé entre ces appareils est pris en compte. Une session inactive sur un périphérique ne réduit pas le score d’engagement enregistré sur un autre périphérique actif.

+++

+++ Pourquoi la mise à jour du badge d’engagement prend-elle jusqu’à deux minutes ?

Le score d’engagement de chaque participant est calculé une fois par minute. Le score d’engagement global est ensuite mis à jour une fois par minute, de sorte que les modifications peuvent prendre jusqu’à deux minutes pour apparaître dans la pastille d’engagement.

+++

+++ Que peuvent faire les instructeurs lorsque le badge d’engagement affiche Faible ?

Un niveau d’engagement faible indique que la plupart des participants ont quitté la fenêtre de session et ne participent pas activement. Les instructeurs peuvent utiliser des sondages, des quiz, des invites de discussion ou des questions de discussion pour encourager la participation et attirer l’attention des participants sur la session.

+++

+++ Les instructeurs peuvent-ils utiliser les scores d’engagement pour suivre l’assiduité ou évaluer les élèves ?

Les scores d’engagement fournissent une indication générale de l’attention et de l’activité des participants pendant une session. Un participant peut maintenir un niveau d’engagement élevé en maintenant la fenêtre de session active, même sans participer activement ou démontrer qu’il a appris. Par conséquent, les scores de l’engagement peuvent ne pas convenir pour évaluer les performances de l’élève ou suivre sa présence.

+++

+++ Les participants peuvent-ils consulter leurs scores d’engagement ?

Non. Le badge d’engagement est visible uniquement par les instructeurs.

+++

+++ Les instructeurs peuvent-ils afficher les scores d’engagement de chaque participant ?

Non. La pastille d’engagement affiche uniquement le score d’engagement global pour la salle principale. Les scores des participants individuels ne sont pas disponibles.

+++

+++ Les instructeurs peuvent-ils désactiver le suivi de l’engagement ?

Non. Le suivi de l’engagement est toujours activé et ne peut pas être désactivé.

+++

+++ Les scores d’engagement sont-ils disponibles dans les rapports ou l’historique des sessions ?

Non. Le badge d’engagement affiche uniquement le score d’engagement global actuel. Les scores d’engagement ne sont pas enregistrés ou inclus dans les rapports ou l’historique des sessions.

+++

+++ Les co-instructeurs peuvent-ils afficher le badge d’engagement ?

Oui. Les co-instructeurs peuvent également afficher le badge d’engagement au cours d’une session.

+++

+++ Comment les scores d’engagement sont-ils calculés sur les appareils mobiles ?

Les participants peuvent accéder aux sessions Live Hub via un navigateur mobile. Les scores d’engagement sont calculés à l’aide des mêmes critères que les navigateurs de bureau.

+++
