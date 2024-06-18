---
jcr-language: en_us
title: Étiquetage blanc dans l’application mobile Adobe Learning Manager
description: L’étiquetage blanc est une pratique consistant à renommer une application ou un service avec votre propre marque et à le personnaliser comme si vous en étiez le créateur d’origine. Dans Adobe Learning Manager, vous pouvez appliquer un étiquetage blanc à l’application mobile, afin de pouvoir renommer l’application et la rendre disponible pour vos utilisateurs sous votre propre marque.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: 73d908674e6c32dafa4f9502634c42ec73fc3b6c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Étiquetage blanc dans l’application mobile Adobe Learning Manager

L’application mobile Adobe Learning Manager prend désormais en charge l’étiquetage blanc, ce qui signifie que vous pouvez désormais publier l’application sous votre propre marque.

## Comment commencer à vous préparer au lancement de votre application marquée d’un blanc

Pour déployer et gérer votre propre application avec étiquette blanche, procédez comme suit :

1. Préparez les ressources (comme l’image de l’écran de démarrage) et le texte afin que les deux puissent être utilisés dans l’application et la description sur l’App Store/Play Store.

1. Attribuer une ressource technique capable de :

* Génération des fichiers de certificat de notification push.
* Signature des binaires d’application fournis par l’équipe ALM.
* Chargement et gestion du processus de publication. Le processus de publication nécessite une communication entre votre gestionnaire d’applications et les équipes de l’app/play store pour que votre application soit conforme à toutes les directives de publication. À partir d’ALM, vous recevrez un binaire d’application entièrement conforme.

## Vue d’ensemble

L’étiquetage blanc est une pratique consistant à renommer une application ou un service avec votre propre marque et à le personnaliser comme si vous en étiez le créateur d’origine. Dans Adobe Learning Manager, vous pouvez appliquer un étiquetage blanc à l’application mobile, afin de pouvoir renommer l’application et la rendre disponible pour vos utilisateurs sous votre propre marque.

## Éléments personnalisables

Les éléments suivants peuvent être personnalisés :

### Champs

<table>

    <tbody>

    <tr>

   <td>

    <p>ID de compte</p></td>

   <td>

    <p>ID de votre compte. Notez que les élèves qui appartiennent à un autre compte n’auront pas accès à l’application avec étiquette blanche.</p></td>

  </tr>

  <tr>

   <td>

    <p>Id De Compte Supplémentaires</p></td>

   <td>

    <p>Ajoutez plusieurs comptes (sous-domaines) si vous le souhaitez. Ajoutez les sous-domaines en les séparant par des virgules, sans espaces. Par exemple, acc01,acc02,acc03, etc.<br> <b>Remarque :</b> Vous devez ajouter l’ID de compte lors de la spécification des sous-domaines.</br> </p></td>

  </tr>

  <tr>

  <td>

  <p>Nom de l’application</p></td>

  <td>

  <p>Nom à utiliser pour l’application.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nom court de l’application</p></td>

  <td>

  <p>Si le nom de l’application est long, donnez à l’application un nom court qui apparaît sur l’appareil.</p></td>

  </tr>

   <tr>

  <td>

  <p>Nom de l’application interne</p></td>

  <td>

  <p>Nom sous lequel le système d’exploitation identifie l’application. Le format généralement utilisé est : com.company-name.product-name.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nom de l’application interne - iOS</p></td>

  <td>

  <p>Donnez un autre nom à l’application si vos utilisateurs se trouvent sur iOS. Nous vous recommandons d’utiliser le même nom pour iOS et Android.</p></td>

  </tr>

  <tr>

  <td>

  <p>Icône d’application</p></td>

  <td>

  <p>L’icône de l’application est png. Cette icône s’affiche sur votre application. Le format à nommer est account-id_appIcon.png. Les dimensions de l’icône de l’application sont de 512 × 512 pixels.</p></td>

  </tr>

  <tr>

  <td>

  <p>Écran de démarrage de l’application</p></td>

  <td>

  <p>Dans l’écran de démarrage de votre application, indiquez une image (png) qui s’affiche lorsque vos utilisateurs lancent l’application. Le format à nommer est account-id_splashIcon.png. Les dimensions des écrans de démarrage à base carrée sont de 1 052 × 1 052 pixels et celles des écrans de démarrage à base circulaire sont de 768 x 768 pixels.</p></td>

  </tr>

  <tr>

  <td>

  <p>ID client et secret client</p></td>

  <td>

  <p>L’administrateur d’intégration de votre compte fournit les détails lors de l’enregistrement de l’application. L’administrateur de l’intégration doit utiliser les éléments suivants :<ul><li>learner:read, learner:write as role</li><li>application interne name://redirect comme URL de redirection</li></ul></p></td>

  </tr>

  <tr>

  <td>

  <p>Logo du compte</p></td>

  <td>

  <p>URL qui héberge le logo de votre organisation. Fournissez un lien vers le contenu comme logo du compte. L’URL doit être codée en Web.</p></td>

  </tr>

  <tr>

  <td>

  <p>ID App Store de l’application (iOS)</p></td>

  <td>

  <p>ID requis pour la mise à jour de force. L’application doit savoir que l’élève doit être redirigé vers l’App Store pour mettre à jour l’application.</p></td>

  </tr>

   <tr>

  <td>

  <p>Identifiant Google Play Store pour l’application (Android)</p></td>

  <td>

  <p>ID requis pour la mise à jour de force.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nom d’hôte pour la liaison approfondie</p></td>

  <td>

  <p>Pour héberger vos liens profonds, utilisez learningmanager. Si vous souhaitez utiliser une autre URL de nom d’hôte comme lien profond, indiquez l’URL de l’hôte. Par exemple, learningmanager.adobe.com.</p></td>

  </tr>

    </tbody>

