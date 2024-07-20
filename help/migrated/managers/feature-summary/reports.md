---
description: Création et gestion de rapports pour les responsables.
jcr-language: en_us
title: Rapports
contentowner: manochan
exl-id: 5a59b56c-111b-46e4-95e5-60cc3af75c4d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 63%

---

# Rapports

Création et gestion de rapports pour les responsables.

Adobe Learning Manager vous permet de créer différents rapports pour suivre, surveiller et contrôler les activités des élèves. Les activités des élèves font l’objet d’un suivi et sont capturées automatiquement dans la base de données. Les rapports Responsable et Administrateur sont générés à partir de la base de données.

## Vue d’ensemble {#overview}

Le processus de génération des rapports est le même pour Administrateur et pour Responsable. Les responsables peuvent afficher les rapports correspondant à leurs subordonnés tandis que les administrateurs peuvent afficher tous les rapports à l’échelle de l’entreprise.

Les rapports sont regroupés dans un tableau de bord. Un rapport se trouve toujours dans un tableau de bord. Un **tableau de bord par défaut** existe par défaut dans la page des rapports. Tout rapport supplémentaire de votre part entre dans ce tableau de bord par défaut. Pour ajouter des rapports à des tableaux de bord individuels, utilisez la flèche déroulante et choisissez Ajouter un rapport. Pour plus d’informations sur la création des tableaux de bord, consultez la section Tableaux de bord sur cette page.

## Tableaux de bord du responsable {#manager-dashboards}

Un responsable peut afficher des informations sur son équipe directe ou indirecte, sous forme de résumé.

Le responsable peut ensuite filtrer le rapport en fonction de plages comme, trimestre, ce mois, les trois derniers mois complets et les 12 derniers mois complets.

## Résumé de l’apprentissage {#learningsummary}

![](assets/manager-learningsummary.png)

*Afficher le résumé d&#39;apprentissage*

![](assets/manager-dashboard.jpg)

*Filtrer le résumé d’apprentissage par date*

## Tableau de bord Conformité {#compliancedashboard}

Vérifiez la conformité de votre équipe et le membre qui frise la non-conformité. Sélectionnez les objets d’apprentissage et affichez l’état de chacun d’eux.

![](assets/compliance-dashboard.png)

*Afficher le tableau de bord de conformité*

## État des compétences {#skillsstatus}

Consultez le pourcentage d’élèves pour chaque compétence. Choisissez au maximum cinq compétences pour lesquelles vous souhaitez afficher le niveau des élèves. La visualisation prend la forme d&#39;un graphique à barres empilées. Lorsque vous passez la souris sur chaque barre, vous pouvez voir le détail de l’état de cette compétence.

![](assets/manager-skills-status.png)

*Afficher l’état des compétences d’un élève*

## Suivi des compétences {#skilstracker}

Affichez une projection de l&#39;accomplissement des compétences au sein d’une équipe. Choisissez le pourcentage d’achèvement cible et la date d’une compétence.

En fonction des données historiques, vous pouvez voir une représentation graphique de la projection de l&#39;accomplissement des compétences à la date sélectionnée.

![](assets/historical-data.png)

*Afficher la projection de l&#39;achèvement des compétences*

## Création de rapports {#creatingreports}

1. Cliquez sur Rapports dans le volet de gauche. La page Synthèse des rapports s’affiche.\
   **Remarque**
Par défaut, au moins trois exemples de rapport apparaissent dans la page de résumé du rapport. Vous pouvez seulement afficher ces exemples de rapport pour avoir une idée quant à la manière dont vous pouvez les créer et les personnaliser.

1. Dans la page Synthèse des rapports, cliquez sur Ajouter. La boîte de dialogue de création de rapport s’affiche.
1. Cliquez sur Enregistrer pour terminer la création d’un rapport. Un exemple de rapport est affiché ci-dessous en référence.

![](assets/add-report.png)

*Boîte de dialogue Ajouter un rapport*

