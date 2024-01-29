---
title: Nouveautés de cette version
description: Découvrez les nouvelles fonctionnalités et les améliorations de la version de novembre 2023 d’Adobe Learning Manager.
source-git-commit: 1b0a89bf14ed4e48c3da925686d5e2becd94e320
workflow-type: tm+mt
source-wordcount: '2373'
ht-degree: 0%

---

# Nouveautés de cette version

## Interface utilisateur remaniée

L’interface utilisateur d’Adobe Learning Manager a fait l’objet de quelques mises à jour pour offrir une expérience plus propre et plus moderne. Les pages de destination des rôles d’administrateur et d’auteur ont été réorganisées et les thèmes de l’interface utilisateur ont été mis à jour pour tous les rôles. Cependant, aucune modification n’a été apportée à l’emplacement des menus, boutons ou liens. Vous pourrez les retrouver exactement à l’endroit où ils se trouvaient auparavant.

Les mises à jour du thème s’appliquent automatiquement aux comptes qui utilisent le thème par défaut. Les mises à jour du thème de l’interface utilisateur n’affecteront pas les comptes qui ont apporté des modifications pour utiliser un thème personnalisé. Ces comptes doivent revenir au thème par défaut pour obtenir les mises à jour du nouveau thème.

![Image de l’interface utilisateur](assets/refreshed-ui.png)

### À propos de cette modification

**Quelles sont les modifications apportées à cette version ?**

L’en-tête contient un nouveau modèle qui redimensionne automatiquement le logo à une taille et une position fixes, tout en conservant les proportions du logo. La modification vise à améliorer l’attrait visuel de l’expérience de l’élève.

Le nom de l’organisation dans l’en-tête est également automatiquement redimensionné à 336 (minimum) x 680 (maximum) px pour les élèves.

**Quelle est la taille recommandée pour le logo ?**

La largeur maximale du logo est de 210 px. Les logos dont la largeur est supérieure à 210 px ou la hauteur supérieure à 42 px sont redimensionnés à 42 x 210 px.

Si la taille du logo est inférieure à la taille recommandée, le logo est téléchargé sans aucune modification et est centré.

**Quel est l&#39;impact?**

Les noms d’entreprise plus longs seront rognés et une ellipse remplira l’espace.

**Que recommandons-nous ?**

* Redimensionnez l’image en conservant les proportions intactes. La taille maximale recommandée pour le logo est de 42 px (vertical) x 210 px (horizontal).
* Pour de nombreux comptes, cela s’appliquerait automatiquement ; aucune modification n’est nécessaire.

## Extensibilité native

Configurez des expériences personnalisées dans la version native d’Adobe Learning Manager, ce qui vous permet de ne pas utiliser l’interface sans en-tête pour les cas moins complexes. Vous pouvez également créer des applications personnalisées et les placer à différents endroits dans la version native des workflows de l’élève, du responsable, de l’administrateur, de l’auteur ou de l’instructeur.

Un élève peut utiliser une application personnalisée ou une extension créée par un administrateur.

Afficher [Extensibilité native](/help/migrated/administrators/feature-summary/native-extensibility.md) pour en savoir plus.

## Outil de création de quiz

Vous pourrez désormais créer des évaluations dans Learning Manager avec le nouvel outil de création de quiz sur la page Bibliothèque de contenu. Les évaluations créées font partie de la bibliothèque de contenu et peuvent être ajoutées à un dossier « public » pour faciliter la réutilisation des cours.

Afficher [Créer un quiz](/help/migrated/authors/feature-summary/content-library.md) pour en savoir plus.

## Signaler les modifications apportées à cette version

### Modifications apportées au rapport d’inscription à l’assistance à la tâche

Dans les versions antérieures d’Adobe Learning Manager, le rapport d’inscription de l’assistance à la tâche ne comportait aucun filtre. Adobe Learning Manager a téléchargé toutes les données d’un compte.

Dans cette version, nous avons ajouté une liste déroulante dans la boîte de dialogue Rapport des assistances à la tâche.

### Modifications apportées au rapport d’annonce de notifications

Dans les versions antérieures d’Adobe Learning Manager, le rapport Annonce de notification ne disposait d’aucun filtre. Adobe Learning Manager a téléchargé toutes les notifications du compte.

Dans cette version, nous avons ajouté un filtre de date, à l’aide duquel vous pouvez télécharger les notifications au cours d’une période spécifiée.  Cependant, vous ne pouvez télécharger que le rapport des six derniers mois.

### Modifications apportées aux données de suivi de cours dans le rapport d’inscription

