---
description: Explique comment Experience Builder peut publier des pages d’apprentissage et des catalogues publics pour les visiteurs anonymes, y compris les fonctionnalités clés, les widgets pris en charge, les conditions préalables (Connecteur d’accès aux données de formation), les limitations et des conseils pour la configuration, l’évolutivité et la migration à partir de la page d’accueil héritée sans connexion.
jcr-language: en_us
title: Configuration et gestion des pages non connectées dans Experience Builder
exl-id: e4685cab-08ca-4b6b-93f4-a9eecf382dc4
source-git-commit: 2f9e931523da6e3e1ed2cf60f1ad05f5caf3cc1b
workflow-type: tm+mt
source-wordcount: '6058'
ht-degree: 1%

---


# Expérience hors connexion dans Experience Builder

## Introduction

L’expérience hors connexion dans Experience Builder permet aux organisations d’afficher leur contenu d’apprentissage et leurs pages de portail à tous les visiteurs, y compris ceux qui ne sont pas connectés. Cette fonctionnalité est conçue pour attirer, informer et impliquer les élèves potentiels en offrant un aperçu fluide et de marque de vos offres de formation avant qu’ils ne soient tenus de se connecter ou de s’inscrire.

Cette fonctionnalité vous permet de créer et de personnaliser des pages accessibles au public à l’aide de la même interface conviviale de glisser-déposer que celle d’Experience Builder standard. Vous pouvez présenter les catalogues de cours, les catégories, les parcours et le contenu statique enrichi, y compris les images, le texte, le HTML et les iframes intégrés, à toute personne visitant votre portail. Il est ainsi facile de mettre en évidence vos programmes d&#39;apprentissage, de promouvoir de nouveaux cours et de fournir des informations essentielles à un public plus large.

Les visiteurs peuvent parcourir le catalogue, afficher des détails sur les cours et les instances, et utiliser la recherche globale pour explorer les possibilités de formation disponibles. Cependant, les actions qui nécessitent l’identité d’un utilisateur, telles que l’inscription à un cours, l’accès à des fonctionnalités personnalisées (comme Calendrier, Conformité, Tableau des scores ou Apprentissage par les réseaux sociaux) ou la consommation d’une formation, invitent le visiteur à se connecter. Cette approche garantit que les informations sensibles et personnalisées restent sécurisées tout en permettant une expérience d’aperçu complète.

Les administrateurs peuvent configurer les pages et widgets visibles pour les utilisateurs qui ne sont pas connectés, en s’assurant que seul le contenu approprié est affiché. Les pages peuvent être définies pour être accessibles aux utilisateurs connectés et non connectés, ou exclusivement pour l’un de ces groupes. Experience Builder offre un mode d’aperçu, qui vous permet de voir exactement comment vos pages apparaîtront aux visiteurs avant leur publication.

Pour activer cette fonctionnalité, votre administrateur d’intégration ALM doit activer le connecteur d’accès aux données de formation. Ce connecteur garantit que les métadonnées de cours sont accessibles au public.

L’image de marque et la localisation sont entièrement prises en charge, ce qui vous permet de personnaliser les titres de page, les icônes et les paramètres linguistiques pour les aligner sur l’identité de votre organisation et répondre aux besoins de votre public. Dans le cadre de la transition vers cette expérience améliorée, la fonctionnalité héritée de la page d’accueil pour les utilisateurs non connectés sera obsolète. Par conséquent, tout nouveau contenu public doit être créé à l’aide d’Experience Builder.

## Objectif de la fonctionnalité

L’expérience hors connexion dans Experience Builder permet aux organisations de présenter publiquement leur contenu d’apprentissage et leurs pages de portail à quiconque, sans exiger que les utilisateurs se connectent. Cela permet d’attirer, d’informer et d’impliquer les élèves potentiels en fournissant un aperçu des formations et des ressources disponibles avant que l’inscription ou l’authentification ne soient nécessaires.

## Cas d’utilisation réels de l’expérience hors connexion

- **Marketing et sensibilisation** : les organisations peuvent promouvoir leurs programmes de formation auprès de publics externes, tels que les clients potentiels, les partenaires ou les candidats à un emploi, en rendant les catalogues de cours et les détails du programme accessibles au public.
- **Exploration avant inscription** : les élèves peuvent parcourir les cours disponibles, afficher des aperçus et explorer les catégories avant de décider de s&#39;inscrire ou de se connecter, ce qui les aide à prendre des décisions éclairées en matière d&#39;inscription.
- **Portails de formation d’entreprise** : les entreprises peuvent fournir un portail public pour les informations de conformité ou d’intégration, ce qui permet aux nouveaux embauchés ou sous-traitants de voir quelle formation est disponible avant de recevoir des informations d’identification.
- **Pages de destination des événements ou des campagnes** : les organisations qui mènent des campagnes d’apprentissage ou des événements peuvent créer des pages publiques dédiées pour mettre en évidence les cours, calendriers ou ressources en vedette, ce qui augmente la visibilité et l’engagement.
- **SEO et découvrabilité** : en rendant publiques certaines pages et certains catalogues, les organisations améliorent la visibilité de leurs moteurs de recherche, ce qui permet aux utilisateurs de découvrir plus facilement leurs offres d’apprentissage en ligne.

## Concepts clés de l’expérience hors connexion

L’expérience hors connexion d’Experience Builder vous permet de présenter publiquement du contenu d’apprentissage et des pages de portail, ce qui permet aux visiteurs de parcourir le site sans se connecter.

