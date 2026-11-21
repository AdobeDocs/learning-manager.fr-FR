---
title: Création d’une session Live Hub
description: Découvrez comment créer un cours Live Hub, ajouter des instances de cours, affecter des instructeurs avec le Finder d'instructeurs, inscrire des élèves et personnaliser l'image de marque de la salle.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 9d05ad4a059bd1fec6e64f050070dae336ba2d1b
workflow-type: tm+mt
source-wordcount: '1617'
ht-degree: 0%
---

# Création d’une session Live Hub

Utilisez Live Hub pour dispenser une formation en direct dispensée par un instructeur dans le cadre d’un cours Adobe Learning Manager. Vous pouvez combiner des sessions Live Hub avec du contenu d’auto-apprentissage pour créer une expérience d’apprentissage mixte.

Lorsque vous ajoutez un module Salle de classe virtuelle à un cours, sélectionnez l’outil de formation virtuelle qui hébergera la session en direct. Vous pouvez choisir **Live Hub**, la solution de formation virtuelle intégrée d&#39;Adobe basée sur l&#39;IA, ou utiliser un fournisseur externe tel que **Adobe Connect**.

>[!NOTE]
>
> Live Hub apparaît comme une option d&#39;outil de formation virtuelle en direct uniquement si votre administrateur l&#39;a activée dans les paramètres Live Hub. Si cette option n’est pas activée, utilisez plutôt un fournisseur externe comme Adobe Connect. Voir [Activer Live Hub](../administrators/feature-summary/enable-live-hub.md) pour plus d&#39;informations.

Lors de la création d&#39;un cours Live Hub, vous pouvez :

* Ajoutez une ou plusieurs sessions Live Hub à un cours.

* Sélectionnez les instructeurs manuellement ou utilisez les recommandations d’instructeur assisté par IA.

* Configurez le cours avec une seule instance par défaut ou créez plusieurs instances pour différents plannings ou audiences.

Cet article explique comment créer un cours Live Hub, affecter des instructeurs et configurer des instances de cours.

## Création d’un cours Live Hub

Une instance par défaut est créée automatiquement lorsque vous ajoutez un module de salle de classe virtuelle. Cela est utile lorsque vous souhaitez fournir une seule session ou un calendrier standard pour tous les élèves.

Pour créer un cours Live Hub :

1. Se connecter à Adobe Learning Manager en tant qu’auteur.

1. Sélectionnez **Créer des cours**.

1. Sur la page **Catalogue de cours**, sélectionnez **Ajouter**, puis saisissez les détails suivants :

   1. Nom du cours

   1. Brève description

   ![Ajouter une description de nom de cours](assets/add-course-name-description.png)
   *Entrez le nom du cours et une brève description avant d&#39;ajouter des modules au cours.*

1. Sélectionnez **Contenu** > **Ajouter des modules** dans la section **Modules**. <br> La fenêtre contextuelle **Sélectionner le type de module** s&#39;affiche.

1. Sélectionnez **Salle de classe virtuelle** et entrez les détails du cours, notamment le titre, la description, le fuseau horaire, les dates de début et de fin, ainsi que les heures de début et de fin.

