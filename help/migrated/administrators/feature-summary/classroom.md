---
jcr-language: en_us
title: Ajouter des emplacements de salle de classe
description: Les administrateurs peuvent désormais configurer une bibliothèque d’emplacements de salle de classe. Pour chaque emplacement de salle de classe, les administrateurs peuvent définir les métadonnées qui incluent le nom de l’emplacement, la limite de places ainsi que des informations supplémentaires telles que l’URL de l’emplacement. Les auteurs et les administrateurs peuvent ensuite utiliser ces emplacements de classe préconfigurés pour configurer des événements de formation dirigée par un instructeur (modules de salle de classe).
contentowner: saghosh
exl-id: 51a1e38f-d4e2-4c19-bbf7-6696505c0dfd
source-git-commit: 8cb8a95812c97b0b59a2ae5188500cfafe09bd27
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 54%

---

# Salle de classe

## Vue d’ensemble

Les administrateurs peuvent désormais configurer une bibliothèque d’emplacements de salle de classe. Pour chaque emplacement de salle de classe, les administrateurs peuvent définir les métadonnées qui incluent le nom de l’emplacement, la limite de places ainsi que des informations supplémentaires telles que l’URL de l’emplacement. Les auteurs et les administrateurs peuvent ensuite utiliser ces emplacements de classe préconfigurés pour configurer des événements de formation dirigée par un instructeur (modules de salle de classe).

Vous pouvez utiliser les deux méthodes suivantes pour ajouter un emplacement de salle de classe.

## Ajouter une salle de classe via l’interface utilisateur

Vous pouvez ajouter un emplacement de salle de classe en utilisant l’interface utilisateur :

1. Dans l’application Administration (interface utilisateur des rôles d’administrateur), cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Lieux de salle de classe]**.

1. Cliquez sur **[!UICONTROL Ajouter]** > **[!UICONTROL Nouvel emplacement]**.

1. Dans la boîte de dialogue **[!UICONTROL Emplacement de salle de classe]**, entrez les informations suivantes :

   * Saisissez le **[!UICONTROL Nom de l’emplacement]**. Utilisez un nom unique. Sinon, Learning Manager affiche un message d’erreur.
   * Saisissez la description de l’emplacement dans le champ **[!UICONTROL Informations de localisation]**. Ce champ est facultatif.
   * Saisissez l’**[!UICONTROL URL de localisation]**. L’élève peut voir ces informations dans les détails de la salle de classe. L’URL peut également être une URL d’emplacement de mappage, si nécessaire. Il s’agit d’un champ facultatif.
   * Saisissez et sélectionnez l’option **[!UICONTROL Région d’emplacement]**. Ce champ est facultatif.
   * Saisissez le nombre de places disponibles dans le champ **[!UICONTROL Limite de siège]**. Cela indique la capacité en sièges de la salle de classe. Cette valeur peut être modifiée lors de la création de l’événement de formation dirigée par un instructeur.

   ![](assets/add-classroom-location.png)

   *Ajouter un emplacement de salle de classe*

Après avoir ajouté l’emplacement, le **[!UICONTROL Paramètres]** > **[!UICONTROL Lieux de salle de classe]** la page répertorie les salles de réunion :

![](assets/list-meeting-rooms.png)

*Voir toutes les salles de réunion*

La liste comporte les champs suivants :

**[!UICONTROL Nom de l’emplacement]** - Nom du lieu de la salle de classe.

**[!UICONTROL Sessions futures]** - Nombre d&#39;événements qui se produiront à l&#39;emplacement correspondant. Cliquez sur le numéro pour afficher les détails dans une boîte de dialogue.

![](assets/sessions-list.png)

*Afficher les sessions futures*

La boîte de dialogue affiche les détails de chaque session, y compris le nom de la session, le nom de la formation qui inclut la session et le calendrier de la session. L’heure affichée s’aligne sur le fuseau horaire système de l’élève.

Le **[!UICONTROL Sessions futures]** affichages de champ **zéro** lorsque la salle de classe n’est utilisée pour aucune session ou lorsqu’elle est associée à des sessions précédentes.

**[!UICONTROL Limite de places]** - Affiche la capacité en sièges de la salle de classe.

