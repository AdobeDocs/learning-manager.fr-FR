---
description: Découvrez comment les auteurs personnalisent les e-mails au niveau du cours et de l’instance dans Email Builder avec une mise en page d’administrateur, et comment résoudre les problèmes courants
jcr-language: en_us
title: Personnalisation des e-mails de cours et d’instance dans Email Builder
exl-id: 06499e3f-0610-4983-83f2-3e8b578fc8bf
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%
---

## Personnalisation des e-mails de cours et d’instance dans Email Builder

Personnalisez les e-mails au niveau du cours et de l’instance dans Adobe Learning Manager avec Email Builder et une mise en page fournie par votre administrateur.

En tant qu’auteur, vous pouvez personnaliser les e-mails d’un cours ou d’une instance spécifique d’un cours. Les deux procédures partent d’une mise en page fournie par votre administrateur.

### Personnalisation d’un e-mail de niveau cours

1. Ouvrez le cours.
2. Sélectionnez **Modèles de courrier électronique**.
3. Sélectionnez **Disposition des e-mails du cours**.
4. Personnalisez le contenu de l’e-mail. Pour définir des polices, des couleurs, des lignes et des boutons.
5. Enregistrez le modèle.
6. Publish du cours.

### Personnalisation d’une adresse e-mail au niveau de l’instance

Utilisez une adresse e-mail au niveau de l’instance lorsque différentes cohortes ont besoin de différents messages. Vous gérez ces cohortes via des instances de cours.

1. Ouvrez l&#39;instance de cours.
2. Ouvrez **Email Builder**.
3. Sélectionnez une mise en page disponible ou héritez de la mise en page déjà utilisée par l’instance.
4. Mettez à jour le contenu du message.
5. Enregistrez le modèle.

>[!NOTE]
>
>Lorsque les deux existent, les e-mails au niveau de l’instance remplacent les modèles au niveau du cours.

### Utiliser la variable Titre et une image pour les en-têtes d’e-mail

Utilisez la variable Titre avec un composant Image pour créer l’en-tête d’e-mail au lieu du composant Bannière. L’image du composant Bannière n’apparaît pas dans certains clients de messagerie, tels qu’Outlook.

La variable Titre, EmailTitle, fonctionne comme la variable ChannelName existante. Chaque e-mail possède sa propre valeur de titre par défaut.

Pour ajouter un en-tête de titre :

1. Ajoutez un composant Image pour l’image d’en-tête.
2. Ajoutez un composant Texte et insérez la variable titre à partir du menu déroulant des variables dans le volet de configuration du composant.
3. Alignez le composant Texte au centre. Dans la disposition globale, placez-la dans l’en-tête supérieur.

Par défaut, chaque e-mail utilise l’en-tête de la mise en page globale. Dans un e-mail individuel, vous pouvez modifier le composant Texte pour :

1. Remplacer la variable par du texte personnalisé
2. Ajouter du texte avant ou après la variable et conserver `EmailTitle`

Si vous ajoutez une image au composant de bannière, Email Builder affiche un avertissement indiquant que l’image peut ne pas s’afficher correctement sur certains clients de messagerie. L’avertissement suggère d’utiliser à la place un composant Image et la variable titre.

### Dépannage

**Vous ne pouvez pas sélectionner de disposition.**
L’héritage de la disposition dépend des dispositions parentes disponibles. Demandez à votre administrateur de créer une disposition de compte.

**Votre e-mail n’affiche pas les modifications de mise en page récentes.**
Le modèle peut être dissocié de sa mise en page. Les modèles non liés ne reçoivent plus de mises à jour de mise en page.

**Les élèves d’une instance reçoivent un e-mail différent de l’e-mail du cours.**
Les e-mails au niveau de l’instance remplacent les modèles au niveau du cours. Passez en revue le modèle au niveau de l’instance.

**Les e-mails relatifs à votre cours ou à votre instance ne s’affichent pas dans Email Builder.**
L’Adobe active Email Builder par phases. Demandez à votre administrateur de confirmer que le générateur d’e-mails est activé pour votre compte.

**Votre image de bannière n’apparaît pas dans l’e-mail.**
Certains clients de messagerie, tels qu&#39;Outlook, n&#39;affichent pas l&#39;image du composant Bannière. Supprimez le composant Bannière, ajoutez un composant Image et ajoutez un composant Texte qui utilise la variable titre.
