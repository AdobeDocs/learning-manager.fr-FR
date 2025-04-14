---
title: Inscription multiple dans Adobe Learning Manager
description: En tant qu’administrateur du compte, l’une de vos principales tâches consiste à créer différentes instances de sessions VILT dans différents fuseaux horaires, voire des sessions destinées à des groupes d’utilisateurs spécifiques.
exl-id: c430545d-b48e-432d-a278-658c9281818f
source-git-commit: 66c46725a5ba1055899f2b4c30d53a4d23d31cff
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 65%

---

# Inscription multiple dans Adobe Learning Manager

Dans Adobe Learning Manager, chaque cours peut présenter différentes instances. En tant qu’administrateur du compte, l’une de vos principales tâches consiste à créer différentes instances de sessions VILT dans différents fuseaux horaires, voire des sessions destinées à des groupes d’utilisateurs spécifiques.

Avant la version de juillet 2023, lorsqu’un administrateur inscrivait un élève, celui-ci pouvait s’inscrire à une seule instance. Si un élève souhaitait suivre un cours dans différentes instances, l’administrateur créait de nombreux cours (un par instance).

La fonctionnalité d’inscription multiple d’Adobe Learning Manager permet à un administrateur d’éviter ce type de scénarios.

## Gestion des instances

>[!INFO]
>
>Dans cette formation, vous apprendrez à modifier les détails et les propriétés de l&#39;instance.<br><br>[![bouton](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318912)</br></br>

Si vous ne pouvez pas lancer la formation, écrivez à <almacademy@adobe.com>.

## Qu’est-ce que l’inscription multiple ?

La fonctionnalité d’inscription multiple inscrit un élève plusieurs fois à un cours via différentes instances disponibles.  Un élève peut s’inscrire à plusieurs instances de cours, quel que soit son état d’inscription, de fin ou de démarrage. Lorsque l’auteur active l’option [!UICONTROL Inscription multiple], un élève peut s’inscrire à plusieurs instances du cours.

![image à inscriptions multiples](assets/multi-enrollment-author.png)
*Lancer l&#39;inscription multiple à partir des paramètres*

Il est possible d’effectuer le suivi de la progression de chaque instance et d’exporter un rapport de suivi de la progression de chaque instance.

## Points importants

* L’inscription multiple s’applique uniquement si un cours dispose de plusieurs instances.
* Lorsque l’option d’inscription multiple est activée et que les utilisateurs sont inscrits à plusieurs instances, de nouvelles lignes sont créées pour chaque cours dans le rapport Relevé de notes de l’élève (une ligne par instance et par élève)
* Si l’automatisation de la génération de rapports est configurée, qui prévoit une seule ligne par cours, vous devez ajuster l’automatisation de la génération de rapports de manière appropriée avant d’activer la fonctionnalité d’inscription multiple.

## Procédure pour activer l’inscription multiple

1. Connectez-vous à votre compte Adobe Learning Manager en tant qu’auteur.
1. Sélectionnez le cours auquel vous souhaitez que les élèves s’inscrivent plusieurs fois.
1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Modifier]** > **[!UICONTROL Configuration de l&#39;instance]** > **[!UICONTROL Activer l&#39;inscription multiple]**.

![image à inscriptions multiples](assets/multi-enrollment-author.png)
*Activer l&#39;inscription multiple*

>[!NOTE]
>
>En tant qu’auteur, vous ne pouvez pas activer le changement d’instance et l’inscription multiple simultanément.

## Vue Élève

Les inscriptions multiples sont utiles si un élève souhaite s’inscrire à un cours en salle de classe ou en classe virtuelle ou s’il souhaiter suivre un cours à nouveau avant de passer à un autre.

Si les élèves ne se sont pas inscrits, l’écran sous le cours affiche plusieurs instances lorsqu’ils sélectionnent un cours. Ils peuvent sélectionner chaque instance et s’inscrire.

![image vue par l’élève](assets/learner-view.png)
*Afficher les instances*

Après l’inscription dans une instance, ils peuvent s’inscrire dans d’autres instances en sélectionnant l’option Afficher toutes les instances dans le volet de droite.

![image du cours à inscriptions multiples](assets/enroll-instance.png)
*S&#39;inscrire à une instance*

Il est possible d’effectuer le suivi de la progression de chaque instance comme suit :

![suivre la progression](assets/check-progress.png)
*Suivre la progression de chaque instance*

## Modifications liées à l’inscription multiple pour l’administrateur

**Inscription :**

Lorsque vous inscrivez des élèves, vous pouvez cocher la case suivante :

*« Le ou les élèves sélectionnés sont peut-être déjà inscrits à d&#39;autres instances de ce cours. Autoriser ce ou ces élèves à s’inscrire également à l’instance ... »*

![modifications d’administrateur](assets/admin-changes.png)
*Option d’inscription pour les administrateurs*

Si l’élève est déjà inscrit à une instance et que vous, en tant qu’administrateur, essayez de l’inscrire à une autre instance de cours, sélectionnez Oui.

## Rapports

Si un élève est inscrit à deux instances du même cours, deux lignes sont créées pour chaque instance du cours. Le rapport affiche également la progression des instances.
