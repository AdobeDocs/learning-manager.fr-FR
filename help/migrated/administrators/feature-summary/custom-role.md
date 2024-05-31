---
jcr-language: en_us
title: Rôles personnalisés
description: La fonctionnalité Parcours d’apprentissage vous aide à définir des rôles personnalisés et à affecter des responsabilités spécifiques à un ensemble d’utilisateurs. Cette fonction vous permet d'attribuer des responsabilités en dehors du rôle existant de la personne.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: 6862dc1958a34a369f0e0e7218f28151a47beb3b
workflow-type: tm+mt
source-wordcount: '2223'
ht-degree: 65%

---

# Rôles personnalisés

Cette fonctionnalité vous aide à définir des rôles personnalisés et à affecter des responsabilités spécifiques à un ensemble d’utilisateurs. Cette fonction vous permet d&#39;attribuer des responsabilités en dehors du rôle existant de la personne.

Vous pouvez créer un rôle personnalisé pour fournir des fonctionnalités de création limitées à un catalogue particulier. Vous pouvez également créer un rôle dédié à la gestion des rapports. Ces rôles peuvent ensuite être affectés à des personnes qui sont censées assumer ces responsabilités spécifiques.

## Création d’un rôle personnalisé {#create-role}

1. Connectez-vous en tant qu’administrateur. Ouvrir **[!UICONTROL Utilisateurs]** > **[!UICONTROL Rôle personnalisé]**.
1. Sélectionner **[!UICONTROL Créer un rôle]**. L’onglet **[!UICONTROL Créer un rôle]** s’ouvre.

   ![](assets/create-new-role.png)

   *Créer un rôle personnalisé*

1. Saisissez le nom dans le champ **[!UICONTROL Nom du rôle]** champ.
1. **[!UICONTROL Privilèges de compte]**: ces privilèges donnent aux propriétaires des rôles l’accès à des aspects spécifiques de la configuration du système et qui agissent sur l’ensemble du compte. Choisissez les autorisations d’accès. L’utilisateur obtient le contrôle total sur les autorisations affectées.

>[!NOTE]
>
>   La portée ne s’applique pas à ces privilèges.


![](assets/account-privileges.png)

*Définir la portée*

1. **Droits de fonctionnalités - fonctionnalités de base**: utilisé pour accorder l’accès à des fonctionnalités spécifiques de gestion des activités d’apprentissage. Les autorisations sur les fonctionnalités suivantes peuvent être accordées à l’aide de cette option.

   * Catalogues
   * Rapports
   * Balises

   ![](assets/core-features.png)

   *Définir l&#39;étendue des catalogues, rapports et balises*

1. **Droits de fonctionnalité - Objets d’apprentissage :**  Utilisez cette option pour donner accès aux fonctionnalités liées aux objets d’apprentissage. Vous pouvez fournir l’accès aux objets d’apprentissage suivants.

   * Certifications
   * Cours
   * Assistances à la tâche
   * Programmes d’apprentissage

   Vous pouvez également accorder un contrôle d’opération spécifique pour les objets d’apprentissage. L’autorisation peut être l’une des suivantes :

   * Contrôle complet
   * Modifier et supprimer
   * Inscription
   * Rapport

   ![](assets/learning-objects.png)

   *Octroi d’autorisations spécifiques*

