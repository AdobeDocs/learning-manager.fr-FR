---
description: L’assistant AI (Beta) pour les élèves est un compagnon de conversation alimenté par GenAI dans Adobe Learning Manager qui aide les élèves à obtenir des réponses rapides et précises à partir du contenu d’apprentissage qui leur est attribué. À l’aide de requêtes en langage naturel, les élèves peuvent récupérer instantanément des réponses ciblées avec des citations claires, ce qui facilite la recherche des bonnes informations, la vérification des sources et l’apprentissage efficace sans devoir rechercher dans des cours entiers.
jcr-language: en_us
title: Assistant IA pour les élèves dans Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 583074cf56b7c468d0027ea6bb4ed500f57e5421
workflow-type: tm+mt
source-wordcount: '1872'
ht-degree: 0%

---

# Assistant d’IA pour les élèves

L’assistant AI (Beta) pour les élèves les aide à trouver rapidement des réponses à partir du contenu d’apprentissage attribué sans parcourir l’intégralité des cours. Vous pouvez poser des questions dans un langage simple et recevoir des réponses précises et ciblées avec des liens sources vers le contenu du cours concerné.

>[!IMPORTANT]
>
>L’assistant AI pour les élèves est actuellement disponible en tant que fonctionnalité Beta. Les capacités, les scénarios pris en charge et les limitations peuvent changer au fur et à mesure de l’évolution de la fonctionnalité.


## Qu’est-ce que l’assistant IA pour les élèves ?

L’assistant AI est un compagnon de chat alimenté par l’IA générative dans Adobe Learning Manager qui fournit des réponses rapides et précises à l’aide de votre contenu d’apprentissage de confiance. Il comprend des citations afin que vous sachiez toujours la source de l&#39;information.

### Capacités

- **Réponse intelligente à une question**
   - Conversations à tour unique et à plusieurs tours
   - Compréhension du langage naturel en anglais
   - Réponses dérivées de cours, certifications, parcours d’apprentissage et assistances à la tâche
   - Questions intelligentes de clarification lorsque les requêtes sont ambiguës

- **Sources de contenu et citations**
   - Récupère les réponses des ressources disponibles dans les catalogues pris en charge
   - Fournit des citations avec des liens directs vers les matériaux sources
   - Prend en charge tous les formats de contenu Learning Manager (statique et interactif) : PDF, DOCX, PPTX, XLSX, audio (MP3, WAV, M4A), vidéo (MP4, MOV, WMV), HTML, SCORM 2004 et SCORM 1.2

- **Expérience utilisateur**
   - Interface du panneau latéral accessible à partir de toutes les pages de l’élève
   - Responsive design qui s’adapte à la zone de contenu
   - Historique de conversation conservé dans la session du navigateur
   - Nettoyer l’ardoise lors de la nouvelle connexion ou de l’actualisation de la page
   - Ton amical, clair et pédagogique

- **Contrôles administrateur**
   - Activer ou désactiver la fonctionnalité au niveau du compte
   - Contrôler l’accès par groupes d’utilisateurs
   - Sélectionner les catalogues inclus pour les réponses de l’IA
   - Exigences d’acceptation des Conditions d’utilisation conformément aux directives d’Adobe AI

## Types de contenu pris en charge

L’assistant AI récupère des informations à partir du contenu d’apprentissage qui vous a été attribué, notamment :

- **Documents :** PDF, Word, PowerPoint, Excel, HTML
- **Média :** audio (MP3, WAV, M4A), vidéo (MP4, MOV, WMV)
- **Contenu interactif :** SCORM 1.2, SCORM 2004
- **Types d’objets d’apprentissage :** cours, parcours d’apprentissage, certifications, assistances à la tâche

Adobe traite votre contenu d’apprentissage de manière sécurisée à l’aide de services approuvés.

### Limitations du catalogue et de la source de contenu

L&#39;Assistant IA utilise uniquement le contenu des catalogues **internes** qui sont explicitement configurés par les administrateurs.

Les sources de contenu suivantes ne sont pas prises en charge dans la version actuelle :

- Catalogues **partagés**
- Catalogues **acquis**
- Catalogues **externes**
- Catalogues **par défaut**
- Bibliothèques de contenu tierces (par exemple, LinkedIn Learning ou Go1)

