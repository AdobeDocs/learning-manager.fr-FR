---
description: En savoir plus sur la purge des données utilisateur dans Learning Manager.
jcr-language: en_us
title: Purger les utilisateurs
contentowner: dvenkate
source-git-commit: 53c1a5283295b56424d697bc26c5db31c2edca0f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---



# Purger les utilisateurs

En savoir plus sur la purge des données utilisateur dans Learning Manager.

## Présentation {#overview}

Utilisez la fonctionnalité Purger l’utilisateur pour supprimer les informations personnelles identifiables et les dossiers d’apprentissage de l’utilisateur de Learning Manager. Notez que Supprimer et Purger l’utilisateur sont deux fonctionnalités différentes. Bien qu&#39;un utilisateur supprimé puisse être restauré, toutes les données utilisateur et tous les dossiers d&#39;apprentissage associés à un utilisateur purgé ne peuvent pas être restaurés.

L’action Purger l’utilisateur peut avoir les résultats suivants :

* Si un utilisateur est purgé, les liens dans les journaux d’importation ne fonctionnent pas pour éviter le téléchargement d’anciens fichiers CSV et le retour des données utilisateur dans le système.
* Si un auteur est purgé, son nom est remplacé par le nom de l’administrateur qui a purgé cet utilisateur.
* Si les instructeurs sont purgés, ils sont supprimés des sessions. L’administrateur doit remplacer/ajouter des instructeurs pour ces sessions.
* La purge d’un utilisateur dans Learning Manager ne le supprime pas de toutes les applications externes (systèmes tiers ou autres applications écrites par vous). Contactez les propriétaires d’applications externes pour supprimer les utilisateurs de ces applications.
* Si un utilisateur purgé est référencé dans les paramètres de configuration d&#39;un connecteur, le connecteur est désactivé. Le connecteur doit être reconfiguré par l’administrateur pour reprendre.

Pour purger les utilisateurs, procédez comme suit :

1. En tant qu’administrateur, sélectionnez **[!UICONTROL Utilisateurs]** dans le volet de gauche. Le **[!UICONTROL Utilisateurs internes]** la page s’ouvre.
1. Supprimez les utilisateurs à vider. Pour supprimer, sélectionnez un ou plusieurs utilisateurs à l’aide de la case à cocher. Ouvrez le panneau **[!UICONTROL Action]** liste déroulante et sélectionnez **[!UICONTROL Supprimer l’utilisateur.]**
1. Dans le volet de gauche, sélectionnez **[!UICONTROL Nettoyage de l’utilisateur]**. Le **[!UICONTROL Nettoyage de l’utilisateur]** s’affiche avec la liste des utilisateurs supprimés. Utilisez les boutons radio pour sélectionner l’utilisateur à purger. Vous ne pouvez purger qu’un seul utilisateur à la fois.

   ![](assets/purge-1.png)

   *Sélectionner un utilisateur à purger*

1. Ouvrez le panneau **[!UICONTROL Actions]** menu déroulant et sélectionnez **[!UICONTROL Purger l’utilisateur]**.

   ![](assets/purge-2.png)

   *Sélectionnez l’option Purger l’utilisateur*

1. Une boîte de dialogue s’affiche pour demander confirmation. Une fois vidés, toutes les données utilisateur et tous les enregistrements d’apprentissage associés à l’utilisateur sélectionné sont définitivement supprimés. Une fois la purge effectuée, l’action ne peut plus être annulée. Pour confirmer, cliquez sur **[!UICONTROL Purger]**.

   ![](assets/purge-3.png)

   *Message de confirmation après la purge d’un utilisateur*

1. Une fois que vous avez confirmé et cliqué sur Purger, la demande de purge est acceptée. Vous recevez une notification une fois l’action terminée. Un ID de demande de purge est également fourni. Vous pouvez fournir cet ID au CSM pour suivre la demande.

## Purge en bloc des utilisateurs

