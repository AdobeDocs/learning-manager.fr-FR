---
description: L'inscription en un clic permet aux élèves de cliquer sur n'importe quel lien profond vers un module partagé par les administrateurs et d'accéder immédiatement au contenu sans passer par plusieurs étapes pour cliquer sur s'inscrire puis commencer le cours. Cela permet de gagner du temps et d’améliorer l’accès aux cours.
jcr-language: en_us
title: Utiliser l’inscription en un clic dans Adobe Learning Manager
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 1%

---


# Inscription en un clic dans Adobe Learning Manager

Recevez le lien profond de votre administrateur par e-mail, chat ou toute autre plate-forme de messagerie pour vous inscrire à un module de formation ou à un cours. Sélectionnez le lien pour vous inscrire instantanément et lancer le module, sans aucune étape supplémentaire.

## Inscrivez un élève et redirigez-le vers le cours

Notez les scénarios suivants et les actions correspondantes. En tant qu’élève, si vous cliquez sur le lien profond qui vous a été envoyé, l’un des événements suivants se produira en fonction du scénario dans lequel vous vous trouvez :

| SN | Scénario | Action |
| --- | --- | --- |
| 1 | Cours en un seul module et non ordonné | Vous serez automatiquement inscrit et le lecteur s’ouvrira. Vous devez appuyer sur Lecture pour lire la vidéo. |
| 2 | Cours multimodule et non ordonné | Vous serez automatiquement inscrit et vous accéderez au module particulier auquel le lien profond est lié. Vous devez appuyer sur Lecture pour lire la vidéo. |
| 3 | Cours multimodule et ordonné | Vous accéderez à la page Présentation avec un message indiquant que vous devez terminer les cours précédents avant de commencer le cours actuel au cas où vous n’auriez pas terminé les précédents. Dans ce cas, vous serez automatiquement inscrit et accéderez au premier module du cours. |
| 4 | Le cours comporte des conditions préalables | Si les conditions préalables sont remplies, vous pouvez lancer le module dans le lecteur. Appuyez sur Lecture pour lire la vidéo. S’ils ne sont pas terminés, le message suivant s’affiche : « Impossible d’ignorer les cours prérequis. Veuillez terminer tous les cours prérequis avant de commencer ce cours. |
| 5 | Cours avec liste d’attente | Vous serez inscrit. Vous atterrirez dans la page de présentation du cours et vous serez ajouté à la liste d’attente. Vous verrez également un message indiquant que le cours est sur liste d’attente. |
| 6 | Si vous êtes déjà inscrit au cours pour lequel un lien profond est généré. | Vous atterrirez sur le module et le lecteur se lancera. Appuyez sur Lecture pour lire la vidéo. |

## Statut d’authentification et comportement de la liaison approfondie

Outre les scénarios ci-dessus, deux autres comportements d’utilisateur sont liés à l’état d’authentification (connecté et déconnecté).

* Si vous cliquez sur un lien profond et que vous n’êtes pas connecté à Adobe Learning Manager, vous serez redirigé vers la page de connexion. Connectez-vous et le lien profond vous redirigera vers le module en question.

* Si vous cliquez sur un lien profond et que vous êtes connecté à Adobe Learning Manager, vous serez directement redirigé vers le module.

## Prise en charge immersive pour mobile et web

Les scénarios suivants s’appliquent aux versions mobiles et web de Adobe Learning Manager.

* Si vous ne disposez pas de la version pour ordinateur de Adobe Learning Manager et que vous recevez un lien profond, la sélection du lien vous redirigera vers la page de connexion de Adobe Learning Manager dans votre navigateur si vous n’êtes pas connecté à la version web ou mobile.
* Si vous ne disposez pas de la version pour ordinateur de Adobe Learning Manager et que vous recevez un lien profond, la sélection du lien vous redirigera directement vers le module de Adobe Learning Manager dans votre navigateur si vous êtes déjà connecté à la version web ou mobile.

## Lecture automatique restreinte au navigateur

Lorsque vous cliquez sur un lien profond, il vous redirige vers un module ou une page de connexion si vous n’êtes pas connecté. Si le module est une vidéo, le lecteur ne lira pas la vidéo automatiquement. Dans tous les cas, le navigateur empêche le lecteur de lire la vidéo automatiquement. Vous devez appuyer sur Lecture manuelle pour lire la vidéo.
