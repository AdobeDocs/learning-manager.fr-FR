---
description: En tant qu’auteur, découvrez comment créer des cours adaptatifs pour vos élèves.
jcr-language: en_us
title: Cours adaptatifs pour les auteurs
contentowner: mmanuel
source-git-commit: 5d4ba4ccd3b32a6108b5c8101f48f12f27775e00
workflow-type: tm+mt
source-wordcount: '3038'
ht-degree: 0%

---


# Cours adaptatifs pour les auteurs

## Créer et configurer un cours adaptatif

Créez un cours avec une visibilité par module et des règles d’achèvement afin que différents élèves voient et terminent différents contenus en fonction de leurs groupes d’utilisateurs.

>[!NOTE]
>
>Le type de cours adaptatif est disponible uniquement si les **règles de visibilité et d&#39;achèvement** ont été activées pour votre compte. Si vous ne voyez pas l’option permettant de créer un cours adaptatif, demandez à votre administrateur d’activer l’apprentissage adaptatif.

### Créer un cours adaptatif

1. Se connecter à Adobe Learning Manager en tant qu’auteur.

   ![](assets/ac-author-001.png)

2. Dans le volet de navigation de gauche, sélectionnez **Cours**. Sélectionnez ensuite **Ajouter**.
3. Saisissez le nom du cours, la description et d’autres détails.
4. Sélectionnez le bouton bascule **Visibilité du contenu et règles d&#39;achèvement**.

   ![](assets/ac-author-002.png)

5. Sélectionnez **Oui** dans la boîte de dialogue de confirmation.

   ![](assets/ac-author-003.png)

   **Ajouter des modules à un cours adaptatif**

   Ajoutez les modules requis. Ajoutez des modules de contenu en téléchargeant le contenu, en effectuant une sélection dans la bibliothèque de contenu ou en ajoutant des sessions de salle de classe ou de classe virtuelle.

   **Types de modules prenant en charge les règles adaptatives (modules de contenu) :**

   * Apprentissage en ligne individualisé
   * Sessions de salle de classe
   * Sessions de classe virtuelle
   * Modules d’activité

   **Types de module qui ne prennent PAS en charge les règles adaptatives :**

   * **Modules de préparation :** affichés à tous les élèves avant le début du contenu de base. Aucune règle de visibilité ou d’achèvement ne peut être définie.
   * **Modules de test :** disponibles pour tous les élèves. La réalisation d&#39;un test hors cours complète le cours entier, quel que soit le statut du module de contenu. Aucune règle de visibilité ou d’achèvement ne peut être définie.
   * **Assistances à la tâche :** visible à tout moment par tous les élèves inscrits.

6. Sélectionnez **Ajouter**.

### Configuration des règles de visibilité et d’achèvement pour chaque module

Après avoir ajouté un module de contenu, configurez ses règles adaptatives :

1. Sélectionnez le module à configurer.
2. Dans les paramètres du module, recherchez la section **Règles de visibilité et d&#39;achèvement**.

   ![](assets/ac-author-004.png)

3. Sélectionnez **Ajouter des règles** pour ajouter les groupes d&#39;utilisateurs qui peuvent voir ce module.

   ![](assets/ac-author-005.png)

   ![](assets/ac-author-006.png)

   Les élèves de ces groupes voient le module dans le cours, mais n&#39;ont pas besoin de le terminer à moins qu&#39;ils ne soient également dans Obligatoire.

4. Sélectionnez **Enregistrer**.
5. Répétez l’opération pour chaque module de contenu du cours.

**Règles clés :**

* Si un groupe rend un module obligatoire, il est obligatoire pour cet élève.
* Vous devez configurer au moins un module comme **Obligatoire** pour au moins un groupe d&#39;utilisateurs avant de pouvoir publier. Le système bloque la publication jusqu&#39;à ce que cette condition soit remplie.

### Cours à l’état de brouillon

Lorsqu&#39;un cours est à l&#39;état de brouillon, il représente la phase au cours de laquelle l&#39;ensemble de la structure adaptative peut être entièrement conçu, configuré et affiné avant d&#39;être verrouillé pour les élèves. À ce stade, les auteurs peuvent définir si le cours doit fonctionner comme un cours adaptatif ou un cours régulier, et cette décision reste réversible jusqu&#39;à ce que le cours soit publié. Cela rend la phase d&#39;ébauche critique, car c&#39;est le seul point où la nature adaptative fondamentale du cours peut être établie ou modifiée.

