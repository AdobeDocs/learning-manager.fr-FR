---
description: Comment les plans de facturation déterminent si les comptes peuvent partager des licences et qu’advient-il des relations de partage lorsqu’un plan est modifié
jcr-language: en_us
title: 'Hiérarchisation : partage des places'
exl-id: 42b4cba4-1e44-40d8-aa57-ce2a855be258
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%
---

# Formules de partage de places et de compte dans Adobe Learning Manager

Le partage de licences permet à un compte de partager une partie de ses licences avec un autre compte, afin que les élèves du compte destinataire puissent accéder à Adobe Learning Manager à l’aide des licences du compte de partage. Les comptes qui peuvent partager des places, et avec qui, dépendent du plan de facturation de chaque compte.

## Quels forfaits prennent en charge le partage de sièges ?

Le partage de places est disponible pour les comptes de la formule **Ultimate**. Les comptes de la formule **Prime** ne peuvent pas partager de places avec un autre compte et ne peuvent pas recevoir de places partagées d&#39;un autre compte.

Les comptes facturés par carte de crédit figurent sur la formule Prime par défaut et ne peuvent donc pas participer au partage de places.

Les comptes d’évaluation sont la seule exception : un compte d’évaluation peut recevoir des places partagées à partir d’un compte Ultimate. Tant qu’une relation de partage active est en place, le compte d’évaluation dispose d’un accès aux fonctionnalités de niveau Ultimate.

## Comptes de pairs définition de la visibilité

Le paramètre Compte de pairs sera visible dans l’application d’administration du compte qui partage cette fonctionnalité.

>[!NOTE]
>
>Si votre compte partage des places avec d’autres comptes que celui dont vous recevez des places, par exemple, si votre compte transfère l’accès partagé à un troisième compte, chaque compte de cette chaîne doit être sur la formule de partage Ultimate pour continuer à fonctionner de bout en bout.

## Combinaisons de comptes prenant en charge le partage de places

Le tableau suivant montre si le partage de places est possible entre différentes combinaisons de formules de compte.

| Compte de partage (parent) | Compte de réception (enfant) | Partage pris en charge ? |
|---|---|---|
| Prime (tout) | Tout | Non, le partage de places est limité aux comptes de formule Ultimate |
| Ultimate | Ultimate | Oui |
| Ultimate | l’application | Non, incompatibilité de forfait |
| Ultimate | Un compte de carte de crédit | Non, il y a incompatibilité de forfait, car les comptes avec carte de crédit figurent sur le forfait Prime |
| Ultimate | Version d’essai | Oui, le compte d’essai obtient un accès de niveau Ultimate pendant que la relation est active |

>[!NOTE]
>
>Certaines restrictions supplémentaires sur le partage de places entre des configurations de compte spécifiques peuvent s’appliquer indépendamment du type de formule, en fonction par exemple de la configuration initiale de l’abonnement d’un compte. Si vous ne parvenez pas à établir une relation de partage entre deux comptes Ultimate, contactez le support technique de l’Adobe pour confirmer la configuration de votre compte.

## Qu’advient-il du partage de places lorsqu’une formule change ?

L’éligibilité au partage de places est évaluée au moment du renouvellement. Si la formule d’un compte change d’une manière qui affecte une relation de partage existante, ce qui suit se produit :

* Si la formule d’un compte de partage (parent) passe d’Ultimate à Prime au moment du renouvellement, ses relations de partage de sièges existantes se terminent.
* Si le compte destinataire dispose de son propre abonnement indépendant, celui-ci n’est pas affecté ; seule la relation de partage prend fin.
* Si le compte destinataire était un compte d’évaluation reposant sur l’accès Ultimate du compte parent, il revient à l’accès de niveau Prime une fois la relation de partage terminée.

Ces modifications prennent effet lors du prochain renouvellement du compte pour les comptes ALM existants, et non immédiatement pendant une durée de contrat active. Toutefois, ces paramètres ne s’appliquent pas aux nouveaux comptes créés après la mise en service de la fonctionnalité de hiérarchisation.

>[!NOTE]
>
>Les comptes facturés par carte de crédit qui ont actuellement un accès de niveau Ultimate passeront à la formule Prime à partir de leur prochain renouvellement. Si un tel compte entretient une relation de partage de siège active à ce stade, cette relation prend fin dans le cadre de la même transition.
