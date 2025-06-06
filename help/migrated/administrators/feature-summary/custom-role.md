---
jcr-language: en_us
title: Rôles personnalisés
description: La fonctionnalité Parcours d’apprentissage vous aide à définir des rôles personnalisés et à affecter des responsabilités spécifiques à un ensemble d’utilisateurs. Cette fonction vous permet d'attribuer des responsabilités en dehors du rôle existant de la personne.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: 7c21986eff480f15cb788cf9a1cb51644bc083c8
workflow-type: tm+mt
source-wordcount: '3466'
ht-degree: 32%

---

# Rôles personnalisés

Cette fonctionnalité vous aide à définir des rôles personnalisés et à affecter des responsabilités spécifiques à un ensemble d’utilisateurs. Cette fonction vous permet d&#39;attribuer des responsabilités en dehors du rôle existant de la personne.

Vous pouvez créer un rôle personnalisé pour fournir des fonctionnalités de création limitées à un catalogue particulier. Vous pouvez également créer un rôle dédié à la gestion des rapports. Ces rôles peuvent ensuite être affectés à des personnes qui sont censées assumer ces responsabilités spécifiques.

>[!NOTE]
>
>L’ajout d’un nouveau rôle personnalisé n’affectera pas les groupes d’utilisateurs personnalisés existants ni les groupes basés sur des rôles tels que Tous les administrateurs, Tous les auteurs, etc.

Les administrateurs peuvent créer des rôles d’administrateur et d’auteur personnalisés avec des autorisations personnalisées pour chaque rôle. Vous trouverez ci-dessous un aperçu des autorisations associées à chaque rôle :

**Autorisations Personnalisées Du Rôle D&#39;Auteur**

Les auteurs personnalisés peuvent effectuer les tâches suivantes :

* Accédez à la bibliothèque de contenu pour ajouter, modifier ou supprimer du contenu de base.
* Créer, modifier et supprimer :
   * Cours
   * Assistances à la tâche
   * Certifications
   * Parcours d’apprentissage
   * Plans d’apprentissage

Les administrateurs et les auteurs, y compris les administrateurs et les auteurs personnalisés, pourront partager des objets d’apprentissage avec des catalogues partagés en externe. Les administrateurs et les auteurs doivent pouvoir rechercher des catalogues partagés en externe lors de la création d’objets d’apprentissage (LO).

**Autorisations personnalisées du rôle administrateur**

Le rôle d’administrateur personnalisé reproduit un ensemble de responsabilités d’administrateur, y compris l’accès aux privilèges au niveau du compte. Les administrateurs personnalisés se voient accorder des autorisations pour gérer les fonctionnalités clés liées aux activités d’apprentissage, telles que :

* Plans d’apprentissage
* Catalogues
* Rapports
* Balises

En outre, les administrateurs personnalisés peuvent :

* Gérez les cours et les assistances à la tâche, y compris l’inscription et la suppression d’utilisateurs.
* Créer, modifier et supprimer des certifications, des parcours d’apprentissage et des plans d’apprentissage.
* Accédez aux fonctionnalités de création de rapports et d’inscription pour tous les objets d’apprentissage.

Les administrateurs peuvent désormais afficher les autorisations créées par CSV dans Adobe Learning Manager. L’option Filtrer par filtre filtre les rôles personnalisés par administrateur créés et ceux importés via un fichier CSV. Après avoir sélectionné un rôle personnalisé, vous pouvez voir ses autorisations.

![](assets/filter.png)
_Filtrer les rôles personnalisés_

## Création d’un rôle personnalisé {#create-role}

1. Connectez-vous en tant qu’administrateur. Ouvrez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Rôle personnalisé]**.
2. Sélectionnez **[!UICONTROL Créer un rôle]**. L’onglet **[!UICONTROL Créer un rôle]** s’ouvre.

   ![](assets/create-new-role.png)

   *Créer un rôle personnalisé*

