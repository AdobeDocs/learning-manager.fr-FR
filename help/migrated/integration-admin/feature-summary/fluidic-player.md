---
description: Lisez cet article pour découvrir comment intégrer le lecteur Fluidic dans une application personnalisée.
jcr-language: en_us
title: Lecteur Fluidic intégrable
contentowner: dvenkate
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---



# Lecteur Fluidic intégrable

Lisez cet article pour découvrir comment intégrer le lecteur Fluidic dans une application personnalisée.

En tant qu’entreprise, vous pouvez désormais fournir une expérience personnalisée à vos élèves même en dehors de Learning Manager. À l’aide de l’API publique, vous pouvez récupérer toutes les informations liées aux objets d’apprentissage, aux inscriptions des élèves et à la progression de l’apprentissage et les afficher sur votre site Web. Plus important encore, vous pouvez même intégrer le lecteur Fluidic de Learning Manager dans votre site Web, afin que l’élève puisse utiliser le contenu directement sur votre site Web. Le lecteur Fluidic vous permet de lire n’importe quel contenu pris en charge par Learning Manager. Lorsqu’il est intégré à votre propre site Web, il possède exactement les mêmes fonctionnalités que lorsqu’il est utilisé dans Learning Manager.

**Lire n’importe quel contenu de formation en ligne[](../../learners/feature-summary/fluidic-player.md#main-pars_text_779047019)**

Le lecteur Fluidic lit pratiquement n’importe quel type de contenu de formation en ligne de la même manière cohérente et intuitive sans nécessiter de plug-ins ou de téléchargements. L’élève peut lancer le contenu et, quel que soit le type de fichier de contenu, la lecture commence.

**Notes et marquage de signets**

Vous pouvez prendre des notes et ajouter des signets à n’importe quel contenu, quel que soit son type de fichier. Si vous voulez faire une certaine sélection à partir d&#39;un long fichier ou d&#39;une vidéo, vous pouvez mettre en signet les points mêmes où vous avez trouvé les informations qui sont pertinentes à vos besoins. Les notes et les signets peuvent être recherchés ou envoyés par e-mail. Un clic dessus vous place dans le lecteur Fluidic exactement à ce point de la vidéo ou de la page du document.

Pour plus d’informations sur le lecteur Fluidic, voir [Lecteur Fluidic](../../learners/feature-summary/fluidic-player.md).

Voici quelques exemples d’utilisation du lecteur Fluidic intégrable.

* Vous pouvez utiliser le lecteur Fluidic intégrable sur votre site Web **** pour répertorier les cours auxquels votre employé est inscrit et également fournir un lien permettant de lancer une formation sur la même page. Cela signifie que vos élèves peuvent suivre des formations sur votre site intranet.

* Si vous êtes dans le domaine de la formation, vous avez peut-être un site Web où vos clients achètent des cours. Vous pouvez intégrer le lecteur au même site Web afin que vos clients puissent utiliser le contenu qu’ils achètent sur votre site Web.

## Étapes pour intégrer le lecteur Fluidic à votre site web {#stepstoembedfluidicplayerinyourwebsite}

La création d’une application personnalisée pour intégrer le lecteur Fluidic à votre site web implique trois étapes de base :

1. Créez une application dans l’application d’administration d’intégration de Learning Manager.
1. Récupérer le jeton d’accès.
1. Utilisez le jeton d’accès pour récupérer des ressources de Learning Manager à l’aide de l’API publique.

### 1. Création d’une application dans l’administrateur d’intégration {#1createanapplicationinintegrationadmin}

Cette étape est nécessaire pour créer un ID d’application/client et un secret d’application/client qui est utilisé pour récupérer le jeton d’actualisation et le jeton d’accès. Pour plus d’informations sur la création d’une application, voir  [Processus de développement d’applications.](developer-manual.md#main-pars_header_994876235)

1. Accéder à **[!UICONTROL IntegrationAdmin]** application et ouvrir **[!UICONTROL Applications]**.

1. Sélectionner **[!UICONTROL S&#39;inscrire]** dans le coin supérieur droit de la page.
1. Le **[!UICONTROL Enregistrer une nouvelle application]** s’ouvre. Renseignez les champs requis.
1. Si l’application personnalisée doit être partagée entre plusieurs comptes, sélectionnez **[!UICONTROL Non]** dans le champ option  **[!UICONTROL Pour ce compte uniquement ?]**
1. Pour enregistrer l’application et générer votre ID et votre secret d’application, cliquez sur **[!UICONTROL Enregistrer]**.

### 2. Récupération du jeton d’accès {#2retrievingaccesstoken}

Comme Learning Manager utilise OAUTH2.0., un jeton d’accès est requis pour récupérer des ressources à l’aide de l’API publique. Le jeton d’accès peut être récupéré à l’aide du jeton d’actualisation, de l’ID client ou du secret client.

**2.1 Jeton d’actualisation**

* Récupérer le code OAuth

Le code OAuth est requis pour récupérer le jeton d’actualisation. Learning Manager redirige l’utilisateur vers l’URL de redirection avec le code OAuth lorsqu’il est connecté à l’aide de l’URL ci-dessous (l’extraction de code OAuth est illustrée dans le fichier « oauthredirect.html » de l’exemple d’application) :

```
code https://learningmanager.adobe.com/oauth/o/authorize  
client_id= <application_id>  
&redirect_uri=<redirect_uri>  
&state=<dummy_data>  
&scope=learner:read,learner:write  
&response_type=CODE  
&account=<account_id>  
&email=<email_id>
```

Ici, **[!UICONTROL id client]** est l&#39;id d&#39;application obtenu à l&#39;étape 1.
**[!UICONTROL redirect_url]** est l&#39;url_redirection définie à l&#39;étape 1.
**[!UICONTROL état]** est une donnée fictive basée sur laquelle nous devons filtrer l’URL de redirection pour obtenir le code OAuth. La portée est la portée de l’élève définie à l’étape 1.
**[!UICONTROL response_type]**e est toujours « CODE ».\
**[!UICONTROL compte]**est un champ facultatif\
**[!UICONTROL e-mail]** est un champ facultatif\
&#42; Si l’ID de compte et l’adresse électronique sont fournis, l’URL ci-dessus permettra à l’utilisateur de se connecter au même compte. Cet exemple de point de terminaison est décrit dans le fichier « index.html » dans l’exemple d’application.

* Récupérer le jeton d’actualisation

Une fois le code OAuth reçu, le jeton d’actualisation peut être récupéré à l’aide du code OAuth, de l’ID client et du secret client reçus à partir du point d’entrée ci-dessous :

**https://learningmanager.adobe.com/oauth/token**

En réponse à votre demande de publication, vous recevrez ce qui suit :

i. refresh_token\
ii. access_token\
iii. user_id\
iv. expires_in\
v. user_role\
vi. account_id

**2.2 Récupération du jeton d’accès à partir du jeton d’actualisation**

Pour récupérer votre jeton d’accès, envoyez une autre demande avec vos paramètres refresh_token, client_id et client_secret en tant que corps de message à l’URL ci-dessous :

**https://learningmanager.adobe.com/oauth/token/refresh**

En réponse à votre demande de publication, vous recevrez ce qui suit :\
i. refresh_token\
ii. access_token\
iii. user_id\
iv. expires_in\
v. user_role\
vi. account_id

### 3. Récupérer des ressources à l’aide de l’api publique {#3retrieveresourcesusingpublicapi}

Comme troisième étape, vous devez utiliser le jeton d’accès pour récupérer des ressources de Learning Manager à l’aide de l’api publique .  Le jeton d’accès est requis pour effectuer tout appel d’api public et doit être ajouté dans l’en-tête comme illustré dans l’exemple d’application.

## Lecteur intégrable {#embeddableplayer}

Les applications tierces peuvent utiliser un lecteur intégrable pour lire le contenu d’un objet d’apprentissage.

**Ouvrir un cours dans un lecteur intégrable**

1. Création d’une URL intégrable

   Pour ouvrir un cours à l&#39;aide d&#39;un lecteur intégrable, vous devez créer une URL intégrable comme indiqué ci-dessous :

   `https://learningmanager.adobe.com/app/player?lo_id=<v2-api course id>&access_token=<access_token>`

   Ici, lo_id doit être conforme au format d’ID de cours de l’API V2.

   Exemple : `https://learningmanager.adobe.com/app/player?lo_id=course:123456&access_token=45b269b75ac65d6696d53617f512450f`

   Les certifications, programmes d’apprentissage et assistances à la tâche peuvent également être lus dans le lecteur intégrable.

   Exemples : `https://learningmanager.adobe.com/app/player?lo_id=certification:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=learningProgram:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=jobAid:1234&access_token=c1a4847dfbf4007826a027d481b93c1e`

1. Définissez cette URL dans l’attribut « src » de iframe.

**Fermeture du lecteur intégrable**

```
code window.addEventListener("message", function closePlayer(){  
   if(event.data === "status:close"){  
     //handle closing event  
   }  
});
```

## Exemple de tutoriel d’application {#sampleapplicationtutorial}

Le document pdf joint contient un exemple de tutoriel d’application.
[Exemple de source de tutoriel et de didacticiel pour intégrer le lecteur Fluidic](assets/sample-applicationtutorial.zip) Contenus alternatifs

Si vous êtes un administrateur, vous pouvez configurer votre matériel de cours de manière à proposer un contenu alternatif à vos élèves dans le lecteur Fluidic. Par exemple, si des élèves de différentes zones géographiques peuvent vouloir utiliser plusieurs langues, vous pouvez créer le même contenu dans plusieurs langues. Le lecteur Fluidic offrira à l&#39;élève la langue pour laquelle il pourrait être configuré, mais l&#39;élève a également le choix de passer à une autre langue directement à partir du lecteur.

Commandes spécifiques à la vidéo

La technologie de diffusion en continu utilisée par le lecteur Fluidic de Learning Manager offre une expérience de lecture vidéo à ses élèves sans aucun retard dans le démarrage de la vidéo et sans aucune exigence d’espace disque sur aucun appareil. Le lecteur Fluidic offre également des commandes intelligentes telles que la vitesse de lecture (1x, 1,5X) et l&#39;option Sauter +-10 secondes, qui sont conçues pour donner à l&#39;élève le niveau de contrôle exact dont il a besoin pour correspondre à sa vitesse d&#39;apprentissage.

Il s&#39;agit d&#39;un effort qui doit être entrepris par une personne de votre équipe informatique ou un consultant externe qui peut créer une application qui est ensuite hébergée sur votre site.

1. Modifiez l’URL du lecteur intégré Learning Manager avec des paramètres qui pointent vers l’objet d’apprentissage exact qui doit être pris.

   URL :  [https://learningmanager.adobe.com/app/player](https://cpcontents.adobe.com/public/embedplayer/index22fa615ec2baa034a22090c8cd4289fa.html)

1. Utilisez l’un de ces paramètres pour lancer un cours :

   * course_id : ID du cours à lancer
   * learning_program_id : ID du programme d’apprentissage à lancer
   * certification_id : ID de certification à lancer
   * lo_id : ID de l’objet d’apprentissage (cours/programme d’apprentissage/certification/assistance à la tâche) à lire


1. Utiliser le jeton d’accès comme paramètre obligatoire.

   * access_token : il s’agit du paramètre de sécurité, utilisez le jeton d’accès oauth de l’API publique

   Vous pouvez obtenir votre jeton en configurant votre lecteur Fluidic intégrable dans votre administrateur d’intégration. Vous pouvez obtenir votre jeton d’authentification qui peut être utilisé comme jeton d’accès.

   Exemple d’URL créée ; https://learningmanager.adobe.com/app/player?lo_id=« +lo_id+« &amp;access_token=« +accToken

   Ici, lo_id sera l’identifiant du cours, du programme d’apprentissage, de la certification et de l’assistance à la tâche .

   Exemples de lo_id - course:21324, learningProgram:2143, certification:23432, jobAid:237

1. Effectuez des appels API Learning Manager pour récupérer les paramètres susmentionnés.

   Ces appels d&#39;API doivent être effectués par l&#39;application que votre équipe informatique/consultant rédigerait et hébergerait sur votre site.

   Pour plus d’informations sur l’utilisation de l’API, cliquez ici :

   API Learning Manager V1 - [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



   API Learning Manager V2 - [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)

   Les ID des objets diffèrent de ceux de l’API V1 et V2. Le lecteur intégrable attend des ID au format v2. Utilisez l’API de mappage d’ID dans la version 2 pour convertir des ID V1 en ID V2.

   Après avoir créé l’URL, l’application peut l’utiliser pour l’afficher à l’élève en la plaçant dans un iFrame. En cliquant sur ce lien, le lecteur Fluidic est lancé avec le cours particulier en contexte.

   ![](assets/salesforce-player.png)

   Pour vérifier les rapports d’avancement et d’achèvement, connectez-vous à Learning Manager.

   Lorsque l’élève ferme le lecteur, le lecteur Fluidic envoie un message « fermer » à l’élément parent à l’aide de html5 postMessage. Le contrôleur de chargement doit traiter ce message et continuer.

Modifiez l’URL du lecteur intégré Learning Manager avec des paramètres qui pointent vers l’objet d’apprentissage exact qui doit être pris.

URL :  [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player)

L’un de ces paramètres peut être utilisé pour lancer un cours :

* course_id : ID du cours à lancer
* learning_program_id : ID du programme d’apprentissage à lancer
* certification_id : ID de certification à lancer
* lo_id : ID de l’objet d’apprentissage (cours/programme d’apprentissage/certification/assistance à la tâche) à lire

Paramètre obligatoire :

* access_token : il s’agit du paramètre de sécurité, utilisez le jeton d’accès oauth de l’API publique

Effectuez des appels API Learning Manager pour récupérer les paramètres susmentionnés. Ces appels d&#39;API doivent être effectués par l&#39;application que votre équipe informatique/consultant rédigerait et hébergerait sur votre site.

Pour plus d’informations sur l’utilisation de l’API, cliquez ici :

API Learning Manager V1 - [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



API Learning Manager V2 -  [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)