![](assets/ac-author-007.png)

Dans la version préliminaire, les auteurs ont un contrôle total sur la structure du cours. Ils peuvent ajouter, supprimer et réorganiser des modules librement pour façonner le flux d’apprentissage prévu. En même temps, ils peuvent configurer le comportement adaptatif à un niveau granulaire en définissant des règles de visibilité pour chaque module. Ces règles déterminent quels groupes d’utilisateurs peuvent accéder à des modules spécifiques, permettant au cours de proposer ultérieurement des expériences d’apprentissage personnalisées. Outre la visibilité, les auteurs peuvent également définir des règles d’achèvement, marquant les modules comme obligatoires ou facultatifs pour différents groupes d’utilisateurs. Le système exige qu&#39;au moins un module soit obligatoire pour garantir des critères d&#39;achèvement significatifs.

L’état Version préliminaire permet également la modification illimitée de la logique adaptative. Les auteurs peuvent ajouter, modifier ou supprimer des règles de manière itérative sans aucune contrainte du système, ce qui permet d&#39;expérimenter différentes configurations avant de finaliser le cours. En plus de la configuration adaptative, tous les éléments de cours standard restent modifiables, y compris les métadonnées du cours telles que le titre et la description, ainsi que le contenu d’apprentissage sous-jacent, y compris les modules SCORM ou d’autres ressources.

Il est important de comprendre que la configuration adaptative dans Draft ne s&#39;applique qu&#39;aux modules de cours de base. D&#39;autres composants, tels que le contenu préparatoire ou de test, ne prennent pas en charge les règles adaptatives et ne sont pas affectés par les configurations de visibilité ou d&#39;achèvement.

Enfin, l&#39;état de brouillon sert de dernière occasion de valider la configuration du cours avant la publication. Une fois le cours publié, la configuration adaptative devient permanente et ne peut pas être rétablie.

### Aperçu en tant qu’élève

La sélection de **Aperçu en tant qu&#39;élève** affiche tous les modules du cours, quelles que soient les règles du groupe d&#39;utilisateurs. Cela permet aux auteurs et aux administrateurs d’avoir une vue complète de la structure du cours. Les élèves en production voient uniquement les modules que leurs groupes d&#39;utilisateurs rendent visibles.

### Publish un cours adaptatif

La publication d&#39;un cours adaptatif suit le même workflow que la publication d&#39;un cours normal.

Après avoir configuré tous les modules et leurs règles, sélectionnez **Publish**.

Une fois publié, le cours est disponible pour inscription. Les élèves voient uniquement les modules configurés pour leurs groupes d’utilisateurs lorsqu’ils ouvrent le cours.

>[!IMPORTANT]
>
>Une fois publié, vous ne pouvez pas faire passer le cours de Adaptatif à Normal ou vice versa. Vérifiez votre configuration avant de publier.

### Comportement de partage de catalogue

Lorsqu&#39;un catalogue contenant des cours adaptatifs est partagé en externe avec un compte de pairs, les comportements suivants s&#39;appliquent :

* **Cours adaptatifs partagés directement :** les cours adaptatifs sont exclus du catalogue partagé. Ils n’apparaissent pas dans le compte de réception.
* **Cours adaptatifs dans un parcours d’apprentissage ou une certification :** si un programme d’apprentissage ou une certification contenant un cours adaptatif est partagé, le programme d’apprentissage ou la certification elle-même est copié sur le compte destinataire. Le cours adaptatif qu&#39;il contient est copié en tant que **cours normal**. La configuration adaptative, y compris toutes les règles de visibilité et d&#39;achèvement, n&#39;est pas copiée. Les auteurs du compte destinataire voient le cours comme un cours régulier avec tous les modules visibles par tous les élèves.
* **Cours adaptatifs définis comme prérequis :** si un cours adaptatif est configuré comme prérequis d’un cours régulier, d’un parcours d’apprentissage ou d’une certification qui est partagé, la relation prérequise n’est pas propagée au compte destinataire. Le cours parent ou l’objet d’apprentissage arrive sur le compte destinataire sans les conditions préalables.

>[!NOTE]
>
>Dans la mesure où les configurations adaptatives ne sont pas copiées lors du partage de catalogue, vérifiez toutes les relations préalables et les structures de programme d&#39;apprentissage/certification avant de partager un catalogue en externe. Les élèves du compte destinataire ne rencontreront pas le même comportement adaptatif que les élèves du compte source.


