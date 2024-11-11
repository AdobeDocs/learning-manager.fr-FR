---
jcr-language: en_us
title: Manuel du développeur d’applications
description: L’API Learning Manager V1 est désormais obsolète. Les API V1 cesseront de fonctionner à partir du 28 février 2021. Nous vous recommandons d’utiliser les API V2 pour interagir avec Learning Manager.
contentowner: jayakarr
exl-id: fa9313ac-67de-4467-9253-7eeabcf14204
source-git-commit: a27c1566678d697512a75d94804b8804b5dc9b2b
workflow-type: tm+mt
source-wordcount: '3377'
ht-degree: 63%

---

# Manuel du développeur d’applications

>[!NOTE]
>
>L’API Learning Manager V1 est désormais obsolète. Nous vous recommandons d’utiliser les API V2 pour interagir avec Learning Manager.


## Vue d’ensemble {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) est une solution de gestion d’apprentissage en libre-service dédiée aux élèves et hébergée sur le cloud. Les clients peuvent accéder aux ressources de Learning Manager par programmation à l’aide de l’API Captivate Prime pour les intégrer à d’autres applications d’entreprise. L’API peut également être utilisée par les partenaires Adobe pour renforcer la proposition de valeur de Learning Manager en étendant ses fonctionnalités ou en les intégrant à d’autres applications ou services.

### Scénario d’utilisation {#usagescenario}

En utilisant l’API Learning Manager, les développeurs peuvent créer des applications autonomes qui étendent la fonctionnalité Learning Manager ou intègrent Learning Manager à d’autres flux de travail d’applications d’entreprise. Vous pouvez développer une application Web, un client de bureau ou une application mobile en utilisant la technologie de votre choix. En tant que développeur, vous pouvez accéder aux données de votre application depuis Learning Manager. Le déploiement de l’application que vous développez est externe à la plate-forme Learning Manager et vous avez un contrôle total sur le cycle de vie du développement logiciel à mesure que l’application évolue. Les applications sont généralement développées par une organisation de client pour être utilisées avec leur compte Learning Manager, et ces applications sont « privées » pour cette organisation spécifique de client. En outre, les partenaires Adobe peuvent créer des applications génériques avec l’API Learning Manager, qui peut être utilisée par un grand nombre de clients Learning Manager.

## API Learning Manager {#apidescription}

L’API Learning Manager est basée sur des principes REST et expose les éléments clés du modèle d’objet Learning Manager aux développeurs d’applications via HTTP. Avant de connaître les détails des points de terminaison API et des méthodes HTTP, les développeurs peuvent se familiariser avec les différents objets Learning Manager, leurs attributs et leurs relations. Une fois les modèles bien compris, il est utile de bien cerner la structure des demandes et des réponses d’API et de bien comprendre quelques termes courants de programmation que nous utilisons de manière générique dans l’ensemble de l’API.

Pour plus de détails sur les différents points de terminaison et méthodes d&#39;API, consultez la [documentation de l&#39;API Learning Manager](https://learningmanager.adobe.com/docs/primeapi/v2/).

## API des élèves

Adobe Learning Manager : les API des élèves vous permettent de créer une expérience d’apprentissage personnalisée pour vos utilisateurs. L’utilisation de ces API nécessite un jeton utilisateur valide et doit être utilisée uniquement dans le cadre des workflows où il y a un élève entièrement licencié/inscrit.

>[!IMPORTANT]
>
>Ils ne doivent pas être utilisés tels quels pour tout type de récupération de données afin de prendre en charge des utilisateurs/utilisateurs partagés non connectés ou tout autre cas de ce type.

Les cas d’utilisation non enregistrés nécessitent une manipulation spéciale.

**Si vous avez des questions sur l&#39;utilisation appropriée de ces API, contactez l&#39;équipe d&#39;architecture de solution et assurez-vous qu&#39;un architecte de solution a validé une solution avant de la déployer**.

## Authentification API {#apiauthentication}

Lorsque vous écrivez une application qui effectue des appels d’API à Learning Manager, vous devez enregistrer votre application à l’aide de l’application d’administration d’intégration.

Les API Learning Manager utilisent l’infrastructure OAuth 2.0 pour authentifier et autoriser vos applications client.

**Procédure**

**1. Configurer votre application**

