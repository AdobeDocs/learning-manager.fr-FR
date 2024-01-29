---
description: Découvrez les nouvelles fonctionnalités et améliorations d’Adobe Learning Manager
jcr-language: en_us
title: Résumé des nouvelles fonctionnalités
contentowner: jayakarr
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '26196'
ht-degree: 0%

---



# Résumé des nouvelles fonctionnalités

<!--<table>
 <tbody>
  <tr>
   <td><img src="assets/cp-prime-appicon-88x84.png"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> was launched in August 2015. As part of our continuous improvement efforts to enhance the product, we have been rolling out regular updates. Read on to know the features enhanced/issues fixed in update releases.<br></p></td>
  </tr>
 </tbody>
</table>-->

+++Mise à jour 95 : version de novembre 2023 d’Adobe Learning Manager

**Date de publication :** 18 novembre 2023

## Nouveautés de cette version

Afficher [Nouveautés d’Adobe Learning Manager](/help/migrated/whats-new.md) pour plus d’informations.
+++

+++Mise à jour 94

**Date de publication :** 23 août 2023

## Nouveautés de cette mise à jour

* Sélectionnez l’icône d’engrenage du lecteur pour modifier la qualité de la vidéo.
* Modifier la qualité et la vitesse d’une vidéo sur les réseaux sociaux.
+++

+++Mise à jour 93 : version de juillet 2023 d’Adobe Learning Manager

**Date de publication :** 10 juillet 2023

Nouveautés de cette version

### Amélioration de Recommendations

Adobe Learning Manager a introduit un nouveau système de recommandations remanié pour les cours. Cette fonctionnalité de recommandations utilise des algorithmes d’IA et les intérêts des utilisateurs tels que les produits, les rôles et les niveaux pour fournir des recommandations de contenu personnalisées.

### Inscription multiple

Dans cette version d&#39;Adobe Learning Manager, nous introduisons l&#39;inscription multiple pour les élèves qui permet aux élèves de s&#39;inscrire à plusieurs instances d&#39;un cours à une ou plusieurs périodes.

### Dépréciation Du Connecteur Exavault

Cette version d’Adobe Learning Manager inclut un nouveau connecteur qui utilise le protocole SFTP de la famille de transfert AWS.

Pour plus d’informations, voir [Nouveautés de la version de juillet 2023 d’Adobe Learning Manager](/help/migrated/whats-new-2023-july.md).
+++

+++Mise à jour : 92

**Date de publication :** 23 juin 2023

**Bogues corrigés dans cette mise à jour**

* Après avoir terminé un module, l’API Grade n’est pas déclenchée automatiquement, ce qui entraîne l’affichage de la coche verte de l’interface utilisateur de manière inattendue.
* Après avoir terminé quelques modules dans un parcours d’apprentissage ou une certification, la coche verte, qui indique la réussite, ne s’affiche pas comme prévu.
* Adobe Learning Manager ne se lance pas comme prévu après le chargement d’un fichier CSV utilisateur avec des champs incorrects.
* La fenêtre contextuelle d’avertissement sur la façon de contacter l’administrateur affiche également d’autres adresses e-mail.
* Tous les badges gagnés par un élève ne s’affichent pas dans la réponse.
* Lors de l’enregistrement de l’utilisateur, un nom d’utilisateur avec « » doit être accepté.

#### Lecteur

* Ajoutez un menu pour sélectionner la résolution d’écran lors de la lecture d’une vidéo.
+++

+++Mise à jour 91

**Date de publication :** 01 juin 2023

### Connecteurs

* Le connecteur Adobe Connect nécessite des API pour envoyer des jetons CSRF. Pour plus d’informations, voir Amélioration de la sécurité du compte Adobe Connect.

### Modification de chaîne

* Nous avons renommé la chaîne Évaluer cette formation pour Évaluer ce cours, Évaluer ce parcours d’apprentissage ou Évaluer cette certification, en fonction de la formation suivie par un élève. Selon le type de formation, un élève voit la chaîne en conséquence.

### Bogues corrigés dans cette mise à jour

* Adobe La description de l’application mobile Learning Manager de Play Store indique de manière incorrecte qu’un élève peut suivre un cours hors ligne.
* Des problèmes sont survenus lors de la migration du contenu (module_version.csv et course_module.csv) de LinkedIn vers Adobe Learning Manager.
* Si un compte est inactif et créé il y a plus de trois ans, tous les utilisateurs du compte sont supprimés conformément au RGPD, quel que soit leur statut.
* Dans l’application de l’instructeur, lorsque vous définissez la limite de liste d’attente sur zéro dans une session et enregistrez la session, l’interface utilisateur affiche de manière incorrecte « Non applicable » au lieu de zéro.
* Lors de la génération des relevés de notes des élèves pour le connecteur de Power BI, la colonne Durée de la formation ou du module (min) affiche des valeurs nulles pour certains modules de salle de classe ou de classe virtuelle.
* Après avoir marqué un cours comme terminé pour les élèves d&#39;une ou plusieurs instances, tous les élèves du cours sont marqués comme terminés, pas seulement les élèves de l&#39;instance ou des instances actuelles.
+++

+++Mise à jour 90

**Date de publication :** 04 avril 2023

### Bogues Corrigés Dans Cette Mise À Jour

La connexion SAML échoue si l’URL de connexion SSO contient entity_id.
+++

+++Mise à jour 89 : version de mars 2023 d’Adobe Learning Manager

**Date de publication :** 01 avril 2023

### Nouveautés de cette mise à jour

**Améliorations apportées à l’expérience de formation avec instructeur**

Plusieurs améliorations ont été apportées à l’expérience de formation dirigée par un instructeur (ILT). Les principales améliorations incluent : la possibilité de filtrer les sessions de classe en fonction de l’emplacement, la possibilité de changer d’instance (VILT) sans perdre la progression, un nouvel « Assistant de planification » pour la gestion des conflits dans la réservation des instructeurs et des salles de classe, la possibilité d’associer des « compétences » aux instructeurs et de choisir des instructeurs en fonction des compétences.

**Améliorations apportées à la liste de contrôle de l&#39;observation**:

Les auteurs peuvent désormais sélectionner « Manager » et « Store Manager » en tant qu’observateur pour les listes de contrôle. Les responsables peuvent afficher et remplir les listes de contrôle dans l’interface du responsable sans avoir à changer de rôle pour un instructeur. Une notification est envoyée à un responsable lorsqu’une liste de contrôle lui est attribuée.

**Utiliser n’importe quel appareil photo d’application/de smartphone pour numériser les codes QR de Learning Manager**

Les élèves pourront désormais utiliser n&#39;importe quelle application de numérisation de codes QR ou l&#39;appareil photo de leur smartphone pour numériser les codes QR générés par Learning Manager afin d&#39;inscrire, d&#39;achever et plus encore les cours.

**Améliorations des rapports**

Un nouveau rapport Utilisation de l’instructeur, un rapport Revue des formations, un rapport Assistances à la tâche et d’autres améliorations apportées aux rapports.

**Prise en charge des sessions hybrides**

Adobe Learning Manager prend désormais en charge la création de sessions de formation « hybrides » avec instructeur (ILT). Les sessions ILT virtuelles peuvent être créées avec des informations de localisation facultatives afin que les élèves puissent assister à la session en personne également s’ils sont disponibles sur le site.

**Meilleur suivi des progrès pour la salle de classe et l’ILT virtuelle**

Les modules de salle de classe et d’ILT virtuel permettent désormais de signaler l’état du quiz d’un élève (réussite ou échec) ainsi que l’état de présence. Par conséquent, la présence et la réussite du quiz peuvent être prises en compte pour décider de la progression de l’élève.

**Adobe de l’application Learning Manager pour les Microsofts Teams**

La nouvelle application Adobe Learning Manager sur les Microsofts Teams est conçue pour favoriser l’apprentissage dans le flux de travail et stimuler l’apprentissage par les réseaux sociaux. Les élèves pourront accéder au contenu d’apprentissage dans la plateforme de Microsofts Teams sans avoir à basculer sur un navigateur. Veuillez contacter votre CSAM pour obtenir la version bêta de l’application Adobe Learning Manager sur MS Teams.

### Bogues corrigés dans cette mise à jour

**Cours**

* Un auteur personnalisé ne peut pas prévisualiser un module lorsque le cours est à l&#39;état « SOUS_CONSTRUCTION ». La réponse affiche l’erreur 404.
* Le titre du cours sur la page de cours/d’ajout d’une application d’auteur déborde lorsque le titre du cours dépasse une certaine limite de caractères.

**Auteur**

* Dans l&#39;application d&#39;auteur, le titre du cours (s&#39;il est long) dépasse les limites de la page lors de la création d&#39;un cours.
* Parfois, un cours est ajouté, même si aucun auteur n&#39;est sélectionné.

**Rapports de tableau de bord**

* Les info-bulles s’affichent correctement lorsque la langue de l’interface est l’anglais, mais renvoient une erreur de console lorsque la langue de l’interface est différente.
* Renommez « Obligatoire » en « Obligatoire » dans le tableau de bord des élèves.

**Application d’instructeur**

* Le format horaire dans l’application de l’instructeur n’est pas cohérent avec les autres applications.

**Social**

* Pour certains types de publications, après la publication, le forum des réseaux sociaux ne s’ouvre pas comme prévu.

**Administrateur**

* Un utilisateur avec un rôle personnalisé ne peut pas télécharger de ressources lors de la prévisualisation d&#39;un cours.

**Modèles de courrier électronique**

* Lorsqu&#39;un élève se désinscrit d&#39;un programme d&#39;apprentissage contenant un cours de salle de classe/classe virtuelle, il ne reçoit aucun e-mail d&#39;annulation.

**Assistances à la tâche**

* Vous ne pouvez pas voir le nom du cours sur le widget d&#39;assistance à la tâche.

**Publication**

* La description du module ajoutée dans Adobe Captivate n’est pas visible dans Learning Manager lorsque le module est publié dans ALM.

**Champs actifs**

* Lorsqu’un fichier CSV contenant un grand nombre d’enregistrements est en cours de traitement, cela prend un temps considérable, au cours duquel, si un utilisateur se connecte et saisit une valeur pour l’un des attributs, il peut créer un nouveau groupe d’utilisateurs qui peut entraîner des erreurs CSV. Pour résoudre ce problème, lorsque l’importation CSV est en cours, le message contextuel de l’attribut Champs actifs est désactivé et réactivé une fois le chargement CSV terminé.
* Si la colonne du fichier csv Utilisateurs porte le même nom que le champ Utilisateurs externes actifs, le chargement du fichier csv échoue.

**Correctifs liés à l’API**

* Dans la réponse learningObjects, l’attribut de signet est manquant.
* Une entrée d’accès est créée lors de la génération de jetons d’actualisation Oauth pour les utilisateurs supprimés.
* L’API LO renvoie un loFormat incorrect, car les modules préparatoires ont été pris en compte pour calculer le type de cours ainsi que le contenu de base.

**Problèmes connus dans cette mise à jour**

* Le bouton Partager du catalogue des élèves ne fonctionne pas comme prévu dans le navigateur Safari, l’application Mobile et iPad MS Teams.
* Les notifications ne s’affichent pas dans l’onglet Activité une fois que l’application est supprimée sur d’autres ordinateurs.
Rien ne se passe lorsque vous cliquez sur les notifications dans l’onglet Activité de l’application sur iPhone 14.
* Dans l’application MS Teams, les notifications de Learning Manager (terminé, inscrit, échéance et en retard) n’affichent pas l’état et le nom du cours dans l’onglet Activité.
* Une fenêtre contextuelle contenant du contenu XML s’affiche lorsque l’administrateur d’intégration n’approuve pas l’application MS Teams.
* La langue de l’interface utilisateur de l’application Learning Manager d’Adobe sur MS Teams ne change pas toujours comme prévu lorsque la langue est modifiée.
* Vous ne pouvez pas interagir avec la première notification lorsque le focus se trouve dans l’Iframe (onglets Accueil et Catalogue).

**Limitations de l’application mobile Adobe Learning Manager**

* Affichage de contenu hors ligne.
* Mode Grille/Liste sur la page Catalogue/Mon apprentissage.
* Tentatives multiples de suivre un cours.
* Date limite d&#39;inscription sur une carte de cours.
* Sur les appareils iOS, les notifications push n’apparaissent pas lorsque l’application est au premier plan.
* Les liens profonds dans les notifications Push ne redirigent pas vers la page de destination prévue.
* En cliquant sur le bouton Enregistrer les intérêts, vous redirigez vers le Web.
* Lorsque vous répondez ou commentez dans Apprentissage par les réseaux sociaux, vous ne pouvez pas joindre de fichier.
* Vous ne pourrez pas vous connecter à LinkedIn Learning.
+++

+++Mise à jour 88

**Date de publication :** 7 mars 2023

### Amélioration Des Performances Dans Cette Version

Lorsqu&#39;une inscription en bloc d&#39;élèves est effectuée, aucun fichier journal n&#39;est généré pour chaque élève.
Nous avons optimisé le traitement des plans d’apprentissage pour les grands comptes. Cela permet d’éviter tout problème ou retard de recherche.
+++

+++Mise à jour 87

**Date de publication :** 1er mars 2023

## Bogues Corrigés Dans Cette Mise À Jour

* Un élève ne reçoit pas l’e-mail d’annulation de session si le module CR/VC est supprimé du cours inscrit.
* Changez GetNotificationData de GET en POST. La mise en œuvre initiale a produit l&#39;erreur, **IllegalArgumentException : l&#39;en-tête de la demande est trop grand**, qui ont conduit à des notifications qui ont échoué.
+++

+++Mise à jour : 86

**Date de publication :** 17 février 2023

### Bogue Corrigé Dans Cette Version

Dans l&#39;application de l&#39;élève, la recherche d&#39;utilisateurs et de groupes d&#39;utilisateurs échoue en raison de certains problèmes avec les paramètres régionaux.
+++

+++Mise à jour 85

**Date de publication :** 13 février 2023

### Modifications apportées à cette mise à jour

Ajout de la prise en charge du code de langue à quatre lettres lors du filtrage des langues dans GET learningmanagerapi/v2/learningObjects.

### Bogues Corrigés Dans Cette Mise À Jour

Pour certaines langues, la recherche renvoie des résultats incorrects.
Les métadonnées du cours sont écrasées lorsque le cours comporte plusieurs variantes des mêmes paramètres régionaux.
+++

+++Mise à jour 84

**Date de publication :** 2 février 2023

### Modifications apportées à cette mise à jour

**Rapport d’assistance à la tâche**

Cette mise à jour comporte un nouveau rapport d&#39;assistances à la tâche qui répertorie toutes les assistances à la tâche du compte.

**Contrôle de version**

Nous avons ajouté le contrôle de version pour les ressources lors de l&#39;ajout des ressources lors de la création d&#39;un cours.

**Signaler les tentatives**

Vous pouvez afficher un rapport de toutes les nouvelles tentatives et visites d’un élève pour chaque formation.

**API de réinitialisation de module**

