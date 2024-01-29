---
description: Lisez cet article pour savoir comment définir les paramètres du profil de l’élève et ajouter une photo de profil. Découvrez comment télécharger le relevé de notes de l’élève pour votre profil.
jcr-language: en_us
title: Paramètres du profil
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 0%

---



# Paramètres du profil

Lisez cet article pour savoir comment définir les paramètres du profil de l’élève et ajouter une photo de profil. Découvrez comment télécharger le relevé de notes de l’élève pour votre profil.

## Configuration des paramètres de profil {#configuringprofilesettings}

1. Dans le coin supérieur droit de la page, cliquez sur la flèche déroulante en regard de votre profil ou de votre photo.
1. Sélectionnez Paramètres du profil.
1. Dans la boîte de dialogue contextuelle qui s’affiche, vous pouvez effectuer les actions suivantes :

   * Ajouter/mettre à jour une photo de profil : survolez la photo. Cliquez sur Charger et ajoutez une photo. Cliquez sur Modifier pour modifier la photo.
   * Supprimer la photo : survolez la photo de profil. Cliquez sur Supprimer.
   * Ajoutez du contenu À propos de moi en cliquant sur la zone de texte située en dessous.
   * Modifiez le contenu About Me en cliquant sur Modifier en regard du champ.
   * Définissez les paramètres régionaux pour votre profil. Dans la liste déroulante Paramètres régionaux, sélectionnez la langue de votre choix.
   * Définissez les paramètres régionaux actuels pour votre profil.
   * Définissez le fuseau horaire de votre profil.
   * Téléchargez le relevé de notes des élèves avec vos données.

   ![](assets/learner-preferences.png)
   *Afficher les préférences de l’élève*

   Lorsque vous cliquez sur le lien XLS Télécharger mon relevé de notes d&#39;apprentissage, une feuille Excel est téléchargée sur votre système. Cette feuille Excel contient des détails sur les objets d’apprentissage que vous avez utilisés, l’état d’achèvement de chaque objet d’apprentissage, les dates d’échéance correspondantes, les compétences acquises, etc. Téléchargez cette feuille pour obtenir rapidement des données globales pour votre profil d’apprentissage.

1. Si un administrateur a activé l’option E-mail de résumé et que vous ne figurez pas dans la liste NPD, vous pouvez vous abonner ou vous désabonner aux e-mails de résumé. Activez l’option ci-dessous.

   ![](assets/digest-email-option-learner.png)
   *S’abonner ou se désabonner des e-mails de résumé*

   En fonction de la fréquence définie par l’administrateur, vous, l’élève recevrez l’e-mail toutes les deux semaines ou tous les mois.

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
    <p>En fonction du temps passé par l’élève, le contenu est personnalisé en fonction des règles définies ci-dessous :</p>
    <p>Si (time_spent) &gt;= 60 minutes, le texte suivant apparaît :</p>
    <p><i>« Au cours des deux dernières semaines/du dernier mois, vous avez <b>(time_spent)</b> minutes de formation pour vous perfectionner. Vous trouverez ci-dessous quelques recommandations pour vous permettre d’en savoir plus. » </i></p>
    <p> Si (time_spent) &lt; 60 minutes, le texte suivant s'affiche :</p>
    <p><i>« Au cours des deux dernières semaines/du dernier mois, vous avez <b>(time_spent)</b> minutes de formation pour vous perfectionner. Vous trouverez ci-dessous quelques recommandations qui, nous l’espérons, vous seront utiles pour commencer et continuer. »</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Activité de formation</p></td>
   <td>
    <p>Cette section affiche le récapitulatif au niveau de l’organisation des activités de formation pour ce compte.</p>
    <p>Le résumé des activités de formation se compose des éléments suivants : </p>
    <ul>
     <li>Nombre de formations disponibles dans le compte.</li>
     <li>Nombre de coélèves qui ont activement suivi les activités de formation.</li>
     <li>Nombre d’heures d’apprentissage passées par les collègues.</li>
     <li>Temps moyen (en minutes) passé par les collègues à améliorer les compétences dans le compte.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Cours recommandés</p></td>
   <td>
    <p>Il s’agit d’une section personnalisée qui inclut les formations recommandées pour les élèves. Dans cette section, un élève peut voir trois formations sélectionnées par le moteur de recommandations.</p>
    <p>Chaque formation dispose d’un bouton Explorer qui, lorsqu’il est cliqué, redirige vers la page d’accueil de l’application de l’élève.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Classement</p></td>
   <td>
    <p>Affiche un graphique à barres avec chaque barre représentant un élève ainsi que les points de ludification de chaque élève (uniquement si l’administrateur a activé la ludification pour tous les élèves).</p>
    <p>Le tableau des scores affiche les éléments suivants :</p>
    <ul>
     <li>Points gagnés par un élève.</li>
     <li>Points nécessaires pour passer au niveau supérieur.</li>
    </ul>
    <p>Il existe également un mini-tableau des scores qui montre la scores principal et deux élèves les plus proches de l'élève dans cette portée d'utilisateur.</p>
    <p>Si le tableau des scores est vide, cette section ne s’affiche pas dans l’e-mail.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Publications pour les réseaux sociaux</a></p></td>
   <td>
    <p>Cette section affiche les trois publications sociales les plus récentes.</p>
    <p>Un élève peut voir la date de création, le nom du forum, le titre de la publication, le cas échéant, le nom d’utilisateur et l’icône du créateur. La publication peut également contenir une vidéo, un document, un pdf ou tout autre fichier.</p>
    <p>Chaque publication contient des liens pour rediriger l’élève vers la page d’apprentissage par les réseaux sociaux de l’application Élève.</p>
    <p>S’il n’y a pas de publications récentes, cette section de l’e-mail ne sera pas visible par l’élève.</p></td>
  </tr>
 </tbody>
</table>

## Foire aux questions {#frequentlyaskedquestions}

**1. Comment télécharger un relevé de notes en tant qu’élève ?**

Dans le coin supérieur droit, cliquez sur votre **[!UICONTROL profil utilisateur]** > **[!UICONTROL Paramètres du profil]**. Dans la boîte de dialogue qui apparaît, cliquez sur **Télécharger Mon relevé de notes d’apprentissage (XLS)**.

![](assets/dowload-lt.png)
*Télécharger le relevé de notes de l’élève*
