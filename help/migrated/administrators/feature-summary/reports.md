---
description: Découvrez les rapports associés au rôle d’administrateur dans l’application Learning Manager.
jcr-language: en_us
title: Rapports
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '6441'
ht-degree: 0%

---



# Rapports

Découvrez les rapports associés au rôle d’administrateur dans l’application Learning Manager.

Adobe Learning Manager vous permet de créer divers rapports pour suivre, surveiller et contrôler les activités des élèves. Les activités des élèves sont suivies et capturées automatiquement dans la base de données. Les rapports des responsables et des administrateurs sont générés à partir de la base de données.

## Présentation {#overview}

Le processus de génération de rapports est similaire pour l’administrateur et le responsable. Les responsables peuvent afficher les rapports correspondant à leurs subordonnés, tandis que les administrateurs peuvent afficher tous les rapports de l’organisation.

Les rapports sont regroupés dans un tableau de bord. Un rapport doit exister dans un tableau de bord. A **[!UICONTROL Tableau de bord par défaut]** existe par défaut dans la page rapports. Tout rapport que vous ajoutez passe dans ce tableau de bord par défaut. Pour ajouter des rapports à des tableaux de bord individuels, utilisez la flèche déroulante et choisissez **[!UICONTROL Ajouter un rapport]**. Pour plus d&#39;informations sur la création de tableaux de bord, consultez la section Tableaux de bord sur cette page.

## Tableaux de bord Résumé de l’apprentissage {#dashboards}

Consultez un rapport récapitulatif de toutes les activités d’apprentissage de la plateforme. Sur cette page, vous pouvez voir les informations récapitulatives suivantes pour l’équipe et les profils externes de l’utilisateur racine sélectionné. Vous pouvez également sélectionner une plage horaire :

* Résumé de l’apprentissage sous la forme d’inscriptions, de vues et d’achèvements
* Principales compétences
* Résumé de la conformité

![](assets/summary-charts.png)
*Graphiques récapitulatifs*

S&#39;il y a des gestionnaires internes de niveau racine, ils seront affichés l&#39;un après l&#39;autre.

Tous les profils externes sont répertoriés après les profils internes (utilisateurs racine internes).

Si un profil externe a un responsable, la hiérarchie du responsable s’affiche dans le panneau **[!UICONTROL Affichage des données pour]** liste déroulante. - L’utilisateur sera répertorié dans la hiérarchie du responsable dans toutes les pages de détails (Résumé de l’apprentissage, Conformité et État des compétences)

Si ce n’est pas le cas, tous les détails des utilisateurs individuels seront affichés dans la liste.

Pour afficher des détails plus précis sur les inscriptions des différentes équipes internes, cliquez sur **[!UICONTROL Détails du résumé d’apprentissage]**.

![](assets/learning-sunnarydetails.png)
*Détails du résumé d’apprentissage*

Lorsque vous cliquez sur une inscription, vous pouvez voir les élèves de chaque responsable et l’inscription à laquelle chaque objet d’apprentissage est associé. Vous pouvez également voir les détails de progression et d’achèvement de chaque élève.

![](assets/learners-for-a-manager.png)
*Voir les élèves affectés à un responsable*

Cliquez sur n’importe quelle équipe et exportez son rapport au format csv. Un administrateur peut exporter le rapport pour n’importe quel utilisateur du groupe d’utilisateurs ou utilisateur individuel en sélectionnant le groupe d’utilisateurs ou l’utilisateur individuel, puis exporter les détails dans la liste déroulante Action.

En outre, vous pouvez voir un graphique à barres des compétences qui sont en cours et ont été acquises. Vous pouvez ajouter/supprimer des compétences que vous souhaitez mettre en avant dans le graphique.

![](assets/skill-status-stackedbarchart.png)
*Graphique à barres empilées de l’état des compétences*

Dans la visualisation finale, vous pouvez vérifier l’état de conformité des élèves et prendre les mesures appropriées.

En outre, un administrateur peut afficher des données de formation individuelles dans le tableau de bord de conformité.

Par exemple, l’administrateur a identifié trois formations pour suivre la conformité. Learning Manager fournit un instantané de la conformité pour les trois formations en même temps.

Désormais, un administrateur peut cliquer sur n’importe quelle formation et consulter rapidement la conformité de la formation sélectionnée.

![](assets/compliance-dashboard.png)
*Afficher le tableau de bord de conformité*

Vous pouvez également voir l’état de conformité de chaque équipe interne.

Cliquez sur le lien **[!UICONTROL Détails de l’état de conformité]** en bas de la visualisation.

Vous pouvez voir que, pour une équipe, le nombre d’élèves dans l’équipe enfreint ou honore la conformité de l’apprentissage.

![](assets/compliance-statusofateam.png)
*Statut de conformité d’une équipe*

## Partager la formation avec les responsables

Learning Manager propose un tableau de bord de conformité à tous les administrateurs et responsables. Les responsables trouvent très utile de suivre la conformité des membres de leur équipe pour une formation particulière. Parallèlement, les administrateurs souhaitent que tous les responsables ajoutent des formations sur la conformité à leur tableau de bord et en assurent le suivi.

Dans Learning Manager, le **[!UICONTROL Partager avec les responsables]** permet aux administrateurs de partager la formation avec les responsables, afin qu&#39;ils puissent être ajoutés au tableau de bord de conformité d&#39;un responsable. Ainsi, les responsables n’ont rien à faire et peuvent commencer immédiatement à suivre la conformité.

Un administrateur peut partager un ensemble de cours de formation avec des responsables individuellement ou au sein d’un groupe. Ce partage peut aider un responsable à suivre facilement la conformité de son équipe pour la formation spécifiée.

L’administrateur peut envoyer une liste par défaut de formation à la conformité pour qu’elle soit affichée dans le tableau de bord de conformité du responsable.

### Partager la formation

1. Entrée **[!UICONTROL Rapports]** > **[!UICONTROL Résumé de l’apprentissage]**, faites défiler vers le bas, puis cliquez sur l’onglet **[!UICONTROL Partager avec les responsables]**.

   ![](assets/share-with-managers.png)
   *Partager la formation avec les responsables*

1. Pour ajouter une ou plusieurs formations, cliquez sur **[!UICONTROL Partager plus]**.

1. Dans le panneau **[!UICONTROL Partager avec les responsables]** , choisissez la ou les formations et le ou les responsables.

   ![](assets/select-training.png)
   *Sélectionner la formation à partager avec les responsables*

1. Cliquez sur **[!UICONTROL Partager]**.

La formation est maintenant partagée avec le responsable spécifié.

### Afficher la formation

Dans la liste des formations partagées, cliquez sur **[!UICONTROL Afficher]**. Vous pouvez afficher la formation affectée à un ou plusieurs responsables.

### Retirer une formation

1. Pour retirer une formation d’un responsable, cliquez sur **[!UICONTROL Retirer]**.

1. Cliquez sur **[!UICONTROL Continuer]**. Cette action retire la formation précédemment partagée du tableau de bord de conformité du responsable.

## Tableaux de bord Activité des utilisateurs {#useractivitydashboards}

Affichez un résumé de toutes les activités des utilisateurs sur la plateforme au fil du temps. Configurez les groupes d’utilisateurs et appliquez des filtres.

Le tableau de bord d’activité des utilisateurs affiche l’activité des utilisateurs dans le compte. Les trois rapports énumérés sont les suivants :

