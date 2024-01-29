---
jcr-language: en_us
title: Manuel du développeur d’applications
description: L’API Learning Manager V1 est désormais obsolète. Les API V1 cesseront de fonctionner à partir du 28 février 2021. Nous vous recommandons d’utiliser les API V2 pour interagir avec Learning Manager.
contentowner: jayakarr
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '3279'
ht-degree: 0%

---



# Manuel du développeur d’applications

L’API Learning Manager V1 est désormais obsolète. Les API V1 cesseront de fonctionner à partir du 28 février 2021. Nous vous recommandons d’utiliser les API V2 pour interagir avec Learning Manager.

## Présentation {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) est une solution de gestion de l’apprentissage en libre-service, centrée sur l’élève et hébergée sur le cloud. Les clients peuvent accéder aux ressources Learning Manager par programme à l’aide de l’API Learning Manager pour les intégrer à d’autres applications d’entreprise. L’API peut également être utilisée par les partenaires d’Adobe pour améliorer la proposition de valeur de Learning Manager, en étendant ses fonctionnalités ou en les intégrant à d’autres applications ou services.

### Scénario d’utilisation {#usagescenario}

À l’aide de l’API Learning Manager, les développeurs peuvent créer des applications autonomes qui étendent les fonctionnalités de Learning Manager ou intègrent Learning Manager à d’autres workflows d’applications d’entreprise. Vous pouvez développer une application web, un client de bureau ou une application mobile en utilisant la technologie de votre choix. En tant que développeur, vous pouvez accéder aux données de votre application depuis Learning Manager. Le déploiement de l’application que vous développez est externe à la plate-forme Learning Manager et vous avez un contrôle total sur le cycle de vie du développement logiciel à mesure que l’application évolue. En règle générale, les applications sont développées par une organisation cliente pour être utilisées avec son compte Learning Manager, et ces applications sont privées pour cette organisation cliente spécifique. En outre, les partenaires Adobe peuvent créer des applications génériques avec l’API Learning Manager, qui peut être utilisée par un grand nombre de clients Learning Manager.

## API Learning Manager {#apidescription}

L’API Learning Manager est basée sur les principes REST et expose les éléments clés du modèle d’objet Learning Manager aux développeurs d’applications via HTTP. Avant de connaître les détails des points de terminaison API et des méthodes HTTP, les développeurs peuvent se familiariser avec les différents objets Learning Manager, leurs attributs et leurs relations. Une fois les modèles compris, il sera utile d’acquérir une compréhension de base de la structure des demandes et des réponses d’API, ainsi que de quelques termes de programmation courants que nous utilisons de manière générique dans l’API.

