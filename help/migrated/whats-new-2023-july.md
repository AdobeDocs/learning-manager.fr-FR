---
title: Nouveautés de cette version (juillet 2023)
description: Découvrez les nouvelles fonctionnalités et améliorations d’Adobe Learning Manager
hidefromtoc: true
exl-id: c6f192b6-f377-47b2-9151-516ac8179543
source-git-commit: ebf4ea065ba799b957b8ce275fd1690f18b26556
workflow-type: tm+mt
source-wordcount: '2059'
ht-degree: 67%

---

# Nouveautés de cette version (juillet 2023)

## Recommandations améliorées

Adobe Learning Manager a introduit un nouveau système revisité de recommandations de cours. Cette fonctionnalité de recommandations utilise des algorithmes d’IA et les intérêts des utilisateurs tels que les produits, les rôles et les niveaux pour fournir des recommandations de contenu personnalisées.

Pour plus d’informations, consultez [Recommandations dans Adobe Learning Manager](recommendations-adobe-learning-manager.md).

## Inscription multiple

Dans cette version d’Adobe Learning Manager, nous introduisons l’inscription multiple pour les élèves afin de leur permettre de s’inscrire à plusieurs instances d’un cours à une ou plusieurs périodes.

Pour plus d’informations, consultez [Inscriptions multiples](/help/migrated/authors/feature-summary/courses.md).

### Inscriptions multiples dans l’application mobile ou en mode immersif

Les élèves ne peuvent pas s’inscrire à plusieurs instances à partir d’une application mobile/en mode immersif. Les inscriptions multiples ne sont pas prises en charge dans l’application mobile et le web mobile immersif.

>[!NOTE]
>
>L’activation de l’inscription multiple entraîne l’ajout de plusieurs lignes au rapport de relevé de notes de l’élève pour chaque cours (une ligne par instance).
>
>Si la configuration de Reporting Automation ne prévoit qu&#39;une seule ligne par cours, vous devez effectuer les ajustements nécessaires avant d&#39;activer la fonction d&#39;inscription multiple.

### Format des badges dans une instance à inscription multiple

Pour prendre en charge les badges dans une instance multi-inscrite, le format du badge est remplacé par `userId_badgeId_COURSE_courseId_courseInstanceId`.

### Lancer le lecteur en mode inscription multiple via un mode sans tête

Dans cette version, nous avons modifié la bibliothèque utilisée pour la communication avec le lecteur sans tête.

Dans le cas d’une inscription multiple, vous devez transmettre les arguments placés à l’intérieur d’un objet.

```
{{startplayer(argument_object) ,
where
argument_object=
{ loId = <loId>, accountId = <accountId>, userId =<userId>, accessToken = <accessToken>, domId = <elementId>, onModuleLoaded = fn(), isMultiEnrolled=<boolean>, instanceId=<instanceId> }
}}
```

## Dépréciation du connecteur Exavault

Cette version d’Adobe Learning Manager inclut un nouveau connecteur, qui utilise le protocole SFTP de la famille AWS Transfer.

Cette modification remplacera également le connecteur Exavault, qui ne sera plus disponible pour les nouveaux utilisateurs. Vous pouvez utiliser n’importe quel client FTP open source pour remplacer ExaVault. Pour plus d&#39;informations, voir [Transition à partir du gestionnaire FTP Adobe](transition-from-ftp-manager.md).

## Rappels dans Outlook pour la salle de classe et les sessions virtuelles

Les sessions de salle de classe et de salle de classe virtuelle créées à partir de Adobe Learning Manager et ajoutées au calendrier Outlook de l’élève prennent désormais en charge les rappels d’Outlook de manière cohérente (comme les rappels de réunion dans Outlook).

## Améliorations apportées à l’affectation de compétences aux cours

Nous avons apporté des améliorations au flux d’attribution de compétences pour les auteurs. La liste des suggestions de compétences sur la page Paramètres du cours inclut désormais une fonction de recherche par frappe anticipée. Les auteurs peuvent désormais rechercher des compétences en saisissant les premiers caractères, et les suggestions s’affichent dans la liste déroulante Compétence en fonction de l’entrée. Grâce à cette amélioration, les auteurs n’ont pas besoin de parcourir la liste complète pour rechercher et attribuer des compétences à des cours.

