---
jcr-language: en_us
title: Intégration de Learning Manager à AEM
description: Learning Manager est un système de gestion de l’apprentissage doté d’un système de gestion de contenu d’apprentissage intégré. Les utilisateurs gèrent leur contenu d’apprentissage en le chargeant sur Learning Manager, de sorte que ce dernier effectue le contrôle de version, l’attribution de cours, la définition de la visibilité pour les élèves, le suivi de la consommation et la génération de rapports aux administrateurs.
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---



# Intégration de Learning Manager à AEM

Learning Manager est un système de gestion de l’apprentissage doté d’un système de gestion de contenu d’apprentissage intégré. Les utilisateurs gèrent leur contenu d’apprentissage en le chargeant sur Learning Manager, de sorte que ce dernier effectue le contrôle de version, l’attribution de cours, la définition de la visibilité pour les élèves, le suivi de la consommation et la génération de rapports aux administrateurs.

Cependant, certains utilisateurs stockent et gèrent leur contenu sur des systèmes de gestion des actifs. Le contenu est ensuite réutilisé pour diverses autres fonctions.

Les différentes bandes présentes dans l’application de l’élève peuvent être intégrées dans les sites AEM. Tout élève qui se connecte au site AEM verra ses données de formation spécifiques dans ces bandes.

## Téléchargement du package de contenu {#downloadthecontentpackage}

Le programme d’installation est fourni en package de contenu AEM. [***Télécharger le pack***](https://github.com/adobe/adobe-learning-manager-reference-site).

Le package de contenu est disponible sous forme de fichier zip et est compatible avec AEM 6.4 et AEM 6.5.

## Installer le composant Learning Manager {#installcaptivateprimecomponent}

Installez le package de contenu Learning Manager à l’aide d’AEM Package Manager :

>[!NOTE]
>
>Pour plus d’informations sur l’installation des packs, voir  [***Utilisation des packs***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=en#how-to-work-with-packages).

1. En tant qu’auteur AEM, ouvrez AEM Package Manager.
1. Cliquez sur le bouton **[!UICONTROL Charger le package]**.
1. Cliquez sur **[!UICONTROL Parcourir]** et téléchargez le package de contenu.
1. Cliquez sur **[!UICONTROL Charger]**.
1. Une fois le package chargé, installez le package de contenu en le sélectionnant, puis en cliquant sur **[!UICONTROL Installer]**.

   ![](assets/install-package.jpg)

   *Installation du package de contenu*

## Générer le jeton d’actualisation {#generatetherefreshtoken}

L’administrateur AEM a besoin d’un jeton d’actualisation du compte Learning Manager. L’administrateur de l’intégration Learning Manager générera le jeton d’actualisation.

1. Approuvez l’application AEM Sites en vedette.

   Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications fournies]** > **[!UICONTROL Adobe Experience Manager - Sites]**.

   ![](assets/launch-aem.jpg)

   *Approuver l’application*

1. Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications fournies]**, puis ouvrez l’application AEM sites.

   Copiez l’ID de l’application et la description.

1. Cliquez sur **[!UICONTROL Ressources pour les développeurs]** > **[!UICONTROL Jetons d’accès]**.

   ![](assets/click-tokens.jpg)

   *Génération des jetons d’accès*

1. Saisissez les détails suivants :

   * ID client, qui correspond à l’ID de l’application.
   * Clé secrète du client, présente dans la description.

1. Obtenez le code OAuth. Vous devez utiliser l’API v2 dans l’URI de redirection.
1. Cliquez sur **[!UICONTROL Envoyer]** et obtenez le jeton d’actualisation.

## Configuration du widget dans AEM {#configurethewidgetinaem}

Pour la configuration du widget, l’auteur AEM n’a besoin que du jeton d’actualisation fourni par l’administrateur de l’intégration de Learning Manager.

Vous pouvez également définir plusieurs configurations de compte sur plusieurs pages.

1. Cliquez sur **[!UICONTROL Outils]** > **[!UICONTROL Cloud Service]** > **[!UICONTROL Configuration du widget Learning Manager]**.
1. Cliquez sur **[!UICONTROL Créer]**.
1. Entrez le jeton d’actualisation ici. Configurez les autres paramètres.
1. Le nom d’hôte doit être remplacé par « learningmanagereu » pour les régions de l’UE.
1. Enregistrez et fermez la configuration.
1. Sélectionnez une configuration et publiez-la.

## Auteur AEM {#aemauthor}

L’auteur AEM doit d’abord ajouter le composant dans le modèle AEM

L’auteur AEM pourra alors faire glisser et déposer le composant Adobe Learning Manager et le configurer en conséquence.

Le composant Learning Manager nécessite que la configuration créée à l’étape ci-dessus soit mappée à la page.  L’auteur peut mapper la configuration en modifiant les propriétés de la page sous **[!UICONTROL Avancé]** > **[!UICONTROL Configuration]** > **[!UICONTROL Configuration du cloud]** et fournir le chemin de configuration. De cette façon, l’auteur peut créer des configurations pour plusieurs comptes Learning Manager et les mapper à différentes pages Sites. Si une configuration n’est pas mappée à la page, le composant lit la configuration de la page parent de manière récursive jusqu’à ce qu’il en trouve une.