* **Utilisateurs enregistrés :** Ce rapport fournit des informations sur le nombre d’utilisateurs enregistrés dans votre compte chaque semaine. Pour les comptes disposant d’une licence Unités mensuelles actives, le rapport affiche plutôt les unités MAU.

* **Rapport de visites d’utilisateurs :** Ce rapport fournit des informations sur le nombre d’utilisateurs accédant à la plateforme au jour le jour. Un rapport mensuel est également disponible.

* **Rapport Temps d’apprentissage passé :** Ce rapport fournit des informations sur le temps d’apprentissage passé sur la plateforme au jour le jour. Un rapport mensuel est également disponible.

## Utilisateurs inscrits {#registeredusers}

Learning Manager enregistre le nombre d’utilisateurs enregistrés dans le système chaque semaine. Les administrateurs peuvent consulter ce rapport pour comprendre le nombre d’utilisateurs enregistrés ce jour de la semaine. Le nombre enregistré une fois stocké pendant une semaine ne change pas. Par conséquent, le nombre d’inscrits historiques n’est pas lié à l’ensemble actuel d’élèves dans le système.

Ce rapport fournit des informations sur le nombre d’utilisateurs enregistrés dans votre compte chaque semaine.

Pour les comptes disposant d’une licence Unités mensuelles actives, le rapport affiche plutôt les unités MAU.

![](assets/registered-usersreport.png)
*Rapport Utilisateurs enregistrés*

***Pour les comptes Unités avec accès mensuel :***

**Rapport Utilisateurs actifs mensuels**

Ce rapport indique le nombre d’élèves actifs dans la plateforme d’apprentissage chaque mois. L’utilisateur est considéré comme actif pour le mois s’il effectue l’une des actions d’apprentissage mentionnées ici. C&#39;est la même façon que les Unités Actives Mensuelles sont comptées.

Le nombre mensuel actif une fois compté et stocké pendant un mois, ne change pas. Par conséquent, le nombre historique affiché n’est pas lié à l’ensemble actuel d’élèves dans le système.

## Visites d’utilisateurs {#uservisits}

Ce rapport affiche le nombre total d’élèves accédant au système sur une période d’un jour ou d’un mois. Naviguer sur la plate-forme d’apprentissage sans consommer d’apprentissage est également considéré comme un « accès » à la plate-forme d’apprentissage. Cela permet à l’administrateur de comprendre l’ensemble total des utilisateurs accédant au système. Le premier jour du mois, Learning Manager crée un enregistrement du nombre total d’utilisateurs accédant à la plateforme pour le mois précédent. Il capture également les informations de groupe d’utilisateurs pour ces utilisateurs.

Seuls les groupes d’utilisateurs configurés par l’administrateur sont enregistrés. Cela permet également aux administrateurs d’appliquer un filtre sur les groupes d’utilisateurs pour les données mensuelles historiques. Notez que si la configuration des groupes d’utilisateurs est modifiée et que Learning Manager n’a pas enregistré de données pour ce groupe d’utilisateurs au cours des mois précédents, Learning Manager ne peut pas afficher les données pour ces groupes d’utilisateurs nouvellement configurés pour les mois précédents.

Ce rapport répertorie les utilisateurs qui accèdent à la plateforme à l’aide de tous les formats, tels que le web, les applications mobiles, les solutions personnalisées sans interface utilisateur, etc. Le graphique d’utilisation de l’application pour appareil mentionne spécifiquement uniquement les utilisateurs accédant à la plateforme à l’aide de l’application pour appareil de Learning Manager. Cela aide les administrateurs à identifier l’utilisation de l’application mobile dans leur compte.

![](assets/user-visit-report.png)
*Rapport de visite d’utilisateur*

## Rapport Temps d’apprentissage passé {#learningtimespentreport}

Vous pouvez voir ici des graphiques linéaires à deux axes qui affichent le temps d’apprentissage total passé par tous les élèves sur une période de 12 mois. Le deuxième axe représente le temps médian passé par un individu à apprendre.

Le temps passé pour différents objets d’apprentissage, tels que les programmes d’apprentissage et les certifications, est calculé pour les éléments suivants :

* Cours individualisé avec contenu statique et interactif
* Cours d’activité avec URL.
* Sessions de week-end avec l’indicateur de week-end activé.
* Session VC connect où l&#39;assiduité est marquée automatiquement.
* Temps passé pour différents objets d’apprentissage, tels que les programmes d’apprentissage et les certifications
* Instructions xAPI pour un cours d’activité xAPI.

Vous pouvez exporter le graphique sous forme de feuille de calcul Excel.

Un filtre permettant de choisir la configuration du groupe d’utilisateurs est fourni. Il vous aidera à afficher les données relatives aux différents groupes d’utilisateurs.

Le filtre de date et de groupe d’utilisateurs sélectionné est appliqué à tous les graphiques pertinents dans le tableau de bord.

>[!NOTE]
>
>Pour **[!UICONTROL Visites d’utilisateurs]** et **[!UICONTROL Temps d’apprentissage]** rapports, les données par défaut affichées (lorsqu’aucun groupe d’utilisateurs n’est configuré) concerneront l’ensemble du compte.

## Tableau de bord Contenu de formation {#trainingcontentdashboard}

Le tableau de bord du contenu de formation offre des informations sur les formations disponibles sur la plateforme. Vous pouvez afficher les formations populaires ou suivre toutes les formations disponibles.

## Rapport de formations {#trainingsreport}

Ce rapport fournit des informations sur le nombre total de formations disponibles sur la plateforme (dans l’état publié) mois après mois. Il donne une indication du nombre de formations proposées au fil du temps.

![](assets/training-report.png)
*Rapport de formation*

## Rapport des formations actives {#activetrainingsreport}

Ce rapport fournit des informations sur les formations actives sur la période sélectionnée. Les formations actives sont des formations auxquelles vous êtes inscrit(e), qui sont visionnées dans le lecteur ou qui sont terminées dans le temps imparti.

Pour les formations actives, les données de tous les groupes internes d’utilisateurs racine (avec le rôle de responsable) seront disponibles pour la sélection lorsqu’aucune configuration de groupe d’utilisateurs n’est effectuée. Outre les groupes d’utilisateurs racine, vous pouvez configurer 10 autres groupes d’utilisateurs si nécessaire.

![](assets/active-trainingsreport.png)
*Rapport sur les formations actives*

>[!NOTE]
>
>Les données ne s’affichent pas comme prévu lorsque **[!UICONTROL Tous les utilisateurs]** et **[!UICONTROL 12 mois]** les filtres sont sélectionnés, mais les données s’affichent lorsque vous sélectionnez **[!UICONTROL Tous les groupes d’utilisateurs internes].**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Référence</b></p></td>
   <td>
    <p><b>Métrique</b></p></td>
   <td>
    <p><b>Description</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Format de départ (%)</p></td>
   <td>
    <p>Rapport entre le nombre d'élèves qui ont commencé le cours et le nombre d'inscriptions.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Taux d’achèvement (%)</p></td>
   <td>
    <p>Rapport entre le nombre total d’utilisateurs ayant terminé le cours et le nombre total d’utilisateurs ayant commencé le cours.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Commentaires des élèves</p></td>
   <td>
    <p>Moyenne de toutes les réponses de retour d’informations L1 reçues sur une échelle de 1 à 10 arrondie à l’entier le plus proche.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Commentaires du responsable</p></td>
   <td>
    <p>Moyenne de toutes les réponses de retour d’informations L3 reçues sur une échelle de 1 à 5 arrondie à l’entier le plus proche<br></p></td>
  </tr>
 </tbody>
