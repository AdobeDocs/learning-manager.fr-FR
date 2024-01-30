---
title: Nouveautés de cette version
description: Découvrez les nouvelles fonctionnalités et les améliorations de la version de novembre 2023 d’Adobe Learning Manager.
source-git-commit: 1b0a89bf14ed4e48c3da925686d5e2becd94e320
workflow-type: tm+mt
source-wordcount: '2373'
ht-degree: 70%

---

# Nouveautés de cette version

## Réorganisation de l’interface utilisateur

L’interface utilisateur d’Adobe Learning Manager a fait l’objet de quelques mises à jour pour offrir une expérience plus propre et plus moderne. Les pages d’accueil des rôles d’administrateur et d’auteur ont été réorganisées et les thèmes de l’interface utilisateur ont été mis à jour pour tous les rôles. Cependant, aucune modification n’a été apportée à l’emplacement des menus, boutons ou liens. Vous pourrez les retrouver exactement à l’endroit où ils se trouvaient auparavant.

Les mises à jour des thèmes s’appliquent automatiquement aux comptes utilisant le thème par défaut. Les mises à jour des thèmes de l’interface utilisateur n’affectent pas les comptes ayant apporté des modifications afin d’utiliser un thème personnalisé. Ces comptes doivent redéfinir le thème par défaut pour obtenir le thème mis à jour.

![Image de l’interface utilisateur](assets/refreshed-ui.png)

### À propos de cette modification

**Modifications apportées dans cette version**

L’en-tête contient un nouveau modèle permettant de redimensionner automatiquement le logo selon un format et une position fixes, tout en conservant les proportions. L’objectif de cette modification est d’améliorer l’apparence dans l’expérience de l’élève.

Le nom de l’organisation dans l’en-tête est également redimensionné automatiquement au format 336 (minimum) x 680 px (maximum) pour les élèves.

**Quelle est la taille recommandée pour le logo ?**

La largeur maximale du logo est de 210 px. Les logos présentant une largeur supérieure à 210 px ou une hauteur supérieure à 42 px sont redimensionnés au format 42 x 210 px.

Si la taille du logo est inférieure à la taille recommandée, le logo est chargé et centré sans aucune modification.

**Quel est l&#39;impact?**

Les noms d’entreprise plus longs seront rognés et affichés avec des points de suspension.

**Que recommandons-nous ?**

* Redimensionnez l’image en conservant les proportions. La taille du logo maximale recommandée est de 42 px (hauteur) x 210 px (largeur).
* Pour de nombreux comptes, ce changement s’applique automatiquement et aucune modification n’est nécessaire.

## Extensibilité native

Configurez des expériences personnalisées dans la version native d’Adobe Learning Manager, ce qui permet de ne pas utiliser l’approche headless pour les cas moins complexes. Vous pouvez également créer des applications personnalisées et les placer à différents points de la version native des flux de travail de l’élève, du responsable, de l’administrateur, de l’auteur ou de l’instructeur.

Un élève peut utiliser une application personnalisée ou une extension créée par un administrateur.

Afficher [Extensibilité native](/help/migrated/administrators/feature-summary/native-extensibility.md) pour en savoir plus.

## Outil de création de quiz

Vous pourrez désormais créer des évaluations dans Learning Manager avec le nouvel outil de création de quiz sur la page Bibliothèque de contenu. Les évaluations créées font partie de la bibliothèque de contenu et peuvent être ajoutées à un dossier « public » pour faciliter la réutilisation des cours.

Afficher [Créer un quiz](/help/migrated/authors/feature-summary/content-library.md) pour en savoir plus.

## Modifications concernant les rapports dans cette version

### Modifications apportées au rapport d’inscription à l’assistance à la tâche

Dans les versions antérieures d’Adobe Learning Manager, le rapport d’inscription de l’assistance à la tâche ne comportait aucun filtre. Adobe Learning Manager téléchargeait l’ensemble des données d’un compte.

Dans cette version, nous avons ajouté une liste déroulante dans la boîte de dialogue Rapport des assistances à la tâche.

