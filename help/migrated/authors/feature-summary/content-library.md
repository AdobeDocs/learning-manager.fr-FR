---
description: Apprenez à créer un contenu aligné sur les cours en tant que contenu d’auto-apprentissage.
jcr-language: en_us
title: Bibliothèque de contenu
exl-id: cc19eca6-6b47-44b2-ad23-2d7ad8975f65
source-git-commit: c1231f48c87c14f7b3acd23b0c0d5e93f0cc692c
workflow-type: tm+mt
source-wordcount: '3124'
ht-degree: 57%

---

# Bibliothèque de contenu

Apprenez à créer un contenu aligné sur les cours en tant que contenu d’auto-apprentissage.

## Bibliothèque de contenu {#contentlibrary}

Le contenu est la base de tout cours. Les auteurs créent une bibliothèque de contenus qui peut être alignée sur les cours en tant que contenu d’auto-apprentissage. Seuls les auteurs ont accès à cette bibliothèque de contenus.

## Types de contenu pris en charge {#supported}

Vous pouvez charger le contenu interactif et le contenu statique dans la bibliothèque.

Le tableau ci-dessous affiche les types de fichiers interactifs et statiques que vous pouvez télécharger dans la bibliothèque.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Contenu interactif</b></p></td>
   <td>
    <p><b>Type de contenu</b></p></td>
   <td>
    <p><b>Extensions</b></p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p></p>
    <ul>
     <li>SCORM 1.2</li>
     <li>SCORM 2004</li>
     <li>AICC</li>
     <li>TinCan</li>
    </ul>
    <p></p></td>
   <td>
    <p>zip</p></td>
  </tr>
  <tr>
   <td>
    <p><b>Contenu statique</b></p></td>
   <td>
    <p><b>Type de contenu</b></p></td>
   <td>
    <p><b>Extensions</b></p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>Vidéo</p></td>
   <td>
    <p>mp4, wmv, 3gp, 3g2, 3gp2, asf, avi, f4v h264, mpe, mpeg, mpg, mpg2, m4v, mov, wmv</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>Audio</p></td>
   <td>
    <p>mp3, wav, aac, m4a, wma, vorbis, pcm, eac3, amr, ac3</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>PDF</p></td>
   <td>
    <p>pdf</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>MS PowerPoint</p></td>
   <td>
    <p>pptx, ppt</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>MS Word</p></td>
   <td>
    <p>docx, doc</p></td>
  </tr>
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>MS Excel</p></td>
   <td>
    <p>xlsx, xls</p></td>
  </tr>
 </tbody>
</table>

## Ajouter du nouveau contenu dans la bibliothèque {#addnewcontentinthelibrary}

