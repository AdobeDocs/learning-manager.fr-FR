---
jcr-language: en_us
title: Interpréter le fichier CSV du relevé de notes de l’élève
description: Interpréter le fichier CSV du relevé de notes de l’élève
contentowner: saghosh
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 0%

---



# Interpréter le fichier CSV du relevé de notes de l’élève

Le relevé de notes de l’élève est l’un des rapports les plus utilisés dans Adobe Learning Manager. Le rapport permet d’obtenir presque tous les détails possibles dans un seul rapport au format CSV.

En plus d’être un rapport que les utilisateurs peuvent récupérer pour suivre et analyser les comportements d’apprentissage, le rapport peut également être vu comme le format dans lequel Learning Manager peut être configuré pour exporter des données sur les comportements d’apprentissage vers des applications/systèmes externes.

Un scénario d’entreprise typique consiste à procéder à une exportation périodique du relevé de notes de l’élève pour Learning Manager, à l’analyser pour extraire les élèves qui terminent un programme d’apprentissage important et à passer une commande pour un bon cadeau afin de reconnaître et de récompenser les finalisations en temps opportun.

Un autre cas d’utilisation consiste à ajouter les données de comportement d’apprentissage à un entrepôt de données d’entreprise, où l’on peut souhaiter combiner des données d’apprentissage avec d’autres données d’entreprise pour analyser les corrélations entre le comportement d’apprentissage et d’autres données de processus.

Dans le reste du document, nous décrivons brièvement comment récupérer le relevé de notes de l’élève à partir de Learning Manager, puis nous fournissons les détails sur la façon dont chaque ligne et chaque colonne du rapport doit être interprétée.

Ces informations peuvent être utiles à tout développeur qui a l’intention d’intégrer Learning Manager à d’autres systèmes en traitant les données exportées du relevé de notes de l’élève.

## Récupérer le relevé de notes de l’élève à partir de l’interface utilisateur {#fetchlearnertranscriptfromtheuserinterface}

Dans les paramètres du profil, un élève peut télécharger son relevé de notes. Pour plus d’informations, voir *** [Télécharger le relevé de notes de l’élève](../../administrators/feature-summary/learner-transcripts.md)***.

Les administrateurs peuvent générer des relevés de notes des élèves pour l&#39;ensemble de l&#39;organisation, pour un ensemble spécifique d&#39;utilisateurs ou un ensemble spécifique d&#39;objets d&#39;apprentissage, ou pour un ensemble spécifique d&#39;utilisateurs et d&#39;objets d&#39;apprentissage. Ils peuvent également obtenir tous les enregistrements d’apprentissage pour une durée d’intervalle et indiquer si des informations au niveau du module sont requises (par défaut, les informations au niveau du module sont omises). Pour plus d’informations, voir [***Télécharger les relevés de notes des élèves***](../../administrators/feature-summary/learner-transcripts.md).

<!--Update above link?-->

Les administrateurs peuvent également configurer le système pour envoyer régulièrement par e-mail le relevé de notes de l’élève.

Le relevé de notes de l’élève généré via l’interface utilisateur sera un fichier Excel, qui contient également le « relevé de notes de l’élève ». Dans ce document, nous ferons référence à ce qui est généré au format CSV, un rapport contenant les activités d’apprentissage relatives à l’inscription, au démarrage, à la progression ou à l’achèvement d’un objet d’apprentissage.

## Exporter le relevé de notes de l’élève {#exportlearnertranscript}

Lorsque le relevé de notes de l’élève doit être utilisé par un système externe, Learning Manager fournit une fonctionnalité appelée Exporter les données, où le relevé de notes de l’élève est l’un des types de données qui peuvent être exportés. Comme expliqué dans le préambule, cela est nécessaire pour l’intégration de Learning Manager à un système externe qui doit traiter les données de comportement d’apprentissage ou pour remplir un entrepôt de données d’entreprise avec des données de comportement d’apprentissage.

