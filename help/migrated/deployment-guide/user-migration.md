---
jcr-language: en_us
title: Guide de déploiement de Learning Manager - Section 2
contentowner: sanm
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2232'
ht-degree: 59%

---



# Guide de déploiement de Learning Manager - Section 2

## Configuration technique {#technicalsetup}

La configuration technique de votre compte Learning Manager est principalement requise pour les utilisateurs en entreprise. Ce document traite de la configuration de l’authentification unique pour votre organisation et de l’intégration de Learning Manager à des connecteurs tiers.

### Configuration de l’authentification unique {#configuresinglesignon}

En tant qu’administrateur système sur l’Admin Console, l’une de vos premières tâches consiste à définir et à configurer un système d’identité à partir duquel vos utilisateurs finaux seront authentifiés. À mesure que votre organisation achète des licences pour Learning Manager, vous devrez les provisionner pour vos utilisateurs finaux. Pour ce faire, vous devrez trouver un moyen d’authentifier ces utilisateurs. Effectuez la procédure suivante pour configurer l’authentification unique pour vos utilisateurs.

1. Dans la page d’accueil de Learning Manager, cliquez sur **[!UICONTROL ** Paramètres **>** Méthodes de connexion **.]**

   ![](assets/configure-sso-step1.png)

1. Selon votre type d&#39;utilisateur, sélectionnez **[!UICONTROL ** Utilisateurs internes **ou** Utilisateurs externes **.]**



1. Dans le champ déroulant **[!UICONTROL **Connexion**]**, sélectionnez **[!UICONTROL ** Authentification unique **.]**

   ![](assets/configure-sso-step3.png)

1. Pour configurer les paramètres d&#39;authentification unique, cliquez sur **[!UICONTROL ** Modifier **.]**

   ![](assets/configure-sso-step4.png)

