---
jcr-language: en_us
title: Intégration d’Adobe Learning Manager à AEM
description: Découvrez comment intégrer Adobe Learning Manager à Adobe Experience Manager (AEM)
contentowner: saghosh
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 44%

---



# Intégration de Learning Manager à AEM

## Vue d’ensemble {#overview}

Learning Manager est un système de gestion de l’apprentissage doté d’un système de gestion de contenu d’apprentissage intégré. Les utilisateurs gèrent leur contenu d’apprentissage en le chargeant vers Learning Manager, de sorte que Learning Manager exécute le contrôle de version, l’allocation aux cours, la définition de la visibilité pour les élèves, le suivi de la consommation et la génération de rapports aux administrateurs.

Toutefois, certains utilisateurs stockent et gèrent leur contenu sur des systèmes de gestion des ressources. Le contenu est ensuite réaffecté à d’autres fonctions.

Les différentes bandes présentes dans l’application d’apprentissage peuvent être incorporées dans les sites AEM. Tout élève qui se connecte au site AEM verra ses données de formation spécifiques sur ces bandes.

## Téléchargement du package de contenu {#downloadthecontentpackage}

Le programme d’installation est livré sous la forme d’un package de contenu AEM. [***Télécharger le pack***](https://github.com/adobe/captivate-prime-aem-components/releases).

Le package de contenu est disponible sous forme de fichier zip et est compatible avec AEM 6.4 et AEM 6.5.

## Installation du composant Learning Manager {#installcaptivateprimecomponent}

Installez le package de contenu Learning Manager à l’aide du Gestionnaire de packages AEM :

>[!NOTE]
>
>Pour plus d’informations sur l’installation des packs, voir  [***Utilisation des packs***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=en#how-to-work-with-packages).

1. En tant qu’auteur AEM, ouvrez le Gestionnaire de packages AEM.

1. Cliquez sur le bouton **Charger le package**.

1. Cliquez sur **[!UICONTROL Parcourir]** et téléchargez le package de contenu.
1. Cliquez sur **[!UICONTROL Charger]**.
1. Une fois le package chargé, installez le package de contenu en le sélectionnant et en cliquant sur **[!UICONTROL Installer]**.

   ![](assets/install-package.jpg)

## Génération du jeton d’actualisation {#generatetherefreshtoken}

L’administrateur AEM a besoin d’un jeton d’actualisation provenant du compte Learning Manager. L’administrateur de l’intégration Learning Manager générera le jeton d’actualisation.

1. Approuvez l’application proposée Sites AEM.

   Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications fournies]** > **[!UICONTROL Adobe Experience Manager - Sites]**.

   ![](assets/launch-aem.jpg)

1. Cliquez sur **[!UICONTROL Applications]** > **[!UICONTROL Applications fournies]**, puis ouvrez l’application AEM sites.

   Copiez l’ID d’application et la description.

1. Cliquez sur **[!UICONTROL Ressources pour les développeurs]** > **[!UICONTROL Jetons d’accès]**.

   ![](assets/click-tokens.jpg)

1. Saisissez les détails suivants :

   * ID client, qui est l’ID d’application.
   * Secret client, présent dans Description.

1. Obtenez le code OAuth. Vous devez utiliser l’API v2 dans l’URI de redirection.
1. Cliquez sur **[!UICONTROL Envoyer]** et obtenez le jeton d’actualisation.

## Configuration du widget dans AEM {#configurethewidgetinaem}

Pour la configuration du widget, l’auteur AEM n’a besoin que du jeton d’actualisation fourni par l’administrateur de l’intégration de Learning Manager.

Vous pouvez également définir plusieurs configurations de compte dans plusieurs pages.

1. Cliquez sur **[!UICONTROL Outils]** > **[!UICONTROL Cloud Service]** > **[!UICONTROL Configuration du widget Captivate Learning Manager]**.
1. Cliquez sur **[!UICONTROL Créer]**.
1. Entrez ici le jeton d’actualisation. Configurez les autres paramètres.
1. Le nom d’hôte doit être remplacé par « learningmanagereu » pour les régions de l’UE.
1. Enregistrez et fermez la configuration.
1. Sélectionnez une configuration et publiez-la.

## Auteur AEM {#aemauthor}

L’auteur AEM doit d’abord ajouter le composant dans un modèle AEM

L’auteur AEM peut ensuite faire glisser et déposer le composant Adobe Learning Manager et le configurer correctement.

Le composant Learning Manager nécessite que la configuration créée à l’étape ci-dessus soit mappée à la page.  L’auteur peut mapper la configuration en modifiant les propriétés de la page sous **[!UICONTROL Avancé]** > **[!UICONTROL Configuration]** > **[!UICONTROL Configuration du cloud]** et fournir le chemin de configuration. De cette façon, l’auteur peut créer des configurations pour plusieurs comptes Learning Manager et les mapper à une page Sites différente. Si une configuration n&#39;est pas mappée à la page, le composant lit la configuration de la page parent de manière récursive jusqu&#39;à ce qu&#39;il en trouve une.

## Un élève {#learner}

L’élève peut suivre les cours sur la page.

Pour pouvoir accéder au widget Learning Manager, l’élève doit être un utilisateur AEM connecté. Également, propriété **e-mail** doit être présent dans le nœud « /profile » du nœud rep:User de l’élève. Cet e-mail doit être identique à celui indiqué dans le compte Learning Manager.

L’élève peut suivre les cours sur la page.

La progression du cours est également enregistrée.

Les widgets suivants sont fournis :

1. Ludification
1. Calendrier d’apprentissage
1. Widget social
1. Widget Catalogue
1. Mon apprentissage
1. Recommandation sur la base de l’apprentissage des pairs
1. Recommandations par l’administrateur
1. Recommandation sur la base des intérêts des élèves

S’il n’existe aucune recommandation, le widget est vide.

## Prise en charge de Skyline

Skyline est la version cloud d’AEM. Vous devez d’abord installer Skyline à partir du gestionnaire de modules. Pour utiliser le composant Skyline dans AEM, un utilisateur doit être présent dans le compte Learning Manager. En d’autres termes, l’adresse électronique de l’utilisateur doit exister dans le compte.

## Déployer Skyline

Les étapes de configuration de Skyline sont mentionnées dans la section  [référentiel GitHub](https://github.com/adobe/captivate-prime-aem-components).

## Widget Catalogue

Le widget Catalogue affiche la formation d’un catalogue spécifique ou d’un ensemble de catalogues pour un utilisateur. Dans la section Propriétés des propriétés de la page, sélectionnez Catalogue dans les options répertoriées.

![](assets/catalog-widget.png)

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
\{ 
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

Si le **[!UICONTROL Ignorer l’inscription LO de niveau supérieur]** Si la case à cocher est activée et qu’un utilisateur est inscrit directement dans un programme d’apprentissage ou une certification, les cours pour cette certification ou ce programme d’apprentissage s’afficheront pour l’utilisateur dans les widgets.

Si la case à cocher est désactivée, les cours présents dans le programme d’apprentissage ou la certification où l’utilisateur n’est pas inscrit directement ne s’affichent pas.

![](assets/higher-order-lo.png)

Le paramètre est alors appliqué au widget.

### Protection

Les champs ID du client et Secret du client sont ajoutés. En outre, le jeton d’actualisation est masqué. Après qu’un utilisateur a créé la configuration entière, s’il ouvre à nouveau la configuration pour la modifier ou si un autre utilisateur ouvre cette configuration, le jeton d’actualisation est masqué.
