---
description: Découvrez comment les administrateurs renvoient des invitations à une session aux élèves inscrits à une session de classe virtuelle dans Adobe Learning Manager
jcr-language: en_us
title: Renvoyer l’invitation à la session
exl-id: 12ee20a8-4521-4235-8120-596812da7809
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 2%
---

# Renvoyer les invitations à une session

## Présentation

>[!NOTE]
>
>Le redéclenchement est disponible uniquement pour les sessions de classe virtuelle (VC). Les autres types de modules, tels que les modules de salle de classe et d’auto-apprentissage (e-learning), ne sont pas pris en charge.

Les élèves peuvent manquer une invitation pour plusieurs raisons. Avec l&#39;option **Renvoyer**, en tant qu&#39;administrateur autorisé à modifier les cours, vous pouvez ouvrir une session VC sur la page de l&#39;instance, rechercher les élèves et envoyer l&#39;e-mail d&#39;invitation à la session. Learning Manager envoie l’e-mail à la demande, en dehors du flux d’événements d’inscription. L’élève reçoit les détails de la session et une invitation de calendrier, et l’état d’inscription reste le même.

## Cas d’utilisation

Voici les cas d’utilisation dans lesquels vous renvoyez une invitation à une session.

* **Récupérer une invitation manquée.** Renvoyez l’invitation à un élève dont la boîte aux lettres était pleine, dont l’e-mail est devenu du spam ou dont l’e-mail d’origine n’a pas été remis.
* **Réduire les absences.** Renvoyez les détails de la session et l’invitation de calendrier juste avant la session ou le jour de la session.
* **Évitez les solutions d’inscription.** Renvoyez une invitation sans désinscrire ni réinscrire l’élève, afin que l’état d’inscription et l’inscription à la session restent intacts.
* **Réduisez les tickets de support.** Les administrateurs résolvent eux-mêmes les demandes d’invitation manquantes, sans impliquer l’équipe d’assistance.

## Conditions préalables

* La session est une session VC.
* L’élève est inscrit à la session cible. Learning Manager envoie l’invitation uniquement aux élèves inscrits à la session.
* La session existe déjà. Cette fonctionnalité ne crée ni ne modifie de sessions.
* Le modèle d’e-mail d’invitation à une session existant est utilisé. Cette fonctionnalité n’introduit pas de nouveau modèle de courrier électronique.

## Configurations prises en charge

| Élément | Assistance |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Rôles | Administrateurs autorisés à modifier le cours. Instructeurs pour les sessions auxquelles ils sont affectés. |
| Types d’éléments de catalogue | Cours et parcours d’apprentissage |
| Type de module | Sessions de classe virtuelle (VC) |
| Séances | Sessions actuelles et futures. Les sessions précédentes ne sont pas prises en charge. |
| fournisseurs VC | Tous les fournisseurs configurés pour la session, tels que Zoom, Équipes et Adobe Connect |
| Modèles de courriers électroniques | Les modèles configurés pour l’objet d’apprentissage : un e-mail de détails de session et une invitation de calendrier |
| Destinataires | Élèves individuels inscrits à la session. Les groupes d’utilisateurs ne sont pas pris en charge. |
| Déclencheur | Manuelle, à partir de l’action Renvoyer l’invitation à une session |

Le rôle de responsable n’a pas accès à cette fonctionnalité dans cette version. L’option est masquée aux élèves et aux responsables.

## Accéder à l’action Renvoyer l’invitation à une session

L’emplacement de l’action dépend de votre rôle.

| Rôle | Où trouver l’action |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L’administrateur | Ouvrez le cours ou le parcours d’apprentissage dans le catalogue, accédez à Instances et ouvrez l’instance. Dans la section Sessions, recherchez la session VC et sélectionnez Renvoyer l’invitation à la session. Vous devez obtenir l’autorisation de modifier le cours. |

## Boîte de dialogue Renvoyer

La boîte de dialogue Renvoyer les invitations à une session contient les éléments suivants.

| Élément | Description |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sélectionner des élèves | Champ de recherche. Saisissez le nom ou l’adresse e-mail d’un élève pour le rechercher, puis sélectionnez-le. Vous pouvez sélectionner plusieurs élèves. Une note explique que chaque élève sélectionné reçoit deux e-mails : un e-mail détaillant la session et une invitation de calendrier, en fonction des modèles configurés pour l’objet d’apprentissage. |
| Annuler | Ferme la boîte de dialogue sans envoyer d’e-mails. |
| Renvoyer | Envoie les e-mails aux élèves sélectionnés. Le bouton est désactivé tant que vous n’avez pas sélectionné au moins un élève. |

