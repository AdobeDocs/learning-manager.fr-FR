---
description: Ce document se compose d’une aide permettant de créer des modules de cours, des instances et des cours pour le rôle d’administrateur.
jcr-language: en_us
title: Création de modules de cours, d’instances et de programmes d’apprentissage
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '4544'
ht-degree: 0%

---



# Création de modules de cours, d’instances et de programmes d’apprentissage

Ce document se compose d’une aide permettant de créer des modules de cours, des instances et des cours pour le rôle d’administrateur.

Les auteurs créent des cours. Les élèves peuvent suivre les cours et les administrateurs peuvent suivre les performances des élèves en fonction de l&#39;utilisation des cours.

## Présentation {#overview}

Les auteurs créent des cours. Les élèves suivent ensuite les cours et les administrateurs peuvent suivre les performances des élèves en fonction de l’utilisation des cours. Les administrateurs peuvent afficher les cours créés par les auteurs et effectuer certaines activités comme expliqué dans cette section. En tant qu’administrateur, vous pouvez créer des programmes d’apprentissage uniques avec un ensemble prédéfini de cours pour les élèves.

## Création d’une instance d’un cours {#createinstanceofacourse}

Une fois qu&#39;un auteur a créé un cours, vous pouvez créer des instances du cours. En créant des instances d&#39;un cours, vous pouvez proposer le même cours à vos élèves à différentes périodes. Les élèves peuvent choisir n’importe quelle instance et s’inscrire. Vous pouvez configurer chaque instance pour qu’elle dispose de son propre ensemble de badges, de commentaires et d’autres paramètres.

Pour créer une instance :

1. Dans l’application web Administrator, cliquez sur **[!UICONTROL Cours]** dans le volet de gauche.
1. Dans la liste des cours, choisissez le cours requis, puis cliquez sur **[!UICONTROL Afficher le cours]**.

   ![](assets/view-course.png)

   *Afficher un cours*

1. Pour créer des instances, cliquez sur **[!UICONTROL Instances]** dans le volet de gauche. Chaque cours a une instance par défaut. Vous pouvez soit modifier l&#39;instance par défaut, soit ajouter des instances. Impossible de supprimer cette instance de cours.
1. Pour créer une instance, cliquez sur **[!UICONTROL Ajouter une nouvelle instance]** dans le coin supérieur droit des informations sur le cours. Une nouvelle instance du cours s&#39;affiche.
1. Entrez les propriétés de l&#39;instance :

   * Dans le panneau **[!UICONTROL Nom de l’instance]** , saisissez le nom de l&#39;instance que vous souhaitez associer au cours. Veillez à utiliser un nom unique pour l&#39;instance.
   * Spécifiez l&#39;échéance d&#39;achèvement de l&#39;instance. Les élèves doivent atteindre l&#39;état d&#39;achèvement du cours avant cette date.
   * Cliquez sur **[!UICONTROL Afficher plus d’options]** pour afficher d’autres options d’échéance.
   * **[!UICONTROL Échéance d’inscription]:** Il s&#39;agit de la date à laquelle un élève doit s&#39;inscrire à un objet d&#39;apprentissage en cas d&#39;auto-inscription.
   * **[!UICONTROL Échéance de désinscription]:** Vous pouvez choisir de restreindre la désinscription par l&#39;élève lui-même en fixant une échéance de désinscription.

   Un administrateur peut décider d&#39;imposer des échéances d&#39;achèvement pour un cours ou un programme d&#39;apprentissage en fonction des exigences. Cependant, il est recommandé d’en avoir une pour les formations en salle de classe/en salle de classe virtuelle.

   ![](assets/create-an-instance.png)

   *Définir l’échéance d’achèvement*

## Afficher les propriétés de l&#39;instance {#viewpropertiesoftheinstance}

![](assets/properties-of-aninstance.png)

*Afficher les propriétés de l&#39;instance*

1. **Modules :** Nombre de modules créés par l&#39;auteur du cours
1. **Élèves inscrits :** Nombre d’élèves inscrits au cours par l’administrateur.
1. **Sessions :** Nombre de modules de salle de classe virtuelle et de salle de classe dans le cours.
1. **Feedback activé :** Indique si les retours d&#39;informations L1, L2 et L3 sont activés pour ce cours.

## Retrait d’une instance {#retireaninstance}

Pour retirer une instance, effectuez les étapes ci-dessous ;

1. Dans l&#39;instance, cliquez sur le menu déroulant et choisissez l&#39;option **[!UICONTROL Retrait de l’instance]**.

   ![](assets/retire-an-instance.png)

   *Retrait d’une instance*

1. Pour rechercher toutes les instances retirées, cliquez sur l’onglet **[!UICONTROL Retraité]** sur la page Instances.

## Restauration d’une instance {#restoreaninstance}

Pour restaurer une instance retirée à un état activé, effectuez les étapes suivantes :

1. Dans l&#39;instance, cliquez sur le menu déroulant et choisissez l&#39;option **[!UICONTROL Rouvrir l’instance]**.

   ![](assets/restore-an-instance.png)

   *Restauration d’une instance*

1. L&#39;instance est maintenant restaurée en mode actif.

## Envoi d’e-mails au niveau de l’instance

Pour envoyer des courriers électroniques au niveau de l’instance aux élèves inscrits :

1. Dans la page Instances, sélectionnez les options d&#39;une instance, puis cliquez sur **[!UICONTROL Envoyer un e-mail aux élèves inscrits]**.

