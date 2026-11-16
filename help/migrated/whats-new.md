---
description: Découvrez les nouvelles fonctionnalités de la version de décembre 2026 de Adobe Learning Manager, notamment les graphiques Reports Builder et Virtual Coach.
jcr-language: en_us
title: Nouveautés de la version de décembre 2026 de Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c54a70f69868320e43d99a1fb2e4def5009f1d5c
workflow-type: tm+mt
source-wordcount: '4685'
ht-degree: 0%
---

# Nouveautés de la version de décembre 2026 de Adobe Learning Manager

La prochaine version de Adobe Learning Manager introduit de nouvelles fonctionnalités et améliorations visant à rationaliser la plate-forme et à étendre ses capacités. Ces mises à jour simplifient les workflows quotidiens, améliorent l’organisation et la diffusion du contenu de formation, et rendent l’expérience globale plus cohérente et intuitive.

## Graphiques et tableaux de bord Report Builder

Adobe Learning Manager prend désormais en charge les graphiques et les tableaux de bord dans Report Builder, ce qui permet aux administrateurs de visualiser les données des rapports directement dans la plateforme. Les administrateurs peuvent créer des graphiques à partir des colonnes du rapport, avec agrégation et filtrage disponibles dans chaque graphique.

Report Builder prend en charge les types de graphiques suivants :

* Grand nombre
* Graphique linéaire
* Graphique en barres
* Graphique circulaire
* Tableau croisé dynamique

Un tableau de bord de rapports contient des graphiques créés à partir d&#39;un rapport. Un tableau de bord personnalisé combine les graphiques de plusieurs rapports, tels que les données d’inscription et d’utilisateur, et prend en charge jusqu’à 20 widgets. Les graphiques appartenant à un rapport sont partagés lorsque vous partagez le rapport. Cela aide les administrateurs à conserver les données de rapport actuelles dans une vue unique au lieu de réexécuter les rapports. Les graphiques affichent jusqu&#39;à 10 000 points de données et les tableaux croisés dynamiques jusqu&#39;à 100 lignes et 100 colonnes. Si un graphique dépasse une limite, appliquez des filtres pour affiner les résultats. Les tableaux de bord ne peuvent pas encore être exportés.

## Rapports Insights Agent dans Report Builder

Les administrateurs peuvent désormais continuer à travailler avec les réponses Insights Agent dans Report Builder. Lorsque Insights Agent répond à une question, Report Builder mappe la même requête à ses propres champs lors d’une étape parallèle. Les administrateurs peuvent ouvrir, réviser, modifier et enregistrer le rapport. À partir de là, vous pouvez utiliser les mêmes fonctionnalités de Report Builder que tout autre rapport, tel que les abonnements.

Si une partie d’une question ne peut pas être exprimée avec des champs de Report Builder, le rapport répertorie cette partie comme une lacune. Si la partie manquante est au cœur de la question, le rapport n&#39;est pas offert. Comme les requêtes complexes peuvent produire des résultats réduits, passez en revue chaque rapport avant de vous y fier.

## Intégration d’Adobe Experience Manager Assets

Adobe Learning Manager s’intègre désormais à Adobe Experience Manager Assets, ce qui permet aux auteurs d’accéder au contenu de formation approuvé et aux ressources d’image et de les utiliser directement à partir d’un référentiel centralisé. Cela supprime l’étape de téléchargement et de téléchargement manuel entre l’équipe qui gère les actifs dans le Gestionnaire d’actifs numériques (DAM) et l’équipe qui crée les cours dans Adobe Learning Manager.

Ce qui change :

* **Accéder aux ressources approuvées :** les auteurs parcourent et sélectionnent les ressources de Experience Manager Assets sans quitter Adobe Learning Manager. Les cours utilisent donc des fichiers approuvés à jour plutôt que des copies locales qui peuvent devenir obsolètes.
* **Maintenir les ressources du cours à jour :** lorsqu&#39;une ressource change dans le DAM, la mise à jour peut être répercutée automatiquement dans les cours qui l&#39;utilisent, ce qui permet de conserver la cohérence du contenu à mesure que les ressources sont révisées.
* **L&#39;accès suit les autorisations existantes :** les auteurs ne voient que les ressources auxquelles ils ont déjà accès dans Experience Manager Assets, de sorte que la navigation dans Adobe Learning Manager respecte les mêmes autorisations que le DAM lui-même.

Le résultat est un chemin unique et régi d’un actif à l’élève, avec moins de travail manuel et moins d’incohérences de version.

## Améliorations de l’envoi de fichiers

Les modules de soumission de fichiers prennent désormais en charge les soumissions d’équipe et l’évaluation par rubrique. Un nouveau paramètre contrôle également si l’approbation de l’instructeur est requise pour les envois.

### Soumissions d’équipe

Les instructeurs peuvent désormais créer des équipes pour les envois de fichiers. Chaque équipe soumet un fichier pour l’ensemble de l’équipe. L&#39;instructeur évalue la soumission une fois et le résultat s&#39;applique à chaque membre. Les équipes se forment de deux manières : les instructeurs les créent manuellement ou un processus planifié les crée avant la date de début de l’instance, en fonction des membres par équipe ou du nombre d’équipes.

