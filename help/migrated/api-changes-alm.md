---
description: Modifications d’API dans ALM
jcr-language: en_us
title: Modifications apportées aux API dans la version d’avril
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '4093'
ht-degree: 0%

---


# Modifications apportées aux API dans la version d’avril 2026

La version d’avril 2026 de Adobe Learning Manager introduit des améliorations ciblées de l’API publique concernant les alternatives et les équivalents, l’accès au contenu par fenêtre temporelle, les tentatives de quiz axées sur le contenu, les expériences hors connexion et la gestion des assistances à la tâche. Les modifications sont conçues pour être largement rétrocompatibles, tout en permettant des intégrations plus précises.

## Apprentissage adaptatif pour les parcours d’apprentissage

Cette version ajoute la prise en charge complète des API publiques pour les parcours d’apprentissage adaptatifs. Les parcours d’apprentissage peuvent désormais définir des règles adaptatives qui contrôlent les sections et les objets de sous-apprentissage (sous-objets d’apprentissage) visibles par différents groupes d’élèves, et l’API publique reflète ce comportement.

Les critères d’évaluation suivants sont concernés :

- GET /primeapi/v2/learningObjects?filter.loTypes=learningPath
- GET /primeapi/v2/learningObjects/{loId}

Un nouvel attribut booléen, attributes.isAdaptive, indique qu&#39;un programme d&#39;apprentissage utilise des règles adaptatives. Lorsque cet indicateur est défini sur true, l’attribut sections est interprété de manière adaptative.

Pour les appels d&#39;élève, seules les sections visibles par l&#39;élève actuel sont renvoyées. Chaque section comprend la liste des ID d’objet d’apprentissage (loId), un indicateur obligatoire et un compte de liste de valeurs obligatoire calculés en fonction de la configuration adaptative pour cet élève, ainsi que l’ID de section. La relation relations.subLOs est désormais également filtrée, de sorte qu’elle contient uniquement les objets de sous-apprentissage qui sont visibles par cet élève.

Pour les appels d&#39;administrateur, les sections peuvent également exposer un tableau adaptiveConfig. Cette section décrit les règles adaptatives par groupe d’utilisateurs, notamment userGroupId et userGroupName, et indique si la section est obligatoire pour ce groupe. Les outils destinés aux administrateurs peuvent les utiliser pour visualiser et gérer les règles adaptatives.

Réinitialiser l’achèvement des programmes d’apprentissage

La version introduit une API permettant d&#39;__actualiser (réinitialiser) l&#39;achèvement__ des objets d&#39;apprentissage, y compris les programmes d&#39;apprentissage adaptatif. Cela prend en charge des scénarios tels que le recyclage, les actualisations périodiques de la conformité ou les redémarrages du programme.

Un nouveau point de terminaison est disponible :

```
POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion
```

Cette opération nécessite des autorisations en écriture appropriées et réinitialise l&#39;état d&#39;achèvement pour l&#39;instance d&#39;objet d&#39;apprentissage spécifiée dans le contexte utilisateur donné. Il est destiné à être utilisé par les automatisations côté administrateur ou par des outils d’élève soigneusement ciblés.

Une version groupée de cette fonctionnalité est prévue via une API Jobs. La forme de demande est conçue pour cibler les utilisateurs par e-mail, ID utilisateur ou ID de groupe d’utilisateurs, par exemple :

```
{  
  "emails": ["[user1@example.com](mailto:user1@example.com)", "[user2@example.com](mailto:user2@example.com)"],  
  "userIds": ["12345", "67890"],  
  "userGroupIds": ["ug1", "ug2"]  
}  
```

Les intégrations doivent utiliser cette API lorsqu’elles doivent redémarrer les élèves dans chaque programme ou cours. Les clients doivent gérer les réponses d’erreur avec élégance : l’API peut rejeter les demandes d’actualisation lorsqu’une réinitialisation n’est pas applicable (par exemple, lorsqu’il n’existe aucune fin ou que les types d’objets d’apprentissage ne sont pas pris en charge).

## Équivalents et autres déclarations de fin

Pour prendre en charge les implémentations où plusieurs objets d’apprentissage peuvent répondre à la même exigence, la version introduit les terminaisons Équivalentes et Alternatives en tant qu’API publiques.

Les points de terminaison de l’objet d’apprentissage contiennent désormais les informations suivantes :

```
- GET /primeapi/v2/learningObjects
- GET /primeapi/v2/learningObjects/{loId}
```

Un nouvel attribut booléen attributes.isAlternateComplete indique si l’achèvement par l’élève pour un objet d’apprentissage donné est le résultat d’un objet d’apprentissage alternatif ou équivalent plutôt que l’objet lui-même. Lorsque c’est le cas, la relation relationship.alternateCompletions répertorie les objets d’apprentissage qui jouaient le rôle d’alternatives. Cela permet aux rapports et aux tableaux de bord en aval de faire la distinction entre les déclarations directes et les déclarations de fin de production de remplacement et de montrer quel produit de remplacement a satisfait à l&#39;exigence.