</table>

Le rapport de formation comporte deux colonnes supplémentaires :

1. Nombre moyen d’étoiles d’un cours.
1. Nombre d’élèves ayant évalué le cours.
1. Chemin incorporé
1. ID du chemin incorporé
1. ID de cours intégré

>[!NOTE]
>
>Le taux de démarrage, le taux d’achèvement, le retour d’informations de l’élève et le retour d’informations du responsable ne sont pas affectés par les filtres appliqués. Les filtres affectent uniquement l’inscription, les vues et les achèvements.

>[!NOTE]
>
>Pour les deux rapports (Contenu de formation, Activité de l’utilisateur), vous pouvez configurer un maximum de 10 groupes d’utilisateurs. Le traitement et la mise à disposition des filtres nouvellement configurés peuvent prendre jusqu’à 24 heures.

## Rapports de tableau de bord {#dashboardreports}

Un tableau de bord est un ensemble de rapports. Les rapports peuvent être regroupés dans un tableau de bord selon votre choix.

## Rapports d’exemple {#samplereports}

Le **[!UICONTROL Rapports d’exemple]** pour afficher certains rapports indicatifs basés sur des exemples de points de données. Explorez ces rapports pour vous faire une idée des différents types de rapports riches en fonctionnalités que vous pouvez générer à l’aide des données de votre compte.

## Rapports de tableau de bord {#DashboardReports-1}

Pour afficher tous les tableaux que vous avez créés, cliquez sur cet onglet du tableau. À partir de **[!UICONTROL Afficher le tableau de bord]** dans la liste déroulante, vous pouvez sélectionner le tableau par défaut ou un tableau de bord que vous avez créé.

## Création d’un tableau de bord {#createadashboard}

1. Pour commencer à créer vos propres tableaux, cliquez sur Ajouter un tableau de bord sur le côté droit de la page.

   ![](assets/add-dashboards.png)
   *Ajouter des tableaux de bord*

1. Indiquez le nom et la description du tableau de bord.
1. Si vous souhaitez partager le tableau de bord avec n’importe quel responsable, sélectionnez-les dans **[!UICONTROL Partager avec]** champ. Vous pouvez utiliser n’importe quel critère de sélection normal pour cette opération.
1. Cliquez sur **[!UICONTROL Enregistrer].**

Vous pouvez afficher le forum récemment créé dans la section **[!UICONTROL Rapports de tableau de bord]** onglet.

Pour ajouter des rapports à votre tableau, cliquez sur la liste déroulante dans l’angle supérieur droit de la fenêtre de votre tableau, puis cliquez sur **[!UICONTROL Ajouter un rapport]**. Le rapport ainsi créé est associé à votre tableau de bord.

>[!NOTE]
>
>Les rapports que vous créez en cliquant sur Ajouter dans le coin supérieur droit de la page Rapports sont ajoutés à votre tableau de bord par défaut.

## Tableaux de bord partagés {#shareddashboards}

Les forums partagés sont un ensemble de rapports qui ont été partagés avec vous par d’autres utilisateurs de votre organisation. Tous les rapports que vous ajoutez à un forum partagé sont automatiquement partagés avec d’autres utilisateurs qui y ont accès.

Vous pouvez partager le forum de deux manières :

* En saisissant des utilisateurs dans **[!UICONTROL Partager avec]** champ avec lequel le tableau de bord est partagé.
* Sélectionnez Modifier le tableau de bord dans la liste déroulante et saisissez les détails de l’utilisateur pour partager le tableau de bord.

>[!NOTE]
>
>Un responsable peut uniquement afficher les rapports des membres de son équipe à partir d’un tableau de bord partagé.

## Téléchargement {#downloads}

La feuille exportée de rapports de tableau de bord fournit des informations détaillées au lieu du résumé du rapport. Le rapport téléchargé suit le format d’un relevé de notes de l’élève.

## Création de rapports {#report}

1. Cliquez sur Rapports dans le volet de gauche. La page Résumé du rapport s’affiche.

   >[!NOTE]
   >
   >Par défaut, au moins trois exemples de rapport s’affichent dans l’onglet du panneau d’exemples. Vous pouvez uniquement consulter les exemples de rapports pour vous faire une idée de la façon dont vous pourriez les créer et les personnaliser.

1. Dans le coin supérieur droit de la page, cliquez sur **[!UICONTROL Ajouter]**.
1. Dans le panneau **[!UICONTROL Ajouter un rapport]** , dans la liste déroulante Type, vous pouvez choisir l’un des rapports prédéfinis ou sélectionner l’option appropriée. **[!UICONTROL Personnalisé]**. Si vous sélectionnez un rapport prédéfini, vous pouvez voir que le formulaire est pré-rempli. Vous pouvez ensuite apporter des modifications à certains champs et cliquer sur **[!UICONTROL Enregistrer]**. Le rapport est ajouté à votre tableau de bord par défaut.

   ![](assets/create-report.png)
   *Créer un rapport*

   Entrée **[!UICONTROL Type de rapport]**, vous pouvez choisir un ensemble prédéfini de rapports ou choisir des valeurs personnalisées. Vous pouvez afficher les rapports suivants dans le cadre d’un ensemble prédéfini de rapports :

   * Compétences attribuées et acquises
   * Cours inscrit et terminé
   * Efficacité des cours
   * Programmes d’apprentissage inscrits et terminés
   * Temps d’apprentissage par cours
   * Temps d’apprentissage par trimestre
   * Certification terminée

1. Choisissez l’option **[!UICONTROL axe Y]** pour votre rapport à partir des options déroulantes. Pour certains des critères sélectionnés, vous pouvez choisir un ou plusieurs états dans les options Etats. Par exemple, pour un critère principal de statistiques d&#39;inscription à un cours, les états peuvent être terminé, incomplet et inscrit. Les données de plage principales sont représentées sous la forme de graphiques à barres dans le rapport.

   ![](assets/axes-for-reports.png)
   *Axes pour les rapports*

1. Choisir le secondaire **[!UICONTROL axe Y]** critères/plage de votre rapport dans les options déroulantes. Par exemple, pour une option d&#39;inscription à un programme d&#39;apprentissage, choisissez un ou plusieurs états dans la liste déroulante États. Les données de plage secondaire sont représentées sous la forme de graphiques linéaires.
1. Choisissez les critères d’axe X**** appropriés pour votre rapport dans les options déroulantes. Si l&#39;axe des x est choisi comme date, une option permettant de regrouper votre critère d&#39;axe des x par jour, mois, trimestre et année est disponible.
1. Dans la section Intervalle de temps, choisissez l’option appropriée dans la liste déroulante. Les options disponibles sont les suivantes :

   * Le mois dernier
   * Trimestre
   * Année
   * QTD (90 derniers jours)
   * cumulé sur l&#39;exercice en cours (365 derniers jours)
   * Période. Fournissez des valeurs dans le champ **[!UICONTROL De]** et **[!UICONTROL Pour]** champs de date.

   ![](assets/time-filter-for-report.png)

