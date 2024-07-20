---
jcr-language: en_us
title: Impossible de rechercher un cours dans Learning Manager
description: Un élève ne peut pas rechercher un cours dans Learning Manager.
contentowner: nluke
exl-id: 702aacb7-a0b9-48fb-8a3d-425bfea63f65
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 55%

---

# Impossible de rechercher un cours dans Learning Manager

## Problème

Un élève ne peut pas rechercher un cours dans Learning Manager.

## Scénario 1 : Inscription via un objet d’apprentissage supérieur

### Résumé

Dans certains scénarios, un élève recherche un cours et celui-ci n’est pas répertorié. Mais si l’élève s’est inscrit à un programme d’apprentissage ou à une certification, il peut afficher le cours dans l’objet d’apprentissage.

### Pourquoi est-ce que cela se produit ?

Dans Learning Manager, lorsqu’un élève est inscrit par le biais d’un programme d’apprentissage ou d’une certification, l’inscription à ce cours se fait par le biais du programme d’apprentissage ou de la certification.

Par conséquent, l’élève ne peut pas rechercher les cours autonomes sous **Mon apprentissage**.

Cependant, l’élève ne peut pas afficher les cours dans le programme d’apprentissage/la certification.

## Scénario 2 : l’élève n’a pas accès au catalogue contenant le cours.

### Résumé

Un élève ne peut pas rechercher des cours dans le catalogue ou dans le tableau de bord d’apprentissage.

### Pourquoi est-ce que cela se produit ?

Ce problème se produit si :

* L’élève ne fait pas partie du catalogue contenant le cours **OU**
* Le cours ne fait pas partie du catalogue auquel l’élève a accès.

### Résolution

1. Connectez-vous en tant qu’administrateur.

1. Cliquez sur **[!UICONTROL Catalogue]** et accédez au catalogue contenant le cours.
1. Cliquez sur **[!UICONTROL Partager en interne]** ou sur **[!UICONTROL Contenu]** (selon le scénario mentionné ci-dessus).

   ![](assets/cp-share-internally.png)

   *Partage du catalogue en interne*

1. Passez en revue les scénarios ci-dessous :

   * L’élève ne fait pas partie du catalogue

     Pour partager le catalogue, cliquez sur **[!UICONTROL Ajouter]** et ajoutez le groupe d&#39;utilisateurs auquel appartient l&#39;utilisateur. Cliquez sur **[!UICONTROL Enregistrer]**.

     ![](assets/cp-add-user-group.png)

     *Ajouter le groupe d&#39;utilisateurs*

   * Le cours ne fait pas partie du catalogue

     Dans la section Contenu, cliquez sur **[!UICONTROL Ajouter du contenu]** et sélectionnez le cours que vous devez ajouter au catalogue.

     ![](assets/cp-add-content.png)

     *Ajouter du contenu au cours*