**URL d’emplacement** - URL fournie lors de la création de l’emplacement de la salle de classe.

**Informations de localisation** - Les informations sur la salle de classe que vous avez fournies lors de sa création.

### Modification des emplacements de salle de classe

Pour modifier les emplacements de salle de classe, procédez comme suit :

1. Dans l’application d’administration (interface utilisateur des rôles d’administrateur), sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Lieux de salle de classe]**.

1. Passez la souris sur l’emplacement de salle de classe souhaité que vous souhaitez modifier.

1. Sélectionner **[!UICONTROL Modifier le lieu de la salle de classe]** icône.

1. Modifier l’emplacement de la salle de classe et sélectionner **[!UICONTROL Enregistrer]**.

## Ajout d’une salle de classe à l’aide du fichier CSV

Vous pouvez également ajouter un ou plusieurs emplacements de salle de classe en important un fichier CSV contenant les informations de la salle de classe.

Entrée **[!UICONTROL Application d’administration]** > **[!UICONTROL Paramètres]** > **[!UICONTROL Lieux de salle de classe]** > **[!UICONTROL Ajouter]**, cliquez sur le bouton **[!UICONTROL Emplacements d’importation en bloc]** bouton. Accédez à l’emplacement contenant le fichier CSV et sélectionnez le fichier.

Le fichier CSV utilise ces champs pour stocker des détails sur un ou plusieurs emplacements de classe :

* name
* info
* url
* (région)
* seatLimit

Vous pouvez personnaliser les en-têtes.

Le fichier CSV doit obligatoirement contenir toutes les colonnes dans le même ordre que celui spécifié ici.

Une fois que le système a importé le fichier CSV, les emplacements sont ajoutés à la bibliothèque.

## Recherche de salles de classe

Pour rechercher des salles de classe, sélectionnez le cours de classe virtuelle, puis accédez à **[!UICONTROL Instances]** > **[!UICONTROL Sessions]**. Un auteur ou un administrateur peut commencer à taper le nom de l’emplacement pour voir les résultats pertinents qui commencent à apparaître. Ils peuvent ensuite sélectionner un emplacement parmi les résultats affichés. Si aucun emplacement n’est affiché dans les résultats de type d’avance, l’utilisateur peut toujours ajouter le nom du nouvel emplacement de salle de classe. Notez que ce nom d’emplacement créé à l’aide du processus de création de sessions n’est pas ajouté à la bibliothèque d’emplacements créée par l’administrateur.

Lorsqu’une salle de classe est ajoutée, la plateforme d’apprentissage indique également si la salle de classe est déjà réservée pour la période mentionnée. Elle fournit même des créneaux horaires alternatifs comme suggestions. Cela permet donc à l’auteur d’ajuster l’heure de la réunion s’il décide d’utiliser le même emplacement de salle de classe.

![](assets/classroom-search.png)

*Rechercher des salles de classe*

## L’administrateur

En tant qu’administrateur, vous pouvez gérer les instructeurs et les instances de cours.

### Configuration des instructeurs :

Dans l’application d’administration, sous **[!UICONTROL Paramètres]** > **[!UICONTROL Généralités]**, les administrateurs peuvent trouver les **[!UICONTROL Gestion des instructeurs]** option. Cette fonctionnalité garantit que seuls des utilisateurs préapprouvés affectés à titre d’instructeurs peuvent être ajoutés pour mener des sessions.

Pour affecter un instructeur, procédez comme suit :

1. Accéder à la section **[!UICONTROL Prise en main]** et sélectionnez **[!UICONTROL Utilisateurs]** dans le volet de gauche.

1. Sélectionnez l’utilisateur souhaité.

1. Attribuez le rôle d’instructeur à l’utilisateur en sélectionnant **[!UICONTROL Actions]** > **[!UICONTROL Attribuer un rôle]**.

### Annulation des sessions :

Sur la **[!UICONTROL Instance de cours]** , les administrateurs peuvent annuler une ou plusieurs sessions. Lorsque des sessions sont annulées, le système supprime tous les détails de la session, mais conserve la limite de places.

En outre, les administrateurs peuvent :

