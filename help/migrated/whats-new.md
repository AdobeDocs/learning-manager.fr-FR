---
description: Découvrez les nouvelles fonctionnalités et les améliorations de la version d’octobre 2025 de Adobe Learning Manager
jcr-language: en_us
title: Nouveautés de la version d’octobre 2025 de Adobe Learning Manager
source-git-commit: fcc50e80f94bdcbc8de2cddac92f1a12b55e1e18
workflow-type: tm+mt
source-wordcount: '5638'
ht-degree: 0%

---


# Nouveautés de la version d’octobre 2025 de Adobe Learning Manager

La version d’octobre 2025 de Adobe Learning Manager introduit des améliorations significatives conçues pour améliorer la précision des rapports, étendre les capacités d’intégration et améliorer l’expérience d’apprentissage pour les administrateurs, les auteurs et les élèves.

* Experience Builder : concevez des portails d’apprentissage entièrement personnalisés en fonction des rôles et de la marque, en fonction des besoins de votre entreprise. Créez des portails d’apprentissage de marque, basés sur des rôles, avec des widgets, des menus et des pages.
* Balisage social dans les forums d’apprentissage : les élèves peuvent désormais baliser leurs homologues à l’aide de @username dans les publications et les commentaires, permettant une collaboration et des notifications ciblées au sein des communautés d’apprentissage par les réseaux sociaux.
* Autorisations d&#39;annonces étendues : les administrateurs personnalisés peuvent créer des annonces limitées aux groupes d&#39;utilisateurs ou aux catalogues qui leur sont attribués, garantissant une communication ciblée et réduisant la surcharge d&#39;informations.
* Suivi de la progression basé sur la langue : la progression de l’élève est désormais enregistrée indépendamment pour chaque langue, ce qui permet de passer facilement d’une langue à l’autre sans perdre sa progression.
* Gestion incrémentielle des rôles personnalisés : les administrateurs peuvent désormais gérer les rôles personnalisés plus efficacement grâce à la prise en charge des importations incrémentielles et multi-incrémentielles dans Adobe Learning Manager.
* API améliorées pour l’analyse et la migration : les API nouvelles et améliorées offrent un meilleur suivi des performances du quiz, une surveillance de l’état de la migration et la prise en charge du balisage des utilisateurs dans l’apprentissage par les réseaux sociaux.

## Experience Builder

>[!IMPORTANT]
>
>Nous sommes ravis d’annoncer qu’Experience Builder, l’outil innovant de création de portails d’apprentissage personnalisables, sera disponible après la version d’octobre 2025 de Adobe Learning Manager.
>
>Restez à l’affût des mises à jour à l’approche de la date de publication. Nous avons hâte de voir comment vous utiliserez Experience Builder pour transformer vos portails d’apprentissage.
>
>Pour toute question ou information supplémentaire, contactez votre gestionnaire de succès client.

Experience Builder est un outil sans code/à code faible dans Adobe Learning Manager qui vous aide à créer des portails d’apprentissage personnalisés. Il vous permet de concevoir des portails d’apprentissage conviviaux et de marque sans avoir besoin de compétences techniques ou de connaissances approfondies en codage.
Avec Experience Builder, les administrateurs peuvent facilement créer des pages, des menus et des widgets pour offrir des expériences d’apprentissage personnalisées adaptées à leur public.

Avant Experience Builder, les entreprises étaient confrontées à plusieurs défis :

1. **Personnalisation limitée** : les portails avaient des conceptions fixes avec peu d’options pour refléter votre marque. Les administrateurs pouvaient uniquement apporter des modifications de base, telles que la modification des en-têtes, des pieds de page ou des couleurs, ce qui limitait la possibilité de créer des expériences uniques.
2. **Coût** : la création de portails personnalisés a nécessité des développeurs coûteux et de longs délais, qui prennent souvent de 6 à 9 mois. Cette approche a augmenté le coût total de possession et retardé le déploiement.
3. **Expériences génériques** : tout le monde a vu le même contenu, même s’il n’était pas pertinent pour son rôle ou ses besoins. Ce manque de personnalisation a réduit l’engagement et la satisfaction des élèves.
4. **Obstacles techniques** : les administrateurs non techniques ont eu du mal à créer ou à mettre à jour les portails car ils avaient besoin de connaissances en codage ou d&#39;un soutien externe.

Experience Builder résout ces problèmes en fournissant une solution simple, sans code/avec code bas pour créer des portails personnalisés de marque.

Cela permet aux administrateurs de concevoir des portails qui répondent aux besoins de leur organisation sans faire appel à une expertise technique ou à des développeurs externes.

**Cas d’utilisation**

* **Portails de marque** : créez un portail qui correspond au site Web de votre entreprise avec des logos, des couleurs et des mises en page. Par exemple, une entreprise de soins de santé peut concevoir un portail qui reflète son image de marque tout en fournissant du contenu d&#39;apprentissage.
* **Apprentissage basé sur les rôles** : créez des pages adaptées à des rôles spécifiques. Les équipes commerciales peuvent consulter les formations sur les produits, tandis que les ingénieurs accèdent aux cours techniques.
* **Formation aux produits** : configurez des pages dédiées pour différents produits, tels que Photoshop ou Illustrator, avec des widgets affichant des cours, des certifications et des ressources associées.

Consultez [Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/overview.md) pour plus d’informations sur la création de pages personnalisées à l’aide de widgets.

## Progression de l’élève en fonction de la langue

Actuellement, Adobe Learning Manager ne suit la progression des élèves que pour la langue des paramètres régionaux sélectionnée, ce qui entraîne une perte de progression significative lors du changement de langue/de paramètres régionaux dans le lecteur. Cette limitation peut entraîner une mauvaise expérience utilisateur, car les élèves peuvent perdre leur progression lors de l’accès au contenu dans différentes langues. La progression de chaque module du lecteur est suivie au niveau de l’utilisateur et du module. Cela conduit à une situation où la progression d&#39;un utilisateur est remplacée lorsqu&#39;il revient à un paramètre régional précédemment utilisé pour le même module.

Par exemple, si un élève atteint 75 % de progression dans la langue A (anglais), puis passe à la langue B (espagnol), lors du retour à la langue A, sa progression est réinitialisée à 0 % au lieu de reprendre à 75 %.

Pour résoudre ces limitations, la fonctionnalité a été améliorée pour prendre en charge le suivi de la progression spécifique aux paramètres régionaux :

* **Stockage spécifique aux paramètres régionaux** : lorsqu&#39;un élève change de paramètres régionaux (par exemple, de Paramètres régionaux A à Paramètres régionaux B) dans le lecteur, Adobe Learning Manager enregistre désormais l&#39;état de progression séparément pour chaque paramètre régional du contenu.
* **Reprise de la progression** : lorsque l&#39;utilisateur revient à un paramètre régional précédemment utilisé (de la langue B à la langue A), le contenu reprend là où il s&#39;était arrêté dans ce paramètre régional spécifique.
* **Suivi de progression indépendant** : chaque paramètre régional conserve son propre état de progression, ce qui permet aux élèves d&#39;explorer le contenu dans plusieurs langues sans perdre leur progression individuelle dans chaque langue.

