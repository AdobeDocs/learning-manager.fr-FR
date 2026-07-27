---
description: Proposez un cours à plusieurs publics en contrôlant les modules que chaque élève voit et ceux qui sont requis, en fonction des groupes d’utilisateurs auxquels ils appartiennent.
jcr-language: en_us
title: Cours adaptatifs dans Adobe Learning Manager
contentowner: mmanuel
source-git-commit: 5d4ba4ccd3b32a6108b5c8101f48f12f27775e00
workflow-type: tm+mt
source-wordcount: '1964'
ht-degree: 0%

---


# Cours adaptatifs dans Adobe Learning Manager

Les cours adaptatifs dans Adobe Learning Manager vous permettent de proposer un cours à plusieurs publics en contrôlant les modules que chaque élève voit et qui sont requis, en fonction des groupes d&#39;utilisateurs auxquels ils appartiennent.

Au lieu de créer des cours distincts pour chaque rôle, région ou profil de conformité, un cours adaptatif unique présente dynamiquement le bon contenu au bon élève.

## Résolution des problèmes liés aux cours adaptatifs

Les organisations qui forment un personnel nombreux et diversifié sont confrontées à un défi commun : la confidentialité des données, l&#39;éthique au travail et la sécurité doivent atteindre les apprenants avec des rôles, des lieux ou des obligations de conformité différents.

Cela crée une duplication : les auteurs maintiennent plusieurs cours presque identiques, le reporting est fragmenté et lorsque le contenu de base change, chaque copie doit être mise à jour.

Un cours adaptatif résout ce problème en permettant aux auteurs de configurer les règles de visibilité et d’achèvement au niveau du module, liées aux groupes d’utilisateurs. Un cours sert chaque public simultanément.

### Scénarios courants

- Un cours sur la conformité comporte un module de base pour tous les employés ainsi que des modules complémentaires spécifiques à chaque juridiction. Chaque élève ne voit que les addenda qui s’appliquent à son emplacement.
- Un cours pour nouvel employé présente différents modules aux employés, aux responsables et aux sous-traitants. Chaque rôle ne voit que ce qui est pertinent pour lui.
- Un cours de sécurité ajoute un nouveau module obligatoire en milieu d&#39;année. Les administrateurs déclenchent une actualisation terminée, de sorte que tous les élèves terminés précédemment doivent suivre le nouveau module pour rester conformes.

### Exemple concret

Une organisation déploie un cours de conformité obligatoire pour l&#39;ensemble de son personnel. Le cours comprend sept modules :

- Deux modules s&#39;appliquent à tous les employés.
- Deux modules s’appliquent uniquement aux responsables de personnes.
- Deux modules s’appliquent uniquement aux contributeurs individuels dans des rôles techniques.
- Un module s&#39;applique uniquement aux administrateurs principaux et supérieurs.

## Fonctionnement de la visibilité et de l’achèvement du module

Chaque module de contenu d’un cours adaptatif possède deux paramètres :

**Visible par :** groupes d&#39;utilisateurs qui peuvent voir le module. Les élèves de ces groupes voient le module du cours et peuvent y accéder, mais il n&#39;est pas comptabilisé dans l&#39;achèvement à moins qu&#39;ils ne soient également dans **Obligatoire pour**.

**Obligatoire pour :** groupes d&#39;utilisateurs pour lesquels le module est requis pour terminer le cours. Un module répertorié sous **Obligatoire pour** est automatiquement visible par ces groupes. Vous n&#39;avez pas besoin d&#39;ajouter les mêmes groupes aux deux paramètres.

Un module est dans l’un des trois états pour un élève donné à un moment donné :

| État | Comment c&#39;est déterminé | Compte jusqu’à l’achèvement ? |
|---|---|---|
| Obligatoire | L&#39;élève fait partie d&#39;un groupe d&#39;utilisateurs répertorié sous **Obligatoire pour** | Oui - doit être rempli |
| Facultatif | L&#39;élève se trouve dans un groupe sous **Visible par** mais pas **Obligatoire pour** | Non : visible et accessible, mais pas obligatoire. |
| Masqué | L’élève ne fait partie d’aucun groupe sous l’un des paramètres | Absolument invisible pour l’élève |