Les instructeurs gèrent les équipes sur une nouvelle page **Gestion des équipes** et examinent le travail sur une page de soumissions d&#39;équipe. Les instructeurs peuvent également annuler l’envoi d’une soumission approuvée pour déverrouiller l’équipe lorsque des modifications sont nécessaires, par exemple lorsqu’un membre de l’équipe quitte l’application. Une équipe peut accueillir jusqu’à 100 membres. Les élèves peuvent afficher leur équipe, ses membres et le résultat de l&#39;évaluation. Les modules d’équipe ne peuvent pas être ajoutés ou supprimés après la publication d’un cours.

### Évaluations basées sur des règles

Les auteurs peuvent désormais définir une rubrique, appelée plan d&#39;évaluation, pour les modules de soumission de fichiers. Une rubrique prend en charge les questions objectives avec les options notées et les questions subjectives avec l&#39;examen écrit.

Les auteurs peuvent également configurer les paramètres suivants :

* Indique si les élèves consultent les questions d’évaluation basées sur des rubriques avant de soumettre
* Indique si le score est un score global ou un score pour chaque critère

Chaque question peut être marquée comme requise et configurée pour permettre aux réviseurs de formuler des remarques. Une évaluation basée sur une rubrique peut contenir jusqu’à 100 questions, et les auteurs saisissent les questions séparément pour chaque locale. Après la publication d’un cours, seul le texte de la question peut changer.

### Approbation de l’instructeur ou achèvement automatique

Les auteurs peuvent désormais choisir si les envois de fichiers nécessitent l’approbation de l’instructeur ou sont effectués automatiquement. Ce paramètre est indépendant du plan d’évaluation.

## Serveur de protocole de contexte de modèle pour l&#39;assistant Élève

ALM permet aux élèves d’accéder à la formation dans les outils qu’ils utilisent déjà via un serveur MCP (Model Context Protocol). Les élèves peuvent accéder à Learning Manager de n’importe où, y compris via ChatGPT, Claude et des agents personnalisés. Configurez le serveur dans l’application d’administration de l’intégration pour permettre aux administrateurs d’accéder à six outils principaux pour les élèves. Il s’agit notamment de deux outils de l’assistant de l’élève : Agent de réponse et Parcours d’apprentissage personnalisé.

Le serveur fournit les fonctionnalités suivantes :

* Recherche
* Inscriptions à la liste
* Obtenir l’objet d’apprentissage
* Obtenir le profil utilisateur
* Répondre à la question sur le contenu d’apprentissage
* Obtenir un parcours d’apprentissage personnalisé

Les administrateurs peuvent modifier chaque description d’outil pour ajouter des exemples spécifiques à l’organisation. Les clients lisent les détails d&#39;autorisation à partir des métadonnées du serveur ; la configuration n&#39;a donc besoin que d&#39;un ID client et d&#39;un secret client.

## Modification personnalisée du parcours d’apprentissage et bandes de marque

Les élèves peuvent désormais supprimer les rubriques ou cours suggérés en une seule étape, en plus de l&#39;option existante permettant d&#39;affiner les listes de rubriques et de cours par le biais de la conversation.

Les administrateurs peuvent désormais repositionner la bande des parcours d’apprentissage personnalisés sur la page d’accueil de l’élève via la page Identité visuelle.

## Entraînez-vous avec des jeux de rôle dans Virtual Coach

Adobe Learning Manager propose désormais Virtual Coach, une solution de coaching et de jeu de rôle optimisée par l’IA qui permet aux élèves de s’entraîner à des conversations réalistes en milieu de travail avant de les affronter au travail. Les exemples incluent les objections de vente, les escalades de clients et les évaluations de performances.

Les auteurs créent des scénarios à partir de leurs propres matériaux de référence à l&#39;aide de modèles ou d&#39;un assistant d&#39;IA, et les élèves parlent avec un personnage d&#39;IA qui s&#39;adapte à leurs réponses en temps réel. Après chaque session, les élèves reçoivent un retour d&#39;informations instantané en termes de score et de coaching sur les connaissances et le style de communication, mesuré par rapport aux critères définis par l&#39;auteur.

Virtual Coach prend en charge neuf langues et peut être utilisé comme assistance à la tâche autonome ou intégré à un cours.

## Citations du parcours d’apprentissage dans l’assistant de l’élève

Les réponses de l’assistant de l’élève citent désormais le parcours d’apprentissage qui contient un cours source, ainsi que le cours lui-même. Les élèves ouvrent la présentation du cours ou la page du parcours d’apprentissage à partir de la citation. Les réponses tirées d’une assistance à la tâche incluent un lien de téléchargement. Cela aide les élèves à trouver la formation qui répond à leur question.

## Configurations de l’assistant AI