1. Sélectionnez **Live Hub** dans **Outils de formation virtuelle en direct**.

   ![Sélectionner l&#39;outil Live Hub](assets/select-live-hub-tool.png)
   *Sélectionnez Live Hub pour activer les recommandations d&#39;instructeur basées sur l&#39;IA pour la session.*

1. Ajoutez des instructeurs à l’aide de l’une des options suivantes :

   1. Saisissez les noms des instructeurs dans le champ **Instructeurs**.

   1. Sélectionnez **Trouver des instructeurs utilisant l&#39;IA** pour afficher les instructeurs recommandés par l&#39;IA. Consultez [Ajouter des instructeurs à l&#39;aide du Finder d&#39;instructeurs](#add-instructors-using-instructor-finder) pour plus d&#39;informations.

1. Sélectionnez **Ajouter** > **Enregistrer**.

1. Sélectionnez les compétences requises dans la section **Compétences du cours**.

1. Sélectionnez le **niveau de compétence**, puis passez en revue ou mettez à jour les **crédits maximum**.

   ![Attribuer Le Niveau De Compétence Du Cours](assets/assign-course-skill-level.png)
   *Attribuez un niveau de compétence pour définir les crédits que les élèves acquièrent en suivant le cours.*

1. Sélectionnez **Enregistrer** > **Publish**. Le cours est créé dans Adobe Learning Manager.

## Création d&#39;une instance de cours

Un administrateur peut créer une ou plusieurs instances d&#39;un cours pour l&#39;offrir à différents publics, calendriers ou emplacements. Chaque instance ayant ses propres détails de session, vous pouvez affecter différents instructeurs, les recommandations du Finder d’instructeurs et le minutage à chaque instance du même cours.

Pour créer une instance de cours :

1. Se connecter à Adobe Learning Manager en tant qu’auteur.

1. Ouvrez le cours, puis sélectionnez **Instances** dans le panneau de gauche.

   Page ![Instance par défaut](assets/default-instance-page.png)
   *L&#39;instance par défaut est créée automatiquement lorsque vous ajoutez un module de salle de classe virtuelle.*

1. Sélectionnez **Ajouter une nouvelle instance**.

1. Saisissez le **nom de l&#39;instance**, la **date de début** et l&#39;**échéance**. Sélectionnez **Afficher plus d&#39;options** pour configurer des paramètres supplémentaires.

   ![Ajouter un formulaire d&#39;instance](assets/add-new-instance-form.png)
   *Entrez un nom d&#39;instance, une date de début et une échéance d&#39;achèvement pour créer une nouvelle instance de cours.*

1. Sélectionnez **Enregistrer**. <br> La nouvelle instance est ajoutée à la liste **Instances**.

   ![Liste des instances Nouvelle instance](assets/instances-list-new-instance.png)
   *La nouvelle instance apparaît à côté de l&#39;instance par défaut dans la liste Instances.*

1. Sélectionnez le nombre sous **Sessions** pour afficher les **Détails de la session**.

   Icône Modifier les détails de la session ![](assets/session-details-edit-icon.png)
   *Les détails de la session indiquent les champs de durée, d&#39;instructeur et d&#39;emplacement qui doivent encore être configurés.*

1. Sélectionnez l’icône de modification (crayon) à côté des détails de la session pour ouvrir le panneau de configuration de la session.

   Panneau de configuration de la session ![](assets/session-configuration-panel.png)
   *Configurez la planification, l&#39;instructeur et l&#39;emplacement d&#39;une instance de session spécifique.*

1. Dans le champ **Instructeurs**, saisissez des noms manuellement ou sélectionnez **Rechercher des instructeurs utilisant l&#39;IA** pour les instructeurs recommandés par l&#39;IA. Consultez [Ajouter des instructeurs à l&#39;aide du Finder d&#39;instructeurs](#add-instructors-using-instructor-finder) pour plus d&#39;informations.

1. Saisissez les détails de l&#39;**emplacement**, puis sélectionnez **Enregistrer**. La session est mise à jour avec les horaires configurés, l’instructeur et les détails de l’emplacement.

## Ajout d’instructeurs à l’aide du Finder d’instructeurs

Au lieu de rechercher et d&#39;ajouter des instructeurs manuellement, utilisez le **Finder d&#39;instructeurs** pour recevoir des recommandations d&#39;instructeurs basées sur l&#39;IA pour la session. Le Finder avec les instructeurs compare les instructeurs en fonction des détails du cours et des compétences requises, tout en tenant compte du calendrier des vacances de l’organisation, de la disponibilité des instructeurs et de l’utilisation des instructeurs pour suggérer les instructeurs les plus appropriés. Voir [Ajouter et gérer des instructeurs](./instructor-management.md) pour plus d&#39;informations.

>[!NOTE]
>
> Le Finder d’instructeurs s’affiche uniquement si votre administrateur a activé l’assistant du Finder d’instructeurs dans les paramètres du hub en direct. Voir [Activer Live Hub](../administrators/feature-summary/enable-live-hub.md) pour plus d&#39;informations.

Pour ajouter des instructeurs à l’aide du Finder d’instructeurs :

1. Accédez à la section **Instructeurs** dans le module **Classe virtuelle**.

1. Sélectionnez **Trouver des instructeurs à l’aide de l’IA**. <br> Le panneau **Assistant IA** s&#39;ouvre sur le côté droit.

   ![Recommendations de l&#39;instructeur du panneau Assistant d&#39;IA](assets/ai-assistant-panel-instructor-recommendations.png)
   *Utilisez le panneau de l&#39;Assistant IA pour obtenir des recommandations d&#39;instructeur et de créneau horaire en fonction des détails de la session.*

1. Consultez la liste des instructeurs recommandés.

1. Accédez à l’instructeur que vous souhaitez affecter, puis sélectionnez **Ajouter**. <br> L&#39;instructeur sélectionné est ajouté au champ **Instructeurs** en tant que balise.

## Créer un cours pour une session volumineuse {#create-large-session}

Live Hub prend en charge de grandes sessions pouvant accueillir jusqu’à 5 000 participants. Lorsque vous créez un cours avec cette capacité, Live Hub configure automatiquement la salle pour un grand public et applique les restrictions de fonctionnalités correspondantes.

Pour créer une session volumineuse :

1. Connectez-vous à ALM en tant qu&#39;**auteur**.
1. Sélectionnez **Ajouter** sur la page **Catalogue de cours**.
1. Saisissez le nom et la description du cours.
1. Sélectionnez **Contenu** > **Ajouter des modules** dans la section **Modules**. La fenêtre contextuelle **Sélectionner le type de module** s&#39;affiche.
1. Sélectionnez **Salle de classe virtuelle** et entrez les détails du cours, notamment le titre, la description, le fuseau horaire, les dates de début et de fin, ainsi que les heures de début et de fin.
1. Sélectionnez **Live Hub** dans **Outils de formation virtuelle en direct**.
1. Sélectionnez **Activer 5 000 participants**. Si vous n’activez pas cette option, la session prend en charge jusqu’à 1 100 participants.

   ![Boîte de dialogue Salle de classe virtuelle avec Live Hub sélectionné et l’option Activer la capacité de 5 000 participants](assets/virtual-classroom-enable-5000-attendee-capacity.png "Boîte de dialogue Salle de classe virtuelle avec Live Hub sélectionné et l’option Activer la capacité de 5 000 participants")

1. Sélectionnez **Enregistrer** > **Publish**.

### Fonctionnalités disponibles dans les sessions étendues

Lorsqu’un instructeur ouvre la session, les paramètres de la salle indiquent que des restrictions de session volumineuse s’appliquent.

| Fonctionnalité | Comportement dans une grande session |
|---|---|
| **Participants** | Une grande session peut accueillir jusqu’à 5 000 participants. Une fois que la session atteint cette limite, d’autres participants ne peuvent plus participer. |
| **Caméras** | Jusqu’à 10 instructeurs peuvent activer leurs caméras simultanément. Les élèves ne peuvent pas activer leurs caméras. Si la caméra maximale est atteinte, un message s’affiche lorsqu’un autre instructeur tente d’activer sa caméra.<p>Les demandes de caméra effectuées en même temps sont traitées par lots. Par conséquent, le nombre de caméras actives peut dépasser la limite configurée. Cependant, l’info-bulle du bouton caméra continue d’afficher la limite configurée. |
| **Microphones** | Jusqu&#39;à 20 participants peuvent activer le son de leur microphone simultanément. Si la limite du microphone est atteinte, un message s’affiche lorsqu’un autre participant tente d’activer le son.<p>Les demandes de microphone effectuées en même temps sont traitées par lots. Par conséquent, le nombre de participants dont le son est rétabli peut temporairement dépasser la limite configurée. |
| **Salles de réunion** | L’icône de la salle de petits déjeuners reste visible, mais les instructeurs ne peuvent pas démarrer les salles de petits déjeuners. Un message s’affiche lorsqu’ils tentent d’en créer un. |
| **Partage d&#39;écran et tableau blanc** | Seuls les instructeurs peuvent partager leurs écrans et utiliser le tableau blanc. Les instructeurs ne peuvent pas fournir ces autorisations aux élèves. |
| **Conversation privée** | Les élèves peuvent envoyer des messages privés aux instructeurs, mais ils ne peuvent pas envoyer de messages privés à d&#39;autres élèves. |
| **Indicateur de saisie** | L’indicateur de saisie n’apparaît pas dans les sessions volumineuses. |
| **Conversation, réactions, questions et mains levées** | Le système traite ces interactions par lots, de sorte qu’elles peuvent apparaître après un court délai. Live Hub regroupe également les réactions et affiche un nombre limité à la fois. |
| **Historique des conversations** | Le système supprime automatiquement les anciens messages de conversation lorsque l&#39;historique des conversations devient trop volumineux pour maintenir la stabilité de la session. |
| **Sondages, questionnaires, enregistrement et présence** | Ces fonctions fonctionnent de la même manière que dans les sessions ordinaires. |
| **Fonctionnalités IA** | <ul><li>Le système détecte les questions dans la conversation et les affiche dans le panneau **Questions**, même si elles peuvent apparaître après un court délai.</li><li>Les fonctionnalités d&#39;IA associées aux salles de petits groupes ne sont pas disponibles car les sessions de grande taille ne prennent pas en charge les salles de petits groupes.</li><li>D’autres fonctionnalités d’IA fonctionnent de la même manière que dans les sessions ordinaires.</li></ul> |

>[!NOTE]
>
>Sans l&#39;option **Activer la capacité de 5 000 participants**, une session régulière prend en charge jusqu&#39;à 1 100 participants, 50 caméras et 20 participants dont le son est rétabli.

## Inscription d’élèves au cours

Les élèves peuvent être inscrits à un cours Live Hub de deux manières :

1. Un **administrateur** inscrit des élèves au cours en fonction des exigences de l&#39;organisation. Pour plus d&#39;informations, consultez [Créer des instances de cours et des parcours d&#39;apprentissage](https://experienceleague.adobe.com/fr/docs/learning-manager/using/admin/courses).

1. Les élèves peuvent directement s&#39;inscrire au cours à partir de la page **Catalogue**. Si le cours est configuré pour l&#39;auto-inscription, les élèves sont immédiatement inscrits et peuvent accéder au cours à partir de **Mes apprentissages**. Consultez [Mes apprentissages](https://experienceleague.adobe.com/fr/docs/learning-manager/using/learner/courses) pour plus d&#39;informations.

Après l’inscription, les élèves sont ajoutés au cours et reçoivent une notification dans leur compte Adobe Learning Manager. En fonction des paramètres de notification par e-mail du compte, les élèves peuvent également recevoir une invitation à rejoindre le cours par e-mail.

## Personnalisation de l’image de marque de la salle Live Hub

Les administrateurs peuvent personnaliser l’apparence des salles Live Hub pour l’aligner sur la marque de votre organisation. Utilisez les paramètres **Thèmes** dans Adobe Learning Manager pour appliquer les couleurs, les logos et le style visuel de la marque dans les sessions Live Hub.

L’image de marque personnalisée permet de créer une expérience d’apprentissage cohérente et garantit que les sessions de formation en direct reflètent l’identité de votre entreprise.

Pour plus d&#39;informations sur la configuration des thèmes, consultez l&#39;article [Thèmes de couleur](../administrators/feature-summary/themes.md#color-themes).