## Élève {#learner}

L’élève peut suivre les cours depuis la page.

Pour pouvoir accéder au widget Learning Manager, l’élève doit être un utilisateur AEM connecté. Également, propriété **e-mail** doit être présent dans le nœud « /profile » du nœud rep:User de l’élève. Cet e-mail doit être identique à celui présent dans le compte Learning Manager.

L’élève peut suivre les cours depuis la page.

La progression du cours est également enregistrée.

Les widgets suivants sont fournis :

1. Ludification
1. Calendrier d’apprentissage
1. Widget Social
1. Widget Catalogue
1. Mon apprentissage
1. Recommandation basée sur l’apprentissage par les pairs
1. Recommendations by admin
1. Recommandation basée sur les intérêts de l’élève

En l’absence de recommandations, le widget apparaît vide.

## Prise en charge de Skyline

Skyline est la version cloud d’AEM. Vous devez d’abord installer Skyline à partir du gestionnaire de modules. Pour utiliser le composant Skyline dans AEM, un utilisateur doit être présent dans le compte Learning Manager. En d’autres termes, l’adresse électronique de l’utilisateur doit exister dans le compte.

### Déployer Skyline

Les étapes de configuration de Skyline sont mentionnées dans la section  [référentiel GitHub](https://github.com/adobe/captivate-prime-aem-components).

## Widget Catalogue

Le widget Catalogue affiche la formation d’un catalogue spécifique ou d’un ensemble de catalogues pour un utilisateur. Dans la section Propriétés des propriétés de la page, sélectionnez Catalogue dans les options répertoriées.

<!--![](assets/catalog-widget.png)-->

Le widget Catalogue contient les options suivantes :

* **[!UICONTROL ID de catalogue]:** ID de catalogue séparés par des virgules pour lesquels la formation doit être affichée.
* **[!UICONTROL Trier]:** Ordre de tri pour la formation. Les options sont : nom, date, dateCreated, dateEnrolled, etc.
* **[!UICONTROL État de l’élève]:** Renvoie toutes les formations qui utilisent les éléments suivants en tant que filtres inscrits, démarrés, terminés et non inscrits. Les résultats de la recherche ne s&#39;affichent pas si l&#39;option de tri est dateEnrolled, dueDate ou dateEnrolled.
* **[!UICONTROL Nom de la compétence]:** Compétence utilisée pour filtrer la formation exacte.
* **[!UICONTROL Nom de la balise]:** Balise utilisée pour filtrer les résultats exacts.

Voici quelques composants supplémentaires que vous pouvez personnaliser :

**[!UICONTROL Types d’objets d’apprentissage]:** Filtrer selon le type de l’objet d’apprentissage. Les types pris en charge sont : cours, certification, assistance à la tâche et programme d’apprentissage.

Dans AEM, le titre d’une carte dans une bande est initialement vide. Dans Propriétés, saisissez le nom du titre dans widgets.html.

**Personnalisation**

Vous pouvez personnaliser l’aspect de la mise en page à l’aide du fichier widgets.html. Vous pouvez modifier l’apparence des cartes qui apparaissent et personnaliser le thème.

Dans le panneau **[!UICONTROL Paramètres généraux]** , vous pouvez choisir les couleurs primaire et secondaire pour les cartes et spécifier les propriétés pour personnaliser le thème.

```
{ 
 "globalCssText":"@import url('https://fonts.googleapis.com/css2?family=Grandstander:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');", 
 "fontNames":"Grandstander", 
 "cardLayout":{ 
 "cardLayoutName":"compact", 
 "cardPrimaryColor":"#376BA4", 
 "cardSecondaryColor":"#F98EB0", 
 "startedStateTextColor":"#ffffff", 
 "continueStateTextColor":"#ffffff", 
 "revisitStateTextColor":"#ffffff", 
 "startedStateColor":"#a0a0a0", 
 "continueStateColor":"#f9a122", 
 "revisitedStateColor":"#7fbc64", 
 "textPrimaryColor":"#ffffff", 
 "textSecondaryColor":"#d93f3f", 
 "navIconColor":"#a0a0a0" 
 } 
}
```

### Ignorer l’inscription LO de niveau supérieur

Si le **Ignorer l’inscription LO de niveau supérieur** Si la case est cochée et qu’un utilisateur est inscrit directement dans un programme d’apprentissage ou une certification, les cours de cette certification ou de ce programme d’apprentissage s’afficheront pour l’utilisateur dans les widgets.

Si la case à cocher est désactivée, les cours présents dans le programme d’apprentissage ou la certification où l’utilisateur n’est pas inscrit directement ne s’affichent pas.

![](assets/higher-order-lo.png)

*Cochez la case Ignorer l’inscription LO de niveau supérieur.

Le paramètre est ensuite appliqué au widget.

### Sécurité

Les champs ID du client et Secret du client sont ajoutés. En outre, le jeton d’actualisation est masqué. Après qu’un utilisateur a créé la configuration entière, s’il ouvre à nouveau la configuration pour la modifier ou si un autre utilisateur ouvre cette configuration, le jeton d’actualisation est masqué.
