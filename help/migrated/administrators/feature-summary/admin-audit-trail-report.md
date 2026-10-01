---
description: Découvrez comment le rapport de piste d’audit de l’administrateur suit les modifications de configuration, en indiquant qui les a effectuées, quand et les valeurs avant et après.
jcr-language: en_us
title: Rapport de piste d’audit de l’administrateur
exl-id: 71b2ee42-ef1c-47fb-95ad-c339562e227d
source-git-commit: 500a467395fc8ada89cd6ea7e3783b73cc43045d
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%
---

# Rapport de piste d’audit de l’administrateur {#adminaudittrailreport}

Générez un rapport des modifications de configuration apportées aux paramètres de base, avancés et d’intégration de votre compte, y compris qui a effectué chaque modification, quand et la valeur avant et après.

## Éléments capturés par le rapport

Le rapport de piste d’audit de l’administrateur vous fournit un enregistrement historique des modifications de configuration afin que vous puissiez déterminer :

- Qui a apporté la modification ?
- Date de la modification
- Définition du paramètre avant la modification
- Définition du paramètre après la modification

Le rapport couvre les modifications apportées à :

- Paramètres **de base**
- Paramètres **avancés**
- Paramètres des **intégrations**

Le rapport est cumulatif uniquement : de nouveaux enregistrements de modification sont ajoutés au fil du temps et les entrées précédemment enregistrées ne sont jamais supprimées. Cela vous permet de passer en revue l’historique complet d’un paramètre sur plusieurs modifications, et pas seulement sa valeur actuelle.

Le rapport est disponible pour tout utilisateur disposant de privilèges de rapport et d’un accès complet au groupe d’utilisateurs. Cela inclut les administrateurs complets et les administrateurs personnalisés qui ont obtenu l’accès aux rapports.

>[!NOTE]
>
>Les dossiers sont disponibles à partir de la mise à jour 112, septembre 2026. Les modifications apportées avant cette mise à jour ne sont pas incluses dans le rapport. Voir [notes de mise à jour](/help/migrated/release-note/release-notes.md) Mise à jour 112.

## Pourquoi ce rapport est important pour la conformité

Les entreprises opérant dans des secteurs réglementés doivent souvent démontrer que les modifications de configuration apportées aux systèmes de traitement des enregistrements électroniques sont suivies, attribuables et conservées. Le rapport de piste d&#39;audit de l&#39;administrateur prend en charge ces exigences en identifiant la personne, le paramètre, l&#39;heure et les valeurs avant et après pour chaque modification.

>[!NOTE]
>
>Ce rapport soutient les activités de conformité de votre organisation. Elle ne certifie pas, à elle seule, le respect d&#39;un règlement ou d&#39;une norme spécifique.

## Générer un rapport de piste d&#39;audit d&#39;administrateur

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Dans la navigation de gauche, sélectionnez **Gérer** > **Rapports** > **Rapports personnalisés**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report1.png)

3. Faites défiler vers le bas et sélectionnez **Piste d&#39;audit de l&#39;administrateur**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report2.png)

4. **Sélectionner la plage** : choisissez la période sur laquelle effectuer le rapport : **Dernière semaine**, **Dernier mois** ou **Choisir des dates**. Si vous sélectionnez **Choisir des dates**, entrez une date **De** et une date **À**.
5. **Sélectionner le type de paramètre** : choisissez **Sélectionner tout**, **Principes de base**, **Intégrations** ou **Avancé**.

   Pour afficher la liste complète des paramètres suivis par ce rapport dans les catégories Principes de base, Intégrations et Avancé, sélectionnez **Télécharger la liste des paramètres**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report6.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report3.png)

6. Sélectionnez **Générer**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report4.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report5.png)

Un fichier `.csv` contenant les modifications est téléchargé dans le dossier Téléchargements de votre navigateur. La génération du rapport peut prendre quelques instants. Vous pouvez continuer à utiliser Adobe Learning Manager pendant le traitement. Si vous fermez la fenêtre du navigateur avant que le rapport ne soit prêt, le téléchargement commencera la prochaine fois que vous vous connecterez.

## Utilisations courantes de ce rapport

- **Recherchez une modification de paramètre inattendue** : confirmez ce qui a changé, quand et qui a effectué la modification, plutôt que de vous fier à des hypothèses.
- **Examiner les modifications apportées par plusieurs administrateurs** : générez une vue consolidée de toutes les activités de configuration qui sont dans la portée du rapport pour une période donnée, au lieu de contacter chaque administrateur individuellement.
- **Confirmer une modification de configuration approuvée** — Vérifiez que l&#39;administrateur prévu a effectué la modification dans le délai prévu et que la nouvelle valeur correspond à ce qui a été approuvé.
- **Comparez l&#39;historique d&#39;un paramètre sur plusieurs modifications** : utilisez la colonne **Révision** pour voir combien de fois un paramètre spécifique a été modifié et passez en revue chaque valeur enregistrée dans l&#39;ordre, y compris si une modification ultérieure a restauré une valeur antérieure.
- **Prendre en charge un examen de conformité** : générez le rapport pour la période examinée dans le cadre de vos enregistrements administratifs et de conformité.
- **Passer en revue les paramètres après un changement de stratégie** — Confirmez que les mises à jour de configuration prévues ont été appliquées de manière cohérente et identifiez toutes les modifications survenues de manière inattendue.
- **Tenir à jour un enregistrement administratif historique** : téléchargez et conservez les rapports conformément aux pratiques de gestion des enregistrements de votre organisation.

