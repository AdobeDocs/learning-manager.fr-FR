---
description: Découvrez les nouvelles fonctionnalités et les améliorations de la version de mars 2024 de Adobe Learning Manager
jcr-language: en_us
title: Résumé des nouvelles fonctionnalités
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: e21eb23c9b99ef5737ca105edede0eea7186ed02
workflow-type: tm+mt
source-wordcount: '3861'
ht-degree: 1%

---

# Résumé des nouvelles fonctionnalités {#new-features-summary}

Découvrez les nouvelles fonctionnalités et les améliorations de la version de mars 2024 de Adobe Learning Manager.

## Nouveautés de cette version {#whatsnewandchanged}

### Importation de compétences à partir de sources externes

Importez des compétences à partir de fournisseurs de contenu, tels que LinkedIn et Go1, à l’aide des connecteurs respectifs. Cette amélioration fait partie de l&#39;objectif visant à renforcer la capacité de Learning Manager à s&#39;intégrer à des systèmes externes de gestion des compétences et des nuages. Les compétences importées seront ajoutées aux compétences définies par l’administrateur dans Learning Manager et seront disponibles pour les auteurs pendant le processus de création du cours. Des améliorations ont également été apportées à la fonctionnalité de recherche de compétences sur toute la plateforme afin de fournir une meilleure expérience de recherche lorsque le compte a un grand nombre de compétences.

Afficher [Importer des compétences](administrators/feature-summary/import-skills-external-sources.md) pour en savoir plus.

### Personnalisation du branding

Vous pourrez désormais personnaliser certains éléments de l’interface utilisateur (nom de l’organisation, logo et thème de l’interface utilisateur) en fonction des groupes d’utilisateurs disponibles dans le compte. Par exemple, une organisation avec plusieurs divisions peut configurer un logo et un thème d’interface utilisateur personnalisés à afficher pour chaque division.

>[!NOTE]
>
>Cette fonctionnalité de marque multiple ne s’applique pas à la vue de l’administrateur. Ils verront toujours l’image de marque au niveau de l’organisation dans leur compte. Ceci est dû au fait qu’il s’agit d’une fonctionnalité destinée aux élèves et que les administrateurs peuvent ne pas la vouloir dans leur compte.

