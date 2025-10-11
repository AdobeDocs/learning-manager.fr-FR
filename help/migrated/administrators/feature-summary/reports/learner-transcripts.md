---
description: Les relevés de notes des élèves dans Adobe Learning Manager (ALM) permettent aux administrateurs de surveiller la progression des élèves dans les cours, modules, parcours d’apprentissage et certifications. Il prend en charge les évaluations de performance, la surveillance de la conformité, les audits et les rapports externes. Le rapport offre un résumé complet de l’engagement et des performances d’un élève.
jcr-language: en_us
title: Relevés de notes des élèves dans Adobe Learning Manager
source-git-commit: 85799b32f3a24fc0e6beb34ae39a502ff8e7a7b4
workflow-type: tm+mt
source-wordcount: '4354'
ht-degree: 8%

---


# Relevés de notes des élèves dans Adobe Learning Manager

## Vue d’ensemble

Les relevés de notes des élèves dans Adobe Learning Manager (ALM) permettent aux administrateurs de suivre la progression des élèves à un niveau précis dans les cours, modules, parcours d’apprentissage et certifications. Les données du relevé de notes aident à réaliser des examens des performances, un suivi de la conformité, des audits et des rapports externes.

>[!NOTE]
>
>Les relevés de notes des élèves peuvent être téléchargés par les administrateurs, les administrateurs personnalisés, les responsables ou les élèves.

Les élèves doivent lancer les paramètres de leur profil, puis télécharger leurs relevés de notes d&#39;apprentissage sous forme de fichier Excel. Ce relevé de notes, généré pour un élève individuel, détaille son parcours d’apprentissage personnel. Elle comprend les noms des parcours d’apprentissage, des cours, des instances et des modules, ainsi que les dates clés telles que l’inscription, l’achèvement et les échéances. Il suit également leur progression par statut, notes, scores du quiz (y compris les scores les plus élevés et les maximums) et tentatives effectuées. En outre, elle affiche les ID de formation, les durées, les dates de désinscription, les prix et tous les commentaires de soumission. Ce rapport fournit un aperçu complet de l’engagement et des performances d’un seul élève.

Les organisations peuvent utiliser les relevés de notes des élèves pour ajouter les données de comportement d&#39;apprentissage à un entrepôt de données d&#39;entreprise, où l&#39;on peut souhaiter combiner des données d&#39;apprentissage avec d&#39;autres données d&#39;entreprise pour analyser les corrélations entre le comportement d&#39;apprentissage et d&#39;autres données de processus.

## Objectif et avantages

* Crée des enregistrements prêts pour l’audit pour les exigences réglementaires avec des horodatages et une preuve d’achèvement.
* Relie les activités d&#39;apprentissage au perfectionnement des employés et à l&#39;acquisition de compétences.
* Suit le statut de certification pour les rôles nécessitant une formation obligatoire.
* Appuie la mesure quantitative de l&#39;efficacité du programme d&#39;apprentissage.

## Cas d’utilisation des relevés de notes des élèves

Les relevés de notes des élèves dans Adobe Learning Manager permettent de suivre la formation, la conformité et le développement des compétences, ce qui permet aux départements de vérifier l’achèvement et d’évaluer l’efficacité du programme dans toute l’organisation.  Voici quelques cas d’utilisation traités par les relevés de notes des élèves :

* Un organisme de services financiers doit fournir la preuve que tous les employés en contact avec les clients ont suivi une formation obligatoire sur la conformité avant la date limite réglementaire.
* Le service informatique doit évaluer les capacités actuelles de programmation Java par rapport aux exigences futures du projet.
* Les RH veulent évaluer l&#39;efficacité du nouveau programme d&#39;intégration des employés dans différents ministères.
* L&#39;équipe d&#39;exploitation doit s&#39;assurer que tous les techniciens sur le terrain maintiennent les certifications de sécurité requises.

## Contrôle d’accès et autorisations

**Administrateurs**

* Peut générer des relevés de notes pour tous les élèves de tous les catalogues.
* Peut accéder à toutes les fonctions de création de rapports, mais peut avoir des restrictions de catalogue ou de groupe d&#39;utilisateurs.
* Administrateurs personnalisés : l’accès est limité par la portée et les autorisations attribuées.

**Restrictions basées sur l&#39;étendue**

* Les administrateurs personnalisés peuvent uniquement afficher les relevés de notes des élèves au sein des groupes d’utilisateurs qui leur sont attribués.
* Les rapports n&#39;incluront que les objets d&#39;apprentissage des catalogues auxquels l&#39;administrateur a l&#39;autorisation d&#39;accéder.