![e-mails au niveau de l’instance](assets/adhoc-email.png)

*Envoyer un courrier électronique aux élèves inscrits à l’instance*

1. Dans la boîte de dialogue Créer une annonce, sélectionnez Saisir comme e-mail. Spécifiez l’objet, saisissez le message, puis cliquez sur Enregistrer. La formation est sélectionnée automatiquement.

   ![Créer une annonce par e-mail](assets/email-announcement.png)

   *Créer une annonce par e-mail*

1. Après avoir cliqué **[!UICONTROL Enregistrer]**, un message de confirmation s&#39;affiche pour la création réussie de l&#39;annonce. Pour publier l’annonce, cliquez sur **[!UICONTROL Publier maintenant]**.

   ![Annonce créée avec succès](assets/announcement-successful.png)

### Inscription d’élèves dans différentes instances

1. Sélectionnez un cours dans la liste des cours.
1. Sélectionner **[!UICONTROL Élèves]** dans le panneau de gauche.
1. Sélectionner **[!UICONTROL S’inscrire]**.

   ![Inscription d’élèves](assets/enroll-learners-new.png)

   *Publier le cours*

1. Dans le panneau [!UICONTROL **Inscrire des élèves**] , vous pouvez :

   * Sélectionnez une instance pour inscrire un élève à partir de la liste déroulante Sélectionner une instance.
   * Sélectionnez l’utilisateur ou les groupes d’utilisateurs, ou les deux, dans le champ Inclure les élèves.
   * Sélectionnez les élèves que vous souhaitez exclure de l&#39;instance dans le champ Exclure des élèves.
   * Au bas de la boîte de dialogue, sélectionnez Oui si vous souhaitez qu&#39;un ou plusieurs élèves soient inscrits à l&#39;instance sélectionnée.

1. Sélectionner **[!UICONTROL Continuer]**.

   ![continuer](assets/proceed.png)

   *Poursuivre l&#39;inscription des élèves*

### Afficher le rapport d&#39;inscription d&#39;une instance

1. Sélectionnez un cours dans la liste des cours.
1. Sélectionner **[!UICONTROL Élèves]** dans le panneau de gauche.
1. Sélectionner **[!UICONTROL Actions]** > **[!UICONTROL Exportation]**.

Le fichier Excel contient des feuilles de calcul pour chaque instance. Une feuille de calcul se compose des champs suivants :

* Élèves
* E-mail
* ID utilisateur unique
* Nom du cours
* ID unique de l’objet d’apprentissage
* Statut
* Critères de sélection
* Date d’inscription/Date de désinscription (fuseau horaire UTC)
* Date d’achèvement (fuseau horaire UTC)
* Date d’échéance (fuseau horaire UTC)
* Date de début (fuseau horaire UTC)
* Score du quiz
* Nom du responsable
* Adresse
* userState
* Domaine d&#39;expertise
* Commentaires
* Nombre de visites
* Dates de visite
* Horodatage (fuseau horaire UTC)
* Temps passé (minutes)

>[!NOTE]
>
>Remarque : l’activation des inscriptions multiples entraîne l’ajout de plusieurs lignes au rapport du relevé de notes de l’élève pour chaque cours (une ligne pour chaque instance).
>
>Si la configuration de Reporting Automation ne prévoit qu&#39;une seule ligne par cours, vous devez effectuer les ajustements nécessaires avant d&#39;activer la fonction d&#39;inscription multiple.

## Définir le niveau d&#39;escalade {#escalation}

Pour envoyer des notifications par e-mail, un administrateur doit choisir explicitement le niveau de réaffectation pour :

* Responsable
* Responsable et ignorer le gestionnaire de niveau

![](assets/escalation-notification.png)

*Définir le niveau d&#39;escalade*

## Modération du cours {#coursemoderation}

Chaque fois qu&#39;un auteur ajoute, met à jour ou supprime des modules et republie un cours, tous les administrateurs reçoivent une notification à ce sujet. En tant qu’administrateur, vous pouvez ensuite afficher les modifications, comparer l’ancien et le nouveau contenu en cliquant sur le lien, puis approuver ou rejeter les modifications en conséquence.

Pour activer la modération de cours, cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Généralités]**. Sélectionnez l’option **[!UICONTROL Modération du cours]** case à cocher pour activer cette fonctionnalité.

![](assets/2.png)

*Activer la modération de cours*

Cliquez sur la notification pour afficher les modifications que l’auteur a apportées au cours. Ensuite, approuvez ou rejetez les modifications apportées par l’auteur. Si vous choisissez d’approuver, le cours sera republié. Si vous rejetez les mises à jour, la version précédente du cours continuera d&#39;exister. Dans les deux cas, une notification est envoyée à l’auteur.

![](assets/1.png)

*Demandes de l’auteur pour les mises à jour de cours*

Si plusieurs auteurs mettent à jour le même cours, la dernière modification effectuée s&#39;affichera dans la notification de l&#39;administrateur. Vous pouvez ensuite approuver ou rejeter les dernières modifications.

## Ajouter des commentaires L1 et L3 {#addl1andl3feedback}

Vous pouvez ajouter des options de retour d&#39;informations L1 et L3 lors de la création des cours :