En outre, une vue objets d’apprentissage associés permet de découvrir des alternatives potentielles pouvant satisfaire un objet d’apprentissage. Cette action est exposée via :

```
GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}
```

La réponse renvoie des objets d&#39;apprentissage qui peuvent agir comme des variantes et inclut un champ meta.count qui indique le nombre total de ces variantes, indépendamment de la limite actuelle. Les intégrations peuvent l&#39;utiliser pour présenter des équivalents recommandés ou pour créer des vues administratives de mappages alternatifs.

## Cas d’utilisation Reporting and analytics

Les utilisateurs qui génèrent des rapports ou des analyses doivent mettre à jour leur logique pour ajouter isAlternateComplete et alternateCompletions dans leurs workflows de création de rapports.

Les intégrations de rapports qui consomment des données d&#39;achèvement (par exemple, exportation LT, flux d&#39;entrepôt de données personnalisés ou tableaux de bord BI) doivent étendre leur logique pour lire et conserver les deux attributs.isAlternateComplete et relations.alternateCompletions à partir des API LO :

- Quand isAlternateComplete == false :\
  Considérez l&#39;enregistrement comme une __achèvement direct__ de l&#39;objet d&#39;apprentissage, comme aujourd&#39;hui.
- Quand isAlternateComplete == true :
   - Marquez l&#39;enregistrement comme __autre achèvement__ dans votre rapport (par exemple, une colonne « Méthode d&#39;achèvement » avec les valeurs DIRECT et ALTERNATE).
   - Utilisez relations.alternateCompletions.data[*].id pour capturer __le(s) objet(s) d&#39;apprentissage source__ ayant accordé cette achèvement (par exemple, « Cours B terminé via l&#39;autre cours A »).

Cas d’utilisation typiques :

- _Rapports de conformité_ : montrent qu&#39;un cours de conformité a été suivi via un équivalent approuvé, et dressent la liste du cours source qui a rempli l&#39;exigence.
- _Tableaux de bord de progression du programme_ : différenciez les élèves qui ont terminé un parcours _directement_ de ceux qui l&#39;ont suivi via des alternatives, pour des vues de progression et de correction plus précises.
- _Pistes d’audit_ : pour tout objet d’apprentissage marqué isAlternateComplete=true, les auditeurs peuvent voir exactement quelle(s) autre(s) formation(s) a(ont) été utilisée(s) pour accorder cette achèvement.

Sans incorporer ces deux champs, les rapports en aval traiteront les autres achèvements comme des achèvements réguliers et ne seront _pas en mesure d&#39;expliquer_ *pourquoi* un élève montre comme ayant terminé une formation qu&#39;il n&#39;a jamais suivie directement.

## Comportement de l’API LO Élève/Administrateur

La structure d’assistance à la tâche multilingue est identique dans les API LO de l’élève et de l’administrateur. La portée de l’élève renvoie uniquement les assistances à la tâche visibles par l’élève, mais pour chaque assistance à la tâche visible, elle expose toutes les langues configurées via plusieurs entités de ressource (une par langue) et plusieurs paramètres régionaux localizedMetadata. La portée d’administrateur renvoie toutes les assistances à la tâche que l’administrateur peut gérer, avec les mêmes ID de ressource spécifiques au modèle d’objet d’apprentissage et aux paramètres régionaux. Les clients avec une étendue d’élève doivent choisir la ressource dont les attributs.locale correspondent le mieux à la langue du contenu de l’élève, tandis que les outils d’administration peuvent énumérer toutes les langues pour la création de rapports et la gestion.

## Liste de contrôle avec possibilité de commentaire

Pour prendre en charge les workflows dans lesquels les réviseurs peuvent partager des commentaires structurés sur les activités basées sur des listes de contrôle, cette version affiche des *commentaires de liste de contrôle* et des contrôles de visibilité des réviseurs via l&#39;API de ressource d&#39;objet d&#39;apprentissage.

Les métadonnées liées à la liste de contrôle sont affichées sur les entités learningObjectResource (JApiLOResource, « type » : « learningObjectResource ») qui représentent des ressources de liste de contrôle dans un cours ou un autre objet d’apprentissage.

Les informations sont disponibles via :

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

Lorsque l&#39;instance d&#39;objet d&#39;apprentissage contient des ressources de type liste de contrôle, les entrées learningObjectResource correspondantes dans le tableau inclus exposent les attributs comment et reviewer-visibility sous attributs, et l&#39;identité du réviseur sous relations.

### Nouveaux attributs de commentaire de liste de contrôle

Pour les ressources de liste de contrôle, les attributs suivants peuvent être présents sur learningObjectResource :

- attributes.checklistComment\
  Commentaire en texte libre laissé par le réviseur pour l’élève, par exemple :\
  « checklistComment »: « Excellente performance ! Tous les protocoles de sécurité ont été suivis correctement. »\
  Cet attribut est renseigné _uniquement si_ :
   - showChecklistComment est true, et
   - la configuration de liste de contrôle a enable_reviewer_comments activée.
