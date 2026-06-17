---
jcr-language: en_us
title: Jeux de données disponibles dans Report Builder
description: Guide de référence des jeux de données, des champs et des champs dérivés disponibles dans le Report Builder Adobe Learning Manager.
contentowner: mmanuel
source-git-commit: b21196a3121c88bf54f33aecc0f4649eceb3ddf6
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 28%

---


# Jeux de données disponibles dans Report Builder

Report Builder organise toutes les colonnes disponibles en jeux de données, groupes nommés de champs associés. Cet article répertorie chaque ensemble de données, décrit ce qu’il contient et indique quels ensembles de données peuvent être combinés dans un seul rapport.

**Ensembles de données dans cette version**

**Ensemble de données**

**Ce qu&#39;il contient**

**Champs clés**

**Utilisateur**

Données de profil d’élève pour les élèves actifs et supprimés

Nom, adresse e-mail, ID utilisateur, responsable, champs actifs, état

**Transcription**

Enregistrements d’inscription et d’achèvement

Date d’inscription, date d’achèvement, pourcentage de progression, état, score

**Objet d&#39;apprentissage**

Métadonnées de cours, de parcours d’apprentissage et de certification

Nom d’objet d’apprentissage, ID d’objet d’apprentissage, type, catalogue, étiquette de catalogue, état

**Instance d&#39;objet d&#39;apprentissage**

Détails au niveau de l’instance pour les cours avec plusieurs instances

Nom de l’instance, ID de l’instance, limite d’inscription, échéance

**Catalogue**

Paires clé-valeur des métadonnées de catalogue et du libellé de catalogue

Nom du catalogue, ID du catalogue, clé de libellé, valeur du libellé. **Les colonnes de libellé de catalogue sont configurées par le client**. Ils apparaissent uniquement si des étiquettes de catalogue sont configurées pour votre compte. Les noms et valeurs d&#39;étiquette qui s&#39;affichent reflètent votre propre configuration.

**Groupe d’utilisateurs**

Appartenance à un groupe d’utilisateurs et hiérarchie

Nom du groupe d’utilisateurs, ID du groupe d’utilisateurs, groupe parent, nombre de membres

**Session de module**

Détails de la session pour la classe, la classe virtuelle et les modules d’apprentissage en ligne

ID de session, nom de la session, nom de l’instructeur, heure de début, heure de fin, emplacement

Liste des colonnes dans les jeux de données

Catalogue

* Date de création
* ID
* Nom

Étiquette de catalogue

* Catalogue
* ID
* Nom
* Valeur

Champ personnalisé (objet d’apprentissage)

* % d’achèvement de l’objet d’apprentissage
* % de conformité de l’objet d’apprentissage

Champ personnalisé (utilisateur)

* % d’achèvement utilisateur
* % de conformité des utilisateurs

Objet d’apprentissage

* Noms des auteurs
* Date de suppression automatique
* Nombre d&#39;achèvements
* Date de création
* Durée (minutes)
* Nombre d’inscriptions
* Type d’inscription
* Format
* ID
* Changement d’instance activé
* Date du dernier accomplissement
* Date de la dernière publication
* Inscription multiple activée
* Nom
* Prérequis appliqués
* Prix
* Crédit de compétence
* Niveau de compétence
* Nom de la compétence
* Moyenne de l’évaluation par étoiles
* Nombre d’évaluations par étoiles
* Nombre de commencé
* Statut
* Balises
* Type
* ID unique

Instance de l’objet d’apprentissage

* Date d’échéance d’achèvement
* Date de création
* Date d’échéance d’inscription
* ID
* Date du dernier accomplissement
* ID de l’objet d’apprentissage
* Nom
* Statut
* Type
* Date d’échéance de désinscription

Module

* Heure de fin de l’accès
* Heure de début de l’accès
* ID du cours
* ID d’instance de cours
* Durée (minutes)
* Heure de fin
* Nombre d’inscriptions
* ID
* Noms des instructeurs
* Lieu
* Informations sur le lieu
* Région de l’emplacement
* URL du lieu
* ID de module
* Nom
* Limite de postes
* Heure de début
* Type
* Limite de liste d’attente

Transcript (objet d’apprentissage)

* Date d&#39;achèvement
* Date d’échéance d’achèvement
* Source d’achèvement
* Source d’achèvement - ID utilisateur
* Source d’achèvement - Nom d’utilisateur
* Date d&#39;inscription
* Source d’inscription
* État de l’inscription
* ID de l’objet d’apprentissage
* Nom de l’objet d’apprentissage
* ID d’instance de l’objet d’apprentissage
* En retard
* ID d’objet d’apprentissage parent
* Date de réussite
* Pourcentage de progression
* ID de la certification racine
* Date de début
* Statut
* Temps passé (minutes)
* Score utilisateur le plus élevé
* ID utilisateur
* Score utilisateur le plus récent

Transcript (module)