3. Saisissez le nom dans le champ **[!UICONTROL Nom du rôle]**.
4. **[!UICONTROL Privilèges de compte]** : ces privilèges donnent aux propriétaires des rôles l&#39;accès à des aspects spécifiques de la configuration du système et qui agissent sur l&#39;ensemble du compte. Choisissez les autorisations d’accès. L’utilisateur obtient le contrôle total sur les autorisations affectées.

   Les administrateurs peuvent accorder des autorisations détaillées pour la section Utilisateur, qui comporte des utilisateurs internes/externes, des groupes d’utilisateurs et des utilisateurs avancés.

   >[!NOTE]
   >
   >   La portée ne s’applique pas à ces privilèges.


   ![](assets/account-privileges.png)

   *Définir la portée*

5. **Droits de fonctionnalités - fonctionnalités de base** : utilisés pour accorder l’accès à des fonctionnalités spécifiques pour la gestion des activités d’apprentissage. Les autorisations sur les fonctionnalités suivantes peuvent être accordées à l’aide de cette option.

   Les administrateurs peuvent fournir des autorisations détaillées telles que des autorisations en lecture seule, de création, de modification et de suppression pour les catalogues.

   * Catalogues
   * Rapports
   * Balises

   ![](assets/core-features.png)

   *Définir l&#39;étendue des catalogues, rapports et balises*

6. **Droits de fonctionnalité - Objets d’apprentissage :** utilisez cette option pour fournir l’accès aux fonctionnalités liées aux objets d’apprentissage. Les administrateurs peuvent fournir des autorisations détaillées pour tous les objets d’apprentissage, y compris les cours, les parcours d’apprentissage, les certifications et les assistances à la tâche. Ils peuvent attribuer aux utilisateurs des autorisations telles que créer, modifier, supprimer ou un accès en lecture seule.

   * Certifications
   * Cours
   * Assistances à la tâche
   * Programmes d’apprentissage

   Vous pouvez également accorder un contrôle d’opération spécifique pour les objets d’apprentissage. L’autorisation peut être l’une des suivantes :

   * Lecture seule
   * Créer
   * Modifier
   * Supprimer
   * Inscription
   * Rapport

   Vous pouvez également accorder le contrôle total des objets d’apprentissage.

   ![](assets/learningobjects.png)

   *Octroyer des autorisations spécifiques*

7. **Portée des privilèges de fonctionnalité :** la portée des privilèges de fonctionnalité alloués à ce rôle peut être limitée à un groupe d&#39;utilisateurs spécifique ou à un ou plusieurs catalogues.

   Catalogues : utilisez le bouton radio pour contrôler **[!UICONTROL Tous les catalogues]** ou utilisez l’option **[!UICONTROL Définir l’accès par catalogue]** pour donner accès à des catalogues spécifiques. Vous pouvez également sélectionner plusieurs catalogues.

   Groupes d’utilisateurs : fournissez un accès à **[!UICONTROL Tous les groupes d’utilisateurs]** ou utilisez l’option **[!UICONTROL Définir l’accès par groupe d’utilisateurs]** pour donner accès à des groupes d’utilisateurs spécifiques. Un seul groupe d’utilisateurs peut être spécifié.

   >[!NOTE]
   >
   >Si vous avez sélectionné Annonce, Ludification, Modèles d’e-mail, Compétences et Utilisateurs sous Privilèges de compte, l’accès Groupe d’utilisateurs est fourni à tous les groupes d’utilisateurs par défaut et cette option est désactivée.

   Si vous avez sélectionné Programmes d’apprentissage sous Droits du compte, l’accès à tous les catalogues et aux groupes d’utilisateurs est fourni par défaut et ces options sont désactivées sous Portée.

   ![](assets/define-scope-of-privileges.png)

   *Définir l&#39;étendue des privilèges*

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

  En tant qu’administrateur, vous pouvez :

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

   **Ajouter des utilisateurs au chargement CSV de rôle personnalisé :** pour ajouter des utilisateurs via CSV chargé, ajoutez une colonne CustomRole au fichier .csv que l&#39;administrateur a utilisé pour importer des utilisateurs. Saisissez le rôle de l’utilisateur dans la colonne CustomRole pour les utilisateurs auxquels vous souhaitez attribuer un rôle personnalisé. Pour télécharger le fichier CSV, cliquez sur **[!UICONTROL Ajouter > Télécharger un fichier CSV]**.

   * Vous ne pouvez pas rechercher des groupes d’utilisateurs.
   * Vous ne pouvez pas rechercher des utilisateurs auxquels un rôle d’administrateur a déjà été attribué.
   * L’affectation d’un nouveau rôle personnalisé à un utilisateur remplace le rôle personnalisé précédent de l’utilisateur.

   <!--![](assets/users.png)-->

   * Un administrateur personnalisé ayant l’autorisation d’accéder à Paramètres pourra configurer la planification pour la synchronisation ou synchroniser les utilisateurs à partir de la source de données même s’ils n’ont pas l’autorisation d’accéder à l’entité Utilisateurs.
   * Si un administrateur personnalisé dispose d’une autorisation sur l’entité Utilisateurs, il peut s’attribuer un rôle d’administrateur et devenir un administrateur standard.

