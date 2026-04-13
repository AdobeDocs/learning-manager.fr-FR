---
description: Découvrez les nouvelles fonctionnalités et améliorations, y compris les modifications d’API et de webhooks, de la version d’avril 2026 de Adobe Learning Manager
jcr-language: en_us
title: Nouveautés de la version d’avril 2026 de Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 971a9c79fc2b831b990e30a44a2eeab5d5c5ce63
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 0%

---

# Nouveautés de la version d’avril 2026 de Adobe Learning Manager

**Pour les élèves :** le lecteur Fluidic affiche désormais le nom du module suivant et un bouton de sortie clair. La langue du lecteur peut être définie via LTI pour une expérience cohérente entre les plateformes. Le nom du paramètre personnalisé est « locale » et il accepte le code de locale. Par exemple, locale=fr-FR. Le contenu Captivate comprend une table des matières unifiée, des repères d’achèvement au niveau des diapositives et des exportations de notes fiables. La prise en charge multilingue est disponible pour les assistances à la tâche, les questions de liste de contrôle et les pistes de texte vidéo. L’assistant AI aide les élèves à obtenir des réponses dans l’expérience d’apprentissage.

**Pour les administrateurs et les auteurs :** le connecteur Zoom prend en charge plusieurs sessions VILT simultanées. Les cours partagés dans des comptes de pairs affichent le véritable auteur au lieu du terme « Auteur externe ». Les administrateurs peuvent restreindre le moment où les modules peuvent être démarrés. Les dates d’expiration des objets d’apprentissage sont affichées dans les API des élèves. Les modules de liste de contrôle prennent en charge la notation pondérée, le texte de question multilingue et les commentaires de réviseur facultatifs. Les certificats personnalisés offrent un éditeur glisser-déposer avec des champs dynamiques et des arrière-plans générés par l’IA. Le créateur d’expériences hors connexion vous permet de créer des pages d’apprentissage publiques sans nécessiter de connexion.

**Pour les instructeurs :** générez des codes QR pour l&#39;inscription à l&#39;instance et la participation aux sessions. Ajoutez des commentaires ou des commentaires pendant l’évaluation de la liste de contrôle.

**Reporting et analyses :** le contenu SCORM peut désormais signaler plusieurs tentatives de quiz dans les rapports L2. Le calcul du temps d’apprentissage passé est amélioré dans les relevés de notes des élèves. Les rapports Relevés de notes d’apprentissage pour les administrateurs sont mis à jour. Des améliorations de la recherche avancée sont disponibles.

**Méthode de connexion :** Découvrez comment fonctionne la connexion OpenID Connect dans Adobe Learning Manager pour les élèves, les auteurs et les administrateurs. OpenID Connect (OIDC) est une méthode de connexion courante basée sur des normes web. De nombreuses organisations utilisent
un fournisseur d’identité (par exemple, Okta, Google Workspace ou Microsoft Entra ID) pour les employés et les partenaires.

Voir [Se connecter avec OIDC](/help/migrated/oidc.md) pour plus d&#39;informations.

## Webhooks et migration dans les variantes et équivalents

### Webhooks

Lorsqu’un élève termine un cours via un autre ou une autre relation, ALM déclenche un événement webhook distinct du webhook d’achèvement de cours standard. Cela garantit que les intégrations peuvent répondre différemment aux autres finalisations si nécessaire. Les événements de webhook sont également déclenchés en cas d’achèvement rétroactif ou d’inachèvement rétroactif, couvrant les mises à jour historiques ainsi que les modifications de relation.

Voir [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-alternates) pour plus d’informations.

### Migration

