---
description: Tout sur l’activation du Gradebook et sa visibilité pour les auteurs et les élèves
jcr-language: en_us
title: Classeur pour l’administrateur
source-git-commit: 971576b95ab0f75b9d28a7f3d1d62440927925f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Activation de la visibilité de l’annuaire de notes pour votre compte

## Présentation

Avant que les auteurs puissent afficher le cahier de notes aux élèves dans un cours, un administrateur doit activer le paramètre de visibilité du cahier de notes au niveau du compte. Ce paramètre agit comme un commutateur principal : lorsqu&#39;il est désactivé, les élèves ne peuvent pas voir le cahier de notes dans un cours, quelle que soit la façon dont les cours individuels sont configurés.

## Ce que ce paramètre contrôle

Le paramètre **Visibilité du cahier de notes** dans **Paramètres** > **Général** détermine si les auteurs sont autorisés à exposer le cahier de notes aux élèves au niveau du cours.

| État du paramètre | Effet |
| --- | --- |
| Activé | Les auteurs peuvent contrôler la visibilité du journal de notes par cours à l&#39;aide de l&#39;option **Afficher le journal de notes aux élèves** dans l&#39;éditeur de cours. Les élèves voient l&#39;onglet **Gradebook** dans les cours où l&#39;auteur l&#39;a activé. |
| Désactivé | Les élèves ne peuvent pas voir le cahier de notes dans un cours. Si elle est désactivée, la configuration du cours n’aura pas le paramètre permettant d’afficher le cahier de notes pour les élèves. |


Cela signifie que le paramètre au niveau du compte et le paramètre au niveau du cours fonctionnent ensemble. Les deux doivent être activés pour qu’un élève puisse afficher le cahier de notes.

## Activer la visibilité des classeurs

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Dans le volet de navigation de gauche, sélectionnez **Paramètres**.
3. Sélectionnez **Général**.
4. Faites défiler jusqu&#39;à la section **Visibilité du Gradebook**.
5. Cochez la case **Activer l&#39;affichage Gradebook pour les élèves**.

   ![](assets/gradebook-admin-1.png)

Les auteurs peuvent désormais configurer la visibilité du cahier de notes par cours.

## Impact sur les workflows des auteurs

Lorsque ce paramètre au niveau du compte est activé, l&#39;option **Afficher le cahier de notes aux élèves** dans l&#39;éditeur de cours devient disponible. Les auteurs utilisent ce bouton pour décider, par cours, si les élèves peuvent voir l&#39;onglet **Gradebook**.

Lorsque ce paramètre au niveau du compte est désactivé :

* L&#39;option **Afficher le journal de notes aux élèves** dans l&#39;éditeur de cours peut toujours apparaître, mais toute configuration au niveau du cours est remplacée. Les élèves ne verront pas le cahier de notes.
* Les scores et les calculs pondérés du carnet de notes continuent d’être exécutés en arrière-plan à des fins de création de rapports par l’administrateur.
* Les administrateurs et les administrateurs personnalisés peuvent toujours télécharger les relevés de notes des élèves avec les données du carnet de notes.

>[!NOTE]
>
>La désactivation de ce paramètre au niveau du compte ne supprime aucune configuration ni note du journal de notes. Si vous l’activez à nouveau, tous les paramètres du carnet de notes de niveau cours précédemment configurés sont immédiatement restaurés.

## Interaction entre les deux paramètres

| Paramètre au niveau du compte | Paramètre au niveau du cours | Ce que l’élève voit |
| --- | --- | --- |
| Activé | Afficher le cahier de notes pour les élèves : **Activé** | Onglet **Gradebook** visible dans le lecteur de cours |
| Activé | Afficher le cahier de notes pour les élèves : **désactivé** | Aucun onglet Gradebook ; scores calculés en interne uniquement |