## Attribution de plusieurs rôles personnalisés à un utilisateur

Vous pouvez affecter plusieurs rôles personnalisés aux utilisateurs de l’une des manières suivantes :

* Utilisation de l’interface utilisateur : vous pouvez attribuer plusieurs rôles personnalisés à un utilisateur directement à partir de l’interface Adobe Learning Manager.
* Utilisation du chargement CSV : vous pouvez charger un fichier CSV pour affecter plusieurs rôles personnalisés à plusieurs utilisateurs à la fois.

Cela facilite la gestion de l’accès des utilisateurs et le contrôle des autorisations sur l’ensemble du système.

### Attribution de plusieurs rôles personnalisés via l’interface utilisateur

L’attribution de plusieurs rôles personnalisés via le Admin Console dans Adobe Learning Manager est une option rapide et intuitive idéale pour l’intégration, les réglages d’autorisation ou les mises à jour plus petites. Les rôles peuvent être attribués visuellement, sans avoir besoin de charger des fichiers CSV, ce qui réduit le risque d’erreurs et fournit une visibilité en temps réel. Cette méthode prend en charge les mises à jour rapides lorsque les responsabilités changent et permet le changement de rôle et la délégation selon les besoins.

Pour attribuer plusieurs rôles personnalisés à un utilisateur, procédez comme suit :

