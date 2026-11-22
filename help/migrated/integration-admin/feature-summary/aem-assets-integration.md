---
description: Importez du contenu d’apprentissage et des images d’Adobe Experience Manager Assets dans Adobe Learning Manager, et mettez automatiquement à jour le contenu lié.
jcr-language: en_us
title: Intégration d’AEM Assets
exl-id: cd33c0f2-59df-4f35-a7d9-d7bff6b9ffba
source-git-commit: f6dc1e97076edf812862b80a6ed5931989c660da
workflow-type: tm+mt
source-wordcount: '3447'
ht-degree: 0%
---

# Intégration des ressources AEM

## Présentation

Adobe Learning Manager s’intègre désormais à Adobe Experience Manager Assets as a Cloud Service. Les équipes peuvent stocker du contenu d’apprentissage et des images dans Adobe Experience Manager Assets, les importer dans Adobe Learning Manager et gérer les mises à jour depuis un seul endroit. Lorsqu’une ressource change, le contenu lié dans la bibliothèque de contenu peut être mis à jour automatiquement, de sorte que les auteurs n’ont pas besoin de recharger les fichiers.

Étant donné que votre organisation gère les ressources au même endroit, les auteurs utilisent des fichiers à jour approuvés par la marque au lieu de télécharger et de recharger des copies. Adobe Experience Manager Assets conserve également l’historique des versions de chaque fichier, qui vous fournit un enregistrement de la version active et de la date.

L&#39;installation est une tâche ponctuelle, et c&#39;est la partie qui a le plus besoin de soins. Après la configuration, l’importation de ressources fonctionne comme tout autre téléchargement.

>[!NOTE]
>
>Cette intégration est disponible pour tous les comptes Adobe Learning Manager disposant d’une licence Adobe Experience Manager Assets, y compris les comptes Prime et Ultimate. La même documentation s’applique aux deux.

## Qui fait quoi

| Rôle | Ce qu&#39;ils font |
|---|---|
| Administrateur d’intégration ALM | Connecte le compte et choisit les paramètres d’intégration. |
| Administrateur Adobe Admin Console | Attribue le compte technique généré aux profils de produit AEM Assets appropriés. |
| Administrateur ALM | Importe des images de différents emplacements à l’aide de l’intégration. |
| Auteur ALM | Importe le contenu et les images, et crée des cours. |

Chaque rôle a une partie distincte dans la configuration et l’utilisation de l’intégration.

## Déploiements pris en charge

| Élément | Pris en charge |
|---|---|
| Adobe Experience Manager Assets as a Cloud Service, instance de l’auteur | Oui |
| Instance Adobe Experience Manager Assets as a Cloud Service, de publication ou de diffusion | Non |
| Adobe Experience Manager sur site | Non |

>[!NOTE]
>
>Adobe Learning Manager se connecte aux instances d’auteur uniquement parce que les ressources y sont créées et gérées. Publish et les instances de livraison ne font pas partie de l’intégration actuelle.

## Configuration de l’intégration

Connectez Adobe Learning Manager à Adobe Experience Manager Assets, attribuez le compte technique et choisissez vos paramètres de mise à jour.

Ce workflow est destiné aux administrateurs d’intégration. Effectuez chaque étape pour que les mises à jour automatiques fonctionnent pour vos auteurs. La configuration comporte cinq parties : connectez-vous à votre organisation IMS, recherchez le compte technique, attribuez-le dans Adobe Admin Console, choisissez vos paramètres et accordez l’accès aux auteurs.

### Conditions préalables {#setup-prerequisites}

Vous devez répondre à toutes ces exigences. La raison la plus courante pour laquelle une connexion échoue est qu’aucun d’entre eux n’est présent.

* Vous avez le rôle Administrateur d’intégration dans Adobe Learning Manager. Le workflow de connexion est disponible uniquement pour ce rôle.
* Vous êtes administrateur d’organisation IMS pour l’organisation Identity Management System (IMS) d’Adobe que vous sélectionnez.
* Vous avez accès à au moins une organisation où des instances d’AEM Assets peuvent être associées à Learning Manager.

