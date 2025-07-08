---
description: Manuel de référence pour les administrateurs d’intégration qui souhaitent migrer un LMS vers un LMS Adobe Learning Manager.
jcr-language: en_us
title: Manuel de migration
exl-id: bfdd5cd8-dc5c-4de3-8970-6524fed042a8
source-git-commit: b128a2adb1d0655078d79b6d46c00612f4ddb996
workflow-type: tm+mt
source-wordcount: '3617'
ht-degree: 73%

---

# Manuel de migration

Manuel de référence pour les administrateurs d’intégration qui souhaitent migrer leur système LMS vers le LMS Learning Manager.

<!-- ## Overview {#overview} -->

## Scénario d’utilisation {#usagescenario}

En règle générale, les grandes entreprises disposent de leur propre LMS en interne ou d’un système de gestion de l’apprentissage provenant d’un fournisseur externe. Le LMS se compose du contenu de formation de votre entreprise et des données de formation. En tant qu’entreprise, lorsque vous achetez Learning Manager, vous pouvez déplacer le contenu et les données de votre système de gestion de l’apprentissage vers Learning Manager afin de tirer parti des avantages d’un système de gestion de l’apprentissage moderne et intuitif sans perdre les données héritées de votre entreprise.

Learning Manager fournit les outils et spécifications nécessaires à l’administrateur d’intégration de votre entreprise pour installer et exécuter les tâches de migration.

Dès aujourd’hui, vous pouvez contacter l’équipe d’assistance Adobe afin que la fonctionnalité de migration de Learning Manager soit accessible par les administrateurs de votre entreprise. Pour activer la fonction de migration de votre compte, vous pouvez contacter l’équipe d’assistance de Learning Manager.

## Processus de migration {#apidescription}

Les conditions préalables à la migration, les étapes clés impliquées dans le processus de migration, les sprints de migration, les spécifications, les étapes de migration des données et du contenu sont expliquées dans cette section comme suit :

### Conditions préalables {#prerequisites}

L’équipe de Learning Manager attend des administrateurs d’intégration de votre entreprise qu’ils effectuent les tâches suivantes avant l’exécution du processus de migration :

* L’administrateur d’intégration extrait les données et le contenu du LMS en place et transforme les données aux formats de fichiers, tel que défini par Learning Manager.
* Learning Manager ne prend pas en charge l’importation des utilisateurs dans le cadre du processus de migration et attend de l’entreprise qu’elle s’en charge à l’aide de connecteurs. Adobe Systems s’attend à ce que ces derniers soient configurés avant l’exécution du processus de migration. Reportez-vous à l&#39;[Aide des connecteurs Learning Manager](connectors.md) pour plus d&#39;informations.

L’équipe Learning Manager recommande aux administrateurs de tester le processus de migration avec un compte d’évaluation avant de migrer les données et le contenu dans l’environnement de production Learning Manager.

### Etapes clés du processus de migration {#keystepsofmigrationprocess}

Les étapes clés impliquées dans la migration du contenu et des données d’un LMS existant vers Learning Manager sont les suivantes :

1. Le partenaire ou l’administrateur d’intégration évalue les données et le contenu du LMS existant à migrer.
1. L’administrateur d’intégration évalue les outils et spécifications fournis par Learning Manager pour la réception des données et du contenu.
1. L’administrateur d’intégration rédige le code ou procède à l’exportation manuelle des données et du contenu de formation depuis l’ancien LMS à partir de la fonctionnalité fournie par ce dernier.
1. Une fois les données et le contenu de formation disponibles, l’administrateur d’intégration analyse et mappe les données et le contenu pour qu’ils correspondent aux spécifications de migration de Learning Manager.
1. L’administrateur d’intégration utilise les outils fournis par Learning Manager pour migrer dans l’ordre suivant :

   1. Transfert des élèves vers Learning Manager
   1. Transférer le contenu de formation dans Learning Manager et
   1. Transfert des données de formation dans Learning Manager.

L’entreprise peut commencer à utiliser le LMS de Learning Manager avec le contenu hérité.