Dans cette version, vous pouvez télécharger les informations de nouvelle visite de cours dans un rapport d’inscription en spécifiant une heure. La période de téléchargement sera limitée à six mois pour les comptes comptant plus de cinq millions d’inscriptions. Pour tous les autres comptes, la période sera de quinze mois.

Vous pouvez télécharger le rapport à partir de **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapports historiques]** > **[!UICONTROL Rapport d’accès au cours]**.

### Modifications apportées au relevé de notes de l’élève

Dans les versions antérieures d’Adobe Learning Manager, si un administrateur personnalisé était défini sur la portée Utilisateur, le relevé de notes de l’apprentissage contenait les utilisateurs supprimés. Dans cette version, le relevé de notes contient les utilisateurs supprimés si l’administrateur personnalisé a la portée Utilisateur ou l’accès à tous les groupes d’utilisateurs.

### Modifications apportées au rapport de présence

Le rapport de présence sur la page de présence des cours dans l&#39;application d&#39;administration et sur la page Élèves de la session de l&#39;application Instructeur était téléchargé de manière synchrone. Dans cette version, ce rapport est téléchargé de manière asynchrone via une notification.

Pour plus d&#39;informations sur les rapports, voir [Rapports](/help/migrated/administrators/feature-summary/reports.md) dans Adobe Learning Manager.

## Mise hors service du marché de contenus

Les cours qui ont expiré dans le catalogue de marché de contenu importé (formation en entreprise) seront automatiquement supprimés une fois qu’ils expireront. Les cours seront définis pour être retirés lorsque le contenu sera marqué pour être mis hors service. Les élèves inscrits existants peuvent les utiliser dans un délai limité, après quoi ils seront supprimés. Cela permet de garder le catalogue propre et de ne pas afficher aux utilisateurs les cours expirés.

## Nouvelles recommandations fondées sur les compétences

Adobe Learning Manager améliore les recommandations pour les comptes clients et partenaires. Cette amélioration de l’algorithme de recommandation avec le changement de l’algorithme de classement pour le cours, le parcours d’apprentissage et la certification offre une meilleure expérience utilisateur en matière de découverte de contenu.

L’algorithme n’autorisera plus les recommandations basées sur les pairs. La modification n’affectera pas les utilisateurs existants, mais l’option Correspondant au secteur continuera d’exister. Pour l’option Personnalisé, Adobe Learning Manager n’autorisera plus la sélection personnalisée par les pairs.

Le groupe de pairs devient désormais un compte, et les élèves verront une chaîne qui montre les sujets tendance dans le groupe. Toutes les recommandations sont explicables. Par exemple, si vous visualisez quelque chose sur un sujet, la carte sur la bande affichera la raison du cours.

## Améliorations du workflow d’administration personnalisé

Les administrateurs personnalisés bénéficieront désormais d’une plus grande parité avec les rôles d’administrateur concernant l’accès aux rapports. Les administrateurs pourront configurer l’accès aux rapports avec un meilleur contrôle.

Dans Adobe Learning Manager, seuls les relevés de notes d’apprentissage et de ludification sont disponibles pour un administrateur personnalisé. Dans cette version, un administrateur personnalisé peut accéder à tous les rapports personnalisés, à l’exception des rapports xAPI et par e-mail, qui ne sont toujours disponibles que pour l’administrateur. L’accès à tous les rapports est soumis à la portée du catalogue et de l’utilisateur dont dispose l’administrateur personnalisé. Il existe peu de rapports qui ne sont disponibles que dans leur intégralité. Il s&#39;agit :

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Signaler</b></p></td>
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

Si vous sélectionnez Lecture seule, l’administrateur personnalisé pourra afficher tous les utilisateurs, mais ne pourra pas modifier les données utilisateur, et créer un portail d’auto-inscription pour les utilisateurs.

**Plans d’apprentissage**:

Si vous sélectionnez Lecture seule, un administrateur personnalisé ne peut pas ajouter ou modifier un plan d’apprentissage. Ils peuvent télécharger un rapport de plan d’apprentissage et consulter ses détails. Mais ils ne peuvent pas modifier les détails du cours.

>[!NOTE]
>
>Les plans d’apprentissage seront en lecture seule supplémentaire avec un contrôle total.

**Modèles de courrier électronique**

Si vous sélectionnez Lecture seule, un administrateur personnalisé peut afficher les modèles de courrier électronique. Ils ne peuvent pas activer ou désactiver les paramètres de modèle d’e-mail, mais peuvent télécharger des rapports d’accès par e-mail.

### Relevés de notes des élèves

Si l’autorisation Utilisateur ou Tous les groupes d’utilisateurs est sélectionnée et que l’administrateur personnalisé tente de télécharger les relevés de notes des élèves, l’option Inclure les élèves supprimés renvoie tous les élèves supprimés dans le rapport.

### Rapports