Si vous n’avez pas accès à un cours ou à une assistance à la tâche, l’assistant IA ne fait pas apparaître les informations de ce contenu et les liens de citation ne sont pas accessibles.

## Cas d’utilisation

### Élève technique

Sarah est ingénieure commerciale et se familiarise avec les cartes graphiques. Elle doit comprendre rapidement les spécifications techniques et les avantages pour répondre aux questions des clients en toute confiance.

L’assistant AI aide Sarah à :

- Explication technique claire de l’architecture GPU complexe
- Compréhension approfondie des différentes cartes graphiques et de leurs différences
- Explication des exemples afin que Sarah puisse associer les fonctionnalités aux cas d’utilisation réels

### Service clientèle

Marcus est un spécialiste du support dans une entreprise partenaire. Il a besoin de réponses rapides sur les fonctionnalités des produits pour aider les clients sans passer par des équipes d’ingénieurs.

L’assistant AI aide Marcus à :

- Recherche de contenu de support pertinent pour les questions fréquemment posées des clients
- Poser des questions de clarification lorsque la réponse initiale n&#39;est pas assez précise
- Trouver des recommandations pour des cours de dépannage connexes pour améliorer ses compétences

### Intégration d’un nouvel employé

Jennifer vient de se joindre à l&#39;entreprise et est submergée par la quantité de matériel de formation. Elle a besoin d’un moyen de trouver des informations spécifiques sans passer en revue l’intégralité des cours.

L’assistant AI aide Jennifer à :

- Obtenir des conseils étape par étape sur la soumission des notes de frais
- Découverte de cours sur les politiques de l’entreprise sans parcourir l’ensemble du catalogue
- L’orienter vers la section appropriée d’un cours sans lui faire passer des heures de visionnage vidéo

## Utilisation du contenu par l’assistant AI

L’assistant AI trouve des réponses précises à partir de votre contenu d’apprentissage. Voici comment cela fonctionne.

### Contenu utilisé par l’assistant AI

L’assistant AI répond aux questions en utilisant uniquement le contenu d’apprentissage activé par l’administrateur de compte. Le contenu du catalogue sélectionné est indexé.

L’assistant AI analyse le contenu d’apprentissage qui vous est attribué pour générer des réponses contextuelles ciblées :

- Chaque réponse comprend des citations qui font référence au contenu source d’origine.
- Vous pouvez sélectionner une citation pour accéder directement au cours, module ou document concerné.
- Les citations vous aident à vérifier les informations et à explorer d’autres contextes si nécessaire.

### Réponses en flux continu

L&#39;assistant AI fournit les réponses progressivement au fur et à mesure de leur génération, de sorte que vous pouvez commencer à lire immédiatement sans attendre que la réponse complète se charge.

### Citations et transparence de la source

Chaque réponse de l&#39;assistant AI comprend des citations qui renvoient directement au cours, module ou objet d&#39;apprentissage d&#39;origine. Les citations vous permettent de :

- Sélectionnez un numéro de citation en ligne pour accéder à la section référencée exacte.
- Ouvrez la liste des sources complète en sélectionnant **Afficher les sources** au bas de la réponse.
- Vérifiez les informations et explorez le contexte supplémentaire à partir de la source faisant autorité.

> **IMPORTANT**
> L’assistant AI fournit des réponses basées sur le contenu activé par l’administrateur. Si vous n’avez pas accès à un élément référencé, un message « non pris en charge » s’affiche lorsque vous essayez de l’ouvrir.


## Invites intégrées

L’assistant AI inclut des invites intégrées pour vous aider à prendre rapidement en main les questions et les scénarios courants. Ces invites vous indiquent comment interagir avec l&#39;assistant et présentent les types de questions que vous pouvez lui poser.

![Invites intégrées fournies par l’Assistant Élève](assets/built-in-prompt-new.png)

Les organisations peuvent personnaliser les invites intégrées pour qu’elles reflètent leurs objectifs d’apprentissage, leurs rôles, la terminologie ou des cas d’utilisation spécifiques. Les administrateurs peuvent collaborer avec leur gestionnaire de succès client pour configurer ou mettre à jour les invites intégrées. Dans la version actuelle, vous ne pouvez pas personnaliser les invites directement dans l’interface de Adobe Learning Manager.

