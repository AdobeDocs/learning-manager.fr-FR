---
description: Découvrez les nouvelles fonctionnalités et les améliorations de la version de novembre 2024 de Adobe Learning Manager
jcr-language: en_us
title: Résumé des nouvelles fonctionnalités
exl-id: 4dfe0e31-d202-4a6e-8c4f-43851218699f
source-git-commit: 537d324d6e266552fdfdd9ba16557fd3228870b7
workflow-type: tm+mt
source-wordcount: '3260'
ht-degree: 2%

---

# Résumé des nouvelles fonctionnalités {#new-features-summary}

Découvrez les nouvelles fonctionnalités et les améliorations de la version de novembre 2024 de Adobe Learning Manager.

* **Recherche basée sur l&#39;IA :** combine la recherche lexicale et sémantique pour des résultats plus intelligents et sensibles au contexte.
* **Webhooks** : intégrez-les aux webhooks pour envoyer des informations en temps réel à des URL spécifiques.
* **Interopérabilité des outils d’apprentissage (LTI)** : prend en charge LTI pour l’interopérabilité avec d’autres plateformes LMS.
* **Intégration Credly** : gérez et partagez des badges externes via Credly.
* **Améliorations du tableau de bord de conformité** : partagez des tableaux de bord avec d’autres administrateurs et définissez des widgets de conformité par défaut sur les pages d’accueil des élèves.
* **Prise en charge multilingue** : créez des instances spécifiques à la langue pour les modules de salle de classe et de classe virtuelle.
* **Rôles personnalisés** : contrôle amélioré des rôles et autorisations des utilisateurs.
* **Commentaires d’achèvement** : ajoutez des commentaires lorsque vous marquez les élèves comme terminés.
* **Rapport de groupe d&#39;utilisateurs** : gérez les groupes d&#39;utilisateurs avec des rapports détaillés.
* **Rapport de liste d&#39;attente** : téléchargez la liste des élèves en liste d&#39;attente pour les instances de cours.
* **Améliorations de l’accessibilité** : prise en charge du texte optionnel sur les en-têtes et les logos d’entreprise.
* **Prise en charge de l&#39;hindi** : prise en charge linguistique de l&#39;interface pour l&#39;hindi.
* **Vérification des blasphèmes** : bloquez les publications sociales contenant des mots interdits.
* **Optimisation des modèles d’e-mail** : modèles d’e-mail combinés et optimisés pour les affectations d’instructeurs et les annulations de sessions.
* **Critères d’achèvement MS Teams** : définissez le temps de présence minimum pour les sessions VILT.
* **Nouveaux workflows de migration** : les modifications apportées à la migration incluent les critères d’achèvement des cours et des modules, ainsi que la migration des modules dans des dossiers.