1. Dans le champ ****[!UICONTROL URL d&#39;authentification initiée par le fournisseur d&#39;identités]****, entrez l&#39;URL d&#39;authentification donnée par votre fournisseur de services.



   ![](assets/configure-sso-step5.png)

1. Cliquez sur **[!UICONTROL **Charger **]**en regard du champ**[!UICONTROL  **Fichier XML de métadonnées IDP **]******et chargez votre fichier XML.
1. Cliquez sur **[!UICONTROL ** Enregistrer **.]**
1. L’authentification SSO est correctement configurée pour votre compte. Vous devriez être en mesure de vous connecter à votre compte Learning Manager à l’aide de l’authentification unique.

   ***L’authentification unique que vous configurez dans Learning Manager doit prendre en charge SAML 2.0.***

## Migration des données utilisateur {#migrationofuserdata}

En tant qu’administrateur, lorsque votre entreprise achète Learning Manager, l’une des étapes cruciales à effectuer est la migration. Il est impératif de déplacer votre contenu de formation existant et vos données utilisateur vers Learning Manager. Le flux de migration suivant vous permet de tirer parti des avantages d’un LMS moderne et intuitif sans perdre les données héritées de votre entreprise.

Learning Manager vous permet de migrer à partir de votre LMS existant via un assistant étape par étape, en sprints itératifs. Vous bénéficiez d’une visibilité complète sur l’état de chaque sprint pour vous assurer que vos élèves ne subissent aucun temps d’arrêt lors de la migration de vos données héritées vers Adobe Learning Manager.

Pour exécuter le flux de migration, vous devez disposer des droits d’administrateur d’intégration. En tant qu’administrateur, vous pouvez soit assumer le rôle d’un administrateur d’intégration, soit affecter ce rôle à un autre utilisateur.

**Nous pouvons utiliser l&#39;aide de Shaleen ici pour créer un visuel.**

1. Prérequis
1. Évaluation du contenu existant et des données utilisateur
1. Exportation et mappage des données à partir du LMS existant
1. Configuration des dossiers FTP et BOX pour la migration
1. Transfert des élèves vers Learning Manager
1. Transfert de contenu d’apprentissage vers Learning Manager
1. Transfert des données restantes vers Learning Manager



### Prérequis {#prerequisite}

Avant de commencer le processus de migration, vous devez effectuer les prérequis suivants :

* Extraction des données et du contenu du système de gestion de l’apprentissage (LMS) en place et transformation des données aux formats de fichier définis par Learning Manager.
* Importation d’utilisateurs à l’aide de connecteurs FTP et BOX. L’administrateur de l’intégration doit s’assurer que les connecteurs sont configurés avant le processus de migration.



***Il est recommandé aux administrateurs d’essayer le processus de migration dans un compte d’évaluation avant de migrer les données et le contenu dans l’environnement de production Learning Manager. ***

### Évaluation et exportation des données {#evaluatingandexportingdata}

L’administrateur de l’intégration doit d’abord examiner les données disponibles dans le LMS actuel. En tant qu’administrateur de l’intégration, vous pouvez migrer uniquement les objets d’apprentissage suivants :

* Module
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
* Inscriptions
* Inscription à une certification
* Inscription à un programme d’apprentissage
* Notes de cours de l’utilisateur



Après avoir évalué vos données existantes, vous devez mapper ces données avec les spécifications CSV standard dans Learning Manager. Téléchargez le fichier d&#39;exemple ***csv-specifications.zip*** suivant qui contient sept feuilles Excel requises pour cette migration. Ces feuilles Excel contiennent des spécifications avec des descriptions pour vous permettre de comprendre comment mapper les données existantes avec les champs dans les fichiers .csv.

<!--
<Download link to the zip file>
-->

Assurez-vous que chaque fichier .csv contient les données de chaque champ au format prescrit :

<table> 
 <tbody> 
  <tr> 
   <th width="7%" valign="top"><p><strong>N°</strong></p></th> 
   <th width="29%" valign="top"><p><strong>Nom de la feuille Excel</strong></p></th> 
   <th width="31%" valign="top"><p><strong>Description du contenu</strong></p></th> 
   <th width="31%" valign="top"><p><strong>Notes</strong></p></th> 
  </tr> 
  <tr> 
   <td><p>1</p></td> 
   <td><p>module.xlsx</p></td> 
   <td><p>Métadonnées pour module.csv</p></td> 
   <td><p> </p></td> 
  </tr> 
  <tr> 
   <td><p>2</p></td> 
   <td><p>course.xlsx</p></td> 
   <td><p>Métadonnées pour course.csv</p></td> 
   <td><p>Indiquez un seul nom d’auteur pour un cours donné dans la mesure où les noms d’auteurs multiples s’affichent parfois de manière incorrecte dans l’application après la migration. </p></td> 
  </tr> 
  <tr> 
   <td><p>3</p></td> 
   <td><p>module_version.xlsx </p></td> 
   <td><p>Métadonnées pour module_version.csv</p></td> 
   <td><p>Veillez à fournir le chemin d’accès URL au dossier du compte Box dans lequel vous avez chargé le contenu. </p></td> 
  </tr> 
  <tr> 
   <td><p>4</p></td> 
   <td><p>course_instance.xlsx</p></td> 
   <td><p>Métadonnées pour course_instance.csv </p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>5</p></td> 
   <td><p>course_module.xlsx</p></td> 
   <td><p>Métadonnées pour course_module.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>6</p></td> 
   <td><p>skill.xlsx</p></td> 
   <td><p>Métadonnées pour skill.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>7</p></td> 
   <td><p>skill_level.xlsx</p></td> 
   <td><p>Métadonnées pour skill_level.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>8</p></td> 
   <td><p>skill_course.xlsx</p></td> 
   <td><p>Métadonnées pour skill_course.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>9</p></td> 
   <td><p>Certification.xlsx</p></td> 
   <td><p>Métadonnées pour Certification.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>10</p></td> 
   <td><p>certification_course.xlsx</p></td> 
   <td><p>Métadonnées pour certification_course.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>11</p></td> 
   <td><p>certification_commit.xlsx</p></td> 
   <td><p>Métadonnées pour certification_commit.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>12</p></td> 
   <td><p>learning_program.xlsx</p></td> 
   <td><p>Métadonnées pour learning_program.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>13</p></td> 
   <td><p>learning_program_course.xls </p></td> 
   <td><p>Métadonnées pour learning_program_course.csv </p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>14</p></td> 
   <td><p>learning_program_instance.xlsx </p></td> 
   <td><p>Métadonnées pour learning_program_instance.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>15</p></td> 
   <td><p>learning_program_instance_course_instance.xlsx </p></td> 
   <td><p>Métadonnées pour learning_program_instance_course_instance.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>16</p></td> 
   <td><p>enrollments.xlsx</p></td> 
   <td><p>Métadonnées pour enrollments.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>17</p></td> 
   <td><p>certification_enrollment.xlsx</p></td> 
   <td><p>Métadonnées pour certification_enrollment.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>18</p></td> 
   <td><p>learning_program_enrollment.xlsx</p></td> 
   <td><p>Métadonnées pour learning_program_enrollment.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>19</p></td> 
   <td><p>User_course_grade.xlsx</p></td> 
   <td><p>Métadonnées pour User_course_grade.csv</p></td> 
   <td><p>Fournissez les données de dossiers d’élèves requises dans le fichier .csv même si elles ne sont pas obligatoires. Sans ces informations, même si le fichier .csv est traité pour la migration, l’application Learning Manager peut ne pas indiquer les données. </p></td> 
  </tr> 
 </tbody> 
</table>

***Learning Manager prend en charge les valeurs de date et d’heure au format UTF 8 et 32 bits uniquement. Vous pouvez obtenir des erreurs lors de la migration si vous spécifiez une date dans des fichiers CSV avec une date hors limites telle que 2038-07-17T08:53:21.000Z ou 1980-04-17T08:13:25.322Z.***

### Dépendances lors de l’importation de données dans des fichiers csv {#dependencieswhileimportingdatatocsvfiles}

Lorsque vous importez les données existantes au format csv standard, tenez compte des dépendances suivantes :

* Le fichier module_version.csv dépend du fichier module.csv
* Le fichier course_instance.csv dépend du fichier course.csv
* Le fichier course_module.csv dépend des fichiers course.csv, module.csv et module_version.csv
* Le fichier course_instance.csv dépend du fichier course.csv
* Le fichier enrollment.csv dépend du fichier course.csv
* Le fichier user_course_grade.csv dépend des fichiers course.csv et module.csv
* skill_course.csv dépend de course.csv
* skill_level.csv dépend de skill.csv
* learning_program_instance.csv dépend du programme d’apprentissage et de learning_program_course.csv
* learning_program_course.csv dépend de learning_program.csv
* learning_program_enrollment.csv dépend du programme d’apprentissage et de learning_program_instance.csv
* learning_program_instance_course_instance.csv dépend de learning_program.csv, learning_program_instance.csv et de course_instance.csv
* certification_course.csv dépend de certification.csv et course.csv
* certification_commit.csv dépend de certification.csv et certification_course.csv
* certification_enrollment.csv dépend de certification.csv, certification_course.csv et certification_enrollment.csv



Après avoir exporté les données, enregistrez les fichiers .csv sur votre ordinateur local. Les fichiers sont maintenant prêts à être déposés dans les dossiers FTP ou BOX.

## Configuration des dossiers FTP et BOX pour la migration {#setupftpandboxfoldersforthemigration}

Avant de planifier et de commencer la migration réelle de tout le contenu, vous devez d’abord configurer les dossiers FTP et BOX. Vous devez disposer de ces dossiers pour déposer vos fichiers .csv dans ces dossiers. Une fois que votre contenu hérité, sous forme de fichiers .csv, est disponible dans les dossiers FTP et BOX, Learning Manager peut utiliser les données.

### Configuration d’un compte FTP {#setupanftpaccount}

Dans la page d&#39;accueil de l&#39;administrateur d&#39;intégration, cliquez sur **[!UICONTROL ** Demander un dossier FTP CSV **.]** Dans la boîte de dialogue contextuelle qui s’affiche, entrez votre ID de messagerie. Accédez à l’assistant en ligne pour créer le compte FTP Exavault. Dès que vous avez créé votre compte, vous pouvez afficher vos dossiers de projet de migration et de sprint sur le FTP Exavault.

Consultez un exemple d’instantané des fichiers de projet et du dossier d’ExaVault, comme illustré ici :

![](assets/set-up-an-ftp-account.png)

Lorsque vous avez configuré avec succès le dossier FTP, le système affiche le message « La configuration du dossier FTP est terminée ».

## Configuration d’un compte BOX {#setupaboxaccount}

Pour créer un compte BOX et configurer un dossier BOX, procédez comme suit :

Dans la page d’accueil de l’administrateur d’intégration, sélectionnez Migration.

Dans la section Configuration, cliquez sur Demander un dossier Box.

![](assets/set-up-a-box-account.png)

Dans le champ ****[!UICONTROL Entrer l’adresse électronique]****, entrez l’ID de messagerie dans lequel vous souhaitez recevoir les instructions de connexion pour vous connecter à Box.

Cliquez sur **[!UICONTROL ** Se connecter **.]**

Vous recevrez un courrier électronique depuis Box contenant un lien vers le dossier partagé. Si vous n’avez pas de compte Box, cliquez sur S’inscrire et créez un compte. Les instructions de connexion sont ensuite envoyées à l’ID de messagerie de l’administrateur d’intégration.

Après avoir enregistré la connexion, la page de migration affiche le message suivant : « La configuration du dossier Box est terminée ».

## Migration du contenu vers Learning Manager {#migratingthecontenttocaptivateprime}

Avant de commencer la migration, il est important de noter les points suivants :

* Un compte ne peut contenir qu’un seul projet de migration actif à un moment donné. Un compte ne peut contenir qu’un seul sprint actif dans un projet à un moment donné.
* Vous ne pouvez pas annuler une exécution faisant déjà partie du processus de Vous pouvez néanmoins utiliser l’option Supprimer existante dans chaque fonctionnalité de Learning Manager pour annuler la migration des données et du contenu.

Dès que le projet de migration démarre, le projet passe à l’état « Migration en cours ». Dans cet état, aucun autre utilisateur que l’administrateur de l’intégration ne peut se connecter à Learning Manager.

Charger le contenu de formation vers les dossiers de contenu :

Dans la page d’accueil de l’administrateur d’intégration, cliquez sur **[!UICONTROL Migration.]**

Dans la page d’accueil de la migration, le système affiche les projets de migration déjà créés dans votre entreprise.

Cliquez sur **[!UICONTROL **Nouveau**]**dans le coin supérieur droit de la page, pour créer un projet de migration.

***Si vous n’avez pas encore créé de dossier FTP, vous serez invité à créer un compte Exavault pour le dossier FTP. Cette étape est obligatoire avant de commencer à créer un projet de migration. ***

Dans la page ****[!UICONTROL Créer un projet de migration]****, indiquez le nom de votre projet.

![](assets/migrating-the-content-1.png)

Spécifiez une balise pour votre projet, le catalogue de cours et fournissez une description pour le projet de migration. Les éléments de données de la migration sont identifiés à l’aide de la balise de projet de migration. Si vous n’avez pas de catalogue de cours spécifique, choisissez le catalogue par défaut dans la liste déroulante, tous les cours que vous migrez à l’aide d’un projet de migration seront inclus dans le catalogue que vous choisissez à ce stade. Si vous ne sélectionnez pas de catalogue, tous les cours migrés seront affichés dans le catalogue par défaut.

Cliquez sur **[!UICONTROL Créer.]**

Dans la page Configuration du sprint, créez un sprint pour votre projet de migration. Un sprint, dans le processus de migration de Learning Manager, définit un ensemble d’éléments de migration que vous avez choisi de migrer à partir du LMS existant.

![](assets/migrating-the-content-2.png)

Spécifiez un nom pour le sprint et fournissez une description pour le sprint.

Cochez la case ****[!UICONTROL Des utilisateurs ont été ajoutés ou modifiés depuis la dernière exécution]**** pour synchroniser la liste d&#39;utilisateurs avec l&#39;application Learning Manager. Si vous migrez du contenu et des données dans l’application Learning Manager, cette étape n’est pas obligatoire. Toutefois, si un laps de temps s’est écoulé entre votre dernière migration de sprint et la plus récente, il est recommandé de synchroniser la liste des utilisateurs. Cette étape permet à la base de données Learning Manager d’être synchronisée avec les utilisateurs de votre LMS.

***L’étape de synchronisation est recommandée lors de la migration des fichiers enrollment.csv et user_course_grade.csv. Cette étape permet à la base de données Learning Manager d&#39;être synchronisée avec votre base de données de migration et garantit que tous les utilisateurs dont les enregistrements doivent être migrés dans le sprint sont disponibles dans la base de données de migration.***

Cliquez sur **[!UICONTROL ** Suivant **.]**

Cliquez sur **[!UICONTROL **Démarrer**]**pour lancer la migration Sprint avec vos données et votre contenu chargés. Cliquez sur ****[!UICONTROL Actualiser]**** avant de lancer l’exécution du sprint pour synchroniser le FTP et les dossiers de contenu avec Learning Manager.

![](assets/migrating-the-content-3.png)

Vous pouvez cliquer sur ****[!UICONTROL Arrêter]****à tout moment au cours du processus de migration de sprint pour abandonner la migration de sprint.

Le système affiche l’état de la migration par rapport à chacun des éléments de données sprint et de leur contenu. Vérifiez le nombre d’éléments ayant réussi et échoué dans le cadre de l’exécution du sprint de migration.

Si vous chargez le contenu du module, assurez-vous que le chemin du dossier de contenu est fourni dans le fichier *module_version.csv *. Si vous ne réalisez pas cette étape, des erreurs peuvent survenir au cours de la migration. Par exemple, si vous chargez un contenu de module en auto-apprentissage, tel que des vidéos, vous devez spécifier le chemin URL Box relatif dans le fichier *module_version.csv *.

Un exemple de capture d’écran de la boîte de dialogue de progression est fourni ci-dessous pour référence. Comme le montre la capture d’écran, vous pouvez consulter le nombre d’enregistrements traités pour chaque élément de données de migration ainsi que l’état des éléments ayant réussi et échoué. Cliquez sur Télécharger les enregistrements d’erreur à côté des éléments ayant échoué pour télécharger et visionner les journaux d’erreurs. Corrigez les problèmes dans les CSV et téléchargez-les de nouveau sur le serveur FTP.

![](assets/migrating-the-content-4.png)

Pour afficher la liste de tous les sprints d&#39;un projet de migration, cliquez sur **[!UICONTROL **Sprint**]**dans le volet de navigation de gauche. Vous pouvez afficher la liste de tous les sprints, le nombre d’exécutions pour chaque sprint, la date de début, la durée et l’état d’achèvement, comme le montre la capture d’écran ci-dessous.

![](assets/migrating-the-content-5.png)

Pour afficher la liste de tous les sprints d&#39;un projet de migration, cliquez sur **[!UICONTROL **Sprint**]**dans le volet de navigation de gauche. Vous pouvez afficher la liste de tous les sprints, le nombre d’exécutions pour chaque sprint, la date de début, la durée et l’état d’achèvement, comme le montre la capture d’écran ci-dessous.

Pour afficher la liste de tous les sprints d&#39;un projet de migration, cliquez sur **[!UICONTROL **Sprint**]**dans le volet de navigation de gauche. Vous pouvez afficher la liste de tous les sprints, le nombre d’exécutions pour chaque sprint, la date de début, la durée et l’état d’achèvement, comme le montre la capture d’écran ci-dessous.

***Avant de marquer le projet de migration comme terminé, assurez-vous que tous les sprints du projet sont terminés. Une fois que vous avez marqué le projet de migration comme terminé, vous ne pouvez pas revenir en arrière et créer des sprints dans ce projet. Vous ne pouvez pas apporter de modifications à ce projet. Vous pouvez uniquement créer un autre projet de migration et y ajouter des sprints.***

Après avoir migré les données et le contenu d’apprentissage à partir du LMS hérité de votre entreprise, vérifiez si les données et le contenu sont importés correctement. Vous pouvez vérifier en vous connectant en tant qu’administrateur et en vérifiant la disponibilité des modules et cours importés, des données et du contenu

Pour obtenir des ressources utiles sur la migration, reportez-vous aux sections suivantes :

* Résolution des problèmes de migration
* FAQ sur le chargement des fichiers CSV

