---
title: Création et personnalisation d’un certificat
description: Les certificats personnalisés dans Adobe Learning Manager (ALM) permettent aux administrateurs et aux auteurs de concevoir, gérer et émettre des certificats personnalisés pour les élèves.
jcr-language: en-us
exl-id: 99e20f00-9f8f-477f-9416-24636ed23b87
source-git-commit: 0d4e8f06c3a9a3dcd6461036ec7fbfa4a54c0b58
workflow-type: tm+mt
source-wordcount: '2845'
ht-degree: 0%

---

# Certificats personnalisés dans Adobe Learning Manager

## Introduction

Les certificats personnalisés dans Adobe Learning Manager changent la façon dont les administrateurs conçoivent, gèrent et délivrent les certificats d’achèvement.

Les administrateurs peuvent :

- Créez des certificats dans un éditeur visuel de type zone de travail au lieu d’écrire du code.
- Joignez des certificats à des cours, des parcours d’apprentissage et des certifications avec des valeurs par défaut flexibles.
- Utilisez des arrière-plans génératifs optimisés par l’Adobe Firefly tout en gardant à l’esprit les besoins en matière de marque et de conformité.

  >[!NOTE]
  >
  >La fonction IA Firefly n’est pas disponible pour les clients FedRAMP.

- Migrez à partir des modèles de HTML existants et restez compatible avec les dossiers historiques des élèves.

Le processus de certification suit le modèle de badge et de réussite existant dans Learning Manager, de sorte que le comportement de l’élève reste familier tandis que les administrateurs et les équipes d’assistance passent moins de temps sur les opérations de certification.

>[!NOTE]
>
>Les fonctionnalités de certificat qui utilisent l’IA générative sont soumises à un quota. La limite est de 10 000 demandes par client.

## Principales fonctionnalités de la certification personnalisée

### Concepteur de certificats (éditeur de style canevas)

Un concepteur de certificats par glisser-déposer fournit une zone de travail WYSIWYG (what-you-see-is-what-you-get) où les administrateurs peuvent créer et gérer des conceptions sans compétences en HTML ou en CSS.

**Modification visuelle**

- Faites glisser, positionnez, redimensionnez, inversez et faites pivoter le texte et les images.
- Aligner les éléments (haut, bas, gauche, droite) ; les déplacer vers l’arrière ou vers l’avant.
- Dupliquez ou dupliquez des éléments pour une mise en page plus rapide.

**Éléments pris en charge**

- Champs de texte avec commandes de police, de couleur, de taille et d’alignement.
- Espaces réservés dynamiques (par exemple, nom de l’élève, nom du cours ou de la certification, date, champs de compte et champs utilisateur actifs où seuls les attributs à valeur unique sont autorisés).
- Les images, y compris les logos et les badges, avec un redimensionnement manuel préférable à l’ajustement automatique pour une mise en page prévisible.

**Arrière-plan et mise en page**

- Orientation portrait ou paysage (fixe après la création).
- Des arrière-plans en couleurs unies ou en images avec transparence réglable.
- Galerie d’images avec images prédéfinies et arrière-plans partagés.
- Commandes de zoom (50 %-150 %) et alignement de la grille ou alignement par accrochage.

**Localisation**

- Prise en charge de plusieurs paramètres régionaux, chaque paramètre régional ayant son propre fichier de mise en page.
- Lorsque vous ajoutez des paramètres régionaux, sa mise en page est copiée à partir des paramètres régionaux par défaut et peut ensuite être personnalisée.
- Liste déroulante Langue avec un aperçu par langue au moment de la conception.

**Cycle de vie de brouillon et de publication**

- Enregistrez les designs sous forme de brouillons ; les brouillons ne peuvent pas être utilisés pour l’émission.
- Après la publication, la structure du design est verrouillée ; certaines modifications peuvent nécessiter la duplication du design à la place.
- Aperçu dans le PDF en temps réel pour vérifier la mise en page avant la publication.

### Catalogue et liste de modèles

La page de liste **Conception de certificat** aide les administrateurs à gérer les modèles de certificat à grande échelle :

- Catalogue basé sur les mosaïques avec onglets **Publié** et **Brouillon**.
- Rechercher par titre de certificat ; filtrer par **Orientation**.
- Actions sur chaque conception :
   - Dupliquer (pour les variantes).
   - Définissez par défaut au niveau **Compte**, **Cours**, **Parcours d’apprentissage** ou **Certification**.
   - Retirez ou désactivez les modèles qui ne sont plus utilisés.