### Mettre à jour un cours adaptatif publié

Vous pouvez mettre à jour un cours adaptatif publié à tout moment. Les modifications prennent effet pour les élèves inscrits en temps quasi réel.

Notez que vous ne pouvez plus modifier les paramètres de visibilité dans le cours adaptatif. Vous ne pouvez pas rendre le cours non\-adaptatif.

![](assets/ac-author-008.png)

>[!NOTE]
>
>Un élève ne peut pas être sur liste d&#39;attente lors du changement d&#39;instance, l&#39;inscription sera bloquée.

### Ajout ou modification de modules

1. Ouvrez le cours publié.
2. Sélectionnez **Modifier**.
3. Ajoutez, modifiez ou supprimez des modules et ajustez leurs règles de visibilité et d’achèvement.
4. Republiez le cours.

**Impact :**

| Modifier | Effet sur les élèves inscrits en cours |
|---|---|
| Nouveau module obligatoire ajouté (visible par le groupe d’utilisateurs d’un élève) | Un module est ajouté à leur condition d’achèvement. Si le module est une salle de classe ou une session de classe virtuelle sans places restantes, l’élève est sur liste d’attente pour ce module. |
| Module supprimé ou rendu masqué pour le groupe d’utilisateurs d’un élève | Module supprimé de son exigence d’achèvement. S’il s’agissait du dernier module obligatoire, le cours est automatiquement rempli pour l’élève. |
| Le module est passé de obligatoire à facultatif pour le groupe d’utilisateurs d’un élève | Le module reste visible ; l’élève n’a plus besoin de le terminer pour terminer le cours. |
| Nouveau module obligatoire ajouté (l’élève a déjà terminé le cours) | Le module devient visible pour l’élève, mais il ne reçoit pas automatiquement de place ou n’y accède pas. Le nouveau module devient accessible uniquement lorsqu’une actualisation est terminée. |

>[!NOTE]
>
>**Parcours d’apprentissage ordonné :** lorsqu’un cours adaptatif est inclus dans un parcours d’apprentissage ordonné, les élèves qui n’ont pas de modules visibles dans le cours adaptatif ne peuvent pas le terminer. Cela empêche tous les éléments suivants du parcours d’apprentissage ordonné d’être accessibles. Assurez-vous que chaque élève inscrit au parcours d’apprentissage appartient à au moins un groupe d’utilisateurs qui rend au moins un module visible dans chaque cours adaptatif du parcours.

>[!NOTE]
>
>**Parcours d’apprentissage normal — désinscription automatique :** lorsqu’un élève est désinscrit automatiquement d’un cours adaptatif dans un parcours d’apprentissage normal parce qu’un changement de groupe d’utilisateurs a supprimé tous ses modules visibles, le parcours d’apprentissage parent reste inscrit. Le parcours d’apprentissage ne se désinscrit pas automatiquement. L’élève voit le parcours d’apprentissage comme inscrit dans son relevé de notes même si le cours adaptatif n’est plus accessible. Si votre cas d’utilisation nécessite que le parcours d’apprentissage se désinscrive également lorsque le cours adaptatif le fait, utilisez un **parcours d’apprentissage adaptatif** au lieu d’un parcours d’apprentissage normal.

### Comportement de changement d’instance

Un élève qui change d’instances d’un cours adaptatif poursuit sa progression :

* Les modules déjà terminés restent terminés dans la nouvelle instance.
* Les places sont consommées uniquement pour les modules visibles non terminés dans la nouvelle instance.
* Ils ne peuvent pas être inscrits sur liste d’attente lorsqu’aucune place n’est disponible pour une instance. L’inscription sera bloquée.

## Gestion des limites de places et des listes d’attente dans les cours adaptatifs

Les cours adaptatifs dans Adobe Learning Manager appliquent les limites de places au niveau de la salle de classe individuelle ou de la session de classe virtuelle. Contrairement aux cours normaux, où une session complète bloque l&#39;inscription entière, un cours adaptatif inscrit immédiatement l&#39;élève et le met en liste d&#39;attente uniquement pour les sessions spécifiques où aucune place n&#39;est disponible. L’élève peut accéder à tous les autres modules sans interruption.

### Fonctionnement des limites de places dans les cours adaptatifs