L’assistant administrateur propose deux agents : Insights Agent et Knowledge Agent. Ils peuvent être configurés individuellement. L’assistant de l’élève propose trois agents : Agent de connaissances, Agent de réponse et Agent du parcours d’apprentissage. Ils peuvent être configurés avec la configuration du catalogue.

## Webhooks pour les modifications des instructeurs sur les instances d’objets d’apprentissage

Le webhook de modification de l&#39;instance d&#39;objet d&#39;apprentissage se déclenche désormais lorsqu&#39;un instructeur modifie une session de classe virtuelle, en plus des modifications d&#39;administrateur et d&#39;auteur. Les modifications telles que les horaires de la session, le lieu et la limite d’inscription la déclenchent. Les clients sans en-tête peuvent ensuite récupérer les détails de la session via l’API publique et transmettre les mises à jour aux élèves.

## Cours multi-inscrits dans le widget de conformité

Le widget de conformité répertorie désormais chaque instance d’un cours à inscriptions multiples qu’un élève doit effectuer. Chaque entrée affiche le nom de l&#39;instance. Si une instance a une échéance, toute instance sans échéance est masquée. Le point de terminaison des inscriptions de l’API publique prend en charge le même comportement via un paramètre facultatif.

## Renvoyer les invitations à une session de classe virtuelle

Les administrateurs disposant d’une autorisation de modification de cours peuvent désormais renvoyer une invitation à une session à partir de la page d’instance. Sélectionnez **Renvoyer**, recherchez l’élève et envoyez. L’option est disponible pour les sessions de classe virtuelle actuelles et futures. Pour les élèves dans plusieurs instances, l’invitation n’est envoyée qu’à l’instance sélectionnée. Les élèves qui ne sont pas inscrits à la session sont ignorés avec un avertissement.

## Participation automatique à partir des vues d’enregistrement Adobe Connect

Adobe Learning Manager marque désormais la présence lorsqu’un élève lit l’enregistrement d’une session de classe virtuelle manquée. Une intégration planifiée extrait les données du lecteur d’Adobe Connect et compare le temps de lecture avec les critères d’achèvement définis pour le compte. Les administrateurs définissent la planification dans l’application d’administration de l’intégration. Adobe Learning Manager ne prend en compte que la durée réelle de visionnage lors de la détermination de l’assiduité. Par conséquent, ignorer un enregistrement n’est pas pris en compte dans les critères d’achèvement.

## Email Builder pour les cours et les instances

Email Builder dans Adobe Learning Manager permet aux administrateurs et aux auteurs de créer des modèles de communication des élèves de marque. Dans la version de décembre 2026 de Learning Manager, l’expérience complète du créateur d’e-mails est disponible pour les e-mails au niveau du cours et de l’instance. Les auteurs peuvent personnaliser ces e-mails tout en héritant des mises en page et du formatage définis par les administrateurs.

Avec Email Builder, vous pouvez :

* Création de mises en page d’e-mails réutilisables
* Appliquer le branding de l’organisation
* Personnalisation des bannières et des signatures
* Définition des polices et des couleurs par défaut
* Normaliser la communication entre les cours et les programmes d’apprentissage

Les administrateurs créent des modèles et des mises en page de courrier électronique à l’échelle du compte. Les auteurs personnalisent les e-mails aux niveaux du cours et de l’instance sans reconstruire les modèles à partir de zéro.

Les paramètres de bannière et de signature ont été déplacés. Auparavant, ces paramètres apparaissaient dans un onglet **Paramètres** distinct. Cet onglet est supprimé et la **bannière** et la **signature** apparaissent désormais dans la **disposition globale**.

### Hiérarchie d’Email Builder

Email Builder utilise une hiérarchie. Chaque niveau hérite de son niveau parent et permet la personnalisation locale.

| **Niveau** | **Ce qu&#39;il fournit** | **Qui le personnalise** |
|-------------------|---------------------------------------------------------------------------------------------------------------------|-----------------------|
| Mise en page du compte | Identité visuelle, polices, couleurs et structure d’en-tête et de pied de page | Administrateurs |
| Modèle de compte | Stylisation globale des e-mails, composants de messagerie courants et image de marque partagée | Administrateurs |
| Modèle de cours | E-mails spécifiques au cours, tels que les messages d’inscription, les rappels de cours, les e-mails de fin et les notifications de session | Auteurs |
| Modèle d’instance | Niveau de personnalisation le plus élevé, tel que les messages spécifiques à une cohorte, à une session ou à une région | Auteurs |

Tous les cours peuvent hériter des modèles de compte. Les e-mails de cours héritent de la mise en page de l’organisation et permettent la personnalisation du contenu.

### Héritage de la mise en page

Un modèle est lié à la mise en page disponible la plus proche. Un modèle au niveau de l’instance est lié à une mise en page au niveau de l’instance, le cas échéant. S’il n’en existe aucun, le modèle est lié à la maquette parent la plus proche. Vous pouvez voir de quel niveau provient une mise en page.

Lorsqu’un modèle est lié à une mise en page :

* Le branding est automatiquement intégré au modèle.
* Les auteurs mettent uniquement à jour le contenu.
* La mise en page réduit la duplication entre les messages.