**Auteurs** peut ajouter des contenus dans ALM. Il existe deux types de contenu dans ALM : **[!UICONTROL Contenu]** et **[!UICONTROL Quiz]**. Pour savoir comment ajouter des contenus, voir [Ajout de contenu statique](content-library.md#addstaticcontent) et [Créer un quiz](content-library.md##createaquiz).

## Ajouter du contenu statique {#addstaticcontent}

1. Sélectionner **[!UICONTROL Bibliothèque de contenu]** dans le volet de gauche après vous être connecté en tant que **Auteur** et sélectionnez **[!UICONTROL Ajouter]**.

   Vous pouvez également sélectionner **[!UICONTROL Créer du contenu]** à partir du **[!UICONTROL Prise en main]** page.

1. Dans le panneau **[!UICONTROL Nom]** , saisissez un nom pour le contenu que vous souhaitez télécharger.
1. Dans le panneau **[!UICONTROL Description]** , saisissez la description du contenu. Assurez-vous que la description que vous voulez saisir est significative. La limite de caractères est de 400 caractères.
1. Pour ajouter le contenu, sélectionnez **[!UICONTROL Ajouter un fichier de contenu]**, puis téléchargez votre fichier de ressources. Lorsque vous ajoutez du contenu dans diverses langues, vous ne pouvez pas combiner le contenu statique et le contenu interactif dans un même groupe. L’ensemble de votre contenu dans toutes les langues doit être soit statique, soit interactif.

   Si vous voulez remplacer le contenu, vous pouvez remplacer un contenu statique par un contenu statique différent. Le même procédé peut s’appliquer au contenu interactif.

1. Dans le panneau **[!UICONTROL Durée]** vous pouvez éventuellement saisir le temps qu’un élève doit passer dans ce module. La durée est calculée en minutes.

   Le temps d’apprentissage de l’élève est calculé sur la base de la durée spécifiée si l’élève a indiqué qu’un cours est terminé. Si l’élève utilise le contenu du lecteur, le temps passé dans le lecteur est ajouté au temps d’apprentissage passé. Si la durée réelle du contenu est inférieure à la durée spécifiée, rien ne se passe car le lecteur respecte toujours la durée d’affichage du contenu.

1. Dans le panneau **[!UICONTROL Balises]** , saisissez les balises du contenu téléchargé afin que votre contenu puisse être découvert.

   Un auteur peut utiliser ces balises pour rechercher le contenu lors de l&#39;ajout du contenu au cours.

### Contrôle de version {#versioning}

La bibliothèque de contenus maintient également le contrôle de version de vos contenus téléchargés. Si vous apportez des modifications au contenu, par exemple une présentation PowerPoint, et que vous téléchargez à nouveau le PPT dans la bibliothèque, le numéro de version est incrémenté d’une unité. Cela vous aide à suivre l’évolution de votre contenu.

## Ajouter du contenu interactif {#addinteractivecontent}

1. Sélectionner **[!UICONTROL Bibliothèque de contenu]** dans le volet de gauche après vous être connecté en tant que **Auteur** et sélectionnez **[!UICONTROL Ajouter]**.

   Vous pouvez également sélectionner **[!UICONTROL Créer du contenu]** à partir du **[!UICONTROL Prise en main]** page.

1. Dans le panneau **[!UICONTROL Nom]** , saisissez un nom pour le contenu que vous souhaitez télécharger.
1. Dans le panneau **[!UICONTROL Description]** , saisissez la description du contenu. Assurez-vous que la description que vous voulez saisir est significative. La limite de caractères est de 245 caractères.
1. Pour ajouter le contenu, sélectionnez **[!UICONTROL Ajouter un fichier de contenu]**, puis téléchargez votre fichier de ressources. Lorsque vous ajoutez du contenu dans diverses langues, vous ne pouvez pas combiner le contenu statique et le contenu interactif dans un même groupe. L’ensemble de votre contenu dans toutes les langues doit être soit statique, soit interactif.

* [Types de fichiers pris en charge](content-library.md#supported)

  Le contenu interactif peut être une option SCORM, AICC ou un projet publié Captivate. Ce fichier doit être un fichier zip.

  Vous pouvez également ajouter du contenu HTML généré à partir de Captivate, Presenter ou Presenter Video Express.

1. Learning Manager prend en charge les légendes du contenu vidéo chargé dans Learning Manager. Désormais, les auteurs peuvent charger le fichier contenant les légendes, ainsi que le fichier vidéo.

   Les élèves peuvent ensuite afficher les légendes pendant la lecture du module vidéo.

   Le format pris en charge est  [Pistes de texte des vidéos web (webVTT)](https://www.w3.org/TR/webvtt1/).

   La prise en charge des légendes est disponible pour le contenu vidéo chargé dans la bibliothèque de contenu dans Learning Manager.

   En tant qu’auteur, lorsque vous chargez un contenu vidéo ou audio, vous pouvez également charger le fichier VTT qui contient les sous-titres.

   Les sous-titres apparaissent ensuite dans le lecteur Fluidic. Les légendes sont également conformes à [normes WCAG2.0](https://www.w3.org/TR/WCAG20/).

   Lorsque vous ajoutez un contenu vidéo à la bibliothèque, vous pouvez également ajouter le fichier VTT, qui **incontournable** être un fichier valide.

   ![](assets/webvtt.png)

   *Ajout d’un fichier webvtt*

   Le fichier VTT chargé correspond à la version existante du contenu. Ainsi, le fichier webVTT chargé ne renvoie pas à l’ancienne version du contenu.

   Si vous créez le contenu dans différentes langues, vous pouvez charger un fichier webVTT différent pour chaque langue. Les élèves pourront voir les légendes correspondant à la langue sélectionnée pendant la lecture.

   >[!NOTE]
   >
   >   Un fichier VTT prend en charge une langue. Pour prendre en charge plusieurs langues, chargez plusieurs fichiers vidéo pour chaque langue de contenu, puis chargez son fichier VTT respectif pour chaque fichier vidéo.

   En tant qu’auteur, chaque fois que vous modifiez le contenu, la vidéo ou l’audio, Learning Manager vous invite à créer un fichier vtt.

   Après avoir ajouté ce contenu à un cours et lorsque vous affichez un aperçu du cours en tant qu’élève, vous pouvez voir les légendes sur la vidéo.

   Sur le lecteur, activez ou désactivez le bouton CC sur le lecteur Fluidic pour afficher ou masquer les légendes.

   La même vue apparaît dans **l&#39;application de l&#39;élève** ainsi que dans **Aperçu en tant qu&#39;élève**.

   Lorsque vous **ajouter, mettre à jour ou supprimer** dans le fichier vtt, vous recevez une notification.
La prise en charge de WebVTT n’est pas disponible pour :

   1. Annonces vidéo.
   1. Vidéo lue dans le contenu de formation en ligne. Cela dépend du contenu.
   1. Vidéo téléchargée dans l&#39;apprentissage par les réseaux sociaux.
   1. Vidéo créée dans l’application de bureau Learning Manager.
   1. Contenu vidéo créé à l’aide du processus de migration.
   1. Lecture vidéo dans l’application mobile en mode hors ligne.

1. Dans le panneau **[!UICONTROL Durée]** vous pouvez éventuellement saisir le temps qu’un élève doit passer dans ce module. La durée est calculée en minutes.
1. Dans le panneau **[!UICONTROL Balises]** , saisissez les balises du contenu téléchargé afin que votre contenu puisse être découvert.

### Prise en charge du catalogue partagé

Si un compte vendeur partage un catalogue contenant les cours et que ces derniers contiennent les modules, audio ou vidéo avec sous-titres, les cours doivent se comporter de la même manière dans le compte acheteur.

La propagation du module doit fonctionner correctement du compte Vendeur au compte Acheteur. Cela peut inclure - modifier/supprimer/ajouter le fichier vtt dans le module.

Une fois que vous avez téléchargé le contenu, une notification s’affiche lorsque vous cliquez sur l’icône en forme de cloche dans le coin supérieur droit de la page. Chaque fois que vous modifiez un contenu et que vous le téléchargez à nouveau, vous recevez une notification. Si vous effectuez les modifications, vous êtes le seul à recevoir la notification. Les autres auteurs ne la recevront pas.

## Création d’un quiz {#createaquiz}

Créez des évaluations dans Adobe Learning Manager avec le nouvel outil de création de questionnaire de la page de la bibliothèque de contenus. Les évaluations créées font partie de la bibliothèque de contenu et peuvent être ajoutées à un dossier « public » pour faciliter la réutilisation des cours.

1. Sélectionnez Bibliothèque de contenu dans le panneau de gauche.
1. Dans le coin supérieur droit de l’écran, sélectionnez **Ajouter > Quiz**.
1. Sur la page Créer un quiz, saisissez le nom et la description du quiz.
1. Dans la section Contenu du questionnaire, sélectionnez **Ajouter une question de questionnaire**.
1. Dans la boîte de dialogue Question de quiz, sélectionnez le type de question. Il existe trois types de questions :
   * Question à choix multiple
   * Vrai ou faux
   * Champ à compléter
1. Saisissez la question et sélectionnez la bonne réponse.
1. Définissez le nombre de points pour le questionnaire.
1. Si vous souhaitez que la réponse correcte à la question soit indispensable pour réussir le questionnaire, cochez la case **Réponse correcte obligatoire pour réussir le questionnaire**.
1. Sélectionnez **Enregistrer et fermer**.
1. Saisissez les points pour réussir le quiz dans le champ **Critères de réussite** champ.
1. Si vous souhaitez qu’un élève voie une réponse correcte, activez le bouton à bascule **Afficher les bonnes réponses** aux élèves après le quiz.
1. Si vous souhaitez que les questions et les réponses s’affichent dans un ordre aléatoire, activez les options :
   * Ordre aléatoire des questions
   * Ordre aléatoire des réponses
1. Spécifiez un dossier où ajouter le questionnaire afin qu’il soit disponible pour tous les auteurs.
1. Dans le panneau **Durée** champ, spécifiez le temps que l’élève doit consacrer au quiz.
1. Spécifiez une balise de la liste des balises déjà créées.
1. Ajoutez un logo et un arrière-plan au questionnaire.
1. Dans le coin supérieur droit de la page, sélectionnez **Publier**.

Le questionnaire est ajouté à la bibliothèque de contenu. Comme tout contenu de la bibliothèque de contenu, vous pouvez retirer un questionnaire, puis le supprimer.


## Ajouter au dossier {#add-folder}

Une fois qu’un administrateur a créé les dossiers de contenu, vous pouvez, en tant qu’auteur, charger un contenu vers un dossier de contenu, de sorte que ce contenu ne soit visible que pour vous ou un groupe d’auteurs sélectionnés dans le compte. Vous pouvez également rendre le contenu public et le rendre visible à tous les auteurs du compte.

**Exemple d’utilisation**

Par exemple, les agences veulent garder le contrôle total du contenu et une personne qui surveille le contenu doit avoir accès à tout le contenu. En même temps, les créateurs de contenu dans les agences doivent avoir accès à leur propre contenu uniquement, et dans certains cas, à celui de quelqu&#39;un d&#39;autre.

La bibliothèque de contenu avec du contenu existant (c’est-à-dire du contenu chargé avant de configurer les dossiers de contenu) est définie comme **Dossier public**. Ce dossier ne peut pas être retiré ou supprimé. Le contenu qui fait partie du dossier Public est accessible à tous les types d’auteurs. Une fois les dossiers de contenu configurés, les auteurs standard et les auteurs personnalisés doivent sélectionner le dossier où le contenu doit être placé, lors du chargement du nouveau contenu.

>[!NOTE]
>
>Le dossier public et les dossiers privés s’excluent mutuellement. Cela signifie que le contenu **impossible** être associé à la fois au dossier public et au dossier privé. Il peut être associé au dossier Public, **ou** il peut être associé à un ou plusieurs dossiers privés à tout moment.

Lorsque vous ajoutez un contenu, vous pouvez choisir le dossier dans lequel le contenu résidera.

![](assets/add-to-content-folder.png)

*Ajouter du contenu au dossier*

Si vous **Public**, le contenu sera visible par tous les auteurs. Par défaut, tout le contenu existant dans le compte qui ne fait partie d’aucun dossier se trouve dans le dossier public.

Notez que les dossiers de contenu sont simplement des compartiments virtuels permettant de lier le contenu. Si un contenu est placé dans deux dossiers, cela signifie que le fichier de contenu est toujours un seul fichier, mais lié à plusieurs dossiers. Ainsi, si le contenu est mis à jour par le custom-author-1 ayant accès au dossier-personnalisé-1, le même contenu mis à jour sera également reflété dans le dossier-personnalisé-2 accessible par le custom-author-2.

Dans la bibliothèque de contenu, deux options permettent de gérer les dossiers de contenu :

**Tous les dossiers**

Il s’agit d’une liste qui affiche tous les dossiers créés dans le compte.

![](assets/list-of-all-folders.png)

*Afficher tous les dossiers*

**Tous les auteurs**

Il s’agit d’une liste qui affiche les auteurs qui ont créé du contenu et l’ont chargé dans la bibliothèque.

![](assets/list-of-all-authors.png)

*Voir tous les auteurs*

Cette option est disponible **uniquement** lorsqu’un administrateur crée un dossier.

## Déplacer le contenu vers le dossier {#movecontenttofolder}

Pour déplacer le contenu d’un dossier public vers un dossier privé,

1. Sélectionner **Public** dossier du **Tous les dossiers** liste déroulante.

   ![](assets/list-of-public-folders.png)

   *Afficher tout le contenu chargé*

1. Choisissez le contenu que vous souhaitez déplacer vers un dossier. Cliquez ensuite sur **[!UICONTROL Actions]** > **[!UICONTROL Organiser le contenu]** > **[!UICONTROL Déplacer le contenu vers le dossier]**.

   ![](assets/move-content-to-folder.png)

   *Déplacer un contenu sélectionné vers le dossier*

1. Sélectionnez le dossier vers lequel vous souhaitez déplacer le contenu. Cliquez sur **[!UICONTROL Déplacer]**.

## Copier le contenu vers le dossier {#copycontenttofolder}

Si vous copiez un dossier, cela signifie que vous ajouteriez une balise au dossier. L’opération de copie ne crée pas de copies du contenu, mais ajoute uniquement une association avec les dossiers spécifiés.

![](assets/copy-content-to-folder.png)

*Copie d’un dossier*

## Annuler le lien d&#39;un dossier {#unlinkfolder}

Dissocier signifie supprimer le contenu du dossier sélectionné.

Le contenu peut être dissocié d’un dossier spécifié **UNIQUEMENT** s’il est également associé à d’autres dossiers. Si le contenu dissocié n’est associé qu’à un seul dossier, il est conseillé d’utiliser l’opération MOVE à la place.

>[!NOTE]
>
>Le menu Organiser, sous Actions, est initialement désactivé. Pour utiliser cette option, vous devez d’abord sélectionner un dossier dans la liste déroulante des dossiers.

![](assets/unlink-a-folder.png)

*Dissociation d’un dossier*

## Ajouter du contenu pour différentes langues {#addcontentfordifferentlanguages}

1. Pour ajouter du contenu pour différentes langues, cliquez sur le bouton **Ajouter une nouvelle langue** et sélectionnez les langues requises. Grâce à cette approche, vous pouvez ajouter une prise en charge multilingue pour votre contenu.

   ![](assets/add-new-languagetab.png)

   *Ajout d’une nouvelle langue pour un contenu*

1. Répétez le processus de téléchargement de contenu pour les nouvelles langues.
1. Si vous souhaitez supprimer une langue, cliquez sur l’onglet Ajouter une nouvelle langue et désélectionnez votre sélection.

   Après avoir apporté les modifications, cliquez sur Enregistrer. Dans la bibliothèque, le nouveau contenu est maintenant disponible pour le suivi.

## Définir des critères d’achèvement {#setcompletioncriteria}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Contenu statique</b></p></td>
   <td>
    <p><b>Contenu interactif</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Vous pouvez définir les critères d’<b>achèvement</b> pour le contenu uniquement pour les options suivantes :</p>
    <ul>
     <li>Au lancement du contenu</li>
     <li>Basé sur le pourcentage minimal requis</li>
    </ul></td>
   <td>
    <p>Vous pouvez définir des critères d’<b>achèvement</b> et de <b>réussite</b> pour le contenu des options suivantes :</p>
    <ul>
     <li>Au lancement du contenu</li>
     <li>Basé sur le pourcentage minimal requis</li>
     <li>Quiz réussi ou options tentées</li>
    </ul>
    <p><b>REMARQUE :</b> Seul le contenu HTML du Captivate, de Presenter Video Express ou de Presenter peut être modifié.</p></td>
  </tr>
 </tbody>
</table>

Après avoir ajouté du contenu, vous pouvez modifier les critères d’achèvement du contenu.

Dans Learning Manager, les badges et les compétences sont attribués en fonction de la réussite et de l’achèvement. Si l’élève a terminé un cours mais qu’il ne l’a pas réussi, il ne reçoit pas le badge et la compétence correspondant à l’Objet d’apprentissage.

Par exemple, si vous avez utilisé Adobe Captivate pour créer votre cours et définir les paramètres d’apprentissage dans la boîte de dialogue Préférences, les mêmes paramètres sont migrés vers Learning Manager dans les options Critères de réussite.

Dans la section Critères d’achèvement, vous pouvez définir les options mentionnées ci-dessous :

**Au lancement de contenu :** si vous activez cette option, vous définissez les critères d’achèvement du contenu lorsqu’un élève ouvre le contenu.

**Basé sur le pourcentage minimum requis :** définissez une valeur comme pourcentage minimum de suivi par votre élève. Par exemple, si vous fixez le pourcentage à 50, votre élève peut utiliser 50 % du contenu tout en respectant les critères d’achèvement.

**Quiz :** choisissez l’un des critères suivants :

* **Réussite du quiz :** le statut est considéré comme terminé uniquement si l’élève réussit le quiz.
* **Quiz tenté :** le statut est considéré comme terminé si les élèves tentent le quiz, qu’ils le réussissent ou non.
* **Quiz réussi ou nombre maximal de tentatives atteint :** le statut est défini sur Terminé si l’utilisateur réussit le quiz ou atteint le nombre maximal de tentatives. Par exemple, si le nombre de tentatives pour le cours est de deux et :

   * Si les élèves font la première tentative et réussissent, l&#39;état est défini sur Terminé et Réussi.
   * Si les élèves font la première tentative et échouent, l&#39;état est signalé comme Incomplet et Échec car la limite de tentatives n&#39;est toujours pas atteinte.
   * Si les élèves reprennent le quiz et échouent, l’état est défini sur Terminé et Échec.
   * Si les élèves tentent à nouveau le quiz et le réussissent, l’état est défini sur Terminé et Réussi.

## Définir des critères de réussite {#setsuccesscriteria}

Vous pouvez également définir les critères de réussite pour le cours. Un critère de réussite indique que les performances d’un élève ont réussi ou échoué. Si vous avez créé un cours dans Captivate, vous pouvez définir les critères de réussite du cours dans la boîte de dialogue Préférences, comme indiqué ci-dessous :

Par exemple, vous avez téléchargé un module qui contient un quiz. Maintenant, vous avez défini les critères d’achèvement pour ce module dans Au lancement du contenu et les critères de réussite sur Quiz réussi.

Si l’élève a lancé le cours et échoué au quiz, le cours sera considéré comme terminé, mais les critères de réussite seront remplis uniquement lorsque l’élève aura réussi le quiz.

## Options de filtrage de contenu {#contentfilteroptions}

### Trier selon la date {#sortaccordingtodate}

Organisez le contenu en fonction de la date à laquelle le contenu a été modifié dernièrement. Vous pouvez trier le contenu par ordre croissant ou décroissant.

![](assets/according-to-date.png)

*Trier le contenu par date*

### Trier selon l’utilisation {#sortaccordingtousage}

Organisez le contenu selon qu’il est utilisé ou non dans un cours. Dans la liste déroulante Type, sélectionnez En cours d’utilisation ou Non utilisé.

![](assets/according-to-usage.png)

*Trier le contenu par utilisation*

## Rechercher des contenus {#searchforcontent}

Dans la bibliothèque de contenus, vous pouvez rechercher un contenu en sélectionnant soit le nom du contenu, soit les balises associées au contenu.

Dans la barre de recherche, saisissez le nom d’un cours ou d’une balise, et vous pouvez voir les recommandations.

<!--![](assets/search-bar.png)-->

## Retirer du contenu {#retirecontent}

Une fois que vous publiez un contenu, vous ne pouvez pas le supprimer. Vous devez d’abord retirer le contenu. Lorsque vous marquez un contenu comme Retiré, le contenu n’est plus visible pour les élèves. Le contenu passe également à la section Retiré. Vous pouvez également déplacer le contenu dans l’état publié ultérieurement.

Pour retirer du contenu, procédez comme suit :

* Dans Bibliothèque de contenus, sélectionnez le contenu que vous souhaitez retirer.
* Sélectionnez Action > Retirer.

Tout contenu utilisé dans des objets d’apprentissage n’est pas affecté. Les élèves peuvent continuer d’accéder au contenu.

## Republier le contenu retiré {#republishretiredcontent}

Une fois que vous retirez un contenu, vous pouvez le republier et le faire apparaître dans la liste Publié. Par exemple, si vous avez retiré la version 1 d’un contenu et que vous souhaitez la remplacer par la version 2, vous pouvez déplacer version1.pptx, par exemple, dans la liste Publié et mettre à jour le fichier avec version2.pptx. Le nouveau fichier est disponible pour être utilisé dans différents cours.

Pour republier le contenu retiré,

1. Accédez à l’onglet **Retiré** et sélectionnez le contenu que vous souhaitez republier.
1. Sélectionner **Action** > **Republier**.

Le contenu apparaît maintenant dans la liste Publié.

## Supprimer le contenu {#deletecontent}

Après avoir retiré un contenu, vous pouvez le supprimer.

* Accédez à l’onglet Retiré et sélectionnez le contenu que vous souhaitez supprimer.
* Sélectionnez Action > Supprimer.

Sachez que les cours existants qui utilisent le contenu, qui sont supprimés de la bibliothèque de contenus, continueront à utiliser le contenu.

## Forum aux questions {#frequentlyaskedquestions}

+++ Comment télécharger un contenu SCORM dans Adobe Learning Manager ?

Créez un cours d’e-learning compatible SCORM dans n’importe quel outil, tel qu’Adobe Captivate, et publiez le contenu sous forme de fichier zip. Ensuite, dans Learning Manager, téléchargez le fichier zip dans le catalogue et définissez les critères d’achèvement et de réussite.
+++

+++Comment puis-je télécharger une nouvelle version du même contenu sur Learning Manager ?

Dans Learning Manager, la bibliothèque de contenu conserve également les versions de vos contenus téléchargés. Si vous modifiez le contenu d’une présentation PowerPoint, par exemple, et que vous la téléchargez à nouveau dans la bibliothèque, le numéro de version est incrémenté d’une unité. Cela vous aide à suivre l’évolution de votre contenu. Une nouvelle version du contenu peut être appliquée à tous les objets d’apprentissage simultanément ou vous pouvez appliquer des mises à jour individuelles pour chaque cours.
+++

+++Comment modifier les détails d’un cours dans une autre langue ?
Après avoir ajouté une langue/des langues, comme décrit dans une section précédente, cliquez sur chaque onglet de langue, puis ajoutez/modifiez les informations sur le cours.

&lt;!--![](assets/edit-course-language.png)--->
+++
