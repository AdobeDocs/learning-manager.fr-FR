---
jcr-language: en_us
title: Limites de débit d’API dans Learning Manager
contentowner: saghosh
preview: true
source-git-commit: 544c695a77c21dd9162b9b943b6119d27aa373dc
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 51%

---



# Limites de débit d’API dans Learning Manager

## Introduction à la limitation de débit {#introductiontoratelimiting}

Adobe Learning Manager propose une suite complète d’API REST qui aide les clients à créer des applications qui s’intègrent à Learning Manager, voire des expériences utilisateur personnalisées et des extensions aux workflows qui aident leur entreprise.

Chaque fois qu’une API est appelée, des ressources de calcul partagées sont utilisées dans les serveurs Learning Manager. Nous devons donc faire preuve de prudence afin de nous assurer que les applications fonctionnent correctement et ne compromettent pas les caractéristiques de performances et de disponibilité de la plateforme. Pour ce faire, des limites sont introduites sur la façon dont les clients API effectuent les appels (fréquence et vélocité).

Par exemple, une application peut essayer d’obtenir tous les utilisateurs de ce compte et effectuer plusieurs appels API paginés à un taux rapide. Et par erreur, un développeur pourrait appeler cela dans une boucle serrée, ce qui entraînerait une énorme charge sur le serveur et rendrait les applications lentes et mettrait même en danger la plate-forme en consommant plus de ressources que ce qui est prévu ou nécessaire.

Pour résoudre ce problème, nous introduisons des limites de débit sur le nombre d’appels API pouvant être effectués par un seul utilisateur dans une application cliente spécifique d’un compte spécifique. Nous mesurons cela en termes de Demandes par minute, abrégées en RPM. Par exemple, lorsque nous disons que la limite pour les appels API GET est de 600 tr/min, cela signifie simplement qu&#39;un utilisateur unique ne peut pas dépasser un maximum de 600 appels en une minute, et si l&#39;utilisateur dépasse cette limite, l&#39;utilisateur sera limité au taux. Les demandes sont suivies à la milliseconde de granularité, cette limite correspond donc à 1 demande toutes les 100 millisecondes (ms). Il existe un autre paramètre, appelé Rafale, qui est également défini avec la limite de débit et qui définit le nombre de demandes qu’un utilisateur peut effectuer au-delà du débit spécifié (dans notre cas, 600RPM). Par exemple, si le paramètre Burst est 10 ; cela signifie que jusqu&#39;à 10 slots seront alloués dans une file d&#39;attente et lorsqu&#39;une demande arrive « trop tôt » (dans notre cas, avant 100ms), elle est traitée immédiatement s&#39;il y a un slot disponible pour elle dans la file d&#39;attente. Le créneau est alors marqué comme « pris » et n&#39;est pas libéré pour être utilisé par une autre requête jusqu&#39;à ce que le temps approprié soit écoulé (dans notre cas, après 100ms). Le trafic dans le monde réel est généralement avec des rafales, et c&#39;est là que le paramètre Burst aide. Pour la plateforme Learning Manager, nous définissons les limites d’une version d’API spécifique (par exemple, V2), d’un rôle (élève/administrateur) et d’un verbe (GET/PUT/POST/DELETE/PATCH). Dans l&#39;exemple décrit ci-dessus, nous dirions que la limite de taux est (600, 10).

Bien que nous ayons toujours eu des limites de taux pour l’API publique dans Learning Manager, nous avons été assez libéraux en permettant un RPM très élevé jusqu’à présent. Cependant, avec la croissance de votre plateforme d’apprentissage préférée, nous avons constaté une croissance rapide de l’utilisation de notre API, et nous avons décidé de faire en sorte que ces limites de taux soient explicitement documentées au profit de tous nos clients et pour une meilleure gestion de la plateforme. Dans ce contexte, nous avons mis à niveau notre API pour commencer à renvoyer une nouvelle réponse API (Code d’état HTTP 429), que vous n’avez pas encore vue. Cette réponse est fournie aux clients API lorsque la limite de taux est dépassée. Les applications clientes devront désormais traiter ce code de réponse comme correspondant à la logique de leur application ; et ce document vise principalement à aider les développeurs avec les informations dont ils ont besoin pour incorporer la bonne logique dans leur code lorsqu’ils voient une telle réponse.

## Comment confirmer les limites de taux appliquées ? {#howtoconfirmtheenforcedratelimits}

Pour chaque demande, les en-têtes de réponse contiennent les informations suivantes :

```
x-rate-limit: 600r/m 
x-burst: 10
```

* x-rate-limit indique le seuil du taux de requête de base en termes de requêtes par minute.
* x-burst spécifie combien de demandes dépassant le taux de demande de base sont acceptées pour être traitées immédiatement.

