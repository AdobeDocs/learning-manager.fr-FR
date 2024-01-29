---
description: Création et gestion de rapports pour les responsables.
jcr-language: en_us
title: Rapports
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 0%

---



# Rapports

Création et gestion de rapports pour les responsables.

Adobe Learning Manager vous permet de créer divers rapports pour suivre, surveiller et contrôler les activités des élèves. Les activités des élèves sont suivies et capturées automatiquement dans la base de données. Les rapports des responsables et des administrateurs sont générés à partir de la base de données.

## Présentation {#overview}

Le processus de génération des rapports est le même pour l’administrateur et le responsable. Les responsables peuvent afficher les rapports correspondant à leurs subordonnés, tandis que les administrateurs peuvent afficher tous les rapports de l’organisation.

Les rapports sont regroupés dans un tableau de bord. Un rapport doit exister dans un tableau de bord. A **Tableau de bord par défaut** existe par défaut dans la page rapports. Tout rapport que vous ajoutez passe dans ce tableau de bord par défaut. Pour ajouter des rapports à des tableaux de bord individuels, utilisez la flèche déroulante et choisissez Ajouter un rapport. Pour plus d&#39;informations sur la création de tableaux de bord, consultez la section Tableaux de bord sur cette page.

## Tableaux de bord de gestion {#manager-dashboards}

Un responsable peut afficher des informations sur son équipe directe ou indirecte, sous forme de résumé.

Le responsable peut ensuite filtrer le rapport en fonction de plages comme, trimestre, ce mois, les trois derniers mois complets et les 12 derniers mois complets.

## Résumé de l’apprentissage {#learningsummary}

![](assets/manager-learningsummary.png)

*Afficher le résumé de l’apprentissage*

![](assets/manager-dashboard.jpg)

*Filtrer le résumé d’apprentissage par date*

## Tableau de bord Conformité {#compliancedashboard}

Vérifiez la conformité de votre équipe et le membre qui frise la non-conformité. Sélectionnez les objets d’apprentissage et affichez l’état de chacun d’eux.

![](assets/compliance-dashboard.png)

*Afficher le tableau de bord de conformité*

## État des compétences {#skillsstatus}

Voir le pourcentage d’élèves pour chaque compétence. Choisissez au maximum cinq compétences pour lesquelles vous souhaitez afficher les compétences des élèves. La visualisation se présente sous la forme d’un graphique à barres empilées. Lorsque vous passez la souris sur chaque barre, vous pouvez voir la répartition de l’état de cette compétence.

![](assets/manager-skills-status.png)

*Afficher l’état des compétences d’un élève*

## Suivi des compétences {#skilstracker}

Affichez une projection de l’achèvement des compétences dans une équipe. Choisissez le pourcentage d’achèvement cible et la date d’une compétence.

En fonction des données historiques, vous pouvez voir une représentation graphique de la projection de l’achèvement des compétences à la date sélectionnée.

![](assets/historical-data.png)

*Afficher la projection de l’achèvement des compétences*

## Création de rapports {#creatingreports}

1. Cliquez sur Rapports dans le volet de gauche. La page Résumé du rapport s’affiche.\
   **Remarque**
Par défaut, au moins trois exemples de rapport apparaissent dans la page de résumé du rapport. Vous pouvez uniquement consulter ces exemples de rapports pour vous faire une idée de la façon dont vous pourriez les créer et les personnaliser.

1. Dans la page Résumé du rapport, cliquez sur Ajouter. La boîte de dialogue de création de rapport s’affiche.
1. Cliquez sur Enregistrer pour terminer la création d’un rapport. Un exemple de rapport est présenté ci-dessous à titre de référence.

![](assets/add-report.png)

*Boîte de dialogue Ajouter un rapport*

Dans Type de rapport, vous pouvez choisir un ensemble prédéfini de rapports ou choisir personnalisé. Vous pouvez afficher les rapports suivants dans le cadre d’un ensemble prédéfini de rapports :

* Compétences attribuées et acquises
* Cours inscrit et terminé
* Efficacité des cours
* Programmes d’apprentissage inscrits et terminés
* Temps d’apprentissage par cours
* Temps d’apprentissage par trimestre

Vous pouvez utiliser les types de rapports mentionnés ci-dessus pour générer des rapports de plus de 300 variations.

Nom du rapport Tapez un titre pour votre rapport.

**Axe Y principal** Choisissez le premier/le critère principal de votre rapport dans les options déroulantes. Pour certains des critères sélectionnés, vous avez la possibilité de choisir un ou plusieurs états dans la liste déroulante États adjacente. Par exemple, pour un critère principal de statistiques d&#39;inscription à un cours, les états peuvent être terminé, Incomplet, Inscrit, etc. Les données de plage principales sont représentées sous la forme de graphiques à barres dans le rapport.

**Axe Y secondaire** Choisissez les critères/la plage de l’axe Y secondaire pour votre rapport dans les options déroulantes. Par exemple, dans l&#39;option d&#39;inscription au programme d&#39;apprentissage, choisissez un ou plusieurs états dans la liste déroulante États adjacente. Les données de plage secondaire sont représentées sous la forme de graphiques linéaires.