>[!NOTE]
>
>La recherche correspond à des élèves individuels uniquement. Vous ne pouvez pas rechercher ou sélectionner des groupes d’utilisateurs.

## Renvoyer une invitation à une session

Effectuez les étapes suivantes en tant qu’administrateur.

1. Connectez-vous en tant qu’administrateur autorisé à modifier le cours.
2. Accédez à **Formation** > **Cours**.

   ![](assets/resend-session-invite1.png)

3. Ouvrez le cours dont vous souhaitez accéder aux instances.

   ![](assets/resend-session-invite2.png)

4. Accédez à l&#39;instance dont vous souhaitez accéder à la session.
5. Dans la section **Détails de la session** ci-dessous, sélectionnez **Renvoyer l&#39;invitation à la session**.

   ![](assets/resend-session-invite3.png)

6. La fenêtre contextuelle **Renvoyer l&#39;invitation à une session** s&#39;ouvre.

   ![](assets/resend-session-invite4.png)

7. Recherchez l’élève ou les élèves auxquels vous souhaitez renvoyer l’invitation.

   ![](assets/resend-session-invite5.png)

   ![](assets/resend-session-invite6.png)

8. Sélectionnez **Renvoyer**. Vous verrez un message indiquant « Invitation à une session envoyée à « x » élèves ».

   ![](assets/resend-session-invite7.png)

9. Si l’un des élèves sélectionnés provient d’une autre session, un message s’affiche indiquant : « Un élève sélectionné n’est pas inscrit à cette session et a été ignoré ».

   ![](assets/resend-session-invite8.png)

10. Après quelques minutes, le ou les élèves recevront un courrier électronique contenant les détails de la session, y compris un lien pour rejoindre la session.

![](assets/resend-session-invite9.png)

Learning Manager vérifie que chaque élève sélectionné est inscrit à la session cible, puis envoie l’invitation à la session existante aux élèves éligibles.

Lorsque Learning Manager accepte la demande, la boîte de dialogue se ferme et un message de confirmation s’affiche : « Des e-mails d’invitation sont envoyés à l’élève(s) pour la session. Cette opération peut prendre un certain temps. » Les e-mails arrivent généralement en quelques minutes.

## Contenu des e-mails

Chaque élève sélectionné reçoit l’e-mail des détails de la session et l’invitation de calendrier pour la session. Le contenu comprend le lien de jointure de la session VC, la date et l&#39;heure, ainsi que les détails de la session. L’e-mail est identique à l’invitation à la session d’origine, car Learning Manager utilise le même modèle.

## Comportement d’inscription multiple

Le renvoi est spécifique à une instance. Si un élève est inscrit dans plusieurs instances, le renvoi d’une instance envoie l’invitation uniquement pour cette instance. Cela ne redéclenche pas les invitations pour les autres instances de l’élève.

| Inscription de l&#39;élève | Action | Résultat |
|------------------------------------------------|------------------------------------------------|----------------------------------------------------------------------------------|
| Instance A et Instance B | Renvoyer à partir de l&#39;instance A | Seule l’invitation Instance A est renvoyée. |
| Instance A uniquement | Renvoyer à partir de l&#39;instance A | L’invitation de l’instance A est renvoyée. |
| Une instance différente de la session sélectionnée | L’élève apparaît dans la recherche au niveau du cours | Learning Manager ignore l’élève pour la session sélectionnée et affiche un avertissement. |

## Comportement dans des scénarios spécifiques

| Scénario | Comportement |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L&#39;instance n&#39;a pas de sessions VC | L’action Renvoyer l’invitation à la session n’est pas disponible. |
| La session a déjà eu lieu | L’action n’est pas disponible. Learning Manager prend uniquement en charge les sessions actuelles et futures. |
| Vous sélectionnez un élève qui n’est pas inscrit à la session | La recherche d’élèves couvre l’ensemble du cours, de sorte que vous pouvez trouver des élèves d’autres instances. Learning Manager ignore les élèves qui ne sont pas inscrits à la session sélectionnée, envoie l’invitation aux autres et affiche un avertissement. |
| Un élève est inscrit dans plusieurs instances | Learning Manager envoie l’invitation uniquement pour l’instance à partir de laquelle vous l’avez envoyée. Cela n’envoie pas d’invitations pour les autres instances. |
| Une instance de parcours d’apprentissage est sélectionnée | L’action fonctionne de la même manière que pour une instance de cours. |

