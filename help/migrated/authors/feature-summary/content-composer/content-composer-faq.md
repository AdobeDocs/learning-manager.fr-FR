---
description: Trouvez des réponses aux questions les plus fréquentes sur le compositeur de contenu, notamment pourquoi l’option Générer le contour est grisée, comment renommer une leçon, pourquoi les questions du quiz semblent mal alignées et ce qu’il faut faire lorsque Publish est désactivé.
jcr-language: en_us
title: FAQ sur Adobe Learning Manager Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---


# FAQ sur Adobe Learning Manager Content Composer

Obtenez des réponses aux questions fréquemment posées sur l’utilisation du compositeur de contenu.

**Le bouton Générer le contour est grisé. Que dois-je faire ?**

Les trois champs **Courte**, **Titre**, **Élèves** et **Objectif** doivent contenir du contenu avant l&#39;activation de la fonctionnalité **Générer l&#39;aperçu**. Dans la zone de travail, recherchez tout champ affichant encore du texte de substitution en italique, tel que *Entrez le profil des élèves ici* ou *Entrez l’objectif de ce cours*. Renseignez le champ vide et le bouton s’active immédiatement.

**Je ne peux pas sélectionner le plan pour renommer une leçon. Pourquoi ?**

La modification des contours est conversationnelle dans la version Beta actuelle. Vous ne pouvez pas sélectionner une leçon ou une rubrique sur la zone de travail pour la renommer ou la réorganiser. Saisissez vos modifications en langage clair dans le panneau de conversation de l’assistant.

Exemples :

- « Renommez la leçon 1 en « Fonctionnement du phishing » »

- « Déplacer le sujet 1.3 pour qu’il devienne le premier sujet de la leçon 2 »

- « Supprimer la leçon 4 et répartir ses rubriques dans la leçon 3 »

**Le contour généré ne correspond pas à ce que je voulais. Que s&#39;est-il passé ?**

Le plan reflète l’invite et le bref. Si la structure semble incorrecte, les causes les plus courantes sont une invite qui couvre trop de sujets à la fois ou un objectif d&#39;apprentissage qui ne nomme pas les compétences ou comportements spécifiques que le cours doit développer.

**L&#39;IA a ignoré une section importante de mon fichier chargé. Comment résoudre ce problème ?**

Le compositeur de contenu donne la priorité aux sections de votre fichier source qui sont les plus pertinentes pour votre objectif d’apprentissage. Si une section a été ignorée, cela n&#39;a probablement pas été reflété dans l&#39;objectif.

Pour résoudre ce problème :

1. Revenez au panneau **Courte** et mettez à jour l&#39;objectif pour nommer explicitement la rubrique manquante.

2. Demandez à l&#39;assistant de régénérer l&#39;outline : « Régénérez l&#39;outline en veillant à inclure la section de stratégie de rétention des données. »

Vous pouvez également ajouter manuellement le contenu manquant en tant que nouveau sujet dans la conversation de l&#39;outline : « Ajouter un nouveau sujet à la leçon 2 appelé « Stratégie de rétention des données ». »

**Puis-je utiliser le compositeur de contenu avec Adobe Captivate ?**

Non. Content Composer et Adobe Captivate ne partagent pas de workflow aller-retour. Vous ne pouvez pas ouvrir les projets du compositeur de contenu dans le Captivate, ni les projets du Captivate dans le compositeur de contenu.

Un fichier MP4 exporté dans un Captivate peut être inséré en tant que composant **Vidéo** dans le compositeur de contenu.

**Puis-je utiliser Content Composer pour la conformité ou une formation réglementée ?**

Oui. C&#39;est l&#39;un de ses cas les plus convaincants. Chargez vos documents de stratégie ou de procédure dans Gérer les fichiers sources et sélectionnez Restreindre la sortie au contenu dans les fichiers afin que l’IA ne génère qu’à partir de ce que vous avez fourni au lieu de compléter avec des connaissances générales.

**Pourquoi les vérifications de connaissances ne sont-elles pas notées ?**

Les vérifications de connaissances dans le compositeur de contenu sont conçues pour apprendre le renforcement au cours d’une leçon, et non pour la notation. Ils fournissent un retour d’informations immédiat à l’élève, mais ne produisent pas d’enregistrement de note ou d’achèvement.

Seules les évaluations de quiz de fin de leçon sont notées. Si vous avez besoin d’une évaluation qui contribue au score d’un élève, utilisez le quiz, et non un composant de vérification des connaissances.

**Les questions du quiz ne correspondent pas à ce que le cours enseigne. Comment résoudre ce problème ?**

Le compositeur de contenu utilise l&#39;IA pour générer des questions de quiz, et la sortie IA est non déterministe. Les questions ne reflètent pas toujours exactement ce à quoi vous vous attendez. Passez en revue toutes les questions du quiz après la génération du cours, modifiez celles qui nécessitent un ajustement directement dans l&#39;éditeur de cours et vérifiez que le contenu est exact avant de le publier.