Afficher [Plusieurs personnalisations de marque](administrators/feature-summary/themes.md#multiple-branding) pour plus d’informations.


## Modifications pour les comptes avec une grande base d’utilisateurs

### Administrateur - Pages Cours ou Parcours d’apprentissage

Si un grand nombre d&#39;élèves sont inscrits au cours, par exemple, plus de 50 000, la liste des élèves ne s&#39;affiche pas. Vous pouvez soit rechercher un élève dans la section *Rechercher des élèves* barre de recherche ou sélectionner **Télécharger** lien en haut de la barre de recherche pour télécharger la liste des élèves.

### Page Administrateur - Élèves

Lors de la recherche d’un utilisateur, le **Télécharger l’élève** et **Exportation** options télécharger le même rapport. En attendant, lors de la recherche d’un groupe d’utilisateurs, vous pouvez désormais télécharger des utilisateurs filtrés à partir de ce groupe d’utilisateurs. Lors de la recherche d’un groupe d’utilisateurs, le **Télécharger la liste des élèves** modifications apportées à **Télécharger la liste des élèves pour le groupe d’utilisateurs** Le **Exportation** télécharge à nouveau la liste complète.

### Page Administrateur - Utilisateurs

#### Utilisateurs internes

Si le nombre d&#39;utilisateurs dépasse, par exemple, 50 000, un message vous invitera à télécharger les données pour une analyse plus détaillée ultérieurement. La barre de recherche est maintenant visible et affiche un utilisateur au format *Nom, adresse e-mail | UUID*.

>[!NOTE]
>
>L’UUID s’affiche uniquement si l’UUID est activé pour le compte.

#### Utilisateurs externes

Pour les utilisateurs externes, le même comportement s’applique. Si le nombre d’utilisateurs est élevé, vous pouvez télécharger les utilisateurs et récupérer les détails les concernant après une recherche au format *Nom, adresse e-mail | UUID*.

#### Page Nettoyage de l’utilisateur

Sur la page Nettoyage de l’utilisateur, pour les utilisateurs supprimés, nous avons supprimé la fonctionnalité de tri sur **Date de suppression**. Vous ne pouvez trier que sur les UUID.

### Pages Admin - Instance

#### Cours ou parcours d’apprentissage

Si le nombre d’inscriptions est élevé, Adobe Learning Manager n’affichera pas le nombre d’élèves. Une icône s’affiche à la place. Vous pouvez la sélectionner, afficher le nombre d’élèves et accéder à la page Élèves.

Le nombre d’élèves sera affiché sous forme de valeur approximative. Par exemple, si le nombre d’élèves est supérieur à 50 000, la valeur s’affichera comme étant supérieure à 50 K.

### Administrateur - Pages L1/L3

Sur la page Retour d&#39;informations L1, si le nombre d&#39;inscriptions au cours est élevé, la liste des élèves ne s&#39;affiche pas. Au lieu de cela, vous pouvez exporter la liste des utilisateurs pour une analyse plus détaillée ultérieurement.

La recherche prend en charge la saisie anticipée et les résultats sont limités à l’instance sélectionnée.

#### Page Présence et notation

Sur la page, lorsque vous recherchez un utilisateur, la recherche s’exécute sur toutes les instances disponibles. Cependant, le résultat s’applique à l’instance sélectionnée.

Sur la page Présence, si vous recherchez un groupe d&#39;utilisateurs et que le nombre d&#39;utilisateurs dépasse 10 000 dans le groupe d&#39;utilisateurs, indépendamment de l&#39;inscription, vous ne pouvez effectuer que des actions au niveau global. Vous ne pourrez pas afficher la liste des utilisateurs.

Si le nombre d’utilisateurs dans le groupe d’utilisateurs est inférieur à 10 000, vous pouvez effectuer des actions individuelles au niveau de l’utilisateur ainsi que des actions au niveau global. Dans ce cas, la liste des utilisateurs n’est pas désactivée.

### Page Administrateur - Certifications

Dans les versions actuelles de Adobe Learning Manager, si un grand nombre d’utilisateurs sont inscrits à une certification, vous ne pouvez pas afficher les élèves non inscrits depuis le **Statut** la liste déroulante est désactivée.

Dans cette version de Adobe Learning Manager, si le nombre d’utilisateurs inscrits est élevé, le **Statut** la liste déroulante affiche uniquement deux options : **Inscrit** et **Non inscrit**. L’option **Inscrit** est sélectionné par défaut. Si vous **Non inscrit**, la liste des élèves non inscrits s’affiche.

#### Modifications apportées au groupe d’utilisateurs

Dans le cas d’un groupe d’utilisateurs, si le nombre d’utilisateurs dans le groupe d’utilisateurs est inférieur à, par exemple, 50 000, le **Statut** La liste déroulante affiche toutes les options Certifié, Attribué et Expirant.

Si le nombre d’utilisateurs d’un groupe d’utilisateurs est élevé, le **Statut** la liste déroulante affiche uniquement deux options : **Inscrit** et **Non inscrit**, selon le nouveau design.

### Tableau de comparaison

<table>
    <tbody>
        <tr>
            <td><b>Page</b></td>
            <td><b>Avant modification du seuil</b></td>
            <td><b>Après modification du seuil</b></td>
        </tr>
        <tr>
            <td>Administrateur - Instance de cours</td>
            <td>Les occurrences s’affichent comme suit :
            <ul>
                <li>Modules</li>
                <li>Élèves inscrits</li>
                <li>Séances</li>
                <li>Badge</li>
                <li>Retour d’informations L1 activé</li>
                <li>Alertes de notification</li>
                <li>Points de ludification</li>
                <li>Code QR</li>
                <li>Extension du parcours d’apprentissage</li>
            </ul>
            <td>
                <ul>
                    <li>Si le nombre d'inscriptions dépasse le seuil prédéfini, ALM n'affiche pas le nombre ; il remplace le nombre par une icône qui, lorsqu'il est cliqué, affiche le nombre réel d'élèves et un lien pour vous amener à la page Élèves.</li>
                    <li>Le nombre d'inscriptions sera affiché sous une forme approximative. Par exemple, si le nombre est supérieur à 50 000, le nombre sera affiché comme supérieur à 50 K au niveau du cours.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Page Administrateur - Élèves</td>
            <td>
                    <ul>
                        <li>La liste des élèves s'affiche pour chaque instance.</li>
                        <li>Vous pouvez rechercher un utilisateur ou un groupe d'utilisateurs inscrit à un cours.</li>
                        <li>Le rapport exporté n’est constitué d’aucun filtre pour le groupe d’utilisateurs.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>La sélection de l'instance est désactivée.</li>
                    <li>Télécharger la liste des élèves télécharge également les mêmes données, à une exception près. Si vous recherchez un groupe d’utilisateurs, puis sélectionnez Télécharger la liste des élèves, il téléchargera ces données de groupe d’utilisateurs.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrateur - Page de commentaires L1/L3</td>
            <td>
                <p>Aucun changement dans le comportement existant</p>
            </td>
            <td>
                <ul>
                    <li>La sélection de l'instance est désactivée.</li>
                    <li>Si l’inscription à un cours dépasse 50 000, ALM ne répertorie pas les élèves et affiche uniquement la barre de recherche. Si l'inscription est inférieure à 50 000, ALM affiche à la fois la liste des élèves et la barre de recherche.</li>
                    <li>La mise en vente est désactivée par défaut.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Page Administrateur - Présence et notation</td>
            <td>
                <p>Aucun changement dans le comportement existant</p>
            </td>
            <td>
                <ul>
                    <li>La sélection de l’instance est désactivée lors de la recherche d’un utilisateur.</li>
                    <li>Si le nombre d'utilisateurs dépasse, par exemple, 50 000, il y aura un message supplémentaire pour télécharger les données pour une analyse plus détaillée plus tard. La barre de recherche est maintenant visible et affiche un utilisateur au format Nom, e-mail | UUID.</li>
                    <li>Si le nombre d’utilisateurs dans le groupe d’utilisateurs est inférieur à 10 000 indépendamment de l’inscription, vous pouvez effectuer des actions individuelles au niveau de l’utilisateur ainsi que des actions au niveau global. Dans ce cas, la liste des utilisateurs n’est pas désactivée.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Page Administrateur - Score du quiz L2</td>
            <td>
                    <ul>
                        <li>La recherche utilisateur est également implémentée.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>La recherche utilisateur est également implémentée. Lors des recherches de frappe anticipée au niveau objet d’apprentissage, la liste est filtrée pour l’instance actuellement sélectionnée.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Page Administrateur - Utilisateurs (interne, externe)</td>
            <td>
                    <ul>
                        <li>L’ID de messagerie s’affiche lors de la recherche d’un utilisateur.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Si le nombre d'utilisateurs dépasse, par exemple, 50 000, il y aura un message supplémentaire pour télécharger les données pour une analyse plus détaillée plus tard. La barre de recherche est maintenant visible et affiche un utilisateur au format Nom, e-mail | UUID.</li>
                    <li>Sur la page Nettoyage de l’utilisateur, pour les utilisateurs supprimés, nous avons supprimé la fonctionnalité de tri sur **Date de suppression**. Vous ne pouvez trier que sur les UUID.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Instructeurs - Envoi</td>
            <td>
                    <ul>
                        <li>Pagination des modules à soumettre.</li>
                        <li>En tant qu’instructeur, vous pouvez désormais filtrer les envois de fichiers des élèves en fonction du statut, de la fin de la révision, de l’envoi en attente, de la réussite et de l’échec. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Vous pouvez uniquement rechercher des utilisateurs, pas des groupes d’utilisateurs dans cette instance.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Compter sur l’aperçu en tant que page de l’élève</td>
            <td>
                    <ul>
                        <li>Le nombre inclut les données de l'inscription d'ordre supérieur.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Le nombre exclut les données des inscriptions de commande supérieure.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Fonctionnalités de recherche avancées

Dans cette version, nous avons amélioré l’expérience de recherche. Les résultats de la recherche sont récupérés en fonction non seulement des métadonnées, mais également de la sémantique et de la recherche dans le contenu pour obtenir des résultats basés sur la précision, l’actualité et le contenu pertinent.

Cette modification se traduit par :

* Catalogue et page Mon apprentissage : l’action de survol du cours, du parcours d’apprentissage et de la certification a été supprimée.
* Apparence de la barre de recherche.
* Ajout de balises de filtre dans l’application d’apprentissage.

Pour activer les fonctionnalités de recherche, contactez l’équipe CSAM de Adobe Learning Manager.

## Modifications de l&#39;interface utilisateur {#ui-changes}

### Page de création de cours

Lors du mappage des cours à un niveau de compétence, la liste des compétences est de recherche en premier. En d’autres termes, recherchez des compétences, et vous verrez une liste de compétences correspondant au terme recherché.

### Groupes d&#39;utilisateurs

#### Page Administrateur : Élèves

Lors de la recherche d’un utilisateur, le **Télécharger l’élève** et **Exportation** options télécharger le même rapport. En attendant, lors de la recherche d’un groupe d’utilisateurs, vous pouvez désormais télécharger des utilisateurs filtrés à partir de ce groupe d’utilisateurs. Lors de la recherche d’un groupe d’utilisateurs, le **Télécharger la liste des élèves** modifications apportées à **Télécharger la liste des élèves pour le groupe d’utilisateurs** Le **Exportation** télécharge à nouveau la liste complète.

## Modifications apportées aux rapports

* Les colonnes Balise(s) et Compétence(s) dans le rapport de formations sont remplacées par Balise et Compétences.
* Ajout du rapport [Piste d’audit de ludification](administrators/feature-summary/reports.md#gamification-audit-trail).
* Si un compte contient plus de 280000 élèves affectés à une compétence, le rapport d’élève est téléchargé au format csv compressé.
Si le compte comporte moins de 250000 élèves, le même rapport est téléchargé au format CSV.
Dans la page Administrateur, sélectionnez **Administrateur** > **Compétences** > **Compétence** > **Élèves**. Le rapport est téléchargé au format CSV.
* Le [Rapport récapitulatif de la session](administrators/feature-summary/reports.md#session-summary-report) comporte deux nouvelles colonnes : Informations sur le lieu et Région Lieu.

## Modifications apportées à la création de salles de classe

D’après [Paramètres administrateur](administrators/feature-summary/classroom.md#classroom-settings), vous, en tant qu’auteur, pouvez [création, modification et suppression d’emplacements](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>Lors de l’ajout d’emplacements et de libellés de catalogue, les auteurs (sur la page de création de cours) et les administrateurs (sur la page d’instance) verront une liste auto-remplie d’emplacements et de libellés de catalogue, respectivement.

En tant qu’administrateur, vous pouvez appliquer des restrictions à un auteur pour modifier ou supprimer un emplacement de salle de classe. Afficher [Paramètres de la salle de classe](administrators/feature-summary/classroom.md#classroom-settings) pour plus d’informations.

## Modifications apportées au parcours d’apprentissage flexible

Tous les comptes (anciens et nouveaux) de commenceront à inclure Échéance d’inscription, Échéance de désinscription et Limite de places dans l’application de l’élève pour un parcours d’apprentissage flexible.
Les élèves pourront désormais s’inscrire au parcours d’apprentissage flexible sans sélectionner d’instance du cours.

## Nouveau déclencheur pour les plans d’apprentissage

Un nouveau déclencheur a été ajouté à la page de configuration du plan d&#39;apprentissage. Les auteurs et les administrateurs pourront désormais déclencher des actions lorsqu’un élève échoue dans un module d’un cours.

Afficher [Plans d’apprentissage](administrators/feature-summary/learning-plans.md) pour plus d’informations.

## Nouvel état d’envoi

En tant qu’instructeur, vous pouvez désormais filtrer les envois de fichiers des élèves en fonction du statut, de la fin de la révision, de l’envoi en attente, de la réussite et de l’échec.

Afficher [Statut de la soumission](instructors/feature-summary/learners.md#filter-file-submissions) pour plus d’informations.

## Améliorations de la liste de contrôle

Dans la version de mars 2024 de Adobe Learning Manager, les améliorations apportées au workflow de liste de contrôle sont les suivantes :

### Interdire la progression en cas d’échec d’une liste de contrôle

Lors de la création d’une liste de contrôle, un auteur peut sélectionner **Activer** dans la section Liste de vérification obligatoire. Cela empêche un élève de continuer dans le module s’il échoue à la liste de contrôle. Ils ne peuvent poursuivre que s&#39;ils réussissent la liste de vérification.

Les examinateurs de la liste de contrôle, c&#39;est-à-dire les instructeurs ou les gestionnaires, peuvent ensuite vérifier l&#39;état de la liste de contrôle. Les réviseurs peuvent également réviser la liste de contrôle d’un élève dans l’ordre.

### Réévaluation d&#39;une liste de contrôle

Lors de la création d’une liste de contrôle, un auteur peut sélectionner **Activer** dans la section Réévaluation. Cela permet à un responsable ou à un instructeur de réévaluer un élève jusqu’à ce qu’il réussisse la liste de contrôle.

Si le module est obligatoire, la case de réévaluation est cochée par défaut.

Un instructeur ou un responsable peut également faire passer l’état d’une liste de contrôle de Échec à Réussite lorsque la réévaluation est activée.

Sur la page Liste de contrôle, un instructeur peut voir le nombre d’élèves à l’état En attente. En tant qu’instructeur, vous pouvez évaluer un élève et le réussir ou l’échouer. Si un élève est dans un état d’échec, vous pouvez uniquement afficher la liste de contrôle lorsque la réévaluation n’est pas activée.

Cela signifie que le **Activer** La case à cocher n&#39;a pas été sélectionnée dans la section Réévaluation lors de la création de la liste de contrôle. Si cette case est cochée, vous pouvez voir le bouton Afficher/Réévaluer sur la page Liste de contrôle de l’instructeur.

Sélectionnez le bouton pour réévaluer un élève et le marquer comme réussi ou échoué.

>[!NOTE]
>
>Ces deux fonctionnalités - Réévaluation et Définition de la liste de contrôle comme obligatoire - ne s’appliquent qu’aux modules nouvellement créés. Une fois qu’un cours est publié, il n’est plus possible d’activer/désactiver ces éléments.


Afficher [Création d’une liste de contrôle](authors/feature-summary/courses.md#checklist-fail) pour plus d’informations.

## Autres améliorations

### Notifications par e-mail relatives à la session

Dans les versions antérieures d’Adobe Learning Manager, un élève n’a pas effectué de courriers électroniques liés à la session, de mise à jour des détails de la session, d’invitation à la session et de rappel de session, lorsque :

* Les élèves ont terminé un cours,
* De nouvelles sessions sont ajoutées à un cours, ou
* Des modifications ont été apportées aux sessions existantes.

Dans la version de mars 2024 de Adobe Learning Manager, les nouvelles modifications sont les suivantes :

* Détails de la session mis à jour et invitation à la session (pour l’élève et l’instructeur)
   * Pour les sessions à venir, envoyez des e-mails à **Détails de la session mis à jour**, **Invitation à une session** pour les élèves inscrits et les instructeurs actuels seront obsolètes. Pour les sessions précédentes, e-mails pour **Détails de la session mis à jour** et **Invitation à une session** pour les élèves inscrits et les instructeurs actuels resteront en l’état.
* E-mails de rappel (pour l’administrateur et l’élève)
   * Pour les sessions suivantes, uniquement **Rappel de session** des e-mails seront envoyés.

>[!NOTE]
>
>Les e-mails ne dépendent pas de la fin de la session et du cours.


### Modifications apportées au site de référence AEM

Dans un site de référence AEM, nous avons ajouté la prise en charge de l’ajout d’un jeton d’actualisation administrateur au jeton d’accès élève.

### Masquer les envois des instructeurs

Une fois que les élèves ont téléchargé leurs fichiers à l&#39;aide du workflow d&#39;envoi de fichier, si un instructeur ne prend aucune action (approuver ou rejeter) sur l&#39;envoi, l&#39;URL d&#39;envoi est masquée de la vue après un nombre de jours prédéfini. Contactez les équipes CSAM de Adobe Learning Manager pour définir ou modifier le nombre de jours.

### Modifications de la terminologie du produit

Nous avons ajouté les colonnes *Instance* et *Élève* au vocabulaire de terminologie du produit.

### Modifications apportées à l’application mobile

Dans cette version de l’application mobile, les élèves peuvent planifier et gérer les rappels de cours en retard. Cliquer sur une notification de rappel en retard vous permet d’accéder aux options suivantes :

* Annuler
* Accéder au cours
* Me le rappeler dans 3 jours
* Me le rappeler dans une semaine

Sur Android : cliquez sur la notification push pour accéder à la page **Présentation du cours** page.
Sur iOS : cliquez sur la notification push pour accéder à la page d’accueil de l’application. Il s’agit d’une limitation connue dans iOS.

### Modifications de la liste de contrôle dans l’application de l’élève sur Salesforce

Si un élève échoue à une liste de contrôle, il ne peut pas passer au module ou cours suivant. Lorsque la case à cocher Liste de contrôle obligatoire est sélectionnée, l&#39;élève ne peut pas progresser dans un cours s&#39;il ne parvient pas à respecter la liste de contrôle.

Comme avec l’application web, si un élève ne parvient pas à une liste de contrôle sur l’application Salesforce, il verra un message et ne pourra pas continuer.

### Modifications apportées à Connect VC

Dans les versions actuelles de Adobe Learning Manager, un élève est marqué comme **Non Terminé** lorsqu&#39;ils sont inscrits à une session Connect VC, mais ne répondent pas aux critères d&#39;achèvement.

Dans cette version, le statut passe à **Encore à marquer**.

### Étiquetage blanc dans Adobe Learning Manager

L’application mobile Adobe Learning Manager prend désormais en charge l’étiquetage blanc, ce qui signifie que vous pouvez désormais publier l’application sous votre propre marque.

Afficher l’étiquetage blanc dans [application mobile Adobe Learning Manager](white-label.md) pour plus d’informations.

### Nouvelle colonne dans les fichiers CSV de migration

Dans cette version, il existe une nouvelle colonne facultative, uniqueLoId, dans les fichiers CSV de migration suivants.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>Le **uniqueLoId** est facultatif.


Si vous effectuez une migration pour mettre à jour un cours, un plan d’apprentissage ou une certification existant, le cours, le plan d’apprentissage ou la certification avec le **uniqueLOId** s’ajoutent à l’application d’auteur.

Lors de la migration, vous devez mettre à jour le **uniqueLOId** dans les fichiers CSV pour le cours, le plan d’apprentissage ou la certification, même s’il s’agit d’une colonne facultative.

Si le **uniqueLoId** n’est pas ajouté avant d’effectuer la migration lors de la mise à jour du cours, du plan d’apprentissage ou de la certification existant ayant **uniqueLOId** s, puis après la migration **uniqueLOId** les valeurs seront remplacées par des valeurs NULL.

>[!NOTE]
>
>La colonne, **uniqueLoId**, ne s’applique pas au fichier CSV de l’assistance à la tâche.


>[!IMPORTANT]
>
>Les valeurs de colonne doivent être uniques dans le compte. Vous ne pouvez pas utiliser la même valeur avec un cours ou une certification.

Téléchargez les fichiers CSV à partir de [Manuel de migration](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### Évaluation de l’application

Un élève peut fournir ses commentaires sur l’application Adobe Learning Manager pour améliorer encore l’expérience de l’application. Si l’élève note quatre étoiles ou plus, une fenêtre contextuelle s’affiche et lui demande d’évaluer l’application sur Play Store ou App Store.

### Bluejeans a atteint sa fin de vie en février 2024

Nous voulions vous informer que Bluejeans a atteint sa fin de vie (EOL) en février 2024. Après février 2024, Bluejeans ne recevra plus de mises à jour ni d’assistance. Nos équipes CSAM et support vous aideront pour toutes les questions ou préoccupations que vous pourriez avoir pendant cette période de transition.

Afficher [Connecteurs dans Adobe Learning Manager](integration-admin/feature-summary/connectors.md) pour plus d&#39;informations sur la configuration des connecteurs.

### Modifications apportées au rapport d’accès de connexion

Le rapport Accès par connexion ne sera disponible que pour les cinq derniers trimestres. Si un administrateur d’intégration demande le téléchargement à la demande de l’exportation unifiée avec **Accès à la connexion** cochée, Adobe Learning Manager affichera un message d’erreur. Cependant, il n&#39;y a pas d&#39;impact sur les autres rapports.

### Modifications apportées à ADFS

D’après les mappages, les champs Type d’employé et ID d’employé d’ADFS sont désormais disponibles dans Adobe Learning Manager.

## Modifications apportées aux API dans cette version

### API des élèves

Dans cette version, nous avons ajouté la prise en charge d’API pour permettre aux élèves d’afficher le logo de marque et les thèmes personnalisés au niveau du groupe d’utilisateurs.

Les API /account et /user?include=account renvoient quatre champs, qui sont remplacés spécifiques au champ actif de l’utilisateur appartenant à logoUrl, logoStyling et themeData.

### Nouveaux attributs

Un nouvel attribut, isExpiredsubmission, dans learningObjectResource, qui indique si l&#39;envoi dans la ressource a expiré ou non.

* API GET /account : renvoie un nouvel attribut **expiresubmissionDuration** X, où X est le nombre de jours défini. Si ce paramètre n’est pas défini, 0 est renvoyé
* API GET /LO avec ressource incluant un nouvel attribut **isExpiredsubmission** » Vrai ou faux.
   * True, si l&#39;envoi a expiré et que « submissionUrl » ne s&#39;affiche pas.
   * Si la valeur est False, l&#39;envoi n&#39;est pas expiré et « submissionUrl » est récupéré.

### Modifications d’API dans la liste de contrôle

Un cours peut être composé de plusieurs modules dont Liste de contrôle est un type de module. Ce module de liste de contrôle est évalué par l’instructeur et peut être marqué comme Échec ou Réussite en fonction de l’évaluation.

Mais dans les deux cas, l&#39;état de la liste de contrôle est marqué comme Terminé et de cette façon, le cours est marqué comme Terminé.

Dans cette version, l’API LO inclut le paramètre *isChecklistMandatory*. Si la valeur est True, la liste de contrôle est obligatoire.

### Prise en charge de plusieurs paramètres régionaux

Un administrateur peut désormais télécharger le rapport de retour d’informations L1 dans la langue de son choix. Cependant, vous ne pouvez pas encore télécharger de rapports de retour d&#39;informations L1 pour Power BI. Dans la demande d’API, utilisez le paramètre preferencesLocale pour spécifier les paramètres régionaux de votre choix.

### Modifications apportées au nombre de résumés d’instances

Cela s’applique aux comptes où les inscriptions à un cours Classroom/VC sont supérieures à 1 000.

Si le nombre est inférieur à 1 000, les inscriptions invalident le cache et retournent les valeurs mises à jour dans un appel API de résumé du GET, telles que le nombre d&#39;inscriptions, l&#39;achèvement et seatLimit.

Si le compte est activé pour cette fonctionnalité et que le nombre d’inscriptions est supérieur à 1 000, les valeurs sont extraites du cache.

### Tracés obsolètes

Actuellement, les API Learning Manager suivent une structure de données de graphique, qui vous permet de récupérer des données en parcourant le modèle d’API par le biais d’inclusions. Même si vous pouvez parcourir une API jusqu’à sept niveaux, la récupération des données à l’aide d’un seul appel API est coûteuse en termes de calcul.

Nous recommandons à tous les clients existants et nouveaux de passer de petits appels plusieurs fois au lieu d&#39;un seul appel important. Cette approche empêchera le chargement de données indésirables dans l&#39;appel.

#### Quels chemins sont obsolètes ?

Les chemins suivants sont obsolètes :

* /learningObjects
   * Chemins d’accès obsolètes :
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Chemins d’accès existants :
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Chemin d’accès obsolète :
      * enrollment.instances.subLoInstances.learningObject
   * Chemin existant :
      * enrollment.instances.subLoInstances
* /enrollments
   * Chemin d’accès obsolète :
      * loInstance.learningObject.enrollment
   * Nouveau chemin :
      * loInstance.learningObject
* /learningObjects/{id}
   * Chemin d’accès obsolète :
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nouveau chemin :
      * instance.subLoInstances

### Modifications de l’archivage des accès de connexion et du rapport d’audit utilisateur pour l’API de tâche

Avec cette version, l’API de tâche conserve le rapport d’accès de connexion pendant cinq trimestres et le rapport d’audit de l’utilisateur pendant six mois. Si vous souhaitez télécharger les données antérieures à cette période, vous devez transmettre le paramètre archive en spécifiant trimestre et année. Reportez-vous à l’exemple de charge utile.

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

Si vous tentez de télécharger le fichier **Accès à la connexion** rapport qui dépasse cinq trimestres, un message d’erreur s’affiche. Un message d’erreur similaire s’affiche si vous tentez de télécharger le fichier **Audit de l’utilisateur** rapport qui va au-delà de six mois.

### API obsolètes

Afficher [Dépréciations d’API dans Adobe Learning Manager](api-deprecations-list.md) pour obtenir la liste cumulée de toutes les API obsolètes du produit.

## Bogues corrigés dans cette mise à jour {#bug-fixes}

* Lorsqu&#39;un élève est inscrit à un cours, puis tente de s&#39;inscrire à un autre cours, un message d&#39;avertissement s&#39;affiche.
* Un groupe d’utilisateurs, même après sa suppression, est visible dans la recherche.
* Lorsque les utilisateurs déclenchent de nombreux relevés de notes d’élèves avec une grande quantité de données, la file d’attente des relevés de notes des élèves est bloquée et empêche toute nouvelle demande.
* Si un compte enfant demande à son compte parent de partager un rapport, le compte parent ne peut pas le faire.
* Les URL d’un cours et d’un parcours d’apprentissage sont redirigées vers des emplacements incorrects.
* Un élève consulte par intermittence l&#39;instance de cours d&#39;un autre cours en cliquant sur le lien du cours sur la page du catalogue.
* Le **Se désinscrire** le bouton ne s’affiche pas comme prévu après la première inscription, mais il s’affiche après une actualisation.
* Vous ne pouvez pas enregistrer le contenu ou un quiz dont le nom comporte un espace vide.
* Dans les cours approuvés par le responsable, vous pouvez réinscrire des élèves à un groupe d’utilisateurs.
* Dans certains cas, si vous tentez d’ajouter un champ actif supplémentaire, le message d’erreur « Impossible d’enregistrer les champs actifs » s’affiche.
* Le texte déborde dans le nom d&#39;un cours à l&#39;intérieur d&#39;une carte de cours dans la section Cours associés.
* Après le changement d&#39;instance et l&#39;inscription d&#39;un élève à l&#39;instance, les anciennes instances existent toujours dans le calendrier Outlook.
* Lorsqu&#39;un élève d&#39;un compte de pairs tente de sélectionner la miniature d&#39;un cours, un message d&#39;erreur s&#39;affiche.
* Lorsque les élèves s&#39;inscrivent à un cours, ils reçoivent plusieurs notifications pour l&#39;inscription.
* Si un utilisateur modifie manuellement le nom des catalogues créés dans un connecteur, de nouveaux catalogues sont créés et les cours sont publiés dans les catalogues incorrects.
* Les utilisateurs appartenant à des comptes inactifs reçoivent toujours des e-mails d’abonnement.

### Correctifs de bugs liés à l’API

* Le GET d’API/les utilisateurs ne récupèrent pas les détails d’un responsable.
* Dans un compte, les utilisateurs ont été créés via une importation d’utilisateur FTP planifiée pendant un temps d’arrêt planifié.
* Dans l&#39;application mobile ou le mode immersif, après avoir supprimé ou retiré une instance de cours et sélectionné l&#39;instance active suivante, le **Enregistrer les intérêts** au lieu de s’afficher **S’inscrire**.
* Lorsqu&#39;un élève d&#39;un compte de pairs tente de sélectionner la miniature d&#39;un cours à l&#39;aide de l&#39;API d&#39;objet d&#39;apprentissage, l&#39;erreur 403 Interdit s&#39;affiche.

## Configuration système

Afficher [Configuration requise pour Adobe Learning Manager](system-requirements.md).

## Versions précédentes d’Adobe Learning Manager

* [Version de novembre 2023](whats-new-november-2023.md)
* [Version de juillet 2023](whats-new-2023-july.md)
