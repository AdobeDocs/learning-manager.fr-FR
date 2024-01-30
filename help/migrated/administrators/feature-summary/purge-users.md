---
description: En savoir plus sur la fonction qui permet de purger les données utilisateur dans Learning Manager.
jcr-language: en_us
title: Purger les utilisateurs
contentowner: dvenkate
source-git-commit: 53c1a5283295b56424d697bc26c5db31c2edca0f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 75%

---



# Purger les utilisateurs

En savoir plus sur la fonction qui permet de purger les données utilisateur dans Learning Manager.

## Vue d’ensemble {#overview}

Utilisez la fonction Purger l’utilisateur pour supprimer les informations personnelles identifiables et les dossiers d’apprentissage de l’utilisateur sur Learning Manager. Notez que Supprimer et Purger l’utilisateur sont deux fonctions différentes. Alors qu’un utilisateur supprimé peut être récupéré, ce n’est pas le cas de toutes les données d’utilisateur et de tous les dossiers d’apprentissage associés à un utilisateur purgé.

Une action Purger l’utilisateur peut avoir les conséquences suivantes :

* Si un utilisateur est purgé, les liens dans les journaux d’importation ne fonctionnent pas pour éviter le téléchargement d’anciens fichiers CSV et le retour des données utilisateur dans le système.
* Si un auteur est purgé, son nom est remplacé par le nom de l’administrateur qui l’a purgé.
* Si des instructeurs sont purgés, ils sont supprimés des sessions. L’administrateur doit remplacer/ajouter des instructeurs pour ces sessions.
* Purger un utilisateur dans Learning Manager ne supprime pas l’utilisateur dans d’autres applications externes (systèmes tiers ou autres applications que vous avez écrites). Contactez les propriétaires des applications externes pour obtenir la suppression des utilisateurs dans ces applications.
* Si un utilisateur purgé est référencé dans les paramètres de configuration d’un connecteur, ce dernier est désactivé. Le connecteur doit être reconfiguré par l’administrateur pour reprendre.

Pour purger les utilisateurs, procédez comme suit :

1. En tant qu’administrateur, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de gauche. La page **[!UICONTROL Utilisateurs internes]** s’ouvre.
1. Supprimez l’utilisateur que vous souhaitez purger. Pour cela, sélectionnez un ou plusieurs utilisateurs à l’aide de la case à cocher. Ouvrez le panneau **[!UICONTROL Action]** liste déroulante et sélectionnez **[!UICONTROL Supprimer l’utilisateur.]**
1. Dans le volet de gauche, sélectionnez **[!UICONTROL Suppression de l’utilisateur]**. La page **[!UICONTROL Suppression de l’utilisateur]** apparaît avec la liste des utilisateurs supprimés. Utilisez les boutons radio pour sélectionner l’utilisateur à purger. Vous ne pouvez purger qu’un utilisateur à la fois.

   ![](assets/purge-1.png)

   *Sélectionner un utilisateur à purger*

1. Ouvrez le panneau **[!UICONTROL Actions]** menu déroulant et sélectionnez **[!UICONTROL Purger l’utilisateur]**.

   ![](assets/purge-2.png)

   *Sélectionnez l’option Purger l’utilisateur*

1. Une boîte de dialogue s’affiche vous demandant une confirmation. Une fois purgés, toutes les données d’utilisateur et les dossiers d’apprentissage associés à l’utilisateur sélectionné sont supprimés de façon permanente. Une fois effectuée, l’action de purge est irréversible. Pour confirmer, cliquez sur **[!UICONTROL Purger]**.

   ![](assets/purge-3.png)

   *Message de confirmation après la purge d’un utilisateur*

1. Une fois que vous confirmez et cliquez sur Purger, la demande de purge est acceptée. Vous recevez une notification une fois l’action terminée. Un ID de demande de purge est également fourni. Vous pouvez fournir cet ID au CSM pour effectuer le suivi de la demande.

## Purge en bloc d’utilisateurs

Vous pouvez sélectionner les 50 premiers utilisateurs et purger les utilisateurs en une seule opération. Cela permet aux administrateurs de sélectionner 50 utilisateurs à la fois et de les purger. Cela aide les administrateurs lorsqu&#39;ils souhaitent purger en bloc les utilisateurs. Il est toujours recommandé de vérifier les utilisateurs sélectionnés pour la purge. Il est important de s&#39;assurer que seul le groupe d&#39;utilisateurs approprié est purgé.

![](assets/bulk-purge-users.png)

*Purger les utilisateurs en bloc*

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
   <td><strong>Purger</strong> <strong>autres utilisateurs - Particuliers (personnes qui ne sont pas des utilisateurs internes ou externes de Learning Manager)</strong></td>
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
   <td>Avertir l’administrateur de l’entreprise de la demande.</td>
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

Learning Manager est désormais conforme au RGPD. Pour plus d’informations sur la conformité au RGPD, voir  [Conformité de Learning Manager au RGPD](../../kb/prime-gdpr.md).

## Forum aux questions {#frequentlyaskedquestions}

+++Combien de jours faut-il pour qu’une demande de purge soit terminée ?

Une demande de purge d’utilisateurs prend un maximum de 30 jours.
+++

+++Pouvez-vous effectuer une purge en bloc dans Learning Manager ?

Oui, vous pouvez effectuer une purge en bloc. Cependant, vous pouvez effectuer une purge en bloc de 50 utilisateurs uniquement.
+++