Pour plus d’informations sur la façon dont les connecteurs qui prennent en charge l’exportation du relevé de notes de l’élève, consultez la section [Section Exporter les données](/help/migrated/integration-admin/feature-summary/connectors.md) dans les connecteurs FTP, Box et PowerBI.

Le but de ces connecteurs est d&#39;exporter périodiquement (une fois en N jours) des données vers une application en aval. Ainsi, ces connecteurs exportent uniquement les données de comportement d’apprentissage incrémentiel à chaque exécution. Notez que ces connecteurs ne permettent pas de récupérer les enregistrements relatifs à un sous-ensemble spécifique d&#39;utilisateurs ou d&#39;objets d&#39;apprentissage. Il s&#39;agit toujours de données concernant tous les utilisateurs et tous les objets d&#39;apprentissage de ce compte.

Dans le cas de PowerBI, le client doit fournir un espace de travail dans lequel Learning Manager peut continuer à exporter ces données de manière incrémentielle dans un jeu de données créé de manière dynamique. Ce connecteur exporte simplement des données, et les clients doivent créer leurs propres rapports/tableaux de bord en fonction de ce jeu de données, le cas échéant.

La section suivante fournit des détails sur la façon dont un système en aval doit interpréter les enregistrements du relevé de notes de l’élève.

## Interpréter le relevé de notes de l’élève {#interpretthelearnertranscript}

Chaque ligne d’un relevé de notes d’un élève correspond à un comportement d’apprentissage capturé dans Learning Manager au cours d’une période spécifique. En règle générale, les connecteurs exportent des « données incrémentielles ». Les lignes représentent donc les activités d&#39;apprentissage qui se sont produites entre la dernière exécution du connecteur et l&#39;exécution en cours.

Bien entendu, les connecteurs vous permettent également de récupérer le relevé de notes de l&#39;élève à la demande. Dans ce cas, l&#39;utilisateur peut spécifier une date de début et la date de fin est supposée être maintenant. En général, il suffit de procéder une première fois, puis de configurer le connecteur pour exporter le relevé de notes incrémentiel de l’élève à un moment spécifique de la journée, une fois dans N jours (la valeur par défaut de N, étant 1).

Définissons maintenant ce que l’on entend par relevé de notes incrémentiel de l’élève

Dans le relevé de notes de l&#39;élève, chaque ligne représente une activité spécifique impliquant un élève spécifique et un objet d&#39;apprentissage spécifique. Nous nous intéressons principalement à l’état d’un élève par rapport à l’objet d’apprentissage : **Inscrit**, **Commencé**, **En cours**, et **Terminé**. Par conséquent, le relevé de notes de l’élève capture également quatre dates correspondantes.

Il existe désormais trois types d’objets d’apprentissage, dans lesquels Learning Manager suit la progression de l’élève. Les données exportées contiennent des informations de progression au niveau du module, qui est l’unité de contenu la plus granulaire qu’un élève peut expérimenter dans Learning Manager.

* **Cours** - une composition d&#39;un ou plusieurs modules
* **Programme d’apprentissage** - une composition d&#39;un ou plusieurs cours
* **Certification** - une composition d&#39;un ou plusieurs cours.

Chaque ligne du relevé de notes de l’élève peut faire référence à l’engagement d’un utilisateur spécifique dans un module, un cours, un programme d’apprentissage ou une certification. Lorsqu&#39;un utilisateur est inscrit à un programme d&#39;apprentissage, le relevé de notes indique que l&#39;utilisateur est e

Les colonnes du relevé de notes de l&#39;élève fournissent diverses informations relatives à chaque activité d&#39;apprentissage, et les tableaux suivants décrivent la sémantique de chaque colonne.