* **[!UICONTROL Afficher l’inscription]**: Obtenir des informations sur les élèves inscrits et sur liste d’attente pour chaque session.
* **[!UICONTROL Désinscription des élèves]**: supprimer des élèves d’un cours avec des sessions annulées sans modifier leur statut d’inscription.
* **[!UICONTROL Gestion de la présence]**: marquer la présence pour les sessions, même si les sessions sont annulées.
* **[!UICONTROL Achèvement du cours]**: les administrateurs peuvent marquer un cours comme terminé même si les sessions ont été annulées.
* **[!UICONTROL Replanification]**: planifier des sessions annulées pour des dates ultérieures et ajouter un instructeur pendant la replanification.

Notez qu’après l’annulation, les élèves restent inscrits à l’instance de formation. Leur statut d’inscription (inscription confirmée, liste d’attente et attente de l’approbation du responsable) reste inchangé. Cela est utile, car l’administrateur peut configurer et replanifier la session annulée à l’avenir.

## Auteur

Si l’administrateur sélectionne l’option **[!UICONTROL Gestion des instructeurs]** , un auteur peut uniquement rechercher et ajouter les utilisateurs dotés du rôle d’instructeur aux sessions de salle de classe, aux sessions de classe virtuelle, aux listes de contrôle et aux modules d’envoi de fichiers.

En outre, un auteur peut :

* Ajouter et supprimer des instructeurs dans des sessions existantes.
* Ajouter des instructeurs aux sessions existantes qui ont déjà un ou plusieurs instructeurs.

Par conséquent, une fois qu’un administrateur a activé le paramètre **[!UICONTROL Gestion des instructeurs]** , seuls les utilisateurs avec le rôle d’instructeur peuvent être ajoutés en tant qu’instructeur.

>[!NOTE]
>
>Cela ne s’applique pas lorsque vous migrez des sessions à l’aide du fichier CSV des sessions. Dans ce cas, un utilisateur qui ne dispose pas du rôle d’instructeur peut être ajouté en tant qu’instructeur.

Sur la **[!UICONTROL Instance de cours]** , un auteur peut annuler une ou plusieurs sessions. Lorsque des sessions sont annulées, le système supprime tous les détails de la session, mais conserve la limite de places.

Par conséquent, un auteur peut utiliser la fonction **[!UICONTROL Annuler la session]** des liens pour annuler une ou plusieurs sessions de classe ou sessions de classe virtuelle disponibles dans la même instance de cours ou dans des instances de cours différentes.

## Se limiter à une liste prédéterminée d’instructeurs

Actuellement, les utilisateurs peuvent ajouter n’importe quel utilisateur inscrit en tant qu’instructeur lors de la création d’une salle de classe ou d’une session de classe virtuelle. Cette fonctionnalité reste inchangée dans cette version.

Cependant, les administrateurs disposent désormais d’une option supplémentaire pour contrôler plus précisément qui est affecté en tant qu’instructeur sur la plateforme d’apprentissage. Cela empêche tout ajout accidentel d’un nouvel instructeur lors de la création d’une session.

## Annuler la session existante

Un auteur ou un administrateur peut annuler une session et la replanifier, si nécessaire.

Lorsqu’un utilisateur annule une session, le système envoie un e-mail d’annulation de réunion à tous les élèves et instructeurs inscrits. L’e-mail inclut les détails de la session mis à jour.

Il existe un modèle nommé **[!UICONTROL Annulation de session]** qui aide à annuler une session.

Sur la page **[!UICONTROL Instance de cours]**, chaque session répertoriée sous une instance de cours inclut une option permettant d’annuler la session.

![](assets/cancel-session.png)

*Annuler une session existante*

Lorsque vous cliquez sur le bouton **[!UICONTROL Annuler la session]**, un message d’avertissement s’affiche.

Dans la boîte de dialogue Message d’avertissement, si vous cliquez sur **[!UICONTROL Continuer]**, le système annule la session.

Le système efface également les détails suivants après l’annulation d’une session :

* Date de début de la session
* Date de fin de la session
* Heure de début de la session
* Heure de fin de la session
* Instructeurs ajoutés à la session
* URL de classe virtuelle
* Emplacement/lieu ajouté à la session
* Limite de liste d’attente ajoutée par le formateur