### Modifications apportées au rapport d’annonce de notifications

Dans les versions antérieures d’Adobe Learning Manager, le rapport Annonce de notification ne disposait d’aucun filtre. Adobe Learning Manager téléchargeait l’ensemble des notifications du compte.

Dans cette version, nous avons ajouté un filtre de date, à l’aide duquel vous pouvez télécharger les notifications au cours d’une période spécifiée.  Cependant, vous ne pouvez télécharger que le rapport des six derniers mois.

### Modifications apportées aux données de suivi de cours dans le rapport d’inscription

Dans cette version, vous pouvez télécharger les informations de retour au cours dans un rapport d’inscription en spécifiant une heure. La période de téléchargement est limitée à six mois pour les comptes comprenant plus de cinq millions d’inscriptions. Pour tous les autres comptes, la période est de quinze mois.

Vous pouvez télécharger le rapport à partir de **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapports historiques]** > **[!UICONTROL Rapport d’accès au cours]**.

### Modifications apportées au relevé de notes de l’élève

Dans les versions antérieures d’Adobe Learning Manager, si un administrateur personnalisé était défini sur l’étendue Utilisateur, le relevé de notes de l’apprentissage contenait les utilisateurs supprimés. Dans cette version, le relevé de notes contient les utilisateurs supprimés si l’administrateur personnalisé est défini sur l’étendue Utilisateur ou s’il a accès à tous les groupes d’utilisateurs.

### Modifications apportées au rapport de présence

Le rapport de participation sur la page de participation des cours dans l’application d’administrateur et sur la page des élèves de la session dans l’application Instructeur était téléchargé de manière synchrone. Dans cette version, ce rapport est téléchargé de manière asynchrone via une notification.

Pour plus d&#39;informations sur les rapports, voir [Rapports](/help/migrated/administrators/feature-summary/reports.md) dans Adobe Learning Manager.

## Mise hors service du Marché de contenus

Les cours ayant expiré dans le catalogue du Marché de contenu importé (formation d’entreprise) sont supprimés automatiquement une fois le délai expiré. Les cours sont définis de telle manière qu’ils sont supprimés si le contenu est défini sur la mise hors service. Les élèves inscrits existants peuvent les suivre dans un délai limité, après quoi les cours sont supprimés. Le catalogue reste ainsi toujours clair et les utilisateurs ne voient plus de cours expirés.

## Nouvelles recommandations basées sur les compétences

Adobe Learning Manager améliore les recommandations pour les comptes clients et partenaires. Grâce à l’amélioration de l’algorithme de recommandation due à la modification de l’algorithme de classement des cours, des parcours d’apprentissage et des certifications, les utilisateurs bénéficient d’une expérience optimisée en termes de découverte de contenu.

L’algorithme n’autorise plus les recommandations basées sur les pairs. La modification n’affecte pas les utilisateurs existants. Toutefois, l’option Correspondant au secteur continue d’exister. Pour l’option Personnalisé, Adobe Learning Manager n’autorise plus la sélection personnalisée basée sur les pairs.

Le groupe de pairs devient désormais un compte. Les élèves verront une chaîne présentant les sujets tendance dans le groupe. Toutes les recommandations sont explicables. Par exemple, si vous consultez un contenu sur un certain type de sujet, la carte sur la bande affiche la raison de la suggestion du cours.

## Améliorations du processus d’administration personnalisé

Les administrateurs personnalisés bénéficient désormais d’une meilleure parité par rapport aux rôles d’administrateur quant à l’accès aux rapports. Les administrateurs pourront configurer l’accès aux rapports pour avoir un meilleur contrôle.

