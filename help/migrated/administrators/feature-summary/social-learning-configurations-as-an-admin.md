---
description: En tant qu’administrateur, vous pouvez activer, désactiver et surveiller les activités effectuées dans l’Apprentissage par les réseaux sociaux. Une fois que la fonction d’Apprentissage par les réseaux sociaux est activée, les élèves peuvent la visualiser et commencer à participer à l’Apprentissage par les réseaux sociaux.
jcr-language: en_us
title: Surveillance et modération de l’Apprentissage par les réseaux sociaux en tant qu’administrateur
contentowner: kuppan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3604'
ht-degree: 63%

---



# Surveillance et modération de l’Apprentissage par les réseaux sociaux en tant qu’administrateur

En tant qu’administrateur, vous pouvez activer, désactiver et surveiller les activités effectuées dans l’Apprentissage par les réseaux sociaux. Une fois que la fonction d’Apprentissage par les réseaux sociaux est activée, les élèves peuvent la visualiser et commencer à participer à l’Apprentissage par les réseaux sociaux.

## Activer et configurer les paramètres dans l’Apprentissage par les réseaux sociaux {#enableandconfiguresettingsinsociallearning}

Pour activer et configurer la fonctionnalité d’Apprentissage par les réseaux sociaux, procédez comme suit :

1. Cliquez sur **[!UICONTROL Apprentissage par les réseaux sociaux]** dans le panneau de navigation de gauche. Vous êtes redirigé vers la page d&#39;activité.
1. Activer **[!UICONTROL Apprentissage par les réseaux sociaux]** fonctionnalité utilisant **[!UICONTROL Activer]** dans la page Activité si vous l’activez pour la première fois. Sinon, il peut être activé à partir de **[!UICONTROL Paramètres]** page.

   Une boîte de dialogue contextuelle apparaît comme dans la copie d’écran ci-dessous.

   ![](assets/artboard-20-2x.png) ![](assets/enable-social-learningforthefirsttime.png)

   *Activer l’apprentissage par les réseaux sociaux*

<!-- ![](assets/enable-social-learningfeatureinsettings.png) ![](assets/enable-social-learningdialog.png)-->

L’administrateur peut configurer les paramètres pour l’apprentissage par les réseaux sociaux. Les paramètres incluent des types de certifications de contenu tels que **[!UICONTROL Curation manuelle uniquement]** et **[!UICONTROL Aucune curation]**. Les paramètres d’étendue peuvent être définis sur une étendue différente, comme le type d’utilisateur (interne/externe) ou tout autre champ actif présent dans le compte. L’administrateur peut définir le chemin d’URL à partir duquel les élèves peuvent télécharger l’application de bureau Adobe Learning Manager.

## Curation de contenu {#contentcuration}

L’Apprentissage par les réseaux sociaux étant un apprentissage informel, ses fonctionnalités sont similaires à celles d’autres plateformes de médias sociaux. Les gens trouvent souvent les médias sociaux distrayants parce qu&#39;ils consomment souvent du contenu non pertinent qui affecte leur productivité. Cette pensée peut être prise en compte par la modération du contenu et la curation.

**[!UICONTROL Curation manuelle uniquement]** et **[!UICONTROL Aucune curation]** sont deux options de curation qui peuvent être sélectionnées par l’administrateur.

**[!UICONTROL Curation manuelle à assistance automatique]:** Learning Manager dispose d’un moteur d’auto-curation basé sur l’intelligence artificielle qui peut trouver intelligemment l’essence du contenu de n’importe quel format qui peut être ultérieurement diffusé aux élèves souhaités. Il peut également approuver ou rejeter la publication d’un contenu en fonction de son score de confiance donné.

Par exemple, Adarsh est un élève et il a trouvé un blog intéressant, il le publie donc sur la plateforme d’apprentissage par les réseaux sociaux d’Adobe Learning Manager. La publication est ensuite transmise au moteur de curation de contenu alimenté par l’IA, qui prédit les compétences présentes dans le contenu et compare ces compétences avec les compétences associées au forum. Si l’une des compétences correspond, le contenu est publié, sinon il est envoyé pour une curation manuelle uniquement.

