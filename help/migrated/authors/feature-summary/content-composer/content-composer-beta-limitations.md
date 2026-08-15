---
description: Passez en revue les limitations de Content Composer (édition uniquement conversationnelle, questionnaires uniquement MCQ/True-False, contours fixes) avec des solutions pour chacun d’eux.
jcr-language: en_us
title: Limitations de Content Composer Beta
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---


# Limitations de la version bêta de Adobe Learning Manager Content Composer

Une liste complète des contraintes Beta actuelles du compositeur de contenu, avec des descriptions et des solutions de contournement, le cas échéant.

## Limitations actuelles

Le tableau suivant couvre toutes les contraintes connues de la version Beta actuelle.

| **Limitation** | **Description** | **Solution** |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **La modification des contours est uniquement une conversation** | Vous ne pouvez pas sélectionner une leçon ou une rubrique sur la zone de travail pour la renommer, la réorganiser ou la supprimer. Toutes les modifications de contour doivent être effectuées via le panneau de conversation de l’assistant. | Demandez à l&#39;assistant : « Renommez la leçon 2 en « Hygiène du mot de passe » ou « Déplacez le sujet 1.3 en leçon 2. » |
| **La hiérarchie des contours est fixe** | La structure du cours est définie sur Leçons > Rubriques. Vous ne pouvez pas créer de sous-rubriques, de niveaux hiérarchiques supplémentaires ou de structures personnalisées. | Utilisez les composants disponibles pour ajouter de la profondeur dans une rubrique. |
| **Le contour ne peut pas être modifié directement après la génération du cours** | Une fois qu&#39;un cours est généré, les noms des sujets et des leçons restent dans la structure hiérarchique. Vous devez revenir aux conversations au niveau du plan pour les modifier. Vous ne pouvez pas les renommer en sélectionnant un titre dans l’éditeur de cours. | Demandez à l’assistant dans l’éditeur de cours : « Renommez la leçon 3 en « Réponse à l’incident ». » |
| **Types d’évaluation : MCQ et True/False uniquement** | La version Beta actuelle prend uniquement en charge les questions à choix multiples (**MCQ**) et les questions Vrai/Faux. D&#39;autres types d&#39;évaluation ne sont pas disponibles. | - |
| **Les banques de questions ne sont pas disponibles** | Vous ne pouvez pas importer ou gérer une banque de questions prérédigées. | Développez d’autres questions par conversation : « Ajoutez deux autres questions au quiz pour la leçon 1. » |
| **Les vérifications de connaissances ne sont pas notées** | Les vérifications de connaissances intégrées dans les leçons ne sont pas notées. Seules les évaluations de quiz de fin de leçon sont notées et enregistrées. | Utilisez des quiz (et non des vérifications de connaissances) pour toute évaluation devant produire un achèvement ou un enregistrement de score. |
| **Actions de conversation limitées aux fonctionnalités prises en charge** | L&#39;assistant peut discuter et réfléchir librement, mais les modifications de cours réelles sont limitées aux fonctionnalités prises en charge par le produit. Les demandes de génération de structures ou de formats de contenu non pris en charge peuvent échouer. | Si une demande ne fonctionne pas, demandez à l&#39;assistant d&#39;expliquer ce qu&#39;il peut faire à la place. |
| **Génération restreinte au document** | Lorsque l&#39;option **Restreindre la sortie au contenu dans les fichiers** est activée, le compositeur de contenu génère du contenu à partir des documents sources chargés uniquement. Il n&#39;introduit pas d&#39;informations au-delà de ces sources. | Désactivez le bouton pour permettre à l’IA de compléter ses connaissances générales. |
| **Les fonctionnalités de collaboration évoluent** | Les options Partager pour révision et commentaires et Partager pour les élèves sont en cours de développement. Les détails de la mise en œuvre peuvent changer avant la disponibilité générale. | Utilisez **Copier le lien** pour partager un lien d&#39;aperçu en vue d&#39;une révision informelle. Pour la cocréation, coordonnez les rotations avec les collaborateurs. La cocréation simultanée n’est pas prise en charge. |
| **L’assistant produit n’est pas un système d’aide produit** | L&#39;assistant conversationnel est conçu pour les tâches de modification de cours, telles que la génération et la modification de contenu. Les réponses aux questions sur l’utilisation du produit peuvent ne pas être fiables, car ce comportement n’est pas encore explicitement conçu. | Pour des questions pratiques, utilisez la documentation d’aide existante au lieu de demander à l’assistant intégré au produit. |
