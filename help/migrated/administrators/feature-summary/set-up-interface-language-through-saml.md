---
description: Découvrez comment configurer la langue de l’interface avec SAML
jcr-language: en_us
title: Configuration de la langue de l’interface via SAML
contentowner: chandrum
exl-id: 726cb45e-1c37-42b1-924a-565c84c82852
source-git-commit: 7b84a4565ccf109ed4789f4963d6e250f5d0a852
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Configuration de la langue de l’interface via SAML

Adobe Learning Manager (ALM) accepte désormais un attribut SAML pour la langue. Cet attribut est ensuite associé aux paramètres de l’interface utilisateur et de la langue du contenu, ce qui garantit une interaction fluide avec le système de gestion de l’apprentissage dans la langue préférée. La configuration de ces paramètres linguistiques est gérée via la plateforme de gestion des identités et des accès (IAM), à l’aide de SAML pour l’authentification unique (SSO). Cela prend en charge les connexions initiées par le fournisseur de services (SP) et le fournisseur d’identité (IdP), ce qui permet aux utilisateurs de voir l’interface et le contenu dans la langue de leur choix. Le workflow est le suivant :

1. Créer une application dans Okta
2. Ajouter un utilisateur dans Okta
3. Configuration de l’authentification unique dans ALM

## Créer une application dans Okta

Pour créer une application dans Okta, procédez comme suit :

