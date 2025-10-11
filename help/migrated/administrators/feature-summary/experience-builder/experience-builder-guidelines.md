---
title: Directives et limitations d’Experience Builder dans Adobe Learning Manager
description: Les directives et limitations d’Experience Builder fournissent des suggestions de cours et de contenu personnalisées aux élèves à l’aide d’algorithmes pilotés par l’IA.
jcr-language: en-us
source-git-commit: b3124c47d56a50437cb284fe809828bcd4c4008d
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Directives et limitations d’Experience Builder

Experience Builder est un outil puissant conçu pour aider les utilisateurs à créer facilement des pages web dynamiques et attrayantes. Pour garantir des performances, une convivialité et une sécurité optimales, il est essentiel de suivre certaines directives et recommandations lors de la configuration des pages, de l’utilisation de widgets et de la personnalisation des mises en page. Ce document fournit un aperçu détaillé des remarques et points importants que les utilisateurs doivent prendre en compte lorsqu’ils travaillent avec Experience Builder.

Les informations présentées ici couvrent des aspects clés tels que les configurations de page et de widget, les options de personnalisation, la gestion du code personnalisé et des considérations de sécurité. En respectant ces recommandations, les utilisateurs peuvent maximiser l’efficacité de leurs projets Experience Builder, éviter les pièges courants et s’adapter facilement aux mises à jour et aux changements.

## Configuration des pages et des widgets

### Nombre maximum de pages

Vous pouvez créer jusqu’à 1 000 pages dans Experience Builder. Il s’agit de la limite supérieure, mais il est recommandé de planifier les pages de manière stratégique pour éviter une complexité inutile.

### Widgets par page

* **Limite stricte** : 25 widgets maximum peuvent être ajoutés à une seule page.
* **Limite recommandée** : pour de meilleures performances, il est conseillé d&#39;utiliser au maximum 10 widgets par page.
* **Widgets basés sur l’API** : les widgets dépendants des API ALM (par exemple, Cours et parcours, Catégorie, Mon apprentissage, Apprentissage par les réseaux sociaux, Calendrier, Conformité, Tableau des scores) doivent être limités à 10 par page.
* **Widgets indépendants** : les widgets tels que HTML et Content Box, qui ne reposent pas sur les API ALM, peuvent être utilisés jusqu’à la limite stricte de 25 widgets.

### Widgets à usage unique

Certains widgets, tels que Calendrier, Apprentissage par les réseaux sociaux, Conformité et Tableau des scores, ne doivent être utilisés qu’une seule fois par page. Les utiliser plusieurs fois peut entraîner des problèmes de performances, en particulier pour les widgets comme le calendrier, qui nécessitent des ressources importantes pour charger les sessions.

### Directives de dimensionnement des widgets

Les widgets tels que Calendrier, Tableau des scores, Social et Conformité doivent être placés dans des mises en page avec une largeur minimale d’un tiers de la page. Les widgets de carte unique sont les mieux adaptés à cette largeur pour assurer un affichage optimal. Les widgets tels que Calendrier et Conformité (vue étendue) sont conçus pour des mises en page demi-largeur afin d’offrir une meilleure expérience utilisateur. Pour les autres tailles de mise en page, les widgets s’adaptent en fonction de l’espace disponible et conservent leur convivialité.

L’utilisation de widgets respectant ces recommandations de taille améliore l’interaction globale des utilisateurs.

## Directives de personnalisation

### Distances en pixels par défaut

**Distance verticale** : la distance verticale par défaut entre les widgets est de 80 pixels.
**Distance horizontale** : la distance horizontale par défaut entre les widgets est de 20 pixels.

### CSS personnalisé

Les utilisateurs peuvent remplacer les distances par défaut et d’autres propriétés visuelles à l’aide de feuilles de style CSS personnalisées.

Étapes de personnalisation :

* Inspect les éléments de page pour identifier les classes CSS.
* Appliquez les modifications au niveau global, au niveau du widget ou de la page.

Par exemple, pour réduire la distance verticale entre les widgets, modifiez la propriété CSS pour la classe concernée.

## Positionnement du menu

Les menus peuvent être placés en haut ou à gauche de la page. D’autres réglages peuvent être effectués à l’aide de feuilles de style CSS personnalisées.

## Recommandations spécifiques aux fonctionnalités

### Widgets Apprentissage par les réseaux sociaux et Ludification

* Si ces fonctionnalités sont désactivées, les administrateurs doivent supprimer manuellement les widgets correspondants des pages.
* Les pages doivent être repensées pour s’assurer qu’elles restent fonctionnelles et visuellement intactes après la désactivation de ces fonctionnalités.

## Gestion du code personnalisé

### Impact des mises à jour

* Le code personnalisé existant (HTML, CSS, JS) injecté dans le backend peut ne pas fonctionner comme prévu après les mises à jour d’Experience Builder.
* Les utilisateurs doivent réécrire leur code pour l’aligner sur les nouvelles modifications de l’interface utilisateur, telles que les noms de classe mis à jour.

### Prise en charge front-end

* Ajoutez du code personnalisé directement dans le portail d’administration à l’aide de widgets de HTML ou de blocs CSS/JS au niveau du compte.

### Clause de non-responsabilité

* Le code personnalisé peut ne pas fonctionner comme prévu dans les prochaines versions, ce qui nécessite des ajustements. Préparez-vous à mettre à jour leur code après chaque version.

## Recommandations générales

### Considérations relatives aux performances

* Évitez de dépasser les limites de widgets recommandées pour éviter une dégradation des performances.
* L’utilisation de widgets gourmands en ressources (par exemple, un calendrier) plusieurs fois sur une page peut avoir un impact significatif sur les temps de chargement des pages.

### Considérations de sécurité

* **Widgets de HTML** : vous devez vous assurer que le code gère les problèmes de sécurité tels que les attaques XSS (Cross-site scripting), car ils ne sont pas du ressort d’Experience Builder.
* **Pied de page personnalisé** : lors de la personnalisation du pied de page à l’aide de HTML ou CSS, assurez-vous que le code respecte les bonnes pratiques de sécurité.

### Modifications de dernière minute

Les mises à jour d’Experience Builder peuvent introduire des modifications de dernière minute pour les personnalisations. Vous devez :

* Ajustez le code pour correspondre aux nouveaux éléments de l’interface utilisateur.
* Test des personnalisations après chaque mise à jour.

## Remarques supplémentaires

### Implémentation CSS personnalisée

* Vous pouvez inspecter des éléments de page, copier des classes CSS et appliquer les propriétés souhaitées pour personnaliser les mises en page de manière globale, au niveau du widget ou au niveau de la page.

### ID de widget et ID de page

Chaque widget et page possède des ID uniques qui peuvent être utilisés pour des modifications CSS ciblées. Cela permet la personnalisation à différents niveaux :

* Niveau global : applique les modifications CSS à toutes les pages.
* Niveau du widget : applique les modifications CSS à des widgets spécifiques.
* Niveau de page : applique les modifications CSS à tous les widgets d’une page spécifique.