## Relevé de notes de l’élève

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Nom de colonne</b></p></th> 
   <th width="160" valign="bottom"><p><b>Type de valeur</b></p></th> 
   <th width="306" valign="bottom"><p><b>Description</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Nom</b></p></td> 
   <td><p>Jamais vide</p></td> 
   <td><p>Nom de l’élève</p></td> 
  </tr> 
  <tr> 
   <td><p><b>e-mail</b></p></td> 
   <td><p>Jamais vide</p></td> 
   <td><p>Adresse e-mail de l’élève</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Peut être vide</td> 
   <td valign="bottom">Adobe ID de l’élève</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID utilisateur unique</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">ID utilisateur unique de l’élève. Cette colonne est basée sur le paramètre d'arrière-plan activé ou désactivé au niveau du compte.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Nom du plan d’apprentissage</b></p></td> 
   <td valign="middle"><p>Peut être vide</p></td> 
   <td valign="middle">Nom du plan d’apprentissage (le cas échéant) auquel l’utilisateur a été automatiquement affecté.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Programme d'apprentissage/certification/cours</b></p></td> 
   <td valign="middle"><p>Jamais vide</p></td> 
   <td valign="middle"><p>Nom du programme d’apprentissage, de la certification ou du cours</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Type</b></p></td> 
   <td valign="middle">Jamais vide</td> 
   <td valign="middle"><p>Type de l’objet d’apprentissage auquel l’utilisateur a été inscrit.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Cours</b></p></td> 
   <td valign="middle"><p>Peut être vide</p></td> 
   <td valign="middle">Nom du cours auquel l’utilisateur est inscrit. Lorsqu’elle est vide, la ligne représente une certification ou un programme d’apprentissage. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID unique de l’objet d’apprentissage</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Apprentissage de l'ID unique de l'objet d'apprentissage. Cette colonne est basée sur le paramètre activé/désactivé au niveau du compte</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instance  </b></p></td> 
   <td valign="middle">Jamais vide</td> 
   <td valign="middle">Nom de l’instance de l’utilisateur de l’objet d’apprentissage dans laquelle il est inscrit. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Critères de sélection</b></p></td> 
   <td valign="middle"><p>Jamais vide</p></td> 
   <td valign="middle"><p>Base de l’inscription (comment cet élève s’est inscrit à cet objet d’apprentissage).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Module</b></p></td> 
   <td valign="middle"><p>Peut être vide</p></td> 
   <td valign="middle">Nom du module dans les cours. Lorsqu’elle est vide, cette ligne représente un cours, un programme d’apprentissage ou une certification.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Version</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Version du module</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Type de livraison</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Type de livraison du module : eLearning, F2F, VC, Activity.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Langue</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Langue dans laquelle le module est utilisé par l’élève. Cette colonne affiche une valeur uniquement pour les modules eLearning.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Commentaire</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Commentaires ajoutés par l’administrateur, instructeur pour l’élève tout en marquant la présence de l’utilisateur.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Date d’inscription (fuseau horaire Asie/Calcutta)</b></td> 
   <td height="19" width="283">Jamais vide</td> 
   <td height="19" width="728">Date d’inscription par l’élève au type d’objet d’apprentissage.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Date de début (fuseau horaire Asie/Calcutta)</b></td> 
   <td><p>Peut être vide</p></td> 
   <td height="19" width="728">Date à laquelle l’élève a démarré l’objet d’apprentissage. Vide signifie que l’élève n’a pas encore commencé.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Date d’achèvement (fuseau horaire Asie/Calcutta)</b></td> 
   <td><p>Peut être vide</p></td> 
   <td><p>Date à laquelle l’élève l’a terminé. Vide signifie que l’élève ne l’a pas encore terminé.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Échéance (fuseau horaire Asie/Calcutta)</b></td> 
   <td><p>Peut être vide</p></td> 
   <td height="19" width="728">Date à laquelle l’élève doit avoir terminé cet objet d’apprentissage. Vide signifie qu'il n'y a pas de date limite pour cela.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>En retard</b></td> 
   <td height="19" width="283">Oui/Non</td> 
   <td height="19" width="728">Statut retard actuel de l’élève inscrit à l’objet d’apprentissage. Oui/Non</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Statut</b></p></td> 
   <td valign="middle">Non démarré/Terminé/En cours/Non inscrit</td> 
   <td valign="middle">Progression actuelle % de l’élève inscrit à l’objet d’apprentissage.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Progression %</b></p></td> 
   <td valign="middle">Peut être vide</td> 
   <td valign="middle"><p>Indique dans quelle mesure l’élève l’a terminé.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Temps passé (minutes)</b></td> 
   <td height="38" width="283">Peut être vide</td> 
   <td height="38" width="728">Temps d’apprentissage passé par l’élève dans l’objet d’apprentissage, les lignes de niveau module affichent le temps d’apprentissage individuel au niveau du module. Les lignes Cours/Programme/Certificat affichent le temps d’apprentissage total passé.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Grade</b></p></td> 
   <td valign="middle">Réussite/Échec</td> 
   <td valign="middle">Indique la réussite de l’élève. « Réussite », si l’utilisateur a rempli les critères de réussite, « Échec » dans le cas contraire.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Score du quiz</b></p></td> 
   <td valign="middle">Peut être vide</td> 
   <td valign="middle">Dernier score de quiz obtenu par l’élève. Peut être vide si l’élève n’a pas tenté le quiz ou si le contenu ne comporte aucun quiz ou si l’administrateur/instructeur n’a attribué aucun score.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Peut être vide</td> 
   <td height="38" width="728">Le dernier score de quiz maximal possible pour le module. Peut être vide si l’élève n’a pas tenté le quiz ou si le contenu ne comporte aucun quiz.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Peut être vide</td> 
   <td height="38" width="728">Score du quiz le plus élevé obtenu par l’élève sur plusieurs tentatives. Peut être vide si l’élève n’a pas tenté le quiz ou si le contenu ne comporte aucun quiz ou si l’administrateur/instructeur n’a attribué aucun score.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Peut être vide</td> 
   <td height="38" width="728">Le score de quiz maximal le plus élevé possible pour le module. Peut être vide si l’élève n’a pas tenté le quiz ou si le contenu ne comporte aucun quiz.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Tentatives effectuées</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Nombre total de tentatives effectuées par l’élève jusqu’à présent pour ce module.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Nombre maximal de tentatives autorisées</b></td> 
   <td height="19" width="283">Peut être vide</td> 
   <td height="19" width="728">Nombre maximal de tentatives autorisées pour que l’élève utilise le module.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>userState</b></p></td> 
   <td valign="middle">Jamais vide</td> 
   <td valign="middle">État utilisateur de l’élève : Actif/Supprimé/Suspendu.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Champ actif regroupable</b></td> 
   <td height="38" width="283">Peut être vide</td> 
   <td height="38" width="728">Pour chaque champ actif regroupable dans le compte, il y aura une colonne, où le nom de la colonne est celui du champ actif et la valeur sera la valeur spécifique que l’élève a pour ce champ.</td> 
  </tr> 
  <tr> 
   <td><p><b>Nom du responsable</b></p></td> 
   <td><p><i>Peut être vide</i></p></td> 
   <td height="19" width="728">Nom du responsable de l’élève</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Nombre d’inscriptions</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Nombre d’inscriptions de l’élève pour l’objet d’apprentissage. La ligne objet d’apprentissage de niveau le plus élevé affiche une valeur = '1'. Les sous-formations affichent une valeur de 0.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Nombre de démarrages</b></td> 
   <td height="19" width="283">1 ou 0</td> 
   <td height="19" width="728">Nombre de démarrages de l’élève pour l’objet d’apprentissage. La ligne objet d’apprentissage de niveau le plus élevé affiche une valeur = '1'. Les sous-formations affichent une valeur de 0.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Nombre d’achèvements</b></td> 
   <td height="58" width="283">1 ou 0</td> 
   <td height="58" width="728">Nombre d’achèvements de l’élève pour l’objet d’apprentissage. La ligne objet d’apprentissage de niveau le plus élevé affiche une valeur = '1' si l’élève est en attente d’achèvement dans cette formation. Les sous-formations affichent une valeur de 0 même lorsqu’elles sont à l’état En attente. La ligne objet d’apprentissage de niveau le plus élevé affiche une valeur = « 0 » si l’élève a terminé la formation.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Échéance dans N jours</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Cela affiche une valeur de « 1 » ou de « 0 » en fonction de l’échéance de l’instance à laquelle l’élève est inscrit. Cela dépend de la valeur saisie dans la feuille Résumé de l’apprentissage I &gt; champ « Date d’échéance à venir dans ».</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Échéance dans N jours pour l’utilisateur</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Cela affiche une valeur de « 1 » ou de « 0 » en fonction de l’échéance de l’instance à laquelle l’élève est inscrit. Cela dépend de la valeur saisie dans la feuille Résumé de l’apprentissage II &gt; champ « Date d’échéance à venir dans ».</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Nombre de (progression supérieure à N %)</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Cela affiche une valeur de « 1 » ou de « 0 » en fonction de la progression de l’élève dans la formation. Cela dépend de la valeur saisie dans la feuille Résumé de l’apprentissage I &gt; champ « Progression supérieure à ».</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Nombre de (progression supérieure à N %) pour l’utilisateur</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Cela affiche une valeur de « 1 » ou de « 0 » en fonction de la progression de l’élève dans la formation. Cela dépend de la valeur saisie dans la feuille Résumé de l’apprentissage II &gt; champ « Progression supérieure à ».</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">T<b>ID de formation</b></td> 
   <td height="19" width="283">Jamais vide</td> 
   <td height="19" width="728">ID de la formation.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Durée de la formation ou du module (min)</b></td> 
   <td height="20" width="283">Jamais vide</td> 
   <td height="20" width="728">Durée totale de la formation ou du module (min) de l'instance par défaut de la formation.</td> 
  </tr> 
 </tbody> 