- attributes.showChecklistComment\
  Indicateur booléen indiquant si les remarques des réviseurs doivent être affichées à l’élève :\
  « showChecklistComment » : true\
  Cet attribut est présent _uniquement lorsque_ enable_reviewer_comments est activé dans la configuration de liste de contrôle.\
  Les clients doivent utiliser cet indicateur pour décider s’ils souhaitent rendre checklistComment dans les expériences des élèves.
- attributes.showReviewerNameToLearner\
  Indicateur booléen contrôlant si l’élève doit voir l’identité du réviseur :\
  « showReviewerNameToLearner » : true\
  Lorsque la valeur est True, les clients peuvent utiliser la relation checklistReviewedBy (voir ci-dessous) pour résoudre et afficher le nom du réviseur (par exemple, via une API de recherche d’utilisateur).

D’autres contextes spécifiques à la liste de contrôle, tels que checklistEvaluationStatus, isChecklistObligatory, resourceSubType : « CHECKLIST » et submissionDate, sont également disponibles sur le même learningObjectResource pour prendre en charge des interfaces utilisateur de liste de contrôle et des rapports plus riches.

### Relation d’identité du réviseur

Lorsque les noms des réviseurs sont censés être visibles, learningObjectResource inclut une relation qui pointe vers l’utilisateur réviseur :

```
"relationships": {
  "checklistReviewedBy": {
    "data": {
      "id": "user_id",
      "type": "user"
    }
  }
}
```

Cette relation est renseignée _uniquement si_ :

- showReviewerNameToLearner a la valeur true, et
- checklistReviewedBy n’est pas null (c’est-à-dire que la liste de contrôle a été révisée).

Les applications clientes doivent :

1. Vérifiez attributes.showReviewerNameToLearner.
2. Si true et relations.checklistReviewedBy.data sont présents, appelez l’API utilisateur appropriée pour résoudre « id » : « user_id » dans un nom d’affichage.
3. Affichez le nom du réviseur en regard du commentaire ou de l’état de la liste de contrôle, selon le cas.

### Accès aux ressources et aux commentaires de la liste de contrôle

Pour récupérer les ressources de liste de contrôle et leurs commentaires pour un objet d&#39;apprentissage donné, les clients doivent :

- Appeler

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

- Dans la réponse :
   - Utilisez relations.instances de l’objet d’apprentissage principal pour localiser les entrées learningObjectInstance pertinentes dans incluses.
   - À partir de chaque learningObjectInstance, suivez relationship.loResources pour trouver les entrées learningObjectResource.
   - Filtrer les entrées learningObjectResource où :
      - attributes.resourceSubType == « CHECKLIST » (pour les ressources de liste de contrôle), et
      - facultativement attributes.showChecklistComment == true pour rechercher des listes de contrôle avec des commentaires visibles par l’élève.

- Pour chaque liste de contrôle learningObjectResource, utilisez :
   - attributes.checklistComment (si présent et showChecklistComment a la valeur true)
   - attributes.checklistEvaluationStatus (par exemple, « PASSED »)
   - attributes.showReviewerNameToLearner
   - relations.checklistReviewéBy (le cas échéant) pour identifier le réviseur.

Ce modèle permet aux clients sans en-tête ou personnalisés de générer une expérience de liste de contrôle complète, comprenant le statut, les indicateurs obligatoires/facultatifs et les commentaires des réviseurs, directement à partir des API Prime.

### Remarques sur les rapports et l’expérience utilisateur

- _Reporting et analyses_
Les intégrations qui suivent les performances des élèves sur les listes de contrôle peuvent incorporer :
   - checklistEvaluationStatus pour les réussites/échecs ou d’autres indicateurs d’état.
   - isChecklistObligatoire pour différencier les activités de liste de contrôle obligatoires des activités de liste de contrôle facultatives.
   - Présence ou absence de checklistComment et showChecklistComment pour les audits de la couverture des commentaires.
- _Expériences des élèves_
Les implémentations de l’interface utilisateur doivent :
   - Respectez showChecklistComment avant d’afficher les remarques.
   - Utilisez showReviewerNameToLearner et checklistReviewedBy pour décider d’afficher le nom du réviseur ou de conserver l’anonymat de la révision.
   - Revenez en arrière gracieusement lorsque les commentaires sont désactivés ou absents, en affichant toujours l’état d’évaluation et les informations de soumission.

## Prise en charge multilingue de l’assistance à la tâche

Pour prendre en charge les implémentations où les assistances à la tâche doivent être fournies dans plusieurs langues aux élèves et aux administrateurs, cette version étend la gestion des assistances à la tâche pour renvoyer *une ressource par locale* au lieu d&#39;une seule ressource en-US codée en dur.

Les assistances à la tâche multilingues continuent d’utiliser la hiérarchie existante :

_Objet d’apprentissage_ (lo) → _learningObjectResource_ (loResource) → _ressource_

Aucune modification n’est requise pour le contrat d’API. Toute assistance à la tâche localisée s’intègre naturellement dans cette structure, avec des entités de ressources distinctes par locale et des métadonnées localisées partagées aux niveaux learningObject / learningObjectResource.

Les données d’assistance à la tâche sont affichées via :