1. **Section Filtres**

   Les filtres s’affichent dans la boîte de dialogue Ajouter un rapport en bas en fonction des types de rapports que vous avez choisis. Certains des filtres importants sont mentionnés ci-dessous.

   * **Responsable :** Vous pouvez choisir l’un des responsables en fonction de la hiérarchie. Pour certains responsables, il peut y avoir des responsables subordonnés et plusieurs employés relevant de chaque responsable subordonné.
   * **Profil :** Choisissez la désignation de votre employé. Cela aiderait à consulter les rapports des employés en fonction de leur profil/désignation. Par exemple, informaticien, ingénieur.
   * **Groupe d’utilisateurs :** Choisissez le groupe d’utilisateurs en fonction duquel vous souhaitez filtrer les rapports. Learning Manager récupère les groupes d’utilisateurs définis pour votre compte à partir de la fonctionnalité Utilisateurs.
   * **Contenu :** Vous pouvez filtrer votre rapport en fonction de n’importe quel cours en les sélectionnant dans la liste déroulante.

   Développez cette section et choisissez les filtres requis.

   ![](assets/choose-filters.png)
   *Choisir des filtres*

1. Cliquez sur **[!UICONTROL Enregistrer]** pour terminer la création d’un rapport.

   ![](assets/sample-report.png)
   *Exemple de rapport*

## Modification d’un rapport {#editareport}

Dans le rapport, cliquez sur la flèche déroulante, puis sélectionnez l’option **[!UICONTROL Modifier le rapport]**.

![](assets/edit-a-report-1.png)
*Modification d’un rapport*

Apportez les modifications requises au rapport. Pour enregistrer les modifications, cliquez sur **[!UICONTROL Enregistrer]**.

## Déplacer un rapport vers un tableau de bord {#moveareporttoadashboard}

Choisissez cette option pour déplacer le rapport actuel vers un tableau de bord existant. Pour déplacer le rapport, cliquez sur l’option **[!UICONTROL Déplacer vers le tableau de bord]**.

![](assets/move-a-report.png)
*Déplacer un rapport vers un tableau de bord*

Sélectionnez le tableau de bord vers lequel vous souhaitez déplacer le rapport et cliquez sur **[!UICONTROL Déplacer]**.

## Création d’une copie d’un rapport {#createacopyofareport}

Pour créer une copie du rapport, sélectionnez l’option **[!UICONTROL Créer une copie]**.

![](assets/copy-a-report.png)
*Création d’une copie d’un rapport*

Sélectionnez le tableau de bord dans lequel vous souhaitez copier le rapport. Pour commencer la copie, cliquez sur **[!UICONTROL Copier]**.

## Suppression d’un rapport {#deleteareport}

Pour supprimer un rapport, sélectionnez l’option **[!UICONTROL Supprimer le rapport]**. Une fois le rapport supprimé, vous ne pouvez plus le restaurer. Le processus est irréversible. Procédez avec précaution lors de la suppression d’un rapport.

![](assets/delete-a-report.png)
*Suppression d’un rapport*

## Téléchargement d’un rapport {#downloadareport}

Pour télécharger le rapport, sélectionnez l’option **[!UICONTROL Télécharger le rapport]**.

![](assets/download-a-report.png)
*Téléchargement d’un rapport*

## Redimensionnement d’un rapport {#resizeareport}

Vous pouvez redimensionner vos rapports en 1×1 (moyenne) et 1×2 (grande) tailles. Cela vous donne un meilleur immobilier pour afficher vos rapports. Vous pouvez également facilement effectuer un panoramique et un zoom sur ces rapports.

## Filtres {#filters}

Les filtres apparaissent dans **[!UICONTROL Ajouter]** la boîte de dialogue rapport située dans la partie inférieure de l’écran, en fonction des types de rapports choisis. Certains des filtres importants sont mentionnés ci-dessous.

**Responsable** Vous pouvez choisir l’un des responsables en fonction de la hiérarchie. Pour certains responsables, il peut y avoir des responsables subordonnés et plusieurs employés relevant de chaque responsable subordonné.

**Profil** Choisissez la désignation de votre employé. Cela aiderait à consulter les rapports des employés en fonction de leur profil/désignation. Par exemple, informaticien, ingénieur.

**Groupe d’utilisateurs** Choisissez le groupe d’utilisateurs en fonction duquel vous souhaitez filtrer les rapports. Learning Manager récupère les groupes d’utilisateurs définis pour votre compte à partir de la fonctionnalité Utilisateurs.

**Cours** Vous pouvez filtrer votre rapport en fonction de n’importe quel cours en les sélectionnant dans la liste déroulante.

![](assets/sample-report-admin.png)
*Filtrage d’un rapport*

Au-dessus de la légende du graphique, vous pouvez voir une zone de zoom. Placez le curseur dessus, cliquez et faites glisser la barre transversale sur n’importe quelle partie de la zone graphique de la zone de zoom avant pour effectuer un zoom avant.

Les valeurs de l’axe y secondaire s’affichent sous la forme d’une ligne sur les barres du graphique. Par exemple, dans l’exemple ci-dessus, les valeurs d’efficacité s’affichent en grisé sur le graphique.

## Rapports de groupe d’utilisateurs {#user-group-reporting}

Suivez les performances des groupes d’utilisateurs tels que les services, les partenaires externes et les rôles par rapport aux autres groupes d’utilisateurs ou à d’autres objectifs d’apprentissage.

### Groupes d’utilisateurs {#usergroups}

Pour générer des rapports en fonction des groupes d’utilisateurs, choisissez **[!UICONTROL Groupe d’utilisateurs]** dans l’axe des x de la liste déroulante comme illustré dans la capture d’écran ci-dessous.

![](assets/user-group-reports.png)
*Rapports de groupe d’utilisateurs*

Pour choisir un groupe d’utilisateurs, saisissez le nom du groupe. Vous pouvez voir les groupes suggérés qui sont affichés en fonction de la chaîne que vous entrez. Une fois que vous voyez une liste de groupes, choisissez le groupe d’utilisateurs requis.

Vous pouvez également choisir plusieurs groupes d’utilisateurs à l’aide de la recherche par frappe anticipée.

Une fois que vous avez enregistré et généré ce rapport, si vous avez sélectionné plusieurs groupes d’utilisateurs, le rapport est généré avec tous les groupes d’utilisateurs représentés dans un graphique à barres côte à côte sur l’axe des x.

Ce rapport de groupe d’utilisateurs vous permet de comparer les performances d’un service/division/rôle par rapport à l’autre afin d’évaluer leurs acquis en matière d’apprentissage.

### Groupes d’utilisateurs/attributs utilisateur personnalisés {#customusergroupsuserattributes}

Vous pouvez également créer des groupes d’utilisateurs personnalisés à l’aide de la fonctionnalité Ajouter des utilisateurs/groupes d’utilisateurs dans Learning Manager. Après avoir créé les groupes d’utilisateurs, vous pouvez générer des rapports pour ces groupes d’utilisateurs personnalisés à l’aide d’une liste d’attributs comme emplacement, branche.

Dans l’axe des abscisses, choisissez l’option Attribut utilisateur et sélectionnez l’attribut dans le menu **sélectionner** liste déroulante en regard de celui-ci. Pour créer un rapport de groupe d’utilisateurs personnalisé basé sur ces attributs, vous devez également choisir le groupe d’utilisateurs approprié dans le filtre.

## Types de rapports {#typesofreports}

Adobe Learning Manager prend en charge quatre types principaux de rapports tels que l’achèvement, le temps passé, les compétences et l’efficacité. Vous pouvez utiliser les types de rapport suivants pour générer des rapports de plus de 300 variations :