Dans Type de rapport, vous pouvez choisir un ensemble prédéfini de rapports ou sélectionner Personnalisé. Vous pouvez afficher les rapports suivants en tant que partie d’un ensemble prédéfini de rapports :

* Compétences attribuées et obtenues
* Cours inscrits et terminé
* Efficacité pour les cours
* Programmes d’apprentissage inscrits et terminés
* Temps passé à apprendre par cours
* Temps passé à apprendre par trimestre

Vous pouvez utiliser les types de rapport mentionnés ci-dessus pour générer plus de 300 rapports différents.

Nom du rapport Tapez un titre pour votre rapport.

**Axe Y principal** Choisissez le premier/le critère principal de votre rapport dans les options déroulantes. Pour certains des critères sélectionnés, vous avez la possibilité de choisir un ou plusieurs états dans la liste déroulante États adjacente. Par exemple, pour un critère principal de statistiques d&#39;inscription à un cours, les états peuvent être terminé, Incomplet, Inscrit, etc. Les données de plage principale sont représentées sous forme de graphiques à barres dans le rapport.

**Axe Y secondaire** Choisissez les critères/la plage de l&#39;axe Y secondaire pour votre rapport dans les options déroulantes. Par exemple, dans l&#39;option d&#39;inscription au programme d&#39;apprentissage, choisissez un ou plusieurs états dans la liste déroulante États adjacente. Les données de plage secondaire sont représentées sous forme de graphiques linéaires.

**Axe des x** Choisissez les critères d&#39;axe des x appropriés pour votre rapport dans les options déroulantes. Si l’axe X est sélectionné en tant que date, une option de regroupement de votre critère d’axe X par Jour, Mois, Trimestre et Année est disponible.

**Date** Choisissez l&#39;option appropriée dans la liste déroulante. Options : dernier mois, dernier trimestre, dernière année, QTD (90 derniers jours), YTD (365 derniers jours) et la plage de dates. Si vous sélectionnez la plage de dates, indiquez les dates Du et Au comme suit :

**De** Choisissez la date de début à partir de laquelle vous souhaitez afficher le rapport.

**À** Choisissez la date de fin de votre rapport.

## Filtres {#filters}

Les filtres s&#39;affichent dans la boîte de dialogue Ajouter un rapport en bas en fonction des types de rapports que vous avez sélectionnés. Certains de ces filtres principaux sont mentionnés ci-dessous.

**Responsable :** vous pouvez sélectionner l’un des responsables en fonction de la hiérarchie. Pour certains responsables, il peut exister des responsables subordonnés ainsi que plusieurs employés supervisés par chaque responsable subordonné.

**Profil :** choisissez la désignation de votre employé. Il est plus pratique d’afficher les rapports des employés selon leur profil/désignation. Par exemple, informaticien, ingénieur, et ainsi de suite.

**Groupe d&#39;utilisateurs** Choisissez le groupe d&#39;utilisateurs à partir duquel vous souhaitez filtrer les rapports. Learning Manager récupère les groupes d’utilisateurs définis pour votre compte depuis la fonction Utilisateurs.

**Cours** Vous pouvez filtrer votre rapport en fonction de n&#39;importe quel cours en le sélectionnant dans la liste déroulante.

![](assets/sample-report-admin.png)

*Afficher le graphique des cours inscrits et terminés*

>[!NOTE]
>
>Au-dessus de la légende du graphique, vous pouvez afficher une case de zoom. Vous pouvez y placer le pointeur de la souris, cliquer et faire glisser la barre transversale sur n’importe quelle partie de la zone de zoom que vous souhaitez agrandir.

Vous pouvez afficher les valeurs de l’axe Y secondaire sous forme de ligne à travers le graphique à barres. Par exemple, dans l’exemple ci-dessus, vous pouvez voir les valeurs de l’efficacité dans une ligne grise à travers le graphique.

## Rapports de groupes d’utilisateurs {#user-group-reporting}

Suivez la manière dont les groupes d’utilisateurs, tels que des services, des partenaires externes et des rôles se comportent en comparaison d’autres groupes d’utilisateurs ou par rapport à d’autres objectifs pédagogiques.