Un administrateur personnalisé peut accéder aux rapports suivants en fonction de la portée définie :

| Signaler | Disponible | Portée |
|--- |--- |
| Piste d’audit de contenu | Oui | Catalogue complet |
| Piste d’audit de l’utilisateur | Oui | Utilisateur complet |
| Accès à la connexion | Oui | Utilisateur complet |

## Intégration Connect améliorée

Les instructeurs peuvent personnaliser leur expérience de session en sélectionnant des salles spécifiques. Dans cette version, nous avons apporté les améliorations suivantes :

### Importer des transcriptions

Vous pourrez importer des transcriptions de session à partir de Connect et les analyser. Les élèves recevront le relevé de notes après l’enregistrement, qu’ils pourront télécharger ultérieurement.

### Modification de vidéos

Les instructeurs peuvent modifier la vidéo et améliorer l’expérience de visionnage des élèves. Les instructeurs verront un lien sur la page Présentation de la session pour accéder à la page de connexion Adobe Connect. Une fois connecté, l’instructeur verra le lien d’enregistrement. Cliquez sur le lien pour les rediriger vers la vidéo, qu’ils peuvent rogner.

## Restriction des rapports de tableau de bord aux utilisateurs avec le rôle de responsable

Les administrateurs peuvent rechercher uniquement des responsables dans les rapports de tableau de bord.

## Limiter le traitement des rapports de tableau de bord hérités

Lorsqu’un administrateur tente de tracer un rapport de tableau de bord et que le tracé du rapport prend trop de temps (plus de 2,5 minutes), Adobe Learning Manager affiche le message suivant :

![image de rapport héritée](assets/error-message.png)
*Message d’erreur lorsque le rapport prend trop de temps*

Les rapports d’une telle ampleur ne peuvent pas être affichés sur l’interface utilisateur, mais l’administrateur peut les télécharger.

## Prise en charge de la migration pour les étiquettes de catalogue

Le flux de travail de migration prend désormais en charge les étiquettes de catalogue. Les fichiers CSV de migration peuvent être utilisés pour importer des clés d’étiquette de catalogue et des valeurs d’étiquette de catalogue et les associer à des cours, des parcours d’apprentissage, des certifications et des assistances à la tâche. Le workflow peut également être utilisé pour supprimer des valeurs et des clés incorrectes, si nécessaire.

## Améliorations de l’API pour le filtrage des cours complexes

Le filtrage avancé des cours par balises et étiquettes de catalogue (en utilisant une combinaison des conditions « ET » et « OU ») sera désormais possible via les API Learning Manager.

## Modifications apportées aux API dans cette version

### Validation dans l’API de traitement

Dans cette version, si le rapport d’assistance à la tâche dépasse les 10 millions générés à l’aide de l’API de tâche, la réponse affiche le message « Le rapport demandé contient trop de données à générer, envisagez d’appliquer des filtres d’assistance à la tâche ! ».

### Notification d’un post supprimé

Dans les versions précédentes d’Adobe Learning Manager, si un cours, une certification ou un plan d’apprentissage est supprimé et que sa notification est présente, vous pouvez toujours accéder au cours, à la certification ou au plan d’apprentissage en consultant sa notification.

Dans cette version, nous nous assurerons qu’une publication supprimée n’est plus accessible. Si vous spécifiez l’id dans le répertoire /posts/{id} API et que l’ID de la publication n’est plus disponible, l’API affiche le message « Publication introuvable pour la ressource spécifiée ».

### Échéance d’achèvement de l’API de l’élève

Dans les versions précédentes, Adobe Learning Manager récupérait l’échéance du tableau d’inscription. Dans cette version, Adobe Learning Manager calculera l’échéance à partir du tableau des instances de cours. Si l’échéance n’est pas disponible, elle sera renvoyée au tableau d’inscription.

### Indicateur de remplacement

Dans la version de novembre 2023 d’Adobe Learning Manager, nous supprimons l’indicateur de remplacement des API. L’indicateur de remplacement ne fait pas partie de la spécification d’API publique et est destiné aux tests principaux. L’indicateur n’est plus disponible pour les API des élèves. Cependant, l’indicateur est toujours valide pour les API d’administration.

La raison pour laquelle nous déprécions l&#39;indicateur pour les API des élèves est que l&#39;indicateur de remplacement récupérait une grande quantité de données via les API des élèves.

À l’avenir, l’API de l’élève suivante cessera de fonctionner car elle comporte l’indicateur de remplacement.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Mettre les résultats en surbrillance

Dans la prochaine version d’Adobe Learning Manager, par exemple, dans l’API /search, nous modifions la valeur par défaut de highlightResults sur false.