Lorsqu&#39;un élève s&#39;inscrit à un cours adaptatif qui comprend des modules de salle de classe ou de salle de classe virtuelle, le système vérifie la disponibilité des places uniquement pour les sessions qui sont visibles par l&#39;élève en fonction de ses groupes d&#39;utilisateurs.

* Si toutes les sessions de salle de classe visible ou de classe virtuelle disposent de places disponibles, l’élève est inscrit et dispose d’un accès complet immédiatement.
* Si une ou plusieurs sessions visibles n’ont pas de places disponibles, l’élève est inscrit et est immédiatement sur liste d’attente pour ces sessions spécifiques uniquement. Ils peuvent commencer et progresser dans tous les autres modules immédiatement.

### Limite de liste d’attente

Dans les cours réguliers, les instructeurs peuvent configurer une **limite de liste d&#39;attente**, une limite sur le nombre d&#39;élèves qui peuvent être placés sur la liste d&#39;attente pour une session.

Dans les cours adaptatifs, le paramètre **Limite de liste d&#39;attente** est désactivé dans l&#39;application de l&#39;instructeur et ne peut pas être configuré. Il n’y a pas de limite au nombre d’élèves qui peuvent être inscrits sur liste d’attente pour une session d’un cours adaptatif. Tous les élèves qui tentent de s’inscrire lorsqu’une session est pleine sont sur liste d’attente sans restriction.

Le tableau suivant décrit tous les scénarios de siège et de liste d&#39;attente pour les cours adaptatifs.

| Condition à l’inscription | Résultat |
| --- | --- |
| Toutes les sessions CR/VC visibles ont des places disponibles | Inscrit avec un accès complet à tous les modules |
| Une ou plusieurs sessions CR/VC visibles sont saturées | Inscrit ; en liste d’attente pour les sessions complètes uniquement ; tous les autres modules accessibles immédiatement |
| Élève déjà inscrit ; l’auteur ajoute une nouvelle session CR/VC obligatoire sans sièges | L’élève est sur liste d’attente pour la nouvelle session ; la progression existante et l’accès ne sont pas affectés |
| L’élève se désinscrit | Tous les sièges bloqués ont été libérés immédiatement ; les élèves inscrits sur liste d&#39;attente suivants ont été effacés dans l&#39;ordre de la date d&#39;inscription |
| La modification du groupe d’utilisateurs supprime une session du jeu visible de l’élève | Siège libéré immédiatement |
| L’élève termine le cours ; une nouvelle session CR/VC obligatoire devient visible | Module visible, mais aucun siège assigné automatiquement. L’élève doit déclencher la fin de l’actualisation pour accéder à la session. |
| L’administrateur ou l’instructeur alloue des licences | Toutes les sessions CR/VC de liste d’attente pour cet élève sont effacées simultanément |

>[!NOTE]
>
>**Comportement du parcours d’apprentissage Flex :** lorsqu’un cours adaptatif fait partie d’un parcours d’apprentissage Flex, le comportement de liste d’attente diffère de celui de l’inscription directe. Si un élève sélectionne une instance du cours adaptatif dans le programme d&#39;apprentissage Flex et qu&#39;aucune place n&#39;est disponible pour cette instance, l&#39;élève est sur liste d&#39;attente pour cette instance spécifique. Les informations sur les élèves inscrits sur liste d&#39;attente pour ce scénario sont visibles uniquement dans **Administrateur > [Cours adaptatif] > Liste d&#39;attente** ; elles n&#39;apparaissent pas dans **Administrateur > Parcours d&#39;apprentissage**. Consultez l’onglet Liste d’attente du cours adaptatif pour gérer les élèves qui étaient sur liste d’attente via un programme d’apprentissage Flex.

Lorsque vous téléchargez le **PDF de rapport de présence** pour une session d’un cours adaptatif qui fait partie d’un parcours d’apprentissage Flex, les élèves inscrits sur liste d’attente apparaissent sous la section **Actif** du PDF. En effet, l’interface du parcours d’apprentissage ne comporte pas de section Liste d’attente distincte. Utilisez **Administrateur > [Cours adaptatif] > Liste d&#39;attente** pour identifier les élèves inscrits sur liste d&#39;attente et les distinguer des participants confirmés avant de marquer leur présence.

### Afficher la liste d’attente

1. Ouvrez le cours adaptatif dans la vue Administrateur.
2. Sélectionnez **Élèves**.
3. Sélectionnez l&#39;onglet **Liste d&#39;attente**.