1. Connectez-vous en tant qu’administrateur et sélectionnez **[!UICONTROL Utilisateurs]**.
2. Sélectionnez **[!UICONTROL Rôles personnalisés]** dans le panneau de gauche.
3. Créez un nouveau rôle personnalisé et ajoutez des privilèges de compte, des catalogues, des objets d’apprentissage ou des portées. Consultez les étapes mentionnées [ici](#create-a-custom-role).
4. Ajoutez des utilisateurs au rôle personnalisé.

   ![](assets/add-users-in-custom-roles.png)
   _Affecter des utilisateurs à un rôle personnalisé_

5. Sélectionnez **[!UICONTROL Enregistrer]**.

Sélectionnez plusieurs rôles personnalisés pour un utilisateur selon vos besoins. Chaque utilisateur peut avoir jusqu’à 50 affectations de rôle personnalisées. Le nombre de rôles disponibles diminue à chaque affectation.

Après avoir affecté des utilisateurs à un rôle personnalisé supplémentaire, vous pouvez afficher le nombre d&#39;affectations de rôle qui restent disponibles pour chaque utilisateur.

>[!NOTE]
>
>Vous pouvez attribuer jusqu’à 50 rôles à chaque utilisateur et ajouter jusqu’à 500 utilisateurs à chaque rôle.

### Attribution de plusieurs rôles personnalisés à l’aide du fichier CSV

Le chargement d’un fichier CSV dans Adobe Learning Manager permet l’affectation en bloc efficace de rôles personnalisés. Ce processus est particulièrement bénéfique pour l’intégration d’un grand nombre d’employés, la réorganisation des équipes ou la mise à jour de l’accès aux nouvelles formations. Les importations CSV permettent d’économiser des efforts manuels, d’assurer la cohérence des affectations et de réduire les erreurs. Cette méthode est particulièrement utile lors des fusions, des mises à jour à l’échelle du département ou des déploiements de formations globales. Cette méthode permet aux administrateurs de gagner du temps, de standardiser les rôles et de maintenir la gouvernance.

Vous pouvez désormais attribuer plusieurs rôles à un utilisateur via l’importation CSV en chargeant deux fichiers dans Box :

* role.csv
* user_role.csv.

Le fichier user_role.csv comprend les champs Rôle personnalisé et ID utilisateur.

Le fichier role.csv comprend les champs, le rôle personnalisé, la source de création et des informations détaillées pour les catalogues, les utilisateurs, les cours, les parcours d’apprentissage, etc.

Si le fichier CSV contient des données incorrectes ou dépasse les limites (50 rôles par utilisateur et 500 utilisateurs par rôle), un message s’affiche et indique les erreurs.

![](assets/error-custom-role.png)
_Notification d&#39;erreur pour les rôles personnalisés_
Les utilisateurs reçoivent des notifications par e-mail lorsque des rôles sont attribués, y compris le nom du rôle.

### Gérer les rôles personnalisés

Les administrateurs peuvent mettre à jour, ajouter ou supprimer des rôles personnalisés pour les utilisateurs dans Adobe Learning Manager à mesure que les responsabilités changent. Cela garantit que l’accès s’aligne sur les rôles actuels sans affecter l’historique d’apprentissage ou les données d’inscription. À partir de la page **[!UICONTROL Utilisateurs]**, l&#39;administrateur peut rechercher des utilisateurs, afficher leurs rôles et les ajuster à l&#39;aide de l&#39;option Gérer les rôles personnalisés. Cette interface guidée permet d’ajouter ou de supprimer facilement des rôles tout en préservant la gouvernance et la sécurité.

>[!NOTE]
>
>Les administrateurs personnalisés ne peuvent pas gérer les rôles personnalisés (ajouter ou supprimer un rôle personnalisé) ni se promouvoir eux-mêmes au rôle d&#39;administrateur.

Après avoir attribué des rôles personnalisés aux utilisateurs, vous pouvez ajouter ou supprimer des rôles personnalisés à partir de la page **[!UICONTROL Utilisateurs]**.

1. Recherchez un utilisateur sur la page **[!UICONTROL Utilisateurs]**.

   ![](assets/search-user-role.png)
   _Rechercher un utilisateur dans la page Utilisateurs_

2. Sélectionnez la flèche déroulante à la fin de la ligne où le nom d&#39;utilisateur est affiché, puis sélectionnez **[!UICONTROL Gérer les rôles personnalisés]**.

   ![](assets/select-manage-custom-roles.png)
   _Sélectionnez Gérer les rôles personnalisés dans la page utilisateur_

3. Une boîte de dialogue s’affiche et affiche la liste des rôles personnalisés attribués à l’utilisateur. Sélectionnez **[!UICONTROL Ajouter/supprimer des rôles]** pour ajouter ou supprimer des rôles personnalisés attribués à l&#39;utilisateur.

   ![](assets/add-remove-roles.png)
   _Sélectionnez Ajouter/supprimer des rôles dans l&#39;invite Gérer les rôles personnalisés_

4. Recherchez d’autres rôles personnalisés à affecter à l’utilisateur. Après en avoir localisé un, sélectionnez le rôle personnalisé.

   ![](assets/add-new-custom-role.png)
   _Sélectionner le rôle personnalisé_

5. Sélectionnez **[!UICONTROL Enregistrer]**. Une boîte de dialogue de confirmation s’affiche pour confirmer la modification du rôle personnalisé. Sélectionnez **[!UICONTROL Oui]**.

   ![](assets/confirmation-prompt.png)
   _Sélectionnez Oui dans l&#39;invite de confirmation_

Un troisième rôle personnalisé est attribué à l’utilisateur.

Pour supprimer les rôles personnalisés, procédez comme suit :

1. Recherchez un utilisateur sur la page **[!UICONTROL Utilisateurs]**.
2. Sélectionnez la liste déroulante près de l&#39;utilisateur et sélectionnez **[!UICONTROL Gérer les rôles personnalisés]**.
3. Sélectionnez **[!UICONTROL Ajouter/supprimer des rôles]** pour ajouter ou supprimer des rôles personnalisés.
4. Sélectionnez l&#39;icône **[!UICONTROL supprimer]** pour supprimer le rôle personnalisé.

   ![](assets/remove-custom-roles.png)
   _Supprimer les rôles personnalisés_

### Changer de rôle personnalisé

Pour afficher et sélectionner tous les rôles personnalisés qui vous sont attribués, utilisez l&#39;option **[!UICONTROL Changer de rôle personnalisé]**.

![](assets/switch-roles.png)
_Sélectionner des rôles personnalisés_

Les utilisateurs reçoivent des notifications par e-mail lorsque les rôles personnalisés leur sont attribués. Les e-mails incluent désormais des noms de rôle pour plus de clarté.

## Télécharger le rapport de rôle personnalisé

Les administrateurs peuvent télécharger un rapport CSV répertoriant tous les rôles personnalisés et leurs autorisations associées. Le rapport indique si chaque rôle a été créé manuellement ou via le chargement CSV et fournit un résumé des droits d’accès et des privilèges attribués à chaque rôle.

Pour télécharger le rapport, procédez comme suit :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur]**.
2. Sélectionnez **[!UICONTROL Utilisateurs]** > **[!UICONTROL Rôles personnalisés]**.
3. Sélectionnez l&#39;option **[!UICONTROL Télécharger]** pour télécharger le rapport CSV.