- **Créer des pages et des menus publics** : vous configurez des pages et un menu unique auxquels tout le monde peut accéder, quel que soit le statut de connexion.
- **Ajouter uniquement les widgets pris en charge** : vous incluez des widgets qui n’ont pas besoin du contexte utilisateur (catégories, cours et parcours d’apprentissage, zone de contenu, HTML, iframe), tandis que le système masque les widgets spécifiques à l’utilisateur.
- **Configurer le comportement de page adaptatif** : vous décidez si une page apparaît pour les utilisateurs connectés et non connectés, et si le système adapte les widgets et le contenu visibles en fonction de l&#39;état de connexion.
- **Prévisualiser les deux expériences** : vous utilisez les options d&#39;aperçu pour voir à quoi ressemblent les pages pour les utilisateurs connectés et non connectés, avec des différences de visibilité et de contenu du widget.
- **Activer la recherche globale** : les visiteurs recherchent des cours et du contenu, mais n&#39;obtiennent que des fonctionnalités de recherche de base sans intégration avancée de l&#39;IA.
- **Autoriser les visiteurs à parcourir les aperçus de catalogue et de cours** : les visiteurs explorent les pages de catalogue, les détails de cours et les instances, mais doivent se connecter pour s&#39;inscrire ou accéder à des fonctionnalités personnalisées.
- **Personnalisation de l&#39;image de marque et de la localisation** : vous définissez des favicons et des paramètres de langue pour répondre aux besoins de votre organisation en matière d&#39;image de marque et d&#39;accessibilité.
- **Activer le connecteur d&#39;accès aux données de formation** : vous activez ce connecteur pour exporter les métadonnées du cours pour un affichage public, en conservant les pages non connectées à jour.
- **Gérer un trafic élevé avec une infrastructure partagée** : le système gère de gros volumes de visiteurs anonymes à l&#39;aide de ressources partagées et de la limitation de débit.
- **Optimiser pour le référencement** : la plateforme prépare des pages publiques pour l&#39;indexation des moteurs de recherche, ce qui facilite la recherche de votre contenu d&#39;apprentissage.

## Conditions préalables pour l’expérience hors connexion

- Vous devez activer le Connecteur d’accès aux données de formation dans l’administrateur d’intégration avant de pouvoir utiliser l’expérience hors connexion.
- Le connecteur exporte les métadonnées du cours vers un référentiel public, qui met à jour les pages non connectées.

### Initialisation du connecteur TDA

Le connecteur Training Data Access (TDA) est un prérequis essentiel à l’activation de la nouvelle fonctionnalité du créateur d’expérience hors connexion dans ALM. Ce connecteur facilite l’exportation des métadonnées de formation, ce qui permet à votre portail d’afficher des informations sur les cours pour les utilisateurs qui ne sont pas connectés.

- **Activation du connecteur** : vous devez activer le connecteur TDA à partir du panneau d&#39;administration de l&#39;intégration. Cette étape déverrouille la fonctionnalité du créateur d’expérience non connectée et rend les options d’interface utilisateur pertinentes visibles dans votre interface d’administration.
- **Exportation de métadonnées** : une fois activé, le connecteur exporte les métadonnées de formation essentielles (telles que le nom du cours, la description, la présentation, l’évaluation, la durée et les compétences) d’ALM vers un référentiel public. Ces données sont utilisées pour remplir les pages et les widgets non connectés.
- **Planification et synchronisation** : le processus d&#39;exportation peut être planifié (par exemple, quotidiennement) pour s&#39;assurer que votre portail reflète les dernières mises à jour de cours. Les modifications apportées dans ALM apparaîtront sur vos pages non connectées après le prochain cycle d’exportation, sous réserve de la mise en cache et de la fréquence d’exportation.
- **Disponibilité des fonctionnalités** : les fonctionnalités du créateur d’expérience non connectées, y compris la création de menus, la prise en charge des widgets et la visibilité des catalogues, ne sont accessibles qu’après l’initialisation du connecteur TDA. Si le connecteur n’est pas activé, votre Experience Builder restera limité aux scénarios d’utilisateur connecté.
- **Migration et prise en charge** : pour les comptes en transition à partir des fonctionnalités héritées de la page d’accueil non connectées, l’initialisation du connecteur TDA est la première étape vers la migration. Cela vous permet de tirer parti de la flexibilité et des fonctionnalités améliorées du nouveau créateur d’expérience.

## Ce que les visiteurs peuvent faire sans se connecter

Sur un site Experience Builder non connecté, les visiteurs peuvent parcourir le catalogue de formation en ouvrant la page du catalogue pour les catalogues publics. Ils peuvent utiliser des filtres tels que le catalogue, le produit, le rôle, le type, les compétences et les balises, selon la façon dont vous avez configuré le site. Les visiteurs peuvent également rechercher des formations à l’aide de la barre de recherche globale dans l’en-tête (si activée) et afficher les résultats de la recherche directement sur la page du catalogue.

Les visiteurs peuvent afficher les détails de la formation en ouvrant des pages de présentation pour les cours, les parcours d’apprentissage et les certifications. Ces pages affichent les métadonnées clés, notamment le titre, la description, l’auteur, la durée, le format, les balises et les compétences.

De plus, les visiteurs peuvent explorer le contenu statique et promotionnel. Ils peuvent lire des blocs de texte et de contenu enrichi, afficher des bannières et des vignettes d’image, et interagir avec des iframes intégrés tels que des microsites externes, des vidéos ou des outils.

Si un visiteur clique sur S’inscrire ou tente de commencer la formation, le système l’invite à se connecter ou à s’inscrire. Une fois la connexion réussie, le visiteur est redirigé vers la page appropriée, qu’il s’agisse de la page d’accueil, d’une page personnalisée ou de la formation spécifique qu’il a sélectionnée.

## Éléments non disponibles sans connexion

Sur un site Experience Builder non connecté, les visiteurs ne peuvent pas accéder aux fonctionnalités ou au contenu qui nécessitent l’authentification de l’utilisateur. Ils ne peuvent pas s’inscrire à des formations, commencer ou suivre des cours, ni accéder à des widgets personnalisés tels que Mon apprentissage, Calendrier, Conformité, Tableau des scores ou Apprentissage par les réseaux sociaux. Ces widgets dépendent de données spécifiques à l’utilisateur et ne sont disponibles qu’après la connexion.

Les visiteurs ne peuvent pas non plus effectuer d&#39;actions telles que l&#39;inscription à un cours ou l&#39;accès à un contenu qui nécessite un suivi de la progression ou du contexte utilisateur. Si vous tentez de vous inscrire ou de démarrer une formation, le visiteur est invité à se connecter ou à s’inscrire avant de continuer.

## Widgets pris en charge en mode hors connexion

En mode non connecté, seuls les widgets qui ne nécessitent pas de données spécifiques à l’utilisateur sont pris en charge. Il s’agit notamment :

