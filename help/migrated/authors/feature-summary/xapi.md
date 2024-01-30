---
jcr-language: en_us
title: xAPI dans Learning Manager
description: L’API Experience (xAPI) est une spécification logicielle d’apprentissage en ligne qui permet au contenu d’apprentissage et aux systèmes d’apprentissage de se parler d’une manière qui enregistre et suit tous les types d’expériences d’apprentissage.
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 50%

---



# xAPI dans Learning Manager

## Qu’est-ce que xAPI ? {#whatisxapi}

L’API Expérience (xAPI) est une spécification de logiciel d’apprentissage en ligne qui permet aux contenus d’apprentissage et aux systèmes d’apprentissage de communiquer de sorte à enregistrer et suivre tous les types d’expériences d’apprentissage. Les expériences d’apprentissage sont enregistrées dans une boutique d’enregistrements d’apprentissage (Learning Record Store, LRS). Les LRS peuvent exister dans les systèmes de gestion d’apprentissage (LMS) traditionnels ou seuls.

Pour plus d’informations sur xAPI, voir :  [https://github.com/adlnet/xAPI-Spec](https://github.com/adlnet/xAPI-Spec).

## Comment Learning Manager prend-il en charge xAPI ? {#howdoescaptivateprimesupportxapi}

Learning Manager dispose d’une boutique d’enregistrements d’apprentissage intégrée. Ce LRS a la pleine capacité d’accepter des instructions xAPI à partir de contenu hébergé dans Learning Manager. Il accepte même les instructions xAPI générées par des tiers. Ces instructions xAPI sont stockées dans Learning Manager et peuvent ensuite être exportées en dehors de Learning Manager pour être visualisées dans tout système d’entrepôt de données tiers.

## Quand utilisez-vous xAPI ? {#whendoyouusexapi}

De plus en plus, il est nécessaire de capturer les expériences d’apprentissage de l’utilisateur final qui s’étendent sur plusieurs systèmes.  Il est également nécessaire de suivre l’engagement exact de l’élève par rapport au contenu de la formation. Cela va au-delà des étapes Démarrer, En cours et Terminé (qui sont les seuls attributs capturés par SCORM).

## Utilisation de xAPI dans Learning Manager {#usingxapiinprime}

## Configuration de votre application {#setupyourapplication}

1. Connectez-vous en tant qu’administrateur d’intégration. Sélectionner **[!UICONTROL Applications]** > **[!UICONTROL S&#39;inscrire]**.

   ![](assets/appregistration.png)

1. Enregistrez une nouvelle application.

   ![](assets/appregistration.png)

1. Définissez l’étendue de l’application.

   * Si l’option **[!UICONTROL Accès en lecture et en écriture au rôle d’administrateur xAPI]** est activée, l’administrateur peut publier et obtenir des instructions et des documents xAPI.
   * Si l’option **[!UICONTROL Accès en lecture et en écriture au rôle d’élève xAPI]** est activée, l’administrateur peut publier et obtenir des instructions et des documents xAPI.

1. Enregistrez les modifications. Vous obtenez votre identifiant de développeur et votre secret.

**Points de fin** :

Cliquez sur le lien ci-dessous pour afficher le document xAPI swagger :

[https://learningmanagereu.adobe.com/docs/primeapi/xapi/](https://learningmanagereu.adobe.com/docs/primeapi/xapi/)

Remarque : la version xAPI prise en charge dans Learning Manager est 1.0.3.

## Authentification API {#apiauthentication}

Learning Manager xAPI utilise l’infrastructure OAuth 2.0 pour authentifier et autoriser vos applications clientes. Une fois l’application enregistrée, vous pouvez obtenir les paramètres clientId et clientSecret. L’option Obtenir l’URL est utilisée dans le navigateur, car elle authentifie les utilisateurs de Learning Manager à l’aide de leurs comptes préconfigurés tels que SSO et Adobe ID.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<admin:xapi or learner:xapi>&response_type=CODE.
```

## Suivi des instructions xAPI en tant qu’objet d’apprentissage Learning Manager {#trackingxapistatementsasprimelo}

En tant qu’auteur, vous pouvez maintenant choisir le module xAPI tout en créant des cours pour surveiller l’expérience utilisateur en dehors de Learning Manager. Par exemple, vous pouvez utiliser cette fonctionnalité pour évaluer les activités des utilisateurs sur une plate-forme tierce utilisée pour l’utilisation des cours.

1. Lors de la création d’un **[!UICONTROL Module d’activité]**, dans la **[!UICONTROL Type]**option, utilisez le menu contextuel pour sélectionner  **[!UICONTROL Module xAPI.]**

   ![](assets/xapimodulecreation.png)

1. Vous êtes invité à fournir un IRI. Si elle n’est pas fournie, Learning Manager en génère une automatiquement.

   L’IRI pour une activité est unique sur un compte. Cela signifie que deux modules dans Learning Manager ne peuvent pas avoir le même IRI. Un nouvel IRI est généré dans les cas suivants :

   * Lorsqu&#39;un cours avec module xAPI est partagé entre plusieurs comptes.
   * Lorsqu’une certification avec le module xAPI se répète



   Toute instruction xAPI avec l’IRI mentionné est suivie dans le module ci-dessus et est reflétée dans les rapports Learning Manager.

1. Pour copier l’IRI généré automatiquement, consultez la page du module Activité.
1. Publiez le module.

**Remarques :**

* Learning Manager ne prend actuellement en charge que mbox en tant qu’identifiant. Les autres identificateurs, notamment mboz_sha1, openid et account, ne sont pas pris en charge.

* Les paramètres stateId et profileId sont des UUID lorsqu’ils sont utilisés avec Learning Manager.
* La demande du PUT ne remplace pas le document pour les xAPI agents/profil, activité/profil et activité/état
* Les groupes non identifiés ne sont pas pris en charge dans Actor.
* Le paramètre « related_activities » n&#39;est pas pris en charge dans l&#39;instruction GET.
* Les paramètres « format=ids » et « format=canonical » ne sont pas pris en charge dans les instructions GET.
* L’annulation d’une instruction xAPI n’annule aucune action effectuée dans Learning Manager lors de la publication de l’instruction.

## Génération de rapports {#generatereports}

Les rapports xAPI peuvent être générés sous forme de rapports Excel. En tant qu’administrateur, ouvrez **[!UICONTROL Rapports]** > **[!UICONTROL Rapports Excel]** > **[!UICONTROL rapport d’activité xAPI]**.

Le rapport téléchargé récupère toutes les informations publiées par l’élève et l’administrateur pour n’importe quelle instruction.

Les mêmes rapports peuvent être générés/planifiés à l’aide des connecteurs FTP et Box pour toute intégration tierce. Procédez comme suit :

Connectez-vous en tant qu’administrateur d’intégration, ouvrez le connecteur FTP/Box, sélectionnez le rapport d’activité xAPI dans le volet gauche et choisissez de planifier/générer un rapport.

![](assets/xapischedule.png)

* Lorsque le score brut est envoyé seul dans l’instruction xAPI sans score maximal, le score du questionnaire ne s’affiche pas dans LT.

* Pour obtenir le score en pourcentage dans Learning Manager, les scores mis à l’échelle sont envoyés via xAPI.

## Exemple de rapport {#samplereport}

[Exemples de rapport xAPI.](assets/xapireport8842560559890766717csv.zip)
