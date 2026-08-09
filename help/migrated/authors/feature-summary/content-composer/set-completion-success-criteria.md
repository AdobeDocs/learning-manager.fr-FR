---
description: Découvrez la différence entre les critères d’achèvement et les critères de réussite dans le compositeur de contenu, comment les configurer et pourquoi la distinction est importante pour un suivi et un reporting précis des élèves dans Adobe Learning Manager.
jcr-language: en_us
title: Définition des critères d’achèvement et de réussite
source-git-commit: f8687710f5b73e8b7cf8d56057cac25483f38cdc
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---


# Définition des critères d’achèvement et de réussite

## Critères d’achèvement

**Critères d’achèvement** : sélectionnez le menu déroulant et choisissez quand le cours est marqué pour être terminé.

- **Lancer :** marque le cours comme terminé dès qu&#39;un élève l&#39;ouvre, quel que soit le nombre d&#39;éléments affichés.
  ![](../assets/21_completion_criteria_dropdown_launch_minview_quiz_updated.png)

- **Vue minimale % :** marque le cours comme terminé une fois qu&#39;un élève consulte le pourcentage spécifié du contenu du cours.
  ![](../assets/22_completion_criteria_minview_percent_field_updated.png)

- **Quiz : marque le cours comme étant terminé en fonction de l&#39;activité du quiz de l&#39;élève. Sélectionner une condition de quiz :**

  - **À la tentative :** marque l&#39;utilisateur comme étant terminé dès que l&#39;élève tente le quiz, quel que soit le résultat.

  - **Au passage :** marque comme terminé uniquement lorsque l’élève réussit le quiz.

  - **Le nombre de tentatives ou de réussites a été atteint :** points terminés lorsque l’élève réussit ou atteint le nombre maximal de tentatives autorisées, en fonction de la première éventualité.
    ![](../assets/23_completion_criteria_quiz_condition_dropdown_updated.png)

## Critères de réussite

Les **critères de réussite** déterminent si un élève est marqué comme ayant réussi ou échoué après avoir suivi le cours. Contrairement aux critères d’achèvement, les critères de réussite sont basés sur des scores.

>[!NOTE]
>
>Les options disponibles dépendent de la version de SCORM sélectionnée dans **Paramètres d&#39;exportation**. Si vous sélectionnez **SCORM 1.2**, les critères d&#39;achèvement et de réussite sont combinés dans un seul paramètre. Si vous sélectionnez **SCORM 2004**, les critères d&#39;achèvement et de réussite apparaissent comme des paramètres distincts, comme décrit ci-dessous.*

- **Critères de réussite** : sélectionnez la liste déroulante et choisissez comment le cours mesure la réussite.

- **Lancer :** marque l&#39;élève comme ayant réussi simplement en lançant le cours.
  ![](../assets/24_success_criteria_dropdown_launch_minview_quiz_updated.png)

- **Vue minimale %** : marque l’élève comme ayant réussi une fois qu’il a affiché le pourcentage de contenu spécifié. Par exemple, saisissez 80 pour exiger des élèves qu’ils affichent au moins 80 % du cours.
  ![](../assets/25_success_criteria_minview_percent_field_updated.png)

- **Quiz :** marque l&#39;élève comme ayant réussi ou échoué selon que son score de quiz atteint le seuil de réussite. Sélectionnez une condition de quiz :

  - **À la tentative : marque comme réussi dès que l’élève tente le quiz.**

  - **Réussite : le quiz n’est marqué comme réussi que lorsque l’élève réussit.**

  - **Une réussite ou une limite atteinte : marque comme réussi lorsque l’élève réussit ou atteint le nombre maximal de tentatives autorisées.**

  ![](../assets/26_success_criteria_quiz_condition_dropdown_updated.png)

>[!NOTE]
>
>Un élève peut terminer un cours, mais échouer malgré tout, par exemple, s’il termine tout le contenu mais n’obtient pas un score suffisant au quiz. Les critères d’achèvement et de réussite sont indépendants ; définissez-les soigneusement en fonction de la façon dont vous souhaitez que la progression de l’élève et les performances soient suivies. Lorsque vous sélectionnez Quiz pour l&#39;un des critères, configurez les tentatives de quiz et le score de réussite dans l&#39;onglet **Paramètres du quiz**.


## Pourquoi les critères d’achèvement et de réussite sont importants pour la création de rapports

- Les critères d’achèvement contrôlent le moment où l’état d’un élève passe à Terminé dans les transcriptions ALM, les tableaux de bord d’achèvement et toute exportation de conformité ou d’audit extraite du LMS : ils mesurent la progression, pas les performances.

- Les critères de réussite contrôlent la valeur Réussite/Échec enregistrée parallèlement à l’état d’achèvement, valeur sur laquelle reposent la plupart des rapports de conformité et de certification.

- Si les critères d&#39;achèvement et de réussite sont également configurés dans la bibliothèque de contenu **Adobe Learning Manager** pour le même module, ces paramètres ont priorité sur ceux définis dans le compositeur de contenu. Décidez rapidement quel produit doit être propriétaire de ces règles et évitez de définir des valeurs contradictoires aux deux endroits.

- Faites correspondre les critères à ce que vous devez prouver : Lancer ou Mon affichage % est suffisant pour le contenu de sensibilisation, tandis que les critères basés sur un quiz vous donnent un enregistrement défendable qu’un élève a démontré des connaissances - pas seulement qu’il a ouvert le cours.