- Prise en charge des modèles de fournisseur tiers qui peuvent être intégrés et réutilisés.

### Configuration et héritage flexibles

Les administrateurs peuvent configurer les certificats à plusieurs niveaux :

**Valeurs par défaut au niveau du compte**

- Définissez une conception de certificat par défaut pour tous les nouveaux objets d’apprentissage.
- La valeur par défaut sert de point de départ ; les objets d’apprentissage existants ne sont pas modifiés automatiquement lorsque la valeur par défaut du compte est modifiée.

**Remplacements au niveau de l’instance**

- Configuration au niveau de l’instance pour les cours, les certifications et les parcours d’apprentissage, notamment :
   - Identité visuelle par cohorte (par exemple, pour différentes régions ou différents comptes de partenaire).
   - Différentes conceptions de certificats pour les cycles de certification récurrents.

**Résolution et secours des certificats**

Lorsqu’un élève termine la formation, Learning Manager choisit une conception dans cet ordre :

- Configuration de l’instance LO
- Configuration de l’objet d’apprentissage
- Modèle LO par défaut
- Modèle de compte par défaut

### Arrière-plans génératifs alimentés par l’Adobe Firefly

>[!NOTE]
>
>La fonction IA Firefly n’est pas disponible pour les clients FedRAMP.

Pour aider les clients à produire des certificats de marque cohérents à grande échelle, le designer s’intègre à Adobe Firefly :

- Les administrateurs génèrent des arrière-plans à partir d’invites de mots-clés et d’une palette de couleurs (par exemple, « minimaliste, santé, palette bleu-vert »).
- Une bibliothèque de mots-clés organisée prend en charge les industries courantes (expédition, soins de santé et autres) pour les utilisateurs qui ne sont pas des designers.
- Les images générées sont ajoutées à la galerie en arrière-plan et peuvent être réutilisées entre les modèles.
- Les crédits et la hiérarchisation pour l’utilisation du Firefly dans Learning Manager sont définis par la politique du produit.

### Migration de certificat de HTML hérité

Les modèles de HTML ou de certificat ZIP existants sont conservés, mais ne peuvent pas être modifiés dans le nouveau concepteur :

- Les modèles hérités sont migrés avec des indicateurs tels que `isLegacy` / `is_active`.
- Ils apparaissent sous la forme d’entrées non modifiables (pas d’aperçu WYSIWYG) et restent valides pour une utilisation historique.
- Lorsque des badges étaient liés à des modèles hérités, la migration permet de télécharger les certificats. Lorsque la configuration ne peut pas être conservée, des valeurs par défaut globales s’appliquent.

### Génération et précuisson PDF

Pour améliorer les performances d’exécution et l’expérience de l’élève :

- Les certificats sont préconfigurés au moment de l’achèvement (lorsque l’objet d’apprentissage se termine), puis mis en cache pour que les élèves puissent les télécharger rapidement.
- Les flux d&#39;élèves existants pour le téléchargement de certificats via des **badges** et des **réussites** restent les mêmes.

## Le défi

Aujourd’hui, la gestion des certificats dans Learning Manager repose sur un modèle à codage élevé et à prise en charge importante :

**Forte dépendance vis-à-vis des équipes CSM et d&#39;assistance** : les administrateurs fournissent des fichiers HTML ou ZIP que les CSM ou les ingénieurs chargent via des outils internes. Chaque changement (branding, logos, texte réglementaire, signatures) nécessite un ticket interne et un cycle de déploiement.

**Agilité limitée pour les équipes métier** : les équipes marketing, de conformité ou de RH ont souvent besoin de mises à jour de certificats fréquentes et localisées (langues, campagnes, règles spécifiques au pays). Le workflow actuel ralentit ces mises à jour et retarde les programmes de conformité.

**Configuration fragmentée et héritage incertain** : les modèles de HTML hérités peuvent être définis au niveau du compte, de l&#39;objet d&#39;apprentissage par défaut et de l&#39;objet d&#39;apprentissage avec des règles de secours complexes. Sans une configuration personnalisée à plusieurs niveaux claire, il peut être difficile de voir quel modèle s’applique où.

**Les contraintes de liaison des badges** Les certificats sont étroitement liés aux **badges** :

- Un certificat doit être associé à un badge ; il n’y a pas d’émission de certificat uniquement.
Ce couplage peut compliquer les modifications de conception lorsque les administrateurs veulent des certificats sans éléments de ludification.