- le widget Catégories, qui affiche les catégories de formation disponibles.
- Widget Cours et parcours, qui affiche les cours et parcours d’apprentissage du catalogue public. 1
- Zone de contenu, pour ajouter du texte statique, des images ou du contenu promotionnel.
- widget de HTML, pour l’incorporation de contenu de HTML personnalisé.
- Widget Iframe, pour afficher des sites externes, des vidéos ou des outils dans la page.
- Les widgets qui nécessitent un contexte utilisateur, tels que Mon apprentissage, Calendrier, Conformité, Tableau des scores et Apprentissage par les réseaux sociaux, ne sont pas disponibles en mode non connecté.

Les widgets qui nécessitent un contexte utilisateur, tels que Mon apprentissage, Calendrier, Conformité, Tableau des scores et Apprentissage par les réseaux sociaux, ne sont pas disponibles en mode non connecté

## Pages et menus en mode hors connexion

- Un seul menu hors connexion est pris en charge, visible par tous les visiteurs sans authentification.
- Les pages peuvent être ajoutées aux menus connectés et non connectés ; si une page est connectée aux deux, elle adapte ses widgets et son contenu en fonction de l’état de connexion de l’utilisateur.
- Les menus hors connexion n’ont pas de ciblage d’audience ni de personnalisation. Tout le monde voit le même ensemble de pages.
- Les widgets non pris en charge en mode hors connexion sont masqués automatiquement ; la mise en page s’ajuste pour remplir les espaces.
- La gestion des menus et des pages (ajout, prévisualisation, suppression) est similaire au mode connecté, mais avec des adaptations pour les contraintes non connectées.

## Comportement de recherche et de catalogue

En mode hors connexion, les utilisateurs peuvent accéder à la page du catalogue et utiliser la recherche pour parcourir les cours et parcours d’apprentissage disponibles. La page du catalogue affiche tous les cours publics, ainsi que les filtres et la fonctionnalité de recherche, en suivant les mêmes paramètres de compte que ceux du mode connecté. Lorsqu&#39;un utilisateur effectue une recherche, les résultats s&#39;affichent sur la page du catalogue et les utilisateurs peuvent afficher les pages de présentation des cours et des instances sans se connecter. Cependant, les actions telles que l’inscription nécessitent une connexion.

Si un utilisateur tente de s’inscrire, le système exige qu’il se connecte d’abord. La recherche d’utilisateurs non connectés est plus simple que celle d’utilisateurs connectés et n’inclut pas de fonctionnalités avancées telles que l’intégration de l’assistant AI.

## Mise en œuvre technique

### Configuration du connecteur d&#39;accès aux données de formation

Vous devez activer le connecteur d’accès aux données de formation dans le panneau d’administration de l’intégration avant de pouvoir utiliser la fonctionnalité du créateur d’expérience non connecté. Ce connecteur exporte les métadonnées de formation d’ALM vers un référentiel public, ce qui les rend accessibles via des API pour vos pages non connectées. La configuration du connecteur est un prérequis pour l’activation de la fonctionnalité et garantit que votre portail affiche des informations de formation à jour.

Exportation et synchronisation des métadonnées\
Le connecteur exporte des champs de métadonnées clés tels que le nom du cours, la présentation, la description, l’évaluation, la durée et les compétences. Vous pouvez planifier des exportations (par exemple, quotidiennes) pour que votre portail reste synchronisé avec ALM. Tous les champs de métadonnées ne peuvent pas être inclus ; consultez les ingénieurs pour obtenir une liste complète. Les données exportées sont utilisées pour remplir les pages non connectées, et les modifications dans ALM apparaîtront après le prochain cycle d’exportation.

Mise en cache et exportation de la fréquence\
Le système utilise la fréquence d&#39;exportation du serveur principal et la mise en cache du serveur principal pour gérer les mises à jour des données. Les modifications apportées dans ALM sont répercutées sur votre portail après l’exportation planifiée et l’actualisation du cache. Certaines mises à jour peuvent ne pas apparaître immédiatement en raison de ces mécanismes. Si vous avez besoin de mises à jour plus rapides, ajustez la planification de l’exportation ou videz le cache selon vos besoins.

Prise en charge de la personnalisation CSS/JS\
Vous pouvez appliquer des feuilles de style CSS et JavaScript personnalisées aux pages connectées et non connectées à l’aide de l’onglet Personnalisation. Cela vous permet de maintenir une image de marque cohérente, d’ajouter des éléments d’interface utilisateur personnalisés et d’améliorer l’expérience utilisateur sur votre portail. Toutes les personnalisations sont appliquées globalement, garantissant un aspect unifié.

Différences d’URL et identité visuelle (icône favorite, titre de la page)\
Les pages non connectées et connectées peuvent avoir des URL différentes pour distinguer les états de l’utilisateur. Vous pouvez personnaliser l’icône favorite et le titre de la page pour votre portail, ce qui contribue à renforcer votre identité de marque. Ces fonctionnalités sont disponibles dans le créateur d’expérience ; consultez les ingénieurs pour connaître le dernier statut de la prise en charge hors connexion.

## Performances et évolutivité

### Pile partagée et pile Premium

La pile partagée permet à plusieurs clients d’utiliser le créateur d’expérience hors connexion sur l’infrastructure commune, prenant en charge les niveaux de trafic standard. La pile Premium est une option payante qui fournit des ressources dédiées, des fonctionnalités en temps réel et des limites de places plus élevées pour les clients ayant des besoins avancés. Choisissez la pile en fonction de votre trafic et de vos besoins commerciaux attendus.

### Limites de trafic et limitation du débit

La pile partagée applique des limites de trafic pour garantir une utilisation équitable entre les clients. L’ingénierie mettra en œuvre une limitation de débit pour empêcher un seul client de consommer toutes les ressources. Si vous planifiez des campagnes marketing ou prévoyez un trafic élevé, coordonnez-vous avec les ingénieurs pour comprendre vos limites et éviter les interruptions de service. La limitation de débit permet de maintenir la stabilité du système et les performances pour tous les utilisateurs.

Considérations relatives au multi-location et au référencement\
La plateforme prend en charge le multi-location, permettant à plusieurs clients d’héberger leurs portails sur des infrastructures partagées. Les pages non connectées sont SEO-friendly, ainsi que sitemap.xml et robots.txt pour optimiser la visibilité des moteurs de recherche. Cela garantit que votre portail est détectable et indexé de manière appropriée par les moteurs de recherche.

