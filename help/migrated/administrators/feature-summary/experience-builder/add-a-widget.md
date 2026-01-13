---
title: Ajout et configuration de widgets dans Experience Builder
description: Découvrez comment ajouter, personnaliser et configurer divers widgets dans Experience Builder dans Adobe Learning Manager. Ce guide couvre les widgets couramment utilisés tels que les calendriers, les catégories, l’état de conformité, les cours et les parcours, la ludification, le contenu de HTML, les IFrames, l’apprentissage par les réseaux sociaux, etc.
jcr-language: en-us
source-git-commit: 7fe4576e2a90b27f51d035f01a30ce3a818b95c2
workflow-type: tm+mt
source-wordcount: '2483'
ht-degree: 0%

---


# Ajout et configuration de widgets

## Widget Calendrier

Le widget Calendrier affiche vos sessions et formations planifiées. Vous pouvez parcourir le calendrier pour afficher les formations prévues pour les mois à venir. Il permet de visualiser les sessions de formation par mois avec la possibilité de faire défiler vers la gauche ou la droite.

Le widget Calendrier peut être ajouté à une page par un administrateur pour afficher les plannings de formation. Les élèves peuvent interagir avec le calendrier en faisant défiler les mois pour voir les sessions à venir. Ils peuvent filtrer les sessions pour trouver rapidement une formation pertinente.

### Ajout d’un widget Calendrier

Dans une société financière dotée d’équipes distinctes de Sales Manager (CSM) et de Customer Success Manager (CSM), les administrateurs peuvent utiliser ce widget pour mettre en avant des sessions de formation spécifiques à l’équipe. Par exemple :

* L’équipe commerciale peut consulter les sessions à venir sur les mises à jour de produits, les formations sur la conformité et les ateliers de présentation.
* L&#39;équipe CSM peut consulter les ateliers d&#39;intégration des clients, la formation en communication avec les clients et les programmes d&#39;excellence du service.

Pour configurer le widget Calendrier :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Calendrier]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-calendar.png)
   _Écran de sélection du widget mettant en évidence l&#39;option du widget Calendrier pour afficher les sessions de formation dans un calendrier_

8. Saisissez un **[!UICONTROL titre de widget]** et une **[!UICONTROL description de widget]**.

   ![](assets/configure-calendar-widget.png)
   _Écran de personnalisation du widget Calendrier, où les administrateurs peuvent définir le titre du widget, la description et sélectionner des catalogues_

9. Sélectionnez un catalogue en recherchant pour afficher ses cours et parcours d&#39;apprentissage dans le widget **[!UICONTROL Calendrier]**.
10. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget Calendrier sera ajouté à la page. L’administrateur peut ajouter d’autres widgets et publier la page.

>[!NOTE]
>
>Si aucun catalogue n’est sélectionné, les sessions de tous les catalogues s’affichent.

## Widget Catégories

Le widget Catégories affiche le contenu de formation organisé par Catalogues, Produits ou Rôles sous forme de catégories. Cela permet aux élèves de parcourir et de trouver facilement des formations regroupées par sujets, services, compétences ou autres classifications pertinentes.

Les administrateurs ajoutent le widget Catégories à une page pour présenter les options d’apprentissage classées. Les élèves utilisent le widget pour explorer la formation en sélectionnant une catégorie d’intérêt, qui révèle ensuite les cours ou les parcours associés.

Consultez les articles [Catalogues](/help/migrated/administrators/feature-summary/catalogs.md) et [Recommendations](/help/migrated/recommendations-adobe-learning-manager.md) pour en savoir plus sur la configuration des catalogues et les recommandations.

<b>Remarque</b> : dans le widget Catégories, lorsque Catalog est sélectionné, la liste est triée par date de création par défaut. Les catalogues créés plus récemment apparaissent en premier.

### Ajouter un widget de catégorie

Dans une entreprise de services financiers, différentes équipes ont souvent besoin d’accéder à une formation spécifique à leur rôle. Le widget Catégories permet d’organiser le contenu de formation en vignettes claires cliquables, ce qui permet aux équipes commerciales et CSM de trouver rapidement ce dont elles ont besoin.

Pour configurer le widget Catégories :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Catégories]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-categories-widget.png)
   _Écran de sélection du widget affichant l’option du widget Catégories pour organiser le contenu d’apprentissage par catalogue, produit ou rôle afin de faciliter la navigation_

8. Sélectionnez les détails à afficher sur les fiches de catégorie :

   * **[!UICONTROL Image de catégorie]**
   * **[!UICONTROL Description de la catégorie]**