## Configuration de l’assistant AI (administrateurs)

![Assistant Élève compatible IA](assets/learner-ai-assistant-new.png)

Les administrateurs sélectionnent les groupes d&#39;utilisateurs et les catalogues **internes** qui peuvent accéder à la fonctionnalité de l&#39;Assistant IA. Assurez-vous que les catalogues que vous attribuez incluent uniquement le contenu d&#39;apprentissage approprié pour les réponses et les citations de l&#39;IA, et que ces catalogues sont **internes** (et non **partagés**, **acquis** ou **externes**).

Avant de configurer l’assistant AI, vérifiez que vous disposez d’informations d’identification d’administrateur et que vous avez identifié les groupes d’utilisateurs et les catalogues auxquels ils doivent avoir accès.

### Configuration de l’accès à l’assistant AI

Pour activer l’assistant d’IA dédiée aux élèves :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.

2. Sélectionnez **Paramètres** dans la page d&#39;accueil.
   ![Console Administrateur avec l&#39;option Paramètres dans le volet de gauche](assets/settings-menu.png)

3. Sélectionnez **Learner AI Assistant (Beta)** dans le menu **Paramètres**.
   ![La console Administrateur affiche l&#39;option Assistant IA de l&#39;élève dans le volet de gauche](assets/learner-assistant-ai-beta.png)

4. Sélectionnez le bouton à bascule pour activer l&#39;**assistant Learner AI (Beta)**.
   ![La console Administrateurs affiche le bouton à bascule activé pour l&#39;Assistant Élève IA](assets/learner-assistant-toggle.png)

5. Sélectionnez un ou plusieurs groupes d&#39;utilisateurs dans l&#39;option **Groupes d&#39;utilisateurs éligibles**.

6. Sélectionnez **Enregistrer** pour appliquer les paramètres du groupe d&#39;utilisateurs.

7. Sélectionnez un ou plusieurs catalogues dans l&#39;option **Catalogues éligibles**.

8. Sélectionnez **Enregistrer** pour appliquer les paramètres du catalogue.

>[!IMPORTANT]
>
>Seuls les catalogues **internes** sont pris en charge. Si un catalogue **partagé**, **acquis**, **externe** ou tout autre catalogue non interne est sélectionné, son contenu ne sera pas affiché par l&#39;assistant IA, même s&#39;il apparaît dans la liste **Catalogues éligibles**.

## Lancer l’assistant AI (élèves)

Pour lancer l’assistant AI :

1. Connectez-vous à Adobe Learning Manager en tant qu’élève.

2. Sélectionnez **Demander à l&#39;assistant IA** sur la page d&#39;accueil.
   ![La page d’accueil de l’élève affiche Demander à l’assistant IA de sélectionner et d’ouvrir le panneau Assistant IA de l’élève](assets/ask-ai-assistant.png)

3. Lorsque l&#39;écran **Assistant IA dédiée aux élèves** apparaît, sélectionnez **Commencer**.
   ![Sélectionnez Commencer pour lancer l’assistant Élève](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Lorsque vous lancez l’assistant AI pour la première fois, vous devez donner votre consentement avant de l’utiliser. La boîte de dialogue de consentement s’affiche uniquement lors de ce lancement initial. Pour tous les lancements suivants, vous serez directement redirigé vers l’assistant AI pour saisir vos invites.

4.Saisissez votre invite dans le champ de texte.
<!-- ![Type prompt in the Learner Assistant](assets/type-prompt-new.png) -->

5.Appuyez sur **Entrée** pour recevoir une réponse. Examinez votre réponse, vos sources et vos recommandations.

Vous pouvez :

- Sélectionnez le numéro de citation en ligne pour accéder à la section référencée exacte
- Ouvrez la liste complète des sources en sélectionnant **Afficher les sources** au bas de la réponse

![Afficher les sources dans la réponse](assets/show-sources-latest.png)

L’assistant d’IA inclut des citations avec chaque réponse pour indiquer d’où viennent les informations. Chaque citation renvoie directement au cours, au module ou à l’objet d’apprentissage d’origine utilisé pour générer la réponse.

Vous pouvez sélectionner n’importe quelle citation pour ouvrir la page du cours dans Adobe Learning Manager et consulter l’intégralité du contenu dans son contexte. Les citations vous aident à vérifier les informations, à explorer des détails supplémentaires et à continuer à apprendre de la source faisant autorité.

## Accéder à l’assistant d’IA via la recherche

Vous pouvez également lancer l’assistant d’IA directement depuis la barre de recherche. Saisissez votre question dans le champ de recherche, puis sélectionnez **Demander l’assistant IA** dans les options qui s’affichent.

![Accédez à l’assistant d’élève à partir de la barre de recherche](assets/learner-assistant-search-new.png)

## Fournir des commentaires sur les réponses de l’assistant d’IA

Vos commentaires sur les réponses générées par l’assistant d’IA (Beta) contribuent à améliorer sa précision, sa pertinence et ses performances globales.

### Aimer ou ne pas aimer une réponse

- Sélectionnez **Pouces vers le haut**, choisissez ce que vous avez trouvé utile dans la réponse, ajoutez éventuellement des commentaires, puis sélectionnez **Envoyer**.
- Sélectionnez **Pouces baissées**, indiquez la raison pour laquelle la réponse n’a pas été utile, ajoutez des commentaires, puis sélectionnez **Envoyer**.

## Démarrer une nouvelle conversation

Démarrer une nouvelle conversation permet de commencer une nouvelle conversation, en effaçant le contexte précédent afin que l&#39;assistant puisse se concentrer sur le nouveau sujet sans référencer les interactions précédentes.

Pour effacer la conversation en cours et recommencer à zéro, sélectionnez **Nouvelle conversation** dans l’écran de l’assistant AI, puis sélectionnez **Oui**.

![Démarrer une nouvelle conversation dans l’assistant d’élève](assets/start-new-chat.png)

L’assistant d’IA fournit aux élèves des réponses contextuelles rapides, prend en charge plusieurs types de contenu et propose des citations en ligne pour plus de transparence. Les administrateurs peuvent contrôler l’accès et s’assurer que l’assistant IA est adapté aux besoins de l’entreprise et améliore l’expérience d’apprentissage.


## Résolution des problèmes de l’assistant AI

> **REMARQUE**
> Après avoir configuré un nouveau catalogue, attendez 4 à 5 heures pour que le contenu soit indexé et disponible pour les réponses de l&#39;Assistant IA.

### Pas d’accès au contenu

**Problème :** un élève a accès à l&#39;assistant IA, mais reçoit des réponses « Je n&#39;ai pas de réponse à cette question ».

**Causes possibles :**

- Les catalogues de l’élève ne sont pas inclus dans la configuration de l’assistant IA.
- Le contenu lié à la question ne se trouve pas dans les catalogues sélectionnés ou les catalogues sont vides.
- L’élève n’a pas de visibilité sur le contenu pertinent.

**Solution :**

- Vérifiez l’accès au catalogue de l’élève.
- Vérifiez quels catalogues sont activés dans les paramètres de l’assistant AI.
- Vérifiez que le contenu pertinent existe dans ces catalogues.
- Patientez quelques heures après l’ajout du nouveau contenu pour qu’il soit indexé.

### Réponses non pertinentes ou de mauvaise qualité

**Problème :** l&#39;Assistant IA fournit des réponses qui ne correspondent pas à la question ou qui sont de mauvaise qualité.

**Causes possibles :**

- La question est trop vaste ou ambiguë.
- Le contenu pertinent a des métadonnées médiocres (descriptions, balises).
- La structure du contenu rend difficile l’extraction des informations.

**Solution :**

- Encouragez les élèves à poser des questions plus spécifiques.
- Examiner et améliorer les descriptions de cours et les métadonnées.
- Assurez-vous que le contenu possède des en-têtes et une structure clairs.
- Consultez le rapport d’utilisation détaillé pour identifier les modèles.
- Envisagez de créer des assistances à la tâche pour les questions fréquemment posées.

### Questions hors du champ d’application

**Problème :** un élève pose des questions sans rapport avec le contenu de la formation.

**Exemples :**

- Questions générales sur les connaissances (« Qui est le président ? »)
- Opinions personnelles (« Que pensez-vous de X ? »)
- Contenu inapproprié

L’assistant AI est conçu pour répondre aux questions uniquement en fonction du contenu d’apprentissage attribué et ne répond pas aux requêtes hors du champ d’application.