### Groupes d’utilisateurs {#usergroups}

Pour générer des rapports en fonction des groupes d&#39;utilisateurs, choisissez **Groupe d&#39;utilisateurs** sur l&#39;axe X dans la liste des options déroulantes comme indiqué dans la capture d&#39;écran ci-dessous.

![](assets/x-axis-reporting.png)

*Générer des rapports de groupe d&#39;utilisateurs*

Un autre menu déroulant **Sélectionner** s&#39;affiche en regard de l&#39;axe x avec une liste de groupes d&#39;utilisateurs disponibles pour votre compte. Dans cette liste déroulante, vous pouvez sélectionner un ou plusieurs groupes d’utilisateurs.

Une fois que vous avez enregistré et généré le rapport, si vous avez sélectionné plusieurs groupes d&#39;utilisateurs, le rapport est généré avec tous les groupes d&#39;utilisateurs représentés dans le graphique à barres à côté des autres sur l&#39;axe des x.

Ce rapport de groupe d’utilisateurs vous permet de comparer la performance d’un(e) service/division/rôle par rapport à l’autre pour leurs progrès en termes de formation.

### Attributs personnalisés de groupes d&#39;utilisateurs/utilisateur {#customusergroupsuserattributes}

Vous pouvez également créer des groupes d&#39;utilisateurs personnalisés à l&#39;aide de la fonction Ajouter des utilisateurs/un groupe d’utilisateurs dans Learning Manager. Après avoir créé des groupes d&#39;utilisateurs, vous pouvez générer des rapports pour ces groupes d&#39;utilisateurs personnalisés avec l&#39;aide d&#39;une liste d&#39;attributs, tels que l&#39;emplacement, la succursale, et ainsi de suite.

Sur l&#39;axe des X, choisissez l&#39;option d&#39;attribut utilisateur et sélectionnez l&#39;attribut dans la liste déroulante **sélectionner** qui se trouve à côté. Pour créer un rapport de groupe d’utilisateurs personnalisé basé sur ces attributs, vous devez également choisir le groupe d’utilisateurs approprié dans le filtre.

Les responsables peuvent créer des rapports de groupe d&#39;utilisateurs uniquement pour les membres de leur propre équipe comme stagiaires.

## Types de rapports {#typesofreports}

* Statistiques de fourniture des cours aux élèves
* Rapport sur l’efficacité des cours
* Rapport basé sur la compétence de l’élève
* Statistiques d’inscription aux programmes d’apprentissage des élèves
* Temps d’apprentissage des élèves
* Fin de certification

## Mes rapports {#myreports}

Un tableau de bord est une série de rapports. Les rapports peuvent être regroupés dans un tableau de bord selon votre choix.

**Exemples de rapport** 

Cliquez sur cet onglet pour afficher certains rapports indicatifs basés sur des exemples de points de données. Explorez ces rapports pour avoir une idée des différents types de rapports riches en fonctions, pouvant être générés en utilisant les données de votre compte.

**Mes rapports** 

Cliquez sur l’onglet de ce tableau pour afficher tous les tableaux que vous avez créés. Dans la liste déroulante du tableau de bord d’affichage, vous pouvez sélectionner le tableau par défaut ou l’un des tableaux de bord que vous avez créés.

**Ajouter le tableau de bord** 

1. Cliquez sur Ajouter un tableau de bord, sur le côté droit de la page, pour commencer à créer vos propres tableaux.

   ![](assets/add-dashboard.png)

   *Créer votre propre forum*

1. Fournissez le nom et une description du tableau de bord, puis cliquez sur **[!UICONTROL Enregistrer]**.

Vous pouvez afficher le tableau récemment créé dans la liste Mes tableaux de bord.

Pour ajouter des rapports à votre forum, cliquez sur la liste déroulante dans l’angle supérieur droit de la fenêtre du forum, puis cliquez sur Ajouter un rapport. Le rapport que vous créez ainsi est associé à votre tableau de bord.