## Comment détecter les erreurs causées par les limites de taux ? {#howtocatcherrorscausedbyratelimits}

Pour chaque demande, vous pouvez vérifier si vous avez dépassé la limite de taux. Si vous obtenez un code de réponse de 429, « {« message »:« 429 Demandes trop nombreuses »} », vous avez atteint la limite de taux.

Il est recommandé d’inclure dans votre script du code qui intercepte 429 réponses. Si votre script ignore l’erreur « Trop de demandes » et continue à essayer d’effectuer des demandes, vous pouvez commencer à obtenir des erreurs nulles. À ce stade, les informations d’erreur ne seront plus utiles pour diagnostiquer le problème.

Par exemple, une requête de boucle qui se heurte à la limite de débit peut renvoyer la réponse suivante :

```
< HTTP/2 429 
< date: Wed, 04 Nov 2020 06:53:04 GMT 
< content-type: application/json; charset=utf-8 
< server: openresty 
< x-rate-limit: 60r/m 
< x-burst: 10 
< retry-after: 10.752 
< access-control-allow-credentials: true 
< access-control-allow-methods: GET, POST, OPTIONS, PUT, HEAD, DELETE, PATCH 
< access-control-allow-headers: X-acap-all-roles, X-acap-account,X-acap-user,X-acap-caller-role,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type, x-experience-api-version, Authorization, X-CSRF-TOKEN, X-HTTP-Method-Override 
< strict-transport-security: max-age=31536000; includeSubDomains 
< x-frame-options: SAMEORIGIN 
< x-xss-protection: 1 
< x-content-type-options: nosniff 
< x-request-id: gwBBFC9741-58A5-43B1-B1FE-7D14275961E7 
< strict-transport-security: max-age=31536000; includeSubDomains
```

La réponse contient des informations sur les touches suivantes :

```
status: 429 
retry-after: 10.752
```

Le code d’état 429 signifie « trop de demandes » et que la demande actuelle n’est pas traitée. L’en-tête retry-after indique que vous pouvez relancer l’appel API dans 10,752 secondes. Votre code doit arrêter de faire des demandes d’API supplémentaires jusqu’à ce qu’un délai suffisant se soit écoulé pour réessayer.

Le pseudo-code suivant présente un moyen simple d’intercepter les erreurs de limite de débit :

```
response = request.get(url) 
if response.status equals 429: 
    alert('Rate limited. Waiting to retry…') 
    wait(response.retry-after) 
    retry(url)
```

En fait, nous avons même créé une API factice Learning Manager pour que vous puissiez vous entraîner et vous familiariser avec la gestion du code d’état 429.

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: oauth < 
<token>
  >' 'https://learningmanager.adobe.com/learningmanagerapi/v2/dummy 