## Comment générer les relevés de notes des élèves

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Rapports]** dans le menu de navigation de gauche.
3. Sélectionnez **[!UICONTROL Rapports personnalisés]** dans Rapports, puis **[!UICONTROL Rapports Excel]**.
4. Sélectionnez **[!UICONTROL Relevés de notes des élèves]**.
5. Sélectionnez **[!UICONTROL Générer]**.
6. Sélectionnez la période pour laquelle vous avez besoin que le relevé de notes soit généré. Par défaut, la date **[!UICONTROL De]** est la date d’inscription de l’élève, et la date **[!UICONTROL À]** est toujours la date actuelle. Vous pouvez modifier la date de départ uniquement à partir du moment où vous avez besoin des données.
7. Sélectionnez les options suivantes :
a. Sélectionnez les noms des élèves dans la section **[!UICONTROL Sélectionner des élèves]**. Vous pouvez sélectionner des utilisateurs ou des groupes d’utilisateurs, ou vous pouvez copier et coller les adresses e-mail des élèves pour lesquels vous souhaitez générer des relevés de notes. Voir la section [Générer le relevé de notes de l&#39;élève](#generate-learner-transcript-using-copy-paste) à l&#39;aide du copier-coller pour plus d&#39;informations.
b. Sélectionnez des catalogues spécifiques dans la liste déroulante **[!UICONTROL Sélectionner des catalogues]**. Le relevé de notes n’est téléchargé que pour les catalogues spécifiés.\
   c. Sélectionnez **[!UICONTROL État d&#39;inscription]**. Cette liste déroulante contient les options suivantes :

       * Sélectionner Tout
       * Terminé
       * En Cours
       * Non Démarré
       * Désinscrit
   &#x200B;8. Options avancées : sélectionnez **[!UICONTROL Options avancées]** pour télécharger les transcriptions afin d’inclure les éléments suivants :

   a. Téléchargez des relevés de notes pour les élèves qui ont été supprimés d&#39;un compte en cochant la case **[!UICONTROL Inclure les élèves supprimés]**.
b. Téléchargez les informations de niveau de module dans le relevé de notes de l&#39;élève en cochant la case **[!UICONTROL Activer les informations de niveau de module]**. Dans ce cas, les noms des modules et le temps passé sur chaque module sont récupérés dans le cadre du relevé de notes si cette option est activée.
c. Téléchargez les données de compétences et les fiches récapitulatives en cochant la case **[!UICONTROL Inclure les données de compétences et les fiches récapitulatives]**. Voir la section Rapports Excel pour plus d&#39;informations.
&#x200B;9. Vous pouvez également sélectionner les valeurs de colonne à remplir dans votre rapport. Cela offre la possibilité de télécharger des rapports avec des valeurs de colonne spécifiques selon les besoins. Sélectionnez les colonnes dans le menu déroulant.
Les transcriptions sont générées et téléchargées sur votre ordinateur sous forme de fichiers .zip lorsque les données de compétences ne sont pas incluses. Si la case à cocher Données de compétences est activée, les transcriptions sont générées et téléchargées en tant que . fichiers xlsx.

### Générer le relevé de notes de l’élève à l’aide du copier-coller

La récupération des relevés de notes de l’élève devient un processus fastidieux, car il ne peut être obtenu que pour un seul élève ou un seul groupe d’utilisateurs à la fois. Ici, avec la fonction copier-coller, vous pouvez copier la liste des identifiants de messagerie des élèves et la coller en une seule fois.

1. Sélectionnez l&#39;onglet **[!UICONTROL ID de messagerie]** pour entrer la liste copiée des ID de messagerie uniques.
2. Collez les ID de messagerie uniques des élèves que vous souhaitez ajouter, séparés par une virgule, un point-virgule ou un saut de ligne.
3. Sélectionnez **[!UICONTROL Valider les ID de messagerie]** pour vérifier si l&#39;ID de messagerie que vous avez saisi est valide. Si l’ID de messagerie saisi est incorrect, il est mis en surbrillance en rouge avec un message de validation.

   >[!NOTE]
   >
   >Le bouton Générer reste désactivé à moins que tous les ID de messagerie saisis ne soient corrects.

4. Sélectionnez **[!UICONTROL Générer]** pour générer les relevés de notes des élèves pour tous les ID de messagerie mentionnés.

   >[!NOTE]
   >
   >La génération des relevés de notes des élèves peut être combinée pour les ID de messagerie saisis sous les onglets Utilisateurs et ID de messagerie.

### Que contient le rapport Relevés de notes des élèves ?

Le rapport Relevé de notes de l’élève combine des informations sur l’utilisateur, l’inscription et les objets d’apprentissage.
Les tableaux suivants décrivent chaque type :

**Informations relatives à l’utilisateur**

Les colonnes suivantes identifient l’élève.

| Champ | Description |
|---|---|
| Nom | Nom de l’élève. |
| Courrier électronique | Adresse électronique de l’élève. |
| ID Adobe | Ce champ est renseigné uniquement lorsque les utilisateurs se connectent à l’aide de leur Adobe ID. S’ils accèdent à Adobe Learning Manager via une [authentification unique (SSO)](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) définie par l’organisation, le champ Adobe ID reste vide. |
| ID utilisateur unique | L’ID utilisateur unique est un ID externe généré par des comptes au cas où ils n’auraient pas l’ID de messagerie de tous les utilisateurs, ou l’ID de messagerie unique de tous les utilisateurs. <br>Le champ ID utilisateur unique est un champ facultatif qui peut être activé pour un compte. L’objectif principal du champ est de permettre aux comptes de baliser chaque utilisateur avec un ID unique pour le suivre, mettre à jour les enregistrements d’utilisateur via les API, auditer ou synchroniser les données dans les workflows automatisés. Le balisage de chaque utilisateur se fait via l’importation CSV des utilisateurs.</br><br>Si un compte a opté pour un ID utilisateur unique, alors les rapports, tels que les relevés de notes des élèves, Adobe Learning Manager fournit la colonne dans les rapports.</br> |

**Informations relatives à l’inscription**

Les colonnes suivantes capturent l&#39;activité, la progression ou les tentatives.

| Champ | Description |
|---|---|
| Date d’inscription (fuseau horaire UTC) | Date et heure de l’inscription par l’élève au type d’objet d’apprentissage, qui est cours, certification ou parcours d’apprentissage. |
| Marquer la date de fin (fuseau horaire UTC) | Date et heure auxquelles un instructeur marque une session ou un module comme terminé. Si aucune session n&#39;a eu lieu, la colonne apparaît vide dans le rapport. En outre, si une session a eu lieu et que l’instructeur n’a pas marqué la session comme terminée, la colonne apparaît vide dans le rapport. |
| Date de début (fuseau horaire UTC) | Date et heure auxquelles l’élève a démarré l’objet d’apprentissage. Vide implique que l’élève n’a pas encore commencé cet objet d&#39;apprentissage. |
| Date d’achèvement (fuseau horaire UTC) | Date et heure auxquelles l’élève l’a terminé. Vide signifie que l’élève ne l’a pas encore terminé. |
| Échéance (fuseau horaire UTC) | Date et heure auxquelles l’élève doit terminer cet objet d’apprentissage. Vide implique qu&#39;il n&#39;y a pas d&#39;échéance pour cet objet d&#39;apprentissage. |
| En retard | Statut retard actuel de l’élève inscrit à l’objet d’apprentissage. Oui/Non |
| Statut | Indique l’état de l’élève lorsqu’il suit le cours, la certification ou le parcours d’apprentissage.  Les statuts disponibles sont Non démarré, Non inscrit, En cours ou Terminé. |
| % de progression | Progression actuelle % de l’élève suivant le cours, la certification ou le parcours d’apprentissage. |
| Temps passé (minutes) | Temps d’apprentissage passé par l’élève dans l’objet d’apprentissage, les lignes de niveau module affichent le temps d’apprentissage individuel au niveau du module. Les lignes Cours/Parcours d’apprentissage/Certificat affichent le temps d’apprentissage total passé. |
| Note | Indique la réussite de l’élève. « Réussite », si l&#39;utilisateur a satisfait aux critères de réussite pour cet objet d&#39;apprentissage, « Échec » sinon. |
| Score_quiz | La colonne est utilisée pour enregistrer le score de la dernière tentative d’un quiz. Par exemple, si un utilisateur fait plusieurs tentatives (par exemple, obtient un score de 10, 50 et 30 en trois tentatives), la colonne Quiz_score affiche le score de la dernière tentative, qui est de 30. Supposons qu’un quiz ait un score maximum de 100 et qu’un utilisateur effectue trois tentatives, avec un score de 30, 60 et 90. La colonne Quiz_score affiche 90 (score le plus récent), tandis que Highest_Quiz_score affiche 90 (meilleur score de toutes les tentatives), et Quiz_score_max reste 100 (score maximal possible). |
| Quiz_score_max | La colonne Quiz_score_max représente le score maximal possible qui peut être atteint pour un quiz ou un module spécifique. Comme Quiz_score_max reste constant, il est utile dans les rapports d&#39;afficher le score total réalisable pour un quiz ou un module, indépendamment des performances de l&#39;utilisateur. |
| Highest_Quiz_score | La colonne Highest_Quiz_score représente le score le plus élevé atteint par un utilisateur sur toutes les tentatives d&#39;un quiz spécifique. Par exemple, si un utilisateur effectue trois tentatives avec un score de 10, 20 et 15, le score Highest_Quiz_score affiche 20, car il s’agit du score le plus élevé atteint. |
| Highest_Quiz_score_max | Score maximal possible associé à la tentative de quiz la plus élevée effectuée par un élève sur plusieurs tentatives. Il ne s’agit pas du score le plus élevé obtenu par l’élève. Au lieu de cela, il capture le score maximal qui était possible dans la tentative où l’élève a obtenu le meilleur score. |
| Tentatives effectuées | Nombre total de tentatives effectuées par l’élève jusqu’à présent pour ce module. |
| Nombre maximal de tentatives autorisées | Nombre maximal de tentatives autorisées pour que l’élève utilise le module. |
| Commentaires d’envoi | Commentaires du responsable d’un élève une fois qu’il a terminé un objet d’apprentissage.<br>Les données des commentaires d&#39;envoi fournies par l&#39;instructeur sont incluses dans le module d&#39;envoi de fichiers . Voir <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/instructor/modules#filesubmissionforactivitymodules">Modules-Adobe Learning Manager pour plus d&#39;informations.</a></br> |
| Source d’achèvement | Fait référence à l’origine ou à la méthode selon laquelle l’accomplissement d’un cours, d’un programme d’apprentissage ou d’une certification par un élève est enregistré. Cela aide les administrateurs à comprendre comment l’achèvement a été atteint ou comment ils se sont connectés au système. La colonne indique si l’achèvement a été déclaré par l’utilisateur, enregistré automatiquement ou facilité par un rôle ou une configuration spécifique. <b>Remarque :</b> pour les workflows d&#39;assiduité du connecteur VC, lorsqu&#39;un élève est marqué comme étant assidu automatiquement, la source affiche « SELF, (learner_email) ». |
| Commentaire d’achèvement | Commentaires effectués par l’administrateur lorsqu’il marque un élève comme terminé après qu’il a terminé un cours, une certification ou un parcours d’apprentissage. L’administrateur peut ajouter les commentaires d’achèvement pour un ou plusieurs élèves. |

**Informations relatives aux objets d’apprentissage**

Il s’agit des cours, modules, parcours d’apprentissage, certifications, etc.

| Champ | Description |
|---|---|
| Nom du plan d&#39;apprentissage | Titre du plan d’apprentissage. |
| Programme d&#39;apprentissage/certification/cours | Titre de l’objet d’apprentissage. |
| Type | Type d’objet d’apprentissage auquel l’utilisateur était inscrit. Par exemple,<ul><li>Parcours d’apprentissage</li><li>Certification</li><li>Cours</li></ul> |
| Chemin incorporé | Un parcours intégré est un type de parcours d’apprentissage inclus dans le cadre d’un autre cours     ou un parcours d’apprentissage. Le champ indique qu’un élève termine ce parcours d’apprentissage dans le cadre d’un autre parcours d’apprentissage plutôt que comme une affectation autonome. |
| Cours | Nom du cours auquel l’utilisateur est inscrit. Lorsqu’elle est vide, la ligne représente une certification ou un parcours d’apprentissage. <br><b>Remarque :</b> bien que les parcours d’apprentissage et les certifications    se composent de cours individuels ou de parcours d’apprentissage imbriqués, chaque composant conservant son propre enregistrement indépendant. Cela garantit que les données de progression, d&#39;achèvement et de rapport sont suivies séparément pour les éléments parent et enfant.</br> |
| ID unique d’objet d’apprentissage | ID unique de l’objet d’apprentissage. Il est nécessaire si le client dispose de l’objet d’apprentissage dans un système externe doté de son propre ID. Ceci est utile si vous souhaitez mapper l’ID d’objet d’apprentissage et l’objet d’apprentissage Adobe Learning Manager du système externe.<br>Un administrateur peut activer l&#39;option ID uniques d&#39;objet d&#39;apprentissage dans la page Paramètres. Lorsque cette option est activée, Adobe Learning Manager affecte un ID unique à un objet d’apprentissage chaque fois qu’un auteur crée un cours, une certification ou un parcours d’apprentissage. </br> |
| Instance | Le nom de l’instance de l’utilisateur de l’objet d’apprentissage est inscrit à. |
| Critères de sélection | Base de l’inscription (comment cet élève s’est inscrit à cet objet d’apprentissage).<br>Dans Adobe Learning Manager, les élèves peuvent s&#39;inscrire à des objets d&#39;apprentissage de plusieurs façons : Inscription proposée par le responsable : les responsables proposent des élèves pour des cours spécifiques. Les élèves ne peuvent pas s&#39;inscrire eux-mêmes à ces cours.</br><ul><li>Inscription approuvée par le responsable : les élèves s&#39;inscrivent à des cours, mais l&#39;inscription nécessite l&#39;approbation du responsable.</li><li>Auto-inscription : les élèves s&#39;inscrivent directement aux cours sans nécessiter d&#39;approbation.</li><li>Inscrit par l&#39;administrateur : les administrateurs inscrivent manuellement les élèves aux cours.</li></ul> |
| Module | Nom du module dans les cours. Seuls les modules dont le statut est Terminé ou En cours apparaissent dans le rapport. Si le statut n’est pas Démarré ou Désinscrit, la colonne Module reste vide.<br>Téléchargez les informations de niveau module dans le relevé de notes de l&#39;élève en cochant la case <b>Activer les informations de niveau module</b>. Dans ce cas, les noms des modules et le temps passé sur chaque module sont récupérés dans le cadre du relevé de notes si cette option est activée.</br> |
| ID de module | ID unique du module.<br><b>Remarque :</b> la colonne ID de module apparaît dans le rapport uniquement si vous avez coché la case Inclure les informations sur le module lors de la génération de la transcription.</br> |
| Version | La version du module fait référence à la version spécifique d’un module avec lequel un élève a interagi. Cela est particulièrement utile lorsqu&#39;un module a fait l&#39;objet de mises à jour ou de modifications, car cela permet aux administrateurs de suivre quelle version du module a été consultée par l&#39;élève.<br>Lorsqu&#39;un auteur télécharge une nouvelle version d&#39;un module, Adobe Learning Manager la traite comme une nouvelle version du module existant. Cela permet au contenu d’être mis à jour sans perturber tous les élèves.</br><br>La version apparaît si la case <b>Activer les informations au niveau du module</b> a été cochée lors de la génération du rapport.</br><br>Voir <a href="https://elearning.adobe.com/2023/03/updating-the-module-in-adobe-learning-manager-how-to-replace-a-content-module-in-a-course-without-disturbing-the-users-progress" />Mise à jour d&#39;un module dans Adobe Learning Manager</a> pour plus d&#39;informations.</br> |
| Type de livraison | Indique comment le module est fourni : Fusionné, Salle de classe ou Salle de classe virtuelle. |
| Langue | Langue dans laquelle le module est utilisé par l’élève. Cette colonne n’affiche de valeur que pour les modules d’apprentissage en ligne. |
| En retard | Statut retard actuel de l’élève inscrit à l’objet d’apprentissage. Oui/Non |
| Note | Indique la réussite de l’élève. « Réussite », si l&#39;utilisateur a satisfait aux critères de réussite pour cet objet d&#39;apprentissage, « Échec » sinon. |

>[!INFO]
>
>Les colonnes suivantes sont masquées dans les relevés de notes des élèves :
>
>* Nombre d’inscriptions
>* Nombre de commencé
>* Nombre d&#39;achèvements
>* Échéance dans N jours
>* Échéance dans N jours pour l&#39;utilisateur
>* Nombre de (progression supérieure à N %)
>* Nombre de (progression supérieure à N %) pour l’utilisateur
>
>Ces colonnes n’apparaissent que si vous avez sélectionné Inclure les données de compétences et les fiches récapitulatives lors de la génération du relevé de notes. Ces colonnes sont utilisées pour calculer les détails récapitulatifs d’un élève inscrit à un objet d’apprentissage.

| Champs | Description |
|---|---|
| ID de formation | Identificateur unique généré par le système et affecté à l’inscription de chaque élève à un cours, une certification ou un parcours d’apprentissage spécifique. Si un élève s’inscrit à nouveau au même cours, un nouvel ID de formation est généré. Un élève peut avoir plusieurs ID de formation pour le même cours. |
| Durée de la formation ou du module (min) | Cette colonne affiche la durée attendue (en minutes) d&#39;un cours, d&#39;un module ou d&#39;une activité de formation telle que définie lors de la création du cours. Ce n’est pas le temps réel passé par un élève, mais la durée configurée/affectée qui représente la durée prévue de la formation. <br>Cette colonne affiche la durée totale (en minutes) de l’élément d’apprentissage attribué, qui peut être un parcours d’apprentissage ou un cours individuel.</br><br><b>Durée du parcours d’apprentissage :<b> si l’élément de formation est un parcours d’apprentissage, sa durée est calculée comme la somme des durées de tous les cours à l’intérieur du parcours d’apprentissage.</br><br>Exemple : si le cours 1 = 50 minutes et le cours 2 = 60 minutes, la durée du parcours d’apprentissage = 110 minutes.</br><br><b>Durée du cours individuel :</b>Si l’élément de formation est un cours individuel (ne faisant pas partie d’un parcours d’apprentissage), la durée reflète le temps nécessaire pour ce cours uniquement.</br> |
| Embedded_Course_ID | ID du cours qui fait partie d’un parcours d’apprentissage ou de tout autre cours.<br>La colonne est remplie lorsque la ligne représente un parcours d’apprentissage ou une certification elle-même. Elle affiche les ID des cours individuels intégrés dans le parcours d’apprentissage ou la certification. Il n&#39;est pas renseigné lorsque la ligne elle-même est un cours uniquement, car il n&#39;y a pas d&#39;éléments incorporés.</br> |
| ID du parcours intégré | ID du chemin d&#39;accès dans lequel se trouve le cours incorporé.<br>La colonne identifie l’ID unique des parcours d’apprentissage intégrés. Cela permet de suivre les cours dans les parcours d’apprentissage et fournit une visibilité sur la structure hiérarchique des parcours d’apprentissage.</br> |
| Date de désinscription (fuseau horaire UTC) | Date de désinscription par l’élève au type d’objet d’apprentissage. |
| Prix ($) | Prix de l’objet d’apprentissage pour lequel il est acheté dans le catalogue des cours. Pour que cette colonne apparaisse dans le relevé de notes de l’élève, l’administrateur doit activer la case à cocher Activer la tarification pour les cours/parcours d’apprentissage/certifications dans les paramètres du compte. |

## Rapports Excel

La boîte de dialogue Relevés de notes des élèves vous permet également de télécharger des données de compétences et des fiches récapitulatives sous forme de fichiers Excel. Cochez la case **[!UICONTROL Inclure les données de compétences et les fiches récapitulatives]**, puis sélectionnez **[!UICONTROL Générer]** pour télécharger un fichier Excel avec les fiches suivantes :

* Résumé d’apprentissage I
* Résumé d’apprentissage II
* Résumé de la conformité
* Transcription des compétences
* Résumé des compétences I
* Résumé des compétences II

### Que contient la feuille Résumé de l’apprentissage I ?

Suivez les parcours d’apprentissage, les cours ou les certifications qui sont activement utilisés. Suivez l’activité en cours ainsi que les échéances à venir pour la formation.

* Nombre d’élèves inscrits : indique le nombre d’élèves inscrits à un objet d’apprentissage particulier (cours, parcours d’apprentissage ou certification), qu’ils l’aient commencé ou non.
* Nombre d’élèves qui ont commencé : indique le nombre d’élèves qui ont lancé ou commencé le cours, la certification ou le parcours d’apprentissage.
* Nombre d’élèves ayant terminé : affiche le nombre d’élèves ayant terminé avec succès la formation et répondant à tous les critères d’achèvement.
* Nombre d’élèves ayant progressé ≥ N % : reflète le nombre d’élèves qui ont atteint au moins le seuil de progression spécifié (par exemple, 70 %) dans la formation, même s’ils ne l’ont pas terminé.
* Nombre d’élèves dont la date d’échéance est dans N jours : indique le nombre d’élèves dont la formation doit être suivie au cours des « N » prochains jours (par exemple, 7 jours), ce qui est utile pour identifier les échéances à venir.

### Interprétation des données

Ce rapport Résumé de l’apprentissage I suit deux parcours d’apprentissage attribués à l’élève.

* L’utilisateur est inscrit à deux parcours d’apprentissage et a démarré les deux.
* Aucun des parcours d’apprentissage n’est encore terminé.
* L’élève n’a pas encore progressé au-delà du seuil de 70 % dans aucun des parcours.
* Aucune échéance ne tombe dans les sept prochains jours pour l&#39;une ou l&#39;autre formation.

### Que contient la fiche Résumé de l’apprentissage II ?

Suivez l’activité d’apprentissage par élève. Suivez les inscriptions, l&#39;activité en cours ainsi que les dates d&#39;échéance pour les élèves.

* Nombre d’objets d’apprentissage inscrits : nombre total d’objets d’apprentissage (LO) auxquels l’élève est inscrit dans chaque cours, certification ou parcours d’apprentissage. compte séparément .
* Nombre d’objets d’apprentissage démarrés : indique le nombre d’objets d’apprentissage que l’élève a lancés ou démarrés.
* Nombre d’objets d’apprentissage terminés : indique le nombre d’objets d’apprentissage démarrés que l’élève a entièrement terminés.
* Nombre d’objets d’apprentissage ayant progressé ≥ N % : reflète le nombre d’objets d’apprentissage pour lesquels l’élève a atteint au moins le seuil de progression spécifié (70 % dans ce cas).
* Nombre d’objets d’apprentissage dont la date d’échéance est dans N jours : identifie les objets d’apprentissage qui doivent être exécutés dans le prochain nombre de jours défini (7 jours dans ce cas), ce qui permet de suivre les échéances proches.

### Interprétation des données

* L’élève est inscrit à deux objets d’apprentissage et a démarré les deux.
* Aucun objet d’apprentissage n’est terminé.
* L’élève n’a encore atteint 70 % de progression dans aucun d’entre eux.
* Aucun des objets d&#39;apprentissage n&#39;est prévu dans les 7 prochains jours.

### Que contient la fiche récapitulative de conformité ?

Suivez les élèves qui ont des échéances à venir pour des cours clés, des parcours d’apprentissage ou des certifications.

| Colonne | Description |
|---|---|
| Type | Type d’objet d’apprentissage pour lequel le tableau Résumé de l’apprentissage doit afficher des données. |
| Libellés de ligne (colonne de gauche) | Nom de l’élève avec la liste des objets d’apprentissage auxquels il est inscrit. |

### Que contient la feuille Relevé de notes de la compétence ?

| Colonne | Description |
|---|---|
| Nom | Nom complet de l’élève associé au relevé de notes de compétence. |
| Courrier électronique | Adresse électronique de l’élève. |
| ID utilisateur unique | Identificateur unique défini par l’organisation pour l’élève. |
| Compétence | Nom de la compétence affectée à l’élève (par exemple, Programmation Java, Leadership). |
| Niveau de compétence | Niveau d’expertise au sein de la compétence que l’élève est censé atteindre (par exemple, débutant, intermédiaire, avancé). |
| Crédits requis | Nombre de crédits d’apprentissage nécessaires pour atteindre le niveau de compétence attribué. |
| Crédits gagnés | Nombre de crédits acquis par l’élève pour atteindre le niveau de compétence attribué. |
| Pourcentage d&#39;achèvement | Pourcentage de crédits requis terminés par l’élève. |
| Date d’attribution (UTC) | Date à laquelle la compétence a été attribuée à l’élève. |
| Date d’obtention (UTC) | Date à laquelle l’élève a obtenu les crédits requis et a rempli les critères de niveau de compétence. |
| Nom du responsable | Nom du responsable de l’élève qui supervise la progression de l’apprentissage. |

### Que contient la fiche Résumé des compétences I ?

| Colonne | Description |
|---|---|
| Après | Représente le nombre d’élèves qui ont acquis une compétence avant une période définie (en jours), au-delà de laquelle la compétence est considérée comme obsolète ou nécessitant une actualisation. Utile pour identifier les élèves dont les compétences sont proches ou expirées.<br>Voir <a href="https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels">Niveaux de compétence</a> pour plus d&#39;informations. |
| Nom | Nom complet de l’élève auquel la compétence est affectée. |
| Nom du responsable | Nom du responsable de la génération de rapports de l’élève. |
| Libellés de ligne | Nom de compétence spécifique attribué aux élèves figurant sur cette ligne. Utilisé comme en-tête de regroupement pour résumer les données de compétence des élèves dans chaque catégorie de compétence. |
| Nombre d’utilisateurs qui doivent avoir cette compétence | Nombre total d’élèves auxquels une compétence spécifique a été attribuée. |
| Nombre d’utilisateurs ayant atteint cette compétence | Nombre d’élèves ayant terminé avec succès les objets d’apprentissage requis pour acquérir la compétence. |
| Nombre d’élèves dont la compétence doit être actualisée | Nombre d’élèves dont les dates d’achèvement des compétences dépassent le seuil d’actualisation défini. |
| Pourcentage de conformité (en fonction des compétences acquises) | Taux de conformité ou d’adoption de la compétence. |


### Que contient la fiche Résumé des compétences II ?

| Colonne | Description |
|---|---|
| Après | Nombre de compétences acquises par l’élève avant le seuil d’actualisation défini (en jours). Cela identifie les compétences qui peuvent être obsolètes et doivent être actualisées. |
| Compétence | Nom des compétences attribuées aux élèves. Cela peut être lié à un ou plusieurs objets d’apprentissage, tels que des cours, des certifications ou des parcours d’apprentissage. |
| Nom du responsable | Nom du responsable direct de l’élève. |
| Libellés de ligne | Nom complet de l’élève. Pour chaque élève, les compétences et la progression sont affichées dans les colonnes suivantes. |
| Nombre de compétences que chaque utilisateur doit posséder | Nombre total de compétences attribuées à l’élève. |
| Nombre de compétences dont dispose chaque utilisateur | Nombre total de compétences que l’élève a acquises avec succès grâce à l’accomplissement des objets d’apprentissage associés. |
| Nombre de compétences nécessitant une actualisation | Nombre de compétences acquises qui ont dépassé la durée d’actualisation et nécessitent désormais une revalidation. Cette valeur permet de suivre les besoins en renouvellement de formation pour la conformité ou le développement continu. |
| Pourcentage de conformité | Indique le niveau de conformité global de l’élève en fonction de l’acquisition de compétences. |

## Historique des téléchargements des relevés de notes des élèves

L’historique des téléchargements de relevés de notes des élèves permet aux administrateurs de suivre qui a téléchargé le relevé de notes de chaque élève et quels utilisateurs ils ont consultés. Cette fonctionnalité est particulièrement utile dans les environnements d’entreprise et axés sur la conformité où plusieurs parties prenantes peuvent avoir besoin de consulter des dossiers d’apprentissage.

Après avoir téléchargé un relevé de notes de l’élève, la page Relevés de notes de l’élève répertorie tous les relevés de notes générés par toute personne de la plateforme.

La liste affiche les attributs suivants :

* De et À : durée des transcriptions à télécharger.
* Généré par : adresse e-mail de l’utilisateur qui a téléchargé le rapport ou demandé le téléchargement.
* Élèves : élèves ou groupes d&#39;élèves dont les relevés de notes doivent être téléchargés.
* Filtres appliqués : filtres appliqués pour le statut d’inscription.
* Données supplémentaires incluses : les données supplémentaires (élèves supprimés, informations sur le module, données sur les compétences et fiches récapitulatives) que l&#39;administrateur avait demandées à partir de l&#39;option Avancé dans le modèle Ajouter le relevé de notes de l&#39;élève
* Statut : téléchargé, en file d’attente ou en cours.
* Annuler : annulez la génération du rapport à tout moment.

## Remarques supplémentaires concernant les relevés de notes des élèves

Les relevés de notes des élèves incluent plusieurs comportements que les administrateurs doivent connaître :

**Affichage du parcours d’apprentissage et de la progression du cours**

Tous les cours qui font partie d’un parcours d’apprentissage apparaîtront dans le relevé de notes de l’élève, même si celui-ci a progressé dans un seul des cours. Cela garantit une visibilité complète d’un parcours d’apprentissage, même lorsque la progression est partiellement terminée.

**Données pour les élèves supprimés**

Si un élève a été supprimé de la plateforme, son relevé de notes n’affichera pas ses enregistrements dans les rapports générés pour le groupe d’utilisateurs auquel il appartenait. Cela signifie que les enregistrements des élèves supprimés seront exclus de tous les rapports filtrés créés à l’aide des filtres de groupe d’utilisateurs.

Mais vous pouvez toujours télécharger les données des élèves supprimés. Si vous avez sélectionné l&#39;option **[!UICONTROL Inclure les élèves supprimés]** lors de la définition des filtres pour la génération du rapport, vous pouvez télécharger le rapport pour les élèves supprimés.

**Comportement des administrateurs personnalisés**

Les administrateurs personnalisés avec une portée définie (par exemple, limitée à des catalogues ou des groupes d’utilisateurs spécifiques) verront des données de transcription filtrées en fonction de leur portée :

* Portée du groupe d&#39;utilisateurs : seuls les élèves du groupe d&#39;utilisateurs de la portée de l&#39;administrateur personnalisé seront inclus dans le rapport.
* Portée du catalogue : seuls les objets d’apprentissage (cours, certifications et parcours d’apprentissage) attribués aux catalogues dont la portée est définie seront inclus dans le rapport.
* Colonnes filtrées : les colonnes restent les mêmes. Seules les lignes seront limitées en fonction des portées des catalogues et des groupes d’utilisateurs.

Ainsi, les administrateurs personnalisés dont la portée est limitée visualisent uniquement les données et le contenu d’apprentissage de l’élève qu’ils sont autorisés à gérer.

**Prise en charge du connecteur**

Le rapport Relevé de notes de l&#39;élève est accessible via l&#39;interface utilisateur de l&#39;administrateur, [FTP, Box, l&#39;API de tâche ou Power BI](/help/migrated/integration-admin/feature-summary/connectors.md). Il n’est pas inclus dans les rapports unifiés de Salesforce, Power BI et Marketo Engage.

Les rapports unifiés téléchargés depuis Salesforce, Marketo Engage et Power BI contiennent moins de colonnes que les relevés de notes des élèves.