* Date d&#39;achèvement
* ID du cours
* ID de module
* Nom du module
* Date de réussite
* Pourcentage de progression
* Score total du module de quiz
* Date de début
* Statut
* Temps passé (minutes)
* Courrier électronique de l’utilisateur
* Score utilisateur le plus élevé
* ID utilisateur
* Score utilisateur le plus récent
* Nom d’utilisateur

Utilisateur

* ID Adobe
* Langue de contenu
* Date de création
* Date de suppression
* Nombre de membres dans l’équipe directe
* Courrier électronique
* ID
* Langue de l’interface
* Est administrateur
* Est Auteur
* Est un rôle personnalisé
* Est Instructeur
* Est Administrateur d’intégration
* Est Élève
* Est Responsable
* Est Utilisateur racine
* Date du dernier accès
* Adresse électronique du responsable
* ID du responsable
* Nom du responsable
* ID du responsable unique
* Nom
* Rôles
* Source
* Statut
* Nombre de membres dans l’équipe
* Fuseau horaire
* Type
* ID unique

Groupe d&#39;utilisateurs

* Date de création
* ID
* Nombre de membres
* Nom
* Statut

Groupe d’utilisateurs (champ actif)

* Date de création
* ID
* Nombre de membres
* Nom
* Statut

Groupe d’utilisateurs (personnalisé)

* Date de création
* ID
* Nombre de membres
* Nom
* Statut

Groupe d’utilisateurs (équipe directe)

* Date de création
* ID
* Nombre de membres
* Nom
* Adresse e-mail du propriétaire
* ID du propriétaire
* Nom du propriétaire
* ID du propriétaire unique
* Statut

Groupe d’utilisateurs (intégré)

* Date de création
* ID
* Nombre de membres
* Nom
* Statut

Groupe d’utilisateurs (équipe)

* Date de création
* ID
* Nombre de membres
* Description
* Nom
* Adresse e-mail du propriétaire
* ID du propriétaire
* Nom du propriétaire
* État du propriétaire
* ID du propriétaire unique
* Statut

**Association des jeux de données**

Toutes les paires de jeux de données ne peuvent pas être combinées dans un seul rapport. Les ensembles de données doivent partager une relation logique dans le modèle de données de Adobe Learning Manager pour pouvoir être joints. Lorsque vous ajoutez votre première colonne, Report Builder filtre les ensembles de données restants pour n’afficher que les ensembles compatibles. Si un ensemble de données apparaît grisé, il ne peut pas être directement joint aux colonnes déjà sélectionnées.

Cela signifie que le jeu de données ne peut pas être joint aux colonnes que vous avez déjà sélectionnées. Il s&#39;agit d&#39;une contrainte stricte dans le modèle de données. Les deux jeux de données ne partagent pas un chemin de jointure compatible.

Un exemple courant est le champ dérivé **Conformité %**. Lorsque le % de conformité est sélectionné, les ensembles de données **Transcription**, **Transcription du module** et **Instance LO** sont désactivés. Le % de conformité est calculé au niveau de l’utilisateur ou du groupe d’utilisateurs par rapport aux objets d’apprentissage et aux catalogues. Il est destiné à être utilisé avec les colonnes et filtres **Utilisateur**, **Groupe d’utilisateurs**, **Objet d’apprentissage** et **Catalogue** uniquement.

Pour utiliser un ensemble de données désactivé, désélectionnez les colonnes à l’origine du conflit, puis ajoutez l’ensemble de données dont vous avez besoin.

Les relations de jointure ci-dessous sont extraites du modèle de données du Report Builder. Leur compréhension vous aide à planifier les ensembles de données à combiner avant de créer un rapport.

**Ensembles de données de hub**

Deux ensembles de données font office de centres centraux. La plupart des autres ensembles de données se connectent par leur intermédiaire :