>[!NOTE]
>
>Consultez ce [webinaire](https://cdn.content.adobelearningmanageracademy.com/public/newlearner/newlearner_0dc0f1e8.html#/overviewPage?instanceId=11932477&amp;loId=11231360&amp;loType=course) pour en savoir plus sur les nouvelles fonctionnalités de cette version.

## Recherche optimisée par l’IA dans Adobe Learning Manager

Adobe Learning Manager remodèle la façon dont les élèves recherchent des cours ou des formations. Il introduit une fonctionnalité de recherche basée sur l’IA qui combine la recherche lexicale et sémantique. La recherche est désormais plus intelligente, car elle recherche des termes spécifiques et comprend le contexte et l&#39;intention qui les sous-tendent. La recherche avancée comprend la signification de votre requête et fournit des résultats pertinents. Il identifie l&#39;objectif principal de la recherche pour vous donner l&#39;ensemble de résultats le plus complet.

>[!NOTE]
>
>La recherche optimisée par l’IA est uniquement disponible pour les élèves.

Reportez-vous à cet article [Recherche avancée](/help/migrated/learners/feature-summary/advanced-search.md) pour plus d&#39;informations.

## Webhooks

Adobe Learning Manager permet l’intégration avec des webhooks pour envoyer des informations en temps réel, telles que les inscriptions aux cours, la création de cours et d’autres informations, à une URL spécifique.

Un webhook dans ALM permet à une entité d’envoyer automatiquement des données à une autre application via HTTP. Elle permettra à une application de fournir des informations à d&#39;autres applications sans les demander constamment. Par exemple, si un utilisateur termine un cours sur un système de gestion de l’apprentissage (LMS), un webhook peut automatiquement envoyer ces informations à une autre plate-forme, telle qu’un outil de gestion de la relation client ou de création de rapports. Les webhooks sont souvent utilisés dans les intégrations pour automatiser les processus et réduire le besoin de mises à jour manuelles entre les systèmes. Configurez les webhooks en fournissant une URL de rappel à laquelle vous enverriez les données.

Reportez-vous à cet article [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md) pour plus d&#39;informations.

## Interopérabilité des outils d’apprentissage

Adobe Learning Manager prend désormais en charge LTI pour améliorer l’interopérabilité entre Adobe Learning Manager et d’autres systèmes de gestion de l’apprentissage (LMS).

### Qu’est-ce que LTI ?

LTI (Learning Tools Interoperability) est une norme qui permet aux outils et fournisseurs de contenu tiers de se connecter à un système de gestion de l’apprentissage (LMS). Les utilisateurs peuvent accéder au contenu d’apprentissage externe de fournisseurs de contenu externes directement dans leur LMS sans se connecter ou accéder à un autre LMS.

**LTI en tant que fournisseur d’outils** : LTI en tant que fournisseur d’outils permet aux systèmes externes de s’intégrer à un LMS. Adobe Learning Manager agit comme un fournisseur d’outils LTI, permettant aux autres plateformes LMS d’accéder aux cours, aux certificats ou aux parcours d’apprentissage à partir de Adobe Learning Manager directement dans leur LMS.

**LTI en tant que consommateur d’outils** : LTI en tant que consommateur d’outils permet au LMS d’intégrer des outils externes via l’interopérabilité des outils d’apprentissage (LTI). Dans ce scénario, le LMS est un consommateur de services fournis par des outils externes. Adobe Learning Manager agit en tant que consommateur d’outils LTI, ce qui lui permet d’intégrer des outils d’apprentissage tiers. Cela permet aux élèves Adobe Learning Manager d’utiliser les cours, les certificats ou les parcours d’apprentissage des outils tiers dans Adobe Learning Manager.

Reportez-vous à cet article [Interopérabilité des outils d’apprentissage](/help/migrated/integration-admin/feature-summary/learning-tools-interoperability.md) pour plus d’informations.

## Credly

À l’aide de Credly, un administrateur dans ALM permet aux élèves de gérer et de partager des badges externes à partir de la plateforme sur divers canaux de médias sociaux.

### Qu’est-ce que Credly ?

Credly est une plateforme d’identification numérique qui permet aux élèves et aux organisations d’obtenir, de partager et de vérifier des réalisations professionnelles, telles que des badges ou des certifications. Les élèves peuvent gérer et partager des badges via leur profil Credly sur les réseaux sociaux et d’autres endroits.

### Intégration de Credly à Adobe Learning Manager

Tout d’abord, ajoutez le connecteur Credly dans Adobe Learning Manager (ALM). Ensuite, migrez les badges existants de Credly pour assurer la continuité des réalisations des élèves. Enfin, créez une compétence dans Adobe Learning Manager pour le parcours d’apprentissage approprié afin d’améliorer le développement et la reconnaissance des élèves.

Reportez-vous à cet article [Credly](/help/migrated/integration-admin/feature-summary/credly-integration.md) pour plus d&#39;informations

## Tableau de bord Conformité

Dans cette version, les administrateurs peuvent désormais partager le tableau de bord avec d’autres administrateurs, des administrateurs personnalisés et des responsables de boutique, ce qui leur donne un accès instantané aux tableaux de bord de conformité. Ils peuvent désormais définir le widget de conformité par défaut sur la page d’accueil de l’élève, ce qui lui permet de suivre ses exigences de conformité. Reportez-vous à cet article [Tableau de bord de conformité](/help/migrated/administrators/feature-summary/reports.md#share-compliance-dashboard-with-admins-and-custom-admins) pour plus d&#39;informations.

## Prise en charge multilingue

Adobe Learning Manager (ALM) permet désormais aux auteurs de créer des instances spécifiques à une langue à l’aide du balisage linguistique pour les modules de salle de classe et de salle de classe virtuelle. Les élèves peuvent accéder aux modules CR/VC dans leur langue préférée. Par exemple, un auteur peut créer un module CR/VC avec deux instances : une en anglais et une en français. Les élèves peuvent sélectionner les instances dans leur langue préférée.

Reportez-vous à cet article [Ajouter des objets d&#39;apprentissage dans différentes langues](/help/migrated/authors/feature-summary/add-new-language-learning-objects.md#multi-language-support-for-crvc-instances-with-language-tagging) pour plus d&#39;informations.

## Rôles personnalisés

Les rôles personnalisés permettent aux administrateurs de définir des rôles et des responsabilités spécifiques pour différents groupes d’utilisateurs, garantissant ainsi une meilleure gestion et un meilleur contrôle. Avec cette version, ALM améliore les rôles personnalisés en fournissant un contrôle plus détaillé sur les sections suivantes.

* Utilisateurs
* Cours
* Parcours d’apprentissage
* Certifications
* Assistances à la tâche
* Catalogues

Les administrateurs peuvent attribuer des autorisations précises en fonction des responsabilités des utilisateurs, en veillant à ce que chaque groupe ait uniquement accès aux fonctionnalités et au contenu pertinents. Ces contrôles améliorés permettent une gestion plus granulaire des sections clés.

Connectez-vous en tant qu’administrateur et accédez à **[!UICONTROL Utilisateurs]** > **[!UICONTROL Rôles personnalisés]** pour créer et gérer les Rôles personnalisés.

Reportez-vous à cet article [Rôles personnalisés](/help/migrated/administrators/feature-summary/custom-role.md) pour plus d&#39;informations.

## Commentaires d’achèvement

Les administrateurs peuvent désormais ajouter des commentaires lorsqu’ils marquent les élèves comme ayant terminé leurs cours, parcours d’apprentissage ou certifications. Les administrateurs peuvent ajouter des commentaires pour un ou plusieurs élèves en même temps, et les commentaires apparaissent dans le rapport [Relevés de notes de l&#39;élève](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts).

Consultez cet article [Commentaires d&#39;achèvement](/help/migrated/administrators/feature-summary/courses.md#completion-comments) pour plus d&#39;informations.

## Rapport de groupe d’utilisateurs

Le nouveau **[!UICONTROL rapport de groupe d&#39;utilisateurs]** de Adobe Learning Manager permet de gérer les groupes d&#39;utilisateurs en offrant une visibilité sur les groupes non gérés lorsque les administrateurs ont quitté l&#39;application. Les administrateurs peuvent accéder aux rapports dans la section **[!UICONTROL Utilisateurs]** > **[!UICONTROL Groupe d’utilisateurs]**. Il fournit des informations détaillées sur chaque groupe, notamment :

* Type de groupe d’utilisateurs
* Nom du groupe
* Description
* Créé par (nom)
* Créé par (adresse e-mail)
* Créé le (fuseau horaire UTC)
* Nombre d&#39;utilisateurs

Consultez cet article [Rapport de groupe d&#39;utilisateurs](/help/migrated/administrators/feature-summary/add-users-user-groups.md#user-group-report) pour plus d&#39;informations.

## Rapport de liste d’attente

Le nouveau **[!UICONTROL rapport de liste d&#39;attente]** de Adobe Learning Manager permet aux administrateurs de télécharger la liste d&#39;élèves inscrits sur liste d&#39;attente pour toutes les instances d&#39;un cours. Les administrateurs et les instructeurs peuvent accéder à ce rapport à partir de la section **[!UICONTROL Liste d&#39;attente]** sur la page **[!UICONTROL Cours]** ou **[!UICONTROL Présentation de la session]**. Le rapport de liste d’attente peut être téléchargé à partir des sections Administrateur et Instructeur.

En suivant les colonnes disponibles dans le rapport Liste d’attente :

* Nom du cours
* Nom d’instance
* ID d’instance
* État d’instance
* Nom d’utilisateur
* Courrier électronique
* ID utilisateur unique
* Date d’inscription (fuseau horaire UTC)
* Statut
* Nombre de listes d’attente
* Limite de liste d’attente
* Limite de postes

Reportez-vous à ces articles [Rapport de liste d&#39;attente (administrateur)](/help/migrated/administrators/feature-summary/courses.md#waitlist-report) et [Rapport de liste d&#39;attente (instructeurs)](/help/migrated/instructors/feature-summary/learners.md#waitlist-report) pour télécharger le rapport à partir de la section Administrateur et instructeur.

## Accessibilité dans la page d’accueil de l’élève

Adobe Learning Manager prend désormais en charge le texte optionnel pour tous les en-têtes afin d’améliorer l’accessibilité pour les élèves. Cela permet aux élèves ayant des besoins spéciaux d’utiliser des lecteurs d’écran pour lire le texte optionnel et comprendre l’image. Vous pouvez sélectionner plusieurs langues et fournir un texte de remplacement pour chaque langue. Veillez à ajouter le texte optionnel dans les langues respectives. Assurez-vous que le logo de la société dans votre compte inclut également un texte de remplacement avec le nom de la société.
Reportez-vous à cet article [Annonce](/help/migrated/administrators/feature-summary/announcements.md#masthead) pour plus d&#39;informations.

## Prise en charge de l’hindi

Adobe Learning Manager introduit désormais l&#39;hindi comme l&#39;un des langages d&#39;interface de la plateforme et prend en charge la croissance de la plateforme en Inde. La prise en charge des langues hindi natives garantit que toutes les fonctionnalités, tous les rapports et l’expérience globale de l’utilisateur sont entièrement accessibles aux utilisateurs.

>[!NOTE]
>
>Les certificats de badge générés par le système au format PDF ne prennent pas en charge l’hindi.

Pour modifier la langue de l’interface, procédez comme suit :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur]**.
2. Accédez à **[!UICONTROL Paramètres du profil]** > **[!UICONTROL Langue de l&#39;interface]**.
3. Sélectionnez **[!UICONTROL Hindi]** comme langue d&#39;interface.


## Vérification des blasphèmes pour les publications sur les réseaux sociaux

Adobe Learning Manager bloque désormais les publications sur les réseaux sociaux dans l’application Élèves qui contiennent des mots interdits. Cela permet de maintenir le professionnalisme et la conformité, en particulier dans les domaines sensibles tels que les soins de santé.

## Optimisation du modèle d’e-mail

### Envoyer un e-mail aux élèves lorsqu’un instructeur est affecté

Les adresses e-mail existantes **[!UICONTROL Vous avez été ajouté en tant qu&#39;instructeur]** et les **[!UICONTROL détails de la session VCProvider]** ont été combinés en une seule adresse e-mail **[!UICONTROL Vous avez été ajouté en tant que type d&#39;utilisateur]**. Le **[!UICONTROL type d&#39;utilisateur]** sera soit **[!UICONTROL instructeur]**, soit **[!UICONTROL organisateur]**, en fonction du rôle de l&#39;utilisateur. Ces e-mails n’étaient pas disponibles dans l’interface utilisateur auparavant. Ils ont été regroupés dans un seul e-mail et ajoutés à l’interface utilisateur. Les administrateurs peuvent accéder à ce modèle dans la section **[!UICONTROL Modèle de courrier électronique]**. Elle sera activée par défaut pour tous les comptes nouveaux et existants, mais les administrateurs peuvent la désactiver ou l’activer à partir de la même section. Cet e-mail sera envoyé à chaque création de session et affectation d’un instructeur, que ce soit pour des sessions telles que Zoom, Équipes, Connect ou d’autres services.

### Envoyer un e-mail aux élèves lorsqu’une session est annulée

Les instructeurs qui sont supprimés d’une session ne recevront désormais qu’un e-mail d’annulation de session. Auparavant, ils recevaient un e-mail d’annulation et de mise à jour. Les instructeurs qui restent dans une session recevront un e-mail de mise à jour de la session avec une nouvelle invitation pour la session.

## Critères d’achèvement de MS Teams

Actuellement, les élèves sont marqués comme participants même s&#39;ils rejoignent une session de formation virtuelle avec instructeur (VILT) pendant quelques secondes seulement. Avec cette version, nous avons introduit des critères d’achèvement pour les modules Teams afin d’assurer une présence plus précise. Les auteurs peuvent désormais définir le temps minimum que les élèves doivent passer dans une session VILT pour que leur présence soit comptabilisée.

Il s’agit d’une fonctionnalité d’arrière-plan désactivée par défaut. Contactez votre CSM pour l’activer.

## Mise à jour des nouvelles adresses IP pour la remise des e-mails

Pour améliorer la fiabilité de la diffusion des e-mails, nous ajoutons de nouvelles adresses IP à notre pool existant. Pour garantir une communication par e-mail ininterrompue, mettez à jour les paramètres de messagerie de votre organisation selon vos besoins.

Nous utilisons actuellement les adresses IP suivantes pour la remise des e-mails :

* 149.72.162.66
* 167.89.5.155

Les adresses IP suivantes seront ajoutées à notre pool de diffusion d’e-mails :

* 159.183.228.93
* 159.183.225.26
* 159.183.218.22
* 168.245.57.144

>[!NOTE]
>
>Si nécessaire, nous vous suggérons de collaborer avec votre équipe informatique pour ajouter les adresses IP à la liste des URL autorisées.

## Modifications apportées à la migration

Les modifications suivantes sont apportées au workflow de migration :

* Migrez les modules dans des dossiers spécifiques.
* Ajout de critères d’achèvement pour les modules.
* Ajout de critères d’achèvement pour les cours

### Modifications apportées à la migration des modules

Lorsque vous migrez des modules dans ALM, ils sont enregistrés dans le dossier public par défaut. Dans cette version, nous avons ajouté une nouvelle colonne appelée `folder` dans le fichier [module_version.csv](assets/module_version.csv). Les administrateurs peuvent utiliser cette colonne pour spécifier le nom du dossier où les modules doivent aller après la migration. Les administrateurs peuvent également placer un seul module dans plusieurs dossiers en listant les noms de dossier séparés par des virgules.

La colonne dossier utilise le type de données string et il s&#39;agit d&#39;une colonne facultative. Les conditions suivantes s’appliquent à la colonne Dossier :

* Le nom du dossier que vous ajoutez doit être un dossier de contenu existant dans le compte ALM.
* Les valeurs doivent être des chaînes séparées par des virgules.
* Si vous ajoutez un nouveau nom de dossier pour un module déjà présent dans un autre dossier, la nouvelle valeur ne remplacera pas le dossier attribué. Le module sera ajouté au nouveau dossier et restera également disponible dans le dossier existant.
* Si la valeur est vide, le dossier sera défini par défaut sur **[!UICONTROL Public]**.

Reportez-vous au fichier [module_version csv spec](assets/4-module_version.xlsx) pour plus d&#39;informations.

### Modifications apportées à la migration des modules - critères d’achèvement

Les administrateurs peuvent spécifier les critères d’achèvement des modules pendant la migration des modules. Dans cette version, nous avons ajouté de nouvelles colonnes `completionCriteria`, `viewPercent` et `quizData` dans le [module_version.csv](assets/module_version.csv).

Voici les conditions applicables aux nouvelles colonnes :

1. `completionCriteria` :

   * Le type de données doit être une chaîne de valeurs et les valeurs prises en charge sont :
      * `LAUNCH_CONTENT`
      * `VIEW_PERCENT`
      * `QUIZ`
      * `MARK_COMPLETE`
   * Ajoutez des critères d&#39;achèvement au niveau du module uniquement pour les types de modules d&#39;auto-apprentissage.
   * Les valeurs prises en charge pour le contenu statique sont `LAUNCH_CONTENT` et `VIEW_PERCENT`.
   * Les valeurs prises en charge pour le contenu interactif sont `LAUNCH_CONTENT`, `VIEW_PERCENT` et `QUIZ`.
   * Les valeurs prises en charge pour le contenu HTML5 sont `LAUNCH_CONTENT` et `MARK_COMPLETE`.

2. `viewPercent` :

   * Le type de données de cette colonne doit être un entier et la valeur doit être comprise entre 0 et 100.
   * Lorsque completionCriteria est défini sur `VIEW_PERCENT`, entrez le pourcentage d&#39;affichage requis dans cette colonne ou laissez-le vide.

3. `quizData` :

   * Le type de données doit être une chaîne et les valeurs prises en charge sont `QUIZ_ATTEMPTED`, `QUIZ_PASSED` et `QUIZPASSED_OR_LIMITREACHED`.
   * Lorsque `completionCriteria` est défini sur `QUIZ`, entrez la valeur de quiz appropriée dans la colonne `quizData`.

Reportez-vous au fichier [module_version csv spec](assets/4-module_version.xlsx) pour plus d&#39;informations.

### Changements dans la migration du cours - Critères d’achèvement

Les administrateurs peuvent spécifier les critères d’achèvement des cours pendant la migration des cours. Dans cette version, nous avons ajouté une nouvelle colonne appelée `completionCriteria` dans le [course.csv](assets/course.csv).

Voici les conditions pour la colonne `completionCriteria` :

* Le type de données doit être une chaîne ou un nombre ; il s&#39;agit d&#39;un champ facultatif.
* Les valeurs doivent être `ALL`, `X` et `SELECTEDMODULES`.
* X est une valeur entière qui doit être supérieure à 0 et inférieure au nombre total de modules.
* Si vous définissez `completionCriteria` sur `SELECTEDMODULES`, vous devez marquer les modules obligatoires dans le fichier [course_module.csv](assets/course_module.csv).
* Dans la colonne `optionalCriteria`, saisissez `TRUE` ou `FALSE`. Si vous définissez la valeur sur `TRUE`, le module deviendra obligatoire.

Reportez-vous aux fichiers [spéc csv de cours](assets/3-course.xlsx) et [spéc csv de module de cours](assets/6-course_module.xlsx) pour plus d&#39;informations.

## Modifications de l’API

Voici les modifications apportées à l’API :

* **API de recherche** :
   * Nouveau filtre de mode avec des options : classicSearch et advanceSearch.
   * Nouvelle option loMetadata pour snippetTypes.
* **API d&#39;annonce** :
   * Inclut l’attribut altText pour les descriptions d’en-tête.
* **API d&#39;instance** :
   * Nouvel attribut de paramètres régionaux pour récupérer les détails des paramètres régionaux.
* **Vérification des blasphèmes** :
   * API mises à jour pour vérifier les mots interdits dans les commentaires et les réponses aux publications sur les réseaux sociaux :
* **TPM et limitation de rafale** :
   * Ajout de RPM (demandes par minute) et de limites de rafale pour toutes les API.
* **API de badge** :
   * Nouvel attribut externalProvider pour récupérer les informations sur les badges externes.
* **API de tâche** :
   * Téléchargez le rapport de groupe d’utilisateurs et le rapport d’audit de rôle personnalisé à l’aide de l’API de tâche.

### Modifications apportées à l’API de recherche

L&#39;API de recherche a désormais un nouveau filtre de mode avec deux options : `classicSearch` et `advanceSearch`. Il existe également une nouvelle option `loMetadata` pour `snippetTypes`. Pour obtenir les meilleurs résultats, incluez `loMetadata` dans `snippetTypes` lorsque vous utilisez le mode `advanceSearch`.

### Modifications apportées à l’API d’annonce

L&#39;élément `GET /announcements API` inclut désormais l&#39;attribut `altText` pour fournir la description de l&#39;en-tête.

#### Exemple de requête à l’aide de cURL :

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' 'https://abcd.adobe.com/primeapi/v2/announcements/123456'
```

#### Exemple de réponse :

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/announcements/123456"
  },
  "data": {
    "id": "12345",
    "type": "adminAnnouncement",
    "attributes": {
      "actionUrl": "google.com",
      "announcementType": "MASTHEAD",
      "expiryDate": "2038-01-19T03:14:07.000Z",
      "liveDate": "2024-07-31T11:11:30.000Z",
      "contentMetaData": [
        {
          "contentType": "IMAGE",
          "contentUrl": "https://abcd.adobe.com",
          "locale": "en-US",
          "altText": "Moonlight - english changed new",
          "thumbnailUrl": "https://abcd.adobe.com/"
        },      ]
    }
  }
}
```

### Modifications apportées aux API d’instance

Le nouvel attribut `locale` a été ajouté aux API suivantes pour récupérer les détails des paramètres régionaux.

* `GET /learningObjects/{loId}/instances/{loInstanceId}`
* `GET /learningObjects/{id}?include=instances,enrollment.loInstance`
* `GET /learningObjects?include=instances,enrollment.loInstance`
* `GET /learningObjects/{id}/relatedLOs?include=instances,enrollment.loInstance`
* `POST /learningObjects/query?include=instances,enrollment.loInstance`
* `POST /search/query?include=model.instances`
* `GET /search?include=model.instances`

#### Exemple de requête à l’aide de cURL :

```
curl --location 'http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567' \
```

#### Exemple de requête :

```
{
    "links": {
        "self": "http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567"
    },
    "data": {
        "id": "course:1234567_1234567",
        "type": "learningObjectInstance",
        "attributes": {
            "dateCreated": "2024-02-27T09:21:25.000Z",
            "isAET": false,
            "isDefault": true,
            "isFlexible": false,
            "locale": "en-US",
            "state": "Active",
            "localizedMetadata": [
                {
                    "locale": "en-US",
                    "name": "Default instance"
                }
            ]
        },
        "relationships": {
            "learningObject": {
                "data": {
                    "id": "course:1234567",
                    "type": "learningObject"
                }
            },
            "loResources": {
                "data": [
                    {
                        "id": "course:123456_1234567_1234567_1",
                        "type": "learningObjectResource"
                    }
                ]
            }
        }
    }
}
```

### Modifications d’API publiques pour le contrôle des blasphèmes

Les API suivantes ont été mises à jour pour effectuer des vérifications de blasphèmes pour les commentaires et les réponses sur les publications sur les réseaux sociaux.

* `POST /boards/{id}/posts `
* `PATCH /posts/{id}`
* `POST /posts/{id}/comments`
* `PATCH /comments/{id}`
* `POST /comments/{id}/replies`
* `PATCH /replies/{id}`

Si un mot restreint est trouvé dans la publication, la réponse suivante sera envoyée.

#### Exemple de réponse :

```
{
  "status": "FORBIDDEN",
  "title": "BAD_WORD_FOUND",
  "source": {
    "info": "Unacceptable word found in post"
  }
}
```

### Modifications du régime et de la limitation de rafale

Dans cette version, des limites de RPM (demandes par minute) et de rafale ont été ajoutées pour toutes les API. Le RPM maximal pour chaque API peut être vérifié sur la page Swagger.

RPM correspond au nombre de demandes que vous pouvez envoyer au serveur API en une minute. La limite de rafale permet un nombre plus élevé de requêtes pendant une courte durée, dépassant la limite de cadence habituelle. Par exemple, l&#39;API `learningObject` autorise un maximum de 15 demandes par minute. Si cette limite est dépassée, l’API renvoie un message d’erreur.

### Modifications apportées aux API de badge

Le nouvel attribut `externalProvider` a été ajouté aux API suivantes pour récupérer des informations sur les badges externes, y compris l&#39;ID de badge et le nom du fournisseur.

* `GET /badges `
* `GET /badges/{id}`
* `GET /skills?include=levels.badge`
* `GET /skills/{id}?include=levels.badge`
* `GET /learningObjects/{loId}/instances/{loInstanceId}?include=badge`
* `GET /users/{userId}/userBadges`
* `GET /users/{userId}/userBadges/{id}`

#### Exemple de requête à l’aide de cURL :

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 123456789' 'https://abcd.adobe.com/primeapi/v2/badges/44'
```

#### Exemple de réponse :

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/badges/44"
  },
  "data": {
    "id": "44",
    "type": "badge",
    "attributes": {
      "imageUrl": "https://abcd.com/accountassets/1/badges/download.png",
      "name": "external badge",
      "state": "Active",
      "externalProvider": {
        "id": "1234sjd-b272-4de1-9b60-1234567",
        "provider": "credly"
      }
    }
  }
}
```

### Téléchargement des rapports d’audit de groupe d’utilisateurs et de rôle personnalisé via l’API de tâche

L&#39;utilisateur peut télécharger le **[!UICONTROL rapport de groupe d&#39;utilisateurs]** et le **[!UICONTROL rapport d&#39;audit de rôle personnalisé]** à l&#39;aide de `Job API`.

#### Exemple de demande de téléchargement de rapport de groupe d’utilisateurs :

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' -d '{ \ 
     "data": { \ 
         "type": "job", \ 
         "attributes": { \ 
             "jobType": "generateUserGroupReport" \ 
         } \ 
    } \ 
 }' 'https://abcd.adobe.com/primeapi/v2/jobs'
```

#### Exemple de demande de téléchargement du rapport d’audit de rôle personnalisé :

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 1234567' -d '{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateCustomRoleAuditReport",
            "payload":{
                 "fromDate": "2020-01-01T18:30:00.000Z",
                 "toDate": "2024-09-31T18:30:00.000Z",
                 "locale":  "en-US"
            }
        }
   }
}
```

### Message d’erreur indiquant l’absence de corps de la demande

Nous avons introduit des messages d’erreur spécifiques pour les cas où le corps de la demande est obligatoire mais n’est pas fourni dans l’API.

#### Exemple de message d’erreur :

```
{
    "status": "BAD_REQUEST",
    "title": "Generic Error"
}
```

## Améliorations des rapports

Les administrateurs peuvent trouver ces modifications de rapport dans la section **Administrateur** > **Rapports**.

### Rapport Relevés de notes d’apprentissage

Le rapport **[!UICONTROL Relevés de notes d&#39;apprentissage]** contiendra deux nouvelles colonnes :

* **[!UICONTROL ID de module]** : affiche l&#39;identifiant unique de chaque module. Cette nouvelle colonne a été ajoutée après la colonne **[!UICONTROL Module]** existante.
* **[!UICONTROL ID d&#39;instance de cours]** : affiche l&#39;identifiant unique de chaque instance de cours. Cette nouvelle colonne a été ajoutée après la colonne **[!UICONTROL Instance]** existante.
* **[!UICONTROL Commentaire d&#39;achèvement]** : cette colonne capture les commentaires saisis par l&#39;administrateur lors du marquage de l&#39;achèvement de l&#39;utilisateur. Cette nouvelle colonne a été ajoutée à la fin du rapport.


### Rapport récapitulatif de la session

Le rapport **[!UICONTROL Résumé de la session]** contiendra trois nouvelles colonnes :

* La colonne **[!UICONTROL ID de module]** a été ajoutée avant la colonne **[!UICONTROL Nom de la session]**.
* La colonne **[!UICONTROL ID de session]** a été ajoutée avant la colonne **[!UICONTROL Nom de session]**.
* La colonne **[!UICONTROL ID d&#39;instance de cours]** a été ajoutée après la colonne **[!UICONTROL Nom de l&#39;instance]**.
* **[!UICONTROL Nombre d&#39;achèvements]** a été ajouté après la colonne **[!UICONTROL Nombre d&#39;inscriptions]**.

## Bogues corrigés dans cette mise à jour

* Correction de l’erreur qui se produisait lors du chargement de vidéos à partir du module d’activité lors de l’envoi de fichiers sur les appareils Android et iOS.
* Correction d’un problème d’ouverture de cours sur l’application mobile. La version web fonctionne correctement.
* Correction du problème d’affichage des assistances à la tâche et d’autres ressources dans Safari.
* Correction d’un problème qui empêchait les utilisateurs de télécharger des assistances à la tâche sur l’application mobile.
* Correction de l’erreur dans la documentation de l’API Patch User.
* Correction d’un problème en raison duquel les organisateurs ne recevaient pas de notifications par e-mail lorsqu’une session était supprimée du cours.
* Correction d’un problème en raison duquel les organisateurs ne recevaient pas d’e-mails d’annulation de session lorsqu’un module était supprimé du cours et republié.
* Ajout de la prise en charge de l’inclusion des caractères spéciaux « + » et « - » dans les adresses électroniques lors de la création d’utilisateurs externes.
* Correction d’un problème en raison duquel la synchronisation du rapport unifié du connecteur Marketo échouait si le rapport de compétences de l’utilisateur contenait des guillemets doubles dans la valeur d’enregistrement CSV.
* Correction d’un problème en raison duquel le point de terminaison `/skills` renvoyait l’état correct pour l’API d’administration, mais que l’API de l’élève affichait systématiquement des données incorrectes ou mises en cache.
* Correction d’un problème d’intégration Go1 pour les cours freemium qui échouait lorsque le connecteur Go1 n’était pas configuré sur le compte.
* Correction d’un problème en raison duquel les cours du parcours d’apprentissage ne sont pas accessibles via la migration si l’élève a déjà terminé le parcours d’apprentissage.
* Correction d’un problème en raison duquel le fichier CSV de l’utilisateur incrémentiel échouait lorsque le gestionnaire de l’utilisateur et le gestionnaire de niveau d’erreur étaient définis en tant que SU (Super utilisateur) au lieu d’administrateur et n’étaient pas inclus dans le fichier CSV.
* Correction des problèmes d&#39;étendue pour les responsables de magasins dans les rapports de tableau de bord.
* Correction d’un problème en raison duquel xapi_iri n’était pas supprimé lorsqu’un brouillon de cours était supprimé.
* Correction d’un problème qui empêchait l’ajout d’un ID d’objet d’apprentissage unique dans certains scénarios.
* Correction d’un problème en raison duquel la propriété IsEmbeddable du plan d’apprentissage ne se mettait pas correctement à jour dans les plans d’apprentissage partagés.
* Correction d’un problème affectant l’affichage de la durée totale des parcours d’apprentissage dans la vue de l’élève.
* Correction d’un problème qui permettait aux élèves de s’inscrire ou de s’inscrire via des liens d’auto-inscription même après la suppression de leur compte.
* Correction d&#39;un problème en raison duquel `www` était supprimé lors de l&#39;ajout de liens dans la description du cours lors de la création du cours.
* Correction d’un problème en raison duquel les assistances à la tâche de masquage et de téléchargement ne fonctionnaient pas correctement.
* Correction d’un problème en raison duquel l’authentification unique (SSO) ne fonctionnait pas pour les nouveaux utilisateurs ajoutés via le lien d’auto-inscription avec un ID IP.
* Correction d’un problème en raison duquel les données du message de notification n’étaient pas récupérées après la suppression d’une annonce.
* Correction du problème de résultats de recherche insuffisants lors de la recherche d’utilisateurs par e-mail.

## Configuration système

Voir [Configuration requise pour Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notes de mise à jour

Consultez les [notes de mise à jour](/help/migrated/release-note/release-notes.md) pour connaître les dernières mises à jour.

## Versions précédentes d’Adobe Learning Manager

* [Version de juillet 2024](/help/migrated/whats-new-july-2024.md)
* [Version de mars 2024](/help/migrated/whats-new-march-2024.md)