Le modèle de données CSV et le comportement de migration pour introduire l’équivalence d’objet d’apprentissage (LO) dans le système sont décrits dans [Webhooks](/help/migrated/integration-admin/feature-summary/migration-manual.md#migration-for-alternates-and-equivalents).

## Purge automatique des utilisateurs supprimés

La purge automatique des utilisateurs supprimés est une fonctionnalité qui purge les données pour les utilisateurs qui ont déjà été supprimés dans ALM. La purge se produit après une période de rétention configurable, en se concentrant sur les opérations en bloc afin que les comptes clients volumineux puissent être gérés efficacement sans nuire aux performances.

Pour plus d&#39;informations, consultez [Purge automatique des utilisateurs supprimés](/help/migrated/administrators/feature-summary/purge-users.md#auto-purge-of-deleted-users).

## Définir le contrôle du temps d&#39;accès au module

L’amélioration permet aux auteurs et aux administrateurs de Adobe Learning Manager de définir une fenêtre temporelle pendant laquelle les élèves sont autorisés à démarrer un module. En dehors de la fenêtre de début/fin configurée, le module reste visible dans la structure du cours, mais les élèves ne peuvent pas le lancer.

Afficher [Définir le contrôle du temps d&#39;accès au module](/help/migrated/administrators/feature-summary/module-access-time-control.md) pour plus d&#39;informations.

## Modifications apportées aux relevés de notes des élèves

Cette version améliore le rapport Relevés de notes de l’apprentissage (LT) avec une prise en charge plus claire de l’auditabilité et de la conformité.

* Une nouvelle colonne Méthode d&#39;achèvement dans le LT administrateur indique si les déclarations de production ont été directes, alternatives ou révoquées, tandis que les déclarations de production alternatives influencent désormais le statut, la date d&#39;achèvement et la source d&#39;achèvement en utilisant les dates héritées des formations source et en se mettant à jour lorsque les origines sont révoquées ou que des déclarations de production directes se produisent.
* Les suppléants révoqués ajustent automatiquement le statut, la date d&#39;achèvement et la source d&#39;achèvement lorsque toutes les relations qualifiantes sont supprimées avec l&#39;option d&#39;inachèvement rétroactif activée.
* Les commentaires des réviseurs des modules de liste de contrôle sont standardisés dans la colonne des remarques des réviseurs renommés dans les LT d’administrateur et d’élève et tous les canaux d’exportation.
* Enfin, les calculs du temps d&#39;apprentissage distinguent désormais mieux le temps actif du temps inactif, ce qui améliore la précision des rapports d&#39;engagement et de conformité.

Consultez [Modifications apportées au rapport Relevé de notes de l&#39;élève](/help/migrated/administrators/feature-summary/reports/changes-in-learner-transcript.md) pour plus d&#39;informations.

## Liste de contrôle avec possibilité de commentaire pour le réviseur

Cette fonctionnalité permet aux réviseurs d’ajouter des commentaires pendant l’évaluation des listes de contrôle. Vous pouvez fournir des commentaires personnalisés et exploitables pour chaque élève. Vous pouvez également choisir d’afficher votre nom avec vos commentaires pour plus de transparence. Toutes les remarques sont enregistrées dans le relevé de notes de l’élève et incluses dans les rapports de liste de contrôle.

Afficher la [liste de contrôle avec commentaires](/help/migrated/authors/feature-summary/courses.md#checklist-with-commenting) pour plus d&#39;informations.

## Prise en charge multilingue de la liste de contrôle

Cette fonctionnalité vous permet de créer et de gérer des modules de liste de contrôle dans plusieurs langues. Chaque question de liste de contrôle, instruction et critère d&#39;évaluation peuvent être traduits afin que les réviseurs et les élèves interagissent avec la liste de contrôle dans leur langue préférée. Le système affiche la liste de contrôle dans la langue de contenu sélectionnée par l’utilisateur, ce qui améliore l’accessibilité et la conformité pour les équipes mondiales.

Afficher [Créer une liste de contrôle multilingue dans les modules](/help/migrated/authors/feature-summary/courses.md#create-a-multi-language-checklist)

## Pondération des questions de la liste de contrôle pour les évaluations des instructeurs

Cette fonctionnalité vous permet d’attribuer différents scores maximaux (pondération) à chaque question de liste de contrôle. Vous pouvez refléter l&#39;importance ou la difficulté variable de chaque question, ce qui favorise des évaluations plus précises et plus significatives. Le système calcule le score total en fonction de vos entrées et détermine si l’élève réussit ou échoue selon les critères que vous définissez.

Afficher [Créer des questions de liste de contrôle pondérées](/help/migrated/authors/feature-summary/courses.md#how-to-create-a-weighted-checklist)

## Certificats personnalisés

Les certificats personnalisés dans Adobe Learning Manager (ALM) permettent aux administrateurs et aux auteurs de concevoir, gérer et émettre des certificats personnalisés pour les élèves.

La fonctionnalité comprend un éditeur par glisser-déposer, des champs dynamiques, une prise en charge multilingue et des arrière-plans générés par l’IA, permettant aux organisations de créer des certificats de marque sans expertise technique.

Afficher [Créer des certificats personnalisés](/help/migrated/administrators/feature-summary/create-customize-certificate.md)

## Expérience hors connexion dans Experience Builder

L’expérience hors connexion dans Experience Builder permet aux organisations d’afficher leur contenu d’apprentissage et leurs pages de portail à tous les visiteurs, y compris ceux qui ne sont pas connectés. Cette fonctionnalité est conçue pour attirer, informer et impliquer les élèves potentiels en offrant un aperçu fluide et de marque de vos offres de formation avant qu’ils ne soient tenus de se connecter ou de s’inscrire.

Voir [Expérience hors connexion dans Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/non-logged-in-experience.md)

## Améliorations de la recherche avancée

Les résultats de la recherche avancée sont désormais plus précis et plus pertinents. Les correspondances de mots-clés exactes sont mieux classées à la fois dans la recherche de contenu et les métadonnées, ce qui permet aux élèves de trouver plus facilement ce qu&#39;ils recherchent précisément.

Les élèves peuvent désormais également voir les objets d’apprentissage inscrits dans les résultats de recherche, même s’ils ne font pas partie d’un catalogue accessible, ce qui garantit qu’aucun contenu pertinent n’est manqué. En outre, le classement des assistances à la tâche a été amélioré à la fois pour la recherche avancée et la recherche dans le contenu, afin de faire apparaître plus rapidement les ressources les plus pertinentes.

## Assistances à la tâche multilingues

Les assistances à la tâche multilingues dans Adobe Learning Manager (ALM) permettent aux auteurs et aux administrateurs de fournir des documents d’accompagnement, des guides ou des ressources dans plusieurs langues dans une seule entrée d’assistance à la tâche. Les élèves de différentes régions peuvent accéder aux documents pertinents dans leur langue préférée, ce qui améliore la compréhension, la conformité et l&#39;expérience utilisateur.

Affichez [Ajouter des assistances à la tâche multilingues](/help/migrated/authors/feature-summary/job-aids.md#create-a-multilingual-job-aid) pour plus d&#39;informations.

## Prise en charge des pistes de texte vidéo multilingues (VTT) (pour les auteurs)

La prise en charge des pistes de texte vidéo multilingues (VTT) dans Adobe Learning Manager permet aux auteurs de fournir des sous-titres et des légendes pour le contenu vidéo et audio dans plusieurs langues. Cette fonctionnalité rationalise la localisation, rend la formation accessible à un public international et garantit la conformité aux normes d’accessibilité. Les auteurs peuvent générer, traduire, réviser et modifier automatiquement les fichiers VTT directement sur la plateforme.

Pour plus d&#39;informations, consultez la [Prise en charge de VTT multilingue](/help/migrated/authors/feature-summary/content-library.md#multi-lingual-vtt-support).

## Afficher l&#39;auteur d&#39;origine des cours partagés dans les comptes de pairs

Lorsqu&#39;un cours est partagé via le catalogue avec un compte de pairs, Adobe Learning Manager nomme actuellement l&#39;auteur « Auteur externe » dans les vues Élève, Administrateur et Auteur du compte de réception. Cela peut poser des problèmes aux élèves et aux administrateurs, en particulier dans les grandes entreprises, car il devient difficile d’identifier et de contacter le propriétaire de contenu approprié lorsque des problèmes ou des questions surviennent.

L’amélioration garantit que les informations sur l’auteur sont conservées et affichées pour les cours partagés dans les comptes de pairs, plutôt que remplacées par un espace réservé générique.

### Nouveautés

Afficher le nom réel de l&#39;auteur pour les cours partagés dans les comptes de pairs

Pour les cours partagés via des catalogues externes ou de pairs, le nom de l’auteur d’origine du compte source s’affiche désormais dans le compte de réception au lieu de « Auteur externe ».

Cela s’applique :

* Application de l’élève (carte de cours ou détails du cours).
* Vues Administrateur et Auteur lors de la prévisualisation en tant qu’élève.

Afficher l&#39;affichage du [nom de l&#39;auteur pour les cours partagés](/help/migrated/administrators/feature-summary/peer-account.md#author-name-display-for-shared-courses-including-previously-acquired-courses) pour plus d&#39;informations.

## Équivalents et substituts

Proposez une expérience d’apprentissage fluide et éliminez les formations redondantes avec des équivalents et des suppléants dans ALM. Cette nouvelle fonctionnalité permet aux administrateurs de configurer des règles unidirectionnelles (alternatives) ou bidirectionnelles (équivalentes), où l’accomplissement d’une formation accorde automatiquement un achèvement alternatif pour une autre. Conçue pour rationaliser les grands écosystèmes d&#39;apprentissage, cette fonctionnalité permet aux élèves de contourner le contenu qu&#39;ils ont déjà maîtrisé et aux organisations de réduire considérablement les tickets de support administrateur, d&#39;éliminer les remplacements manuels et de conserver un dossier d&#39;élève plus propre et plus précis.

Voir [Équivalents et variantes](/help/migrated/administrators/feature-summary/alternates-equivalence.md) pour plus d&#39;informations.

## Codes QR de l&#39;instructeur pour l&#39;inscription et la présence à la session d&#39;instance

Les instructeurs peuvent générer des codes QR eux-mêmes pour :

* Inscription à l’instance de cours,
* Participation à la session, ou
* Inscription + participation ensemble

au niveau de la session. Il est conçu pour les situations où les élèves entrent dans une classe physique ou hybride et ont besoin d&#39;une option rapide et en libre-service pour s&#39;inscrire et enregistrer leur présence à l&#39;aide d&#39;un code QR.

Afficher [Télécharger les codes QR pour l&#39;inscription et la présence des élèves](/help/migrated/instructors/feature-summary/learners.md#download-qr-codes-for-learner-enrollment-and-attendance) pour plus d&#39;informations.

## Invitations au calendrier (ICS) avec liens de session

Adobe Learning Manager inclut le lien de participation à la **session directement dans les invitations au calendrier (fichiers ICS)** envoyées aux élèves et aux instructeurs. Cela permet aux participants de participer à des sessions directement à partir de leur calendrier sans rechercher l’adresse e-mail de la session.

Cette amélioration améliore l&#39;expérience des clients de calendrier tels que **Gmail** et **Outlook**.

Pour plus d&#39;informations, consultez les [invitations de calendrier avec des liens de session](/help/migrated/instructors/feature-summary/learners.md#joining-a-session-from-gmail).

## Assistant d’IA pour les élèves

L’assistant AI (Beta) pour les élèves les aide à trouver rapidement des réponses à partir du contenu d’apprentissage attribué sans parcourir l’intégralité des cours. Vous pouvez poser des questions dans un langage simple et recevoir des réponses précises et ciblées avec des liens sources vers le contenu du cours concerné.

Les capacités, les scénarios pris en charge et les limitations peuvent changer au fur et à mesure de l’évolution de la fonctionnalité. L’assistant AI est un compagnon de chat alimenté par l’IA générative dans Adobe Learning Manager qui fournit des réponses rapides et précises à l’aide de votre contenu d’apprentissage de confiance. Il comprend des citations afin que vous sachiez toujours la source de l&#39;information.

Voir [Assistant IA pour les élèves](/help/migrated/learners/feature-summary/learner-ai-assistant.md)


## Modifications d’API dans la version

La version d’avril 2026 de Adobe Learning Manager introduit des améliorations ciblées de l’API publique concernant les alternatives et les équivalents, l’accès au contenu par fenêtre temporelle, les tentatives de quiz axées sur le contenu, les expériences hors connexion et la gestion des assistances à la tâche. Les modifications sont conçues pour être largement rétrocompatibles, tout en permettant des intégrations plus précises.

Afficher les [modifications d&#39;API dans la version d&#39;avril](/help/migrated/api-changes-alm.md)

## Configuration système

Voir [Configuration requise pour Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notes de mise à jour

Consultez les [notes de mise à jour](/help/migrated/release-note/release-notes.md) pour connaître les dernières mises à jour.

## Versions précédentes d’Adobe Learning Manager

* [Version d’octobre 2025 de Adobe Learning Manager](/help/migrated/whats-new-october-2025.md)
* [Version de mai 2025 de Adobe Learning Manager](/help/migrated/whats-new-may-2025.md)
