---
jcr-language: en_us
title: Étiquetage blanc dans l’application mobile Adobe Learning Manager
description: L’étiquetage blanc est une pratique consistant à renommer une application ou un service avec votre propre marque et à le personnaliser comme si vous en étiez le créateur d’origine. Dans Adobe Learning Manager, vous pouvez appliquer un étiquetage blanc à l’application mobile, afin de pouvoir renommer l’application et la rendre disponible pour vos utilisateurs sous votre propre marque.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: 0c97b147a1e4c6e1a4a0cc69f56f8e9420c4602b
workflow-type: tm+mt
source-wordcount: '2098'
ht-degree: 0%

---

# Étiquetage blanc dans l’application mobile Adobe Learning Manager

L’application mobile Adobe Learning Manager prend désormais en charge l’étiquetage blanc, ce qui signifie que vous pouvez désormais publier l’application sous votre propre marque.

ALM mettra à disposition des fichiers binaires blancs mis à jour selon les calendriers suivants :

1. Pour les versions majeures de l’application mobile, les fichiers seront disponibles deux semaines à l’avance.
2. Pour toute mise à jour prévue pour des correctifs urgents, les fichiers seront disponibles une semaine à l’avance.
3. Pour les corrections non planifiées, urgentes et immédiates, les fichiers seront mis à disposition au mieux de leurs possibilités.

Les fichiers binaires seront disponibles dans les dossiers désignés du client. Contactez vos CSM pour accéder aux fichiers. Le client est responsable de la publication en temps opportun et des processus associés.

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

    <p>ID de compte</p>

   </td>

   <td>

    <p>ID de votre compte. Notez que les élèves qui appartiennent à un autre compte n’auront pas accès à l’application avec étiquette blanche.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Id De Compte Supplémentaires</p>

   </td>

   <td>

    <p>Ajoutez plusieurs comptes (sous-domaines) si vous le souhaitez. Ajoutez les sous-domaines en les séparant par des virgules, sans espaces. Par exemple, acc01,acc02,acc03, etc.<br> <b>Remarque :</b> vous devez ajouter l'ID de compte lors de la spécification des sous-domaines.</br> </p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nom de l’application</p></td>

   <td>

    <p>Nom à utiliser pour l’application.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nom court de l’application</p>

   </td>

   <td>

    <p>Si le nom de l’application est long, donnez à l’application un nom court qui apparaît sur l’appareil.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nom de l’application interne</p></td>

   <td>

    <p>Nom sous lequel le système d’exploitation identifie l’application. Le format généralement utilisé est : com.company-name.product-name.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nom de l’application interne - iOS</p>

   </td>

   <td>

    <p>Donnez un autre nom à l’application si vos utilisateurs se trouvent sur iOS. Nous vous recommandons d’utiliser le même nom pour iOS et Android.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Icône d’application</p>

   </td>

   <td>

    <p>L’icône de l’application est png. Cette icône s’affiche sur votre application. Le format à nommer est account-id_appIcon.png. Les dimensions de l’icône de l’application sont de 512 × 512 pixels.<div>Veuillez noter qu’Apple n’autorise pas le canal Alpha dans les icônes d’application. Assurez-vous donc de supprimer le canal Alpha de la ressource avant de la soumettre.</div></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Écran de démarrage de l’application</p></td>

   <td>

    <p>Dans l’écran de démarrage de votre application, indiquez une image (png) qui s’affiche lorsque vos utilisateurs lancent l’application. Le format à nommer est account-id_splashIcon.png. Les dimensions des écrans de démarrage à base carrée sont de 1 052 × 1 052 pixels et celles des écrans de démarrage à base circulaire sont de 768 x 768 pixels.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID client et secret client</p>

   </td>

   <td>

    <p>L’administrateur d’intégration de votre compte fournit les détails lors de l’enregistrement de l’application. L’administrateur de l’intégration doit utiliser les éléments suivants :<ul><li>learner:read, learner:write as role</li><li>application interne name://redirect comme URL de redirection</li></ul></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Logo du compte</p>

   </td>

   <td>

    <p>URL qui héberge le logo de votre organisation. Fournissez un lien vers le contenu comme logo du compte. L’URL doit être codée en Web.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID App Store de l’application (iOS)</p>

   </td>

   <td>

    <p>ID requis pour la mise à jour de force. L’application doit savoir que l’élève doit être redirigé vers l’App Store pour mettre à jour l’application.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Identifiant Google Play Store pour l’application (Android)</p>

   </td>

   <td>

    <p>ID requis pour la mise à jour de force.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nom d’hôte pour la liaison approfondie</p>

   </td>

   <td>

    <p>Pour héberger vos liens profonds, utilisez learningmanager. Si vous souhaitez utiliser une autre URL de nom d’hôte comme lien profond, indiquez l’URL de l’hôte. Par exemple, learningmanager.adobe.com.</p>

   </td>

  </tr>

 </tbody>

