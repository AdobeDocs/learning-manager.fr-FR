---
description: Lors du chargement d’un fichier CSV, une erreur s’affiche. Lisez ce qui suit pour résoudre le problème.
jcr-language: en_us
title: Impossible de charger le fichier CSV
contentowner: saghosh
exl-id: 10458499-1038-4c62-971f-f950d383e970
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 71%

---

# Impossible de charger le fichier CSV

## Erreur : Troncation de données : Données trop longues pour la colonne

Lorsque vous tentez de charger un fichier CSV dans Adobe Learning Manager, le message d’erreur suivant s’affiche.

![](assets/csv-upload-failed.png)

*Message d’erreur indiquant que le traitement CSV a échoué*

## Cause

L’erreur se produit si les données présentes dans la colonne spécifiée dépassent la limite de caractères définie pour la colonne.

## Résolution

* Ouvrez le fichier CSV.
* Vérifiez les données de la colonne mentionnée dans l’erreur.
* Si une valeur est grande (par exemple, supérieure à 60 caractères), modifiez la valeur pour corriger les données.

## Erreur : La première colonne du fichier CSV affiche un caractère spécial.

Vous ne pouvez pas charger de fichier CSV, car la première colonne affiche un caractère spécial lors du mappage des colonnes.

![](assets/csv-2.png)

*Caractère spécial dans la colonne Nom*

## Cause

Le problème se produit lorsque le fichier CSV est enregistré au format UTF-8 dans Excel. Lorsque vous enregistrez un fichier CSV dans Excel au format UTF-8, le fichier est enregistré au format UTF-BOM. Vous pouvez vérifier cela à l’aide du Bloc-notes++ ou lorsque vous chargez un fichier CSV vers Learning Manager. Lors du mappage des colonnes, la première colonne affiche un caractère spécial.

## Résolution

* **A :** Enregistrement via Excel :

   1. Ouvrez le fichier CSV dans Excel.
   1. Enregistrez le fichier au format CSV normal.

* **B:** enregistrement via le Bloc-notes ou le Bloc-notes ++ :

   * Ouvrez le fichier CSV dans le Bloc-notes ou le Bloc-notes++.
   * Enregistrez le fichier au format UTF-8.

## Erreur : Adresse électronique de l’utilisateur déjà présente dans le système

Vous ne pouvez pas charger de fichier CSV, car le traitement CSV a échoué. Vous voyez le message d’erreur ci-dessous :

![](assets/csv-3.png)

*Message d’erreur pour un utilisateur dupliqué*

## Cause

Ce problème se produit si un utilisateur est déjà présent dans le système avec la même adresse e-mail ou le même UUID.

## Résolution

### Scénario 1

**Comptes sur lesquels l’UUID n’est pas activé.**

Dans ce scénario, cette erreur s’explique par deux raisons :

1. L’utilisateur que vous essayez d’ajouter est le gestionnaire d’un profil externe. Pour résoudre ce problème, ouvrez le profil externe dont fait partie l&#39;utilisateur, sélectionnez l&#39;utilisateur, cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Attribuer un rôle]** > **[!UICONTROL Responsable]**, puis modifiez le Responsable du profil.
1. L’utilisateur que vous essayez d’ajouter a été purgé. Dans ce scénario, vous ne pourrez pas ajouter l’utilisateur avec la même adresse e-mail tant que le processus de purge n’est pas terminé. Pour résoudre ce problème **&#x200B; a**&#x200B;joutez une adresse e-mail secondaire à l’utilisateur pour lui donner accès à la plateforme. Une fois le processus de purge terminé, modifiez l’utilisateur et remplacez l’adresse e-mail par l’adresse correcte.

### Scénario 2

**Comptes UUID.**

Pour les comptes UUID, ce problème peut se produire si un utilisateur s’est vu attribuer un UUID déjà utilisé par un autre utilisateur du compte ou si l’utilisateur a une autre adresse e-mail.

Par exemple, imaginons qu’il y ait deux utilisateurs, A et B, avec des adresses e-mail, <a@xyz.com> et <b@xyz.com> avec l’UUID 1 et 2 respectivement.

Si vous chargez un fichier CSV dont l’UUID de l’utilisateur A est défini sur 3 et l’UUID de l’utilisateur B sur 2, une erreur s’affiche.

>[!TIP]
>
>Pour résoudre ce problème, **vous devez avoir la même adresse e-mail et le même UUID pour l’utilisateur sur le fichier CSV et le système.**