Vous pouvez dissocier un modèle de sa mise en page. Après avoir dissocié un modèle :

* Le modèle conserve sa conception existante.
* Les futures mises à jour de la mise en page n’affectent pas le modèle.
* Le modèle devient modifiable indépendamment.

L’héritage de la disposition dépend des dispositions parentes disponibles. Lorsque les deux niveaux existent, les e-mails au niveau de l’instance remplacent les modèles au niveau du cours.

### Workflow d’administrateur et d’auteur

Les administrateurs utilisent des modèles au niveau du compte pour assurer la cohérence des messages dans l’ensemble du compte, qu’ils gèrent en créant une mise en page et un modèle, puis en publiant le branding.

Les auteurs utilisent des modèles au niveau de l’instance lorsque les cohortes ont besoin de messages différents, qu’ils gèrent via des instances de cours.

### Disponibilité d’Email Builder pour les e-mails de cours et d’instance

Si Email Builder est déjà activé pour votre compte, vous recevez automatiquement les nouvelles modifications et n’avez rien à faire. La fonctionnalité de messagerie existante continue de fonctionner indépendamment des activités de migration d’Email Builder.

## Attributs d’élève personnalisés dans l’interopérabilité des outils d’apprentissage

Adobe Learning Manager lit désormais les attributs personnalisés de l’élève via le point de terminaison facultatif Noms et services de provisionnement des rôles de l’interopérabilité des outils d’apprentissage. Il les lit également à partir de la demande de lancement. Les attributs tels que le pays ou la ville sont stockés dans des champs de profil regroupables. Les paramètres de lancement nécessitent un préfixe permettant à Adobe Learning Manager de les reconnaître. Certains systèmes d’apprentissage, tels que Moodle, ne prennent pas en charge ce point de terminaison.

## Notifications de l&#39;instructeur du forum de discussion

Les clients sans en-tête peuvent désormais envoyer aux instructeurs et aux responsables de cohorte un résumé de l’activité du forum de discussion. À l’aide de l’API, vous ajoutez des abonnés à un forum. Ils reçoivent les nouvelles publications, les nouveaux commentaires et les nouvelles réponses dans un seul e-mail, à un intervalle que vous définissez. Les mentions J’aime et Je n’aime pas ne sont pas incluses. Vous activez la fonctionnalité par le biais de l’API.

## Classement par pertinence dans la recherche du catalogue de l’administrateur

La recherche de catalogue dans la vue Administrateur classe désormais les résultats par pertinence, en utilisant le même service de recherche que la recherche d’élève et d’administrateur ailleurs. Une correspondance exacte, telle qu’un nom de catalogue avec une date spécifique, apparaît en premier, suivie de correspondances partielles. La liste de suggestions lors de la saisie suit le même ordre.

## Synchronisation des annulations de session depuis Adobe Workfront

Les sessions annulées dans Adobe Workfront sont transférées vers Adobe Learning Manager via le processus de migration, sans procédure manuelle. La migration ajoute une colonne facultative **État** qui accepte **Actif** ou **Annulé**. Une valeur vide ne modifie pas la session. Une annulation effectuée via la migration se comporte comme une annulation effectuée dans l’interface Learning Manager. Les élèves, les instructeurs, les administrateurs, les auteurs et les responsables reçoivent les mêmes e-mails d’annulation.

Deux comportements s’appliquent aux sessions annulées :

* La migration n’applique pas les modifications détaillées à une session annulée et renvoie une erreur de validation pour ces lignes.
* Le fait de définir l’état sur Actif réactive la session, et vous pouvez ensuite mettre à jour ses détails ou l’annuler à nouveau.

Les mises à jour de session continuent de fonctionner comme avant.

## Limite de caractères pour les prénoms

Adobe Learning Manager accepte désormais les prénoms comportant jusqu’à 255 caractères, contre 63 auparavant. Cela s’applique aux utilisateurs ajoutés dans l’interface, via l’importation CSV et l’auto-inscription, afin que la synchronisation des utilisateurs à partir d’autres systèmes n’échoue plus sur les noms longs.

Cela est particulièrement utile lorsque vous migrez des utilisateurs à partir d’un système externe ou automatisez la création d’utilisateurs.

À partir de la version de décembre 2026, le champ Prénom accepte jusqu’à 255 caractères. Les versions antérieures acceptaient un maximum de 63 caractères.

>[!NOTE]
>
>La limite s’applique à tous les utilisateurs de votre compte, quel que soit leur rôle. Les utilisateurs existants et leurs noms ne sont pas affectés par cette modification.

Vous pouvez entrer des noms longs lorsque vous ajoutez ou modifiez des utilisateurs de l’une des manières suivantes :

* Ajout d’un utilisateur unique dans l’interface d’administration
* Modifier un utilisateur existant
* Importation d’utilisateurs à l’aide d’un fichier CSV
* Enregistrement automatique des utilisateurs
* Ajout d&#39;utilisateurs externes

