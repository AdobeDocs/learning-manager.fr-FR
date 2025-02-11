---
jcr-language: en_us
title: Documentation sur les API d’interaction avec le lecteur intégré
description: Découvrez les différentes API permettant d’écouter des événements et de déclencher des actions dans le lecteur intégré
contentowner: chandrum
exl-id: 4734ecc1-cc8a-40b0-8997-32a31ec661ec
source-git-commit: 3d183dc40e4d1962d25160b74d8cf6cfa26e3171
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 69%

---

# Documentation sur les API d’interaction avec le lecteur intégré

Adobe Learning Manager fournit une bibliothèque pouvant être intégrée dans une application. Cette bibliothèque fournit diverses API permettant d’écouter des événements et de déclencher des actions dans le lecteur intégré.

Avec les API fournies, vous pouvez lire et mettre en pause la lecture, ainsi qu’effectuer des actions supplémentaires sur le lecteur.

## Chargement de la bibliothèque

La bibliothèque est disponible à cet [emplacement](https://cpcontents.adobe.com/public/publiccdn/playerInteractionLib.min.js).

Pour charger la bibliothèque, procédez comme suit :

1. Chargez le fichier js dans l’application client.
2. Lors du chargement de la bibliothèque, window.cpPlayerLib sera renseigné.

>[!NOTE]
>
>Si vous n&#39;utilisez pas prod US, définissez les paramètres cpPlayerLib.env et cpPlayerLib.sourceOrigin en fonction de votre env.

Les valeurs par défaut sont :

* window.cpPlayerLib.env = [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player);
* window.cpPlayerLib.sourceOrigin = &quot;[https://cpcontents.adobe.com](https://cpcontents.adobe.com/)&quot;;

### Méthodes disponibles

La bibliothèque cpPlayerLib comporte les fonctions suivantes :

**startPlayer**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>startPlayer</td>
</tr>
<tr>
<td>Description</td>
<td>Charge un lecteur dans l’application.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>loId : ID de l’objet d’apprentissage.</li><li>accountId : ID de compte du compte ALM.</li><li>userId : ID utilisateur.</li><li>accessToken : jeton d’accès.</li><li>domRefId : ID du conteneur div dans lequel afficher le lecteur.</li><li>onModuleLoaded : cette fonction est appelée lorsque les modules avec les détails ci-dessous sont chargés.</li><br><li>contentType</li><li>loId</li><li>moduleId</li><li>completed</li><li>currentLanguage</li><li>availableLanguages</li><li>isCCAvailable</li><li>ccEnabled</li></br></td>
</tr>
<tr>
<td>Retours</td>
<td>Renvoie une promesse. Une fois la promesse résolue, un playerObj sera passé.</td>
</tr>
<tr>
<td>Exception</td>
<td>La promesse entraînera une exception.</td>
</tr>
<tr>
<td>Exemple de code</td>
<td>cpPlayerLib.startPlayer(loId, accountId, userId, accessToken, domRefId, onModuleLoaded).then((playerObj) =&gt; {//playerObj dispose des api pour interagir avec le lecteur}) &gt;</td>
</tr>
</tbody>
</table>

**getAllPlayers**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>getAllPlayers</td>
</tr>
<tr>
<td>Description</td>
<td>Renvoie tous les objets Player de la page active.</td>
</tr>
<tr>
<td>Paramètres</td>
<td>Aucune</td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>cpPlayerLib.getAllPlayers()</td>
</tr>
</tbody>
</table>

**getPlayer**


<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>getPlayer</td>
</tr>
<tr>
<td>Description</td>
<td>Renvoie un objet Player avec l'ID d'objet d'apprentissage spécifié.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>loId : ID de l’objet d’apprentissage.</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>cpPlayerLib.getPlayer(loId)</td>
</tr>
</tbody>
</table>

**navigateToModule**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>navigateToModule</td>
</tr>
<tr>
<td>Description</td>
<td>Accéder au module suivant.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>moduleId : ID du module.</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.navigateToModule(moduleID)</td>
</tr>
</tbody>
</table>

**suivant**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>suivant</td>
</tr>
<tr>
<td>Description</td>
<td>Accéder au module suivant.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.next()</td>
</tr>
</tbody>
</table>

**précédent**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>previous</td>
</tr>
<tr>
<td>Description</td>
<td>Accéder au module précédent.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.previous()</td>
</tr>
</tbody>
</table>

**toggleTOC**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>toggleTOC</td>
</tr>
<tr>
<td>Description</td>
<td>Activer/désactiver le panneau Table des matières sur le lecteur.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.toggleTOC()</td>
</tr>
</tbody>
</table>

**toggleNotes**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>toggleNotes</td>
</tr>
<tr>
<td>Description</td>
<td>Activer/désactiver le panneau Notes sur le lecteur.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.toggleNotes()</td>
</tr>
</tbody>
</table>

**toggleClosedCaption**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>toggleClosedCaption</td>
</tr>
<tr>
<td>Description</td>
<td>Activez/désactivez l’affichage des sous-titres sur le lecteur.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.toggleClosedCaption()</td>
</tr>
</tbody>
</table>

**changeLanguage**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>changeLanguage</td>
</tr>
<tr>
<td>Description</td>
<td>Modifiez la langue du contenu sur le lecteur.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>language : code de langue à spécifier.</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.changeLanguage("es")</td>
</tr>
</tbody>
</table>

**closePlayer**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>closePlayer</td>
</tr>
<tr>
<td>Description</td>
<td>Fermez le lecteur et supprimez-le de la page. </td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.closePlayer()</td>
</tr>
</tbody>
</table>

**togglePlayPause**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>togglePlayPause</td>
</tr>
<tr>
<td>Description</td>
<td>Basculez entre la lecture et la suspension du contenu sur le lecteur.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.togglePlayPause()</td>
</tr>
</tbody>
</table>

**setVolume**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>setVolume</td>
</tr>
<tr>
<td>Description</td>
<td>Régler le volume du lecteur. La valeur doit être comprise entre 0 et 1.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>volume : valeur du volume. La plage valide est 0-1. </li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.setVolume(0.5)</td>
</tr>
</tbody>
</table>

**setPlayBackSpeed**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>setPlayBackSpeed</td>
</tr>
<tr>
<td>Description</td>
<td>Définissez la vitesse de lecture dans le lecteur.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>speed : valeur de la vitesse à spécifier. Les valeurs valides sont .25, .5, .75, 1, 1.25, 1.5, 1.75, 2.</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.setPlayBackSpeed(1.25)</td>
</tr>
</tbody>
</table>

**recherche**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>rechercher</td>
</tr>
<tr>
<td>Description</td>
<td>Accès à n’importe quel moment de la vidéo.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>time : heure de sauter. L’heure est spécifiée en secondes.</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.seek(50)</td>
</tr>
</tbody>
</table>

**en avant**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>avance</td>
</tr>
<tr>
<td>Description</td>
<td>Avance de 10 secondes dans la vidéo.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.forward()</td>
</tr>
</tbody>
</table>

**en arrière**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>backward</td>
</tr>
<tr>
<td>Description</td>
<td>Retour de 10 secondes dans la vidéo.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.backward()</td>
</tr>
</tbody>
</table>

**navigateToPage**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>navigateToPage</td>
</tr>
<tr>
<td>Description</td>
<td>Accès à la page spécifiée sur le PPT/PDF.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>pageNumber : numéro de la page cible.</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.navigateToPage (5)</td>
</tr>
</tbody>
</table>

**nextPage**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>nextPage</td>
</tr>
<tr>
<td>Description</td>
<td>Accès à la page suivante sur le PPT/PDF.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.nextPage()</td>
</tr>
</tbody>
</table>

**previousPage**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>previousPage</td>
</tr>
<tr>
<td>Description</td>
<td>Retour à la page précédente sur le PPT/PDF.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.previousPage()</td>
</tr>
</tbody>
</table>

**zoomIn**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>zoomIn</td>
</tr>
<tr>
<td>Description</td>
<td>Effectuer un zoom avant du contenu d’un PPT/PDF.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.zoomIn()</td>
</tr>
</tbody>
</table>

**zoom arrière**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>zoomOut</td>
</tr>
<tr>
<td>Description</td>
<td>Effectuer un zoom arrière du contenu d’un PPT/PDF.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.zoomOut()</td>
</tr>
</tbody>
</table>

**downloadJobAid**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>downloadJobAid</td>
</tr>
<tr>
<td>Description</td>
<td>Téléchargement d’une assistance à la tâche à partir d’un cours</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.downloadJobAid()</td>
</tr>
</tbody>
</table>

**toggleJobAidPullout**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>toggleJobAidPullout</td>
</tr>
<tr>
<td>Description</td>
<td>Si vous souhaitez télécharger une assistance à la tâche.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.toggleJobAidPullout()</td>
</tr>
</tbody>
</table>

**plein écran**

<table>
<tbody>
<tr>
<td>Nom de la méthode</td>
<td>fullScreen</td>
</tr>
<tr>
<td>Description</td>
<td>Définissez le lecteur en mode plein écran.</td>
</tr>
<tr>
<td>Paramètres</td>
<td><li>Aucune</li></td>
</tr>
</tr>
<tr>
<td>Exemple de code</td>
<td>playerObj.fullScreen()</td>
</tr>
</tbody>
</table>

## Liste des événements

**onPlayerEvents(callBack)**

Lors de l’enregistrement, la fonction de rappel est appelée sur tous les événements du lecteur. Voici les noms des événements :

* PLAY (vidéo / audio / CP)
* PAUSE (vidéo / audio / CP)
* TIMEUPDATE (vidéo / audio / CP)
* PAGECHANGE (PPT / PDF)
* NOTEADDED (tout le contenu)
* LAUNCHED (tout le contenu)
* STARTED (tout le contenu)
* COMPLETED (tout le contenu)
* PASSED (tout le contenu)
* FAILED (tout le contenu)

**onStreamingEvents(callBack)**

Lors de l’enregistrement, la fonction de rappel est appelée sur toutes les instructions du lecteur envoyées pour effectuer le suivi de l’activité de l’utilisateur.