1. Cliquez sur Cours dans le volet de gauche après vous être connecté en tant qu&#39;administrateur. La liste de tous les cours s’affiche sur la page de droite.
1. Cliquez sur la vignette du cours pour lequel vous souhaitez ajouter un retour d&#39;informations L1 ou L3
1. Cliquez sur la valeur d&#39;instance par défaut dans le volet de gauche.
1. Cliquez sur le cercle du bouton bascule en regard du retour d&#39;informations L1 ou L3 pour l&#39;activer.
1. Ajoutez la question de retour d&#39;informations L3 dans la zone de texte située sous Question L3.

## Retour d&#39;informations L1 obligatoire {#mandatory-l1-feedback}

Vous pouvez rendre obligatoires toutes les questions ou la première question d&#39;un retour d&#39;informations L1.

![](assets/make-all-questionsmandatory.png)

*Rendre obligatoires toutes les questions ou la première question d&#39;un retour d&#39;informations L1*

Maintenant, vous pouvez créer les questions, qui deviennent maintenant obligatoires.

![](assets/create-mandatoryquestions.png)

*Création des questions*

Si les deux questions obligatoires, pour une raison quelconque, n’ont pas de texte, les questions n’apparaîtront pas dans le formulaire de retour d’informations.

>[!NOTE]
>
>Il ne suffit pas d&#39;activer ces paramètres dans l&#39;instance du programme d&#39;apprentissage. Vous devez également activer ces paramètres au niveau de l’instance de cours pour chaque cours du programme d’apprentissage.

Dans la page Valeurs par défaut de l’instance, si vous activez **[!UICONTROL Rendre toutes les questions obligatoires]**, toutes les nouvelles instances créées par la suite hériteront de ces paramètres.

![](assets/instance-defaults-makeallquestionsmandatory.png)

*Affichage de la page Valeurs par défaut de l’instance*

## Retour d’informations L1 au niveau du cours {#l1-feedback-course-level}

Dans les versions précédentes de Learning Manager, un administrateur pouvait activer le retour d’informations L1 pour le programme d’apprentissage.

Dans cette version de Learning Manager, l&#39;administrateur peut envoyer un retour d&#39;informations L1 pour tous les cours qui font partie du programme d&#39;apprentissage. L&#39;administrateur doit s&#39;assurer que le retour d&#39;informations L1 est activé pour tous les cours au niveau de l&#39;instance de cours.

1. Pour activer le retour d’informations L1 pour chaque cours, dans l’application d’administration, cliquez sur **[!UICONTROL Programmes d’apprentissage]** > **[!UICONTROL Afficher le programme d’apprentissage]**.