* Statistiques de prestation de cours pour les élèves
* Rapport sur l&#39;efficacité des cours
* Rapport basé sur les compétences de l’élève
* Statistiques d&#39;inscription au programme d&#39;apprentissage pour les élèves
* Temps d’apprentissage passé par les élèves
* Nombre d’élèves
* Certification terminée

## Affichage des rapports {#viewingreports}

Sur la page Rapports, vous pouvez afficher tous les rapports. Vous pouvez réduire chaque rapport en cliquant sur l’icône moins (-) dans le coin supérieur droit de chaque rapport. Cliquez sur l’icône (+) pour afficher à nouveau votre rapport.

## Affichage rapide avec différentes dates {#quickviewwithdifferentdates}

Vous pouvez modifier la plage/valeur de date pour n’importe quel rapport et afficher rapidement un rapport à une date différente sans modifier ni enregistrer le rapport. Cliquez sur l’icône Modifier (comme illustré par une flèche dans l’instantané ci-dessous) en regard de la période, telle que QTD, la dernière année. Pour confirmer la modification, choisissez la nouvelle valeur dans le menu déroulant et cliquez sur la coche. Vous pouvez annuler la modification en cliquant sur la croix (X).

>[!NOTE]
>
>Les valeurs de date que vous utilisez pour afficher le rapport sont temporaires. Cette vue du rapport n’est pas téléchargée lorsque vous sélectionnez l’option de téléchargement. Cette vue est uniquement temporaire.

![](assets/learner-count-report.png)
*Afficher le nombre d’élèves*

## Affichage rapide avec différents responsables {#quickviewwithdifferentmanagers}

Si plusieurs responsables vous rendent des comptes, vous pouvez afficher rapidement les rapports de chaque responsable. Pour afficher un rapport unique pour chaque responsable, choisissez le nom du responsable dans la liste déroulante.

>[!NOTE]
>
>Les valeurs de responsable que vous utilisez pour afficher le rapport sont temporaires. Cette vue du rapport n’est pas téléchargée lorsque vous sélectionnez l’option de téléchargement. Cette vue est uniquement temporaire.

## Afficher les rapports de cours {#viewcoursereports}

Vous pouvez afficher les rapports spécifiques à chaque cours en suivant les étapes ci-dessous :

1. Cliquez sur **[!UICONTROL Afficher les rapports de cours]** dans l&#39;onglet Mes tableaux de bord de la page Rapports.\
   Une boîte de dialogue contextuelle s’affiche. Un champ de saisie de texte apparaît dans lequel vous pouvez saisir le cours requis et les noms de cours suggérés apparaissent dans la liste déroulante. Choisissez le cours dans la liste qui s’affiche.

   ![](assets/view-course-report-300x117.png)

   *Afficher les rapports de cours*

1. Sélectionnez le cours de votre choix dans la liste déroulante et cliquez sur Afficher.
1. Vous êtes redirigé vers la page des résultats du quiz du cours sélectionné pour afficher le rapport spécifique au cours.

**Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner le rapport**

Pour afficher les options déroulantes Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner, cliquez sur la flèche déroulante dans le coin supérieur droit de chaque rapport.

![](assets/edit-options-dashboard-300x126.png)

*Modifier/Déplacer vers le tableau de bord/Créer une copie/Supprimer/Redimensionner les rapports*

**[!UICONTROL Modifier]** Pour revenir aux valeurs initiales lors de la modification des données, cliquez sur Réinitialiser. Cliquez sur Enregistrer après avoir modifié les valeurs.

**[!UICONTROL Déplacer vers le tableau de bord]** Vous pouvez déplacer le rapport actuel vers un autre tableau de bord, qui est choisi dans la liste des tableaux de bord.

**[!UICONTROL Créer une copie]** Vous pouvez copier le rapport dans le même tableau de bord ou dans un autre, qui est choisi dans la liste des tableaux de bord.

**[!UICONTROL Supprimer]** Cliquez sur Supprimer pour supprimer le rapport. Un message d’avertissement/de confirmation s’affiche avant la suppression du rapport.

**[!UICONTROL Redimensionner]** Vous pouvez redimensionner vos rapports en tailles 1×1 (moyenne) et 2×2 (grande).

## Générer et afficher des rapports pour le compte de pairs {#generateandviewreportsforpeeraccount}

En tant qu’administrateur, outre la génération de rapports pour votre compte, vous pouvez également générer et afficher des rapports pour les comptes de pairs que vous avez définis.

Lorsque vous avez établi un compte de pairs avec un autre utilisateur, vous pouvez afficher les rapports de ce compte de pairs à partir de la page **[!UICONTROL Rapports]** page. Lors de la création d’un rapport, le **[!UICONTROL Sélectionner un compte]** champ. Dans la liste déroulante qui répertorie tous les comptes de pairs auxquels vous êtes associé, sélectionnez le compte pour lequel vous souhaitez afficher les rapports partagés.

Lors de la création d’un compte de pairs, si l’option Partager le catalogue n’a pas été sélectionnée, vous ne pouvez pas afficher ce compte de pairs dans cette liste.

![](assets/acc1-jpg.png)
*Gérer les rapports pour le compte de pairs*

1. Sélectionnez l&#39;axe des abscisses et l&#39;axe des ordonnées de ce rapport, puis sélectionnez la date de ce rapport.
1. Notez que dans le champ Filtres, le bouton Catalogues partagés est activé automatiquement. C&#39;est obligatoire. Si l’option Catalogue partagé n’est pas activée, cela signifie que vous ne pouvez pas générer ou afficher de rapports pour le compte de pairs.
1. Dans la liste déroulante sous Catalogue partagé, sélectionnez le catalogue partagé pour lequel vous souhaitez afficher le rapport.
1. Cliquez sur [!UICONTROL **Enregistrer**].

   ![](assets/acc2.png)
   *Sélectionner le catalogue partagé pour le compte de pairs*

1. Après avoir cliqué **[!UICONTROL Enregistrer]**, vous pouvez afficher la représentation graphique de vos rapports dans votre tableau de bord par défaut. À partir de ce tableau de bord, vous pouvez filtrer davantage le rapport par le responsable pour le compte de pairs spécifique.
1. Si vous apportez des modifications au catalogue, ces modifications sont immédiatement répercutées dans les rapports et le tableau de bord générés par l’homologue. Cependant, lorsque l’homologue modifie le catalogue, les modifications n’apparaissent pas automatiquement dans votre tableau de bord.
1. Si vous souhaitez que votre tableau de bord soit mis à jour automatiquement, votre homologue doit vous envoyer une nouvelle demande d’homologue.

   >[!NOTE]
   >
   >Les responsables ne peuvent pas afficher les rapports de pairs.

## Abonnements aux e-mails {#emailsubscriptions}

Vous pouvez obtenir vos rapports préférés dans un e-mail en vous abonnant à eux.

Entrée **[!UICONTROL Rapports]** , cliquez sur  **[!UICONTROL Abonnement]** onglet. La page d’abonnement Rapports s’affiche.

Pour sélectionner le nom du rapport dans la liste déroulante, commencez à saisir le nom du rapport dans le champ Rapports. Choisissez la fréquence du courrier électronique dans la liste déroulante. Vous pouvez ajouter l’objet de l’e-mail et fournir un autre ID d’e-mail.