Les noms longs peuvent être plus larges que l’espace disponible dans certaines parties de l’interface. Pour que la mise en page reste lisible, Adobe Learning Manager raccourcit les noms longs dans les zones compactes suivantes :

* Cellules de tableau
* Éléments de liste déroulante
* Résultats de la recherche

Pour afficher le nom complet, survolez le nom abrégé.

## Informations sur le badge pour les cours et les parcours d’apprentissage

Lorsque les auteurs ajoutent un cours ou un parcours d’apprentissage, une fenêtre répertorie les cours et parcours d’apprentissage existants avec des informations de badge. La fenêtre affiche le nom, le type (cours ou parcours d’apprentissage), l’état de la publication et le format du cours, tel que auto-apprentissage, virtuel, salle de classe ou fusionné.

## Améliorations hors connexion

Learning Manager permet désormais un accès contrôlé au contenu d’apprentissage sans que les utilisateurs aient à se connecter. Les administrateurs peuvent spécifier quels catalogues sont publics, tandis que les auteurs peuvent déterminer quels cours et modules sont disponibles sans compte. Le contenu public est publié sous forme de pages consultables par l&#39;IA, ce qui rend l&#39;académie détectable par les moteurs de recherche et les assistants d&#39;IA tels que Claude et ChatGPT. L’utilisation anonyme est suivie par visiteur et signalée séparément de l’utilisation lors de la connexion.

### Consommation de contenu sans connexion

Les visiteurs de votre académie publique peuvent désormais lire du contenu sélectionné directement à partir de la page de présentation du cours, sans avoir besoin d’un compte, d’un e-mail ou d’un formulaire.

* **Activer ou désactiver l&#39;accès hors connexion :** les administrateurs peuvent activer ou désactiver la consommation de contenu hors connexion pour l&#39;ensemble du compte.
* **Rendre des cours ou des modules disponibles sans se connecter :** les auteurs peuvent rendre un cours entier disponible sans se connecter ou ouvrir uniquement des modules spécifiques, tels qu&#39;un module d&#39;introduction gratuit avant le contenu avancé contrôlé.
* **Hériter des paramètres des cours :** les parcours d’apprentissage et les certifications suivent les paramètres des cours qu’ils contiennent, sans configuration supplémentaire.
* **Afficher le contenu sans connexion :** les élèves non authentifiés peuvent afficher le contenu disponible sans connexion à leur compte.
* **Contenu d&#39;auto-apprentissage uniquement :** le contenu sous licence tiers et le contenu de catalogue acquis ne peuvent pas être rendus disponibles sans connexion.
* **Rapports sur la consommation anonyme :** un rapport sur la consommation mensuelle hors connexion peut être généré.
* **Activer l’apprentissage hors connexion sur toutes les plateformes :** la consommation de contenu hors connexion est prise en charge sur Adobe Learning Manager natif sur le web et les appareils mobiles, sur les déploiements sans interface utilisateur et dans les académies basées sur des widgets Adobe Experience Manager Sites.

### Choix des catalogues publics

Les administrateurs peuvent désormais sélectionner les catalogues spécifiques qui apparaissent dans l’académie publique. Seuls ces catalogues peuvent être consultés par des visiteurs anonymes et indexés par les moteurs de recherche et les assistants d&#39;IA, de sorte que les cours de test ou le contenu interne restent privés.
 

### Trouvez-vous dans les moteurs de recherche et les assistants IA (Beta)

Adobe Learning Manager peut désormais rendre votre académie publique détectable par les moteurs de recherche tels que Google et par les assistants d’IA tels que ChatGPT, Claude et Gemini. Vos cours peuvent ensuite apparaître dans les résultats de recherche et les réponses générées par l&#39;IA, attribués à votre académie.

* Les contrôles au niveau du compte permettent aux administrateurs de décider si les analyseurs de liens peuvent accéder à l&#39;académie publique et si son contenu peut être indexé.
* Chaque académie a son propre plan de site et robots.txt, généré automatiquement à partir des catalogues que vous avez rendus publics.
* Les pages sont prérendues pour les analyseurs de liens, de sorte que les assistants IA qui n’exécutent pas JavaScript peuvent toujours les lire.
* Les analyseurs de liens ne voient jamais que ce à quoi un visiteur peut accéder. Le contenu conditionnel n’est jamais exposé.
* Méta-titre, description et données structurées : Adobe Learning Manager les génère automatiquement pour chaque cours, parcours d’apprentissage et certification, en fonction des métadonnées d’apprentissage.

>[!NOTE]
>
>L’IA et la découverte de recherche sur Adobe Learning Manager natif nécessitent un domaine personnalisé. Les déploiements sans interface utilisateur devront implémenter certaines parties de la configuration dans leur propre environnement.

## Retirer un cours sans rendre un parcours d’apprentissage inaccessible

Un cours retiré ou un parcours d’apprentissage imbriqué est supprimé de l’objet d’apprentissage de niveau supérieur, qui reste ouvert aux nouvelles inscriptions. Le retrait d’un cours ne rend plus le parcours d’apprentissage inaccessible.

## URL de page non connectée pour les profils d&#39;auto-inscription

