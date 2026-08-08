---
description: Découvrez les nouvelles fonctionnalités et améliorations de la version d’août 2026 de Adobe Learning Manager
jcr-language: en_us
title: Nouveautés de la version d’août 2026 de Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 458d21d11bfcfb701dbd61b865411f80a306adc1
workflow-type: tm+mt
source-wordcount: '2743'
ht-degree: 0%

---

# Nouveautés de la version d’août 2026 de Adobe Learning Manager

## Gradebook

Un cahier de notes dans Adobe Learning Manager ajoute une notation pondérée aux cours, ce qui permet aux auteurs d’affecter un pourcentage de contribution à chaque module noté et de définir un score agrégé minimal pour l’achèvement du cours. Les élèves peuvent suivre leurs notes tout au long du cours et les administrateurs peuvent afficher les notes finales et télécharger les relevés de notes pertinents.

### Ce que fait l’annuaire de notes

Un cours avec catalogue de notes calcule le score final de chaque élève en combinant les scores de module individuels en fonction du pourcentage de pondération attribué à chaque module. Cela fournit une mesure précise et pondérée des performances plutôt qu’une simple somme de scores ou un marqueur de réussite/échec basé uniquement sur l’achèvement.

Gradebook prend en charge deux modèles d’achèvement :

* **Modules obligatoires uniquement** : le cours se termine lorsque tous les modules obligatoires sont terminés. Les scores du carnet de notes sont toujours calculés et visibles, mais le score global ne contribue pas aux critères de réussite.

* **Modules requis plus score total** : l’élève doit terminer tous les modules requis et obtenir un score total égal ou supérieur au seuil de réussite minimal. Ces deux conditions doivent être remplies pour obtenir la note de passage.

### Mode de calcul des scores de cours

Pour chaque module évaluable, la contribution au score global du cours est :

(Score obtenu ÷ Score maximum) × % de pondération = Contribution du module

Le score total du cours est la somme de toutes les contributions du module. Les pourcentages de poids de tous les modules évaluables doivent totaliser exactement 100. La configuration du classeur ne peut pas être enregistrée tant que cette condition n&#39;est pas remplie.

Le score total du cours est la somme de toutes les contributions du module. Les pourcentages de poids de tous les modules évaluables doivent totaliser exactement 100. La configuration du classeur ne peut pas être enregistrée tant que cette condition n&#39;est pas remplie.

L’échelle de notation n’a pas besoin d’être cohérente entre les modules. Une session de classe notée sur 100 et un module SCORM noté sur 10 peuvent coexister dans le même cahier de notes. La formule normalise chaque contribution avant d&#39;appliquer la pondération.

**Modules avec et sans score**

Seuls les modules qui produisent un score sont éligibles pour la pondération. Les types de modules pouvant être notés sont les suivants :

* Contenu SCORM, AICC et xAPI avec notation activée
* packages de contenu de Captivate
* Quiz natifs dans Adobe Learning Manager
* Sessions de salle de classe et de classe virtuelle où l’instructeur ou l’administrateur saisit un score
* Modules d’activité notés par un instructeur ou un administrateur

Les types de modules non marquables, les fichiers de PDF, les fichiers vidéo, les fichiers audio, les présentations PowerPoint, les documents Word, les fichiers Excel et le contenu de HTML ne peuvent pas se voir attribuer de pourcentage pondéré et ne contribuent pas au score total. Ces modules peuvent toujours être requis pour terminer le cours. Lorsque l&#39;option Inclure les modules qui ne contribuent pas à la note finale est activée, ils apparaissent dans le catalogue de notes sans valeur de pondération.

Afficher le [Gradebook pour les auteurs](/help/migrated/authors/feature-summary/alm-author-gradebook.md) pour plus d&#39;informations.

## Dossiers de contenu hiérarchique

La bibliothèque de contenu prend désormais en charge jusqu’à trois niveaux de hiérarchie de dossiers privés. Les administrateurs créent la structure de dossiers et contrôlent les rôles personnalisés qui peuvent accéder aux dossiers de niveau 1. Accédez automatiquement en cascade à tous les sous-dossiers d’un dossier de niveau 1.

Les auteurs peuvent copier et déplacer du contenu entre les dossiers, filtrer la bibliothèque de contenu par dossier et parcourir la hiérarchie lors de l&#39;ajout de modules à un cours.

Fonctionnalités clés :