</table>

>[!NOTE]
>
>Fournissez les données à vos CSAM afin qu’ils puissent les ajouter dans votre binaire d’application personnalisé.


#### Mise à jour de l’association de sites pour gérer les liens profonds personnalisés

Si vous utilisez un domaine personnalisé ou learningmanager\*.adobe.com en tant qu’hôte, vous n’avez rien à faire. Toutefois, si vous utilisez une solution personnalisée ou un nom d’hôte spécifique pour les URL, ajoutez les fichiers d’association de sites.

>[!CAUTION]
>
>Si les fichiers ne sont pas présents, les liens profonds ne fonctionneront pas. Vérifiez que les fichiers sont présents.


Reportez-vous aux liens suivants pour plus d’informations :

* [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Obtention de l’ID de votre équipe pour App Store

Pour obtenir votre ID d’équipe :

1. Connectez-vous à votre compte **[!UICONTROL Développeur Apple]**.
2. Sélectionnez **[!UICONTROL Détails de l’abonnement]** en haut de la page et copiez votre ID d’équipe.

Cet ID est requis pour ajouter l’entrée d’application blanche dans les fichiers de métadonnées afin d’activer la liaison approfondie.

## Obtenir l’empreinte SHA-256 pour Android

L’empreinte SHA-256 du certificat de signature Android est requise lors de l’ajout de l’entrée d’application blanche.

Pour générer une empreinte SHA-256 :

1. Exécutez la commande suivante :

```
keytool -list -v -keystore <keystore/jks file> -alias <aliaskey> -storepass <storepassword> -keypass <keypassword>
```

Dans la sortie, recherchez les empreintes du certificat, puis copiez la valeur SHA-256. Partagez cette empreinte digitale selon vos besoins pour la configuration de la liaison approfondie.

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

1. Générez ou téléchargez le **certificat de notification Push** et la clé privée (.p12). Pour plus d&#39;informations, consultez le [document du développeur Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Installez le fichier p12 après son téléchargement. Utilisez le mot de passe pour installer dans votre **accès au trousseau**.

1. Accédez à **Mes certificats** et exportez le certificat. Veillez à sélectionner le type mime .cer.

1. Une fois le fichier p12 et le fichier cer disponibles, exécutez les commandes suivantes :

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Si vous pouvez vous connecter au serveur, le certificat que vous avez créé est valide. Dans le fichier myapnappkey.pem, copiez les valeurs du certificat et de la clé privée.

### Notifications Push sur Android

Pour Android, l’utilisateur doit fournir le fichier services.json à partir du projet Firebase pour ajouter l’entrée au service SNS.

Créez un projet dans Firebase et partagez le fichier services.json avec l’équipe CSM. Ce fichier est nécessaire pour l’entrée basée sur les jetons dans le SNS. Notez que la clé de serveur n’est plus utilisée. Voir [Créer un projet dans Firebase](#create-project-in-firebase).

Pour télécharger le fichier services.json, procédez comme suit :

1. Connectez-vous à la console **Firebase**.
1. Accédez aux **paramètres du projet** et sélectionnez **Cloud Messaging**.
1. Recherchez **l&#39;API Firebase Cloud Messaging** et sélectionnez **Gérer les comptes de service**.
1. Dans la page **Comptes de service**, sélectionnez **Comptes de service** dans le panneau de gauche.
1. Recherchez l&#39;entrée de votre projet et sélectionnez **Gérer les détails** sous Actions.

   >[!NOTE]
   >
   >   Le format d’entrée du projet sera &lt;-accountname->@appspot.gserviceaccount.com.

1. Accédez à l&#39;onglet **Touches** et sélectionnez **Ajouter une touche**.
1. S&#39;il n&#39;y a pas de clé, sélectionnez **Créer une clé** et sélectionnez **JSON** comme type de clé. Cette opération génère et télécharge le fichier JSON.
1. S&#39;il existe déjà une clé, sélectionnez **Télécharger la clé existante**, collez la clé, puis chargez-la. Cette opération génère et télécharge le fichier JSON.

<!-- Set up a project in Firebase and share the server key with the CSAM.-->

Contactez l’équipe CSM et partagez le fichier JSON pour ajouter l’entrée aux services SNS sur AWS. Les utilisateurs devront obtenir l’entrée enregistrée dans le service SNS pour la notification push, qui les obligera à partager les certificats générés ci-dessus pour validation.

## Créer un projet dans Firebase {#create-project-in-firebase}

### Android

Réutilisez le même projet que celui que vous avez créé dans les étapes ci-dessus pour les notifications push.

[Ajouter le projet](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) dans Firebase et récupérer le fichier ***google-services.json***.

### iOS

[Ajouter le projet](https://firebase.google.com/docs/ios/setup) à Firebase et récupérer le fichier ***GoogleService-Info.plist***.

>[!IMPORTANT]
>
>Envoyez les fichiers à l’équipe Adobe Learning Manager CSAM pour les inclure dans la version de votre fichier binaire d’application.


## Génération des fichiers binaires signés

### iOS

<!--```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```-->

Le dossier `<root>` contient le fichier **Runner.xcarchive.zip**. Exécutez les commandes ci-dessous pour générer le binaire signé :

1. Exécutez la commande suivante pour décompresser l&#39;archive :

   ```
   unzip Runner.xcarchive.zip
   ```

2. Accédez au répertoire de l’application :

   ```
   cd Runner.xcarchive/Products/Applications/Runner.app
   ```

3. Copiez le fichier d’approvisionnement mobile :

   ```
   cp <path>/<mobile-provisioningfile>.mobileprovision embedded.mobileprovision
   ```

4. Exécutez la commande suivante pour mettre à jour vos informations de signature dans la bibliothèque d’infrastructure :

   ```
   codesign -f -s "Distribution Certificate Name" Frameworks/*
   ```

5. Revenez au dossier `<root>` (où se trouve Runner.xcarchive.zip) :

   ```
   cd <root>
   ```

6. Exportez l’archive à l’aide de xcodebuild :

   ```
   xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath ipa_path/ -exportOptionsPlist <path>/<ExportOptions-file>.plist
   ```

7. Recherchez le fichier .ipa dans le dossier ipa_path.
8. Chargez le fichier .ipa sur le site Web `Diawi`.
9. Une fois le téléchargement terminé, sélectionnez le bouton **[!UICONTROL Envoyer]**.
10. Une fois l’opération terminée, vous recevrez un code QR et un lien.
11. Ouvrez le code QR ou le lien directement dans Safari.

Si le périphérique est inclus dans le profil d’approvisionnement, l’installation doit se poursuivre sur le périphérique.

>[!NOTE]
>
>Vous aurez besoin de XCode 15.2 ou version ultérieure pour créer les fichiers binaires signés.


### Android

**Pour le fichier apk**

>[!IMPORTANT]
>
>Avant d&#39;exécuter la commande `apksigner`, exécutez les commandes suivantes pour exporter votre mot de passe Key Store et votre mot de passe Key Alias en tant que variables d&#39;environnement :
>
>```
>export KS_PASS=your_keystore_password
>export KEY_PASS=your_key_password
>```

```
sh""" <path>/apksigner sign --ks $storeFile. --ks-pass env:KS_PASS --ks-key-alias $key_alias --key-pass env:KEY_PASS --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Le chemin d&#39;accès à l&#39;outil `apksigner` ressemble généralement à ceci : ~/Library/Android/sdk/build-tools/30.0.3/apksigner.

**Pour le fichier aab**

>[!NOTE]
>
>Vous aurez besoin des outils de construction du kit de développement logiciel Android pour créer les fichiers binaires signés.

Le Play Store nécessite des binaires Android au format aab pour la publication. Par conséquent, nous fournirons le fichier .aab non signé.

>[!NOTE]
>
>Lors de la création d’un fichier KeyStore, vous devez générer un mot de passe KeyStore, un alias de clé de signature et un mot de passe d’alias de clé de signature.

Procédez comme suit pour signer le fichier .aab :

Exécutez la commande suivante :

```
<path>/jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore <keystore-file> app-release.aab <signingKeyAlias>
```

>[!NOTE]
>
>**[!UICONTROL jarsigner]** est inclus dans Java. Assurez-vous d’utiliser Java 21.

À l’invite, entrez les mots de passe suivants :

* Mot de passe KeyStore
* mot de passe pour l’alias de clé de signature

Vous pouvez utiliser l’application fournie. Cependant, si vous devez générer une apk à partir d’un fichier aab, veuillez suivre ces étapes :

>[!NOTE]
>
>Vous devrez installer **[!UICONTROL bundletool]** pour générer des API.


Exécutez la commande suivante pour créer le fichier apk :

```
java -jar <path>/bundletool-all.jar  build-apks --bundle=app-release.aab --output=my_app.apks --mode=universal
```

Pour décompresser le fichier, exécutez la commande suivante :

```
unzip my_app.apks -d output_dir
```

Vous obtiendrez le fichier apk à partir du dossier **[!UICONTROL output_dir]**.

**Prochaine étape**

Après avoir généré les fichiers binaires, insérez-les dans Play Store ou App Store.

### Transfert des applications vers la boutique pour révision

Après avoir reçu les binaires finaux, vous pouvez les charger sur les boutiques d’applications respectives (iOS ou Android) pour révision. Procédez comme suit pour charger les fichiers binaires dans les boutiques d’applications.

**iOS**

1. Connectez-vous à l’application Transporter avec vos identifiants App Store.
2. Sélectionnez le bouton **+** en haut à gauche et chargez le certificat de production (fichier .ipa).
3. Si le fichier .ipa est correct, vous serez invité à télécharger l’application vers App Store.
4. Une fois l’application distribuée, connectez-vous au portail App Store. Dans quelques heures, le binaire apparaîtra dans la section TestFlight. Vous pouvez l’activer pour le test d’intégrité final dans TestFlight avant la révision de l’application et utiliser cet IPA comme binaire lors de la soumission de l’application pour une nouvelle version.

**Android**

1. Ouvrez la console Google Play Store.
2. Accédez au **[!UICONTROL Tableau de bord]** > **[!UICONTROL Afficher les versions de l&#39;application]** > **[!UICONTROL Tableau de bord des versions]**, puis sélectionnez **[!UICONTROL Créer une nouvelle version]**.
3. Chargez le fichier .aab généré en tant qu’offre groupée d’applications et saisissez les détails de la version, tels que le numéro de version et les nouvelles informations.
4. Enregistrez vos modifications et soumettez l’application pour révision.
5. Assurez-vous de définir la distribution de l’application sur 100 % (Google la définit sur 20 % par défaut).

#### Liens utiles pour la publication d’applications

**Android**

[Créez et configurez votre application](https://support.google.com/googleplay/android-developer/answer/9859152?hl=en)
[Préparez votre application pour la révision](https://support.google.com/googleplay/android-developer/answer/9859455?sjid=2454409340679630327-AP)

**iOS**

[Envoyer pour révision](https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-for-review)

## Comment appliquer les modifications

Envoie les ressources et les fichiers requis à l’équipe CSM. L&#39;équipe CSM remplit ensuite le [formulaire](https://forms.office.com/r/bJRRaRBvSh) avec les modifications requises et joint les ressources requises. L&#39;équipe examinera ensuite les modifications et en informera les équipes d&#39;ingénieurs. L’équipe d’ingénieurs génère ensuite une build et la partage avec l’équipe CSM.

L’équipe CSM partage la version avec le client.

## Éléments non personnalisables

* Écran Mettre à jour le mot de passe
* Écran Création d’un compte