1. Créez un compte développeur dans Okta à l’aide de l’adresse e-mail de votre entreprise et connectez-vous à votre compte.
2. Sélectionnez **[!UICONTROL Applications]** > **[!UICONTROL Créer Une Intégration D&#39;Application]**.
3. Sélectionnez **[!UICONTROL SAML 2.0]**, puis **[!UICONTROL Suivant]**.
4. Saisissez le nom de l’application, puis sélectionnez Suivant.
5. Configurez les champs suivants :

   * **[!UICONTROL URL d&#39;authentification unique]** : saisissez l&#39;URL de domaine spécifique à laquelle vous souhaitez lier l&#39;application (par exemple, [https://learningmanagerstage.adobe.com/saml/SSO](https://learningmanagerstage.adobe.com/saml/SSO)). Modifiez l’URL de l’environnement si nécessaire.
   * **[!UICONTROL URI d’audience (ID d’entité SP)]** : utilisez la même URL d’environnement que ci-dessus.
   * **[!UICONTROL Format d&#39;ID de nom]** : sélectionnez l&#39;adresse électronique.
   * **[!UICONTROL Nom d&#39;utilisateur de l&#39;application]** : sélectionnez le nom d&#39;utilisateur Okta.

6. Sous Instructions d’attribut, ajoutez les champs suivants (ou des champs supplémentaires si nécessaire) :
   * **Nom** : paramètres régionaux
   * **Format De Nom** : Non Défini
   * **Valeur** : user.locale

7. Sélectionnez Suivant, puis Terminer.
8. Une fois terminé, faites défiler la page jusqu’à Certificats de signature SAML :

   * Recherchez la ligne dont l&#39;état est **[!UICONTROL Actif]**.
   * Sélectionnez **[!UICONTROL Actions]** > **[!UICONTROL Afficher les métadonnées du fournisseur d’identité]**.
   * Un fichier XML s’ouvre alors dans un nouvel onglet. Copiez le code XML et enregistrez-le localement en tant que fichier .xml.

## Ajouter un utilisateur dans Okta

Pour créer un utilisateur dans Okta, procédez comme suit :

1. Sélectionnez **[!UICONTROL Répertoire]** > **[!UICONTROL Personnes]**, puis **[!UICONTROL Ajouter une personne]**.
2. Saisissez les informations nécessaires pour l&#39;utilisateur et sélectionnez **[!UICONTROL Enregistrer]**.
3. Recherchez et sélectionnez le nom d’utilisateur du nouvel utilisateur.
4. Sélectionnez **[!UICONTROL Attribuer l&#39;application]**.
5. Sélectionnez l&#39;application que vous avez créée précédemment, puis sélectionnez **[!UICONTROL Enregistrer]**.
6. Accédez au profil de l&#39;utilisateur et sélectionnez **[!UICONTROL Modifier]**.
7. Dans le champ Paramètres régionaux, saisissez la valeur requise (par exemple, fr_FR, en_US) et sélectionnez **[!UICONTROL Enregistrer]**.

## Configuration de l’authentification unique dans ALM

Pour configurer l’authentification unique dans ALM, procédez comme suit :

1. Connectez-vous en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Méthodes de connexion]**.
3. Accédez à l&#39;onglet **[!UICONTROL Configuration de l&#39;authentification unique (SSO)]**.
4. Sélectionnez **[!UICONTROL Ajouter une nouvelle configuration SSO]**.

   ![](assets/sso-add.PNG)
   _Ajouter l&#39;authentification unique dans ALM_

5. Configurez les détails suivants et sélectionnez Enregistrer.
   * Saisissez un nom pour la configuration.
   * Sélectionnez **[!UICONTROL Initié par le FI]** dans la liste déroulante **[!UICONTROL Paramètres d’authentification unique (SSO)]**.
   * Pour **[!UICONTROL l&#39;URL d&#39;authentification initiée par l&#39;IDP]** :

      * Ouvrez le fichier XML de métadonnées que vous avez téléchargé précédemment.
      * Recherchez la valeur d’emplacement et copiez-la.
      * Collez cette valeur dans le champ URL d’authentification initiée par le FI.

   * Pour le **[!UICONTROL fichier XML de métadonnées]** : chargez le fichier .xml que vous avez téléchargé précédemment.

6. Revenez à l&#39;onglet **[!UICONTROL Configuration]**.
7. Dans la liste déroulante, sélectionnez **[!UICONTROL Configuration de l’authentification unique]**.
8. Dans la liste déroulante **[!UICONTROL Configuration SSO]**, sélectionnez le nom de configuration que vous avez créé précédemment.
9. Sélectionnez **[!UICONTROL Enregistrer]**.

## Connexion utilisateur et paramètre de langue

Lorsqu’un utilisateur se connecte à l’aide des informations d’identification via l’authentification unique, l’attribut de langue transmis par l’IDP est mappé à l’interface utilisateur et aux champs de langue du contenu dans ALM. Les paramètres de langue sont immédiatement reflétés dans l’interface utilisateur et le contenu sans aucun temps de mise en cache.

Les utilisateurs peuvent mettre à jour manuellement leurs paramètres de langue dans la section du profil utilisateur. Ces préférences de langue mises à jour manuellement resteront en vigueur et ne seront pas remplacées par les paramètres du FI lors des prochaines connexions.

Si un utilisateur est supprimé de manière logicielle d’ALM, les paramètres de langue sont conservés dans la base de données. Lorsque le même utilisateur est ajouté à nouveau, la langue précédemment définie est restaurée.

Les administrateurs peuvent vérifier les rapports Activité des utilisateurs, Résumé de l’apprentissage et Tableau de bord de conformité pour obtenir des détails spécifiques à la langue.

## Mise à jour des préférences de langue de l’utilisateur lors de la connexion via SAML

Adobe Learning Manager est une plate-forme multilingue qui prend en charge les préférences linguistiques des élèves de plusieurs manières, par le biais de l’interface, du contenu et des modules de cours, tous disponibles dans plusieurs langues.

Grâce à cette amélioration, Adobe Learning Manager améliore le provisionnement des utilisateurs Just-In-Time pour les utilisateurs de la plate-forme native. Lorsque de nouveaux utilisateurs créent des comptes et se connectent pour la première fois, leurs préférences linguistiques sont capturées avec précision et appliquées automatiquement.

### Principaux avantages

* Met automatiquement à jour les préférences linguistiques des utilisateurs lors de la connexion.
* Offre une expérience personnalisée en affichant l’interface et le contenu dans la langue préférée de l’utilisateur.
* S’intègre parfaitement au processus d’authentification SAML.

Lorsque les utilisateurs se connectent via SAML, leur préférence de langue (langue de l’interface et du contenu) est vérifiée et mise à jour en fonction des informations fournies pendant le processus de connexion.

La fonctionnalité s’intègre au processus de connexion SAML pour capturer et mettre à jour la préférence de langue de l’utilisateur en toute transparence.
