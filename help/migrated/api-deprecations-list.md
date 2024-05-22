---
jcr-language: en_us
title: Dépréciations d’API dans Adobe Learning Manager
description: À mesure que les API dans Adobe Learning Manager évoluent, elles sont régulièrement réorganisées ou mises à niveau. Lorsque les API évoluent, l’ancienne API est obsolète et finalement supprimée. Cette page contient les informations que vous devez connaître lors de la migration de versions d’API obsolètes vers des versions d’API plus récentes et plus stables.
contentowner: saghosh
exl-id: 0fe9a3cb-9114-42d6-81ae-1a4f28c984fa
source-git-commit: 670d0477b246af2a0257e41eca799817e391b348
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 32%

---

# Dépréciations et modifications d’API dans Adobe Learning Manager

## Dépréciations d’API dans la version de mars 2024 de Adobe Learning Manager

<!-- ### Changes in Rate Limits

With the next release of Adobe Learning Manager, we're restructuring API rate limits for new accounts. For existing accounts, only the Admin APIs will be rate-limited. After 90 days (about 3 months), we will restructure rate limits for all APIs, but existing accounts will be whitelisted according to current usage. Existing accounts need to revisit their learner API usage. 

For new accounts, if they want to increase the rate limits, they must contact the Customer Success team of ALM. 

#### Which APIs will be rate limited 

For new accounts, all Admin, Learner, and Search APIs will have rate limits and burst enforced.  

The API burst rate or burst limit refers to the maximum number of requests allowed to be made to an API in a short burst within a limited timeframe. 

The following table lists the rate and burst limits for the APIs.

<table>
    <tr>
        <th>API</th>
        <th>Number of requests-RPM</th>
        <th>Number of requests-Burst</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Learner</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>
-->

### Modification des limites de décalage

En raison du nombre élevé d’enregistrements récupérés par la valeur de décalage et du ralentissement des performances globales, nous appliquons une limite de **500** enregistrements. Dans la prochaine version, pour l’administrateur et l’élève, le **Utilisateurs GET** L’API renvoie un maximum de **500** enregistrements.

Si vous avez besoin d’autres enregistrements à récupérer, utilisez la commande **Offres d’emploi GET** API.

<!--### Exclude paths 

At present, Learning Manager APIs follow a graph data structure, which allows you to fetch data by traversing the API model through includes. Even though you could traverse an API up to seven levels, fetching the data using a single API call is computationally expensive. 

We recommend that all existing and new customers make small calls multiple times instead of one large call. This approach will prevent unwanted data from being loaded in the call. 

We want to enforce these restrictions on new accounts and maintain a whitelist of existing accounts.-->

#### Quels chemins sont obsolètes ?

Les chemins suivants sont obsolètes :

* /learningObjects
   * Chemins d’accès obsolètes :
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Nouveaux tracés :
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Chemin d’accès obsolète :
      * enrollment.instances.subLoInstances.learningObject
   * Nouveau chemin :
      * enrollment.instances.subLoInstances

* /enrollments
   * Chemin d’accès obsolète :
      * loInstance.learningObject.enrollment
   * Nouveau chemin :
      * loInstance.learningObject

* /learningObjects/{id}
   * Chemin d’accès obsolète :
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nouveau chemin :
      * instance.subLoInstances

<!--### Instance summary count changes 

Currently, in the LO summary endpoint, you fetch the number of all possible instances. For example, for a course, you can view the number of enrollments and waitlists in the response for **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. You can then view the completionCount and enrollmentCount in the response. If the course is a VC or classroom, you can also view its seat limit and waitlist limit. 

The process of retrieving the completion and enrollment counts is computationally expensive, therefore the calculation is done on a request basis. If the data is not present in the cache, the data is reloaded, which is computationally intensive. If there are many users enrolling in a course, the counts will be large, and effectively impacts CPU performance. 

In the next release of Adobe Learning Manager, in the LO Instance summary endpoint, the completionCount, enrollmentCount, seatLimit, and waitlistCount are cached. The cached information persists till there are changes in enrollments or unenrollments. For counts exceeding 1000 enrollments, we'll assume the estimated counts, and invalidate the results for all existing and new accounts.

>[!NOTE]
>
>For counts, such as, completionCount, enrollmentCount, seatLimit, and waitlistCount exceeding1000, it's advisable to interpret them as estimates rather than precise figures, as these will be retrieved from cache.-->

### Trier par nom

Dans la prochaine version de Adobe Learning Manager, name et -name sont obsolètes dans le champ de tri des API suivantes :

* GET /userGroups/{userGroupId}/users
* GET /users

>[!NOTE]
>
>Pour tous les comptes existants et nouveaux, le tri par nom et par -nom sera déconseillé.


## Dépréciations d’API dans la version de novembre 2023 de Adobe Learning Manager

### Indicateur de remplacement

Dans la version de novembre 2023 de Adobe Learning Manager, nous avons supprimé l’indicateur de remplacement des API. L’indicateur de remplacement ne fait pas partie de la spécification d’API publique et est destiné aux tests backend. L’indicateur n’est plus disponible pour les API des élèves. Cependant, l’indicateur reste valide pour les API d’administrateur.

La raison pour laquelle nous déprécions l&#39;indicateur pour les API des élèves est que l&#39;indicateur de remplacement récupérait une grande quantité de données via les API des élèves.

À l’avenir, l’API des élèves suivante cessera de fonctionner car elle comporte l’indicateur de remplacement.

_/primeapi/v2/users?page[décalage]=0&amp;page[limite]=10&amp;sort=id&amp;override=TRUE_

### Modifications d’API pour les nouvelles recommandations basées sur les compétences

Adobe Learning Manager améliore les recommandations pour les comptes clients et partenaires. Grâce à l’amélioration de l’algorithme de recommandation due à la modification de l’algorithme de classement des cours, des parcours d’apprentissage et des certifications, les utilisateurs bénéficient d’une expérience optimisée en termes de découverte de contenu.

L’algorithme n’autorise plus les recommandations basées sur les pairs. La modification n’affecte pas les utilisateurs existants. Toutefois, l’option Correspondant au secteur continue d’exister. Pour l’option Personnalisé, Adobe Learning Manager n’autorise plus la sélection personnalisée basée sur les pairs.

Le groupe de pairs devient désormais un compte. Les élèves verront une chaîne présentant les sujets tendance dans le groupe. Toutes les recommandations sont explicables. Par exemple, si vous consultez un contenu sur un certain type de sujet, la carte sur la bande affiche la raison de la suggestion du cours.

### Modifications Apportées Au Rapport D&#39;Annonce Des Notifications

Dans les versions antérieures de Adobe Learning Manager, le rapport Annonce de notification ne comportait aucun filtre. Adobe Learning Manager téléchargeait l’ensemble des notifications du compte.

Dans la version de novembre 2023, nous avons ajouté un filtre de date, à l’aide duquel vous pouvez télécharger les notifications au cours d’une période spécifiée.  Cependant, vous ne pouvez télécharger que le rapport des six derniers mois.

### Dépréciation des valeurs de décalage élevées dans le point de terminaison GET /users

Pour améliorer les performances du système et gérer plus efficacement l’utilisation des ressources, Adobe a déprécié les valeurs de décalage élevées dans le point d’entrée GET /users pour les deux **ADMINISTRATEUR** et **ÉLÈVE** étendues. Nous vous recommandons d’utiliser la **API des tâches** pour extraire les enregistrements avec une valeur de décalage.