>[!NOTE]
>
>Les rapports que vous créez en cliquant sur Ajouter dans l’angle supérieur droit de la page Rapports sont ajoutés à votre tableau de bord par défaut.

**Rapports partagés** 

Les rapports partagés sont un ensemble de rapports qui ont été partagés ave vous par d&#39;autres utilisateurs dans votre entreprise. Si vous disposez des autorisations, vous pouvez télécharger ou dupliquer les rapports partagés. Contactez l&#39;administrateur de votre société pour obtenir des droits d&#39;accès pour télécharger/dupliquer les rapports partagés.

**Rapports abonné** 

Vous pouvez souscrire à vos rapports favoris en fournissant votre adresse électronique ici. Vos rapports abonnés vous sont envoyés par courrier électronique.

Cliquez sur l&#39;icône **Modifier** dans le coin droit du nom de votre rapport dans la liste des rapports pour modifier votre abonnement à tout moment.

## Affichage des rapports {#viewingreports}

Dans la page Synthèse des rapports, vous pouvez afficher tous les rapports. Vous pouvez réduire chaque rapport en cliquant sur l’icône moins (-) dans l’angle supérieur droit de chaque rapport. Cliquez sur l’icône + pour afficher votre rapport.

**Affichage rapide avec différentes dates**

Les valeurs de date que vous utilisez pour afficher le rapport sont temporaires. Cette vue de rapport n’est pas téléchargée lorsque vous sélectionnez l’option de téléchargement. Il ne s’agit que d’une vue temporaire.

Vous pouvez modifier la valeur/plage de dates de tout rapport et afficher rapidement une date différente sans modifier ni enregistrer le rapport. Cliquez sur l’icône Modifier (comme illustré avec une flèche dans l’instantané ci-dessous) en regard de la plage de dates, telle que QTD, la dernière année et ainsi de suite. Choisissez la nouvelle valeur dans le menu déroulant et cliquez sur la coche pour confirmer la modification. Vous pouvez annuler la modification en cliquant sur le symbole X.

**Affichage rapide avec différents responsables** 

Si vous supervisez plusieurs responsables, vous pouvez afficher rapidement les rapports de chaque responsable. Choisissez le nom du responsable dans la liste déroulante pour afficher un rapport unique pour chaque responsable.
**Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner les rapports** Cliquez sur la flèche déroulante dans le coin supérieur droit de chaque rapport pour afficher les options déroulantes Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Modifier** lors de la modification des données, pour revenir aux valeurs initiales, cliquez sur Réinitialiser. Cliquez sur Enregistrer après avoir modifié les valeurs.

**Déplacer vers le tableau de bord** Vous pouvez déplacer le rapport actuel vers un autre tableau de bord, qui est choisi dans la liste des tableaux de bord.

**Créer une copie** Vous pouvez copier le rapport dans le même tableau de bord ou dans un autre, qui est choisi dans la liste des tableaux de bord.

**Supprimer** Cliquez sur Supprimer pour supprimer le rapport. Un message d’avertissement/de confirmation s’affiche avant de pouvoir supprimer le rapport.

**Redimensionner** Vous pouvez redimensionner vos rapports en tailles 1×1 (moyenne) et 2×2 (grande).

## Abonnements par e-mail {#emailsubscriptions}

Vous pouvez obtenir vos rapports favoris par courrier électronique en vous abonnant.

Dans la page Rapports, cliquez sur Abonnement par e-mail, en regard du bouton Ajouter dans l’angle supérieur droit de la page. La page Abonnement aux rapports s’affiche.

Commencez à saisir le nom du rapport dans le champ Rapports pour sélectionner le nom du rapport dans la liste déroulante. Choisissez la fréquence du courrier électronique : quotidienne, hebdomadaire, mensuelle, selon votre choix. Ajoutez l’objet du courrier électronique et cliquez sur Ajouter pour vous abonner.

Cliquez sur Modifier pour modifier l’abonnement. Cliquez sur Supprimer pour supprimer l’abonnement.