L’onglet Liste d’attente répertorie les élèves qui sont sur liste d’attente dans un ou plusieurs modules. Pour les cours adaptatifs, le rapport se situe au niveau du module d&#39;instance de cours plutôt qu&#39;au niveau de l&#39;instance de cours, car un élève peut être en cours sur certains modules alors qu&#39;il est en liste d&#39;attente sur d&#39;autres simultanément.

### Effacer la liste d’attente et allouer des places

Lorsqu&#39;une place devient disponible, en raison de la désinscription d&#39;un élève, d&#39;une augmentation de la limite de places ou d&#39;une affectation manuelle, les élèves inscrits sur liste d&#39;attente sont effacés dans l&#39;ordre de la date d&#39;inscription (la date d&#39;inscription la plus ancienne en premier).

Pour allouer manuellement des places à un ou plusieurs élèves :

1. Ouvrez le cours adapté.
2. Sélectionnez l&#39;onglet **Élèves** > **Liste d&#39;attente**.
3. Cochez la case en regard de l’élève ou des élèves pour lesquels vous souhaitez allouer des places.
4. Sélectionnez **Allouer Des Places**.

La sélection de Allouer des places efface l’élève sélectionné de la liste d’attente simultanément dans toutes les sessions sur liste d’attente, et pas seulement dans la session que vous consultez actuellement. Le système suppose que le siège a été physiquement ou virtuellement aménagé pour l’élève.

**Déclencheurs d&#39;effacement de liste d&#39;attente :**

La liste d’attente est automatiquement traitée lorsque l’un des événements suivants se produit :

* Un élève se désinscrit du cours (libérant son siège sur toutes les sessions)
* La limite de sièges pour une session est augmentée
* Un élève change d’instance
* Un administrateur ou un instructeur alloue des places

>[!NOTE]
>
>Lorsque vous créez une nouvelle instance d&#39;un cours adaptatif, l&#39;option **Avertir les élèves inscrits sur liste d&#39;attente** n&#39;est pas disponible. Il s’agit d’un comportement attendu qui diffère des cours normaux.

Dans un cours normal, la liste d&#39;attente est suivie au niveau de l&#39;instance, de sorte que le système peut vous inviter à informer les élèves en attente lorsqu&#39;une nouvelle instance s&#39;ouvre. Dans un cours adaptatif, les listes d&#39;attente sont suivies au niveau de la classe individuelle ou de la classe virtuelle **session**, et non au niveau de l&#39;instance. Il n’existe pas de liste d’attente au niveau de l’instance à avertir lorsqu’une nouvelle instance est créée. L’invite ne s’affiche donc pas et aucune notification automatique n’est envoyée.

## Déclencher l&#39;actualisation pour un cours adaptatif

L’actualisation de l’achèvement dans Adobe Learning Manager permet à l’achèvement du cours adaptatif d’un élève d’être réévalué lorsque ses exigences d’apprentissage changent. Cela est pertinent lorsqu’un groupe d’utilisateurs d’un élève change, lorsqu’un auteur met à jour des règles de module ou lorsqu’un élève souhaite reprendre un cours adaptatif sous son profil actuel.

### Rôle de l’actualisation terminée

Dans un cours adaptatif, l’ensemble de modules obligatoires d’un élève est déterminé par ses groupes d’utilisateurs au moment où il termine le cours. Si ses groupes d’utilisateurs changent ultérieurement ou si l’auteur ajoute de nouveaux modules obligatoires, l’élève peut avoir besoin de compléter du contenu supplémentaire pour répondre aux exigences de son nouveau profil.

L’actualisation permet d’effectuer deux opérations :

1. Annule l’achèvement du cours existant de l’élève s’il a maintenant de nouveaux modules obligatoires qui sont incomplets.
2. Crée un nouvel enregistrement dans le relevé de notes de l’élève représentant l’exigence d’achèvement mise à jour.

![](assets/ac-author-009.png)

L’enregistrement d’achèvement d’origine est conservé dans le relevé de notes de l’élève en tant qu’entrée historique. Les modules précédemment terminés restent terminés. L’élève n’a pas besoin de les répéter, sauf s’il s’agit de nouveaux modules obligatoires qui n’étaient pas visibles ou terminés auparavant.

### Lorsque l’actualisation est terminée

**Scénario 1 : la modification du groupe d’utilisateurs ajoute de nouveaux modules obligatoires**