Les profils d’auto-inscription permettent aux utilisateurs externes, tels que les partenaires ou les membres de plusieurs organisations, de créer leurs propres comptes Adobe Learning Manager. Chaque profil peut désormais avoir sa propre URL de menu non connectée partageable, intégrée à Experience Builder.

Lorsque les utilisateurs sélectionnent **S&#39;abonner** à partir d&#39;une page accessible via cette URL, ils sont ajoutés au profil auquel l&#39;URL appartient. Cela permet de conserver les utilisateurs de différentes organisations, telles que des agences distinctes ou des sociétés partenaires, dans des profils distincts.

## Stocker les dates de dernier accès pour les inscriptions au parcours d’apprentissage

Adobe Learning Manager vous permet désormais d’associer des métadonnées personnalisées, telles qu’une date de dernier accès, à une inscription à un parcours d’apprentissage. Vous le définissez et le lisez via l’API, ce qui vous permet de suivre l’accès limité dans le temps aux parcours d’apprentissage que vous attribuez.

Les inscriptions au cours prennent déjà en charge une date de dernier accès via l’API, qui contrôle la durée pendant laquelle un élève peut accéder au cours. Les inscriptions au parcours d’apprentissage proposent désormais un champ de métadonnées générique, ce qui vous permet de stocker une date de dernier accès ou toute autre valeur que vous souhaitez suivre.

## Exportation de rapports de Report Builder avec l’API de tâche

Cette version de Adobe Learning Manager ajoute un nouveau type de tâche API de tâche, `generateCustomReport`. Transmettez un ID de rapport pour exporter automatiquement tout rapport créé dans Report Builder.

Associé au nouveau jeu de données de quiz L2 dans Report Builder, vous pouvez désormais :

* Exportez les données de quiz au niveau des questions (L2) entre plusieurs cours et modules dans un seul rapport, plutôt que d&#39;exécuter `generateQuizReport` une fois par cours.
* Automatisez les exportations récurrentes, telles qu’une exportation incrémentielle quotidienne vers votre entrepôt de données ou votre outil de Business Intelligence.

Les types de travaux existants, y compris `generateQuizReport`, sont inchangés.

## Modifications de l’en-tête de colonne dans les rapports téléchargés

Report Builder inclut désormais le nom de l&#39;ensemble de données dans les en-têtes de colonne par défaut des rapports téléchargés. Le nom de l&#39;ensemble de données de l&#39;objet d&#39;apprentissage apparaît donc comme **Objet d&#39;apprentissage - Nom** au lieu de **Nom**. Pour les colonnes agrégées, l’en-tête inclut également la fonction, telle que « **Nombre d’objets d’apprentissage - ID** ». Si vous saisissez un nom personnalisé dans le champ **Alias** d&#39;une colonne, cet alias est utilisé comme en-tête et reste inchangé.

Après la mise à niveau, les rapports existants sans alias personnalisés affichent les en-têtes mis à jour, tandis que les données de rapport, les filtres et les planifications ne sont pas affectés. Si vos scripts, feuilles de calcul, tableaux de bord Business Intelligence ou intégrations font référence à des colonnes par en-tête, mettez-les à jour vers les nouveaux noms ou définissez un alias personnalisé pour conserver un en-tête spécifique.

## Hub en direct

Live Hub est désormais généralement disponible pour les clients Ultimate et reste en version Beta pour les clients Prime.

## Prise en charge multilingue des sous-titres dans Live Hub

Les sous-titres dans Live Hub ont été améliorés pour prendre en charge d’autres langues. Les instructeurs peuvent désormais sélectionner la langue des sous-titres dans les **paramètres de la salle** en fonction de la langue parlée pendant la session.

Les légendes sont générées automatiquement dans la langue sélectionnée et affichées dans un panneau dédié qui est mis à jour en permanence pendant que l’instructeur parle. Tous les participants affichent les légendes dans la langue sélectionnée par l’instructeur.

Cette amélioration améliore l’accessibilité pour les participants dans différentes langues et les aide à suivre les sessions en direct plus efficacement.

## Interface Live Hub localisée et lecteur d&#39;enregistrement

L’interface Live Hub apparaît désormais dans la langue sélectionnée pour l’interface utilisateur de Learning Manager. Les libellés et les en-têtes tout au long de la session, y compris la conversation, les participants, les sondages, les salles de réunion et les paramètres, apparaissent dans la langue choisie par l’utilisateur. Live Hub prend en charge les mêmes 18 langues d’interface que Learning Manager, y compris l’anglais. Le lecteur d’enregistrement est également localisé, de sorte que les éléments tels que les sondages apparaissent dans la langue du cours. Par exemple, l’enregistrement d’un cours d’allemand affiche l’interface du lecteur en allemand.

Les participants du monde entier bénéficient ainsi d’une expérience cohérente sur toute la plateforme et dans les enregistrements de session.

## Sessions Live Hub pouvant accueillir jusqu’à 5 000 participants