</table>

### Résumé de l’apprentissage I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Nom de la colonne<br></th> 
   <th>Type de valeur</th> 
   <th>Description</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Type</td> 
   <td height="19" width="253">Tous, Programme d’apprentissage, Certificat, Cours.</td> 
   <td height="19" width="412">Type d’objet d’apprentissage pour lequel le tableau Résumé de l’apprentissage doit afficher des données.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Champ regroupable (profil)</td> 
   <td height="19" width="253">Jamais vide</td> 
   <td height="19" width="412">Profil pour lequel le tableau résumé de l’apprentissage doit afficher des données.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Nom du responsable</td> 
   <td height="38" width="253">Jamais vide</td> 
   <td height="38" width="412">Nom du responsable dont les données d’engagement d’objet d’apprentissage des subordonnés doivent être affichées dans le tableau de résumé de l’apprentissage.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Libellés de ligne</td> 
   <td height="19" width="253">Jamais vide</td> 
   <td height="19" width="412">Nom de l’objet d’apprentissage avec la liste des élèves inscrits à l’objet d’apprentissage.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Nombre d’élèves inscrits</td> 
   <td height="19" width="253">Jamais vide</td> 
   <td height="19" width="412">Nombre d’élèves inscrits à l’objet d’apprentissage.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Nombre d’élèves ayant commencé</td> 
   <td height="19" width="253">Jamais vide</td> 
   <td height="19" width="412">Nombre d’élèves ayant démarré l’objet d’apprentissage.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Nombre d’élèves ayant terminé</td> 
   <td height="19" width="253">Jamais vide</td> 
   <td height="19" width="412">Nombre d’élèves ayant terminé l’objet d’apprentissage.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Nombre d’élèves ayant progressé &gt;= N %</td> 
   <td height="38" width="253">Jamais vide</td> 
   <td height="38" width="412">Nombre d’élèves ayant progressé &gt;= N % (valeurs).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Nombre d’élèves dont la date d’échéance est dans N jours</td> 
   <td height="39" width="253">Jamais vide</td> 
   <td height="39" width="412">Nombre d’élèves dont la date d’échéance est dans N jours (valeurs).</td> 
  </tr> 
 </tbody> 
