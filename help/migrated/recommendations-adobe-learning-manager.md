---
title: Recommendations dans Adobe Learning Manager
description: Le cœur du moteur de recommandations est basé sur le nouvel algorithme de classement des cours de Learning Manager. L'algorithme utilise 50 millions de points de données et cinq années de données d'apprentissage agrégées sur des millions d'utilisateurs pour classer les cours en fonction de leur probabilité d'inscription. Ce classement garantit que la plupart des cours auxquels vous pouvez vous inscrire sont affichés à l'avance pour les élèves.
source-git-commit: 40f6732147b7babeb1f11ce52045e6baf6338ce1
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 0%

---



# Recommendations dans Adobe Learning Manager

Adobe Learning Manager a introduit un nouveau système de recommandations remanié pour les cours. Cette fonctionnalité de recommandations utilise des algorithmes d’IA et les intérêts des utilisateurs tels que les produits, les rôles et les niveaux pour fournir des recommandations de contenu personnalisées.

Le nouveau système de recommandations vous permet de créer des paramètres personnalisés que les élèves peuvent sélectionner pour recevoir des recommandations personnalisées. Ces recommandations seront affichées sous la forme de cours, de parcours d’apprentissage et de certifications aux élèves sur leur flux de page d’accueil.

Pour commencer à utiliser cette fonctionnalité, vous devez l’activer dans l’application d’administration.

## Activation et configuration des recommandations

1. Chargez le cours et les données utilisateur (facultatif).
1. Appliquez les modifications en direct.
1. Après avoir activé et configuré les recommandations, téléchargez les données dans Adobe Learning Manager pour que les recommandations commencent à fonctionner. Ces données sont les suivantes :

   * Données du cours
   * Données utilisateur (facultatif)

## Algorithme de classement des cours

Le noyau du moteur de recommandations est piloté par la nouvelle version de Learning Manager **[!UICONTROL Algorithme de classement des cours]**. L&#39;algorithme utilise 50 millions de points de données et cinq années de données d&#39;apprentissage agrégées sur des millions d&#39;utilisateurs pour classer les cours en fonction de leur probabilité d&#39;inscription. Ce classement garantit que la plupart des cours auxquels vous pouvez vous inscrire sont affichés à l&#39;avance pour les élèves.

## Termes clés

Le nouveau moteur de recommandation basé sur l’IA de Learning Manager fournit aux responsables de l’apprentissage un système de recommandation basé sur des paramètres configurable pour créer une expérience personnalisée pour les élèves.

Les paramètres sont : **Produits/rubriques**, **Rôles**, et **Niveaux**. En outre, ces paramètres peuvent être renommés en fonction de vos besoins. Ainsi, les « produits » peuvent devenir des « sujets » ou les « rôles » peuvent devenir des « régions ».

## Configuration du système de recommandations

Le nouveau moteur de recommandations d’Adobe Learning Manager simplifie le workflow d’administration impliqué dans la configuration de recommandations personnalisées, car les données sur les produits et les rôles associés à un client/partenaire sont généralement disponibles pour les administrateurs (par exemple, à partir des enregistrements d’achat).

La configuration du nouveau moteur de recommandations implique principalement trois workflows :

* Administrateur
* Auteur
* Élève

Les administrateurs configurent les valeurs des paramètres Produits, Rôles et Niveaux du compte. Par exemple, un fournisseur de solutions informatiques dont la clientèle principale est les banques peut configurer le paramètre « Product » pour qu’il ait des valeurs telles que Payment Gateway, Secure Cloud Storage, Fraud Detection System, Trading Platform, etc., et le paramètre « Role » pour qu’il ait des valeurs telles que Spécialiste de l’intégration, Administrateur réseau, Analyste des risques, Responsable de la conformité, etc.

Les administrateurs bénéficient d’un workflow guidé dans Learning Manager pour configurer de manière optimale le moteur de recommandations et le personnaliser en fonction du cas d’utilisation du compte. En outre, les administrateurs ont également la possibilité de configurer des recommandations PRL via un chargement CSV unique.

1. Sélectionner **[!UICONTROL Recommendations]** dans l’application d’administration.

   ![Sélection de Recommendations dans l’application d’administration](assets/image831538.png)

   *Sélectionnez l’option Recommendations*

1. Cliquez sur **[!UICONTROL Mettre à niveau]**.

   ![Mise à niveau vers le nouveau système](assets/image784236.png)

   *Sélectionnez l’option Mettre à niveau.*