**Axe X** Choisissez les critères d’axe x appropriés pour votre rapport dans les options déroulantes. Si l&#39;axe des x est choisi comme date, une option permettant de regrouper votre critère d&#39;axe des x par jour, mois, trimestre et année est disponible.

**Date** Choisissez l’option appropriée dans la liste déroulante. Options : dernier mois, trimestre, année, QTD (90 derniers jours), Cumul annuel cumulé (365 derniers jours) et période. Si vous choisissez une plage de dates, indiquez les dates De et A comme suit :

**De** Choisissez la date à partir de laquelle vous souhaitez afficher le rapport.

**Pour** Choisissez la date de fin de votre rapport.

## Filtres {#filters}

Les filtres s’affichent dans la boîte de dialogue Ajouter un rapport en bas en fonction des types de rapports que vous avez choisis. Certains des filtres importants sont mentionnés ci-dessous.

**Responsable** Vous pouvez choisir l’un des responsables en fonction de la hiérarchie. Pour certains responsables, il peut y avoir des responsables subordonnés et plusieurs employés relevant de chaque responsable subordonné.

**Profil** Choisissez la désignation de votre employé. Cela aiderait à consulter les rapports des employés en fonction de leur profil/désignation. Par exemple, informaticien, ingénieur, etc.

**Groupe d’utilisateurs** Choisissez le groupe d’utilisateurs en fonction duquel vous souhaitez filtrer les rapports. Learning Manager récupère les groupes d’utilisateurs définis pour votre compte à partir de la fonctionnalité Utilisateurs.

**Cours** Vous pouvez filtrer votre rapport en fonction de n’importe quel cours en les sélectionnant dans la liste déroulante.

![](assets/sample-report-admin.png)

*Afficher le graphique des cours inscrits et terminés*

>[!NOTE]
>
>Au-dessus de la légende du graphique, vous pouvez voir une zone de zoom. Déplacez le curseur dessus, cliquez et faites glisser la barre transversale sur n’importe quelle partie de la zone de zoom avant.

Les valeurs de l’axe y secondaire s’affichent sous la forme d’une ligne sur les barres du graphique. Par exemple, dans l’exemple ci-dessus, les valeurs d’efficacité s’affichent en grisé sur le graphique.

## Rapports de groupe d’utilisateurs {#user-group-reporting}

Suivez les performances des groupes d’utilisateurs tels que les services, les partenaires externes et les rôles par rapport aux autres groupes d’utilisateurs ou à d’autres objectifs d’apprentissage.

### Groupes d’utilisateurs {#usergroups}

Pour générer des rapports en fonction des groupes d’utilisateurs, choisissez **Groupe d’utilisateurs** dans l’axe X dans la liste des options déroulantes, comme illustré dans la capture d’écran ci-dessous.

![](assets/x-axis-reporting.png)

*Générer des rapports de groupe d’utilisateurs*

Un autre **Sélectionner** Une liste déroulante apparaît en regard de l’axe X et affiche la liste des groupes d’utilisateurs disponibles pour votre compte. Dans cette liste déroulante, vous pouvez sélectionner un ou plusieurs groupes d’utilisateurs.

Une fois que vous avez enregistré et généré ce rapport, si vous avez sélectionné plusieurs groupes d’utilisateurs, le rapport est généré avec tous les groupes d’utilisateurs représentés dans le graphique à barres adjacents sur l’axe des x.

Ce rapport de groupe d’utilisateurs vous permet de comparer les performances d’un service/division/rôle par rapport à l’autre afin d’évaluer leurs acquis en matière d’apprentissage.

### Groupes d’utilisateurs/attributs utilisateur personnalisés {#customusergroupsuserattributes}

Vous pouvez également créer des groupes d’utilisateurs personnalisés à l’aide de la fonctionnalité Ajouter des utilisateurs/groupes d’utilisateurs dans Learning Manager. Après avoir créé les groupes d’utilisateurs, vous pouvez générer des rapports pour ces groupes d’utilisateurs personnalisés à l’aide d’une liste d’attributs tels que l’emplacement, la branche, etc.

Dans l’axe des X, choisissez l’option Attribut utilisateur et sélectionnez l’attribut depuis **sélectionner** liste déroulante en regard de celui-ci. Pour créer un rapport de groupe d’utilisateurs personnalisé basé sur ces attributs, vous devez également choisir le groupe d’utilisateurs approprié dans le filtre.

Les responsables peuvent créer des rapports de groupe d&#39;utilisateurs uniquement pour les membres de leur propre équipe en tant qu&#39;élèves.

## Types de rapports {#typesofreports}

* Statistiques de prestation de cours pour les élèves
* Rapport sur l&#39;efficacité des cours
* Rapport basé sur les compétences de l’élève
* Statistiques d&#39;inscription au programme d&#39;apprentissage pour les élèves
* Temps d’apprentissage passé par les élèves
* Certification terminée

## Mes rapports {#myreports}

Un tableau de bord est un ensemble de rapports. Les rapports peuvent être regroupés dans un tableau de bord selon votre choix.

**Exemples de rapports**

