---
jcr-language: en_us
title: Ajouter des utilisateurs par groupe
description: Découvrez comment ajouter plusieurs utilisateurs à la fois.
contentowner: saghosh
exl-id: c3309ce5-8764-452e-82d5-5637c23c661b
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 25%

---

# Ajouter des utilisateurs par groupe

Dans cette formation, vous apprendrez à ajouter des utilisateurs en bloc via un fichier CSV.

[![bouton](feature-summary/assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=51TC8QS1&amp;mv=display&amp;mv2=display#/course/7555555)

Si vous ne pouvez pas lancer la formation, écrivez à <almacademy@adobe.com>.

## Comment ajouter plusieurs utilisateurs

Vous pouvez ajouter plusieurs utilisateurs à la fois en procédant comme suit :

1. Cliquez sur **[!UICONTROL Utilisateurs]** dans le volet gauche de la connexion Administrateur, puis cliquez sur **[!UICONTROL Ajouter]** > **[!UICONTROL Charger un fichier csv]**. Une boîte de dialogue contextuelle s’affiche.

1. Vous pouvez ajouter plusieurs utilisateurs en utilisant un fichier .CSV. Cliquez sur **[!UICONTROL Importer]** et sélectionnez/ouvrez le fichier .csv depuis votre ordinateur.

1. Après l’importation du fichier, vous devez mapper le contenu du fichier.csv avec les libellés de l’application lorsque vous chargez un fichier.csv pour la première fois.

   Pour tous les téléchargements ultérieurs, les paramètres précédents des libellés sont pris en compte. Cliquez sur **[!UICONTROL Enregistrer]** après avoir terminé le mappage des données et cliquez sur **[!UICONTROL Ajouter]** pour télécharger le fichier .csv mappé.

1. Cliquez sur **[!UICONTROL Enregistrer]** après avoir terminé le mappage des données et cliquez sur **[!UICONTROL Ajouter]** pour télécharger le fichier .csv mappé.

## Téléchargement CSV avec les champs obligatoires {#csvuploadwithmandatoryfields}

Il n’est pas obligatoire d’ajouter le profil de l’utilisateur et l’ID de messagerie du responsable dans le fichier CSV. Le nom d’utilisateur et l’ID de messagerie de l’utilisateur sont les seuls champs obligatoires.

Dans ce cas, par défaut, l’administrateur de votre société est traité comme le responsable des utilisateurs. Par défaut, employee est considéré comme le profil de l&#39;utilisateur.

**Exemple CSV** 

L’exemple de fichier CSV pour Learning Manager est disponible ci-dessous avec des champs obligatoires.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## Téléchargement CSV avec tous les champs {#csvuploadwithallthefields}

Avant d’inclure l’ID de messagerie du responsable pour tout employé, assurez-vous que le responsable est d’abord ajouté en tant qu’employé dans le fichier CSV. Par exemple, repérez le nom de l&#39;employé Howard Walters dans l&#39;instantané ci-dessous :

![](assets/csv-example.png)

*Modèle CSV à télécharger*

En outre, les administrateurs d’une organisation peuvent s’ajouter en tant qu’employés et mentionner l’ID de messagerie de leur responsable en tant que racine.

**Exemple CSV** 

L’exemple de fichier CSV pour Learning Manager est disponible ci-dessous avec tous les champs.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Reportez-vous au contenu d&#39;aide sur l&#39;[utilisation du chargement CSV](/help/migrated/administrators/feature-summary/add-users-user-groups.md) pour plus d&#39;informations.