Dans Adobe Learning Manager, seuls les relevés de notes d’apprentissage et de ludification sont disponibles pour les administrateurs personnalisés. Dans cette version, les administrateurs personnalisés peuvent accéder à l’ensemble des rapports personnalisés, à l’exception des rapports xAPI et e-mail, qui restent disponibles uniquement pour l’administrateur. L’accès à l’ensemble des rapports est sujet à l’étendue catalogue et utilisateur défini pour l’administrateur personnalisé. Peu de rapports sont disponibles uniquement avec une étendue complète. Ce sont :

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Rapport</b></p></td>
   <td>
    <p style="text-align: left;"><b>Disponible</b></p></td>
   <td>
    <p style="text-align: left;"><b>Portée</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Piste d’audit de contenu</p></td>
   <td>
    <p>Oui</p></td>
   <td>
    <p>Catalogue complet</p></td>
  </tr>
  <tr>
   <td>
    <p>Piste d’audit de l’utilisateur</p></td>
   <td>
    <p>Oui</p></td>
   <td>
    <p>Utilisateur complet</p></td>
  </tr>
  <tr>
   <td>
    <p>Accès à la connexion</p></td>
   <td>
    <p>Oui</p></td>
   <td>
    <p>Utilisateur complet</p></td>
  </tr>
    </tbody>
</table>

**Nouveaux contrôles en lecture seule**

Dans la page Rôles personnalisés, nous avons ajouté les options en lecture seule suivantes pour permettre aux administrateurs de fournir des options plus flexibles à l’administrateur personnalisé : l’administrateur personnalisé disposera désormais d’autorisations en lecture seule supplémentaires pour les utilisateurs, les modèles de courrier électronique et les plans d’apprentissage.

**Utilisateurs**:

Si vous sélectionnez l’option Lecture seule, les administrateurs personnalisés peuvent afficher tous les utilisateurs, mais ils ne peuvent pas modifier les données utilisateur, ni créer de portail d’auto-inscription pour les utilisateurs.

**Plans d’apprentissage**:

Si vous sélectionnez Lecture seule, les administrateurs personnalisés ne peuvent pas ajouter ni modifier de plan d’apprentissage. Ils peuvent télécharger un rapport de plan d’apprentissage et consulter les détails. Toutefois, ils ne peuvent pas modifier les détails du cours.

>[!NOTE]
>
>Les plans d’apprentissage seront en lecture seule supplémentaire avec un contrôle total.

**Modèles de courrier électronique**

Si vous sélectionnez l’option Lecture seule, les administrateurs personnalisés peuvent afficher les modèles de courrier électronique. Ils ne peuvent pas activer ni désactiver les paramètres des modèles de courrier électronique. Toutefois, ils peuvent télécharger des rapports d’accès aux e-mails.

### Relevés de notes de l&#39;élève

Si l’autorisation Utilisateur ou Tous les groupes d’utilisateurs est sélectionnée et que l’administrateur personnalisé tente de télécharger les relevés de notes des élèves, l’option Inclure les élèves supprimés renvoie tous les élèves supprimés dans le rapport.

### Rapports

Les administrateurs personnalisés peuvent accéder aux rapports suivants selon l’étendue définie :

| Rapport | Disponible | Portée |
|--- |--- |
| Piste d’audit de contenu | Oui | Catalogue complet |
| Piste d’audit de l’utilisateur | Oui | Utilisateur complet |
| Accès à la connexion | Oui | Utilisateur complet |

## Intégration de Connect améliorée

Les instructeurs peuvent personnaliser leur expérience de session en sélectionnant des salles spécifiques à l’instructeur. Dans cette version, nous avons apporté les améliorations suivantes :

### Importation des relevés de notes

Vous pourrez importer des transcriptions de session à partir de Connect et les analyser. Les élèves reçoivent le relevé de notes après l’enregistrement, qu’ils peuvent télécharger ultérieurement.

### Modification des vidéos

Les instructeurs peuvent modifier la vidéo et améliorer l’expérience de visionnage des élèves. Un lien s’affiche pour les instructeurs sur la page de présentation de la session permettant d’accéder à la page de connexion à Adobe Connect. Une fois que l’instructeur est connecté, le lien d’enregistrement s’affiche. S’il clique sur le lien, il est redirigé vers la vidéo qu’il peut rogner.

## Restriction des rapports de tableau de bord aux utilisateurs avec le rôle de responsable