### Objets concernés par la migration {#scopeofmigrationobjects}

Vous pouvez migrer le contenu uniquement pour les objets d’apprentissage suivants :

* Module
* Badges
* Cours
* Version du module
* Instance du cours
* Module du cours
* Compétences
* Niveau de compétence
* Cours de compétence
* Certification
* Cours de certification
* Validation de certification
* Programme d’apprentissage
* Cours de programme d’apprentissage
* Instance du programme d’apprentissage
* Instance de cours de programme d’apprentissage
* Assistance à la tâche
* Version de l’assistance à la tâche
* Cours sur l’assistance à la tâche
* Compétences de l’assistance à la tâche
* Inscription
* Inscription à une certification
* Inscription à un programme d’apprentissage
* Inscription à l’assistance à la tâche
* Notes de cours de l’utilisateur

### Concepts clés de migration {#keyconceptsofmigration}

Certains des concepts clés du processus de migration de Learning Manager sont expliqués brièvement à titre de référence rapide, comme suit :

**Projet de migration**

Dans Learning Manager, un projet de migration est composé d’un ou plusieurs sprints. Vous pouvez également créer plusieurs projets de migration pour un même compte. Le processus de migration dans Learning Manager débute par la création d’un projet de migration.

**Sprint**

Dans le processus de migration de Learning Manager, un sprint correspond à un ensemble d’éléments de migration que vous souhaitez migrer depuis le LMS existant. Un élément de migration peut être un module de cours, des dossiers d’élèves ou un ensemble de cours. Un sprint peut contenir plusieurs éléments de données d’apprentissage. Vous pouvez exécuter des tâches de migration dans chaque sprint.

**Exécutions de sprints**

Une exécution de sprint correspond au processus de lancement d’une tâche de migration d’un sprint. Vous pouvez l’interrompre à tout moment.

**Réexécutions de sprints**

Vous pouvez réexécuter un sprint de migration à tout moment une fois qu’il a été effectué. Cette situation se produit lorsque vous souhaitez ajouter les données à un élément de sprint et les migrer à nouveau vers l’application ou corriger les erreurs dans les fichiers CSV.

**Spécification de fichier CSV**