**Création non visuelle et incohérence de la marque** : les certificats basés sur le HTML sont flexibles, mais nécessitent des compétences en amont dont de nombreux administrateurs ne disposent pas. Certains clients s’appuient sur des certificats par défaut génériques, ce qui affaiblit la cohérence de la marque.

**Écart concurrentiel** : certains systèmes de gestion de l’apprentissage incluent des concepteurs de certificats personnalisés natifs (par exemple, Docebo). La conception de certificats libre-service dans ce domaine a été une lacune connue pour Adobe Learning Manager.

Cela se traduit par une lenteur des modifications, des coûts de support élevés et une expérience de création qui ne correspond pas aux attentes des administrateurs en matière de certificats et d’informations d’identification.

## Comment les certifications personnalisées relèvent ces défis

### Workflows en libre-service conviviaux pour les administrateurs

Voici les workflows :

- Le concepteur de certificats et la liste remplacent les scripts de téléchargement de HTML et le provisionnement interne par une expérience pilotée par l’administrateur :
- Les administrateurs créent, publient et retirent des conceptions de certificat dans Learning Manager sans code ni implication CSM.
- Les mises à jour de conception (par exemple, l’image de marque saisonnière ou spécifique à un partenaire) prennent quelques minutes dans l’interface utilisateur au lieu de tickets et de cycles d’ingénierie.
- Les valeurs par défaut au niveau du compte et de l’objet d’apprentissage réduisent la configuration répétitive par objet.

### Réduction des frais généraux de support et des risques opérationnels

En consolidant la gestion des certificats sous **Réalisations** avec une expérience utilisateur claire :

- Les charges de travail pour les demandes « télécharger ou modifier mon certificat » chutent pour CSM et les équipes d’ingénieurs.
- Le produit applique des contraintes sécurisées (par exemple, une orientation verrouillée, des modèles hérités non modifiables) pour réduire les risques aux déploiements existants.
- Les modèles hérités migrés permettent de conserver les certificats historiques disponibles sans effort de support supplémentaire.

### Gouvernance, cohérence et contrôle de la marque

Les paramètres par défaut, le Firefly et les galeries aident les clients à :

- Exportez les modèles de marque une fois au niveau du compte et remplacez-les uniquement si nécessaire.
- Utilisez des arrière-plans de Firefly dans les limites de protection de l’entreprise plutôt que des ressources externes ad hoc.
- Gérez les certificats par le biais des états de publication et de retrait, avec des brouillons pouvant être prévisualisés avant le déploiement.

### Alignement sur les badges et les flux de certificats existants

La conception conserve le parcours d’élève actuel : les certificats sont toujours téléchargés à partir de **Badges** et de **Réalisations**, ce qui limite la reconversion.

### Performances et évolutivité

Certificats préconfigurés et performances cibles de rendu pilotées par JSON :

- Les certificats sont générés à la fin et sont stockés, le téléchargement est donc en fait une récupération statique.
- Les conceptions JSON restent légères pour l’éditeur et le rendu à l’exécution à grande échelle.

## Cas d’utilisation réels

### Formation des clients et des partenaires : informations d’identification de la marque à grande échelle

**Scénario :** une société de logiciels dirige des académies clients et partenaires avec des centaines de programmes dans différentes régions et marques.

- Utilisez des modèles par défaut au niveau du compte avec des arrière-plans générés par le Firefly alignés sur chaque ligne de produits.
- Ajoutez des mises en page spécifiques aux paramètres régionaux pour les titres de certification, les clauses de non-responsabilité et les signatures localisés.
- Pour les partenaires Premium, dupliquez les modèles de base et ajoutez le co-branding du partenaire (logo et texte juridique) au niveau de l’instance.
- Les PDF préconfigurés permettent aux partenaires de télécharger des certificats directement après avoir terminé les certifications des partenaires, avec une charge minimale sur Learning Manager.

Ce modèle convient aux écosystèmes de franchise ou multimarques dans lesquels les certificats renforcent la valeur de la marque et du partenaire (par exemple, les grands réseaux de partenaires tels que RealPage).

### Conformité et formation réglementaire : environnements multilingues à forte évolution

**Scénario :** une entreprise réglementée doit mettre à jour le libellé du certificat de conformité, souvent par pays et par langue.

- **La modification dirigée par l&#39;administrateur** permet aux équipes juridiques ou de conformité de modifier le libellé et les champs dynamiques sans tickets d&#39;ingénierie.
- Les dispositions spécifiques aux paramètres régionaux prennent en charge les **clauses de non-responsabilité** spécifiques au pays ou à la région et les signatures sur une dorsale de conception partagée.
- **La logique de secours** garantit que si un modèle d&#39;instance LO spécifique est manquant, le système utilise toujours des valeurs par défaut sécurisées et évite les échecs d&#39;émission.