* **Inscription** (ensemble de données d&#39;inscription), la table de faits principale. Il se connecte directement à l&#39;**utilisateur** (l&#39;élève qui s&#39;est inscrit), à l&#39;**objet d&#39;apprentissage** (à quoi il s&#39;est inscrit) et, par l&#39;intermédiaire de l&#39;objet d&#39;apprentissage, à la **session de module**, au **catalogue**, au **libellé de catalogue** et à l&#39;**instance d&#39;objet d&#39;apprentissage**.
* **Transcription du module** (ensemble de données moduleTranscript) : table de faits de progression au niveau du module. Il se connecte à **Utilisateur** et à **Session de module**, qui à son tour renvoie à **Objet d&#39;apprentissage**.

La plupart des rapports qui combinent les données d’élève, de cours et d’achèvement sont créés via l’un de ces deux hubs.

**Joindre les chemins par cas d’utilisation**

**Pour combiner ces ensembles de données**

**Chemin de jointure**

**Utilisateur** + **Inscription**

Utilisateur du → d’inscription (via l’ID de l’élève)

**Inscription** + **Objet D’Apprentissage**

Inscription → objet d’apprentissage (via l’ID objet d’apprentissage)

**Objet D’Apprentissage** + **Catalogue**

Objet d’apprentissage → Catalogue → Catalogue LO

**Objet D’Apprentissage** + **Étiquette De Catalogue**

Étiquettes du catalogue d&#39;objets d&#39;apprentissage → d&#39;objets d&#39;apprentissage

**Objet d’apprentissage** + **Instance LO**

Objet d&#39;apprentissage → d&#39;instance LO

**Session De Module** + **Objet D’Apprentissage**

Module Session → Objet d’apprentissage (via un cours de session)

**Session de module** + **Utilisateur** (instructeur)

Session de module → Utilisateur (via un instructeur alias FK)

**Utilisateur** + **Groupe D’Utilisateurs**

Appartenance au groupe d’utilisateurs → Utilisateur + Groupe d’utilisateurs

**Objet d’apprentissage** + **Utilisateur** (auteur)

LO Author → User (via l&#39;alias d&#39;auteur FK)

**Utilisateur** + **Champs actifs**

Champ actif de l’utilisateur → Utilisateur (via ID utilisateur)

**Relations crénelées**

Certains champs du modèle de données se joignent à l&#39;entité **Utilisateur** via un rôle nommé plutôt qu&#39;un ID d&#39;élève direct. Il s’agit de clés étrangères crénelées. Ils pointent vers la même table utilisateur mais représentent un rôle différent :

* **Instructeur** : la session de module rejoint l&#39;utilisateur en tant qu&#39;instructeur de la session
* **Auteur** : l&#39;auteur LO rejoint l&#39;utilisateur en tant qu&#39;auteur de l&#39;objet d&#39;apprentissage
* **Responsable** : l’utilisateur se joint à lui-même pour représenter le responsable de l’élève
* **Terminé par** : l&#39;inscription et le relevé de notes du module comportent chacun une référence utilisateur distincte « terminé par »

C’est pourquoi un rapport unique peut afficher à la fois le nom d’un élève et le nom de son instructeur. Ils proviennent tous deux de l’entité utilisateur via des chemins de jointure différents.

**Types d&#39;ensemble de données de groupe d&#39;utilisateurs**

La catégorie **Groupe d&#39;utilisateurs** contient plusieurs vues d&#39;ensemble de données distinctes, chacune couvrant un type de groupe différent :

**Ensemble de données**

**Type de groupe**

**Groupe d’utilisateurs** (userGroup)

Tous les groupes d’utilisateurs. Utilisez-le comme ensemble de données du groupe d’utilisateurs principal

**Groupe d’utilisateurs de champ actif** (groupe_utilisateur_de_champ_actif)

Groupes basés sur les valeurs des champs actifs (par exemple, région, service)

**Groupe d’utilisateurs d’équipe** (groupe_utilisateur_équipe)

Groupes basés sur la hiérarchie du responsable

**Groupe d&#39;utilisateurs personnalisé** (custom_user_group)

Groupes personnalisés configurés manuellement

**Groupe d&#39;utilisateurs intégré** (inembedded_user_group)

Groupes définis par le système

Les ensembles de données de groupe d&#39;utilisateurs basés sur la vue (**Champ actif**, **Équipe**, **Personnalisé**, **Incorporé**) n&#39;ont pas de relations de clé étrangère directes dans le schéma, il s&#39;agit de vues SQL. Cela signifie qu&#39;ils ont des contraintes de jointure plus lâches que l&#39;ensemble de données de base du **groupe d&#39;utilisateurs**. Utilisez l&#39;ensemble de données de base du **groupe d&#39;utilisateurs** lorsque vous joignez des données de groupe d&#39;utilisateurs avec des données d&#39;inscription ou de relevé de notes pour obtenir les résultats les plus fiables.

**Champs dérivés**

Les champs dérivés sont des colonnes pré-calculées calculées par Report Builder. Ils sont répertoriés séparément des colonnes standard dans le sélecteur de colonnes.

**Champ dérivé**

**Ce qu&#39;il calcule**

**Ensembles de données requis**

**Conformité %**

Pourcentage d’élèves requis ayant terminé des cours marqués comme étant conformes

Groupe d’utilisateurs, Objet d’apprentissage, Transcription

**Achèvement %**

Terminations divisées par inscriptions × 100

Transcription ou objet d’apprentissage

**Nombre d&#39;utilisateurs inscrits**

Nombre total d’élèves inscrits pour un objet d’apprentissage

Objet d’apprentissage

**Nombre d&#39;achèvements**

Nombre total d’achèvements pour un objet d’apprentissage

Objet d’apprentissage

**Démarrer le comptage**

Élèves ayant commencé mais pas terminé

Objet d’apprentissage

**Nombre de membres**

Nombre d’utilisateurs dans un groupe d’utilisateurs

Groupe d’utilisateurs
