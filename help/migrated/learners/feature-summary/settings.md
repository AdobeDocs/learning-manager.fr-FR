---
description: Lisez cet article pour savoir comment définir les paramètres du profil d’élève et ajouter une photo de profil. Découvrez comment télécharger le relevé de notes d’élève pour votre profil.
jcr-language: en_us
title: Paramètres du profil
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 75%

---



# Paramètres de profils

Lisez cet article pour savoir comment définir les paramètres du profil d’élève et ajouter une photo de profil. Découvrez comment télécharger le relevé de notes d’élève pour votre profil.

## Configuration des paramètres de profil {#configuringprofilesettings}

1. Dans l’angle supérieur droit de la page, cliquez sur la flèche déroulante en regard de votre photo ou de votre profil.
1. Sélectionnez Paramètres de profils.
1. Dans la boîte de dialogue contextuelle qui s’affiche, vous pouvez réaliser les actions suivantes :

   * Ajoutez une photo de profil ou mettez à jour la photo existante : placez le pointeur de la souris sur la photo. Cliquez sur Charger et ajoutez une photo. Cliquez sur Modifier pour modifier la photo.
   * Supprimer la photo : placez le pointeur de la souris sur la photo de profil. Cliquez sur Supprimer.
   * Ajoutez du contenu À propos de moi en cliquant sur la zone de texte située au-dessous.
   * Modifiez le contenu À propos de moi en cliquant sur Modifier en regard du champ.
   * Définissez les paramètres régionaux de votre profil. Dans la liste déroulante Paramètres régionaux, sélectionnez la langue de votre choix.
   * Définissez les paramètres régionaux actuels de votre profil.
   * Définissez le fuseau horaire de votre profil.
   * Téléchargez le relevé de notes des élèves avec vos données.

   ![](assets/learner-preferences.png)
   *Afficher les préférences de l’élève*

   Lorsque vous cliquez sur le lien Télécharger mon transcript d’apprentissage (XLS), une feuille Excel est téléchargée sur votre système. Cette feuille Excel contient des informations sur les objets d’apprentissage que vous utilisez, l’état d’achèvement de chaque objet d’apprentissage, les dates d’échéance correspondantes, les compétences obtenues, et ainsi de suite. Téléchargez cette feuille pour obtenir rapidement des informations globales pour votre profil d’apprentissage.

1. Si un administrateur a activé l’option E-mail de résumé et que vous ne figurez pas dans la liste NPD, vous pouvez vous abonner ou vous désabonner aux e-mails de résumé. Activez l’option ci-dessous.

   ![](assets/digest-email-option-learner.png)
   *S’abonner ou se désabonner des e-mails de résumé*

   En fonction de la fréquence définie par l’administrateur, vous, l&#39;élève, recevrez l&#39;e-mail toutes les deux semaines ou tous les mois.

## Se désabonner des e-mails de résumé {#unsubscribefromdigestemails}

Lorsque vous recevez un e-mail, vous pouvez vous désabonner de l’e-mail de résumé en cliquant sur le bouton **Se désabonner** au bas de l’e-mail.

Après avoir cliqué **[!UICONTROL Se désabonner]**, vous êtes redirigé vers votre **Paramètres du profil** , où vous pouvez désactiver l’option de réception des e-mails.

## Anatomie d’un e-mail de résumé {#anatomyofadigestemail}

Un e-mail de résumé se compose des sections suivantes :

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Section</b></p></td>
   <td>
    <p><b>Description</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Résumé de la formation personnelle</p></td>
   <td>
    <p>Cette section personnalise les mesures de formation d’un élève en mentionnant le nombre de minutes consacrées aux formations.</p>
    <p>En fonction du temps passé par l’élève, le contenu est personnalisé selon les règles définies ci-dessous :</p>
    <p>Si (time_spent) &gt;= 60 minutes, le texte suivant s'affiche :</p>
    <p><i>« Au cours des deux dernières semaines/du dernier mois, vous avez <b>(time_spent)</b> minutes de formation pour vous perfectionner. Vous trouverez ci-dessous quelques recommandations pour vous permettre d’en savoir plus. » </i></p>
    <p> Si (time_spent) &lt; 60 minutes, le texte suivant s'affiche :</p>
    <p><i>« Au cours des deux dernières semaines/du dernier mois, vous avez <b>(time_spent)</b> minutes de formation pour vous perfectionner. Vous trouverez ci-dessous quelques recommandations qui, nous l’espérons, vous seront utiles pour commencer et continuer. »</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Activité de formation</p></td>
   <td>
    <p>Cette section affiche un résumé des activités de formation au niveau de l’organisation pour ce compte.</p>
    <p>Le résumé des activités de formation se compose des éléments suivants : </p>
    <ul>
     <li>Nombre de formations disponibles dans le compte.</li>
     <li>Nombre de co-élèves qui suivent activement des activités de formation.</li>
     <li>Nombre d'heures de formation suivies par les collègues.</li>
     <li>Temps moyen (en minutes) passé par les collègues à monter en compétence dans le compte.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Cours recommandés</p></td>
   <td>
    <p>Il s’agit d’une section personnalisée incluant les formations recommandées aux élèves. Dans cette section, un élève peut voir trois formations qui ont été sélectionnées par le moteur de recommandation.</p>
    <p>Chaque formation comporte un bouton Explorer qui, lorsque l’utilisateur clique dessus, le redirige vers la page d’accueil de l’application Élève.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Tableau des scores</p></td>
   <td>
    <p>Affiche un graphique dont chaque barre représente un élève, ainsi que les points de ludification de chaque élève (uniquement si l’administrateur a activé l’option Ludification pour tous les élèves).</p>
    <p>Le tableau des scores affiche les éléments suivants :</p>
    <ul>
     <li>Points obtenus par un élève.</li>
     <li>Points nécessaires pour atteindre le niveau suivant.</li>
    </ul>
    <p>Un mini tableau des scores montre également le leader et les deux élèves les plus proches de l’élève dans cette étendue utilisateur.</p>
    <p>Si le tableau des scores est vide, cette section n’apparaît pas dans l’e-mail.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Publications de réseaux sociaux</a></p></td>
   <td>
    <p>Cette section affiche les trois dernières publications de réseaux sociaux.</p>
    <p>Un élève peut voir la date de création, le nom du forum, le titre de la publication, le cas échéant, le nom d’utilisateur et l’icône de l'auteur. La publication peut également contenir une vidéo, un document, un pdf ou tout autre fichier.</p>
    <p>Chaque publication comporte des liens permettant de rediriger l’élève vers la page d’apprentissage par les réseaux sociaux de l’application Élève.</p>
    <p>Si aucune publication récente n'est disponible, l'élève ne verra pas cette section de l’e-mail.</p></td>
  </tr>
 </tbody>
</table>

## Forum aux questions {#frequentlyaskedquestions}

**1. Comment télécharger un relevé de notes en tant qu’élève ?**

Dans le coin supérieur droit, cliquez sur votre **[!UICONTROL profil utilisateur]** > **[!UICONTROL Paramètres du profil]**. Dans la boîte de dialogue qui apparaît, cliquez sur **Télécharger Mon relevé de notes d’apprentissage (XLS)**.

![](assets/dowload-lt.png)
*Télécharger le relevé de notes de l’élève*