Le score de confiance minimum requis pour l’affichage est de 50 %.

**[!UICONTROL Curation manuelle uniquement]:** Pour vérifier l’authenticité du contenu avant sa mise en ligne, l’administrateur peut activer le paramètre Curation manuelle uniquement. Une fois que le paramètre Curation manuelle uniquement est activé, il est transféré aux meilleurs experts (3 maximum) pour la curation. Sur la base de la réponse moyenne, la publication est approuvée/rejetée en conséquence. Si la réponse est supérieure à 50 %, la publication en direct est rejetée. Pour plus d’informations sur les experts, [cliquez ici](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

## Auto-curation du contenu {#autocuration}

La modération manuelle du contenu est souvent chronophage et sujette aux erreurs. En outre, le processus n’est pas évolutif et ne convient pas à un volume élevé d’activités sur les réseaux sociaux. Par conséquent, l’auto-curation du contenu devient essentielle pour servir de nombreux utilisateurs actifs sur les réseaux sociaux.

Dans Learning Manager, il existe une option permettant de conserver automatiquement le contenu. La curation est pilotée par un moteur compatible avec l’IA, qui mappe les travaux avec les compétences prédéfinies, après que l’administrateur a mappé les compétences prédéfinies avec une compétence. Pour plus d’informations, voir [Mappage du domaine de compétence](curation-skills.md).

Dans l’auto-curation, les types de contenu suivants sont autorisés :

* PDF
* Fichiers audio et vidéo
* Présentations au format PPT ou PPTX
* Documents au format .doc, .docx

Un administrateur peut activer l’option permettant de conserver automatiquement le contenu à partir de l’application Administrateur.

1. Dans le volet de gauche de l’application Administrateur, cliquez sur **[!UICONTROL Apprentissage par les réseaux sociaux]**.
1. Sur la page, cliquez sur l’onglet **[!UICONTROL Paramètres]**.
1. Activez l’option **[!UICONTROL Curation manuelle à assistance automatique]**.

   ![](assets/auto-curation.png)

   *Sélectionnez l’option Curation manuelle à assistance automatique*

Lorsqu’un utilisateur télécharge un contenu sur un forum, un algorithme basé sur l’IA extrait le texte du contenu puis le texte est ensuite transmis au moteur de curation. Le moteur de curation essaie de trouver les compétences présentes dans le contenu.

Les compétences prévues du contenu téléchargé sont mises en correspondance avec celles du forum dans lequel le contenu a été téléchargé.  Si une compétence correspond à un score de confiance supérieur à 50 % de la compétence du forum, le contenu est publié dans le forum. Si le score de confiance est inférieur à 50 %, le contenu est envoyé pour curation manuelle.

Chaque fois qu’un contenu est conservé automatiquement, l’utilisateur reçoit une notification l’informant que le contenu est disponible sur le forum sur lequel il a été précédemment téléchargé.

![](assets/only-ai-based.png)

*Organigramme des paramètres de curation*

Il est recommandé que l’administrateur ajoute des experts pour des compétences si la Curation manuelle uniquement est activée. L’administrateur peut ajouter des experts en fournissant à l’avance des points d’experts aux utilisateurs possédant une expertise dans une compétence. Pour en savoir plus sur la manière de fournir des points aux PME,  [cliquez ici](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

**Aucune curation :** Toutes les publications des élèves sont automatiquement publiées sans aucune modération de contenu.

<!--![](assets/artboard-6-2x.png)-->

## Questions fréquentes sur l&#39;auto-curation du contenu {#faq-auto-curation}

+++Combien de temps l’expert dispose-t-il pour organiser une publication ?

Un expert dispose d&#39;au moins 24 heures à consacrer à la curation d&#39;une publication. En raison des différences de fuseau horaire, elle peut être portée à 47 heures.

+++

+++Est-ce qu&#39;on passe à la prochaine série de trois PME si les trois sont disponibles? Est-ce toujours trois experts qui sont impliqués ?

Le premier jour, la demande de curation est adressée aux experts principaux. S&#39;ils ne répondent pas, la demande est adressée aux trois experts suivants le lendemain.

Si les trois nouveaux experts ne répondent pas, la demande est adressée aux modérateurs du conseil.

Si les modérateurs du forum ne répondent pas, la demande est automatiquement approuvée.

+++

+++Si deux experts procèdent à la curation et que l’autre ne le fait pas, la demande est-elle adressée au quatrième expert ou prend-elle la moyenne de ce que le premier ensemble d’experts évalue comme publication ?

Une évaluation d&#39;approbation de 50 % est requise pour approuver la publication. De même, une évaluation de rejet de 50 % est utilisée pour rejeter la publication. Chaque approbation effectuée par un expert est évaluée si elle a atteint 50 %.

Si elle n&#39;atteint pas 50 % après un jour, elle est envoyée à l&#39;ensemble suivant d&#39;experts, menant à l&#39;expiration des précédentes demandes de curation sans réponse.

Par exemple, le premier jour, la demande de curation est envoyée à trois experts. L&#39;un d&#39;eux l&#39;approuve et deux n&#39;ont pas répondu. Le jour suivant, la demande de curation est adressée à trois experts à ce niveau, il y a maintenant quatre experts actifs au total. Au moins deux experts doivent l&#39;approuver pour que le curation soit approuvée.(S&#39;il y a 2 approbations et 2 rejets, la première catégorie à atteindre 50 % en premier sera prise en compte.)

+++

+++ D&#39;après ce que je vois, un « modérateur » n&#39;est affecté (et ce n&#39;est pas obligatoire) que lorsqu&#39;une personne crée un nouveau forum. Quel est l&#39;intérêt pour un élève d&#39;affecter un « modérateur » à un forum si des experts seront affectés à la compétence à laquelle un forum est associé ?

Les responsabilités suivantes incombent à un modérateur de Forum de réseau social :

* Possibilité de modifier le nom, la description, les paramètres de visibilité du forum et d’autres paramètres de configuration.
* Possibilité de supprimer une publication dans le forum au cas où celle-ci ne conviendrait pas au public.
* Le modérateur reçoit des notifications « Signaler un abus » pour le forum.
* Le modérateur reçoit des demandes de curation si aucun expert n&#39;est présent pour le forum.

+++

+++Notre équipe de formation ajoutera/surveillera les compétences associées au niveau de compétence ainsi que les experts affectés aux compétences.

Les experts sont ajoutés/affectés en fonction des compétences, et non du niveau de compétence. C&#39;est comme prévu.

+++

+++ Quelle est la différence entre un « modérateur » d’apprentissage par les réseaux sociaux et un « expert » d’apprentissage par les réseaux sociaux ?

**Modérateurs :** propriétaires secondaires du forum. Ils sont ajoutés par les créateurs lors de la création du forum afin de pouvoir contrôler le forum en l&#39;absence du créateur. Par défaut, le créateur du forum est le modérateur.

**PME :** Les experts sont des experts dans des compétences spécifiques. L’administrateur peut affecter des experts à une compétence particulière pour organiser le contenu de cette compétence. Les experts reçoivent les demandes de curation de forums liés à leurs compétences. Les élèves peuvent également devenir des experts en gagnant des points.

+++

+++S’il y a deux ou trois experts affectés à une compétence : l’approbation ou le rejet d’un post Apprentissage par les réseaux sociaux dépend-il de la curation de tous les experts ou du curateur en premier ?

Une évaluation d&#39;approbation de 50 % est requise pour approuver la publication. De même, une évaluation de rejet de 50 % est utilisée pour rejeter la publication. Chaque approbation effectuée par un expert est évaluée si elle a atteint 50 %.

Si elle n&#39;atteint pas 50 % après un jour, elle est envoyée à l&#39;ensemble suivant d&#39;experts, menant à l&#39;expiration des précédentes demandes de curation sans réponse.

+++

## Paramètres de l’étendue {#scopesettings}

Dans l’Apprentissage par les réseaux sociaux, le paramètre de l’étendue détermine les forums que vous voyez, ce qui contrôle la visibilité du contenu. Si un utilisateur a une portée, par exemple, ***Vendor_A***, il/elle ne peut voir que les forums et les publications associées qui ont été créés par d’autres personnes appartenant à la même portée ***Vendor_A***.

Cela permet aux administrateurs de gérer un groupe d’utilisateurs, par exemple, des fournisseurs, des partenaires ou des départements dans une organisation séparée.

Activez l’apprentissage par les réseaux sociaux et le tableau des scores pour les utilisateurs internes et externes.

Des sections séparées sont prévues pour autoriser les utilisateurs internes et externes.

**Activer pour les élèves internes**

Dans cette section, vous pouvez choisir la caractéristique de l’utilisateur pour définir l’étendue de l’apprentissage par les réseaux sociaux pour les utilisateurs internes. Utilisateurs ayant les mêmes caractéristiques **valeur** partager le même espace Apprentissage par les réseaux sociaux.

À partir de **Caractéristique de l’utilisateur** dans la liste déroulante, sélectionnez l’option requise.

![](assets/choose-value-of-usercharacteristic.png)

*Sélectionner les caractéristiques de l’utilisateur pour définir l’étendue*

Par défaut, l’option **[!UICONTROL Tous les utilisateurs internes]** dans la liste déroulante des caractéristiques de l’utilisateur, l’option est toujours sélectionnée.

Vous pouvez définir les utilisateurs internes en fonction de leurs champs actifs.

**Activer pour les élèves externes**

Pour définir l’étendue de l’apprentissage pour les utilisateurs externes, utilisez un profil externe. Les élèves ayant le même profil externe partagent un espace commun d’apprentissage par les réseaux sociaux.

![](assets/choose-an-externalprofile.png)

*Activer l’étendue pour les élèves externes*

Les utilisateurs externes sont évalués en fonction de leurs profils externes.

Par exemple, dans la liste ci-dessus, si vous activez **[!UICONTROL Acme Corp]**, tous les élèves appartenant à Acme Corp peuvent voir les forums qu’ils ont créés. Si vous désactivez l’option **Henry Cavill**, les élèves ne peuvent voir aucun forum créé par Henry Cavill.

L’administrateur peut étendre la visibilité du contenu en fonction du champ actif affiché dans le champ **[!UICONTROL Caractéristique utilisateur]**.

Par exemple, l’administrateur peut définir l’étendue sur **[!UICONTROL Type d’utilisateur (interne/externe)]** utilisateurs. Lors de la définition de l’étendue sur Type d’utilisateur, le contenu partagé sur la plateforme d’apprentissage par les réseaux sociaux par n’importe quel élève interne n’est visible que par les autres élèves internes de l’organisation et non par les utilisateurs externes et inversement.

Une fois qu’une caractéristique d’utilisateur est sélectionnée par l’administrateur, ce dernier peut limiter la fonctionnalité d’Apprentissage par les réseaux sociaux aux élèves et aux groupes d’élèves en cochant la case située sous le champ Caractéristique de l’utilisateur. Cliquez sur le champ de valeur pour sélectionner l’élève ou les groupes d’élèves pour lesquels vous souhaitez activer la fonctionnalité d’Apprentissage par les réseaux sociaux.

Par défaut, la portée est définie par **[!UICONTROL Type d’utilisateur]** qui sont des élèves internes ou externes.

Si le champ actif ne contient aucune valeur, la liste déroulante du champ **[!UICONTROL Valeur]** n’est pas visible pour l’administrateur.

<!--![](assets/scope-settings.png) ![](assets/scope-settings1-png.jpg)-->

Les utilisateurs peuvent également publier leur contenu à l’aide de l’application de bureau Adobe Learning Manager. En fonction de ce que vous utilisez, Mac ou Windows, cliquez sur les liens donnés pour télécharger l’application de bureau et suivez les étapes décrites pour l’installer sur votre système. Si vous êtes confrontés à des difficultés d’installation, [cliquez ici](../../kb/troubleshooting-issues-with-adobe-learning-manager-desktop-app.md).

## Autorisations de création de forums {#permission}

Pour restreindre la création de forums par tous les élèves et pour modérer efficacement les forums, un administrateur peut accorder des autorisations pour créer des forums dédiés à un groupe d’utilisateurs sélectionné.

![](assets/grant-permissiontocreateboards.png)

*Définir les autorisations pour créer un forum*

Par défaut, l’option **[!UICONTROL Tous les élèves]** est activée.

**[!UICONTROL Tous les élèves]:** Si vous choisissez cette option, tous les utilisateurs internes et externes peuvent créer des tableaux.

**Un groupe d’élèves :** si vous sélectionnez cette option, seuls les utilisateurs ayant les autorisations de créer un forum voient le lien **[!UICONTROL Créer un nouveau forum]** dans l’Apprentissage par les réseaux sociaux. Choisissez le groupe d’utilisateurs auquel vous devez accorder l’autorisation de créer un forum. Vous pouvez également ajouter des groupes d’utilisateurs générés automatiquement ainsi que des groupes personnalisés.

<!--![](assets/grant-permissiontoausergroup.png)-->

Les utilisateurs qui partagent la même étendue peuvent uniquement voir le forum. Pour les utilisateurs qui n’ont pas obtenu d’autorisation, le lien **[!UICONTROL Créer un nouveau forum]** reste invisible.

Patientez 60 minutes pour que les modifications prennent effet.

## Utilisateurs spéciaux {#privilege}

Un administrateur peut accorder des privilèges spéciaux à un groupe d’utilisateurs, en utilisant les membres du groupe qui peuvent participer à tous les forums. Toutes les restrictions qui ont été définies dans la section Paramètres de l’étendue sont contournées par le groupe d’utilisateurs spéciaux.

Le groupe d’utilisateurs peut être généré automatiquement ou personnalisé.

Un utilisateur auquel ce privilège a été accordé a accès à tous les forums, à l’exception des **forums privés**.

![](assets/special-users.png)

*Octroi de privilèges spéciaux*

Lorsque l’administrateur sélectionne un groupe d’utilisateurs, par défaut, tous les utilisateurs du groupe peuvent accéder à tous les forums, quelle que soit l’étendue de l’utilisateur. Tout utilisateur bénéficiant de ces privilèges élevés peut afficher tous les forums internes et externes et y participer.

Les utilisateurs spéciaux reçoivent des demandes de curation dans toutes les étendues si les utilisateurs ont suffisamment de points d’expert pour cette compétence.

Si l’utilisateur n’a pas les points d’expert requis, les privilèges de curation sont transmis aux trois premiers experts de cette compétence.

Dans la nouvelle étendue, il/elle obtient des points pour des activités sur les forums.

Dans les sections Tableau des scores des réseaux sociaux, un utilisateur peut voir tous les utilisateurs de son étendue ainsi que les utilisateurs spéciaux.

Si vous avez obtenu des privilèges d’utilisateur spécial, vous pouvez voir tous les utilisateurs dans le compte de votre tableau des scores, indépendamment de l’étendue des utilisateurs.

Si des utilisateurs spéciaux deviennent des experts en gagnant suffisamment de points, ils apparaissent dans le panneau **[!UICONTROL Experts en la matière]** dans le tableau des scores sociaux.

Patientez 60 minutes pour que les modifications prennent effet.

## Personnalisation de la bannière pour réseaux sociaux {#customize-social-banner}

L’administrateur peut personnaliser le titre et le sous-titre qui apparaissent sur l’image d’en-tête sur la page d’accueil Apprentissage par les réseaux sociaux. Quelle que soit la décision de l’administrateur de saisir le titre et le sous-titre, les mêmes fonctionnalités sont disponibles sur la page d’accueil de l’apprentissage par les réseaux sociaux de l’élève.

1. Dans l’application d’administration, cliquez sur **[!UICONTROL Apprentissage par les réseaux sociaux]** > **[!UICONTROL Paramètres]**.
1. Cliquez sur **[!UICONTROL Personnaliser]**.
1. Modifiez l’image de la bannière. Les dimensions de l&#39;image doivent être au moins **1 600 x 240 px**.
1. Activez/désactivez l’option permettant de masquer ou d’afficher les **[!UICONTROL En savoir plus]** lien sur la bannière.
1. Saisissez le titre et le sous-titre dans les champs spécifiés ci-dessous :

   ![](assets/image012.png)

   *Personnalisation de la bannière pour réseaux sociaux*

Vous disposez de quelques options supplémentaires :

* **[!UICONTROL Langue]:** Dans la liste déroulante, sélectionnez la langue vers laquelle traduire le titre et le sous-titre. Vous pouvez également ajouter du texte personnalisé pour différentes langues.
* **[!UICONTROL Répliquer]:** Cliquez sur ce bouton pour répliquer le titre et le sous-titre dans toutes les langues.
* **[!UICONTROL Réinitialiser]:** Cliquez sur ce bouton pour revenir au titre et au sous-titre d’origine.

Sur la page d’accueil de l’apprentissage par les réseaux sociaux, les informations fournies par l’administrateur s’affichent en tant qu’en-tête de page.

<!--![](assets/banner-learner.png)-->

## Tendances {#trends}

Les tendances de l’activité sociale de l’élève peuvent être affichées et suivies dans l’onglet Activité de la section Tendances. Ces données peuvent être visualisées pour différentes périodes telles que les sept derniers jours, le mois dernier, les trois derniers mois et tous les temps.

Sept derniers jours est la valeur par défaut dans le filtre de dates.

>[!NOTE]
>
>Sept derniers jours est la valeur par défaut dans le filtre de dates.

Le premier visuel fournit à l’administrateur les informations suivantes pour la période sélectionnée dans le filtre de dates :

1. **[!UICONTROL Nouvelles publications]** : affiche le nombre de nouvelles publications créées au cours de la période. Le nombre total de publications pour toute la période est également affiché.
1. **[!UICONTROL Pourcentage d’utilisateurs actifs]** : affiche le pourcentage total d’utilisateurs actifs dans l’apprentissage par les réseaux sociaux par rapport au nombre total d’utilisateurs disponibles dans le compte.
1. **[!UICONTROL Nouveaux tableaux]**: affiche le nombre de nouveaux tableaux créés. Le nombre total de tableaux pour toute la période est également affiché.

Le deuxième visuel est un graphique linéaire affichant la tendance du nombre de forums ou de publications créés en fonction de la période sélectionnée dans le filtre de dates. Cliquez sur le filtre pour afficher les différentes options de temps comme les sept derniers jours, le dernier mois, les trois derniers mois et tous les temps.

![](assets/trends.png)

*Graphique linéaire affichant la tendance*

## Compétences {#skills}

Vous pouvez afficher toutes les compétences utilisées dans la plateforme d’activités sociales dans cette section. L’administrateur peut utiliser le champ de recherche pour rechercher une compétence qui n’est pas encore utilisée lors de la création d’un forum et du mappage des experts. En effectuant cette opération, les experts recevraient une notification lors de la création d’un forum utilisant cette compétence et pourraient examiner la publication dans le cadre du processus de curation manuelle.

Pour un compte avec l’Apprentissage par les réseaux sociaux désactivé, aucune compétence n’est affichée. La barre de recherche est disponible pour ces comptes afin que l’administrateur dispose des fonctionnalités lui permettant de rechercher une compétence et d’y ajouter des experts.

L’administrateur peut afficher le score d’activité, le nombre de publications, les forums, les utilisateurs et le nom des experts pour chaque compétence utilisée lors de la création d’un forum ou d’une publication.

<!--![](assets/modify-smes-2.png)-->

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Appr. Rés. Soc. N°</b></p></td>
   <td>
    <p><b>Nom de la colonne</b></p></td>
   <td>
    <p><b>Explication</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Nom de la compétence</p></td>
   <td>
    <p>Affiche les noms des compétences utilisées dans Apprentissage par les réseaux sociaux.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Score d’activité</p></td>
   <td>
    <p>Affiche la somme des points d’activité de tous les forums qui appartiennent à la compétence.</p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Publications</p></td>
   <td>
    <p>Affiche le nombre total de publications créées à l’aide d’une compétence.</p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Forums</p></td>
   <td>
    <p>Affiche le nombre total de forums créés à l’aide d’une compétence.</p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>Utilisateurs</p></td>
   <td>
    <p>Affiche le nombre total d’élèves ayant utilisé cette compétence.</p></td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>Experts</p></td>
   <td>
    <p>Affiche les 3 principaux experts actuels pour cette compétence. L’administrateur peut ajouter ou modifier des experts en cliquant sur le lien.</p></td>
  </tr>
 </tbody>
</table>

## Domaine de compétence {#skilldomain}

En se basant sur les compétences principalement utilisées par les utilisateurs finaux de Learning Manager, Adobe Learning Manager a classé une liste de 25 domaines de compétences que le système de curation automatique utilise pour curer le contenu. L’administrateur doit mapper les compétences d’entreprise configurées aux domaines de compétence fournis par Prime. Le mappage des compétences peut être effectué à partir de la page des compétences d’administrateur lors de la création d’une compétence ou en modifiant une compétence existante. Pour plus d’informations sur la façon de mapper ou d’ajouter une compétence, [cliquez ici](skills-levels.md#Createaskillandalevel).

+++Liste des domaines de compétence utilisés par le système de curation de Learning Manager

1. Comptabilité
1. Analyses
1. Éthique professionnelle
1. Droit des affaires
1. Processus professionnels
1. Sécurité informatique
1. Gestion de la relation client
1. Conception
1. Finance
1. Gestion des ressources humaines
1. Technologies de l’information
1. Apprentissage
1. Gestion
1. Marketing
1. Santé
1. Production et fabrication
1. Gestion qualité
1. Ventes
1. Recherche scientifique et ingénierie
1. Médias sociaux
1. Savoir-être
1. Gestion stratégique
1. Gestion de la chaîne logistique
1. Communication technique
1. Sécurité au travail

+++

## Experts {#subjectmatterexpertssmes}

**Experts** Ce sont des gens qui ont une connaissance et une expertise considérables dans une compétence. Une **PME** joue un rôle important dans l’apprentissage par les réseaux sociaux lorsque l’administrateur a défini les paramètres de curation comme manuels ou lorsque la méthode d’auto-curation ne parvient pas à curer le contenu. Seuls les trois premiers experts sont affichés dans la colonne Expert.

## Conditions pour être un expert {#requirementstobeansme}

Le statut d’expert ne peut être obtenu qu’en accumulant des points d’experts dans le cadre d’activités d’apprentissage par les réseaux sociaux. L’administrateur peut attribuer des points à un expert en fonction de son expertise dans le niveau de compétence.

## Ajout d’experts à une compétence {#addingsmestoaskill}

Pour ajouter des experts à une compétence, suivez les étapes indiquées :

1. Cliquez sur **[!UICONTROL Ajouter des experts]** ou **[!UICONTROL Modifier des experts]**.

   ![](assets/add-smes-06.png)

   *Ajout ou modification d’un fichier SME*

1. Cliquez sur **[!UICONTROL Options avancées]** dans la boîte de dialogue contextuelle.

   ![](assets/advanced-optionssmes.png)

   *Boîte de dialogue Afficher les options avancées*

1. Recherchez l’utilisateur ayant une expertise dans la compétence. Une fois l’utilisateur trouvé, saisissez le nombre de points que vous souhaitez lui accorder dans la zone **Ajouter des points** zone de saisie.

   Si l’utilisateur a déjà des points, le nombre de nouveaux points attribués à l’utilisateur est ajouté au nombre actuel de points.

   Par défaut, pour chaque nouvel utilisateur d’Apprentissage par les réseaux sociaux, le point actuel est 0.

   ![](assets/advanced-options.png)

   *Ajout de points pour un utilisateur*

1. En cochant la case **[!UICONTROL Activer le minimum de points d’experts]**, vous pouvez définir une limite au nombre minimal de points qu’un utilisateur doit afficher en tant qu’expert dans la liste des meilleurs experts. Une fois la valeur seuil définie, les experts dont le nombre de points est inférieur ou égal à la valeur minimale requise ne sont pas répertoriés dans les listes d’experts.

   Si le **[!UICONTROL Activer le nombre minimum de points SME]** Si la case n’est pas cochée, les trois premiers utilisateurs avec les points les plus élevés sont considérés comme les experts pour cette compétence particulière.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour afficher les modifications qui ont été apportées.

## Système de points d’experts {#smepointsystem}

**Les experts reçoivent des points en fonction des éléments suivants :**

* 2 points sont attribués à un utilisateur chaque fois qu’un autre utilisateur évalue une publication créée par lui.
* 2 points sont attribués à un utilisateur chaque fois qu’un autre utilisateur donne un vote positif à son commentaire.
* 5 points sont attribués à un élève pour répondre à une question.
* 2 points supplémentaires sont attribués à l’élève chaque fois que la réponse fournie reçoit un vote positif.

## Points de statut expert basés sur l’activité de curation {#smestatuspointsbasedoncurationactivity}

**Les experts reçoivent des points en fonction des activités de curation pour les éléments suivants :**

* Lorsqu’une publication est envoyée pour une curation manuelle parce que l’auto-curation ne garantit pas que le contenu est pertinent ou non, l’expert gagne 5 points lors de la soumission de la modération.

## Télécharger des configurations {#downloadconfigurations}

<!--![](assets/download-config.png)-->

Pour les serveurs d’entreprise, l’administrateur peut modifier l’emplacement depuis lequel les élèves peuvent télécharger l’application de bureau pour Windows et Mac.

![](assets/enterprise-servers.png)

*Modification de l’emplacement de téléchargement*

L’URL du serveur d’entreprise doit être hébergée publiquement.

## Activités sociales pour la facturation mensuelle des utilisateurs actifs {#socialactivitiesformonthlyactiveusersbillingplan}

Chaque fois qu&#39;un utilisateur crée un nouveau forum de réseaux sociaux, une publication de réseaux sociaux ou un commentaire sur les réseaux sociaux, cela est considéré comme une activité valide à comptabiliser dans le **Utilisateur de l’activation mensuelle**(MAU) plan si le compte suit le modèle de facturation MAU. Pour plus d’informations, reportez-vous à la [gestion de la facturation](billing-management.md).

## Forum aux questions {#frequentlyaskedquestions}

+++Comment activer l’apprentissage par les réseaux sociaux pour les élèves externes ?

Entrée **[!UICONTROL Apprentissage par les réseaux sociaux]** > **[!UICONTROL Paramètres]**, dans la section Paramètres d’étendue, activez l’option **[!UICONTROL Activer pour les élèves externes]**. Dans la liste déroulante, choisissez un profil externe et définissez l’étendue d’apprentissage pour ce profil

![](assets/social-scope-external-users.png)

*Sélectionnez l’option Activer pour les élèves externes*
+++
