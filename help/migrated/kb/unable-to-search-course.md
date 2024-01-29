---
jcr-language: en_us
title: Impossible de rechercher un cours dans Learning Manager
description: Un élève ne peut pas rechercher un cours dans Learning Manager.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---



# Impossible de rechercher un cours dans Learning Manager

## Problème

Un élève ne peut pas rechercher un cours dans Learning Manager.

## Scénario 1 : Inscription via un objet d’apprentissage supérieur

### Résumé

Dans certains scénarios, un élève recherche un cours et celui-ci n’est pas répertorié. Mais si l’élève s’est inscrit à un programme d’apprentissage/une certification, il peut afficher le cours dans l’objet d’apprentissage.

### Pourquoi cela se produit-il ?

Dans Learning Manager, lorsqu’un élève est inscrit par le biais d’un programme d’apprentissage ou d’une certification, l’inscription à ce cours se fait par le biais du programme d’apprentissage ou de la certification.

Par conséquent, l’élève ne peut pas rechercher les cours autonomes sous **Mon apprentissage**.

Cependant, l’élève ne peut pas afficher les cours dans le programme d’apprentissage/la certification.

## Scénario 2 : l’élève n’a pas accès au catalogue contenant le cours.

### Résumé

Un élève ne peut pas rechercher des cours dans le catalogue ou le tableau de bord d’apprentissage.

### Pourquoi cela se produit-il ?

Ce problème se produit si :

* L’élève ne fait pas partie du catalogue contenant le cours **OU**
* Le cours ne fait pas partie du catalogue auquel l’élève a accès.

### Résolution

1. Connectez-vous en tant qu’administrateur.

1. Cliquez sur **[!UICONTROL Catalogue]** et accédez au catalogue contenant le cours.
1. Cliquez sur **[!UICONTROL Partage en interne]** ou **[!UICONTROL Contenu]** (selon le scénario mentionné ci-dessus).

   ![](assets/cp-share-internally.png)

   *Partage du catalogue en interne*

1. Passez en revue les scénarios ci-dessous :

   * L’élève ne fait pas partie du catalogue

     Pour partager le catalogue, cliquez sur **[!UICONTROL Ajouter]**, puis ajoutez le groupe d’utilisateurs dont l’utilisateur fait partie. Cliquez sur **[!UICONTROL Enregistrer]**.

     ![](assets/cp-add-user-group.png)

     *Ajouter le groupe d’utilisateurs*

   * Le cours ne fait pas partie du catalogue

     Dans la section Contenu, cliquez sur **[!UICONTROL Ajouter du contenu]** et sélectionnez le cours à ajouter au catalogue.

     ![](assets/cp-add-content.png)

     *Ajouter du contenu au cours*
