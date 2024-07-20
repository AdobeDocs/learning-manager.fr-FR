---
jcr-language: en_us
title: Notifications
description: La fonctionnalité Notifications s’applique à tous les utilisateurs d’Adobe Learning Manager. Mais, chaque utilisateur en fonction de son rôle reçoit différents types de notifications selon différents scénarios.
contentowner: manochan
exl-id: 27eb3830-ff4f-44e6-9f63-096d9444378e
source-git-commit: 69ef7d1e27fac3db49cbb4b9f9403f74e146efb5
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 66%

---

# Notifications

La fonctionnalité Notifications s’applique à tous les utilisateurs d’Adobe Learning Manager. Mais, chaque utilisateur en fonction de son rôle reçoit différents types de notifications dans différents scénarios. Toutes les alertes et notifications aux utilisateurs sont affichées dans la boîte de dialogue contextuelle de notifications.

## Notifications d’accès {#accessnotifications}

Les utilisateurs peuvent consulter les notifications en cliquant sur l’icône Notifications dans l’angle supérieur droit de la fenêtre. Cette boîte de dialogue contextuelle affiche les zones mises en surbrillance de toutes les notifications ainsi que l’heure de l’occurrence avec une barre de défilement. Pour afficher plus d’informations sur toutes les notifications, cliquez sur Afficher toutes les notifications au bas de la boîte de dialogue contextuelle. La page des notifications s’affiche.

Vous pouvez connaître le nombre des dernières notifications par le nombre mis en surbrillance sur l’icône de notification. Par exemple, s’il y a cinq dernières notifications depuis votre connexion précédente, vous pouvez voir le numéro 5 affiché sur l’icône de notification. Ces numéros disparaissent une fois que vous avez lu toutes les dernières notifications.

## Types de notifications destinées aux administrateurs {#typesofnotificationsforadministrators}

Les administrateurs reçoivent des notifications dans les cas suivants :

* Chaque fois qu’une liste d’utilisateurs au format csv est téléchargée.
* Chaque fois que le téléchargement d’une liste d’utilisateurs au format csv a échoué. L’administrateur reçoit un message avec la raison de l’échec.
* L’administrateur peut également configurer des alertes de notification au niveau de l’instance pour les cours et les programmes d’apprentissage. Dans ce cas, l’administrateur reçoit les notifications en fonction de la fréquence sélectionnée au niveau de l’instance.

>[!NOTE]
>
>Si un administrateur dispose de privilèges d’auteur ou de responsable en plus de son rôle, il reçoit des notifications relatives à chaque rôle.

Un exemple de fenêtre de notification pour le rôle d’administrateur est illustré dans l’instantané suivant :

![](assets/admin-notification.png)

*Afficher les notifications de l&#39;administrateur*

Cette fenêtre contextuelle affiche les zones en surbrillance de toutes les notifications, ainsi que l’heure de l’occurrence et une barre de défilement. Vous pouvez connaître le nombre des dernières notifications basées sur le nombre en surbrillance sur l’icône des notifications. Par exemple, s’il y a cinq dernières notifications depuis votre connexion précédente, vous pouvez voir le numéro 5 affiché sur l’icône de notification. Ces numéros disparaissent une fois que vous avez lu toutes les dernières notifications.

Cliquez sur le lien **[!UICONTROL Afficher toutes les notifications]** en bas de la fenêtre contextuelle des notifications pour afficher toutes les notifications dans une page distincte. Sur la page des notifications, vous pouvez voir les éléments suivants :

* **Toutes les notifications** : consultez toutes les notifications ici
* **En attente** : affichez les notifications en attente ici
* **Discussion** : recherchez des cours pour voir les discussions en cours.

## Configurer des notifications d’escalade à plusieurs niveaux {#setupmultilevelescalationnotifications}

Lorsque les élèves ne respectent pas les échéances, les courriers électroniques d’escalade peuvent être envoyés au responsable et à un responsable direct. Vous pouvez configurer des notifications d’escalade à plusieurs niveaux pour le non-achèvement du cours pendant le processus de création d’un cours, ou même après sa création. Les notifications d’escalade peuvent être configurées pour être envoyées à une fréquence définie à un responsable ou à un responsable direct.

1. Connectez-vous en tant qu’administrateur ou auteur et cliquez sur Cours.
1. Sélectionnez le cours pour lequel vous souhaitez modifier les notifications d&#39;escalade et cliquez sur **[!UICONTROL Afficher le cours]**.

   ![](assets/view-courses.png)

   *Sélectionnez l&#39;option Afficher le cours*

1. Cliquez sur **[!UICONTROL Instances]** > **[!UICONTROL Avertissements]**.

   ![](assets/notification-alert.png)

   *Sélectionnez l&#39;option Alertes de notification*

1. Un calendrier s’ouvre indiquant l’échéance définie pour le cours surligné en rouge. Cliquez sur la date en surbrillance pour voir que les rappels sont définis pour l’élève.

   ![](assets/deadline-calender.png)

   *Afficher les rappels d’échéance*

1. Définissez des rappels en sélectionnant des dates antérieures à l’échéance. Cela vous permet de configurer des rappels pour l’élève à propos de l’échéance qui approche.

   ![](assets/deadline-reminder.png)

   *Définir une date de rappel d&#39;échéance*

1. Sélectionnez une date après l’échéance pour configurer un calendrier de rappels pour l’élève et de notifications d’escalade pour le responsable.

   ![](assets/set-reminders-andescalation.png)

   *Définir des rappels et des dates de réaffectation*

1. Si l’élève ne parvient toujours pas à terminer le cours même après la réaffectation au responsable, les paramètres vous permettent de réaffecter le cours au responsable de l’erreur de l’élève. Cliquez sur une date après l&#39;échéance prolongée, sélectionnez la périodicité des rappels, le nombre de jours pour la planification et sélectionnez **Manager et ignorer le gestionnaire de niveau** dans le menu déroulant **Escalade**. Cliquez sur la coche bleue pour enregistrer les paramètres de notification.

   ![](assets/reminder-to-managerandskipmanager.png)

   *Enregistrer les paramètres de notification*

## Forum aux questions {#frequentlyaskedquestions}

+++Comment configurer les notifications de rappel sur l’instance ?

Sur une instance, cliquez sur Alertes de notification. Un calendrier s’ouvre indiquant l’échéance définie pour le cours surligné en rouge. Cliquez sur la date en surbrillance pour voir que les rappels sont définis pour l’élève. Définissez les rappels, comme expliqué dans cette [section](user-notifications.md#Setupmultilevelescalationnotifications).
+++