## Migration et dépréciation

### Transition depuis la page d’accueil existante sans connexion

La fonctionnalité héritée de la page d’accueil non connectée sera obsolète. Les nouveaux comptes ne verront pas cette option et les comptes existants qui l’utilisent seront informés de la migration vers la solution basée sur Experience Builder. Vous devez recréer votre page d’accueil à l’aide du nouveau créateur d’expérience pour bénéficier d’une flexibilité, d’une prise en charge des widgets et d’une expérience utilisateur améliorées. Le plan de transition assure une interruption minimale et un soutien continu.

Plan de communication\
Les clients qui utilisent la page d’accueil héritée recevront une communication claire sur le calendrier d’obsolescence et les étapes de migration. Une assistance sera fournie pour vous aider à déplacer votre page d’accueil vers la nouvelle plateforme experience builder, afin que vous puissiez bénéficier des nouvelles fonctionnalités et des mises à jour continues.

### Prise en charge de la localisation et de la connexion

Logique de secours des paramètres régionaux\
Le système affiche les pages dans les paramètres régionaux dans lesquels elles ont été créées. Si les paramètres régionaux d’un utilisateur ne sont pas disponibles, le système utilise une logique de secours pour sélectionner les meilleurs paramètres régionaux disponibles suivants. Cela garantit que les utilisateurs voient toujours le contenu dans une langue prise en charge, améliorant ainsi l’accessibilité et la satisfaction des utilisateurs.

Types de connexion pris en charge\
L’expérience hors connexion prend en charge tous les types de connexion disponibles dans ALM, y compris l’authentification unique et la connexion standard. Les utilisateurs peuvent parcourir le contenu sans se connecter et seront invités à se connecter si nécessaire, comme pour s&#39;inscrire à un cours ou accéder à des fonctionnalités personnalisées. Cela permet une transition en douceur de la navigation à l’engagement.

## API non connectées

### API de l’objet d’apprentissage d’administrateur

Les pages Experience Builder non connectées et les portails sans tête organisent ou filtrent souvent les cours en fonction du produit et du rôle. L’API Admin LO a été améliorée pour garantir que ces associations sont accessibles de manière cohérente pour les intégrations back-end et headless, ainsi que pour le connecteur TDA.

**Point de terminaison et comportement**

Vous continuez à utiliser le point de terminaison Admin LO existant :

GET /primeapi/v2/learningObjects/{loId}?forcedFields[learningObject]=products,roles


Où :

- loId est l&#39;ID de l&#39;objet d&#39;apprentissage (par exemple, course:12345).
- forcedFields[learningObject] indique à l&#39;API d&#39;inclure explicitement des produits et des rôles pour cet objet d&#39;apprentissage.

Pour ce faire, assurez-vous que les associations de produit et de rôle de l’objet d’apprentissage sont présentes dans la réponse lorsque celle-ci est demandée par l’intermédiaire des champs appliqués. La réponse contient ensuite, dans les attributs, les métadonnées de produit et de rôle nécessaires pour calculer ou afficher les produits recommandés (rec_products) et les rôles (rec_roles) pour Experience Builder et les autres utilisateurs.

Un appel typique d’un administrateur ou d’une intégration se présente comme suit :

curl -X GET \
  « https://{your-domain}/primeapi/v2/learningObjects/course:12345?forcedFields[learningObject]=products,roles » \
  -H « Autorisation : Porteur {admin_token} » \
  -H « Accepter : application/vnd.api+json »

Le fichier JSON LO renvoyé est la même structure de base qu’auparavant, mais vous pouvez désormais compter sur la présence de champs de produit/rôle lorsque vous les demandez avec forcedFields. Les intégrations qui n’utilisent pas forcément forcées continuent de se comporter comme auparavant.

### Liste des objets d’apprentissage - Prise en charge de JobAid dans le filtre Date de modification effective

**Objectif**

Le connecteur TDA (Training Data Access) et les implémentations sans tête doivent souvent effectuer une synchronisation incrémentielle, en fonction de la **date de modification effective** des objets d&#39;apprentissage. Jusqu&#39;à cette version, les assistances à la tâche (assistance à la tâche de type objet d&#39;apprentissage) n&#39;étaient pas correctement gérées lorsqu&#39;elles étaient combinées avec les filtres effectiveModifiedDate. Cette version corrige ce problème afin que les assistances à la tâche puissent être synchronisées de manière incrémentielle, tout comme les cours et les parcours d’apprentissage.

**Point de terminaison et comportement**

Vous utilisez le point de terminaison de liste d’objet d’apprentissage existant avec les filtres de date et le type d’objet d’apprentissage :

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Auparavant, lorsque filter.loTypes=jobAid était combiné à une plage effectiveModifiedDate, le filtre excluait effectivement les assistances à la tâche et l&#39;appel se comportait comme si les assistances à la tâche n&#39;étaient pas prises en charge.

À partir de cette mise à jour, l&#39;appel retourne uniquement les objets d&#39;apprentissage JobAid dont la date effectiveModifiedDate est comprise dans la fenêtre spécifiée.

```
{  
  "links": {  
    "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"  
  },  
  "data": [  
    {  
      "id": "jobAid:144968",  
      "type": "learningObject",  
      "attributes": {  
        "authorNames": ["Sid"],  
        "dateCreated": "2026-01-20T08:48:55.000Z",  
        "datePublished": "2026-01-20T08:48:55.000Z",  
        "dateUpdated": "2026-01-20T08:48:55.000Z",  
        "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",  
        "loType": "jobAid",  
        "loFormat": "Content",  
        "loResourceType": "Content",  
        "localizedMetadata": [  
          {  
            "description": "Link jobAid new",  
            "locale": "en-US",  
            "name": "Link jobAid new"  
          },  
          {  
            "description": "Link jobAid new fre",  
            "locale": "fr-FR",  
            "name": "Link jobAid new fre"  
          }  
        ],  
        "relationships": {  
          "authors": {  
            "data": [  
              { "id": "13385176", "type": "user" }  
            ]  
          },  
          "instances": {  
            "data": [  
              { "id": "jobAid:144891_-1", "type": "learningObjectInstance" }  
            ]  
          }  
        }  
      }  
    }  
  ]  
}
```

