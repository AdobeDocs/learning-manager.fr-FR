---
description: Manuel de référence pour les administrateurs d’intégration qui souhaitent migrer un LMS existant vers le LMS Learning Manager
jcr-language: en_us
title: Manuel de migration
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '3705'
ht-degree: 0%

---



# Manuel de migration

Manuel de référence pour les administrateurs d’intégration qui souhaitent migrer un LMS existant vers le LMS Learning Manager

## Présentation {#overview}

<table>
 <tbody>
  <tr>
   <td><img src="assets/migration.jpg"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> est une solution de gestion de l’apprentissage en libre-service, centrée sur l’élève et hébergée sur le cloud. Adobe permet aux entreprises disposant des systèmes de gestion de l’apprentissage (LMS) de migrer les données et le contenu de formation de leur organisation vers l’application LMS de Learning Manager. </p></td>
  </tr>
 </tbody>
</table>

### Scénario d’utilisation {#usagescenario}

En général, les grandes entreprises disposent de leur système de gestion de l’apprentissage (LMS) interne ou de tout système de gestion de l’apprentissage fourni par un fournisseur. Le LMS se compose du contenu de formation de votre entreprise et des données de formation. En tant qu’entreprise, lorsque vous achetez Learning Manager, vous pouvez déplacer le contenu et les données de votre système de gestion de l’apprentissage vers Learning Manager afin de tirer parti des avantages d’un système de gestion de l’apprentissage moderne et intuitif sans perdre les données héritées de votre entreprise.

Learning Manager fournit les outils et spécifications nécessaires à l’administrateur d’intégration de votre organisation pour installer et effectuer les tâches de migration.

À partir d’aujourd’hui, la fonctionnalité de migration de Learning Manager est accessible aux administrateurs d’une organisation en contactant l’équipe d’assistance de l’Adobe. Pour activer la fonctionnalité de migration de votre compte, vous pouvez contacter l’équipe d’assistance d’Adobe Learning Manager.

## Processus de migration {#apidescription}

Les conditions préalables à la migration, les étapes clés impliquées dans le processus de migration, les sprints de migration, les spécifications, les étapes de migration des données et du contenu sont expliquées dans cette section comme suit :

### Conditions préalables {#prerequisites}

L’équipe de Learning Manager s’attend à ce que les tâches suivantes soient effectuées par les administrateurs d’intégration de votre organisation avant d’entreprendre le processus de migration :

* L’administrateur d’intégration extrait les données et le contenu du LMS en place et transforme les données aux formats de fichiers définis par Learning Manager.
* Learning Manager ne prend pas en charge l’importation d’utilisateurs dans le cadre du processus de migration et s’attend à ce que l’organisation importe les utilisateurs à l’aide de connecteurs. Adobe Systems s’attend à ce que ces connecteurs soient configurés avant le processus de migration. Reportez-vous à [Aide des connecteurs Learning Manager](connectors.md) pour plus d’informations.

Learning Manager recommande aux administrateurs de tester le processus de migration dans un compte d’évaluation avant de migrer les données et le contenu dans l’environnement de production Learning Manager.

### Étapes clés du processus de migration {#keystepsofmigrationprocess}

Les étapes clés impliquées dans la migration du contenu et des données d’un LMS existant vers Learning Manager sont les suivantes :

1. L’administrateur d’intégration ou le partenaire évalue les données et le contenu du LMS existant qui doivent être migrés.
1. L’administrateur d’intégration évalue les outils et spécifications fournis par Learning Manager pour l’ingestion de données et de contenu.
1. L’administrateur d’intégration écrit du code ou effectue un travail manuel pour exporter les données et le contenu de formation de l’ancien LMS en fonction des fonctionnalités fournies par l’ancien LMS.
1. Une fois les données et le contenu de formation disponibles, l’administrateur d’intégration analyse et mappe les données et le contenu pour qu’ils correspondent aux spécifications de migration de Learning Manager.
1. L’administrateur d’intégration utilise les outils fournis par Learning Manager pour migrer dans l’ordre suivant :

   1. Transfert des élèves vers Learning Manager
   1. Transférer le contenu de formation dans Learning Manager et
   1. Enfin, transférez les données de formation dans Learning Manager.

