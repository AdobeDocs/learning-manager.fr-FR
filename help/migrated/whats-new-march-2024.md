---
description: Découvrez les nouvelles fonctionnalités et améliorations de la version de mars 2024 de Adobe Learning Manager
jcr-language: en_us
title: Résumé des nouvelles fonctionnalités
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: c833d92533b7fbf5a87c980d8b5e088185d02ef5
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 1%

---

# Résumé des nouvelles fonctionnalités {#new-features-summary}

Découvrez les nouvelles fonctionnalités et améliorations de la version de mars 2024 de Adobe Learning Manager.

Découvrez quelques-unes des dernières fonctionnalités d’Adobe Learning Manager, telles que :

1. Importation de compétences à partir de sources externes
1. Prise en charge de plusieurs marques
1. Liste de contrôle du module réévaluation-activité
1. Application d’apprentissage mobile en marque blanche

>[!NOTE]
>
>Consultez ce [webinaire](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) pour en savoir plus sur les nouvelles fonctionnalités de cette version.


## Nouveautés de cette version {#whatsnewandchanged}

### Importation de compétences à partir de sources externes

Importez des compétences à partir de fournisseurs de contenu, tels que LinkedIn et Go1, à l’aide des connecteurs respectifs. Cette amélioration fait partie de l’objectif de la capacité du gestionnaire de la formation à s’intégrer aux nuages de compétences externes et aux systèmes de gestion des talents. Les compétences importées seront ajoutées aux compétences définies par l’administrateur dans Learning Manager et seront disponibles pour les auteurs pendant le processus de création de cours. Des améliorations ont également été apportées à la fonctionnalité de recherche de compétences sur l’ensemble de la plateforme afin d’offrir une meilleure expérience de recherche lorsque le compte possède un grand nombre de compétences.

Voir [les compétences](administrators/feature-summary/import-skills-external-sources.md) d’importation pour en savoir plus.

### Personnalisation de la marque

Vous pourrez désormais personnaliser certains éléments de l’interface utilisateur : le nom de l’organisation, le logo et le thème de l’interface utilisateur en fonction des groupes d’utilisateurs disponibles dans le compte. Par exemple, une organisation avec plusieurs divisions peut configurer un logo personnalisé et un thème d’interface utilisateur à afficher pour chaque division.

>[!NOTE]
>
>Cette fonctionnalité de marques multiples ne s’applique pas à la vue de l’administrateur. Ils verront toujours la valorisation de marque au niveau de l’organisation dans leur compte. C’est parce qu’il s’agit d’une fonctionnalité destinée aux apprenants et que les administrateurs peuvent ne pas la vouloir dans leur compte.