9. Saisissez un **[!UICONTROL titre de widget]** et une **[!UICONTROL description de widget]**.
10. Recherchez et choisissez un catalogue dans la **[!UICONTROL source des catégories]**.

   ![](assets/configure-calendar-widget.png)
   _Configurez les options du widget Catégories pour définir le titre et la description du widget, puis sélectionnez la source de la catégorie_

11. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget Catégories sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget Conformité

Le widget État de conformité affiche la progression de l’élève vers la conformité ou la certification. Elle indique l’état de la formation obligatoire affectée à l’utilisateur, y compris les cours terminés, en attente ou en retard.

Les administrateurs ajoutent le widget État de conformité aux pages pour fournir une visibilité sur la progression de la formation à la conformité. Les élèves l&#39;utilisent pour vérifier rapidement quels cours obligatoires ils ont terminés et lesquels nécessitent encore une attention.

### Ajout d’un widget d’état de conformité

Dans une société de services financiers, l’équipe commerciale et l’équipe du gestionnaire de succès client (CSM) doivent suivre la formation sur la conformité à temps. Le widget État de conformité permet aux élèves de suivre plus facilement les échéances à venir et la progression de leur formation directement à partir des pages spécifiques à leur équipe.

Pour configurer le widget Conformité :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL État de conformité]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-compliance-status.png)
   _Écran de sélection du widget mettant en évidence le widget État de conformité utilisé pour afficher les inscriptions d&#39;élèves avec des échéances et des indicateurs d&#39;état_

8. Saisissez un **[!UICONTROL titre de widget]** et une **[!UICONTROL description de widget]**.

   ![](assets/configure-compliance.png)
   _Écran du widget État de conformité, où les administrateurs peuvent définir le titre et la description du widget pour afficher les échéances d&#39;inscription et le statut des élèves_

9. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget d’état de conformité sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget Cours et parcours

Le widget Cours et parcours affiche les cours et parcours d’apprentissage recommandés, adaptés au rôle, aux intérêts ou aux besoins de formation de l’élève.

Les administrateurs ajoutent le widget Cours et parcours aux pages pour mettre en évidence le contenu de formation clé pour des publics spécifiques. Les élèves utilisent le widget pour parcourir les cours ou les parcours recommandés et peuvent s’inscrire directement aux cours.

### Ajout d’un widget Cours et parcours

Une société financière souhaite créer des pages de formation spécifiques à chaque rôle pour ses deux équipes : Responsables des ventes et de la réussite client (CSM). Le widget Cours et parcours peut être utilisé pour afficher les programmes d’apprentissage les plus pertinents pour chaque équipe.

Pour configurer le widget Cours et parcours :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Cours et parcours]**.

   ![](assets/select-course-path.png)
   _Écran de sélection du widget affichant le widget Cours et parcours pour afficher les cours, les parcours d’apprentissage, les certifications et les assistances à la tâche sous forme de cartes interactives pour les élèves_

8. Sélectionnez **[!UICONTROL Continuer]**.
9. Saisissez **[!UICONTROL Titre du widget]** et **[!UICONTROL Description du widget]**.
10. Sélectionnez les catalogues ou choisissez manuellement jusqu’à 25 cours à afficher.

![](assets/configure-course-paths.png)
_Widget Cours et parcours où les administrateurs définissent le titre et la description du widget, et sélectionnent les cours ou parcours d’apprentissage à afficher sous forme de cartes interactives_
11. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget Cours et parcours sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget Zone de contenu

Le widget Zone de contenu permet aux administrateurs d’ajouter du contenu personnalisé, tel que du texte, des images, des annonces ou des liens, à une page. Il offre un espace flexible pour partager des informations importantes, des conseils, des mises à jour ou des messages promotionnels directement dans l’environnement d’apprentissage.

### Ajout d’un widget Zone de contenu

Une société financière souhaite créer des pages de formation spécifiques à chaque rôle pour ses deux équipes : Responsables des ventes et de la réussite client (CSM). Le widget Zone de contenu peut être utilisé pour ajouter des sections personnalisées avec des titres, des descriptions, des images et des boutons d’appel à l’action qui partagent des ressources ciblées, des mises à jour et des messages de motivation.

Pour configurer le widget Zone de contenu :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Zone de contenu]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-content-box.png)
   _Écran de sélection du widget mettant en évidence le widget Zone de contenu pour afficher des images, du texte et des boutons d&#39;action personnalisés afin d&#39;améliorer l&#39;engagement des élèves_

