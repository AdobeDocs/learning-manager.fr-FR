---
description: Découvrez comment utiliser les champs actifs dans Adobe Learning Manager pour capturer, organiser et gérer des informations utilisateur personnalisées. Améliorez la création de rapports, le filtrage et la segmentation des utilisateurs grâce à des configurations de champs flexibles.
jcr-language: en_us
title: Configuration des champs actifs dans Adobe Learning Manager
exl-id: e68300d6-9f19-4e42-b485-c4bbbbcf5518
source-git-commit: a01ec6117ad49a1f9af0b31d48ad19ddc8443dde
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# Champs actifs

Les champs actifs dans Adobe Learning Manager sont des attributs utilisateur personnalisés qui aident les administrateurs à organiser et à gérer efficacement les utilisateurs. Ils vous permettent de capturer des informations supplémentaires sur l’utilisateur, telles que le service, le lieu ou la fonction. Les administrateurs peuvent utiliser ces données pour créer des groupes d’utilisateurs, personnaliser l’apprentissage et filtrer les rapports plus efficacement.

Les attributs utilisateur sont des informations telles que le prénom, le nom et l’adresse e-mail d’un utilisateur. Ces attributs aident les administrateurs à :

* Identification des utilisateurs
* Groupes d’utilisateurs
* Gestion des autorisations utilisateur et des restrictions d’accès

En ajoutant des attributs personnalisés aux profils utilisateur, les champs actifs capturent des informations supplémentaires pertinentes pour votre organisation.

