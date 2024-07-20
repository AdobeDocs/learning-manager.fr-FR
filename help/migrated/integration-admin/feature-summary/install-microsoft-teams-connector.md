---
description: Installer le connecteur Microsoft Teams dans Adobe Learning Manager
jcr-language: en_us
title: Installer le connecteur Microsoft Teams dans Adobe Learning Manager
contentowner: saghosh
exl-id: 68092187-ac69-4727-a3dc-f3047a1e164d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 24%

---

# Installer le connecteur Microsoft Teams dans Adobe Learning Manager

## Vue d’ensemble

Microsoft® Teams® est une plate-forme de collaboration basée sur le chat permanent qui prend en charge le partage de documents, les réunions en ligne, et d’autres fonctionnalités pour la communication en entreprise.

Adobe Learning Manager utilise un connecteur de salle de classe virtuelle qui peut être utilisé pour intégrer les réunions de Microsofts Teams à Learning Manager.

Le connecteur Microsoft Teams connecte les systèmes Learning Manager et Microsoft Teams pour permettre la synchronisation automatique de la réunion virtuelle. La liste suivante décrit les fonctionnalités du connecteur Microsoft Teams :

**Configuration de sessions virtuelles à l&#39;aide de Microsofts Teams**

Ce connecteur vous aide à intégrer votre compte Adobe Learning Manager avec votre compte Microsoft Teams. Après intégration, le connecteur permet à un auteur dans Learning Manager d’utiliser Microsoft Teams comme fournisseur de services technologiques pour les modules de salle de classe virtuelle dans Learning Manager.

**Autoriser les Microsofts Teams à authentifier les élèves lorsqu&#39;elles entrent dans une salle de classe virtuelle**

Ce connecteur permet de configurer l’organisateur de réunion Microsofts Teams à partir de Learning Manager lors de la création d’une réunion. L’organisateur de la réunion peut gérer l’entrée pour restreindre ou autoriser l’entrée à une réunion, ainsi que contrôler d’autres options de réunion fournies par Microsoft Teams.

**Utiliser la synchronisation automatisée de l’achèvement des travaux des utilisateurs**

Le processus automatisé de synchronisation de l’achèvement des travaux des utilisateurs permet à un administrateur Learning Manager de récupérer automatiquement les enregistrements d’achèvement et l’URL d’enregistrement pour la réunion de Microsofts Teams.

## Rôles dans Microsoft Teams

Si vous organisez une réunion avec plusieurs participants, vous pouvez attribuer des rôles à chaque participant afin qu’il sache ce qu’il peut faire lors de la réunion.

Deux rôles sont proposés : **présentateur** et **participant**.

Pour plus d&#39;informations, voir [Rôles lors d&#39;une réunion Teams - Microsoft](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## Configurer le connecteur Microsoft Teams

>[!NOTE]
>
>Les éléments marqués comme &lt;Developer/Optional> ci-dessous sont facultatifs et servent principalement à configurer des clients d’évaluation/de développement avec Microsoft si l’utilisateur ne dispose pas d’un client de production. Ces tâches sont facultatives, car elles auraient déjà été généralement effectuées par l’administrateur de votre équipe.

## Créer un compte développeur E5 Microsoft &lt;Developer/Optional>

Vous pouvez accéder au connecteur de Microsofts Teams si vous disposez d&#39;Office 365 E3 ou d&#39;Office 365 E5. L’option recommandée est Office 365 E5.

* Consultez la [page des formules Microsoft](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&amp;ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;lnkd=Google_O365SMB_Brand&amp;gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE) . Sur la page Web, vous pouvez acheter un compte E3 ou E5 ou cliquer sur Essayer gratuitement.

* Fournissez les informations nécessaires et créez un compte.

>[!NOTE]
>
>Le compte doit utiliser le format `<username>@<company name>.onmicrosoft.com`.

## Création d’une application pour le connecteur de Microsofts Teams