1. Cliquez sur **[!UICONTROL Continuer]** pour passer au nouveau système de recommandations.

   ![Passer au nouveau système](assets/image521152.png)
   *Cliquez sur le bouton Continuer.*

1. Créez les paramètres de recommandation pour les produits et les rôles.

   ![Création des paramètres](assets/image43406.png)
   *Créer des paramètres pour la recommandation*

1. Cliquez sur **[!UICONTROL Ajouter d’autres valeurs]**.
1. Ajoutez les produits. Saisissez le nom d’un produit et appuyez sur Entrée.

   Vous devez ajouter au moins deux produits pour commencer à utiliser.

   ![ajouter des produits](assets/image623058.png)
   *Ajouter des produits*

1. Ajoutez les rôles. Saisissez le nom des rôles et appuyez sur Entrée.

   ![ajouter des rôles](assets/image156786.png)
   *Ajout des rôles*

1. Cliquez sur **[!UICONTROL Continuer]**.

   Les produits et les rôles figurent désormais dans la liste des paramètres.

   ![produits et rôles](assets/image266930.png)
   *Liste des produits et des rôles*

## Préparation des données

Les données d’intérêt de l’utilisateur, le produit, les rôles et les niveaux doivent être chargés pour que les recommandations fonctionnent correctement.

**Options de téléchargement des données**

La fonction de recommandations est configurable. Ainsi, au lieu de produits/rôles/niveaux, vous pouvez utiliser les rubriques/rôles/niveaux ou choisir l’une de ces options : produit/rubriques uniquement, rôles uniquement, produit/rubriques et rôles uniquement, rôles-niveaux uniquement ou produits-niveaux uniquement.

En fonction de la configuration de recommandation choisie, modifiez vos feuilles de données en conséquence.

La section suivante explique l’option la plus étendue d’utilisation du produit, des rôles et des niveaux.

L’administrateur doit télécharger les données utilisateur dans un format prédéterminé. Les données chargées sont ensuite intégrées dans l’algorithme de recommandation, de sorte qu’un élève reçoive des recommandations pour les bons cours en fonction de ses rôles et niveaux.

**Conditions préalables**

Pour charger les données afin que les recommandations fonctionnent, renseignez les champs Produits, Rôles et Niveaux dans les fichiers CSV User et RecommendationsLO.

Dans le cadre de l’exercice de préparation des données, nous fournissons deux modèles CSV :

**RecUser.csv**

* ID utilisateur
* Produits
* Rôles
* Niveaux (Débutant, Intermédiaire ou Avancé)

Voici un exemple d’enregistrements dans le fichier csv :

| ID utilisateur | Produits | Rôles | Niveaux |
|--- |--- |--- |--- |
| 123 | Data Science | Analyste | Analyste : Intermédiaire |
| 456 | Génie aérospatial | Technicien | Technicien : avancé |

**RecLO.csv**

* Formation
* Type de formation
* Nom de la formation
* Produits
* Rôles
* Niveaux
* Balises
* Compétences

Voici un exemple d’enregistrements dans le fichier csv :

| ID de formation | Type de formation | Nom de la formation | Produits | Rôles | Niveaux | Balises | Compétences |
|---|---|---|---|---|---|---|---|
| 111 | COURS | Python 101 | Data Science | Analyste | Analyste : Intermédiaire | données | Généralités |
| 222 | COURS | Julia 101 | Data Science | Analyste | Analyste : avancé | données | Généralités |

Remplissez ces fichiers CSV et contactez votre équipe de réussite client pour télécharger les formats et charger ces fichiers CSV.

## Application des recommandations en direct

Une fois les deux fichiers CSV chargés, cliquez sur Accéder en direct. Cela rendra le nouveau système de recommandation visible aux élèves.

![passer en direct](assets/computerdescription-automatically.png)
*Application des recommandations en direct*

Le système de recommandation est désormais disponible pour vos élèves.

## Modification d’un paramètre

1. Dans la liste des paramètres, sélectionnez l’icône représentant trois points, puis sélectionnez **[!UICONTROL Modifier le nom du paramètre]**.

   ![Modifier le paramètre](assets/edit-parameter.png)

1. Modifiez le nom du paramètre et cliquez sur **[!UICONTROL Enregistrer]**.

   ![résultats](assets/image688522.png)
   *Modifier le paramètre*

## Suppression d’un paramètre

1. Dans la liste des paramètres, sélectionnez l’icône représentant trois points, puis sélectionnez **[!UICONTROL Supprimer le paramètre]**.