![](assets/download-report.png)
_Télécharger le rapport des rôles personnalisés_

Le rapport comporte deux fichiers CSV : role.csv et user_role.csv. Le fichier role.csv comprend :

* Rôle personnalisé
* ID utilisateur
* Source de création.

Le fichier user_role.csv comprend les champs, le rôle personnalisé, la source de création et des informations détaillées sur les catalogues, les utilisateurs, les cours, les parcours d’apprentissage, etc.

## Piste d’audit pour les rôles personnalisés

Les administrateurs peuvent télécharger le rapport d’audit des rôles personnalisés pour suivre toutes les modifications apportées aux rôles personnalisés, y compris la création, la modification et la suppression des rôles personnalisés et de leur accès aux fonctionnalités associées.

Reportez-vous à cet article [Journal d&#39;audit pour les rôles personnalisés](/help/migrated/administrators/feature-summary/reports.md#audit-trail-for-custom-roles) pour plus d&#39;informations.

## Restreindre l&#39;accès aux dossiers aux auteurs personnalisés {#folder-custom-author}

Learning Manager prend déjà en charge la possibilité de donner accès à la bibliothèque de contenu à l’aide de rôles personnalisés. Tous les auteurs personnalisés qui ont déjà accès à la bibliothèque de contenu continueront d’avoir accès à tous les fichiers de contenu même après la configuration des dossiers de contenu. Cette approche vise à conserver l&#39;ancien comportement. Les administrateurs n’ont pas besoin d’apporter de modifications s’ils souhaitent continuer à adopter le comportement actuel.

S’ils souhaitent restreindre l’accès à ces auteurs personnalisés, les administrateurs doivent modifier le rôle personnalisé existant et le configurer en ne donnant accès qu’à des dossiers de contenu spécifiques.

![](assets/folder-access-forcustomauthors.png)

*Restreindre l’accès aux dossiers aux auteurs personnalisés*

Lorsque vous créez un auteur personnalisé, vous pouvez désormais lui attribuer des dossiers de contenu. Sélectionnez l&#39;option **Dossiers sélectionnés**.

Lorsque vous cliquez sur l&#39;option, une nouvelle boîte de dialogue s&#39;ouvre, dans laquelle vous pouvez attribuer les dossiers à l&#39;auteur personnalisé.

![](assets/choose-folder.png)

*Sélectionner les dossiers de l&#39;auteur personnalisé*

Sélectionnez les dossiers et cliquez sur **[!UICONTROL OK]**.

## Tableau de bord Résumé de l’apprentissage pour l’administrateur personnalisé {#custom-admin-dashboard}

Les administrateurs personnalisés peuvent voir la même vue que les administrateurs. Un administrateur personnalisé peut stocker des données en dehors de son périmètre. Cela s’applique uniquement si l’administrateur personnalisé a une portée complète. Pour accorder l&#39;étendue complète, lors de la création d&#39;un administrateur personnalisé, activez l&#39;option **[!UICONTROL Contrôle total]** dans Rapport récapitulatif du compte.

![](assets/create-custom-role.png)

*Créer un rôle personnalisé*

Par conséquent, les options **[!UICONTROL Tous les catalogues]** et **[!UICONTROL Tous les groupes d&#39;utilisateurs]** seront sélectionnées et les autres options seront désactivées.

![](assets/scope-of-featureprivileges.png)

*Définir l&#39;étendue des privilèges*

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
     Balise <br>
     Compétence<br>
     Badge<br>
     Assistance à la tâche</td>
   <td>Lire tout</td>
  </tr>
  <tr>
   <td>Créer</td>
   <td>Programme d'apprentissage<br>
     Certification<br></td>
   <td>Cours<br>
     Balise <br>
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
   <td>Identité visuelle<br>
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

Tous les plans d&#39;apprentissage créés par un administrateur, par défaut, s&#39;appliquent à tous les utilisateurs. Les utilisateurs peuvent également se voir attribuer n’importe quel objet d’apprentissage. D’un autre côté, les utilisateurs avec des rôles personnalisés bénéficient d’un accès complet, par exemple à tous les catalogues, objets d’apprentissage ou groupes d’utilisateurs. Cela signifiait que les administrateurs n&#39;étaient pas en mesure de créer des rôles personnalisés comme prévu, qui permettaient l&#39;accès aux plans d&#39;apprentissage pour les utilisateurs avec une portée limitée.

Avec cette mise à jour de Learning Manager, vous pouvez créer des rôles personnalisés pour les plans d’apprentissage qui permettent de définir leur portée en ce qui concerne les utilisateurs et les objets d’apprentissage. En d&#39;autres termes, les plans d&#39;apprentissage peuvent être créés avec une portée limitée dérivée de la portée d&#39;un rôle d&#39;administrateur personnalisé.

Désormais, un administrateur peut définir ou restreindre la portée tout en accordant un accès en tant que responsable du plan d&#39;apprentissage.

Les administrateurs personnalisés peuvent créer des plans d&#39;apprentissage avec une portée limitée, déterminée par la portée du rôle configurable de l&#39;administrateur personnalisé. Ces plans d&#39;apprentissage sont uniquement accessibles aux administrateurs personnalisés ayant le même rôle, en plus d&#39;être accessibles aux administrateurs réguliers. En outre, les administrateurs personnalisés ne peuvent pas voir d’autres plans d’apprentissage dans le compte.

Les administrateurs personnalisés existants ayant accès aux plans d’apprentissage auront toujours une portée complète (par définition). Ils auront accès à tous les plans d’apprentissage du compte, tout comme les administrateurs habituels. Les nouveaux rôles personnalisés créés avec une portée complète et les nouveaux administrateurs personnalisés ajoutés à ces rôles continueront d&#39;avoir accès à tous les plans d&#39;apprentissage.

Les plans d’apprentissage créés par l’administrateur et les administrateurs personnalisés avec une portée complète seront créés comme d’habitude et ne seront pas limités par la portée.

Dans la section **Portée des droits de fonctionnalités**, accordez l’accès aux groupes d’utilisateurs et/ou au catalogue pour le rôle personnalisé.

![](assets/scope-for-featureprivileges.png)

*Accorder l&#39;accès aux groupes d&#39;utilisateurs et/ou au catalogue pour le rôle personnalisé*

Attribuez un utilisateur au rôle personnalisé.

![](assets/assign-users-to-customrole.png)

*Attribuer un utilisateur à un rôle personnalisé*

L’utilisateur se connecte désormais à Learning Manager en tant qu’administrateur personnalisé et ajoute désormais un plan d’apprentissage.

Lorsqu’un nouvel élève est ajouté, l’administrateur personnalisé peut uniquement sélectionner une formation à partir des catalogues étendus du rôle configurable.

Ce plan d&#39;apprentissage ne s&#39;applique désormais à l&#39;élève que si l&#39;utilisateur est également ajouté au groupe au sein du groupe d&#39;utilisateurs de la portée du plan d&#39;apprentissage. Tous les autres élèves sont exemptés de ce plan d’apprentissage.

## L’élève est ajouté au groupe {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

L’administrateur personnalisé peut sélectionner n’importe quel groupe d’utilisateurs qui a des utilisateurs dans le groupe d’utilisateurs concerné.

Lorsqu’un utilisateur est ajouté au groupe spécifié, seuls les utilisateurs qui font déjà partie du groupe d’utilisateurs du plan d’apprentissage et qui ont été ajoutés au groupe d’utilisateurs spécifié se verront attribuer l’objet d’apprentissage.

## Modification de la portée {#changeinscope}

Lorsque l’administrateur modifie l’étendue du rôle personnalisé, la modification est également répercutée sur l’administrateur personnalisé. Lorsque l’administrateur personnalisé choisit un plan d’apprentissage dont la portée était déjà définie par un rôle personnalisé précédent, un message s’affiche, comme indiqué ci-dessous :

![](assets/change-scope.png)

*Message après les modifications de l&#39;étendue*

L&#39;administrateur personnalisé doit maintenant mettre à jour ou actualiser l&#39;étendue précédente vers la nouvelle étendue.

Il suffit de cliquer sur **[!UICONTROL Actualiser la portée]** pour mettre à jour la portée. Un message d’avertissement s’affiche.

![](assets/refresh-scope-message.png)

*Message d&#39;avertissement après l&#39;actualisation d&#39;une étendue*

Il suffit de cliquer sur **[!UICONTROL Oui]** pour mettre à jour la portée.

## Ajouter un rapport de ludification à un rôle personnalisé {#gamification-custom}

Un administrateur peut activer les rapports de ludification pour un utilisateur personnalisé.

1. Dans la page **[!UICONTROL Rôles personnalisés]**, saisissez le nom du rôle personnalisé.
1. Dans la section **[!UICONTROL Privilèges de fonctionnalités : fonctionnalités principales]**, activez l&#39;option **[!UICONTROL Contrôle total]** pour la catégorie **[!UICONTROL Rapports]**.

1. Dans la section **[!UICONTROL Utilisateurs]**, sélectionnez l’utilisateur auquel sera attribué le rôle personnalisé nouvellement créé.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

Lorsqu&#39;un utilisateur se connecte en tant qu&#39;administrateur personnalisé et clique sur **[!UICONTROL Rapports]** dans le volet de gauche, les transcriptions s&#39;affichent, comme indiqué ci-dessous :

![](assets/download-gamificationtranscripts.png)

*Téléchargez les transcriptions de ludification*

Cliquez sur **[!UICONTROL Relevés de notes de ludification]**, choisissez un utilisateur et générez le rapport.

Si un administrateur modifie les points de niveau, les rapports affichent les niveaux en fonction des points actuels.

La réinitialisation de la ludification ne réinitialise pas la date à laquelle le niveau a été atteint.

## Forum aux questions {#frequentlyaskedquestions}

+++Comment créer un rôle personnalisé ?

Un rôle personnalisé est semblable à un sous-ensemble d’un rôle d’auteur ou d’administrateur. Autoriser un ou plusieurs privilèges, définir la portée et attribuer le rôle à un utilisateur.

Cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Rôles personnalisés]**. Dans la page Rôles personnalisés, cliquez sur **[!UICONTROL Créer un rôle]**. Entrez le nom du rôle personnalisé et définissez les privilèges du rôle. Pour plus d’informations, voir [Création d’un rôle personnalisé](custom-role.md#create-role).
+++