Un élève termine un cours adapté. Leur groupe d’utilisateurs est modifié ultérieurement et le nouveau groupe d’utilisateurs rend obligatoires les modules précédemment masqués ou facultatifs.

* L’entrée d’achèvement existante reste sur le relevé de notes de l’élève.
* Si l’élève dispose de nouveaux modules obligatoires non terminés, une nouvelle ligne de relevé de notes de l’élève est créée et le cours s’affiche en cours.
* L’élève doit terminer les nouveaux modules obligatoires pour atteindre un nouvel achèvement.

**Scénario 2 : la modification du groupe d’utilisateurs n’entraîne aucun nouveau module obligatoire**

Un élève termine un cours adapté. Leur groupe d’utilisateurs change, mais les exigences du nouveau groupe d’utilisateurs sont déjà satisfaites par leurs finalisations existantes.

* Le cours reste dans un état terminé.
* Aucune nouvelle ligne de relevé de notes de l’élève n’est créée.
* Aucune action n’est requise de la part de l’élève.

**Scénario 3 : reprise initiée par l’élève**

Un élève qui a déjà terminé un cours adaptatif peut choisir de le reprendre pour le terminer dans son profil de groupe d’utilisateurs actuel. Cela est utile lorsque le rôle d’un élève a changé depuis son achèvement initial.

1. L’élève ouvre le cours adaptatif terminé.
2. L’élève sélectionne l’option pour reprendre ou redémarrer le cours.
3. Le cours est réévalué à l&#39;aide de leurs groupes d&#39;utilisateurs actuels afin de déterminer le nouvel ensemble de modules obligatoires.
4. Une nouvelle ligne Relevé de notes de l’élève est créée.

**Scénario 4 : comportement du module de test**

Si un élève a terminé un module de test avant le déclenchement de l&#39;actualisation, la fin du test est toujours valide après l&#39;actualisation. Une fois que le système évalue l’achèvement du cours (déclenché par l’achèvement d’un module ou une action de l’élève), le cours sera à nouveau automatiquement terminé, car le test est déjà terminé, sauf si le cours comporte des modules de contenu obligatoires supplémentaires qui sont maintenant obligatoires et incomplets.

>[!NOTE]
>
>Si une nouvelle session de salle de classe ou de classe virtuelle est ajoutée au cours adaptatif après qu&#39;un élève l&#39;a terminé via le test, et qu&#39;une actualisation est déclenchée par la suite, l&#39;élève peut ne pas apparaître automatiquement dans l&#39;onglet **Présence et notation** ou dans la **Liste d&#39;attente** pour la nouvelle session. Cela se produit car la fin du test maintient le cours dans un état terminé et la logique d&#39;attribution de siège n&#39;est pas relancée. Si vous devez suivre l&#39;assiduité d&#39;un élève à un test pour une nouvelle session ajoutée, allouez son siège manuellement à partir de l&#39;onglet **Liste d&#39;attente**. Notez que les modules de test ne sont pas l’approche recommandée pour les cours adaptatifs.

**Scénario 5 : actualisation déclenchée par l’administrateur**

Un administrateur peut déclencher une fin d’actualisation au nom d’un élève si son profil a changé et que l’administrateur détermine que l’enregistrement d’achèvement existant ne reflète plus les exigences actuelles.

>[!CAUTION]
>
>Si le cours adaptatif fait partie d&#39;une certification récurrente, l&#39;achèvement de l&#39;actualisation s&#39;applique uniquement à l&#39;inscription de l&#39;élève au cycle de certification racine. Les cycles récurrents suivants contiennent une instance distincte du cours adaptatif qui n&#39;est pas affectée par l&#39;actualisation. Les élèves inscrits à un cycle récurrent ne voient pas les mises à jour de module, et leurs achèvements ne sont pas annulés. Si votre organisation utilise des cours adaptatifs dans les certifications récurrentes, communiquez cette limitation aux administrateurs avant de déclencher les fins d&#39;actualisation

1. Ouvrez le profil de l’élève ou l’onglet Élève du cours dans la vue Administrateur.
2. Recherchez l’inscription de l’élève.
3. Sélectionnez **Actualiser la visibilité et l&#39;achèvement**.

ALM réévalue les modules obligatoires en fonction des groupes d&#39;utilisateurs actuels de l&#39;élève et annule l&#39;achèvement si de nouveaux modules obligatoires existent.