Vous pouvez modifier et supprimer des abonnements.

## Rapports Excel {#excelreports}

Le **[!UICONTROL Rapports Excel]** permet d’exporter des rapports au format XLS.

Voici les types de rapports disponibles au téléchargement.

* Rapports de cours
* Relevés de notes des élèves
* Rapport Annonces
* Rapport sur les assistances à la tâche
* Piste d’audit de contenu
* Piste d’audit de l’utilisateur
* Rapport de connexion/d’accès
* Transcriptions de ludification

## Relevés de notes des élèves {#learnertranscripts}

Les relevés de notes des élèves dans les rapports Excel affichent les colonnes Crédits requis et Crédits gagnés sous forme de nombres décimaux.

## Rapports de cours {#coursereports}

En tant qu’administrateur, vous pouvez télécharger des rapports pour les cours. Procédez comme suit :

1. Ouvrir **[!UICONTROL Rapports]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Rapports de cours]**.
1. Le **[!UICONTROL Rapport de cours]** s’affiche. Sélectionnez le cours dont vous souhaitez récupérer le rapport et cliquez sur **[!UICONTROL Afficher]**.

   ![](assets/course-reports.png)
   *Rapports de cours*

1. Vous êtes redirigé vers la page du cours. Vous pouvez exporter le score du quiz par utilisateur et par question en fonction de chaque inscription en choisissant le type d’inscription spécifique.
1. Sélectionner **[!UICONTROL Exporter le score du quiz]** pour exporter le rapport. A **[!UICONTROL Génération de la demande de rapport]** s’affiche. Cliquez sur **[!UICONTROL OK]** pour confirmer.

   ![](assets/generating-reportrequest.png)
   *Génération de la demande de rapport*

   >[!NOTE]
   >
   >Le rapport de score du quiz exporté contient les détails du score pour chaque tentative si l’option à tentatives multiples est configurée pour le module.

## Relevés de notes des élèves {#LearnerTranscripts-1}

Adobe Learning Manager permet aux administrateurs d’une organisation de générer des relevés de notes associés aux élèves. Le rapport Relevé de notes de l’élève comporte les éléments suivants :

1. Relevé de notes de l’élève : tableau de bord des activités d’apprentissage
1. Compétence : Tableau de bord des compétences
1. Tableau de bord Conformité

Les relevés de notes des élèves dans les rapports Excel affichent les colonnes Crédits requis et Crédits gagnés sous forme de nombres décimaux.

Pour plus d&#39;informations sur la génération de rapports Relevés de notes des élèves, voir [Relevés de notes des élèves](learner-transcripts.md).

## Rapports des annonces {#announcementsreports}

En tant qu&#39;administrateur, vous pouvez générer un rapport de toutes les annonces que vous envoyez. Le rapport contient des détails sur :

* Type d’annonce
* Nom de l’annonce
* Date d’annonce
* État de l’annonce
* Nom de l’élève

Pour télécharger un rapport, effectuez l’une des étapes suivantes :

1. Ouvrir **[!UICONTROL Rapports]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Rapport Annonces]**. Le **[!UICONTROL Génération de la demande de rapport]** s’ouvre. Cliquez sur OK.
1. [!UICONTROL **Annonce**] > [!UICONTROL **Actions**] > [!UICONTROL **Exporter le rapport**].

   ![](assets/announcements.png)
   *Rapport Annonces*

1. Vous pouvez extraire un rapport pour une annonce spécifique en cliquant sur Exporter le rapport sous l’icône des paramètres.

   ![](assets/announcements-specific-report.png)
   *Rapport pour des annonces spécifiques*

## Rapport sur les assistances à la tâche {#jobaidsreport}

Les assistances à la tâche sont du contenu de formation auquel un élève peut accéder sans s&#39;inscrire à un objet d&#39;apprentissage spécifique comme un cours ou un programme d&#39;apprentissage. Les administrateurs peuvent extraire et télécharger le rapport Assistances à la tâche.

Le rapport extrait comprend des informations sur les éléments suivants :

* Nom
* Type d’assistance à la tâche
* Etat de l&#39;assistance à la tâche (publiée ou retirée)
* Date d’inscription
* Date d’achèvement
* Date de téléchargement
* Nom de l’élève
* Nom du responsable
* Créé par

Pour télécharger un rapport, effectuez l’une des opérations suivantes :

* Ouvrir  **[!UICONTROL Rapports]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Rapports d’assistance à la tâche]**. Le **[!UICONTROL Génération de la demande de rapport]** s’affiche. Cliquez sur **[!UICONTROL Ok]**.
* Ouvrir **[!UICONTROL Assistance à la tâche]** > **[!UICONTROL Actions]** > **[!UICONTROL Exporter le rapport]**.

![](assets/job-aids.png)
*Rapport Assistances à la tâche*

* Vous pouvez également extraire un rapport pour une assistance à la tâche spécifique en cliquant sur **[!UICONTROL Exporter le rapport]** sous l’icône paramètres.

![](assets/job-aid-specific-download.png)
*Rapport pour assistance à la tâche spécifique*

### Rapport sur les assistances à la tâche

Après **[!UICONTROL Rapport sur les assistances à la tâche]** deux options s’affichent dans la liste :

![rapport sur les assistances à la tâche](assets/job-aids-new.png)
*Télécharger le rapport d&#39;inscription des utilisateurs des assistances à la tâche*

**Toutes les assistances à la tâche**: si le nombre d&#39;assistances à la tâche dans le compte est inférieur à 10 millions, le rapport généré contiendra les informations d&#39;inscription de toutes les assistances à la tâche. Il s’agira de la sélection par défaut. Si le nombre de lignes dépasse 10 millions, une erreur s&#39;affiche et vous devez sélectionner manuellement les assistances à la tâche requises.

**Assistances à la tâche sélectionnées**: si vous sélectionnez cette option, vous pouvez saisir les assistances à la tâche pour lesquelles vous souhaitez générer le rapport. Vous pouvez sélectionner jusqu&#39;à 10 assistances à la tâche. Adobe Learning Manager vérifie si le nombre d’assistances à la tâche dépasse 10 millions.