Vous pouvez configurer votre application avec l’ID client et le secret client pour utiliser les points de terminaison appropriés. Une fois l’application enregistrée, vous pouvez obtenir les paramètres clientId et clientSecret. Get URL doit être utilisé dans le navigateur, car il authentifie les utilisateurs de Learning Manager à l’aide de leurs comptes préconfigurés tels que SSO, Adobe ID, etc.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Une fois l’authentification réussie, votre navigateur se redirige vers l’URI de redirection de l’URL ci-dessus. Un **code** de paramètre est ajouté avec l’URI de redirection.

**2. Obtenir le jeton d’actualisation à partir du code**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Corps de la demande de publication :

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

**3.** **Obtenir un jeton d&#39;accès à partir du jeton d&#39;actualisation**

URL d’obtention du jeton d’accès :

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Content-Type: application/x-www-form-urlencoded

Corps de la demande de publication :

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

Certains termes fréquemment utilisés dans l’API Learning Manager sont expliqués ci-dessous pour référence.

**Inclut**

Les développeurs peuvent accéder à un seul modèle d’objet API et à plusieurs modèles associés à ce modèle. Pour accéder aux modèles connexes suivants, vous devez comprendre la relation de chaque modèle avec d’autres modèles. Le paramètre **Includes** permet aux développeurs d&#39;accéder aux modèles dépendants. Vous pouvez utiliser le séparateur de virgule pour accéder à plusieurs modèles. Pour obtenir un exemple d&#39;utilisation et plus de détails sur **l&#39;inclusion**, consultez la section Exemple de modèle d&#39;API dans cette page.

**Demande d’API**