Cela s’applique aux secteurs de la santé, de la finance, des administrations et à d’autres secteurs où le texte des certificats change souvent et est audité.

### Certifications récurrentes avec contenu de catalogue partagé ou homologue

**Scénario :** un compte Learning Manager maître partage du contenu avec plusieurs **comptes de pairs** (par exemple, de nombreux comptes clients), chacun avec des certifications récurrentes et ses propres certificats.

- Les comptes de pairs peuvent **ajouter des cours acquis à des certifications récurrentes** et configurer **des modèles de certificats locaux** au niveau de l&#39;instance.
- Les mises à jour de cours à partir du compte principal sont récurrentes comme prévu, tandis que les conceptions de certificats peuvent rester **par client**.

### Programmes d’activation et de leadership internes

**Scénario :** les programmes internes (par exemple, les accélérateurs de responsables ou les académies de produits) souhaitent **des certificats visuellement distincts** que les administrateurs peuvent mettre à jour sans travail de HTML.

- Les propriétaires de programmes peuvent concevoir des **modèles de programme** (par exemple, des visuels de style académie interne ou MAP) sans compétences en HTML.
- Les remplacements au niveau de l’instance permettent à différentes cohortes ou régions d’utiliser des variantes (par exemple, un branding spécifique à la cohorte ou régional).
- Les arrière-plans Firefly prennent en charge les visuels **spécifiques à un événement ou à une cohorte** et sont moins dépendants des équipes de conception.

### Transition à partir des certificats de HTML hérités

**Scénario :** les clients existants utilisent des certificats personnalisés HTML5 gérés via des CSM.

- Les modèles ZIP ou de HTML hérités sont migrés et marqués comme hérités, ce qui préserve l’utilisation et les téléchargements passés.
- Les administrateurs peuvent passer progressivement à des modèles basés sur des concepteurs, en commençant par les programmes hautement prioritaires.
- Si la migration ne peut pas préserver un mappage (par exemple, les badges sont désactivés à mi-chemin), le système revient au modèle global par défaut afin que les élèves ne soient pas bloqués.

## Exceptions à connaître lors de l’utilisation de certificats personnalisés

L’expérience de création de certificats personnalisés introduite dans M45 étend la façon dont les certificats sont créés et gérés. Les exceptions suivantes s’appliquent lors de l’utilisation de certificats créés avant cette version :

### Les certificats existants sont conservés mais ne peuvent pas être modifiés

Les certificats créés avant M45 et déjà associés à des objets d’apprentissage sont migrés automatiquement. Ces certificats continuent d’être émis pour les objets d’apprentissage existants. Après la migration, ils sont disponibles en mode lecture seule. Vous ne pouvez pas modifier leur disposition ou leur contenu.

Pour mettre à jour les conceptions de certificat, créez un nouveau modèle de certificat à l’aide de l’éditeur de certificat personnalisé.

### Les nouveaux objets d’apprentissage utilisent les certificats nouvellement créés

Les objets d’apprentissage créés après la version d’avril 2026 doivent utiliser des certificats créés via le nouvel éditeur. Les certificats migrés ne peuvent pas être sélectionnés lors de la configuration de nouveaux objets d&#39;apprentissage.

Les administrateurs peuvent créer de nouveaux certificats et les définir comme valeurs par défaut pour rationaliser la réutilisation.

### Les certificats et les badges doivent être activés pendant la création

Les auteurs doivent explicitement activer les certificats ou les badges pour chaque objet d’apprentissage. Cela garantit que les certificats sont émis uniquement pour les objets d&#39;apprentissage auxquels ils sont destinés.

### La création de certificat nécessite une configuration unique

Les organisations qui s&#39;appuient sur des certificats pour plusieurs objets d&#39;apprentissage doivent prévoir du temps pour recréer les modèles couramment utilisés. L’éditeur glisser-déposer est conçu pour rendre ce processus rapide et cohérent.

## Création d’un certificat personnalisé

1. Connectez-vous à Adobe Learning Manager en tant qu&#39;**administrateur**.
2. Dans la section **Configurer**, sélectionnez **Réalisations**. La page **Badges** s&#39;ouvre.
   ![Créer un certificat personnalisé](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate1.png)
   *Accéder à Réalisations dans le panneau de navigation de gauche*