## Caractéristiques d&#39;un parcours adapté

La caractéristique principale des cours adaptatifs est que le cours évalue le profil de l’élève en continu, et pas seulement lors de l’inscription.

Lorsque le groupe d’utilisateurs d’un élève change pendant son inscription :

- Les modules qui ne sont plus visibles sous leur nouveau groupe d’utilisateurs disparaissent immédiatement.
- Si un module nouvellement visible est obligatoire pour son nouveau groupe d’utilisateurs, il est ajouté à leur condition d’achèvement.
- Si un module auparavant obligatoire n’est plus obligatoire, il est supprimé de l’exigence d’achèvement.
- Les modules précédemment terminés restent terminés. Un changement de profil ne réinitialise pas le travail déjà effectué.

### Désinscription automatique

Si une modification de groupe d’utilisateurs supprime tous les modules obligatoires d’un élève, celui-ci est automatiquement désinscrit du cours.

### Saisie semi-automatique

Si une modification de groupe d’utilisateurs supprime tous les modules obligatoires incomplets restants d’un élève en cours, le cours se termine automatiquement pour cet élève.

Si une modification de profil entraîne de nouveaux modules obligatoires que l’élève n’a pas terminés, un administrateur peut déclencher une actualisation de la fin pour annuler la fin existante et exiger que l’élève termine les nouveaux modules.

## Qu’est-ce qui s’adapte et reste le même

Les règles adaptatives s&#39;appliquent uniquement aux **modules de contenu**. Les éléments suivants s’appliquent à tous les élèves inscrits, quel que soit le groupe d’utilisateurs :

- **Modules de préparation :** affichés à tous les élèves avant le début du contenu de base.
- **Modules de test :** disponibles pour tous les élèves ; terminer un test termine le cours quel que soit le statut du module de contenu.
- **Conditions préalables :** si des conditions préalables sont configurées pour un cours, tous les élèves doivent les remplir avant de s&#39;inscrire, quel que soit leur groupe d&#39;utilisateurs. Les conditions préalables ne sont pas adaptatives et ne peuvent pas être étendues à des groupes d’utilisateurs spécifiques.

Les assistances à la tâche et les ressources associées au cours ne sont pas non plus adaptatives. Ils sont visibles par tous les élèves inscrits.

Les compétences, les points de ludification et les badges sont attribués en fonction de la première fin de cours de l’élève et ne sont pas affectés par les nouvelles finalisations résultant de changements de profil.

>[!NOTE]
>
>Lorsqu’un cours adaptatif fait partie d’un objet d’apprentissage d’ordre supérieur partagé en externe, le cours adaptatif est copié en tant que cours normal dans le compte enfant.


## Disponibilité des fonctionnalités

La fonctionnalité de cours adaptatif est contrôlée par un indicateur à deux niveaux au niveau du compte. Contactez l’équipe chargée de votre compte Adobe pour activer cette fonctionnalité pour votre compte.

Une fois l’indicateur de compte activé :

- Un bouton à bascule **Règles d&#39;achèvement et de visibilité** est disponible lors de la création ou de la modification d&#39;un cours.
- L’activation du bouton à bascule active le panneau de configuration adaptative.

**Attention :** l&#39;activation de l&#39;indicateur de fonctionnalité adaptative est **irréversible**. Une fois activée au niveau du compte, elle ne peut pas être désactivée.

## Partage de catalogue

Des cours adaptatifs peuvent être ajoutés aux catalogues de votre compte. Lorsqu&#39;un catalogue est partagé en externe avec un compte de pairs, les cours adaptatifs sont automatiquement exclus du contenu partagé.

>[!NOTE]
>
>Lorsqu’un parcours d’apprentissage ou une certification contenant un cours adaptatif est partagé en externe, le compte destinataire voit le parcours d’apprentissage ou la certification dans son catalogue, mais le cours adaptatif qu’il contient n’apparaît pas. L’objet d’apprentissage n’est pas entièrement exclu ; seul le composant de cours adaptatif est supprimé de la version partagée. Les auteurs du compte destinataire doivent savoir que l’objet d’apprentissage partagé peut comporter moins de modules que la version source.

