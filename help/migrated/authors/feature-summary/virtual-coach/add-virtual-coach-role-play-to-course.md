---
description: Apprenez à publier un jeu de rôle de coach virtuel pour faciliter votre travail, puis ajoutez-le à un cours dans le cadre d’un parcours d’apprentissage structuré
jcr-language: en_us
title: Ajout d’un jeu de rôle d’entraîneur virtuel à un cours
exl-id: c33ec5e4-0e96-4452-ada7-d48f9c71a123
source-git-commit: 8bde6827835a7f8cd8cc28f3d2c4014527e4a96c
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%
---

# Ajout d’un jeu de rôle d’entraîneur virtuel à un cours

Publish d’un jeu de rôle de coach virtuel pour faciliter la tâche, puis ajoutez-le à un cours afin que les élèves puissent y accéder dans le cadre d’un parcours d’apprentissage structuré.

Les jeux de rôle de coach virtuel ne sont pas ajoutés directement aux cours. Au lieu de cela, vous publiez d’abord le jeu de rôles en tant qu’assistance à la tâche, puis vous ajoutez cette assistance à la tâche à un cours en tant que module. Ce processus en deux étapes vous permet de réutiliser le même jeu de rôle dans plusieurs cours sans le dupliquer. Sous le capot, un jeu de rôle publié est ajouté à votre bibliothèque de contenu en tant que module LTI, ce qui permet de le déployer en tant qu’assistance à la tâche autonome ou en tant que module de cours. Avant de commencer, [créez et publiez un jeu de rôle d&#39;entraîneur virtuel](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md) si ce n&#39;est pas déjà fait.

## Ajout du jeu de rôle en tant qu’outil de travail

1. Dans le volet de navigation de gauche de la page d&#39;accueil de l&#39;auteur, sélectionnez **Assistances à la tâche**.
2. Sélectionnez **Créer** > **Virtual Coach** dans le coin supérieur droit.
3. Entrez un nom et une description pour l&#39;assistance à la tâche.
4. Sélectionnez le jeu de rôle **Virtual Coach** à utiliser dans le champ **Rechercher et sélectionner Virtual Coach**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach8.png)
   *Recherchez et sélectionnez le jeu de rôle publié que vous souhaitez transformer en assistance à la tâche.*

5. Définir la visibilité :
   - Conservez le paramètre **Partagé** par défaut pour permettre aux autres auteurs d&#39;affecter cette assistance à la tâche à leurs cours.
   - Sélectionnez **Privé** pour restreindre l&#39;accès à vos propres cours.
6. Éventuellement, entrez le temps d&#39;exécution attendu en minutes dans le champ **Durée**.
7. Dans le champ **Balises**, saisissez des mots-clés pour rendre l&#39;assistance à la tâche détectable dans la recherche et le catalogue.
8. Éventuellement, attribuez des compétences et des niveaux de compétence. Seules les compétences déjà présentes dans votre compte Adobe Learning Manager peuvent être utilisées. Les compétences ne peuvent pas être créées à partir de cet écran et leur affectation n’est pas obligatoire.
9. Sélectionnez **Enregistrer**. L’assistance à la tâche est publiée et disponible pour être ajoutée à un cours.

## Ajout du jeu de rôle à un cours

Une fois l’assistance à la tâche publiée, ajoutez-la à n’importe quel cours en tant que module. Le jeu de rôle apparaît aux élèves dans la séquence du cours avec d&#39;autres contenus, tels que des vidéos, des documents ou des quiz.

1. Dans le volet de navigation de gauche de la page d&#39;accueil de l&#39;auteur, sélectionnez **Cours**.
2. Ouvrez le cours auquel vous souhaitez ajouter le jeu de rôle ou sélectionnez **Créer** pour commencer un nouveau cours. Si vous ouvrez un cours existant, sélectionnez **Modifier** après son ouverture.
3. Ajoutez le nom et la description du cours.
4. Accédez à la section **Modules** de l&#39;éditeur de cours.
5. Il existe trois sections dans lesquelles vous pouvez ajouter des modules. Lorsque vous souhaitez sélectionner un coach virtuel, accédez à la première section intitulée **Contenu**, sélectionnez **Ajouter un module**, puis **Coach virtuel**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach18.png)

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach9.png)
   *Choisissez Virtual Coach comme type de module pour ajouter votre jeu de rôle publié à un cours.*

