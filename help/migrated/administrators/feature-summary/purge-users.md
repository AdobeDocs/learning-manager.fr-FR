---
description: En savoir plus sur la fonction qui permet de purger les données utilisateur dans Learning Manager.
jcr-language: en_us
title: Purger les utilisateurs
contentowner: dvenkate
exl-id: 4449146c-6247-44fb-b695-a12023c31dc6
source-git-commit: 7c21986eff480f15cb788cf9a1cb51644bc083c8
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 52%

---

# Purger les utilisateurs

En savoir plus sur la fonction qui permet de purger les données utilisateur dans Learning Manager.

## Vue d’ensemble {#overview}

Utilisez la fonction Purger l’utilisateur pour supprimer les informations personnelles identifiables et les dossiers d’apprentissage de l’utilisateur sur Learning Manager. Notez que Supprimer et Purger l’utilisateur sont deux fonctions différentes. Alors qu’un utilisateur supprimé peut être récupéré, ce n’est pas le cas de toutes les données d’utilisateur et de tous les dossiers d’apprentissage associés à un utilisateur purgé.

Une action Purger l’utilisateur peut avoir les conséquences suivantes :

* Si un utilisateur est purgé, les liens dans les journaux d’importation ne fonctionnent pas pour éviter le téléchargement d’anciens fichiers CSV et le retour des données utilisateur dans le système.
* Si un auteur est purgé, son nom est remplacé par le nom de l’administrateur qui a purgé cet utilisateur.
* Si des instructeurs sont purgés, ils sont supprimés des sessions. L’administrateur doit remplacer/ajouter des instructeurs pour ces sessions.
* Purger un utilisateur dans Learning Manager ne supprime pas l’utilisateur dans d’autres applications externes (systèmes tiers ou autres applications que vous avez écrites). Contactez les propriétaires des applications externes pour obtenir la suppression des utilisateurs dans ces applications.
* Si un utilisateur purgé est référencé dans les paramètres de configuration d’un connecteur, ce dernier est désactivé. L&#39;administrateur doit reconfigurer le connecteur pour reprendre.

<!---### Manage users

In this training, you will learn how to assign and remove roles, send a welcome email, and delete and purge users. 

