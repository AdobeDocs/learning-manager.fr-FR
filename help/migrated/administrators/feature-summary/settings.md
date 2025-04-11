---
description: Découvrez les paramètres de compte Learning Manager que vous pouvez configurer en tant qu’administrateur.
jcr-language: en_us
title: Paramètres
contentowner: manochan
exl-id: a563d955-f67e-4218-88df-625cde673601
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '3669'
ht-degree: 65%

---

# Paramètres

Découvrez les paramètres de compte Learning Manager que vous pouvez configurer en tant qu’administrateur.

Vous pouvez modifier les paramètres du profil de l’administrateur et mettre à jour les paramètres du compte. Affichez vos informations de profil, ajoutez/modifiez la photo de profil et modifiez le contenu de **[!UICONTROL À propos de moi]**. Mettez à jour les informations de votre entreprise, installez les méthodes de connexion pour les utilisateurs, et configurez l’intégration de Connect à l’aide des paramètres du compte.

![](assets/settings-admin.png)

## Configuration d’Adobe Learning Manager

Cette formation permet d’acquérir les bases des paramètres au niveau du compte.

[![bouton](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/7476018)


Si vous ne pouvez pas lancer la formation, écrivez à <almacademy@adobe.com>.

## Paramètres du compte {#accountsettings}

Pour mettre à jour les paramètres du compte de votre organisation, cliquez sur **[!UICONTROL Paramètres]** dans le volet de gauche.

**Informations de base (Informations sur la société)**

Cliquez sur **[!UICONTROL Modifier]** sur la page et modifiez le pays, le fuseau horaire, les paramètres régionaux et les paramètres de l&#39;exercice.

**Configuration des données de contact de l’administrateur**

Si vous souhaitez ajouter ou modifier les adresses électroniques des administrateurs de support pour votre entreprise, vous pouvez les configurer en cliquant sur **[!UICONTROL Général]** dans le volet de gauche. Cliquez sur **[!UICONTROL Modifier]** en regard de **[!UICONTROL ID de messagerie de support]** et ajoutez les ID de messagerie. Un e-mail est envoyé à ces administrateurs lorsque l&#39;élève clique sur **[!UICONTROL Contacter l&#39;administrateur]** en bas de page.

Ajoutez d’autres ID de messagerie avec un point-virgule comme séparateur.

**Méthodes de connexion** : les administrateurs peuvent choisir le mode d’accès au compte pour vos utilisateurs internes ou externes.

* **Utilisateurs internes :** pour les utilisateurs internes, vous pouvez définir Adobe ID ou l’authentification unique comme mode de connexion.
* **Utilisateurs externes :** pour les utilisateurs externes, vous pouvez définir un ID Adobe ID, Authentification unique ou Learning Manager.

Si vous choisissez l’ID Learning Manager, les utilisateurs externes peuvent se connecter à ce compte après avoir créé leurs nom d’utilisateur et mot de passe Learning Manager.

>[!NOTE]
>
>Si plusieurs profils externes sont définis, tous les profils peuvent avoir un seul type de connexion. Par exemple, si le type de connexion est défini sur Adobe ID, les profils ne peuvent utiliser que l’Adobe ID pour se connecter. Les profils ne peuvent pas utiliser un type de connexion individuel.

Vous pouvez accéder à l’application Learning Manager en utilisant un ID Adobe ou l’authentification unique. L’authentification unique est un mécanisme permettant à un utilisateur de s’authentifier une fois et d’accéder à plusieurs applications de nombreuses fois. Cette configuration n’est pas obligatoire pour l’entreprise. Si votre entreprise possède un fournisseur d’authentification unique basée sur SAML 2.0, vous pouvez l’utiliser pour configurer l’application Learning Manager. La configuration doit être effectuée au niveau de l’entreprise et de l’application Learning Manager. Si vous choisissez d’utiliser l’authentification unique, contactez l’assistance d’Adobe pour obtenir les instructions de configuration

**Commentaire** 

Cliquez sur **[!UICONTROL Commentaire]** dans le panneau de gauche pour installer le questionnaire pour obtenir des commentaires des stagiaires après l&#39;exécution d&#39;un cours. Reportez-vous au [contenu d&#39;aide sur les fonctionnalités des cours](/help/migrated/administrators/feature-summary/courses.md#add-l1-and-l3-feedback) concernant la création de commentaires L1 et L3.

**Tentatives multiples**

Sélectionnez **[!UICONTROL Paramètres]** > **[!UICONTROL Général]** > **[!UICONTROL Tentatives Multiples]**.

Si vous activez la case à cocher « Tentatives multiples », les auteurs peuvent définir « Tentatives multiples » pour les cours ou modules de formation en ligne interactifs. Lorsque vous cochez la deuxième case, les administrateurs peuvent définir « Tentatives infinies » par défaut pour tout cours de formation en ligne interactif nouvellement créé.

![](assets/admin-config.png)

*Cochez la case Tentatives multiples*

**Modération de cours**

Cliquez sur **[!UICONTROL Général]** dans le volet de gauche, puis cochez la case Modération de cours pour activer la fonctionnalité correspondante. Pour en savoir plus sur cette fonction, voir [Modération de cours](courses.md#main-pars_header_1879001177).

**Tableau de bord des discussions**

Si vous avez coché la case Forum de discussion, les élèves et les formateurs peuvent publier des commentaires sur les cours à l’aide de l’onglet Discussion de la page Cours dans l’application Élèves. Cependant, si les paramètres de niveau de cours indiquent que cette fonctionnalité n’est pas sélectionnée, ces paramètres sont prioritaires par rapport aux paramètres de l’administrateur.

**Tableau de bord de l’élève**

Dans le volet de gauche, cliquez sur Tableau de bord de l’élève. Cette page vous permet de sélectionner les widgets à afficher sur la page Élèves. Sélectionnez les widgets que vous souhaitez activer sur la page Élèves. Les éléments non sélectionnés ne s’afficheront pas sur la page Élèves.

**Adobe Connect** 

Cliquez sur **[!UICONTROL Adobe Connect]** dans le volet de gauche pour configurer le compte Adobe Connect afin d&#39;héberger les sessions de classe virtuelle. Pour plus d’informations, reportez-vous à l’aide sur les fonctionnalités d’Adobe  [Connect](adobeconnect-integration.md) .

## Paramètres généraux {#general}

Activation ou désactivation des paramètres suivants :

<table>
 <tbody>
  <tr>
   <th>
    <p><b>Nom</b></p>
    </th>
   <th>
    <p><b>Description</b></p>
   </th>
  </tr>
  <tr>
   <td>Afficher l’efficacité du cours</td>
   <td>Si cette option est activée, les élèves peuvent voir l’efficacité actuelle du cours sur la vignette du cours. Cette fonctionnalité est uniquement disponible pour les cours. L’évaluation par étoiles n’est pas prise en charge pour les programmes d’apprentissage ou les certificats. Elle est disponible pour les cours et les programmes d’apprentissage, mais pas pour les certifications.</td>
  </tr>
  <tr>
   <td>Modération de cours</td>
   <td>Si cette option est activée, toutes les modifications apportées aux cours devront être approuvées par l’administrateur avant d’être visibles par les élèves.</td>
  </tr>
  <tr>
   <td>Forum de discussion</td>
   <td>Si vous avez coché la case Forum de discussion, les élèves et les formateurs peuvent publier des commentaires sur les cours à l’aide de l’onglet Discussion de la page Cours dans l’application Élèves. Cependant, si les paramètres de niveau de cours indiquent que cette fonctionnalité n’est pas sélectionnée, ces paramètres sont prioritaires par rapport aux paramètres de l’administrateur.</td>
  </tr>
  <tr>
   <td>Tentatives multiples</td>
   <td>Si cette option est activée, l’auteur peut configurer plusieurs tentatives pour les modules de cours.</td>
  </tr>
  <tr>
   <td>Option Explorer les compétences</td>
   <td>Si cette option est activée, les élèves peuvent explorer les compétences Homologue et Leadership et s’abonner aux compétences de leur choix.</td>
  </tr>
  <tr>
   <td>Visibilité des balises/compétences</td>
   <td>Affichage de toutes les compétences et balises pour les élèves. Vous pouvez soit afficher toutes les compétences et balises, soit afficher les compétences et les balises qui sont attribuées, ou celles faisant partie des catalogues visibles par l’élève.</td>
  </tr>
  <tr>
   <td>ID d’objet d’apprentissage uniques</td>
   <td>Si cette option est activée, un administrateur ou un auteur peut ajouter un ID unique pour chaque objet d’apprentissage.</td>
  </tr>
  <tr>
   <td>Affichage des panneaux de filtrage</td>
   <td>
    <p><a id="filter-panels"></a>Contrôlez les panneaux de filtrage qui sont disponibles pour les utilisateurs dans l’application de l’élève afin d’affiner leurs résultats de recherche. Les options sont les suivantes :</p>
    <ul>
     <li>Catalogues</li>
     <li>Type</li>
     <li>Format</li>
     <li>Durée</li>
     <li>Compétences</li>
     <li>Niveaux de compétence</li>
     <li>Balises</li>
    </ul>
    <p>Lorsqu’un élève lance l’application de l’élève, il peut voir les filtres dans leurs panneaux respectifs, dans les sections Mon apprentissage et Catalogue.</p>
    <p><b>Remarque : </b>les filtres <b>Format </b>et <b>Durée </b>sont désactivés par défaut et n’apparaissent pas aux élèves immédiatement après la publication. L’administrateur doit les activer. <br></p></td>
  </tr>
  <tr>
   <td>Afficher la liste des catalogues</td>
   <td>Si cette option est activée, les élèves peuvent afficher la liste de tous les catalogues disponibles. Les élèves peuvent ainsi affiner la recherche et l’affichage de leurs objets d’apprentissage.</td>
  </tr>
  <tr>
   <td>Terminologie du produit</td>
   <td>Learning Manager comporte une terminologie standard, utilisée dans l’ensemble du produit. Modifiez la terminologie en fonction des besoins de votre organisation.</td>
  </tr>
  <tr>
   <td>Mise à jour de la version du module</td>
   <td>Configurez le paramètre par défaut pour mettre à jour le contenu. Les paramètres peuvent être modifiés pour chaque contenu de la page du cours.</td>
  </tr>
  <tr>
   <td>Enregistrement automatique des utilisateurs</td>
   <td>Si cette option est activée, les utilisateurs nouvellement importés sont automatiquement enregistrés. Par défaut, les utilisateurs doivent être enregistrés avant de pouvoir utiliser Learning Manager.</td>
  </tr>
  <tr>
   <td><a id="autodelete"></a>Supprimer automatiquement les utilisateurs internes</td>
   <td>Si cette option est activée, les utilisateurs internes sont automatiquement supprimés s’ils n’accèdent pas au système pendant un nombre de jours spécifié. Cette fonctionnalité s’applique aux utilisateurs qui n’ont que le rôle <b>Élève</b>. Pour rétablir l’accès, les utilisateurs doivent contacter l’administrateur.<br></td>
  </tr>
  <tr>
   <td>Afficher les étiquettes de catalogue</td>
   <td>Si cette option est activée, les administrateurs et les auteurs peuvent définir des étiquettes et des valeurs de catalogue et les lier à des objets d’apprentissage. La sélection de cette option permet également aux auteurs d’ajouter des cours, des parcours d’apprentissage, des certifications ou des assistances à la tâche aux catalogues.</td>
  </tr>
  <tr>
   <td>Les élèves peuvent consulter leurs scores</td>
   <td>Si cette option est activée, les élèves peuvent consulter leurs scores dans le relevé de notes de l’élève.</td>
  </tr>
  <tr>
   <td>E-mail de résumé</td>
   <td>
    <p>Un administrateur peut activer ou désactiver l’envoi d’un e-mail aux élèves. L’administrateur pourra également contrôler la fréquence des e-mails envoyés.</p>
    <ul>
     <li>Pour les <b>comptes actifs</b>, les e-mails de résumé sont désactivés par défaut, et l’administrateur peut les activer manuellement.</li>
     <li>Pour les <b>comptes d’essai</b>, les e-mails de résumé restent désactivés, et l’administrateur ne peut pas activer cette option.</li>
    </ul>
    <p>Si la fonctionnalité est désactivée :</p>
    <ul>
     <li>L’option <b>E-mail de résumé</b> sera désactivée.</li>
     <li>Un élève ne peut pas voir le paramètre utilisateur pour l’abonnement aux e-mails de résumé.</li>
    </ul>
    <p> Si la fonctionnalité est activée :</p>
    <ul>
     <li>L’administrateur peut activer et modifier l’option E-mail de résumé.</li>
     <li>Dans les <b>paramètres du profil</b> de l’application de l'élève, l'élève (qui ne figure pas dans la liste NPD) peut choisir de s’abonner ou de se désabonner de l’e-mail de résumé.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Activer les icônes des cartes de formation<br></td>
   <td>Si cette option est activée, des icônes apparaîtront sur les cartes de formation dans l’application d’apprentissage.<br></td>
  </tr>
  <tr>
   <td>Liens du pied de page</td>
   <td>
    <p>Ajoutez des liens ou des ID de messagerie qui apparaissent en pied de page. Vous pouvez ajouter un maximum de trois liens dans le pied de page.</p>
    <p>Pour personnaliser les liens du pied de page, suivez les étapes suivantes :</p>
    <ol>
     <li>Cliquez sur <b>Ajouter plus</b>, saisissez le nom et l’URL ou l’ID de messagerie dans les champs spécifiés. Ajoutez le préfixe http:// ou https:// à l’URL.</li>
     <li>Pour appliquer la modification à toutes les langues, cliquez sur <b>Répliquer</b>. Cela permet de s’assurer que toutes les langues obtiennent le nom et l’URL.</li>
     <li>Cliquez sur <b>Enregistrer</b> pour enregistrer les modifications. Un message s’affiche pour confirmer la modification. Cliquez sur OK pour que le pied de page soit rempli avec les nouveaux liens ajoutés.</li>
    </ol>
    <p>De plus, vous pouvez :</p>
    <ul>
     <li>Cliquez sur l'icône <b>Réinitialiser</b> pour réinitialiser les valeurs par défaut dans les champs <b>Aide</b> et <b>Contacter l'administrateur</b>.</li>
     <li>Personnaliser le lien sur le pied de page pour toutes les langues. Cliquez sur la liste déroulante <b>Langue</b>, sélectionnez la langue et ajoutez le <b>Nom</b> et l’<b>URL</b> dans les champs spécifiés. Après avoir sauvegardé les modifications, les liens mis à jour s’affichent dans le pied de page.<br></li>
    </ul></td>
  </tr>
  <tr>
   <td>Fuseau horaire du rapport<br></td>
   <td>
    <p>Définissez une préférence au niveau du compte pour exporter le relevé de notes dans les fuseaux horaires suivants :</p>
    <ul>
     <li>UTC (comportement par défaut)</li>
     <li>Préférence de fuseau horaire au niveau du compte</li>
    </ul>
    <p>Le relevé de notes de l’élève téléchargé à l’aide de l’API des tâches télécharge également les données dans le fuseau horaire sélectionné.</p>
    <p><b>Remarque :</b>Aucune modification n'est attendue dans le relevé de notes de l'élève par défaut immédiatement après la publication. Les administrateurs peuvent configurer ce paramètre dans l’application d’administration &gt; Paramètres &gt; Général &gt; Fuseau horaire du rapport.</p></td>
  </tr>
 </tbody>
</table>

<table border="0" cellpadding="0" cellspacing="0" width="1709">
 <tbody>
  <tr>
   <td height="20" width="147">Nom</td>
   <td>Description</td>
  </tr>
  <tr>
   <td height="20">Afficher l’efficacité du cours</td>
   <td>Si l’option est activée, les élèves pourront visualiser l’efficacité actuelle du cours dans la vignette correspondante.</td>
  </tr>
  <tr>
   <td height="20">Modération de cours</td>
   <td>Si cette option est activée, toutes les modifications apportées aux cours devront être approuvées par l’administrateur avant d’être visibles par les élèves.</td>
  </tr>
  <tr>
   <td height="20">Forum de discussion</td>
   <td>Si vous avez coché la case Forum de discussion, les élèves et les formateurs peuvent publier des commentaires sur les cours à l’aide de l’onglet Discussion de la page Cours dans l’application Élèves. Cependant, si les paramètres de niveau de cours indiquent que cette fonctionnalité n’est pas sélectionnée, ces paramètres sont prioritaires par rapport aux paramètres de l’administrateur.</td>
  </tr>
  <tr>
   <td height="20">Tentatives multiples</td>
   <td>Si cette option est activée, l’auteur peut configurer plusieurs tentatives pour les modules de cours.</td>
  </tr>
  <tr>
   <td height="20">Option Explorer les compétences</td>
   <td>Si cette option est activée, les élèves peuvent explorer les compétences Homologue et Leadership et s’abonner aux compétences de leur choix.</td>
  </tr>
  <tr>
   <td height="20">Visibilité des balises/compétences</td>
   <td>Affichage de toutes les compétences et balises pour les élèves. Vous pouvez soit afficher toutes les compétences et balises, soit afficher les compétences et les balises qui sont attribuées, ou celles faisant partie des catalogues visibles par l’élève.</td>
  </tr>
  <tr>
   <td height="20">ID d’objet d’apprentissage uniques</td>
   <td>Si cette option est activée, un administrateur ou un auteur peut ajouter un ID unique pour chaque objet d’apprentissage.</td>
  </tr>
  <tr>
   <td rowspan="10" height="191">Affichage des panneaux de filtrage</td>
   <td>Contrôlez les panneaux de filtrage qui sont disponibles pour les utilisateurs dans l’application de l’élève afin d’affiner leurs résultats de recherche. Les options sont les suivantes :</td>
  </tr>
  <tr>
   <td height="19">Catalogues</td>
  </tr>
  <tr>
   <td height="19">Type</td>
  </tr>
  <tr>
   <td height="19">Format</td>
  </tr>
  <tr>
   <td height="19">Durée</td>
  </tr>
  <tr>
   <td height="19">Compétences</td>
  </tr>
  <tr>
   <td height="19">Niveaux de compétence</td>
  </tr>
  <tr>
   <td height="19">Balises</td>
  </tr>
  <tr>
   <td height="19">Lorsqu’un élève lance l’application de l’élève, il peut voir les filtres dans leurs panneaux respectifs, dans les sections Mon apprentissage et Catalogue.</td>
  </tr>
  <tr>
   <td height="20">Remarque : les filtres Format et Durée sont désactivés par défaut et n’apparaissent pas aux élèves immédiatement après la publication. L’administrateur doit les activer. </td>
  </tr>
  <tr>
   <td height="20">Afficher la liste des catalogues</td>
   <td>Si cette option est activée, les élèves peuvent afficher la liste de tous les catalogues disponibles. Les élèves peuvent ainsi affiner la recherche et l’affichage de leurs objets d’apprentissage.</td>
  </tr>
  <tr>
   <td height="20">Terminologie du produit</td>
   <td>Learning Manager comporte une terminologie standard, utilisée dans l’ensemble du produit. Modifiez la terminologie en fonction des besoins de votre organisation.</td>
  </tr>
  <tr>
   <td height="20">Mise à jour de la version du module</td>
   <td>Configurez le paramètre par défaut pour mettre à jour le contenu. Les paramètres peuvent être modifiés pour chaque contenu de la page du cours.</td>
  </tr>
  <tr>
   <td height="20">Enregistrement automatique des utilisateurs</td>
   <td>Si cette option est activée, les utilisateurs nouvellement importés sont automatiquement enregistrés. Par défaut, les utilisateurs doivent être enregistrés avant de pouvoir utiliser Learning Manager.</td>
  </tr>
  <tr>
   <td height="20">Supprimer automatiquement les utilisateurs internes</td>
   <td>Si cette option est activée, les utilisateurs internes sont automatiquement supprimés s’ils n’accèdent pas au système pendant un nombre de jours spécifié. Cette fonctionnalité s’applique aux utilisateurs qui n’ont que le rôle Élève. Pour rétablir l’accès, les utilisateurs doivent contacter l’administrateur.</td>
  </tr>
  <tr>
   <td height="20">Afficher les étiquettes de catalogue</td>
   <td>Si cette option est activée, les administrateurs et les auteurs peuvent définir des étiquettes de catalogue et des valeurs et les associer à des objets d’apprentissage.</td>
  </tr>
  <tr>
   <td height="20">Les élèves peuvent consulter leurs scores</td>
   <td>Si cette option est activée, les élèves peuvent consulter leurs scores dans le relevé de notes de l’élève.</td>
  </tr>
  <tr>
   <td rowspan="9" height="172">E-mail de résumé</td>
   <td>Un administrateur peut activer ou désactiver l’envoi d’un e-mail aux élèves. L’administrateur pourra également contrôler la fréquence des e-mails envoyés.</td>
  </tr>
  <tr>
   <td height="19">Pour les comptes actifs, les e-mails de résumé sont désactivés par défaut, que l’administrateur peut activer manuellement.</td>
  </tr>
  <tr>
   <td height="19">Pour les comptes d’évaluation, l’option pour les e-mails de résumé reste désactivée et l’administrateur ne peut pas activer l’option.</td>
  </tr>
  <tr>
   <td height="19">Si la fonctionnalité est désactivée :</td>
  </tr>
  <tr>
   <td height="19">L’option E-mail de résumé sera désactivée.</td>
  </tr>
  <tr>
   <td height="19">Un élève ne peut pas voir le paramètre utilisateur pour l’abonnement aux e-mails de résumé.</td>
  </tr>
  <tr>
   <td height="19"> Si la fonctionnalité est activée, alors :</td>
  </tr>
  <tr>
   <td height="19">L’administrateur peut activer et modifier l’option E-mail de résumé.</td>
  </tr>
  <tr>
   <td height="20">À partir des paramètres du profil de l’application learber, un élève (qui ne figure pas dans la liste NPD) peut choisir de s’abonner ou de se désabonner du courriel de synthèse.</td>
  </tr>
  <tr>
   <td height="20">Activer les icônes des cartes de formation</td>
   <td>Si cette option est activée, des icônes apparaîtront sur les cartes de formation dans l’application d’apprentissage.</td>
  </tr>
  <tr>
   <td rowspan="8" height="153">Liens du pied de page</td>
   <td>Ajoutez des liens ou des ID de messagerie qui apparaissent en pied de page. Vous pouvez ajouter un maximum de trois liens dans le pied de page.</td>
  </tr>
  <tr>
   <td height="19">Pour personnaliser les liens du pied de page, suivez les étapes suivantes :</td>
  </tr>
  <tr>
   <td height="19">1. Cliquez sur Ajouter plus, entrez le nom et l’URL ou l’identifiant de messagerie dans les champs spécifiés. Ajoutez le préfixe http:// ou https:// à l’URL.</td>
  </tr>
  <tr>
   <td height="19">2. Pour répercuter la modification sur tous les paramètres régionaux, cliquez sur Répliquer. Cela permet de s’assurer que toutes les langues obtiennent le nom et l’URL.</td>
  </tr>
  <tr>
   <td height="19">3. Pour enregistrer les modifications, cliquez sur Enregistrer. Un message s’affiche pour confirmer la modification. Cliquez sur OK pour que le pied de page soit rempli avec les nouveaux liens ajoutés.</td>
  </tr>
  <tr>
   <td height="19">De plus, vous pouvez :</td>
  </tr>
  <tr>
   <td height="19">Cliquez sur l’icône Réinitialiser pour réinitialiser les valeurs par défaut dans les champs Aide et Contacter l’administrateur.</td>
  </tr>
  <tr>
   <td height="20">Personnaliser le lien sur le pied de page pour toutes les langues. Cliquez sur la liste déroulante Langue, sélectionnez la langue, puis ajoutez le Nom et l’URL dans les champs spécifiés. Après avoir sauvegardé les modifications, les liens mis à jour s’affichent dans le pied de page.</td>
  </tr>
  <tr>
   <td rowspan="5" height="96">Fuseau horaire du rapport</td>
   <td> Définissez une préférence au niveau du compte pour exporter le relevé de notes dans les fuseaux horaires suivants :</td>
  </tr>
  <tr>
   <td height="19">UTC (comportement par défaut)</td>
  </tr>
  <tr>
   <td height="19">Préférence de fuseau horaire au niveau du compte</td>
  </tr>
  <tr>
   <td height="19">Le relevé de notes de l’élève téléchargé à l’aide de l’API Jobs télécharge également les données dans le fuseau horaire sélectionné.</td>
  </tr>
  <tr>
   <td height="20">Remarque : Par défaut, aucun changement n’est prévu dans le relevé de notes de l’élève immédiatement après la publication. Les administrateurs peuvent configurer ce paramètre dans l’application d’administration &gt; Paramètres &gt; Général &gt; Fuseau horaire du rapport.</td>
  </tr>
  <tr>
   <td height="19">Intégration de Badgr</td>
   <td>Si cette option est activée, les élèves pourront charger leurs badges sur le site Web Badgr. Dans les scénarios d’éducation des clients, les organisations veulent pouvoir « certifier » leurs clients et leur donner la possibilité d’afficher ces références sur les réseaux sociaux. Cela motive l’élève à suivre une formation et à partager ses résultats avec d’autres. </td>
  </tr>
  <tr>
   <td height="135">
    <p>Afficher l’évaluation</p></td>
   <td>
    <ul>
     <li>Si l’option <b>Efficacité du cours</b> est activée, les élèves ne pourront voir que la valeur de l’efficacité du cours.</li>
     <li>Si l’option <b>Évaluation par étoiles</b> est activée, les élèves ne pourront afficher que la note moyenne et le nombre d’élèves ayant évalué le cours.<br></li>
    </ul>
    <p>Cette fonctionnalité est uniquement disponible pour les cours. L’évaluation par étoiles n’est pas prise en charge pour les programmes d’apprentissage ou les certificats.<br><br><b>Remarque :</b>Cette modification affecte uniquement l’application de l’élève. </p>
    <p>Dans toutes les autres applications (administrateur, auteur, manager, administrateur personnalisé, auteur personnalisé), les modifications des paramètres (évaluation par étoiles/efficacité du cours/désactivation de l’affichage de l’évaluation) n’auront aucun effet. </p>
    <p>Pour les nouveaux comptes, la section <b>Afficher les évaluations</b> aura l'option <b>Évaluation par étoiles</b> activée par défaut.</p>
    <p>Pour les comptes existants, si l'option <b>Efficacité du cours</b> était activée pour le compte précédemment, la section <b>Afficher les évaluations</b> sera activée avec l'option Efficacité du cours sélectionnée. Si l'option <b>Efficacité du cours</b>s est désactivée, la section <b>Afficher les évaluations</b> sera également désactivée. Lorsque la section <b>Afficher les évaluations</b> est activée, l'option <b>Évaluation par étoiles</b> est activée par défaut.</p></td>
  </tr>
  <tr>
   <td height="19">Suppression</td>
   <td>Sélectionnez l’une des options de retrait suivantes :<li>Une fois retirés, les élèves inscrits pourront afficher et effectuer des actions, mais les élèves non encore inscrits perdront l’accès.</li><li>Une fois retirés, les élèves inscrits et non encore inscrits perdront l’accès.</li><div><b>Remarque :</b> vous pouvez retirer des cours, des parcours d'apprentissage ou des certifications de leurs pages de présentation.</div> </td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p>Parcours d’apprentissage</p></td>
   <td>
    <p>Si l’option <b>Activer les fonctionnalités étendues du parcours d’apprentissage</b> est activée, les administrateurs peuvent inclure des parcours d’apprentissage dans les parcours d’apprentissage et les combiner avec les cours. L’option est irréversible.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Gestion de l’instructeur<br></p></td>
   <td>
    <p>Activez ce paramètre pour restreindre la liste des instructeurs qui peuvent être sélectionnés lors de la création des sessions de salle de classe/salle de classe virtuelle Tous les utilisateurs avec le privilège instructeur ne peuvent être désignés que comme instructeur dans une session. Cette restriction ne s’applique pas aux workflows de migration.<br></p>
  </td>
  <tr>
    <td>
      <p>Importation des compétences</p>
    </td>
    <td>
      <p>Si cette option est activée, vous pouvez choisir une source externe pour importer les compétences. Les compétences des ressources d’apprentissage existantes seront importées dans le référentiel de compétences une seule fois lors de l’exécution initiale. Pour toutes les importations ultérieures de ressources d’apprentissage, les compétences seront importées dans le référentiel de compétences uniquement pour les éléments nouvellement importés.
      Une fois l’option activée, l’action est irréversible. Vous ne pouvez pas désactiver ou passer à une autre source ultérieurement.
      </p>
    </td>
  </tr>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>Une fois le paramètre d&#39;importation des compétences activé, la mise en page du compte ne peut pas être basculée vers la vue classique, c&#39;est-à-dire que le basculement vers un compte classique est désactivé après l&#39;activation de l&#39;option **Importation des compétences**.

## Renommer des objets d’apprentissage {#renaminglearningobjects}

Cette fonction est uniquement disponible en anglais.

Les administrateurs peuvent désormais renommer les objets d’apprentissage dans Learning Manager. Les terminologies suivantes peuvent être renommées.

Module\
Cours\
Programme d’apprentissage\
Certification\
Plan d&#39;apprentissage\
Assistance à la tâche\
Catalogue\
Compétence\
Badge\
Annonce\
Mon apprentissage\
Tableau des scores\
Efficacité\
Prérequis\
Prétravail\
Contenu principal\
Test\
À mon propre rythme\
Fusionné\
Salle de classe\
Salle de classe virtuelle\
Activité

## Paramètres du profil {#profilesettings}

1. Cliquez sur la flèche déroulante dans le coin supérieur droit, à côté de votre photo/compte, puis choisissez **[!UICONTROL Paramètres du]** profil.
1. Dans la boîte de dialogue contextuelle, vous pouvez ajouter/modifier une photo en passant la souris et en cliquant sur **[!UICONTROL Modifier]** dans la zone de la photo de profil.
1. Ajouter/modifier **[!UICONTROL À propos]** du contenu en cliquant sur **[!UICONTROL Modifier]** à côté de celui-ci.
1. Cliquez sur **[!UICONTROL Enregistrer].**

## Dossier de contenu {#content-folder}

Learning Manager prend en charge les dossiers de contenu privés. Un administrateur peut configurer des dossiers de contenu privés et fournir son accès à des auteurs personnalisés spécifiques à l’aide de rôles personnalisés. Notez que les auteurs standard (également appelés auteurs complets) conservent l’accès à tout le contenu du compte. Par conséquent, les auteurs complets ont accès à tous les dossiers et à tout le contenu.

Les dossiers de contenu peuvent être configurés par les administrateurs. Une fois configurés, les dossiers de contenu deviennent visibles pour les auteurs, qui peuvent alors placer le contenu dans un ou plusieurs dossiers.

Pour ajouter un dossier de contenu, dans l’application Administrateur, cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Dossier]** de contenu.

![](assets/manage-content-folders.png)

*Modifier les paramètres du dossier de contenu*

### Dossier

Un dossier est un référentiel de contenu, qui est un sous-ensemble de la bibliothèque de contenu complète disponible dans un compte avec les propriétés suivantes :

* Seul un administrateur peut créer, modifier ou supprimer un dossier.
* Un administrateur peut contrôler l’accès aux dossiers dans le cadre de la définition des rôles uniquement pour les administrateurs personnalisés.
* Le contenu **doit à tout moment être associé à au moins un dossier**. Pour commencer, tout le contenu sera associé au dossier Public, qui pourra être modifié ultérieurement.
* Le contenu peut être associé à plusieurs dossiers au moment de la création, ce qui est également possible par une opération de copie.
* Tous les noms de dossier doivent être uniques au sein du compte, faute de quoi une erreur s’affichera lors de la désignation d’un dossier.

Les dossiers contrôlent uniquement la visibilité du contenu et ne créent pas de copies de celui-ci. Par conséquent, la modification du contenu sera répercutée dans tous les dossiers associés.

### Dossier public

Un dossier public est toujours présent dans un compte et tout le contenu sera initialement inclus dans ce dossier. Par la suite, les auteurs peuvent déplacer du contenu de ce dossier vers d’autres dossiers. Un dossier public possède les propriétés suivantes :

* Par défaut, tout le contenu associé à ce dossier sera accessible à tous les types d’auteurs.
* Tout contenu faisant partie d’un dossier public ne peut faire partie d’aucun autre dossier. L’inverse est également vrai.

Ce dossier ne peut pas faire partie de la définition de rôle configurable. Par conséquent, le fait de ne pas avoir de dossier public dans la définition de rôle configurable ne restreint pas l’accès à un dossier public.

### Dossier privé

* Tout dossier créé par un administrateur est un dossier privé.

### Opérations de dossier

**Ajouter un dossier**

Pour ajouter un dossier, cliquez sur **[!UICONTROL Ajouter]** dans le coin supérieur droit de la fenêtre.

**Supprimer un dossier**

Vous pouvez également supprimer un dossier. Sélectionnez le dossier à supprimer, cliquez sur le menu Actions, puis cliquez sur **[!UICONTROL Supprimer le dossier]**.

>[!NOTE]
>
>Les dossiers peuvent être supprimés lorsque tout le contenu associé est également associé à d’autres dossiers. Si du contenu est lié uniquement au dossier en cours de suppression, déplacez d’abord le contenu vers un autre dossier, puis supprimez le dossier.

## Emplacements de classe

Les administrateurs peuvent utiliser ce paramètre pour créer et configurer une bibliothèque d’emplacements de salle de classe. Les auteurs peuvent sélectionner un emplacement préconfiguré pour configurer leur événement de salle de classe. Sélectionnez un emplacement dans la bibliothèque pour renseigner automatiquement les informations d’emplacement, l’URL et la limite de places.

En tant qu’administrateur, vous pouvez :

### Importer des emplacements au format CSV

Ajouter des emplacements à votre compte en important un fichier CSV d’emplacements. Le fichier CSV doit contenir la colonne City.

### Ajouter un lieu

Ajoutez les éléments suivants :

1. Nom du lieu : entrez le nom de la classe.
2. Informations sur le lieu : entrez les informations relatives à l’emplacement.
3. Région du lieu : la valeur saisie s’affiche sous la forme d’un filtre Lieux de formation pour les élèves.
4. URL de l’emplacement : entrez l’URL de l’emplacement.
5. Limite de places : entrez la capacité de la salle.

![emplacement de la salle de classe](assets/location-alm.gif)

*Ajouter des emplacements de salle de classe*

Vous pouvez également ajouter le lieu à l’aide d’un fichier CSV. Le fichier CSV doit contenir les champs suivants :

* name
* info
* url
* seatlimit
* (région)

<!--![Add classroom locations](assets/add-classroom-csv.png)-->

### Paramètres {#admin-classroom-settings}

Sélectionnez **Modifier** pour modifier les éléments suivants :

* **Autoriser les auteurs à créer des lieux** : Une fois activé, tous les lieux créés par les auteurs seront répertoriés sous l’onglet « Tous les lieux ». Les apprenants verront également ces emplacements sous les filtres Catalogue et Calendrier.
* **Autoriser les auteurs à modifier et à supprimer des emplacements** :
Une fois activé, les auteurs pourront modifier et supprimer tous les emplacements de Classroom. Les modifications apportées par les auteurs seront répercutées sur l’ensemble de la plateforme, y compris les rapports.

## Forum aux questions {#frequentlyaskedquestions}

+++Comment créer différents dossiers pour la bibliothèque de contenu ?

Cliquez sur **[!UICONTROL Paramètres]** > **[!UICONTROL Dossier de contenu]**. Pour ajouter un dossier, cliquez sur **[!UICONTROL Ajouter]** dans le coin supérieur droit et, dans la boîte de dialogue, entrez le nom et la description du dossier.

Les dossiers de contenu peuvent être configurés par les administrateurs. Une fois configurés, les dossiers de contenu deviennent visibles pour les auteurs, qui peuvent alors placer le contenu dans un ou plusieurs dossiers.

Pour plus d’informations, consultez la section [Dossier de contenu](settings.md#content-folder).
+++

+++Comment ajouter un exercice financier pour le compte ?

Dans **[!UICONTROL Paramètres]** > **[!UICONTROL Informations de base]**, cliquez sur **[!UICONTROL Modifier]**. Dans la liste déroulante **[!UICONTROL L&#39;exercice commence à partir de]**, sélectionnez le mois.
+++
