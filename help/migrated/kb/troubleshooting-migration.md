---
description: Ce document contient des conseils de dépannage de base permettant de résoudre certains problèmes standard que vous pouvez rencontrer lors de la migration des données et du contenu d’un système de gestion de l’apprentissage (LMS) existant vers Learning Manager.
jcr-language: en_us
title: Dépannage des problèmes de migration
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 43%

---



# Dépannage des problèmes de migration

Ce document contient des conseils de dépannage de base permettant de résoudre certains problèmes standard que vous pouvez rencontrer lors de la migration des données et du contenu d’un système de gestion de l’apprentissage (LMS) existant vers Learning Manager.

## Problèmes génériques de migration {#genericmigrationissues}

### Impossible de se connecter au dossier FTP ou au dossier de contenu {#unabletologintoftpfolderorcontentfolder}

Assurez-vous que vos comptes ont été créés dans les services FTP et Box. Lorsque vous créez un projet de migration, vous demandez à configurer ces deux services. Une fois les services créés, vous recevez des messages électroniques d’Exavault et de Box pour réinitialiser ou configurer les mots de passe. Si vous ne vous souvenez pas des mots de passe, vous pouvez les réinitialiser en vous rendant sur les sites web Exavault et Box.

### Les tâches ne sont pas prises en compte même après avoir cliqué sur le bouton Actualiser {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Assurez-vous que les fichiers .csv sont chargés dans le dossier correct dans Exavault FTP. La structure du chemin doit se présenter comme suit :

`code Account>Project>Sprint location`

* Assurez-vous que les noms des fichiers .csv respectent les noms de spécification des fichiers CSV :

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Les erreurs s’affichent pour les tâches avec des enregistrements d’erreur {#failuresareshownforjobswitherrorrecords}

1. Téléchargez les journaux d’erreurs en cliquant sur le lien **Télécharger des enregistrements d’erreur**
1. Corrigez les fichiers .csv d’origine en fonction des erreurs signalées, et
1. Réexécutez le sprint avec les fichiers CSV modifiés.

Il est recommandé d’exécuter des fichiers CSV modifiés dans un nouveau sprint lorsque le nombre de modifications est inférieur au nombre total d’enregistrements.

### Impossible de se connecter à l’application Learning Manager, même après avoir arrêté la migration Sprint {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Une fois une exécution Sprint arrêtée ou terminée, le déverrouillage du compte peut prendre de 10 à 15 minutes. Essayez d’accéder à l’application après 15 minutes.

### Certaines tâches de migration affichent le statut En cours même après le déclenchement de l’option Arrêter. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

L’arrêt de l’exécution de toutes les tâches peut prendre entre 10 et 15 minutes une fois qu’elle est à l’état « En cours ». Vérifiez à nouveau le statut après 10 minutes.

### Impossible de créer un élément Sprint car le bouton est désactivé {#unabletocreateasprintasthebuttonisdisabled}

Assurez-vous que le sprint actuel est marqué comme terminé avant de créer un sprint. Cliquez sur **[!UICONTROL Marquer Sprint comme terminé]** en haut de la page pour terminer une migration Sprint.

### Impossible de marquer un projet de migration comme terminée car le bouton est désactivé {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Assurez-vous que le sprint actuel est marqué comme terminé, avant de marquer le projet de migration comme terminé. Cliquez sur **[!UICONTROL Marquer Sprint comme terminé]** en haut de la page pour terminer une migration Sprint.

## Problèmes de fichier CSV {#csvissues}

### la migration du fichier module_version.csv échoue et le contenu n’est pas encore migré {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Assurez-vous que le contenu est disponible dans le dossier Contenu (compte Box sous le projet de migration spécifié, chemin d’accès sprint). Assurez-vous également d’avoir sélectionné l’option **Oui** pour **Allez-vous migrer du contenu pour ce sprint ?** dans la page de création Sprint.

Si vous omettez de sélectionner **Oui**, puis poursuivez cette exécution de Sprint, vous devez attendre la fin de l’exécution. Créez un autre sprint et assurez-vous de cliquer **[!UICONTROL Oui]**.

### Les enregistrements enrollment.csv ou user_course_grade.csv échouent avec un message d’erreur « ID Learning Manager non valide » {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Assurez-vous que l’identifiant de courrier électronique indiqué dans les champs userId, assignedByUserID fait partie des utilisateurs valides de Learning Manager. Dans le cas contraire, ajoutez l’utilisateur, créez un nouvel élément Sprint en sélectionnant l’option **Synchroniser les utilisateurs**. Si l’utilisateur ne fait pas partie de l’organisation, ajoutez-le en tant qu’utilisateur supprimé dans Learning Manager en utilisant la spécification CSV Ajouter des utilisateurs. Un exemple de spécification CSV pour ajouter des utilisateurs supprimés est fourni ci-dessous pour référence.

[Users.csv](assets/users.zip) Reportez-vous à **Spécifications et exemples de fichiers CSV** section dans [Manuel de migration](../integration-admin/feature-summary/migration-manual.md) pour télécharger l’ensemble complet des spécifications CSV et des exemples de fichiers CSV.

### Les cours apparaissent vides ou les modules incorrects sont lus pour un cours migré {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Assurez-vous que le **moduleOrderInCourse** La valeur clé d’un cours commence par **0** et est dans l&#39;ordre continu. L&#39;ordre en termes de courseModuleType doit être PRETEST, TESTOUT, CONTENT

Assurez-vous également que deux versions d’Activity, Classroom et VC ne sont pas liées au cours existant.

### Réception d&#39;un message comme « Le module est déjà lié à un cours existant » {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Learning Manager ne permet pas d’associer un module d’activité/de classe virtuelle/de salle de classe à plus d’un cours. Assurez-vous que le module n’est lié à aucun autre cours.

### Tous les cours affichent la dernière version des modules d’activité/de classe virtuelle/de salle de classe même si les cours sont associés à différentes versions de module {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Le contrôle de version des modules d’activité, de salle de classe et de classe virtuelle n’est pas pris en charge dans Learning Manager. Si vous fournissez des versions via le fichier moduleVersion.csv, il met à jour le fichier existant au lieu de créer une nouvelle version.

### La durée souhaitée n’apparaît pas pour un module Activité/VC/Salle de classe migré {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

La durée souhaitée n’est pas une entrée valide pour le module Activité/VC/Salle de classe.

### L’URL de lien hypertexte ne s’ouvre pas dans Learning Manager {#hyperlinkurldoesntopenupincaptivateprime}

Assurez-vous que les liens fournis sont préfixés par &#39;http://&#39; ou &#39;https://&#39;

### La migration de moduleVersion échoue avec des erreurs « Fichier introuvable » {#moduleversionmigrationfailswithfilenotfounderrors}

Assurez-vous que le fichier référencé est présent dans le dossier de contenu et qu’il a été migré avec succès.

### La migration de moduleVersion échoue avec un message d’erreur comme « Une erreur interne s’est produite - pour Module : x et moduleVersion : y » {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Réexécutez le sprint pour résoudre le problème.