Cela signifie que vous pouvez désormais implémenter en toute sécurité des synchronisations d&#39;assistance à la tâche incrémentielles basées sur effectiveModifiedDate, comme vous le faites déjà pour les autres types.

Si vous omettez filter.loTypes=jobAid, le comportement des autres types d&#39;objet d&#39;apprentissage reste inchangé ; la modification n&#39;affecte que la combinaison de JobAid avec ce filtre.

### **API de menu : filtre de menu non connecté**

**Objectif**

Experience Builder et les frontends sans tête ont besoin d’un moyen simple de récupérer le **menu hors connexion** , celui qui définit la navigation pour les visiteurs publics. Avant cette version, vous deviez récupérer tous les menus, puis appliquer une logique personnalisée pour identifier celui qui représentait la navigation hors connexion. Cette version ajoute un filtre côté serveur simple.

**Point de terminaison et comportement**

Vous utilisez le point de terminaison de liste Menu existant avec un nouveau paramètre de requête :

GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true


Les points clés :

- include=pages,subMenus.pages est facultatif, mais recommandé lorsque vous avez besoin des détails de la page et du sous-menu dans la même réponse.
- isNonLoggedIn=true est une nouvelle version de cette version et indique au serveur de renvoyer uniquement les menus marqués comme non connectés.

Sans le paramètre isNonLoggedIn, le point de terminaison se comporte exactement comme auparavant et renvoie des menus en fonction du comportement par défaut existant. Avec isNonLoggedIn=true, il renvoie généralement le menu unique utilisé par l’expérience hors connexion pour votre compte (puisqu’il n’y a normalement qu’un seul menu hors connexion par compte).

En pratique, un client peut désormais émettre :

curl -X GET \
  « https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true » \
  -H « Autorisation : Porteur {admin_token} » \
  -H « Accepter : application/vnd.api+json »


et récupérez la structure de navigation hors connexion en un seul appel, avec toutes les pages qui devraient être visibles par les visiteurs anonymes.

Cela est particulièrement utile lorsque vous créez un site sans en-tête non connecté et que vous souhaitez refléter la même navigation qu’Experience Builder utilise, ou lorsque vous déboguez si le menu hors connexion a été configuré correctement.

## Autoriser la liste de domaines personnalisés

La pile non connectée se compose des éléments suivants :

- Domaine CDN public (par exemple cpcontents.adobe.com ou yourdomain.example.com) qui sert les mises en page, la configuration JSON et les actifs statiques.
- Point de terminaison d&#39;Elasticsearch public (ES) qui fournit des données de catalogue et de recherche, mais uniquement si la demande provient d&#39;un **domaine autorisé** pour ce compte ALM.

Lorsque vous introduisez un domaine personnalisé, il fonctionne de manière transparente sans effort supplémentaire suivant le processus existant pour ajouter un domaine personnalisé.

### Conditions préalables

Avant de mettre un domaine personnalisé en liste blanche pour les utilisateurs non connectés :

1. Le domaine personnalisé est configuré pour votre compte ALM (par exemple, DNS pour academy.yourcompany.com pointe vers Adobe / Akamai et des certificats sont fournis).
2. Le connecteur **Training Data Access (TDA)** est activé pour le compte.
3. La fonctionnalité **Experience Builder** non connecté est activée (côté Adobe).

Ces étapes garantissent que :

- Votre compte a un **compte JSON** non connecté (souvent référencé sous le nom de accountConfig / experienceBuilderConfig), qui inclut des champs tels que cpDomain, almDomain, almCdnBaseUrl, esBaseUrl et des domaines inscrits dans la liste autorisée.
- La pile non connectée sait où servir les données et à partir de quels domaines elle doit accepter les demandes.

### Fonctionnement de la liste autorisée

La liste autorisée est stockée dans la configuration exportée par TDA et lue par la pile non connectée. Cette configuration comprend :

- Domaines ALM (cpDomain, almDomain).
- **URL de base CDN** pour le contenu non connecté (almCdnBaseUrl).
- **URL de base de recherche publique** (esBaseUrl).
- Liste des domaines autorisés à effectuer des appels publics non connectés pour ce compte.

Pour qu’Experience Builder non connecté fonctionne sur un domaine personnalisé :

- Le navigateur doit charger le HTML non connecté à partir de ce domaine personnalisé (ou du domaine CDN ALM non connecté, selon votre configuration).
- Les appels de ce domaine vers les points de terminaison ES et CDN publics doivent être acceptés. Cela se produit uniquement si le domaine est présent dans la liste autorisée.

Cette version ajoute un nouveau domaine CDN non connecté, cpcontents.adobe.com, et spécifie qu&#39;il doit être placé dans les **domaines autorisés** dans le connecteur TDA. Pour les utilisateurs natifs existants non connectés, une mise à jour est nécessaire.

### Autoriser la liste d’un domaine personnalisé

**Configuration du domaine personnalisé dans ALM**

Travaillez avec Adobe pour enregistrer votre domaine, par exemple academy.yourcompany.com, en tant que domaine personnalisé pour votre compte ALM. Vous mettez à jour DNS pour pointer vers l&#39;Adobe Akamai comme indiqué et attendez que le protocole SSL et le routage se terminent.

À ce stade, le trafic connecté et non connecté peut atteindre ALM via ce domaine, mais les appels de recherche et de catalogue non connectés peuvent toujours être bloqués si le domaine n’est pas autorisé.

**Activer TDA et Experience Builder hors connexion**

Assurez-vous que :

- Le **connecteur Training Data Access** est activé.
- La fonctionnalité **Experience Builder** non connecté est activée pour le compte.

L’activation de TDA crée ou met à jour le compte non connecté JSON. Pour les nouveaux comptes, le processus autorise également le nouveau domaine CDN non connecté (cpcontent.adobe.com) par défaut, de sorte que le point de terminaison ES public attend des appels de ce domaine.

Pour les comptes qui utilisaient déjà l’ancienne pile non connectée, la spécification M45 indique que les connecteurs existants doivent être supprimés et recréés pour prendre en charge le nouveau domaine.

**Ajouter le domaine personnalisé à la liste autorisée**

La partie critique indique à la pile ES non connectée que academy.yourcompany.com est une origine approuvée. Il existe deux chemins communs.