Live Hub prend désormais en charge des sessions à grande échelle comptant jusqu’à 5 000 participants, ce qui permet aux organisations de mener des sessions de formation de grande envergure. Les auteurs peuvent choisir une capacité de 5 000 participants lors de l’ajout d’un module de salle de classe virtuelle à un cours. Live Hub configure automatiquement la salle en fonction de la taille de l&#39;audience et applique des restrictions d&#39;interaction spécifiques.

Dans les sessions volumineuses, les capacités et comportements suivants s’appliquent :

* L’accès aux caméras, le partage d’écran et les fonctionnalités du tableau blanc sont réservés aux instructeurs.
* Les salles de petits groupes ne sont pas disponibles.
* De grands volumes de messages de chat, de réactions et de questions simultanés sont distribués par lots échelonnés.
* D’autres interactions et fonctionnalités, notamment les sondages, les quiz, l’enregistrement et le suivi de l’assiduité, fonctionnent comme dans les sessions ordinaires.

Cela permet aux organisations d’organiser de grandes sessions de formation au sein de la même plateforme, avec une salle qui peut être définie sur la taille de public attendue.

## Canaux

Les chaînes sont désormais généralement disponibles pour tous les clients.

## Réservation d’inscription de groupe et gestion des listes d’attente

La réservation d’inscription de groupe et la gestion des listes d’attente permettent aux auteurs de contrôler plus précisément qui peut s’inscrire aux cours en salle de classe et en salle de classe virtuelle. Les auteurs peuvent allouer des places à des groupes d&#39;utilisateurs spécifiques et définir des dates d&#39;ouverture d&#39;inscription distinctes pour ces groupes et pour tous les autres élèves. Ils peuvent également activer la promotion automatique de liste d&#39;attente avec une date limite, de sorte qu&#39;une place disponible passe au prochain élève éligible. La réservation de tous les sièges limite un cours aux groupes sélectionnés.

## Prise en charge de plusieurs connexions Zoom

Adobe Learning Manager prend désormais en charge plusieurs connexions Zoom au sein d’un même compte, ce qui permet aux organisations de gérer les sessions de classe virtuelle entre différents comptes Zoom.

Les administrateurs d’intégration peuvent configurer plusieurs connexions Zoom et les affecter à des rôles ou des groupes d’utilisateurs spécifiques. Lors de la création ou de la modification d&#39;une session de cours, les auteurs peuvent sélectionner une connexion Zoom disponible, chaque session utilisant une connexion.

Cette amélioration offre une plus grande flexibilité aux organisations qui utilisent plusieurs comptes Zoom, en particulier dans les cas suivants :

* **Formation spécifique au service** : gérez des comptes Zoom distincts pour différents services ou équipes au sein du même compte Learning Manager.
* **Formation des partenaires et externe** : attribuez des connexions Zoom dédiées à des partenaires ou des groupes d’utilisateurs spécifiques pour prendre en charge leurs sessions de formation.
* **Accès contrôlé** : restreignez la disponibilité des connexions Zoom en fonction des rôles ou des groupes d&#39;utilisateurs, en veillant à ce que les auteurs puissent sélectionner uniquement les connexions qui leur sont attribuées.
* **Gestion simplifiée des connexions** : permet aux administrateurs d&#39;intégration de gérer de manière centralisée plusieurs connexions Zoom sans affecter les sessions existantes.

## Intégration de Safe Exam Browser pour les quiz

Adobe Learning Manager s’intègre désormais à Safe Exam Browser pour les questionnaires natifs, offrant ainsi un environnement sécurisé et contrôlé pour la réalisation des évaluations. Les administrateurs peuvent activer l’intégration au niveau du compte et charger un fichier de configuration Explorateur d’examens sans échec (.seb) pour définir les restrictions d’évaluation. Les auteurs peuvent ensuite choisir les quiz individuels qui nécessitent l&#39;Explorateur d&#39;examens sécurisé.

Lorsque les élèves tentent un quiz qui nécessite un Explorateur d’examens sécurisé, ils sont invités à lancer le navigateur. Cela bloque l&#39;accès aux autres navigateurs et applications pendant la durée de l&#39;évaluation en fonction des restrictions définies par l&#39;administrateur. Les élèves qui ne l’ont pas installé sont invités à le télécharger.

**Là où cela peut être utile :**

* **Évaluations de certification :** effectuez des quiz lorsqu&#39;il est important de restreindre l&#39;accès aux ressources externes.
* **Formation à la conformité :** prise en charge des évaluations contrôlées pour la formation obligatoire et les exigences réglementaires.
* **Évaluations à enjeux élevés :** réduisez les possibilités d&#39;accès à des applications ou des ressources non autorisées pendant les évaluations importantes.
* **Gestion flexible de l&#39;évaluation :** autoriser les auteurs à exiger un navigateur d&#39;examen sécurisé uniquement pour les quiz nécessitant des restrictions supplémentaires.

## Correctifs d’accessibilité dans Live Hub

Les correctifs d’accessibilité dans Live Hub améliorent l’expérience des utilisateurs des technologies d’assistance et de la navigation par clavier.