## Améliorations du workflow des cours approuvés par le responsable

Les cours approuvés par le responsable fournissent désormais les bonnes informations d’erreur aux responsables et aux élèves.

![messages d&#39;erreur](assets/error-messages.png)

Les responsables peuvent désormais consulter des messages d’erreur pertinents ainsi que des informations (par exemple, la date limite d’inscription est passée) lorsqu’ils ne peuvent pas approuver une demande d’inscription à un cours. Les élèves voient l’erreur et l’action corrective.

## Rapport Nouveau plan d’apprentissage

Les administrateurs/administrateurs personnalisés peuvent désormais exporter une liste de tous les plans d’apprentissage du compte ainsi que des métadonnées telles que l’état, les groupes d’utilisateurs applicables, les informations de déclencheur, les cours/parcours d’apprentissage inclus dans le plan d’apprentissage et les informations de rappel.

## Rapport pour suivre les instances retirées à venir

Le rapport de formation comprend une colonne supplémentaire pour afficher l’échéance d’achèvement des instances présentes dans les cours ou les parcours d’apprentissage, afin que les administrateurs et les auteurs sachent quelles instances seront supprimées et puissent prendre les mesures nécessaires.

## Améliorations apportées à la capture des évaluations de cours des élèves

Une fenêtre contextuelle permettant de capturer l’évaluation par étoiles d’un cours s’affiche dès que l’utilisateur termine le dernier module du cours.

![évaluations](assets/ratings.png)

## Personnalisation des modèles de courrier électronique

Les modèles de courrier électronique dans Learning Manager incluent désormais des sections entièrement modifiables, qui offrent une plus grande flexibilité pour personnaliser les communications par e-mail en fonction des préférences de messagerie et d’éléments de marque.

Pour plus d’informations, consultez [Personnaliser les modèles de courrier électronique](/help/migrated/administrators/feature-summary/email-templates.md#flexibility-in-customizing-the-templates).

## Améliorations apportées à l’assistant de planification

Affiner le processus de sélection d’un instructeur pour les sessions en salle de classe ou virtuelles. Un filtre Groupe d’utilisateurs a été ajouté au champ Instructeur dans l’assistant de planification. Les auteurs peuvent désormais filtrer les instructeurs en fonction de leurs « compétences » et de tout paramètre supplémentaire tel que l’emplacement, la langue, la désignation, etc.

Pour plus d’informations, consulter [Filtre du groupe d’utilisateurs dans l’assistant Planification](/help/migrated/authors/feature-summary/courses.md#user-group-filter).

## Améliorations apportées au processus de retrait de l&#39;objet d&#39;apprentissage

Les auteurs peuvent désormais fournir une date de **Suppression automatique** d’un cours. Cela permet d’éviter l’inflation du catalogue au fil du temps et de devoir revenir en arrière pour supprimer manuellement les cours.

Les administrateurs peuvent également décider au niveau du compte de la nature de l’accès aux objets d’apprentissage « retirés ».

Le rapport de formation comprend une nouvelle colonne, **Date de retrait automatique**, pour afficher la date de retrait pour chaque objet d&#39;apprentissage (si elle est définie).

## Valeurs d’étiquette de catalogue par auteur

Les auteurs peuvent désormais ajouter leurs valeurs aux étiquettes de catalogue lors de la création ou de la modification d’un cours. Les administrateurs peuvent activer cette fonctionnalité au niveau du compte. Lorsqu’un auteur ajoute une nouvelle valeur d’étiquette de catalogue, elle devient partie intégrante de la recherche par frappe anticipée.

![sélectionner le catalogue](assets/select-catalog.png)

## Améliorations apportées à la recherche de cours pour les rôles d’administrateur, d’auteur et de responsable

Des améliorations ont été apportées à la recherche pour les rôles d’administrateur, d’auteur et de responsable. Ils pourront désormais rechercher les titres à l’aide de mots-clés. Cela s’applique aux cours, aux parcours d’apprentissage et aux certifications.

## Notifications pour les échecs de migration

Les administrateurs de l’intégration sont avertis par courrier électronique si des opérations d’importation ou d’exportation échouent pendant la migration ou lors de l’utilisation de connecteurs de données tels que PowerBI, FTP, Box, etc.

## Configuration multi-gestionnaire via des API

Une nouvelle API a été ajoutée à l’ensemble d’API Managed Office pour prendre en charge la configuration de plusieurs responsables.

## Améliorations apportées à l’API d’inscription

Des améliorations ont été apportées à l’API d’inscription afin de prendre en charge et d’optimiser les inscriptions en masse à grande échelle.

## Application mobile - Affichage de contenu hors ligne

Les élèves peuvent télécharger et consommer le contenu hors connexion. Les parcours d’apprentissage imbriqués et flexibles ne sont pas pris en charge pour l’affichage hors connexion.

*Dans cette version, l&#39;affichage de contenu hors ligne est pris en charge uniquement pour le contenu en anglais.*

## Accessibilité

De nombreuses améliorations ont été apportées pour améliorer l’accessibilité, notamment pour optimiser la lisibilité par les lecteurs d’écran.

## Prise en charge des applications mobiles

Lorsque la prochaine version majeure sera publiée, l’application mobile Adobe Learning Manager prendra en charge uniquement les trois versions les plus récentes du système d’exploitation de l’appareil mobile.

## Contenu de LinkedIn

Le contenu de LinkedIn n’est pas chargé comme prévu dans l’application immersive du navigateur Safari. Pour contourner ce problème, procédez comme suit :

1. Sur l&#39;appareil, sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Safari]**.
1. Désactivez **Empêcher le suivi intersite**.
1. Désactivez **Bloquer tous les cookies**.
1. Connectez-vous à l’application Immersive.
1. Lancez la lecture du contenu.
1. Autorisez les fenêtres contextuelles.

## Autres améliorations

### Changer d’instance dans MS Teams

Un élève peut passer à une autre instance de cours jusqu’à ce qu’il soit terminé et conserver la progression du cours.

### Prise en charge de plusieurs inscriptions dans MS Teams

Un élève peut s’inscrire à une autre instance de cours, quel que soit l’état d’achèvement des instances précédentes. Cela permet à l’élève de s’inscrire à plusieurs instances du même cours.

### Les notes de cours sont compatibles avec l’inscription multiple dans MS Teams

Les notes de cours sont disponibles au niveau de l’instance de cours pour être compatibles avec l’inscription multiple.

## Modifications de l’API

Pour plus d’informations sur les modifications de l’API, consultez [Référence API Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

### Prise en charge des API pour les nouvelles recommandations

**GET /account**

Renvoie si prlRecommendation est activé.

**Demande**

`https://learningmanagerstage1.adobe.com/primeapi/v2/account`

**GET /data?filter.recommendationCriteria=product**

Renvoie la liste des produits/rubriques. Les résultats dépendent des paramètres du compte qui confirment que tous les produits seront visibles par l’élève ou que le catalogue sera visible par les produits/rubriques.

**Demande**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=product&filter.showAllRecommenda`

**`GET /data?filter.recommendationCriteria=role`**

Renvoie la liste des rôles recommandés.

**Demande**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=role&filter.showAllRecommendationCriteria=false`

**`GET /data?filter.recommendationCriteria=level`**

Renvoie la liste des rôles recommandés.

**Demande**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=level&filter.showAllRecommendationCriteria=false`

**POST /search/query**

La recherche inclut également les produits et les paramètres de rôle dans la requête. Il n’y a aucune modification dans la requête et le corps. Nous ajouterons de nouvelles options de tri

**Demande**

`https://learningmanagerstage1.adobe.com/primeapi/v2/search/query?...`

**GET /learningObjects**

Le modèle Objet d’apprentissage renvoie des recommandations portant la balise Auteur si la recommandation PRL est en ligne.

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects?sort=recommendationScore&filter.recommendationProducts=...&filter.recommendationRoles=...&filter.excludeIgnoredRecommendations=true`

POST /learningObjects/query

Les attributs suivants sont pris en charge dans le corps de l&#39;appel de requête :

```javascript {line-numbers="true"}
{
  "filter.announcedGroups": [
    "string"
  ],
  "filter.bookmarks": true,
  "filter.catalogIds": [
    "string"
  ],
  "filter.cityName": [
    "string"
  ],
  "filter.duration.range": [
    "string"
  ],
  "filter.effectiveModifiedDate.fromDate": "string",
  "filter.effectiveModifiedDate.toDate": "string",
  "filter.excludeIgnoredRecommendations": true,
  "filter.ignoreEnhancedLP": true,
  "filter.ignoreHigherOrderLOEnrollment": true,
  "filter.lang.subLOs": true,
  "filter.lang.twoLetterCode": true,
  "filter.learnerState": [
    "string"
  ],
  "filter.loFormat": [
    "string"
  ],
  "filter.loTypes": [
    "string"
  ],
  "filter.price": "string",
  "filter.priceRange": [
    "string"
  ],
  "filter.recommendationLevels": [
    "string"
  ],
  "filter.skill.level": [
    "string"
  ],
  "filter.skillName": [
    "string"
  ],
  "filter.tagName": [
    "string"
  ],
  "language": [
    "string"
  ],
  "preferredSortPartitionOrder": [
    "string"
  ],
  "showLoContentSource": true,
  "useCache": true,
  "filter.recommendationProducts": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ],
  "filter.recommendationRoles": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ]
}
```

**GET /recommendationProducts**

Récupère le produit PRL par ID de produit de recommandation.

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationProducts`

GET /recommendationRoles

Récupère le produit PRL par ID de produit de recommandation. Seuls les rôles visibles de (objets d’apprentissage) seront renvoyés.

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/prlRecommendations/roles`

`POST /users/{id}/recommendationPreferences`

Crée/recrée (remplace) les préférences de recommandation PRL. Exemple de charge utile :

```javascript {line-numbers="true"}
{
    "data": {
        "id": "userRecommendationPreferences:14755328",
        "type": "userRecommendationPreferences",
        "attributes": {
            "products": [
                {
                    "id": "recommendationProduct:1",
                    "dateCreated": "2023-05-07T20:00:00.000Z"
                },
                {
                    "id": "recommendationProduct:37",
                    "dateCreated": "2023-05-07T21:00:00.000Z"
                }
            ],
            "roles": [
                {
                    "id": "recommendationRole:23",
                    "dateCreated": "2023-05-07'T'21:00:00.000'Z'"
                },
                {
                    "id": "recommendationRole:1",
                    "dateCreated": "2023-05-07'T'20:01:00.000'Z'"
                },
                {
                    "id": "recommendationRole:2",
                    "dateCreated": "2023-05-07'T'19:02:00.000'Z'"
                },
                 {
                    "id": "recommendationRole:3",
                    "dateCreated": "2023-05-07'T'18:02:00.000'Z'"
                },
                {
                    "id": "recommendationRole:20",
                    "dateCreated": "2023-05-07'T'17:02:00.000'Z'",
                    "levels": [
                        "INTERMEDIATE"
                    ]
                }
            ]
        }
    }
}
```

**`GET /users/{id}/recommendationPreferences`**

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2//users/123/recommendationPreferences`

**`DELETE /users/{id}/recommendationPreferences`**

Supprime les préférences utilisateur de recommandation PRL pour un produit ou un rôle.

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/users/123/recommendationPreferences?ids=recommendationRole:123,recommendationRole:234`

Paramètres :

Ids = Liste des id à supprimer

**PATCH /users/{id}/recommendationPreferences**

Ajout/Mise à jour partiel. Exemple de charge utile :

```javascript {line-numbers="true"}
{
  "data": {
    "id": "userRecommendationPreferences:<USER_ID>",
    "type": "userRecommendationPreferences",
    "attributes": {
      "roles": [
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "INTERMEDIATE"
            ]
          }
        },
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "ADVANCED"
            ]
          }
        }
      ]
    }
  }
}
```

**POST /recommendationPreferences/learningObjects/{id}/ignore**

Ajouter LO aux recommandations bloquées.

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`DELETE /recommendationPreferences/learningObjects/{id}/ignore`**

Supprime l’objet d’apprentissage des recommandations bloquées.

**Demander l&#39;URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`GET /users/{id}/recommendationStrips`**

Extrait toutes les bandes à utiliser pour afficher les recommandations prl

### Prise en charge de plusieurs inscriptions pour l’API

**GET /primeapi/v2/account**

Deux nouveaux attributs sont ajoutés :

* instanceSwitchEnabled
* multiEnrollmentEnabled

**GET /users/{userId}/userNotifications**

Ajout de l’ID d’instance de cours dans les notifications du nouvel attribut de métadonnées.

**GET /learningObjects**

La relation d’inscription affiche uniquement l’inscription principale, c’est-à-dire la première inscription ou la première inscription terminée.

**`GET /learningObjects/{id}`**

La relation d’inscription affiche uniquement l’inscription principale, c’est-à-dire la première inscription ou la première inscription terminée.

**`GET /learningObjects/{loId}/instances/{loInstanceId}`**

Une nouvelle relation est ajoutée au modèle d’instance d’objet d’apprentissage.

**`GET /enrollments/{id}`**

Récupère l’inscription des cours à inscription multiple.

**`DELETE /enrollments/{id}`**

Se désinscrit d’une instance d’objet d’apprentissage particulière.

**POST /enrollments**

Prend en charge l’inscription dans différentes instances.

**GET /enrollments**

Obtient les inscriptions pour les inscriptions primaires uniquement pour l’objet d’apprentissage.

**`GET /learningObjects/{id}/note`**

Récupère une liste de notes pour un cours.

**`GET /learningObjects/{lo_id}/instances/{loi_id}/note`**

Récupère une liste de notes pour un cours et l’instance.

**`GET /learningObjects/{id}/resources/{loResourceId}/note`**

Récupère une liste de notes pour une ressource dans un cours.

**`POST /learningObjects/{id}/resources/{loResourceId}/note`**

Ajoute une note dans un module pour un cours donné.

**`DELETE /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Supprime des notes spécifiques d’un module donné par rapport à une instance spécifique (faisant partie de l’ID loResource).

