---
jcr-language: en_us
title: Intégration d’Okta Active Directory à Adobe Learning Manager
description: Intégration d’Okta Active Directory à Adobe Learning Manager
contentowner: nluke
exl-id: 6d7711a9-7a7f-49b7-8948-9a42407463b3
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 57%

---

# Intégration d’Okta Active Directory à Adobe Learning Manager {#okta-active-directory-integration-with-adobe-learning-manager}

Dans ce document, vous apprendrez à intégrer Adobe Learning Manager à Okta Active Directory (AD). Lorsque vous intégrez Adobe Learning Manager à Okta AD, vous pouvez :

* Vérifier et contrôler l’accès de l’utilisateur Learning Manager dans Okta AD.
* Permettre aux utilisateurs d’être automatiquement connectés à Adobe Learning Manager avec leurs comptes Okta AD.
* Gérer vos comptes dans un emplacement central : le portail Okta.

Adobe Learning Manager prend en charge l’authentification unique initiée par le fournisseur d’identité (IdP) et le fournisseur de services (SP).

## Création d’une application dans OKTA

1. Connectez-vous en tant qu’administrateur sur Okta AD.
1. Cliquez sur **[!UICONTROL Applications]**. La boutique d’applications s’ouvre alors dans Okta.

   ![](assets/cp-application-store.png)

   *Afficher le magasin d&#39;applications dans Okta*

1. Cliquez sur **[!UICONTROL Créer une intégration d&#39;application]**.

   ![](assets/cp-app-integrations.png)

   *Sélectionnez Créer Une Intégration D&#39;Application*

1. Sélectionnez **[!UICONTROL SAML 2.0]** dans la nouvelle fenêtre d’intégration de l’application.

   ![](assets/cp-saml2.0.png)

   *Sélectionner l&#39;option SAML2.0*

1. Sélectionnez **[!UICONTROL Créer une intégration SAML]** > **[!UICONTROL Page des paramètres généraux]**. Saisissez un nom d’application.

   Notez qu’il peut s’agir de n’importe quel nom pour identifier votre application de manière unique. Une fois terminé, cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/cp-saml-integration.png)

   *Entrez le nom de l&#39;application*

1. Effectuez les étapes suivantes sur la page Configurer les paramètres SAML :

   **Pour la configuration du FI :**

   1. Dans le champ URL d&#39;authentification unique, saisissez l&#39;URL : [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Dans le champ URL du public, saisissez l’URL : [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. Dans la liste déroulante **Format d&#39;ID de nom**, sélectionnez **Adresse électronique**.
   1. Dans la liste déroulante **Nom d&#39;utilisateur de l&#39;application**, sélectionnez Nom d&#39;utilisateur Okta.
   1. Si vous souhaitez transmettre des attributs supplémentaires, vous pouvez ajouter les attributs sous l&#39;**Instruction Attributes** (Facultatif)

   ![](assets/cp-saml-integration-step1.png)

   *Ajouter des attributs SAML*

   **Configuration SP :**

   1. Dans le champ URL d&#39;authentification unique, saisissez l&#39;URL : [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Dans le champ URL du public, saisissez l’URL : [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. Dans la liste déroulante Format d’ID de nom, sélectionnez **Adresse électronique**.
   1. Dans la liste déroulante Application, sélectionnez Nom d’utilisateur Okta.
   1. Cliquez sur **Afficher les paramètres avancés**.
   1. Sous **Algorithme de signature**, sélectionnez RSA-SHA256
   1. Dans l&#39;**algorithme d&#39;assertion**, sélectionnez SHA256.
   1. Dans la boîte de dialogue **Chiffrement d&#39;assertion**, sélectionnez **Chiffrement chiffré**.

   1. Dans l&#39;option **Certificat de chiffrement**, chargez le fichier de certificat partagé par Adobe.
   1. Si vous souhaitez transmettre des attributs supplémentaires, vous pouvez les ajouter sous l&#39;**Instruction Attributs** (Facultatif).

   ![](assets/cp-saml-integration-step2.png)

   *Ajouter des attributs supplémentaires*

   Une fois terminé, cliquez sur **[!UICONTROL Suivant]**.

1. L&#39;onglet **Commentaires** est facultatif. Une fois que vous avez sélectionné les options et donné votre avis, cliquez sur **[!UICONTROL Terminer]**.

   ![](assets/cp-saml-integration-step3.png)

   *Terminer la configuration SAML*

## Extraction du fichier d’URL et de métadonnées initié par l’IDP

Pour afficher l’URL et le fichier de métadonnées initiés par l’IdP/SP, effectuez les étapes ci-dessous :

1. Ouvrez l’application que vous avez créée.
1. Sous l&#39;onglet **Authentification unique**, cliquez sur **[!UICONTROL Afficher les instructions]**.

   ![](assets/cp-prime-sso.png)

   *Sélectionnez l’onglet SSO*

   **Pour le FI :**

   1. L’URL d’authentification unique du fournisseur d’identité est l’URL initiée par l’IdP.
   1. Copiez tout le texte présent sous le champ **Facultatif**.
   1. Ouvrez un nouveau document du bloc-notes et collez le texte copié.
   1. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Enregistrer sous]** > « filename.xml ». Il s’agit du fichier de métadonnées.

   **Pour SP :**

   1. L’URL d’authentification unique du fournisseur d’identité est l’URL initiée par l’IdP.
   1. L&#39;émetteur du fournisseur d&#39;identité est l&#39;ID d&#39;entité.
   1. Copiez tout le texte présent sous le champ **Facultatif**.
   1. Ouvrez un nouveau document du bloc-notes et collez le texte copié.
   1. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Enregistrer sous]** > **[!UICONTROL filename.xml]**. Il s’agit du fichier de métadonnées.

   ![](assets/cp-saml-integration-step4.png)

   *Enregistrer le fichier XML SP*

   Vous devez enregistrer ce fichier au format XML.

## Configuration de l’authentification unique Adobe Learning Manager

Pour configurer l’authentification unique Adobe Learning Manager, effectuez les étapes mentionnées dans l’article ci-dessous.

<!--

article not in TOC

[SSO Authentication](/help/migrated/kb/sso-authentication-for-learning-manager.md)
-->