1. **Portée des privilèges de fonctionnalité :** La portée des privilèges de fonctionnalité alloués à ce rôle peut être limitée à un groupe d’utilisateurs spécifique ou à un ou plusieurs catalogues.

   Catalogues : utilisez le bouton radio pour contrôler **[!UICONTROL Tous les catalogues]** ou utilisez l’option **[!UICONTROL Définir l’accès par catalogue]** pour donner accès à des catalogues spécifiques. Vous pouvez également sélectionner plusieurs catalogues.

   Groupes d’utilisateurs : fournissez un accès à **[!UICONTROL Tous les groupes d’utilisateurs]** ou utilisez l’option **[!UICONTROL Définir l’accès par groupe d’utilisateurs]** pour donner accès à des groupes d’utilisateurs spécifiques. Un seul groupe d’utilisateurs peut être spécifié.

   >[!NOTE]
   >
   >Si vous avez sélectionné Annonce, Ludification, Modèles d’e-mail, Compétences et Utilisateurs sous Privilèges de compte, l’accès Groupe d’utilisateurs est fourni à tous les groupes d’utilisateurs par défaut et cette option est désactivée.

   Si vous avez sélectionné Programmes d’apprentissage sous Droits du compte, l’accès à tous les catalogues et aux groupes d’utilisateurs est fourni par défaut et ces options sont désactivées sous Portée.

   ![](assets/define-scope-of-privileges.png)

   *Définition de l’étendue des privilèges*

>[!NOTE]
>
>   Dans Learning Manager 27.6, vous pouvez créer un rôle personnalisé dont la portée s’étend à plusieurs catalogues disposant chacun d’ensembles d’autorisations différents.


Pour accorder différentes autorisations aux catalogues, suivez les étapes ci-dessous :

1. Cliquez sur l’option **[!UICONTROL Définir l’accès par catalogue]**.
1. Choisissez les catalogues. Vous pouvez voir le niveau d’autorisation pour chaque catalogue. Les autorisations sont les suivantes :

   <table>
        <tbody>
        <tr>
          <td>
          <p><b>Autorisation</b></p></td>
          <td>
          <p><b>Description</b></p></td>
        </tr>
        <tr>
          <td>
          <p>Contrôle complet</p></td>
          <td>
          <p>Accorde un contrôle complet sur tous les objets d’apprentissage. Les autorisations incluent Ajouter, Modifier, Supprimer, Lire, Inscrire et Rapport.<br></p></td>
        </tr>
        <tr>
          <td>
          <p>Rapport</p></td>
          <td>
          <p>Accorde uniquement l’accès à l’onglet Rapports de l’objet d’apprentissage.</p></td>
        </tr>
        <tr>
          <td>
          <p>Inscrire</p></td>
          <td>
          <p>Accorde uniquement l’autorisation de s’inscrire à l’objet d’apprentissage.</p></td>
        </tr>
        <tr>
          <td>
          <p>Lecture seule</p></td>
          <td>
          <p>Accorde uniquement l’autorisation d’afficher les objets d’apprentissage dans le catalogue.</p></td>
        </tr>
        </tbody>
      </table>

1. Activez ou désactivez les autorisations conformément à vos exigences.
1. Cliquez sur **[!UICONTROL OK]** pour enregistrer les modifications. Ensuite, pour enregistrer les modifications pour le rôle personnalisé, cliquez sur **[!UICONTROL Enregistrer]**.

Par exemple, considérons le scénario suivant.

L’autorisation résultante qu’un utilisateur personnalisé aurait sur un objet d’apprentissage est une combinaison de l’autorisation de l’objet d’apprentissage et de l’autorisation du catalogue.

Un utilisateur personnalisé a une autorisation complète pour les cours, un accès en lecture seule seulement pour le catalogue A et une autorisation complète pour le catalogue B. Il aura donc un accès en lecture seule aux cours du catalogue A et le contrôle complet sur les cours du catalogue B.

Un utilisateur avec un rôle personnalisé peut :

* afficher le contenu des catalogues auxquels il a accès uniquement ;
* accéder à n’importe quel objet d’apprentissage conformément aux autorisations du catalogue dont l’objet d’apprentissage fait partie.

  En tant qu’administrateur, vous pouvez :