## Référence de colonne de rapport

Le fichier `.csv` téléchargé comprend les colonnes suivantes.

| Colonne | Description |
|---|---|
| **ID d&#39;événement** | Identifiant unique pour cet enregistrement de modification spécifique. |
| **Horodatage (UTC)** | Date et heure de la modification, en temps universel coordonné. |
| **Courrier électronique** | Adresse e-mail de l’administrateur qui a apporté la modification. |
| **UUID** | Identifiant unique pour l’administrateur qui a effectué la modification. Renseigné uniquement si l’UUID est activé au niveau du compte. |
| **Nom de l&#39;administrateur** | Nom d&#39;affichage de l&#39;administrateur qui a apporté la modification. |
| **Type d&#39;événement** | Catégorie de l&#39;événement enregistré, par exemple `Modify`, `Create` ou `Delete`. |
| **Type d&#39;action** | Type d&#39;action effectuée sur le paramètre, par exemple, `CREATE_SETTING`, `UPDATE_SETTING` ou `DELETE_SETTING`. |
| **Type d&#39;objet** | Objet de configuration ou de paramètre modifié. |
| **ID d&#39;objet** | Identifiant unique de l&#39;objet paramètre ou configuration spécifique qui a été modifié. |
| **Valeur précédente** | Valeur du paramètre avant la modification. (Pour un paramètre supprimé, cela indique la valeur qui existait avant la suppression.) |
| **Nouvelle valeur** | Valeur du paramètre après la modification. (Pour un paramètre supprimé, ce champ est vide.) |
| **Révision** | Nombre de modifications apportées à cet ID d&#39;objet spécifique lors de l&#39;enregistrement de l&#39;événement. La première modification enregistrée pour un objet commence à 1. |

>[!TIP]
>
>Pour trouver tous les paramètres supprimés au cours d&#39;une période, filtrez le fichier téléchargé dont le **type d&#39;action** est `DELETE_SETTING`.

## Accéder à ce rapport par programme

Vous pouvez récupérer le rapport de piste d’audit d’administrateur par programme à l’aide de l’API des tâches, plutôt que de le générer manuellement à partir de l’application d’administration. Ceci est utile si vous souhaitez planifier des exportations régulières ou alimenter le rapport dans un système de surveillance ou d’alerte en aval. Voir [Rapport de piste d&#39;audit d&#39;administrateur d&#39;API de travaux](/help/migrated/api-changes-sep-2026.md#job-api-for-admin-audit-trail-report).

## Limitations

- **Localisation** : le contenu du rapport n&#39;est pas localisé. Le rapport est généré dans la langue par défaut du compte, quels que soient les paramètres régionaux configurés de votre compte.
- **Motif de la modification** : le rapport ne saisit pas la raison pour laquelle une modification a été apportée. Conservez séparément toute demande de modification, approbation ou justification commerciale associée.

## Bonnes pratiques

- Sélectionnez une plage de dates qui couvre la modification suspectée ou prévue.
- Sélectionnez **Tout sélectionner** lorsque la zone des paramètres affectés n&#39;est pas connue.
- Comparez les colonnes **Valeur précédente** et **Nouvelle valeur** pour chaque entrée.
- Utilisez les colonnes **Nom de l&#39;administrateur** et **Horodatage** pour corréler une modification avec le travail approuvé ou les enregistrements internes.
- Conservez séparément la demande de modification, l&#39;approbation ou la justification commerciale associée lorsque votre organisation exige une explication documentée pour une modification.

## Dépannage

**Je ne vois aucun enregistrement avant une certaine date**
Les enregistrements sont disponibles uniquement à partir de la mise à jour 112 (septembre 2026). Les modifications apportées avant cette mise à jour ne sont pas incluses dans le rapport. Voir [notes de mise à jour](/help/migrated/release-note/release-notes.md)

**La colonne UUID est vide pour tout ou partie des enregistrements**
La colonne UUID est remplie uniquement si l’UUID est activé au niveau du compte. Si elle n’est pas activée, cette colonne n’est pas présente.

**J&#39;ai un rôle d&#39;administrateur personnalisé, mais je ne trouve pas ce rapport**
Confirmez que votre rôle personnalisé dispose de privilèges de rapport et d’un accès complet au groupe d’utilisateurs. Contactez le propriétaire de votre compte ou un administrateur complet pour demander cet accès si nécessaire.