Cliquez sur cet onglet pour afficher certains rapports indicatifs basés sur des exemples de points de données. Explorez ces rapports pour vous faire une idée des différents types de rapports riches en fonctionnalités que vous pouvez générer à l’aide des données de votre compte.

**Mes rapports**

Cliquez sur l’onglet de ce tableau pour afficher tous les tableaux que vous avez créés. Dans la liste déroulante du tableau de bord d’affichage, vous pouvez sélectionner le tableau par défaut ou l’un des tableaux de bord que vous avez créés.

**Ajouter un tableau de bord**

1. Cliquez sur Ajouter un tableau de bord sur le côté droit de la page pour commencer à créer vos propres tableaux.

   ![](assets/add-dashboard.png)

   *Créer votre propre forum*

1. Indiquez le nom et la description du tableau de bord, puis cliquez sur **[!UICONTROL Enregistrer]**.

Vous pouvez afficher le tableau récemment créé dans la liste Mes tableaux de bord.

Pour ajouter des rapports à votre forum, cliquez sur la liste déroulante dans l’angle supérieur droit de la fenêtre du forum, puis cliquez sur Ajouter un rapport. Le rapport ainsi créé est associé à votre tableau de bord.

>[!NOTE]
>
>Les rapports que vous créez en cliquant sur Ajouter dans l’angle supérieur droit de la page Rapports sont ajoutés à votre tableau de bord par défaut.

**Rapports partagés**

Les rapports partagés sont un ensemble de rapports qui ont été partagés avec vous par d’autres utilisateurs au sein de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez télécharger ou dupliquer les rapports partagés. Contactez l’administrateur de votre organisation pour obtenir les droits de téléchargement/de duplication sur les rapports partagés.

**Rapports abonnés**

Vous pouvez vous abonner à vos rapports préférés en fournissant votre ID de messagerie ici. Les rapports souscrits vous sont envoyés par e-mail.

Cliquez sur le bouton **Modifier** dans le coin droit du nom de votre rapport à partir de la liste des rapports pour modifier votre abonnement à tout moment.

## Affichage des rapports {#viewingreports}

Sur la page Résumé du rapport, vous pouvez afficher tous les rapports. Vous pouvez réduire chaque rapport en cliquant sur l’icône moins (-) dans le coin supérieur droit de chaque rapport. Cliquez sur l’icône + pour afficher à nouveau votre rapport.

**Affichage rapide avec différentes dates**

Les valeurs de date que vous utilisez pour afficher le rapport sont temporaires. Cette vue du rapport n’est pas téléchargée lorsque vous sélectionnez l’option de téléchargement. Il s’agit uniquement d’une vue temporaire.

Vous pouvez modifier la plage/valeur de date pour n’importe quel rapport et afficher rapidement une date différente sans modifier ni enregistrer le rapport. Cliquez sur l’icône Modifier (comme illustré par une flèche dans l’instantané ci-dessous) en regard de la plage de dates, telle que QTD, dernière année, etc. Choisissez la nouvelle valeur dans le menu déroulant et cliquez sur la coche pour confirmer la modification. Vous pouvez annuler la modification en cliquant sur la croix (X).

**Affichage rapide avec différents responsables**

Si plusieurs responsables vous rendent des comptes, vous pouvez afficher rapidement les rapports de chaque responsable. Choisissez le nom du responsable dans la liste déroulante pour afficher un rapport unique pour chaque responsable.
**Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner les rapports** Cliquez sur la flèche déroulante dans le coin supérieur droit de chaque rapport pour afficher les options déroulantes Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Modifier** Lors de la modification des données, pour revenir aux valeurs initiales, cliquez sur Réinitialiser. Cliquez sur Enregistrer après avoir modifié les valeurs.

**Déplacer vers le tableau de bord** Vous pouvez déplacer le rapport actuel vers un autre tableau de bord, qui est choisi dans la liste des tableaux de bord.

**Créer une copie** Vous pouvez copier le rapport dans le même tableau de bord ou dans un autre, qui est choisi dans la liste des tableaux de bord.

**Supprimer** Cliquez sur Supprimer pour supprimer le rapport. Un message d’avertissement/de confirmation s’affiche avant la suppression du rapport.

**Redimensionner** Vous pouvez redimensionner vos rapports en taille 1×1 (moyenne) et 2×2 (grande).

## Abonnements aux e-mails {#emailsubscriptions}

Vous pouvez obtenir vos rapports préférés par courrier électronique en vous abonnant à ceux-ci.

Dans la page Rapports, cliquez sur Abonnement par e-mail en regard du bouton Ajouter dans le coin supérieur droit de la page. La page d’abonnement Rapports s’affiche.

Commencez à saisir le nom du rapport dans le champ Rapports pour sélectionner le nom du rapport dans la liste déroulante. Choisissez la fréquence du courrier électronique : quotidienne, hebdomadaire, mensuelle, selon votre choix. Ajoutez l’objet du courrier électronique et cliquez sur Ajouter pour vous abonner.

Cliquez sur Modifier pour modifier l’abonnement. Cliquez sur Supprimer pour supprimer l’abonnement.