* choisir plus d’un catalogue pour un rôle personnalisé ;
* modifier les autorisations d’un catalogue à tout moment ;
* supprimer les catalogues d’une portée à laquelle vous ne souhaitez plus accorder d’autorisations ;
* accorder implicitement l’autorisation Lecture seule à un catalogue lorsque vous accordez des autorisations au catalogue.

  Le tableau ci-dessous illustre la façon dont les autorisations sont accordées.

  <table>
    <tbody>
     <tr>
      <td>
       <p><strong> </strong></p></td>
      <td>
       <p><strong>Autorisation au niveau du catalogue</strong></p></td>
     </tr>
     <tr>
      <td>
       <p><strong>Autorisation au niveau de l’objet d’apprentissage</strong></p>
       <p><strong>(Ex : cours)</strong></p></td>
      <td>
       <p>Contrôle complet</p></td>
      <td>
       <p>Inscrire</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Lecture seule</p></td>
     </tr>
     <tr>
      <td>
       <p>Contrôle complet</p></td>
      <td>
       <p>Contrôle complet</p></td>
      <td>
       <p>Inscrire</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Lecture seule</p></td>
     </tr>
     <tr>
      <td>
       <p>Inscrire</p></td>
      <td>
       <p>Inscrire</p></td>
      <td>
       <p>Inscrire</p></td>
      <td>
       <p>Lecture seule</p></td>
      <td>
       <p>Lecture seule</p></td>
     </tr>
     <tr>
      <td>
       <p>Modifier et supprimer</p></td>
      <td>
       <p>Modifier et supprimer</p></td>
      <td>
       <p>Lecture seule</p></td>
      <td>
       <p>Lecture seule</p></td>
      <td>
       <p>Lecture seule</p></td>
     </tr>
     <tr>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Lecture seule</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Lecture seule</p></td>
     </tr>
    </tbody>
   </table>

1. **Utilisateurs :** utilisez cette option pour déterminer les utilisateurs auxquels ce rôle est affecté. Vous pouvez choisir un ou plusieurs utilisateurs à l’aide de la zone de recherche.

   **Ajouter des utilisateurs au chargement CSV de rôle personnalisé :** Pour ajouter des utilisateurs via le chargement CSV, ajoutez une colonne CustomRole au fichier .csv que l’administrateur a utilisé pour importer des utilisateurs. Saisissez le rôle de l’utilisateur dans la colonne CustomRole pour les utilisateurs auxquels vous souhaitez attribuer un rôle personnalisé. Pour charger le fichier CSV, cliquez sur  **[!UICONTROL Ajouter > Charger un fichier CSV]**.

   CustomRole columnNote :

* Vous ne pouvez pas rechercher des groupes d’utilisateurs.
* Vous ne pouvez pas rechercher les utilisateurs auxquels le rôle d’administrateur a déjà été affecté.
* L’affectation d’un nouveau rôle personnalisé à un utilisateur remplace le rôle personnalisé précédent de l’utilisateur.

  <!--![](assets/users.png)-->

* Un administrateur personnalisé ayant l’autorisation d’accéder à Paramètres pourra configurer la planification pour la synchronisation ou synchroniser les utilisateurs à partir de la source de données même s’ils n’ont pas l’autorisation d’accéder à l’entité Utilisateurs.
* Si un administrateur personnalisé dispose d’une autorisation pour l’entité Utilisateurs, il peut s’affecter un rôle d’administrateur et devenir un administrateur standard.

## Restreindre l&#39;accès aux dossiers aux auteurs personnalisés {#folder-custom-author}

Learning Manager prend déjà en charge la possibilité de donner accès à la bibliothèque de contenu à l’aide de rôles personnalisés. Tous les auteurs personnalisés qui ont déjà accès à la bibliothèque de contenu continueront d’avoir accès à tous les fichiers de contenu même après la configuration des dossiers de contenu. Cette approche vise à conserver l&#39;ancien comportement. Les administrateurs n’ont pas besoin d’apporter de modifications s’ils souhaitent continuer à adopter le comportement actuel.

S’ils souhaitent restreindre l’accès à ces auteurs personnalisés, les administrateurs doivent modifier le rôle personnalisé existant et le configurer en ne donnant accès qu’à des dossiers de contenu spécifiques.

![](assets/folder-access-forcustomauthors.png)