**`GET /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Récupère une note spécifique dans un module de cours pour une instance donnée (partie de loResourceId).

**`PATCH /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Met à jour les notes spécifiques d’un module donné par rapport à une instance spécifique (faisant partie de l’ID loResource).

**Modifications apportées à l’API d’administration**

* GET /users/{id}/enrollments
* POST /users/{id}/enrollments
* DELETE /users/{id}/enrollments/{enrollmentId}
* PATCH /users/{id}/enrollments/{enrollmentId}

### Champs appliqués pour les points de terminaison

Les produits et les rôles sont chargés uniquement lorsqu’ils sont appliqués.

Exemple de requête

* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course%3A7418798?enforcedFields[learningObject]=products`
* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/users/11255638/userBadges?include=model&page[offset]=0&page[limit]=10&sort=dateAchieved&enforcedFields[learningObject]=products,roles`

### Mise en œuvre des modifications de l’API de recherche (paramètres régionaux anglais)

La racine est le processus de réduction d&#39;un mot à sa forme racine. Cela garantit que les variantes d’un mot sont mises en correspondance lors d’une recherche. Par exemple, marcher et marcher peut être lié au même mot racine : marcher. Une fois la chaîne terminée, une occurrence de l’un des mots correspondrait à l’autre dans une recherche.