</token>
```

Cette API factice a une limite de :

```
x-rate-limit: 5r/m 
x-burst: 2
```

La limite de l’API factice est intentionnellement basse, de sorte que vous vous heurtez très rapidement aux limites de débit et pouvez ensuite vous concentrer davantage sur le développement du code pour intercepter et gérer les erreurs de limite de débit.

## Test de l’API factice {#testingthedummyapi}

Nous avons fourni un point de terminaison pour vous permettre de vérifier comment fonctionne la limitation de débit. Pour cela, nous avons créé un point de terminaison spécial appelé GET /dummy qui a une portée de lecture de l&#39;élève. Cette API a été délibérément configurée pour une limite de débit très stricte de 5 demandes par minute, avec une limite de rafale = 2.

Vous pouvez facilement le tester en atteignant ce point d’entrée avec des vitesses inférieures à 5 tr/min et supérieures à 5 tr/min. Écrivez le code pour gérer le code d’état HTTPS 429 et en fonction des informations dans les en-têtes de réponse.

Pour vous faciliter la tâche, consultez cet exemple de code JavaScript qui illustre ce point. Cliquez ici [jouer du violon](https://jsfiddle.net/ACAPJS/9yv8zcmL/) et voir le code en action.

Cette application nécessite que vous fournissiez un jeton d’application de rôle d’élève pour votre compte. Reportez-vous au [Manuel du développeur d’applications](https://captivateLearning Manager.adobe.com/docs/Learning Managerapi/v2/) pour plus d’informations sur les jetons d’API. Vous pouvez utiliser l’assistant de jeton dans la section Ressources pour les développeurs de l’application d’administration de l’intégration Learning Manager pour générer les jetons.

Cette application effectue 10 appels à l’API factice en une boucle, en une seule fois. Étant donné que la limite de taux est de (5, 2) pour l’API factice, elle sera dépassée une fois que les 5+2 premiers appels reçus par Learning Manager auront réussi et que vous verrez une réponse positive à ces appels.

Cependant, notez comment cette application recherche le code d&#39;état 429 en réponse et les traite. Lorsque cette application reçoit une telle réponse, elle imprime les détails dans la réponse de l’API, attend le temps suggéré et tente à nouveau les tentatives ayant échoué.

## Bonnes pratiques pour gérer la limitation de débit {#bestpracticestohandleratelimiting}

Bien souvent, les données d’un compte ne changent pas aussi souvent. Par exemple, les cours d’un compte peuvent ne pas changer aussi souvent. Au lieu d’essayer d’obtenir toutes les données à chaque fois, essayez d’obtenir les données spécifiques lorsque vous en avez besoin et envisagez d’utiliser un mécanisme de cache. De cette façon, lorsque votre application aura vraiment besoin de faire de nombreux appels, vous aurez un quota suffisant dans les limites de votre tarif pour faire ces appels importants.

Certaines données peuvent changer plus souvent et vous devrez peut-être les obtenir plus souvent. Même si c&#39;est le cas, demandez-vous si votre application peut se permettre d&#39;avoir des données légèrement obsolètes (quelque chose qui peut se trouver dans votre cache, que vous avez récupéré il y a N minutes), car elles peuvent n&#39;avoir aucune incidence sur le workflow de l&#39;utilisateur. Même si vous devez obtenir des données récentes à partir des serveurs, vous pouvez à nouveau être judicieux en récupérant uniquement les données spécifiques dont vous avez besoin, au lieu de tout obtenir.

Il y aura également des moments où vous n&#39;aurez pas le choix d&#39;obtenir beaucoup de données parce que l&#39;API peut ne pas être assez flexible pour vous donner exactement ce que vous voulez avec un seul appel. Vérifiez si l’API vous fournit des filtres et des critères de tri qui peuvent être utilisés pour réduire le nombre d’appels. Vous devez également envisager la mise en cache, car de nombreux utilisateurs de votre compte peuvent avoir besoin des mêmes données.

Lorsque vous obtenez trop de données dans le contexte d’une application interactive avec une interface graphique, il est probable que l’application tente d’en faire trop et puisse submerger l’utilisateur avec beaucoup d’informations/de fonctionnalités ayant un impact sur l’expérience utilisateur de votre application.

Lorsque vous créez une application non interactive (par exemple un travail quotidien), vous devrez peut-être récupérer beaucoup de données en bloc. Dans ce cas, envisagez d’utiliser l’API de tâche, principalement conçue pour renvoyer des données en bloc au format CSV. Notez que l’API de tâche aura une contrainte de quota que vous pourrez invoquer N fois par jour.

Étant donné que Learning Manager a implémenté les spécifications JSONAPI, il existe une API dans laquelle vous pouvez également charger des données de version test. Cela vous aidera à éviter de faire des appels API supplémentaires, mais vous devrez en contrepartie obtenir les données trop tôt. Comme les données chargées de version test peuvent parfois être très volumineuses, dans les appels paginés par API, vous définissez une taille de page maximale de 10 ; mais pour les appels API sans inclusion, vous pouvez spécifier une taille de page plus grande (jusqu’à 100)

En fin de compte, si vous effectuez beaucoup de demandes d’API en peu de temps, vous atteindrez la limite de taux d’API pour les demandes. Lorsque vous atteindrez cette limite, Learning Manager cessera de traiter toutes les demandes jusqu’à ce qu’un certain temps se soit écoulé.

Les limites de taux sont décrites dans la dernière section de cet article. Il est recommandé de se familiariser avec les limites.

## Limites de débit pour les points d’entrée de l’API V2 {#ratelimitsforv2apiendpoints}

Le tableau suivant indique les limites des différents points de terminaison V2. À l&#39;heure actuelle, les limites de taux ne sont pas imposées aux clients, mais ces limites seront appliquées à partir du JJ/MM/AAAA. Par conséquent, il est important que les clients examinent le code de leurs applications existantes pour voir comment ils peuvent ajuster leur code afin de connaître ces limites de taux et gérer les réponses API avec le code d’état HTTP 429.

<table> 
 <tbody>
  <tr> 
   <td><p><b>Opération</b></p></td> 
   <td><p><b>API d’administration</b></p></td> 
   <td><p><b>API de l’élève</b></p></td> 
  </tr> 
  <tr> 
   <td><p>DELETE</p></td> 
   <td><p>(25, 10) <br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PATCH</p></td> 
   <td><p>(60, 20)</p></td> 
   <td><p>(15, 5) <br></p></td> 
  </tr> 
  <tr> 
   <td><p>POST</p></td> 
   <td><p>(30, 10)<br></p></td> 
   <td><p>(30, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PUT</p></td> 
   <td><p>(20, 10)<br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>GET</p></td> 
   <td><p>(100, 100)<br></p></td> 
   <td><p>(100, 30)<br></p></td> 
  </tr> 
 </tbody>
</table>

