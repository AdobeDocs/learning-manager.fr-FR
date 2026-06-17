---
description: L'inscription en un clic permet aux élèves de cliquer sur n'importe quel lien profond vers un module partagé par les administrateurs et d'accéder immédiatement au contenu sans passer par plusieurs étapes pour cliquer sur s'inscrire puis commencer le cours. Cela permet de gagner du temps et d’améliorer l’accès aux cours.
jcr-language: en_us
title: Configuration de l’inscription en un clic dans Adobe Learning Manager
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Configuration de l’inscription en un clic dans Adobe Learning Manager

## Fonctionnement de l’inscription en un clic

L’inscription en un clic repose sur la combinaison de deux fonctionnalités Adobe Learning Manager (ALM) :
Les liens profonds fournissent une URL directe vers un cours ou un objet d’apprentissage spécifique dans ALM. Vous pouvez incorporer ces liens (qui sont des URL directes vers des modules) dans des e-mails, des portails intranet ou des applications tierces. Si un élève n’est pas déjà connecté lorsqu’il clique sur le lien, ALM l’invite à s’authentifier, puis l’amène directement au cours.

Elle est généralement utile lorsque les élèves sont en plein travail et utilisent le Slack ou les équipes, ou lorsqu’ils ont besoin d’une formation de deux minutes avant de voyager ou d’assister à une réunion ou à un appel commercial. Ils peuvent accéder au contenu immédiatement et se former.
Les services liés à l’inscription inscrivent automatiquement un élève à un cours avant que le lien profond ne lance le lecteur de cours. Cela supprime l’étape d’inscription manuelle qui, sinon, interromprait l’expérience de l’élève.

Lorsqu&#39;un élève sélectionne un lien d&#39;inscription en un clic, ALM l&#39;inscrit via l&#39;API en arrière-plan, puis le redirige vers le cours à l&#39;aide du lien profond. Le lecteur de cours s&#39;ouvre immédiatement.

>[!NOTE]
>
>L’inscription se produit au niveau du cours uniquement, et non au niveau des objets d’apprentissage de niveau supérieur (parcours d’apprentissage ou certifications).

## Génération d’un lien profond pour un module

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **Cours** dans le volet de navigation de gauche.
   ![](assets/one-click-enroll1.png)
3. Sélectionner un cours
4. Sélectionnez **Instances**.
   ![](assets/one-click-enroll2.png)
5. Sélectionnez la section **Module** l&#39;instance dont vous souhaitez copier les liens profonds des modules. Les détails du module s&#39;affichent dans la section développée au bas de l&#39;instance.
   ![](assets/one-click-enroll3.png)
6. Accédez au module dont vous souhaitez copier le lien.
   ![](assets/one-click-enroll4.png)
7. Sélectionnez **Copier le lien**. Le lien profond est maintenant copié. Ce lien profond est un lien permettant d&#39;ouvrir le module particulier dans un cours.

Vous pouvez désormais utiliser ce lien profond pour l’envoyer à un élève.
