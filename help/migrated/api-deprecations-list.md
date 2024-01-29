---
jcr-language: en_us
title: Dépréciations d’API dans Adobe Learning Manager
description: À mesure que les API dans Adobe Learning Manager évoluent, elles sont régulièrement réorganisées ou mises à niveau. Lorsque les API évoluent, l’ancienne API est obsolète et finalement supprimée. Cette page contient les informations que vous devez connaître lors de la migration de versions d’API obsolètes vers des versions d’API plus récentes et plus stables.
contentowner: saghosh
source-git-commit: 83fdd06aed823a50458d50c8ac240d56af873a6d
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---


# Dépréciations d’API dans Adobe Learning Manager

## Dépréciations d’API dans la version de mars 2024 d’Adobe Learning Manager

### Modification des limites de taux

Avec la prochaine version d’Adobe Learning Manager, nous restructurons les limites de taux des API pour les nouveaux comptes. Pour les comptes existants, seules les API d’administration seront limitées par le taux. Après 90 jours (environ 3 mois), nous restructurerons les limites de taux pour toutes les API, mais les comptes existants seront autorisés en fonction de l’utilisation actuelle. Les comptes existants doivent revoir l’utilisation de leur API d’élève.

Pour les nouveaux comptes, s’ils souhaitent augmenter les limites de taux, ils doivent contacter l’équipe de réussite client d’ALM.

#### Quelles API seront limitées par des tarifs ?

Pour les nouveaux comptes, toutes les API d’administration, d’élève et de recherche auront des limites de taux et des bustes appliqués.

Le taux de rafale de l’API ou la limite de rafale fait référence au nombre maximal de demandes pouvant être adressées à une API en rafale courte sur une période limitée.

Le tableau suivant répertorie les limites de taux et de rafale pour les API.

<table>
    <tr>
        <th>API</th>
        <th>Nombre de demandes-RPM</th>
        <th>Nombre de demandes-Rafale</th>
    </tr>
    <tr>
        <td>Administrateur</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Élève</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>

### Modification des limites de décalage

En raison du nombre élevé d’enregistrements récupérés par la valeur de décalage et du ralentissement des performances globales, nous appliquons une limite de **500** enregistrements. Dans la prochaine version, pour l’administrateur et l’élève, le **Utilisateurs GET** L’API renvoie un maximum de **500** enregistrements.

Si vous avez besoin d’autres enregistrements à récupérer, utilisez la commande **Offres d’emploi GET** API.

La modification des limites de compensation s&#39;applique à tous les nouveaux clients. Pour les clients existants, la règle des 90 jours s’applique.

### Exclure des tracés

Actuellement, les API Learning Manager suivent une structure de données de graphique, qui vous permet de récupérer des données en parcourant le modèle d’API par le biais d’inclusions. Même si vous pouvez parcourir une API jusqu’à sept niveaux, la récupération des données à l’aide d’un seul appel API est coûteuse en termes de calcul.

Nous recommandons à tous les clients existants et nouveaux de passer de petits appels plusieurs fois au lieu d&#39;un seul appel important. Cette approche empêchera le chargement de données indésirables dans l&#39;appel.

Nous voulons appliquer ces restrictions aux nouveaux comptes et maintenir une liste blanche des comptes existants.

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

### Modifications du nombre de résumés d&#39;instances

Actuellement, dans le point de terminaison résumé de l’objet d’apprentissage, vous récupérez le nombre de toutes les instances possibles. Par exemple, pour un cours, vous pouvez afficher le nombre d&#39;inscriptions et de listes d&#39;attente dans la réponse pour **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. Vous pouvez ensuite afficher completionCount et enrollmentCount dans la réponse. Si le cours est une classe virtuelle ou une salle de classe, vous pouvez également afficher sa limite de places et sa limite de liste d’attente.

Le processus d&#39;extraction du nombre d&#39;achèvements et d&#39;inscriptions est coûteux sur le plan informatique. Par conséquent, le calcul est effectué sur demande. Si les données ne sont pas présentes dans la mémoire cache, elles sont rechargées, ce qui représente une charge de calcul importante. Si de nombreux utilisateurs s&#39;inscrivent à un cours, le nombre sera important et aura un impact réel sur les performances du processeur.

Dans la prochaine version d’Adobe Learning Manager, dans le point de terminaison résumé de l’instance d’objet d’apprentissage, completionCount, enrollmentCount, seatLimit et waitlistCount sont mis en cache. Les informations mises en cache sont conservées jusqu&#39;à ce que des modifications soient apportées aux inscriptions ou aux désinscriptions. Pour les nombres supérieurs à 1 000 inscriptions, nous supposerons les nombres estimés et invaliderons les résultats pour tous les comptes existants et nouveaux.

>[!NOTE]
>
>Pour les nombres, tels que completionCount, enrollmentCount, seatLimit et waitlistCount supérieurs à 1 000, il est conseillé de les interpréter comme des estimations plutôt que comme des chiffres précis, car ils seront récupérés à partir du cache.

### Trier par nom

Dans la prochaine version d’Adobe Learning Manager, name et -name sont obsolètes dans le champ de tri des API suivantes :

* GET /userGroups/{userGroupId}/users
* GET /users

>[!NOTE]
>
>Pour tous les comptes existants et nouveaux, le tri par nom et par -nom sera déconseillé.


## Dépréciations d’API dans la version de novembre 2023 d’Adobe Learning Manager

### Indicateur de remplacement

Dans la version de novembre 2023 d’Adobe Learning Manager, nous avons supprimé l’indicateur de remplacement des API. L’indicateur de remplacement ne fait pas partie de la spécification d’API publique et est destiné aux tests principaux. L’indicateur n’est plus disponible pour les API des élèves. Cependant, l’indicateur est toujours valide pour les API d’administration.

La raison pour laquelle nous déprécions l&#39;indicateur pour les API des élèves est que l&#39;indicateur de remplacement récupérait une grande quantité de données via les API des élèves.

À l’avenir, l’API de l’élève suivante cessera de fonctionner car elle comporte l’indicateur de remplacement.

<code>https://captivateprime.adobe.com/primeapi/v2/users?page[décalage]=0&amp;page[limite]=10&amp;sort=id&amp;override=TRUE</code>

### Modifications d’API pour les nouvelles recommandations basées sur les compétences

Adobe Learning Manager améliore les recommandations pour les comptes clients et partenaires. Cette amélioration de l’algorithme de recommandation avec le changement de l’algorithme de classement pour le cours, le parcours d’apprentissage et la certification offre une meilleure expérience utilisateur en matière de découverte de contenu.

L’algorithme n’autorisera plus les recommandations basées sur les pairs. La modification n’affectera pas les utilisateurs existants, mais l’option Correspondant au secteur continuera d’exister. Pour l’option Personnalisé, Adobe Learning Manager n’autorisera plus la sélection personnalisée par les pairs.

Le groupe de pairs devient désormais un compte, et les élèves verront une chaîne qui montre les sujets tendance dans le groupe. Toutes les recommandations sont explicables. Par exemple, si vous visualisez quelque chose sur un sujet, la carte sur la bande affichera la raison du cours.

### Modifications Apportées Au Rapport D&#39;Annonce Des Notifications

Dans les versions antérieures d’Adobe Learning Manager, le rapport Annonce de notification ne disposait d’aucun filtre. Adobe Learning Manager a téléchargé toutes les notifications du compte.

Dans la version de novembre 2023, nous avons ajouté un filtre de date, à l’aide duquel vous pouvez télécharger les notifications au cours d’une période spécifiée.  Cependant, vous ne pouvez télécharger que le rapport des six derniers mois.