6. Recherchez le jeu de rôle Virtual Coach que vous avez créé et sélectionnez-le.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach10.png)
   *Recherchez l&#39;assistance à la tâche par nom ou par balise, puis cochez sa case pour l&#39;ajouter au cours.*

7. Sélectionnez **Ajouter**.
8. Configurez les critères d’achèvement et de réussite du module en fonction de la conception de votre cours.
9. Sélectionnez **Republier** si vous avez mis à jour un cours existant. Si vous avez mis à jour un cours existant, seul le bouton **Republier** s&#39;affiche. Sélectionnez **Enregistrer** si vous avez créé le cours à nouveau. Vous verrez uniquement le bouton **Enregistrer** si vous avez créé le cours à nouveau. Cliquez sur le bouton **Enregistrer** pour enregistrer le cours sous l&#39;onglet **Brouillon** dans la page Catalogue de cours. Pour publier le même cours, accédez au même cours dans la page **Catalogue de cours**, sélectionnez les points de suspension et sélectionnez **Cours Publish**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach19.png)

>[!NOTE]
>
>Toutes les mises à jour apportées à l’assistance à la tâche, y compris les modifications apportées au contenu du jeu de rôles, sont automatiquement répercutées dans tous les cours auxquels elle a été ajoutée. Si le jeu de rôles fait partie d’une évaluation formelle, republiez l’assistance à la tâche après avoir apporté des modifications afin que les élèves puissent voir la dernière version.

## Inclusion d’un coach virtuel dans un parcours d’apprentissage

Virtual Coach est conçu pour fonctionner au mieux comme le « dernier kilomètre » de la formation : le point où les élèves démontrent qu&#39;ils peuvent appliquer ce qu&#39;ils viennent d&#39;apprendre, plutôt qu&#39;une activité autonome. Compressez le jeu de rôles dans un cours ou un parcours d’apprentissage avec le contenu associé, et diffusez le lien du cours par e-mail ou d’autres communications de gestion du changement afin que les élèves sachent exactement quand et pourquoi le terminer.

Cette approche de packaging s&#39;applique bien à plusieurs déploiements courants :

- **Intégration et montée en puissance d’une nouvelle personne embauchée**, où le jeu de rôle suit le contenu d’intégration et confirme qu’une nouvelle personne embauchée est prête pour sa première conversation en direct.
- **Certification et renforcement des ventes**, où le jeu de rôle est le point de contrôle de certification à la fin d’un cours d’activation commerciale.
- **Préparation au lancement du produit**, où le jeu de rôle suit la formation au lancement et confirme que les représentants peuvent positionner le nouveau produit avant sa mise sur le marché, par exemple, le scénario de préparation au lancement du produit décrit dans [Qu&#39;est-ce que Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md), où un représentant doit adapter sa présentation au sein d&#39;un comité d&#39;achat à plusieurs personnes.
- **Leadership et encadrement des responsables**, où le jeu de rôle suit un cours de compétences en gestion et précède une véritable conversation sur les performances.
- **Programmes de préparation des partenaires**, où le jeu de rôle confirme qu&#39;un partenaire externe peut représenter correctement votre produit avant qu&#39;il ne soit certifié.
- **Formation à la communication et à la gestion des changements**, où le jeu de rôle renforce un nouveau processus ou un message de réorganisation une fois que les employés ont terminé le contenu associé.

Une fois que les élèves ont trouvé et commencé le jeu de rôle, consultez [Entraînez-vous avec Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/practice-role-play-with-virtual-coach.md) pour savoir ce qu&#39;ils vont découvrir.