1. Rendez-vous sur le [portail Microsoft Azure®](https://portal.azure.com/).
1. Connectez-vous avec le compte Microsoft E5 que vous avez créé dans la section précédente.
1. Recherchez **Azure Active Directory**.
1. Cliquez sur **[!UICONTROL Enregistrements d&#39;applications]**.
1. Cliquez sur **[!UICONTROL Nouvel enregistrement]**, saisissez les informations suivantes, puis enregistrez l&#39;application :

   1. **Nom** : tout nom de votre choix.
   1. **Types de comptes pris en charge** : comptes dans n’importe quel répertoire organisationnel (tout multiclient Azure Active Directory).
   1. **URI de redirection (facultatif)** : champ facultatif indiquant l’URL de réponse.

1. Dans la colonne **Essentials**, notez les ID suivants, qui seront utilisés ultérieurement lors de l’intégration :

   1. **ID (client) de l&#39;application**
   1. **ID (client) de répertoire**

1. Recherchez les informations d&#39;identification du client et cliquez sur **[!UICONTROL Ajouter un certificat ou un secret]**.
1. Cliquez sur **[!UICONTROL Nouveau secret du client]** et ajoutez les détails suivants :

   1. **Description** : saisissez un nom.
   1. **Expire** - Définissez n&#39;importe quelle valeur (la valeur recommandée est 24 mois. Assurez-vous que les informations d’identification du nouveau client soient bien générées après expiration des précédentes).

Notez le secret du client, qui sera utilisé ultérieurement lors de l’intégration.

## Obtenir l&#39;autorisation d&#39;accès pour le connecteur de Microsofts Teams

1. Accédez au [portail Microsoft Azure](https://portal.azure.com/).
1. Connectez-vous avec le Microsoft E5 que vous avez créé précédemment.
1. Recherchez **Azure Active Directory**.
1. Cliquez sur **[!UICONTROL Enregistrements d&#39;applications]**.
1. Cliquez sur l’application que vous avez créée à la section précédente.
1. Cliquez sur **[!UICONTROL Autorisations API]**.
1. Cliquez sur **[!UICONTROL Ajouter une autorisation]**.
1. Sélectionnez **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Autorisations de l&#39;application]** et ajoutez les autorisations suivantes :

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All

1. Cliquez sur **[!UICONTROL Accorder l&#39;accès administrateur pour l&#39;Adobe]**.
1. Cliquez sur **[!UICONTROL Rôles d&#39;application]** > **[!UICONTROL Créer un rôle d&#39;application]**.
1. Saisissez les valeurs suivantes :

   1. **Nom d&#39;affichage** : nom de l&#39;API/autorisation (par exemple, Calendars.ReadWrite).

   1. **Types de membres autorisés** : spécifiez à la fois les utilisateurs et les applications (Utilisateurs/Groupes + Applications).

   1. **Valeur** : nom de l’API/autorisation (par exemple, Calendars.ReadWrite).

   1. **Description** : nom de l&#39;API/autorisation (par exemple, Calendars.ReadWrite).

   1. **Voulez-vous activer ce rôle d&#39;application ?** - Cochez cette case.

1. Répétez les étapes précédentes pour les neuf API/autorisations ajoutées.

## Configuration de la stratégie d’accès à l’aide de scripts PowerShell

Pour configurer la stratégie d&#39;accès de l&#39;application pour le connecteur de Microsofts Teams en exécutant des scripts PowerShell, suivez la procédure décrite dans ce [document](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

Cela permet au connecteur d’accéder aux réunions en ligne de Microsoft Teams.

>[!NOTE]
>
>Dans le document ci-dessus, exécutez également l’étape facultative 5 pour vous assurer que tout utilisateur actif peut se voir accorder le rôle d’organisateur dans l’application Learning Manager Author. Si cette étape n’est pas exécutée, les utilisateurs ne disposeront pas des autorisations d’accès requises pour être organisateurs et la création de la réunion échouera (les API Microsoft considèrent l’organisateur comme le créateur d’une réunion Teams).

## Configuration du connecteur de Microsofts Teams dans Learning Manager

1. Se connecter à Learning Manager en tant qu’administrateur d’intégration.

1. Dans la page Connecteurs, sélectionnez Connecteur Microsofts Teams et cliquez sur **[!UICONTROL Connecter]**.

1. Saisissez les valeurs suivantes :

   1. **Nom de la connexion** : donnez le nom que verra l&#39;auteur lors de la création de la session.

   1. **ID du client Microsofts Teams** : entrez la valeur précédemment déterminée.

   1. **ID du client de Microsofts Teams** : entrez la valeur précédemment déterminée.

   1. **Secret du client Microsofts Teams** : entrez la valeur précédemment déterminée.

   1. **Adresse e-mail de l’utilisateur administrateur des Microsofts Teams** : entrez l’adresse e-mail par défaut de l’organisateur. Cet utilisateur (généralement un utilisateur du service) sera le créateur de la réunion si aucun organisateur n’est sélectionné dans l’application Learning Manager Author.

## Attribuer des licences aux utilisateurs &lt;Developer/Optional>

1. Visitez [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage).
1. Cliquez sur **[!UICONTROL Utilisateurs]** > **[!UICONTROL Utilisateurs actifs]**.
1. Cliquez sur **[!UICONTROL Autres actions pour les utilisateurs]** pour les utilisateurs auxquels vous souhaitez donner accès aux Microsofts Teams.
1. Cliquez sur **[!UICONTROL Gérer les licences de produit]**.
1. Activer la licence pour Office 365 E5 sans conférence audio.

## Enregistrer une session

L’API utilisée pour enregistrer une session est une API protégée. Pour accéder à l’API, vous devez demander l’accès à Microsoft. Pour plus d&#39;informations, consultez ce [document](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

Dans le document,

*« Pour demander l&#39;accès à ces API protégées, remplissez le [formulaire de demande](https://aka.ms/teamsgraph/requestaccess) suivant. Nous passons en revue les demandes d’accès tous les mercredis et nous déployons des autorisations tous les vendredis, sauf lors de semaines de fêtes aux États-Unis. Les envois reçus durant ces semaines seront traités la semaine ouvrée suivante. Pour vérifier si votre demande a été approuvée, testez votre accès à l&#39;application le prochain lundi.«*

Pour les élèves, l’URL de l’enregistrement est affichée sur la page de présentation du cours de la classe virtuelle.

30 minutes après la fin d’un cours, l’assiduité de l’élève est notée.

## Forum aux questions

+++Qui est un organisateur et un présentateur ?

Consultez la [documentation](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019) de Microsoft pour connaître les différents rôles et capacités pris en charge par les Microsofts Teams.

+++

+++Un organisateur doit-il être un utilisateur inscrit à Learning Manager et aux Microsofts Teams ?

Oui, le présentateur doit faire partie à la fois de Learning Manager et de Microsoft Teams. En outre, l’organisateur doit faire partie du même locataire Microsoft, qui est configuré dans l’application d’administration de l’intégration.

+++

+++Un présentateur doit-il être un utilisateur inscrit à Learning Manager et aux Microsofts Teams ?

Oui, le présentateur doit faire partie à la fois de Learning Manager et des Microsofts Teams. Le présentateur doit avoir un ID Azure Active Directory (peut faire partie du même client que l’organisateur ou de tout autre client). En outre, même les utilisateurs anonymes (utilisateurs qui se connectent uniquement avec le nom d’utilisateur et qui ne font pas partie d’Active Directory) peuvent également être désignés comme présentateurs par l’organisateur/les présentateurs existants pendant la réunion.

+++

+++Microsofts Teams a des réunions, des webinaires et des événements en direct. Lequel est pris en charge par le connecteur Teams ?

Actuellement, le connecteur Teams prend uniquement en charge les réunions dans les Microsofts Teams. Pour plus d&#39;informations, consultez ce [document](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++