Un administrateur peut désormais réinitialiser un module à l’aide de l’API de réinitialisation de module. Pour plus d’informations, voir [Référence API Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

**Modèle d’e-mail**

Pour quelques modèles d’e-mail, vous pouvez désormais ajouter un prérequis au modèle.

**Autres modifications**

* Vous pouvez ajouter un cours approuvé par le responsable comme condition préalable.
* Amélioration des performances lors de l’actualisation du tableau de bord de résumé de l’apprentissage.
* Les ID de messagerie et les ID de compte sont vérifiés avant l’envoi d’un rapport de rebond.

### BOGUES CORRIGÉS DANS CETTE MISE À JOUR

* Les noms des auteurs en double s&#39;affichent sur la page de présentation du cours.
* Un hyperlien sur la page de création du compte a généré l’erreur 404.
* Les paramètres régionaux tchèques ne se sont pas reflétés comme prévu dans les paramètres du lecteur.
* Dans certains cas, les compétences sont affichées comme non définies pour les élèves en cours et non démarrés.
* Le temps passé sur plusieurs jours affiche un temps différent dans les rapports Relevé de notes de l&#39;élève et Inscription.
* Le bouton Précédent ne répond pas pour les profils d’administrateur et de responsable dans Cours > Score du quiz L2 > Par onglet Question et Présence et notation, respectivement.
* Pour certaines langues, dans un modèle d’e-mail, une partie du contenu du corps de l’e-mail est manquante et la traduction linguistique du modèle n’est pas cohérente.
+++

+++Mise à jour 83

**Date de publication :** 18 janvier 2023

### Modifications apportées à cette mise à jour

**Nouvelle colonne**

Une nouvelle colonne, **unenrollmentAllowed**, est ajouté à course.xlsx. Téléchargez le fichier à partir de ce manuel.

**Connecteur LinkedIn Learning**

Pour le connecteur d’apprentissage LinkedIn, une nouvelle case à cocher permet à l’élève de se désinscrire sur la page Filtres. Pour plus d’informations, voir [Connecteur linkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md).

### Bogues Corrigés Dans Cette Mise À Jour

* Lorsque vous survolez les graphiques à barres, l’info-bulle du rapport de tableau de bord s’affiche comme prévu.
* Dans Rapports sous Activité de l’utilisateur, le rapport Temps d’apprentissage passé affiche des données incorrectes pour les données quotidiennes/mensuelles.
* Dans certains cas, le graphique de score du quiz affiche des valeurs incorrectes.
* Dans un cours avec du contenu SCORM avec plusieurs tentatives définies, lorsqu’un élève tente le cours, le bouton Revisiter est désactivé.
* Dans certains cas, après avoir inscrit un élève à un cours et téléchargé un journal d’audit d’e-mail, l’e-mail est envoyé, mais il n’apparaît pas dans le journal.
* L’invitation calendaire d’un instructeur doit inclure le texte instructeur dans l’objet.
* L’icône de la carte de formation n’est pas reflétée sur les recommandations de cours associées et les cartes de parcours d’apprentissage présentes sur la page de présentation du cours.
* Dans les paramètres de la page d’accueil de l’élève, ajoutez une section Enregistré par moi.
* Pour certains comptes, un utilisateur est invité à se connecter à l’authentification unique pour un compte pour lequel l’ID d’Adobe est requis.
* Dans les fuseaux horaires avec Daylight Savings, le champ « start_time » est calculé en fonction de la différence de temps actuelle, et non en fonction de la différence de temps entre la date et l&#39;heure de début réelles. Cela a provoqué des invitations avec des heures incorrectes.
* Chaque fois qu’une certification est récurrente, une copie des cours sous-jacents est créée en interne dans la base de données. Ces cours apparaissent alors dans la recherche, contrairement au comportement attendu.
* Lorsque le chargement d’un fichier CSV échoue, vous ne recevez aucune notification par e-mail.
* Si les noms des champs actifs sont longs, les noms disparaissent lorsque vous les faites glisser et les déposez. Ensuite, le bouton Enregistrer ne fonctionne pas non plus comme prévu.
* Un rapport de session n&#39;est pas exporté via la page de présence et de notation d&#39;un cours si le premier utilisateur du rapport a un enregistrement dans le tableau de notes d&#39;activité avec le commentaire comme valeur Null.
* Lorsque vous utilisez le compte administrateur pour récupérer les badges, vous pouvez trier la liste comme prévu. Mais lorsque vous effectuez la même opération pour un élève, les résultats ne sont pas triés.
* Si vous choisissez un cours dans vos résultats de recherche et que vous essayez de revenir aux résultats de la recherche à l&#39;aide du bouton Précédent, les résultats de la recherche disparaissent.
* Tous les utilisateurs ne sont pas ajoutés à un groupe d’utilisateurs en tant qu’instructeurs dans une session.
* Les modèles qui contiennent plusieurs modèles utilisateur sont remplacés par leur objet avec certaines valeurs.
+++

+++Mise à jour 82

**Date de publication :** 15 décembre 2022

* L’API GET LO inclut désormais des informations tarifaires, le cas échéant.
* Une nouvelle colonne, Terminé par, est ajoutée aux rapports LT. Cela aide l’administrateur à identifier la source d’achèvement d’un objet d’apprentissage.
* Nous avons ajouté un nouveau module ILT qui peut enregistrer le statut Réussite/Échec de l’élève ainsi que son assiduité. Les instructeurs peuvent désormais marquer un élève comme ayant participé avec l’option Réussite ou ayant participé avec l’option Échec.
* Un administrateur peut désormais exiger des élèves qu’ils terminent et réussissent avant de passer au module/cours suivant. Cela s’applique aux conditions préalables, aux cours commandés et aux programmes d’apprentissage.

**Correctifs de bogues**

* Problèmes de langue bahasa dans l’expérience mobile immersive sur la barre latérale et le pied de page.
* Correctifs de vue immersive liés à la prévisualisation du module.
* Une recherche de cours dans l’administrateur et l’auteur renvoie des résultats dans des paramètres régionaux différents de ceux saisis.
* Les modifications apportées aux modèles d’e-mail de bienvenue n’étaient pas enregistrées après modification.
* Les utilisateurs ayant des ID de messagerie et des ID Adobe différents ne pouvaient pas se connecter à l’application mobile.
* Les utilisateurs n&#39;ont pas été correctement identifiés lors de la participation aux sessions Zoom / BJ VC.
+++

+++Mise à jour 81 - Version de novembre 2022 d’Adobe Learning Manager

**Date de publication :** 05 novembre 2022

**Remarque :** Avec cette version d’Adobe Learning Manager, les utilisateurs disposant de comptes inactifs ne peuvent plus accéder à leurs comptes à l’aide de sous-domaines. Les comptes sont accessibles à l’aide de l’ID de compte ou en utilisant la page acapindex.html et en saisissant l’ID de messagerie.

### Nouveautés de cette version

La version de novembre 2022 d’Adobe Learning Manager se compose des éléments suivants :

* Configuration SSO multiple
* Prise en charge des fonctionnalités hors connexion
* Améliorations apportées à la page Présentation de la formation
* Personnalisation du lecteur
* Emprunt d’identité de l’élève et du responsable

Pour plus d’informations, voir [Nouveautés de la version de novembre 2022 d’Adobe Learning Manager](/help/migrated/whats-new-2022-november.md).

**Remarque :** Avec la version de novembre 2022 d’Adobe Learning Manager, Zoom sera abandonné [Authentification JWT avant juin 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). En conséquence, le connecteur Zoom avec JWT continuera de fonctionner jusqu’à la date mentionnée, mais nous recommandons aux utilisateurs de créer une application OAuth de serveur à serveur pour remplacer la fonctionnalité dans leur compte. Par défaut, l’authentification OAuth Zoom est appliquée à toute nouvelle connexion.

### Bogues corrigés dans cette mise à jour

* En tant qu’élève, lorsque vous tentez d’accéder à un programme d’apprentissage comportant plus de 10 cours sur mobile, un message d’erreur s’affiche.
* Si un cours a défini un rappel à envoyer n jours après l’expiration du délai, l’e-mail est envoyé au bout de n jours comme prévu, mais le nombre de jours de dépassement du délai est n-1 au lieu de n.
* Une vidéo ne se charge pas dans le lecteur si le retour d’informations L1 est activé pour le cours dans l’application de l’élève et que l’utilisateur n’a qu’un rôle d’élève.
* Un e-mail de rappel d’achèvement n’affiche pas l’heure dans le fuseau horaire de l’utilisateur comme prévu.
* Les relevés de notes des élèves qui sont générés via des rapports de tableau de bord ne respectent pas les filtres et affichent plus d&#39;informations que nécessaire.
* Vous ne pouvez pas sélectionner de contenu dans lequel la langue de l’interface n’est pas ajoutée comme langue du contenu.
* Lors de la seconde auto-inscription à un cours, l&#39;URL affichée était incorrecte.
* Lorsqu&#39;un instructeur est supprimé d&#39;une session VC, il ne reçoit aucun message l&#39;informant de l&#39;annulation de la session.
* Le texte « minute » sur une vignette de la page de formation de l’élève n’est pas traduit en bahasa indonésien comme prévu.
* Le tableau de bord Conformité affiche des données incorrectes pour les élèves non conformes.
* Lors de l’ajout d’un rapport, vous ne pouvez pas sélectionner de cours ou de catalogues dans lesquels la langue de l’interface n’a pas été ajoutée à la langue du contenu.
* Nous avons ajouté les langues de contenu suivantes dans cette version :
   * Bulgare
   * Flamand
   * Portugais (Brésil)

### Problèmes connus dans cette mise à jour

* Dans certains cas, le graphique de score du quiz ne s’affiche pas comme prévu. Lorsque vous redimensionnez le graphique, un espace vide apparaît au début. En outre, toutes les questions n’apparaissent pas et des données incorrectes s’affichent par intermittence.
+++

+++Mise à jour 80

**Date de publication :** 20 septembre 2022

* Les problèmes de connexion sur l’application mobile dans iOS ont désormais été résolus.
* Correction d’un problème lié aux rebonds d’e-mails.
* Les instructeurs étaient avertis de manière incorrecte avant même les envois des élèves.
* Un instructeur reçoit une notification par e-mail même si un élève n’a pas envoyé d’activité.
* Après la création d’une session VC sur MS Teams ou Adobe Connect, les instructeurs ne reçoivent pas les invitations à la session.
* Statut incorrect dans un parcours d’apprentissage.
* Amélioration des performances de l’application.
+++

+++Mise à jour 79

**Date de publication :** 18 août 2022

* La confirmation d’invitation au calendrier pour les sessions ILT/VILT fonctionne désormais avec le calendrier Google.
* Un responsable de magasin peut désormais voir les notifications pour les utilisateurs qui lui sont rattachés, même s’il est supprimé en tant que responsable de personnes.
* Dans certains cas, l’inscription au cours échoue et l’erreur 500 s’affiche.
* Dans certains cas, vous ne pouvez pas modifier une instance de cours virtuel pour Teams.
* Les administrateurs et les instructeurs peuvent ajouter des commentaires pour les utilisateurs qui n’ont pas participé aux sessions ILT/VILT.
* Amélioration des performances lors du téléchargement de rapports volumineux.
* Lorsque l’adresse e-mail d’un utilisateur est rejetée, l’administrateur reçoit une notification par e-mail. L’e-mail contient un lien qui, lorsque vous cliquez dessus, télécharge un fichier CSV avec la liste des utilisateurs dont l’e-mail a été rejeté. L’administrateur peut alors prendre les mesures nécessaires.
   * L’e-mail se déclenche lorsqu’un e-mail est rejeté ou abandonné.
   * L’e-mail se déclenche une fois par jour pour tous les administrateurs ajoutés à la liste.
   * Le lien expire dans sept jours.
* Un message d’erreur s’affiche lors de la tentative d’intégration d’un compte Adobe Connect déjà intégré à un autre compte Learning Manager.
+++

+++Mise à jour 78

**Date de publication :** 4 août 2022

### Bogues corrigés dans cette mise à jour

* Si vous avez un cours contenant un module avec un aperçu, puis utilisez une API pour récupérer les ressources du cours, la réponse ne contiendra aucune donnée de l&#39;emplacement, contentZipUrl et contentStructureInfoUrl.
* Réponse incorrecte après l’envoi d’une demande XAPI à partir du document Swagger, où le nom de domaine est learningmanager.
* Dans /boards/{id}Réponse de l’API /posts : la propriété « post.attributes.myPoll » s’affiche comme un objet vide.
* Dans certains cas, pour un utilisateur non connecté, le bouton Ajouter au panier est désactivé pour certains cours ou parcours d’apprentissage.
* URL de sous-domaine incorrecte sur la page de l’identité visuelle.
+++

+++Mise à jour 77

**Date de publication :** 24 mai 2022

**Problèmes résolus dans cette mise à jour :**

* Les nouveaux cours ne respectent pas la séquence dans l’application Salesforce. Si vous modifiez la séquence, le cours ne s&#39;affiche pas dans la séquence prévue.
* Une fois que vous avez modifié les paramètres dans la page d’accueil Classic et que vous les avez enregistrés, les modifications ne sont pas enregistrées comme prévu. Cela se produit par intermittence.
* Le code de HTML s’affiche lorsque les élèves consultent leurs notifications, ce qui a un impact négatif sur l’expérience.
* Sur le tableau de bord, le temps passé à apprendre s’affiche de manière incorrecte comme zéro heure.

## MISE À JOUR : Adobe Learning Manager sera renommé Adobe Learning Manager

Il s’agit d’une mise à jour concernant un changement à venir et qui vous aide à vous y préparer.

**Adobe Learning Manager en tant que produit sera renommé Adobe Learning Manager en juillet 2022**. Il s’agit d’un effort stratégique visant à refléter plus précisément l’alignement du produit sur certaines priorités commerciales.

L’équipe produit prend toutes les mesures nécessaires pour s’assurer qu’il n’y a aucun impact sur votre utilisation de la plateforme. Vous pouvez continuer à utiliser le produit comme d’habitude. Les administrateurs de la plate-forme peuvent remarquer le nouveau nom de la marque sur certains écrans en juillet.

Dans le cadre de cette modification, les URL d’accès à Learning Manager sont affectées.

Par exemple, si l’URL d’accès de votre compte est `https://learningmanager.adobe.com/XYZ`, alors la nouvelle URL sera `https://learningmanager.adobe.com/XYZ`.

Toutes les URL existantes continueront de fonctionner.

Pour terminer cette action, contactez le service informatique de votre organisation. Pour plus d’informations, contactez-nous à l’adresse `learningmanagersupport@adobe.com`.
+++

+++Mise à jour 76

**Date de publication :** 20 avril 2022

* Correctifs apportés aux terminologies du produit dans quelques rapports de tableau de bord.
* Une double barre oblique (« // ») dans l’URL d’un point d’entrée a entraîné des erreurs de validation.
* Après l’actualisation d’une page, le pourcentage d’achèvement et les derniers champs visités affichaient des informations incorrectes.
* Nous avons modifié la façon dont la valeur Certificat ou Plan d’apprentissage est calculée.
* Un administrateur personnalisé a pu ajouter tous les utilisateurs en tant qu’instructeurs même s’il était autorisé à ajouter un seul utilisateur.
* Sur un PDF de badge, une date d’achèvement incorrecte s’affichait.
+++

+++Mise à jour 75

**Date de publication :** 29 mars 2022

* Dans certains comptes, après la copie du fichier csv brut à l’emplacement FTP, l’importation des utilisateurs ne se déroule pas comme prévu et plusieurs notifications d’erreurs s’affichent.
* Dans les versions précédentes de Learning Manager, pour configurer un connecteur Zoom, vous deviez d’abord configurer FTP Exavault pour copier le fichier csv. Dans cette version, le connecteur FTP n’est plus utilisé pour le fichier csv. Par conséquent, vous n’avez pas besoin de configurer d’abord le FTP.
+++

+++Mise à jour 74 : instance AWS India de Learning Manager

**Date de publication :** 15 février 2022

### Présentation

Une [instance](https://learningmanagerapac.adobe.com/acapindex.html) de Learning Manager sera désormais hébergé sur AWS à Mumbai (ap-south-1). Pour les clients utilisant cette instance en Inde, les informations d’identification personnelle (PII) et les dossiers d’apprentissage de l’utilisateur sont stockés uniquement en Inde.

### Éléments pris en charge

L’instance d’Adobe Learning Manager en Inde est au même niveau en termes de fonctionnalités que les autres instances, telles que les régions UE et États-Unis. Certaines fonctionnalités ne sont pas prises en charge en Inde. Il s’agit des éléments suivants :

* Paiement par carte de crédit pour l’achat de places
* catalogue de contenu du Creative Cloud
* Application Slack
* **&#42;** En attente de certification pour la conformité SOC2

### Foire aux questions

**En quoi cette instance de Mumbai est-elle différente des autres environnements AWS uniquement ?**

Il n&#39;y a pas de différence. L&#39;instance de Mumbai est la même que [AWS (ÉTATS-UNIS)](http://learningmanager.adobe.com/) ou [AWS EU](http://learningmanagereu.adobe.com/) instances. Cette instance est hébergée en Inde. Tous les dossiers d’apprentissage et les données utilisateur restent en Inde. Les fonctionnalités suivantes ne sont pas prises en charge dans l’instance en Inde :

* Paiement par carte de crédit pour l’achat de places
* catalogue de contenu du Creative Cloud
* Application Slack
* **&#42;** En attente de certification pour la conformité SOC2

**Cet environnement sera-t-il conforme au framework CCF (Common Controls Framework) ?**

Oui. La nouvelle instance est conforme au framework CCF (Common Control Framework).
+++

+++Mise à jour 73

Date de publication : 5 février 2022

* La prise en charge des modèles d’e-mail est désormais disponible pour les langues de contenu, notamment le hongrois et le finnois.
+++

+++Mise à jour 72 - Version de janvier 2022 de Learning Manager

Date de publication : 15 janvier 2022

### Nouveautés et modifications

* Ajouter des emplacements de salle de classe
* Modifications de ludification
* connecteur de Microsofts Teams
* Modifications d’API
* Modifications web immersives mobiles

<!--
For more information, see What's new in the [**January 2022 release of Adobe Learning Manager**](../whats-new.md).
-->

### Corrections de bugs dans cette version

**Bibliothèque de contenu**

* La recherche de fichiers de contenu dans des dossiers de contenu privés ne fonctionnait pas pour les utilisateurs disposant de privilèges de rôle personnalisés. Ce problème est maintenant résolu.

**Cours**

* La suppression d’un cours ou d’un parcours d’apprentissage n’était pas possible s’ils avaient une association historique avec un plan d’apprentissage. Ce problème est maintenant résolu. Les utilisateurs peuvent désormais supprimer un cours ou un parcours d’apprentissage s’ils ne sont pas actuellement associés à un plan d’apprentissage.
* Lors de la prévisualisation d’un cours ou d’un parcours d’apprentissage, si le fichier de ressources a un nom long sans espaces, le nom du fichier ne se poursuit pas comme prévu et déborde sur la ligne suivante. Ce problème a été résolu.
* Dans le cas d&#39;une salle de classe virtuelle, vous pouviez auparavant créer un module sans sélectionner de système de conférence VC dans une nouvelle instance. L&#39;URL VC ne disposait pas des informations requises. Cela est désormais évité par un message d&#39;erreur lors de la création du module vous demandant de spécifier le système de conférence VC avant de pouvoir enregistrer le module.
* La page de liste d’attente affichait un message de bannière trompeur sur les utilisateurs enregistrés, qui est maintenant supprimé.
* Dans le cas d’une désinscription en bloc pour les cours, la fenêtre contextuelle permettant de saisir des ID de messagerie ne s’affichait pas, ce qui est maintenant corrigé.
* L&#39;option permettant d&#39;envoyer un courrier électronique aux élèves à partir de l&#39;onglet Présence et notation dans l&#39;application de l&#39;administrateur et de l&#39;instructeur n&#39;excluait pas les élèves non cochés après avoir effectué l&#39;opération Tout sélectionner. Par conséquent, Learning Manager envoyait un e-mail à tous les élèves. Ce problème a été résolu.
* Le rapport d’inscription indique « Pas commencé », même si un élève a déjà terminé le cours.

**SSO**

* Dans la configuration SSO, si l’ID d’entité comportait des espaces d’interlignage ou de formation, la configuration de connexion ne fonctionnait pas. Elle est désormais gérée dans le cadre du correctif.

**Annonce**

* En tant qu’administrateur, les dates de début et de fin d’une annonce n’étaient pas enregistrées si le langage d’interface et de contenu était défini sur Deutsch/Espanol. Ce problème a été résolu.

**Modèle d’e-mail**

* Les invitations de session s’étendant sur plusieurs jours lorsque les invitations ne reflétaient pas les informations correctes sur les jours sont bloquées dans certains clients de messagerie. Ce problème est maintenant résolu.
* La variable « Nom du lieu » était manquante dans le modèle de courrier électronique « Rappel de la session à venir » pour les élèves dans la langue allemande. Ceci est maintenant ajouté.
* Le lien permettant de créer un compte dans l’e-mail de bienvenue à l’utilisateur ne tenait pas compte des paramètres régionaux de l’utilisateur, qui sont désormais corrigés.

**E-mails de rappel**

* Si les élèves étaient inscrits à la formation via un plan d’apprentissage, les courriers électroniques de rappel d’achèvement étaient envoyés plusieurs fois en fonction du nombre de modifications apportées aux dates d’achèvement du même plan d’apprentissage. Ce problème a été résolu.

**Utilisateur**

* Le message affiché à l’utilisateur lorsque son compte est inactif/suspendu a été amélioré, il indique qu’il doit contacter son administrateur pour que ses comptes soient réactivés.

**Activité**

* Un instructeur ne pouvait pas afficher les envois de l’élève si le nom du fichier envoyé contenait un caractère spécial. Ce problème est maintenant résolu.

**Signaler**

* Un administrateur n’a pas pu télécharger le rapport d’inscription à un cours s’il contient un élève indirectement inscrit à ce cours via un parcours d’apprentissage flexible, mais qui doit encore choisir une instance pour ce cours dans le parcours d’apprentissage. Ce problème a été résolu.
* La réorganisation des rapports dans le tableau de bord des rapports pour les rôles d’administrateur et de responsable ne conservait pas l’état de l’ordre des rapports. Ce problème a été résolu.

**Contenu**

* Le contenu audio de la formation n’était pas lu automatiquement dans l’aperçu en mode élève en raison des stratégies de lecture automatique du navigateur. Ce problème est maintenant résolu pour les navigateurs pris en charge, à l’exception de Safari.

**Ludification**

* Si un élève externe a été converti en élève interne dans le même compte, il n’a pas pu accéder au tableau des scores de ludification dans l’application de l’élève. Ce problème a été résolu.

**Lecteur**

* Le lecteur n&#39;affichait pas de message d&#39;avertissement lorsque l&#39;utilisateur tentait de sauter des modules dans un cours ordonné ayant le type AICC de modules. Ce problème est maintenant résolu.
* Pour certains cours acquis ayant des modules vidéo dans un LMS sans en-tête, la lecture de la casse ne fonctionnait pas pour certains utilisateurs. Ce problème a été résolu.

**Tableau de bord du responsable**

* Un responsable n’a pas pu exporter le rapport pour son équipe directe à partir de la page des compétences d’équipe du tableau de bord des responsables. Ce problème a été résolu.

**Publier**

* En Europe, le contenu Learning Manager directement publié sur Adobe Learning Manager à partir d’Adobe Captivate était publié en langue allemande par défaut. Ce problème est maintenant résolu.

**API**

* Le champ de durée est maintenant ajouté au modèle d’assistance à la tâche.
* Pour les API de recommandation, une demande de GET renvoie parfois l’erreur 500.
* Lorsque vous migrez des formations via Exavault et que le texte contient des caractères non anglais, il était mis à jour avec des caractères parasites dans le texte. Ce problème a été résolu.

**Localisation**

* `NormalTextRun  BCX0 SCXW38820519 For the`Applications d’administrateur, d’auteur et d’élève, certains contenus en allemand ne s’affichent pas comme prévu.

## Problèmes connus dans cette version

* Sur la page Apprentissage par les réseaux sociaux, lors de la création d’une publication, vous ne pouvez pas enregistrer un fichier audio ou charger l’audio après avoir appuyé sur le bouton du micro. Il s’agit d’une limitation du navigateur.
* Dans iOS, les fichiers audio H264 et WMA ne sont pas pris en charge dans le navigateur mobile.
* La progression des élèves qui ont un + dans leur adresse e-mail n’est pas marquée. C&#39;est après qu&#39;ils aient suivi un cours de CV en Microsofts Teams.
* Dans le navigateur Safari Mobile, les élèves ne pourront pas charger plus de 200 Mo de fichier dans Apprentissage par les réseaux sociaux. Il s’agit d’une limitation du navigateur.
+++

+++Mise à jour 71

Date de publication : 17 novembre 2021

### Partager la formation avec les responsables

Learning Manager propose un tableau de bord de conformité à tous les administrateurs et responsables. Les responsables trouvent très utile de suivre la conformité des membres de leur équipe pour une formation particulière. Parallèlement, les administrateurs souhaitent que tous les responsables ajoutent des formations sur la conformité à leur tableau de bord et en assurent le suivi.

Dans Learning Manager, le **Partager avec les responsables** permet aux administrateurs de partager la formation avec les responsables, afin qu&#39;ils puissent être ajoutés au tableau de bord de conformité d&#39;un responsable. Ainsi, les responsables n’ont rien à faire et peuvent commencer immédiatement à suivre la conformité.

Pour plus d’informations, voir  [**Partager la formation avec les responsables**](../administrators/feature-summary/reports.md#share_training_managers).

### Bogues corrigés dans cette mise à jour

* S’il existe deux comptes et que la fonctionnalité de parcours d’apprentissage amélioré est désactivée, et qu’il existe un catalogue partagé du premier compte vers l’autre, le parcours d’apprentissage du deuxième compte comporte des sections en double dans la page du cours.
* Un FTP personnalisé prend désormais en charge sftp:// en plus de http:// et https://
* Le connecteur Exavault utilise désormais des API V2.
* Dans certains cas, la qualité des vidéos n’était pas optimale. Le problème est maintenant résolu.
* Même lorsqu’un élève a terminé un cours obligatoire et a été approuvé par le responsable, la certification reste à l’état Approbation en attente.
* Si les noms des auteurs contiennent des caractères accentués, la migration du cours échoue.
* Si le champ actif comporte des valeurs en majuscules, il n’est pas enregistré comme prévu.
* Impossible de filtrer les parcours d’apprentissage en fonction des compétences.
* Lorsqu’un administrateur crée une instance et ajoute une nouvelle session, un instructeur ne reçoit pas l’e-mail d’invitation à la session. Ce problème se produit dans les cours Zoom VC.
+++

+++Mise à jour 70

Date de publication : 28 octobre 2021

### Bogues corrigés dans cette mise à jour

* Dans certains cas, les informations sur un parcours d’apprentissage ne sont pas reflétées dans le relevé de notes de l’élève.
* Le texte à l’intérieur du **Marquer comme terminé** est mis à jour pour indiquer que l’opération est irréversible.
* Dans certains cas, l’API des objets d’apprentissage a renvoyé une erreur de métadonnées.
+++

+++Mise à jour 69 - Version d’octobre 2021 de Learning Manager

**Date de publication :** 09 octobre 2021

### Parcours d’apprentissage

Le **Version d’octobre 2021 d’Adobe Learning Manager** introduit le concept de parcours d’apprentissage.

>[!NOTE]
>
>Le **Paramètres > Général** propose une nouvelle option pour activer les fonctionnalités étendues des parcours d’apprentissage. Si cette option est activée, vous pouvez ajouter des parcours d’apprentissage dans un autre parcours d’apprentissage. Vous ne pouvez pas modifier l’option une fois qu’elle est activée.

Les parcours d’apprentissage remplacent notre fonctionnalité existante des programmes d’apprentissage. Imaginez que les programmes d’apprentissage bénéficient d’améliorations puissantes sans abandonner les fonctionnalités existantes. En outre, la fonctionnalité est marquée comme parcours d’apprentissage.

Pour plus d’informations, voir [***Parcours d’apprentissage***](../administrators/feature-summary/learning-paths.md).

### Autres modifications

* Nouvelle application Salesforce
* Hub de contenu
* Signalement des modifications
* Rapport récapitulatif de la session
* Modifications de la table des matières du lecteur
* Modifications d’API
* Modifications liées au connecteur

Pour plus d’informations, voir [***Nouveautés de la version d’octobre 2021 de Learning Manager***](../whats-new.md).

### Bogues corrigés dans cette mise à jour

* Les modèles de courrier électronique, tels que Annulation de cours, Annulation du programme d’apprentissage ou Annulation de la certification, ne reflètent pas les dernières terminologies de produit telles que définies dans le fichier csv. Désormais, le texte par défaut dans les modèles d’e-mail prend en charge les terminologies personnalisées.
* La langue utilisateur dans Learning Manager n’est pas prise en charge dans le flux de travaux Publier vers Learning Manager. Si la langue de l’utilisateur est différente, Publier sur Learning Manager se passe en anglais.
* Si vous ajoutez de nombreux catalogues à un rôle personnalisé, une erreur se produit lorsque vous mettez à jour le rôle. Désormais, la limite du nombre de catalogues est augmentée à 50 catalogues.
* Dans certains cas, les formations supprimées sont toujours visibles dans un catalogue. Ce problème s’est produit dans l’application d’administration uniquement et est maintenant résolu.
* Lorsque le rôle de responsable était modifié d’un utilisateur à un autre, le rôle de responsable de l’utilisateur précédent était toujours reflété dans l’interface utilisateur. Ce problème est maintenant résolu. Ce problème était présent uniquement pour les utilisateurs externes et non pour les utilisateurs internes.
* Dans certains scénarios spécifiques pour un grand nombre d’utilisateurs importés via le fichier CSV utilisateur, l’importation a échoué. Ce problème a été résolu.
* Un relevé de notes n’affiche pas la date d’achèvement d’un certificat externe si un cours obligatoire est ajouté après la création d’un certificat externe et qu’un utilisateur y est inscrit. Ce problème est maintenant résolu.
* Un certificat n’affiche pas le nom localisé de l’élève comme prévu. Ce problème est maintenant résolu.
* Dans le cas de sessions Zoom VC, un instructeur ne reçoit pas toujours l’invitation pour la session. Ce problème est maintenant résolu. L’instructeur reçoit désormais la communication requise.
* Un élève ne reçoit pas d’invitations pour une session si les modèles de niveau de cours sont activés mais que les modèles de niveau de compte sont désactivés. Ce problème est maintenant résolu.
* Pour des fuseaux horaires spécifiques, des rappels par e-mail ont été envoyés un jour plus tard que prévu. Ce problème est maintenant résolu.
* Les élèves ne reçoivent pas d’e-mails de notification de session si certains modèles de courrier électronique sont désactivés.
* Au cas où une réunion BlueJeans serait mise à jour par les auteurs, les administrateurs, l&#39;URL de la réunion BJ devenait inutilisable. Ce problème est maintenant résolu.
* Dans certains cas, lors de l’exécution de l’API GET/LO, les cours qui font partie d’un programme d’apprentissage ne sont pas renvoyés.
* Si l’élève tente de télécharger du contenu dont le nom comporte un espace vide, il rencontre une erreur de serveur interne.
* Les PDF de badge générés pour les élèves rencontraient des problèmes de formatage lorsqu’ils étaient générés dans des langues autres que l’anglais. Ces problèmes sont maintenant résolus.
+++

+++Mise à jour 68

Date de publication : 28 septembre 2021

### Bogues corrigés dans cette mise à jour

* Sur le navigateur mobile, les liens profonds ont été activés pour les éléments suivants :

   * Tous les forums
   * Forum et publication publics
   * Forum et publication privés avec accès
   * Forum et publication privés sans accès
   * Forum et publication restreints
   * Commentaire sur la publication
   * Répondre au commentaire
   * Profil d’utilisateur pour les réseaux sociaux

* Pour les comptes utilisant un domaine personnalisé, l’application de l’élève n’affiche pas l’icône des favoris.
* Sur AEM, le composant Learning Manager supprime la configuration des autres composants.
* La page d’aide du composant AEM redirige vers un emplacement incorrect.
* Obtention et stockage en externe des e-mails/jetons utilisateur afin que les utilisateurs puissent mettre en œuvre leur propre back-end de stockage au lieu d’utiliser des nœuds utilisateur AEM.
* Lors de la modification de la description en texte brut dans les cours, programmes d&#39;apprentissage, certificats et assistances à la tâche, un message d&#39;avertissement s&#39;affiche.
* Les rapports du tableau de bord des responsables ne sont pas téléchargés lorsqu’un utilisateur a à la fois un rôle personnalisé et un rôle de responsable.
* Un résumé d’e-mail affiche une valeur incorrecte de l’activité de formation.
* Dans certains cas, Learning Manager se comporte de manière inattendue lorsque vous passez du Marché de contenus à la page Élève.
* Dans l’application pour réseaux sociaux, les filtres ne fonctionnent pas comme prévu dans la vue Liste.
* Le courrier électronique de bienvenue que les utilisateurs internes reçoivent est également reçu par les utilisateurs externes.
* Ajoutez le widget Learning Manager dans le modèle de page dans AEM.
* Si vous souhaitez republier un certificat après avoir supprimé un cours, vous ne pouvez pas le faire.
* Les élèves ne reçoivent pas d’e-mails contenant les détails d’une session.
+++

+++Mise à jour 67 - Mises à jour d’Azure

Cette mise à jour introduit une nouvelle instance d’Azure.

>[!NOTE]
>
>Les éléments suivants ne sont pas pris en charge dans l’instance :
>
>* [Domaine personnalisé](../custom-domain.md)
>* [Achat par carte de crédit](../administrators/feature-summary/billing-management.md)
>* [Catalogue de contenu](../administrators/feature-summary/content-catalogs.md)

+++

+++Mise à jour 66 - Version d’août 2021 de Learning Manager

Le **Août 2021** **version d’Adobe Learning Manager** se concentre sur l&#39;amélioration de l&#39;expérience des élèves, des rapports et des workflows administratifs. Voici quelques faits saillants :

* **Marché de contenus :** Learning Manager propose désormais plus de 70000 cours dans divers domaines, tels que la technologie, la gestion, le leadership, etc.
* **Prise en charge de l’accessibilité améliorée :** La prise en charge de l’accessibilité pour le rôle d’élève est renforcée par une navigation au clavier améliorée, la fonctionnalité de lecteur d’écran et la conformité au taux de contraste.
* **Formatage de texte enrichi :** Learning Manager propose désormais l’édition de texte enrichi pour les descriptions de cours, de programmes, de certificats et d’assistances à la tâche. Cela permet aux auteurs de spécifier des descriptions en texte enrichi, y compris des hyperliens, des images et d’autres options de formatage de texte, au lieu d’utiliser du texte brut.
* **Évaluation par étoiles :** Un élève peut désormais évaluer un cours sur une échelle de 5 points. Un administrateur peut choisir entre l’évaluation de l’efficacité existante ou l’évaluation à 5 étoiles.
* **Intégration de Badgr :** Les élèves peuvent désormais autoriser Learning Manager à envoyer automatiquement les badges qu’ils ont acquis dans Learning Manager vers leur compte Badgr, d’où ils peuvent les partager sur leurs réseaux sociaux.
* **Exportation d’événements d’apprentissage vers Salesforce :** Learning Manager permet désormais d’exporter certains événements spécifiques dans Learning Manager, tels que l’ajout d’un nouvel utilisateur, l’inscription et l’achèvement vers un client Salesforce, et permet de les lier à l’objet Utilisateur ou Contact approprié dans Salesforce.

Pour plus d’informations, voir [***Nouveautés et modifications de la version d’août 2021 de Learning Manager***](../whats-new.md).


**Date de publication :** 7 août 2021

### Bogues corrigés dans cette mise à jour

**Expérience de l’élève**

* Une fois qu’un élève est ajouté à deux groupes d’utilisateurs et qu’un plan d’apprentissage est ajouté, il est inscrit à une instance différente du même cours.
* Dans certains cas, après l’inscription et le début du cours, la lecture du cours ne se déroule pas comme prévu.
* La description du cours affiche les balises de HTML, ce qui est maintenant corrigé.
* Si vous commentez une publication sur un forum de réseaux sociaux qui s’étend sur plusieurs lignes, le commentaire apparaît sur une seule ligne. Ce problème est maintenant résolu.

**Création**

* Dans certains cas d’inscriptions automatiques, les élèves reçoivent plusieurs e-mails d’inscription.

**Rapports**

* Lorsque l’interface est définie sur quelques langues autres que l’anglais, les relevés de notes des élèves ne sont pas générés comme prévu.
* Possibilité de réinitialiser la progression d’un cours dans un programme d’apprentissage et une certification.
* Si un fichier CSV contient des champs actifs portant le même nom, mais avec une sensibilité à la casse différente, le fichier CSV génère une exception.

**Autres**

* L’option permettant de modifier les notes et les commentaires doit être désactivée lorsqu’aucun élève n’est sélectionné ou si la présence de l’élève sélectionné n’est pas marquée.
* Les valeurs des champs actifs s’affichent en minuscules dans la boîte de dialogue Modifier l’utilisateur, même si un utilisateur avait précédemment ajouté les valeurs en majuscules.
* Possibilité pour les administrateurs et la direction d’afficher les approbations en attente pour les cours. Cela permet à la direction de s’assurer que les responsables suivent l’apprentissage et la formation des employés, et permet également aux administrateurs de Learning Manager d’approuver l’inscription aux cours selon les besoins.
* Un utilisateur disposant d&#39;une autorisation d&#39;auteur ou d&#39;administrateur/auteur personnalisé ne peut pas modifier une assistance à la tâche créée par un autre utilisateur.
* Dans le rôle d’administrateur, lorsque l’utilisateur accède à Cours > Instance et sélectionne « Élèves inscrits » pour n’importe quelle instance, auparavant, cela affichait les élèves de l’instance par défaut. L’administrateur devait modifier manuellement l’instance dans la liste déroulante. Désormais, Learning Manager dirige correctement l’utilisateur vers la page des élèves avec l’instance correcte sélectionnée.

**Application pour appareil**

* Sur les appareils Android et iPhone, un élève ne peut pas lancer les modules de cours au hasard. Cela génère l’erreur 401 Non autorisé.
* Un élève peut analyser deux codes QR, mais lors de l&#39;analyse du troisième code QR, un message d&#39;erreur s&#39;affiche.
* Sur certains appareils Android et iOS, un fichier ne s’ouvre pas comme prévu pour certains cours téléchargés.
* La tentative d’ouverture d’une assistance à la tâche affiche un message d’erreur.
* L’application pour appareil se comporte de manière inattendue lorsqu’un programme d’apprentissage est utilisé hors ligne.
* Lorsqu’un élève revient en ligne et ouvre l’application, celle-ci reste bloquée sur l’écran de démarrage.
* Parfois, lorsqu’un utilisateur est de nouveau en ligne, l’application passe à la vue classique.
* Parfois, lorsqu&#39;un cours est consommé hors ligne, la progression n&#39;est pas enregistrée.
* Parfois, un nom de cours ne s&#39;affiche pas comme prévu dès le début lorsque le nom est long.
* Sur la page du catalogue, les cours ne sont pas triés comme prévu.
+++

+++Mise à jour 65

Date de publication : juillet 2021

### Bogues corrigés dans cette mise à jour

* Problèmes liés aux connexions pour les utilisateurs.
* Le modèle d’e-mail d’inscription à un cours pour Manager n’affiche pas la date limite d’achèvement du cours si la variable est ajoutée au modèle.
* TLS 1.0 et TLS 1.1 ont été abandonnés.
* Problèmes liés à la suppression de données RGPD pour un utilisateur.
+++

+++Mise à jour 64

Date de publication : juillet 2021

### Bogues corrigés dans cette mise à jour

* Une notification d&#39;inscription est envoyée aux élèves déjà inscrits à un cours.
* Lorsqu’un certificat personnalisé en tant que badge est généré, le format de la date n’est pas pris en charge en allemand.
+++

+++Mise à jour 63

Date de publication : juin 2021

### Bogues corrigés dans cette mise à jour

* Vous pouvez créer un utilisateur avec un nom vide dans un fichier CSV.
* Si le champ actif contient un caractère &#39;/&#39;, après la création d’une tâche pour télécharger user.csv, la tâche ne passe pas de l’état « Envoyé » à « Terminé ».
* Les modules ordonnés ne respectent pas la séquence.
* Lorsqu&#39;un auteur externe est supprimé, le cours que cet auteur a créé n&#39;est plus disponible.
* La recherche d’un objet d’apprentissage avec plusieurs compétences produit des résultats inattendus.
+++

+++Mise à jour 62

Date de publication : juin 2021

### Bogues corrigés dans cette mise à jour

* Impossible de se connecter à l’application lorsque la connexion SP du compte est initiée.
* Le rendu des vidéos à partir de Brightcove n&#39;est pas celui attendu.
* L’API userGroupInfo n’est pas visible lors de la consultation du programme d’apprentissage dans les applications.
* Impossible de rechercher un programme d&#39;apprentissage et une certification obsolètes lors de la création d&#39;un rapport de tableau de bord.
* Un auteur ne peut pas modifier ou mettre à jour une assistance à la tâche créée par un autre auteur.
* L’API d’envoi de fichiers ne fonctionne pas comme prévu dans le cluster EU.
+++

+++Mise à jour 61

Date de publication : mai 2021

### Bogues corrigés dans cette mise à jour

* Amélioration des performances des appels userGroupInfo.
* Après avoir activé les nouveaux profils Brightcove, Learning Manager prend en charge les contenus avec des modules vidéo et audio.
* Les relevés de notes ne parviennent pas à capturer les données si une plage de dates étroite est sélectionnée.
* Une invitation à une session est envoyée aux élèves inscrits pour toutes les sessions, même lorsqu’une seule nouvelle session est ajoutée.
* Les modules audio ne sont pas chargés comme prévu.
+++

+++Mise à jour 60

Date de publication : avril 2021

### Bogues corrigés dans cette mise à jour

**Signaler**

* Après avoir créé un rapport, si vous recherchez un cours retiré, vous ne pouvez pas le faire.
* Les erreurs d’un rapport se propagent aux autres. En conséquence, ces rapports ont donné lieu à des erreurs.

**Assistances à la tâche**

* Après avoir téléchargé une assistance à la tâche, vous ne pouvez pas la supprimer.

**Lecteur**

* Les légendes WebVTT ne s’affichent pas comme prévu.

**Application de l’élève**

* Sur la page Présentation de la certification, la certification externe n&#39;affiche pas la durée ajoutée par un auteur.
* Ajout de l’option **Tous** dans le filtre Compétence.
* Les élèves recevaient plusieurs e-mails de résumé.
* Le nombre de lignes sélectionnées n’est pas reflété comme prévu sur une page.

**composant AEM**

* Les widgets ne sont pas mis à jour comme prévu après une actualisation de page.

**Localisation**

* Quelques chaînes allemandes ne sont pas localisées comme prévu.
* La traduction des chaînes est définie par défaut sur l’anglais si un élève n’a pas sélectionné la langue de l’interface et du contenu.

**Certification**

* L&#39;ordre du module peut être ignoré si les conditions préalables ne sont pas appliquées.

**Navigateur**

* Les applications d&#39;auteur, de responsable ou d&#39;élève ne s&#39;affichent pas comme prévu dans IE 11.

**Ludification**

* Les points de ludification ne sont pas récupérés comme prévu.

**Bibliothèque de contenu**

* Les cours d’application d’évaluation de contenu ne fonctionnent pas comme prévu.

**Lecteur**

* Le lecteur se charge uniquement dans l’espace dans lequel le widget est présent.
* Les vidéos dans un module Captivate ne sont pas lues comme prévu.

**Connecteur**

* Dans certains cas, les fichiers sont supprimés d’un connecteur FTP/Box.
* Les fichiers sont supprimés de ftp si les fichiers sont mis à jour avec les mêmes noms.
* Un événement BlueJeans prend en charge la pagination lorsque le nombre d’événements est supérieur à 100.

**Mise à jour de l’application mobile 3.3 - Mars 2021**

Date de publication : 26 mars 2021

### Nouveautés et modifications {#whatsnewandchanged}

La mise à jour 3.3 de l’application mobile Captivate Learning Manager introduit une toute nouvelle page d’accueil, qui prend en charge les en-têtes et les recommandations de formation basées sur l’IA. Cette page d’accueil est disponible pour tous les comptes configurés pour la nouvelle option de mise en page immersive. Les comptes configurés avec la mise en page classique continuent d’afficher la page d’accueil classique/héritée. Ils ne doivent pas constater de modifications dans la page d’accueil.

En outre, cette mise à jour permet également aux élèves de télécharger leur badge en tant que PDF et en tant qu’image. La mise à jour introduit également une fenêtre contextuelle de retour d’informations, qui permet aux élèves de fournir des commentaires anonymes sur l’application.

Pour plus d’informations, voir  [Application pour appareil Learning Manager](../learners/feature-summary/ipad-android-tablet-users.md).

Lisez ce qui suit pour en savoir plus.

#### Nouvelle page d’accueil

Pour tous les comptes pour lesquels l’option Mise en page immersive est activée, une toute nouvelle page d’accueil prend en charge la configuration de mise en page immersive.

#### Évaluation

Dans cette version, Learning Manager invite l’utilisateur à fournir un retour d’informations sur son expérience avec l’application mobile.

#### Télécharger le badge

Cette mise à jour permet aux élèves de télécharger leurs badges au format PDF et Image.

<!--## Previous update releases {#previousupdatereleases}-->
+++

+++Mise à jour 60 - Version de février 2021 de Learning Manager

Date de publication : 20 février 2021

### Nouveautés et modifications {#Whatsnewandchanged-1}

* Mode Tableau dans les réseaux sociaux.
* Personnalisation de la bannière pour réseaux sociaux.
* Filtres de catalogue dans l’application de l’élève.
* Désinscription de la formation.
* Importez des utilisateurs à partir de contacts Salesforce.
* ... et bien d&#39;autres.

Pour plus d’informations, voir Nouveautés de la section [Mise à jour de Learning Manager de février 2021](../whats-new.md).

### Bogues corrigés dans cette mise à jour {#bug-fixes}

**Certification**

* Dans certains cas, un élève n’a pas pu reprendre un cours faisant partie d’une certification, même si le nombre maximal de tentatives pour ce cours est défini sur infini. Ce problème a été résolu.
* Dans certains cas, un élève ne peut pas s’inscrire à une certification en raison de **S’inscrire** le bouton n&#39;est pas visible comme prévu.

**Bibliothèque de contenu**

* URL d&#39;aide incorrecte sur le **Ajouter un nouveau contenu** page. L’URL correcte a été mise à jour.

**Cours**

* Un rapport de score de quiz L2 téléchargé pour un module de contenu AICC affiche un score incorrect sous la colonne Score total de l’utilisateur / Score du quiz. Ce problème a été résolu.
* Le téléchargement des ressources d&#39;un cours ne fonctionnait pas s&#39;il était dupliqué à partir d&#39;un autre cours et que l&#39;élève n&#39;avait pas accès au cours original utilisé pour créer un double.
* Les images de bannière ne sont pas supprimées lorsque l’auteur les supprime d’un cours à l’état de brouillon. Ce problème a été résolu.

**AEM**

* Après l’insertion du composant Learning Manager dans AEM, le chargement de la page prenait beaucoup de temps, empêchant ainsi l’accès aux autres composants. Ce problème a été résolu.

**Administrateur**

* Les cours retirés n&#39;apparaissent pas dans les résultats de recherche comme prévu. Ce problème a été résolu.
* L’administrateur n’a pas pu rechercher les cours retirés dans **Application d’administration** -> **Rapports personnalisés** -> **Rapports Excel** -> **Rapports de cours**, qui est maintenant corrigé.

* Le téléchargement d&#39;un rapport de quiz au format Excel ne fonctionne pas si le fichier contient des élèves qui ont suivi les formations avant et après la mise à jour du contenu. Ce problème a été résolu.
* Le chargement d’un fichier CSV échoue si les champs actifs contiennent des caractères spéciaux. Ce problème a été résolu.
* Dans certains cas, lorsqu’un élève répond à un quiz créé en Captivate, les réponses ne sont pas capturées comme prévu.
* Après avoir créé un abonnement et tenté de le modifier, le **Enregistrer** et **Annuler** les boutons ne s’affichent pas comme prévu. Ce problème a été résolu.

**Lecteur**

* Pour un type de contenu spécifique de SCORM-2004, le scénario de reprise ne fonctionnait pas. Par conséquent, les élèves devaient naviguer jusqu’au point où ils s’étaient arrêtés. Ce problème est maintenant résolu. Le contenu devrait maintenant reprendre à partir du point où vous l’aviez laissé.
* Après l&#39;inscription à un cours, dans certains cas, le contenu n&#39;est pas lu comme prévu. Ce problème a été résolu.

**Désinscription**

* Un rapport d&#39;inscription répertorie uniquement 20 élèves non inscrits, même s&#39;il y a plus d&#39;élèves non inscrits au cours/à la certification. Ce problème a été résolu.
* Dans certains cas, un problème survenait lors de l&#39;exportation de la liste des élèves non inscrits dans le rapport d&#39;inscription. Ce problème est maintenant résolu.

**Programme d’apprentissage**

* Pour un plan d’apprentissage flexible, si un élève n’est inscrit qu’à une seule instance de cours, lorsque vous cliquez sur le lien des autres cours dont les instances n’ont pas été sélectionnées, une page vide s’ouvre.

**Élève**

* Certains élèves, dont les noms d&#39;utilisateur comportent des caractères spéciaux, ne reçoivent pas de notifications par e-mail comme prévu.
* Dans la vue immersive, dans certains cas, le widget Calendrier n&#39;affiche pas les sessions VC à venir comme prévu.
* Dans l’application de l’élève, le **Compétence** le filtre ne fonctionnait pas comme prévu. Ce problème a été résolu.

**Search**

* Dans un scénario spécifique, le responsable ne pouvait pas rechercher le groupe d&#39;utilisateurs d&#39;un responsable auparavant. Ce problème est maintenant résolu pour le rôle de responsable.

**Groupe d’utilisateurs**

* Lors de l’exportation d’un rapport de groupe d’utilisateurs comptant plus de 500 utilisateurs, les valeurs de données et les en-têtes de colonne du rapport ne correspondaient pas, ce qui est maintenant corrigé.
* Lorsque l’administrateur modifie la signature électronique dans les modèles d’e-mail et ajoute plusieurs lignes, il ne voit les balises html que dans l’interface d’administration. Ce problème a été résolu.
* Entrée **Application d’administration > Catalogue > rechercher un catalogue**, vous ne pouvez pas effectuer de recherche.

**Utilisateurs**

* Quelques utilisateurs externes actifs ont été supprimés. Nous avons apporté quelques modifications et le problème est maintenant résolu.

**Importer**

* L’importation d’un fichier csv échoue si l’en-tête csv contient des espaces blancs de fin ou si l’adresse e-mail d’un utilisateur contient des accents ou des caractères diacritiques.

**Soumission d’activité**

* Dans la page des soumissions d’activités de l’application de l’instructeur, la valeur de date soumise chevauchait un long nom de fichier. Ce problème d’interface utilisateur est maintenant résolu.

**Instructeur**

* Un instructeur reçoit des invitations de session pour toutes ses sessions même si seule une nouvelle session est ajoutée. Ce problème a été résolu.

**SCORM**

* Pour certains contenus SCORM, il existe peu de problèmes liés au navigateur, de problèmes de navigation du lecteur et d’incohérences dans l’enregistrement du score du quiz. Ces problèmes ont été résolus.

**SAML et SSO**

* Nous avons mis à jour le message d’erreur qui s’affiche lorsque les informations d’identification SSO ont expiré.

**API Learning Manager**

* L&#39;API getlearningObject a renvoyé des données d&#39;inscription incorrectes en raison de problèmes de mise en cache. Ce problème a été résolu.
* Une session VC affiche désormais l&#39;URL de la réunion dans le champ Emplacement d&#39;une invitation à une réunion.
* Si vous avez configuré plusieurs intégrations de fournisseurs VC et que l’une d’elles ne fonctionne pas comme prévu, la liste déroulante de sélection VC est vide. Ce problème est maintenant résolu. L’intégration VC restante est maintenant correctement répertoriée.
* Les modèles Connect VC ne se chargent pas comme prévu lorsqu&#39;un instructeur rejoint la session.
* Une durée incorrecte s’affiche dans l’interface utilisateur après la migration des modules avec durée dans le fichier csv module_version.
* Pour certains comptes, la mise à jour d’un utilisateur ne fonctionne pas comme prévu. Ce problème a été résolu.

### Problèmes connus dans cette mise à jour {#known-issues}

* Lors de l’utilisation de **Durée** Dans l’application de l’élève, le contenu et le filtre peuvent ne pas être synchronisés si l’élève utilise d’autres paramètres régionaux de contenu et ne fait pas partie de l’instance par défaut en termes d’inscription.

>[!NOTE]
>
>La formation **Durée**&#39; et &#39;**Format**&#39; les filtres sont identifiés en fonction du contenu de formation disponible pour l&#39;instance par défaut et pour les paramètres régionaux préférés du compte.

+++

+++Mise à jour 59

## Mise à jour 59

Date de publication : 18 décembre 2020

### Connecteur d&#39;événement BlueJeans {#bluejeanseventconnector}

Le connecteur d’événements BlueJeans connecte les systèmes Learning Manager et BlueJeans pour automatiser la synchronisation des données. À l&#39;aide de ce connecteur, vous pouvez :

* **Configuration de sessions virtuelles à l’aide d’événements BlueJeans :** Configurez un nouvel événement dans BlueJeans et configurez une session VC dans Learning Manager en sélectionnant l’événement BlueJeans approprié. Les détails de date et d&#39;heure sont automatiquement sélectionnés à partir des événements BlueJeans.
* **Synchronisation automatisée de l’achèvement des travaux des utilisateurs :** Un processus automatisé de synchronisation de l’achèvement des travaux des utilisateurs permet à l’administrateur de Learning Manager de récupérer automatiquement les enregistrements d’achèvement pour les événements BlueJeans.

Ce nouveau connecteur nécessite un ensemble distinct d&#39;informations d&#39;identification pour configurer le connecteur.

Pour plus d’informations, voir [***Connecteur d&#39;événement BlueJeans***](../integration-admin/feature-summary/connectors.md#bj-events).

+++

+++Mise à jour 58 - Version de décembre 2020 de Learning Manager

## Mise à jour 58 - Version de décembre 2020 de Learning Manager

Date de publication : 5 décembre 2020

### Nouveautés et modifications {#Whatsnewandchanged-2}

Cette version se concentre sur les éléments suivants :

* Toute nouvelle expérience de la page d’accueil des élèves
* Mise en page Web mobile réactive pour le rôle d&#39;élève
* Recommandation basée sur l’IA pour les élèves
* E-mails hebdomadaires de résumé
* Liste de contrôle
* Intégration de Marketo engage
* Domaine personnalisé
* Importation des scores du quiz à partir d’Adobe Connect
* Lien profond vers le catalogue pour les élèves
* Améliorations apportées à linkedIn Learning
* ... et bien d&#39;autres

Pour plus d’informations, voir  [***Nouveautés de la version de décembre 2020 d’Adobe Learning Manager***](../whats-new.md).

### Fonctionnalités non prises en charge dans l’expérience immersive mobile {#unsupportedfeaturesinmobileimmersiveexperience}

Les fonctionnalités suivantes ne sont pas prises en charge :

* Application pour les réseaux sociaux : un élève est redirigé vers l’expérience classique s’il clique sur le widget Réseaux sociaux sur la page d’accueil
* Paramètres du profil/Modifier le profil
* Afficher le badge/les compétences
* Tableau des scores : un élève est redirigé vers l’expérience classique s’il clique sur le widget Tableau des scores sur la page d’accueil
* Téléchargement des assistances à la tâche.
* Options de filtre dans la recherche.

### Bogues corrigés dans cette mise à jour {#bug-fixes-1}

* Vous ne pouvez pas supprimer un dossier de contenu si le dossier de contenu contient du contenu supprimé.
* Le plan d’apprentissage permet aux administrateurs de configurer un cours avec l’instance automatique. Pour un cours avec le module de soumission d&#39;activité, les informations de l&#39;instructeur n&#39;étaient pas correctement configurées auparavant. À présent, Learning Manager affecte automatiquement l’instructeur de l’instance par défaut à cette instance automatique.
* Un badge personnalisé avec un libellé de catalogue avec un espace ne permet pas au fichier PDF de se télécharger comme prévu.
* Un rapport téléchargé à partir du tableau de bord est différent de l’e-mail d’abonnement reçu pour le rapport du tableau de bord.
* Un relevé de notes d’élève ne contient pas de données mises à jour pour une certification récurrente.
* Après avoir commencé un cours, si vous laissez le délai expirer, le nombre de tentatives ne s&#39;affiche pas comme prévu. En outre, il y a parfois un écran vide lorsque vous tentez plusieurs fois un cours.
* Une erreur 5xx se produit après le téléchargement d’un module.
* Un forum de réseau social privé n’est pas visible par tous les élèves.

### Problèmes connus dans cette mise à jour {#known-issues-1}

Après avoir suivi un cours ou obtenu une certification, la fenêtre contextuelle de commentaires ne s’affiche pas immédiatement. Ce problème se produit uniquement lorsque vous suivez le cours dans l’interface utilisateur immersive. Si vous suivez le cours dans l’interface utilisateur classique, la fenêtre contextuelle de commentaires s’affiche comme prévu.

+++

+++Mise à jour 57

## Mise à jour 57

Date de publication : 23 septembre 2020

**Bibliothèque de contenu**

* Dans la bibliothèque de contenu, le retrait d’un contenu ne supprime pas le contenu de la **Publié** onglet. Lorsque vous actualisez la page, le contenu retiré ne s’affiche plus.
* Lors de la création d’un dossier de contenu, le **Nom** n’est pas marqué comme obligatoire, ce qui est en fait un champ obligatoire.

**Demande du client**

* Pour identifier tous les cours auxquels chaque élève est inscrit et s’il l’a terminé, incluez les champs suivants dans le rapport d’abonnement du tableau de bord :

   * UUID
   * Adresse électronique

**Relevé de notes de l’élève**

* La génération d&#39;un relevé de notes de l&#39;élève dans les paramètres régionaux indonésiens produisait des erreurs.

**Search**

* Vous ne pouvez pas rechercher un cours spécifique. Ce problème a été résolu.

+++

+++Mise à jour 56 - Application mobile

Date de publication : 25 août 2020

### Suivre des cours de LinkedIn Learning {#takecoursesfromlinkedinlearning}

Learning Manager prend déjà en charge les cours LinkedIn Learning sur la plateforme d’apprentissage. Les élèves peuvent désormais suivre ces cours LinkedIn Learning dans l’application mobile Learning Manager. Dans l’application pour appareil, recherchez un cours, puis démarrez-le.

Pour plus d’informations, voir Suivre des cours à partir de [***LinkedIn Learning***](../learners/feature-summary/ipad-android-tablet-users.md#linkedin).

### Notification Push pour les inscriptions d’administrateur {#pushnotificationforadminenrollments}

Lorsque l&#39;administrateur inscrit des élèves à des formations, les élèves reçoivent des notifications concernant les inscriptions.

La notification Push est désormais également prise en charge pour les annonces.

### Retour d&#39;informations L1 obligatoire {#mandatoryl1feedback}

Dans sa dernière version d’août 2020, Learning Manager permet aux administrateurs de configurer le retour d’informations L1 de sorte que toutes les questions deviennent obligatoires. Cette option est désormais prise en charge du point de vue de l’élève dans l’application mobile.

### Améliorations de l’interface utilisateur {#userinterfaceenhancements}

**Liens de pied de page**

L’administrateur peut configurer plusieurs liens de pied de page dans la vue Administrateur sur le web. Les élèves peuvent désormais accéder à ces liens en appuyant sur l’icône Hamburger et l’icône Aide .

Par défaut, il y aura deux liens et l’administrateur peut ajouter trois autres liens (via la vue Administrateur sur le Web) qui apparaîtront dans l’application.

**Vue Carte pour les objets d’apprentissage**

Par défaut, dans les sections Mon apprentissage et Catalogue de l&#39;application, les formations apparaissent sous forme de cartes au lieu de listes. Il s&#39;agit d&#39;une modification pour les élèves, car auparavant l&#39;affichage par défaut était « Mode Liste ».

Les élèves peuvent toutefois basculer entre la vue Liste et la vue Carte.

+++

+++Mise à jour 55 - Version d’août 2020 de Learning Manager

Date de publication : 23 août 2020

### Nouveautés et modifications {#Whatsnewandchanged-3}

Cette version se concentre sur les éléments suivants :

* Améliorations des rapports
* Dossiers de contenu privés
* FTP personnalisé
* Prise en charge des sous-titres pour les vidéos
* Améliorations de Power BI
* Améliorations des commentaires
* API nouvelles et modifiées
* Modifications de la stratégie de rétention des données
* ... et bien d&#39;autres

Pour plus d’informations, voir  [***Nouveautés de la version d’août 2020 d’Adobe Learning Manager***](../whats-new.md).

### Remarques concernant cette version {#notes}

* La génération d’un relevé de notes (~1 Go) prend moins de 15 minutes.
* Dans les versions antérieures de Learning Manager, les colonnes du relevé de notes de l&#39;élève intitulées Score du quiz et Score du quiz le plus élevé fournissaient le score et le score maximal au format 25/100. Pour améliorer la lisibilité et l’analyse, le score du quiz est désormais également exporté en tant que colonnes distinctes - **Quiz_score, Quiz_score_max, Highest_Quiz_score et Highest_Quiz_score_max**. Cela permet aux administrateurs d’effectuer des calculs et des analyses rapides.

### Bogues corrigés dans cette mise à jour {#bug-fixes-2}

**Connecteur**

* Un élève ne peut pas participer à deux réunions différentes en même temps, qui sont créées par deux auteurs différents.
* Cliquez sur l’option Gérer les connexions de la carte Adobe Connect pour accéder à la page de connexion FTP.
* Une synchronisation FTP planifiée se ferme avec une exception.
* La connexion à Exavault présente des problèmes liés au mot de passe.

**Cours**

* Vous pouvez créer un module VC sans sélectionner de système de conférence. En guise d&#39;effet secondaire, le processus de création d&#39;un cours renvoie l&#39;erreur 500.
* Un élève ne peut pas télécharger de ressources même s’il est inscrit à un cours qui a été dupliqué.
* Lors de la prévisualisation d’un cours en tant qu’élève, un administrateur ou un auteur ne peut pas télécharger de ressources à moins d’être inscrit au cours.

**Application pour appareil**

* Dans des cas d&#39;inscription spécifiques, le graphique en anneau sous Mon apprentissage en attente affiche différentes valeurs de l&#39;application de l&#39;élève du navigateur à l&#39;application mobile.

**Certification**

* Le statut du filtre de rapport ne fonctionne pas comme prévu lors de la tentative de téléchargement d&#39;un rapport de tableau de bord pour certification.

**Search**

* Sur la page Catalogue de l&#39;élève, lorsque vous tentez de rechercher un cours par note, aucun résultat de recherche n&#39;apparaît.

**SCORM**

* Pour certains contenus, le lecteur SCORM affiche un écran vide.
* Un contenu Storyline est identifié comme un contenu de Captivate si le projet Storyline publié contient un objet Web pointant vers la sortie du Captivate publié.
* Impossible de lancer le contenu SCORM en raison d’une URL incorrecte.

**Rôle personnalisé**

* Dans certains scénarios, un administrateur personnalisé ne peut pas afficher la liste complète des objets d’apprentissage.
* Un administrateur personnalisé ne peut pas rechercher un programme d’apprentissage ou une certification dans les rapports du tableau de bord.
* Un administrateur personnalisé ne peut pas rechercher un responsable dans un tableau de bord.
* Les relevés de notes des élèves générés par un administrateur personnalisé ne contiennent pas de données des utilisateurs supprimés.
* Un auteur personnalisé ou un administrateur personnalisé ne peut pas dupliquer un programme d&#39;apprentissage, un cours ou une certification.

**Rapports**

* La colonne Type d’un relevé de notes affiche la valeur en tant que cours pour les cours qui font partie d’une certification, si l’élève n’est pas inscrit à la certification.

**Compétences**

* Lors de l&#39;ajout d&#39;une compétence pour un cours, il y a quelques problèmes lors de la recherche d&#39;une compétence.

**Ludification**

* Si de nombreux utilisateurs sont rendus confidentiels, lorsque vous cliquez sur l&#39;onglet d&#39;élève confidentiel sur Edge et Internet Example, le navigateur se comporte de manière inattendue.
* Lorsque la fréquence d&#39;un critère est modifiée, les points calculés avec une fréquence plus ancienne sont ajoutés au calcul actuel.

**Administrateur**

* Les élèves ne peuvent pas être marqués comme participants si l&#39;instance de cours mappée à un programme d&#39;apprentissage est modifiée.

**Modèles de courrier électronique**

* Pour les programmes d’apprentissage et les certifications, le bouton bascule dans le modèle de courrier électronique est manquant.

**Bibliothèque de contenu**

* Le contenu SCORM n&#39;est pas lancé comme prévu en raison d&#39;une URL incorrecte.

**Relevés de notes des élèves**

* Lors de la génération des relevés de notes des élèves, si vous ajoutez un élève supprimé dans la zone de saisie Sélectionner les élèves, puis activez l&#39;option « Inclure les données des élèves supprimés » dans Avancé, la page se comporte de manière inattendue.

**Search**

* Vous ne pouvez pas rechercher un cours à l&#39;aide de ses notes.

**Rapports Excel**

* Si le téléchargement d’un rapport de piste d’audit de l’utilisateur prend plus d’une heure en raison de données volumineuses ou d’un traitement lent, la connexion expire et le rapport ne se télécharge jamais.
* Dans un relevé de notes, la colonne Type s’affiche en tant que « Cours » au lieu de « Certification » pour les cours qui font partie de la certification, si l’élève n’est pas inscrit à la certification.

**Application de l’élève**

* Un élève peut suivre un cours ordonné de manière non ordonnée en accédant aux cours via un e-mail de désinscription ou une notification de désinscription.
* Un élève ne reçoit pas d’e-mails de rappel de session comme prévu.
* Un cours ne se lance pas comme prévu si un certain module est manquant.

**Annonce**

* Si une annonce contient la balise <a>, l’annonce n’est pas créée comme prévu.

**Compte**

* Dans certains cas, les comptes sont désactivés même si un compte a une commande valide.

**API**

* Si vous cliquez sur Gérer les connexions dans la carte Adobe Connect, vous êtes redirigé vers la page Connexion FTP.
* Dans certains cas, l’administrateur Connect reçoit des alertes incorrectes.
* La migration de linkedIn Learning génère quelques erreurs.

### Problèmes connus dans cette mise à jour {#known-issues-2}

**Rapports de tableau de bord**

* Lorsqu&#39;un programme d&#39;apprentissage de certification est supprimé, le rapport de formations actives affiche les cours présents dans le programme d&#39;apprentissage ou la certification, même si le programme d&#39;apprentissage ou la certification n&#39;avait pas d&#39;inscription.

+++

+++Mise à jour 54 - Application mobile

## Mise à jour 54 - Application mobile

Date de publication : 16 avril 2020

Pour bénéficier des dernières fonctionnalités et mises à jour, ainsi que d’une meilleure expérience, nous vous recommandons de mettre à jour l’application pour appareil vers la dernière version. La mise à jour est **obligatoire**.

### Nouvelles fonctionnalités et améliorations {#newandenhancedfeatures}

Un administrateur peut communiquer des informations importantes à tous les utilisateurs de l’application. Les annonces peuvent être du type vidéo ou image, ou un simple message texte. Avec cette version de l&#39;application pour appareil, nous prenons désormais en charge les annonces dans l&#39;application pour appareil. Une nouvelle annonce s’affiche dès le lancement de l’application, afin que les élèves ne manquent aucune communication importante envoyée par les administrateurs. Les élèves peuvent la lire instantanément ou ultérieurement en consultant la page **Annonce** onglet.

Lorsqu&#39;il y a une ou plusieurs annonces, vous pouvez voir les annonces dans la section **Annonce** section.

Pour afficher une annonce, appuyez sur **Annonce**. L’annonce la plus récente s’affiche à l’écran.

Pour afficher la prochaine annonce, appuyez sur **Balayer vers la gauche pour passer au suivant**.

### Annonce {#announcements}

![](assets/read-later.png)

Si vous ne voulez pas lire l&#39;annonce à ce moment-là, vous pouvez toujours choisir de lire l&#39;annonce plus tard. Appuyer **Lire plus tard** sur l&#39;annonce et l&#39;annonce retourne à l&#39;état non lu.

### Bogues corrigés dans cette mise à jour {#bugsfixedinthisupdate}

* Sur iOS, la lecture d’un podcast s’arrête lorsque l’écran est verrouillé. Le problème a été résolu et l’audio sera lu même lorsque l’écran sera verrouillé.
* Si vous suivez un cours sur l’application pour appareil, la diapositive de résultat peut parfois apparaître vide. Ce problème a été résolu dans cette mise à jour.

+++

+++Mise à jour 53 - Version d’avril 2020 de Learning Manager

Date de publication : 4 avril 2020

La version d’avril 2020 de Learning Manager se concentrait sur les éléments suivants :

* [Améliorations des performances](../whats-new.md#performance)
* [Formation en salle de classe](../whats-new.md#classroom)
* [Workflows de gestion](../whats-new.md#manager)
* [Apprentissage par les réseaux sociaux](../whats-new.md#social)
* [Rapports](../whats-new.md#reporting)
* [Expérience de l’élève](../whats-new.md#learner)
* [Modifications au niveau de l’API](../whats-new.md#api)

Pour plus d’informations, voir [***Nouveautés de la version d’avril 2020 de Learning Manager***](../whats-new.md).

+++

+++Mise à jour 52 - Application mobile

## Mise à jour 52 - Application mobile

Date de publication : 20 décembre 2019

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-1}

#### Logo de la marque de l’entreprise {#companybrandinglogo}

L&#39;application peut désormais afficher le nom de la marque, le logo de la marque ou les deux dans l&#39;application pour appareil en fonction des paramètres définis par l&#39;administrateur.

#### Liens profonds {#deeplinks}

Learning Manager lance désormais l’application pour appareil dès que vous cliquez sur une URL ou un lien pris en charge par Learning Manager. Si l’application n’est pas installée sur l’appareil, l’URL s’ouvre dans le navigateur.

Voici quelques cas d’utilisation qui seront pris en charge dans cette mise à jour.

* Cliquez sur une URL de formation reçue dans un e-mail.
* URL de formation par défaut qui apparaissent dans les modèles de courrier électronique.
* L’URL du compte qui apparaît dans les modèles d’e-mails.
* URL d’accès à Mon apprentissage et au catalogue.

En outre, toute URL avec domaine *learningmanager.adobe.com* s’ouvre dans l’application pour appareil.

#### Charger des actifs dans un certificat externe comme justificatif d’accomplissement {#uploadassetsinexternalcertificateasproofofcompletion}

Dans cette mise à jour, un élève peut charger des ressources comme justificatif d’accomplissement d’un certificat externe.

Un élève peut ouvrir un certificat externe et charger des ressources, telles que des fichiers PDF, texte ou image.

Pour plus d’informations, voir  [***Charger des actifs dans un certificat externe***](../learners/feature-summary/ipad-android-tablet-users.md#externalcert).****

### Problèmes résolus dans cette version {#issuesfixedinthisrelease}

* Un utilisateur ne peut pas se connecter à l’application pour appareil si l’e-mail contient des caractères spéciaux.
* Lors du défilement, l’icône de l’objet d’apprentissage clignote lorsque vous êtes dans une vue de liste.
* Vous pouvez désormais afficher toutes les notifications push sans appuyer sur le bouton fléché vers le bas et afficher les messages un par un.
* Lorsque vous cliquez sur une notification pour une publication qui a été acceptée ou rejetée lors de la curation, une page vierge s’ouvre dans l’application. Dans cette mise à jour, la page du forum s’ouvre.

+++

+++Mise à jour 51

Dans cette mise à jour, vous pouvez également modifier l&#39;image de bannière pour un objet d&#39;apprentissage.

Vous pouvez également personnaliser la bannière dans une page Apprentissage par les réseaux sociaux.

## Mise à jour 51

Date de publication : 17 décembre 2019

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-2}

### Portée des plans d’apprentissage définie en fonction de rôles configurables {#learningplansscopedbyconfigurableroles}

Vous pouvez créer des rôles personnalisés pour les plans d&#39;apprentissage qui permettent de définir la portée des utilisateurs et des objets d&#39;apprentissage. En d’autres termes, les plans d’apprentissage peuvent être créés avec une portée limitée dérivée de la portée du rôle d’un administrateur personnalisé.

Désormais, un administrateur peut définir ou restreindre la portée tout en accordant un accès en tant que responsable du plan d&#39;apprentissage.

Pour plus d’informations, voir [***Portée des plans d’apprentissage définie en fonction de rôles configurables***](../administrators/feature-summary/custom-role.md#scopeconfigure).

### Restreindre les champs actifs dans les rapports {#restrictactivefieldsinreports}

Pour les champs actifs, nous avons ajouté deux nouvelles options... **Déclarable** et **Exportable**.

Pour les champs CSV et les champs ajoutés manuellement, si un champ actif est marqué comme **Déclarable**, le champ actif peut être recherché dans un filtre à l’intérieur d’un rapport de tableau de bord.

Pour plus d’informations, voir  [***Restreindre les champs actifs dans les rapports***](../administrators/feature-summary/add-users-user-groups.md#restrictactivefields)***,***

### Afficher la description du module de contenu {#viewdescriptionofcontentmodule}

En tant qu&#39;auteur, vous pouvez voir la description des modules lors de l&#39;ajout du module à un cours.

Lors de la création d’un module, ajoutez sa description. Pour en savoir plus sur la création d&#39;un cours, voir [***Création d’un cours***](../authors/feature-summary/courses.md).

### Afficher les noms des cours et des sessions {#displaycourseandsessionnames}

En tant qu’instructeur, vous pouvez voir les noms des sessions et des cours dans la vue Présence. Vous pouvez effectuer le suivi des sessions en cours de modification.

### Annonce pour les élèves {#announcementforlearners}

Les élèves peuvent désormais afficher une annonce en plein écran au lieu d&#39;une vue sous forme de liste. Cela se produit lorsque l’élève a une annonce non lue. Cela améliore l’expérience des élèves lors de la visualisation de l’annonce.

Adobe Learning Manager vous permet désormais de personnaliser votre compte afin d’améliorer l’expérience de vos utilisateurs. Voici une liste des éléments qui peuvent être personnalisés. Contact [Prise en charge de Learning Manager](mailto:learningmanagersupport@adobe.com)pour apporter ces modifications.

* Couleurs de la carte d&#39;entraînement.
* Icône Progression
* Image du pointeur de la souris
* Police

Pour plus d’informations, voir [***Personnalisation de votre compte***](../administrators/feature-summary/themes.md#customize).

### Charger des images de bannière {#uploadbannerimages}

Dans cette mise à jour, vous pouvez également modifier l&#39;image de bannière pour un objet d&#39;apprentissage.

Vous pouvez également personnaliser la bannière dans une page Apprentissage par les réseaux sociaux.

### Prise en charge des API {#apisupport}

Cette mise à jour de Learning Manager inclut une API pour les opérations suivantes :

**Télécharger le PDF de badges**

Cette mise à jour inclut une API permettant à l’élève de télécharger le PDF d’un badge.

**Télécharger le relevé de notes de l’élève**

Cette mise à jour inclut une API permettant à l&#39;élève de télécharger ses relevés de notes.

**Télécharger le rapport de quiz**

Cette mise à jour inclut une API permettant à un administrateur de télécharger les rapports de quiz.

**Ludification paginée**

L’API de l’élève permet désormais la récupération de tous les élèves et points de ludification dans la portée de l’élève. Cela aide à construire un tableau des scores de ludification.

**API :** `GET /users`

**Demande :** `GET\\ users?page[offset]=0&page[limit]=10&sort=id&filter=gamification`

**Réponse :** *La réponse contiendra les utilisateurs triés par ordre de points de ludification.*

**Ne pas déranger**

Actuellement, seuls les administrateurs peuvent ajouter des utilisateurs à une liste Ne pas déranger via l’interface utilisateur. Après cette version, un élève pourra définir ces autorisations lui-même via l’API à condition que cette dernière soit activée par l’administrateur. L’activation de cette API pour un compte nécessite un paramètre de serveur principal. Cette API permet à l’élève de modifier les autorisations liées aux e-mails ci-dessous.

* Courriers électroniques directs à l’élève
* Courriers électroniques d’escalade aux responsables d’élèves
* À propos des subordonnés directs
* À propos des rapports de niveau d’ignorance

Pour plus d’informations sur les API Learning Manager, voir :

* [***Référence API***](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v2/)
* [***Guide du développeur d’API***](<https://helpx.adobe.com/captivate-Learning> Manager/integration-admin/feature-summary/developer-manual.html)

### Problèmes résolus dans cette version {#Issuesfixedinthisrelease-1}

* Seuls les utilisateurs appartenant à un groupe d&#39;utilisateurs spécifique doivent recevoir les annonces qui leur sont destinées. Les autres utilisateurs ne doivent pas recevoir les annonces.
* Le lecteur affiche une double flèche de chargement avant que le contenu ne s’affiche.
* Les métadonnées utilisateur dans les rapports provoquent une exception de pointeur Null.
* Lors de l&#39;ajout d&#39;un instructeur pour une instance par défaut pour le cours Connect VC, le message, *« Aucune session pour ce module »*, s’affiche dans la page Instance de cours de l’application d’administration.

* L&#39;exportation d&#39;un relevé de notes d&#39;élève entraîne un comportement inattendu lors d&#39;un transfert FTP.
* Le nom d&#39;un auteur ne s&#39;affiche pas correctement dans les cours d&#39;un programme d&#39;apprentissage.
* Les modifications de la terminologie des assistances à la tâche ne sont pas reflétées comme prévu.
* Le nom d’un module est tronqué s’il est long et affiché en mode portrait sur un appareil mobile.
* Impossible de créer une instance pour un ancien cours Connect après la mise à jour de l&#39;instance par défaut avec l&#39;ancienne implémentation Connect.
* Un instructeur reçoit une invitation de calendrier avant même la publication du cours.

+++

+++Mise à jour 50

## Mise à jour 50

Date de publication : 24 octobre 2019

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-3}

#### Créer un rôle personnalisé avec plusieurs portées de catalogue {#createcustomrolewithmultiplecatalogscopes}

En tant qu’administrateur, vous pouvez restreindre un rôle personnalisé en fonction des catalogues et des groupes d’utilisateurs. Tous les utilisateurs appartenant à ces rôles peuvent uniquement voir les objets d’apprentissage du catalogue dans leur portée. Ces utilisateurs peuvent uniquement effectuer des actions définies dans la portée de leurs groupes d’utilisateurs.

Jusqu’à présent, dans Learning Manager, la portée d’un rôle personnalisé pouvait s’étendre à plusieurs catalogues pour un seul groupe d’utilisateurs avec des autorisations complètes.

Dans cette mise à jour de Learning Manager, vous pouvez créer un rôle personnalisé dont la portée s’étend à plusieurs catalogues disposant chacun d’ensembles d’autorisations différents. Pour plus d’informations, voir [***Rôle personnalisé étendu à plusieurs catalogues***](../administrators/feature-summary/custom-role.md#multi-scope).

### Améliorations apportées à la recherche {#enhancementstosearch}

**Plan d’apprentissage**

Sur la page Plans d&#39;apprentissage pour les administrateurs et les auteurs, il y a maintenant une barre de recherche, que vous pouvez utiliser pour rechercher n&#39;importe quel plan d&#39;apprentissage.

![](assets/search-for-as-learningplan.png)

**Applications de l’administrateur et de l’auteur**

Dans cette mise à jour de Learning Manager, en tant qu’administrateur ou auteur, en plus de la recherche par frappe anticipée, vous pouvez effectuer une recherche libre pour rechercher n’importe quel objet d’apprentissage.

### Le filtre de recherche est conservé {#searchfilterispreserved}

Cela s’applique uniquement à un profil d’élève.

Sur la **Catalogue** et **Mon apprentissage** pages, un élève peut appliquer un filtre sur le panneau de gauche, par exemple, **Cours** ou **Programmes d’apprentissage**, puis cliquez sur un cours ou un élément de catalogue.

![](assets/choose-learning-objects.png)

Lorsque l’élève revient à la page **Catalogue** ou **Mon apprentissage** à l’aide du bouton Précédent du navigateur, le filtre reste conservé. Le filtre qu’un élève avait appliqué précédemment n’est plus réinitialisé.

### Contrôle de la visibilité des filtres de recherche {#controlvisibilityofsearchfilters}

Dans les versions antérieures de Learning Manager, les administrateurs ne contrôlent pas les options de visibilité d’un filtre de catalogue, de sorte que les élèves ne voient pas les compétences et les balises. Dans cette version de Learning Manager, les administrateurs peuvent filtrer les types, les compétences et les balises d’un catalogue.

Dans le panneau **Paramètres** , pour la catégorie Afficher les panneaux de filtres, lorsque vous cliquez sur **[!UICONTROL Modifier]**, vous pouvez voir les options suivantes. Les options déterminent les panneaux de filtres qui sont visibles par les élèves, afin que ceux-ci puissent affiner les résultats de la recherche.

Pour plus d’informations, voir [***Afficher les panneaux de filtres***](../administrators/feature-summary/settings.md#filter-panels).

### Télécharger le code QR à partir de l’application Administrateur {#downloadqrcodefromadministratorapp}

Dans les mises à jour précédentes de Learning Manager, un administrateur personnalisé rencontrait des problèmes lors du téléchargement d’un code QR. Dans cette mise à jour, un administrateur personnalisé qui a eu accès à **Tous les élèves** et autorisation pour **Inscription au cours** peut télécharger le code QR.

Le code QR n’est toujours pas disponible pour les utilisateurs avec un rôle personnalisé s’ils disposent d’autorisations pour une portée limitée d’utilisateurs.

### Ajouter des commentaires lors de l’inscription des élèves {#addcommentswhileenrollinglearners}

En tant qu&#39;administrateur ou responsable, vous pouvez ajouter des commentaires lors de l&#39;inscription d&#39;élèves à un cours. Vous pouvez mentionner des informations supplémentaires sur la cohorte d’utilisateurs qui s’inscrivent. Ces données sont exportées dans les rapports de cours.

Pour plus d’informations, voir [***Ajouter des commentaires lors de l’inscription des élèves***](../administrators/feature-summary/courses.md#enroll-comments).

### Prise en charge de la salle de réunion persistante d’Adobe Connect {#supportforadobeconnectpersistentmeetingroom}

Dans Adobe Connect, les clients utilisent des salles de réunion existantes qu’ils ont déjà créées dans Connect. Toutes les salles de réunion dans Connect sont persistantes et les modèles de salle de réunion sont soigneusement configurés pour fournir une expérience unifiée pour chaque salle persistante.

Dans cette version de Learning Manager, l’intégration à Adobe Connect est désormais améliorée pour prendre également en charge les salles persistantes. Cela signifie que vous pouvez désormais créer une session de classe virtuelle en utilisant l’une des salles déjà créées dans Adobe Connect.

Learning Manager permet désormais également aux élèves d’entrer dans la salle Connect pour leur session virtuelle à l’aide de l’authentification SSO.

Pour plus d’informations, voir [***Prise en charge des salles persistantes dans Adobe Connect***](../integration-admin/feature-summary/connectors.md#persistent).

### Avertissement avant d’indiquer l’assiduité si la durée de la session est nulle {#warningbeforemarkingattendanceifthesessiondurationiszero}

Un auteur ou un administrateur peut créer une session d’une durée égale à 0. Il est possible lorsque :

* les dates de début et/ou de fin sont vides.
* l&#39;heure de début et/ou l&#39;heure de fin sont vides.

Dans cette mise à jour, un **message d’avertissement indiquant que la durée d’une session est égale à zéro**, est présenté à l’administrateur, au responsable ou à l’instructeur.

### Avertissement si un module de salle de classe est créé sans ajouter de données de session {#warningifaclassroommoduleiscreatedwithoutaddingsessiondata}

Si un auteur crée un cours en ajoutant un module de salle de classe ou de classe virtuelle, il peut choisir de :

* Ne pas ajouter de date de début/fin ni d&#39;heure de début/fin.
* Ajoutez une date, mais pas d&#39;heure de début/fin.
* Ajoutez une date et une heure de début.

Dans tous les cas ci-dessus, lorsqu&#39;un administrateur, un responsable ou un instructeur indique l&#39;assiduité ou l&#39;achèvement, les valeurs des dates de début et de fin de la session deviennent égales, ce qui signifie que dans le relevé de notes de l&#39;élève, la valeur Temps d&#39;apprentissage passé est affichée comme zéro.

Dans cette mise à jour, un **message d’avertissement indiquant que les données de session sont incomplètes**, est présenté à l’auteur.

### Problèmes résolus dans cette version {#Issuesfixedinthisrelease-2}

**Application de l’élève**

* Un élève ne peut pas afficher un cours dans un programme d’apprentissage si le cours a été créé par un auteur externe.
* Si un administrateur ajoute une publication à un forum externe, la demande de curation est envoyée à un expert interne, qui est affecté à cette compétence.
* Un élève ne peut pas afficher le bouton Démarrer ou Continuer après s’être inscrit aux cours LinkedIn.

**E-mail**

* Lorsqu&#39;il y avait un grand nombre d&#39;utilisateurs dans une liste de courriers électroniques NPD, le **Paramètres** La page se charge très lentement. Dans cette mise à jour, la pagination est ajoutée à une liste d’e-mails NPD.
* Un instructeur reçoit des mises à jour/des courriers électroniques pour les sessions dont il ne fait pas partie. Dans cette mise à jour, ce problème a été résolu.

**Compétences**

* Dans un relevé de notes d’élève, le type de valeur d’une compétence s’affiche de manière incorrecte sous forme de texte.

**Application mobile**

* Dans l’application mobile, un élève pouvait afficher une instance de plan d’apprentissage et s’y inscrire, ce qui n’était pas le comportement prévu. Dans cette mise à jour, ce problème a été résolu.

**Rôles personnalisés**

* En tant qu’administrateur personnalisé, vous ne pouvez pas rechercher un responsable dans un rapport de tableau de bord.

**Tentatives multiples**

* Dans certains scénarios, certains modules de cours ne sont pas affichés aux élèves.

**Inscription externe**

* Vous ne pouvez pas modifier le profil externe d’un utilisateur si des places ont été occupées par des profils supérieurs.

### Problèmes connus dans cette version {#knownissuesinthisrelease}

* Sur les navigateurs mentionnés ci-dessous, lorsque vous passez la souris sur le volet de gauche, le texte apparaît après un léger retard.

   * Edge 42.17134.1.0
   * Edge 44.17763.1.0
   * Internet Explorer 11.1006
   * Internet Explorer 11.615

* Un élève est autorisé à entrer dans une salle de réunion Connect avant et après la session.

+++

+++Mise à jour 49

## Mise à jour 49

Date de publication : 26 août 2019

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-4}

**Améliorations des performances**

* L’importation d’utilisateurs dans le système est plus rapide que dans les versions précédentes. L’importation de données utilisateur volumineuses apporte une amélioration significative.
* Pour les responsables et les administrateurs, les options de la liste déroulante Configuration du rapport ont été modifiées pour charger les données à la demande.
* Les performances des API ont été améliorées. De nombreuses API devraient désormais bénéficier d’un temps de réponse amélioré.
* Le temps nécessaire pour générer le relevé de notes de l&#39;élève a été amélioré.
* Il n’y a pas de décalage dans les pages où les élèves internes et externes sont répertoriés, en particulier lorsqu’il y a un grand nombre d’utilisateurs.

**Privilèges d’utilisateur spécial**

Un administrateur peut accorder des privilèges spéciaux à un groupe d&#39;utilisateurs, en utilisant les membres du groupe qui peuvent participer à tous les forums. Toutes les restrictions définies dans la section Paramètres de l&#39;étendue sont contournées par le groupe d&#39;utilisateurs spéciaux. Pour plus d’informations, voir [***Privilèges d’utilisateur spécial***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#privilege).

**Modifications apportées à l’interface utilisateur**

* Dans le panneau **Ajouter un rapport** , la boîte de dialogue **Plage temporelle** et **Filtres** par défaut, les sélecteurs s’affichent sous la forme de sections distinctes réduites. Pour plus d’informations, voir [***Création de rapports***](../administrators/feature-summary/reports.md#report).

* Dans le panneau **Ajouter un rapport** , pour un groupe d’utilisateurs, vous pouvez utiliser la recherche par frappe anticipée pour choisir un ou plusieurs groupes d’utilisateurs. Pour plus d’informations, voir [***Rapports de groupe d’utilisateurs***](../administrators/feature-summary/reports.md#user-group-reporting).

**Modifications des valeurs dans les colonnes de temps**

Dans les relevés de notes des élèves, dans les colonnes de temps, les minutes sont arrondies à la minute la plus proche et la valeur de la seconde est 00. Pour plus d’informations, voir [***Colonnes de temps***](../administrators/feature-summary/learner-transcripts.md#datetime).

### Problèmes résolus dans cette version {#Issuesfixedinthisrelease-3}

**Tableau de bord de l’élève**

* Un calendrier d&#39;apprentissage affichait l&#39;état **Inscrit à la session** même lorsqu’un responsable devait encore approuver l’inscription. Statut correct **En attente** s’affiche pour l’élève jusqu’à ce que le responsable approuve l’inscription.

* Dans un cas particulier, pour une session, le calendrier d&#39;apprentissage affichait le statut **Inscrit** même si l’élève a terminé un cours.

**Tableau de bord du responsable**

* Les responsables n’ont pas pu suivre les formations de conformité de leur équipe si les membres de l’équipe sont inscrits via des plans d’apprentissage.

**Search**

* Dans la vue de l’instructeur, vous n’avez pas pu rechercher un élève.

**Interface utilisateur**

* Pour un compte avec des modifications de taxonomie appliquées, les modifications n’étaient pas reflétées comme prévu dans les notifications.

### Problèmes connus dans cette version {#Knownissuesinthisrelease-1}

* À l’aide de la barre de recherche, vous ne pouvez pas rechercher les utilisateurs supprimés dans la liste Utilisateurs externes. Pour contourner ce problème, faites défiler la liste vers le bas pour afficher la liste de tous les utilisateurs et localiser l’utilisateur requis manuellement.
* Si un utilisateur spécial publie sur un forum externe, la demande de curation est reçue par les experts dans son domaine d’application.

+++

+++Mise à jour 48

## Mise à jour 48

Date de publication : 2 août 2019

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-5}

**Séparation de l’étendue dans l’apprentissage par les réseaux sociaux pour les utilisateurs internes et externes** Un administrateur peut définir des portées distinctes pour les élèves internes et externes. Il existe deux nouvelles sections pour les utilisateurs internes et externes. Dans les deux sections, vous pouvez définir les étendues pour les groupes d&#39;élèves. Pour les utilisateurs internes, vous pouvez définir les valeurs de la caractéristique utilisateur. Pour les utilisateurs externes, vous pouvez définir le profil externe, au sein duquel les élèves peuvent partager le même espace social. Pour plus d’informations, voir [***Paramètres d’étendue***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#scopesettings).  **Restrictions concernant la création de forums de réseaux sociaux** Pour restreindre la création de forums par tous les élèves et pour modérer efficacement les forums, un administrateur peut accorder des autorisations pour créer des forums dédiés à un groupe d’utilisateurs sélectionné. L’administrateur peut restreindre la création d’un forum à un groupe sélectionné et non à tous les élèves qui participent à l’apprentissage par les réseaux sociaux. Pour plus d’informations, voir [***Autorisations de création de forums***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#permission).  **Afficher uniquement les champs actifs vides pour les élèves** Un administrateur peut choisir d’afficher les champs actifs ou de masquer les champs une fois les valeurs renseignées. Pour plus d’informations, voir [***Affichage de l’utilisateur***](../administrators/feature-summary/add-users-user-groups.md#activefields).  **Les utilisateurs internes sont supprimés après une durée d’inactivité spécifiée** Un administrateur peut définir la durée (en jours) pendant laquelle un élève interne est supprimé si l’élève reste inactif pendant la durée spécifiée. Pour plus d’informations, voir ***[Supprimer automatiquement les utilisateurs](../administrators/feature-summary/settings.md#autodelete)***.  **Personnalisation des liens du pied de page** Un administrateur peut ajouter et personnaliser des liens dans le pied de page. Les liens peuvent également être personnalisés pour différentes langues. La méthode existante pour ajouter le lien Contacter l’administrateur dans le pied de page est également disponible dans la section **Liens du pied de page** section. Pour plus d’informations, voir [***Personnalisation des liens de pied de page***](../administrators/feature-summary/settings.md#footer).

### Problèmes connus dans cette version {#Knownissuesinthisrelease-2}

* Les liens de pied de page personnalisés n’apparaissent pas pour les rôles d’administrateur d’intégration.

+++

+++Mise à jour 47 - Application mobile

## Mise à jour 47 - Application mobile

Date de publication : 24 juillet 2019

Utilisateurs Android :

Cette mise à jour prend également en charge les modifications nécessaires pour adhérer aux recommandations révisées de Google pour mettre en œuvre les notifications push. Vous ne recevrez donc plus **notifications** si vous utilisez la version 2.7.4 ou antérieure.

Pour recevoir des notifications, nous vous recommandons de mettre à niveau à la version 2.8.

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-6}

**Apprentissage par les réseaux sociaux**

Partagez votre expertise avec vos pairs sous la forme de contenu généré par les utilisateurs et publié sur des forums de discussion thématiques. D&#39;autres élèves intéressés par des compétences similaires peuvent suivre ces forums pour apprendre et même contribuer au sujet, un peu comme une plateforme de médias sociaux.

Partagez des idées et des idées significatives dans un environnement informel. Aimez, n’aimez pas une publication, chargez du contenu et commentez des publications. Pour plus d’informations, voir [***Apprentissage par les réseaux sociaux dans l’application mobile***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Partage de médias dans un forum**

Partagez des photos, des documents ou des fichiers audio ou vidéo sur n’importe quel forum, afin que les autres membres du forum puissent voir votre publication et commencer une interaction.  Pour plus d’informations, voir [***Partager la publication***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Envoyer un fichier pour la classe et les modules d’activité**

Envoyez des fichiers comme preuve de l’accomplissement du cours à votre instructeur. L&#39;instructeur peut ensuite approuver ou rejeter votre envoi, en fonction du contenu du fichier. Pour plus d’informations, voir [***Soumettre le fichier pour approbation***](../learners/feature-summary/ipad-android-tablet-users.md#submitfile).

**Prise en charge des plateformes mise à jour**

L’application mobile Learning Manager est désormais prise en charge sur les appareils équipés d’Android 7 et versions ultérieures, ainsi que d’iOS 10 et versions ultérieures. Pour plus d’informations, voir [***Configuration requise***](../system-requirements.md).

### Problèmes connus dans cette version {#Knownissuesinthisrelease-3}

1. Sur Android, vous ne pouvez pas charger de fichier de GIF dans une publication, un commentaire ou en répondant à un commentaire.
1. En tant que modérateur d’un forum, vous ne pouvez pas supprimer une publication, un commentaire ou une réponse d’un utilisateur. Vous pouvez toutefois effectuer la même opération à partir de l’application web.
1. Dans l’application, vous ne pouvez pas marquer un type de question.
1. Après avoir activé l’apprentissage par les réseaux sociaux sur l’application, relancez l’application pour afficher l’onglet **Apprentissage par les réseaux sociaux**. Si l’Apprentissage par les réseaux sociaux n’est pas affiché, fermez l’application, puis redémarrez-la. L’onglet Apprentissage par les réseaux sociaux s’affiche.

+++

+++Mise à jour 46

### Nouvelles fonctionnalités et améliorations {#Newandenhancedfeatures-7}

## Mise à jour 46

Date de publication : 20 juin 2019

**Auto-curation du contenu**

L’apprentissage par les réseaux sociaux permet au contenu publié par les élèves d’être conservé de deux manières : **Aucune curation** et **Curation manuelle**. Dans cette version, Adobe Learning Manager améliore l&#39;apprentissage par les réseaux sociaux en fournissant des fonctionnalités d&#39;auto-curation compatibles avec l&#39;IA. Une fois le contenu publié, il est analysé pour déterminer s’il appartient à la compétence pour laquelle il a été publié. En fonction du score de confiance, le contenu est publié en direct ou envoyé pour une curation manuelle. Pour plus d’informations, voir *[** Curation à assistance automatique **](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#autocuration)**.***

**Mapper une compétence avec des domaines de compétence**

Mappez les compétences de votre compte avec les domaines de compétence présents dans le LMS Learning Manager. Cela permet de lier les compétences de votre compte aux domaines de compétence pris en charge par Learning Manager pour la curation à assistance automatique. Pour plus d’informations, voir [***Mapper les compétences avec les domaines***](../administrators/feature-summary/curation-skills.md).

**Spécifications et exemples de fichiers CSV**

Spécifications CSV mises à jour que vous pouvez utiliser pour mapper vos données de migration LMS existantes. Utilisez les dernières spécifications csv téléchargeables et les fichiers zip d’exemple csv pour comprendre le format prescrit des données à saisir. Pour plus d’informations, voir  [***Manuel de migration***.](../integration-admin/feature-summary/migration-manual.md)

### Problèmes résolus dans cette version {#Issuesfixedinthisrelease-4}

**API Learning Manager**

* Lorsqu’un profil externe est ajouté à l’aide de la méthode de POST de l’API *externalProfile*, le message de bienvenue ne s’affiche pas.

**Tableau de bord du responsable**

* Lorsqu’un responsable a sélectionné l’option **Ce trimestre**, les détails d&#39;inscription, de progression et d&#39;achèvement d&#39;un objet d&#39;apprentissage ne s&#39;affichaient pas. Dans cette version, ces détails s’affichent désormais comme prévu.

**Élèves sur liste d’attente**

* Dans les versions antérieures de Learning Manager, après inscription des élèves par un responsable, un message d’erreur s’affichait lorsqu’un instructeur voulait vérifier les élèves inscrits sur liste d’attente. Dans cette version, un instructeur peut parcourir la liste des élèves inscrits sur liste d’attente sans rencontrer de message d’erreur.

**Présentation de la certification**

* Après qu&#39;un auteur a créé un cours et une certification qui contenait une description et un contenu de présentation, lorsqu&#39;un élève accédait à la page du cours, le contenu de la présentation ne s&#39;affichait pas comme prévu. Le contenu, cependant, était visible sur les pages d&#39;aperçu de l&#39;élève dans les applications Administrateur et Auteur. Dans cette version, le contenu de la présentation s&#39;affiche comme prévu dans l&#39;application Élève.

**Catalogue**

* Pour chaque catalogue, un élève peut afficher tous les objets d’apprentissage. Dans les versions précédentes, si un catalogue ne contenait pas d&#39;objet d&#39;apprentissage, le catalogue s&#39;affichait toujours au début des autres catalogues. Dans cette version, tous les catalogues qui n’ont pas d’objets d’apprentissage apparaissent au bas des catalogues.

+++

+++Mise à jour 45

Date de publication : 30 mai 2019

**Nouvelles fonctionnalités et améliorations**

* Recherche consolidée dans toutes les instances pour les élèves inscrits dans la section des élèves de l&#39;objet d&#39;apprentissage. Recherchez les utilisateurs inscrits dans la section Élève de l&#39;objet d&#39;apprentissage à l&#39;aide de la recherche par frappe anticipée. Pour plus d’informations, voir [***Recherche d’utilisateurs inscrits***](../administrators/feature-summary/courses.md#searchforusers).
* Fonctions d’édition complètes des objets d’apprentissage acquis via un catalogue partagé. Pour plus d’informations, voir [***Contrôle de catalogue partagé***](../administrators/feature-summary/shared-catalog-full-control.md). Pour activer la fonctionnalité, contactez l’assistance de Learning Manager.
* Les instructeurs peuvent désormais facilement identifier les sessions et modules avec des révisions en attente. Pour plus d’informations, voir [***Révisions en attente***](../instructors/feature-summary/learners.md#pending).

* Les compétences permettent désormais d’attribuer des valeurs de crédit au format décimal. Cela permet aux auteurs d’attribuer une valeur de crédit de niveau décimal à un cours donné. Pour plus d’informations, voir [***Prise en charge des décimales***](../administrators/feature-summary/skills-levels.md#decimal).
* Automatisez la création de rôles personnalisés. Pour plus d’informations, voir [***Configuration des rôles via des fichiers CSV***](../integration-admin/feature-summary/configure-role-csv-files.md).
* Les envois requis pour les certifications externes et les modules d’activité sont désormais facultatifs. Cela permet aux responsables et aux instructeurs d&#39;évaluer sans envoi. Pour plus d’informations, voir [***Envoi facultatif***](../managers/feature-summary/learning-objects.md#optional).
* Télécharger les relevés de notes des élèves pour les utilisateurs supprimés. Pour plus d’informations, voir [***Relevés de notes des élèves***](../administrators/feature-summary/learner-transcripts.md).
* Prise en charge des langues suivantes :

   * Coréen
   * Turc
   * Néerlandais
   * Polonais

**Problèmes connus**

* La prise en charge des décimales dans les crédits de compétence est uniquement prise en charge pour l’anglais.
* Pour les langues coréenne, japonaise et russe, la valeur du méridien de temps de session ne s&#39;affiche pas comme prévu.

**Problèmes résolus dans cette version**

* Les scores du quiz ne sont pas enregistrés pour un programme d&#39;apprentissage ou une certification dans les onglets Présence et notation.
* Un administrateur ou un responsable ne peut pas marquer une certification externe comme terminée.
* Dans la boîte de dialogue Relevés de notes des élèves, un administrateur ne peut pas sélectionner une plage de dates personnalisée si la langue est définie sur Portugais ou Espagnol.
* Un administrateur ne peut pas créer de profil externe lorsque la langue du profil est le français.
* Les champs actifs ne sont pas visibles dans la boîte de dialogue Modifier l’utilisateur si les paramètres régionaux sont dans une autre langue que l’anglais.

+++

+++Mise à jour 44 - Application mobile

Date de publication : 26 avril 2019

* **Modifications apportées à l’interface utilisateur :** Dans l’application, le  ![](assets/hamburger.jpg) et le  ![](assets/search-magnifying-glass-icon.png) Les options s’affichent désormais en haut.

![](assets/1.png)

* **Scannez le code QR pour vous inscrire :** Les fonctionnalités de code QR sont améliorées. En plus de prendre en charge la notation de l&#39;assiduité à l&#39;aide du code QR, il prend désormais également en charge l&#39;inscription à un cours et l&#39;achèvement d&#39;un cours à l&#39;aide du code QR.

  Pour vous inscrire à un cours et le terminer, vous pouvez lire un code QR fourni par votre administrateur. Pour plus d’informations sur la numérisation des codes QR dans la version web de Learning Manager, voir  [***Scanner le code QR***](<https://helpx.adobe.com/captivate-Learning> Manager/whats-new.html#QRcodetoenrollcompleteenrollcompleteacourse).

* **Tentatives multiples au cours :** L’application Learning Manager permet à l’élève d’utiliser des cours avec plusieurs tentatives activées. Pour plus d’informations sur la configuration des tentatives multiples, voir  [***Tentatives multiples***](<https://helpx.adobe.com/captivate-Learning> Manager/authors/feature-summary/courses.html#Multiattempts).

+++

+++Mise à jour 43

## Mise à jour 43

Date de publication : 28 janvier 2019

* Le temps d&#39;apprentissage passé par un élève sur un module peut être compté plusieurs fois pour marquer l&#39;assiduité plus d&#39;une fois. Ce problème a été résolu.
* Le fait de marquer l&#39;assiduité d&#39;un objet d&#39;apprentissage dans une session de plusieurs jours peut afficher une date de début de session incorrecte pour un élève dans un relevé de notes d&#39;apprentissage. Ce problème a été résolu.
* Les utilisateurs peuvent ne pas être en mesure d’afficher un cours lorsqu’il est ajouté à un programme d’apprentissage ou à une certification terminé. Ce problème a été résolu.
* L’inscription des utilisateurs peut se produire de manière incorrecte lorsqu’ils sont retirés d’un groupe d’utilisateurs. Ce problème a été résolu.
* L’élève et l’instructeur peuvent ne pas recevoir de courrier électronique lorsque les détails de la session sont modifiés dans l’application Instructeur. Ce problème a été résolu.
* L’URL Adobe Connect peut ne pas fonctionner correctement lorsque « / » est fourni à la fin de l’URL. Ce problème a été résolu.
* Un message d&#39;erreur peut s&#39;afficher lors de la sélection d&#39;au moins un module obligatoire pour un cours déjà publié. Ce problème a été résolu.
* Lorsqu&#39;un élève a terminé un cours et que celui-ci est ensuite marqué comme obligatoire par l&#39;auteur, l&#39;achèvement du cours peut ne pas être marqué comme terminé. Ce problème a été résolu.
* La valeur vérifiée d&#39;un module sélectionné pour un cours en double peut ne pas apparaître instantanément. Il s&#39;affiche uniquement en double lorsque la page est actualisée. Ce problème a été résolu.
* Tous les modules seront affichés comme désélectionnés en mode édition après la publication d&#39;un cours. La page doit être actualisée pour afficher les modifications. Ce problème a été résolu.
* La sélection d&#39;un module obligatoire peut avoir été disponible pour un cours commandé alors qu&#39;elle n&#39;aurait pas dû l&#39;être. Ce problème a été résolu.
* Un module obligatoire continue d&#39;apparaître dans la case à cocher de la liste déroulante même après l&#39;avoir supprimé lors de la modification du cours. Ce problème a été résolu.
* Les modules de préparation et de test peuvent être marqués comme obligatoires par défaut. Ce problème a été résolu.
* Lorsque vous cliquez sur le lien de retour d’informations L3 dans votre e-mail, le modèle de retour d’informations peut ne pas s’ouvrir. Ce problème a été résolu.
* La certification est manquante dans le menu déroulant du rapport du tableau de bord bien qu’elle soit visible dans l’application du gestionnaire et dans la liste de l’API de données. Ce problème a été résolu.
* Certains objets d&#39;apprentissage n&#39;ont pas pu être retirés par l&#39;administrateur en raison d&#39;un manque d&#39;autorisations, bien que les catalogues partagés soient indépendants des comptes Learning Manager. Ce problème a été résolu.

+++

+++Mise à jour 42

Mise à jour 42

Date de publication : 11 janvier 2019.

* L’insertion de notifications utilisateur peut échouer de manière aléatoire, ce qui entraîne la non-remise des e-mails associés. Ce problème a été résolu.
* `If a Learner is enrolled in Learning Program 1 and a Course in Learning Program 2, when the Learning Transcript is downloaded for a user group or more than one individual, the Learning Transcript may have missing data. This issue is fixed.`

+++

+++Mise à jour 41

Mise à jour 41Date de publication : 1er décembre 2018.

* Les administrateurs peuvent contrôler l’autorisation donnée aux élèves d’afficher les scores du quiz dans leurs relevés de notes. Cette option peut être activée/désactivée à partir de la page Paramètres.
* L’insertion de notifications utilisateur peut échouer de manière aléatoire, ce qui entraîne la non-remise des e-mails associés. Ce problème a été résolu.
* Les données du temps d&#39;apprentissage passé peuvent ne pas apparaître dans le relevé de notes des élèves et les rapports du tableau de bord. Ce problème a été résolu.
* Les informations sur les activités telles que l&#39;inscription/l&#39;achèvement peuvent ne pas figurer dans le relevé de notes de l&#39;élève téléchargé par un responsable. Ce problème est résolu.
* Les modules qui font partie d&#39;un cours en cours peuvent apparaître comme terminés dans le relevé de notes de l&#39;élève. Ce problème a été résolu.
* Le relevé de notes de l’élève peut ne pas afficher les données téléchargées dans la période sélectionnée. Ce problème a été résolu.
* Pour les utilisateurs auxquels seul le rôle d’auteur est attribué, les catalogues peuvent ne pas s’afficher. Ce problème a été résolu.
* Lorsqu&#39;un administrateur de rôle personnalisé télécharge le relevé de notes de l&#39;élève, le rapport téléchargé ne contient pas d&#39;informations sur les objets d&#39;apprentissage qui faisaient partie des catalogues par défaut uniquement. Ce problème a été résolu.
* Il peut y avoir une incompatibilité entre le nombre total d’utilisateurs et la liste d’utilisateurs dans la page Groupe d’utilisateurs. Ce problème est résolu.
* La fenêtre contextuelle Programme d’apprentissage peut ne pas s’afficher même lorsqu’elle est activée et les utilisateurs peuvent être redirigés vers la page Objets d’apprentissage. Ce problème a été résolu.
* Lorsque la liste d’attente est effacée et que les élèves sont inscrits à un cours, l’administrateur peut recevoir une notification par e-mail avec son nom mentionné au lieu du nom de l’élève. Ce problème a été résolu.
* Le nom peut ne pas apparaître sur l’interface utilisateur pour un utilisateur ajouté via l’API utilisateur du POST. Ce problème a été résolu.

+++

+++Mise à jour 40

Mise à jour 40

Date de publication : septembre 2018.

Amélioration des performances

* Les utilisateurs peuvent rencontrer des problèmes d’expiration lors du téléchargement de grands ensembles de relevés de notes d’élèves. Ce problème a été résolu.
* Les utilisateurs peuvent rencontrer des retards lors du téléchargement d’un ensemble important de rapports d’inscription où le score du quiz de l’élève est enregistré. Ce problème a été résolu.
* Le téléchargement d&#39;un grand ensemble de rapports de score du quiz peut prendre plus de temps que d&#39;habitude. Ce problème est résolu.
* Lorsque l&#39;élève termine un programme d&#39;apprentissage, le formulaire de retour d&#39;informations L1 peut ne pas s&#39;afficher automatiquement, même si la fenêtre contextuelle automatique est activée par l&#39;administrateur. Ce problème a été résolu.
* Dans les rapports téléchargés de la piste d’audit d’utilisateur et de la piste d’audit de contenu, les colonnes modifiées par nom d’utilisateur et modifiées par e-mail d’utilisateur peuvent ne pas être enregistrées. Le rapport indique Système dans de tels cas. Cette information a été mise à jour pour être marquée comme Inconnue.

+++

+++Mise à jour 39

Date de publication : 19 mai 2018.

* Cette version d’Adobe Learning Manager propose de nouvelles fonctionnalités et des améliorations. Elle vous permet de créer des rôles personnalisés, d&#39;ajouter des étiquettes de catalogue, de purger les utilisateurs, de gérer les balises, de renommer les objets d&#39;apprentissage, d&#39;intégrer des Slack, de nouvelles intégrations de connecteurs, de prendre en charge xAPI, et bien plus encore. Pour plus d&#39;informations sur les nouvelles fonctionnalités et améliorations, voir  [Résumé de la nouvelle fonctionnalité](../whats-new.md#main-pars_text).

* Learning Manager est conforme au RGPD. Pour plus d’informations, voir [Conformité de Learning Manager au RGPD](/help/migrated/kb/prime-gdpr.md).

## Problème connu {#knownissue}

* Le lien hypertexte vers le nombre de cours et de certifications dans le modèle de balises inclut les cours fantômes et les certifications récurrentes. Lorsque vous cliquez sur l’hyperlien, ces cours et certifications peuvent ne pas être répertoriés, ce qui entraîne une différence de nombre.

+++

+++Mise à jour 38

* Les élèves à l&#39;état En attente ou En attente d&#39;acceptation étaient marqués comme terminés. Ce problème a été résolu.
* Lorsqu&#39;un instructeur recherche et sélectionne tous les élèves, le nombre d&#39;élèves sélectionnés et le nombre affiché sont différents. Ce problème a été résolu.
* Lorsque vous recherchez et sélectionnez un élève et marquez qu’il est présent, Learning Manager peut marquer que tous les élèves sont présents. Ce problème est résolu.
* Learning Manager affichait l’heure au format 24 heures dans les e-mails. Ce problème a été résolu. L’heure s’affiche désormais au format 12 heures.
* Lorsqu&#39;un responsable désigne un élève pour un cours à l&#39;aide du bouton Désigner disponible dans la page des notifications, le modèle Désigner ne se charge pas. Ce problème a été résolu.
* Dans les rapports Excel exportés, la date d’échéance, qui doit être la date d’inscription + jours pour terminer la valeur définie dans l’instance automatique des objets d’apprentissage, s’affichait de manière incorrecte. Ce problème a été résolu.

* Les résultats de la recherche utilisateur sont vides lorsqu&#39;aucun utilisateur n&#39;est présent dans le groupe qui est recherché. Ce problème est maintenant résolu.
* Les responsables n’ont pas pu être supprimés même s’il n’y a pas de rapports directs. Ce problème a été résolu. Les responsables peuvent désormais être supprimés.
* La fonctionnalité de réinitialisation de la progression du module peut cesser de fonctionner. Ce problème est maintenant résolu.
* La certification supprimée peut apparaître dans le widget pour les élèves. Ce problème a été résolu.
* Le problème de calcul de l&#39;efficacité du cours a été résolu.

* Le problème d’intégration du nouveau compte de connexion a été résolu.
* La fenêtre contextuelle automatique Retour d&#39;informations L1 peut ne pas apparaître si elle est activée dans des instances autres que celles par défaut. Le problème a été résolu.
* Il se peut que l’instructeur ne puisse pas marquer la présence de tous les utilisateurs en une seule fois pour les sessions qui font partie du programme d’apprentissage/de la certification. Ce problème est résolu.

+++

+++Mise à jour 37

Date de publication : 25 mars 2018

La version de mars 2018 d’Adobe Learning Manager propose de nouvelles fonctionnalités et améliorations intéressantes. Il vous permet de générer des rapports de piste d’audit d’utilisateur et des rapports de connexion/accès, et donne aux élèves la capacité de choisir des instances de cours, des améliorations aux salles de classe et aux classes virtuelles, et bien plus encore. Cette version vous apporte également des correctifs de bogues et des améliorations de performances.

Pour prendre connaissance de toutes les nouveautés de cette version, voir  [Nouveautés d’Adobe Learning Manager](../whats-new.md).

### Problème connu {#KnownIssue-1}

**Problème :** L’accès à quelques objets d’apprentissage spécifiques à l’aide d’Internet Explorer v11.1478.10586.0 peut entraîner le blocage de Learning Manager.

**Solution :** Mettez à jour votre navigateur Internet Explorer 11 vers la dernière version en contactant l’équipe informatique de votre organisation.

+++

+++Mise à jour 36

Date de publication : 22 janvier 2018.

### Problèmes résolus {#issuesfixed}

* Toute modification apportée au paramètre du modèle d’e-mail peut entraîner la disparition de la bannière d’e-mail. Ce problème a été résolu.
* Les élèves peuvent ne pas être en mesure d&#39;ajouter/de lancer des assistances à la tâche privées. Ce problème est résolu.
* Les groupes d’utilisateurs personnalisés présents dans un compte peuvent ne pas être répertoriés sous le champ Groupe d’utilisateurs dans le modèle d’ajout/de modification de rapport. Ce problème a été résolu.
* Si le nom d’une image de badge comporte un espace, il se peut qu’elle n’apparaisse pas à l’élève dans la page d’accueil.
* Lorsqu&#39;un utilisateur inscrit est supprimé d&#39;un cours, le rapport de cours et le rapport de quiz peuvent ne pas être générés pour ce cours particulier. Ce problème a été résolu.
* Si l’administrateur modifie le nombre de sièges nommés pour un responsable, le nombre peut apparaître comme incorrect dans la demande de nomination lorsqu’elle est ouverte à partir de différents endroits. Ce problème a été résolu.
* Lors de la conversion d&#39;un utilisateur externe en utilisateur interne, il se peut que l&#39;utilisateur ne soit pas ajouté au groupe Tous les élèves internes. Ce problème a été résolu.
* Si vous recherchez un élève, sélectionnez-le et effectuez l&#39;action de désinscription, cela peut entraîner la désinscription de tous les élèves de ce groupe au lieu de celle de l&#39;élève sélectionné. Ce problème a été résolu.
* En tant qu’administrateur, vous pouvez ne pas être en mesure d’utiliser la case à cocher pour sélectionner un élève dans les certifications. Ce problème a été résolu.
* La création et la mise à jour de groupes d’utilisateurs de plus de 600 utilisateurs individuels peuvent échouer. Ce problème a été résolu. Vous pouvez désormais créer des groupes d’utilisateurs avec plus de 600 utilisateurs individuels.
* Si vous supprimez un groupe d&#39;utilisateurs personnalisé qui fait partie d&#39;un autre groupe d&#39;utilisateurs personnalisé, la règle d&#39;intersection peut déplacer le numéro d&#39;utilisateur vers le groupe supérieur. Ce problème a été résolu.
* Lorsque le catalogue par défaut est désactivé et qu&#39;un nouveau catalogue est créé, et si le responsable a accès à ce catalogue nouvellement créé, il peut ne pas être en mesure de rechercher des cours dans ce catalogue. Ce problème a été résolu.
* Les utilisateurs d&#39;applications mobiles peuvent ne pas recevoir de commentaires L1 sous forme de notifications push. Ce problème a été résolu.

+++

+++Mise à jour 35

Date de publication : 7 janvier 2018.

Cette version de Learning Manager vous apporte des optimisations de performances visant à améliorer l’évolutivité, les performances et la sécurité.

### Améliorations {#enhancements}

* Découvrez la recherche élastique lors de la recherche de cours et d’utilisateurs dans toutes les applications. Cela inclut la recherche de cours, d&#39;utilisateurs et de groupes d&#39;utilisateurs.
* Prendre en charge l’utilisation du connecteur Box pour intégrer Learning Manager à des systèmes externes afin d’automatiser la synchronisation des données. Pour plus d’informations, voir [Connecteur Box](../integration-admin/feature-summary/connectors.md#main-pars_header_302653946).
* Spécifications CSV mises à jour que vous pouvez utiliser pour mapper vos données de migration LMS existantes. Utilisez les dernières spécifications csv téléchargeables et les fichiers zip d’exemple csv pour comprendre le format prescrit des données à saisir. Pour plus d’informations, voir [Manuel de migration.](../integration-admin/feature-summary/migration-manual.md)

+++

+++Mise à jour 34

### Problèmes résolus {#IssuesFixed-1}

* Les annonces peuvent échouer lorsque le nombre d&#39;utilisateurs est élevé. Ce problème est résolu.
* L’accès au compte Learning Manager à l’aide de l’URL de sous-domaine en UE peut rediriger les utilisateurs vers une autre page. Ce problème est résolu.
* Lorsqu&#39;un programme d&#39;apprentissage est commandé, un élève ne doit pouvoir utiliser ce programme que dans l&#39;ordre spécifié. Les élèves pouvaient utiliser des cours qui n&#39;étaient pas répertoriés en premier en utilisant les hyperliens du cours. Ce problème a été résolu. Les élèves ne peuvent plus commencer un cours tant qu&#39;ils n&#39;ont pas terminé le précédent.

* Le message d’erreur de version de navigateur non prise en charge peut ne pas s’afficher dans les versions non prises en charge d’Internet Explorer ( IE 7, IE 8, IE 9 et IE 10) et de Safari ( versions 7, 8 et 9). Ce problème a été résolu.



+++

+++Mise à jour 33

Date de publication : 5 octobre 2017.

### Problèmes résolus {#IssuesFixed-2}

* Les modifications apportées à un cours partagé peuvent ne pas être propagées au compte partagé si l&#39;auteur du compte d&#39;origine enregistre automatiquement le cours. Ce problème a été résolu.
* Parfois, pour des projets Learning Manager spécifiques, le contenu était utilisé pour se figer dans le lecteur Fluidic. Ce problème a été résolu.

* La liste de calendriers dans le widget Calendrier d&#39;apprentissage du tableau de bord peut apparaître dans un ordre aléatoire. Ce problème a été résolu. La liste s’affiche désormais de manière ordonnée.
* Lorsque vous marquez l’assiduité à l’aide de l’option Tout sélectionner, les élèves sont marqués comme participants sur les objets d’apprentissage pour la même session. Ce problème a été résolu.
* Dans certains écrans haute résolution, l’e-mail reçu de Learning Manager a rencontré des problèmes d’alignement et de coupure pour le texte et l’image de la bannière. Ce problème a été résolu.
* Certains courriers électroniques de Learning Manager, tels que les courriers électroniques sans aucune donnée de notification, n’étaient pas déclenchés pour les utilisateurs. Exemple : e-mail reçu lors de la création et de l’activation du profil externe et e-mail reçu lors de la configuration du compte Connect. Ce problème a été résolu.
* Lorsque vous créez un programme d&#39;apprentissage, définissez un rappel, inscrivez des utilisateurs, puis modifiez l&#39;échéance de l&#39;instance, l&#39;échéance modifiée peut ne pas être reflétée pour les rappels. Ce problème est résolu. Les rappels comportent désormais la nouvelle échéance.
* Dans certains cas, pour le contenu créé à l’aide d’Adobe Presenter, le total et le temps écoulé dans le lecteur Fluidic n’étaient pas synchronisés avec le contenu. Ce problème a été résolu.
* Dans certains cas, après l’ajout d’un programme d’apprentissage à un catalogue, l’option d’ajout peut toujours être activée. Ce problème a été résolu.
* L’ouverture de Learning Manager dans un navigateur d’appareil affiche une option permettant de tester Learning Manager sur l’application de l’appareil. Cliquez sur Oui pour lancer le Play Store (Android) si l’application n’est pas installée, ou l’application si elle est installée (sous Android et iOS). Ce workflow a rencontré des problèmes et a été résolu.

+++

+++Mise à jour 32

Date de publication : 17 août 2017

### Problèmes résolus {#IssuesFixed-3}

**Cours avec plusieurs versions de module restaurées vers la version précédente lors d&#39;une action de suppression.**

Lorsqu&#39;un cours avait plusieurs entrées de version de module pour des modules spécifiques, lors de la suppression du module, il retournait à la version précédente et n&#39;était pas supprimé complètement. Ce problème a été résolu.

**Les modifications apportées à un cours partagé ne sont pas propagées si le cours est enregistré automatiquement lors du déplacement entre les onglets.**

Les modifications apportées à un cours partagé peuvent ne pas être propagées au compte client si l&#39;auteur du compte parent enregistre automatiquement le cours en passant à l&#39;onglet suivant. Ce problème a été résolu.

**Les utilisateurs ne pouvaient pas modifier l&#39;échéance des instances pour un cours d&#39;une seule activité.**

Les utilisateurs ne pouvaient pas modifier la date d&#39;échéance d&#39;une instance dans les cours d&#39;activité, car elle revenait à la date d&#39;échéance précédente. Ce problème a été résolu.

**Impossible d’utiliser un ID unique une fois supprimé d’un objet d’apprentissage.**

Lorsque vous affectiez un ID unique à un cours et que vous le supprimiez, vous ne pouviez plus utiliser à nouveau l&#39;ID. Ce problème a été résolu.

**Un programme d&#39;apprentissage qui faisait déjà l&#39;objet d&#39;une inscription dans un événement de plan d&#39;apprentissage pouvait apparaître à nouveau dans le cadre d&#39;un autre événement dans l&#39;application Élève.**

Si un programme d&#39;apprentissage est déjà inscrit dans le cadre d&#39;un événement de plan d&#39;apprentissage, il peut apparaître à nouveau dans le cadre d&#39;un autre événement dans l&#39;application Élève. Ce problème a été résolu.

**Courriers électroniques de rappel envoyés à l’élève avec un délai/une heure de session incorrects.**

Les élèves recevaient souvent des courriers électroniques avec des rappels d’échéance/d’heure de session incorrects en raison de corrections de fuseau horaire. Ce problème a été résolu.

**Le montage chronologique du tableau des scores de ludification affiche des élèves externes s&#39;il est converti d&#39;un élève externe en élève interne.**

Le montage chronologique du tableau des scores de ludification d&#39;un élève interne peut afficher un élève externe lorsqu&#39;il est converti d&#39;un élève externe en élève interne. Ce problème a été résolu.

**Le champ UUID d&#39;un élève est affiché dans un format modifiable lors de la création d&#39;utilisateurs uniques et CSV dans un compte UUID.**

Le champ UUID était affiché à l’élève lors du remplissage de son profil même lorsque l’administrateur avait fourni l’UUID pour les utilisateurs uniques et CSV. Ce problème a été résolu.

**Dans certains cas, le temps d’apprentissage passé n’est pas capturé dans les rapports.**

Les données du temps d&#39;apprentissage passé ne s&#39;affichaient pas dans les rapports d&#39;un élève,

* Si sa présence est marquée automatiquement par le système pour les modules de connexion.
* Lorsqu&#39;un code QR est scanné pour les modules CR et VC à l&#39;aide de l&#39;application pour appareil Learning Manager.

**Cette version de Learning Manager a également introduit des améliorations et des correctifs de bogues liés au lecteur de périphérique.**

* Problèmes liés à l’achèvement des modules d’activité. Ce problème a été résolu.
* Lorsque l’élève lit une vidéo en mode portrait, les boutons +10 et -10 peuvent ne pas fonctionner. Ce problème a été résolu
* Amélioration de l’expérience de lecture de certains exemples de projets lors de la lecture sur un appareil Android (mobile et tablette) qui auparavant scintillait.
* Lorsque vous ajoutez une nouvelle note, le panneau Notes doit se fermer et la lecture doit reprendre dans le lecteur. Cela pourrait ne pas se produire dans certains cas. Ce problème a été résolu.
* Lorsque vous ouvrez les notes ajoutées à un module, le bouton de fermeture peut ne pas s&#39;afficher. Ce problème a été résolu.
* Lorsque l&#39;élève ouvrait le panneau des notes à l&#39;aide du marqueur de note, il devait peut-être cliquer deux fois sur l&#39;icône Notes pour fermer le panneau.
* Lorsque vous cliquez sur la table des matières, elle peut ne pas se réduire automatiquement et nécessite une fermeture manuelle pour afficher le contenu. Ce problème a été résolu.
* Un cours comportant un module en plusieurs langues peut ne pas afficher toutes les langues disponibles, car la barre de défilement peut ne pas être mise à l&#39;échelle en conséquence. Ce problème a été résolu.
* Lorsque vous ouvrez un module de cours d’activité tiers dans un lecteur en mode paysage, l’orientation du texte peut ne pas s’ajuster, ce qui rend le défilement difficile. Ce problème a été résolu.
* Augmentation de la zone de frappe du bouton de fermeture du lecteur en mode en ligne et hors ligne.
* La table des matières ne se ferme pas automatiquement lorsque l’orientation du périphérique est modifiée. Ce problème a été résolu.
* Certains problèmes mineurs liés à l’interface utilisateur, tels que l’alignement du bouton de lecture, du bouton radio et d’autres paramètres en mode paysage et portrait, ont été résolus.

* Le problème d’affichage de la barre de recherche même lorsque l’option Afficher la commande de lecture n’est pas cochée dans le contenu a été résolu.
* Le bouton de fermeture du lecteur n’était pas visible pour certains projets lorsque l’orientation de l’appareil était modifiée. Ce problème a été résolu.
* Le problème concernant la troncature de la section de table des matières du module en mode paysage sur le lecteur d&#39;appareil a été résolu. Dans certains cas, la table des matières n’était pas visible pour le contenu dans le lecteur d’appareil. Cette situation a également été corrigée.

**Cette version de Learning Manager contient également des améliorations et des correctifs répertoriés ci-dessous pour l’application pour appareil**.

* La notification push liée aux délais d&#39;achèvement peut ne pas être remise sur certains appareils. Ce problème a été résolu.
* Nous prenons désormais également en charge le cycle de vie des objets d’apprentissage sur les applications pour appareil. Les élèves peuvent désormais accéder au contenu le plus récent des objets d&#39;apprentissage s&#39;ils ont été modifiés par l&#39;auteur.

* Les problèmes d’orientation (y compris l’orientation par défaut en mode portrait) de l’application Learning Manager ont été résolus.
* Il se peut qu’il n’existe pas d’option de mise à jour du contenu lorsque l’utilisateur passe du mode hors ligne au mode en ligne.
* La commande de modules est désormais prise en charge pour les cours dans l’application pour appareil en mode en ligne.

* Si un utilisateur n&#39;a téléchargé aucune assistance à la tâche, le fait de cliquer sur l&#39;onglet Mes assistances à la tâche en mode hors ligne peut bloquer l&#39;application dans IOS et afficher un message indiquant une erreur de chargement des données dans Android. Ce problème a été résolu.
* L’application Learning Manager se ferme ou affiche une erreur si nous accédons au cours immédiatement après la déconnexion d’Internet, même s’il s’agit d’un cours téléchargé. Ce problème a été résolu.
* Parfois, lorsque vous scannez le code QR, une image capturée du code QR scanné précédemment s’affiche. Cela a été corrigé.
* Parfois, la tentative de suppression d&#39;une assistance à la tâche déjà ajoutée à partir de l&#39;onglet Assistances à la tâche affichait un message d&#39;erreur. Ce problème a été résolu.

+++

+++Mise à jour 31

Date de publication : 16 juillet 2017

### Améliorations {#Enhancements-1}

**Ludification**

Cette version améliore la portée de la ludification. Les utilisateurs externes peuvent désormais participer à la ludification. En tant qu’administrateur, vous pouvez définir l’étendue de la ludification en modifiant les paramètres de l’étendue. Vous pouvez activer de manière sélective la ludification parmi des utilisateurs, des groupes ou des emplacements de profil similaires.

**Améliorations concernant les utilisateurs externes**

Grâce à cette amélioration, vous pouvez définir une plage temporelle au terme de laquelle les utilisateurs sont automatiquement supprimés après la période d’inactivité. L&#39;amélioration permet également à l&#39;administrateur d&#39;ajouter à nouveau l&#39;utilisateur en tant qu&#39;élève externe pour les élèves supprimés automatiquement et manuellement.

**Assistance à la tâche, annonces et rapport de désinscription**

Les assistances à la tâche sont du contenu de formation auquel un élève peut accéder sans s&#39;inscrire à un objet d&#39;apprentissage spécifique comme un cours ou un programme d&#39;apprentissage. Grâce à cette amélioration, les administrateurs peuvent extraire et télécharger le rapport Assistances à la tâche. En tant qu&#39;administrateur, vous pouvez également générer un rapport de toutes les annonces que vous avez envoyées. Les administrateurs et les responsables peuvent également extraire un rapport des élèves qui ont été désinscrits.

**Connecteurs Learning Manager**

Vous pouvez désormais exporter des compétences d’utilisateur vers un emplacement FTP à des fins d’intégration avec un système tiers à l’aide de l’option Exportation de données. Vous pouvez spécifier le Nom de connexion pour votre intégration et choisir si vous souhaitez importer les utilisateurs internes ou exporter les compétences des utilisateurs en les configurant ou en les récupérant sur demande.

**Copier des instances de cours**

Vous pouvez maintenant copier l&#39;URL d&#39;instance en cliquant sur la flèche déroulante dans le coin supérieur droit d&#39;une instance.

### Problèmes résolus {#IssuesFixed-4}

**Les utilisateurs ne reçoivent pas d&#39;invitation de calendrier lorsqu&#39;ils sont inscrits au programme d&#39;apprentissage**

Parfois, les utilisateurs ne recevaient pas de fichier d&#39;invitation au calendrier (.ics) lorsqu&#39;ils s&#39;inscrivaient à des programmes d&#39;apprentissage, à des classes avec certificats et à des sessions Connect. Ce problème a été résolu. Les utilisateurs reçoivent désormais les fichiers .ics sous forme de pièces jointes qui mentionnent les détails de la session ainsi que l’e-mail d’inscription.

**La description de l’activité, même si elle était fournie en plusieurs langues, s’affichait toujours en anglais**

Un utilisateur dont la préférence de langue du contenu est définie sur une langue autre que l’anglais pourra toujours voir la description du module d’activité en anglais. Ce problème a été résolu.

+++

+++Mise à jour 30

Date de publication : 30 juin 2017

### Améliorations {#Enhancements-2}

**Prise en charge de plusieurs objets d’apprentissage dans le plan d’apprentissage**

En tant qu&#39;administrateur ou auteur, vous pouvez désormais affecter plusieurs objets d&#39;apprentissage à un plan d&#39;apprentissage. Si une instance de l&#39;objet d&#39;apprentissage est retirée ou expire, l&#39;ensemble du plan d&#39;apprentissage est désactivé automatiquement. Grâce à cette amélioration, vous pouvez également effectuer une recherche **[!UICONTROL Formation terminée]** et **[!UICONTROL Attribuer l’apprentissage]** champs utilisant des ID uniques d&#39;objets d&#39;apprentissage.

**Accessibilité**

Avec cette mise à jour, l’expérience de l’élève Learning Manager prend désormais en charge la section 508 Norme d’accessibilité. Learning Manager est également compatible avec la dernière version de **[!UICONTROL MÂCHOIRES]**. Cette fonctionnalité n’est prise en charge que pour l’application de l’élève. Utilisez Internet Explorer 11, Windows Chrome ou macOS Safari pour accéder à cette fonctionnalité.

### Problèmes résolus {#IssuesFixed-5}

**Informations incorrectes dans certains fuseaux horaires**

Les rappels d&#39;échéance mentionnaient de manière incorrecte le nombre de jours restants pour les élèves dans certains fuseaux horaires. Ce problème a été résolu.

**Problèmes liés au programme d’apprentissage dans le cas d’une instance expirée du programme**

Le lancement des modules à partir du programme d&#39;apprentissage a rencontré des problèmes si l&#39;instance du programme a expiré. Cela a entraîné l’extension du module qui ne fonctionnait pas et les élèves ne pouvaient pas lancer le lecteur et consulter le contenu. Ce problème a été résolu.

**Problèmes de traduction dans l’application de l’élève**

Les utilisateurs de Learning Manager ont rencontré certains problèmes de traduction dans l’application de l’élève. Ces problèmes ont été résolus.

**Problèmes liés à l’abonnement à une compétence**

Dans certains cas, les élèves n’ont pas pu s’abonner à une nouvelle compétence. Ce problème a été résolu.

+++

+++Mise à jour 29

Date de publication : 9 avril 2017

### Nouvelles fonctionnalités {#newfeatures}

Pour obtenir une liste des nouvelles fonctionnalités et améliorations effectuées dans la version d&#39;avril de Learning Manager, consultez [Nouveautés.](../whats-new.md)

**Application d’élève basée sur un widget**

Utilisez des widgets sur la page d’accueil pour gérer vos cours, compétences et réussites. Utilisez la barre de recherche pour effectuer une recherche dans l’ensemble de votre système de gestion de l’apprentissage qui couvre tous les objets d’apprentissage, catalogues, compétences, notes et discussions

Pour plus d’informations sur la nouvelle page d’accueil, voir  [Page d’accueil de l’élève dans Learning Manager](../learners/feature-summary/getting-started-learner.md).

**Paramètres administrateur pour le tableau de bord des élèves**

En tant qu’administrateur, vous pouvez contrôler la page d’accueil des élèves en activant ou désactivant différents widgets.

**Application mobile Learning Manager pour les élèves**

La nouvelle application mobile Learning Manager permet aux élèves de s’inscrire et de suivre des cours. L’application peut également être utilisée pour gérer les tableaux de bord.

Pour en savoir plus sur l&#39;utilisation de Learning Manager sur les appareils mobiles, voir  [Application des élèves Learning Manager pour appareils mobiles](../learners/feature-summary/ipad-android-tablet-users.md#main-pars_header_1451175907).

**Indication de l’assiduité à l’aide du code QR**

Utilisez le code QR Scan pour marquer votre présence aux sessions de classe à l’aide de vos appareils mobiles.

**Rôle d’instructeur**

Learning Manager introduit désormais des instructeurs pour les modules. Les instructeurs peuvent gérer les sessions de module, y compris l’heure, le lieu et la limite de places pour les modules qui leur sont attribués.

Pour afficher des informations détaillées sur les instructeurs, voir  [Instructeurs dans Learning Manager](../instructors/feature-summary/getting-started.md#main-pars_header).

**Compte de pairs**

Si vous êtes administrateur, vous pouvez créer des comptes de pairs avec lesquels vous pouvez partager les places que vous avez achetées.

Pour savoir comment créer et gérer des comptes de pairs, voir  [Comptes de pairs](../administrators/feature-summary/peer-account.md#main-pars_text).

**Offres d’équivalence de cours**

Utilisation **[!UICONTROL Ajouter une nouvelle langue]** lorsque vous ajoutez un module ou un cours pour le rendre disponible dans plusieurs langues et sous plusieurs formats.

**Relevé de notes de l’élève**

Learning Manager permet aux responsables et administrateurs de télécharger les données des relevés de notes afin d’effectuer le suivi de l’historique de l’apprentissage des personnes et des équipes.

**Intégration avec d’autres fournisseurs de contenu**

Learning Manager a introduit trois nouveaux connecteurs dans cette version, afin que les élèves puissent accéder aux cours des fournisseurs de contenu suivants et les suivre : Lynda.com, getAbstract et Harvard ManageMentor.

Pour savoir comment configurer et utiliser chacun de ces connecteurs, voir  [Connecteurs](../integration-admin/feature-summary/connectors.md#main-pars_header).

**ID unique pour les objets d’apprentissage**

Lors de la création d&#39;objets d&#39;apprentissage, les auteurs et les administrateurs peuvent désormais spécifier des ID uniques pour les cours, les programmes d&#39;apprentissage ou les certifications. Si vous souhaitez activer l’ID unique lors de la création d’un objet d’apprentissage, cliquez sur Paramètres > Général. Cochez la case Activer en regard de l’option ID uniques d’objets d’apprentissage.

**Forum de discussion pour les élèves**

Utilisez le forum de discussion dans les cours pour interagir avec vos pairs et les instructeurs. En tant qu’élève, vous pouvez afficher toutes les publications des cours. Cependant, vous ne pouvez également supprimer que les publications que vous avez saisies. Pour plus d&#39;informations sur le forum de discussion, voir  [Affichage et participation aux discussions](../learners/feature-summary/courses.md#main-pars_header_1772461149).

### Améliorations {#Enhancements-3}

**X cours sur Y**

Les critères d&#39;achèvement des objets d&#39;apprentissage tels que les cours, les certifications et les plans d&#39;apprentissage peuvent être définis de telle sorte que les élèves n&#39;aient besoin de terminer que X modules ou cours sur Y. Les auteurs peuvent également définir les critères d&#39;achèvement pour les certifications et les plans d&#39;apprentissage.

Pour plus d’informations sur cette fonctionnalité, voir  [Critères d’achèvement du cours](../learners/feature-summary/courses.md#main-pars_image_1164377098).

**Modération du cours**

Les administrateurs reçoivent désormais des notifications chaque fois qu&#39;un auteur modifie ou met à jour des modules et publie à nouveau un cours.

**Paramètres administrateur pour la réinitialisation des modules**

Les administrateurs peuvent désormais configurer l’option Réinitialiser le module pour permettre aux élèves de réinitialiser un cours auquel ils ont échoué ou qu’ils n’ont pas terminé.

**Catalogue de rapports**

Lorsque vous créez des rapports dans Learning Manager, vous pouvez désormais générer des rapports et des graphiques pour les catalogues.

**Améliorations du plan d’apprentissage**

Les administrateurs peuvent désormais créer des plans d&#39;apprentissage de types À la date. Avec le plan d&#39;apprentissage À la date, un administrateur peut spécifier le nom de l&#39;événement, choisir la date de l&#39;événement et sélectionner le groupe d&#39;utilisateurs auquel l&#39;événement appartient.

**Messages d’inscription spécifiques au cours**

Les administrateurs peuvent désormais configurer et envoyer aux élèves des messages d&#39;inscription spécifiques au cours par courrier électronique.

**Annonces pense-bêtes**

En tant qu&#39;administrateur, vous pouvez désormais activer la fonction Pense-bête pour les annonces.

**Prise en charge de l’URL dans les annonces**

Vous pouvez ajouter des URL en tant qu&#39;annonces en les ajoutant dans le HTML.

**Ajouter de nouveaux types de livraison (cours)**

Adobe Learning Manager vous permet désormais d’ajouter des types de livraison pour vos cours.

**Améliorations du rôle d’auteur**

Auparavant, les auteurs ne pouvaient créer que des modules et des cours. Désormais, les auteurs ont également la possibilité de créer des certifications et des programmes d’apprentissage pour les élèves.

**Rôle d’auteur pour les utilisateurs externes**

En tant qu’administrateur, vous pouvez désormais attribuer des rôles d’auteur aux utilisateurs externes.

**Auteurs multiples**

Learning Manager permet désormais à plusieurs auteurs de modifier simultanément le même groupe de contenus.

**Améliorations d’Adobe Connect**

Vous pouvez désormais configurer une seule URL Adobe Connect avec plusieurs comptes Learning Manager.

**Prise en charge de nouvelles langues**

Cette version inclut la prise en charge du japonais, du portugais brésilien et de l’italien.



+++

+++Mise à jour 28

Date de publication : 30 janvier 2017

### Problèmes résolus {#IssuesFixed-6}

#### Paramètres du compte {#accountsettings}

En tant qu’administrateur, lorsque vous cliquiez sur Profil externe et sélectionniez Actions > Modifier le profil, tous les profils n’étaient pas répertoriés. Ce problème a été résolu.

#### Cycle de vie du cours {#courselifecycle}

* Lorsque vous lanciez un cours créé à l&#39;aide de l&#39;outil d&#39;apprentissage en ligne de la bibliothèque Biz, l&#39;action « Reprendre » ne fonctionnait pas. Ce problème a été résolu.
* Certains utilisateurs n&#39;ont pas pu lancer un cours dans iPad à l&#39;aide du lien de cours dans Annonces. Ce problème est maintenant résolu.
* Lorsque vous cliquiez sur le bouton Continuer dans le programme des élèves, vous ne pouviez pas accéder aux cours dans l&#39;ordre. Ce problème est maintenant résolu.
* L&#39;étiquette Présentation du cours pour les cours du programme de l&#39;élève était auparavant mal placée. Ce problème a été résolu.

#### Application de l’élève {#learnerapp}

* Sur votre appareil, si vous ouvriez une image d&#39;annonce en mode plein écran, vous ne pouviez pas revenir à l&#39;application. Ce problème est maintenant résolu.
* Le contenu Tincan chargé à partir du Captivate n’a pas été lu en mode en ligne dans les systèmes d’exploitation Android et iOS. Ce problème a été résolu.

#### Rapports de cours {#coursereports}

Des rapports de relevé de notes de l’élève incorrects sont générés dans Learning Manager lorsque le cours comporte plusieurs versions de modules. Ce problème est maintenant résolu.

#### Calque d’API {#apilayer}

Vous rencontrez une erreur chaque fois que vous tentez de récupérer les informations de version du module à l&#39;aide de l&#39;API AP/courses/{coursesid}. Ce problème a été résolu.

+++

+++Mise à jour 27

Date de publication : 23 décembre 2016.

### Nouvelles fonctionnalités {#Newfeatures-1}

Adobe permet aux entreprises de migrer leurs données et le contenu de formation depuis leurs systèmes de gestion de l’apprentissage (LMS) vers l’application LMS Learning Manager.

Learning Manager fournit les outils et modèles nécessaires à l’administrateur d’intégration de votre organisation pour installer et effectuer les tâches de migration.

Pour plus d’informations sur la fonctionnalité de migration, consultez  [Aide du manuel de migration](../integration-admin/feature-summary/migration-manual.md)

### Améliorations {#Enhancements-4}

**Inscription d’utilisateur**

En tant qu’administrateur, vous pouvez désormais ajouter des noms de domaine spécifiques lors de l’ajout d’utilisateurs externes. Lorsque les élèves s&#39;inscrivent au compte, ils ne peuvent saisir que les adresses électroniques de ces noms de domaine.

Vous pouvez également envoyer des liens de vérification par e-mail à l’adresse des utilisateurs lorsqu’ils s’inscrivent au compte. Pour plus d&#39;informations sur cette amélioration, voir  [Ajouter des utilisateurs/groupes d’utilisateurs](../administrators/feature-summary/add-users-user-groups.md#main-pars_header_1217981931).

**Lecteur Fluidic**

Le Lecteur Fluidic vous permet désormais de modifier la vitesse de lecture. Vous avez le choix entre cinq variantes de vitesse disponibles. Le Lecteur Fluidic vous permet également de contrôler les paramètres de volume lorsque vous suivez un cours.

En tant qu’élève, vous pouvez également avancer ou reculer de 10 secondes à l’aide des nouvelles icônes situées de chaque côté du bouton de lecture dans le lecteur Fluidic. Pour plus d&#39;informations sur ces améliorations, voir  [Lecteur Fluidic](../learners/feature-summary/fluidic-player.md).

Les améliorations apportées au lecteur Fluidic s’appliquent uniquement à la vidéo.

+++

+++Mise à jour 26

Date de publication : 6 décembre 2016.

### Amélioration {#enhancement}

Dans le cadre de cette mise à jour, Learning Manager fournit un point de terminaison [PATCH/users/{id}](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v1/# !/user/patch_users_id) pour mettre à jour les utilisateurs dans une application. Vous pouvez accéder à ce point de terminaison d’API dans le rôle d’administrateur. À l****aide de ce point de terminaison, vous pouvez mettre à jour les informations suivantes sur les utilisateurs de Learning Manager :

* Nom
* E-mail
* Profil
* Rôle
* Responsable

### Problème résolu {#issuefixed}

**Lecteur Fluidic**

Lorsque vous suivez un cours qui a été développé en Captivate à l’aide de  `code cpQuizInfoStudentName` variable, le nom de l&#39;étudiant ne s&#39;affichait pas comme prévu. Ce problème a été résolu.

+++

+++Mise à jour 25

Date de publication : 17 novembre 2016.

### Améliorations {#Enhancements-5}

**Catalogues partagés**

La fonctionnalité Catalogue partagé permet aux administrateurs de tous les comptes de partager ou d&#39;acquérir des catalogues avec des objets d&#39;apprentissage. En tant qu’extension de cette fonctionnalité de catalogue partagé, nous prenons en charge la propagation des mises à jour des objets d’apprentissage tels que les badges, les compétences, les modules, les cours, les programmes d’apprentissage, les certifications et les assistances à la tâche.

Pour plus d’informations sur cette fonctionnalité, reportez-vous à la section  [Aide sur les catalogues partagés](../administrators/feature-summary/catalogs.md#propagation)

**Retour d&#39;informations L1 et L3**

* La boîte de dialogue de retour d’informations L1 s’affiche dès qu’un élève termine le suivi du cours. En outre, l’élève reçoit une notification lorsque le retour d’informations L1 est terminé.
* Une option permettant d&#39;ajouter des questions descriptives a été fournie dans la fonction de retour d&#39;informations L1 et L3. Les administrateurs peuvent ajouter ces questions descriptives aux élèves. Cette fonctionnalité vient s’ajouter à l’ensemble de questions par défaut fournies par Learning Manager. Vous pouvez ajouter deux questions descriptives pour le retour d&#39;informations L1 et une pour le retour d&#39;informations L3.\
  Pour plus d’informations sur cette fonctionnalité, reportez-vous à la section [Aide sur les questions descriptives de retour d&#39;informations L1 et L3](../administrators/feature-summary/courses.md#descriptive)

**Exportation d’utilisateurs**

* À la demande de certains utilisateurs de grandes entreprises, une nouvelle option permettant de télécharger la liste de tous les utilisateurs du compte Learning Manager est fournie. Dans Connexion administrateur, cliquez sur **[!UICONTROL Utilisateurs]** dans le volet de gauche et cliquez sur **[!UICONTROL Exportation des données utilisateur]** pour télécharger la liste des utilisateurs sous forme de feuille excel.

### Problèmes résolus {#Issuesfixed-1}

**Inscriptions au cours**

* Dans certains cas, lorsqu&#39;un administrateur essayait d&#39;afficher les inscriptions au cours à l&#39;aide de l&#39;onglet élèves, certains noms d&#39;élèves inscrits ne s&#39;affichaient pas. Ce problème a été résolu.

**Ajouter des cours**

* Lors de l&#39;ajout d&#39;une compétence au cours, si un auteur ajoute une compétence qui comporte un espace vide à la fin du nom, une erreur se produisait et le cours n&#39;était pas enregistré. Ce problème a été résolu.

**Suivre des cours**

* Dans un cours ordonné, certains élèves ne pouvaient pas passer d&#39;un module à un autre tout en suivant un cours car les modules n&#39;étaient pas marqués comme terminés. Ce problème a été résolu.
* Dans un cours ordonné, les élèves ne pouvaient pas naviguer entre les modules dans la table des matières en mode normal et de visite. Ce problème a été résolu.

**Lecteur Fluidic**

* Dans certains cas, lorsqu’un utilisateur téléchargeait un contenu de module avec des images/diapositives masquées, la table des matières du volet de gauche affichait les images/diapositives masquées. Ce problème a été résolu.

**Rapports**

* Le temps de chargement des rapports est plus long dans la dernière mise à jour de Learning Manager. Ce problème a été résolu.

+++

+++Mise à jour 24

Date de publication : 12 octobre 2016.

### Améliorations {#Enhancements-6}

**Rapports de cours**

* Pour les comptes Learning Manager UUID (Universal Unique Identifier) activés, l’UUID apparaît dans le rapport d’inscription au cours, les relevés de notes des élèves et les rapports de score du quiz.

### Problèmes résolus {#Issuesfixed-2}

**Assistances à la tâche**

* Dans certains cas, lorsqu&#39;un élève essayait d&#39;accéder à l&#39;onglet Apprentissage > Assistances à la tâche d&#39;apprentissage > Cours, les cours n&#39;étaient pas chargés comme prévu dans l&#39;onglet Apprentissage > Cours. Ce problème a été résolu.

**Ajouter des utilisateurs**

* Dans certains cas, lorsqu’un utilisateur unique est ajouté à l’application Learning Manager, il ne reçoit pas de notification par e-mail. Ce problème a été résolu.
* Les administrateurs ne pouvaient pas télécharger le fichier CSV si le processus de chargement du fichier CSV échouait. Ce problème est résolu : les administrateurs peuvent télécharger le fichier CSV le plus récent même si le processus de chargement du fichier CSV échoue.
* Si un fichier CSV était importé après la modification des informations de l’utilisateur inscrit automatiquement avec des lettres majuscules et minuscules, ces informations ne s’affichaient pas dans l’interface utilisateur de l’administrateur. Ce problème a été résolu.

**Rapports de cours**

* Dans certains cas, les scores du quiz n&#39;apparaissaient pas pour les cours même si les scores apparaissent dans les relevés de notes des élèves. Ce problème a été résolu.

**Rapports d’inscription**

* Dans certains cas, les rapports Excel d&#39;inscription des élèves n&#39;étaient pas téléchargés pour les objets d&#39;apprentissage. Ce problème se produisait lorsque des caractères non ASCII ou spéciaux étaient utilisés dans les noms des objets d&#39;apprentissage. Ce problème a été résolu.

**Connexion utilisateur**

* Lors de la configuration d&#39;un mot de passe lors de l&#39;inscription ou de la réinitialisation, le message d&#39;erreur ne s&#39;affichait pas même si le mot de passe saisi ne respectait pas la stratégie de mot de passe. Ce problème a été résolu.

**Efficacité du cours**

* Dans le rôle d&#39;élève, l&#39;efficacité du cours était affichée comme l&#39;une des **Trier par** filtrer les options même lorsqu’un administrateur a désactivé l’efficacité du cours pour les élèves. Ce problème a été résolu.

**Certifications**

* Lorsqu&#39;un administrateur supprimait des élèves d&#39;une certification récurrente, une erreur se produisait et l&#39;application Learning Manager se bloquait. Ce problème a été résolu.

**Rapports**

* Lorsqu&#39;un administrateur tente de générer un rapport de certification avec **Jusqu’à la date** par défaut, les utilisateurs inactifs n&#39;étaient pas affichés dans le rapport. Ce problème a été résolu.
* Lorsqu&#39;un administrateur cliquait sur le lien Rapports de cours dans l&#39;onglet Rapports > Mes rapports, une boîte de dialogue contextuelle s&#39;affichait sans le bouton Fermer. Ce problème a été résolu.

**Lecteur Fluidic**

* Lors de la prévisualisation des cours en tant qu&#39;administrateur ou auteur, lorsqu&#39;un utilisateur choisit le mode Plein écran dans le lecteur Fluidic, l&#39;écran apparaît vide. Ce problème a été résolu.

**Prise en charge multilingue**

* Les caractères de point d’interrogation s’affichaient auparavant à la place des caractères chinois en réponse aux appels API des utilisateurs. Ce problème a été résolu.

**Calque d’API**

* Une erreur se produisait chaque fois qu’un utilisateur essayait de récupérer l’ID de catalogue par défaut à l’aide de l’API get/catalog/catalogId. Un ID de catalogue par défaut peut être similaire à « 970_default ». Ce problème a été résolu.

**Interface utilisateur**

* Quelques erreurs typographiques mineures ont été corrigées dans l&#39;interface utilisateur de l&#39;application Learning Manager pour le rôle d&#39;élève.

+++

+++Mise à jour 23

Date de publication : 19 septembre 2016.

### Problèmes résolus {#Issuesfixed-3}

**Relevés de notes des élèves**

* Dans certains cas, s&#39;il y avait plus de vingt élèves inactifs/supprimés sur un compte, les élèves inactifs au-delà de vingt n&#39;étaient pas affichés dans la liste déroulante de recherche de la boîte de dialogue de relevé de notes de l&#39;élève. Ce problème a été résolu.
* Si un compte d&#39;utilisateur externe expirait, ses élèves n&#39;étaient pas répertoriés dans le relevé de notes de l&#39;élève généré. Ce problème a été résolu.

**Catalogues**

* Certains clients rencontraient un problème d’affichage des groupes d’utilisateurs dans un catalogue. Même s’il y avait plus de vingt groupes d’utilisateurs dans un catalogue, seuls 20 groupes d’utilisateurs étaient affichés. Nous avons résolu ce problème en affichant 200 groupes d’utilisateurs dans une page.

+++

+++Mise à jour 22

Date de publication : 13 septembre 2016.

Dans cette mise à jour, nous avons résolu certains problèmes principaux d’ingénierie produit afin d’améliorer l’expérience client.

### Problèmes résolus {#Issuesfixed-4}

* Un problème lié à l&#39;exportation des données de module dans les relevés de notes des élèves a entraîné des données d&#39;exportation incorrectes. Ce problème a été résolu.
* Si un utilisateur utilisait une extension d’ID de messagerie de plus de quatre caractères, celle-ci n’était pas prise en charge. Par exemple, si un ID de messagerie est <abcd@company.world> elle n’était pas prise en charge, car l’extension world comportait plus de quatre caractères. Nous l’avons corrigé pour prendre en charge l’extension avec plus de quatre caractères.

+++

+++Mise à jour 21

Date de publication : 1er septembre 2016.

### Améliorations {#Enhancements-7}

**Efficacité du cours**

Les administrateurs peuvent désormais personnaliser la fonctionnalité d&#39;efficacité des cours ou des programmes d&#39;apprentissage pour masquer le score d&#39;efficacité dans la vue des élèves.

**Ajout d’utilisateurs externes**

Learning Manager a augmenté la limite maximale d&#39;auto-inscriptions externes à 5 chiffres.

**Rapports**

Tous les rapports et listes d&#39;élèves téléchargés pour tous les objets d&#39;apprentissage affichent désormais les utilisateurs supprimés avec une délimitation claire.

### Problèmes résolus {#Issuesfixed-5}

**Cycle de vie du cours**

Dans certains cas, lorsqu&#39;un auteur modifiait un cours partagé pour mettre à jour des informations de module modifiées, un message d&#39;avertissement s&#39;affichait indiquant que l&#39;utilisateur ne pouvait pas modifier ces informations car des modifications précédentes étaient en cours de traitement. Ce problème a été résolu.

**Prise en charge multilingue**

Dans certaines fonctionnalités de l&#39;interface utilisateur de Learning Manager, les messages n&#39;étaient pas traduits et ne s&#39;affichaient pas dans des phrases de paramètres régionaux appropriés. Ce problème a été résolu.

**Ajouter des utilisateurs**

* Lorsqu&#39;un utilisateur supprimé était rajouté en tant qu&#39;utilisateur unique, il n&#39;était pas ajouté au groupe d&#39;utilisateurs Tous les utilisateurs par défaut. Ce problème a été résolu.
* Un nombre limité de profils s&#39;affichait dans les boîtes de dialogue de modification de profil d&#39;inscription externe et d&#39;auto-inscription. La pagination est désormais implémentée.

**Assistances à la tâche**

Chaque fois qu&#39;un élève accédait à l&#39;onglet Assistances à la tâche dans le compte de l&#39;élève, un message d&#39;erreur s&#39;affichait comme « Cette assistance à la tâche n&#39;existe plus dans votre liste » avant le chargement du contenu. Ce problème a été résolu.

**Catalogues**

Lors de la création du catalogue, lors de l&#39;ajout de cours en tant que contenu au catalogue, le filtre Trier par ne fonctionnait pas comme prévu. Ce problème a été résolu.

**Paramètres**

Dans les paramètres du compte, lorsqu&#39;un administrateur utilisait un sous-domaine déjà utilisé par un autre compte, aucun message d&#39;erreur ne s&#39;affichait pour l&#39;administrateur. Ce problème a été résolu.

**Calque d’API**

* Lorsque l&#39;option inclure le responsable était utilisée lors de la récupération des utilisateurs, la hiérarchie complète des responsables était récupérée au lieu du responsable immédiat de l&#39;utilisateur. Ce problème a été résolu.
* Lorsqu&#39;un utilisateur avec une autorisation de portée d&#39;élève tentait d&#39;ajouter des utilisateurs, un message d&#39;erreur générique s&#39;affichait. Ce problème a été résolu et un message d’accès non autorisé s’affiche désormais pour l’élève.
* Lorsqu&#39;un utilisateur tentait de supprimer un dernier utilisateur existant dans un groupe d&#39;utilisateurs, un message d&#39;erreur 204 s&#39;affichait pour l&#39;utilisateur. Ce problème est maintenant résolu en affichant un message d’erreur pertinent à l’utilisateur indiquant que le groupe doit avoir au moins un utilisateur.
* L’espace, s’il existe au début du nom, a été coupé lors de l’affichage du nom d’utilisateur dans l’API GET/users. Ce problème est maintenant résolu.
* Les brouillons des cours étaient également renvoyés lorsque l&#39;administrateur essayait de récupérer tous les cours. Ces brouillons sont censés être privés pour l&#39;auteur. Ce problème est résolu, les brouillons des cours ne reviennent pas pour le moment.

**Intégration d’Adobe Connect**

* Dans certains cas de sessions de classe virtuelle basées sur Adobe Connect, la participation n’était pas marquée automatiquement après la session. Ce problème se produisait uniquement lorsqu’un ID de connexion était utilisé par un instructeur pour se connecter au lieu de l’ID de messagerie. C&#39;est maintenant réglé.
* Dans certains cas, le nom de l’instructeur apparaissait plusieurs fois dans la liste déroulante Instructeur lors de la création du module de salle de classe virtuelle basé sur Adobe Connect. Ce problème a été résolu.

+++

+++Mise à jour 20

Date de publication : 22 août 2016.

### Améliorations {#Enhancements-8}

**Calque d’API**

Dans le cadre de cette mise à jour, nous avons ajouté les nouvelles API suivantes pour répondre à certaines des exigences de nos clients :

1. Utilisateurs du POST
1. Utilisateurs du DELETE
1. GET userGroups
1. GET userGroups /{id}
1. userGroups DELETE /{id}/Users
1. userGroups POST /{id}/Users
1. GET /users/userId/userGroups

Nous avons également amélioré le modèle utilisateur existant avec les ajouts suivants :

1. Le modèle du responsable est ajouté en tant que relation au modèle utilisateur
1. userGroupId est ajouté en tant que nouveau paramètre à GetUsers

**Relevé de notes de l’élève**

Lorsqu&#39;un utilisateur générait le relevé de notes d&#39;un élève, la boîte de dialogue contextuelle s&#39;affichait pendant un court instant et disparaissait sans demander à l&#39;utilisateur d&#39;intervenir. Nous avons amélioré l’expérience utilisateur en fournissant une fenêtre contextuelle qui s’interrompt et invite l’utilisateur à cliquer sur OK.

**Intégration d’Adobe Connect**

L’ID de connexion est fourni en tant que nouveau champ facultatif dans les paramètres d’intégration d’Adobe Connect pour les utilisateurs qui n’utilisent pas leur ID de messagerie pour se connecter.

### Problèmes résolus {#Issuesfixed-6}

**Rapports de cours**

* Lorsqu&#39;un module de cours se composait de questions ouvertes ou uniquement de questions d&#39;enquête, un rapport de score du quiz vide s&#39;affichait lorsqu&#39;il était exporté. Ce problème a été résolu.
* Dans certains cas, le rapport de score du quiz n&#39;était pas téléchargé lorsqu&#39;un utilisateur utilisait le lien Exporter le score du quiz. Ce problème a été résolu.

**Création de cours**

La page Paramètres du cours dans le rôle d&#39;auteur n&#39;apparaissait pas chaque fois qu&#39;une compétence associée à ce cours était retirée par l&#39;administrateur. Ce problème a été résolu.

**Inscription intelligente**

Le champ de recherche ne prenait pas en charge les caractères spéciaux comme entrée et, par conséquent, les résultats de la recherche ne s’affichaient pas. Ce problème a été résolu.

+++

+++Mise à jour 19

Date de publication : 11 août 2016.

### Améliorations {#Enhancements-9}

**Inscription intelligente**

Les performances du moteur de recherche ont été améliorées pour fournir des résultats de recherche plus précis aux utilisateurs.

**Intégration d’Adobe Connect**

Le processus de vérification/authentification de la demande d’intégration a été amélioré dans l’application Learning Manager.

### Problèmes résolus {#Issuesfixed-7}

**Ajouter des utilisateurs**

* Lorsque les utilisateurs Learning Manager étaient très nombreux, le chargement de la page des utilisateurs et des groupes d’utilisateurs était ralenti. Ce problème a été résolu.
* Une fois que l’administrateur a terminé le chargement du fichier CSV avec de nouveaux utilisateurs, la liste des utilisateurs de la page n’a pas été mise à jour avec de nouveaux utilisateurs tant que la page n’a pas été actualisée. Ce problème a été résolu.
* Parfois, après l’importation d’utilisateurs à l’aide du fichier CSV, la valeur de l’ID utilisateur dans la page était remplacée par l’ID de messagerie. Ce problème a été résolu.

**Création de groupes d’utilisateurs**

Dans certains cas, le nombre d’utilisateurs ne s’affichait pas dans la page des groupes d’utilisateurs par défaut de Learning Manager. Ce problème a été résolu.

**Relevé de notes de l’élève**

Les valeurs d’attribut des champs actifs n’étaient pas affichées correctement dans les relevés de notes des élèves pour les certifications. Ce problème a été résolu.

**Partage multi-comptes**

Dans un scénario où un administrateur de compte partageait un catalogue de cours avec le destinataire et mettait à jour le module de test ou de préparation ultérieurement, le contenu du module de test ou de préparation était lu dans le module de contenu pour le destinataire. Ce problème a été résolu.

**Thèmes et image de marque**

Lorsqu&#39;un administrateur remplaçait un thème dans l&#39;application à l&#39;aide du widget Aperçu en direct et changeait de rôle, le widget Aperçu en direct ne fonctionnait pas comme prévu dans un nouveau rôle. Ce problème a été résolu.

**Prise en charge multilingue**

Lorsqu&#39;un administrateur remplaçait les paramètres régionaux de l&#39;application par chinois simplifié ou espagnol, une partie du contenu du menu dans le volet de gauche, les instructions en ligne et les messages contextuels ne s&#39;affichaient pas sous forme de mots ou de phrases significatifs. Ce problème a été résolu.

**Lecteur Fluidic**

* Lorsqu&#39;un auteur créait un cours avec du contenu AICC ou Tin Can et essayait de prévisualiser le contenu, celui-ci n&#39;était pas lu. Ce problème a été résolu.
* L&#39;aperçu du module ne fonctionnait pas lors de la création d&#39;un cours ou de la modification du cours par un auteur. Ce problème a été résolu.

**Catalogues**

Lorsqu&#39;un élève essayait d&#39;accéder à l&#39;URL des catalogues/programmes d&#39;apprentissage directement dans le navigateur, il était redirigé vers les cours. Ce problème a été résolu.

**Intégration de Salesforce**

* Après avoir établi une connexion Salesforce ou FTP, dans la page Attributs de mappage, les flèches déroulantes pour les champs ne s’affichaient pas dans les navigateurs IE, Edge et Safari. En outre, certains messages contextuels ne s’affichaient pas dans les workflows. Ce problème a été résolu.
* Dans certains cas, lorsqu&#39;un administrateur essayait de synchroniser les données importées au format .csv dans le connecteur FTP, la synchronisation échouait et affichait des entrées répliquées. Ce problème a été résolu.

**Calque d’API**

* Lorsqu&#39;un administrateur autorisait l&#39;élève externe à utiliser l&#39;authentification OAuth, il arrivait que les élèves externes ne puissent pas se connecter à l&#39;application. Ce problème a été résolu.
* Parfois, lorsqu&#39;il y avait un appel API pour les assistances à la tâche des élèves, une erreur d&#39;accès non autorisé s&#39;affichait. Ce problème a été résolu.

**Paramètres**

Dans la page sources de données, lorsqu&#39;une heure de planification automatique est définie et enregistrée, elle revient parfois à l&#39;ancien état. Ce problème a été résolu.

**Rapport de groupe d’utilisateurs**

Les valeurs de groupe d&#39;utilisateurs dans le filtre n&#39;étaient pas renseignées lorsque le type de rapport Personnalisé était sélectionné. Ce problème a été résolu.

**Intégration d’Adobe Connect**

Un titre d’en-tête inapproprié s’affichait pour l’intégration d’Adobe Connect une fois la connexion établie. Le texte de l’en-tête de page est corrigé.

**Rapports**

Parfois, même si l’option Afficher les données pour les valeurs actuelles était sélectionnée, les données les plus récentes n’étaient pas affichées dans les rapports. Ce problème a été résolu.

+++

+++Mise à jour 18

Date de publication : 31 juillet 2016.

## Nouvelles fonctionnalités et améliorations {#newfeaturesandenhancements}

Pour obtenir une liste des nouvelles fonctionnalités et améliorations effectuées dans la version de juillet de Learning Manager, consultez [Nouveautés](../whats-new.md).

Certaines fonctionnalités d&#39;amélioration sont répertoriées ci-dessous pour référence.

**Relevé de notes de l’élève**

Learning Manager vous fournit une fonctionnalité permettant de générer des relevés de notes pour les élèves Learning Manager de votre organisation. Pour plus d’informations, voir  [Contenu d’aide sur les relevés de notes des élèves](../administrators/feature-summary/learner-transcripts.md).

**Exporter le badge en tant que PDF**

Learning Manager vous permet d’exporter vos badges sous forme de fichiers de PDF. Pour plus d’informations, voir  [Contenu des fonctionnalités des badges](../administrators/feature-summary/badges.md).

**Score du quiz pour les modules**

Vous pouvez ajouter le score du quiz pour les modules Salle de classe, Salle de classe virtuelle et Activité.

**Ajouter des utilisateurs**

* Vous pouvez déplacer des élèves d&#39;un groupe d&#39;auto-inscription à un autre groupe.
* Vous pouvez déplacer des utilisateurs d’un groupe externe à un autre groupe externe.
* Vous pouvez faire d&#39;un utilisateur d&#39;un groupe externe le gestionnaire du même groupe externe.
* Après avoir ajouté un groupe d’utilisateurs externes à Learning Manager, vous pouvez également suspendre le processus d’inscription des utilisateurs externes. À tout moment, vous pouvez toujours révoquer le blocage (pause) en choisissant une option de reprise.
* Vous pouvez désormais modifier le nom et l’ID de messagerie des élèves.

**Auto-inscription**

Les élèves peuvent également se désinscrire des objets d’apprentissage tels que le cours, le programme d’apprentissage ou la certification. Cependant, l’élève ne peut pas se désinscrire d’un objet d’apprentissage après l’avoir terminé.

**Consommation d’objets d’apprentissage**

Désormais, les administrateurs peuvent marquer une activité d’apprentissage des élèves comme terminée.

**Rapports**

* Vous pouvez vous abonner à des rapports de cours, de programmes d&#39;apprentissage ou de certificats. Vous pouvez également vous abonner à des rapports de cours individuels pour des données telles que le score du quiz et le statut de l&#39;élève. Les abonnements seront envoyés à votre ID de messagerie enregistré dans le compte Learning Manager. Vous pouvez également modifier cet ID de messagerie.
* Lorsque vous exportez le rapport d&#39;inscription de certification, une nouvelle colonne nommée **Échéance** est également exporté. Ces données de colonne permettent aux administrateurs de connaître les élèves qui ont manqué les échéances de consommation de leurs objets d&#39;apprentissage.

**Modèles de courrier électronique**

Vous pouvez désormais modifier l’en-tête des modèles de courrier électronique.

+++

+++Mise à jour 17

Date de publication : 15 juin 2016.

### Problèmes résolus {#Issuesfixed-8}

**Ajouter des utilisateurs**

Lorsque les utilisateurs Learning Manager étaient très nombreux, le chargement de la page des utilisateurs et des groupes d’utilisateurs était ralenti. Ce problème a été résolu.

**Création de groupes d’utilisateurs**

Dans certains cas, le nombre d’utilisateurs ne s’affichait pas dans la page des groupes d’utilisateurs par défaut de Learning Manager. Ce problème a été résolu.

+++

+++Mise à jour 16

Date de publication : 10 juin 2016.

## Problème résolu {#Issuefixed-1}

Certains clients rencontraient des problèmes lors de l’utilisation de la fonctionnalité d’authentification unique dans Learning Manager. Ce problème a été résolu en renvoyant l’entityId de Learning Manager vers une URL (<https://learningmanager.adobe.com>) au lieu d’un mot-clé. Learning Manager est conforme à la spécification SAML 2.0.

+++

+++Mise à jour 15

Date de publication : 25 mai 2016

### Améliorations {#Enhancements-10}

**Certifications/programmes d’apprentissage**

* Dans la liste d&#39;inscription des élèves pour les certifications et les programmes d&#39;apprentissage, le nom complet (prénom et nom) des élèves est affiché. Auparavant, seul le prénom des élèves s&#39;affichait.
* Les compétences avec le plus haut niveau de crédits sont prises en compte dans la liste des cours des certifications/programmes d’apprentissage et affichées sur les cartes en tant que compétence de certification/programme d’apprentissage. S’il existe plusieurs cours avec la même valeur de crédits, ils sont sélectionnés par ordre alphabétique. Auparavant, les noms de compétence pour les programmes de certification/d&#39;apprentissage étaient considérés aléatoirement à partir d&#39;une liste de cours respectifs.

**Importer un fichier CSV**

Pour la fonction de chargement automatique d’un fichier CSV à l’aide d’un FTP, les administrateurs reçoivent des notifications par e-mail en cas d’échec du chargement du fichier CSV.

**Ajouter des partenaires externes**

Lorsque des élèves externes consultent la page d&#39;inscription à l&#39;aide d&#39;une URL de profil externe, le nom du profil externe s&#39;affiche dans la page d&#39;inscription pour une meilleure identification.

### Problèmes résolus {#Issuesfixed-9}

**Aperçu et publication de cours**

* Dans le rôle d&#39;auteur, lorsque vous prévisualisez un cours qui a été téléchargé à partir du Captivate en tant que contenu SCORM+SWF avec `code $$cpQuizInfoStudentName$$` variable, la variable affichait une valeur nulle. Ce problème a été résolu.
* Lorsqu&#39;un cours Presenter avec un titre contenant une apostrophe (&#39;) était publié et affiché dans Learning Manager, des points d&#39;interrogation ( ???) s&#39;affichaient dans la table des matières. Ce problème a été résolu.

**Certifications**

* Si une certification est associée à un catalogue et qu&#39;elle se répète, elle apparaît dans tous les catalogues associés. Auparavant, il arrivait que les utilisateurs ne puissent pas afficher les certifications récurrentes dans leurs catalogues.
* Lors de la création de certifications, si un administrateur entre **jours pour terminer** valeur supérieure ou égale à la période de validité de la certification, un message d&#39;avertissement s&#39;affiche. Auparavant, le message d&#39;avertissement ne s&#39;affichait pas pour les administrateurs.
* La certification **validité** s’affiche en mois pour les utilisateurs. Auparavant, la valeur de base apparaissait en années.

**Définition des programmes d’apprentissage**

L&#39;échéance n&#39;apparaît pas pour les instances de programme d&#39;apprentissage par défaut. Auparavant, une échéance prédéfinie s&#39;affichait, qui pouvait ne pas être pertinente pour les utilisateurs.

**Création de cours à l’aide de modules**

* Lorsqu&#39;un auteur mettait à jour un module d&#39;un cours fusionné, la page de présence ne s&#39;affichait pas dans le rôle d&#39;administrateur. Ce problème a été résolu.
* Lorsqu&#39;un nom d&#39;instance de cours contenait deux-points ( :), l&#39;exportation de la liste des élèves échouait. Ce problème a été résolu.

+++

+++Mise à jour 14

Date de publication : 4 mai 2016

### Améliorations {#Enhancements-11}

**Catalogues**

Lorsqu’un élève accède au catalogue, le focus par défaut passe d’un onglet à l’autre en fonction de la disponibilité des objets d’apprentissage, dans l’ordre suivant : 1. Cours 2. Programmes 3. Certifications et 4. Assistances à la tâche. Par exemple, si les cours ne sont pas disponibles dans l&#39;onglet Cours pour cet élève, le curseur passe à l&#39;objet d&#39;apprentissage suivant, à savoir Programmes, s&#39;il existe des programmes d&#39;apprentissage.

**Paramètres du compte**

Une option de retour d’informations est fournie dans la boîte de dialogue de confirmation de la désactivation du compte lorsqu’un administrateur choisit de désactiver un compte.

### Problèmes résolus {#Issuesfixed-10}

**Rapports d’exportation**

* L&#39;exportation de la liste d&#39;élèves échouait lorsqu&#39;un grand nombre d&#39;utilisateurs étaient inscrits à un programme d&#39;apprentissage. Ce problème a été résolu.
* Lorsqu&#39;un cours possédait deux instances portant le même nom et que le nom de l&#39;instance était long, deux feuilles de calcul n&#39;étaient pas créées dans le fichier Excel exporté. Ce problème a été résolu.

**Inscription en bloc**

Lorsqu&#39;un grand nombre d&#39;élèves étaient inscrits à des objets d&#39;apprentissage tels que des programmes d&#39;apprentissage, des cours, des certifications, des assistances à la tâche et des plans d&#39;apprentissage, l&#39;inscription échouait. Ce problème a été résolu.

+++

+++Mise à jour 13

Date de publication : 20 avril 2016

### Problèmes résolus {#Issuesfixed-11}

**Création de cours à l’aide de modules**

Lorsqu&#39;un contenu de module avec un nom de fichier long était chargé, l&#39;apparence des boutons présentait des problèmes. En outre, les options de téléchargement et de suppression du module ne fonctionnaient pas comme prévu. Ce problème a été résolu.

**Importer un fichier CSV**

À la demande des clients américains, l’heure de chargement automatique du fichier CSV FTP a été modifiée de minuit GMT à minuit HNP.

**Rapports d’exportation**

L&#39;exportation des données d&#39;inscription échouait si l&#39;un des élèves inscrits était supprimé après avoir suivi le cours. Ce problème a été résolu.

**Modèles de courrier électronique**

* Le mot **partenaires,** qui a été utilisée pour représenter des groupes extérieurs,**** est **** supprimé du corps et du titre des modèles de courrier électronique. Les groupes externes ne sont pas nécessairement appelés partenaires.\
  **Remarque :** Ce modèle mis à jour n’apparaît pas si le modèle par défaut a déjà été modifié. Pour afficher le modèle mis à jour, cliquez sur **Rétablir l’original** dans **Aperçu du modèle** boîte de dialogue.

* L&#39;URL n&#39;est pas cliquable dans l&#39;e-mail reçu par les administrateurs lorsque **Profil Créé (Auto-Inscription)** et **Profil Créé (Externe/Partenaires)** les modèles de courrier électronique sont modifiés. Ce problème a été résolu.

+++

+++Mise à jour 12

Date de publication : 7 avril 2016

### Améliorations {#Enhancements-12}

**Assistances à la tâche**

Créez des assistances à la tâche à l’aide d’une URL. Vous pouvez mentionner uniquement un nom d&#39;URL dans le flux de création d&#39;assistance à la tâche et créer une assistance à la tâche si vous souhaitez utiliser du contenu en ligne existant comme assistance à la tâche.

**Ajouter des élèves**

La modification des données d’un utilisateur unique, telles que le nom, l’adresse e-mail, le profil et le nom du responsable, est autorisée. Tous les groupes d’utilisateurs correspondants sont mis à jour avec les dernières données utilisateur.

**Rapports d’exportation**

Le nom du responsable, le nom de l&#39;objet d&#39;apprentissage et les colonnes de valeurs non uniques définies par l&#39;utilisateur à partir du fichier CSV sont ajoutés à la liste des élèves exportée pour les objets d&#39;apprentissage. Auparavant, seules les données de base des élèves telles que le nom, la date, le courrier électronique et le statut s&#39;affichaient.

**Ajouter des partenaires externes**

L’application Learning Manager ne permet pas aux élèves externes de se connecter à l’application une fois que leur compte a expiré. Les partenaires externes peuvent afficher l’état de leur compte dans l’application.

**Certifications**

Vous pouvez renouveler les certifications en mois en mentionnant la valeur dans **Validité** champ. Auparavant, le renouvellement de la certification n&#39;était autorisé qu&#39;en termes d&#39;années.

### Problèmes résolus {#Issuesfixed-12}

**Annonce**

Dans la connexion Administrateur, la pagination ne fonctionnait pas dans la page Annonces. Ce problème a été résolu.

**Programmes et plans d’apprentissage**

* Lorsqu&#39;un élève tentait d&#39;ignorer un module de cours ordonné dans un programme d&#39;apprentissage, aucun message d&#39;erreur ne s&#39;affichait. Ce problème a été résolu. Un message d’erreur **Impossible d’ignorer les modules** apparaît.
* Les cours n&#39;étaient pas ajoutés aux programmes d&#39;apprentissage lorsque la pagination était utilisée dans la liste des cours. Ce problème a été résolu.
* **Retraité** s&#39;affichait deux fois dans Programmes d&#39;apprentissage > Instances. Ce problème a été résolu.

**Assistances à la tâche**

* Lorsqu&#39;un élève supprime les assistances à la tâche de **Formation** onglet, **Nom** le tri ne fonctionnait pas comme prévu tant que la page n’était pas actualisée. Ce problème a été résolu.

* Si une assistance à la tâche faisait partie de plusieurs cours, ceux-ci ne s&#39;affichaient pas dans la liste des assistances à la tâche. Ce problème a été résolu.
* Si un élève effectuait un zoom avant ou arrière dans le navigateur, la pagination de la liste des assistances à la tâche ne fonctionnait pas comme prévu. Ce problème a été résolu.

**Suivi de cours**

* Si un élève effectuait un zoom avant ou arrière dans le navigateur, la pagination des cours ne fonctionnait pas comme prévu. Ce problème a été résolu.

**Création de compétences**

Dans la connexion Élèves, info-bulle du nom de compétence dans **Mappage des compétences **était** **le nom **** complet n’est pas affiché. Ce problème a été résolu.

**Ajouter des partenaires externes**

* Un message texte a été inclus dans la page d’enregistrement des utilisateurs externes comme **Les utilisateurs doivent d’abord s’enregistrer et créer un nom d’utilisateur et un mot de passe pour les connexions suivantes**.

**Notifications utilisateur**

* Lorsqu’un élève externe clique sur le bouton **Ouvrir les notes** lien dans l’e-mail de notification de nouveau suivi d’un cours, le lecteur s’ouvre mais le panneau Notes ne fonctionne pas. Ce problème a été résolu.
* Lorsqu’un élève externe tente d’ouvrir les modules préparatoires ou de test à l’aide de **Ouvrir les notes** lien dans l’e-mail de notification de nouveau suivi du cours, le contenu des notes n’était pas visible. Ce problème a été résolu.

**Création de cours à l’aide de modules**

Lorsqu&#39;un administrateur tentait d&#39;inscrire des élèves à un cours fusionné contenant un module de salle de classe expiré, la boîte de dialogue d&#39;inscription ne s&#39;ouvrait pas. Ce problème a été résolu.

**Rapports d’exportation**

Si un texte de question contient plus de 255 caractères et est activé pour le format SCORM 1.2, le rapport de quiz de ces questions ne fonctionnait pas. Ce problème a été résolu.

+++

+++Mise à jour 11

Date de publication : 15 mars 2016

### Problèmes résolus {#Issuesfixed-13}

**Création de cours avec des modules**

* Dans la connexion Administrateur, lorsque vous essayez de créer une nouvelle instance pour les cours de **Retraité** tab, une erreur s&#39;est produite. Ce problème a été résolu.
* Dans la connexion Administrateur du contenu localisé, les mises en page des écrans Actions et Inscription étaient déformées lors de l&#39;inscription d&#39;élèves à l&#39;instance de cours. Ce problème a été résolu.
* Lorsqu&#39;un auteur créait des modules de salle de classe ou de salle de classe virtuelle, le mois par défaut du calendrier était janvier 2015. Ce problème est corrigé pour refléter la date actuelle par défaut.
* Lorsqu&#39;un nom d&#39;instance de cours se composait d&#39;une barre oblique inverse ou inverse, l&#39;exportation de la liste d&#39;élèves échouait. Ce problème a été résolu.

**Annonce**

Lorsqu&#39;un élève passait le curseur de la souris sur une annonce vidéo, le curseur ne se changeait pas en doigt pointé comme prévu. Ce problème a été résolu.

**Notifications utilisateur**

Lorsqu’un élève externe clique sur le bouton **Ouvrir les notes** lien dans l’e-mail de notification de nouveau suivi d’un cours, cela ne fonctionnait pas. Ce problème a été résolu. Ce lien ouvre le lecteur avec des notes, même si l’utilisateur n’est pas connecté à Learning Manager.

**Prise en charge du français et de l’allemand**

Les URL d&#39;aide de la fonctionnalité de chargement de fichiers CSV renvoyaient à du contenu d&#39;aide en anglais. Ce problème a été résolu.

**Aperçu et publication des cours**

Dans la connexion Auteur, lorsque vous prévisualisiez le contenu de l&#39;API TinCan (SWF/HTML) de Presenter 10 et 11, le contenu ne fonctionnait pas. Ce problème a été résolu.

**E-mails personnalisables**

Les noms de titre dans les modèles d’e-mail n’étaient pas appropriés. Le contenu est mis à jour dans ces titres de modèle pour les rendre lisibles.

**Assistances à la tâche**

Dans le navigateur Internet Explorer 11, le nom et l&#39;icône de l&#39;assistance à la tâche apparaissaient déformés dans l&#39;aperçu de l&#39;auteur et de l&#39;administrateur. Ce problème a été résolu.

+++

+++Mise à jour 10

Date de publication : 28 février 2016.

## Nouvelles fonctionnalités {#Newfeatures-2}

### Assistances à la tâche

Les assistances à la tâche sont un référentiel de contenu de formation accessible aux élèves sans aucun critère d&#39;inscription ou d&#39;achèvement. Les élèves peuvent se référer à ces assistances à la tâche pour obtenir de l&#39;aide pour effectuer une activité ou une tâche dans une organisation. L’administrateur peut suivre le nombre de téléchargements par assistance à la tâche.

Pour plus d’informations sur cette fonctionnalité, reportez-vous à la section  [Aide sur les assistances à la tâche](../learners/feature-summary/job-aids.md).

### Annonce

Une annonce est un message multimédia (texte, image ou vidéo) qu’un administrateur peut créer et diffuser auprès d’un ensemble défini d’utilisateurs. Utilisez les annonces pour motiver les élèves à suivre des formations et ainsi construire une culture de l&#39;apprentissage.

Pour plus d’informations sur cette fonctionnalité, reportez-vous à la section  [Aide sur les annonces](../learners/feature-summary/announcements.md).

### Prise en charge de l’API Tin Can

Adobe Learning Manager prend en charge la spécification de l’API Tin Can (également appelée API Expérience ou xAPI). Vous pouvez charger et suivre du contenu compatible avec l’API Tin Can de la même manière que vous suivez le contenu SCORM et AICC.

Pour plus d’informations, contactez l’équipe d’assistance Adobe.

### Séquencement des cours

Vous pouvez créer un parcours d’apprentissage en affectant automatiquement un cours de suivi ou toute activité d’apprentissage.

Les événements des plans d&#39;apprentissage ont été mis à jour. Deux nouveaux événements ont été ajoutés. Reportez-vous à  [Plans d’apprentissage](../learners/feature-summary/learning-programs.md) pour plus d’informations.

### Rappel de notes

Si vous prenez des notes lors de l’utilisation d’un cours, Learning Manager vous rappelle après 15 jours en envoyant une notification pour réviser les notes.

### Ludification au niveau du groupe

Les administrateurs peuvent définir l’étendue de la ludification en modifiant les paramètres de l’étendue. Vous pouvez activer de manière sélective la ludification parmi des utilisateurs, des groupes ou des emplacements de profil similaires. Reportez-vous à  [Ludification](../learners/feature-summary/gamification.md) pour plus d’informations.

### Prise en charge du français et de l’allemand

L’application Learning Manager est disponible en français et en allemand. Vous pouvez personnaliser la langue pour les commentaires, les instances de cours et la communication.

### Améliorations {#Enhancements-13}

Des améliorations importantes ont été apportées aux fonctionnalités existantes de Learning Manager. Certaines des principales améliorations sont les suivantes :

### Importer un fichier CSV

Si vous supprimez des utilisateurs, vous ne pouvez pas les réajouter dans l’application à l’aide de l’ajout d’un seul utilisateur. Cependant, vous pouvez rajouter l’utilisateur supprimé à l’aide du processus de chargement CSV. Des modifications importantes ont été apportées à la restriction des champs obligatoires dans la fonction de téléchargement CSV. Reportez-vous à  [FAQ sur les fichiers CSV](../administrators/add-users-in-bulk.md) pour plus d’informations.

### Vue de la liste des cours

Par défaut, vous pouvez afficher les cours sous forme de cartes. Une vue de liste a été introduite dans cette version. Vous pouvez cliquer sur l’icône de barre triple en regard du champ de recherche pour modifier l’affichage.

### Supprimer des cours

Vous pouvez désormais supprimer des cours à l&#39;état de brouillon et de retiré. Reportez-vous à  [Cours](../administrators/feature-summary/courses.md) pour plus d’informations. Si un objet d&#39;apprentissage est supprimé, toutes ses données de rapport sont également supprimées. Si un cours est supprimé et s&#39;il faisait partie d&#39;un autre objet d&#39;apprentissage, un message approprié s&#39;affiche pour l&#39;utilisateur.

**Programmes et plans d’apprentissage**

Vous pouvez imposer l’ordre dans lequel les élèves peuvent suivre des cours dans le cadre des programmes d’apprentissage. Vous pouvez supprimer des programmes d&#39;apprentissage aux stades de brouillon et retiré. Si un objet d&#39;apprentissage est supprimé, toutes ses données de rapport sont également supprimées.

**Certifications**

Vous pouvez supprimer des certifications par étapes de brouillon et de retrait. Si un objet d&#39;apprentissage est supprimé, toutes ses données de rapport sont également supprimées.

**Évaluation de l’efficacité du cours**

Dans la connexion Administrateur, vous pouvez exporter les données de retour d&#39;informations L1 et L3 pour n&#39;importe quel cours.

**Création de cours avec des modules**

Vous pouvez obliger les élèves à remplir les conditions préalables avant de suivre les cours.

**Notifications utilisateur**

Les élèves reçoivent des notifications chaque fois qu&#39;ils s&#39;auto-inscrivent à un programme d&#39;apprentissage.

**Modules de salle de classe (ILT)**

Vous pouvez créer des cours en salle de classe pour une date antérieure. Cette fonctionnalité permet aux administrateurs d’entreprise d’importer également d’anciennes informations sur les cours en salle de classe dans Learning Manager et de générer des rapports.

**Rapports d’exportation**

Le rapport Élèves a été amélioré. Vous pouvez afficher le nom, l&#39;adresse électronique, l&#39;état de l&#39;objet d&#39;apprentissage, les critères d&#39;inscription, la date d&#39;inscription, la date d&#39;achèvement et la date de début dans le rapport.

**Ajouter des partenaires externes**

Après avoir inscrit des élèves externes dans le compte Learning Manager, vous pouvez également en réduire le nombre, si nécessaire. Cependant, vous ne pouvez pas réduire le nombre d’élèves au-delà du nombre de places utilisées. Pour contourner le problème, vous pouvez d’abord supprimer les élèves inscrits, puis vous inscrire à nouveau avec le nombre requis de places.

### Problèmes résolus {#Issuesfixed-14}

**Participation des élèves**

La feuille de présence dans la vue Administrateur affiche le nom complet de l&#39;employé s&#39;il est disponible. Auparavant, seul le prénom de l’élève s’affichait.

**Programmes et plans d’apprentissage**

Tous les cours des programmes d&#39;apprentissage sont affichés dans l&#39;ordre prévu. Auparavant, il y avait des problèmes dans l&#39;ordre des cours dans un programme d&#39;apprentissage. Ce problème a été résolu.

**Ajouter des élèves**

Si un utilisateur auto-inscrit existant tente de s&#39;inscrire à nouveau à l&#39;aide du processus d&#39;auto-inscription, un message approprié s&#39;affiche. Le format et le contenu du message sont fixes.

**Rapports**

Si vous souhaitez que le contenu identifie le temps passé par l’utilisateur dans le contenu, vous pouvez l’identifier à l’aide d’une variable, `code cmi.core.session_time`. La variable n’était pas définie auparavant. Ce problème a été résolu.

**Création de cours avec des modules**

Chaque fois qu&#39;un module de cours existant est remplacé par un autre module, une nouvelle version est générée. Si le quiz de ce nouveau module était exporté, une exception se produisait et le rapport de quiz n&#39;était pas généré. Ce problème a été résolu.

**Modèles de courrier électronique**

Les fautes de frappe dans les modèles de courrier électronique sont corrigées.

+++

+++Mise à jour 9

Date de publication : 9 février 2016.

## Comportement de déconnexion mis à jour {#signoutbehaviorupdated}

Lorsque les utilisateurs cliquent sur **[!UICONTROL Se déconnecter]** dans Learning Manager, ils sont désormais déconnectés de l’application Learning Manager et de leur ID d’Adobe.

+++

+++Mise à jour 8

Date de publication : 20 janvier 2016.

### Améliorations {#Enhancements-14}

**E-mails personnalisables**

* Les utilisateurs peuvent modifier la section de pied de page des modèles de courrier électronique. Vous pouvez personnaliser le pied de page d&#39;un modèle de courrier électronique avec le texte de votre choix. Le pied de page personnalisé est automatiquement appliqué à tous les types de modèles de courrier électronique.

**Suivi de cours**

* Les objets de ressource en mode Aperçu d&#39;un cours sont répertoriés l&#39;un après l&#39;autre sur une nouvelle ligne. Auparavant, dans certains cas, les ressources d&#39;un cours s&#39;affichaient les unes à côté des autres sur une seule ligne.

**Lien direct vers les objets d’apprentissage**

* Vous pouvez accéder aux objets d’apprentissage (à l’exception de la certification) à l’aide d’une URL directe. Le **[!UICONTROL Copier l’URL]** s’affiche sur les mosaïques des objets d’apprentissage. Les utilisateurs peuvent cliquer sur **[!UICONTROL Copier l’URL]** et collez le lien dans une page de navigateur distincte pour accéder directement à l’objet d’apprentissage.

**Création de cours à l’aide de modules**

* Lors de la création d’un cours, les auteurs peuvent organiser les cours prérequis dans n’importe quel ordre. Auparavant, cette option n’était pas disponible dans Learning Manager.

* Les auteurs peuvent ajouter ou supprimer des cours prérequis dans les cours publiés. Auparavant, cette fonctionnalité n&#39;était disponible que pour les cours Draft.

**Inscription d’utilisateur**

* Les utilisateurs peuvent se connecter à Learning Manager sans vérification d’URL supplémentaire si leur Adobe ID correspond à l’ID de messagerie de Learning Manager. Lors de l’ajout d’utilisateurs au compte, l’administrateur d’une organisation fournit l’ID de messagerie Learning Manager.

**Créer un catalogue**

* Dans le rôle d&#39;administrateur, lors de la création de catalogues à l&#39;aide de **Ajout d’objets d’apprentissage** , les cours retirés n&#39;apparaissent pas dans la liste des cours.

**Autres correctifs**

* Dans le rôle d&#39;administrateur, le nom complet des élèves est affiché dans **Élèves** onglet. Auparavant, seul le prénom de l’élève s’affichait.

+++

+++Mise à jour 7

Date de publication : 13 janvier 2016.

### Problèmes résolus {#Issuesfixed-15}

**Suivi de cours**

* Lors de l&#39;accès au contenu du cours, la barre de lecture du contenu apparaît toujours à l&#39;écran. Auparavant, la barre de contenu présentait un problème, car elle disparaissait de l’écran par intermittence.
* Lors de l&#39;accès au contenu du cours, si une boîte de dialogue contextuelle s&#39;affiche pour demander aux utilisateurs s&#39;ils souhaitent vraiment quitter la page ou y rester, appuyer sur Rester sur cette boîte de dialogue ramène l&#39;utilisateur au contenu. Dans certains cas, cliquer sur le bouton de suspension permettait à l&#39;utilisateur de quitter le contenu du cours.

**Autres correctifs**

* Peu de problèmes liés à la lecture du contenu sont résolus.

+++

+++Mise à jour 6

Date de publication : 22 décembre 2015

### Améliorations {#Enhancements-15}

**Tableau de bord personnel**

* Lors de l&#39;accès aux cours, catalogues et programmes d&#39;apprentissage dans les rôles d&#39;administrateur et d&#39;auteur, l&#39;ordre des onglets est modifié en **Publié - Brouillon - Tous - Retiré**. La sélection par défaut est **Publié.**

### Problèmes résolus {#Issuesfixed-16}

**Suivi de cours**

* Dans le rôle d&#39;élève lorsque vous suivez un cours, si le lecteur est fermé à l&#39;aide du bouton Précédent du navigateur ou de la touche Retour arrière du clavier, le temps d&#39;apprentissage passé sur le cours est capturé dans les rapports. Dans certains scénarios, il arrivait que cette durée ne soit pas enregistrée dans les rapports.

**Inscription d’utilisateur**

* Si un utilisateur inscrit un compte Learning Manager à l’aide de l’auto-inscription à authentification unique, le nom d’utilisateur dans la liste des utilisateurs s’affiche correctement selon les enregistrements. Dans certains cas, le nom d’utilisateur s’affichait de manière incorrecte.

**Création de cours à l’aide de modules**

* Lorsqu&#39;un auteur duplique un cours, les fichiers de ressources du cours dupliqué peuvent être supprimés ou mis à jour. Dans certains scénarios, les utilisateurs rencontraient des problèmes pour mettre à jour ou supprimer les ressources des cours dupliqués.

**Création d’un catalogue personnalisé pour un groupe d’utilisateurs**

* Lors de l’utilisation de **Ajout d’objets d’apprentissage** dans le rôle d&#39;administrateur, vous pouvez filtrer des cours, choisir un cours et ajouter à l&#39;aide de **Ajouter** au bas de la boîte de dialogue. Dans certains cas, **Ajouter** n&#39;apparaissait pas pour certains utilisateurs.

+++

+++Mise à jour 5

Date de publication : 11 décembre 2015

### Problèmes résolus {#Issuesfixed-17}

**Connexion utilisateur**

* Lorsqu&#39;un utilisateur tentait de se connecter à l&#39;application Learning Manager sans utiliser le lien d&#39;activation, le message d&#39;erreur s&#39;affichait dans un format incorrect. Ce problème a été résolu.

**Application pour tablettes**

* Après l’installation de Learning Manager sur tablette Android ou iPhone, les messages relatifs à la compatibilité avec les navigateurs ne s’affichent plus. Auparavant, un message de compatibilité de navigateur s&#39;affichait pour les utilisateurs. Ce problème a été résolu.

+++

+++Mise à jour 4

Date de publication : 9 décembre 2015

### Améliorations {#Enhancements-16}

**Ajouter des utilisateurs**

* Dans le rôle d&#39;administrateur, lorsque l&#39;administrateur enregistre des utilisateurs ou termine d&#39;ajouter un seul utilisateur, un message s&#39;affiche pour indiquer que le workflow est terminé et indiquer les étapes à suivre.
* Lorsqu’un utilisateur tente de se connecter directement à l’application Learning Manager sans utiliser le lien d’activation par utilisateur, un message d’erreur s’affiche et invite les utilisateurs à utiliser le lien d’activation.

**Navigateurs pris en charge**

* Si un utilisateur accède à l’application Learning Manager par le biais de navigateurs non pris en charge, il reçoit un message d’alerte indiquant la liste des navigateurs inscrits dans la liste blanche.

### Problèmes résolus {#Issuesfixed-18}

**Rapports**

* Dans le rôle d&#39;administrateur ou de responsable, lorsque vous créiez un rapport avec le temps d&#39;apprentissage en axe secondaire, appliquiez le filtre de responsable et enregistriez le rapport, l&#39;utilisateur ne pouvait pas télécharger ces rapports. Vous pouvez télécharger tous les types de rapports.

**Ajouter des utilisateurs**

* Le message d&#39;alerte affiché lors de l&#39;activation d&#39;élèves externes dans le rôle d&#39;administrateur comportait quelques erreurs typographiques. Le problème a été résolu.
* Dans le rôle d’administrateur, un message d’erreur approprié s’affiche lorsque le champ Responsable n’est pas correctement sélectionné lors de l’ajout d’un utilisateur unique.

**Inscription d’utilisateur**

* Le courrier électronique de bienvenue reçu par de nouveaux utilisateurs souligne l’importance de lier Adobe ID à l’ID Learning Manager pour une connexion réussie.

**E-mails personnalisables**

* Lorsque vous ajoutez plusieurs élèves à des cours en salle de classe qui ont des sessions en tant que pièces jointes, certains élèves ne recevaient pas de notifications par courrier électronique. Ce problème a été résolu.
* Les courriers électroniques envoyés aux élèves concernant les inscriptions aux objets d&#39;apprentissage et autres événements contiennent le nom de l&#39;objet d&#39;apprentissage dans l&#39;objet du courrier électronique.

**Autres correctifs**

* Les problèmes liés aux liens URL dans les modèles de courrier électronique sont résolus.
* Prise en charge fournie pour

   * Publier sur Learning Manager
   * Prise en charge du chargement de contenu plus rapide pour la version CP 8 (correctif CP803 requis)

+++

+++Mise à jour 3

Date de publication : 26 octobre 2015.

### Améliorations {#Enhancements-17}

**Ajouter des utilisateurs**

* Lien d’aide en ligne fourni dans la boîte de dialogue Ajouter des utilisateurs > Chargement CSV pour mieux comprendre les utilisateurs lors du chargement du fichier CSV.

**Lecteur Fluidic**

* Lorsque vous chargiez du contenu de cours de Captivate d&#39;une taille supérieure à 500 Mo, le contenu n&#39;était pas lu dans le lecteur Fluidic. Cette restriction est supprimée. Actuellement, la limite de taille a été modifiée à 2 Go.

**Facturation**

* Dans le rôle d’administrateur, lorsqu’un utilisateur saisit le nombre d’élèves et clique sur **Passer une commande,** une boîte de dialogue contenant des détails sur les frais d’abonnement mensuels et annuels par utilisateur s’affiche.

### Problèmes résolus {#Issuesfixed-19}

**Création de cours à l’aide de modules**

* Lors de la création de cours avec des modules d&#39;activité, les auteurs peuvent choisir des URL externes valides même si elles contiennent des chemins de dossier dans l&#39;URL. Auparavant, les URL avec des chemins de dossier n&#39;étaient pas prises en charge. Ce problème a été résolu.
* Si le contenu du cours était un projet chargé à l’aide d’un fichier zip dans Learning Manager et si ce fichier zip contenait des chemins d’accès à des dossiers, tels que Zip>dossier>contenu, ce type de contenu n’était pas pris en charge. Ce problème a été résolu.

**Application pour tablettes**

* Lorsqu&#39;un utilisateur tentait de télécharger les fichiers de ressources d&#39;un cours dans l&#39;application Android Learning Manager, ceux-ci n&#39;étaient pas téléchargeables. Ce problème a été résolu.
* Lors de l&#39;utilisation d&#39;un cours à l&#39;aide du lecteur Fluidic, lorsqu&#39;un utilisateur enregistrait une note et tentait de la télécharger à partir du cours ultérieurement, elle n&#39;était pas téléchargeable. Ce problème a été résolu.

+++

+++Mise à jour 2

Date de publication : 28 septembre 2015

### Améliorations {#Enhancements-18}

**Création de cours à l’aide de modules**

* L&#39;application Learning Manager prend en charge le chargement de contenu SCORM même si la version n&#39;est pas mentionnée dans le fichier manifest.xml. Par défaut, la version est considérée comme 1.2.
* Lorsque vous chargiez du contenu de cours de Captivate d&#39;une taille supérieure à 500 Mo, le contenu n&#39;était pas lu dans le lecteur Fluidic. Dans le cadre de la mise à jour 2, la taille limite a été modifiée à 800 Mo.

**Facturation**

* Dans le rôle d&#39;administrateur, lors de l&#39;achat d&#39;un abonnement par carte de crédit, l&#39;utilisateur peut choisir la première commande en commençant par 10 élèves. Le nombre minimum d’élèves requis pour la première commande a été réduit de 100 à 10.

**Inscription d’utilisateur**

* Un lien URL permettant de créer Adobe ID a été fourni dans le courrier électronique de bienvenue reçu par les élèves après leur inscription.

**Ajouter des utilisateurs**

* Dans le rôle d’administrateur, l’ajout d’utilisateurs à l’aide de l’option de chargement CSV directement à partir du compte Exavault ne fonctionnait pas pour certains clients. Ce problème a été résolu.

### Problèmes résolus {#Issuesfixed-20}

**Programmes et plans d’apprentissage**

* Les élèves peuvent être automatiquement inscrits au même programme d&#39;apprentissage dans le cadre de plusieurs plans d&#39;apprentissage. Auparavant, il y avait quelques exceptions à ce workflow. Ce problème a été résolu.

**Affichage du tableau des scores et des badges**

* Dans le rôle d&#39;élève, après avoir suivi un cours contenant un badge, l&#39;image du badge ne s&#39;affichait pas dans la carte des badges du tableau de bord des élèves ni dans le fichier téléchargé. Ce problème a été résolu.

**Application pour tablettes**

* Une fenêtre contextuelle s&#39;affiche pour indiquer la disponibilité de l&#39;application de l&#39;élève lorsque son URL est ouverte dans un navigateur sur un appareil Android.

**Autres correctifs**

* Un problème lié à la création de compte d’utilisateur en raison de la prise en charge du stockage réseau Akamai a été résolu.
* Un problème lié au chargement de contenu SCORM 1.2 contenant un fichier zip avec plusieurs dossiers a été résolu.

+++