![supprimer le paramètre](assets/delete-parameter.png)
*Supprimer le paramètre*

## Page des paramètres du cours

Dans la page des paramètres d&#39;un cours, la recommandation pour les produits et les rôles est répertoriée. Les élèves seront recommandés pour ce cours s’ils ont exprimé leur intérêt pour ces produits et rôles.

![définition de l’image](assets/course-settings-image.png)
*Page des paramètres du cours*

## Vue Élève

Pour un compte avec des recommandations basées sur PRL configurées, lorsqu’un élève se connecte à la plateforme d’apprentissage, un workflow guidé aide l’élève à configurer des recommandations en fonction de ses préférences de produit, de rôle et de niveau. Le profil de l&#39;élève est alors créé pour le moteur de recommandations à analyser.

Les élèves sur des comptes qui ont basculé vers le nouveau système de recommandations peuvent afficher les cours et formations recommandés.

Les élèves peuvent voir les éléments suivants :

* Produits, rôles - Niveaux : les élèves sont invités à sélectionner d’abord les produits, les rôles, puis les niveaux pour chacun des rôles sélectionnés
* Produit - Niveaux : les élèves sont invités à sélectionner d’abord les produits, puis les niveaux pour chacun des produits sélectionnés
* Rôles - Niveaux : les élèves sont invités à choisir d’abord les rôles, puis les niveaux pour chaque rôle sélectionné.
* Produits et rôles : les élèves sont invités à choisir d’abord Produits, puis Rôles.
* Produits : les élèves sont invités à sélectionner uniquement des produits.
* Rôles : les élèves sont invités à choisir uniquement des rôles.

Après avoir sélectionné Recommendations dans le panneau de gauche, l’élève voit une fenêtre contextuelle permettant de configurer les recommandations.

![recommandations de configuration](assets/image575540.png)
*L’élève configure la recommandation*

En cliquant sur Configurer Recommendations, l’élève accède à la fenêtre contextuelle de sélection de produits.

![fenêtre contextuelle sélection de produit](assets/product-selection-popup.png)
*Sélectionner des produits*

Dans la fenêtre contextuelle suivante, l’élève peut sélectionner le rôle.

![sélectionner un rôle](assets/image270860.png)
*Sélectionner des rôles*

L’élève peut ensuite ajouter les niveaux.

![ajouter des niveaux](assets/image650040.png)
*Sélectionner des niveaux*

## Bandes d’apprentissage dans l’application de l’élève

Un élève peut voir les bandes suivantes sur l’application :

* Mon parcours d’apprentissage
* Bande avec calendrier, widget de réseaux sociaux et de ludification
* Enregistré par moi-même
* Bande super pertinente
* Bande de produits - 1
* Product strip - 2
* Bande de découverte
* Bande recommandée par l’administrateur
* Parcourir par bande de catalogue

### Cartes sur mon support d’apprentissage

![cartes de bande d’apprentissage](assets/image770606.png)
*Cartes sur bande d’apprentissage*

Chaque carte comporte une note, une image de carte, un titre, une compétence, la date de publication, l’auteur, la durée, la barre de progression et un bouton Continuer ou Explorer.

### Cartes enregistrées par moi

![cartes enregistrées](assets/cards-saved-by-me.png)
*Cartes enregistrées*

Chaque carte comporte une note, une image de carte, un titre, une compétence, la date de publication, l’auteur, la durée, la barre de progression et un bouton Démarrer, Explorer, Continuer ou Revisiter.

Aucune barre de progression n’apparaît sur la carte une fois qu’un élève a commencé le cours. Un élève peut également Annuler l’enregistrement du cours.

### Cartes sur la bande super pertinente

![cartes à bande très pertinentes](assets/super-relevant-cards.png)
*Cartes pertinentes*

Chaque carte comporte une note, une image de carte, un titre, une compétence, la date de publication, l’auteur, la durée, la barre de progression et un bouton Démarrer, Explorer, Continuer ou Revisiter.

Aucune barre de progression n’apparaît sur la carte une fois qu’un élève a commencé le cours.

Au menu, deux options : **[!UICONTROL Enregistrer]** et **[!UICONTROL Ne pas recommander]**. Si l’élève clique sur **[!UICONTROL Enregistrer]**, le cours est enregistré dans la bande « Enregistré par moi ». Si l’élève clique sur **[!UICONTROL Ne pas recommander]**, la formation recommandée est supprimée de la liste.
