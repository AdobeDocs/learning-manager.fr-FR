---
description: Apprenez à créer un contenu aligné sur les cours en tant que contenu d’auto-apprentissage.
jcr-language: en_us
title: Bibliothèque de contenu
exl-id: cc19eca6-6b47-44b2-ad23-2d7ad8975f65
source-git-commit: 8780f8bf0c56d27c1acdaff018544ecc0c21ea23
workflow-type: tm+mt
source-wordcount: '4620'
ht-degree: 36%

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
  <tr>
   <td>
    <p> </p></td>
   <td>
    <p>HTML</p></td>
   <td>
    <p>fichier zip</p></td>
  </tr>
 </tbody>
</table>

## Ajouter du nouveau contenu dans la bibliothèque {#addnewcontentinthelibrary}

**Les auteurs** peuvent ajouter du contenu dans ALM. Il existe deux types de contenu dans ALM : **[!UICONTROL Contenu]** et **[!UICONTROL Quiz]**. Pour savoir comment ajouter du contenu, consultez [Ajouter du contenu statique](content-library.md#addstaticcontent) et [Créer un quiz](content-library.md##createaquiz).

## Ajouter du contenu statique {#addstaticcontent}

1. Sélectionnez **[!UICONTROL Bibliothèque de contenu]** dans le volet de gauche après vous être connecté en tant qu&#39;**auteur** et sélectionnez **[!UICONTROL Ajouter]**.

   Vous pouvez également sélectionner **[!UICONTROL Créer du contenu]** dans la page **[!UICONTROL Prise en main]**.

1. Dans le champ **[!UICONTROL Nom]**, saisissez un nom pour le contenu que vous souhaitez télécharger.
1. Dans le champ **[!UICONTROL Description]**, saisissez la description du contenu. Assurez-vous que la description que vous voulez saisir est significative. La limite de caractères est de 400 caractères.
1. Pour ajouter du contenu, sélectionnez **[!UICONTROL Ajouter un fichier de contenu]**, puis chargez votre fichier de ressources. Lorsque vous ajoutez du contenu dans diverses langues, vous ne pouvez pas combiner le contenu statique et le contenu interactif dans un même groupe. L’ensemble de votre contenu dans toutes les langues doit être soit statique, soit interactif.

   Si vous voulez remplacer le contenu, vous pouvez remplacer un contenu statique par un contenu statique différent. Le même procédé peut s’appliquer au contenu interactif.

1. Dans le champ **[!UICONTROL Durée]**, vous pouvez éventuellement saisir le temps qu&#39;un élève doit passer dans ce module. La durée est calculée en minutes.

   Si l’élève marque un cours comme terminé, nous calculons le temps d’apprentissage en fonction de la durée spécifiée. Si l’élève utilise le contenu du lecteur, le temps passé dans le lecteur est ajouté au temps d’apprentissage passé. Si la durée réelle du contenu est inférieure à la durée spécifiée, le lecteur affiche la durée du contenu telle quelle. Aucune modification n’est apportée dans ce cas.

1. Dans le champ **[!UICONTROL Balises]**, saisissez les balises du contenu chargé afin que votre contenu puisse être découvert.

   Un auteur peut utiliser ces balises pour rechercher le contenu lors de l&#39;ajout du contenu au cours.

### Ajout d’un type de fichier HTML5 dans la bibliothèque de contenu

Les auteurs peuvent ajouter du contenu HTML5 sous forme de fichier .zip au contenu d’auto-apprentissage. Le dossier .zip doit contenir un fichier de HTML nommé `index.html`. S&#39;il y a plusieurs fichiers de HTML, ils doivent tous être liés, avec le fichier principal nommé `index.html`. Les élèves peuvent afficher le contenu HTML5 dans le lecteur Fluidic. L&#39;auteur peut ajouter ce contenu HTML5 au module d&#39;auto-apprentissage d&#39;un cours et définir les critères d&#39;achèvement. Les auteurs peuvent définir les critères d’achèvement du cours HTML de l’une des deux manières suivantes :

* L’élève peut le marquer comme terminé lui-même.
* Il sera marqué comme terminé une fois qu’ils auront lancé le cours.

Pour ajouter le type de fichier par HTML (.zip) à la bibliothèque de contenu, procédez comme suit.

1. Dans l&#39;application d&#39;auteur, sélectionnez **[!UICONTROL Créer du contenu]** sur la page d&#39;accueil.
1. Dans l&#39;écran **[!UICONTROL Bibliothèque de contenu]**, sélectionnez **[!UICONTROL Ajouter]** > **[!UICONTROL Contenu]**.
1. Saisissez le nom et la description du contenu.
1. Sélectionnez l&#39;option **[!UICONTROL Ajouter un fichier de contenu]**, puis parcourez et sélectionnez les fichiers de HTML (compressés sous forme de dossier).
1. Une fois le contenu ajouté, vous pouvez l&#39;afficher dans la section **[!UICONTROL Bibliothèque de contenu]**.
1. Sélectionnez le contenu du HTML, puis **[!UICONTROL Modifier]**.
1. Sélectionnez l&#39;une des options suivantes dans l&#39;option **[!UICONTROL Critères d&#39;achèvement]**.
   * **[!UICONTROL Lors du lancement du contenu]** : le cours sera marqué comme terminé automatiquement lorsque l’élève le lancera.
   * **[!UICONTROL L’élève marque le cours comme terminé]** : l’élève a la possibilité de marquer le cours comme terminé dans le lecteur Fluidic.

   ![](assets/completion-criteria.png)
   _Critères d&#39;achèvement_

1. Sélectionnez **[!UICONTROL Enregistrer]**.
1. Créez un cours en ajoutant ce contenu.  Pour plus d&#39;informations, consultez [Création, modification et publication de cours](/help/migrated/authors/feature-summary/courses.md).

Dans l&#39;application de l&#39;élève, si un auteur sélectionne le critère de sélection **[!UICONTROL Au lancement du contenu]**, le cours sera marqué comme terminé lorsque l&#39;élève le lancera. Lorsqu&#39;un auteur choisit **[!UICONTROL L&#39;élève marque le cours comme terminé]**, il a la possibilité de le marquer comme terminé.

![](assets/completion-criteria-fluidic-player.png)

_Notes de l’élève terminées_

### Contrôle de version {#versioning}

La bibliothèque de contenus maintient également le contrôle de version de vos contenus téléchargés. Si vous apportez des modifications au contenu, par exemple une présentation PowerPoint, et que vous téléchargez à nouveau le PPT dans la bibliothèque, le numéro de version est incrémenté d’une unité. Cela vous aide à suivre l’évolution de votre contenu.

## Ajouter du contenu interactif {#addinteractivecontent}

1. Sélectionnez **[!UICONTROL Bibliothèque de contenu]** dans le volet de gauche après vous être connecté en tant qu&#39;**auteur** et sélectionnez **[!UICONTROL Ajouter]**.

   Vous pouvez également sélectionner **[!UICONTROL Créer du contenu]** dans la page **[!UICONTROL Prise en main]**.

1. Dans le champ **[!UICONTROL Nom]**, saisissez un nom pour le contenu que vous souhaitez télécharger.
1. Dans le champ **[!UICONTROL Description]**, saisissez la description du contenu.

   >[!NOTE]
   >
   >Assurez-vous que la description que vous voulez saisir est significative. La limite de caractères est de 245 caractères.

1. Pour ajouter du contenu, sélectionnez **[!UICONTROL Ajouter un fichier de contenu]**, puis chargez votre fichier de ressources. Lorsque vous ajoutez du contenu dans diverses langues, vous ne pouvez pas combiner le contenu statique et le contenu interactif dans un même groupe. L’ensemble de votre contenu dans toutes les langues doit être soit statique, soit interactif.

* [Types de fichier pris en charge](content-library.md#supported)

  Le contenu interactif peut être une option SCORM, AICC ou un projet publié Captivate. Ce fichier doit être un fichier zip.

  Vous pouvez également ajouter du contenu HTML généré à partir de Captivate, Presenter ou Presenter Video Express.

1. Adobe Learning Manager prend en charge les légendes pour le contenu vidéo chargé dans Adobe Learning Manager. Désormais, les auteurs peuvent charger le fichier contenant les légendes, ainsi que le fichier vidéo.

   Les élèves peuvent ensuite afficher les légendes pendant la lecture du module vidéo.

   Le format pris en charge est [Web Video Text Tracks (webVTT)](https://www.w3.org/TR/webvtt1/).

   La prise en charge des légendes est disponible pour le contenu vidéo chargé dans la bibliothèque de contenu de Adobe Learning Manager.

   En tant qu’auteur, lorsque vous chargez un contenu vidéo ou audio, vous pouvez également charger le fichier VTT qui contient les sous-titres.

   Les sous-titres apparaissent ensuite dans le lecteur Fluidic. Les sous-titres sont également conformes aux [normes WCAG2.0](https://www.w3.org/TR/WCAG20/).

   Lorsque vous ajoutez un contenu vidéo à la bibliothèque, vous pouvez également ajouter le fichier VTT, qui **doit** être un fichier valide.

   ![](assets/webvtt.png)

   *Ajouter un fichier webvtt*

   Le fichier VTT chargé correspond à la version existante du contenu. Ainsi, le fichier webVTT chargé ne renvoie pas à l’ancienne version du contenu.

   Si vous créez le contenu dans différentes langues, vous pouvez charger un fichier webVTT différent pour chaque langue. Les élèves pourront voir les légendes correspondant à la langue sélectionnée pendant la lecture.

   >[!NOTE]
   >
   >   Un fichier VTT prend en charge une langue. Pour prendre en charge plusieurs langues, chargez plusieurs fichiers vidéo pour chaque langue de contenu, puis chargez son fichier VTT respectif pour chaque fichier vidéo.

   En tant qu’auteur, chaque fois que vous modifiez le contenu, la vidéo ou l’audio, Adobe Learning Manager vous invite à créer un fichier vtt.

   Après avoir ajouté ce contenu à un cours et lorsque vous affichez un aperçu du cours en tant qu’élève, vous pouvez voir les légendes sur la vidéo.

   Sur le lecteur, activez ou désactivez le bouton CC sur le lecteur Fluidic pour afficher ou masquer les légendes.

   La même vue apparaît dans **l&#39;application de l&#39;élève** ainsi que dans **Aperçu en tant qu&#39;élève**.

   Lorsque vous **ajoutez, mettez à jour ou supprimez** le fichier vtt, vous recevez une notification.
La prise en charge de WebVTT n’est pas disponible pour :

   1. Annonces vidéo.
   1. Vidéo lue dans le contenu de formation en ligne. Cela dépend du contenu.
   1. Vidéo téléchargée dans l&#39;apprentissage par les réseaux sociaux.
   1. Vidéo créée dans l’application de bureau Adobe Learning Manager.
   1. Contenu vidéo créé à l’aide du processus de migration.
   1. Lecture vidéo dans l’application mobile en mode hors ligne.

1. Dans le champ **[!UICONTROL Durée]**, vous pouvez éventuellement saisir le temps qu&#39;un élève doit passer dans ce module. La durée est calculée en minutes.
1. Dans le champ **[!UICONTROL Balises]**, saisissez les balises du contenu chargé afin que votre contenu puisse être découvert.

### Prise en charge du catalogue partagé

Si un compte vendeur partage un catalogue contenant les cours et que ces derniers contiennent les modules, audio ou vidéo avec sous-titres, les cours doivent se comporter de la même manière dans le compte acheteur.

La propagation du module doit fonctionner correctement du compte Vendeur au compte Acheteur. Cela peut inclure - modifier/supprimer/ajouter le fichier vtt dans le module.

Une fois que vous avez téléchargé le contenu, une notification s’affiche lorsque vous cliquez sur l’icône en forme de cloche dans le coin supérieur droit de la page. Chaque fois que vous modifiez un contenu et que vous le téléchargez à nouveau, vous recevez une notification. Si vous effectuez les modifications, vous êtes le seul à recevoir la notification. Les autres auteurs ne la recevront pas.

## Création d’un quiz {#createaquiz}

Créez des évaluations dans Adobe Learning Manager avec le nouvel outil de création de questionnaire de la page de la bibliothèque de contenus. Les évaluations créées font partie de la bibliothèque de contenu et peuvent être ajoutées à un dossier « public » pour faciliter la réutilisation des cours.

1. Sélectionnez Bibliothèque de contenu dans le panneau de gauche.
1. Dans le coin supérieur droit de l&#39;écran, sélectionnez **Ajouter > Quiz**.
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
1. Saisissez les points pour réussir le quiz dans le champ **Critères de réussite**.
1. Si vous souhaitez qu&#39;un élève affiche une réponse correcte, activez l&#39;option **Afficher les réponses correctes** pour les élèves après le quiz.
1. Si vous souhaitez que les questions et les réponses s’affichent dans un ordre aléatoire, activez les options :
   * Ordre aléatoire des questions
   * Ordre aléatoire des réponses
1. Spécifiez un dossier où ajouter le questionnaire afin qu’il soit disponible pour tous les auteurs.
1. Dans le champ **Durée**, spécifiez le temps que l’élève doit passer sur le quiz.
1. Spécifiez une balise de la liste des balises déjà créées.
1. Ajoutez un logo et un arrière-plan au questionnaire.
1. Dans le coin supérieur droit de la page, sélectionnez **Publish**.

Pour ajouter les quiz dans une autre langue, procédez comme suit :

1. Pour ajouter le quiz pour différentes langues, sélectionnez l&#39;onglet **Ajouter une nouvelle langue** et choisissez les langues requises. Grâce à cette approche, vous pouvez ajouter une prise en charge multilingue pour votre contenu.

   ![](assets/add-new-languagetab.png)

   *Ajouter une nouvelle langue pour un contenu*

1. Répétez le processus de téléchargement de contenu pour les nouvelles langues.
1. Si vous souhaitez supprimer une langue, sélectionnez l&#39;onglet **[!UICONTROL Ajouter une nouvelle langue]** et effacez votre sélection.

   Après avoir apporté les modifications, cliquez sur **[!UICONTROL Enregistrer]**. Dans la bibliothèque, le nouveau contenu est maintenant disponible pour le suivi.

Le quiz est ajouté à la **[!UICONTROL Bibliothèque de contenu]**. Comme tout contenu de la bibliothèque de contenu, vous pouvez retirer un questionnaire, puis le supprimer.


## Ajouter au dossier {#add-folder}

Une fois qu’un administrateur a créé les dossiers de contenu, vous pouvez, en tant qu’auteur, charger un contenu vers un dossier de contenu, de sorte que ce contenu ne soit visible que pour vous ou un groupe d’auteurs sélectionnés dans le compte. Vous pouvez également rendre le contenu public et le rendre visible à tous les auteurs du compte.

**Exemple d’utilisation**

Par exemple, les agences veulent garder le contrôle total du contenu et une personne qui surveille le contenu doit avoir accès à tout le contenu. En même temps, les créateurs de contenu dans les agences doivent avoir accès à leur propre contenu uniquement, et dans certains cas, à celui de quelqu&#39;un d&#39;autre.

La bibliothèque de contenu avec du contenu existant (c.-à-d. du contenu chargé avant de configurer les dossiers de contenu) est définie comme **dossier public**. Ce dossier ne peut pas être retiré ou supprimé. Le contenu qui fait partie du dossier Public est accessible à tous les types d’auteurs. Une fois les dossiers de contenu configurés, les auteurs standard et les auteurs personnalisés doivent sélectionner le dossier où le contenu doit être placé, lors du chargement du nouveau contenu.

>[!NOTE]
>
>Le dossier public et les dossiers privés s’excluent mutuellement. Cela signifie que le contenu **ne peut pas** être associé au dossier public et au dossier privé en même temps. Il peut être associé au dossier public, **ou** il peut être associé à un ou plusieurs dossiers privés à tout moment.

Lorsque vous ajoutez un contenu, vous pouvez choisir le dossier dans lequel le contenu résidera.

![](assets/add-to-content-folder.png)

*Ajouter du contenu au dossier*

Si vous choisissez **Public**, le contenu sera visible par tous les auteurs. Par défaut, tout le contenu existant dans le compte qui ne fait partie d’aucun dossier se trouve dans le dossier public.

Notez que les dossiers de contenu sont simplement des compartiments virtuels permettant de lier le contenu. Si un contenu est placé dans deux dossiers, cela signifie que le fichier de contenu est toujours un seul fichier, mais lié à plusieurs dossiers. Ainsi, si le contenu est mis à jour par le custom-author-1 ayant accès au dossier-personnalisé-1, le même contenu mis à jour sera également reflété dans le dossier-personnalisé-2 accessible par le custom-author-2.

Dans la bibliothèque de contenu, deux options permettent de gérer les dossiers de contenu :

**Tous les dossiers**

Il s’agit d’une liste qui affiche tous les dossiers créés dans le compte.

![](assets/list-of-all-folders.png)

*Afficher tous les dossiers*

**Tous les auteurs**

Il s’agit d’une liste qui affiche les auteurs qui ont créé du contenu et l’ont chargé dans la bibliothèque.

![](assets/list-of-all-authors.png)

*Afficher tous les auteurs*

Cette option est disponible **uniquement** lorsqu&#39;un administrateur crée un dossier.

## Déplacer le contenu vers le dossier {#movecontenttofolder}

Pour déplacer le contenu d’un dossier public vers un dossier privé,

1. Sélectionnez le dossier **Public** dans la liste déroulante **Tous les dossiers**.

   ![](assets/list-of-public-folders.png)

   *Afficher tout le contenu chargé*

1. Choisissez le contenu que vous souhaitez déplacer vers un dossier. Cliquez ensuite sur **[!UICONTROL Actions]** > **[!UICONTROL Organiser le contenu]** > **[!UICONTROL Déplacer le contenu vers le dossier]**.

   ![](assets/move-content-to-folder.png)

   *Déplacer un contenu sélectionné vers le dossier*

1. Sélectionnez le dossier vers lequel vous souhaitez déplacer le contenu. Cliquez sur **[!UICONTROL Déplacer]**.

## Copier le contenu vers le dossier {#copycontenttofolder}

Si vous copiez un dossier, cela signifie que vous ajouteriez une balise au dossier. L’opération de copie ne crée pas de copies du contenu, mais ajoute uniquement une association avec les dossiers spécifiés.

![](assets/copy-content-to-folder.png)

*Copier un dossier*

## Annuler le lien d&#39;un dossier {#unlinkfolder}

Dissocier signifie supprimer le contenu du dossier sélectionné.

Le contenu peut être dissocié d&#39;un dossier spécifié **UNIQUEMENT** s&#39;il est également associé à d&#39;autres dossiers. Si le contenu dissocié n’est associé qu’à un seul dossier, il est conseillé d’utiliser l’opération MOVE à la place.

>[!NOTE]
>
>Le menu Organiser, sous Actions, est initialement désactivé. Pour utiliser cette option, vous devez d’abord sélectionner un dossier dans la liste déroulante des dossiers.

![](assets/unlink-a-folder.png)

*Dissocier un dossier*

## Ajouter du contenu pour différentes langues {#addcontentfordifferentlanguages}

1. Pour ajouter du contenu pour différentes langues, cliquez sur l&#39;onglet **Ajouter une nouvelle langue** et choisissez les langues requises. Grâce à cette approche, vous pouvez ajouter une prise en charge multilingue pour votre contenu.

   ![](assets/add-new-languagetab.png)

   *Ajouter une nouvelle langue pour un contenu*

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
    <p><b>REMARQUE :</b> seul le contenu HTML du Captivate, de Presenter Video Express ou de Presenter peut être modifié.</p></td>
  </tr>
 </tbody>
</table>

Après avoir ajouté du contenu, vous pouvez modifier les critères d’achèvement du contenu.

Dans Adobe Learning Manager, les badges et les compétences sont attribués en fonction du succès et de l’achèvement. Si l’élève a terminé un cours mais qu’il ne l’a pas réussi, il ne reçoit pas le badge et la compétence correspondant à l’Objet d’apprentissage.

Par exemple, si vous avez utilisé Adobe Captivate pour créer votre cours et définir les paramètres d’apprentissage dans la boîte de dialogue Préférences, les mêmes paramètres sont migrés vers Adobe Learning Manager dans les options Critères d’achèvement.

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

## Ajouter un ID de contenu unique et une date d’expiration

### Qu’est-ce qu’un ID de contenu unique ?

L’ID unique de contenu est un code unique donné à chaque élément de contenu dans Adobe Learning Manager. Il aide les administrateurs et les auteurs à trouver et à gérer facilement le contenu, en particulier lors de la mise à jour ou du déplacement entre les systèmes. Cet ID unique de contenu est également utile pour intégrer du contenu à d’autres outils tels que les RH ou les systèmes de conformité. Le même ID unique de contenu est utilisé dans toutes les versions linguistiques, afin que tout reste cohérent pour les élèves.

* Les ID de contenu unique doivent être uniques dans tout le contenu.
* L’ID de contenu unique ne peut pas inclure d’espaces ni de caractères spéciaux.
* Si un ID unique de contenu dupliqué est saisi, une erreur s’affiche lors de la création.

### Qu’est-ce que la date d’expiration ?

La Date d’expiration marque le contenu qui peut être obsolète ou qui n’est plus nécessaire. Même après la date d’expiration, le contenu reste disponible, mais il rappelle aux auteurs et aux administrateurs de le vérifier et de le mettre à jour si nécessaire. En fonction des paramètres, le contenu expiré peut être supprimé des nouvelles inscriptions ou archivé. Comme l’ID unique de contenu, la Date d’expiration fonctionne de la même manière pour toutes les versions linguistiques, ce qui permet au contenu d’être propre et à jour pour tout le monde.

* Le contenu reste disponible même après l’expiration.
* Un avertissement s’affiche si une date passée est sélectionnée.
* Le champ Expiration accepte toute date comprise entre 1990 et 2037.

Cela aide les organisations à conserver la pertinence du contenu sans supprimer accidentellement les éléments publiés.

L’ID unique du contenu et la date d’expiration s’appliquent à toutes les versions linguistiques d’un groupe de contenus, ce qui garantit une expérience cohérente pour tous les utilisateurs, quelle que soit la langue. Les auteurs peuvent utiliser l’ID unique de contenu pour rechercher et trouver rapidement du contenu spécifique, ce qui facilite la gestion et la mise à jour des supports de formation.

Le **[!UICONTROL rapport de formation]** inclut désormais deux nouvelles colonnes : **[!UICONTROL Date d&#39;expiration du contenu (fuseau horaire UTC)]** et **[!UICONTROL ID de contenu unique]**, pour suivre l&#39;ID de contenu unique et la date d&#39;expiration. Ces champs peuvent être ajoutés via l’interface utilisateur ou la migration, et l’administrateur peut les suivre de manière centralisée via des rapports de formation.

### Ajouter un ID de contenu unique et une date d’expiration

Les auteurs peuvent ajouter un ID de contenu unique et définir une date d’expiration lors de la création de contenu.

Pour ajouter un ID de contenu unique et une date d’expiration :

1. Connectez-vous en tant qu’auteur.
2. Sélectionnez **[!UICONTROL Créer du contenu]** ou sélectionnez **[!UICONTROL Bibliothèque de contenu]** dans le panneau de gauche.

   ![](assets/create-content.png)
   _Sélectionnez Créer du contenu dans la page d&#39;accueil_

3. Sélectionnez **[!UICONTROL Ajouter]**, puis **[!UICONTROL Contenu]** dans la page d&#39;accueil de l&#39;auteur.

   ![](assets/add-content.PNG)
   _Sélectionnez Ajouter du contenu dans la bibliothèque de contenu_

4. Saisissez le **[!UICONTROL nom]** et la **[!UICONTROL description]**

5. Sélectionnez le contenu dans l&#39;option **[!UICONTROL Ajouter un fichier de contenu]**
6. Sélectionnez l&#39;option **[!UICONTROL Ajouter au dossier]** pour ajouter le contenu au dossier.

   ![](assets/add-a-new-content.png)
   _Ajouter du nouveau contenu_

7. Saisissez l&#39;ID du contenu chargé dans le champ **[!UICONTROL ID de contenu unique]**. L’ID doit être unique et respecter les directives de dénomination correctes. L’ID ne doit pas contenir de caractères ou d’espaces non ASCII. Si vous saisissez un ID en double, un message d’erreur s’affiche.

   ![](assets/content-unique-id.png)
   _Champ permettant de saisir un ID de contenu alphanumérique unique_

8. Sélectionnez la date d’expiration du contenu. Cette date n’affecte pas la disponibilité du contenu ni l’accès des élèves. Vous pouvez choisir n’importe quelle date entre 1990 et 2037. Si une date passée est sélectionnée, un avertissement s’affiche, mais le contenu peut toujours être publié.
9. Sélectionnez **[!UICONTROL Enregistrer]**.
Le contenu chargé apparaît désormais dans la **[!UICONTROL bibliothèque de contenu]**.

### Définir l’ID unique du contenu et la date d’expiration pour les langues

L’ID unique du contenu et la date d’expiration sont définis au niveau du groupe de contenus, ce qui signifie qu’ils sont définis une fois et s’appliquent automatiquement à toutes les versions linguistiques du contenu.

1. Sélectionnez le contenu dans la **[!UICONTROL Bibliothèque de contenu]**.
2. Sélectionnez **[!UICONTROL Modifier]**.
3. Sélectionnez **[!UICONTROL Ajouter une nouvelle langue]**.
4. Sélectionnez une langue dans la liste.
5. Sélectionnez **[!UICONTROL Enregistrer]**.
L’ID unique du contenu et la Date d’expiration s’affichent désormais sur la version spécifique à la langue du contenu, comme l’allemand dans cet exemple.

### Recherche à l’aide de l’ID de contenu unique

Vous pouvez utiliser l’ID unique de contenu pour rechercher du contenu dans toutes les versions linguistiques, ce qui facilite la recherche et la gestion d’éléments spécifiques. En outre, l’ID unique du contenu et la date d’expiration sont inclus dans les rapports de formation pour un suivi et des rapports cohérents.

1. Lancez la **[!UICONTROL bibliothèque de contenu]**.
2. Saisissez l&#39;**[!UICONTROL ID de contenu unique]** dans la barre de recherche.

   ![](assets/search-unique-id.png)
   _Recherche de contenu à l&#39;aide de l&#39;ID de contenu unique_
3. Sélectionnez le contenu à afficher ou à modifier.

### Prise en charge de la migration du contenu

Lors de la migration de contenu, vous pouvez inclure **expiryDate** et **uniqueContentId** dans le fichier module_version.csv. Cela garantit la continuité des métadonnées lors du déplacement de contenu entre les systèmes.

### Modifications des rapports

Deux nouvelles colonnes, ID unique du contenu et Date d’expiration du contenu, sont désormais disponibles dans le rapport de formation. Ces champs aident les administrateurs à surveiller plus efficacement les dates d’expiration du contenu.

## Retirer du contenu {#retirecontent}

Une fois que vous publiez un contenu, vous ne pouvez pas le supprimer. Vous devez d’abord retirer le contenu. Lorsque vous marquez un contenu comme Retiré, le contenu n’est plus visible pour les élèves. Le contenu est également déplacé vers la section **[!UICONTROL Retiré]**.

Pour retirer du contenu, procédez comme suit :

* Dans la **[!UICONTROL Bibliothèque de contenu]**, sélectionnez le contenu que vous souhaitez retirer.
* Sélectionnez **[!UICONTROL Action]**, puis **[!UICONTROL Retirer]**.

Tout contenu utilisé dans des objets d’apprentissage n’est pas affecté. Les élèves peuvent continuer d’accéder au contenu.

>[!NOTE]
>
>Vous pouvez également ajouter du contenu à partir de la section **[!UICONTROL Retiré]**, accéder à la **[!UICONTROL Bibliothèque de contenu]**, puis sélectionner **[!UICONTROL Retiré]**. Sélectionnez **[!UICONTROL Ajouter du contenu]**. Pour plus de détails, voir [Ajouter du contenu statique](content-library.md#addstaticcontent).


## Rechercher des contenus {#searchforcontent}

Dans la bibliothèque de contenus, vous pouvez rechercher un contenu en sélectionnant soit le nom du contenu, soit les balises associées au contenu.

Dans la barre de recherche, saisissez le nom d’un cours ou d’une balise, et vous pouvez voir les recommandations.

<!--![](assets/search-bar.png)-->

## Republier le contenu retiré {#republishretiredcontent}

Une fois que vous retirez un contenu, vous pouvez le republier et le faire apparaître dans la liste Publié. Par exemple, si vous avez retiré la version 1 d’un contenu et que vous souhaitez la remplacer par la version 2, vous pouvez déplacer version1.pptx, par exemple, dans la liste Publié et mettre à jour le fichier avec version2.pptx. Le nouveau fichier est disponible pour être utilisé dans différents cours.

Pour republier le contenu retiré,

1. Accédez à l’onglet **Retiré** et sélectionnez le contenu que vous souhaitez republier.
1. Sélectionnez **Action** > **Republier**.

Le contenu apparaît maintenant dans la liste Publié.

## Mise à jour du contenu

Les auteurs peuvent mettre à jour le contenu du cours publié.
Pour mettre à jour le contenu :

1. Connectez-vous en tant qu’auteur.
2. Sélectionnez **[!UICONTROL Bibliothèque de contenu]**.
3. Recherchez le contenu et sélectionnez **[!UICONTROL Modifier]**.
4. Supprimez le contenu plus ancien, chargez un nouveau fichier et publiez.

Cela aidera les élèves à obtenir la dernière version du contenu.

Consultez ce [blog](https://elearning.adobe.com/2024/06/how-to-update-the-content-in-the-course/) pour plus d&#39;informations.

### Contrôle de version du contenu pour les élèves qui ont terminé un cours

Adobe Learning Manager offre désormais aux auteurs des options plus claires pour gérer les mises à jour de contenu. Les auteurs peuvent mettre à jour le contenu déjà disponible dans un cours. Lorsqu’une nouvelle version est ajoutée, le numéro de version apparaît en regard du contenu.

Lorsqu&#39;un administrateur consulte un cours dont le contenu est mis à jour, un bouton Mettre à jour apparaît en regard de la nouvelle version. Les administrateurs verront également des options de mise à jour claires pour choisir comment la nouvelle version du contenu est appliquée aux élèves.

| État de l’élève | Mettre à jour maintenant | Mettre à jour éventuellement | Mise à jour non commencée |
|---|---|---|---|
| Non inscrit | V2 | V2 | V2 |
| Pas encore commencé | V2 | V2 | V2 |
| En cours | V2 * | V1 → V2 * | V1 |
| Terminé | V2 * | V2 * | V1 (conservé) |

(*) Indique que le module sera réinitialisé lorsque la version sera mise à jour.

Avec Mise à jour non commencée, les élèves qui ont déjà terminé le cours continuent de voir la version de contenu d’origine (V1). Cela évite les problèmes de lecture inattendus et garantit une expérience cohérente pour les élèves qui consultent les cours terminés.

### Options de mise à jour du contenu

Lorsqu&#39;un administrateur clique sur **[!UICONTROL Mettre à jour]**, il peut choisir parmi les options suivantes :

* **[!UICONTROL Mettre à jour tous les élèves maintenant]** : appliquez immédiatement la mise à jour du contenu pour tous les élèves. Les élèves n&#39;ont pas commencé, sont en cours et terminés passent immédiatement à la nouvelle version.
* **[!UICONTROL Mettre à jour tous les élèves par la suite]** : appliquez la mise à jour à tous les élèves par phases. Les élèves non commencés et terminés reçoivent la nouvelle version maintenant. Les élèves en cours reçoivent la mise à jour une fois qu’ils ont terminé la version actuelle.
* **[!UICONTROL La mise à jour n&#39;a pas encore commencé pour les élèves]** : appliquez la mise à jour uniquement aux élèves qui n&#39;ont pas encore commencé le cours. Les élèves en cours et terminés restent sur la version d&#39;origine.

![](assets/version-control-options.png)
_Options de mise à jour du contenu disponibles dans les paramètres de mise à jour_


## Supprimer le contenu {#deletecontent}

Après avoir retiré un contenu, vous pouvez le supprimer.

* Accédez à l’onglet Retiré et sélectionnez le contenu que vous souhaitez supprimer.
* Sélectionnez Action > Supprimer.

Sachez que les cours existants qui utilisent le contenu, qui sont supprimés de la bibliothèque de contenus, continueront à utiliser le contenu.

## Forum aux questions {#frequentlyaskedquestions}

+++ Comment télécharger un contenu SCORM dans Adobe Learning Manager ?

Créez un cours d’e-learning compatible SCORM dans n’importe quel outil, tel qu’Adobe Captivate, et publiez le contenu sous forme de fichier zip. Ensuite, dans Adobe Learning Manager, téléchargez le fichier zip dans le catalogue et définissez les critères d’achèvement et de réussite.
+++

+++Comment puis-je télécharger une nouvelle version du même contenu sur Adobe Learning Manager ?

Dans Adobe Learning Manager, la bibliothèque de contenu conserve également les versions de vos contenus téléchargés. Si vous modifiez le contenu d’une présentation PowerPoint, par exemple, et que vous la téléchargez à nouveau dans la bibliothèque, le numéro de version est incrémenté d’une unité. Cela vous aide à suivre l’évolution de votre contenu. Une nouvelle version du contenu peut être appliquée à tous les objets d’apprentissage simultanément ou vous pouvez appliquer des mises à jour individuelles pour chaque cours.
+++

+++Comment modifier les détails d’un cours dans une autre langue ?
Après avoir ajouté une langue/des langues, comme décrit dans une section précédente, cliquez sur chaque onglet de langue, puis ajoutez/modifiez les informations sur le cours.

&lt; !—![](assets/edit-course-language.png)—>
+++