Pour plus d’informations, voir [Marques personnalisées](administrators/feature-summary/themes.md#multiple-branding) multiples.


## Changements pour les comptes avec une base d’utilisateurs importante

### Pages Admin- Cours ou Cursus de formation

Si un grand nombre d’apprenants sont inscrits au cours, par exemple plus de 50 000, la liste des apprenants ne sera pas affichée. Vous pouvez rechercher un apprenant dans la *barre de recherche Search Apprenants* ou sélectionner le **lien Télécharger** en haut de la barre de recherche pour télécharger la liste des apprenants.

### Admin- Page Apprenants

Lorsque vous recherchez un utilisateur, les options Télécharger l’élève **** et **Exporter** téléchargent le même rapport. Pendant ce temps, lors de la recherche d’un groupe d’utilisateurs, vous pouvez désormais télécharger des utilisateurs filtrés de ce groupe d’utilisateurs. Lors de la recherche d’un groupe d’utilisateurs,
La **liste** des élèves téléchargée **devient Télécharger la liste des élèves pour le groupe** d’utilisateurs L’option **Exporter** permet à nouveau de télécharger la liste complète.

### Page Admin- Utilisateurs

#### Utilisateurs internes

Si le nombre d’utilisateurs dépasse, par exemple, 50 000, il y aura un message pour télécharger les données pour une analyse plus détaillée plus tard. La barre de recherche est maintenant bien visible et affiche un utilisateur au format *Nom, e-mail | UUID*.

>[!NOTE]
>
>L’UUID s’affiche uniquement si l’UUID est activé pour le compte.

#### Utilisateurs externes

Pour les utilisateurs externes, le même comportement s’applique. Si le nombre d’utilisateurs est important, vous pouvez télécharger les utilisateurs, et également récupérer les détails d’un utilisateur après une recherche au format *Nom, e-mail | UUID*.

#### Page de nettoyage de l’utilisateur

Sur la page Nettoyage des utilisateurs, pour les utilisateurs supprimés, nous avons supprimé la fonctionnalité de tri sur **Date de** suppression. Vous pouvez trier uniquement sur les UUID.

### Pages d’instances d’administration

#### Cours ou cursus de formation

Si le nombre d’inscriptions est important, Adobe Gestionnaire de formation n’affiche pas le nombre d’apprenants. Au lieu de cela, il y aura une icône, que vous pourrez sélectionner, afficher le nombre d’apprenants et accéder à la page Apprenants.

Le nombre d’apprenants s’affiche sous la forme d’une valeur approximative. Par exemple, si le nombre d’apprenants est supérieur à 50 000, la valeur sera affichée comme 50K+.

### Admin- Pages L1/L3

Sur la page L1 Feedback, si le nombre d’inscriptions aux cours est important, la liste des apprenants n’est pas affichée. Vous pouvez exporter la liste des utilisateurs en vue d’une analyse plus détaillée ultérieurement.

La recherche prend en charge la saisie anticipée et les résultats sont limités à l’instance sélectionnée.

#### Page Présence et notation

Sur la page, lorsque vous recherchez un utilisateur, la recherche s’exécute sur toutes les instances disponibles. Toutefois, le résultat concerne l’instance sélectionnée.

Sur la page Présence, si vous recherchez un groupe d’utilisateurs et que le nombre d’utilisateurs dépasse 10 000 dans le groupe d’utilisateurs, quelle que soit l’inscription, vous ne pouvez effectuer que des actions au niveau de l’ensemble. Vous ne pourrez pas afficher la liste des utilisateurs.

Si le nombre d’utilisateurs dans le groupe d’utilisateurs est inférieur à 10 000, vous pouvez effectuer des actions individuelles au niveau de l’utilisateur ainsi que des actions au niveau de l’ensemble. Dans ce cas, la liste des utilisateurs n’est pas désactivée.

### Admin- Page Certifications

Dans les versions actuelles de Adobe Learning Manager, si un grand nombre d’utilisateurs sont inscrits à une certification, vous ne pouvez pas afficher les élèves non inscrits car la **liste déroulante État** est désactivée.

Dans cette version de Adobe Learning Manager, si le nombre d’utilisateurs inscrits est important, la liste déroulante État n’affiche **que deux options :** Inscrits **et** Non inscrits **.** L’option **Inscrit est sélectionnée** par défaut. Si vous sélectionnez **Non inscrit**, la liste des apprenants non inscrits s’affiche.

#### Modifications apportées au groupe d’utilisateurs

Dans le cas d’un groupe d’utilisateurs, si le nombre d’utilisateurs dans le groupe d’utilisateurs est inférieur, par exemple, à 50 000, la **liste déroulante État** affiche toutes les options - Certifié, Attribué et Expiration.

Si le nombre d’utilisateurs dans un groupe d’utilisateurs est important, la liste déroulante État n’affiche **que deux options :** Inscrit **et** Non inscrit **, selon la nouvelle conception.**

### Tableau comparatif

<table>
    <tbody>
        <tr>
            <td><b>Page</b></td>
            <td><b>Avant le changement de seuil</b></td>
            <td><b>Après le changement de seuil</b></td>
        </tr>
        <tr>
            <td>Admin- Instance de cours</td>
            <td>Les instances s’affichent comme conçues avec ce qui suit :
            <ul>
                <li>Modules</li>
                <li>Apprenants inscrits</li>
                <li>Séances</li>
                <li>Badge</li>
                <li>Retour d’informations L1 activé</li>
                <li>Alertes de notification</li>
                <li>Points de ludification</li>
                <li>Code QR</li>
                <li>Extension du cursus de formation</li>
            </ul>
            <td>
                <ul>
                    <li>Si le nombre d’inscriptions dépasse le seuil prédéfini, ALM n’affichera pas le nombre ; il remplacera le décompte par une icône qui, une fois cliquée, affiche le nombre réel d’apprenants et un lien pour vous diriger vers la page Apprenants.</li>
                    <li>Le nombre d’inscriptions sera affiché dans un format approximatif. Par exemple, si le nombre est supérieur à 50 000, le nombre sera affiché comme 50K+ au niveau du cours.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Page Apprenants</td>
            <td>
                    <ul>
                        <li>La liste des apprenants s’affiche pour chaque instance.</li>
                        <li>Vous pouvez rechercher un utilisateur ou un groupe d’utilisateurs inscrit à un cours.</li>
                        <li>Le rapport exporté ne comporte aucun filtre pour le groupe d’utilisateurs.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>La sélection de l’instance est désactivée.</li>
                    <li>Télécharger la liste des apprenants télécharge également les mêmes données, sauf dans un cas. Si vous recherchez un groupe d’utilisateurs, puis sélectionnez Télécharger la liste des élèves, il téléchargera ces données de groupe d’utilisateurs.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Page de commentaires L1/L3</td>
            <td>
                <p>Aucun changement du comportement existant</p>
            </td>
            <td>
                <ul>
                    <li>La sélection de l’instance est désactivée.</li>
                    <li>Si le nombre d’inscriptions à un cours est supérieur à 50K, ALM ne répertorie pas les apprenants et affiche uniquement la barre Search. Si le nombre d’inscriptions est inférieur à 50 Ko, ALM affiche à la fois la liste des apprenants et la barre de recherche.</li>
                    <li>La liste est désactivée par défaut.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Page de présence et de notation</td>
            <td>
                <p>Aucun changement du comportement existant</p>
            </td>
            <td>
                <ul>
                    <li>La sélection d’instance est désactivée lors de la recherche d’un utilisateur.</li>
                    <li>Si le nombre d’utilisateurs dépasse, par exemple, 50 000, il y aura un message supplémentaire pour télécharger les données pour une analyse plus détaillée plus tard. La barre de recherche est maintenant bien visible et affiche un utilisateur au format Nom, e-mail | UUID.</li>
                    <li>Si le nombre d’utilisateurs dans le groupe d’utilisateurs est inférieur à 10 000, quelle que soit l’inscription, vous pouvez effectuer des actions individuelles au niveau de l’utilisateur ainsi que des actions au niveau de l’ensemble. Dans ce cas, la liste des utilisateurs n’est pas désactivée.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Page du score du quiz L2</td>
            <td>
                    <ul>
                        <li>La recherche d’utilisateurs est également implémentée.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>La recherche d’utilisateurs est également implémentée. Alors que la recherche par saisie anticipée au niveau LO, la liste est filtrée selon l’instance actuellement sélectionnée.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Page Admin- Utilisateurs (interne, externe)</td>
            <td>
                    <ul>
                        <li>L’ID de message électronique s’affiche lors de la recherche d’un utilisateur.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Si le nombre d’utilisateurs dépasse, par exemple, 50 000, il y aura un message supplémentaire pour télécharger les données pour une analyse plus détaillée plus tard. La barre de recherche est maintenant bien visible et affiche un utilisateur au format Nom, e-mail | UUID.</li>
                    <li>Sur la page Nettoyage des utilisateurs, pour les utilisateurs supprimés, nous avons supprimé la fonctionnalité de tri sur **Date de suppression**. Vous pouvez trier uniquement sur les UUID.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Instructeurs - Soumission</td>
            <td>
                    <ul>
                        <li>Pagination des modules à soumettre.</li>
                        <li>En tant qu’instructeur, vous pouvez désormais filtrer les soumissions de fichiers des élèves en fonction de l’état, de la fin de la révision, de la soumission en attente, de la réussite et de l’échec. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Dans ce cas, vous pouvez rechercher uniquement des utilisateurs, et non des groupes d’utilisateurs.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Comptez sur l’aperçu en tant que page des élèves</td>
            <td>
                    <ul>
                        <li>Nombre inclut les données d’inscription d’ordre supérieur.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Le nombre exclut les données des inscriptions d’ordre supérieur.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Fonctions de recherche avancées

Dans cette version, nous avons amélioré l’expérience de recherche. Les résultats de la recherche sont récupérés en fonction non seulement des métadonnées, mais aussi de la recherche sémantique et dans le contenu pour dériver des résultats basés sur la précision, la récence et le contenu pertinent.

Ce changement se reflète sur les éléments suivants :

* Catalogue et page Mon apprentissage : l’action de survol sur le cours, le cursus de formation et la certification a été supprimée.
* Apparence de la barre de recherche.
* Ajout de balises de filtre dans l’application d’apprentissage.

Pour activer les fonctionnalités de recherche, contactez l’équipe CSAM de Adobe Learning Manager.

## Modifications de l&#39;interface utilisateur {#ui-changes}

### Page de création de cours

Lors de la cartographie des cours à un niveau de compétence, la liste des compétences est la recherche en premier. En d’autres termes, recherchez des compétences, et vous verrez une liste de compétences correspondant au terme recherché.

### Groupes d&#39;utilisateurs

#### Admin : page des apprenants

Lorsque vous recherchez un utilisateur, les options Télécharger l’élève **** et **Exporter** téléchargent le même rapport. Pendant ce temps, lors de la recherche d’un groupe d’utilisateurs, vous pouvez désormais télécharger des utilisateurs filtrés de ce groupe d’utilisateurs. Lors de la recherche d’un groupe d’utilisateurs, la liste **des élèves de téléchargement** devient **Télécharger la liste des élèves pour le groupe** d’utilisateurs L’option **Exporter** télécharge à nouveau la liste complète.

## Modifications apportées aux rapports

* Les colonnes Balise(s) et Compétence(s) du rapport Formations sont remplacées par Balise et compétences.
* Ajout du rapport [Gamification Audit Trail](administrators/feature-summary/reports.md#gamification-audit-trail).
* Si un compte contient plus de 280000 apprenants affectés à une compétence, le rapport sur les compétences est téléchargé au format CSV compressé.
Si le compte compte moins de 250000 élèves, le même rapport est téléchargé au format CSV.
Sur la page Admin, sélectionnez **Compétences****>** administration > **compétences** > **apprenants**. Le rapport est téléchargé au format CSV.
* Le [rapport](administrators/feature-summary/reports.md#session-summary-report) Résumé de la session comporte deux nouvelles colonnes : Informations de localisation et Région de localisation.

## Changements apportés à la création de salles de classe

En fonction des [paramètres](administrators/feature-summary/classroom.md#classroom-settings) administrateurs, vous, en tant qu’auteur, pouvez [créer, modifier et supprimer des emplacements](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>Lors de l’ajout d’étiquettes d’emplacement et de catalogue, les auteurs (dans la page de création de cours) et les administrateurs (à la page de l’instance) verront une liste d’emplacements et d’étiquettes de catalogue renseignée automatiquement, respectivement.

En tant qu’administrateur, vous pouvez imposer des restrictions à un auteur pour modifier ou supprimer l’emplacement d’une salle de classe. Afficher [les paramètres](administrators/feature-summary/classroom.md#classroom-settings) de la salle de classe pour plus d’informations.

## Modifications apportées au cursus de formation flexible

Tous les comptes (anciens et nouveaux) commenceront, y compris la date limite d’inscription, la date limite de désinscription et la limite de siège dans l’application Apprenant pour un parcours d’apprentissage flexible.
Les apprenants pourront désormais s’inscrire au parcours d’apprentissage flexible sans sélectionner aucune instance du cours.

## Nouveau déclencheur pour les plans d’apprentissage

Un nouveau déclencheur a été ajouté à la page de configuration du plan d’apprentissage. Les auteurs et les administrateurs pourront désormais déclencher des actions lorsqu’un élève échoue à un module d’un cours.

Pour plus d’informations, consultez [les plans](administrators/feature-summary/learning-plans.md) pédagogiques.

## Nouvel état d’envoi

En tant qu’instructeur, vous pouvez désormais filtrer les soumissions de fichiers des élèves en fonction de l’état, de la fin de la révision, de la soumission en attente, de la réussite et de l’échec.

Voir [l’état](instructors/feature-summary/learners.md#filter-file-submissions) de soumission pour plus d’informations.

## Améliorations aux listes de contrôle

Dans la version de mars 2024 de Adobe Learning Manager, les améliorations apportées au workflow de liste de contrôle sont les suivantes :

### Interdire la progression en cas d’échec d’une liste de contrôle

Lors de la création d’une liste de contrôle, un auteur peut sélectionner **Activer** dans la section Liste de contrôle obligatoire. Cela empêche un apprenant de poursuivre le module s’il échoue à la liste de contrôle. Ils ne peuvent continuer que s’ils réussissent la liste de contrôle.

Les réviseurs de la liste de contrôle, c’est-à-dire les instructeurs ou les gestionnaires, peuvent alors vérifier l’état de la liste de contrôle. Les réviseurs peuvent également consulter la liste de contrôle d’un élève dans le désordre.

### Réévaluation d’une liste de contrôle

Lors de la création d’une liste de contrôle, l’auteur peut sélectionner **Activer** dans la section Réévaluation. Cela permet à un responsable ou à un instructeur de réévaluer un apprenant jusqu’à ce qu’il réussisse la liste de contrôle.

Si le module est obligatoire, la case à cocher Réévaluation est sélectionnée par défaut.

Un instructeur ou un responsable peut également modifier l’état d’une liste de contrôle de Échec à Réussi lorsque la réévaluation est activée.

Sur la page Liste de contrôle, un instructeur peut voir le nombre d’apprenants dans l’état En attente. En tant qu’instructeur, vous pouvez évaluer un apprenant et le réussir ou l’échouer. Si un élève est dans un état d’échec, vous ne pouvez afficher la liste de contrôle que lorsque la réévaluation n’est pas activée.

Cela signifie que la **case à cocher Activer** n’a pas été sélectionnée dans la section Réévaluation lors de la création de la liste de contrôle. Si cette case est cochée, vous pouvez voir le bouton Afficher/Réévaluer sur la page Liste de contrôle de l’instructeur.

La sélection du bouton vous permet de réévaluer un apprenant et de le noter comme ayant réussi ou échoué.

>[!NOTE]
>
>Ces deux fonctionnalités - la réévaluation et le fait de rendre la liste de contrôle obligatoire - ne s’appliquent qu’aux modules nouvellement créés. Une fois qu’un cours est publié, il n’est pas possible de l’activer/de le désactiver.


Voir [Créez une liste de contrôle](authors/feature-summary/courses.md#checklist-fail) pour plus d’informations.

## Autres améliorations

### Notifications par courrier électronique liées à la session

Dans les versions antérieures de Adobe Learning Manager, un élève n’avait pas les courriers électroniques liés à la session, les détails de la session mis à jour, l’invitation à la session et le rappel de session, lorsque :

* Les apprenants ont terminé un cours,
* De nouvelles sessions sont ajoutées à un cours, ou
* Des modifications ont été apportées aux sessions existantes.

Dans la version de mars 2024 de Adobe Learning Manager, voici les nouvelles modifications :

* Détails de la session mis à jour et invitation à une session (pour l’apprenant et l’instructeur)
   * Pour les sessions futures, les e-mails pour **les détails de la session mis à jour**, **l’invitation** de session pour les apprenants inscrits et les instructeurs actuels seront obsolètes. Pour les sessions précédentes, les e-mails pour **les détails de la session mis à jour** et **l’invitation** de session pour les apprenants inscrits et les instructeurs actuels resteront tels quels.
* Messages électroniques de rappel (pour l’administrateur et l’élève)
   * Pour les sessions futures, seuls **des e-mails de rappel** de session seront envoyés.

>[!NOTE]
>
>Les emails ne dépendent pas de l’achèvement de la session et du cours.


### AEM Modifications apportées au site de référence

Dans un site de référence AEM, nous avons ajouté la prise en charge de l’ajout d’un jeton d’actualisation administrateur au jeton d’accès des élèves.

### Masquer les soumissions aux professeurs

Une fois que les élèves ont téléchargé leurs fichiers à l’aide du flux de travail d’envoi de fichier, si un instructeur n’entreprend aucune action (approuver ou rejeter) sur l’envoi, l’URL d’envoi est masquée de la vue après un nombre prédéfini de jours. Contactez les équipes CSAM de Adobe Learning Manager pour définir ou modifier le nombre de jours.

### Changements de terminologie du produit

Nous avons ajouté les colonnes *Instance* et *Apprenant* au vocabulaire terminologique du produit.

### Modifications apportées aux applications mobiles

Dans cette version de l’application mobile, les apprenants peuvent planifier et gérer les rappels de cours en retard. En cliquant sur une notification de rappel en retard, vous pouvez accéder aux options suivantes :

* Annuler
* Accéder au cours
* Me le rappeler dans 3 jours
* Me le rappeler dans une semaine

Sur Android : en cliquant sur la notification push, vous serez dirigé vers la page Aperçu **du**cours.
Sur iOS : en cliquant sur la notification push, vous serez dirigé vers la page d’accueil de l’application. Il s’agit d’une limitation connue dans iOS.

### Modifications apportées à la liste de contrôle dans l’application Apprenant sur Salesforce

Si un apprenant échoue à une liste de contrôle, il ne peut pas passer au module ou au cours suivant. Lorsque la case Liste de contrôle obligatoire est cochée, l’apprenant ne peut pas avancer dans un cours s’il échoue à la liste de contrôle.

Comme pour l’application Web, si un élève échoue à une liste de contrôle sur l’application Salesforce, il verra un message et ne progressera pas.

### Changements dans Connect VC

Dans les versions actuelles de Adobe Learning Manager, un élève est marqué **Non assisté** lorsqu’il est inscrit à une session Connect VC, mais qu’il ne répond pas aux critères d’achèvement.

Dans cette version, l’état passe à **À marquer**.

### Marque blanche dans Adobe Learning Manager

Adobe’application mobile Learning Manager prend désormais en charge la marque blanche, ce qui signifie que vous pouvez désormais publier l’application sous votre propre marque.

Voir Étiquetage blanc dans [Adobe application mobile](white-label.md) Learning Manager pour plus d’informations.

### Nouvelle colonne des CSV de migration

Dans cette version, il existe une nouvelle colonne facultative, uniqueLoId, dans les fichiers CSV de migration suivants.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>La **colonne uniqueLoId** est facultative.


Si vous effectuez une migration pour mettre à jour un cours, un plan d’apprentissage ou une certification existant, le cours, le plan d’apprentissage ou la certification avec les **LOId** uniques est ajouté à l’application Auteur.

Lors de la migration, vous devez mettre à jour les **valeurs LOId uniques dans les fichiers CSV pour le cours, le plan d’apprentissage ou la certification, même s’il s’agit d’une** colonne facultative.

Si la colonne uniqueLoId **n’est** pas ajoutée avant d’effectuer la migration lors de la mise à jour du cours existant ou du plan d’apprentissage ou de la certification ayant **des LOId uniques, les valeurs uniqueLOId****après la** migration seront remplacées par des valeurs NULL.

>[!NOTE]
>
>La colonne « **uniqueLoId** » ne s’applique pas au fichier CSV d’aide à la tâche.


>[!IMPORTANT]
>
>Les valeurs de colonne doivent être uniques pour l’ensemble du compte. Vous ne pouvez pas utiliser la même valeur avec un cours ou une certification.

Téléchargez les fichiers CSV depuis le [manuel](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs) de migration.


### Évaluation de l’application

Un apprenant peut fournir ses commentaires sur l’application Adobe Learning Manager pour améliorer davantage l’expérience de l’application. Si l’élève note quatre étoiles ou plus, une fenêtre contextuelle s’affiche pour lui demander d’évaluer l’application sur le Play Store ou l’App Store.

### Bluejeans a atteint sa fin de vie (EOL) en février 2024

Nous voulions vous informer que Bluejeans a atteint sa fin de vie (EOL) en février 2024. Après février 2024, Bluejeans ne recevra plus de mises à jour ni de support. Nos équipes de CSAM et de soutien vous aideront à répondre à toutes vos questions ou préoccupations pendant cette période de transition.

Afficher [les connecteurs dans Adobe Learning Manager](integration-admin/feature-summary/connectors.md) pour plus d’informations sur la configuration des connecteurs.

### Modifications apportées au rapport Identifiants d’accès

Le rapport Connexion d’accès ne sera disponible que pour les cinq derniers trimestres. Si des demandes d’administration d’intégration Le téléchargement à la demande de l’exportation unifiée avec **accès de connexion** est coché, Adobe Learning Manager affiche un message d’erreur. Cependant, il n’y a aucun impact sur les autres rapports.

### Modifications d’ADFS

Les champs Type d’employé et ID d’employé d’ADFS sont désormais disponibles sur Adobe Gestionnaire de formation, en fonction des mappages.

## Modifications apportées aux API dans cette version

### API de l’apprenant

Dans cette version, nous avons ajouté la prise en charge des API permettant aux apprenants d’afficher le logo de marque et les thèmes personnalisés au niveau Groupe d’utilisateurs.

Les API /account et /user ?include=account renvoient quatre champs, qui sont remplacés spécifiquement pour le champ actif de l’utilisateur appartenant à logoUrl, logoStyling et themeData.

### Nouveaux attributs

Un nouvel attribut, isExpiredSubmission, dans learningObjectResource, qui indique si l’envoi dans la ressource a expiré ou non.

* API GET /account : renvoie le nouvel attribut **expireSubmissionDuration** X, où X correspond au nombre de jours défini. Si le paramètre n’est pas défini, 0 sera renvoyé
* GET l’API /LO avec ressource inclut le nouvel attribut **isExpiredSubmission** » True ou False.
   * True, si l’envoi a expiré et que « submissionUrl » n’est pas affiché.
   * Si la valeur est False, l’envoi n’est pas expiré et « submissionUrl » est récupéré.

### Modifications d’API dans la liste de contrôle

Un cours peut être composé de plusieurs modules dont la liste de contrôle est un type de module. Ce module de liste de contrôle est évalué par l’instructeur et peut être marqué comme Échec ou Succès en fonction de l’évaluation.

Mais dans les deux cas, l’état de la liste de contrôle est marqué comme terminé et de cette façon, le cours est marqué comme terminé.

Dans cette version, l’API LO inclut le paramètre *isChecklistMandatory*. Si la valeur est True, la liste de contrôle est obligatoire.

### Prise en charge de plusieurs paramètres régionaux

Un administrateur peut désormais télécharger le rapport de commentaires L1 dans la langue de son choix. Toutefois, vous ne pouvez pas encore télécharger de rapports de commentaires L1 pour Power BI. Dans la requête API, utilisez le paramètre preferredLocale pour spécifier les paramètres régionaux de votre choix.

### Changements dans le nombre de Résumé d’instance

Ceci s’applique aux comptes où le nombre d’inscriptions à un cours en classe / VC est supérieur à 1000.

Si le nombre est inférieur à 1000, les inscriptions invalident le cache et renvoient les valeurs mises à jour dans un appel d’API GET Summary, telles que number of enrollment, completion et seatLimit.

Si le compte est activé pour cette fonctionnalité et que le nombre d’inscriptions est supérieur à 1000, les valeurs sont récupérées à partir du cache.

### Chemins obsolètes

À l’heure actuelle, les API Learning Manager suivent une structure de données graphique, ce qui vous permet de récupérer des données en parcourant le modèle d’API via des inclusions. Même si vous pouvez traverser une API jusqu’à sept niveaux, la récupération des données à l’aide d’un seul appel d’API est coûteuse en calcul.

Nous recommandons à tous les clients existants et nouveaux de passer de petits appels plusieurs fois au lieu d’un seul appel volumineux. Cette approche empêche le chargement de données indésirables dans l’appel.

#### Quels sont les chemins obsolètes

Les chemins suivants sont obsolètes :

* /learningObjects
   * Chemins obsolètes :
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Chemins existants :
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Chemin d’accès obsolète :
      * enrollment.instances.subLoInstances.learningObject
   * Chemin existant :
      * enrollment.instances.subLoInstances
* /Inscriptions
   * Chemin d’accès obsolète :
      * loInstance.learningObject.enrollment
   * Nouveau chemin d’accès :
      * loInstance.learningObject
* /learningObjects/{id}
   * Chemin d’accès obsolète :
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nouveau chemin d’accès :
      * instance.subLoInstances

### Modifications de l’archivage des rapports d’accès aux utilisateurs et des rapports d’audit des utilisateurs pour l’API Tâche

Avec cette version, l’API Job conservera le rapport d’accès de connexion jusqu’à cinq trimestres et le rapport d’audit utilisateur pendant six mois. Si vous souhaitez télécharger les données antérieures à cette période, vous devez transmettre le paramètre archive, en spécifiant trimestre et année. Faites référence à l’exemple de charge utile.

```
{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateLoginAccessReport",
            "payload": {
                "fromDate": "2023-04-01T18:30:00.000Z",
                "toDate": "2023-04-30T18:30:00.000Z",
                "archive": {
                    "quarter": "4",
                    "year": "2021"
                }
            }
        }
    }
}
```

Si vous essayez de télécharger le rapport d’accès **** de connexion qui va au-delà de cinq trimestres, un message d’erreur s’affiche. Un message d’erreur similaire s’affiche si vous essayez de télécharger le rapport d’audit **** utilisateur qui va au-delà de six mois.

### API obsolètes

Affichez [les obsolescences d’API dans Adobe Learning Manager](api-deprecations-list.md) pour obtenir la liste cumulative de toutes les API obsolètes du produit.

## Bogues corrigés dans cette mise à jour {#bug-fixes}

* Lorsqu’un élève est inscrit à un cours, puis tente de s’inscrire à un autre cours, un message d’avertissement s’affiche.
* Un groupe d’utilisateurs, même après avoir été supprimé, est visible dans Search.
* Lorsque les utilisateurs déclenchent un grand nombre de relevés de notes de l’apprenant avec une grande quantité de données, la file d’attente des relevés de notes de l’apprenant est bloquée et empêche une nouvelle demande.
* Si un compte enfant demande à son compte parent de partager un rapport, le compte parent ne peut pas le faire.
* Les URL d’un cours et d’un cursus de formation redirigent vers des emplacements incorrects.
* Un élève affiche par intermittence l’instance de cours d’un autre cours en cliquant sur le lien du cours sur la page du catalogue.
* Le **bouton Désinscrire** ne s’affiche pas comme prévu après la première inscription, mais le bouton s’affiche après une actualisation.
* Vous ne pouvez pas enregistrer le contenu ou un quiz dont le nom contient un espace vide.
* Dans les cours approuvés par le responsable, vous pouvez réinscrire des apprenants dans un groupe d’utilisateurs.
* Dans certains cas, si vous essayez d’ajouter un champ actif supplémentaire, le message d’erreur « Impossible d’enregistrer les champs actifs » s’affiche.
* Le texte déborde dans le nom d’un cours à l’intérieur d’une carte de cours dans la section Cours associés.
* Après avoir changé d’instance et inscrit un élève à l’instance, les anciennes instances existent toujours dans le calendrier Outlook.
* Lorsqu’un élève d’un compte homologue tente de sélectionner la vignette d’un cours, un message d’erreur s’affiche.
* Lorsque les apprenants s’inscrivent à un cours, ils reçoivent plusieurs notifications pour l’inscription.
* Si un utilisateur modifie manuellement le nom des catalogues créés dans un connecteur, de nouveaux catalogues sont créés et les cours sont publiés dans les catalogues incorrects.
* Les utilisateurs appartenant à des comptes inactifs reçoivent toujours des courriers électroniques d’abonnement.

### Corrections de bogues liés à l’API

* L’API GET/users ne récupère pas les détails d’un gestionnaire.
* Dans un compte, les utilisateurs ont été créés via une importation d’utilisateur FTP planifiée pendant un temps d’arrêt planifié.
* Dans l’application mobile ou le mode immersif, après avoir supprimé ou retiré une instance de cours et sélectionné la prochaine instance active, le bouton Enregistrer l’intérêt s’affiche **au lieu de S’inscrire****.**
* Lorsqu’un élève d’un compte homologue tente de sélectionner la miniature d’un cours à l’aide de l’API d’objet d’apprentissage, l’erreur 403 Forbidden s’affiche.

## Configuration système

Consultez [Adobe configuration système requise](system-requirements.md) pour Learning Manager.

## Versions précédentes d’Adobe Learning Manager

* [Version de novembre 2023](whats-new-november-2023.md)
* [Version de juillet 2023](whats-new-2023-july.md)