## Gestion des erreurs

Si une erreur empêche Learning Manager d’envoyer les e-mails, la boîte de dialogue affiche l’un des messages suivants.

| Condition | Message |
|---------------------------------------|------------------------------------------------------------------------|
| Le modèle de courrier électronique d’invitation est désactivé | Impossible d’envoyer l’e-mail : le modèle d’e-mail d’invitation est actuellement désactivé. |
| Toute autre erreur | Une erreur s’est produite lors de l’envoi de l’e-mail. Veuillez réessayer ultérieurement. |

Si vous sélectionnez des élèves qui ne sont pas inscrits à la session, Learning Manager affiche un avertissement indiquant que l’invitation a été ignorée pour ces élèves. L’invitation est toujours envoyée aux élèves inscrits.

>[!NOTE]
>
>Le service de messagerie signale l’état de remise à Learning Manager de manière asynchrone, après la fermeture de la boîte de dialogue.

## Limitations

* Vous pouvez renvoyer des invitations pour les sessions actuelles et futures uniquement.
* Seuls les modèles configurés pour l’objet d’apprentissage sont utilisés. Vous ne pouvez pas sélectionner un autre modèle.
* Vous pouvez renvoyer des invitations pour une session à la fois. Le renvoi simultané de plusieurs instances n’est pas pris en charge.
* Vous ne pouvez pas sélectionner de groupes d’utilisateurs. Vous ne pouvez sélectionner que des élèves individuels.
* Learning Manager envoie des invitations uniquement aux élèves inscrits à la session sélectionnée.
* La boîte de dialogue n’affiche pas l’état de remise des e-mails et ne propose pas de nouvelle tentative pour les élèves individuels.
* Vous ne pouvez pas planifier de nouvelles sessions ni modifier les détails de session existants à partir de la boîte de dialogue.

## Dépannage

| Symptôme | Cause probable | Action |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| L’action Renvoyer l’invitation à la session n’est pas visible | Le module n&#39;est pas une session VC, la session s&#39;est déjà produite ou vous n&#39;êtes pas autorisé à modifier le cours. | Confirmez que la session est une session VC actuelle ou future. Demandez à un administrateur de vérifier vos autorisations de cours. |
| Un avertissement s’affiche après l’envoi des e-mails | Un ou plusieurs élèves sélectionnés ne sont pas inscrits à la session sélectionnée. | Vérifiez quels élèves sont inscrits à la session et renvoyez l’invitation à partir de la session ou de l’instance appropriée. |
| L’invitation est envoyée pour la mauvaise instance | L’élève est inscrit dans plusieurs instances et vous renvoyez l’invitation à partir d’une autre instance. | Ouvrez l’instance dont l’élève a besoin et renvoyez l’invitation à partir de là. |
| L’erreur « Le modèle de courrier électronique d’invitation est actuellement désactivé » s’affiche | Le modèle de courrier électronique d’invitation est désactivé pour l’objet d’apprentissage. | Demandez à un administrateur d’activer le modèle, puis renvoyez l’invitation. |
| L’e-mail présent a le même aspect que l’invitation d’origine | C&#39;est ce qui est attendu. Learning Manager réutilise le modèle d’invitation à une session existant. | Aucune action n’est requise. |
| Vous devez renvoyer des invitations à plusieurs instances à la fois | Ce n’est pas pris en charge. | Renvoyez les invitations de chaque instance séparément. |
| Vous devez renvoyer une invitation pour une classe ou un module d’e-learning | Ce n’est pas pris en charge. Le redéclenchement est disponible uniquement pour les sessions VC. | Aucune action n&#39;est disponible pour ces types de module. |
| Un élève dit que l’e-mail n’est pas arrivé | L’e-mail est toujours en cours de traitement, la boîte aux lettres de l’élève est pleine ou l’e-mail a été filtré comme courrier indésirable. | Patientez quelques minutes, demandez à l&#39;élève de vérifier le dossier de courrier indésirable et de libérer de l&#39;espace dans la boîte aux lettres, puis renvoyez l&#39;invitation. |