1. Cliquez sur **[!UICONTROL Instances]** > **[!UICONTROL Retour d&#39;informations L1 activé]**.

1. Activer l’option **[!UICONTROL Activer pour chaque cours]**.

   ![](assets/enable-l1-feedbackforcourse.png)

   *Activer le retour d’informations sur le cours*

   Seule l’activation de cette option au niveau du programme d’apprentissage ne déclenchera pas le retour d’informations L1 pour les cours de ce programme. Pour activer le retour d&#39;informations L1, accédez à chaque cours du programme d&#39;apprentissage et activez le bouton Retour d&#39;informations L1.

   ![](assets/l1-reaction-feedback.png)

   *Activer le retour d&#39;informations L1 pour chaque cours*

   Si le retour d&#39;informations L1 est activé pour tous les cours, mais désactivé dans l&#39;instance du programme d&#39;apprentissage, le retour d&#39;informations L1 ne sera pas déclenché pour les cours.

## Rapports de quiz spécifiques à la langue

Les rapports de quiz permettent d&#39;évaluer les performances d&#39;un élève après la fin d&#39;un programme d&#39;apprentissage ou d&#39;un cours.

Learning Manager facilite actuellement l’apprentissage dans 13 langues d’interface et 32 langues de contenu. Bien que cette option soit conviviale pour les élèves et soit pratique pour prendre en charge nos élèves globaux, il est difficile pour les administrateurs d’extraire les rapports tentés dans diverses langues.

Les rapports de quiz affichent les données dans différentes langues, à condition que le cours soit proposé en plusieurs langues. Jusqu’à présent, les réponses étaient affichées l’une après l’autre dans les rapports générés par l’administrateur, quelle que soit la langue dans laquelle le quiz était tenté. **Par exemple**, si un utilisateur a répondu à un quiz en néerlandais, l’administrateur ne pourra afficher que les rapports de quiz tentés par des utilisateurs en néerlandais à la fois. L’administrateur qui a sélectionné l’anglais comme langue d’interface n’a pas pu afficher les rapports pour tous les utilisateurs à la fois, indépendamment des paramètres régionaux tentés dans.

Cela est maintenant corrigé, car l’administrateur peut désormais afficher tous les rapports dans la langue respective que l’élève a tenté tous en même temps, indépendamment de la langue de contenu choisie. Le quiz tenté dans différentes langues sera ajouté en tant que colonnes supplémentaires dans le rapport de quiz.

## Activer le retour d&#39;informations L1 au niveau du compte {#l1-feedback-account-level}

*Activer le retour d&#39;informations L1 au niveau du compte*

Un administrateur pourra activer le retour d’informations L1 pour les cours et le programme d’apprentissage nouvellement créés en activant ce paramètre au niveau du compte. Toutefois, l’activation de ce paramètre n’a aucune incidence sur les cours et programmes d’apprentissage existants

Si cette option est activée, le retour d’informations sera activé par défaut pour toutes les nouvelles formations et toutes les nouvelles instances. Si un auteur/administrateur visite l’instance, celle-ci est définie par défaut et désactivée manuellement, puis elle est respectée.

Pour activer le retour d&#39;informations L1, dans l&#39;application d&#39;administration, cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Commentaires]**.

![](assets/l1-feedback-settings.png)

*Affichage de la page Paramètres de retour d’informations*

Cliquez sur **[!UICONTROL Modifier]** dans le coin supérieur droit et activez l&#39;option pour activer le retour d&#39;informations L1.

Lorsqu&#39;un auteur crée un cours, sur la page Instance de l&#39;application d&#39;administration, le **[!UICONTROL Retour d&#39;informations L1]** est automatiquement activé pour le nouveau cours.

<!--![](assets/l1-feedback-enabled.png)-->

Vous pouvez également désactiver le retour d&#39;informations L1 en activant la case à cocher **[!UICONTROL Activer]** comme indiqué ci-dessous :

![](assets/disable-l1-feedback.png)

*Activation ou désactivation du retour d&#39;informations L1*

## Ajout de questions descriptives pour le retour d&#39;informations L1 et L3 {#descriptive}

Dans la version de novembre de Learning Manager, une option permettant d&#39;ajouter des questions descriptives a été ajoutée. Les administrateurs ont la possibilité d’ajouter ces questions aux élèves. Cette fonctionnalité vient s’ajouter à l’ensemble de questions par défaut fournies par Learning Manager. Vous pouvez également les rendre obligatoires si nécessaire en sélectionnant l’option sous la question.

Vous pouvez ajouter deux questions descriptives pour le retour d&#39;informations L1 et une pour le retour d&#39;informations L3.

Une fois que vous avez activé le retour d&#39;informations L1, vous pouvez afficher les options comme illustré dans l&#39;instantané suivant.

![](assets/l1-feedback-desc-questions.png)

*Ajout de questions descriptives pour le retour d&#39;informations L1 et L3*

Si vous souhaitez que le questionnaire apparaisse à l’élève immédiatement après la fin du cours, vous pouvez choisir l’option en conséquence.

Un exemple de sortie du questionnaire L1 est fourni ci-dessous à titre de référence. Les élèves peuvent afficher le questionnaire dans le format ci-dessous. Test-1 et Test-2 sont les questions descriptives.

![](assets/l1-output.png)

*Exemple de questions de retour d’informations sur un cours*

Une fois que vous avez activé le retour d&#39;informations L3, vous pouvez afficher les options comme indiqué dans l&#39;instantané ci-dessous :

![](assets/l3-feedback-desc-questions.png)

*Activer le retour d&#39;informations L3*

Question 2 est la question descriptive pour le retour d&#39;informations L3. Vous pouvez la rendre obligatoire en cliquant sur l’option correspondante sous la question.

Un exemple de sortie du questionnaire L3 est fourni ci-dessous à titre de référence. Les élèves peuvent afficher le questionnaire dans le format ci-dessous.

![](assets/l3-output.png)

*Afficher la sortie du retour d’informations L3*

## Configurer le questionnaire de retour d&#39;informations L1 et L3 {#setupl1andl3feedbackquestionnaire}

Vous pouvez configurer un questionnaire de retour d’informations L1 et L3 et également définir des rappels au niveau du compte.

1. Cliquez sur **[!UICONTROL Paramètres]** et ensuite **[!UICONTROL Commentaires]** dans le volet de gauche après vous être connecté en tant qu’administrateur.\
   La page Paramètres de retour d’informations s’affiche avec deux onglets : **[!UICONTROL Retour d&#39;informations L1]** et **[!UICONTROL Retour d&#39;informations L3]**.\
   **[!UICONTROL Retour d&#39;informations L1]** se compose d’une liste de valeurs par défaut **[!UICONTROL Retour d&#39;informations L1]** questionnaire pour les cours en salle de classe et en auto-apprentissage, avec paramètres de rappel. Entrée **[!UICONTROL Retour d&#39;informations L3]** , vous pouvez afficher la déclaration par défaut du retour d&#39;informations L3 et les paramètres de rappel.

1. Cliquez sur Modifier dans le coin supérieur droit de la page pour modifier le questionnaire existant.\
   Entrée **[!UICONTROL Retour d&#39;informations L1]** , vous pouvez activer/désactiver chaque question en cliquant sur le bouton bascule Oui/Non.\
   Entrée **[!UICONTROL Retour d&#39;informations L3]** , vous pouvez modifier la déclaration de retour d&#39;informations par défaut.\
   Cliquez sur **[!UICONTROL Ajouter un nouveau rappel]** au bas de la page et choisissez quand envoyer les rappels.

1. Cliquez sur **[!UICONTROL Enregistrer]** dans le coin supérieur droit de la page.

Dans Retour d&#39;informations L1, vous pouvez voir deux ensembles de questionnaires accompagnés d&#39;une question par défaut. Le premier ensemble de questionnaires fait référence aux cours en auto-apprentissage qui peuvent également être utilisés pour des cours basés sur l&#39;activité. Un deuxième ensemble de questionnaires peut être utilisé pour les cours en salle de classe et en salle de classe virtuelle.

## Exporter les données de liste de contrôle {#export-checklist-data}

Dans la liste des cours, ouvrez un cours contenant une liste de contrôle. Dans le volet de gauche, une option s’affiche **[!UICONTROL Liste de contrôle]**.

![](assets/export-checklist.png)

*Exporter les données de liste de contrôle*

Cliquez sur l&#39;option puis, sur la page du cours, effectuez les opérations suivantes :

1. Sélectionnez l&#39;instance et le module.
1. Cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Exportation]**, puis exportez le rapport de liste de contrôle de l’élève.

Sur la **[!UICONTROL Liste de contrôle]** , un instructeur peut exporter le rapport de liste de contrôle à partir de **[!UICONTROL Actions]** liste déroulante.

Le rapport CSV contient les champs suivants :

* Nom d’utilisateur
* Adresse e-mail de l’utilisateur
* Nom et adresse e-mail du responsable
* Nom de la formation
* Instance de formation
* Nom et adresse électronique de l’instructeur
* Envoyé le
* Statut d&#39;évaluation
* Questions-avec texte réel
* État de l’utilisateur
* Profil
* Champ(s) actif(s)

Lorsque vous téléchargez un rapport après avoir sélectionné un filtre d’état, le rapport sur le relevé de notes de l’élève téléchargé contient les données de l’élève en fonction du filtre d’état appliqué. Ce filtre ajouté s’affiche également à l’administrateur et au responsable personnalisés lorsqu’ils sont sur le point de générer un relevé de notes de l’élève.

## Affichage des cours {#viewingcourses}

En tant qu’administrateur, vous pouvez afficher une liste de tous les cours disponibles.   Cliquez sur **[!UICONTROL Cours]** dans le volet de gauche pour afficher la liste des cours avec les options de recherche et de filtre. Vous pouvez également afficher le pourcentage d&#39;efficacité de cours pour chaque cours sur les vignettes de cours.

>[!NOTE]
>
>Vous pouvez retirer un cours après que le cours a été suivi par les élèves ou lorsque vous souhaitez retarder un cours particulier après l’avoir publié. Vous ne pouvez retirer un cours que s&#39;il est publié. La liste de tous les cours retirés peut être visualisée en cliquant sur le bouton **[!UICONTROL Retraité]** onglet.

## Afficher les scores du quiz {#viewquizscores}

1. Cliquez sur le nom du cours sur la vignette du cours.
1. Cliquez sur Score du quiz dans le volet de gauche.

Vous pouvez afficher les scores du quiz d&#39;un cours particulier en fonction du nom d&#39;utilisateur ou de chaque question. Sélectionnez les onglets Par utilisateur ou Par question en conséquence.

Choisissez le type d&#39;instance dans la liste déroulante pour afficher les scores en fonction de chaque instance du cours.

## Gérer la liste des élèves pour un cours {#managelearnerslistforacourse}

1. Cliquez sur le nom du cours sur la vignette du cours.
1. Dans le volet de gauche, cliquez sur **[!UICONTROL Élèves]**.

![](assets/courses-learners.png)

*Sélectionner des élèves dans un cours*

Vous pouvez effectuer les actions suivantes à partir de la page Élèves :

* Sélectionnez l’élève à supprimer, puis cliquez sur [!UICONTROL **Actions**] > [!UICONTROL **Supprimer**].
* Sélectionnez l’élève dont vous souhaitez marquer l’assiduité, puis cliquez sur [!UICONTROL **Actions**] > [!UICONTROL **Marquer comme terminé**].

Pour permettre aux élèves de réinitialiser un module et de l’utiliser à nouveau, cliquez sur [!UICONTROL **Réinitialiser**]. Dans la boîte de dialogue contextuelle, cliquez sur Oui pour confirmer la réinitialisation. Impossible de réinitialiser les modules terminés. Seuls les modules ayant échoué ou incomplets peuvent être réinitialisés.

Vous pouvez également exporter la liste des élèves dans une feuille Excel. Pour exporter la liste des élèves, cliquez sur [!UICONTROL **Actions**] > [!UICONTROL **Exportation**].

>[!NOTE]
>
>S&#39;il existe plusieurs instances d&#39;un cours, la liste des élèves dans Excel est fournie dans chaque onglet séparément. La liste des élèves comprend le nom de l&#39;élève, son statut et les critères de sélection. Le statut des élèves peut être **Non démarré** ou **En cours** ou **Terminé**.

## Exporter la présence des élèves {#attendance}

Pour n’importe quelle classe et n’importe quel cours VC, vous pouvez télécharger la liste des élèves qui ont suivi ce cours, par exemple.

Sur la page de détails du cours, cliquez sur **[!UICONTROL Présence et notation]** dans le volet de droite.

Dans le coin supérieur droit de la page, cliquez sur le bouton **[!UICONTROL Actions]** liste déroulante. Cliquez ensuite sur l’option **[!UICONTROL Exporter la liste des élèves (PDF)]**.

![](assets/export-list-of-learners.png)

*Exporter la liste des élèves en tant que PDF*

Dans le PDF, vous pouvez afficher le même ensemble d’élèves qu’un instructeur.

Lorsque vous téléchargez le PDF, vous pouvez voir le fuseau horaire (en UTC) qui a été utilisé lors de la création du cours.

## Exporter les élèves dans l&#39;état d&#39;approbation en attente

Un administrateur, un responsable ou un administrateur personnalisé peut exporter les données des élèves qui sont en attente d&#39;inscription à l&#39;approbation. Vous pouvez exporter les données via **Cours > Élève** , puis cliquez sur la liste déroulante Action.

L’option sera présente lorsqu’aucun élève n’est inscrit/en attente d’approbation du cours approuvé par le responsable et un rapport vide sera généré. Vous pouvez également exporter lorsque les élèves sont dans l&#39;état d&#39;approbation en attente, l&#39;état inscrit, l&#39;état en attente et l&#39;état non inscrit.

Le rapport contient les données des utilisateurs actifs, supprimés et suspendus s&#39;ils sont en attente d&#39;approbation. Le rapport contient également les données des utilisateurs internes et externes, qui sont en attente d&#39;approbation.

Si un élève qui se trouvait auparavant dans l&#39;état d&#39;approbation en attente se désinscrit, son enregistrement ne sera pas présent dans le rapport. En outre, si un élève qui se trouvait auparavant dans l&#39;état d&#39;approbation en attente est inscrit au cours par inscription d&#39;administrateur/de responsable/d&#39;administrateur personnalisé, son enregistrement est présent dans le rapport.

## Afficher le retour d&#39;informations L1 et L3 {#viewl1andl3feedback}

Vous pouvez afficher le retour d&#39;informations L1 fourni par les élèves pour un cours et le retour d&#39;informations L3 fourni par les responsables pour les élèves.

1. Cliquez sur n&#39;importe quelle vignette de cours dans la liste Cours.
1. Cliquez sur Retour d&#39;informations L1 ou Retour d&#39;informations L3 dans le volet de gauche pour afficher le retour d&#39;informations reçu.
1. Sélectionnez l&#39;instance dans la liste déroulante pour afficher le retour d&#39;informations pour cette instance particulière.

## Aperçu des cours {#previewcourses}

L&#39;administrateur peut prévisualiser les cours en cliquant sur **[!UICONTROL Aperçu en tant qu’élève]** lors de l&#39;affichage des modules de cours.

1. Cliquez sur **[!UICONTROL Cours]** dans le volet de gauche après vous être connecté en tant qu’administrateur.
1. Cliquez sur une vignette de cours dans la liste des cours de la page.
1. Cliquez sur Aperçu en tant qu&#39;élève dans le volet de gauche et cliquez sur le nom du module sur la page pour prévisualiser le module de cours dans le lecteur.

## Efficacité du cours {#courseeffectiveness}

L’efficacité du cours est évaluée pour comprendre l’utilité d’un cours pour l’élève. Il s’agit d’une combinaison des résultats des retours d’informations de l’élève sur le contenu du cours, des résultats du quiz de cours pour un élève et du retour d’informations du responsable évaluant un élève en fonction des apprentissages du cours.

L&#39;administrateur peut afficher l&#39;évaluation de l&#39;efficacité des cours sur les vignettes de cours comme indiqué dans l&#39;instantané ci-dessous. L&#39;évaluation de ce cours est de 100.

<!--![](assets/course-effectiveness-tag1.png)-->

La valeur d&#39;évaluation de l&#39;efficacité du cours est obtenue en tenant compte des valeurs de retour d&#39;informations L1, L2 et L3. Pour afficher la répartition de chaque retour d&#39;informations, cliquez sur la valeur d&#39;efficacité du cours. Une fenêtre contextuelle s’affiche, comme illustré ci-dessous.

![](assets/course-effectiveness.png)

*Afficher l&#39;efficacité des cours pour les retours d&#39;informations L1, L2 et L3*

Dans cet exemple, 1 utilisateur sur 1 a reçu les trois retours d’informations, le score est donc de 100/100. À partir de ce tableau, vous pouvez comprendre que si l&#39;un des trois retours d&#39;informations (L1, L2 et L3) n&#39;est pas fourni pour un cours, il y a un impact négatif sur l&#39;efficacité globale. Cliquez sur la flèche vers le bas dans le coin inférieur droit de la fenêtre contextuelle pour afficher comment les calculs d&#39;efficacité de cours sont effectués.

![](assets/course-effectiveness-calculations.png)

*Calcul de l&#39;efficacité du cours*

Comme indiqué dans le graphique circulaire ci-dessus, le retour d’informations L3 du responsable est davantage pondéré.

## Recherche de cours et de programmes d&#39;apprentissage {#searchingcoursesandlearningprograms}

Adobe Learning Manager facilite la recherche rapide des cours/programmes d’apprentissage de votre choix. Vous pouvez rechercher vos cours de deux manières :

1. À l’aide du champ Rechercher. Cliquez sur l’icône de recherche affichée dans le coin supérieur droit. Un champ de recherche s’affiche. Saisissez le nom du cours ou tout mot-clé associé à vos cours pour localiser vos cours/programmes d&#39;apprentissage. Vous pouvez également effectuer une recherche à l’aide de balises prédéfinies telles que Captivate, C, Java et HTML. Les balises sont indexées dans le champ de recherche, ce qui signifie que les balises sont affichées dans le champ de recherche lors de la saisie.
1. En filtrant la liste des cours/programmes d’apprentissage à l’aide des filtres. Vous pouvez filtrer les cours par état, par exemple Tous, Publié, Brouillon et Retiré. En mode Administrateur, le filtre Brouillon ne s’affiche pas.

Vous pouvez effectuer une recherche en fonction des compétences en cliquant sur Compétences et en les sélectionnant. En tant qu’administrateur, vous pouvez trier les cours de quatre manières, afin de mieux localiser le cours requis. Cliquez sur Trier par et choisissez l’ordre croissant alphabétique, l’ordre décroissant alphabétique, la date de mise à jour du cours ou l’efficacité des cours.

<!--![](assets/admin-sortby.png)-->

Vous pouvez trier les programmes d&#39;apprentissage de trois manières : ordre croissant alphabétique, ordre décroissant alphabétique et en fonction de la date de mise à jour.

## Inscription d’élèves {#enrollinglearners}

Vous pouvez suivre les mêmes étapes pour inscrire des élèves à un cours, à un programme d&#39;apprentissage et à des certifications. Les responsables peuvent également inscrire des élèves en dessous de lui en procédant comme suit.

L’administrateur inscrit certains élèves à des cours obligatoires en fonction des exigences de l’organisation :

1. Placez le curseur de la souris sur les vignettes de cours publiées et cliquez sur Inscrire des élèves.\
   Vous pouvez également cliquer sur une vignette de cours publié et cliquer sur Élèves dans le volet de gauche. Une page s’affiche avec une liste d’élèves. Cliquez sur S’inscrire.\
   La boîte de dialogue Inscrire des élèves s&#39;affiche.

1. Sélectionnez l&#39;instance dans la liste déroulante Sélectionner une instance. La liste déroulante répertorie toutes les instances, y compris les instances actives, retirées et expirées.

>[!NOTE]
>
>L’administrateur peut supprimer tous les élèves inscrits à un cours en cliquant sur la flèche déroulante de la page des élèves et en cliquant sur **[!UICONTROL Actions]** > **[!UICONTROL Supprimer]**.

![](assets/enroll-learners.png)

*Ajouter des commentaires lors de l’inscription des élèves*

*Inscription d’élèves*

## Utilisateurs

+++Inclure les élèves

Sélectionnez les groupes d&#39;utilisateurs et les élèves individuels (à l&#39;aide de l&#39;ID ou du nom de messagerie) que vous souhaitez inclure. Ajoutez tous les groupes d&#39;utilisateurs dans une intersection sous le même ensemble. Pour ajouter un autre groupe d&#39;utilisateurs dans l&#39;union, utilisez un nouveau jeu d&#39;inclusion.

+++

+++Exclure des élèves

Sélectionnez les groupes d&#39;utilisateurs et les élèves individuels (à l&#39;aide de l&#39;ID ou du nom de messagerie) que vous souhaitez exclure. Ajoutez tous les groupes d&#39;utilisateurs dans une intersection sous le même ensemble. Pour ajouter un autre groupe d&#39;utilisateurs dans une union, utilisez un nouveau jeu d&#39;inclusion.

+++

## ID d’e-mail de l’utilisateur

+++ID d’e-mail

Copiez-collez les ID de messagerie des élèves auxquels vous souhaitez vous inscrire, séparés par des points-virgules, des virgules ou un interligne. Utilisez la commande **[!UICONTROL Valider les ID de messagerie]** pour valider les entrées. Toutes les entrées non valides s’affichent en rouge. Supprimez ou corrigez ces entrées et continuez en cliquant sur **[!UICONTROL Continuer.]**

![](assets/email-id-option.png)

*Inscription d’élèves*

La boîte de dialogue Résumé affiche le nombre d&#39;utilisateurs du jeu d&#39;inclusion, du jeu d&#39;exclusion et le nombre d&#39;utilisateurs déjà inscrits à l&#39;instance de cours.

+++

### Ajouter des commentaires lors de l’inscription des élèves {#enroll-comments}

<!---![](assets/enroll-learners-dialog.png)-->

En tant qu&#39;administrateur ou responsable, vous pouvez ajouter des commentaires lors de l&#39;inscription d&#39;élèves à un cours. Vous pouvez mentionner des informations supplémentaires sur la cohorte d’utilisateurs qui s’inscrivent. Ces données sont exportées dans les rapports de cours.

Le commentaire est **non** s’affiche pour l’élève.

Lorsqu&#39;un administrateur génère le rapport de cours de l&#39;élève, tout commentaire, s&#39;il est ajouté, apparaît dans le rapport. La boîte de dialogue Résumé affiche le nombre d&#39;utilisateurs du jeu d&#39;inclusion, du jeu d&#39;exclusion et le nombre d&#39;utilisateurs déjà inscrits à l&#39;instance de cours.

Sur la **[!UICONTROL Inscrire des élèves]** boîte de dialogue, développer l’option **[!UICONTROL Options avancées]**. Dans le panneau **[!UICONTROL Commentaire supplémentaire]** champ, saisissez le commentaire requis.

![](assets/comment-for-learner.png)

*Ajouter des commentaires pour les élèves*

## Recherche d’utilisateurs inscrits {#searchforusers}

Recherchez les utilisateurs inscrits dans la section Élève de l&#39;objet d&#39;apprentissage à l&#39;aide de la recherche par frappe anticipée. En utilisant la recherche par frappe anticipée, vous pouvez rechercher progressivement des utilisateurs inscrits en utilisant le nom, l’ID de messagerie et l’uuid.

![](assets/typeahead.gif)

*Procédure pas à pas pour rechercher des utilisateurs inscrits*

Ce type de recherche est également parfois appelé saisie semi-automatique, recherche incrémentielle, recherche lors de la saisie, recherche intégrée ou recherche instantanée.

Lorsque vous recherchez un élève ou un groupe d&#39;utilisateurs dans le champ de recherche, une ou plusieurs correspondances pour le(s) terme(s) de recherche sont trouvées et vous sont immédiatement présentées.

Le processus vous permet de trouver ce que vous recherchez d&#39;une manière beaucoup plus rapide et moins lourde que d&#39;exécuter un certain nombre de recherches consécutives.

Les élèves ou groupes d’utilisateurs de toutes les instances s’affichent après une recherche. Pour chaque élève, l’instance dans laquelle il est inscrit s’affiche dans le **[!UICONTROL Instance]** colonne.

![](assets/search-result.png)

*Afficher les résultats de la recherche*

En utilisant la recherche par frappe anticipée, vous pouvez :

* Affichez tous les utilisateurs inscrits, indépendamment des instances.
* Affichez tous les groupes d’utilisateurs qui ont un ou plusieurs utilisateurs inscrits.

Une fois la recherche exécutée, vous ne pouvez pas filtrer les élèves par instances. Option permettant de sélectionner une instance dans le panneau **[!UICONTROL Sélectionner une instance]** la liste déroulante est désactivée.

En outre, à l’aide des résultats de la recherche, vous pouvez choisir un élève ou un groupe d’utilisateurs et effectuer les actions suivantes :

* Se désinscrire
* Marquer comme terminé
* Réinitialiser le module

Lors d&#39;une recherche, l&#39;option Désinscrire > En bloc dans la liste déroulante Actions est désactivée pour le cours/programme d&#39;apprentissage.

## Partager le code QR avec les élèves pour inscription, achèvement ou les deux {#shareqrcodewithlearnerstoenrollcompleteorboth}

Les administrateurs d’Adobe Learning Manager peuvent partager les codes QR avec les élèves pour s’inscrire rapidement au cours. Les trois codes QR différents sont utilisés pour marquer l&#39;inscription, l&#39;achèvement ou l&#39;inscription et l&#39;achèvement d&#39;un cours.

Les élèves peuvent simplement utiliser l&#39;application pour appareil Learning Manager d&#39;Adobe pour numériser le code QR correspondant.

**Pour télécharger le code QR, procédez comme suit :**:

1. Cliquez sur **[!UICONTROL Cours]** dans la section Apprentissage du panneau de navigation de gauche.
1. Sélectionner un cours > **[!UICONTROL Afficher le cours]**.
1. Cliquez sur **[!UICONTROL Instances]** > **[!UICONTROL Plus]** > **[!UICONTROL code QR]**.

   <!--![](assets/admin-instance-edit.png)-->

1. Activez le code QR, puis cliquez sur les icônes de téléchargement « S’inscrire », « Terminé » et « S’inscrire et terminer » pour télécharger un fichier PDF contenant le code QR pour chacun d’eux. L’administrateur peut ensuite partager le code QR avec les élèves.

   ![](assets/qr-code-download-01.png)

   *Partager le code QR avec les élèves*

## Cycle de vie du cours {#courselifecycle}

Un cycle de vie de cours typique se présente comme suit :

**Brouillon** - Lorsqu&#39;un auteur termine la création d&#39;un cours et l&#39;enregistre. À ce stade, le cours n’est pas encore disponible pour les élèves. Vous pouvez supprimer un cours à cet état.

**Publié** - Lorsqu&#39;un auteur termine la publication d&#39;un cours. À ce stade, le cours est disponible pour que les élèves s’y inscrivent.

**Retraité** - Après la publication d&#39;un cours, un auteur peut le passer au stade retiré s&#39;il ne veut pas que le cours apparaisse dans le catalogue de cours pour les élèves. Vous pouvez republier ou supprimer un cours à cet état.

**Supprimé** Adobe - Un cours est à l’état Supprimé lorsqu’il a été complètement supprimé de l’application Learning Manager. Les cours peuvent être supprimés par des auteurs uniquement lorsqu’ils sont à l’état de brouillon. Vous pouvez également supprimer des cours de l&#39;état retiré.

![](assets/lifecycle-03.png)

*Workflow du cycle de vie d&#39;un cours*

## Paramètres de notification {#notificationsettings}

En tant qu’administrateur, vous pouvez ajuster les paramètres de notification. Pour plus d’informations, voir [Notifications.](user-notifications.md)

## Foire aux questions {#frequentlyaskedquestions}

+++Comment réinitialiser le module en tant qu’administrateur ?

Sur la page Élèves d’un cours, sélectionnez l’élève ou les élèves ou un groupe, puis cliquez sur **[!UICONTROL Actions]** > **[!UICONTROL Réinitialiser les modules]**.

![](assets/reset-modules.png)

*Option d’affichage pour réinitialiser les modules*

Après avoir cliqué sur l&#39;option, l&#39;état des modules de tous les élèves sélectionnés sera réinitialisé. Les modules terminés ne seront pas réinitialisés.

+++

+++Comment ajouter l’URL du cours afin que les élèves soient redirigés directement vers le cours ?

Placez le curseur sur une carte de cours et cliquez sur **[!UICONTROL Copier l’URL]**. Après avoir copié l’URL, les élèves peuvent accéder au cours directement avec l’URL.

+++

+++Comment rouvrir une instance ?

Pour rouvrir une instance retirée, cliquez sur le menu déroulant de l&#39;instance, puis cliquez sur **[!UICONTROL Rouvrir l’instance]**.

+++