Les types de contenu suivants ne sont pas pris en charge pour la progression des élèves basée sur la langue :

* Le contenu vidéo et audio n’est pas pris en charge.
* Le contenu tiers, notamment Go1, LinkedIn Learning, getAbstract et Harvard ManageMentor, n’est pas pris en charge.
* La progression n’est pas suivie ou enregistrée pour le contenu qui n’envoie pas de données au magasin des enregistrements d’apprentissage (LRS).
* Les utilisateurs de l’application mobile ne peuvent pas suivre la progression de cette fonctionnalité en mode hors ligne.

Consultez [Mon apprentissage](/help/migrated/learners/feature-summary/courses.md#language-based-progress-management) pour plus d&#39;informations sur la progression de l&#39;élève en fonction de la langue.

## Prise en charge incrémentielle et multi-incrémentielle des rôles personnalisés

Adobe Learning Manager prend désormais en charge les importations incrémentielles et multi-incrémentielles pour les rôles personnalisés et les attributions de rôles. Avec les importations incrémentielles, les administrateurs peuvent uniquement charger de nouveaux enregistrements, des enregistrements mis à jour ou des enregistrements supprimés des utilisateurs au lieu de retélécharger l’intégralité du fichier CSV.

Les importations multi-incrémentielles étendent cette fonctionnalité en permettant aux grandes organisations de fractionner les fichiers incrémentiels par région ou département (par exemple, États-Unis, UE, APAC) et de les traiter en parallèle. Adobe Learning Manager prend également en charge jusqu’à 20 fichiers CSV utilisateur incrémentiels et les fichiers CSV de rôles personnalisés correspondants, ce qui le rend évolutif pour les opérations de grande envergure.

Les administrateurs peuvent désormais charger des fichiers de rôle et de rôle utilisateur (role.csv et user_role.csv) de manière incrémentielle, ainsi que des fichiers utilisateur (user.csv), au lieu de toujours effectuer des chargements complets. Chaque importation utilisateur (user1.csv) est liée à ses propres fichiers de rôle et de mappage de rôle (user1_role.csv, user1_user_role.csv), stockés dans des dossiers FTP distincts.

Trois colonnes supplémentaires ont été ajoutées aux fichiers CSV suivants :

* État d’enregistrement de l’utilisateur (user.csv) : indique le statut d’enregistrement actuel de l’utilisateur dans le système (par exemple, actif, inactif ou supprimé).
* État du rôle (role.csv) : indique si un rôle personnalisé est actuellement actif ou inactif dans le compte.
* État du rôle utilisateur (user_role.csv) : définit l&#39;état du mappage entre un utilisateur et un rôle, en indiquant si l&#39;affectation est active ou a été supprimée.

Adobe Learning Manager capture désormais les actions d’ajout, de mise à jour et de suppression dans les rapports d’audit des utilisateurs et de rôle personnalisé, ce qui permet aux administrateurs d’avoir une meilleure visibilité sur les modifications.

>[!NOTE]
>
>Ces modifications s’appliquent uniquement aux comptes qui utilisent des utilisateurs incrémentiels.

Consultez [Prise en charge incrémentielle et multi-incrémentielle des rôles personnalisés](/help/migrated/integration-admin/feature-summary/configure-role-csv-files.md#incremental-and-multi-incremental-support-for-custom-roles) pour plus d&#39;informations sur la prise en charge incrémentielle et multi-incrémentielle des rôles personnalisés.

## Améliorations de l’intégration Go1

L’intégration Go1 est améliorée pour permettre la curation directe des cours Go1 pour la création de programmes d’apprentissage (LP) dans Adobe Learning Manager. Cette mise à jour prend en charge l’inclusion de cours Go1 dans les certifications récurrentes et introduit une nouvelle version de l’expérience du hub de contenu Go1, permettant une curation plus efficace des cours.

* Créez et gérez des listes de lecture directement dans Go1 à l’aide de l’assistance par chat IA ou de la sélection manuelle.
* Incluez les cours Go1 dans les cycles de certification récurrents avec réinitialisation automatique de la progression. Afficher [Certifications](/help/migrated/administrators/feature-summary/certifications.md) pour plus d&#39;informations sur la création de certificats.
* Interface de découverte de contenu mise à niveau pour améliorer la navigation et la curation du contenu.

**Remarques importantes**

* Toutes les fonctionnalités Go1 nécessitent une licence Go1 active.
* Le contenu Go1 gratuit précédent sera mis hors service. Les organisations doivent prévisualiser et acheter les offres groupées de contenu requises.
* Les administrateurs et les auteurs peuvent créer et gérer des listes de lecture ; les élèves conservent un accès en lecture seule.

Consultez [Curater des cours Go1 dans le parcours d’apprentissage](/help/migrated/administrators/feature-summary/content-marketplace/curate-go1-playlist.md) pour plus d’informations sur l’ajout de cours Go1 au parcours d’apprentissage.

## Prise en charge des URL vidéo dans le module Activité

Le module Activité prend désormais en charge l’intégration des URL Vimeo, comme les intégrations YouTube. Cette amélioration permet aux administrateurs d’ajouter des liens vidéo Vimeo directement dans le module Activité. Lorsque les auteurs créent un cours et ajoutent un module d’activité, ils voient désormais une option permettant d’inclure une URL Vimeo. Comme pour l’ajout de liens YouTube, les auteurs peuvent coller un lien Vimeo directement dans la configuration du module. Une fois publiée, les élèves peuvent lire la vidéo Vimeo de manière transparente dans l’application de l’élève sans être redirigés en dehors de la plateforme.

Consultez [Ajouter des modules](/help/migrated/authors/feature-summary/courses.md#add-modules) pour plus d&#39;informations sur l&#39;ajout de modules aux cours.

## Informations de fuseau horaire pour les modules CR/VC

Les détails du fuseau horaire sont désormais affichés pour les modules Salle de classe (CR) et Salle de classe virtuelle (VC) sur la page Présentation du cours, la page Instance, la page Aperçu de l’élève et dans le widget Calendrier. Les élèves et les administrateurs peuvent clairement voir le fuseau horaire associé aux sessions planifiées sur les pages clés et les invitations au calendrier. Les élèves peuvent mieux planifier et participer aux sessions sans erreurs de fuseau horaire. Cette amélioration est disponible uniquement dans l’application d’apprentissage immersif.

Les élèves de différentes régions peuvent confirmer l’heure de la session dans le fuseau horaire approprié. L’affichage du fuseau horaire permet d’éviter les sessions manquées et garantit une planification précise du calendrier.

## Renseignez automatiquement le nom de l&#39;auteur lors de la création d&#39;un cours

Lors de la création du cours, le champ **[!UICONTROL Auteur(s)]** est désormais renseigné automatiquement avec le nom des auteurs qui créent le cours. Les auteurs n’ont plus besoin de saisir manuellement leurs propres noms. D’autres auteurs peuvent toujours être ajoutés ou mis à jour selon les besoins.

Pour les organisations avec des règles de propriété du contenu strictes, le remplissage automatique garantit que les auteurs sont toujours correctement attribués. Lors de la modification d&#39;un cours existant, les auteurs peuvent mettre à jour ou ajouter des coauteurs sans perdre l&#39;entrée renseignée automatiquement.

Consultez [Créer un cours](/help/migrated/authors/feature-summary/courses.md#create-a-course---advanced-workflow) pour plus d&#39;informations sur la création d&#39;un cours.

## Rechercher des profils externes lors de la modification du profil

Auparavant, les administrateurs faisaient défiler la liste complète des profils externes et sélectionnaient manuellement le profil souhaité lors de la réaffectation des élèves. Le processus était alors très long, en particulier pour les comptes avec de nombreux profils. Grâce à cette amélioration, les administrateurs et les administrateurs personnalisés peuvent désormais rechercher des profils externes directement dans l’onglet pendant le processus de modification du profil.

**Cas d’utilisation**

* Dans les comptes avec des centaines de profils externes (par exemple, les emplacements de franchise, les sociétés partenaires ou les groupes régionaux), les administrateurs peuvent désormais localiser le profil exact instantanément à l’aide de la recherche, ce qui réduit les erreurs et fait gagner du temps.
* Lors de changements organisationnels, tels que des fusions ou des réalignements de service, les élèves peuvent devoir être déplacés en bloc vers de nouveaux profils externes. La réaffectation basée sur la recherche rend cette tâche plus fluide et plus précise.

Affichez [Modifier le profil externe](/help/migrated/administrators/feature-summary/add-users-user-groups.md#change-profile) pour plus d&#39;informations sur la modification du profil.

## Ajout d’un coorganisateur pour les sessions de Microsofts Teams

Auparavant, les auteurs ne pouvaient affecter qu’un seul organisateur aux sessions de Microsoft Teams. Grâce à cette amélioration, les administrateurs peuvent désormais ajouter des co-organisateurs à une session. Un nouveau champ, **[!UICONTROL Co-organisateur]**, a été introduit dans les sessions de Microsofts Teams, permettant aux auteurs d’affecter des organisateurs supplémentaires en plus de l’organisateur principal.

Les auteurs peuvent affecter plusieurs coorganisateurs à chaque session de Microsofts Teams. Les co-organisateurs disposent des mêmes droits d’accès et autorisations que l’organisateur principal. Les auteurs peuvent ajouter jusqu’à 10 organisateurs par session, ce qui offre une plus grande flexibilité et améliore la gestion des sessions.

**Cas d&#39;utilisation**

Lors de sessions à grande échelle avec de nombreux élèves, les co-organisateurs peuvent aider à gérer l&#39;assiduité, modérer les discussions et surveiller le chat pendant que l&#39;organisateur principal se concentre sur la prestation de la formation.

Consultez l&#39;article [Ajouter des modules](/help/migrated/authors/feature-summary/courses.md#add-modules) pour plus d&#39;informations sur l&#39;ajout de sessions CR/VC aux cours.

## Télécharger le rapport des élèves intéressés

Lorsqu&#39;un administrateur retire toutes les instances de cours (par exemple, à la fin du cycle de vie du cours), le bouton **[!UICONTROL S&#39;inscrire]** sur la page **[!UICONTROL Présentation du cours]** est remplacé par une option [!UICONTROL Enregistrer vos intérêts]. Les élèves peuvent sélectionner cette option pour exprimer leur intérêt à suivre le cours. Les administrateurs peuvent désormais afficher et exporter une liste d&#39;élèves qui se sont inscrits à un cours.

Les administrateurs peuvent ensuite accéder à cette liste et la télécharger sous forme de rapport. Un bouton **[!UICONTROL Élèves intéressés]** a été ajouté à la page du cours lorsqu&#39;aucune instance active n&#39;est disponible. Le nom de l’élève et la date à laquelle il s’est inscrit à l’interface utilisateur de l’administrateur s’affichent.

Les administrateurs peuvent sélectionner les **[!UICONTROL actions]**, puis sélectionner **[!UICONTROL Exporter le rapport]** pour exporter le **[!UICONTROL rapport sur les élèves intéressés]**.

![](assets/register-interest.png)
_Section Présentation du cours où les élèves peuvent afficher l&#39;option Enregistrer leur intérêt_

Afficher [Télécharger l&#39;élève intéressé](/help/migrated/administrators/feature-summary/courses.md#download-the-interested-learner-report) pour plus d&#39;informations.

## Réinitialisation des recommandations dans l’application Salesforce

Auparavant, les élèves utilisant l’application Adobe Learning Manager Salesforce ne pouvaient sélectionner les rôles et les préférences de recommandation qu’une seule fois. Si leur rôle a changé, ils ont dû basculer vers l’application Adobe Learning Manager native pour mettre à jour leur profil et recevoir les recommandations de cours pertinentes. Grâce à la dernière amélioration, les élèves peuvent désormais réinitialiser rapidement leurs préférences directement dans l’application Salesforce chaque fois que leur rôle, leur équipe ou leurs responsabilités professionnels changent.

Ce processus rationalisé leur permet de continuer à recevoir des recommandations de cours pertinentes et mises à jour sans quitter Salesforce. Les administrateurs bénéficient de taux d’achèvement de la formation plus élevés et d’un meilleur alignement entre les rôles d’utilisateur et le contenu recommandé, le tout sans fournir d’assistance ou de conseils supplémentaires sur le changement de plate-forme.

Adobe Learning Manager propose désormais un bouton **[!UICONTROL Réinitialiser les centres d’intérêt]** dans l’application Salesforce. Les élèves peuvent désormais réinitialiser leurs rôles et préférences d’apprentissage sans avoir à quitter Salesforce ou à se connecter à l’application Adobe Learning Manager native.

Consultez [Réinitialiser les recommandations dans l’application Salesforce](/help/migrated/learners/feature-summary/sfdc-app.md#reset-recommendations-in-salesforce-app) pour plus d’informations sur les recommandations de réinitialisation dans l’application Salesforce.

## Amélioration du widget Calendrier

Les élèves peuvent désormais voir les sessions passées et à venir dans le widget Calendrier. Ils peuvent parcourir le calendrier jusqu’à n’importe quelle date et vérifier les détails de la session. Cela signifie qu’ils peuvent examiner les sessions qui ont déjà eu lieu, ce qui leur permet de suivre ce qu’ils ont manqué ou assisté. Ils peuvent également visualiser toutes les sessions à venir pour les 24 prochains mois, y compris le mois en cours, ce qui facilite la planification et la gestion de leurs plannings.

Afficher le [calendrier](/help/migrated/learners/feature-summary/learner-home-page.md#calendar) pour plus d&#39;informations sur le widget Calendrier.

## Balisage des utilisateurs dans les forums de réseaux sociaux

Les forums de réseaux sociaux prennent désormais en charge la fonctionnalité de balisage des utilisateurs, permettant des discussions plus ciblées et une meilleure collaboration au sein des communautés d’apprentissage. Les élèves peuvent être balisés dans les publications et les commentaires d’apprentissage par les réseaux sociaux via l’application d’élève, les API et le site de référence Adobe Learning Manager.

Impossible de baliser les utilisateurs en dehors de la portée du forum, ce qui empêche les notifications indésirables. Si un utilisateur balisé est supprimé du système, sa mention apparaît comme « anonyme ». Le balisage des groupes d&#39;utilisateurs ou « @all » n&#39;est pas autorisé pour empêcher le spam de notification.

* **@username** : les utilisateurs peuvent baliser d&#39;autres membres du forum à l&#39;aide du format « @username ».
* **Balisage limité à la portée** : seuls les utilisateurs ayant accès au forum spécifique peuvent être balisés, ce qui garantit la confidentialité et la pertinence.
* **Notifications multicanaux** : les utilisateurs balisés reçoivent des notifications dans l’application et par e-mail avec des liens directs vers les publications ou commentaires pertinents.

**Cas d’utilisation**

* Professionnels de la santé à la recherche de commentaires de collègues spécifiques sur des cas médicaux : le balisage permet aux médecins et aux infirmières d&#39;informer rapidement les bons spécialistes, assurant des conseils opportuns et précis sur des cas de patients complexes.
* Consulter des experts sur des sujets spécialisés : en marquant les experts, les équipes peuvent impliquer directement les bonnes personnes, réduire le temps de réponse et améliorer la prise de décision pour les requêtes techniques ou de niche.
* Discussions en équipe nécessitant la contribution de parties prenantes spécifiques : le balisage des parties prenantes garantit que les décideurs concernés sont au courant des mises à jour et peuvent fournir des commentaires, ce qui permet de maintenir les projets sur la bonne voie et de les aligner sur les objectifs commerciaux.

Consultez [Balisage des utilisateurs dans les forums de réseaux sociaux](/help/migrated/learners/feature-summary/social-learning-web-user.md#tag-users-in-social-board-posts) pour plus d&#39;informations sur le balisage des utilisateurs dans les forums de réseaux sociaux.

## Autorisations d’annonce étendues pour les administrateurs personnalisés

Les administrateurs personnalisés peuvent désormais créer des annonces, mais uniquement pour les groupes d&#39;utilisateurs ou les catalogues qui leur sont attribués. Cela empêche toute communication involontaire au-delà des frontières de l’entreprise. Les administrateurs personnalisés peuvent uniquement créer des annonces pour les utilisateurs faisant partie de leur portée assignée. Les annonces peuvent être limitées à des groupes d&#39;utilisateurs ou des catalogues spécifiques. Les administrateurs complets conservent la visibilité et le contrôle de toutes les annonces, y compris celles créées par les administrateurs personnalisés étendus.

**Principaux avantages**

* Communication ciblée garantissant que les annonces n&#39;atteignent que les publics concernés.
* Réduction de la surcharge d’informations en empêchant les notifications non pertinentes d’atteindre des utilisateurs non prévus.
* Maintient les limites organisationnelles et empêche les communications croisées accidentelles.

**Remarques importantes**

* Si la portée d&#39;un administrateur personnalisé change, les annonces affectées affichent une icône d&#39;avertissement et nécessitent des réinitialisations de portée individuelles.
* Chaque annonce doit être mise à jour individuellement lorsque des modifications de portée se produisent.
* Le rapport [Annonce de notification](/help/migrated/administrators/feature-summary/announcements.md) affiche uniquement les élèves dans la portée affectée par l&#39;administrateur personnalisé.

**Cas d’utilisation**

* Organismes de franchise où les gestionnaires régionaux doivent communiquer uniquement avec leurs franchisés.
* Grandes organisations avec des administrateurs régionaux ou départementaux ciblant les annonces à leurs équipes.

Voir [Créer une annonce pour la portée affectée](/help/migrated/administrators/feature-summary/announcements.md#create-announcement-for-the-assigned-scope) pour plus d&#39;informations sur la création d&#39;une annonce pour la portée affectée.

## Sélectionner un rôle personnalisé lors de la publication d’un contenu à partir d’Adobe Captivate

Lors de la publication de contenu d’Adobe Captivate vers Adobe Learning Manager, si un utilisateur a plusieurs rôles personnalisés, il sera invité à sélectionner le rôle personnalisé spécifique sous lequel le cours doit être publié. Cela garantit que la propriété et les autorisations correctes du rôle sont appliquées au cours publié.

Consultez [Rôle personnalisé](/help/migrated/administrators/feature-summary/custom-role.md) pour plus d&#39;informations sur la création de rôles personnalisés pour les utilisateurs.

## Améliorations apportées au widget Enregistré par moi

Auparavant, la sélection de la bande **[!UICONTROL Enregistré par moi]** affichait tous les cours disponibles dans le catalogue. Désormais, les élèves ne voient que leurs cours marqués d&#39;un signet dans la bande **[!UICONTROL Enregistré par moi]** sur la page d&#39;accueil de l&#39;élève. En sélectionnant cette bande, les élèves accèdent à la page du catalogue, où seuls les cours qu&#39;ils ont enregistrés sont affichés.

Dans le catalogue, les élèves peuvent appliquer des filtres supplémentaires pour affiner leur recherche. Lorsqu’un filtre est appliqué, seuls les cours qui répondent aux critères sélectionnés sont affichés. Les cours précédemment marqués d’un signet s’affichent uniquement s’ils correspondent au filtre appliqué.

Consultez [Configurer les widgets de cours enregistrés dans les sites AEM](/help/migrated/integrate-aem-learning-manager.md#configure-my-saved-courses-widgets-in-aem-sites) pour plus d&#39;informations sur le widget de cours enregistrés dans les sites AEM.

## Prise en charge de l’affichage des noms des auteurs dans les cours partagés

Auparavant, lorsqu&#39;un cours était partagé avec un [compte de pairs](/help/migrated/administrators/feature-summary/peer-account.md), l&#39;auteur apparaissait en tant qu&#39;auteur externe. Désormais, les cours affichent le nom de l’auteur, qu’il s’agisse d’un utilisateur interne du compte principal ou d’un auteur hérité (c’est-à-dire, tout nom saisi sous forme de chaîne dans le champ Auteurs lors de la création du cours). La sélection d’un auteur affiche le nombre de cours qu’il a partagés avec le compte de pairs ; toutefois, ces auteurs ne sont pas de vrais utilisateurs du compte de pairs.

Si un utilisateur est supprimé du compte principal, ses données y sont supprimées, mais les informations sur l’auteur restent dans tous les comptes de pairs où son contenu a été partagé.

>[!NOTE]
>
>Il s&#39;agit d&#39;une fonctionnalité basée sur des indicateurs. Contactez notre équipe du service clientèle à l&#39;adresse [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) pour activer cette option.

Consultez [Compte d&#39;homologue](/help/migrated/administrators/feature-summary/peer-account.md) pour plus d&#39;informations sur le partage de contenu avec un compte d&#39;homologue.

## Visibilité de la recherche pour les objets d’apprentissage de niveau inférieur

Auparavant, les résultats de recherche n’affichaient pas systématiquement les cours individuels lorsqu’ils faisaient partie d’objets d’apprentissage de niveau supérieur tels que les parcours d’apprentissage ou les certifications. Si un élève était inscrit uniquement à un parcours d’apprentissage ou à une certification, la recherche renvoyait uniquement la structure de niveau supérieur et non le cours individuel.

Grâce à cette amélioration, les élèves peuvent désormais voir des cours individuels dans les résultats de recherche, même si ces cours font partie de parcours d’apprentissage ou de certifications. Un nouveau paramètre d&#39;administrateur, **[!UICONTROL Afficher tous les cours inscrits dans les résultats de recherche]**, a été introduit. Lorsque cette option est activée, ce paramètre garantit que la recherche d’un cours spécifique affiche toujours le cours lui-même ainsi que les parcours d’apprentissage ou certifications associés.

Consultez [Paramètres](/help/migrated/administrators/feature-summary/settings.md#general-settings) pour plus d&#39;informations sur les paramètres généraux.

## Modifications de l’API

### Améliorations de l’API de migration

Adobe Learning Manager prend désormais en charge la migration de divers objets de données vers un compte via le processus de migration. Ce processus peut être lancé via les API et l’interface utilisateur. Lorsqu’une migration échoue, des erreurs sont disponibles au téléchargement via l’interface. Ces erreurs sont utiles pour déboguer les erreurs de migration et gérer les exécutions de migration.

Avec cette version, les journaux d’erreurs seront également disponibles au téléchargement via les API pour un suivi et un débogage des erreurs par programmation efficaces.

**Modifications d’API**

Il existe une nouvelle API de migration, `runStatus`, qui permet aux administrateurs d’intégration de vérifier l’état des exécutions de migration déclenchées via l’API, ce qui n’était pas possible dans les versions précédentes de Adobe Learning Manager.

En outre, l&#39;API `runStatus` fournit désormais un lien direct pour télécharger les journaux d&#39;erreurs (CSV) pour les exécutions terminées. Notez que le lien est valide pendant sept jours uniquement et que les journaux sont conservés pendant un mois.

La réponse de l&#39;API `startRun` a été mise à jour pour inclure l&#39;ID de projet de migration, l&#39;ID de sprint et l&#39;ID de série de sprint, qui sont requis pour interroger le nouveau point de terminaison d&#39;état.

#### API runStatus

**Description**

Récupère l&#39;état d&#39;une exécution de migration existante.

**Point de terminaison**

```
GET /bulkimport/runStatus
```

**Paramètres**

* **migrationProjectId** : (obligatoire). Identificateur unique d&#39;un projet de migration. Un projet de migration est utilisé pour transférer des données et du contenu d’un système de gestion de l’apprentissage (LMS) existant vers Adobe Learning Manager. Chaque projet de migration peut se composer de plusieurs sprints, qui sont des unités plus petites de tâches de migration.

* **sprintId** : (obligatoire). Identificateur unique d’un sprint dans un projet de migration. Un sprint est un sous-ensemble de tâches de migration qui inclut des éléments d’apprentissage spécifiques (par exemple, cours, modules, dossiers d’élève) à migrer d’un LMS existant vers Adobe Learning Manager. Chaque sprint peut être exécuté indépendamment, ce qui permet une migration progressive.

* **sprintRunId** : (obligatoire). Identificateur unique utilisé pour suivre l’exécution d’un sprint spécifique dans un projet de migration. Elle est associée au processus de migration réel des éléments définis dans un sprint. Le sprintRunId permet de surveiller, de dépanner et de gérer le travail de migration.

**Réponse**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

#### API startRun

La réponse API `startRun` a été mise à jour pour inclure trois champs supplémentaires : migrationProjectId, sprintId et sprintRunId. Ces champs permettent aux utilisateurs de suivre et d’interroger l’état d’exécutions de migration spécifiques à l’aide de la nouvelle API runStatus.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Produit la réponse suivante. La réponse contient :

* `migrationId`
* `sprintId`
* `sprintRunId`

**Réponse**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

Consultez le [Manuel de migration](/help/migrated/integration-admin/feature-summary/migration-manual.md) pour plus d’informations sur la migration du contenu à partir du LMS existant.

### Modifications de l’API pour les réseaux sociaux (balise utilisateur, commentaires et réponses)

Adobe Learning Manager prend désormais en charge la fonctionnalité de balisage des @user dans les forums de réseaux sociaux, ce qui permet aux élèves de mentionner et d’informer leurs homologues dans les publications, les commentaires et les réponses. Cette fonctionnalité améliore la collaboration et la découverte de contenu sur toute la plateforme.

Cette version introduit de nouvelles fonctionnalités d’API pour prendre en charge les mentions d’utilisateurs, y compris un POST et des points de terminaison de GET améliorés, ainsi qu’une nouvelle fonctionnalité de recherche pour les utilisateurs balisés.

**Présentation des modifications d’API**

* API de POST mises à jour pour la création de publications/commentaires/réponses avec des mentions d’utilisateur
* API GET mises à jour avec les données de mention utilisateur dans les réponses

**Format des mentions utilisateur**

Un utilisateur est mentionné en utilisant le format : @(utilisateur:userId)

#### Créer un post avec des mentions

**Point de terminaison**

```
POST /primeapi/v2/posts
```

**Description**

Créez une nouvelle publication d’apprentissage par les réseaux sociaux avec des mentions d’utilisateur.

**Corps de la demande**

```
{
  "data": {
    "type": "post",
    "attributes": {
      "boardId": 13282,
      "accountId": 11152,
      "text": "<p>This is a new post mentioning @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "postType": "discussion"
    },
    "id": null
  }
}
```

**Réponse**

Réponse de post-création standard avec les données de mention incluses dans la relation _userMentions_.

#### Créer un commentaire avec des mentions

**Point de terminaison**

```
POST /primeapi/v2/comments
```

**Description**

Ajoutez un commentaire à une publication avec des mentions d’utilisateur.

**Corps de la demande**

```
{
  "data": {
    "type": "comment",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Test Comment @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 0
    },
    "id": null
  }
}
```

#### Créer une réponse avec des mentions

**Point de terminaison**

```
POST /primeapi/v2/replies
```

**Description**

Réponse à un commentaire avec des mentions d’utilisateur.

**Corps de la demande**

```
{
  "data": {
    "type": "reply",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Thanks for the update @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 1,
      "parentCommentId": 55621
    },
    "id": null
  }
}
```

#### Récupérer les publications avec des mentions

**Point de terminaison**

```
GET /primeapi/v2/posts/{id}
```

**Description**

Récupérez les détails de la publication, y compris les utilisateurs mentionnés.

**Réponse**

```
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/posts/7522"
  },
  "data": {
    "id": "7522",
    "type": "post",
    "attributes": {
      "commentCount": 3,
      "dateCreated": "2025-06-10T11:33:29.000Z",
      "dateUpdated": "2025-06-25T14:52:04.000Z",
      "downVote": 0,
      "postingType": "DEFAULT",
      "richText": "<p>my updated fourth post @[user:14707776] second mention my first post</p>",
      "state": "ACTIVE",
      "text": "my updated fourth post @[user:14707776] second mention my first post",
      "upVote": 0,
      "viewsCount": 0
    },
    "relationships": {
      "createdBy": {
        "data": {
          "id": "14707776",
          "type": "user"
        }
      },
      "parent": {
        "data": {
          "id": "3971",
          "type": "board"
        }
      },
      "userMentions": {
        "data": [
          {
            "id": "14707776",
            "type": "user"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "14707776",
      "type": "user",
      "attributes": {
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "binUserId": "45664b87-75a3-43ec-b0b7-5064958eac6f",
        "email": "user@example.com",
        "enrollOnClick": false,
        "fields": {
          "Location": "BLR"
        },
        "gamificationEnabled": true,
        "lastLoginDate": "2025-06-27T11:21:17.000Z",
        "name": "John Doe",
        "pointsEarned": 1690,
        "pointsRedeemed": 0,
        "preferredResolution": "AUTO",
        "profile": "admin",
        "roles": [
          "Learner",
          "Admin",
          "Author",
          "Instructor",
          "Integration Admin",
          "Manager"
        ],
        "state": "ACTIVE",
        "userType": "Internal"
      },
      "relationships": {
        "account": {
          "data": {
            "id": "9238",
            "type": "account"
          }
        }
      }
    }
  ]
}
```

### Modifications de l’API pour les réseaux sociaux (recherche utilisateur)

**Point de terminaison**

```
GET /primeapi/v2/users/search?q={searchTerm}&context=tagging
```

**Description**

Recherchez les utilisateurs disponibles pour le balisage en fonction des paramètres de portée sociale.

**Paramètres de demande**


* q (obligatoire) : terme de recherche (au moins 3 caractères).
* context : Définissez « tagging » pour que les utilisateurs soient éligibles aux mentions.
* boardId (facultatif) : ID de la carte pour filtrer les utilisateurs en fonction des autorisations d’accès.

**Réponse**

```
{
  "data": [
    {
      "id": "11257229",
      "type": "user",
      "attributes": {
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "userType": "Internal",
        "state": "ACTIVE"
      }
    }
  ]
}
```

### Améliorations de l’API de l’élève pour le suivi des performances du quiz

L&#39;API `GET /loResourceGrades` a été améliorée pour fournir des données détaillées sur les performances du quiz, permettant des analyses plus sophistiquées et une prise de décision automatisée.

La réponse de l’API inclut désormais deux champs supplémentaires :

* **[!UICONTROL meilleur score]** : meilleur score obtenu par un élève lors de toutes les tentatives de quiz
* **[!UICONTROL score max]** : score total possible pour le quiz

**Exemple de réponse API**

```
{
    "links": {
        "self": "https://learningmanagerstage1.adobe.com/primeapi/v2/loResourceGrades/course:15067_30122_41715_1_3400468"
    },
    "data": {
        "id": "course:15067_30122_41715_1_3400468",
        "type": "learningObjectResourceGrade",
        "attributes": {
            "completed": false,
            "duration": 0,
            "hasPassed": false,
            "highestScore": 0,
            "maxScore": 0,. 
            "progressPercent": 0,
            "score": 0
        },
        "relationships": {
            "loResource": {
                "data": {
                    "id": "course:15067_30122_41715_1",
                    "type": "learningObjectResource"
                }
            }
        }
    }
}
```

En réponse, **course:15067_30122_41715_1_3400468** est l&#39;ID de la note de la ressource Objet d&#39;apprentissage pour laquelle les informations sont demandées. L&#39;ID `learningObjectResourceGrad`e peut être obtenu à partir de l&#39;API `GET /enrollments/{id}`.

### Les réponses API prennent en charge la sensibilité à la casse pour les noms d’auteurs

La réponse de l’API donne désormais la casse exacte des noms d’auteurs hérités tels qu’ils ont été saisis lors de la création ou de la mise à jour du cours. Cela garantit que les noms apparaissent de manière cohérente dans l’interface utilisateur des élèves et les API publiques.

* Lorsqu’un nouveau nom d’auteur est ajouté, la casse est stockée et renvoyée exactement telle qu’elle a été saisie.
* Si un nom d’auteur existant est supprimé et ajouté à nouveau avec une casse différente, la casse mise à jour sera respectée et reflétée dans tous les cours à l’aide de ce nom d’auteur.
* Aucune migration automatique ne sera effectuée pour les noms précédemment stockés ; seuls les noms nouvellement ajoutés ou mis à jour suivront ce comportement.

### Amélioration de l’API Calendrier

Le calendrier charge désormais les sessions pour le mois sélectionné par l’utilisateur. Pour récupérer les sessions passées et à venir via l&#39;API, un nouveau paramètre `year` a été ajouté au point de terminaison de l&#39;élève `GET /users/{id}/calendar`. Les paramètres `month` et `year` doivent être fournis ensemble pour récupérer les détails de la session.

**Exemple de boucle**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth a4ae04eb9f06f4bf88abcde17' 'https://abc.adobe.com/primeapi/v2/users/12345678/calendar?month=7&year=2025&currentMonthOnly=false&filter.allSessions=false'
```

### Prise en charge de l’achèvement du marquage via l’API de l’administrateur

Auparavant, l’API publique ne prenait pas en charge le marquage d’achèvement basé sur l’instance dans les scénarios d’inscription multiple. Grâce à cette amélioration, vous pouvez désormais inclure l&#39;ID d&#39;instance de cours dans le corps de la demande de `POST /users/{userId}/userModuleGrade` et l&#39;administrateur peut marquer l&#39;achèvement d&#39;une instance spécifique.

### Définition de la préférence d’ID utilisateur pour les rapports SCORM

Certains clients ont besoin de l’UUID (Universally Unique Identifier) de l’élève au lieu de l’id_utilisateur par défaut pour l’achèvement du contenu SCORM. L’utilisation de l’UUID fournit un suivi plus précis entre les programmes d’apprentissage et empêche la duplication de l’utilisation des licences dans les comptes MAU (Monthly Active User).

Pour prendre en charge ce paramètre, un nouveau paramètre au niveau du compte, `reporting_userid_preference`, a été ajouté. Lorsqu’il est activé, ce paramètre envoie l’UUID à la place de l’ID_utilisateur chaque fois que les élèves terminent le contenu SCORM.

>[!NOTE]
>
> Contactez notre équipe du service clientèle à l&#39;adresse [learningmanagersupport@adobe.com](mailto:learningmanagersupport@adobe.com) pour configurer ce paramètre.

Le nouvel attribut `reportingUserIdPreference` a été introduit pour le suivi `get /account` des préférences d&#39;ID utilisateur.

### Informations sur l’auteur dans les cours partagés

Dans l’API d’objets d’apprentissage, la façon dont les informations sur l’auteur sont renvoyées a été mise à jour pour distinguer les cours sur le compte principal des cours partagés avec des comptes de pairs :

* Cours partagés (compte de pairs) : les détails de l&#39;auteur sont maintenant renvoyés sous un nouvel attribut, `authorDetails`. Cet attribut fournit le nom de l&#39;auteur même lorsque le cours provient d&#39;un autre compte.

* Cours sur le compte principal : les informations sur l&#39;auteur continuent d&#39;être renvoyées sous l&#39;attribut `authors` existant, sans modification du comportement actuel.

Cette modification garantit la cohérence dans la façon dont les données de l’auteur sont exposées via l’API pour les cours principaux et partagés, tout en préservant la compatibilité pour les intégrations existantes.

## Modifications apportées aux webhooks

### Enregistrement de webhooks LinkedIn Learning à l’aide du connecteur

Auparavant, les administrateurs devaient enregistrer manuellement les webhooks d’apprentissage LinkedIn auprès de Adobe Learning Manager via les API. Grâce à cette amélioration, le connecteur LinkedIn Learning (LIL) prend désormais en charge l’enregistrement automatique des webhooks lors de la nouvelle configuration de connexion dans ALM. L&#39;**URL du serveur OAuth** et l&#39;**URL du serveur client** seront renseignées automatiquement sur la page de configuration de LinkedIn Learning.

Consultez [LinkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md#linkedin-learning-connector) pour plus d’informations sur l’intégration de LinkedIn Learning.

### Modifications apportées à l’utilisation de la licence MAU dans LinkedIn Learning

Auparavant, pour les comptes MAU (Utilisateurs actifs mensuels), lorsqu’un élève terminait un cours LinkedIn Learning directement sur la plateforme d’apprentissage LinkedIn, Adobe Learning Manager ne comptait pas le nombre de licences utilisées. La consommation de licences a été déclenchée uniquement pour les cours suivis via le lecteur Adobe Learning Manager, ce qui a entraîné un suivi inexact des utilisateurs actifs mensuels (MAU).

Grâce à cette amélioration, Adobe Learning Manager génère désormais un webhook externe chaque fois qu’un élève consulte un cours sur la plateforme d’apprentissage LinkedIn. Lorsque Adobe Learning Manager reçoit ce webhook, il calcule le nombre de licences utilisées pour assurer un suivi précis sur les deux plateformes.

## Modifications des rapports

### Terminaisons marquées par l’instructeur dans les relevés de notes des élèves

Les relevés de notes incrémentiels des élèves capturent désormais les terminaisons marquées par un instructeur, même si la participation est enregistrée après la date de la session.
Cette amélioration corrige une lacune critique dans les relevés de notes incrémentiels des élèves, où les terminaisons marquées par un instructeur étaient précédemment manquées si la participation était enregistrée après la date de la session d&#39;origine.

Les relevés de notes incrémentiels des élèves sont des rapports planifiés qui capturent uniquement les modifications (telles que les finalisations ou les mises à jour de la progression) qui se produisent au cours d’une période spécifiée, plutôt que de fournir un vidage complet des données historiques. Ils sont couramment utilisés pour l’automatisation, les tableaux de bord et les intégrations, ce qui permet aux utilisateurs de suivre efficacement les activités d’apprentissage récentes sans traiter l’ensemble de l’historique des relevés de notes à chaque fois.

* **Colonne Marquer la date de fin (fuseau horaire UTC)** : nouvelle colonne d’horodatage qui capture la date et l’heure exactes auxquelles un instructeur marque une session ou un module comme terminé.
* **Suivi amélioré de la source d’achèvement** : effectue le suivi de l’instructeur et du module spécifiques (par exemple, « Salle de classe ») où les achèvements ont été enregistrés.

Ces modifications garantissent que les terminaisons marquées après la date de la session sont correctement reflétées dans les relevés de notes incrémentiels des élèves.

**Cas d’utilisation**

* Organisations disposant de sessions en salle de classe où les instructeurs peuvent marquer les jours de présence après la session réelle.
* Systèmes automatisés ou tableaux de bord reposant sur des relevés de notes incrémentiels des élèves pour la conformité ou la création de rapports.

![Les rapports de relevé de notes de l’élève affichent des dates marquées comme terminées (surlignées en jaune) pour le suivi de l’achèvement du cours dans l’apprentissage par l’Adobe](/help/migrated/assets/mark-completion-column.png)
_Le rapport Relevé de notes de l’élève affiche une nouvelle colonne en jaune mettant en évidence les dates d’achèvement individuelles pour chaque utilisateur_

Afficher le [relevé de notes de l’élève](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md) pour plus d’informations sur le rapport Relevé de notes de l’élève.

### Rapport utilisateur amélioré avec champs de données étendus

Le rapport d’utilisateur inclut désormais des champs supplémentaires pour améliorer le suivi des utilisateurs et le mappage organisationnel. Ces mises à jour simplifient l’identification des utilisateurs, prennent en charge l’intégration avec les workflows de gestion des utilisateurs en aval, améliorent la compréhension des relations hiérarchiques et maintiennent les limites organisationnelles pour éviter les communications croisées accidentelles.

* Colonne ID utilisateur interne : fournit des identifiants internes uniques pour un suivi fluide des utilisateurs entre différents systèmes et points d’entrée API.
* Colonne E-mail du responsable : inclut les coordonnées du responsable direct pour le suivi de la hiérarchie de l’organisation.

![Rapport d’utilisateur montrant les colonnes d’ID utilisateur interne et d’e-mail du responsable surlignées en jaune](/help/migrated/assets/user-report-columns.png)
_Rapports utilisateur mettant en évidence les ID utilisateur internes et les adresses e-mail des responsables pour rationaliser la gestion des utilisateurs_

Consultez [Télécharger le rapport d&#39;utilisateur](/help/migrated/administrators/feature-summary/add-users-user-groups.md#download-the-user-report) pour plus d&#39;informations sur le rapport d&#39;utilisateur.

### Rapport utilisateur dans FTP, FTP personnalisé et Box

**Présentation**

Le rapport utilisateur est désormais disponible pour les connecteurs Box, FTP et FTP personnalisé, en plus des API de tâche existantes. Ces rapports fournissent des informations détaillées sur l’ID utilisateur interne, l’adresse e-mail de l’utilisateur, le nom, l’adresse e-mail du responsable, le type d’utilisateur, etc.

Les rapports peuvent être générés à la demande ou de manière planifiée, les données étant stockées dans le connecteur correspondant pour faciliter l’accès et l’analyse. Cette amélioration améliore la surveillance et l&#39;audit des activités des utilisateurs, ce qui permet un meilleur suivi de la sécurité et de la conformité.

Ces rapports sont disponibles parallèlement aux rapports existants, tels que l’enregistrement des utilisateurs, l’accès par connexion, la ludification et la formation, ce qui permet aux administrateurs d’accéder à tous les rapports essentiels à partir d’un emplacement unique pour rationaliser la gestion et l’analyse des données.

Consultez [Connecteur](/help/migrated/integration-admin/feature-summary/connectors.md) pour plus d&#39;informations sur le FTP, le FTP personnalisé et le connecteur Box.

### Inclure les utilisateurs suspendus dans les relevés de notes des élèves

**Présentation**

Les organisations peuvent désormais inclure des utilisateurs suspendus (ceux dont les profils externes sont désactivés) dans les relevés de notes des élèves, garantissant ainsi la conservation complète de l’historique des données d’apprentissage.

* Indicateur au niveau du compte pour configurer la visibilité des utilisateurs suspendus, ce qui permet aux utilisateurs suspendus d’apparaître dans les relevés de notes des élèves.
* Conservation des données historiques même après la désactivation des profils externes suspendus.

**Exigences de mise en œuvre**

* Contactez votre gestionnaire de succès client (CSM) pour activer l’indicateur au niveau du compte.

>[!NOTE]
>
>Cet indicateur est désactivé par défaut pour les comptes existants et doit être explicitement demandé pour les nouveaux comptes.

Consultez l&#39;article [Relevé de notes de l&#39;élève](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md) pour plus d&#39;informations.

### Rapport Assistances à la tâche avec liens d’accès direct

**Présentation**

Le rapport Assistances à la tâche a été amélioré pour inclure des liens de téléchargement directs vers les assistances à la tâche, rationalisant la gestion du contenu et les processus d’audit pour les administrateurs et les auteurs. Cette amélioration permet de télécharger directement les fichiers et d’accéder aux URL à partir du rapport. Élimine les tâches manuelles de localisation et de téléchargement des assistances à la tâche pour les audits de conformité ou d’accessibilité.

* Colonne Lien d’assistance à la tâche : accès direct aux fichiers d’assistance à la tâche et aux URL externes à partir du rapport.
* Contrôle d’accès basé sur les rôles : l’accessibilité des liens dépend des rôles utilisateur et des autorisations du catalogue.
* Les assistances à la tâche supprimées restent accessibles si elles sont toujours liées à des cours actifs.

**Cas d’utilisation**

* Les auteurs ou les administrateurs effectuent régulièrement des audits d’accessibilité sur les assistances à la tâche, selon les besoins des grandes organisations.
* Tout scénario dans lequel un accès rapide et basé sur les rôles aux fichiers d’assistance à la tâche est nécessaire pour la révision ou la conformité.

![](/help/migrated/assets/job-aid-report.png)
_Le rapport Assistances à la tâche affiche des liens de téléchargement directs, ce qui facilite l&#39;accès et le téléchargement des assistances à la tâche dans Adobe Learning Manager_

Consultez [Rapport d&#39;assistances à la tâche](/help/migrated/administrators/feature-summary/reports.md#job-aids-report) pour plus d&#39;informations sur le rapport d&#39;assistances à la tâche.

## Bogues corrigés dans cette mise à jour

* Les scores du quiz L2 sont désormais correctement générés pour les quiz non interactifs, y compris les détails des utilisateurs qui les ont remplis.
* La signature est désormais correctement envoyée à l’hôte cible lorsque le mécanisme d’authentification est défini sur Signature lors de la configuration de la connexion.
* Les utilisateurs fictifs créés pendant les sessions Adobe Connect n’ont pas été supprimés à la fin de la session. Le pipeline SnapLogic supprime désormais correctement ces utilisateurs, même lorsque l&#39;API `principals-delete` avait précédemment retourné une réponse de 200 sans les supprimer.
* Les objets `null` `eventDetail` dans les réponses API ne provoquent plus d&#39;exceptions. Le système ignore désormais les entrées nulles et traite l&#39;ensemble de la baie, garantissant ainsi des enregistrements complets.
* La colonne Date du retour d&#39;informations des rapports de retour d&#39;informations affiche désormais la date correcte. Auparavant, les secondes étaient incorrectement transmises au constructeur Date, qui attend des millisecondes, ce qui entraînait l&#39;affichage des dates en janvier 1970. Cette erreur a été corrigée pour garantir un affichage précis des dates lors de la génération des rapports de retour d’informations.
* Les élèves peuvent désormais mettre à jour l’inscription à un parcours d’apprentissage Flex même si l’une des instances de cours est retirée. Auparavant, la sélection d&#39;une nouvelle instance provoquait une erreur de console (Impossible de lire les propriétés de non défini) et empêchait la mise à jour.
* Les noms de ressources dans les parcours d’apprentissage s’affichent désormais correctement sans sauter les mots intermédiaires.
* Les webhooks linkedIn Learning sont désormais activés à partir du connecteur LIL lors de la création de connexions pour les nouveaux utilisateurs. Le système enregistre également le compte via l’API privée et affiche des informations de configuration supplémentaires (URL OAuth et URL du client) sur la page de configuration de LinkedIn Learning.
* Les valeurs d&#39;attribut utilisateur mises à jour via les workflows SAML (`UpdateUserWorkerTask`) sont désormais enregistrées avec leur casse d&#39;origine au lieu d&#39;être converties en minuscules.
* La réorganisation des modules dans un cours ne réinitialise plus le nombre de modules obligatoires sur « Tous » ; le nombre reste désormais tel que configuré.
* Les pipelines Go1 gèrent désormais les codes linguistiques de manière cohérente en mappant des codes à deux lettres à des codes à quatre lettres, à l’instar des pipelines LinkedIn Learning.
* Dans les comptes Retire+, les élèves voyaient auparavant « Ce cours n’existe pas » lors du lancement d’un cours du parcours d’apprentissage après leur désinscription d’une certification. Les sources d’inscription sont désormais correctement mises à jour, ce qui permet aux cours des Parcours d’apprentissage de se lancer sans erreurs.
* Lorsque le fichier module_version.csv contient des champs contentType avec des valeurs vides ou nulles, la création de cours fonctionne désormais sans problème.
* Les cours s&#39;affichent désormais correctement lors du filtrage par catalogue ou étiquette de catalogue. Auparavant, l&#39;application de ces filtres sur la page du cours n&#39;affichait pas les cours, même s&#39;ils étaient associés au catalogue.
* Dans l&#39;application de l&#39;élève, appuyer sur TAB dans le lecteur Fluidic était bloqué sur le bouton « Entrer en plein écran ». La navigation au clavier se déplace désormais correctement dans tous les éléments d’écran.
* Placer le curseur de la souris sur les noms de cours longs dans le tableau de bord de conformité de l&#39;application du responsable affiche désormais le nom complet des cours inscrits ou conformes.
* Seuls les paramètres Partagé ou CACHÉ sont acceptés pour la colonne de visibilité du module dans module.csv. Toute autre valeur déclenche une erreur lors de la migration, empêchant les défaillances sur le serveur principal.
* La création d’un nouvel administrateur avec un e-mail à casse mixte ne génère plus d’entrées utilisateur en double lorsque l’UUID est désactivé. Le système gère désormais systématiquement la casse des e-mails pour éviter les doublons.
* Notes Les PDF s&#39;affichent désormais correctement pour les cours de langues telles que l&#39;arabe, le grec, l&#39;hébreu, l&#39;hindi, le thaï et l&#39;ukrainien. Auparavant, les caractères semblaient déformés dans le PDF téléchargé, même s’ils s’affichaient correctement dans le lecteur.

## Configuration système

Voir [Configuration requise pour Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notes de mise à jour

Consultez les [notes de mise à jour](/help/migrated/release-note/release-notes.md) pour connaître les dernières mises à jour.

## Versions précédentes d’Adobe Learning Manager

* [Version de mai 2025 de Adobe Learning Manager](/help/migrated/whats-new-may-2025.md)
* [Version de novembre 2025 de Adobe Learning Manager](/help/migrated/whats-new-nov-24.md)


