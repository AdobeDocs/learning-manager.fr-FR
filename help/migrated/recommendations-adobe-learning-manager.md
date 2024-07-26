---
title: Recommandations dans Adobe Learning Manager
description: Le cœur du moteur de recommandations est basé sur le nouvel algorithme de classement des cours de Learning Manager. L'algorithme utilise 50 millions de points de données et cinq années de données d'apprentissage agrégées sur des millions d'utilisateurs pour classer les cours en fonction de leur probabilité d'inscription. Ce classement garantit que la plupart des cours auxquels les élèves peuvent s’inscrire sont affichés à l’avance.
exl-id: 42083095-60a0-4e20-9097-3344d290da1a
source-git-commit: f171fab1b5c1aa56f6f398430c49740a0239c6fe
workflow-type: tm+mt
source-wordcount: '1470'
ht-degree: 58%

---

# Recommandations dans Adobe Learning Manager

Adobe Learning Manager a introduit un nouveau système revisité de recommandations de cours. Cette fonctionnalité de recommandations utilise des algorithmes d’IA et les intérêts des utilisateurs tels que les produits, les rôles et les niveaux pour fournir des recommandations de contenu personnalisées.

Le nouveau système de recommandations vous permet de créer des paramètres personnalisés que les élèves peuvent sélectionner pour recevoir des recommandations personnalisées. Ces recommandations s’affichent en tant que cours, parcours d’apprentissage et certifications dans le flux de la page d’accueil des élèves.

Pour commencer à utiliser cette fonctionnalité, vous devez l’activer dans l’application d’administrateur.

## Activation et configuration des recommandations

1. Transférez le cours et les données utilisateur (facultatif).
1. Publiez les modifications.
1. Après avoir activé et configuré les recommandations, téléchargez les données dans Adobe Learning Manager pour que les recommandations puissent commencer à fonctionner. Ces données sont les suivantes :

   * Données du cours
   * Données utilisateur (facultatif)

## Algorithme de classement des cours

Le noyau du moteur de recommandations est piloté par le nouvel **[!UICONTROL algorithme de classement des cours]** de Learning Manager. L&#39;algorithme utilise 50 millions de points de données et cinq années de données d&#39;apprentissage agrégées sur des millions d&#39;utilisateurs pour classer les cours en fonction de leur probabilité d&#39;inscription. Ce classement garantit que la plupart des cours auxquels les élèves peuvent s’inscrire sont affichés à l’avance.

## Termes clés

Le nouveau moteur de recommandation basé sur l’IA de Learning Manager fournit aux responsables de l’apprentissage un système de recommandation basé sur des paramètres configurable pour créer une expérience personnalisée pour les élèves.

Les paramètres sont : **Produits/rubriques**, **Rôles** et **Niveaux**. En outre, vous pouvez renommer ces paramètres selon vos besoins. Ainsi, les « produits » peuvent devenir des « sujets » ou les « rôles » peuvent devenir des « régions ».

## Configuration du système de recommandations

Le nouveau moteur de recommandations de Adobe Learning Manager simplifie le workflow d’administration impliqué dans la configuration des recommandations personnalisées, car les données sur les produits et les rôles associés à un client/partenaire sont généralement disponibles pour les administrateurs (par exemple, à partir des enregistrements d’achat).

Trois workflows principaux sont impliqués dans la configuration du nouveau moteur de recommandation :

* Administrateur
* Auteur
* Gestion

Les administrateurs configurent les valeurs des paramètres Produits, Rôles et Niveaux du compte. Par exemple, un fournisseur de solutions informatiques dont la clientèle principale est les banques peut configurer le paramètre « Product » pour qu’il ait des valeurs telles que Payment Gateway, Secure Cloud Storage, Fraud Detection System, Trading Platform, etc., et le paramètre « Role » pour qu’il ait des valeurs telles que Spécialiste de l’intégration, Administrateur réseau, Analyste des risques, Responsable de la conformité, etc.

Les administrateurs bénéficient d’un workflow guidé dans Learning Manager pour configurer de manière optimale le moteur de recommandations et le personnaliser en fonction du cas d’utilisation du compte. En outre, les administrateurs peuvent également configurer des recommandations PRL en chargeant une seule fois un fichier CSV.