8. Saisissez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]**.
9. Saisissez le texte dans le **[!UICONTROL libellé du bouton d&#39;action]** et fournissez un lien.
10. Sélectionnez l’une des options de remplissage d’arrière-plan :

   * **[!UICONTROL Couleur]** : sélectionnez la couleur dans le sélecteur de couleurs ou saisissez le code couleur dans le champ de texte.
   * **[!UICONTROL Image]** : parcourez et chargez une photo.

11. Ajustez la hauteur de la zone à l&#39;aide de l&#39;option **[!UICONTROL Hauteur de la zone de contenu]**.
12. Sélectionnez les options de mise en forme du texte.

   ![](assets/configure-content-box.png)
   _Écran de personnalisation du widget Zone de contenu, où les administrateurs peuvent saisir un titre, une description, un libellé de bouton d&#39;action et un lien_

13. Sélectionnez **[!UICONTROL Ajouter des widgets]**.

Le widget Zone de contenu sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget Ludification

Les administrateurs ajoutent le widget Ludification aux pages personnalisées pour présenter les réussites des élèves, telles que les badges gagnés, les points accumulés et le classement dans le classement. Les élèves peuvent suivre leurs progrès et comparer les résultats avec leurs pairs, ce qui favorise la motivation et la participation soutenue.

### Ajout d’un widget Ludification

Une société financière souhaite stimuler l’engagement et la motivation des élèves au sein de ses deux principales équipes : les directeurs commerciaux et les gestionnaires de la réussite client (CSM). Le widget de ludification peut être utilisé pour récompenser les élèves avec des points, des badges et des classements dans le classement pour avoir suivi la formation et participé activement.

Pour l’équipe commerciale, la ludification pourrait se concentrer sur la récompense des réalisations liées aux compétences commerciales, à la connaissance des produits et à la formation à l’engagement client. Pour l&#39;équipe CSM, cela peut mettre l&#39;accent sur les certifications du service client, la formation à la conformité et les compétences en gestion client.

Pour configurer le widget Ludification :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Ludification]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-gamification.png)
   _Écran de sélection du widget mettant en évidence le widget de ludification utilisé pour afficher les activités d&#39;apprentissage et les réussites sur le tableau des scores_

8. Saisissez le **[!UICONTROL titre du widget]** et la **[!UICONTROL description du widget]**.
9. Sélectionnez **[!UICONTROL Ajouter des widgets]**.

Le widget Ludification sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget HTML

Le widget de HTML permet aux administrateurs d’intégrer du code de HTML personnalisé directement dans une page. Vous bénéficiez ainsi d’une plus grande souplesse pour ajouter du contenu personnalisé, intégrer des outils tiers ou inclure des éléments interactifs qui vont au-delà de la fonctionnalité standard du widget. Il prend en charge une personnalisation complète via HTML, CSS et même JavaScript, permettant des conceptions uniques et des intégrations externes au sein de la plateforme d’apprentissage.

### Ajout d’un widget HTML

Une société financière veut offrir du contenu personnalisé et interactif adapté à ses deux principales équipes : les directeurs commerciaux et les gestionnaires de la réussite client (GSE). Le widget HTML permet d’intégrer des ressources personnalisées basées sur le HTML, telles que des tableaux de bord financiers, des visualisations de données, des formulaires interactifs ou des outils d’analyse de marché, directement dans les pages dédiées à la formation ou à l’équipe.

Pour configurer le widget de HTML :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL HTML]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-html.png)
   _Écran de sélection du widget affichant le widget de HTML pour personnaliser les pages à l&#39;aide de HTML, CSS et de code JavaScript_

8. Saisissez votre code **[!UICONTROL HTML]**, **[!UICONTROL CSS]** et **[!UICONTROL JavaScript]** dans les champs respectifs.
9. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget de HTML sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget IFrame

Le widget Iframe affiche le contenu d’une URL externe directement dans une page de la plate-forme d’apprentissage. Il intègre un site Web, un outil ou une application externe dans un cadre, ce qui permet aux élèves de visualiser ce contenu et d’interagir avec lui sans quitter le LMS.

### Ajouter un widget Iframe

Une société financière souhaite intégrer de manière transparente des outils et des ressources externes dans ses pages de formation et de collaboration internes pour ses équipes de responsables des ventes et de la réussite client (CSM). Le widget Iframe peut être utilisé pour afficher des tableaux de bord financiers tiers, des plateformes d’analyse de marché ou des portails de gestion de clients directement dans l’interface LMS.

Pour configurer le widget Iframe :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Iframe]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-iframe.png)
   _Écran de sélection du widget affichant le widget Iframe pour incorporer des applications externes ou des pages web dans une section sélectionnée_