![inscription au rapport d&#39;assistances à la tâche](assets/job-aids-2-new.png)
*Sélectionner une assistance à la tâche*

**Rapport sur les assistances à la tâche**

Si vous sélectionnez cette option, les détails de toutes les assistances à la tâche présentes dans le système, ainsi que leurs métadonnées et leur formation, sont téléchargés.

Le rapport téléchargé se compose des champs suivants :

* Nom de l’assistance à la tâche
* Langue(s)
* ID
* Type
* Durée (minutes)
* État
* Date de publication (fuseau horaire UTC)
* Créé par nom
* Créé Par E-Mail
* Créé par ID utilisateur unique
* Catalogue(s)
* Parcours d’apprentissage
* Cours(s)
* Balise(s)
* Compétence(s)

**Rapport d&#39;inscription des utilisateurs des assistances à la tâche**

Le rapport d’inscription contient des détails sur l’inscription des utilisateurs et d’autres informations.

Le rapport téléchargé se compose des champs suivants :

* Nom de l’assistance à la tâche
* Type
* État
* Date d’inscription (fuseau horaire UTC)
* Date de fin (fuseau horaire UTC)
* Date de téléchargement (fuseau horaire UTC)
* Nom de l’élève
* E-mail
* ID utilisateur unique
* Nom du responsable
* Adresse e-mail du responsable
* ID unique de l’utilisateur responsable
* Attribué par nom
* Attribué par e-mail
* Attribué par ID unique de l’utilisateur
* Créé par nom
* Créé par e-mail
* Créé par ID utilisateur unique
* Code de tâche
* Nouveau champ
* Profil

### Rapports de journal d’audit de contenu {#contentaudittrailreports}

Utilisez la commande **[!UICONTROL Piste d’audit de contenu]** génération d&#39;un rapport pour générer un rapport de toutes les modifications apportées à un cours au cours de sa vie dans le système. Le rapport généré contient les informations suivantes extraites.

* ID de l’objet
* Nom de l’objet
* Type d’objet
* Type de modification
* Description
* ID de l’objet référencé
* Nom de l’objet référencé
* Modifié par nom d’utilisateur
* Modifié par ID utilisateur
* Date de modification (fuseau horaire UTC)

Les informations concernant les métadonnées ne sont pas récupérées dans le rapport généré.

Pour générer un rapport d’audit de piste de cours, procédez comme suit.

1. Sélectionner **[!UICONTROL Signaler]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Piste d’audit du cours]**. Le **[!UICONTROL Piste d’audit de contenu]** s’affiche.

   ![](assets/course-audit-trial.png)
   *Piste d’audit du cours*

1. Sélectionnez le cours, le programme d’apprentissage et la certification dont vous souhaitez télécharger le rapport. S’ils ne sont pas spécifiés, tous les rapports sont téléchargés par défaut.
1. Sélectionnez une période pour le rapport et cliquez sur **[!UICONTROL Générer]**.
1. Le rapport est généré et vous êtes informé que le rapport d’audit de contenu est prêt. Vous pouvez télécharger le rapport.

## Rapports de journal d’audit d’utilisateur {#useraudittrailreports}

Le journal d’audit des utilisateurs capture le cycle de vie des utilisateurs, des groupes d’utilisateurs et des profils d’auto-inscription. Les ajouts d’utilisateurs, les suppressions et les changements dans le responsable sont tous capturés. La création et la suppression de profils d’auto-inscription sont enregistrées. Vous pouvez également suspendre et reprendre l’auto-inscription.

Vous pouvez ajouter, activer, désactiver, mettre en pause ou reprendre des profils externes, mais aussi ajouter, supprimer, suspendre ou reprendre l’inscription. Les chargements CSV sont également capturés.

1. Sélectionner  **[!UICONTROL Rapport > Rapport Excel > Piste utilisateur]**. La boîte de dialogue Piste d’audit de l’utilisateur s’affiche.
1. La boîte de dialogue Piste d’audit de l’utilisateur s’affiche. Sélectionnez la plage de dates dans le menu déroulant. Vous pouvez choisir de générer le rapport pour la semaine dernière, le mois dernier ou sélectionner une date personnalisée.

   ![](assets/user-audit-trail.png)
   *Piste d’audit de l’utilisateur*

1. Cliquez sur **[!UICONTROL Générer]** pour générer le rapport.

Il y a deux filtres sur le **[!UICONTROL Rapport de piste d’audit d’utilisateur]** boîte de dialogue.

**Filtre de plage de dates :** Choisissez la période pour laquelle vous souhaitez générer le rapport. Il existe trois options :

* La semaine dernière
* Le mois dernier
* Date personnalisée

Filtre Sélectionner des élèves : recherchez un utilisateur ou un groupe d’utilisateurs.

Le rapport exporté contiendra les données des utilisateurs qui répondent aux deux critères de recherche spécifiés.

![](assets/user-audit-trail.png)
*Piste d’audit de l’utilisateur*

>[!NOTE]
>
>Lorsqu’une compétence est affectée ou supprimée, elle peut être suivie pour le rapport d’audit de l’utilisateur, qu’elle soit affectée ou supprimée.

## Rapports de ludification {#gamification}

Les administrateurs peuvent télécharger la transcription de ludification au format CSV. Vous pouvez télécharger le rapport pour un utilisateur individuel ou pour des groupes d’utilisateurs. Le nom d’utilisateur, l’adresse e-mail de l’utilisateur, l’UUID de l’utilisateur, le nombre total de points de l’utilisateur marqués, la répartition des points collectés, le nom des groupes dans lesquels l’utilisateur joue, le nom du responsable et les valeurs des champs actifs sont tous récupérés dans le rapport. Les administrateurs peuvent utiliser ce rapport pour évaluer et comprendre le classement des utilisateurs au niveau de l’organisation ou pour un groupe spécifique.

1. Sélectionnez Rapport > Rapport Excel > Rapport de ludification.

   ![](assets/gamification.png)
   *Rapport de ludification*

1. La boîte de dialogue Transcriptions de ludification s’affiche. Sélectionnez les élèves en utilisant leur nom, profil, groupes d’utilisateurs, ID de messagerie ou UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Boîte de dialogue Transcriptions de ludification*

1. Cliquez sur  **[!UICONTROL Générer]** pour générer le rapport.

   Après avoir généré le rapport d’un élève, vous devez être en mesure d’exporter les informations de niveau actuel et atteint pour tous les utilisateurs (internes, externes ou supprimés) du compte. Vous pouvez également vérifier les dates des niveaux atteints par un élève :

   * Date d’obtention du bronze
   * Date d’obtention de l’argent
   * Gold Achived Date
   * Platinum Date d&#39;obtention

   Ces colonnes contiennent les dates auxquelles le niveau a été atteint pour la toute première fois. La colonne **[!UICONTROL Niveau actuel]** affiche le niveau actuel de l’élève.

   Lorsque l’administrateur réinitialise la ludification, tous les points de l’élève sont réinitialisés en conséquence.

## Rapport d’inscription et de désinscription {#enrollmentandunenrollmentreport}

Les administrateurs et les responsables peuvent extraire un rapport des élèves qui ont été inscrits et désinscrits. En tant qu&#39;administrateur, vous pouvez voir tout élève, administrateur ou responsable inscrit ou désinscrit d&#39;une instance de cours, de programme d&#39;apprentissage ou de certification et exporter le rapport. En tant que responsable, vous ne pouvez récupérer qu’un rapport des membres de votre équipe. En tant que responsable, vous ne pouvez pas voir les élèves supprimés ou votre propre nom dans l’application du responsable en tant qu’élève inscrit ou non inscrit.

Pour télécharger un rapport, procédez comme suit : Ouvrez le  **[!UICONTROL Cours/ Programme d’apprentissage/ Certification]** > **[!UICONTROL Élèves]** > **[!UICONTROL Action]** > **[!UICONTROL Exporter le rapport]**.

![](assets/unenrollment.png)
*Rapport de désinscription*

## Rapport de commentaires {#feedback-report}

En tant qu’administrateur, vous pouvez désormais récupérer les retours d’informations de l’élève (L1) et du responsable (L3) pour les formations sélectionnées pendant une période spécifiée.

Vous pouvez exporter les données à partir de l’interface utilisateur ou via le connecteur PowerBI pour une analyse plus approfondie.

Les rapports de retour d&#39;informations L1 et L3 offrent la possibilité de télécharger un rapport de retour d&#39;informations consolidé pour les réponses L1 et L3 des formations sélectionnées pour un **d&#39;un an** ou jusqu’à 10 formations sélectionnées pour une période donnée.