3. Dans le panneau de navigation de gauche, sélectionnez **Certificats**. La page **Certificats** s&#39;ouvre.
   ![Créer un certificat personnalisé](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate2.png)
   *Page Certificat*

4. Dans la zone supérieure droite de la page, sélectionnez **Nouveau certificat**. La boîte de dialogue **Créer un certificat** s&#39;ouvre.
5. Sélectionnez **Paysage** ou **Portrait**, selon l&#39;aspect que vous souhaitez donner au certificat. Après avoir sélectionné une orientation, vous voyez un modèle vierge et des modèles prêts à l’emploi pour cette orientation.
   ![Créer un certificat personnalisé](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate3.png)
   *Option Paysage ou Portrait*

6. Sélectionnez le modèle vierge ou un modèle existant.
7. Entrez un nom de certificat.
8. Dans le menu déroulant, sélectionnez une langue par défaut.
9. Sélectionnez **Créer**. Si vous avez choisi le modèle vide, une zone de travail vide apparaît sous le nom de votre certificat.
10. Ajoutez des éléments : **Texte**, **Image**, **Valeur dynamique** et **Arrière-plan du certificat**.
    ![Créer un certificat personnalisé](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate4.png)
    *Ajouter des éléments au certificat*

11. Pour le **texte**, ajoutez du contenu sous **Texte préformaté** ou **Modèles de texte**, ou ajoutez du texte personnalisé. Le texte apparaît sur la zone de travail. Lorsque du texte est sélectionné, les options de mise en forme apparaissent au-dessus de la zone de travail. Pour supprimer le contenu indésirable, sélectionnez l&#39;icône **Supprimer** dans le coin supérieur droit de la zone de travail.
12. Pour ajouter des images, sélectionnez **Image** en regard de **Ajouter des éléments**. Chargez des images depuis votre ordinateur ou sélectionnez des images dans les listes de catégories.
13. Sélectionnez **Valeur dynamique** pour ajouter des détails de base, des étiquettes de catalogue et des champs actifs.
14. Sélectionnez **Arrière-plan du certificat** pour appliquer des couleurs ou des images. Pour créer des images avec Adobe Firefly, sélectionnez **Générer l&#39;image**.
15. Dans le champ d&#39;invite, décrivez ce que vous souhaitez (jusqu&#39;à 100 caractères) et sélectionnez **Générer**. Quatre options d’image s’affichent en fonction de votre invite.
16. Sélectionnez l’image souhaitée. Il est appliqué en tant qu’arrière-plan du certificat.
    ![Créer un certificat personnalisé](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate5.png)
    *Ajouter une image au certificat*

17. Sélectionnez **Aperçu** pour vérifier le certificat avant de publier. Cela vous aide à comprendre à quoi ressemble le certificat.
    ![Créer un certificat personnalisé](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate6.png)
    *Aperçu du certificat*

18. Dans l’aperçu, vous pouvez enregistrer sur Google Drive, télécharger, imprimer ou utiliser d’autres options telles que les propriétés d’annotation ou de document.
19. Sélectionnez **Enregistrer comme brouillon** pour continuer plus tard ou sélectionnez **Publish** pour publier le certificat. Après la publication, les élèves peuvent télécharger le certificat lorsqu’ils atteignent le jalon configuré.

Après avoir enregistré un certificat sous **Publié** ou **Brouillons**, vous pouvez le modifier, le cloner, le renommer ou le supprimer.

## Modification d’un certificat personnalisé

1. Dans la section **Configurer**, sélectionnez **Réalisations**. La page **Badges** s&#39;ouvre.
2. Dans le panneau de navigation de gauche, sélectionnez **Certificats**. La page **Certificats** s&#39;ouvre.
3. Sélectionnez l&#39;onglet **Publié** ou **Brouillons** pour le certificat que vous souhaitez.
4. Ouvrez le menu d&#39;actions (**...**) pour le certificat et sélectionnez **Modifier**.
   ![Modifier le certificat à partir du menu Actions](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0001.png)
   *Option Modifier dans le menu déroulant*

5. Apportez vos modifications.
6. Sélectionnez **Publish** ou **Enregistrer comme brouillon**.

## Cloner un certificat personnalisé

Utilisez **Cloner** lorsque vous souhaitez obtenir une copie d&#39;un certificat pour un nouveau nom ou un cas d&#39;utilisation similaire. Après avoir cloné le certificat, renommez-le afin qu’il porte un nom distinct ; sinon, le nom peut correspondre à la source même si vous avez modifié la conception.