</table>

### Résumé de l’apprentissage II

| Nom de la colonne | Type de valeur | Description |
|---|---|---|
| Type | Tous, Programme d’apprentissage, Certificat, Cours. | Type d’objet d’apprentissage pour lequel le tableau Résumé de l’apprentissage doit afficher des données. |
| Champ regroupable (profil) | Jamais vide | Profil pour lequel le tableau résumé de l’apprentissage doit afficher des données. |
| Nom du responsable | Jamais vide | Nom du responsable dont les données d’engagement d’objet d’apprentissage des subordonnés doivent être affichées dans le tableau de résumé de l’apprentissage. |
| Libellés de ligne | Jamais vide | Le nom de l’élève avec la liste des objets d’apprentissage auxquels il est inscrit. |
| Nombre d’objets d’apprentissage inscrits | Jamais vide | Nombre d’objets d’apprentissage auxquels l’élève est inscrit. |
| Nombre d’objets d’apprentissage démarrés | Jamais vide | Nombre d’objets d’apprentissage que l’élève a démarrés. |
| Nombre d’objets d’apprentissage terminés | Jamais vide | Nombre d’objets d’apprentissage terminés par l’élève. |
| Nombre d’objets d’apprentissage ayant progressé >= N % | Jamais vide | Nombre d’objets d’apprentissage dans lesquels l’élève a progressé >= N %. |
| Nombre d’objets d’apprentissage dont la date d’échéance est dans N jours | Jamais vide | Nombre d’objets d’apprentissage dont la date d’échéance est dans N jours. |