>[!NOTE]
>
>Lorsqu&#39;un cours adaptatif est configuré comme prérequis d&#39;un autre cours et que ce cours parent est partagé avec un compte destinataire via le partage de catalogue, le cours prérequis adaptatif n&#39;est pas partagé avec le compte destinataire. Cela s’applique que la condition préalable soit définie directement sur le cours ou via un objet d’apprentissage d’ordre supérieur tel qu’un parcours d’apprentissage ou une certification.
>
>Dans le compte de réception, le cours parent est disponible, mais la condition préalable adaptative est absente. Les élèves du compte destinataire ne sont pas affectés par la condition préalable manquante, car la dépendance de la condition préalable n’est pas appliquée pour le contenu qui arrive par partage de catalogue sans que ses conditions préalables soient présentes.
>
>Ne configurez pas les cours adaptatifs comme conditions préalables pour le contenu que vous avez l&#39;intention de partager en externe.

## Configurations prises en charge

| Configuration | Pris en charge ? |
| --- | --- |
| Cours adaptatif dans un parcours d’apprentissage régulier | Oui (voir note ci-dessous) |
| Cours adaptatif dans un parcours d’apprentissage flexible | Oui |
| Cours adaptatif dans un parcours d’apprentissage adaptatif | Non |
| Cours adaptatif dans une certification | Oui (non recommandé pour les certifications récurrentes) |
| Inscription multiple | Non |
| Changement d’instance | Oui |
| Partage de catalogue (entre comptes) | Non |
| Règles de visibilité des modules préparatoires ou de test | Non |
| Règles de visibilité sur les modules de contenu de base | Oui |
| Cours adaptatif dans un parcours d’apprentissage flexible | Oui |

>[!NOTE]
>
>Lors du téléchargement du **PDF de rapport de présence** pour une session d’un cours adaptatif qui fait partie d’un parcours d’apprentissage Flex, les élèves inscrits sur liste d’attente apparaissent sous la section Actif du PDF. L’interface du parcours d’apprentissage ne dispose pas d’une section de liste d’attente dédiée, il n’existe donc aucun compartiment de liste d’attente distinct dans l’exportation du PDF. Pour identifier précisément les élèves inscrits sur liste d&#39;attente, cochez la case **Administrateur > [Cours adaptatif] > Liste d&#39;attente** avant de marquer l&#39;assiduité.

La colonne **Incorporé dans** du rapport Liste d’attente identifie les instances du parcours d’apprentissage Flex qui contiennent ce cours adaptatif en tant qu’élément. Le nom du parcours d’apprentissage et l’ID de l’objet d’apprentissage s’affichent. Il n&#39;est pas destiné à afficher les chemins d&#39;inscription d&#39;un élève individuel. Pour les cours adaptatifs imbriqués dans un sous-parcours d’apprentissage qui se trouve lui-même dans un parcours d’apprentissage parent, seul le parcours d’apprentissage parent direct apparaît dans cette colonne.

Lorsque le cours adaptatif fait partie d&#39;une **certification récurrente**, l&#39;achèvement de l&#39;actualisation s&#39;applique uniquement à l&#39;inscription de l&#39;élève au cycle de certification racine. Les cycles récurrents suivants contiennent une instance distincte du cours adaptatif qui n&#39;est pas affectée par l&#39;actualisation. Les élèves inscrits à un cycle récurrent ne voient pas les mises à jour du module ou voient leurs achèvements annulés. Si votre organisation utilise des cours adaptatifs dans les certifications récurrentes, communiquez cette limitation aux administrateurs avant de déclencher les fins d&#39;actualisation.

>[!NOTE]
>
>Lorsqu&#39;un cours adaptatif est inclus dans un parcours d&#39;apprentissage **ordonné**, les élèves qui n&#39;ont pas de modules visibles dans le cours adaptatif, car leur groupe d&#39;utilisateurs ne correspond à aucune règle de visibilité des modules, ne peuvent pas terminer ce cours. Dans un parcours d’apprentissage ordonné, cela empêche tous les éléments suivants d’être accessibles. Pour éviter cela, assurez-vous que chaque élève inscrit au parcours d’apprentissage appartient à au moins un groupe d’utilisateurs qui a une visibilité sur au moins un module dans n’importe quel cours adaptatif du parcours.

