---
jcr-language: en_us
title: Intégration d’Okta Active Directory à Adobe Learning Manager
description: Intégration d’Okta Active Directory à Adobe Learning Manager
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---



# Intégration d’Okta Active Directory à Adobe Learning Manager {#okta-active-directory-integration-with-adobe-learning-manager}

Dans ce document, vous apprendrez à intégrer Adobe Learning Manager à Okta Active Directory (AD). Lorsque vous intégrez Adobe Learning Manager à Okta AD, vous pouvez :

* Vérifier et contrôler l’accès de l’utilisateur Learning Manager dans Okta AD.
* Permettre aux utilisateurs d’être automatiquement connectés à Adobe Learning Manager avec leurs comptes Okta AD.
* Gérez vos comptes dans un emplacement central : le portail Okta.

Adobe Learning Manager prend en charge l’authentification unique initiée par le fournisseur d’identité (IdP) et le fournisseur de services (SP).

## Création d’une application dans OKTA

1. Connectez-vous en tant qu’administrateur sur Okta AD.
1. Cliquez sur **[!UICONTROL Applications]**. La boutique d’applications s’ouvre alors dans Okta.

   ![](assets/cp-application-store.png)

   *Afficher la boutique d’applications dans Okta*

1. Cliquez sur **[!UICONTROL Créer une intégration d’application]**.

   ![](assets/cp-app-integrations.png)

   *Sélectionnez Créer une intégration d’application*

1. Sélectionner **[!UICONTROL SAML 2.0]** à partir de la fenêtre nouvelle intégration d’application.

   ![](assets/cp-saml2.0.png)

   *Sélectionner l’option SAML2.0*

1. Sélectionner **[!UICONTROL Création d’une intégration SAML]** > **[!UICONTROL Page Paramètres généraux]**. Saisissez un nom d’application.

   Notez qu’il peut s’agir de n’importe quel nom pour identifier votre application de manière unique. Une fois terminé, cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/cp-saml-integration.png)

   *Saisissez le nom de l’application*

1. Effectuez les étapes suivantes sur la page Configurer les paramètres SAML :

   **Pour la configuration du FI :**

   1. Dans le champ URL d’authentification unique, saisissez l’URL : [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Dans le champ URL de l’audience, saisissez l’URL : [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. Dans le panneau **Format d’ID de nom** liste déroulante, sélectionnez **Adresse e-mail**.
   1. Dans le panneau **Nom d’utilisateur de l’application** dans la liste déroulante, sélectionnez Nom d’utilisateur Okta.
   1. Si vous souhaitez transmettre des attributs supplémentaires, vous pouvez ajouter les attributs sous la rubrique **Attributes, instruction** (Facultatif)

   ![](assets/cp-saml-integration-step1.png)

   *Ajout d’attributs SAML*

   **Pour la configuration SP :**

   1. Dans le champ URL d’authentification unique, saisissez l’URL : [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Dans le champ URL de l’audience, saisissez l’URL : [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. Dans la liste déroulante Format d’ID de nom, sélectionnez **Adresse e-mail**.
   1. Dans la liste déroulante Application, sélectionnez Nom d’utilisateur Okta.
   1. Cliquez sur **Afficher les paramètres avancés**.
   1. Sous **Algorithme de signature**, sélectionnez RSA-SHA256
   1. Dans le panneau **Algorithme d&#39;assertion**, sélectionnez SHA256
   1. Dans le panneau **Chiffrement d&#39;assertion** dropbox, sélectionner **Chiffré**.

   1. Dans le panneau **Certificat de chiffrement** , téléchargez le fichier de certificat partagé par Adobe.
   1. Si vous souhaitez transmettre des attributs supplémentaires, vous pouvez ajouter les attributs sous la rubrique **Attributes, instruction** (Facultatif)

   ![](assets/cp-saml-integration-step2.png)

   *Ajout d’attributs supplémentaires*

   Une fois terminé, cliquez sur **[!UICONTROL Suivant]**.

1. Le **Commentaires**  est facultatif. Une fois que vous avez sélectionné les options et donné votre avis, cliquez sur **[!UICONTROL Terminer]**.

   ![](assets/cp-saml-integration-step3.png)

   *Terminer la configuration SAML*

## Extraction de l’URL et du fichier de métadonnées initiés par l’IDP

Pour afficher l’URL et le fichier de métadonnées initiés par l’IdP/SP, effectuez les étapes ci-dessous :

1. Ouvrez l’application que vous avez créée.
1. Sous le **Authentification unique** onglet, cliquez sur **[!UICONTROL Afficher les instructions]**.

   ![](assets/cp-prime-sso.png)

   *Sélectionnez l’onglet SSO.*

   **Pour les FI :**

   1. L’URL d’authentification unique du fournisseur d’identité est l’URL initiée par l’IdP.
   1. Copiez tout le texte présent sous **Facultatif** champ.
   1. Ouvrez un nouveau document du bloc-notes et collez le texte copié.
   1. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Enregistrer sous]** > « filename.xml ». Il s’agira du fichier de métadonnées.

   **Pour SP :**

   1. L’URL d’authentification unique du fournisseur d’identité est l’URL initiée par l’IdP.
   1. L’émetteur du fournisseur d’identité est l’ID d’entité.
   1. Copiez tout le texte présent sous **Facultatif** champ.
   1. Ouvrez un nouveau document du bloc-notes et collez le texte copié.
   1. Cliquez sur **[!UICONTROL Fichier]** > **[!UICONTROL Enregistrer sous]** > **[!UICONTROL filename.xml]**. Il s’agira du fichier de métadonnées.

   ![](assets/cp-saml-integration-step4.png)

   *Enregistrer le fichier XML SP*

   Vous devez enregistrer ce fichier au format XML.

## Configuration de l’authentification unique Adobe Learning Manager

Pour configurer l’authentification unique Learning Manager Adobe, effectuez les étapes mentionnées dans l’article ci-dessous.

<!--

article not in TOC

[SSO Authentication](/help/migrated/kb/sso-authentication-for-learning-manager.md)
-->