[![button](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&sdid=4X3B8VJ2&mv=display&mv2=display#/course/7555586)

If you're unable to launch the training, write to <almacademy@adobe.com>.-->

## Comment purger les utilisateurs

Pour purger les utilisateurs, procédez comme suit :

1. En tant qu’administrateur, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de gauche. La page **[!UICONTROL Utilisateurs internes]** s’ouvre.
1. Supprimez l’utilisateur que vous souhaitez purger. Pour cela, sélectionnez un ou plusieurs utilisateurs à l’aide de la case à cocher. Ouvrez la liste déroulante **[!UICONTROL Action]** et sélectionnez **[!UICONTROL Supprimer l’utilisateur]**.
1. Dans le volet de gauche, sélectionnez **[!UICONTROL Suppression de l’utilisateur]**. La page **[!UICONTROL Suppression de l’utilisateur]** apparaît avec la liste des utilisateurs supprimés. Utilisez les boutons radio pour sélectionner l’utilisateur à purger. Vous ne pouvez purger qu’un utilisateur à la fois.

   ![](assets/purge-1.png)

   *Sélectionner un utilisateur à purger*

1. Ouvrez le menu déroulant **[!UICONTROL Actions]** et sélectionnez **[!UICONTROL Purger l&#39;utilisateur]**.

   ![](assets/purge-2.png)

   *Sélectionnez l&#39;option Purger l&#39;utilisateur*

1. Une boîte de dialogue s’affiche vous demandant une confirmation. Une fois purgés, toutes les données d’utilisateur et les dossiers d’apprentissage associés à l’utilisateur sélectionné sont supprimés de façon permanente. Une fois effectuée, l’action de purge est irréversible. Pour confirmer, cliquez sur **[!UICONTROL Purger]**.

   ![](assets/purge-3.png)

   *Message de confirmation après la purge d&#39;un utilisateur*

1. Une fois que vous confirmez et cliquez sur Purger, la demande de purge est acceptée. Vous recevez une notification une fois l’action terminée. Un ID de demande de purge est également fourni. Vous pouvez fournir cet ID au CSM pour effectuer le suivi de la demande.

>[!NOTE]
>
>Une fois l’utilisateur supprimé ajouté à nouveau au système, les rôles précédents (par exemple, Administrateur, Responsable, Auteur, Instructeur, etc.) ne sont pas conservés. Ils sont ajoutés avec le rôle d’élève.

## Purge en bloc d’utilisateurs

Vous pouvez sélectionner les 50 premiers utilisateurs et purger les utilisateurs en une seule opération. Cela permet aux administrateurs de sélectionner 50 utilisateurs à la fois et de les purger ensemble. Cela aide les administrateurs lorsqu’ils souhaitent purger en bloc les utilisateurs. Il est toujours recommandé de vérifier les utilisateurs sélectionnés pour la purge. Il est important de s&#39;assurer que seul le groupe d&#39;utilisateurs approprié est purgé.

![](assets/bulk-purge-users.png)

*Purger les utilisateurs en bloc*

## Filtrage des utilisateurs supprimés avant la purge

Adobe Learning Manager permet aux administrateurs de supprimer définitivement des utilisateurs qui ont déjà été supprimés de la plateforme. Ce processus, appelé purge, aide les organisations à maintenir une base de données d’élèves propre, à se conformer aux politiques de conservation des données et à empêcher tout accès non autorisé aux données utilisateur.
Ceci est particulièrement utile pour maintenir l&#39;hygiène des données et s&#39;assurer que les anciennes données utilisateur inutilisées sont supprimées du système.
La purge des utilisateurs est essentielle pour se conformer aux directives de confidentialité des données ou pour maintenir un magasin de données assaini en supprimant les enregistrements redondants.

### Filtrer les utilisateurs supprimés par mois

Vous pouvez filtrer les utilisateurs supprimés en sélectionnant un mois spécifique, puis les supprimer définitivement.

Pour filtrer les utilisateurs supprimés à l’aide du mois de suppression :

1. Sélectionnez **[!UICONTROL Utilisateurs]** dans la page d&#39;accueil de l&#39;administrateur, puis sélectionnez **[!UICONTROL Nettoyage de l&#39;utilisateur]**.
2. Sélectionnez le sélecteur de dates **[!UICONTROL Sélectionner le mois de suppression]** et sélectionnez la date.

   ![](assets/deletion-date.png)
   _Sélectionner le mois où les utilisateurs ont été supprimés_

   La liste des utilisateurs supprimés dans le mois sélectionné s’affiche.

   ![](assets/list-of-user-deleted.png)
   _Liste des utilisateurs supprimés affichée pour le mois sélectionné_

### Trier les utilisateurs supprimés par mois

Vous pouvez trier les utilisateurs filtrés par **[!UICONTROL ID d’utilisateur unique]** et **[!UICONTROL Date de suppression]**.

1. Dans la liste des utilisateurs supprimés, triez les utilisateurs en fonction de leur ID utilisateur ou de leur date de suppression.

   ![](assets/sort-by-date.png)
   _Liste d&#39;utilisateurs filtrée par ID utilisateur unique_

2. Sélectionnez un ou plusieurs utilisateurs.
3. Sélectionnez **[!UICONTROL Actions]**, puis **[!UICONTROL Purger l’utilisateur]**.
4. Sélectionnez Purger dans le message de confirmation pour supprimer définitivement les enregistrements utilisateur de Adobe Learning Manager.

   ![](assets/select-purge.png)
   _Confirmation finale avant de purger définitivement les utilisateurs_

>[!NOTE]
>
>La purge des utilisateurs supprime définitivement leurs données. Vérifiez votre sélection avant de continuer.

+++En savoir plus sur les résultats de l’action Purger l’utilisateur

<table>
 <tbody>
  <tr>
   <th><strong>Purger à l’aide de l’interface utilisateur de Learning Manager : Entreprise</strong></th>
   <th> </th>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné du compte de l’entreprise demandeuse.<br></td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer tous les utilisateurs de tous les comptes d’essai dont l’adresse électronique, adobe_id correspond à l’adresse électronique des utilisateurs sélectionnés.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer tous les utilisateurs de tous les comptes d’essai dont l’adresse électronique, adobe_id correspond à l’adresse électronique des utilisateurs sélectionnés et qui sont les créateurs du compte d’essai.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Supprimez l’adresse e-mail de l’utilisateur de tous les autres champs du compte d’entreprise et de tous les comptes d’évaluation demandeurs.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Avertir l’initiateur de la confirmation de suppression.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger à l’aide de l’interface utilisateur de Learning Manager - Particulier</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné du compte d’essai demandeur.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer tous les utilisateurs de tous les comptes d’essai dont l’adresse électronique, adobe_id correspond à l’adresse électronique des utilisateurs sélectionnés.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer tous les utilisateurs de tous les comptes d’essai dont l’adresse électronique, adobe_id correspond à l’adresse électronique des utilisateurs sélectionnés et qui sont les créateurs du compte d’essai.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Supprimez l’adresse e-mail de l’utilisateur de tous les autres champs de tous les comptes d’évaluation.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Avertir l’initiateur de la confirmation de suppression.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger d’autres utilisateurs - Entreprise (personnes qui ne sont pas des utilisateurs internes ou externes de Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné de tous les autres champs du compte de l’entreprise demandeuse et de tous les comptes d’essai.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur des comptes.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Avertir l’initiateur de la confirmation de suppression. </td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger</strong> <strong>d’autres utilisateurs hors entreprise (personnes qui ne sont pas des utilisateurs internes ou externes de Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné de tous les autres champs de tous les comptes d’essai.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur des comptes.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Avertir l’initiateur de la confirmation de suppression.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger à l’aide d’Adobe IMS - Entreprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Informez l’administrateur Enterprise de la demande.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Cocher les champs Adresse électronique pour envoyer des notifications.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td><strong>Purger à l’aide d’Adobe IMS - Particulier</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer tous les utilisateurs avec les ID/adresses électroniques Adobe fournis de tous les comptes d’essai.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer tous les utilisateurs d’un compte d’essai si l’adresse électronique/ID Adobe a été le créateur du compte.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimer l’ID d’adresse électronique sélectionné de tous les autres champs de tous les comptes d’essai.</td>
   <td>Oui</td>
  </tr>
 </tbody>
</table>

+++

## Forum aux questions {#frequentlyaskedquestions}

+++Combien de jours faut-il pour qu’une demande de purge soit terminée ?

Une demande de purge d’utilisateurs prend un maximum de 30 jours.
+++

+++Pouvez-vous effectuer une purge en bloc dans Adobe Learning Manager ?

Oui, vous pouvez effectuer une purge en bloc. Cependant, vous pouvez effectuer une purge en bloc de 50 utilisateurs uniquement.
+++

+++ Puis-je restaurer un utilisateur purgé ?

Non. Une fois vidées, toutes les données utilisateur sont définitivement supprimées et ne peuvent pas être récupérées.

+++