Si vous n’êtes pas administrateur d’organisation IMS, demandez à votre administrateur informatique de vous accorder l’accès ou d’exécuter la connexion avec vous.

### Mise en correspondance de Adobe Learning Manager avec votre organisation IMS

Chaque compte Adobe Learning Manager se connecte à une organisation IMS (également appelée profil IMS). Gardez les points suivants à l’esprit lorsque vous planifiez votre configuration :

* Une organisation IMS peut contenir plusieurs programmes et environnements, et chaque programme peut avoir des instances Adobe Experience Manager Assets. Vous pouvez utiliser n’importe laquelle de ces instances avec le compte connecté.
* Les instances d’une autre organisation IMS ne peuvent pas être utilisées avec ce compte.
* Une organisation IMS liée à un compte Adobe Learning Manager ne peut pas être liée à un autre compte en même temps.

>[!NOTE]
>
>Si votre société dispose de plusieurs organisations IMS, choisissez celle qui détient votre licence Adobe Experience Manager Assets et les instances que vous souhaitez que les auteurs utilisent.

### Connexion à votre organisation IMS

1. Connectez-vous à Adobe Learning Manager en tant qu&#39;**administrateur d&#39;intégration**.
1. Sélectionnez **Adobe Experience Manager Assets** comme type de connecteur.

   ![](assets/aem-assets-integrationstep1.png)

1. Sélectionnez **Se connecter**.

   ![](assets/aem-assets-integrationstep2.png)

1. Lorsque vous y êtes invité, connectez-vous avec votre Adobe ID et sélectionnez l’organisation IMS qui contient vos instances Adobe Experience Manager Assets.

   ![](assets/aem-assets-integrationstep3.png)

   ![](assets/aem-assets-integrationstep4.png)

Adobe Learning Manager vérifie ensuite votre rôle d’administrateur d’organisation IMS et votre accès à l’instance. Si les deux vérifications réussissent, votre compte est lié au compte IMS déjà créé avec la portée d’API AEM Assets Author à l’organisation IMS sélectionnée et un compte technique est créé pour votre organisation. La page de présentation de la connexion s’ouvre alors et affiche les détails techniques du compte.

### Recherche du compte technique

Le compte technique est créé spécifiquement pour votre organisation. Adobe Learning Manager l&#39;utilise pour lire ou écrire à l&#39;aide de l&#39;[API Open](https://developer.adobe.com/experience-cloud/experience-manager-apis/api/experimental/assets/author/) AEM Assets en arrière-plan.

1. Connectez-vous en tant qu&#39;**administrateur d&#39;intégration** et ouvrez la page de présentation de la connexion **Adobe Experience Manager Assets**.
1. Dans la section **Informations d&#39;identification**, recherchez l&#39;**adresse électronique du compte technique**.
1. Copiez l’e-mail du compte technique. Vous l&#39;utiliserez pour rechercher le compte dans **Adobe Admin Console**.

### Attribution du compte technique dans Adobe Admin Console

Ajoutez le compte technique à un profil de produit pour chaque instance Adobe Experience Manager Assets que vous souhaitez que Adobe Learning Manager utilise. Par exemple, si vous disposez de 10 instances et que vous souhaitez que seules 6 d’entre elles fonctionnent avec Adobe Learning Manager, attribuez le compte aux profils de ces 6 instances.

1. Connectez-vous à **Adobe Admin Console** en tant qu’administrateur de la même organisation IMS.
2. Sélectionnez **Produits et services**, puis sélectionnez **Adobe Experience Manager as a Cloud Service**.

   ![](assets/aem-assets-integration6.png)

3. Sélectionnez l’instance à utiliser avec Adobe Learning Manager.

   ![](assets/aem-assets-integration7.png)

4. Ouvrez le profil de produit disposant de l’accès dont Adobe Learning Manager a besoin. Par exemple, le profil Administrateurs AEM.

   ![](assets/aem-assets-integration8.png)

5. Sélectionnez **Ajouter des identifiants d&#39;API**.

   ![](assets/aem-assets-integration9.png)

6. Recherchez le compte technique. Faites-le correspondre à l’adresse e-mail du compte technique que vous avez copiée à partir de l’administrateur d’intégration. Le compte se trouve généralement au bas de la liste.

   ![](assets/aem-assets-integration10.png)