Connectez-vous en tant qu’administrateur, puis cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]**, puis, dans la liste des rapports, cliquez sur **[!UICONTROL Rapport de commentaires]**.

![](assets/download-feedbackreport.png)
*Télécharger le rapport de commentaires*

En cliquant sur Télécharger après avoir sélectionné les filtres, vous recevrez une notification pour télécharger le rapport au format CSV.

Le rapport téléchargé contiendra des détails tels que le nom et le type de la formation, le nom de l’instance, le nom et l’adresse e-mail de l’élève, le type de retour d’informations : L1 ou L3, les dates du retour d’informations envoyé pour les nouvelles données.

Pour les données existantes avant cette mise en œuvre de la fonctionnalité, la date d’achèvement de l’objet d’apprentissage sera affichée, la date d’achèvement de l’objet d’apprentissage, la question de retour d’informations L1 Texte réel individualisé et le texte de la salle de classe dans différentes colonnes, les réponses respectives du retour d’informations L1, le nom et l’adresse e-mail du responsable, la valeur du retour d’informations L3 et la date de soumission, les champs actifs.

Vous pouvez également exporter les données de l’interface utilisateur ou vers Power BI, qui prend en charge toutes les formations pour n’importe quelle période afin d’effectuer une analyse plus approfondie

## Rapport de formations {#training-report}

Learning Manager prend en charge le rapport de formation, qui permet aux administrateurs de télécharger les détails de la formation et les métadonnées associées, notamment l’auteur, la date de publication, les compétences, les étiquettes de catalogue, etc.

Dans l’application d’administration, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL Rapport de formations]**.

Vous pouvez télécharger des rapports pour les éléments suivants :

* Formations sélectionnées (10 maximum) : sélectionne une ou plusieurs formations (jusqu’à 10) dans n’importe quel catalogue
* Formations dans les catalogues sélectionnés (5 maximum) : (la sélection du catalogue contiendra jusqu’à cinq catalogues)
* Toutes les formations : (toutes les formations dans le compte)

![](assets/download-trainingreport.png)
*Télécharger le rapport de formation*

Dans la section Options avancées, les options suivantes sont disponibles :

* Inclure les mappages de cours dans le programme d’apprentissage et la certification
* Inclure les informations au niveau du module

Après avoir sélectionné les filtres et cliqué sur Télécharger, vous recevrez une notification pour télécharger le rapport au format CSV.

Le rapport contiendra les champs suivants :

*Nom du catalogue, Type de formation, ID de formation, ID unique de formation, Nom de la formation, Sous-formations, Modules, Durée de la formation ou du module, Format, État de la formation, Compétences, Auteur, Date de la dernière publication, Date du dernier achèvement, Nombre d’inscriptions des instructeurs, Nombre de cours démarrés, Nombre d’achèvements, Score L1 moyen, Score L2 moyen, Score L3 moyen, Réponses L1 reçues, Réponses L2 reçues, Réponses L3 reçues, Étiquettes de catalogue et balises.*

![](assets/more-options.png)
*Options supplémentaires*

## Rapport récapitulatif de la session

Le rapport récapitulatif de la session contient toutes les sessions prévues pour un élève à une date spécifiée.

Cela permet à l’administrateur d’exporter tous les détails des sessions Virtuelle et Salle de classe incluses dans la période donnée. L’administrateur peut également exporter le rapport de session en ce qui concerne des formations ou des instructeurs spécifiques.

Cela aidera également l&#39;administrateur à comprendre les sessions planifiées sur une base mensuelle et à identifier le calendrier des instructeurs et les sessions déjà dispensées.

En tant qu’administrateur, cliquez sur **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapport récapitulatif de la session]**.

Dans la boîte de dialogue qui suit, choisissez la période, ainsi que la formation ou l’instructeur pour obtenir un résumé.

![](assets/session-summary-report.png)
*Rapport récapitulatif de la session*

Le fichier csv téléchargé contient les champs suivants :

* Date et heure de début
* Date et heure de fin

* Nom du module
* Durée de la session (en minutes)
* Nombre de places
* Emplacement
* Nom de l’instance

* Nom du cours
* ID du cours
* Nom de l’instructeur
* E-mail de l’instructeur
* Nombre d’inscriptions

* Type de session
* Limite de liste d’attente
* Nombre de listes d’attente
* E-mails des utilisateurs de la liste d’attente

## Rapport d’utilisation de l’instructeur

Ce rapport capture le temps (en minutes) passé quotidiennement par un instructeur à enseigner des sessions attribuées. Le rapport peut être téléchargé pendant une période de trois mois à compter de la date de début sélectionnée.

Pour télécharger le rapport, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapport d’utilisation de l’instructeur]**.

Sélectionnez un ou plusieurs instructeurs et la plage de dates.

![Télécharger le rapport d’utilisation de l’instructeur](assets/utilization-report.png)
*Télécharger le rapport d’utilisation de l’instructeur*

Le rapport téléchargé contient les champs suivants :

* Nom de l’instructeur
* ID de l’instructeur
* Niveau de compétence
* Dates sous forme de colonnes. Si l’instructeur est utilisé à une date donnée, le nombre de sessions est indiqué. Si l&#39;instructeur n&#39;est pas utilisé un jour, la valeur affiche zéro.

Le rapport contient des enregistrements pour trois mois à partir du mois sélectionné.

Pour récupérer les enregistrements de tous les instructeurs, laissez le champ Instructeur vide.

En outre, un administrateur personnalisé autorisé à générer des rapports peut récupérer ce rapport.

## Rapport de piste d’audit d’utilisateur

Ce rapport capture des informations sur les élèves qui ont changé d&#39;instance, de « de l&#39;instance » à « vers l&#39;instance », qui ont changé d&#39;heure, de date, etc.

Sélectionnez les élèves ou un groupe d’utilisateurs.

Pour télécharger le rapport, cliquez sur **[!UICONTROL Rapports]** > **[!UICONTROL Rapports personnalisés]** > **[!UICONTROL Rapport de piste d’audit d’utilisateur]**.

![Télécharger le rapport de piste d’audit de l’utilisateur](assets/user-audit-report.png)

*Télécharger le rapport de piste d’audit de l’utilisateur*

## Rapport sur le plan d’apprentissage

Ce rapport contient des détails sur tous les plans d’apprentissage d’un compte, par exemple, les groupes d’utilisateurs associés, le statut et les informations de déclenchement.

Le rapport contient les éléments suivants :

* Nom du plan d’apprentissage
* Type (se produit lorsque)
* Formation (terminée)
* Compétence (acquise)
* Date (le)
* Action
* Statut, créé par
* Date de création
* Date de la dernière modification
* Groupe d’utilisateurs (s’applique à)
* Groupe d’utilisateurs (ajouter à)
* S’inscrire après
* Type(s) d’élément d’apprentissage
* Elément(s) d’apprentissage
* Instance(s) d’élément d’apprentissage
* Élément d’apprentissage
* Date d’achèvement
* Rappel d’élément d’apprentissage
* Scope-Catalog
* Scope-Usergroup

## Foire aux questions {#frequentlyaskedquestions}

+++Comment partager un tableau de bord personnalisé avec un responsable ?

Lors de la création d’un tableau de bord, saisissez le nom et la description. Pour partager avec des responsables, saisissez le nom du responsable dans le champ **[!UICONTROL Partager avec]** champ.

![](assets/share-dashboard-manager.png)
*Partage d’un tableau de bord*
+++