1. **Réactivez le connecteur TDA (simple, en libre-service)**

Le wiki Experience Builder M45 explique que les utilisateurs natifs non connectés existants devront supprimer et réactiver la connexion TDA afin que le nouveau domaine soit automatiquement autorisé. Cela permet d’atteindre deux objectifs :
1. Le compte JSON non connecté est régénéré.
2. Les domaines autorisés répertoriés sont mis à jour pour inclure le nouveau domaine CDN non connecté et votre domaine personnalisé.

Cette option est recommandée lorsque vous disposez d&#39;un petit nombre de comptes et que vous tolérez la désactivation et la réactivation temporaires du connecteur.

1. **Vérifiez que le domaine est bien autorisé**

Après la liste autorisée, ouvrez votre site non connecté sur le domaine personnalisé et inspectez les appels réseau du navigateur.

Vous voulez voir :

- Demandes à almCdnBaseUrl (par exemple [https://cpcontent.adobe.com/](https://cpcontent.adobe.com/)...) avec 200/304.
- Demandes à esBaseUrl (API de recherche publique, par exemple [https://primeapps.adobe.com/almsearch/api/v1/](https://primeapps.adobe.com/almsearch/api/v1/)...) opération réussie, retour de JSON avec les données de recherche/catalogue.

Si ces appels retournent 4xx ou des erreurs explicites suggérant « domaine non approuvé » ou « origine non autorisée », la liste autorisée est incomplète ou mal configurée et le support doit l’ajuster.

Le LLD hors connexion note également que la configuration du compte peut contenir une valeur de domaine attendue. Lors de l’exécution, le site vérifie que le domaine dans l’URL correspond à ce qui est défini dans la configuration. Si ce n’est pas le cas, l’utilisateur peut être redirigé vers une page d’erreur. Cela vous protège contre l’accès à la configuration d’un client via le domaine d’un autre client.

## Utilisation des recommandations dans Experience Builder non connecté

L’Experience Builder non connecté vous permet de créer des pages d’apprentissage publiques où les visiteurs peuvent parcourir votre catalogue et voir le contenu mis en évidence avant de se connecter. Même si ces visiteurs sont anonymes, vous pouvez toujours présenter des formations recommandées en utilisant des métadonnées et des widgets.

Dans l’application de l’élève connecté, les recommandations peuvent être personnalisées : elles peuvent dépendre du profil, de l’historique, des compétences et de la progression de l’élève. Dans l&#39;expérience **hors connexion**, il n&#39;y a pas encore d&#39;identité d&#39;élève, la plateforme ne peut donc pas personnaliser par utilisateur.

Par conséquent, Recommendations en mode hors connexion est :

- **Sélectionné ou basé sur des règles** : basé sur le catalogue, le produit, le rôle, les libellés, les balises et d&#39;autres métadonnées.
- **Orienté segment** : « recommandé pour les développeurs », « recommandé pour les partenaires », « recommandé pour les débutants ».
- **Axé sur le marketing** : utilisé pour attirer et guider les visiteurs pour qu&#39;ils s&#39;inscrivent une fois qu&#39;ils se connectent.

### Métadonnées et API prenant en charge les recommandations

En coulisse, les pages non connectées utilisent :

- Le **connecteur TDA** pour exporter les métadonnées des objets d&#39;apprentissage (cours, parcours, certifications, assistances à la tâche) vers un index de recherche public.
- La **pile de recherche publique** pour répondre aux requêtes des widgets non connectés (catalogue, recherche, cours et parcours, catégories).
- L&#39;**API Admin Learning Objects** pour exposer les métadonnées de produit et de rôle qui peuvent être utilisées pour les règles de recommandation.

Dans cette version, l’API Admin LO a été étendue afin que les associations de produits et de rôles soient disponibles de manière fiable :

GET /primeapi/v2/learningObjects/{loId}?forcedFields[learningObject]=products,roles

Cela permet aux widgets et aux intégrations sans en-tête de créer des recommandations basées sur des règles à l’aide de produits, de rôles, d’étiquettes de catalogue, de balises et d’autres champs de manière cohérente.

### Conception de sections de recommandation avec les widgets Experience Builder

Vous créez des sections de recommandation sur des pages non connectées en combinant des **widgets Experience Builder** avec des filtres de métadonnées.

#### Widget **Cours et parcours**

Utilisez le widget **Cours et parcours** pour afficher une ligne ou une grille d&#39;éléments recommandés. Dans sa configuration, vous pouvez choisir :

- À partir de quels catalogues extraire.
- Étiquettes, produits, rôles ou balises de catalogue à utiliser comme filtres.
- Indique s’il faut afficher des cours, des parcours, des certifications, des assistances à la tâche ou un mixage.
- Tri et nombre maximal d’éléments.

Par exemple, vous pouvez créer :

- « Recommandé pour les développeurs » : filtrez en fonction d’un produit ou d’un rôle que vous utilisez pour le contenu développeur.
- « Commencer ici » : filtrez par un libellé tel que « Démarrer » ou « Intégration ».
- « En vedette ce trimestre » : filtrez par un libellé limité dans le temps comme en vedette-t3-2026.

Le widget n’apprend pas à tirer des leçons du comportement ; il affiche tout ce qui correspond aux règles de métadonnées que vous définissez. Du point de vue du visiteur, cependant, cela ressemble à une bande de recommandation.

#### Widget **Catégories**

Utilisez le widget **Catégories** pour aider les visiteurs à naviguer dans les ensembles de contenu « recommandés », même s&#39;ils ne connaissent pas les noms de vos produits.

Vous pouvez configurer des vignettes qui représentent chacune un segment, par exemple :

- « Pour les administrateurs »
- « Pour les équipes commerciales »
- « Pour les partenaires »
- « Par gamme de produits »

Chaque vignette peut être liée à :

- Une page de catalogue filtrée (par exemple, le catalogue filtré par certains produits ou étiquettes).
- Une page dédiée non connectée qui utilise des cours et des chemins préconfigurés pour ce segment.

Cela vous offre une expérience « chemins recommandés par segment » sans personnalisation.

### Élaboration de recommandations par segment

Étant donné que les visiteurs non connectés n&#39;ont pas encore de profil ALM, il est utile de concevoir des recommandations **par segment** et de laisser les visiteurs choisir eux-mêmes.

1. Utilisez une **page d&#39;accueil non connectée** qui explique brièvement à qui votre académie est destinée et affiche un petit nombre de points d&#39;entrée de segment (par exemple, « Développeurs », « Marketing », « Partenaires », « Nouveaux employés »). Pour ce faire, utilisez un widget Catégories ou une simple zone de contenu ou une section de HTML avec des boutons.
2. Pour chaque segment, créez une **page non connectée dédiée** dans Experience Builder. Sur cette page, utilisez un ou plusieurs widgets Cours et parcours configurés avec des filtres qui représentent ce qui est « recommandé » pour ce groupe. Par exemple, pour « Développeurs », vous pouvez filtrer sur :
   1. Catalogue = « Formation publique »
   2. Produit = « Adobe Experience Manager »
   3. Balises = « Principes de base du développeur »
3. Utilisez ces pages de segment comme destination de vos campagnes marketing et comme cible des vignettes de la page d’accueil non connectée.

Les visiteurs perçoivent qu&#39;ils voient des recommandations adaptées à leur situation, même si la logique est définie au moment de la conception via des métadonnées.

### Transition des utilisateurs non connectés aux recommandations personnalisées

Les recommandations hors connexion concernent principalement la **découvrabilité** et la **conversion**. Une fois que les visiteurs décident de s’inscrire ou de commencer une formation, ils se connectent et deviennent des élèves à part entière avec un profil et un historique.

Le flux habituel est :

1. Un visiteur découvre du contenu via vos sections de recommandation non connectées (recommandations d’accueil, pages de destination des segments, lignes en vedette).
2. Ils cliquent sur une vue d’ensemble de cours ou de parcours et choisissent de s’inscrire ou de commencer.
3. ALM les invite à s’inscrire ou à se connecter.
4. Une fois qu’ils se sont connectés, l’expérience d’élève standard connectée prend le relais, notamment :
   1. « Mon apprentissage »
   2. Catalogue connecté avec progression personnelle
   3. Tous les systèmes de recommandation internes que vous utilisez pour les élèves existants.

En d’autres termes, les recommandations connectées les aident à décider de ce qu’il faut faire ensuite et à continuer.

## Comment les assistances à la tâche peuvent être utilisées dans le nouvel Experience Builder non connecté

Sur l&#39;**interface utilisateur**, les assistances à la tâche participent à des expériences non connectées, principalement via les widgets qui peuvent afficher des objets d&#39;apprentissage :

1. **Widget Cours et parcours**\
   Ce widget peut afficher plusieurs types d’objet d’apprentissage, y compris des assistances à la tâche. Dans les pages non connectées, vous pouvez le configurer pour :
   1. Inclure ou exclure explicitement les assistances à la tâche.
   2. Filtrez les assistances à la tâche par catalogue, produit, rôle, étiquettes, balises et autres métadonnées.
   3. Présentez-les en même temps que des cours et des parcours ou sous la forme d’une bande « Ressources » distincte.

Par exemple, sur une page de destination publique, vous pouvez configurer une bande intitulée « Ressources utiles » qui affiche uniquement les assistances à la tâche, et une autre bande intitulée « Cours recommandés » qui affiche les cours et les parcours.

1. **Page de catalogue et recherche**\
   Les surfaces **catalogue** et **recherche** non connectées utilisent l&#39;index de recherche publique (alimenté par le connecteur Training Data Access). Cet index prend désormais correctement en charge les assistances à la tâche.
   1. Les résultats de recherche hors connexion peuvent inclure des assistances à la tâche.
   2. Filtres de catalogue non connectés (par type, produit, balises, etc.) peut inclure des assistances à la tâche tant que la configuration de votre compte et les widgets sont configurés pour les afficher.
2. **Pages de présentation LO**\
   Lorsqu&#39;un visiteur clique sur une assistance à la tâche à partir d&#39;un widget ou du catalogue, il accède à une **page de présentation LO** pour cette assistance à la tâche en mode non connecté. De là, ils peuvent lire sa description et ses métadonnées. Le téléchargement ou la consommation réels nécessitent généralement toujours une connexion, mais la présence et la découvrabilité de l&#39;assistance à la tâche elle-même sont gérées par l&#39;expérience hors connexion.

### Affichage des assistances à la tâche via des API non connectées

Du côté **API**, les assistances à la tâche sont prises en charge par :

1. **Connecteur Training Data Access et recherche publique**\
   TDA exporte les métadonnées des assistances à la tâche ainsi que d’autres types d’objet d’apprentissage vers l’index de recherche public qui sert aux requêtes de recherche et de catalogue non connectées. C’est ce sur quoi reposent Experience Builder et les systèmes frontaux sans tête.
2. La liste **Objets d’apprentissage avec effectiveModifiedDate**\
   Dans cette version, le point de terminaison de liste LO a été corrigé afin que les assistances à la tâche fonctionnent correctement avec le filtre effectiveModifiedDate. Vous pouvez désormais appeler :

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Avant cette modification, la combinaison effectiveModifiedDate avec loTypes=jobAid ne renvoyait pas d&#39;assistances à la tâche de manière fiable. C&#39;est désormais le cas, comme documenté dans le wiki *Modifications de l&#39;API publique M45*. Cela signifie :

1. Vos tâches TDA ou ETL peuvent **synchroniser de manière incrémentielle les assistances à la tâche** pour les expériences non connectées, de la même manière qu’ils le font pour les cours et les parcours.
2. Toute implémentation sans en-tête qui crée un répertoire d&#39;assistance à la tâche public peut interroger les modifications en fonction de effectiveModifiedDate et loType=jobAid.

L’exemple de réponse dans le document M45 montre un learningObject avec loType : « jobAid » et loFormat : « Content » retourné lors de l’utilisation de ce modèle.

1. **API Admin LO**\
   Bien qu’il ne soit pas spécifique aux objets non connectés, M45 met également à jour l’API d’objet d’apprentissage d’administrateur pour afficher de manière cohérente les métadonnées de produit et de rôle pour tous les types d’objet d’apprentissage via :

GET /primeapi/v2/learningObjects/{loId}?forcedFields[learningObject]=products,roles


Pour les assistances à la tâche, cela signifie que vous pouvez gérer leurs produits, rôles, étiquettes et balises de manière centralisée et vous appuyer sur ces métadonnées dans des expériences publiques non connectées, par exemple dans les sections « Ressources pour les marketeurs » ou les pages d’accueil spécifiques aux produits.

**Remarque** :

Dans l’état non connecté :

- Les assistances à la tâche sont principalement **détectables** : les visiteurs peuvent voir qu&#39;elles existent, lire les descriptions et comprendre comment elles prennent en charge les sujets ou les cours.
- La **consommation** réelle (téléchargement ou ouverture du contenu de l&#39;assistance à la tâche) nécessite généralement toujours la connexion, en particulier si les assistances à la tâche sont considérées comme faisant partie du contenu sous licence ou interne.

## Modifications apportées à la « brève description » dans la recherche LO (non connecté)

Dans la pile non connectée, la recherche et la liste des objets d’apprentissage sont optimisées par le connecteur TDA (Training Data Access) et un index d’Elasticsearch publics. Historiquement, cette pile utilisait un seul champ de présentation/description pour chaque objet d’apprentissage. Les clients qui créent des portails sans en-tête non connectés voulaient afficher la même brève description sur les vignettes d’objet d’apprentissage que celle de l’interface utilisateur des élèves connectés, plutôt que la seule vue d’ensemble longue.

La modification introduit la prise en charge de l&#39;objet d&#39;apprentissage **brève description** dans les API de recherche et de liste non connectées :

- Pour **cours**, la sémantique de l’interface utilisateur existante est la suivante :
   - Les cartes connectées affichent « Brève description » (champ de 140 caractères) si elles sont présentes ; sinon, elles se limitent à la longue « Vue d’ensemble détaillée ».
- Pour les **parcours d’apprentissage**, l’interface utilisateur connectée utilise le champ « Avantages » comme brève description, si elle est définie, et revient à la vue d’ensemble dans les autres cas.
- Pour les **certifications**, une brève « Description » est utilisée, avec une « Présentation de la certification » plus longue comme solution de secours.
- Pour les **assistances à la tâche**, le champ de description principal est utilisé.

## Autres modifications

### Restriction selon laquelle deux comptes ne peuvent pas partager le même domaine personnalisé

Dans les architectures non connectées et connectées de Adobe Learning Manager, un **domaine personnalisé** (par exemple, academy.example.com) est traité comme une clé unique au niveau mondial qui doit être mappée à exactement un compte ALM. La plateforme applique donc une restriction stricte selon laquelle **aucun compte ne peut partager le même domaine personnalisé**. Ceci est requis pour la sécurité, le routage et le référencement : la couche de routage et la pile non connectée utilisent le domaine pour rechercher la configuration de compte correcte (y compris son compte non connecté JSON, les menus Experience Builder, le branding et les points d’entrée TDA/search),

Autoriser le même domaine personnalisé sur deux comptes rendrait impossible de garantir les données du compte retournées, pourrait provoquer des fuites entre locataires et corromprait également les artefacts générés tels que sitemap.xml et robots.txt qui sont produits par compte mais découverts par les moteurs de recherche par hôte. Sur le plan opérationnel, cela signifie que lorsque vous attribuez ou déplacez un domaine personnalisé, vous devez d&#39;abord vous assurer qu&#39;il n&#39;est pas associé à un autre compte (ou l&#39;y radier), et l&#39;outillage interne d&#39;Adobe rejettera les tentatives de liaison du même domaine à plusieurs comptes.

### Mise en cache des ressources du navigateur dans l’expérience hors connexion

Dans l’expérience hors connexion de Adobe Learning Manager, la mise en cache des ressources dans le navigateur est un élément essentiel de la stratégie de performances et d’évolutivité, car les pages publiques doivent gérer un trafic marketing important et parfois chargé avec une faible latence et une charge d’origine minimale. Les actifs statiques et semi-statiques tels que le shell de HTML non connecté (par exemple, index.html/guest.html), la configuration au niveau du compte JSON (account.json ou config.json), la mise en page JSON Experience Builder (menus, mises en page de widgets, paramètres de carte), CSS, JS, les images et les favicons sont servis à partir d’un CDN Akamai (cpcontents.adobe.com / cpcontent.adobe.com) avec des en-têtes de cache qui encouragent la réutilisation côté CDN et côté navigateur, de sorte qu’après le chargement de la première page, le navigateur peut effectuer le rendu des pages non connectées suivantes en grande partie à partir de son cache, en les revalidant uniquement lorsque nécessaire via ETag ou Last-Modified.

## Lancer les options de la page d’accueil

Sur la page d&#39;accueil de Adobe Learning Manager, sélectionnez **Identité visuelle**. Ensuite, dans le volet de gauche, sélectionnez Page d’accueil non connectée.

![options de page d’accueil](/help/migrated/administrators/feature-summary/assets/non-logged-in-homepage.png)

*Sélectionnez l&#39;option Page d&#39;accueil non connectée*

## Ajouter une bannière

Ajoutez une bannière pour n’importe quelle annonce marketing ou présentez le sujet tendance du jour. Sélectionnez **Ajouter une bannière**.

![bannière](/help/migrated/administrators/feature-summary/assets/add-banner-image.png)

*Ajouter une bannière*

Accédez à l’emplacement de l’image à utiliser comme bannière. Fournissez ensuite un lien sous forme de bouton d’action sur l’image de bannière.

## Ajouter des catégories

Ce composant peut être utilisé pour filtrer le catalogue par balises, compétences et catalogue. Cette section contient un en-tête et une description pour chaque catégorie. Après avoir cliqué, l’utilisateur est redirigé vers la page du catalogue avec les filtres appliqués.

Sélectionnez **[!UICONTROL Ajouter une catégorie]**. Saisissez ensuite les détails de la catégorie.

![ajouter une catégorie](/help/migrated/administrators/feature-summary/assets//add-category.png)

*Ajouter les catégories*

Enregistrez la catégorie. La catégorie est ajoutée à la section.

## Ajouter un catalogue

Ajoutez un catalogue pour les utilisateurs non connectés afin qu’ils puissent parcourir toutes les formations sur la plateforme.

![ajouter un catalogue](/help/migrated/administrators/feature-summary/assets//add-catalog.png)

*Ajouter un catalogue*

Toutes les formations exportées seront présentes.