>[!INFO]
>
>Regardez cette formation ALM Academy pour apprendre à ajouter, personnaliser et configurer des champs actifs.<br>[![bouton](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7555741)</br>

## Ajouter des champs actifs

Les champs actifs s&#39;appliquent aux élèves internes et externes, ce qui permet aux organisations de définir et de gérer des attributs d&#39;utilisateur personnalisés pour tous les utilisateurs.

Pour ajouter ou gérer des champs actifs pour les utilisateurs internes :

1. Sélectionnez **Utilisateurs** sur la page d&#39;accueil de l&#39;administrateur.

2. Sélectionnez **Champs actifs**.

3. Saisissez le nom du champ actif, puis sélectionnez **Ajouter**. Le processus d’ajout de champs actifs pour les élèves externes est le même que pour les élèves internes.

   ![](assets/add-active-field-alm.png)
   _Champ permettant de saisir le nom d&#39;un nouvel attribut personnalisé pour les utilisateurs_

4. Sélectionnez **Enregistrer**.

## Ajouter des valeurs personnalisées aux champs actifs

Les champs actifs peuvent inclure des valeurs prédéfinies ou personnalisées qui correspondent à la structure de votre organisation. L’ajout de valeurs personnalisées permet de capturer des détails spécifiques à vos utilisateurs internes, tels que les noms des services, les niveaux de poste ou les bureaux régionaux.

Pour ajouter des valeurs personnalisées pour les utilisateurs internes :

1. Sélectionnez **Afficher les valeurs** dans la section **Champ actif**.
2. Dans la boîte de dialogue **Valeurs dans les champs personnalisés** :

   * Sélectionnez un champ actif dans la liste déroulante **Sélectionner un champ**.
   * Saisissez les valeurs du champ actif dans le champ **Nouvelle valeur**.

   ![](assets/add-value-active-fields.png)
   _Boîte de dialogue pour saisir des valeurs personnalisées pour un champ actif spécifique_

3. Sélectionnez **Terminé**, puis **Enregistrer** pour appliquer les modifications.

## Configuration des paramètres de champ actif

Personnalisez les champs actifs pour faciliter les tâches de gestion des utilisateurs et de création de rapports, et configurez les propriétés des champs actifs :

* **Regroupable** : cette option vous permet de regrouper les élèves en fonction des valeurs de champ actives.
* **Reportable** : cette option vous permet de créer un groupe d&#39;utilisateurs de rapport en fonction de la valeur du champ actif et active le filtre de rapport pour le champ dans les rapports du tableau de bord.
* **Configurable par l’élève** : cette option permet aux élèves de configurer le champ eux-mêmes.
* **Exportable** : cette option inclut le champ actif dans les rapports de groupe d&#39;utilisateurs exportés.
* **Valeurs multiples** : cette option prend en charge plusieurs valeurs pour le champ actif.

Pour configurer les paramètres des champs actifs :

1. Sélectionnez l&#39;onglet **Paramètres**, puis accédez à la section **Affichage utilisateur**.

   ![](assets/settings-active-field.png)
   _Sélectionnez l&#39;onglet Paramètres pour personnaliser les champs actifs_

2. Sélectionnez une ou les deux options, selon vos besoins.:

   * **Afficher uniquement les champs non remplis lors de la connexion de l&#39;élève :** lorsque cette option est sélectionnée, les élèves ne verront que les champs actifs qu&#39;ils n&#39;ont pas encore remplis. Cela les invite à compléter leur profil, ce qui permet de garantir que les données utilisateur sont exactes et à jour. L’affichage de ces champs prend en charge des profils d’élève complets et permet des expériences d’apprentissage personnalisées.
   * **Si cette case n&#39;est pas cochée, la page « Finaliser votre profil » n&#39;est pas affichée aux utilisateurs :** Lorsque cette option est désactivée, les élèves ne verront pas la page **Finaliser votre profil** lors de la connexion. Ils ne seront pas invités à mettre à jour ou à remplir les informations de profil et peuvent accéder directement à la plateforme.

   ![](assets/user-display-alm.png)
   _Interface Paramètres permettant de contrôler quand et comment les champs actifs sont affichés_

3. Sélectionnez **Enregistrer** pour appliquer vos modifications.

>[!NOTE]
>
>L’attribution d’un nouveau rôle n’affectera pas les groupes d’utilisateurs personnalisés. Toutefois, cela aura un impact sur les groupes d’utilisateurs générés automatiquement tels que Tous les administrateurs, Tous les auteurs et les groupes basés sur des rôles similaires.

## Champs actifs à plusieurs valeurs

Les champs actifs à plusieurs valeurs vous permettent d’affecter plusieurs valeurs à un seul attribut utilisateur, tel que les lieux, les titres de poste ou les équipes de projet. Cela permet de capturer des informations utilisateur plus détaillées et plus flexibles.

Vous pouvez configurer jusqu’à trois champs actifs à valeurs multiples par compte. Ils sont disponibles pour les utilisateurs internes et externes. Une fois qu’un champ est défini comme à plusieurs valeurs, ce paramètre ne peut plus être modifié.

Pour affecter plusieurs valeurs à un champ actif :

1. Sélectionnez **Utilisateurs**, puis **Champs actifs**.
2. Dans l&#39;onglet **Paramètres**, sélectionnez **Valeurs multiples**.

![](assets/multi-values.png)
_Interface Paramètres permettant de contrôler quand et comment les champs actifs sont affichés_

Vous pouvez ajouter plusieurs valeurs via le fichier CSV ou via l’interface utilisateur. Une fois que le champ à plusieurs valeurs est utilisé dans un groupe d’utilisateurs, il ne peut pas être remplacé par un champ à valeur unique.

## Ajouter des champs actifs en téléchargeant un fichier CSV

Ajoutez des champs actifs lors du chargement d’utilisateurs via CSV en incluant des en-têtes correspondants pour chaque champ défini. Les administrateurs peuvent télécharger des utilisateurs en bloc à l’aide d’un fichier CSV. Le fichier CSV doit inclure les nouveaux champs actifs qui définissent les utilisateurs à importer. Assurez-vous que les noms d’en-tête dans le fichier correspondent exactement aux champs actifs configurés dans le système afin que les mappages de données soient corrects. Chargez le fichier CSV à partir de la section **Utilisateurs**.

Consultez cet [article](/help/migrated/administrators/feature-summary/add-users-user-groups.md) pour plus d&#39;informations sur l&#39;ajout d&#39;utilisateurs par lot.

## Limitation des valeurs des champs CSV

L&#39;option **Restreindre la sélection** dans **Valeurs dans les champs personnalisés** contrôle si les utilisateurs qui importent des données via des fichiers CSV peuvent uniquement sélectionner des valeurs prédéfinies pour les champs personnalisés. Lorsque cette option est activée, les utilisateurs doivent faire leur choix dans la liste de valeurs définie, ce qui garantit la cohérence des données et empêche toute entrée nouvelle ou inattendue. Si cette option est désactivée, les utilisateurs peuvent saisir n’importe quelle valeur, ce qui offre plus de flexibilité mais moins de contrôle sur la précision des données.

![](assets/restrict-active.png)
_Case à cocher pour activer la restriction de valeur pendant le chargement CSV_

## Gestion des champs actifs manquants dans l’importation CSV de l’utilisateur

Dans certains cas, les administrateurs préfèrent que les élèves remplissent manuellement certains champs actifs lorsqu’ils se connectent à Adobe Learning Manager. Cette option est prise en charge pour les utilisateurs importés via un fichier CSV. Reportez-vous à cet [article](/help/migrated/administrators/feature-summary/add-users-user-groups.md) pour savoir comment ajouter des utilisateurs en bloc. Les utilisateurs sont automatiquement ajoutés aux champs actifs ou aux groupes basés sur des rôles en fonction des valeurs des champs FTP Box. Ils ne peuvent pas être ajoutés aux groupes personnalisés.

Si un fichier CSV ne comprend pas tous les champs actifs, l’administrateur doit saisir manuellement les valeurs manquantes après l’importation.

Par défaut, chaque champ actif doit être mappé à un champ correspondant dans le fichier CSV source. Toutefois, si vous ne souhaitez pas mapper un champ actif spécifique à une colonne du fichier CSV, vous pouvez sélectionner la valeur **DontImportFromSource** dans la liste déroulante pendant les processus d&#39;importation Box et FTP. Cette option est disponible lors de l’importation d’utilisateurs via des connecteurs FTP ou Box. Consultez cet [article](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/connectors) pour plus d&#39;informations sur les connecteurs.