8. Saisissez l&#39;URL dans l&#39;option **[!UICONTROL Page liée au bouton Action]**.
9. Ajustez la hauteur de l&#39;iframe à l&#39;aide de l&#39;option **[!UICONTROL Hauteur d&#39;iframe]**.

   ![](assets/configure-iframe.png)
   _Écran de personnalisation du widget Iframe, où les administrateurs peuvent saisir une URL de page et spécifier la hauteur de l&#39;iframe pour intégrer du contenu externe_

10. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget Iframe sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

Les administrateurs doivent inclure le jeton d’accès en tant que paramètre de requête dans l’URL iframe pour récupérer les informations correctes. Par exemple, pour afficher des informations de Adobe Learning Manager dans un iframe, l’URL doit inclure les paramètres suivants :

* userId : identifiant unique de l’élève
* accountId : Identifiant de compte associé à l’élève
* jeton : jeton d’authentification requis pour les appels API
* locale : langue de l’élève ou préférence de langue

## Widget Mon apprentissage

Le widget Mon apprentissage fournit aux élèves une vue personnalisée de tous les cours, programmes d’apprentissage et certifications qui leur sont attribués ou auxquels ils s’inscrivent. Il organise le contenu d’apprentissage par type et par échéance, ce qui permet aux élèves de suivre facilement leur progression et d’accéder au matériel d’apprentissage. Ce widget aide les élèves à rester concentrés sur la formation dont ils ont besoin et à voir brièvement les échéances à venir.

### Ajout d’un widget Mon apprentissage

Une entreprise financière souhaite offrir des expériences d&#39;apprentissage personnalisées adaptées à ses deux principales équipes : les directeurs commerciaux et les gestionnaires de la réussite client (GSE). Le widget Mon apprentissage peut être utilisé pour offrir à chaque membre de l’équipe une vue consolidée des cours qui lui sont attribués, des parcours d’apprentissage en cours et des certifications.

Pour configurer le widget Mon apprentissage :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Mon apprentissage]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-my-learning.png)
   _Écran de sélection du widget, mettant en surbrillance le widget Mon apprentissage utilisé pour afficher la liste personnalisée des cours inscrits de l’élève_

8. Saisissez le **[!UICONTROL titre du widget]** et la **[!UICONTROL description du widget]**.
9. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget Mon apprentissage sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Widget Apprentissage par les réseaux sociaux

Le widget Apprentissage par les réseaux sociaux permet aux élèves d’interagir, de partager des idées et de collaborer au sein de la plateforme d’apprentissage. Il prend en charge la publication de différents types de contenu, tels que du texte, des vidéos, de l’audio, des captures d’écran, des questions et des sondages. Les élèves peuvent commenter, répondre, voter pour ou contre les publications, ce qui favorise le partage des connaissances et l&#39;engagement entre pairs. Ce widget crée un espace d’apprentissage informel qui complète la formation formelle en encourageant l’interaction sociale et l’apprentissage continu.

### Ajout d’un widget Apprentissage par les réseaux sociaux

Une société financière souhaite la collaboration et le partage de connaissances entre ses deux principales équipes : les directeurs commerciaux et de succès client (CSM). Le widget Apprentissage par les réseaux sociaux peut être utilisé pour créer des espaces interactifs où les membres de l’équipe peuvent poser des questions, partager les bonnes pratiques, charger du contenu utile et engager des discussions.

Pour configurer le widget Apprentissage par les réseaux sociaux :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Identité visuelle]** dans le volet de navigation de gauche.
3. Sélectionnez **[!UICONTROL Pages personnalisées]**.
4. Sélectionnez la page requise, puis **[!UICONTROL Conception de page]**.
5. Sélectionnez **[!UICONTROL Modifier]**, puis sélectionnez la mise en page.
6. Sélectionnez **[!UICONTROL Ajouter un widget]**.
7. Sélectionnez **[!UICONTROL Apprentissage par les réseaux sociaux]**, puis **[!UICONTROL Continuer]**.

   ![](assets/select-social-learning.png)
   _Écran de sélection du widget mettant en évidence le widget Apprentissage par les réseaux sociaux pour afficher des publications visant à encourager la collaboration et l’engagement_

8. Saisissez le **[!UICONTROL titre du widget]** et la **[!UICONTROL description du widget]**.
9. Sélectionnez **[!UICONTROL Ajouter un widget]**.

Le widget Apprentissage par les réseaux sociaux sera ajouté à la page. Les administrateurs peuvent ajouter d’autres widgets et publier la page.

## Étape suivante

Après avoir configuré les widgets sur les pages, utilisez les menus pour organiser et regrouper les pages.