Les administrateurs peuvent rechercher uniquement des responsables dans les rapports de tableau de bord.

## Limitation du traitement des rapports de tableau de bord hérités

Lorsqu’un administrateur tente de tracer un rapport de tableau de bord et que le tracé du rapport prend trop de temps (plus de 2,5 minutes), Adobe Learning Manager affiche le message suivant :

![image de rapport héritée](assets/error-message.png)
*Message d’erreur lorsque le rapport prend trop de temps*

L’interface utilisateur ne permet pas d’afficher les rapports de cette taille. Toutefois, l’administrateur peut les télécharger.

## Prise en charge de la migration pour les étiquettes de catalogue

Le processus de migration prend désormais en charge les étiquettes de catalogue. Les fichiers CSV de migration permettent d’importer des clés d’étiquette de catalogue et des valeurs d’étiquette de catalogue et les associer à des cours, des parcours d’apprentissage, des certifications et des assistances à la tâche. Ce processus permet également de supprimer des valeurs et des clés incorrectes si nécessaire.

## Améliorations de l’API pour filtrer les cours complexes

Le filtrage avancé des cours par balises et étiquettes de catalogue (en utilisant une combinaison des conditions « ET » et « OU ») sera désormais possible via les API Learning Manager.

## Modifications apportées aux API dans cette version

### Validation dans l’API de traitement

Dans cette version, si le rapport d’assistance à la tâche dépasse les 10 millions générés à l’aide de l’API de tâche, la réponse affiche le message « Le rapport demandé contient trop de données à générer, envisagez d’appliquer des filtres d’assistance à la tâche ! ».

### Notification de post supprimé

Dans les versions précédentes d’Adobe Learning Manager, si un cours, une certification ou un plan d’apprentissage est supprimé et que sa notification est présente, il reste possible d’accéder au cours, à la certification ou au plan d’apprentissage en consultant sa notification.

Dans cette version, nous nous assurerons qu’une publication supprimée n’est plus accessible. Si vous spécifiez l’id dans le répertoire /posts/{id} API et que l’ID de la publication n’est plus disponible, l’API affiche le message « Publication introuvable pour la ressource spécifiée ».

### Échéance d’accomplissement des API de l’élève

Dans les versions précédentes, Adobe Learning Manager récupérait l’échéance à partir du tableau d’inscription. Dans cette version, Adobe Learning Manager calcule l’échéance à partir du tableau des instances de cours. Si l’échéance n’est pas disponible, le tableau d’inscription est utilisé.

### Indicateur de remplacement

Dans la version de novembre 2023 d’Adobe Learning Manager, nous supprimons l’indicateur de remplacement des API. L’indicateur de remplacement ne fait pas partie de la spécification d’API publique et est destiné aux tests backend. L’indicateur n’est plus disponible pour les API des élèves. Cependant, l’indicateur reste valide pour les API d’administrateur.

La raison pour laquelle nous déprécions l&#39;indicateur pour les API des élèves est que l&#39;indicateur de remplacement récupérait une grande quantité de données via les API des élèves.

À l’avenir, l’API des élèves suivante cessera de fonctionner car elle comporte l’indicateur de remplacement.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Mise en surbrillance des résultats

Dans la prochaine version d’Adobe Learning Manager, par exemple, dans l’API /search, nous modifions la valeur par défaut de highlightResults sur false.

En outre, nous allons remplacer la valeur par défaut de snippetTypes par courseName. Cela mettra en surbrillance les noms de cours dans la recherche uniquement si highlightResults a la valeur True.

### Nouveau type de ressource pour les questionnaires

Le `instances.loResources.resources` le point de terminaison reviendra `ResourceContentType` avec le quiz.

## Avis d’abandon

À compter du 30 novembre 2023, LinkedIn Learning abandonne l’utilisation de la méthode GET HTTP pour obtenir un jeton OAuth. Après la dépréciation, vous ne pourrez générer un jeton OAuth qu’à l’aide de la méthode de POST HTTP.
Adobe Learning Manager supprimera BlueJeans en février 2024. Tous les nouveaux comptes créés après février 2024 n’incluront pas le connecteur BlueJeans.