Dans cette version, nous avons ajouté un enchaînement pour les langues anglaises, qui comprend les variantes suivantes : en_US, en_AU, en_GB.

L’attribut racinisé indique si la racinisation est requise dans les résultats de recherche. Par défaut, cette propriété est définie sur False.

Paramètres de requête API :

* matchType=expression_and_match
* stemmed=true

### Suppression des points de terminaison V1

Les API V1 cesseront de fonctionner dans cette version. Pour plus d’informations, consultez le [Manuel du développeur](/help/migrated/integration-admin/feature-summary/developer-manual.md).

### Notifications pour l’inscription ou la désinscription aux cours

Cette version introduit la prise en charge de l’ID d’instance de cours avec des notifications dans le nouvel attribut de métadonnées.

### Prise en charge du retour d’informations L1

Permet à l’élève de fournir un retour d’informations à chaque niveau d’instance de la fonction d’inscription multiple.

**API :** `POST /enrollments/{id}/l1Feedback`

### Liste des champs appliqués par l’objet d’apprentissage

Dans cette version, vous devez envoyer explicitement des sections, prequisiteConstraints, prerequisiteLOs, subLOs, additionalResources, additionalLOs, instances, catalogLabels à learningObject.

Par exemple,

`enforcedFields[learningObject]=prerequisiteLOs,instances`