</table>

>[!NOTE]
>
>Fournissez les données à vos CSAM afin qu’ils puissent les ajouter dans votre binaire d’application personnalisé.


#### Mettre à jour l&#39;association de site pour gérer les liens profonds personnalisés

Si vous utilisez un domaine personnalisé ou learningmanager\*.adobe.com en tant qu’hôte, vous n’avez rien à faire. Toutefois, si vous utilisez une solution personnalisée ou un nom d’hôte spécifique pour les URL, ajoutez les fichiers d’association de sites.

>[!CAUTION]
>
>Si les fichiers ne sont pas présents, les liens profonds ne fonctionneront pas. Vérifiez que les fichiers sont présents.


Reportez-vous aux liens suivants pour plus d’informations :

* [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Générer des notifications push

L’envoi de notifications push aux applications Android et iOS nécessite deux mécanismes différents.

* Pour iOS, générez les certificats de notification push.
* Pour Android, fournissez une clé de serveur générée à partir du projet Firebase.

Suivez les instructions ci-dessous pour configurer les projets dans Firebase :

### Notifications push sur iOS

Dans le développement d’applications iOS, un certificat de notification push est un identifiant cryptographique émis par Apple qui permet à un serveur d’envoyer de manière sécurisée des notifications push à un appareil iOS via le service de notification push d’Apple (APN).

Le certificat garantit une communication sécurisée entre votre serveur (ou fournisseur) et les APN Apple lors de l’envoi de notifications push aux appareils iOS.

Android et iOS utilisent Firebase Cloud Messaging (FCM) comme service d’envoi de notifications push aux appareils.

### Génération du certificat sur iOS

Procédez comme suit :

1. Générez ou téléchargez le fichier **Certificat de notification Push** et une clé privée (.p12). Pour plus d’informations, voir la section [Document de développeur Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Installez le fichier p12 après son téléchargement. Utiliser le mot de passe pour installer dans votre **Accès au trousseau**.

1. Accéder à **Mes certificats** et exportez le certificat. Veillez à sélectionner le type mime .cer.

1. Une fois le fichier p12 et le fichier cer disponibles, exécutez les commandes suivantes :

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Si vous pouvez vous connecter au serveur, le certificat que vous avez créé est valide. Dans le fichier myapnappkey.pem, copiez les valeurs du certificat et de la clé privée.

### Notifications Push sur Android

Configurez un projet dans Firebase et partagez la clé du serveur avec le CSAM.

Contactez l’équipe CSM et obtenez les fichiers ajoutés aux services SNS sur AWS. Les utilisateurs devront obtenir l’entrée enregistrée dans le service SNS pour la notification push, qui les obligera à partager les certificats générés ci-dessus pour validation.

>[!NOTE]
>
>Pour Android, l’utilisateur doit fournir la clé de serveur du projet Firebase qu’il crée pour Android afin d’ajouter l’entrée au service SNS.


## Créer un projet dans Firebase

### Android

Réutilisez le même projet que celui que vous avez créé dans les étapes ci-dessus pour les notifications push.

[Ajouter le projet](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) dans Firebase et récupérer ***google-services.json*** fichier.

### iOS

[Ajouter le projet](https://firebase.google.com/docs/ios/setup) pour Firebase et récupérer le fichier ***GoogleService-Info.plist*** fichier.

>[!IMPORTANT]
>
>Envoyez les fichiers à l’équipe Adobe Learning Manager CSAM pour les inclure dans la version de votre fichier binaire d’application.


## Génération des fichiers binaires signés

### iOS

```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```

>[!NOTE]
>
>Vous aurez besoin de XCode 15.2 ou version ultérieure pour créer les fichiers binaires signés.


## Android

```
sh""" ~/Library/Android/sdk/build-tools/30.0.3/apksigner sign --ks $storeFile --ks-pass "pass:$store\_password" --ks-key-alias $key\_alias --key-pass "pass:$key\_password" --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Vous aurez besoin des outils de construction du kit de développement logiciel Android pour créer les fichiers binaires signés.

**Prochaine étape**

Après avoir généré les fichiers binaires, insérez-les dans Play Store ou App Store.

## Comment appliquer les modifications

Envoie les ressources et les fichiers requis à l’équipe CSM. L’équipe CSM remplit ensuite le [formulaire](https://forms.office.com/r/bJRRaRBvSh) avec les modifications requises et joint les ressources requises. L&#39;équipe examinera ensuite les modifications et en informera les équipes d&#39;ingénieurs. L’équipe d’ingénieurs génère ensuite une build et la partage avec l’équipe CSM.

L’équipe CSM partage la version avec le client.

## Éléments non personnalisables

* Écran Mettre à jour le mot de passe
* Écran Création d’un compte