### Résumé de la conformité

| Nom de la colonne | Type de valeur | Description |
|---|---|---|
| Type | Tous, Programme d’apprentissage, Certificat, Cours. | Type d’objet d’apprentissage pour lequel le tableau Résumé de l’apprentissage doit afficher des données. |
| Libellés de ligne (colonne de gauche) | Jamais vide | Le nom de l’élève avec la liste des objets d’apprentissage auxquels il est inscrit. |
| Libellés de ligne (colonne de gauche) | Jamais vide | Le nom de l’élève avec la liste des objets d’apprentissage auxquels il est inscrit. |

### Transcription des compétences

| .Nom de la colonne | Type de valeur | Description |
|---|---|---|
| Nom | Jamais vide | Nom de l’élève |
| e-mail | Jamais vide | Adresse e-mail de l’élève |
| Adobe ID | Peut être vide | Adobe ID de l’élève |
| ID utilisateur unique | Peut être vide | ID utilisateur unique de l’élève. Cette colonne est basée sur le paramètre d&#39;arrière-plan activé ou désactivé au niveau du compte. |
| Compétence | Jamais vide | Nom de compétence attribué à l’élève. |
| Niveau de compétence | Jamais vide | Niveau de compétence attribué à l’élève. |
| Crédits requis | Jamais vide | Total des crédits requis par l’élève pour acquérir la compétence. |
| Crédits gagnés | Jamais vide | Total des crédits gagnés par l’élève pour la compétence. |
| Pourcentage d’achèvement | Jamais vide | Pourcentage de progression pour atteindre la compétence. |
| Date d’attribution (fuseau horaire UTC) | Jamais vide | Date à laquelle la compétence a été attribuée à l’élève. |
| Date d’obtention (fuseau horaire UTC) | Jamais vide | Date à laquelle l’élève a acquis la compétence. |
| userState | Jamais vide | État utilisateur de l’élève : Actif/Supprimé/Suspendu. |
| Champ actif regroupable | Peut être vide | Pour chaque champ actif regroupable dans le compte, il y aura une colonne, où le nom de la colonne est celui du champ actif et la valeur sera la valeur spécifique que l’élève a pour ce champ. |
| Nom du responsable | Peut être vide | Nom du responsable de l’élève. |