7. Sélectionnez le compte technique, puis sélectionnez **Enregistrer**.
8. Répétez les étapes 3 à 7 pour chaque instance à utiliser.

Si la liste d’identifiants d’API du profil est vide, le compte technique n’est pas encore attribué. Pour en savoir plus sur les profils de produit et les identifiants d’API, consultez la documentation Adobe Admin Console.

>[!IMPORTANT]
>
>Ne sautez pas cette étape. Si vous n’attribuez pas de compte technique, les auteurs peuvent toujours importer des ressources à partir d’Adobe Experience Manager Assets, mais les mises à jour automatiques ne fonctionnent pas. Vous devez ensuite mettre à jour le contenu manuellement.

### Choix des paramètres d’intégration

Après vous être connecté, activez la connexion et choisissez la façon dont Adobe Learning Manager gère les mises à jour et les aperçus.

| Paramètre | Ce qu’il fait |
|---|---|
| Mises à jour automatiques | Met à jour les éléments liés de la bibliothèque de contenu lorsque la ressource change dans Adobe Experience Manager Assets. |
| Mise à jour des objets d’apprentissage | Applique également la mise à jour aux objets d&#39;apprentissage qui utilisent l&#39;élément Bibliothèque de contenu. |
| Lien d’aperçu public | Crée un lien d’aperçu pour le contenu pris en charge et l’enregistre dans les métadonnées de la ressource sur AEM Assets. |

La mise à jour de l&#39;objet d&#39;apprentissage est un paramètre enfant des mises à jour automatiques. Elle ne peut être activée que si les mises à jour automatiques sont activées en premier. Si vous désactivez les mises à jour automatiques, les auteurs mettent à jour le contenu manuellement dans la bibliothèque de contenu.

>[!IMPORTANT]
>
>Les modifications apportées à ces paramètres, y compris leur désactivation, peuvent prendre jusqu’à une heure pour prendre effet. Il en va de même après l’activation de la connexion. Le retard ne signifie pas que quelque chose ne va pas. Attendez jusqu’à une heure avant de tester.

### Donner l’accès à Adobe Experience Manager Assets aux auteurs {#give-authors-access}

La configuration de l’intégration ne donne pas aux auteurs l’accès à vos ressources. Chaque auteur ou administrateur Adobe Learning Manager qui importe des ressources doit également avoir accès à l’instance d’auteur Adobe Experience Manager Assets correspondante.

* Ajoutez des auteurs en tant qu’utilisateurs de l’instance Adobe Experience Manager Assets author, dans la même organisation IMS.
* Donnez-leur au moins l’accès dont ils ont besoin pour parcourir et sélectionner des actifs. Votre administrateur Adobe Experience Manager décide des rôles et des profils de produit à utiliser.

>[!NOTE]
>
>L’octroi de cet accès relève de votre responsabilité en tant qu’administrateur Adobe Experience Manager. Adobe Learning Manager ne prescrit pas de rôle spécifique. Pour obtenir de l’aide sur les utilisateurs et les profils, consultez la documentation Adobe Experience Manager Assets.

### Vérification de la configuration

1. Attendez la fin du délai des paramètres décrit ci-dessus.
1. Connectez-vous en tant qu’auteur avec accès à l’instance.
1. Dans la **bibliothèque de contenu**, sélectionnez **Parcourir** et vérifiez que **AEM Assets** s&#39;affiche en regard de **Appareil**.
1. Importez une ressource et confirmez qu’elle est importée.
1. Si la ressource est remplacée, s’il s’agit d’une nouvelle version ou si elle est retraitée, elle est mise à jour en quelques minutes dans la plupart des cas ou, dans de rares cas, elle peut prendre jusqu’à une heure. Si cela prend plus d’une heure, vous pouvez retraiter la ressource dans AEM Assets.

## Importation de contenu à partir d’Adobe Experience Manager Assets

Importez du contenu d’apprentissage et des images depuis Adobe Experience Manager Assets, et créez des cours à partir de contenu qui reste à jour.

Ce workflow est destiné aux auteurs. Votre administrateur d’intégration doit d’abord configurer l’intégration.