L’organisation peut commencer à utiliser le LMS Learning Manager avec le contenu hérité.

### Portée des objets de migration {#scopeofmigrationobjects}

Vous pouvez migrer le contenu uniquement pour les objets d’apprentissage suivants :

* Module
* Badges
* Cours
* Version du module
* Instance de cours
* Module Cours
* Compétences
* Niveau de compétence
* Cours de compétences
* Certification
* Cours de certification
* Validation de certification
* Programme d’apprentissage
* Cours du programme d’apprentissage
* Instance de programme d&#39;apprentissage
* Instance de cours du programme d&#39;apprentissage
* Assistance à la tâche
* Version de l’assistance à la tâche
* Cours d’assistance à la tâche
* Compétences d’assistance à la tâche
* Inscription
* Inscription à la certification
* Inscription au programme d&#39;apprentissage
* Inscription à l’assistance à la tâche
* Notes de cours de l’utilisateur



### Principaux concepts de migration {#keyconceptsofmigration}

Certains des concepts clés du processus de migration de Learning Manager sont expliqués brièvement à titre de référence rapide, comme suit :

**Projet de migration**

Dans Learning Manager, un projet de migration se compose d’un ou plusieurs sprints. Vous pouvez également avoir plusieurs projets de migration pour votre compte. Le processus de migration dans Learning Manager commence par la création d’un projet de migration.

**Sprint**

Un sprint, dans le processus de migration de Learning Manager, définit un ensemble d’éléments de migration que vous avez choisi de migrer à partir du LMS existant. Un élément de migration peut être un module de cours, des enregistrements d’élève ou un ensemble de cours. Un sprint peut contenir plusieurs éléments de données d’apprentissage. Vous pouvez exécuter des tâches de migration dans chaque sprint.

**Exécutions de sprint**

L&#39;exécution du sprint est le processus de démarrage d&#39;un travail de migration du sprint. Vous pouvez arrêter l’exécution du sprint à tout moment au cours d’une exécution.

**Réexécutions de sprint**

Vous pouvez réexécuter un sprint de migration une fois qu’il est terminé à tout moment. Cette situation de réexécution ou de réexécution d’un sprint se produit lorsque vous souhaitez ajouter les données dans un élément sprint et les migrer à nouveau vers l’application ou corriger les erreurs dans les fichiers CSV.

**Spécification CSV**