### I Résumé des compétences

| Nom de la colonne | Type de valeur | Description |
|---|---|---|
| Après | Jamais vide | Nombre d’élèves qui ont acquis la compétence avant le nombre (valeur) de jours saisi qui doit être actualisé. |
| Nom | Tous les noms ou n’importe quel nom d’élève | Nom de l’élève auquel une compétence est affectée. |
| Nom du responsable | Jamais vide | Nom du responsable dont les données d’engagement des compétences des subordonnés doivent être affichées dans le tableau de résumé des compétences. |
| Libellés de ligne | Jamais vide | Nom de la compétence avec la liste des élèves affectés à la compétence. |
| Nombre d’utilisateurs qui doivent avoir cette compétence | Jamais vide | Nombre d’élèves affectés à la compétence. |
| Nombre d’utilisateurs ayant acquis cette compétence | Jamais vide | Nombre d’élèves ayant atteint la compétence. |
| Nombre d’élèves dont la compétence doit être actualisée | Jamais vide | Nombre d’élèves dont la compétence doit être actualisée. |
| Pourcentage de conformité (en fonction des compétences acquises) | Jamais vide | Pourcentage de progression de la compétence assignée. |

### Résumé des compétences II

| Nom de la colonne | Type de valeur | Description |
|---|---|---|
| Après | Jamais vide | Nombre d’élèves qui ont acquis la compétence avant le nombre (valeur) de jours saisi qui doit être actualisé. |
| Compétence | Tout ou n’importe quel nom de compétence | Noms des compétences attribuées aux élèves. |
| Nom du responsable | Jamais vide | Nom du responsable dont les données d’engagement des compétences des subordonnés doivent être affichées dans le tableau de résumé des compétences. |
| Libellés de ligne | Jamais vide | Nom de l’élève avec la liste des compétences attribuées. |
| Nombre de compétences que chaque utilisateur doit posséder | Jamais vide | Nombre de compétences attribuées à l’élève. |
| Nombre de compétences dont dispose chaque utilisateur | Jamais vide | Nombre de compétences acquises par l’élève. |
| Nombre de compétences nécessitant une actualisation | Jamais vide | Nombre d’élèves dont la compétence doit être actualisée. |
| Pourcentage de conformité | Jamais vide | Pourcentage de progression de la compétence assignée. |

* Parfois, les administrateurs peuvent marquer manuellement l’achèvement d’un objet d’apprentissage (en particulier pour les cours en salle de classe) beaucoup après le cours. Dans un tel scénario, si les données d’exportation sont configurées pour exporter LT quotidiennement, la date d’achèvement réelle peut déjà être passée et l’exportation n’obtiendra donc jamais de tels enregistrements d’achèvement qui ont été marqués comme terminés beaucoup après l’événement de la classe. Lorsque cela est détecté, exportez le relevé de notes d’une date de début à une date donnée (à la demande) dans l’interface utilisateur, puis transférez-le vers l’application en aval pour « traitement tardif ». Ce faisant, vous devrez peut-être ignorer les enregistrements qui ont déjà été traités.
* Les tentatives multiples pour un module dépendent de l’activation ou non de cette option pour cet objet d’apprentissage. Lorsque cette option est activée, ce que vous voyez maintenant dans une ligne CSV associée à un module est une tentative. Toutes les tentatives au cours d&#39;une journée ne sont pas signalées. Par conséquent, le nombre total de tentatives peut augmenter de plus d&#39;une. En outre, une tentative peut ne pas nécessairement améliorer un score, et à un moment donné, vous n&#39;obtiendrez que le meilleur score.
