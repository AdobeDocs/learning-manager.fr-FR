---
title: Créer des couches
description: Découvrez comment activer, créer et modifier des canaux dans Adobe Learning Manager pour regrouper le contenu d’apprentissage vidéo à partir de pages web et de pages Confluence Cloud dans un emplacement unique et indexable pour les élèves.
source-git-commit: 362d56b5758d55e7aa564893beade853f4c72deb
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%

---


# Créer des couches

Les organisations stockent souvent des sessions de partage de connaissances, des enregistrements de formation et d&#39;autres contenus vidéo sur des contenus d&#39;apprentissage informels organisés sur le web et des pages Confluence Cloud. Les canaux connectent Adobe Learning Manager à ces sources de contenu, ce qui facilite la découverte et l’utilisation des vidéos sans que les élèves aient à parcourir plusieurs systèmes. Les canaux vous permettent d’organiser et de partager du contenu de formation basé sur la vidéo à partir de pages Web d’entreprise et de pages Confluence Cloud dans un emplacement unique et indexable. Au lieu de parcourir plusieurs sites internes, les élèves peuvent découvrir et accéder à des enregistrements pertinents directement depuis Adobe Learning Manager. Consultez [Découvrir et interagir avec les canaux](../../learners/feature-summary/discover-and-engage-with-channels.md) pour plus d&#39;informations.

En tant qu’administrateur, vous pouvez créer et gérer des canaux, configurer les paramètres de visibilité, synchroniser le contenu avec sa source et vérifier que les vidéos sont disponibles avant de rendre le canal accessible aux élèves. Cet article explique comment effectuer ces tâches de gestion des canaux.

**Principaux avantages**

- Consolidez le contenu d’apprentissage basé sur la vidéo à partir de plusieurs sources internes dans un seul emplacement.
- Organisez le contenu vidéo de plusieurs emplacements intranet dans des pages web, qui s’affichent ensuite en tant que canaux dans ALM.
- Permettre aux élèves de rechercher, de jouer et d’interagir avec le contenu sans accéder à plusieurs sites.
- Gardez le contenu synchronisé avec sa source d’origine.

## Activer les canaux

Canaux est une fonctionnalité que les administrateurs activent pour le compte. Une fois cette option activée, vous pouvez créer des canaux qui se connectent à des pages web d’entreprise et à des pages de convergence cloud contenant du contenu vidéo.

L’analyseur de liens de canaux extrait de manière fiable les vidéos des pages sources qui présentent leur contenu dans les formats suivants :

- Tableaux
- Listes à puces
- Articles

Pour activer la fonctionnalité **Canaux** :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.

1. Sélectionnez **Canaux** dans la navigation de gauche.
   <br> La page **Canaux** s&#39;ouvre.

1. Sélectionnez l&#39;onglet **Paramètres**.

   ![Activer la fonctionnalité Canaux](assets/enable-channels-feature.png)

   *Activez la fonctionnalité Canal dans l&#39;onglet **Paramètres**&#x200B;pour permettre aux administrateurs de créer des canaux pour le compte.*

1. Activez la fonctionnalité **Canal**.

   <br> Les canaux sont activés pour le compte.

## Création d’un canal

Créez un canal pour définir la source de contenu que Adobe Learning Manager analyse pour les vidéos, et personnalisez l’apparence du canal et de la page vidéo.

1. Accédez à l’onglet **Canaux** et sélectionnez **Ajouter un canal**.
   <br> La page **Créer un canal** s&#39;ouvre.

   ![Créer une source de contenu de canal](assets/create-channel-content-source.png)

   *Définissez la source de contenu et configurez les options de visibilité et de synchronisation lors de la création d’un canal.*

1. Dans la section **Canal**, saisissez le **Nom du canal** et la **Description**.

1. Sélectionnez un **type de source** dans le menu déroulant. Les options suivantes sont disponibles :

   1. **Page web** : sélectionnez cette option pour analyser une page web et importer des liens vidéo avec leurs métadonnées associées.

   1. **Page Confluence** : sélectionnez cette option pour récupérer les liens vidéo et les métadonnées d&#39;une page Confluence Cloud. Pour vous connecter à Confluence Cloud, fournissez les informations suivantes :
      - **Adresse e-mail atlassienne** : entrez l&#39;adresse e-mail associée à votre compte atlassien.
      - **Jeton API Atlassian** : entrez le jeton API généré à partir de votre compte Atlassian. Sélectionnez **Comment créer un jeton API** pour obtenir des instructions sur la génération d&#39;un jeton. Ce jeton est utilisé pour l&#39;authentification lors de l&#39;analyse de la source et est stocké chiffré.

      ![Page de confluence du cloud](assets/cloud-confluence-page.png)

      *Entrez l’adresse e-mail et le jeton API Atlassian utilisés pour l’authentification auprès de Confluence Cloud.*

1. Entrez l&#39;**URL source** du contenu du type de source sélectionné.

1. Dans la section **État**, configurez les options suivantes :

   1. **Visible par les élèves** : activez cette option pour rendre le canal disponible pour les élèves. Désactivez-le pour masquer le canal pendant que vous continuez à le configurer ou à le tester.

   1. **Synchroniser automatiquement** : activez cette option pour mettre à jour automatiquement le canal lorsque de nouvelles vidéos sont ajoutées à la source. Désactivez-la si vous souhaitez synchroniser manuellement le canal.