>[!NOTE]
>
>Vous ne pouvez pas définir de nouveau nom lors de l’enregistrement immédiatement après le clonage. Renommez le certificat après son enregistrement comme brouillon ou après sa publication.

1. Dans la section **Configurer**, sélectionnez **Réalisations**. La page **Badges** s&#39;ouvre.
2. Dans le panneau de navigation de gauche, sélectionnez **Certificats**. La page **Certificats** s&#39;ouvre.
3. Sélectionnez l&#39;onglet **Publié** ou **Brouillons** pour le certificat que vous souhaitez.
4. Ouvrez le menu d&#39;actions (**...**) pour le certificat, puis sélectionnez **Cloner**.
   ![Cloner le certificat à partir du menu Actions](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0002.png)
   *Option de duplication dans le menu déroulant*

5. Apportez vos modifications.

6. Sélectionnez **Publish** ou **Enregistrer comme brouillon**.

7. Renommez le certificat cloné en suivant les étapes indiquées dans [Renommer un certificat personnalisé](#rename-a-custom-certificate).

## Renommer un certificat personnalisé

Vous pouvez renommer un certificat sans le cloner.

1. Dans la section **Configurer**, sélectionnez **Réalisations**. La page **Badges** s&#39;ouvre.
2. Dans le panneau de navigation de gauche, sélectionnez **Certificats**. La page **Certificats** s&#39;ouvre.
3. Sélectionnez l&#39;onglet **Publié** ou **Brouillons** pour le certificat que vous souhaitez.

4. Ouvrez le menu d&#39;actions (**...**) pour le certificat et sélectionnez **Renommer**.
   ![Renommer le certificat à partir du menu Actions](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0003.png)
   *Option Renommer dans le menu déroulant*

5. Dans la boîte de dialogue **Renommer le certificat**, entrez le nouveau nom.
   Boîte de dialogue ![Renommer le certificat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0004.png)
   *Entrez un nouveau nom*

6. Sélectionnez **Enregistrer**. Learning Manager affiche un message de confirmation.

## Supprimer un certificat personnalisé

La suppression d’un certificat est irréversible. N’effectuez cette opération que si vous êtes sûr.

>[!NOTE]
>
>Vous ne pouvez pas supprimer un certificat lié à un objet d&#39;apprentissage ou à une instance.

1. Dans la section **Configurer**, sélectionnez **Réalisations**. La page **Badges** s&#39;ouvre.
2. Dans le panneau de navigation de gauche, sélectionnez **Certificats**. La page **Certificats** s&#39;ouvre.
3. Sélectionnez l&#39;onglet **Publié** ou **Brouillons** pour le certificat que vous souhaitez.
4. Ouvrez le menu d&#39;actions (**...**) pour le certificat et sélectionnez **Supprimer**. Adobe Learning Manager affiche un message de confirmation.
   ![Supprimer le certificat du menu des actions](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0005.png)
   *Option Supprimer dans le menu déroulant*
   ![Confirmation de suppression de certificat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0006.png)
   *Message de confirmation*

5. Sélectionnez **Oui**. Si le certificat n’est pas joint à un objet d’apprentissage ou à une instance, Learning Manager termine la suppression et peut afficher une autre confirmation.

## Définir un certificat personnalisé comme certificat par défaut

Vous pouvez définir un certificat comme certificat par défaut pour :

- Formations
- Parcours d’apprentissage
- Certifications
- Tout

![Options de certificat par défaut](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0007.png)
*Définir comme certificat par défaut*

1. Dans la section **Configurer**, sélectionnez **Réalisations**. La page **Badges** s&#39;ouvre.
2. Dans le panneau de navigation de gauche, sélectionnez **Certificats**. La page **Certificats** s&#39;ouvre.
3. Sélectionnez l&#39;onglet **Publié** ou **Brouillons** pour le certificat que vous souhaitez.
4. Ouvrez le menu d&#39;actions (**...**) pour le certificat, sélectionnez **Définir par défaut**, puis sélectionnez l&#39;une des quatre options. Learning Manager affiche un message de confirmation.
5. Sélectionnez **Oui**. Learning Manager affiche une autre confirmation. Le certificat affiche un libellé **Par défaut pour** avec la catégorie que vous avez sélectionnée (par exemple, **Par défaut pour les formations**).
   ![Valeur par défaut pour le libellé de catégorie sur le certificat](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0008.png)
   *Après qu&#39;il soit devenu le certificat par défaut*
