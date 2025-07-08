---
description: Découvrez comment créer et gérer des groupes d’utilisateurs dans Adobe Learning Manager. Découvrez comment le regroupement d’utilisateurs vous aide à attribuer des cours, à suivre la progression et à automatiser efficacement les workflows d’apprentissage.
jcr-language: en_us
title: Gestion des groupes d’utilisateurs dans Adobe Learning Manager | Organiser et affecter des élèves
exl-id: 5569a201-0648-4b2c-bab3-927e5c149290
source-git-commit: 0dade561e53e46f879e22b53835b42d20b089b31
workflow-type: tm+mt
source-wordcount: '1441'
ht-degree: 0%

---

# Groupes d’utilisateurs dans Adobe Learning Manager

Les groupes d&#39;utilisateurs dans Adobe Learning Manager vous aident à organiser les élèves en fonction d&#39;attributs communs tels que le service, l&#39;emplacement ou le rôle. Le regroupement d’utilisateurs facilite l’attribution de cours, la gestion des autorisations et le suivi de la progression de l’apprentissage pour plusieurs utilisateurs à la fois.

>[!INFO]
>
>Regardez cette formation ALM Academy pour apprendre à créer un groupe d’utilisateurs par noms, ID de messagerie et combinaison de plusieurs groupes d’utilisateurs générés automatiquement. <br>[![bouton](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555694)</br>

## Types de groupes d’utilisateurs

Adobe Learning Manager prend en charge les groupes d’utilisateurs suivants :

1. **Groupes d&#39;utilisateurs générés automatiquement :** dans Adobe Learning Manager, le système crée automatiquement certains groupes d&#39;utilisateurs en fonction des rôles et des attributs des utilisateurs. Ces groupes définis par le système incluent Tous les auteurs, Tous les administrateurs, Tous les élèves et Tous les responsables. Adobe Learning Manager génère ces groupes pour vous aider à organiser les utilisateurs par rôle. Vous ne pouvez pas renommer ou supprimer ces groupes définis par le système.

2. **Groupes d&#39;utilisateurs personnalisés :** dans Adobe Learning Manager, les administrateurs peuvent créer des groupes d&#39;utilisateurs personnalisés pour organiser les élèves en fonction de critères spécifiques. Ces groupes sont dynamiques et ajoutent automatiquement des utilisateurs qui remplissent les conditions définies. Les groupes personnalisés permettent d’attribuer des parcours d’apprentissage ciblés, d’appliquer un branding personnalisé et de générer des rapports ciblés. C&#39;est un outil flexible pour gérer et personnaliser l&#39;expérience d&#39;apprentissage.

## Création d’un groupe d’utilisateurs personnalisé

Les administrateurs créent manuellement des groupes d’utilisateurs pour organiser les utilisateurs en fonction d’attributs définis. Ces groupes peuvent être dynamiques, ajoutant automatiquement des utilisateurs qui répondent aux critères spécifiés. Les groupes d’utilisateurs simplifient des tâches telles que l’affectation de parcours d’apprentissage, l’application d’un branding personnalisé et la génération de rapports ciblés.

Pour créer un groupe d’utilisateurs personnalisé :

1. Sélectionnez **Utilisateurs** sur la page d&#39;accueil de l&#39;administrateur.
2. Sélectionnez **Groupes d&#39;utilisateurs**, puis **Ajouter**.

   ![](assets/add-a-user-group.png)
   _Bouton pour ajouter un nouveau groupe d&#39;utilisateurs dans la page Groupes d&#39;utilisateurs_

3. Saisissez le nom et la description du groupe.

   ![](assets/group-name.png)
   _Champs de saisie pour saisir le nom du groupe et une description facultative_

## Ajout d’utilisateurs au groupe d’utilisateurs

Les administrateurs peuvent ajouter des utilisateurs à un groupe d’utilisateurs de deux manières :

### Section Utilisateurs

Les administrateurs peuvent utiliser les jeux d’inclusion et d’exclusion pour ajouter ou supprimer des utilisateurs ou des groupes d’utilisateurs dans la section Utilisateurs.

* **Jeux d&#39;inclusion** ajoutent des utilisateurs à un groupe d&#39;utilisateurs personnalisé. Vous pouvez inclure un ou plusieurs groupes d’utilisateurs, et Adobe Learning Manager utilise la logique (ET/OU) pour décider quel utilisateur inclure. Reportez-vous à cette [section](#_Inclusion_and_exclusion) pour en savoir plus sur la logique ET/OU.
* **Les jeux d&#39;exclusion** suppriment des utilisateurs du groupe, même s&#39;ils faisaient partie du jeu d&#39;inclusion. La liste des utilisateurs du groupe est ainsi affinée.

Pour ajouter des utilisateurs au groupe :

1. Recherchez et sélectionnez des utilisateurs ou un groupe d&#39;utilisateurs existant dans le champ **Inclure des élèves**.

![](assets/add-users-using-users.png)
_Paramètres d&#39;inclusion pour ajouter des utilisateurs ou des groupes spécifiques à un groupe d&#39;utilisateurs personnalisé_

### Section ID de messagerie

1. Saisissez les adresses e-mail des utilisateurs au format point-virgule, point-virgule ou saut de ligne pour ajouter les utilisateurs au groupe.

2. Sélectionnez **Valider Les Id De Messagerie**.

   ![](assets/validate-email.png)
   _Sélectionnez Valider les ID de messagerie pour valider les ID de messagerie saisis_

   Une erreur s’affiche si Adobe Learning Manager ne dispose pas de l’ID de messagerie ou si l’ID de messagerie est incorrect.

   ![](assets/add-user-using-email-id.png)
   _Champ permettant de saisir plusieurs adresses e-mail manuellement pour ajouter des utilisateurs à un groupe_

3. Sélectionnez **Enregistrer** pour créer le groupe.

## Exclure des utilisateurs du groupe

Les administrateurs peuvent exclure des utilisateurs spécifiques d’un groupe d’utilisateurs même s’ils répondent aux critères du groupe. Cela est utile lorsque vous souhaitez faire des exceptions, par exemple empêcher certains utilisateurs de recevoir des cours attribués ou d&#39;apparaître dans des rapports liés à ce groupe.

Pour exclure des utilisateurs spécifiques ou des groupes d’utilisateurs entiers lors de la création d’un groupe d’utilisateurs personnalisé :

1. Sélectionnez n&#39;importe quel **groupe d&#39;utilisateurs**, puis sélectionnez **Ajouter**.
2. Accédez à la section **Exclure des élèves**.
3. Sélectionnez les utilisateurs ou les groupes à exclure.

![](assets/exclude-learner.png)
_Paramètres d&#39;exclusion pour supprimer des utilisateurs ou des groupes d&#39;un groupe personnalisé_

## Afficher les membres du groupe

Les administrateurs peuvent afficher la liste des utilisateurs d’un groupe d’utilisateurs, y compris des détails tels que le nom, l’ID de messagerie et l’état. Pour afficher la liste des utilisateurs :

1. Sélectionnez **Utilisateurs**, puis **Groupes d’utilisateurs**.
2. Sélectionnez un groupe, puis la valeur dans le **Non. de la colonne Personnes**.

![](assets/view-group-members.png)
_Liste des utilisateurs actuellement inclus dans un groupe d&#39;utilisateurs sélectionné_

![](assets/no-of-people.png)
_Liste des utilisateurs disponibles dans le groupe d&#39;utilisateurs sélectionné_

## Télécharger les membres du groupe

Les administrateurs peuvent télécharger une liste des membres du groupe pour consulter les détails des utilisateurs, notamment le nom, l’adresse e-mail, le statut, la date d’ajout (fuseau horaire UTC), la date de suppression (fuseau horaire UTC) et la date de la dernière connexion (fuseau horaire UTC). Cela aide au suivi, au reporting et à l’audit de l’appartenance au groupe.

1. Sélectionnez **Utilisateurs**, puis **Groupes d’utilisateurs**.
2. Sélectionnez l’icône de téléchargement en regard d’un groupe pour exporter le rapport sous forme de fichier CSV.

![](assets/download-group-members.png)
_Icône de téléchargement pour exporter les données des membres du groupe sous forme de fichier CSV_

Voici les colonnes du rapport des membres du groupe :

* **Nom** : nom de l&#39;utilisateur
* **Adresse électronique** : ID de messagerie de l&#39;utilisateur
* **État** : état de l&#39;utilisateur (inscrit ou non inscrit).
* **Date ajoutée (fuseau horaire UTC)** : date à laquelle l’utilisateur a été ajouté dans le fuseau horaire UTC.
* **Date de suppression (fuseau horaire UTC)** : date à laquelle l’utilisateur a été supprimé dans le fuseau horaire UTC.
* **Date de la dernière connexion (fuseau horaire UTC)** : date de la dernière connexion de l’utilisateur au fuseau horaire UTC.

![](assets/csv-sample-download-ug.png)
_Exemple de fichier CSV contenant les détails de l’utilisateur_

## Modification d’un groupe d’utilisateurs

Les administrateurs peuvent modifier le nom, la description ou d’autres détails d’un groupe.

Pour modifier un groupe d’utilisateurs :

1. Sélectionnez **Utilisateurs** sur la page d&#39;accueil de l&#39;administrateur.
2. Sélectionnez **Groupes d&#39;utilisateurs**.
3. Sélectionnez le groupe d’utilisateurs que vous souhaitez modifier.
4. Effectuez les modifications nécessaires, telles que la mise à jour du nom, de la description ou d’autres détails.
5. Sélectionnez **Enregistrer** pour appliquer les modifications. Les modifications seront appliquées au groupe d’utilisateurs.

![](assets/edit-a-group.png)
_Champs pour modifier le nom, la description ou les règles d&#39;appartenance du groupe d&#39;utilisateurs_

## Suppression d’un groupe d’utilisateurs

Les administrateurs peuvent supprimer les groupes d’utilisateurs qui ne sont plus nécessaires pour que la liste des groupes reste organisée et à jour.

Pour supprimer un groupe d’utilisateurs :

1. Sélectionnez **Utilisateurs**, puis **Groupes d’utilisateurs**.
2. Sélectionnez le groupe à supprimer.
3. Sélectionnez **Actions**, puis **Supprimer**.

   ![](assets/delete-a-group.png)
   _Option Supprimer dans le menu Actions pour supprimer un groupe d&#39;utilisateurs_

4. Confirmez la suppression lorsque vous y êtes invité. Le groupe d’utilisateurs sera supprimé.

## Télécharger le rapport de groupe d’utilisateurs

Les rapports de groupes d’utilisateurs de Adobe Learning Manager fournissent aux administrateurs et aux responsables des informations sur les performances des différents groupes d’utilisateurs, tels que les services, les rôles ou les partenaires externes. Ces rapports permettent de comparer les groupes afin d’évaluer la progression de l’apprentissage, les taux d’achèvement des cours et les niveaux d’engagement.

Pour télécharger le rapport :

1. Sélectionnez **Utilisateurs**, puis **Groupes d’utilisateurs**.
2. Sélectionnez **Actions**, puis **Télécharger le rapport de groupe d&#39;utilisateurs**.

![](assets/download-user-group.png)
_Option permettant de télécharger des informations et des métadonnées au niveau du groupe à partir du menu Actions_

Ce rapport comprend :

| Colonne | Description |
|---|---|
| Type de groupe d’utilisateurs | Catégorie du groupe d’utilisateurs, telle que groupe généré automatiquement ou groupe personnalisé. |
| Nom | Nom attribué au groupe d’utilisateurs. |
| Description | Brève explication de l’objectif ou de la portée du groupe d’utilisateurs. |
| Créé par (nom) | Nom complet de l’administrateur qui a créé le groupe. |
| Créé par (adresse e-mail) | Adresse e-mail de l’administrateur qui a créé le groupe. |
| Créé le (fuseau horaire UTC) | Date et heure de création du groupe, affichées en temps universel coordonné (UTC). |
| Nombre d’utilisateurs | Nombre total d’utilisateurs actuellement inclus dans le groupe. |

![](assets/user-group-report.png)
_Le rapport de groupe d&#39;utilisateurs contient tous les champs_

## Règles d’inclusion et d’exclusion pour la création de groupes d’utilisateurs personnalisés

Lors de la création d&#39;un **groupe d&#39;utilisateurs personnalisé** en ajoutant des groupes d&#39;utilisateurs générés automatiquement ou existants, Adobe Learning Manager applique des **règles d&#39;inclusion et d&#39;exclusion** spécifiques basées sur la **logique ET/OU**. Ces règles dépendent de la manière dont les groupes d’utilisateurs sont combinés dans les jeux d’inclusion et d’exclusion.

Vous pouvez ajouter un ou plusieurs groupes d’utilisateurs générés automatiquement au jeu d’inclusion. La logique appliquée dépend de la façon dont vous sélectionnez ces groupes :

### Utilisation de la logique AND dans les groupes d’utilisateurs

Si vous sélectionnez plusieurs groupes d&#39;utilisateurs dans le même jeu d&#39;inclusion, les utilisateurs doivent remplir toutes les conditions pour être inclus.

Par exemple,

* Groupe de l’équipe commerciale : 120 utilisateurs
* Location (Bangalore) groupe : 80 utilisateurs
* Utilisateurs courants dans les **deux** groupes : 40 utilisateurs

Adobe Learning Manager utilise la logique AND pour créer un groupe de 40 utilisateurs seulement. Ces utilisateurs font partie de l&#39;équipe commerciale et sont également situés à Bangalore, répondant aux deux conditions.

![](assets/and-logic.png)
_Exemple d&#39;affichage de plusieurs groupes combinés à l&#39;aide de la logique AND_

### Utilisation de la logique OR dans les groupes d’utilisateurs

Si vous ajoutez des groupes d’utilisateurs dans des jeux d’inclusion distincts, les utilisateurs répondant à toutes les conditions sont inclus. Par exemple :

* Groupe de l’équipe commerciale : 120 utilisateurs
* Location (Bangalore) groupe : 80 utilisateurs
* Nombre total d’utilisateurs dans chaque groupe : 160 utilisateurs (certains utilisateurs peuvent appartenir aux deux groupes)

Lorsque vous utilisez la logique OR, Adobe Learning Manager ajoute les utilisateurs qui font partie de l’équipe commerciale ou qui se trouvent à Bangalore. Cela signifie qu’il inclut les utilisateurs qui répondent à l’une des deux conditions. Par conséquent, le groupe comprend 160 utilisateurs après la suppression des doublons.

![](assets/or-logic.png)
_Exemple d&#39;affichage de plusieurs groupes combinés à l&#39;aide de la logique OR_