*Restreindre l’accès aux dossiers aux auteurs personnalisés*

Lorsque vous créez un auteur personnalisé, vous pouvez désormais lui attribuer des dossiers de contenu. Choisir l’option **Dossiers sélectionnés**.

Lorsque vous cliquez sur l&#39;option, une nouvelle boîte de dialogue s&#39;ouvre, dans laquelle vous pouvez attribuer les dossiers à l&#39;auteur personnalisé.

![](assets/choose-folder.png)

*Sélectionner les dossiers de l’auteur personnalisé*

Sélectionnez les dossiers et cliquez sur **[!UICONTROL OK]**.

## Tableau de bord récapitulatif des apprentissages pour un administrateur personnalisé {#custom-admin-dashboard}

Les administrateurs personnalisés peuvent afficher la même vue que les autres utilisateurs. Un administrateur personnalisé peut stocker des données en dehors de son périmètre. Cela s’applique uniquement si l’administrateur personnalisé a une portée complète. Pour accorder une portée complète, lors de la création d’un administrateur personnalisé, activez l’option **[!UICONTROL Contrôle total]** dans Rapport récapitulatif du compte.

![](assets/create-custom-role.png)

*Créer un rôle personnalisé*

Par conséquent, les options, **[!UICONTROL Tous les catalogues]** et **[!UICONTROL Tous les groupes d’utilisateurs]** sera sélectionné et le reste désactivé.

![](assets/scope-of-featureprivileges.png)

*Définition de l’étendue des privilèges*

## Autorisations implicites {#implicitpermissions}

Lorsqu&#39;un utilisateur se voit attribuer un rôle avec une entité spécifique, il peut y avoir des cas où il a besoin d&#39;accéder à d&#39;autres entités également pour pouvoir effectuer des tâches sur l&#39;entité accordée. Par exemple, si un utilisateur dispose d’un accès Créer sur l’entité Cours, il doit avoir accès aux entités Compétence et Balise afin de pouvoir les associer au cours en cours de création. Ce tableau fournit des informations sur ces autorisations implicites.

<table>
 <tbody>
  <tr>
   <th>Type d’accès</th>
   <th>Autorisation pour l’entité accordée par l’administrateur</th>
   <th>Autorisations implicites pour l’entité</th>
   <th>Accès implicite</th>
  </tr>
  <tr>
   <td>Gérer</td>
   <td>Utilisateur</td>
   <td>Groupe</td>
   <td>Crud</td>
  </tr>
  <tr>
   <td>Inscrire</td>
   <td>Tous les objets d’apprentissage (cours, assistance à la tâche, programme d’apprentissage, certification)</td>
   <td>Utilisateur<br>
     Plan d’apprentissage</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>
    <p>Groupe de contenus<br>
      Assistance à la tâche<br></p></td>
   <td>Balise</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>Cours</td>
   <td>Groupe de contenus<br>
     Balise<br>
     Compétence<br>
     Badge<br>
     Assistance à la tâche</td>
   <td>Lire tout</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>Programme d’apprentissage<br>
     Certification<br></td>
   <td>Cours<br>
     Balise<br>
     Compétence<br>
     Badge</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>Programme d’apprentissage</td>
   <td>Catalogue<br>
     Groupe<br>
     Compétence<br>
     Toutes les pertes (cours, aide à l'emploi, programme d'apprentissage, certification)</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>Annonce</td>
   <td>Utilisateur<br>
     Groupe<br>
     Toutes les pertes (cours, aide à l'emploi, programme d'apprentissage, certification)</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>Ludification</td>
   <td>Identité visuelle</td>
   <td>Écrire</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Utilisateur</td>
   <td>Facturation</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Catalogue</td>
   <td>Groupe<br>
     Toutes les pertes (cours, aide à l'emploi, programme d'apprentissage, certification)</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Paramètre</td>
   <td>Branding<br>
     Utilisateur</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Identité visuelle</td>
   <td>Paramètre</td>
   <td>Lire</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Facturation<br>
     Ludification</td>
   <td>Utilisateur</td>
   <td>Lire</td>
  </tr>
 </tbody>
