---
description: En savoir plus sur la création de formulaires de retour d’informations L1 pour les élèves
jcr-language: en_us
title: Formulaire de retour d'informations L1
source-git-commit: 13efc4d72ac56cecf6313dbda28a3853fc3b5498
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---


# Formulaire de retour d&#39;informations L1

>[!IMPORTANT]
>
>La fonctionnalité de retour d’informations L1 améliorée est déployée pour certains clients. Si vous ne voyez pas cette fonctionnalité dans votre compte, consultez [Ajouter un retour d&#39;informations L1 et L3](/help/migrated/administrators/feature-summary/courses.md#add-l1-and-l3-feedback) pour en savoir plus sur la fonctionnalité de retour d&#39;informations existante.
>
>Contactez votre équipe Customer Success Manager (CSM) pour activer le nouveau système de commentaires et en savoir plus sur le calendrier de migration.

La fonction de retour d’informations de niveau 1 (L1) de Adobe Learning Manager permet aux élèves de partager leurs commentaires après avoir suivi un cours ou suivi un parcours d’apprentissage. Ce retour d’informations aide les administrateurs à évaluer la qualité du cours, l’efficacité des instructeurs et l’expérience d’apprentissage globale.

Les administrateurs peuvent désormais créer et gérer plusieurs formulaires de commentaires réutilisables et les affecter à des cours et parcours d’apprentissage spécifiques.

La fonctionnalité offre une plus grande flexibilité en permettant aux administrateurs de :

* Création de formulaires de commentaires réutilisables
* Personnaliser les commentaires pour différents cours ou parcours d’apprentissage
* Attribuez des formulaires personnalisés selon vos besoins

Le **[!UICONTROL rapport de retour d&#39;informations L1]** et le **[!UICONTROL rapport de retour d&#39;informations]** (rapport personnalisé) incluent désormais deux nouvelles colonnes : Nom du formulaire de retour d&#39;informations et Version du retour d&#39;informations. Ces colonnes fournissent des détails sur les formulaires de retour d’informations utilisés.

## Créer un formulaire de retour d&#39;informations L1

Les administrateurs peuvent créer plusieurs formulaires de retour d’informations L1 au niveau du compte et affecter le bon formulaire à un cours, un parcours d’apprentissage ou une certification.

Pour créer un formulaire de retour d&#39;informations L1 :

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **[!UICONTROL Formulaires de commentaires]**.

   ![](assets/feedback-form.png)
   _Page d’accueil de l’administrateur affichant l’option Formulaires de commentaires pour créer et gérer les formulaires de commentaires_
3. Sélectionnez **[!UICONTROL Ajouter un formulaire]**.

   ![](assets/add-form.png)
   _Écran Formulaires de commentaires affichant le bouton Ajouter un formulaire pour créer les formulaires de commentaires_
4. Choisissez la **[!UICONTROL langue du modèle par défaut]**, puis sélectionnez **[!UICONTROL Enregistrer]**.

   ![](assets/default.png)
   _Ajouter une invite de nouveau modèle affichant l&#39;option permettant de sélectionner la langue par défaut_
5. Saisissez le titre et la description du formulaire.

   ![](assets/field-name.png)
   _Page Ajouter un formulaire de commentaires affichant l’option saisir le titre du formulaire et la description du formulaire_
6. Dans le menu **[!UICONTROL Ajouter une question]**, sélectionnez un type de question parmi les suivants :

   a. **[!UICONTROL Texte gratuit]** : permet aux élèves de fournir des réponses dans leurs propres mots.

   * Saisissez votre question dans le champ de texte **[!UICONTROL Question]**.
   * Pour rendre la question obligatoire, sélectionnez l&#39;option **[!UICONTROL Obligatoire]**.
     ![](assets/free-text.png)
     _Ajouter une question en texte libre au formulaire de retour d&#39;informations_

   b. **[!UICONTROL Échelle numérique/NPS]** : les élèves peuvent évaluer leur satisfaction vis-à-vis du cours ou leur probabilité de recommander le cours à l&#39;aide d&#39;une échelle numérique (généralement de 1 à 10).

   * Saisissez votre question dans le champ de texte **[!UICONTROL Question]**.
   * Sélectionnez la plage d’évaluation (1 à 10).
   * Pour rendre la question obligatoire, sélectionnez l&#39;option **[!UICONTROL Obligatoire]**.
     ![](assets/numerical.png)\
     _Ajouter une question Échelle numérique/NPS au formulaire de retour d&#39;informations_

   c. **[!UICONTROL Échelle de Likert]** : les élèves peuvent spécifier dans quelle mesure ils sont d&#39;accord avec une instruction, de Fortement en désaccord à Fortement en accord.

   * Saisissez votre question dans le champ de texte **[!UICONTROL Question]**.
   * Pour rendre la question obligatoire, sélectionnez l&#39;option **[!UICONTROL Obligatoire]**.
     ![](assets/likert.png)
     _Ajouter une question Échelle de Likert au formulaire de retour d&#39;informations_

   d. **[!UICONTROL Score d&#39;efficacité du cours]** : échelle permettant de mesurer l&#39;efficacité avec laquelle un cours influence les élèves, à l&#39;aide d&#39;un système d&#39;évaluation relatif.

   * Une question prédéfinie avec une échelle de Likert de 1 à 10 sera ajoutée au formulaire de retour d’informations.
   * Vous ne pouvez ajouter qu&#39;une seule question **[!UICONTROL Score d&#39;efficacité du cours]** et elle ne peut pas être modifiée
     ![](assets/course-effective.png)
     _Ajout d&#39;une question sur le score d&#39;efficacité du cours au formulaire de retour d&#39;informations_
7. Sélectionnez **[!UICONTROL Enregistrer]**. Vous pouvez afficher les formulaires créés dans la section Forms des commentaires.

### Aperçu du formulaire de retour d’informations

Vous pouvez prévisualiser le formulaire de commentaires en sélectionnant Aperçu en anglais (États-Unis). Si vous avez créé le formulaire dans plusieurs langues, vous pouvez également le prévisualiser dans chaque langue respective. Consultez cette [section](/help/migrated/administrators/feature-summary/l1-feedback-form.md#add-feedback-forms-in-other-languages) pour découvrir comment ajouter des formulaires de retour d&#39;informations dans d&#39;autres langues.

![](assets/preview.png)
_L’écran Formulaires de retour d’informations affiche l’option Aperçu pour afficher le formulaire de retour d’informations dans la langue par défaut_

### Ajout de formulaires de commentaires dans d’autres langues

Créez des traductions pour les questions du formulaire de retour d’informations dans plusieurs langues. Cependant, vous ne pouvez ajouter ou supprimer des questions que dans la langue par défaut (l’anglais, par exemple). Pour les autres langues, vous ne pouvez traduire que les questions ajoutées initialement dans la langue par défaut. Il n’est pas possible d’ajouter ou de supprimer des questions directement dans les versions traduites.

1. Sélectionnez **[!UICONTROL Ajouter une nouvelle langue]** dans le formulaire de retour d&#39;informations.

   ![](assets/add-new-language.png)
   _Ajouter une nouvelle version linguistique au formulaire de retour d&#39;informations_
2. Choisissez la langue souhaitée et sélectionnez **[!UICONTROL Enregistrer]**.
3. Accédez à l’onglet correspondant à la langue que vous avez ajoutée.
4. Sélectionnez **[!UICONTROL Traduire]** en regard de chaque question pour ajouter votre traduction.

   ![](assets/translate.png)
   _Écran de formulaire de retour d&#39;informations affichant l&#39;option Traduire pour traduire les questions dans les langues respectives_

   >[!NOTE]
   >
   >La question Score d’efficacité du cours se traduit automatiquement.

5. Après avoir ajouté les traductions, sélectionnez **[!UICONTROL Enregistrer]**.

## Définition d’un formulaire de commentaires par défaut

Les administrateurs peuvent définir des formulaires de retour d’informations par défaut pour les cours en auto-apprentissage, en salle de classe, en salle de classe virtuelle et mixtes. Une fois qu&#39;un formulaire par défaut est défini, il est automatiquement appliqué à tous les cours nouvellement créés. Les élèves verront ce formulaire après avoir terminé un cours. Les administrateurs peuvent choisir d’attribuer un formulaire de retour d’informations différent pour des cours spécifiques, si nécessaire.

![](assets/set-as-default.png)
_L&#39;écran Formulaires de commentaires affiche l&#39;option permettant de définir le formulaire de commentaires par défaut_

## Configuration des paramètres de retour d’informations de l’élève

Les administrateurs peuvent configurer les paramètres suivants dans la section Commentaires des élèves :

* **[!UICONTROL Activer le formulaire pour recueillir les commentaires des élèves pour ce cours]** : activez cette option pour recueillir les commentaires des élèves pour le cours. Lorsque cette option est activée, les élèves seront invités à fournir des commentaires après avoir terminé le cours.
* **[!UICONTROL Paramètre de formulaire]** : lorsque cette option est activée, le formulaire de retour d&#39;informations s&#39;ouvre automatiquement pour les élèves immédiatement après avoir terminé le cours, ce qui facilite la collecte des commentaires en temps opportun.

![](assets/course-settigs.png)
_Écran de retour d’informations de l’élève affichant les paramètres de retour d’informations de l’élève_

>[!NOTE]
>
>Les instances de cours utilisent le formulaire de retour d’informations par défaut du niveau de cours. Lorsque vous créez de nouvelles instances, elles utilisent également le formulaire par défaut au niveau du cours plutôt qu’au niveau du compte.

### Modifier le formulaire de retour d&#39;informations par défaut d&#39;un cours

Le formulaire de retour d’informations par défaut s’applique à tous les cours. En tant qu’administrateur, vous pouvez soit créer un nouveau formulaire, soit en choisir un dans la liste existante. Pour modifier les formulaires de retour d’informations par défaut, le retour d’informations de l’élève doit être activé pour ce cours.

Pour modifier le formulaire de retour d’informations par défaut :

1. Sélectionnez **[!UICONTROL Cours]** sur la page d&#39;accueil de l&#39;administrateur.
2. Sélectionnez un cours dans la section **[!UICONTROL Cours]**.
3. Sélectionnez **[!UICONTROL Afficher le cours]**, puis **[!UICONTROL Retour d&#39;informations de l&#39;élève]**.

   ![](assets/edit-form.png)
   _Les écrans de retour d’informations de l’élève affichent l’option Modifier pour modifier le formulaire_
4. Sélectionnez **[!UICONTROL Modifier]** dans la section **[!UICONTROL Retour d&#39;informations de l&#39;élève]**.
5. Sélectionnez **[!UICONTROL Modifier le formulaire]**.

   ![](assets/change-form.png)
   _Les écrans de retour d’informations de l’élève affichent l’option Modifier le formulaire pour modifier le formulaire de retour d’informations pour le cours_
6. Choisissez un autre formulaire de retour d&#39;informations dans le menu ou sélectionnez **[!UICONTROL Commencer avec un formulaire vierge]** pour en créer un nouveau.

   ![](assets/pick.png)
   _Ajouter un écran de formulaire affichant l&#39;option permettant de choisir parmi le modèle disponible ou de créer un nouveau formulaire_
7. Sélectionnez **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

Si un cours utilise le formulaire de retour d’informations par défaut et que le formulaire par défaut est mis à jour au niveau du compte, tous ces cours reflètent automatiquement le nouveau formulaire. Toutefois, si un administrateur modifie le formulaire ou attribue un nouveau formulaire au niveau du cours, les modifications futures du formulaire par défaut n&#39;auront aucune incidence sur le formulaire de retour d&#39;informations de ce cours.

L’instance utilise par défaut le formulaire de retour d’informations au niveau du cours. Si un administrateur modifie le formulaire de retour d&#39;informations au niveau du cours, cela n&#39;affectera pas le formulaire déjà défini au niveau de l&#39;instance. Cependant, toute nouvelle instance créée après la modification utilise le formulaire de retour d’informations mis à jour au niveau du cours par défaut.

Suivez les mêmes étapes pour modifier les formulaires de retour d’informations par défaut pour un parcours d’apprentissage.

>[!NOTE]
>
>Si vous ne modifiez pas le formulaire, le cours utilise le formulaire de retour d&#39;informations par défaut.