## Notes de mise à jour

Pour plus d’informations sur les versions actuelles et précédentes de l’application web et de l’application pour appareil Learning Manager, consultez la section [Notes de mise à jour](release-note/release-notes.md).

## Bogues corrigés dans cette version

* Une vignette de cours, qui constitue un prérequis pour un parcours d’apprentissage ou un autre cours, ne s’affiche pas lorsqu’un élève ouvre la page d’aperçu du parcours d’apprentissage ou du cours.
* Si les options Calendrier, Ludification et Apprentissage par les réseaux sociaux ne sont pas sélectionnées, le paramètre du tableau de bord de l’élève ne conserve pas le paramètre suivant. Les options telles que Recommandé dans vos champs d’intérêt et Rechercher par catalogue ne semblent pas sélectionnées, mais elles s’affichent dans l’aperçu.
* Un élève reçoit un e-mail de rappel l’invitant à terminer le cours alors qu’il l’a terminé en classe virtuelle.
* Pour les comptes de pairs, vous ne pouvez pas télécharger les rapports de tableau de bord.
* La suppression et l’ajout d’un module de liste de contrôle dans un cours entraînent une erreur interne.
* Dans les modèles d’invitation à une session, l’ID de messagerie de l’expéditeur comprend le texte captivatePrime au lieu d’AdobeLearningManager.
* Si vous définissez l’efficacité du cours pour l’axe Y secondaire, le téléchargement du rapport échoue avec une exception de valeur nulle du pointeur.
* Si un rôle d’administrateur personnalisé est attribué à un élève, il accède au profil d’administrateur personnalisé par défaut. Cependant, lorsqu’une URL de redirection d’élève est définie sur le compte, l’administrateur personnalisé est dirigé vers une autre destination, et non vers le profil de rôle d’administrateur personnalisé par défaut.
* L’étendue de la ludification ne fonctionne pas comme prévu si disabled_sub_groups est défini sur un grand nombre.
* Dans certains cas, les utilisateurs supprimés déclenchent une migration.
* Un élève ne peut pas lire les cours LinkedIn dans l’application MS Teams.
* L’API d’inscription ne renvoie pas les inscriptions à un plan d’apprentissage flexible ou à un plan d’apprentissage intégré comme prévu.
* Dans l’application mobile, les noms d’un cours, d’une certification ou d’un plan d’apprentissage s’affichent en minuscules.
* Dans les versions précédentes d’Adobe Learning Manager, si un cours, une certification ou un plan d’apprentissage est supprimé et que sa notification est présente, il reste possible d’accéder au cours, à la certification ou au plan d’apprentissage en consultant sa notification. Dans cette version, nous nous assurerons qu’une publication supprimée n’est plus accessible. Si vous spécifiez l’id dans le répertoire /posts/{id} API et que l’ID de la publication n’est plus disponible, l’API affiche le message « Publication introuvable pour la ressource spécifiée ».
* Dans l’API des élèves, le champ d’échéance d’achèvement ne s’affiche pas dans la réponse de l’API d’inscription.
* Dans l’API Get Enrollment pour les élèves, les détails d’inscription s’affichent même si vous avez spécifié un ID d’instance incorrect.

## Problèmes connus dans cette version

* Une nouvelle inscription ou la mise à jour d’une inscription échoue si un plan d’apprentissage flexible est inclus dans un autre plan d’apprentissage flexible.
* L’URL de relevés de notes n’affiche pas les enregistrements de session dans les sessions Adobe Connect.
* Un élève peut répondre à un questionnaire hors ligne dans l’application mobile même en cas d’échec.

## Configuration requise

[Configuration requise pour Learning Manager](system-requirements.md)

## Versions précédentes d’Adobe Learning Manager

* [Version de juillet 2023](whats-new-2023-july.md)
* [Version d’avril 2023](whats-new-2023-april.md)
* [Version de novembre 2022](whats-new-2022-november.md)
