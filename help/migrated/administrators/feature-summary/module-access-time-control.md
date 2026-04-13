---
description: Définissez une fenêtre temporelle pendant laquelle les élèves sont autorisés à démarrer un module.
jcr-language: en_us
title: Contrôle du temps d'accès au module
contentowner: mmanuel
source-git-commit: 6423fd5c0853705a28c6c67b6936d93e68cbca20
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 1%

---

# Contrôle du temps d&#39;accès au module

## Présentation

L’amélioration permet aux auteurs et aux administrateurs de Adobe Learning Manager de définir une fenêtre temporelle pendant laquelle les élèves sont autorisés à démarrer un module. En dehors de la fenêtre de début/fin configurée, le module reste visible dans la structure du cours, mais les élèves ne peuvent pas le lancer.

Cette fonctionnalité est essentielle pour les utilisateurs qui ont besoin d’un contrôle plus strict sur le moment où certains contenus deviennent disponibles ou doivent cesser d’être initiés, par exemple, dans le cadre de programmes chronométrés, de formations en cohorte ou d’exercices sensibles au facteur temps.

## Nouveautés

Les auteurs peuvent désormais configurer, au niveau du module dans un cours, une date/heure de début et une date/heure de fin qui régissent le moment où les élèves sont autorisés à lancer ce module. Dans cette fenêtre, le module se comporte comme d&#39;habitude : avant l&#39;heure de début ou après l&#39;heure de fin, l&#39;élève voit le module dans l&#39;aperçu du cours mais ne peut pas le démarrer.
La configuration apparaît dans l&#39;interface utilisateur de création de cours sous forme de commandes de planification supplémentaires pour des types de module spécifiques, tels que le contenu d&#39;auto-apprentissage, les quiz ou les activités. Les administrateurs peuvent utiliser ces commandes pour créer des modules qui s’ouvrent par phases ou pour empêcher les démarrages tardifs dans les programmes où le contenu doit être consommé dans un délai défini.

## Principaux avantages

Le principal avantage est la possibilité de contrôler quand les modules sont accessibles. Les équipes de formation peuvent synchroniser la disponibilité des modules avec des événements réels, tels que les lancements de nouveaux produits, les délais réglementaires et les programmes internes. Cela garantit que les élèves terminent le contenu prérequis avant de pouvoir accéder aux modules suivants.
Par exemple, la cohorte 1 peut accéder au module 2 uniquement au cours de la semaine 2, tandis que le module 3 reste verrouillé jusqu’à la semaine 3, éliminant ainsi la nécessité de masquer et d’afficher manuellement le contenu ou de créer des versions de cours distinctes.
Cela améliore l’expérience de l’élève : au lieu de faire face à des modules qui sont techniquement accessibles mais qui ne devraient pas l’être à ce moment-là (ou qui devraient déjà être terminés), les élèves voient une structure de cours où les modules qu’ils sont autorisés à commencer sont clairement alignés sur le calendrier prévu.

## Cas d’utilisation

**Programme d&#39;accompagnement par cohorte** : dans ce programme, chaque semaine ouvre un nouveau module. Le contenu de la semaine 1 est disponible immédiatement, tandis que la semaine 2 est visible, mais ne peut pas être démarrée avant une date spécifiée. La semaine 3 suit le même processus de contrôle. Les élèves peuvent voir l’intégralité du parcours d’apprentissage, mais le système contrôle à quel moment ils peuvent réellement commencer chaque étape.
**Formation liée au produit ou à la campagne** : les équipes marketing ou produit peuvent créer un module de formation qui n’est accessible que lorsqu’une campagne est active ou lorsqu’une version spécifique d’un produit est toujours disponible. Cette fenêtre de début désignée permet de s’assurer que les élèves ne commencent pas un module sur une version de produit retirée après l’heure de fin spécifiée.
**Environnements d’évaluation ou d’examen** : les organisations peuvent ouvrir un module (tel qu’un test) pendant une courte période bien définie (par exemple, « vous pouvez commencer l’examen à tout moment entre 9:00 et 12:00 à une date donnée »). Les élèves ne peuvent pas commencer l&#39;examen en dehors de cette fenêtre, ce qui permet un planning équitable entre les fuseaux horaires et les cohortes.

## Définition du temps d&#39;accès au module

1. Connectez-vous à Adobe Learning Manager en tant qu’auteur.
2. Accédez à la section **Formation** > **Cours**. ALM affiche une liste de cours.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time1.png)
3. Sélectionnez le cours pour lequel vous souhaitez définir la restriction.
4. Sélectionnez **Instances**. ALM affiche une liste d’instances.
5. Sélectionnez **Modules** dans la section d&#39;instance pour laquelle vous souhaitez définir la limite d&#39;accès. Le bouton **Modifier** apparaît.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time2.png) ![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time3.png)
6. Sélectionnez **Modifier**. Les sections pertinentes liées au module s&#39;ouvrent vers le bas de la page.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time4.png)
7. Pour chaque section, sélectionnez une date de début, une heure de fin, une date de fin et une heure de fin.
8. Sélectionnez **Enregistrer**. ALM affiche un message indiquant « Mappage enregistré avec succès ».