Pour plus d’informations sur les différents points de terminaison et méthodes API, reportez-vous à la section  [Documentation de l’API Learning Manager](https://learningmanager.adobe.com/docs/primeapi/v2/).

## Authentification API {#apiauthentication}

Lors de l’écriture d’une application qui effectue des appels API vers Learning Manager, vous devez enregistrer votre application à l’aide de l’application d’administration de l’intégration.

Les API Learning Manager utilisent la structure OAuth 2.0 pour authentifier et autoriser vos applications clientes.

**Procédure**

**1. Configuration de l’application**

Vous pouvez configurer votre application avec l’ID client et le secret client pour utiliser les points de terminaison appropriés. Une fois l’application enregistrée, vous pouvez obtenir les paramètres clientId et clientSecret. Get URL doit être utilisé dans le navigateur, car il authentifie les utilisateurs de Learning Manager à l’aide de leurs comptes préconfigurés tels que SSO, Adobe ID, etc.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Une fois l’authentification réussie, votre navigateur redirige vers redirect_uri mentionné dans l’URL ci-dessus. Paramètre A **code** est ajouté avec l’uri de redirection.

**2. Obtenir le jeton d’actualisation à partir du code**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Corps de la requête de publication :

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  code: 
  <code from step 1></code>
 </enter>
</enter>
```

**3.** **Obtenir un jeton d’accès à partir du jeton d’actualisation**

URL d’obtention du jeton d’accès :

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Content-Type : application/x-www-form-urlencoded

Corps de la requête de publication :

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  refresh_token: 
  <refresh token>
   
  </refresh>
 </enter>
</enter>
```

**URL de vérification des détails du jeton d’accès**

`GET https://learningmanager.adobe.com/oauth/token/check?access_token=<access_token>`

**Limitation d’utilisation**

Un jeton d’accès est valide pendant sept jours. Après une journée, vous devez générer un nouveau jeton d’accès à l’aide du jeton d’actualisation. Si vous générez un nouveau jeton d’accès à partir du jeton d’actualisation alors qu’un jeton d’accès existant est toujours valide, le jeton existant est renvoyé.

Certains termes fréquemment utilisés dans l’API Learning Manager sont expliqués ci-dessous pour référence.

**Comprend**

Les développeurs peuvent accéder à un seul modèle d’objet API ainsi qu’à plusieurs modèles associés à ce modèle. Pour accéder aux modèles associés suivants, vous devez comprendre la relation de chaque modèle avec les autres modèles. **Comprend** permet aux développeurs d&#39;accéder aux modèles dépendants. Vous pouvez utiliser le séparateur de virgule pour accéder à plusieurs modèles. Pour obtenir un exemple d’utilisation et plus de détails sur **comprend**, reportez-vous à la section d’exemple de modèle d’API dans cette page.

**requête API**

Les demandes d’API peuvent être effectuées en effectuant une requête HTTP. Selon le point de terminaison et la méthode, le développeur peut avoir le choix entre divers verbes HTTP tels que GET, PUT, POST, DELETE, PATCH, etc. Pour certaines demandes, les paramètres de requête peuvent être transmis. Lors d’une demande pour un modèle de données spécifique, l’utilisateur peut également demander des modèles associés comme décrit dans les spécifications de l’API JSON. La structure d’une requête d’API typique est décrite dans [exemple d’utilisation du modèle](#main-pars_header_1415780624).

**Réponse de l’API**

Lorsqu’une demande API est effectuée par un client, un document SON est obtenu conformément à la spécification de l’API JSON. La réponse contient également le code d’état HTTP, que le développeur peut vérifier pour effectuer les étapes suivantes appropriées dans sa logique d’application. La structure d’une réponse d’API typique est décrite dans  [exemple d’utilisation du modèle](#main-pars_header_1415780624).

**Erreurs**

Lorsqu’une demande d’API échoue, une réponse d’erreur est obtenue. Le code d’état HTTP renvoyé dans la réponse indique la nature de l’erreur. Les codes d’erreur sont représentés par des numéros pour chaque modèle dans la référence API. 200, 204, 400 et 404 sont quelques-unes des erreurs courantes représentées dans les API indiquant des problèmes d’accès HTTP.

**Champs**

Les attributs de l’objet API et ses relations sont collectivement appelés Champs. Reportez-vous à [API JSON pour plus d’informations.](http://jsonapi.org/format/#document-resource-object-fields) Vous pouvez utiliser Fields comme paramètre lors des appels API pour récupérer un ou plusieurs attributs spécifiques à partir du modèle. En l&#39;absence du paramètre Fields, l&#39;appel API récupère tous les attributs disponibles à partir du modèle. Par exemple, dans l’appel API suivant, les champs[compétence]=name vous récupère l&#39;attribut name du modèle de compétence seul.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Pagination**

Parfois, une demande d’API entraîne une longue liste d’objets à retourner dans la réponse. Dans de tels cas, l’attribut de pagination permet au développeur de récupérer les résultats de manière séquentielle en termes de plusieurs pages, chaque page contenant une plage d’enregistrements. Par exemple, l’attribut de pagination dans Learning Manager vous permet de définir le nombre maximal d’enregistrements à afficher dans une page. Vous pouvez également définir la valeur de plage des enregistrements à afficher sur la page.

**Tri**

Le tri est autorisé dans les modèles API. En fonction du modèle, choisissez le type de tri à appliquer pour les résultats. Le tri peut être appliqué par ordre croissant ou décroissant. Par exemple, si vous spécifiez `code sort=name`, puis tri par nom croissant. Si vous `code sort=-name`, il s’agit d’un tri par nom décroissant. Reportez-vous à [Spécification d’API JSON pour plus d’informations](http://jsonapi.org/format/#fetching-sorting).

## Illustration de l’utilisation de l’API {#samplemodel}

Imaginons un scénario dans lequel un développeur souhaite obtenir le nom de la compétence, le nombre maximal de points attribués pour le niveau de compétence et les points obtenus par l’élève pour cette compétence.

Un modèle userSkill dans les API Learning Manager est constitué des attributs par défaut suivants : id, type, dateAchived, dateCreated et pointsEarned. Ainsi, lorsqu’un développeur utilise la méthode GET pour acquérir des détails du modèle userSkill, les données courantes relatives aux attributs par défaut sont affichées dans la sortie de la réponse.

Mais, dans ce scénario, le développeur souhaite obtenir le nom de la compétence et les points de niveau de compétence pour l’utilisateur. L’API Learning Manager vous permet d’accéder à ces informations associées à l’aide des champs de relation et du paramètre include. Les modèles associés pour userSkill sont obtenus dans la balise Relations. Vous pouvez obtenir les détails de chaque modèle associé en appelant ces modèles avec userSkill. Pour obtenir ces informations, utilisez **`code include`** paramètre avec des valeurs séparées par des points (point) pour chacun des modèles associés. Vous pouvez utiliser une virgule comme séparateur pour demander un autre modèle comme l’utilisateur include=skillLevel.skill, course

**Appel API**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

Par exemple, userId peut être 746783 et userSkills id : 746783_4426_1.

**Réponse de l’appel API**

```
\{ 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1?include=skillLevel.skill&fields[userSkill]=pointsEarned&fields[skillLevel]=maxCredits&fields[skill]=name"}, 
 "data": { 
 "id": "746783_4426_1", 
 "type": "userSkill", 
 "attributes": {"pointsEarned": 5}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1"} 
 }, 
 "included": [ 
 { 
 "id": "4426", 
 "type": "skill", 
 "attributes": {"name": "Java"}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/skills/4426"} 
 }, 
 { 
 "id": "4426_1", 
 "type": "skillLevel", 
 "attributes": {"maxCredits": 10} 
 } 
 ] 
} 
```

## Modèles Learning Manager {#models}

L’API Learning Manager permet aux développeurs d’accéder aux objets Learning Manager en tant que ressources RESTful. Chaque point de terminaison d’API représente une ressource, généralement une instance d’objet comme Badge, ou une collection de tels objets. Les développeurs utilisent ensuite les verbes HTTP tels que PUT, GET, POST et DELETE pour effectuer les opérations CRUD sur ces objets (collections).

API +++V1

Le diagramme suivant représente les différents éléments du modèle d’objet Learning Manager dans l’API V1.

![](assets/er-diag-primemodels.png)

Le tableau suivant décrit les différents éléments du modèle objet Learning Manager V1 :

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>N° de série</strong></p></td>
   <td>
    <p><strong>Objet Learning Manager</strong></p></td>
   <td>
    <p><strong>Description</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>utilisateur</p></td>
   <td>
    <p>L’utilisateur est le modèle clé dans Learning Manager. Les utilisateurs sont généralement les élèves internes ou externes d’une organisation qui utilisent des objets d’apprentissage. Cependant, ils peuvent jouer d’autres rôles, tels que l’auteur et le responsable, en même temps que le rôle d’élève. L’ID utilisateur, le type et l’adresse e-mail font partie des attributs en ligne. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>cours</p></td>
   <td>
    <p>Le cours est l’un des objets d’apprentissage pris en charge dans Learning Manager, qui se compose d’un ou plusieurs modules. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>module</p></td>
   <td>
    <p>Le module est une composante permettant de créer des objets d’apprentissage dans Learning Manager. Les modules peuvent être de quatre types différents tels que salle de classe, salle de classe virtuelle, activité et auto-apprentissage. Utilisez ce modèle de module pour obtenir les détails de tous les modules d’un compte. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certification</p></td>
   <td>
    <p>La certification est accordée aux élèves en fonction de l’achèvement réussi des cours. Les cours sont requis dans l’application avant d’utiliser les certifications. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>programme d'apprentissage</p></td>
   <td>
    <p>Les programmes d’apprentissage sont des cours conçus de manière unique pour répondre aux besoins d’apprentissage spécifiques des utilisateurs. En règle générale, les programmes d’apprentissage sont utilisés pour atteindre des objectifs d’apprentissage couvrant plusieurs cours individuels. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>badge</p></td>
   <td>
    <p>Le badge est un jeton d’accomplissement que les élèves reçoivent lorsqu’ils atteignent des étapes spécifiques tout au long d’un cours. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>compétence</p></td>
   <td>
    <p>Le modèle de compétences se compose de niveaux et de crédits. Les compétences peuvent être acquises par les élèves après la fin du cours concerné. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnenrollment</p></td>
   <td>
    <p>Ce modèle fournit des détails sur l'inscription d'un utilisateur à une certification unique.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnenrollment</p></td>
   <td>
    <p>Ce modèle fournit des détails sur l'inscription d'un utilisateur à un cours unique. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Un cours peut être associé à une ou plusieurs instances. Vous pouvez obtenir l’instance de cours </p></td>
  </tr>
  <tr>
   <td>
    <p>11.  </p></td>
   <td>
    <p>courseSkill</p></td>
   <td>
    <p>Un modèle courseSkill spécifie la progression d'une seule compétence obtenue en suivant un cours.</p></td>
  </tr>
  <tr>
   <td>
    <p>12.  </p></td>
   <td>
    <p>courseModule</p></td>
   <td>Un modèle courseModule spécifie comment un module est inclus dans un cours. Par exemple, si le module est utilisé pour le test préliminaire ou pour le contenu.</td>
  </tr>
  <tr>
   <td>
    <p>13.  </p></td>
   <td>learningProgramInstance</td>
   <td>
    <p>Un programme d’apprentissage peut consister en plusieurs instances qui imbibent des propriétés similaires d’un programme d’apprentissage ou en instances personnalisées. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>assistance à la tâche</p></td>
   <td>
    <p>L’assistance à la tâche est un contenu d’apprentissage accessible aux élèves sans aucun critère d’inscription ou d’achèvement. Vous pouvez récupérer, mettre à jour la date, l’état, les informations d’identification ainsi que les modèles associés tels que la version de l’assistance à la tâche, les auteurs et le niveau de compétence. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>Une ou plusieurs versions peuvent être associées à l’assistance à la tâche en fonction du nombre de révisions de contenu et du nombre de téléchargements. Ce modèle fournit des détails sur une version d’assistance à la tâche unique. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnenrollment</p></td>
   <td>
    <p>Le programme d’apprentissage se compose d’une ou de plusieurs instances. Les élèves peuvent s'inscrire à une instance de programme d'apprentissage par eux-mêmes ou attribués par l'administrateur. Ce modèle fournit les détails d'une inscription par un utilisateur à une seule instance de programme d'apprentissage. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Un module peut avoir une ou plusieurs versions en fonction de ses téléchargements de contenu révisés. Utilisez ce modèle pour obtenir des informations spécifiques sur une version de module unique. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Un niveau de compétence comprend un ou plusieurs cours à consommer afin d'acquérir un niveau ainsi que ses crédits associés. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge associe un badge unique à un utilisateur unique. Il contient des détails tels que quand il a été atteint, assertionUrl et ainsi de suite. </p></td>
  </tr>
  <tr>
   <td>
    <p>20.  </p></td>
   <td>
    <p>userSkill</p></td>
   <td>
    <p>UserSkill indique la proportion d’un niveau de compétence unique atteinte par un seul utilisateur.</p></td>
  </tr>
 </tbody>
</table>

+++

API +++V2

Voici les différents éléments du diagramme de classes de Learning Manager dans l’API V2.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Objet Learning Manager</b></th>
   <th><b>Description</b></th>
  </tr>
  <tr>
   <td>compte</td>
   <td>Encapsule les détails d’un client Learning Manager.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>Le badge est un jeton d’accomplissement que les élèves reçoivent lorsqu’ils atteignent des étapes spécifiques tout au long d’un cours. <br></td>
  </tr>
  <tr>
   <td><code>
     catalog
    </code></td>
   <td>Le catalogue est une collection d’objets d’apprentissage.</td>
  </tr>
  <tr>
   <td><code>
     user
    </code></td>
   <td>L’utilisateur est le modèle clé dans Learning Manager. Les utilisateurs sont généralement les élèves internes ou externes d’une organisation qui utilisent des objets d’apprentissage. Cependant, ils peuvent jouer d’autres rôles, tels que l’auteur et le responsable, en même temps que le rôle d’élève. L’ID utilisateur, le type et l’adresse e-mail font partie des attributs en ligne. </td>
  </tr>
  <tr>
   <td>ressource</td>
   <td>Il est utilisé pour modéliser chaque ressource de contenu qu'un module cherche à encapsuler. Toutes les ressources encapsulées dans <code>
     an
    </code> <code>
     loResource
    </code> sont équivalentes en termes d’objectif d’apprentissage, mais diffèrent les unes des autres en termes de type de diffusion ou de paramètres régionaux de contenu.<br></td>
  </tr>
  <tr>
   <td>userNotification</td>
   <td>Ce modèle contient des informations de notification relatives à un élève.<br></td>
  </tr>
  <tr>
   <td>userSkill</td>
   <td>UserSkill indique la proportion d’un niveau de compétence unique atteinte par un seul utilisateur.<br></td>
  </tr>
  <tr>
   <td>userBadge</td>
   <td>UserBadge associe un seul badge <code>
     with
    </code> un seul utilisateur. Il contient des détails tels que la date à laquelle il a été réalisé, <code>
     assertionUrl
    </code> etc. <br></td>
  </tr>
  <tr>
   <td>compétence</td>
   <td>Le modèle de compétences se compose de niveaux et de crédits. Les compétences peuvent être acquises par les élèves après la fin du cours concerné. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Un niveau de compétence comprend un ou plusieurs cours à consommer afin d'acquérir un niveau ainsi que ses crédits associés. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Un objet d’apprentissage est une abstraction pour divers types d’objets auxquels les utilisateurs peuvent s’inscrire et auprès desquels ils peuvent apprendre. Actuellement, Learning Manager propose les quatre types d’objets d’apprentissage : cours, certification et programme d’apprentissage <code>
     and
    </code> Assistance à la tâche.<br></td>
  </tr>
  <tr>
   <td>learningObjectInstance<br></td>
   <td>Instance spécifique d’un objet d’apprentissage.<br></td>
  </tr>
  <tr>
   <td>learningObjectResource</td>
   <td>Cela équivaut au concept de <code>
     module
    </code>. Un cours est composé d'un cours <code>
     of
    </code> plus de modules. Dans Learning Manager, un module peut être fourni de diverses manières équivalentes. Par conséquent, le <code>
     loResource
    </code> représente essentiellement toutes ces ressources équivalentes.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Cela encapsule le résultat obtenu lorsque l’utilisateur consomme une ressource spécifique dans le contexte d’un objet d’apprentissage auquel il est inscrit. Il contient des informations telles que la durée passée par <code>
     user
    </code> dans la ressource, pourcentage de progression effectuée par l’utilisateur, état réussite/échec et score obtenu par l’utilisateur dans tout quiz associé.<br></td>
  </tr>
  <tr>
   <td>calendrier<br></td>
   <td>Un objet Calendrier est une liste de <code>
     upcoming classroom
    </code> ou des cours de classe virtuelle auxquels l’utilisateur peut s’inscrire.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>Le retour d’informations L1 encapsule les réponses fournies par un élève aux questions de retour d’informations associées aux objets d’apprentissage. En général, ces informations sont collectées une fois que l’utilisateur a terminé un objet d’apprentissage s’il est configuré pour collecter ces commentaires des élèves.<br></td>
  </tr>
  <tr>
   <td>inscription<br></td>
   <td>Cette abstraction encapsule les détails relatifs à la transaction représentant l'affectation d'un utilisateur spécifique à une instance d'objet d'apprentissage spécifique.<br></td>
  </tr>
 </tbody>
</table>

+++

Liste des attributs et des relations de l&#39;objet.

+++account

**Attributs**
dateCreated\
gamificationEnabled\
id\
paramètres régionaux\
loginUrl\
logoUrl\
nom\
sous-domaine\
themeData\
timeZoneCode

**Relations**
contentLocales(localizationMetadata)\
gamificationLevels(gamificationLevel)\
timeZones(timeZone)\
uiLocales(localizationMetadata)

+++

+++badge

**Attributs**
id\
imageUrl\
nom\
état

+++

+++catalog

**Attributs**
dateCreated\
dateUpdated\
description\
id\
isDefault\
isInternallySearchable\
isListable\
nom\
état

+++

+++data

**Attributs**
id\
noms

+++

+++ludification

**Attributs**
couleur\
nom\
points

+++

+++learningObject

**Attributs**
authorNames\
dateCreated\
datePublished\
dateUpdated\
effectivenessIndex\
enrollmentType\
id\
imageUrl\
isExternal\
isSubLoOrderEnforced\
loType\
état\
balises

**Relations**
author(user)\
enrollment(learningObjectInstanceEnenrollment)\
instances(learningObjectInstance)\
prerequisiteLOs(learningObject)\
skills(learningObjectSkill)\
subLOs(learningObject)\
additionalLOs(learningObject)\
additionalResources(ressource)

+++

+++learningObjectInstance

**Attributs**
completionDeadline\
dateCreated\
enrollmentCount\
id\
isDefault\
seatLimit\
état\
validité

**Relations**
badge(badge)\
l1FeedbackInfo(feedbackInfo)\
learningObject(learningObject)\
loResources(learningObjectResource)\
localizedMetadata(localizationMetadata)\
subLoInstances(learningObjectInstance)

+++

+++learningObjectInstanceEnenrollment

**Attributs**
dateCompleted\
dateEnrolled\
dateStarted\
hasPassed\
id\
progressPercent\
score\
état

**Relations**
learner(user)\
learnerBadge(userBadge)\
learningObject(learningObject)\
loInstance(learningObjectInstance)\
loResourceGrades(learningObjectResourceGrade)

+++

+++learningObjectResource

**Attributs**
externalReporting\
id\
loResourceType\
resourceType\
version

**Relations**
learningObject(learningObject)\
loInstance(learningObjectInstance)\
localizedMetadata(localizationMetadata)\
resources(resource)

+++

+++learningObjectResourceGrade

**Attributs**
dateCompleted\
dateStarted\
dateSuccess\
durée\
hasPassed\
id\
progressPercent\
score

**Relations**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Attributs**
crédits\
id\
**Relations**
learningObject(learningObject)\
skillLevel(skillLevel)

+++

+++recommandation

**Attributs**
id\
raison

**Relations**
learningObject(learningObject)

+++

+++resource

**Attributs**
authorDesiredDuration\
completionDeadline\
contentStructureInfoUrl\
contentType\
contentZipSize\
contentZipUrl\
dateCreated\
dateStart\
requiredDuration\
downloadUrl\
extraData\
hasQuiz\
hasToc\
id\
instructorNames\
isDefault\
paramètres régionaux\
emplacement\
nom\
onlyQuiz\
reportingInfo\
reportingType\
seatLimit

+++

+++skill

**Attributs**
description\
id\
nom\
état

**Relations**
levels(skillLevel)

+++

+++skillLevel

**Attributs**
id\
niveau\
maxCredits\
nom\
**Relations**
badge(badge)\
skill(skill)

+++

+++user

**Attributs**
avatarUrl\
bio\
contentLocale\
e-mail\
champs\
id\
nom\
pointsEarned\
profil\
rôles\
état\
timeZoneCode\
uiLocale

**Relations**
account(account)\
manager(user)

+++

+++userBadge

**Attributs**
assertionUrl\
dateAchived\
id\
modelType

**Relations**
badge(badge)\
learner(user)\
model(learningObject)

+++

+++userCalendar

**Attributs**
cours\
courseType\
dateStart\
inscrit\
id\
mois\
quart

**Relations**
containerLO(learningObject)\
course(learningObject)

+++

+++userNotification

**Attributs**
actionUsed\
canal\
dateCreated\
id\
message\
modelIds\
modelNames\
modelTypes\
lire\
rôle

+++

+++userSkill

**Attributs**
dateAchived\
dateCreated\
id\
pointsEarned

**Relations**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(user)

+++

## Processus de développement d’applications {#registration}

## Conditions préalables {#prerequisites}

En tant que développeur, vous devez créer un compte d’évaluation sur Learning Manager afin de pouvoir accéder pleinement à tous les rôles au sein de ce compte. Pour pouvoir écrire une application, un développeur doit créer des utilisateurs et des cours, puis placer le compte dans un état raisonnable afin que l’application en cours de développement puisse avoir accès à des exemples de données.

## Création d’un ID client et d’un secret {#createclientidandsecret}

1. Entrée **Administrateur de l’intégration** connexion, cliquez sur **[!UICONTROL Applications]** dans le volet de gauche.

   ![](assets/application-development-menu.png)

   *Sélectionner des applications dans l’administrateur d’intégration*

1. Cliquez sur **[!UICONTROL S&#39;inscrire]** dans le coin supérieur droit de la page pour enregistrer les détails de votre candidature. La page d’inscription s’affiche.

   ![](assets/register-application.png)

   *Enregistrement de l’application*

   Il est obligatoire de remplir tous les champs de cette page.

   **Nom de l’application**: saisissez le nom de votre application. Il n&#39;est pas obligatoire d&#39;utiliser le même nom d&#39;application, il peut s&#39;agir de n&#39;importe quel nom valide.

   **URL**: Si vous connaissez l’URL exacte où l’application est hébergée, vous pouvez la mentionner. Si vous ne le savez pas, vous pouvez mentionner l’URL de votre société. Un nom d’URL valide est obligatoire dans ce champ.

   **Redirection de domaines**: entrez le nom de domaine de l’application vers laquelle vous souhaitez que l’application Learning Manager redirige après l’authentification OAuth. Vous pouvez mentionner plusieurs URL ici, mais vous devez utiliser les URL valides telles que `http://google.com`, `http://yahoo.com` etc.

   **Description :** Saisissez la brève description de votre application.

   **Portées :** Choisissez l’une des quatre options disponibles pour définir la portée de votre application. En fonction de votre choix mentionné ici, le point de terminaison de l’API Learning Manager est accessible pour votre application. Par exemple, si vous choisissez **Accès en lecture au rôle d’élève**, tous les points de terminaison de l’API de l’élève Learning Manager sont alors accessibles en lecture seule à votre application.

   **Pour ce compte uniquement ?**\
   **Oui** - si vous choisissez Oui, l’application n’est pas visible par les autres administrateurs de compte.\
   **Non** - Si vous choisissez Non, les autres administrateurs de compte peuvent également accéder à cette application, mais ils doivent utiliser l’id de l’application pour y accéder. L’ID d’application est généré et affiché en mode de modification d’application Learning Manager.

   Si vous **Accès en lecture et en écriture au rôle d’administrateur** comme portée lors de l’enregistrement de l’application et choisissez **Accès en lecture au rôle d’administrateur** lors de la création des API, vous pouvez toujours avoir un accès en écriture pour l’application, car la portée d’enregistrement de l’application remplace le workflow d’autorisation.

1. Cliquez sur **[!UICONTROL S&#39;inscrire]** dans le coin supérieur droit après avoir renseigné les détails dans la page d’enregistrement.

## Développement et test d’applications {#applicationdevelopmentandtesting}

Les développeurs peuvent utiliser l’API Learning Manager pour créer n’importe quelle application. Les développeurs doivent s’assurer que leurs comptes comprennent des utilisateurs et des cours valides. Ils peuvent créer quelques utilisateurs et cours factices et simuler l’activité dans le compte d’évaluation, afin de tester la fonctionnalité de l’application.

## Déploiement d’applications {#applicationdeployment}

Nous recommandons à l’administrateur Learning Manager ou à un administrateur d’intégration du compte de production de prendre en charge la mise à disposition de l’application aux utilisateurs de leur organisation. Une fois que l’application a été testée et qu’elle est considérée comme prête pour la production, informez l’administrateur du compte de production. Idéalement, les administrateurs souhaitent générer un nouvel ID client et un secret client pour l’application dans le compte de production et effectuer les étapes nécessaires pour les incorporer dans l’application de manière sécurisée. La procédure réelle de déploiement des applications varie d’une entreprise à l’autre et l’administrateur Learning Manager de votre organisation doit demander l’assistance du service informatique de votre organisation pour effectuer le déploiement.

## Approbation d’application externe {#externalapplicationapproval}

Vous pouvez ajouter des applications externes en cliquant sur **Approuver** dans le coin supérieur droit de la fenêtre **Applications** page. Indiquez l’ID de l’application externe et cliquez sur **Enregistrer.**

![](assets/add-external-application.png)

*Ajout et approbation d’une application externe*

## Foire aux questions

+++Learning Manager propose-t-il une intégration pour le commerce électronique ?

Adobe Learning Manager n’a pas d’intégration pour le commerce électronique. Cependant, nous fournissons des API afin que vous puissiez créer votre propre système de gestion de l’apprentissage sans en-tête et mettre en œuvre des fonctionnalités de commerce électronique.
+++