Vous pouvez sélectionner les 50 premiers utilisateurs et purger les utilisateurs en une seule prise. Cela permet aux administrateurs de sélectionner 50 utilisateurs à la fois et de les purger ensemble. Cela aide les administrateurs lorsqu’ils souhaitent purger en bloc les utilisateurs. Il est toujours recommandé de vérifier les utilisateurs sélectionnés pour la purge. Il est important de s’assurer que seul le groupe d’utilisateurs approprié est purgé.

![](assets/bulk-purge-users.png)

*Purger les utilisateurs en bloc*

+++En savoir plus sur les résultats de l’action Purger l’utilisateur

<table>
 <tbody>
  <tr>
   <th><strong>Purger à l’aide de l’interface utilisateur de Learning Manager - Entreprise</strong></th>
   <th> </th>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné du compte d’entreprise demandeur.<br></td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimez tous les utilisateurs de tous les comptes d’essai dont l’adresse e-mail, adobe_id correspond à l’adresse e-mail des utilisateurs sélectionnés.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimez tous les utilisateurs de tous les comptes d’évaluation dont l’adresse e-mail, adobe_id correspond à l’adresse e-mail des utilisateurs sélectionnés et qui sont les créateurs du compte d’évaluation.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Supprimez l’adresse e-mail de l’utilisateur de tous les autres champs du compte d’entreprise et de tous les comptes d’évaluation demandeurs.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Avertissez l’initiateur de la confirmation de suppression.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger à l’aide de l’interface utilisateur de Learning Manager - Particulier</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné du compte d’évaluation demandeur.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimez tous les utilisateurs de tous les comptes d’essai dont l’adresse e-mail, adobe_id correspond à l’adresse e-mail des utilisateurs sélectionnés.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimez tous les utilisateurs de tous les comptes d’évaluation dont l’adresse e-mail, adobe_id correspond à l’adresse e-mail des utilisateurs sélectionnés et qui sont les créateurs du compte d’évaluation.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Supprimez l’adresse e-mail de l’utilisateur de tous les autres champs de tous les comptes d’évaluation.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Avertissez l’initiateur de la confirmation de suppression.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger d’autres utilisateurs - Entreprise (personnes qui ne sont pas des utilisateurs internes ou externes de Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné de tous les autres champs du compte d’entreprise et de tous les comptes d’évaluation à l’origine de la demande.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Suppression de l’utilisateur des comptes.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Avertissez l’initiateur de la confirmation de suppression. </td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger</strong> <strong>autres utilisateurs - Particuliers (personnes qui ne sont pas des utilisateurs internes ou externes de Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimer l’utilisateur sélectionné de tous les autres champs de tous les comptes d’évaluation.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Suppression de l’utilisateur des comptes.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td>Avertissez l’initiateur de la confirmation de suppression.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td><strong>Purger à l’aide d’Adobe IMS - Entreprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Informez l’administrateur d’entreprise de la demande.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Vérifiez les champs E-mail pour l’envoi des notifications.</td>
   <td>Non</td>
  </tr>
  <tr>
   <td><strong>Purger à l’aide d’Adobe IMS - Particulier</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Supprimez tous les utilisateurs disposant de l’Adobe ID/de l’adresse e-mail fournie de tous les comptes d’évaluation.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimez tous les utilisateurs d’un compte d’évaluation si l’e-mail/l’AdobeId fourni était le créateur du compte.</td>
   <td>Oui</td>
  </tr>
  <tr>
   <td>Supprimez l’ID de messagerie sélectionné de tous les autres champs de tous les comptes d’évaluation.</td>
   <td>Oui</td>
  </tr>
 </tbody>
</table>

+++

Learning Manager est désormais conforme au RGPD. Pour plus d’informations sur la conformité au RGPD, voir  [Conformité de Learning Manager au RGPD](../../kb/prime-gdpr.md).

## Foire aux questions {#frequentlyaskedquestions}

+++Combien de jours faut-il pour qu’une demande de purge soit terminée ?

Une demande de purge des utilisateurs prend un maximum de 30 jours.
+++

+++Pouvez-vous effectuer une purge en bloc dans Learning Manager ?

Oui, vous pouvez effectuer une purge en bloc. Cependant, vous ne pouvez effectuer une purge en bloc que de 50 utilisateurs.
+++