* **Lecteurs d’écran** : les contrôles et le contenu sont désormais annoncés correctement avec NVDA, JAWS, VoiceOver et TalkBack.
* **Navigation au clavier** : chaque élément interactif est accessible dans un ordre de tabulation logique avec un indicateur de mise au point visible, le focus n’est plus piégé et un lien de navigation par contournement est disponible.
* **Sous-titres** : les sessions en direct affichent des sous-titres en temps réel, les enregistrements prennent en charge le chargement et l’activation/désactivation des sous-titres et le basculement des sous-titres peut être effectué à partir du clavier.
* **Contraste des couleurs** : les composants de texte et d&#39;interface utilisateur répondent désormais aux taux de contraste requis et un thème à contraste élevé est disponible.
* **Zoom et redistribution** : le contenu et les fonctionnalités sont préservés à un zoom de 200 % dans le navigateur, et Live Hub fonctionne avec des agrandisseurs d’écran.

## Modifications apportées aux API dans la version de décembre 2026 de Adobe Learning Manager

### Commande d’API de signet et gestion du contenu retiré

Les élèves peuvent ajouter des signets aux formations pour y revenir ultérieurement. Auparavant, les API de signet renvoyaient les formations enregistrées dans un ordre non spécifique, ce qui empêchait les intégrations sans en-tête d’afficher d’abord les formations enregistrées les plus récentes. Les signets des objets d&#39;apprentissage retirés restaient également dans la liste et entraînaient des erreurs « Page introuvable ».

Cette mise à jour corrige les deux problèmes suivants :

* Les signets sont désormais renvoyés en premier.
* Les signets vers les objets d&#39;apprentissage retirés ne sont plus renvoyés.

Aucun nouveau point de terminaison, paramètre ou attribut de réponse n’est ajouté. Les intégrations existantes continuent donc de fonctionner sans modifications.

### API pour les notifications des instructeurs des forums de discussion

Cette version inclut de nouvelles API qui prennent en charge les notifications des instructeurs des forums de discussion. Utilisez-les pour abonner des instructeurs et des gestionnaires de cohorte à des forums de discussion et pour contrôler quelle activité apparaît dans leurs courriels de résumé.

### Prise en charge d’API pour les instances multi-inscrites dans l’application de l’élève

L’API d’inscription prend désormais en charge les instances multi-inscrites dans l’application Élève. Ajoutez le paramètre facultatif `includeMultiInstanceEnrollments=true` à `GET /enrollments` pour les inclure. La valeur par défaut est `false`. Par conséquent, les intégrations existantes, y compris les implémentations sans en-tête, continuent de fonctionner sans modification.

### Date du dernier accès pour l’inscription au parcours d’apprentissage

Vous pouvez désormais stocker des métadonnées personnalisées, telles qu’une date de dernier accès, sur une inscription à un parcours d’apprentissage, puis les définir et les lire via l’API. Cela vous permet de suivre l’accès limité dans le temps aux parcours d’apprentissage que vous attribuez.

* Définissez les métadonnées sur une inscription existante ou lorsque vous inscrivez un élève à l’aide d’un jeton d’administration.
* Lisez-le avec un jeton d’administrateur ou d’élève.

Les métadonnées sont destinées à votre propre suivi. Il ne contrôle pas l’accès et n’est pas appliqué aux cours du chemin.

### Type de tâche d’API de tâche pour les exportations de Report Builder

L&#39;API de tâche a un nouveau type de tâche, `generateCustomReport`, qui exporte tout rapport de Report Builder enregistré lorsque vous transmettez son ID de rapport. Avec le nouveau jeu de données de quiz L2, vous pouvez exporter les données de quiz au niveau des questions entre plusieurs cours dans un seul rapport et automatiser les exportations récurrentes.

Les types de travaux existants, y compris `generateQuizReport`, sont inchangés.

### API pour le connecteur Zoom

Utilisez ces API pour afficher et gérer les connecteurs Zoom dans Adobe Learning Manager. Utilisez-les pour récupérer des connexions Zoom existantes, enregistrer des informations d’identification Zoom, créer ou mettre à jour des connexions et gérer les autorisations d’accès pour les groupes d’utilisateurs et les rôles personnalisés.

**Séquence d&#39;API**

Utilisez les API dans cette séquence :

| **Étape** | **API** | **Objectif** | **Authentification** |
|------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------|-----------------------------------------------------|
| 1 | `POST /ctr/authcred/uuid/20012    ` | Enregistrez les informations d’identification du zoom. | Session d’administration de l’intégration |
| 2 | `POST /ctr/app/esconnect  ` | Créez une connexion Zoom ou mettez à jour une connexion existante. | Session d’administration de l’intégration |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Définissez les groupes d&#39;utilisateurs et les rôles personnalisés qui peuvent utiliser la connexion. | Session d’administration de l’intégration |

**Authentification et autorisations**

Ces API utilisent l’authentification basée sur la session et nécessitent que l’utilisateur se connecte en tant qu’administrateur d’intégration dans Adobe Learning Manager.