1. Sélectionnez **[!UICONTROL Recommendations]** dans l&#39;application d&#39;administration.

   ![Sélectionnez Recommendations dans l&#39;application d&#39;administration](assets/image831538.png)

   *Sélectionnez l&#39;option Recommendations*

1. Cliquez sur **[!UICONTROL Mettre à niveau]**.

   ![Mise à niveau vers le nouveau système](assets/image784236.png)

   *Sélectionnez l&#39;option de mise à niveau*

1. Cliquez sur **[!UICONTROL Continuer]** pour passer au nouveau système de recommandations.

   <!--![Proceed to the new system](assets/image521152.png)
   *Select the Proceed button*-->

1. Créez les paramètres de recommandations pour les produits et les rôles.

   ![Créer les paramètres](assets/image43406.png)
   *Créer des paramètres pour la recommandation*

1. Cliquez sur **[!UICONTROL Ajouter d’autres valeurs]**.
1. Ajoutez les produits. Saisissez le nom d’un produit et appuyez sur Entrée.

   Vous devez ajouter au moins deux produits pour commencer.

   ![ajouter des produits](assets/image623058.png)
   *Ajouter des produits*

1. Ajoutez les rôles. Saisissez le nom des rôles et appuyez sur Entrée.

   ![ajouter des rôles](assets/image156786.png)
   *Ajouter les rôles*

1. Cliquez sur **[!UICONTROL Continuer]**.

   Les produits et les rôles apparaissent désormais dans la liste des paramètres.

   ![produits et rôles](assets/image266930.png)
   *Liste des produits et des rôles*

## Préparation des données

Les données d’intérêt de l’utilisateur, le produit, les rôles et les niveaux doivent être chargés pour que les recommandations fonctionnent correctement.

**Options de téléchargement de données**

La fonction de recommandations est configurable. Ainsi, au lieu de produits/rôles/niveaux, vous pouvez utiliser les rubriques/rôles/niveaux ou choisir l’une de ces options : produit/rubriques uniquement, rôles uniquement, produit/rubriques et rôles uniquement, rôles-niveaux uniquement ou produits-niveaux uniquement.

Modifiez vos fiches produit en fonction de la configuration de recommandation que vous choisissez.

L’option la plus complète d’utilisation des produits, des rôles et des niveaux est expliquée dans la section suivante :

L’administrateur doit transférer les données utilisateur dans un format prédéterminé. Les données transférées seront ensuite envoyées dans l’algorithme de recommandation, de sorte qu’un élève reçoive des recommandations pour les cours appropriés en fonction de ses rôles et niveaux.

**Conditions préalables**

Pour transférer les données afin que les recommandations fonctionnent, renseignez les champs Produits, Rôles et Niveaux dans les fichiers CSV User et RecommandationLO.

Dans le cadre de l’exercice de préparation des données, nous fournissons deux modèles CSV :

**RecUser.csv**

* ID utilisateur
* Produits
* Rôles
* Niveaux (débutant, intermédiaire ou avancé)

Voici un exemple d’enregistrements du fichier CSV :

| ID utilisateur | Produits | Rôles | Niveaux  |
|--- |--- |--- |--- |
| 123 | Science des données | Analyste | Analyste : Intermédiaire |
| 456 | Ingénieur en aérospatiale | Technicien | Technicien : Avancé |

**RecLO.csv**

* Cours/parcours d’apprentissage
* Type de formation
* Nom de la formation
* Produits
* Rôles
* Niveaux 
* Balises
* Compétences

Voici un exemple d’enregistrements du fichier CSV :

| ID de formation | Type de formation | Nom de la formation | Produits | Rôles | Niveaux  | Balises | Compétences |
|---|---|---|---|---|---|---|---|
| 111 | COURS | Python 101 | Science des données | Analyste | Analyste : Intermédiaire | data | Généralités |
| 222 | COURS | Julia 101 | Science des données | Analyste | Analyste : avancé | data | Généralités |

Remplissez ces fichiers CSV et contactez votre équipe de réussite client pour télécharger les formats et charger ces fichiers CSV.

## Publication des recommandations

Une fois les deux fichiers CSV chargés, cliquez sur Accéder en direct. Le nouveau système de recommandations sera ainsi visible pour les élèves.

![mise en ligne](assets/computerdescription-automatically.png)
*Mettez les recommandations en ligne*

Le système de recommandation est désormais disponible pour vos élèves.

## Modification d’un paramètre

1. Dans la liste des paramètres, sélectionnez l’icône représentant trois points puis **[!UICONTROL Modifier le nom du paramètre]**.

   ![Modifier le paramètre](assets/edit-parameter.png)

1. Modifiez le nom du paramètre et cliquez sur **[!UICONTROL Enregistrer]**.

   ![résultats](assets/image688522.png)
   *Modifier le paramètre*

## Suppression d’un paramètre

Les administrateurs peuvent supprimer un paramètre en cliquant sur l&#39;icône représentant trois points et en sélectionnant **[!UICONTROL Supprimer le paramètre]**. Les administrateurs peuvent supprimer un paramètre s’il n’est pas lié à des objets d’apprentissage. S’il est lié, ils peuvent uniquement masquer le paramètre. Cependant, ils ne peuvent pas masquer les deux derniers paramètres car au moins deux paramètres sont nécessaires pour que les recommandations fonctionnent.

![supprimer le paramètre](assets/delete-parameter.png)
*Supprimer le paramètre*

## Page Paramètres du cours

Sur la page des paramètres d’un cours, la recommandation pour les produits et les rôles est répertoriée. Ce cours sera recommandé aux élèves s’ils ont exprimé leur intérêt pour ces produits et ces rôles.

![définition de l&#39;image](assets/course-settings-image.png)
*Page des paramètres du cours*

## Vue Élève

Si les recommandations basées sur PRL sont configurées sur un compte, un workflow guidé permet à l’élève de configurer les recommandations en fonction du produit, du rôle et des préférences de niveau appropriées lorsqu’il se connecte à la plateforme d’apprentissage. Le profil d’élève est ainsi créé et analysé par le moteur de recommandation

Les élèves dont les comptes ont basculé vers le nouveau système de recommandation peuvent afficher les cours et les formations recommandés.

Les élèves peuvent voir les éléments suivants :

* Produits, rôles - niveaux : les élèves sont invités à sélectionner d’abord des produits, des rôles, puis des niveaux pour chacun des rôles sélectionnés.
* Produit - niveaux : les élèves sont invités à sélectionner d’abord des produits, puis des niveaux pour chacun des produits sélectionnés.
* Rôles - niveaux : les élèves sont invités à sélectionner d’abord des rôles, puis des niveaux pour chacun des rôles sélectionnés.
* Produits et rôles : les élèves sont invités à sélectionner d’abord des produits, puis des rôles.
* Produits : les élèves sont invités à sélectionner uniquement des produits.
* Rôles : les élèves sont invités à sélectionner uniquement des rôles.

Lorsque l’élève sélectionne Recommandations dans le panneau de gauche, une fenêtre contextuelle s’affiche permettant de configurer les recommandations.

![recommandations de configuration](assets/image575540.png)
*L&#39;élève configure la recommandation*

En cliquant sur Configurer les recommandations, l’élève accède à la fenêtre contextuelle de sélection de produits.

![fenêtre contextuelle de sélection de produit](assets/product-selection-popup.png)
*Sélectionner des produits*

Dans la fenêtre contextuelle suivante, l’élève peut sélectionner le rôle.

![sélectionner un rôle](assets/image270860.png)
*Sélectionner des rôles*

L’élève peut ensuite ajouter les niveaux.

![ajouter des niveaux](assets/image650040.png)
*Sélectionner des niveaux*

## Bandes liées à l’apprentissage sur l’application de l’élève

Un élève peut voir les bandes suivantes sur l’application :

* Bande Mon apprentissage
* Bande avec calendrier, réseaux sociaux et widget de ludification
* Bande Enregistré par moi
* Bande Très pertinent
* Bande de produit - 1
* Bande de produit - 2
* Bande Découverte
* Bande Recommandé par l’administrateur
* Bande Rechercher par catalogue

### Cartes sur mon support d’apprentissage

![cartes de bandes d’apprentissage](assets/image770606.png)
*Cartes sur bande d&#39;apprentissage*

Chaque carte indique une note, une image, un titre, une compétence, une date de publication, un auteur, une durée, une barre de progression et un bouton Continuer ou Explorer.

### Cartes enregistrées par moi

![cartes enregistrées](assets/cards-saved-by-me.png)
*Cartes enregistrées*

Chaque carte indique une note, une image, un titre, une compétence, une date de publication, un auteur, une durée, une barre de progression et un bouton Démarrer, Explorer, Continuer ou Revoir.

La carte ne comporte pas de barre de progression une fois que l’élève a commencé le cours. Un élève peut également annuler l’enregistrement du cours.

### Cartes sur la bande super pertinente

![cartes à bande très pertinentes](assets/super-relevant-cards.png)
*Cartes pertinentes*

Chaque carte indique une note, une image, un titre, une compétence, une date de publication, un auteur, une durée, une barre de progression et un bouton Démarrer, Explorer, Continuer ou Revoir.

La carte ne comporte pas de barre de progression une fois que l’élève a commencé le cours.

Dans le menu, il y a deux options : **[!UICONTROL Enregistrer]** et **[!UICONTROL Ne pas recommander]**. Si l&#39;élève clique sur **[!UICONTROL Enregistrer]**, le cours est enregistré dans la barre « Enregistré par moi ». Si l&#39;élève clique sur **[!UICONTROL Ne pas recommander]**, la formation recommandée est supprimée de la liste.