### Conditions préalables {#import-prerequisites}

* Votre administrateur d’intégration a connecté le compte et activé la connexion.
* Vous avez accès à l’instance d’auteur Adobe Experience Manager Assets qui contient vos ressources, dans l’organisation IMS connectée. Votre administrateur Adobe Experience Manager accorde cet accès. Voir [Donner l&#39;accès à Adobe Experience Manager Assets](#give-authors-access) aux auteurs.

Une fois l’intégration activée, toute option de téléchargement dans Adobe Learning Manager qui la prend en charge affiche deux sources : Appareil et AEM Assets. Cela inclut la bibliothèque de contenu et les options de téléchargement pour les images de cours. L’appareil reste disponible, ce qui vous permet de télécharger des fichiers depuis votre ordinateur.

### Emplacement d’importation

L’option AEM Assets s’affiche aux emplacements de téléchargement qui la prennent en charge. Le téléchargement à partir de l’appareil reste actif. Vous pouvez importer :

* Contenu du module de la bibliothèque de contenu.
* Images, telles que les images de couverture de cours et de bannière.
* Assistances à la tâche

Seuls les types de fichiers pris en charge à cet emplacement de téléchargement apparaissent. Par exemple, l’option Image de couverture n’affiche que les images. Les types pris en charge sont les images (JPEG, PNG, SVG), les vidéos (MP4) et les documents (PDF, packages SCORM, PowerPoint et Word). Les extensions de fichier et les limites de taille sont les mêmes que pour les autres chargements à cet emplacement.

### Le contenu et les images sont traités différemment

| Élément | Comment c&#39;est géré |
|---|---|
| Contenu de la bibliothèque de contenu | Copié et lié à l’actif source, afin qu’il puisse être mis à jour automatiquement. |
| Images, telles que les images de couverture et de bannière | Copiés lorsque vous les sélectionnez. Ils ne sont pas liés et ne sont pas mis à jour automatiquement. |

### Importation de contenu dans la bibliothèque de contenu

1. Ouvrez la **Bibliothèque de contenu** et ajoutez du contenu.
1. Sélectionnez **Parcourir**.
1. Sélectionnez **AEM Assets**.
1. Si vous y êtes invité, connectez-vous avec votre Adobe ID.
1. Dans la fenêtre **Adobe Experience Manager Assets**, accédez à la ressource. Si vous avez accès à plusieurs référentiels (instance AEM activée avec AEM Assets), basculez entre eux selon vos besoins.
1. Sélectionnez la ressource, puis finalisez le téléchargement et l’enregistrement.
1. Créez votre cours à l’aide du groupe de contenus.

Gardez les points suivants à l’esprit :

* Vous sélectionnez les ressources une par une. L’importation en bloc et l’importation de dossiers ne sont pas disponibles, et vous ne pouvez pas migrer une bibliothèque de contenu existante vers Adobe Experience Manager Assets.
* Le sélecteur de ressources vous permet d’ouvrir une ressource dans Adobe Experience Manager Assets.
* Adobe Learning Manager ne fournit pas de contenu directement à partir d’Adobe Experience Manager Assets. Il copie chaque actif importé et conserve une copie locale.
* Le contenu importé est traité comme tout autre contenu dans Adobe Learning Manager, y compris la transcription pour l’assistant de l’élève.

### Ajouter des assistances à la tâche

Sélectionnez des fichiers d’assistance à la tâche, tels que des PDF et des documents de référence, à partir d’AEM Assets de la même manière que vous importez du contenu de bibliothèque de contenu.

### Auteurs sans accès

Si un auteur n’a pas accès à Adobe Experience Manager Assets pour l’organisation IMS connectée, un message s’affiche indiquant que son accès est limité lorsqu’il sélectionne AEM Assets.

## Maintenir le contenu à jour

Maintenez les éléments liés de la bibliothèque de contenu à jour à mesure que les actifs changent dans Adobe Experience Manager Assets.

### Fonctionnement des mises à jour automatiques

Lorsque les mises à jour automatiques sont activées à partir de la section Administrateur d’intégration et que le compte technique est attribué, Adobe Learning Manager conserve la bibliothèque de contenu synchronisée avec Adobe Experience Manager Assets.

1. Dans **Adobe Experience Manager Assets**, téléchargez une nouvelle version de la ressource ou restaurez une version précédente.
1. Adobe Experience Manager Assets termine le traitement de la ressource. Si la ressource est remplacée, elle est mise à jour en quelques minutes dans la plupart des cas ou, dans de rares cas, elle peut prendre jusqu’à une heure. Si cela prend plus d’une heure, vous pouvez retraiter la ressource dans AEM Assets.
1. Adobe Learning Manager met à jour les éléments liés de la **bibliothèque de contenu** et incrémente le numéro de version.
1. Si la fonctionnalité **Mise à jour des objets d&#39;apprentissage** est activée, les objets d&#39;apprentissage qui utilisent ces éléments sont également mis à jour. Les élèves actuellement inscrits et les futurs élèves reçoivent la dernière version.
1. Les élèves recevront la dernière version la prochaine fois qu&#39;ils lanceront le contenu. Un élève dont le contenu est déjà ouvert doit le fermer et le relancer.

La mise à jour n&#39;est pas instantanée. Patientez quelques instants, puis actualisez la bibliothèque de contenu pour voir la modification.

### Mettre à jour le contenu manuellement

Si les mises à jour automatiques sont désactivées ou si le compte technique n’est pas attribué dans Adobe Admin Console, mettez à jour le contenu manuellement :

1. Ouvrez l&#39;élément dans la **Bibliothèque de contenu**.
1. Sélectionnez le fichier mis à jour dans **AEM Assets**.
1. Sélectionnez **Enregistrer**.

### Application des mises à jour entre les langues

Si plusieurs paramètres régionaux d’un élément de bibliothèque de contenu multilingue utilisent la même ressource, la mise à jour de cette ressource met à jour tous ces paramètres régionaux. Les paramètres régionaux qui utilisent une ressource différente ne sont pas affectés.

### Combien de groupes de contenus une ressource peut avoir

Une ressource peut être liée à 10 groupes de contenus au maximum.

>[!NOTE]
>
>Organisez vos groupes de contenus en gardant cela à l’esprit. Si vous avez besoin de plus de 10 groupes de contenu de la même source, utilisez une copie de la ressource pour les groupes supplémentaires.

## Aperçu du contenu d’Adobe Experience Manager Assets

Utilisez des liens d&#39;aperçu pour examiner le contenu SCORM et HTML sans le lancer en tant qu&#39;élève.

Si le paramètre Lien d’aperçu public est activé, Adobe Learning Manager crée un lien d’aperçu pour le contenu pris en charge que vous importez dans la bibliothèque de contenu et l’enregistre dans les métadonnées de la ressource dans Adobe Experience Manager Assets.

Le lien d’aperçu est créé pour les types de contenu suivants :

* SCORM 1.2
* SCORM 2004
* HTML

Pour rechercher et utiliser le lien :

1. Dans Adobe Experience Manager Assets, ouvrez les propriétés de la ressource.
1. Dans les métadonnées, recherchez le lien d’aperçu.

   <!-- TODO: The source document says "path to be mentioned here". Add the exact metadata location (confirm with Kranthi). -->

1. Copiez le lien et collez-le dans un navigateur pour prévisualiser la ressource.

Toute personne qui ouvre les métadonnées de la ressource peut voir et utiliser ce lien.

>[!NOTE]
>
>L’utilisation d’un lien d’aperçu n’est pas prise en compte dans votre utilisation de licence ALM. Si vous désactivez l’option Lien d’aperçu public, les fichiers d’aperçu créés par Adobe Learning Manager dans Adobe Experience Manager Assets sont supprimés.

## Lorsque les actifs, les accès ou les connexions changent

Comprendre comment la suppression d’une ressource, la perte d’accès ou la déconnexion affecte votre contenu.

### Que se passe-t-il lorsque vous supprimez une ressource ? {#delete-asset}

Les cours qui utilisent déjà le contenu continuent de fonctionner même si vous supprimez la ressource source. La manière dont la suppression affecte la bibliothèque de contenu dépend des paramètres régionaux du groupe de contenus.

| Scénario | Que se passe-t-il ? |
|---|---|
| La ressource est utilisée par l’un des paramètres régionaux d’un groupe de contenus multilingues | Ces paramètres régionaux sont supprimés. Les autres paramètres régionaux restent. |
| La ressource est la seule derrière un groupe de contenus | Le groupe de contenus est retiré. |

Lorsqu&#39;un groupe de contenus est retiré :

* Les cours existants continuent de lire le contenu copié.
* Vous ne pouvez pas utiliser le groupe de contenus pour créer de nouvelles associations de cours.
* Vous ne pouvez pas modifier le groupe de contenus.

### Que se passe-t-il si un auteur perd l’accès ?

Le contenu précédemment importé par l’auteur continue de fonctionner. Cependant, l’auteur ne peut pas importer de nouvelles ressources à partir de cette instance, créer des groupes de contenus ou modifier les groupes de contenus existants qui l’utilisent.

### Que se passe-t-il si vous vous déconnectez ?

Le contenu et les images importés restent dans Adobe Learning Manager, car il s’agit de copies. Les liens vers les actifs sources sont rompus, le contenu lié n’est donc plus mis à jour. Les objets d’apprentissage et les groupes de contenus continuent de fonctionner.

## Dépannage

**Je ne peux pas me connecter ou je ne vois pas le connecteur**

Assurez-vous d’avoir le rôle Administrateur d’intégration dans Adobe Learning Manager.

**La connexion échoue même si je suis administrateur d’organisation IMS**

Assurez-vous également d’avoir accès à au moins une instance Adobe Experience Manager Assets dans l’organisation IMS sélectionnée. Cela peut se produire lorsque votre équipe de support informatique administre l’organisation, mais n’est pas affectée aux produits Adobe Experience Manager Assets. Demandez à votre administrateur Adobe Experience Manager de vous ajouter à une instance, puis reconnectez-vous.

**Mon instance Adobe Experience Manager Assets n&#39;est pas répertoriée**

Assurez-vous que l’instance appartient à l’organisation IMS liée à votre compte Adobe Learning Manager et qu’il s’agit d’une instance de création d’Adobe Experience Manager Assets as a Cloud Service.

**Je ne vois pas AEM Assets comme option de téléchargement**

Demandez à votre administrateur d’intégration de confirmer que la connexion est activée et patientez jusqu’à une heure après l’avoir activée.

**Un auteur ne peut pas voir les ressources ou ne peut pas importer**

Demandez à votre administrateur Adobe Experience Manager de donner à l’auteur l’accès à l’instance Adobe Experience Manager Assets author dans l’organisation IMS connectée.

**Le contenu n&#39;a pas été mis à jour ou mon cours affiche un ancien contenu**

1. Vérifiez que les mises à jour automatiques sont activées dans les paramètres de l’administrateur d’intégration et attendez que la modification prenne effet.
2. Confirmez que le compte technique est affecté au profil de produit de l’instance dans Adobe Admin Console.
3. Relancez le contenu. S’il affiche toujours un ancien contenu, mettez-le à jour manuellement.

**Un groupe de contenus a été retiré**

La ressource source a été supprimée dans Adobe Experience Manager Assets. Voir [Que se passe-t-il lorsque vous supprimez une ressource](#delete-asset).

**Le lien d&#39;aperçu n&#39;apparaît pas dans les métadonnées de la ressource**

Vérifiez que le lien d’aperçu public est activé, que le contenu est SCORM 1.2, SCORM 2004 ou version HTML et que vous avez attendu jusqu’à une heure après avoir activé le paramètre.

## Intégration d’AEM Assets - FAQ

**Q. ALM fournit-il du contenu d’apprentissage directement à partir d’AEM Assets ?**

**A.** Non. Nous copions le contenu d’AEM Assets vers ALM et conservons une copie locale dans ALM.

**Q. Que se passe-t-il lorsqu’une ressource est mise à jour dans AEM Assets ?**

**A.** Si l’option Mise à jour automatique est activée dans ALM, le contenu correspondant associé à AEM Assets est mis à jour, ainsi que la version.

**Q. Les administrateurs peuvent-ils contrôler si les mises à jour AEM peuvent accéder automatiquement aux cours ?**

**A.** Oui. Au cours de l’intégration, l’administrateur d’intégration doit sélectionner Mise à jour automatique et décider si la mise à jour s’applique automatiquement aux objets d’apprentissage. En fonction des paramètres du compte, la mise à jour des objets d’apprentissage fonctionnera.

**Q. Les auteurs peuvent-ils toujours télécharger des fichiers à partir de leur ordinateur ?**

**A.** Oui

**Q. Les clients peuvent-ils migrer leur bibliothèque de contenu ALM vers AEM Assets ?**

**A.** Non. Il n&#39;y a pas de disposition de ce genre à ce jour.

**Q. Un dossier AEM Assets entier peut-il être importé dans la bibliothèque de contenu ?**

**A.** Non. Il n&#39;y a pas de disposition de ce genre à ce jour.

**Q. L’intégration prend-elle en charge l’importation en bloc de ressources ?**

**A.** Non, il n&#39;existe aucune disposition de ce type à ce jour.

**Q. Quel contenu ALM peut être sélectionné dans AEM Assets ?**

**A.** Nous prenons en charge les mêmes extensions de fichiers que celles que nous prenons en charge aujourd&#39;hui pour chaque emplacement de téléchargement. Les filtres sont appliqués à l’ouverture d’AEM Content Advisor à ce point de contact de téléchargement.

**Q. Les actifs de contenu et les actifs d’image se comportent-ils de la même manière ?**

**A.** La fonctionnalité de mise à jour automatique s&#39;applique uniquement aux ressources de contenu, et non à toute autre ressource dans ALM.

**Q. Une image d’origine AEM Assets peut-elle être remplacée ultérieurement par un fichier local ?**

**A.** Oui

**Q. Quel AEM Assets un auteur ALM peut-il voir ?**

**A.** Un auteur ALM peut voir tous les dossiers et fichiers auxquels il a accès, en fonction de ses autorisations utilisateur dans AEM Assets.

**Q. Que se passe-t-il si l’accès AEM d’un auteur est supprimé ?**

**A.** L’auteur ne pourra pas modifier ou créer de groupes de contenus à partir d’AEM Assets, car il n’a plus accès aux instances d’actifs de ce profil IMS via AEM Content Advisor.

**Q. Que se passe-t-il si l’intégration AEM Assets est désactivée ou déconnectée ?**

**A.** les objets d’apprentissage et les groupes de contenus fonctionnent toujours, mais la fonctionnalité de mise à jour automatique de ces ressources s’arrêtera et ne poursuivra pas plus loin.

**Q. L’intégration prend-elle en charge AEM sur site ?**

**A.** Non. Il ne prend en charge que les instances cloud.

**Q. Un compte ALM peut-il se connecter à plusieurs comptes AEM Assets ?**

**A.** Le compte ALM est mappé au profil IMS et toutes les instances AEM Assets de ce profil IMS peuvent être connectées et utilisées. Une fois que le profil IMS est lié à un compte ALM, ce profil IMS ne peut pas être lié à un autre compte ALM.

**Q. Le contenu importé à partir d’AEM Assets peut-il être utilisé par l’assistant Élève ?**

**A.** Si le contenu importé à partir d&#39;AEM Assets est utilisé pour créer un cours, celui-ci peut être référencé par l&#39;Assistant Élève dans les conversations pertinentes.

**Q. Les auteurs peuvent-ils prévisualiser une ressource AEM avant de la sélectionner ?**

**A.** Non. La fonction d’aperçu n’est pas disponible avant la sélection de la ressource, bien qu’AEM Assets prenne en charge l’aperçu pour quelques formats de fichiers.

**Q. ALM génère-t-il un lien d’aperçu public ?**

**A.** Oui, uniquement pour les fichiers SCORM 1.2, SCORM 2004 et HTML. Cela est possible uniquement lorsque la fonctionnalité d’aperçu public est activée par l’administrateur d’intégration.

**Liens associés :**

* [Gestion du contenu dans la bibliothèque de contenu](/help/migrated/authors/feature-summary/content-library.md)
* [Documentation Adobe Admin Console](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)
* [Documentation Adobe Experience Manager Assets](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/overview)
