---
jcr-language: en_us
title: Soumettre un apprentissage externe dans Adobe Learning Manager
description: Les responsables peuvent examiner les demandes d’apprentissage externes soumises par les membres de leur équipe, vérifier les détails et tout justificatif d’accomplissement, et approuver ou rejeter chaque demande avec un commentaire facultatif. Les envois approuvés sont ajoutés au relevé de notes de l’élève.
contentowner: saghosh
source-git-commit: 2495d33fc1595bd962ba07988123e3563d4c69a0
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 1%

---


# Examiner les demandes d’apprentissage externes en tant que responsable

Lorsqu’un élève de votre équipe envoie une demande d’apprentissage externe dans Adobe Learning Manager, vous recevez une notification sur la plateforme. Vous pouvez consulter les détails de l’envoi, approuver ou rejeter la demande et ajouter un commentaire pour l’élève.

## Fonctionnement du processus de révision du responsable

Lorsqu’un élève soumet une demande d’apprentissage externe, les événements suivants se produisent :

1. Vous recevez une **notification dans l&#39;application** vous invitant à vérifier l&#39;envoi. L&#39;envoi apparaît dans l&#39;onglet **Apprentissage externe** sur votre tableau de bord de responsable.
2. Vous ouvrez une soumission, passez en revue tous les champs et tout document chargé comme preuve, puis sélectionnez **Approuver** ou **Rejeter**.
3. Vous pouvez ajouter un **commentaire de révision** que l’élève verra lorsqu’il recevra sa notification.
4. L&#39;élève reçoit une **notification sur la plateforme** avec votre décision.

Si vous approuvez une soumission, l&#39;activité d&#39;apprentissage externe est ajoutée au **relevé de notes de l&#39;élève administrateur** et apparaît dans l&#39;enregistrement du relevé de notes de l&#39;élève.

<!--You can also change a previously **Rejected** submission to **Approved** if the circumstances change.-->

## Réviser et approuver ou rejeter une soumission

1. Connectez-vous à Adobe Learning Manager en tant que responsable.

2. Sélectionnez **Apprentissage externe** dans le volet de navigation de gauche.

3. Dans la liste d&#39;envoi, sélectionnez la demande que vous souhaitez examiner. Les soumissions sont triées par date de soumission, la plus récente apparaissant en haut.

4. Passez en revue la soumission complète :

   - Titre, description, dates, durée et score

   - Tout champ personnalisé configuré par votre administrateur

   - Le document justificatif joint, s’il est fourni. Sélectionnez la pièce jointe à afficher ou à télécharger

5. Sélectionnez **Approuver** ou **Rejeter**.

6. Dans le champ **Commentaire de révision**, saisissez des notes pour l&#39;élève. Cette option est facultative, mais recommandée lors du rejet d’une demande, afin que l’élève sache quoi corriger.

7. Sélectionnez **Envoyer**.

L’élève reçoit une notification dans l’application de votre décision. Si vous avez approuvé l’envoi, il apparaît désormais dans le relevé de notes de l’élève.

## Gestion de la file d’attente d’envoi

Votre file d’attente Apprentissage externe affiche toutes les envois en attente et passés de vos subordonnés directs.

**Filtrer par état**

Utilisez le filtre **État** pour affiner la liste :

- **Tout**- affiche chaque envoi quel que soit son statut

- **En attente de révision-** affiche uniquement les envois en attente de votre révision

- **Approuvé-** affiche les envois que vous avez déjà approuvés

- **Rejeté-** affiche les envois que vous avez rejetés

**Rechercher et trier**

- Utilisez le champ **Rechercher** pour rechercher des envois par nom d&#39;élève.

- Par défaut, les soumissions sont triées par date de soumission, la plus récente apparaissant en haut.

### Règles d&#39;acheminement pour l&#39;approbation

Par défaut, les soumissions d’apprentissage externes sont acheminées vers le responsable direct d’un élève. Les règles suivantes s’appliquent lorsqu’aucun responsable direct n’est affecté à un élève :

| **L’élève a un responsable** | **L’élève est un responsable lui-même** | **L&#39;envoi est acheminé vers** |
|---------------------------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Oui | Non | Responsable direct (cas par défaut) |
| Oui | Oui | Responsable direct (cas par défaut) |
| Non | Non | Utilisateur du compte racine, si l’utilisateur du compte racine a un rôle de responsable ; sinon, l’envoi est approuvé automatiquement. |
| Non | Oui | Utilisateur du compte racine, si l’utilisateur du compte racine a un rôle de responsable ; sinon, la soumission est acheminée à l’élève. |

Si vous avez des questions sur l’affectation d’un responsable pour un élève spécifique, contactez l’administrateur de votre compte.

## Modifications des rapports d’apprentissage externe et des relevés de notes

Lorsque la soumission d&#39;apprentissage externe d&#39;un élève est approuvée dans Adobe Learning Manager, l&#39;activité est ajoutée au système de rapports et apparaît à la fois dans le relevé de notes de l&#39;élève administrateur et dans le relevé de notes de l&#39;élève.

### Affichage de l’apprentissage externe dans les relevés de notes des élèves

**Remarque :** l’activation de l’apprentissage externe ajoute les nouvelles colonnes suivantes au relevé de notes de l’élève administrateur : **Nom de l’apprentissage externe**, **Commentaire d’achèvement** et une colonne dynamique pour chaque champ personnalisé. Les colonnes de champs personnalisés apparaissent toujours à la fin de l’exportation. Si les données du relevé de notes de l’élève sont intégrées aux outils de création de rapports automatisés ou de veille stratégique, assurez-vous que ces pipelines sont mis à jour pour gérer les colonnes supplémentaires.

Seules les demandes d&#39;apprentissage externes **approuvées** apparaissent dans les transcriptions. Les envois dont le statut est **En attente d&#39;approbation** ou **Refusé** ne sont pas inclus dans les exportations de relevé de notes.

Le relevé de notes de l’élève administrateur et le relevé de notes de l’élève gèrent différemment le titre d’apprentissage externe :

- Dans le **relevé de notes de l’élève administrateur**, le titre de l’apprentissage externe est placé dans la colonne **Programme d’apprentissage/Certification/Cours** existante, en conservant la structure de la colonne cohérente avec les autres types d’activités d’apprentissage.

- Dans le **relevé de notes de l&#39;élève** (généré par l&#39;élève), une nouvelle colonne intitulée **Nom de l&#39;apprentissage externe** est ajoutée immédiatement après la colonne **Module**.

Les champs personnalisés configurés par votre administrateur apparaissent sous forme de colonnes dynamiques à la fin des deux exportations de relevé de notes une fois qu’une soumission est approuvée.

Le filtrage basé sur la date dans le relevé de notes de l&#39;élève administrateur pour les lignes d&#39;apprentissage externes est basé sur la **date d&#39;achèvement**, qui correspond à la date d&#39;approbation.