Les demandes d’API peuvent être faites à l’aide d’une requête HTTP. Selon le point de terminaison et le développeur de méthodes, vous avez le choix entre divers verbes HTTP, tels que GET, PUT, POST, DELETE, PATCH, etc. Pour certaines requêtes, les paramètres de requête peuvent être transmis. Lors de la création d’une requête pour un modèle de données spécifique, l’utilisateur peut également demander des modèles associés, comme décrit dans les spécifications de l’API JSON. La structure d’une demande d’API typique est décrite dans [l’exemple d’utilisation du modèle](#main-pars_header_1415780624).

**Réponse de l’API**

Lorsqu’une demande d’API est faite par un client, un document SON est obtenu conformément à la spécification de l’API JSON. La réponse contient également le code d’état HTTP, que le développeur peut vérifier pour effectuer les étapes suivantes appropriées dans sa logique d’application. La structure d&#39;une réponse API typique est décrite dans [exemple d&#39;utilisation de modèle](#main-pars_header_1415780624).

**Erreurs**

Lorsqu’une demande d’API échoue, une réponse Erreur est obtenue. Le code d’état HTTP renvoyé dans la réponse indique la nature de l’erreur. Les codes d’erreur sont représentés avec des numéros pour chaque modèle dans la référence API. 200, 204, 400 et 404 sont quelques-unes des erreurs courantes représentées dans les API indiquant des problèmes d’accès HTTP.

**Champs**

Les attributs de l’objet API et ses relations sont appelés collectivement Champs. Reportez-vous à [l’API JSON pour plus d’informations.](http://jsonapi.org/format/#document-resource-object-fields) Vous pouvez utiliser Fields comme paramètre lors d&#39;appels API pour récupérer un ou plusieurs attributs spécifiques à partir du modèle. En l’absence du paramètre Champs, l’appel API extrait tous les attributs disponibles du modèle. Par exemple, dans l&#39;appel d&#39;API suivant, fields[skill]=name vous récupère l&#39;attribut name du modèle de compétence seul.

`https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&fields[skill]=name `

**Pagination**

Parfois, une requête API entraîne une longue liste d’objets à retourner dans la réponse. Dans de tels cas, l’attribut de pagination permet au développeur d’extraire les résultats séquentiellement en termes de pages multiples, chaque page contenant une série d’enregistrements. Par exemple, l’attribut de pagination dans Learning Manager vous permet de définir le nombre maximal d’enregistrements à afficher dans une page. En outre, vous pouvez définir la valeur de plage des enregistrements à afficher sur la page.

**Tri**

Le tri est autorisé dans les modèles d’API. En fonction du modèle, choisissez le type de tri à appliquer pour les résultats. Le tri peut être appliqué par ordre croissant ou décroissant. Par exemple, si vous spécifiez `code sort=name`, il s&#39;agit d&#39;un tri croissant par nom. Si vous spécifiez `code sort=-name`, il s&#39;agit d&#39;un tri décroissant par nom. Reportez-vous à la [spécification technique de l&#39;API JSON](http://jsonapi.org/format/#fetching-sorting) pour plus d&#39;informations.

## Illustration d’utilisation de l’API {#samplemodel}

Imaginons un scénario dans lequel un développeur souhaite obtenir le nom de la compétence, le nombre maximal de points attribués pour le niveau de compétence et les points obtenus par l’élève pour cette compétence.

Un modèle userSkill dans les API Learning Manager est constitué des attributs par défaut suivants : id, type, dateAchieved, dateCreated, pointsEarned. Ainsi, lorsqu’un développeur utilise la méthode GET pour acquérir des détails du modèle userSkill, les données actuelles relatives aux attributs par défaut sont affichées dans la sortie de réponse.

Mais, dans ce scénario, le développeur veut obtenir le nom de la compétence et les points de niveau de compétence pour l’utilisateur. L’API Learning Manager vous permet d’accéder à ces informations associées à l’aide de champs de relation et d’inclure des paramètres. Les modèles associés à userSkill sont obtenus dans la balise de relations. Vous pouvez obtenir les détails de chaque modèle associé en appelant ces modèles avec userSkill. Pour obtenir ces informations, utilisez le paramètre **`code include`** avec des valeurs séparées par des points (point) pour chacun des modèles associés. Vous pouvez utiliser une virgule comme séparateur pour demander un autre modèle comme l’utilisateur include=skillLevel.skill, course

**Appel API**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

Par exemple userId peut être 746783 et userSkills id 746783_4426_1.

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

## Modèles Learning Manager {#models}

L’API Learning Manager permet aux développeurs d’accéder aux objets Learning Manager en tant que ressources RESTful. Chaque point de terminaison de l’API représente une ressource. Il s’agit généralement d’une instance d’objet comme Badge ou un ensemble de ces objets. Les développeurs utilisent ensuite les verbes HTTP tels que PUT, GET, POST et DELETE pour effectuer des opérations CRUD sur ces objets (collections).

API +++V1

Le schéma suivant représente les différents éléments du modèle d’objet Learning Manager dans l’API V1.

![](assets/er-diag-primemodels.png)

Le tableau suivant décrit les différents éléments du modèle objet Learning Manager V1 :

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>Numéro de série</strong></p></td>
   <td>
    <p><strong>Objet Learning Manager</strong></p></td>
   <td>
    <p><strong>Description</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>l'interface</p></td>
   <td>
    <p>L’utilisateur est le modèle principal de Learning Manager. Les utilisateurs sont généralement les apprenants internes ou externes d’une organisation qui utilisent des objets d’apprentissage. Cependant, ils peuvent jouer d’autres rôles tels que celui de l’auteur et du responsable outre le rôle de l’élève. L’ID de l’utilisateur, le type, le courrier électronique sont quelques-uns des attributs en ligne. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>cours</p></td>
   <td>
    <p>Le cours est l’un des objets d’apprentissage pris en charge dans Learning Manager, qui composé d’un ou de plusieurs modules. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>module</p></td>
   <td>
    <p>Le module est un bloc de construction pour créer des objets d’apprentissage dans Learning Manager. Les modules présentent quatre types différents : la salle de classe, la salle de classe virtuelle, l’activité et l’auto-apprentissage. Utilisez ce modèle de module pour obtenir les détails de tous les modules d’un compte. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certification</p></td>
   <td>
    <p>La certification est accordée aux élèves en fonction de la réussite des cours. Des cours sont requis dans l’application avant d’utiliser les certifications. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>learning program</p></td>
   <td>
    <p>Les programmes d’apprentissage sont des cours conçus de manière unique qui répondent aux besoins d’apprentissage spécifiques des utilisateurs. Généralement, les programmes d’apprentissage sont utilisés pour atteindre des objectifs d’apprentissage couvrant des cours individuels. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>badge</p></td>
   <td>
    <p>Le badge constitue une preuve de réussite que les élèves obtiennent lorsqu’ils atteignent des étapes spécifiques à mesure qu’ils progressent dans un cours. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>skill</p></td>
   <td>
    <p>Le modèle de compétences se compose de niveaux et de crédits. Les compétences peuvent être acquises par les élèves après la fin du cours concerné. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnrollment</p></td>
   <td>
    <p>Ce modèle fournit des informations sur l’inscription d’un utilisateur à une certification.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnrollment</p></td>
   <td>
    <p>Ce modèle fournit des informations sur l’inscription d’un utilisateur à un cours. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Un cours peut comporter une ou plusieurs instances associées. Vous pouvez obtenir l’instance de cours </p></td>
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
    <p>Un programme d’apprentissage peut comporter plusieurs instances assimilant des propriétés similaires d’un programme d’apprentissage ou d’instances personnalisées. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>job aid</p></td>
   <td>
    <p>L’assistance à la tâche est un contenu d’apprentissage accessible aux élèves sans aucun critère d’inscription ou d’achèvement de cours. Vous pouvez récupérer la date, l’état, les informations d’identification mis à jour avec ses modèles connexes tels que la version de l’assistance à la tâche, les auteurs et le niveau de compétence. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>L’assistance à la tâche peut avoir une ou plusieurs versions associées en fonction des révisions de contenu et du nombre de téléchargements. Ce modèle fournit des détails sur une seule version d’assistance à la tâche. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>Le programme d’apprentissage comprend une ou plusieurs instances. Les élèves peuvent s’inscrire eux-mêmes à une instance de programme d’apprentissage ou être affectés par un administrateur. Ce modèle fournit des informations sur l’inscription d’un utilisateur à une instance de programme d’apprentissage. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Un module peut avoir une ou plusieurs versions basées sur ses téléchargements de contenu révisé. Utilisez ce modèle pour obtenir des informations spécifiques sur une version de module. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Un niveau de compétence comprend un ou plusieurs cours auxquels assister afin d’acquérir un niveau avec ses crédits associés. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge met en relation un badge avec un utilisateur. Il contient des informations telles que la date d’obtention, assertionUrl, etc. </p></td>
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

Voici les différents éléments du schéma de classe de modèle d’objet Learning Manager dans l’API V2.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Objet Learning Manager</b></th>
   <th><b>Description</b></th>
  </tr>
  <tr>
   <td>account</td>
   <td>Encapsule les détails d’un client Learning Manager.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>Le badge constitue une preuve de réussite que les élèves obtiennent lorsqu’ils atteignent des étapes spécifiques à mesure qu’ils progressent dans un cours. <br></td>
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
   <td>L’utilisateur est le modèle principal de Learning Manager. Les utilisateurs sont généralement les apprenants internes ou externes d’une organisation qui utilisent des objets d’apprentissage. Cependant, ils peuvent jouer d’autres rôles tels que celui de l’auteur et du responsable outre le rôle de l’élève. L’ID de l’utilisateur, le type, le courrier électronique sont quelques-uns des attributs en ligne. </td>
  </tr>
  <tr>
   <td>resource</td>
   <td>Cet élément est utilisé pour modéliser chaque ressource de contenu qu’un module cherche à encapsuler. Toutes les ressources encapsulées dans <code>
     an
    </code> <code>
     loResource
    </code> sont équivalentes en termes d'objectif d'apprentissage, mais elles diffèrent les unes des autres en termes de type de livraison ou de paramètres régionaux de contenu.<br></td>
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
    </code> à un seul utilisateur. Il contient des détails tels que quand il a été atteint, <code>
     assertionUrl
    </code> et ainsi de suite. <br></td>
  </tr>
  <tr>
   <td>skill</td>
   <td>Le modèle de compétences se compose de niveaux et de crédits. Les compétences peuvent être acquises par les élèves après la fin du cours concerné. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Un niveau de compétence comprend un ou plusieurs cours auxquels assister afin d’acquérir un niveau avec ses crédits associés. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Un objet d’apprentissage est une abstraction pour différents types d’objets auxquels les utilisateurs peuvent s’inscrire et desquels ils peuvent apprendre. Actuellement, Learning Manager dispose des quatre types d'objets d'apprentissage : Cours, Certification, Programme d'apprentissage <code>
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
    </code>. Un cours est composé de <code>
     of
    </code> modules supplémentaires. Dans Learning Manager, un module peut être fourni de diverses manières équivalentes. Par conséquent, le <code>
     loResource
    </code> encapsule essentiellement toutes ces ressources équivalentes.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Cet objet encapsule le résultat de l’utilisateur qui consomme une ressource spécifique dans le contexte d’un objet d’apprentissage auquel il est inscrit. Il contient des informations telles que la durée passée par <code>
     user
    </code> dans la ressource, le pourcentage de progression effectué par l'utilisateur, le statut Réussite/Échec et le score obtenu par l'utilisateur dans tout quiz associé.<br></td>
  </tr>
  <tr>
   <td>calendar<br></td>
   <td>Un objet Calendrier est une liste de <code>
     upcoming classroom
    </code> cours de classe virtuelle auxquels l'utilisateur peut s'inscrire.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>Le retour d’informations L1 encapsule les réponses fournies par un élève aux questions de retour d’informations associées à des objets d’apprentissage. En général, ces informations sont collectées une fois que l’utilisateur a terminé un objet d’apprentissage s’il est configuré pour collecter ces commentaires des élèves.<br></td>
  </tr>
  <tr>
   <td>enrollment<br></td>
   <td>Cette abstraction encapsule les détails relatifs à la transaction représentant l’affectation d’un utilisateur spécifique à une instance d’objet d’apprentissage spécifique.<br></td>
  </tr>
 </tbody>
</table>

+++

Liste des relations et des attributs d’objet.

+++account

**Attributs**
dateCreated\
gamificationEnabled\
l&#39;identifiant\
paramètres régionaux\
loginUrl\
logoUrl\
name\
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
name\
l&#39;état

+++

+++catalog

**Attributs**
dateCreated\
dateUpdated\
description\
l&#39;identifiant\
isDefault\
isInternallySearchable\
isListable\
name\
l&#39;état

+++

+++data

**Attributs**
id\
noms

+++

+++ludification

**Attributs**
couleur\
name\
 point(s)

+++

+++learningObject

**Attributs**
authorNames\
dateCreated\
datePublished\
dateUpdated\
effectivenessIndex\
enrollmentType\
l&#39;identifiant\
imageUrl\
isExternal\
isSubLoOrderEnforced\
loType\
l&#39;état\
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
l&#39;identifiant\
isDefault\
seatLimit\
l&#39;état\
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
l&#39;identifiant\
progressPercent\
score\
l&#39;état

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
l&#39;identifiant\
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
l&#39;identifiant\
progressPercent\
score

**Relations**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Attributs**
crédits\
l&#39;identifiant\
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
l&#39;identifiant\
instructorNames\
isDefault\
paramètres régionaux\
emplacement\
name\
onlyQuiz\
reportingInfo\
reportingType\
seatLimit

+++

+++skill

**Attributs**
description\
l&#39;identifiant\
name\
l&#39;état

**Relations**
levels(skillLevel)

+++

+++skillLevel

**Attributs**
id\
niveau\
maxCredits\
name\
**Relations**
badge(badge)\
skill(skill)

+++

+++user

**Attributs**
avatarUrl\
bio\
contentLocale\
courrier électronique\
champs\
l&#39;identifiant\
name\
pointsEarned\
profile\
Rôles\
l&#39;état\
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
l&#39;identifiant\
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
l&#39;identifiant\
mois\
trimestre

**Relations**
containerLO(learningObject)\
course(learningObject)

+++

+++userNotification

**Attributs**
actionUsed\
canal\
dateCreated\
l&#39;identifiant\
message\
modelIds\
modelNames\
modelTypes\
lire\
Rôle

+++

+++userSkill

**Attributs**
dateAchived\
dateCreated\
l&#39;identifiant\
pointsEarned

**Relations**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(user)

+++

## Processus de développement de l’application {#registration}

## Prérequis {#prerequisites}

En tant que développeur, vous devez créer un compte d’évaluation sur Learning Manager afin de bénéficier d’un accès complet à tous les rôles dans ce compte. Pour pouvoir créer une application, le développeur doit également créer certains utilisateurs et cours et obtenir un état satisfaisant pour le compte, de façon à ce que l’application en cours de développement puisse avoir accès à des données factices.

## Créer l’ID et le secret client {#createclientidandsecret}

1. Dans la connexion **Administrateur de l&#39;intégration**, cliquez sur **[!UICONTROL Applications]** dans le volet de gauche.

   ![](assets/application-development-menu.png)

   *Sélectionner des applications dans l&#39;administrateur d&#39;intégration*

1. Cliquez sur **[!UICONTROL S&#39;inscrire]** dans le coin supérieur droit de la page pour enregistrer les détails de votre application. La page d’inscription s’affiche.

   ![](assets/register-application.png)

   *Enregistrer l&#39;application*

   Il est obligatoire de renseigner tous les champs de cette page.

   **Nom de l’application** : saisissez le nom de votre application. Il n&#39;est pas obligatoire d&#39;utiliser le même nom d&#39;application, il peut s&#39;agir de n&#39;importe quel nom valide.

   **URL** : si vous connaissez l’URL exacte où l’application est hébergée, vous pouvez l’indiquer. Si vous ne disposez pas de cette URL, vous pouvez indiquer l’URL de votre entreprise. Un nom d’URL valide est obligatoire dans ce champ.

   **Rediriger les domaines** : saisissez le nom de domaine de l’application vers laquelle vous souhaitez que l’application Learning Manager redirige après l’authentification OAuth. Vous pouvez mentionner plusieurs URL ici, mais vous devez utiliser les URL valides telles que `http://google.com`, `http://yahoo.com`, etc.

   **Description :** entrez la brève description de votre application.

   **Étendues :** choisissez l&#39;une des quatre options disponibles pour définir l&#39;étendue de votre application. En fonction de votre choix indiqué ici, le point de terminaison de l’API Learning Manager est accessible pour votre application. Par exemple, si vous avez choisi **Accès en lecture au rôle de l’élève**, tous les points de terminaison de l’API de l’élève Learning Manager sont accessibles en lecture seule à votre application.

   **Pour ce compte uniquement ?**\
   **Oui** : si vous choisissez Oui, l&#39;application n&#39;est pas visible pour les autres administrateurs de compte.\
   **Non** : si vous choisissez Non, les autres administrateurs de compte peuvent également accéder à cette application, mais ils doivent utiliser l’id de l’application pour y accéder. L’ID d’application est généré et affiché en mode de modification d’application Learning Manager.

   Si vous choisissez l&#39;accès en lecture et en écriture **rôle administrateur** lors de l&#39;enregistrement de l&#39;application et l&#39;accès en lecture **rôle administrateur** lors de la création des API, vous pouvez toujours avoir un accès en écriture pour l&#39;application, car l&#39;étendue de l&#39;enregistrement de l&#39;application remplace le workflow d&#39;autorisation.

1. Cliquez sur **[!UICONTROL Enregistrer]** dans le coin supérieur droit après avoir rempli les détails dans la page d’inscription.

## Développement et test d’applications {#applicationdevelopmentandtesting}

L’API Learning Manager peut être utilisée par les développeurs pour créer n’importe quelle application. Les développeurs doivent s’assurer que leurs comptes disposent d’utilisateurs et de cours valides. Ils peuvent créer quelques utilisateurs et cours fictifs et simuler une activité dans le compte d’essai afin qu’ils puissent tester le fonctionnement de l’application.

## Déploiement de l’application {#applicationdeployment}

Nous recommandons à l’administrateur Learning Manager ou à un administrateur d’intégration du compte de production de prendre en charge la mise à disposition de l’application aux utilisateurs de leur organisation. Une fois que l’application a été testée et considérée comme prête pour la production, informez l’administrateur du compte de production. Dans l’idéal, les administrateurs veulent générer un nouveau client-id et un nouveau client-secret pour l’application dans le compte de production et effectuer les étapes nécessaires pour les intégrer de manière sécurisée. La procédure de déploiement des applications varie d’une entreprise à l’autre et l’administrateur Learning Manager de votre organisation doit collaborer avec le département informatique de votre organisation pour terminer le déploiement.

## Approbation des applications externes {#externalapplicationapproval}

Vous pouvez ajouter des applications externes en cliquant sur **Approuver** dans le coin supérieur droit de la page **Applications**. Indiquez l’ID de l’application externe et cliquez sur **Enregistrer.**

![](assets/add-external-application.png)

*Ajouter et approuver une application externe*

## Forum aux questions

+++Learning Manager propose-t-il une intégration pour le commerce électronique ?

Adobe Learning Manager n’offre pas d’intégration pour le commerce électronique. Cependant, nous fournissons des API afin que vous puissiez créer votre propre système de gestion de l’apprentissage (LMS) sans interface utilisateur et mettre en œuvre des fonctionnalités pour le commerce électronique.
+++