En outre, nous allons remplacer la valeur par défaut de snippetTypes par courseName. Cela mettra en surbrillance les noms de cours dans la recherche uniquement si highlightResults a la valeur True.

### Nouveau type de ressource pour le quiz

Le `instances.loResources.resources` le point de terminaison reviendra `ResourceContentType` avec le quiz.

## Avis de dépréciation

Le 30 novembre 2023, LinkedIn Learning abandonnera l’utilisation de la méthode de GET HTTP pour obtenir un jeton OAuth. Après la dépréciation, vous ne pourrez générer un jeton OAuth qu’à l’aide de la méthode de POST HTTP.
Adobe Learning Manager arrêtera BlueJeans en février 2024. Tous les nouveaux comptes après février 2024 n’incluront pas le connecteur BlueJeans.

## Notes de mise à jour

Pour plus d’informations sur les versions actuelles et précédentes de l’application web et de l’application pour appareil Learning Manager, consultez la section [Notes de mise à jour](release-note/release-notes.md).

## Corrections de bugs dans cette version

* Une vignette de cours, qui est un prérequis pour un parcours d’apprentissage ou un autre cours, ne s’affiche pas lorsqu’un élève ouvre la page d’aperçu du parcours d’apprentissage ou du cours.
* Si les options Calendrier, Ludification et Apprentissage par les réseaux sociaux ne sont pas sélectionnées, le paramètre du tableau de bord de l’élève ne conserve pas le paramètre suivant. Les options telles que Recommandé dans vos zones d’intérêt et Parcourir par catalogue n’apparaissent pas comme sélectionnées, mais s’affichent dans l’aperçu.
* Même lorsqu’un élève a terminé un cours en classe virtuelle, il reçoit un e-mail de rappel pour terminer le cours.
* Pour les comptes de pairs, vous ne pouvez pas télécharger les rapports de tableau de bord.
* La suppression et l&#39;ajout d&#39;un module de liste de contrôle dans un cours produisent une erreur interne.
* Dans le cas des modèles d’invitation à une session, l’ID de messagerie de l’expéditeur contient le texte captivatePrime au lieu d’AdobeLearningManager.
* Lorsque vous utilisez l&#39;efficacité du cours comme axe Y secondaire, le téléchargement du rapport échoue avec une exception de pointeur Null.
* Si un rôle d’administrateur personnalisé est attribué à un élève, il accède au profil d’administrateur personnalisé par défaut. Cependant, lorsqu’une URL de redirection d’élève est définie sur le compte, l’administrateur personnalisé est dirigé vers une autre destination, et non vers le profil Rôle d’administrateur personnalisé.
* L&#39;étendue de la ludification ne fonctionne pas comme prévu si disabled_sub_groups est défini sur un grand nombre.
* Dans certains cas, les utilisateurs supprimés déclenchent une migration.
* Un élève ne peut pas lire de cours LinkedIn dans l’application MS Teams.
* L’API d’inscription ne renvoie pas les inscriptions à un plan d’apprentissage Flex ou à un plan d’apprentissage intégré comme prévu.
* Dans l’application mobile, les noms d’un cours, d’une certification ou d’un plan d’apprentissage apparaissent en minuscules.
* Dans les versions précédentes d’Adobe Learning Manager, si un cours, une certification ou un plan d’apprentissage est supprimé et que sa notification est présente, vous pouvez toujours accéder au cours, à la certification ou au plan d’apprentissage en consultant sa notification. Dans cette version, nous nous assurerons qu’une publication supprimée n’est plus accessible. Si vous spécifiez l’id dans le répertoire /posts/{id} API et que l’ID de la publication n’est plus disponible, l’API affiche le message « Publication introuvable pour la ressource spécifiée ».
* Dans l’API de l’élève, le champ d’échéance d’achèvement ne s’affiche pas dans la réponse de l’API d’inscription.
* Dans l&#39;API Get Enenrollment pour les élèves, les détails d&#39;inscription apparaissent même après que vous avez spécifié un ID d&#39;instance incorrect.

## Problèmes connus dans cette version

* Une nouvelle inscription ou la mise à jour d’une inscription échoue lorsqu’un plan d’apprentissage Flex est inclus dans un autre plan d’apprentissage Flex.
* L’URL de transcription n’affiche pas les enregistrements de session dans les sessions Adobe Connect.
* Un élève peut répondre à un quiz hors ligne dans l’application mobile même s’il échoue.

## Configuration requise

[Configuration requise pour Learning Manager](system-requirements.md)

## Versions précédentes d’Adobe Learning Manager

* [Version de juillet 2023](whats-new-2023-july.md)
* [Version d’avril 2023](whats-new-2023-april.md)
* [Version de novembre 2022](whats-new-2022-november.md)