Learning Manager vous fournit un ensemble de [spécifications CSV standard](migration-manual.md#main-pars_header_140933605). Il est recommandé de parcourir ces spécifications CSV avant de commencer le processus de migration. L’administrateur d’intégration de votre organisation peut analyser les formats de données existants et les mapper pour qu’ils correspondent aux éléments de modèle CSV fournis par Learning Manager.

**Balises de projet de migration**

Adobe Systems vous recommande d’utiliser un ensemble de mots-clés comme balises pour identifier facilement vos projets de migration dans l’application Learning Manager. Ces balises vous permettent d’identifier vos projets en interne dans l’application Learning Manager à tout moment.

**Module sans contenu**

Learning Manager vous permet de charger un module sans contenu. Adobe Systems le considère comme un module sans contenu dans Learning Manager. Si vous souhaitez migrer certaines des données héritées de votre LMS existant sans avoir besoin de contenu, vous pouvez télécharger le fichier module_version.csv sans référence d’URL.

## Spécifications et exemples de fichiers CSV {#csv}

Vous trouverez ci-dessous les spécifications CSV standard que vous pouvez utiliser pour mapper avec vos données de migration LMS existantes. Cliquez sur csv-specifications et sample-csv pour télécharger des fichiers zip. Le fichier csv-specifications.zip téléchargé contient sept fichiers de feuille Excel. Ces fichiers Excel sont des spécifications avec des descriptions pour vous faire comprendre comment remplir les fichiers .csv. Les fichiers .csv correspondants doivent contenir les données de chaque champ au format prescrit, comme expliqué dans ces fichiers .xlsx.

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>Sl.no</b></p></th>
   <th>
    <p><b>Nom de fichier</b></p></th>
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
    <p>Mentionnez un seul nom d'auteur pour un cours donné, car parfois plusieurs noms d'auteurs ne s'affichent pas correctement dans l'application après la migration. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Métadonnées pour module_version.csv</p></td>
   <td>
    <p>Assurez-vous de fournir le chemin d’accès URL du dossier du compte Box dans lequel vous avez chargé le contenu. </p></td>
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
    <p>Assurez-vous que chaque entrée du fichier csv de session est associée à au moins un module Salle de classe/Salle de classe virtuelle</p></td>
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
    <p>Chaque assistance à la tâche migrée doit avoir une ou plusieurs versions de l’assistance à la tâche.</p></td>
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
    <p>Fournissez les données des dossiers d’élève requises dans le fichier .csv même si elles ne sont pas obligatoires. Sans ces informations, même si le fichier .csv est traité pour la migration, l’application Learning Manager peut ne pas refléter de données. le fichier sample-csvs.zip contient sept fichiers .csv dont la convention d’appellation est similaire à celle décrite ci-dessus.</p></td>
  </tr>
 </tbody>
</table>

Learning Manager prend en charge les valeurs de date et d’heure au format UTF 8 et 32 bits uniquement. Vous risquez d’obtenir des erreurs lors de la migration si vous mentionnez une date dans les fichiers CSV dont la date est hors limites comme 2038-07-17T08:53:21.000Z ou 1980-04-17T08:13:25,322Z.
[sample-csvs.zip](assets/sample-csvs.zip) [csv_specifications.zip](assets/csv-specifications.zip)Vous devez tenir compte des dépendances suivantes sur les fichiers CSV lors de l’importation :

* module_version.csv dépend de module.csv
* course_instance.csv dépend de course.csv
* course_module.csv dépend de course.csv, module.csv et module_version.csv
* course_instance.csv dépend de course.csv
* session.csv dépend de course.csv et module.csv
* enrollment.csv dépend de course.csv
* user_course_grade.csv dépend de course.csv et module.csv
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

* Un seul projet de migration peut être actif dans un compte à un moment donné. Dans un projet, un seul sprint peut être actif à un moment donné.
* Vous ne pouvez pas annuler une exécution déjà en cours de migration. Cependant, vous pouvez utiliser l’option de suppression existante dans chaque fonctionnalité de Learning Manager pour annuler toute migration de données ou de contenu.
* Dès que le projet de migration démarre, il passe à l’état « Migration en cours ». Pendant la migration, aucun autre rôle que celui d’administrateur d’intégration ne peut se connecter à Learning Manager.

### Création de comptes FTP et Box {#creatingftpandboxaccounts}

La planification de votre projet de migration est très importante. Il est recommandé de diviser vos projets en plusieurs sprints et d’identifier clairement ce que vous souhaitez migrer dans chaque sprint. Il peut même être judicieux de procéder à une validation après chaque sprint pour être sûr des données migrées dans ce sprint, au lieu d’une phase de validation générale à la fin du projet. Avant de commencer le sprint dans le cadre de votre projet de migration, vous devez télécharger les fichiers CSV de données et de contenu respectivement sur les serveurs FTP et Box. Si vous ne disposez pas de comptes pour FTP et Box personnalisés, vous pouvez les créer.

**Créer un compte FTP**

Cliquez sur **[!UICONTROL Demande du dossier FTP CSV]**. Une boîte de dialogue contextuelle s’affiche et vous invite à saisir votre ID de messagerie. Suivez les instructions en ligne et créez un compte FTP. Dès que vous avez créé votre compte, vous pouvez afficher vos dossiers de projet de migration et de sprint sur FTP.

Un exemple d’instantané de fichiers de projet et de dossier FTP est présenté ci-dessous pour référence.

<!--![](assets/exavault-migration-upload-folders.png)-->

**Créer un compte Box**

Créez le dossier de téléchargement de contenu en suivant un processus similaire à celui suivi pour la création du dossier FTP. Cliquez sur Migration dans le volet de gauche, puis sur Demander un dossier de téléchargement de contenu au bas de la page qui s’affiche.

Vous recevrez un e-mail de Box avec un lien vers le dossier partagé. Si vous n’avez pas de compte Box, cliquez sur S’abonner et créez un compte. Les instructions de connexion sont envoyées à l’ID de messagerie de l’administrateur de l’intégration.

**Téléchargement de données (fichiers .csv) vers des dossiers FTP ou Box**

La création d’un compte FTP ou Box est une condition préalable à la création d’un projet de migration. À ce stade, vous pouvez donc créer un projet de migration et un sprint dans l’application Learning Manager.  Reportez-vous à **Procédure de migration des données et du contenu** dans cette page pour créer un projet de migration.

Dans le compte FTP ou Box, cliquez sur le nom du dossier de votre projet, puis sur le nom du sprint. Dans le dossier sprint, vous pouvez charger les fichiers de données .csv que vous avez l’intention de migrer. Pour ce faire, cliquez sur le bouton Charger les fichiers en haut du serveur FTP ou Box, puis déposez les fichiers .csv. Un exemple d’instantané après le chargement sur FTP est présenté ci-dessous pour référence.

<!--![](assets/exavault-upload.png)-->

Vous pouvez revenir au projet de migration Learning Manager, puis cliquer sur **[!UICONTROL Actualiser]** et afficher tous les types de données .csv répertoriés dans votre sprint de migration.

**Charger le contenu de formation vers les dossiers de contenu**

Chargez le contenu de formation de votre LMS existant sur votre compte Box. Si vous avez déjà créé le projet de migration et le sprint, le compte Box renseigne le projet de migration et le nom du sprint. Vous pouvez télécharger le contenu dans le même chemin d’accès. Reportez-vous à **Procédure de migration des données et du contenu** dans cette page pour créer un projet de migration.

Vous pouvez faire glisser et déposer les fichiers de contenu ou cliquer sur **[!UICONTROL Charger]** et sélectionnez les fichiers à partir de votre bureau. Si la taille de fichier de votre contenu est énorme, vous pouvez rencontrer un certain retard dans le téléchargement des fichiers. Selon la taille du fichier, le temps nécessaire au téléchargement des fichiers vers votre compte Box varie.

Un exemple de capture d’écran du compte Box après y avoir téléchargé du contenu est illustré ci-dessous pour référence :

![](assets/box-account.png)

*Fichiers dans le compte Box*

Une fois les fichiers chargés sur votre compte Box, assurez-vous de mentionner le chemin relatif de ce fichier de contenu Box dans le fichier module_version.csv. Il s&#39;agit d&#39;une étape obligatoire pour vous d&#39;indiquer le chemin du contenu du module.

Une fois que vous vous êtes connecté aux serveurs FTP et Box et que vous avez chargé le contenu, les emplacements des fichiers CSV s’affichent comme illustré dans la capture d’écran ci-dessous dans Learning Manager.

![](assets/after-setup.jpg)

*Emplacements CSV dans le compte Box*

## Procédure de migration des données et du contenu {#dataandcontentmigrationprocedure}

La procédure de migration des données et du contenu de votre LMS d’entreprise vers Learning Manager est expliquée comme suit :

Passez en revue les conditions préalables du processus de migration avant de commencer la migration. Reportez-vous à [Spécifications et exemples de fichiers CSV](migration-manual.md#main-pars_header_140933605) dans cette page et préparez les fichiers CSV pour la migration des données et du contenu.

1. Connectez-vous à l’application Learning Manager en tant qu’administrateur d’intégration et cliquez sur **[!UICONTROL Migration]** dans le volet de gauche.

   La page d’accueil des projets de migration s’affiche. Si votre organisation a déjà créé des projets de migration, vous pouvez afficher la liste de tous les projets de migration sur cette page.

1. Cliquez sur **[!UICONTROL Nouveau]** dans le coin supérieur droit de la page pour créer un projet de migration. Vous pouvez également cliquer sur **[!UICONTROL Créer un projet de migration]** lien sur la page pour créer un projet de migration. La page Créer un projet de migration s’affiche.

   Si vous n’avez pas encore créé de dossier FTP, vous serez invité à en créer un dans le compte. Cette étape est obligatoire avant de commencer à créer un projet de migration.

   ![](assets/create-project.png)
   *Créer un dossier FTP*

   Indiquez le nom du projet, le numéro de projet, le catalogue de cours et la description de votre projet de migration. Cliquez sur **[!UICONTROL Créer]**.

   Vos éléments de données de migration sont identifiés à l’aide de cette balise de projet de migration. Si vous n&#39;avez pas de catalogue de cours spécifique, choisissez le catalogue par défaut dans la liste déroulante. Tous les cours que vous migrez à l’aide d’un projet de migration seront inclus dans le catalogue que vous choisissez à ce stade. Si vous ne choisissez aucun catalogue, tous les cours migrés feront partie du catalogue par défaut.

1. La page de configuration du sprint s’affiche comme illustré dans l’instantané suivant. Vous devez créer un sprint dans le cadre de votre projet de migration. Sélectionnez le nom du sprint et fournissez une brève description du sprint. Vous pouvez choisir Oui si vous souhaitez migrer du contenu dans le cadre de ce sprint. Cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/users-modified-sprint.png)
   *Migration de sprint*

   Cochez la case avec le titre **Des utilisateurs ont été ajoutés ou modifiés depuis la dernière exécution**, pour synchroniser la liste d’utilisateurs avec l’application Learning Manager. Si vous migrez le contenu et les données dans l’application Learning Manager, cette étape n’est pas obligatoire. Toutefois, si un laps de temps s’est écoulé entre votre dernière migration de sprint et la plus récente, il est recommandé de synchroniser la liste des utilisateurs. Cette étape permet à la base de données Learning Manager d’être synchronisée avec les utilisateurs de votre LMS.

   Cette étape de synchronisation est recommandée lors de la migration des fichiers enrollment.csv et user_course_grade.csv. Cette étape permet à la base de données Learning Manager d’être synchronisée avec votre base de données de migration et garantit que tous les utilisateurs dont les enregistrements doivent être migrés dans le sprint sont disponibles dans la base de données de migration.

1. Vous pouvez commencer la migration Sprint avec vos données et votre contenu chargés. Cliquez sur **[!UICONTROL Actualiser]** avant de lancer l’exécution du sprint pour synchroniser le FTP et les dossiers de contenu avec l’application Learning Manager.

   ![](assets/sprint1-filesupload.png)
   *Démarrer la migration du sprint*

   Cliquez sur **[!UICONTROL Début]** dans le coin supérieur droit de la page. Vous pouvez cliquer **[!UICONTROL Arrêter]** à tout moment au cours du processus de migration de sprint, pour interrompre la migration de sprint.

   L’état de migration est affiché sur chacun des éléments de données sprint et de leur contenu. Vérifiez le nombre d’éléments ayant réussi et échoué lors de l’exécution du sprint de migration.

   Si vous chargez le contenu du module, assurez-vous que le chemin du dossier de contenu est fourni dans module_version.csv. Si vous manquez cette étape, vous risquez de subir des erreurs lors de la migration. Par exemple, si vous chargez un contenu de module en auto-apprentissage, tel que des vidéos, vous devez spécifier un chemin d’URL Box relatif dans module_version.csv. Pour le contenu du module Activité, vous pouvez spécifier le nom de l’URL.

   Un exemple de boîte de dialogue de progression est fourni ci-dessous pour référence. Comme le montre l&#39;instantané, vous pouvez afficher le nombre d&#39;enregistrements traités pour chaque élément de données de migration, ainsi que l&#39;état des éléments ayant réussi et échoué. Cliquez sur Télécharger les enregistrements d’erreur correspondant aux éléments en échec pour télécharger et afficher les journaux d’erreurs. Vous pouvez résoudre les problèmes dans le fichier CSV et le charger à nouveau par FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Afficher la progression du sprint*

   Cliquez sur Liste des sprints dans le volet de gauche pour afficher la liste de tous les sprints d’un projet de migration. Vous pouvez afficher une liste de tous les sprints, le nombre d’exécutions pour chaque sprint, la date de début, la durée et l’état d’achèvement, comme illustré dans l’exemple de capture d’écran ci-dessous.

   ![](assets/sprint-list.png)
   *Afficher la liste des sprints*

1. Après avoir chargé les derniers fichiers CSV mis à jour, vous pouvez cliquer sur Réexécuter dans le coin supérieur droit de la page. Réexécutez le traitement de tous les éléments de données une nouvelle fois, en ignorant ceux qui n&#39;ont pas été modifiés. Une fois que vous êtes satisfait de la migration des éléments de données d’un sprint, vous pouvez marquer la migration de printemps comme terminée en cliquant sur le bouton en haut de la page. Vous pourrez commencer un nouveau sprint avec d’autres éléments de données ultérieurement. Une fois qu’un sprint est marqué comme terminé, vous ne pouvez plus le réexécuter. De même, dans un projet de migration, vous pouvez avoir un nombre quelconque de sprints. Une fois que vous êtes satisfait du statut de migration de tous les Sprints, vous pouvez marquer le projet de migration comme terminé en cliquant sur **Marquer le projet comme terminé** sur la page Liste de sprint.

   Avant de marquer le projet de migration comme terminé, vous devez vous assurer que tous les sprints du projet sont terminés. Une fois que vous avez marqué le projet de migration comme terminé, vous ne pouvez plus revenir en arrière et créer des sprints dans ce projet ni apporter des modifications à ce projet. Vous devez créer un autre projet de migration et y ajouter des sprints.

## Vérification de la migration {#registration}

Après avoir migré les données et le contenu d’apprentissage à partir du LMS hérité de votre organisation, vous pouvez vérifier les données et le contenu importés à l’aide de diverses fonctionnalités d’objet d’apprentissage. Par exemple, vous pouvez vous connecter à l’application Learning Manager en tant qu’administrateur et vérifier que les données et le contenu des modules et cours importés sont disponibles.

## Modernisation en cours de migration {#retrofittinginmigration}

Cette fonctionnalité d’intégration vous permet de mettre à niveau les données historiques d’un objet d’apprentissage d’un système de gestion de l’apprentissage vers un cours actif créé dans Learning Manager.

Vous trouverez ci-dessous les spécifications CSV standard que vous pouvez utiliser pour mapper avec vos données de migration LMS existantes. Cliquez sur csv-specifications et sample-csv pour télécharger des fichiers zip. Le fichier csv-specifications.zip téléchargé contient quatre fichiers de feuille Excel. Ces fichiers Excel sont des spécifications avec des descriptions pour vous faire comprendre comment remplir les fichiers .csv. Les fichiers .csv correspondants doivent contenir les données de chaque champ au format prescrit, comme expliqué dans ces fichiers .xlsx.

1-enrollment.xlsx-contient des descriptions des métadonnées requises pour le fichier retrofit_enrollment.csv.

2-certification_enrollment.xlsx-contient des descriptions des métadonnées requises pour le fichier retrofit_certification_enrollment.csv.

3-learning_program_enrollment.xlsx-contient des descriptions des métadonnées requises pour le fichier retrofit_learning_program_enrollment.csv.

4-user_course_grades.xlsx-contient des descriptions des métadonnées requises pour le fichier retrofit_user_course_grades.csv.
[csv-specifications.zip](assets/csv-specifications.zip)

## Dépannage des problèmes de migration {#troubleshootingmigrationissues}

[Cliquez ici](../../kb/troubleshooting-migration.md) pour en savoir plus sur la solution de contournement/la solution aux problèmes rencontrés par les administrateurs d’intégration lors de la migration des données et du contenu de leur LMS existant vers l’application Learning Manager.

## Conseils pour la gestion des utilisateurs {#usermanagement}

Dans cette rubrique, vous trouverez quelques conseils pour comprendre comment les utilisateurs sont considérés et gérés dans Learning Manager. Ces concepts vous aideront à mieux gérer les utilisateurs lors de l’utilisation de l’importation CSV, des connecteurs et des fonctionnalités de migration de Learning Manager.

## ID Learning Manager {#captivateprimeids}

Learning Manager fournit deux types d’ID uniques aux utilisateurs :

* ID d’e-mail
* UUID (Universally Unique Id)

Learning Manager prend en charge l’UUID pour offrir une certaine flexibilité aux organisations dans le contrôle des comptes utilisateur. En tant qu’administrateur, si vous avez l’UUID des utilisateurs dans un compte, vous pouvez modifier les ID de messagerie des utilisateurs pour ce compte.

**Scénario d’utilisation de l’UUID dans une organisation**

Imaginez un scénario dans lequel un employé A rejoint une société nommée Learning Manager, en tant que sous-traitant. Pendant la période du contrat, l’entreprise Learning Manager ne peut pas fournir l’ID de messagerie de l’entreprise comme A@example.com, mais peut uniquement prendre en compte le compte de messagerie personnel de l’employé, par exemple A@gmail.com. Après avoir terminé 6 mois de période contractuelle, si le même employé A rejoint Learning Manager en tant qu’employé à temps plein, Learning Manager peut souhaiter modifier son ID de messagerie en ID de messagerie de son entreprise : A@example.com.

Avoir un accès UUID au compte utilisateur sera bénéfique pour la société Learning Manager dans le scénario mentionné ci-dessus. L’entreprise Learning Manager peut facilement remplacer l’ID de messagerie personnel de l’employé A par un ID de messagerie officiel. Les dossiers de l&#39;employé relatifs à ce compte ne sont pas touchés par ce changement.

## Identification d’un utilisateur unique {#singleuseridentification}

Learning Manager identifie et mémorise la manière dont un utilisateur unique y est ajouté, par exemple en utilisant l’auto-inscription, en utilisant le chargement CSV ou un utilisateur unique ajouté à l’aide de l’interface utilisateur ou au moyen de l’API.

* Si un utilisateur unique est ajouté à l’aide de l’interface utilisateur ou via l’API, vous pouvez supprimer ce type d’utilisateurs uniques à l’aide de l’interface utilisateur ou de l’API.
* Vous pouvez mettre à jour des utilisateurs uniques à l’aide du processus de chargement CSV, mais vous devez vous rappeler que ces utilisateurs uniques sont traités comme les utilisateurs CSV et que les workflows CSV s’appliquent à ces utilisateurs.

## Attribution du rôle de responsable {#assigningmanagerrole}

Vous ne pouvez pas attribuer un rôle de responsable directement à un utilisateur dans Learning Manager. Un utilisateur X ne peut devenir un gestionnaire Learning Manager que lorsque vous définissez un attribut de gestionnaire de n’importe quel utilisateur (par exemple, Y) dans ce compte comme X.

Dans un scénario où X est le responsable des utilisateurs, disons, A, B et C, si X quitte l&#39;organisation, vous devez vous assurer que l&#39;attribut du responsable de A, B et C est défini sur le nouveau responsable. Vous pouvez également définir temporairement l’attribut Responsable de ces utilisateurs comme ROOT et l’attribuer ultérieurement avec le nouveau nom du Responsable.

Pour plus d’informations sur cette rubrique, reportez-vous au contenu de l’aide suivant :

* [FAQ sur le chargement de fichiers CSV](/help/migrated/administrators/add-users-in-bulk.md)
* [Aide sur les fonctionnalités d’ajout d’utilisateurs](/help/migrated/administrators/feature-summary/add-users-user-groups.md)

