---
jcr-language: en_us
title: Marché de contenus
description: Learning Manager propose désormais un Marché de contenus qui vous permet d’explorer et d’acheter des formations. Explorez plus de 70 000 cours couvrant un large éventail de sujets, disponibles dans plusieurs formats. Faites votre choix parmi des listes de lecture sélectionnées qui correspondent à une grande variété de rôles et répondent à vos besoins en matière d’apprentissage et d’acquisition de compétences.
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 69%

---



# Marché de contenus

Learning Manager propose désormais un Marché de contenus qui vous permet d’explorer et d’acheter des formations. Explorez plus de 70 000 cours couvrant un large éventail de sujets, disponibles dans plusieurs formats. Faites votre choix parmi des listes de lecture sélectionnées qui correspondent à une grande variété de rôles et répondent à vos besoins en matière d’apprentissage et d’acquisition de compétences.

L’application Administrateur propose une nouvelle option **[!UICONTROL Marché de contenus]**, qui se trouve dans le panneau de gauche.

Les utilisateurs peuvent effectuer des achats dans des listes de lecture sélectionnées couvrant différents sujets ou acheter l’intégralité du catalogue.

Sur la page, vous pouvez voir deux vignettes : Formation en entreprise et Formation Creative Cloud. La première vignette ouvre le marché, à l’aide duquel vous pouvez acquérir des cours pour vos élèves. La deuxième vignette ouvre le catalogue des contenus.

La page Formation en entreprise de l’application Administrateur vous permet d’inviter des utilisateurs et de télécharger le rapport des intérêts, mais aussi d’acheter l’intégralité du catalogue ou une liste de lecture sélectionnée.

**Inviter des utilisateurs**

Invitez les utilisateurs à explorer le Marché de contenus et à exprimer leur intérêt. En tant qu’administrateur, vous pouvez inviter tous les élèves du compte ou inviter des élèves sélectionnés. Pour accorder l’accès aux élèves, vous devez les inviter.

Un élève peut également être supprimé de l’option Marché de contenus. Pour révoquer l’accès, cliquez sur le bouton **[!UICONTROL Révoquer l’accès]** lien.  Les utilisateurs ne pourront plus voir la page Marché de contenus dans l’application de l’élève.

Cette option est sélectionnée par défaut pour tous les nouveaux comptes. Pour les comptes existants, l’administrateur doit inviter les utilisateurs à explorer le marché.

## Achat

Vous bénéficiez d’un accès illimité à l’ensemble de la bibliothèque de cours. Cliquez sur le bouton **[!UICONTROL Achat]** pour télécharger un formulaire de demande d’achat.

![](assets/purchase-request.png)

*Saisissez le nombre de places à acheter*

Spécifiez le nombre de places pour lesquelles vous souhaitez acheter les cours. Téléchargez le formulaire de demande d’achat, puis envoyez-le à l’équipe commerciale de Learning Manager.

L’équipe validera ensuite les informations, puis générera une clé qui vous sera fournie. Il s’agit de la clé d’activation à l’aide de laquelle vous accorderez l’accès à vos utilisateurs à l’offre de contenu.

Une fois la clé générée par l’équipe CSAM, l’administrateur peut utiliser la clé pour importer les cours et migrer les cours vers le catalogue existant ou le nouveau catalogue.

Lors de la migration des cours, l’état **[!UICONTROL Importation de cours]** s’affiche. Une fois la migration terminée, l’administrateur reçoit une notification indiquant que la migration est terminée et réussie.

Le **[!UICONTROL Licences]** La section affiche ensuite toutes les licences acquises pour le compte.

L’administrateur peut voir les liens des catalogues achetés dans la page Présentation du catalogue.

Une fois les cours ajoutés au catalogue, l’administrateur peut alors accorder l’accès aux formations à divers utilisateurs ou groupes d’utilisateurs.

![](assets/licenses.png)

*Accorder l’accès à la formation aux utilisateurs et aux groupes d’utilisateurs*

## Rapport des intérêts