</table>

## Accès à un rôle personnalisé {#accessacustomrole}

Lorsqu’un administrateur attribue un rôle personnalisé, vous recevez une notification par courrier électronique.

Remarque : si vous êtes déjà connecté à Learning Manager avec un rôle personnalisé, vous devez vous reconnecter à Learning Manager pour accéder au nouveau rôle.

Pour changer de rôle, cliquez sur l’icône de votre profil en haut à droite de Learning Manager et sélectionnez le rôle.

## Portée des plans d&#39;apprentissage définie en fonction de rôles configurables {#scopeconfigure}

Dans les versions antérieures de Learning Manager, tout rôle personnalisé autorisé à créer des plans d’apprentissage pouvait étendre le plan d’apprentissage à tous les types de groupes d’utilisateurs et d’objets d’apprentissage.

Le paramètre d&#39;étendue était désactivé lorsque l&#39;accès au plan d&#39;apprentissage était accordé, ce qui donnait à l&#39;utilisateur l&#39;accès à Tous les catalogues et Tous les groupes d&#39;utilisateurs par défaut.

Tous les plans d’apprentissage créés par un administrateur s’appliquent par défaut à tous les utilisateurs. Les utilisateurs peuvent également se voir attribuer n’importe quel objet d’apprentissage. D’un autre côté, les utilisateurs avec des rôles personnalisés bénéficient d’un accès complet, par exemple à tous les catalogues, objets d’apprentissage ou groupes d’utilisateurs. Cela signifiait que les administrateurs n’étaient pas en mesure de créer des rôles personnalisés comme prévu, ce qui aurait permis aux utilisateurs bénéficiant d’une portée limitée d’accéder aux plans d’apprentissage.

Avec cette mise à jour de Learning Manager, vous pouvez créer des rôles personnalisés pour les plans d’apprentissage qui permettent de définir leur portée en ce qui concerne les utilisateurs et les objets d’apprentissage. En d&#39;autres termes, les plans d&#39;apprentissage peuvent être créés avec une portée limitée dérivée de la portée d&#39;un rôle d&#39;administrateur personnalisé.

Un administrateur peut désormais définir ou restreindre la portée tout en accordant un accès en tant que responsable du plan d&#39;apprentissage.

Les administrateurs personnalisés peuvent créer des plans d’apprentissage avec une portée limitée, déterminée par la portée du rôle configurable de l’administrateur personnalisé. Ces plans d’apprentissage ne sont accessibles qu’aux administrateurs personnalisés ayant le même rôle, en plus d’être accessibles aux administrateurs réguliers. De plus, les administrateurs personnalisés ne peuvent voir aucun autre plan d’apprentissage dans le compte.

Les administrateurs personnalisés existants ayant accès aux plans d’apprentissage bénéficieront toujours d’une portée complète (par définition). Ils auront accès à tous les plans d’apprentissage du compte, comme les administrateurs habituels. De nouveaux rôles personnalisés créés avec une portée complète et de nouveaux administrateurs personnalisés ajoutés à ces rôles continueront d’avoir accès à tous les plans d’apprentissage.

Les plans d’apprentissage créés par les administrateurs et les administrateurs personnalisés bénéficiant d’une portée complète seront créés comme d’habitude et ne seront pas limités par la portée.

Dans la section **Portée des droits de fonctionnalités**, accordez l’accès aux groupes d’utilisateurs et/ou au catalogue pour le rôle personnalisé.

![](assets/scope-for-featureprivileges.png)

*Octroyer l’accès aux groupes d’utilisateurs et/ou au catalogue pour le rôle personnalisé*

Attribuez un utilisateur au rôle personnalisé.

![](assets/assign-users-to-customrole.png)

*Affectation d’un utilisateur à un rôle personnalisé*