### Avis d’abandon pour la prochaine version

* Indicateur de remplacement pour les API des élèves.
* Nous allons modifier la valeur par défaut pour highlightResults=false. Nous allons également modifier la valeur par défaut de snippetType=courseName.
* Nous allons déprécier matchType=bool dans le point de terminaison de recherche.
* autoCompleteMode a la balise [Obsolète] et pour fournir la même fonctionnalité autoCompleteMode =false, nous avons ajouté un matchType appelé Match.

### Format d’ID de badge avec inscription multiple

Pour prendre en charge les badges d&#39;instance inscrits plusieurs fois, nous remplaçons le format des badges de cours `userId_badgeId_COURSE_courseId to userId_badgeId_COURSE_courseId_courseInstanceId` par des badges d&#39;identification unique.

## Notes de mise à jour

Pour plus d&#39;informations sur les versions actuelles et précédentes de l&#39;application web et de l&#39;application pour appareil Learning Manager, consultez les [Notes de mise à jour](/help/migrated/release-note/release-notes.md).

## Problèmes connus ou limitations de cette version

Voici les limitations de cette version :

### Affichage du contenu hors connexion dans l’application mobile

Les éléments suivants ne sont pas pris en charge lors de l’affichage hors connexion du contenu dans l’application :

* Cours, plans d’apprentissage ou certifications flexibles.
* Cours, plans d’apprentissage ou certifications améliorés.
* Cours, plans d’apprentissage ou certifications avec fonction de quiz multiple activée.
* Harvard Manage Mentor, Content Marketplace, GetAbstract ou LinkedIn Courses, Learning Plans ou Certifications.
* Plans d’apprentissage et certificats avec les conditions préalables activées.
* Cours, plans d’apprentissage ou certifications ayant été retirés.
* Cours, plans d’apprentissage ou certifications dont l’échéance a expiré.
* Certificats externes.
* Cours, plans d’apprentissage ou certifications compatibles avec le commerce électronique.

Les parcours d’apprentissage, cours ou certifications suivants rencontrent quelques problèmes de synchronisation hors ligne :

* Tous les parcours d’apprentissage.
* Tous les certificats internes.
* Contenu avec appels POST.

### Recommandations

Le nouveau système de recommandations ne prend pas en charge les éléments suivants pour Produit/Rôle/Niveau :

* Adobe Experience Manager, Teams, SFDC et Non connecté.
* L’application mobile ne prend pas en charge la modification des produits et des rôles sur la page de recommandation.
* Le mappage n’est pas possible lors de la migration.
* Balisage automatique de LinkedIn, du marché de contenus et d’autres cours, plans d’apprentissage ou certifications externes.
* Retour à l’environnement basé sur les compétences ou classique après la mise en ligne.
* Menu de recherche pour les produits et les rôles dans l’application des élèves.
* Mappage en bloc des cours, des plans d’apprentissage ou des certifications, et des utilisateurs dans l’application d’administration.

## Configuration requise

[Configuration requise pour Learning Manager](/help/migrated/system-requirements.md)