* Jusqu’à trois niveaux d’imbrication (25 sous-dossiers maximum par parent)
* Accès basé sur les rôles attribué au niveau 1 uniquement
* Le contenu peut apparaître dans plusieurs dossiers sans duplication
* Le dossier public et la structure du dossier privé s’excluent mutuellement
* Parcourir les dossiers lors de la sélection de modules dans la création de cours

Consultez [Dossiers de contenu hiérarchique](/help/migrated/administrators/feature-summary/settings/advanced-settings.md#content-folder) pour plus d&#39;informations sur les fonctionnalités au niveau de l&#39;administrateur. Consultez [Dossiers de contenu hiérarchique](/help/migrated/authors/feature-summary/content-library.md#add-content-to-a-folder) pour plus d&#39;informations sur les fonctionnalités au niveau de l&#39;auteur.

Si vous migrez votre contenu d’apprentissage à partir d’une autre plate-forme vers Adobe Learning Manager et que vous souhaitez conserver l’organisation de vos dossiers existants, vous pouvez utiliser les fichiers CSV pour créer une structure de dossiers hiérarchique et associer vos fichiers de contenu aux dossiers appropriés. En savoir plus sur la migration dans la [hiérarchie des dossiers de contenu migrés](/help/migrated/integration-admin/feature-summary/migration-manual.md#migratecontentfolderhierarchy)

## Live Hub (Beta)

Live Hub est une expérience de formation virtuelle basée sur l&#39;IA au sein de Adobe Learning Manager qui aide les organisations à fournir un apprentissage en direct attrayant et percutant. Grâce à des fonctionnalités intelligentes telles que les sondages optimisés par l&#39;IA, l&#39;orchestration des salles de classe, les espaces d&#39;apprentissage persistants et l&#39;assistance optimisée par l&#39;IA, Live Hub optimise la productivité des instructeurs tout en réduisant la complexité de la prestation des sessions.

Points saillants :

* Améliorez l’apprentissage en direct grâce à une expérience Adobe Learning Manager native qui améliore la qualité pédagogique et les résultats des élèves.
* Donnez à vos instructeurs un coanimateur optimisé par l’IA qui stimule l’engagement grâce à des sondages intelligents, une assistance pour les questions et réponses et des informations sur les salles de réunion.
* Aidez vos élèves à tirer le meilleur parti de chaque session avec des résumés et des enregistrements de session générés par l’IA consultables par sujet.
* Mesurez ce qui compte grâce à des analyses d’engagement qui vont au-delà de l’assiduité pour révéler une véritable participation à l’apprentissage.
* Aidez vos auteurs à utiliser le Finder d’instructeurs basé sur l’IA pour trouver le bon instructeur en fonction des compétences, de la disponibilité, des heures préférées, du fuseau horaire et de l’utilisation actuelle.

Consultez [Prise en main du concentrateur en direct](./getting-started-with-live-hub/getting-started-live-hub.md) pour plus d&#39;informations.

## Adobe Learning Manager Content Composer (Beta)

Adobe Learning Manager inclut désormais le compositeur de contenu, un outil de création de cours natif basé sur l’IA qui vous fait passer en quelques minutes d’une invite en langage clair à un cours structuré prêt pour la publication.

Fonctionnalités clés :

* L&#39;IA conversationnelle guide les auteurs à travers les objectifs de formation, le matériel source et les objectifs d&#39;apprentissage pour générer un résumé et un plan de cours complets.
* La génération basée sur les documents limite la sortie de l’IA à vos fichiers chargés, ce qui est essentiel pour la conformité, la réglementation et la formation basée sur les procédures.
* Génération d’un cours complet en une seule passe, par exemple des leçons, des sujets, du texte, des images, des vérifications de connaissances et des questionnaires notés.
* Système de thème visuel avec modes clair et sombre, commandes de police, prise en charge des en-têtes et pieds de page et exportation JSON pour une personnalisation avancée.
* Critères d&#39;achèvement configurables, critères de réussite, paramètres du quiz et version de SCORM avant la publication.
* et plus encore.

Consultez [Adobe Learning Manager Content Composer](/help/migrated/authors/feature-summary/content-composer/content-composer-help.md) pour plus d&#39;informations.


## Créateur de modèles d’e-mail basé sur des composants

Les organisations peuvent désormais créer des notifications par e-mail de marque de niveau entreprise dans Adobe Learning Manager à l’aide d’un éditeur de composant WYSIWYG moderne. Les administrateurs peuvent créer une mise en page globale une seule fois, avec un en-tête, un pied de page et des éléments de marque réutilisables, et l’appliquer à tous les modèles de courrier électronique au niveau du compte. Les modèles individuels peuvent ensuite être personnalisés au niveau du cours ou de l’instance, héritant de la mise en page parente par défaut et la remplaçant uniquement si nécessaire.

Fonctionnalités clés :

* Éditeur WYSIWYG avec une bibliothèque de composants réutilisables (texte, image, bouton, séparateur, en-tête, pied de page)
* Prise en charge des variables : insérez des champs dynamiques tels que le nom de l’élève, le nom du cours et la date d’échéance
* Hiérarchie des modèles liés et non liés : les modifications apportées à un modèle lié se propagent à tous les modèles enfants ; les modèles non liés sont modifiables indépendamment.
* Prise en charge de modèles multilingues
* Aperçu et test-envoi avant la publication
* Rétrocompatibilité : les modèles de courrier électronique existants continuent de fonctionner

Consultez [Créateur d&#39;e-mails basé sur les composants](/help/migrated/administrators/feature-summary/email-builder.md) pour plus d&#39;informations.

## Support d’apprentissage externe

Les élèves peuvent désormais soumettre des formations hors plateforme, telles que des certifications, des ateliers, des conférences et des cours externes, pour approbation par le responsable directement à partir de leur tableau de bord d’élève. Les envois approuvés apparaissent dans le relevé de notes de l’élève.

Fonctionnalités clés :

* Formulaire de soumission configurable avec champs standard et personnalisés
* Processus de révision et d’approbation du responsable avec prise en charge des commentaires
* Les envois approuvés apparaissent dans le relevé de notes de l’élève avec les métadonnées complètes
* L’administrateur peut configurer les champs obligatoires, y compris les champs personnalisés
* Nouvelles colonnes dans les relevés de notes des administrateurs et des élèves : nom de l’apprentissage externe, commentaire d’achèvement, colonnes de champs personnalisés
* Prise en charge de l’API : cinq nouveaux points d’entrée de portée élève pour la création, la récupération et la mise à jour des envois

Pour plus d&#39;informations au niveau administrateur, consultez [Support d&#39;apprentissage externe](/help/migrated/administrators/feature-summary/settings/basic-settings.md). Pour plus d&#39;informations au niveau du responsable, consultez [Support d&#39;apprentissage externe](/help/migrated/managers/feature-summary/review-external-learning-requests.md). Pour plus d&#39;informations au niveau de l&#39;élève, consultez [Support d&#39;apprentissage externe](/help/migrated/learners/feature-summary/submit-external-learning.md).

## Fonctionnalités d’IA

### Assistant d’IA pour les élèves

L’assistant AI pour les élèves prend désormais en charge quatre nouvelles fonctionnalités en plus de répondre aux questions du contenu d’apprentissage attribué :

* **Résumés de cours** : utilisez la commande / pour sélectionner un élément de catalogue et générer un résumé sans ouvrir le cours
* **Comparaison des objets d&#39;apprentissage** : sélectionnez jusqu&#39;à deux objets d&#39;apprentissage à l&#39;aide de la commande / et demandez à l&#39;assistant de les comparer
* **Adobe Experience League répond** : l’assistant recherche désormais des réponses aux questions pratiques de la documentation d’aide de Adobe Learning Manager
* **Requêtes de contenu tiers** : le contenu du catalogue Go1 et LinkedIn Learning peut être interrogé (métadonnées uniquement ; anglais uniquement ; l’ingestion prend 1 à 2 heures après l’ajout du catalogue)

Voir [Assistant IA pour les élèves](/help/migrated/learners/feature-summary/learner-ai-assistant.md) pour plus d&#39;informations.

### Agent du parcours d’apprentissage

Les élèves peuvent désormais avoir une conversation guidée avec l&#39;assistant AI pour générer un parcours d&#39;apprentissage personnalisé et séquencé en fonction de leurs objectifs, de leur arrière-plan et du temps disponible. Le parcours d’apprentissage est créé automatiquement et l’élève est inscrit.

Fonctionnalités clés :

* La conversation à plusieurs tours guide l&#39;élève à travers la sélection du sujet, la révision du cours et la confirmation du chemin
* Jusqu’à cinq sujets d’apprentissage suggérés par conversation
* Sélection de cours dans les catalogues attribués
* Maximum de 10 parcours d’apprentissage personnalisés visibles sur la page d’accueil de l’élève
* Les tracés terminés peuvent être partagés avec des collègues

Voir [Agent du parcours d’apprentissage](/help/migrated/learners/feature-summary/learning-path-agent.md) pour plus d’informations.

### Agent d’informations

Insights Agent aide les administrateurs à analyser les données d’apprentissage par le biais de requêtes en langage naturel. Posez des questions sur les tendances d’inscription, les taux d’achèvement, l’engagement des élèves et les lacunes en compétences. L&#39;agent génère des rapports et des visualisations en réponse.

Consultez [Insights Agent](/help/migrated/administrators/feature-summary/insights-agent.md) pour plus d&#39;informations.

### Crédits d’IA de génération

Adobe Learning Manager intègre des fonctionnalités optimisées par l’IA gérées via un système basé sur les crédits et lié aux licences Agent Orchestrator. Ce système nécessite que les administrateurs activent les fonctionnalités, définissent des limites de crédit et contrôlent l’utilisation via la page Facturation. Pour activer les fonctionnalités d’IA de génération, il est essentiel de lier le compte Adobe Learning Manager à une organisation Adobe Admin Console disposant d’une licence Agent Orchestrator active.

Voir [Crédits d’IA de génération](/help/migrated/administrators/feature-summary/billing-management.md#genaicredits) pour plus d’informations.

## Canaux (Beta)

Les canaux fournissent un moyen centralisé d’organiser, de publier et de découvrir du contenu vidéo à partir du web et des pages Confluence. Les administrateurs peuvent créer et gérer des canaux en connectant des pages web prises en charge ou des pages de convergence, configurer les paramètres des canaux, contrôler la visibilité et synchroniser le contenu à partir de la source. Les élèves peuvent parcourir les canaux disponibles, s’abonner aux canaux qui les intéressent et regarder du contenu vidéo de qualité à partir d’un seul emplacement.

Voir [Créer des canaux](/help/migrated/administrators/feature-summary/create-channels.md) pour plus d&#39;informations.

## Créateur de rapports

Report Builder offre aux administrateurs un outil de création de rapports flexible et en libre-service qui va au-delà des types de rapports fixes disponibles ailleurs dans Adobe Learning Manager. Plutôt que de se limiter à des structures de rapport prédéfinies, les administrateurs peuvent joindre des champs de plusieurs jeux de données, tels que Utilisateur, Groupes d’utilisateurs, Cours et parcours d’apprentissage, Modules, Transcription, Catalogues et bien plus encore, dans un seul rapport personnalisé, adapté aux besoins en données spécifiques de leur organisation.

Les rapports sont créés une seule fois et enregistrés pour une utilisation répétée. Il n’est pas nécessaire de reconstruire les filtres, de réappliquer les regroupements ou de rejoindre les jeux de données à chaque téléchargement. Les rapports enregistrés peuvent être téléchargés à la demande, partagés avec d’autres administrateurs ou configurés avec un abonnement afin que les destinataires reçoivent automatiquement les rapports mis à jour à intervalles réguliers.

Voir [Report Builder](/help/migrated/administrators/feature-summary/alm-report-builder.md) pour plus d&#39;informations.

## Modifications de rôle personnalisées

Les administrateurs personnalisés peuvent désormais bénéficier de fonctionnalités de gestion des utilisateurs étendues via le niveau d’autorisation Avancé sous Utilisateurs dans une définition de rôle personnalisée.

Deux niveaux d&#39;accès sont disponibles :

| Niveau d’accès | Ce que l’administrateur personnalisé peut faire |
|---|---|
| **Lecture seule** | Afficher tous les rôles personnalisés, les journaux d’importation et les utilisateurs supprimés ; télécharger le rapport des rôles personnalisés |
| **Contrôle total** | Toutes les fonctionnalités en lecture seule plus : créer, modifier, supprimer et affecter des rôles personnalisés ; importer des utilisateurs via CSV ; purger les utilisateurs supprimés |

### Limitations

**Rôles créés manuellement uniquement** : les fonctionnalités étendues d&#39;administration de rôles personnalisés s&#39;appliquent uniquement aux rôles créés via l&#39;interface de l&#39;administrateur Adobe Learning Manager. Les rôles importés via le chargement CSV ne sont pas pris en charge.

En savoir plus sur les modifications de rôle personnalisées. Pour plus d&#39;informations, consultez [Ce que l&#39;autorisation utilisateur avancé déverrouille](/help/migrated/administrators/feature-summary/custom-role.md#whatadvanceduserpermissionunlocks)

## Liaison profonde LTI

Les administrateurs d’intégration peuvent désormais activer la liaison profonde LTI pour les configurations de l’outil LTI, ce qui permet aux auteurs de cours de parcourir et d’intégrer des cours Adobe Learning Manager directement à partir d’un système de gestion de l’apprentissage externe sans copier manuellement les URL des cours.

Une fois activé, les auteurs voient un bouton **Sélectionner le contenu** dans la configuration de l&#39;activité LMS externe. Ils peuvent parcourir les catalogues approuvés, sélectionner des cours et confirmer la sélection, tous les champs étant renseignés automatiquement.

Voir [Liens profonds LTI](/help/migrated/integration-admin/feature-summary/lti-deep-links.md) pour plus d&#39;informations.

## Lieux de salles de classe

Les emplacements de salle de classe prennent désormais en charge un **format d&#39;emplacement structuré à quatre champs**, y compris le pays, l&#39;État/la province/la région, la ville et le nom de l&#39;emplacement, ce qui facilite la gestion et l&#39;organisation des emplacements de formation entre les régions. La mise à jour inclut une migration unique à partir du format de champ unique hérité et ajoute la prise en charge multilingue des champs **Nom de l&#39;emplacement** et **Informations sur l&#39;emplacement**, permettant ainsi de localiser les détails de la salle de classe pour les élèves.

Voir [Emplacements de salle de classe](/help/migrated/administrators/feature-summary/classroom.md) pour plus d&#39;informations.

## Signalement des modifications apportées à la version

Pour plus d&#39;informations, consultez [les rapports de modification de la version d&#39;août 2026 de Adobe Learning Manager](/help/migrated/reporting-changes-august-2026.md).

## Modifications d’API dans la version

Consultez les [modifications d&#39;API dans la version d&#39;août 2026 de Adobe Learning Manager](/help/migrated/api-changes-august-2026.md) pour plus d&#39;informations.

## Autres améliorations de la version

| Amélioration | Description |
|---|---|
| **MQA : score le plus récent et score le plus élevé** | Pour les modules avec plusieurs tentatives, les auteurs peuvent désormais choisir si le score de tentative le plus récent ou le plus élevé est enregistré dans le relevé de notes de l&#39;élève et utilisé dans les calculs du carnet de notes. La dernière option était la valeur par défaut existante et le reste lorsque le paramètre n’est pas configuré. Pour plus d&#39;informations, consultez le [Gradebook pour les auteurs](/help/migrated/authors/feature-summary/alm-author-gradebook.md#configurescoresettingsmultipleattempts). |
| **Aperçu du contenu dans la bibliothèque de contenu** | Les auteurs peuvent désormais prévisualiser les fichiers de contenu chargés directement dans la bibliothèque de contenu avant de les ajouter aux cours. Pour plus d&#39;informations, consultez [Aperçu de la bibliothèque de contenu](/help/migrated/authors/feature-summary/content-library.md#previewcontentlibrary). |
| **Rapport utilisateur incrémentiel** | Un nouveau rapport d’utilisateur basé sur l’API renvoie uniquement les utilisateurs créés ou modifiés depuis la dernière demande, ce qui réduit le transfert de données pour les grands comptes à l’aide des workflows de synchronisation automatisée des utilisateurs. Pour plus d&#39;informations, consultez le [Rapport utilisateur incrémentiel](/help/migrated/incremental-user-report.md). |
| **11 nouvelles langues dans le lecteur fluidic** | Le lecteur Fluidic prend désormais en charge 11 langues supplémentaires, y compris la prise en charge des scripts de droite à gauche (RTL). Pour plus d&#39;informations, consultez [Lecteur Fluidic](/help/migrated/learners/feature-summary/fluidic-player.md). |
| **Migration du module LTI** | Les modules LTI 1.1 existants peuvent désormais être migrés vers LTI 1.3 à l’aide de l’outil de migration. Pour plus d&#39;informations, consultez la migration [LTI des modules](/help/migrated/integration-admin/feature-summary/migration-manual.md#migrationofltimodules). |
| **Email Builder : prise en charge de l’éditeur de texte enrichi** | Les modèles d’e-mail dans Adobe Learning Manager prennent désormais en charge le formatage de texte enrichi, les pièces jointes et les automatisations personnalisées. Pour plus d&#39;informations, consultez [Email Builder](/help/migrated/administrators/feature-summary/email-builder.md). |
| **Email Builder : fonctionnalité Aperçu** | Vous pouvez vérifier l’e-mail que vous avez composé pour voir à quoi il ressemblerait du côté du destinataire à l’aide de l’option Aperçu. Pour plus d&#39;informations, consultez [Email Builder](/help/migrated/administrators/feature-summary/email-builder.md). |
| **Normalisation de l’horodatage du webhook** | Tous les champs de date et d’heure de l’objet `data` des charges utiles de webhook ont désormais la valeur `00` en secondes, ce qui offre une précision à la minute cohérente avec les rapports de relevé de notes de l’élève. |
| **Améliorations de Connect** | Mises à jour du connecteur Azure Data Lake Storage (ADLS) ; prise en charge des noms de salle persistants pour les sessions de classe virtuelle récurrentes ; suivi de l’assiduité basé sur la vue d’enregistrement. |
| **Améliorations des performances du lecteur** | Le lecteur de cours fluidic a été optimisé pour des temps de chargement plus rapides et des transitions plus fluides entre les modules. |
| **Avertissement d’impact avant de retirer des cours/programmes d’apprentissage** | L’auteur/l’administrateur verra une liste d’avertissement des objets d’apprentissage dépendants avant qu’un cours ou un parcours d’apprentissage ne puisse être retiré. Indique à l’auteur qu’un objet d’apprentissage constitutif a été retiré. Les administrateurs reçoivent l’objet d’apprentissage s’ils l’ont créé mais n’ont pas le rôle d’auteur. |
| **Module CR/VC : durée attendue** | Les auteurs peuvent désormais définir une durée attendue pour les modules de salle de classe et de salle de classe virtuelle, indépendamment de l’heure de la session planifiée. Cette valeur apparaît dans les rapports et les informations sur les cours destinés aux élèves. |
| **Confirmation avant de modifier les cours acquis** | Les administrateurs de comptes de pairs voient désormais une boîte de dialogue de confirmation avant de modifier un cours acquis via le partage de catalogue, ce qui empêche toute modification involontaire du contenu partagé. |
| **URL de session avec ID d&#39;instance** | Les URL de lancement de session pour les sessions Microsoft Teams, Adobe Connect et Zoom incluent désormais l’ID d’instance, ce qui garantit que les élèves sont redirigés vers la bonne session lorsqu’il existe plusieurs instances. |
| **Avertissement pour les annonces grand public** | Lorsqu’ils envoient un e-mail d’annonce ad hoc à plus d’un seuil configurable de destinataires, les administrateurs voient désormais un avertissement relatif au volume avant l’envoi. |
| **Modèles de courrier électronique : URL du compte pour les élèves externes** | Les modèles de notification par e-mail peuvent désormais inclure une URL de compte distincte spécifiquement pour les élèves externes, en les acheminant vers l’expérience de connexion appropriée. |
| **AEM Sites** | Il n&#39;y a qu&#39;un seul bouton **Modifier** maintenant dans la section **Votre profil** > Vos centres d&#39;intérêt pour modifier vos préférences pour les produits et les rôles et compétences. Cela fait également partie de Learning Manager natif. |
| **AEM Sites** | Auparavant, il y avait deux boutons **Modifier**, mais désormais, le bouton **Modifier** est un bouton consolidé pour modifier vos préférences pour les produits et les rôles et compétences. |
| **Fuseau horaire** | Une nouvelle zone de recherche a été ajoutée juste en dessous du champ Fuseau horaire dans les Paramètres de profil de l’utilisateur connecté. La zone de recherche permet de rechercher directement un fuseau horaire au lieu de faire défiler la liste complète des fuseaux horaires disponibles. Si vous souhaitez modifier le fuseau horaire existant, sélectionnez un nouveau fuseau horaire, puis cliquez sur Enregistrer. Le nouveau fuseau horaire est enregistré. Le bouton Enregistrer s’affiche uniquement lorsque vous sélectionnez un fuseau horaire. |

## Configuration système

Consultez [Configuration requise pour Adobe Learning Manager](/help/migrated/system-requirements.md) pour plus d&#39;informations.

## Notes de mise à jour

Consultez les [notes de mise à jour](/help/migrated/release-note/release-notes.md) pour connaître les dernières mises à jour.

## Versions précédentes d’Adobe Learning Manager

* [Version d’avril 2026 de Adobe Learning Manager](/help/migrated/whats-new-april-2026.md)
* [Version d’octobre 2025 de Adobe Learning Manager](/help/migrated/whats-new-october-2025.md)