Learning Manager vous fournit un ensemble de [spécifications CSV standard](migration-manual.md#main-pars_header_140933605). Il est recommandé de parcourir ces spécifications CSV avant de démarrer le processus de migration. L’administrateur d’intégration de votre organisation peut analyser les formats de données existants et les mapper pour qu’ils correspondent aux éléments de modèle CSV fournis par Learning Manager.

**Balises du projet de migration**

Adobe Systems recommande d’utiliser un ensemble de mots-clés comme balises pour identifier facilement vos projets de migration dans l’application Learning Manager. Ces balises vous permettent d’identifier facilement vos projets en interne dans l’application Learning Manager à tout moment.

**Module sans contenu**

Learning Manager permet de charger un module dépourvu de contenu. Adobe Systems le considère comme un module sans contenu dans Learning Manager. Si vous souhaitez migrer certaines données héritées depuis votre LMS existant sans nécessiter de contenu, vous pouvez charger le fichier module_version.csv sans référence d’URL.

## Spécifications et exemples de fichiers CSV {#csv}

Vous trouverez ci-dessous les spécifications CSV standard que vous pouvez utiliser pour effectuer le mappage avec les données de migration de votre LMS existant. Cliquez sur les fichiers csv-specifications et sample-csvs pour télécharger les fichiers ZIP. Le fichier csv-specifications.zip téléchargé contient sept feuilles Excel. Ces feuilles sont des spécifications contenant des descriptions qui permettent de savoir comment remplir les fichiers .csv. Les fichiers .csv correspondants doivent contenir les données de chaque champ au format requis comme expliqué dans ces fichiers .xlsx.

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>N ° de série</b></p></th>
   <th>
    <p><b>Nom du fichier</b></p></th>
   <th>
    <p><b>Description du contenu</b></p></th>
   <th>
    <p>Notes</p></th>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>module.xlsx</p></td>
   <td>
    <p>Métadonnées pour module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>badge.xlsx</p></td>
   <td>
    <p>Métadonnées pour badge.xlsx</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>course.xlsx</p></td>
   <td>
    <p>Métadonnées pour course.csv</p></td>
   <td>
    <p>Indiquez un seul nom d’auteur pour un cours donné dans la mesure où les noms d’auteurs multiples s’affichent parfois de manière incorrecte dans l’application après la migration. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Métadonnées pour module_version.csv</p></td>
   <td>
    <p>Veillez à fournir le chemin d’accès URL au dossier du compte Box dans lequel vous avez chargé le contenu. </p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>course_instance.xlsx</p></td>
   <td>
    <p>Métadonnées pour course_instance.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>session.xlsx</p></td>
   <td>
    <p>Métadonnées pour session.csv</p></td>
   <td>
    <p>Assurez-vous que chaque entrée du fichier session.csv est associée à au moins un module de salle de classe/salle de classe virtuelle.</p></td>
  </tr>
  <tr>
   <td>
    <p>7</p></td>
   <td>
    <p>course_module.xlsx</p></td>
   <td>
    <p>Métadonnées pour course_module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>8</p></td>
   <td>
    <p>skill.xlsx</p></td>
   <td>
    <p>Métadonnées pour skill.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>9</p></td>
   <td>
    <p>skill_level.xlsx</p></td>
   <td>
    <p>Métadonnées pour skill_level.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>10</p></td>
   <td>
    <p>skill_course.xlsx</p></td>
   <td>
    <p>Métadonnées pour skill_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>11</p></td>
   <td>
    <p>certification.xlsx</p></td>
   <td>
    <p>Métadonnées pour Certification.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>12</p></td>
   <td>
    <p>certification_course.xlsx</p></td>
   <td>
    <p>Métadonnées pour certification_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>13</p></td>
   <td>
    <p>certification_commit.xlsx</p></td>
   <td>
    <p>Métadonnées pour certification_commit.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>14</p></td>
   <td>
    <p>learning_program.xlsx</p></td>
   <td>
    <p>Métadonnées pour learning_program.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>15</p></td>
   <td>
    <p>learning_program_course.xls </p></td>
   <td>
    <p>Métadonnées pour learning_program_course.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>16</p></td>
   <td>
    <p>learning_program_instance.xlsx </p></td>
   <td>
    <p>Métadonnées pour learning_program_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>17</p></td>
   <td>
    <p>learning_program_instance_course_instance.xlsx </p></td>
   <td>
    <p>Métadonnées pour learning_program_instance_course_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>18</p></td>
   <td>
    <p>job_aid.xlsx</p></td>
   <td>
    <p>Métadonnées pour job_aid.csv</p></td>
   <td>
    <p>Chaque job_aid migré nécessite une ou plusieurs versions de job_aid.</p></td>
  </tr>
  <tr>
   <td>
    <p>19</p></td>
   <td>
    <p>Job_aid_version.xlsx</p></td>
   <td>
    <p>Métadonnées pour job_aid_version.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>20</p></td>
   <td>
    <p>job_aid_course.xlsx</p></td>
   <td>
    <p>Métadonnées pour job_aid_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>21</p></td>
   <td>
    <p>job_aid_skills.xlsx</p></td>
   <td>
    <p>Métadonnées pour job_aid_skills.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>22</p></td>
   <td>
    <p>enrollments.xlsx</p></td>
   <td>
    <p>Métadonnées pour enrollments.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>23</p></td>
   <td>
    <p>certification_enrollement.xlsx</p></td>
   <td>
    <p>Métadonnées pour certification_enrollement.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>24</p></td>
   <td>
    <p>learning_program_enrollment.xlsx</p></td>
   <td>
    <p>Métadonnées pour learning_program_enrollment.csv<br><br></p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>25</p></td>
   <td>
    <p>job_aid_enrollment.xlsx</p></td>
   <td>
    <p>Métadonnées pour job_aid_enrollment.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>26</p></td>
   <td>
    <p>user_course_grade.xlsx</p></td>
   <td>
    <p><br>
      Métadonnées pour user_course_grade.csv</p></td>
   <td>
    <p>Fournissez les données de dossiers d’élèves requises dans le fichier .csv même si elles ne sont pas obligatoires. Sans ces informations, même si le fichier .csv est traité pour la migration, l’application Learning Manager peut ne pas refléter de données. Le fichier sample-csvs.zip contient sept fichiers .csv dont la convention d’appellation est similaire à celle indiquée ci-dessus.</p></td>
  </tr>
  <tr>
   <td>
    <p>27</p></td>
   <td>
    <p>user_skill.xlsx</p></td>
   <td>
    <p><br>
      Métadonnées pour user_skill.csv</p></td>
   <td>
    <p> </p></td>
  </tr>
 </tbody>
</table>

Learning Manager prend en charge les valeurs de date et d’heure aux formats UTF 8 et 32 bits uniquement. Vous risquez d’obtenir des erreurs lors de la migration si vous mentionnez la date dans des fichiers CSV avec une date hors limites comme 2038-07-17T08:53:21.000Z ou 1980-04-17T08:13:25.322Z.

* [sample-csvs.zip](assets/sample-csvs.zip)
* [csv_specifications.zip](assets/csv-specifications.zip)

Vous devez tenir compte des dépendances suivantes sur les fichiers CSV lors de l’importation :

* Le fichier module_version.csv dépend du fichier module.csv
* Le fichier course_instance.csv dépend du fichier course.csv
* Le fichier course_module.csv dépend des fichiers course.csv, module.csv et module_version.csv
* Le fichier course_instance.csv dépend du fichier course.csv
* Le fichier session.csv dépend des fichiers course.csv et module.csv
* Le fichier enrollment.csv dépend du fichier course.csv
* Le fichier user_course_grade.csv dépend des fichiers course.csv et module.csv
* skill_course.csv dépend de course.csv
* skill_level.csv dépend de skill.csv
* learning_program_instance.csv dépend de learning_program et learning_program_course.csv
* learning_program_course.csv dépend de learning_program.csv
* learning_program_enrollment.csv dépend de learning_program et learning_program_instance.csv
* learning_program_instance_course_instance.csv dépend de learning_program.csv, learning_program_instance.csv et course_instance.csv
* certification_course.csv dépend de certification.csv et course.csv
* certification_commit.csv dépend de certification.csv et certification_course.csv
* certification_enrollment.csv dépend de certification.csv, certification_course.csv et certification_enrollment.csv

## Procédure de migration {#migrationprocedure}

Avant de commencer la procédure de migration, il est important de noter les points suivants :

* Un compte ne peut contenir qu’un seul projet de migration actif à un moment donné. Un compte ne peut contenir qu’un seul sprint actif dans un projet à un moment donné.
* Vous ne pouvez pas annuler une exécution faisant déjà partie du processus de migration. Vous pouvez néanmoins utiliser l’option Supprimer existante dans chaque fonctionnalité de Learning Manager pour annuler la migration des données et du contenu.
* Dès que le projet de migration démarre, il passe à l’état « Migration en cours ». Pendant la migration, l’administrateur d’intégration est le seul autorisé à se connecter à Learning Manager.

### Création de comptes FTP et Box {#creatingftpandboxaccounts}

La planification de votre projet de migration est très importante. Il est recommandé de diviser vos projets en plusieurs sprints et d’identifier clairement ce que vous souhaitez migrer dans chaque version. Il peut même être judicieux d’effectuer une validation après chaque sprint afin d’être sûr des données migrées dans ce sprint, au lieu de procéder à une grande phase de validation à la fin du projet. Avant de débuter le sprint dans le cadre de votre projet de migration, vous devez télécharger les fichiers CSV des données et du contenu respectivement sur les serveurs FTP et Box. Si vous ne disposez pas de comptes pour FTP et Box personnalisés, vous pouvez les créer.

<!--**Create FTP account**-->

<!--Click **[!UICONTROL Request for CSV FTP folder]**. A pop-up dialog appears prompting you to enter your e-mail id. Go through online instructions and create an FTP account. As soon as you create your account, you can view your migration project and sprint project folders in FTP. 

A sample snapshot of project files and folder of FTP is shown below for your reference. -->

<!--![](assets/exavault-migration-upload-folders.png)-->

**Créer un compte Box**

Créez un dossier de chargement du contenu en procédant comme pour le dossier FTP. Cliquez sur Migration dans le volet de gauche, puis sur Demander le dossier de téléchargement en bas de la page qui s’affiche.

Vous recevrez un courrier électronique depuis Box contenant un lien vers le dossier partagé. Si vous n’avez pas de compte Box, cliquez sur S’inscrire et créez un compte. Les instructions de connexion sont envoyées à l’ID de messagerie de l’administrateur d’intégration.

**Chargement des données (fichiers .csv) vers des dossiers FTP ou Box**

La création d’un compte FTP ou Box est une condition préalable à la création d’un projet de migration. À ce stade, vous pouvez donc créer un projet de migration et un sprint dans l’application Learning Manager.  Reportez-vous à la section **Procédure de migration des données et du contenu** sur cette page pour créer un projet de migration.

Dans le compte FTP ou Box, cliquez sur le nom de dossier de votre projet puis sur le nom du sprint. À l’intérieur du dossier du sprint, vous pouvez télécharger les fichiers de données CSV que vous avez l’intention de migrer. Pour ce faire, cliquez sur le bouton Charger les fichiers en haut du serveur FTP ou Box, puis déposez les fichiers .csv. Un exemple d’instantané après le chargement sur FTP est présenté ci-dessous pour référence.

<!--![](assets/exavault-upload.png)-->

Vous pouvez revenir au projet de migration Learning Manager, cliquer sur **[!UICONTROL Actualiser]** et afficher tous les types de données .csv répertoriés dans votre sprint de migration.

**Charger le contenu de formation vers les dossiers de contenu**

Chargez le contenu de formation de votre LMS existant vers votre compte Box. Si vous avez déjà créé le projet de migration et le sprint, il se peut que le compte Box ait rempli leur champ de nom. Vous pouvez charger le contenu dans le même chemin d’accès. Reportez-vous à la section **Procédure de migration des données et du contenu** sur cette page pour créer un projet de migration.

Vous pouvez glisser et déposer des fichiers de contenu ou cliquez sur **[!UICONTROL Charger]** puis sélectionnez les fichiers depuis votre bureau. Si la taille de fichier du contenu est considérable, il est possible que le chargement des fichiers prenne un certain temps. Selon la taille du fichier, le temps nécessaire au téléchargement des fichiers vers votre compte Box varie.

Un exemple de capture d’écran du compte Box après y avoir téléchargé du contenu est illustré ci-dessous pour référence :

![](assets/box-account.png)

*Fichiers dans le compte Box*

Une fois les fichiers chargés dans votre compte Box, veillez à préciser le chemin d’accès relatif à ce fichier de contenu Box dans le fichier module_version.csv. Vous devez impérativement indiquer le chemin d’accès au contenu du module.

Une fois que vous êtes connecté aux serveurs FTP et Box et que vous avez chargé le contenu, les emplacements des fichiers CSV s’affichent dans Learning Manager comme le montre la capture d’écran ci-dessous.

![](assets/after-setup.jpg)

*Emplacements CSV dans le compte Box*

## Procédure de migration des données et du contenu {#dataandcontentmigrationprocedure}

La procédure de migration des données et du contenu de votre LMS d’entreprise vers Learning Manager est expliquée comme suit :

Consultez les conditions préalables à la migration avant de débuter celle-ci. Reportez-vous à la section [Spécifications CSV et exemples de fichiers CSV](migration-manual.md#main-pars_header_140933605) de cette page et préparez les fichiers CSV pour la migration des données et du contenu.

1. Connectez-vous à l’application Learning Manager en tant qu’administrateur d’intégration et cliquez sur **[!UICONTROL Migration]** dans le volet de gauche.

   La page d’accueil des projets de migration s’affiche. Si votre entreprise a déjà créé des projets de migration, vous pouvez consulter la liste de ceux-ci dans cette page.

1. Cliquez sur **[!UICONTROL Nouveau]** dans le coin supérieur droit de la page pour créer un projet de migration. Vous pouvez également cliquer sur le lien **[!UICONTROL Créer un projet de migration]** pour créer un projet de migration. La page Créer un projet de migration s’affiche.

   Si vous n’avez pas encore créé de dossier FTP, vous serez invité à en créer un dans le compte. Il s’agit d’une étape obligatoire avant de commencer à créer le projet de migration.

   ![](assets/create-project.png)
   *Créer un dossier FTP*

   Fournissez un nom, une balise, un catalogue de cours et une description pour votre projet de migration. Cliquez sur **[!UICONTROL Créer]**.

   Les éléments de données de la migration sont identifiés à l’aide de cette balise de projet de migration. Si vous ne disposez pas de catalogue de cours spécifique, choisissez le catalogue par défaut dans la liste déroulante. Tous les cours que vous migrez à l’aide d’un projet de migration figureront dans le catalogue que vous sélectionnez à ce stade. Si vous ne sélectionnez pas de catalogue, tous les cours migrés seront affichés dans le catalogue par défaut.

1. La page de configuration du sprint s’affiche, comme le montre la capture d’écran suivante. Vous devez créer un sprint dans le cadre de votre projet de migration. Choisissez le nom du sprint et indiquez une brève description de celui-ci. Sélectionnez Oui si vous souhaitez migrer le contenu dans le cadre de ce sprint. Cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/users-modified-sprint.png)
   *Migration de sprint*

   Cochez la case intitulée **Des utilisateurs ont été ajoutés ou modifiés depuis la dernière exécution**, pour synchroniser la liste d&#39;utilisateurs avec l&#39;application Learning Manager. Si vous effectuez une migration du contenu et des données dans l’application Learning Manager, cette étape n’est pas obligatoire. Toutefois, si un laps de temps s’est écoulé entre votre dernière migration de sprint et la plus récente, il est recommandé de synchroniser la liste des utilisateurs. Cette étape permet à la base de données Learning Manager d’être synchronisée avec les utilisateurs de votre LMS.

   Cette étape de synchronisation est conseillée si les fichiers enrollment.csv et user_course_grade.csv sont migrés. Cette étape permet à la base de données de Learning Manager d’être synchronisée avec votre base de données de migration et garantit que tous les utilisateurs dont les dossiers doivent être migrés dans le sprint figurent dans la base de données de migration.

1. Vous pouvez lancer la migration de sprint avec les données et le contenu chargés. Cliquez sur le lien **[!UICONTROL Actualiser]** avant de lancer l&#39;exécution du sprint pour synchroniser le FTP et les dossiers de contenu avec l&#39;application Learning Manager.

   ![](assets/sprint1-filesupload.png)
   *Démarrer la migration du sprint*

   Cliquez sur **[!UICONTROL Démarrer]** dans le coin supérieur droit de la page. Vous pouvez cliquer sur **[!UICONTROL Arrêter]** à tout moment au cours du processus de migration de sprint pour arrêter la migration de sprint.

   L’état de la migration est affiché sur chacun des éléments de données et de contenu du sprint. Vérifiez le nombre d’éléments ayant réussi et échoué dans le cadre de l’exécution du sprint de migration.

   Si vous chargez le contenu du module, assurez-vous que le chemin d’accès au dossier de contenu est fourni dans le fichier module_version.csv. Si vous ne réalisez pas cette étape, des erreurs peuvent survenir au cours de la migration. Par exemple, si vous chargez un module en auto-apprentissage, tel que des vidéos, vous devez spécifier son chemin d’accès URL dans le fichier module_version.csv. Pour le contenu du module d’activité, vous pouvez spécifier le nom d’URL.

   Un exemple de capture d’écran de la boîte de dialogue de progression est fourni ci-dessous pour référence. Comme le montre la capture d’écran, vous pouvez consulter le nombre d’enregistrements traités pour chaque élément de données de migration ainsi que l’état des éléments ayant réussi et échoué. Cliquez sur Télécharger les enregistrements d’erreur à côté des éléments ayant échoué pour télécharger et visionner les journaux d’erreurs. Corrigez les problèmes dans les CSV et téléchargez-les de nouveau sur le serveur FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Afficher la progression du sprint*

   Cliquez sur Liste des sprints dans le volet de gauche pour afficher la liste de tous les sprints d’un projet de migration. Vous pouvez afficher une liste de tous les sprints, le nombre d’exécutions pour chaque sprint, la date de début, la durée et l’état d’achèvement, comme illustré dans l’exemple de capture d’écran ci-dessous.

   ![](assets/sprint-list.png)
   *Afficher la liste des sprints*

1. Après avoir téléchargé les CSV mis à jour les plus récents, vous pouvez cliquer sur Réexécuter dans le coin supérieur droit de la page. La réexécution traite à nouveau tous les éléments de données, en ignorant ceux pour lesquels il n’y a pas de modification. Une fois que vous êtes satisfait de la migration des éléments de données d’un sprint, vous pouvez marquer la migration comme terminée en cliquant sur le bouton situé en haut de la page. Vous pouvez initier un nouveau sprint avec plus d’éléments de données ultérieurement. Une fois qu’un sprint est marqué comme terminé, vous ne pouvez pas le réexécuter. De manière similaire, vous pouvez avoir autant de sprints que vous le souhaitez dans un projet de migration. Une fois que vous êtes satisfait du statut de migration de tous les Sprints, vous pouvez marquer le projet de migration comme terminé en cliquant sur le lien **Marquer le projet comme terminé** sur la page Liste des sprints.

   Avant de marquer le projet de migration comme terminé, vous devez vous assurer que tous ses sprints du projet sont terminés. Une fois que vous avez marqué le projet de migration comme terminé, vous ne pouvez ni revenir pour créer de sprints dans ce projet ni y apporter de modifications. Vous devez créer un autre projet de migration et y ajouter des sprints.

## Vérification de la migration {#registration}

Après avoir migré les données et le contenu de formation depuis l’ancien LMS de votre entreprise, vous pouvez vérifier les données et le contenu importés à l’aide de différentes fonctionnalités liées aux objets de formation. Par exemple, vous pouvez vous connecter à l’application Learning Manager en tant qu’administrateur et vérifier que les données et le contenu des modules et cours importés sont disponibles.

## Mise à jour lors de la migration {#retrofittinginmigration}

Cette fonctionnalité d’intégration vous permet de mettre à jour les données d’historique pour un objet d’apprentissage d’un système de gestion de l’apprentissage vers un cours actif qui est créé dans Learning Manager.

Vous trouverez ci-dessous les spécifications CSV standard que vous pouvez utiliser pour effectuer le mappage avec les données de migration de votre LMS existant. Cliquez sur les fichiers csv-specifications et sample-csvs pour télécharger les fichiers ZIP. Le fichier csv-specifications.zip téléchargé contient quatre feuilles Excel. Ces feuilles sont des spécifications contenant des descriptions qui permettent de savoir comment remplir les fichiers .csv. Les fichiers .csv correspondants doivent contenir les données de chaque champ au format requis comme expliqué dans ces fichiers .xlsx.

1-enrollment.xlsx : contient les descriptions de métadonnées nécessaires pour le fichier retrofit_enrollment.csv.

2-certification_enrollment.xlsx : contient les descriptions de métadonnées nécessaires pour le fichier retrofit_certification_enrollment.csv.

3-learning_program_enrollment.xlsx : contient les descriptions de métadonnées nécessaires pour le fichier retrofit_learning_program_enrollment.csv.

4-user_course_grades.xlsx-contient des descriptions des métadonnées requises pour le fichier retrofit_user_course_grades.csv.
[csv-specifications.zip](assets/csv-specifications.zip)

>[!NOTE]
>
>L’UUID (Universally Unique Id) est également une colonne dans le fichier CSV de migration.


## Résolution des problèmes de migration {#troubleshootingmigrationissues}

[Cliquez ici](../../kb/troubleshooting-migration.md) pour en savoir plus sur la solution de rechange/la résolution des problèmes que rencontrent les administrateurs d’intégration lors de la migration de données et du contenu depuis leur LMS existant vers l’application Learning Manager.

## Conseils pour la gestion des utilisateurs {#usermanagement}

Dans cette rubrique, vous trouverez certains conseils pour comprendre comment les utilisateurs sont considérés et gérés par Learning Manager. Ces concepts vous aideront à mieux gérer les utilisateurs lorsque vous utilisez les fonctionnalités d’importation de CSV, de connecteurs et de migration dans Learning Manager.

## ID Learning Manager {#captivateprimeids}

Learning Manager propose deux types d’ID uniques aux utilisateurs :

* ID d’e-mail
* UUID (ID universel unique)

Learning Manager prend en charge l’UUID pour fournir aux entreprises de la flexibilité dans le contrôle des comptes utilisateurs. En tant qu’administrateur, si vous avez l’UUID des utilisateurs dans un compte, vous pouvez modifier les ID de messagerie des utilisateurs pour ce compte.

**Scénario d’utilisation d’un UUID au sein d’une entreprise**

Imaginez un scénario dans lequel un employé A rejoint une société nommée Learning Manager, en tant que sous-traitant. Pendant la période du contrat, l’entreprise Learning Manager ne peut pas fournir l’ID de messagerie de l’entreprise comme ```A@example.com```, mais peut uniquement prendre en compte le compte de messagerie personnel de l’employé, par exemple, ```A@gmail.com```. Après avoir terminé 6 mois de période contractuelle, si le même employé A rejoint Learning Manager en tant qu’employé à temps plein, Learning Manager peut vouloir modifier son ID de messagerie en ID de messagerie de son entreprise : ```A@example.com```.

Avoir un accès UUID au compte utilisateur sera bénéfique pour la société Learning Manager dans le scénario mentionné ci-dessus. L’entreprise Learning Manager peut facilement remplacer l’ID de messagerie personnel de l’employé A par un ID de messagerie officiel. Les dossiers de l’employé pertinents pour ce compte ne sont pas affectés par cette modification.

## Identification d’utilisateur unique {#singleuseridentification}

Learning Manager identifie et mémorise la manière dont un utilisateur unique est ajouté, par exemple par auto-inscription, en utilisant le chargement CSV ou l’interface utilisateur ou encore au moyen de l’API.

* Si un utilisateur unique est ajouté à l’aide de l’interface utilisateur (IU) ou via l’API, vous pouvez supprimer ce type d’utilisateurs uniques en utilisant l’IU ou via l’API.
* Vous pouvez mettre à jour les utilisateurs uniques à l’aide du processus de chargement CSV mais retenez que ces utilisateurs uniques sont traités comme des utilisateurs CSV et que les flux de travaux CSV s’appliquent à ces utilisateurs.

## Affectation du rôle de gestionnaire {#assigningmanagerrole}

Vous ne pouvez pas affecter un rôle de gestionnaire directement à un utilisateur dans Learning Manager. Un utilisateur X ne peut devenir un gestionnaire Learning Manager que lorsque vous définissez un attribut de gestionnaire de n’importe quel utilisateur (par exemple, Y) dans ce compte comme X.

Dans un scénario où X est le gestionnaire des utilisateurs, par exemple A, B et C, si X quitte l’entreprise, vous devez vous assurer que l’attribut de gestionnaire de A, B et C est défini en fonction du nouveau gestionnaire. Vous pouvez également définir temporairement l’attribut de gestionnaire de ces utilisateurs sur ROOT et lui affecter ultérieurement le nouveau nom du gestionnaire.

Pour plus d’informations sur cette rubrique, reportez-vous au contenu de l’aide suivant :

* [FAQ sur le chargement des fichiers CSV](/help/migrated/administrators/feature-summary/add-users-user-groups.md#bulk-upload-internal-users/)
* [Fonctionnalité d’aide pour l’ajout d’utilisateurs](/help/migrated/administrators/feature-summary/add-users-user-groups.md)