```
GET /primeapi/v2/learningObjects/jobAid:{jobAidId}?include=instances.loResources.resources
```

Lorsqu’une assistance à la tâche comporte plusieurs variantes de langue, le tableau inclus contient plusieurs entrées « type » : « resource » (une pour chaque environnement linguistique (par exemple, en-US, fr-FR, es-ES), toutes liées à partir d’une seule ressource learningObjectResource.

### Structure d&#39;assistance à la tâche multilingue

Utilisation d’assistances à la tâche multilingues :

- _learningObject (type : learningObject)_
   - Contient des métadonnées localisées avec plusieurs entrées (par exemple, en-US, fr-FR) afin que les clients puissent présenter le titre/la description de l’assistance à la tâche dans la langue appropriée.
- _learningObjectInstance (type : learningObjectInstance)_
   - Fait référence à une ou plusieurs entrées learningObjectResource via relations.loResources.
- _learningObjectResource (type : learningObjectResource)_
   - Contient la configuration commune (type de contenu, version, etc.) et localizedMetadata multilingue.
   - Liens vers une ou plusieurs entités de ressource via relations.resources.
- _ressource (type : ressource)_
   - *Une par locale*, chacune avec son propre identifiant, sa propre langue, son propre nom et sa propre URL (location/downloadUrl).

Dans le cas d’une assistance à la tâche multilingue, le schéma typique est le suivant :

- learningObjectResource avec localizedMetadata pour en-US et fr-FR
- relations.resources.data pointant vers :
   - ressource avec paramètres régionaux : « fr-FR »
   - ressource avec paramètres régionaux : « fr-FR »

Les clients peuvent sélectionner la ressource appropriée en faisant correspondre les paramètres régionaux de l’élève au champ resource.attributes.locale.

### Nouveau format d&#39;ID de ressource pour les assistances à la tâche

Pour distinguer correctement plusieurs variantes localisées d&#39;une ressource d&#39;assistance à la tâche, le format _ID de ressource a été modifié_.

_Ancien format d&#39;ID de ressource (hérité)_

Auparavant, les ressources d’assistance à la tâche utilisaient un format d’ID opaque, tel que :

jobAid:131032_-1_-1_2_resource

Ce format ne codait pas les paramètres régionaux et les API n’exposaient efficacement qu’une seule ressource (généralement en-US).

_Nouveau format d&#39;ID de ressource (compatible multilingue)_

Le nouveau format est le suivant :

```
jobAid:<jobAidId>_<version>_<localeCode>
```

Exemples :

- jobAid:131032_2_en-US
- jobAid:131032_2_fr_FR
- jobAid:131032_2_es_ES

Décomposition visuelle :

```
jobAid:131032_2_fr_FR

        │      │ │ │

        │      │ │ └──► Locale Code (fr_FR, en_US, es_ES, etc.)

        │      │ └────► Version (2)

        │      └──────► JobAid ID (131032)

        └─────────────► Resource Type Prefix ("jobAid:")
```

Cette structure permet aux clients :

- Identifiez rapidement l’assistance à la tâche et la version à laquelle appartient une ressource.
- Déduisez directement les paramètres régionaux à partir de l’ID de ressource lorsque cela est nécessaire.

### Rétrocompatibilité : 

```/resources/{resourceId}```

Le point de terminaison de ressource hérité reste disponible :

```GET /primeapi/v2/resources/{resourceId}

```

Il est désormais _rétrocompatible_ avec les anciens et les nouveaux formats d&#39;ID :

- _Ancien format d&#39;ID_ (par exemple, jobAid:131032_-1_-1_2_resource)
   - Continue à travailler.
   - Retourne la _première ressource créée_ associée à cet identifiant hérité (généralement la ressource en-US d&#39;origine).
- _Nouveau format d&#39;ID_ (par exemple, jobAid:131032_2_fr_FR)
   - Retourne la _ressource exacte spécifique aux paramètres régionaux_ correspondant à cet ID.
   - Cela permet une récupération et une manipulation précises des variantes d’assistance à la tâche localisées.

Les intégrations qui stockent ou référencent actuellement les anciens ID de ressource peuvent continuer à fonctionner sans changement, tandis que les implémentations plus récentes sont encouragées à adopter le nouveau format d&#39;ID pour les opérations spécifiques aux paramètres régionaux.

### Considérations relatives à l’intégration et à l’expérience utilisateur

- _Interface utilisateur Élève/Administrateur_
   - Utilisez learningObject.localizedMetadata et learningObjectResource.localizedMetadata pour présenter les titres et les descriptions dans la langue appropriée.
   - Utilisez resource.attributes.locale pour sélectionner l’URL correcte (emplacement / downloadUrl) pour les paramètres régionaux de l’élève.
   - Mettez en œuvre un comportement de secours (par exemple, revenir à en-US) si les paramètres régionaux exacts d’un élève ne sont pas disponibles.
- _API et stockage_
   - Pour les nouvelles intégrations, stockez les _ID de ressource au nouveau format_ (```jobAid:<jobAidId>_<version>_<localeCode>```) pour permettre une récupération non ambiguë spécifique aux paramètres régionaux.
   - Les ID hérités peuvent toujours être utilisés avec /resources/{resourceId}, mais ils ne feront pas la distinction entre les paramètres régionaux.

## Contraintes de créneau horaire pour le démarrage de modules

Certaines expériences d’apprentissage ne doivent être disponibles que dans une fenêtre temporelle définie. La version affiche des informations de créneau horaire sur les ressources d&#39;objet d&#39;apprentissage et introduit un point de terminaison de validation qui vérifie si un élève peut démarrer une ressource à l&#39;instant présent.

Les métadonnées de créneau horaire sont disponibles via le point d’entrée :

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

Au niveau de la ressource de l&#39;objet d&#39;apprentissage, un objet timeSlot peut désormais être présent dans les attributs, avec les valeurs startTime et endTime en UTC. Cette option spécifie la fenêtre pendant laquelle la ressource peut être démarrée.

Avant de lancer un module, les intégrations peuvent appeler un nouveau point de terminaison de validation :

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

Ce point de terminaison, destiné aux scénarios lus par l&#39;élève, renvoie si l&#39;élève est actuellement autorisé à démarrer la ressource, en tenant compte du créneau horaire configuré, du type de livraison et d&#39;autres règles d&#39;arrière-plan.

Les lecteurs personnalisés et les applications clientes doivent utiliser canStart pour appliquer l’accès basé sur le temps et utiliser les métadonnées timeSlot pour afficher un message clair indiquant quand le contenu devient disponible ou expire. Les réponses négatives de canStart doivent être traitées explicitement pour informer les élèves des raisons pour lesquelles le contenu ne peut pas encore être démarré ou plus.

## Questionnaires axés sur le contenu et à tentatives multiples

Certains packages de contenu mettent en œuvre leur propre suivi des tentatives plutôt que de dépendre uniquement de Adobe Learning Manager. L’autorisation introduit un indicateur qui indique quand les tentatives sont pilotées par le contenu lui-même.

Via :

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

Les ressources d’objet d’apprentissage peuvent désormais exposer un attribut booléen hasContentDrivenAttemptTracking. Lorsque c’est le cas, le quiz ou module gère les tentatives en interne (par exemple, via la logique SCORM ou xAPI) et les compteurs de tentatives standard de la plateforme peuvent ne pas refléter entièrement l’expérience de l’élève.

Les intégrations qui affichent le nombre de tentatives ou contrôlent le comportement des nouvelles tentatives doivent cocher cet indicateur. Lorsqu’elle est activée, ils ne doivent pas déduire de limites de tentatives uniquement à partir des métadonnées de la plateforme et doivent être prêts à s’appuyer sur des rapports côté contenu (par exemple, via des instructions xAPI) ou sur des règles spécifiques à l’entreprise.

## Changement de comportement dans le format d&#39;ID de ressource d&#39;assistance à la tâche

Cette version introduit un __changement de comportement__ important dans le format des ID de ressource d&#39;assistance à la tâche. Bien qu’aucun nouveau point de terminaison ne soit impliqué, cela a un impact direct sur les systèmes qui stockent ou analysent ces ID.

Auparavant, les ID de ressource d&#39;assistance à la tâche utilisaient un format tel que :

```jobAid:<jobAidId>_-1_-1_2_resource```

Dans la version d’avril 2026, ce format est remplacé par un format simplifié et plus explicite :

```jobAid:<jobAidId>_<version>_<localeCode>```

Par exemple :

jobAid:131032_2_fr_FR

Les composants sont les suivants :

- ```<jobAidId>``` : ID d&#39;assistance à la tâche numérique (par exemple, 131032),
- ```<version>``` : numéro de version de l&#39;assistance à la tâche (par exemple, 2),
- ```<localeCode>``` : code de paramètres régionaux (par exemple, en_US, fr_FR, es_ES).

Toute intégration qui indexe des ressources ou est conservée dans les ID de ressources d&#39;assistance à la tâche doit mettre à jour sa logique d&#39;analyse et de stockage pour reconnaître le nouveau format. Étant donné que les identificateurs eux-mêmes changent, il est fortement recommandé de reconstruire tous les index locaux clés par des ID de ressource d’assistance à la tâche après la mise à niveau vers la version d’avril 2026.

## Définition d’images de bannière de cours via la migration

Vous pouvez désormais définir ou mettre à jour les images de bannière de cours dans Adobe Learning Manager dans le cadre de votre workflow de migration standard. Cela vous permet de lancer ou de nettoyer des catalogues volumineux tout en conservant la cohérence visuelle de vos pages de cours, sans les modifier manuellement

### Où les images de bannière sont définies

Les images de bannière sont configurées dans le fichier de migration _course.csv_, que vous utilisez déjà pour fournir des métadonnées de cours telles que :

- l&#39;identifiant
- courseName
- courseCreationDate
- l&#39;état
- auteur
- thumbnailUrl

Grâce à cette amélioration, la spécification course.csv inclut une _colonne facultative_ supplémentaire pour l&#39;image de bannière de cours. Le nom exact de l’en-tête est défini dans la spécification CSV que vous téléchargez à partir de votre compte Learning Manager (par exemple, il peut apparaître sous la forme bannerUrl ou bannerImageUrl).

La colonne de bannière :

- Pointe vers le fichier image à utiliser comme _bannière de cours_.
- Fonctionne de la même manière que thumbnailUrl, en utilisant des images disponibles dans votre référentiel de contenu configuré (Box/FTP).

### Préparation des images de bannière pour la migration

1. Charger les images de bannière : placez vos fichiers d’image de bannière dans le même emplacement Box ou FTP que celui que vous utilisez pour les autres ressources de migration, en suivant la structure de répertoires existante.
2. Vérifier le format de fichier :
Utilisez l’un des formats d’image pris en charge (par exemple png, jpg, jpeg, gif), comme décrit dans la configuration requise :
   1. [*Configuration requise*](/help/migrated/system-requirements.md)
3. Mettre à jour course.csv : dans la nouvelle colonne de bannière, référencez le chemin relatif ou l’identifiant de l’image de bannière. Exemple conceptuel :

```
id,courseName,courseCreationDate,state,author,thumbnailUrl,bannerUrl  
12345,DEMO1,2018-05-05T08:56:21.000Z,Published,Sudheer,pic1.png,banners/banner1.png  
45678,DEMO2,2018-05-05T08:56:21.000Z,Published,Sudheer,pic2.png,banners/banner2.png  
```

### Application de bannières pendant une exécution de migration

Une fois votre fichier course.csv mis à jour, le flux est le même que pour toute autre migration :

1. _Charger des fichiers CSV_
Chargez le fichier course.csv mis à jour (et tout autre fichier pertinent) dans le dossier Box/FTP configuré pour la migration. Les noms de fichiers doivent correspondre exactement aux noms spécifiés dans csv_specifications.zip (ils sont sensibles à la casse).
2. _Démarrer une exécution de sprint_
Dans Adobe Learning Manager, en tant qu’administrateur de l’intégration, démarrez une migration _sprint run_ qui inclut course.csv.\
   Le moteur de migration lit la colonne de bannière et applique l’image de bannière à chaque cours.
3. _Examen des résultats et des journaux d’erreurs_
Après le sprint :
   1. Vérifiez les bannières dans les applications _Auteur_ et _Élève_.
   2. Si certaines lignes échouent (par exemple, en raison d’un chemin de fichier non valide ou d’un format non pris en charge), téléchargez le fichier CSV d’erreur à partir de l’exécution de migration et corrigez les données.

### Nouveaux cours et cours existants

Le champ de bannière fonctionne dans les deux scénarios :

- _Nouveaux cours créés via la migration_
Lorsqu&#39;un cours est créé pour la première fois à partir de course.csv et que la colonne de bannière est remplie, cette bannière est immédiatement définie.
- _Cours existants (mise à niveau/corrections)_
Si vous réexécutez la migration avec le même ID de cours et une nouvelle valeur de bannière :
   - Learning Manager localise le cours existant.
   - L&#39;image de bannière est _mise à jour_ vers la nouvelle image spécifiée dans le fichier CSV.

Vos noms et chemins de colonne réels doivent correspondre à la _spécification CSV téléchargée_ et à la mise en page de votre référentiel de contenu.

## Supprimer la colonne d’ordre dans LearningProgramCourse

Adobe Learning Manager prend désormais en charge un modèle simplifié de _commande de cours dans les Parcours d’apprentissage (programmes d’apprentissage)_ pendant la migration. Dans le cadre de cette modification, la colonne _commande est supprimée_ du fichier de migration learning_program_course.csv.

Auparavant, le fichier learning_program_course.csv incluait une colonne (souvent appelée order ou similaire) qui était utilisée pour :

- Définissez explicitement la _position_ de chaque cours dans un programme d’apprentissage, en fonction de la valeur numérique de cette colonne.
- Exigez des administrateurs ou des scripts qu&#39;ils gèrent manuellement cette séquence numérique, en particulier lors de l&#39;insertion ou de la réorganisation de cours.

Désormais, Adobe Learning Manager n’utilise plus la colonne Ordre dans learning_program_course.csv pour déterminer l’ordre des cours. Au lieu de cela, le fichier CSV de migration se concentre sur _l&#39;appartenance des cours à chaque programme d&#39;apprentissage_, plutôt que sur leur ordre numérique.

## Impact sur les fichiers CSV de migration

### learning_program_course.csv

Vous devez traiter la colonne d’ordre héritée comme supprimée ou ignorée :

- Ne vous fiez pas à afin de contrôler la séquence de cours dans un programme d’apprentissage pendant la migration.
- Si vous disposez toujours d’une colonne de commande provenant d’anciens modèles :
   - Learning Manager l’ignorera pour la commande.
   - Vous pouvez le supprimer en toute sécurité de votre fichier CSV au fil du temps pour simplifier vos fichiers de migration.
- La mise en correspondance essentielle requise demeure la suivante :
   - ID du programme d’apprentissage ↔ ID du cours (et toute autre colonne encore documentée telle que id, learningProgramId, courseId et dates).

Reportez-vous toujours aux [_spécifications CSV_](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual) les plus récentes de votre compte Learning Manager (via csv_specifications.zip) pour confirmer l’ensemble d’en-têtes et les exigences actuelles.

## timeZoneCode sur les instances de cours

À partir de cette version, le modèle d’instance de cours (learningObjectInstance) expose un nouvel attribut :

timeZoneCode : champ de chaîne qui lie explicitement une instance de cours à l&#39;un des fuseaux horaires configurés du compte.

Cela permet aux clients de :

- Résolvez le fuseau horaire d&#39;une instance de cours de manière cohérente et basée sur l&#39;API.
- Interprétez et affichez correctement toutes les dates/heures au niveau de l&#39;instance pour cette instance, quel que soit le fuseau horaire de l&#39;utilisateur.

### Où timeZoneCode apparaît

Le champ est ajouté dans les attributs du modèle learningObjectInstance
pour les instances de cours uniquement.

Exemple :

```
{
  "id": "course:1262748_1359228",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2019-08-06T13:50:39.000Z",
    "isAET": false,
    "isDefault": true,
    "timeZoneCode": "356",
    "isFlexible": false,
    "state": "Active",
    "localizedMetadata": [
      {
        "locale": "en-US",
        "name": "Default instance"
      }
    ]
  }
}
```

### Comment résoudre timeZoneCode

Le code de fuseau horaire numérique est une clé de recherche dans le catalogue de fuseau horaire du compte, qui s’affiche via l’API de compte :

```http
GET /primeapi/v2/account
Authorization: Bearer <access_token>
```

Dans la réponse, les fuseaux horaires sont répertoriés dans :

```
"data": {
  "attributes": {
    "timeZones": [
      {
        "name": "Etc/GMT+12",
        "timeZoneCode": "356",
        "utcOffset": -720,
        "utcOffsetCode": "UTC-12:00(Etc/GMT+12)",
        "zoneId": "Etc/GMT+12"
      },
      "..."
    ]
  }
}
```

### Flux client recommandé :

1. Appelez GET /account une fois, cache attributes.timeZones pour le client.
2. Pour chaque instance de cours :
   - Lire attributes.timeZoneCode.
   - Recherchez l&#39;entrée correspondante dans timeZones où timeZoneCode correspond.
   - Utilisez les valeurs zoneId, utcOffset et utcOffsetCode de cette entrée pour la logique d&#39;affichage et de planification.

## API publiques asynchrones pour l’appartenance à un groupe d’utilisateurs

### Introduction

Adobe Learning Manager expose deux _API asynchrones administrateur_ pour gérer l’appartenance à un groupe d’utilisateurs :

- POST /async/userGroups/{userGroupId}/users - ajouter des utilisateurs à un UG de manière asynchrone
- DELETE /async/userGroups/{userGroupId}/users - supprimer des utilisateurs d&#39;un UG de manière asynchrone

Au lieu de mettre à jour l&#39;abonnement dans la même demande, ces API acceptent votre lot et renvoient un _ID d&#39;événement_. Le résultat réel est fourni ultérieurement via des webhooks.

Utilisez-les lorsque :

- Vous gérez de grands groupes ou des mises à jour par lots fréquentes.
- La latence est moins importante que la fiabilité et le débit.
- Vous créez des intégrations (RH, CRM, LXP) plutôt que des clics d’interface utilisateur.

Pour les petites actions d&#39;administration interactives, vous pouvez continuer à utiliser les API `/userGroups/{id}/users` synchrones.

### Authentification et URL de base

Ces API font partie de la surface standard de l&#39;__API d&#39;administration v2__.

- [URL de base (prod)](https://learningmanager.adobe.com/docs/primeapi/v2/)
- Auth : jeton d’accès OAuth 2.0 avec portée `admin:write`
- En-têtes requis :
   - Autorisation : Bearer &lt;access_token>
   - Content-Type : application/json
   - Accepter : application/json

Pour connaître le comportement et les portées de l’API d’administration, voir :

- [Manuel du développeur](/help/migrated/integration-admin/feature-summary/developer-manual.md)
- [Guide de référence de l’API](https://learningmanager.adobe.com/docs/primeapi/v2/)

### Format de la demande

Les options __ajouter__ et __supprimer__ utilisent exactement la même forme de corps.

#### Body

```
{
  "metadata": {
    "event_id": "my-optional-correlation-id",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

#### données (obligatoire)

données est la liste des identificateurs de ressources utilisateur pour ce lot.

- `type` doit être « utilisateur ».
- `id` est l&#39;_ID utilisateur numérique_ dans ALM (pas l&#39;adresse e-mail, pas l&#39;UUID).

#### Contraintes

- `data` doit être présent et non vide.
- Au moins un utilisateur est requis.
- La taille maximale de la charge utile est de 20 utilisateurs par demande.
- Tous les ID doivent être numériques et faire référence à des utilisateurs valides.

Si l’une de ces conditions échoue, l’API renvoie une erreur et rien n’est mis en file d’attente.

#### métadonnées (facultatif)

`metadata` toutes les données de corrélation supplémentaires que vous souhaitez retrouver dans le webhook.

Utilisation standard :

- `event_id` - ID de corrélation que vous générez.
- `sourceSystem` - nom de votre système en amont.
- `batchId` - identifiants de lot ou de tâche.

Le service renvoie cet objet sans le modifier dans la réponse du webhook, afin que vous puissiez faire correspondre le rappel à votre tâche interne.

Contraintes :

- Facultatif ; peut être entièrement omis.
- La longueur combinée de toutes les touches et valeurs ne doit pas dépasser 1 000 caractères.

### Format de réponse

Les deux points de terminaison répondent de manière synchrone avec un ID d’événement :

```
{ "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" }
```

Comportement :

- Si `metadata.event_id` est passé, cette valeur est utilisée.
- Sinon, le service génère un UUID.

Vous devez toujours :

- Stockez ce `event_id` en tant qu&#39;identificateur principal pour le lot.
- Attendez-vous à recevoir la même valeur dans le rappel de webhook.

Affichez [Webhooks pour l’ajout et la suppression d’appartenances à un groupe d’utilisateurs](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-adding-and-removing-user-group-membership) pour plus de détails.

## Foire aux questions

_En quoi la version d’avril 2026 modifie-t-elle l’API learningObjects pour les programmes d’apprentissage adaptatif ?_

Cette version ajoute un indicateur isAdaptive aux programmes d’apprentissage et prend en compte les sections et les sous-objets d’apprentissage. Dans les programmes adaptatifs, les élèves ne voient que les sections et les objets de sous-apprentissage qui leur sont visibles en fonction de règles adaptatives, tandis que les administrateurs peuvent voir la configuration adaptative sous-jacente d&#39;un groupe d&#39;utilisateurs.

_Dois-je mettre à jour mon intégration si elle suppose que toutes les sections et les sous-objets d’apprentissage sont toujours renvoyés ?_

Oui. Pour les programmes d’apprentissage adaptatif, l’API renvoie désormais uniquement les sections et les sous-objets d’apprentissage qui sont visibles par l’élève actuel. Le code client doit traiter la réponse comme une vue faisant autorité, éventuellement filtrée, au lieu d&#39;assumer une liste complète.

_Comment puis-je réinitialiser par programme l’achèvement d’un élève pour un cours ou un programme d’apprentissage ?_

Utiliser le nouveau point de terminaison :

```POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion```
Cela réinitialise l&#39;achèvement pour l&#39;instance ciblée lorsque les autorisations et l&#39;état l&#39;autorisent.

_Comment savoir si un élève a terminé quelque chose via un objet d’apprentissage alternatif ou équivalent ?_

Vérifiez l’attribut isAlternateComplete sur l’objet d’apprentissage. Si c’est le cas, la relation alternateCompletions répertorie les objets d’apprentissage qui ont servi d’alternatives à l’achèvement de cet élève.

_Comment puis-je trouver toutes les alternatives qui peuvent satisfaire un objet d’apprentissage particulier ?_

Utilisez le point d’entrée suivant :

```GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}```

et utilisez le tableau de données (pour les variantes) et meta.count (pour le nombre total de variantes).

_Comment savoir si un élève est autorisé à démarrer un module pour le moment ?_

Tout d&#39;abord, récupérez l&#39;intervalle de temps de la ressource à partir de :

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```
puis utilisez :

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

_Que signifie hasContentDrivenAttemptTracking sur une ressource ?_

Cela indique que le suivi des tentatives est contrôlé par le contenu lui-même (par exemple, via la logique SCORM/xAPI) plutôt que par les compteurs de plateforme uniquement. Lorsque c’est vrai, ne vous fiez pas uniquement au nombre de tentatives de plateforme ou aux limites pour votre UX et vos rapports.

_Comment obtenir des menus adaptés aux utilisateurs non connectés (expériences publiques) ?_

Utilisation :

```GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true```

Cela renvoie des structures de menu et de page filtrées pour les utilisateurs anonymes, adaptées à Experience Builder ou à d’autres sites sans en-tête.

_Qu&#39;est-ce qui a changé dans le filtrage des assistances à la tâche avec effectiveModifiedDate ?_

Les demandes qui combinent filter.effectiveModifiedDate avec filter.loTypes=jobAid retournent désormais correctement uniquement les assistances à la tâche dans la fenêtre de date spécifiée.

_Qu&#39;est-ce qui a changé dans le format d&#39;ID de ressource d&#39;assistance à la tâche et comment dois-je le gérer ?_

Le format d’ID a changé pour des valeurs telles que :

```jobAid:<jobAidId>_-1_-1_2_resource```

à :

```jobAid:<jobAidId>_<version>_<localeCode>```

par exemple jobAid:131032_2_fr_FR. Tout système qui stocke ou analyse les ID de ressource d’assistance à la tâche doit être mis à jour. Vous devez prévoir de reconstruire les index locaux clés par ces ID après la mise à niveau vers la version d’avril 2026.