1. (Facultatif) Sélectionnez **Afficher les paramètres avancés**, puis configurez les options suivantes selon vos besoins :

   1. **Couleur du thème de la couche** : sélectionnez une couleur pour personnaliser l&#39;apparence visuelle de la couche.

   1. **Profondeur d&#39;analyse** : entrez la profondeur d&#39;analyse pour les pages liées à analyser pour le contenu vidéo. Il prend en charge une profondeur d&#39;analyse maximale de **2**.

   1. **Fréquence d&#39;analyse (en heures)** : entrez la fréquence à laquelle Adobe Learning Manager doit vérifier la source pour le contenu nouveau ou mis à jour.

      ![Planification de la vérification du contenu du canal](assets/channel-content-check-schedule.png)

      *Sélectionnez Afficher les paramètres avancés pour configurer la couleur du thème de canal, la profondeur d&#39;analyse et la fréquence d&#39;analyse.*

1. Sélectionnez **Tester maintenant** pour valider la source. Les exemples de vidéos sont récupérés et affichés à partir de la source configurée.

   ![Tester la connexion source du canal](assets/test-channel-source-connection.png)

   *Utilisez **Tester maintenant**&#x200B;pour confirmer que les vidéos sont récupérées à partir de la source avant de créer le canal.*

1. Sélectionnez **Créer un canal**. Le canal est créé et ajouté à la liste **Canaux**.

## Recherche d’un canal

Utilisez la zone de recherche pour localiser rapidement un canal par son nom.

1. Sélectionnez l&#39;onglet **Canaux**.
1. Sélectionnez la zone **Rechercher des canaux**.
1. Entrez le nom du canal ou une partie de celui-ci dans la zone **Rechercher des canaux**.
   <br> La liste filtre pour afficher uniquement les canaux qui correspondent à votre recherche.

   ![Rechercher des canaux](assets/search-channels.png)

   *Entrez un nom de canal dans la zone de recherche pour filtrer la liste **Canaux**.*

## Gestion de la visibilité des canaux

Utilisez le menu **Actions** pour désactiver ou masquer un ou plusieurs canaux simultanément.

### Désactiver les canaux

Désactivez un ou plusieurs canaux pour empêcher les élèves d’accéder à leur contenu tout en conservant la configuration des canaux.

Pour désactiver les canaux :

1. Accédez à **Canaux**.
1. Cochez la case en regard d&#39;un ou de plusieurs canaux, puis sélectionnez **Actions**.

   ![Sélectionnez Désactiver dans le menu Actions pour désactiver un ou plusieurs canaux sélectionnés.](assets/disable-channels.png)
   *Sélectionnez Désactiver dans le menu Actions pour désactiver un ou plusieurs canaux sélectionnés.*
1. Sélectionnez **Désactiver**.<br> La fenêtre contextuelle **Désactiver les canaux** s&#39;affiche.
1. Sélectionnez **Désactiver**.<br> Les canaux sélectionnés sont désactivés.

### Masquer les canaux aux élèves

Masquez un ou plusieurs canaux pour les rendre indisponibles pour les élèves sans les supprimer.

Pour masquer les canaux aux élèves :

1. Accédez à **Canaux**.
1. Cochez la case en regard d&#39;un ou de plusieurs canaux, puis sélectionnez **Actions**.
1. Sélectionnez **Masquer aux élèves**.<br> La fenêtre contextuelle **Masquer aux élèves** s&#39;affiche.

   ![Masquer les canaux aux élèves sans supprimer la configuration des canaux.](assets/hide-channels-from-learners.png)
   *Masquer les canaux aux élèves sans supprimer la configuration des canaux.*

1. Sélectionnez **Masquer aux élèves**.
   <br> Les canaux sélectionnés sont masqués aux élèves.

## Modification d’un canal

Vous pouvez modifier un canal existant pour mettre à jour sa configuration et ses paramètres.

Pour modifier un canal :

1. Sélectionnez le canal requis dans la liste **Canaux**.
   <br> La page **Modifier le canal** s&#39;ouvre et affiche la configuration de canal actuelle.

1. Mettez à jour les paramètres de canal selon vos besoins.

   ![Modifier les paramètres de canal](assets/edit-channel-settings.png)

   *Mettez à jour le nom, la description, la source et les paramètres d&#39;un canal à partir de la page **Modifier le canal**.*

1. (Facultatif) Sélectionnez **Tester maintenant**.

1. Sélectionnez **Enregistrer les modifications**.
   <br> Les paramètres de canal mis à jour sont enregistrés.

## Suppression d’un canal

Vous pouvez supprimer un ou plusieurs canaux qui ne sont plus nécessaires.

1. Accédez à l&#39;onglet **Canaux**.

1. Cochez la case en regard de chaque canal à supprimer.

1. Sélectionnez **Supprimer** en bas à droite de la liste des canaux. <br> La fenêtre contextuelle **Supprimer des canaux** s&#39;affiche.

   ![Supprimer les canaux](assets/delete-channels.png)

   *Une boîte de dialogue de confirmation répertorie les canaux que vous avez sélectionnés.*

1. Sélectionnez **Supprimer**.
   <br> Les canaux sélectionnés sont définitivement supprimés. Cette action est irréversible.