Lorsqu’un élève clique sur Exprimer l’intérêt pour le catalogue dans l’application Élève, l’intérêt est enregistré dans un rapport des intérêts. L’administrateur peut télécharger le rapport. Le rapport (csv) contient les champs suivants :

* Nom du catalogue
* Nombre d’utilisateurs exprimant leur intérêt
* Adresse e-mail de l’utilisateur exprimant son intérêt

## Modèles de courriers électroniques

Pour prendre en charge ce flux de travail, vous pouvez choisir entre trois modèles de courriers électroniques :

1. **[!UICONTROL Activation du contenu réussie]:** Cet e-mail est envoyé lorsque l’achat d’un contenu avec un nom de clé a réussi. Toute la formation achetée est alors disponible.
1. **[!UICONTROL Échec du chargement utilisateur automatisé]:** Cet e-mail est envoyé lorsque la mise à jour automatique du fichier CSV dans le compte échoue pour une raison quelconque.
1. **[!UICONTROL Inviter les utilisateurs à explorer le contenu]:** Il s’agit d’un e-mail d’invitation envoyé aux élèves lorsque l’administrateur a acheté des cours. L’administrateur peut consulter le rapport des intérêts pour comprendre les exigences générales et prendre la décision d’achat.

1. Les cours achetés ne peuvent pas être ajoutés aux certificats récurrents.
1. Les cours achetés ne peuvent pas être partagés avec des comptes d’homologues.
1. Les cours achetés peuvent être consommés par tous les utilisateurs qui y ont accès. Configurez la visibilité du catalogue pour restreindre la visibilité des cours achetés à certains utilisateurs.
1. Les cours achetés ne peuvent pas être consommés une fois que la clé d’activation a expiré. Veuillez acheter/activer une autre clé pour permettre la consommation.

## Hub de contenu dans le Marché de contenus

Le Hub de contenu permet aux administrateurs et aux experts en la matière (SME) de présélectionner les listes de lecture requises dans l’application de l’élève. Une fois la sélection effectuée, les administrateurs peuvent télécharger le formulaire de demande d’achat et le partager avec l’agent commercial Adobe.

Un administrateur peut inviter les experts en la matière à sélectionner la liste de lecture qui les intéresse.

![](assets/content-hub.png)

*Lancer le Hub de contenu à partir du marché*

Le Hub de contenu est disponible dans le rôle Élève pour tous les administrateurs. Les administrateurs autorisent les experts en la matière à présélectionner la liste de lecture qu’ils souhaitent acheter.

La page Hub de contenu est toujours visible par les administrateurs dans leur rôle d’élève, car cela leur permet de présélectionner facilement des listes de lecture. Pour vous aider à présélectionner la liste de lecture appropriée, les administrateurs peuvent rendre cette page accessible aux experts en la matière dans leur compte. Il vous suffit de consulter la page Formation en entreprise côté administrateur et de prendre les mesures nécessaires pour fournir l’accès.

![](assets/content-hub-resources.png)

*Afficher les ressources dans le Hub de contenu*

Learning Manager permet également aux administrateurs de télécharger une liste de lecture présélectionnée et de la partager avec l’équipe des ventes d’Adobe. Avant de télécharger la présélection, rendez-vous sur le Hub de contenu et sélectionnez une liste de lecture en ajoutant une liste de lecture à votre bibliothèque.

Ensuite, en tant qu’administrateur, cliquez sur **[!UICONTROL Marché de contenus]** > **[!UICONTROL Formation en entreprise]** > **[!UICONTROL Section Achat]** > **[!UICONTROL Listes de lecture sélectionnées]**. Cliquez sur le bouton **[!UICONTROL Acheter]** pour télécharger le formulaire de demande d’achat qui contient les détails de votre liste de lecture présélectionnée.

![](assets/download-purchase-request.png)

*Télécharger le formulaire de demande d’achat*

Les cours et la liste de lecture que vous voyez dans le Hub de contenu sont les mêmes que ceux que vous voyez dans le Marché de contenus. Le Hub de contenu permet simplement aux administrateurs et aux experts en la matière avec accès limité de présélectionner facilement une liste de lecture en vue de l’acheter.