L’utilisateur se connecte désormais à Learning Manager en tant qu’administrateur personnalisé et ajoute un plan d’apprentissage.

Lorsqu’un nouvel élève est ajouté, l’administrateur personnalisé peut sélectionner une formation uniquement dans le rôle configurable dont la portée s’étend à plusieurs catalogues.

Ce plan d&#39;apprentissage ne s&#39;applique désormais à l&#39;élève que si l&#39;utilisateur est également ajouté au groupe au sein du groupe d&#39;utilisateurs de la portée du plan d&#39;apprentissage. Tous les autres élèves sont exemptés de ce plan d’apprentissage.

## L’élève est ajouté au groupe {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

L’administrateur personnalisé peut sélectionner n’importe quel groupe d’utilisateurs qui a des utilisateurs dans le groupe d’utilisateurs concerné.

Lorsqu’un utilisateur est ajouté au groupe spécifié, seuls les utilisateurs qui font déjà partie du groupe d’utilisateurs du plan d’apprentissage et qui ont été ajoutés au groupe d’utilisateurs spécifié se verront attribuer l’objet d’apprentissage.

## Modification de la portée {#changeinscope}

Lorsque l’administrateur modifie la portée du rôle personnalisé, la modification se répercute également sur l’administrateur personnalisé. Lorsque l’administrateur personnalisé choisit un plan d’apprentissage qui était déjà défini par un rôle personnalisé précédent, un message s’affiche, comme illustré ci-dessous :

![](assets/change-scope.png)

*Message après les modifications de l’étendue*

L’administrateur personnalisé doit maintenant mettre à jour ou actualiser la portée précédente vers la nouvelle portée.

Il suffit de cliquer sur **[!UICONTROL Actualiser la portée]** pour mettre à jour la portée. Un message d’avertissement s’affiche.

![](assets/refresh-scope-message.png)

*Message d’avertissement après l’actualisation d’une portée*

Il suffit de cliquer sur **[!UICONTROL Oui]** pour mettre à jour la portée.

## Ajouter un rapport de ludification à un rôle personnalisé {#gamification-custom}

Un administrateur peut activer les rapports de ludification pour un utilisateur personnalisé.

1. Dans la page **[!UICONTROL Rôles personnalisés]**, saisissez le nom du rôle personnalisé.
1. Dans le panneau **[!UICONTROL Privilèges de fonctionnalité : fonctionnalités principales]** section, activer l’option **[!UICONTROL Contrôle total]** pour la catégorie **[!UICONTROL Rapports]**.

1. Dans la section **[!UICONTROL Utilisateurs]**, sélectionnez l’utilisateur auquel sera attribué le rôle personnalisé nouvellement créé.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

Lorsqu’un utilisateur se connecte en tant qu’administrateur personnalisé et clique sur **[!UICONTROL Rapports]** dans le volet de gauche, les relevés de notes apparaissent, comme illustré ci-dessous :

![](assets/download-gamificationtranscripts.png)

*Télécharger les transcriptions de ludification*

Cliquez sur **[!UICONTROL Relevés de notes de ludification]**, choisissez un utilisateur et générez le rapport.

Si un administrateur modifie les points de niveau, les rapports affichent les niveaux en fonction des points actuels.

La réinitialisation de la ludification ne réinitialise pas la date à laquelle le niveau a été atteint.

## Forum aux questions {#frequentlyaskedquestions}

+++Comment créer un rôle personnalisé ?

Un rôle personnalisé est semblable à un sous-ensemble d’un rôle d’auteur ou d’administrateur. Autoriser un ou plusieurs privilèges, définir la portée et attribuer le rôle à un utilisateur.

Cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Rôles personnalisés]**. Dans la page Rôles personnalisés, cliquez sur **[!UICONTROL Créer un rôle]**. Entrez le nom du rôle personnalisé et définissez les privilèges du rôle. Pour plus d’informations, voir [Création d’un rôle personnalisé](custom-role.md#create-role).
+++
