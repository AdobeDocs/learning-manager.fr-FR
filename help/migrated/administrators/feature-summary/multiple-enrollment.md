---
title: Inscription multiple à Adobe Learning Manager
description: En tant qu’administrateur de compte, l’une de vos principales tâches consiste à créer différentes instances de sessions VILT dans différents fuseaux horaires, et éventuellement à créer des sessions pour des groupes d’utilisateurs spécifiques.
source-git-commit: fc5b5afd8dd42ac3aa0e5190d6f421035df41a89
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Inscription multiple à Adobe Learning Manager

Dans Adobe Learning Manager, chaque cours peut avoir différentes instances. En tant qu’administrateur de compte, l’une de vos principales tâches consiste à créer différentes instances de sessions VILT dans différents fuseaux horaires, et éventuellement à créer des sessions pour des groupes d’utilisateurs spécifiques.

Avant la version de juillet 2023, lorsqu’un administrateur inscrivait un élève, il ne pouvait s’inscrire que dans une seule instance. Si un élève souhaitait suivre un cours dans différentes instances, l’administrateur créait de nombreux cours, un pour chaque instance.

La fonctionnalité de multi-inscription d’Adobe Learning Manager permet à un administrateur d’éviter de tels scénarios.

## Qu’est-ce que le multi-inscription ?

Les inscriptions multiples inscrivent un élève plusieurs fois dans un cours via différentes instances disponibles.  Un élève peut s’inscrire à plusieurs instances de cours, quel que soit son état d’inscription, de fin ou de démarrage. Lorsque l’auteur active l’option [!UICONTROL Inscription multiple] Activez/désactivez, un élève peut ensuite s’inscrire à plusieurs instances du cours.

![image multi-inscription](assets/multi-enrollment-author.png)
*Lancer l’inscription multiple à partir des paramètres*

La progression de chaque instance peut être suivie individuellement, et un rapport peut être exporté pour suivre la progression de chaque instance.

## Points importants

* L&#39;inscription multiple s&#39;applique uniquement lorsqu&#39;un cours comporte plusieurs instances.
* Une fois l&#39;option d&#39;inscription multiple activée et les utilisateurs inscrits à plusieurs instances, de nouvelles lignes sont créées pour chaque cours dans le rapport Relevé de notes de l&#39;élève (une ligne pour chaque instance et chaque élève)
* Si l&#39;automatisation de la création de rapports est configurée pour ne prévoir qu&#39;une seule ligne par cours, vous devez apporter les ajustements nécessaires à l&#39;automatisation de la création de rapports avant d&#39;activer la fonctionnalité Inscription multiple.

## Activation de l’inscription multiple

1. Connectez-vous à votre compte Learning Manager d’Adobe en tant qu’auteur.
1. Sélectionnez le cours auquel vous souhaitez que les élèves s’inscrivent plusieurs fois.
1. Dans le panneau de gauche, sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Modifier]** > **[!UICONTROL Configuration de l’instance]** > **[!UICONTROL Activer l’inscription multiple]**.

![image multi-inscription](assets/multi-enrollment-author.png)
*Activer les inscriptions multiples*

>[!NOTE]
>
>En tant qu’auteur, vous ne pouvez pas activer le changement d’instance et l’inscription multiple simultanément.

## Vue Élève

Les inscriptions multiples sont utiles lorsqu&#39;un élève souhaite s&#39;inscrire à un cours en salle de classe ou en classe virtuelle ou veut terminer à nouveau un cours avant de passer à un autre cours.

Pour les élèves qui ne se sont pas inscrits, lorsqu&#39;ils sélectionnent un cours, l&#39;écran sous le cours s&#39;affiche avec plusieurs instances. Ensuite, ils peuvent sélectionner chaque instance et s’inscrire.

![image vue par l’élève](assets/learner-view.png)
*Afficher les instances*

Après l’inscription dans une instance, ils peuvent s’inscrire dans d’autres instances en sélectionnant l’option Afficher toutes les instances dans le volet de droite.

![image de cours à inscriptions multiples](assets/enroll-instance.png)
*Inscription à une instance*

La progression de chaque instance peut être suivie comme suit :

![suivre la progression](assets/check-progress.png)
*Suivi de la progression de chaque instance*

## Modifications multi-inscriptions dans l’administrateur

**Inscription :**

Lors de l’inscription des élèves, vous pouvez activer la case à cocher suivante :

*« Le ou les élèves sélectionnés peuvent déjà être inscrits à d’autres instances de ce cours. Autoriser ces élèves à être également inscrits à l&#39;instance ... »*

![modifications d’administrateur](assets/admin-changes.png)
*Option d’inscription pour les administrateurs*

Si l’élève est déjà inscrit à une instance et que vous, en tant qu’administrateur, essayez de l’inscrire à une autre instance de cours, sélectionnez Oui.

## Rapports

Pour un élève inscrit à deux instances du même cours, deux lignes sont créées pour chaque instance de cours. Le rapport affiche également la progression des instances.