En outre, n’incorporez pas un parcours d’apprentissage contenant un cours adaptatif dans un parcours d’apprentissage d’ordre supérieur (imbriqué). Dans cette configuration, si un élève ne dispose d’aucun module visible ou obligatoire dans le cours adaptatif, le lecteur intégré peut ne plus répondre, empêchant la navigation dans le contenu restant. Ce comportement sera traité dans une prochaine version.

>[!NOTE]
>
>Lorsqu’un élève est automatiquement désinscrit d’un cours adaptatif dans un parcours d’apprentissage **normal**, car un changement de groupe d’utilisateurs a supprimé tous leurs modules visibles, le parcours d’apprentissage parent reste inscrit. Le parcours d’apprentissage ne se désinscrit pas automatiquement. L’élève verra le parcours d’apprentissage tel qu’il est inscrit dans son relevé de notes même si le cours adaptatif qu’il contient n’est plus accessible. Si votre cas d’utilisation nécessite que le parcours d’apprentissage parent se désinscrive également lorsque le cours adaptatif le fait, envisagez d’utiliser un **parcours d’apprentissage adaptatif** au lieu d’un parcours d’apprentissage normal pour contenir le cours adaptatif.

## Activation des cours adaptatifs pour votre compte

Activez l’apprentissage adaptatif afin que les auteurs puissent créer des cours qui affichent différents modules à différents élèves en fonction de l’appartenance à un groupe d’utilisateurs.

## Avant d’activer

- **Permanent:** Une fois activé, l&#39;apprentissage adaptatif ne peut pas être désactivé pour le compte.
- **Affecte à la fois les cours et les parcours d’apprentissage simultanément :** Le même indicateur qui active les cours adaptatifs active également les parcours d’apprentissage adaptatifs.
- **Les cours existants restent inchangés :** seuls les cours nouvellement créés peuvent être adaptés. Aucun cours normal existant n’est converti automatiquement.
- **Les auteurs voient immédiatement l&#39;option :** dès que vous enregistrez, le type de cours adaptatif apparaît dans le workflow de création.
- **Provisionnement à deux niveaux :** si votre compte a été provisionné pour l’apprentissage adaptatif, l’option est activée et verrouillée. Il ne peut pas être modifié à partir de l’interface utilisateur. Si le compte n’a pas été configuré, le paramètre n’est pas visible du tout. Adobe de contact pour demander l’approvisionnement.

## Activer les cours adaptatifs

1. Connectez-vous à Adobe Learning Manager en tant qu’administrateur.
2. Sélectionnez **Paramètres** dans le volet de navigation de gauche.
3. Sélectionnez **Général**.
4. Accédez à la section **Règles de visibilité et d&#39;achèvement**. Si l’apprentissage adaptatif a été activé pour votre organisation, l’option s’affiche comme verrouillée, comme indiqué :

![](assets/image_0001.png)

L’apprentissage adaptatif est désormais actif pour votre compte. Les auteurs peuvent créer immédiatement des cours adaptatifs et des parcours d’apprentissage adaptatifs.

## Modifications après l’activation

Après avoir activé l’apprentissage adaptatif :

- Les auteurs voient une option **Visibilité du contenu et règles d&#39;achèvement** lors de la création d&#39;un cours, en plus du type de cours normal existant.
- Chaque module de contenu d&#39;un cours adaptatif peut être configuré avec des règles **facultatives** et **obligatoires** pour les groupes d&#39;utilisateurs.
- Les élèves inscrits à un cours adaptatif voient uniquement les modules que leurs groupes d&#39;utilisateurs rendent visibles.
- Tous les cours réguliers existants restent inchangés.

## Dépannage

- **La section Règles de visibilité et d&#39;achèvement n&#39;est pas visible dans Paramètres :** La fonctionnalité doit être configurée en arrière-plan avant que le bouton bascule n&#39;apparaisse. Contactez votre représentant de compte Adobe ou le support Adobe pour demander l’accès.
- **Le bouton est déjà activé et semble verrouillé :** l&#39;apprentissage adaptatif a été activé lors de la configuration de votre compte. Aucune action n’est nécessaire. Les auteurs peuvent déjà créer des cours adaptés.
