---
title: Nouveautés de la version d’avril 2026 de Adobe Learning Manager
description: Découvrez les nouvelles fonctionnalités, améliorations et mises à jour importantes de la version d’avril 2026 de Adobe Learning Manager.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 33f503b69b979bfa962387388b453492a44cac5d
workflow-type: tm+mt
source-wordcount: '20354'
ht-degree: 3%

---

# Mises à jour dans Adobe Learning Manager

>[!IMPORTANT]
>
>Les fonctionnalités de cette version sont disponibles en version Beta. Les fonctionnalités et le comportement peuvent changer avant la mise à disposition générale. Partagez vos commentaires via les canaux de support Adobe habituels.


Ce document résume les nouvelles fonctionnalités, améliorations et mises à jour de la version d’avril 2026 de Adobe Learning Manager. Utilisez-le pour planifier les modifications pour votre organisation et comprendre ce qui est disponible pour les élèves, les administrateurs et les auteurs.

**Pour les élèves :** le lecteur Fluidic affiche désormais le nom du module suivant et un bouton de sortie clair. La langue du lecteur peut être définie via LTI pour une expérience cohérente entre les plateformes. Le contenu Captivate comprend une table des matières unifiée, des repères d’achèvement au niveau des diapositives et des exportations de notes fiables. La prise en charge multilingue est disponible pour les assistances à la tâche, les questions de liste de contrôle et les pistes de texte vidéo. L’assistant AI aide les élèves à obtenir des réponses dans l’expérience d’apprentissage.

**Pour les administrateurs et les auteurs :** le connecteur Zoom prend en charge plusieurs sessions VILT simultanées. Les cours partagés dans des comptes de pairs affichent le véritable auteur au lieu du terme « Auteur externe ». Les administrateurs peuvent restreindre le moment où les modules peuvent être démarrés. Les dates d’expiration des objets d’apprentissage sont affichées dans les API des élèves. Les modules de liste de contrôle prennent en charge la notation pondérée, le texte de question multilingue et les commentaires de réviseur facultatifs. Les certificats personnalisés offrent un éditeur glisser-déposer avec des champs dynamiques et des arrière-plans générés par l’IA. Le créateur d’expériences hors connexion vous permet de créer des pages d’apprentissage publiques sans nécessiter de connexion.

**Pour les instructeurs :** générez des codes QR pour l&#39;inscription à l&#39;instance et la participation aux sessions. Ajoutez des commentaires ou des commentaires pendant l’évaluation de la liste de contrôle.

**Reporting et analyses :** le contenu SCORM peut désormais signaler plusieurs tentatives de quiz dans les rapports L2. Le calcul du temps d’apprentissage passé est amélioré dans les relevés de notes des élèves. Les rapports Relevés de notes d’apprentissage pour les administrateurs sont mis à jour. Des améliorations de la recherche avancée sont disponibles.

## Navigation dans le lecteur Fluidic : affiche le nom du module suivant

### Présentation

Cette amélioration était déjà incluse dans la version de novembre 2025 de Adobe Learning Manager.

L’action « Suivant » dans le lecteur indique ce qui se passera lorsque l’utilisateur cliquera dessus en affichant le nom du module ou cours suivant et en signalant explicitement lorsque l’élève est sur le point de quitter le lecteur.

### Nouveautés

Libellé **« Module suivant : {ModuleName} » dans le lecteur**

L&#39;icône Suivant du Lecteur Fluidic affiche désormais le nom du module suivant du cours. Par exemple, Module suivant : Leçon 2 - Prise en main.

Cela s’applique partout où l’élève passe d’un module à l’autre dans le même cours.

**Effacer l&#39;action de sortie sur le dernier module**

Lorsque l&#39;élève se trouve sur le dernier module d&#39;un cours, un nouveau bouton d&#39;action Quitter s&#39;affiche, indiquant que si vous cliquez dessus, le lecteur sera fermé et l&#39;élève reviendra au contexte du cours.

**Comportement réactif pour le contenu mobile et de PDF**

Dans les fenêtres plus petites (par exemple, d’une largeur d’environ 320 px), le libellé Suivant peut être raccourci ou masqué, en affichant uniquement l’icône, afin d’éviter tout chevauchement avec les contrôles du PDF.

Pour les modules de PDF, le lecteur ajuste les contrôles sur une ligne distincte, de sorte que les étiquettes de navigation et les contrôles de PDF n’interfèrent pas les uns avec les autres.

**Administrateur > Identité visuelle > Aperçu du lecteur** mis à jour

L’aperçu du lecteur dans Admin > Identité visuelle reflète désormais le nouveau libellé, par exemple Module suivant : Leçon 2. Cela permet aux administrateurs de voir le comportement de navigation mis à jour.

### Principaux avantages

**Navigation plus claire pour les élèves**

Les élèves n&#39;ont plus à deviner ce qui se passera lorsqu&#39;ils sélectionneront « Suivant ». L&#39;étiquette précise clairement ce qui suit, qu&#39;il s&#39;agisse d&#39;un module ou d&#39;un cours. Cette réduction de l’ambiguïté permet d’atténuer l’hésitation et la confusion, en particulier dans les grands publics d’éducation des clients où de nombreux élèves peuvent ne pas être familiarisés avec les interfaces LMS.

**Taux d’achèvement des cours plus élevés**

Le fait de définir clairement l&#39;étape suivante (Module suivant : {ModuleName}) et d&#39;ajouter une action de sortie distincte pour le module final réduit la probabilité que les élèves abandonnent le cours ou négligent la dernière étape d&#39;achèvement.

**Expérience utilisateur plus prévisible sur tous les appareils**

Les libellés mis à jour s’alignent sur le comportement et les icônes Suivant ou Précédent sur les ordinateurs de bureau, les tablettes et les appareils mobiles. Les contraintes de mise en page sont respectées sur tous les appareils et dans tous les flux de PDF afin que les commandes restent utilisables et accessibles.

Cela est particulièrement important pour les implémentations sans en-tête où le lecteur Fluidic est intégré dans une expérience d’apprentissage personnalisée.

### Cas d’utilisation

**Portails d’éducation pour les clients et les partenaires (sans interface utilisateur ou intégré à AEM)**

Comptes utilisant Adobe Learning Manager dans une configuration sans en-tête, dirigeant les élèves à partir de canaux de marketing externes. Ces élèves :

* Consomment souvent du contenu vidéo en longues séquences.

* Attendez-vous à une expérience de style curriculum où le système indique clairement le prochain épisode/module.

Dans ces environnements, le libellé **Module suivant :{ModuleName}** :

* Renforce la nature guidée du voyage.

* Réduit la dépose entre les modules.

**Cours de conformité et de certification avec modules commandés**

Dans les scénarios réglementés ou à forte conformité :

* Les élèves doivent terminer une séquence stricte de modules.

* Les auteurs désactivent souvent la table des matières pour éviter de l’ignorer.

Ici, affichage du **Module suivant :{ModuleName}** :

* Confirme aux élèves qu’ils suivent la bonne séquence.

* Réduit la probabilité qu’ils interprètent mal l’action suivante et quittent l’action plus tôt que prévu.

**Parcours d’apprentissage où les cours se suivent**

Où les parcours d’apprentissage ou équivalents enchaînent plusieurs cours. Ceci est utile lors de la création de séquences de style curriculum pour un large public.

**Consommation mobile en premier**

Pour les élèves utilisant principalement un téléphone ou une tablette :

* Les étiquettes mises à jour et le comportement réactif garantissent que la navigation reste compréhensible sans dépendre de minuscules icônes proches ou de contrôles masqués.

* Cela est important pour l’éducation des clients, les travailleurs à la demande ou les élèves de première ligne qui peuvent accéder au contenu lors de courtes sessions sur des appareils mobiles.

## Connecteur Zoom : créez plusieurs sessions Zoom simultanées.

### Présentation

La mise à niveau du connecteur Zoom améliore la façon dont Adobe Learning Manager gère la formation virtuelle dirigée par un instructeur (VILT). Auparavant, les utilisateurs ne pouvaient créer qu’une seule session Zoom à la fois. Avec la nouvelle mise à jour, les administrateurs et les auteurs peuvent planifier plusieurs sessions Zoom en même temps à l’aide de l’intégration standard.

### Nouveautés

#### Prise en charge de plusieurs sessions Zoom simultanées via le connecteur

* Le connecteur Zoom permet désormais de créer plusieurs sessions VILT à la même date/heure à partir d’ALM.

* La logique de planification n’applique plus une contrainte « réunion Zoom à la fois » au niveau du compte/connecteur.

* Les administrateurs et les auteurs peuvent configurer des sessions VILT qui se chevauchent (par exemple, des salles de classe régionales, des pistes parallèles ou des sessions répétées pour différents groupes de partenaires) sans solutions de contournement.

#### Les réunions sont créées à l’aide de l’identité Zoom de l’instructeur (pas du super administrateur Zoom).

Pour prendre en charge les réunions simultanées en toute sécurité, le connecteur a été mis à jour afin que :

* Les réunions Zoom sont désormais créées à l’aide de l’adresse e-mail de l’instructeur, au lieu de l’adresse e-mail du super administrateur Zoom.

* Le compte Zoom de chaque instructeur peut organiser ses propres réunions en parallèle avec d’autres instructeurs, sous réserve des limites de la formule Zoom existante.

**Remarque** :

* Un seul instructeur par réunion est toujours pris en charge.

* Si l’adresse e-mail d’un instructeur est mise à jour ultérieurement dans Adobe Learning Manager, les réunions existantes restent associées à l’adresse e-mail d’origine utilisée lors de la création.

#### Fini le collage manuel d’URL Zoom pour les sessions simultanées

Auparavant, lorsqu’une deuxième ou troisième session Zoom devait s’exécuter en même temps :

* Les auteurs devaient créer manuellement des réunions Zoom en dehors d&#39;ALM, puis coller l&#39;URL de jointure Zoom dans la configuration de l&#39;instance de cours.

* Cette opération était source d’erreurs et ne bénéficiait pas des fonctionnalités du connecteur telles que le suivi de l’assiduité.

Avec le connecteur mis à jour :

* Toutes les sessions peuvent être créées directement à partir de l’interface utilisateur ALM à l’aide du connecteur Zoom, même si elles se chevauchent dans le temps.

* Le cycle de vie de la session (création/annulation) continue d’être géré de manière centralisée via l’intégration.

### Principaux avantages

#### Meilleure planification VILT à grande échelle

Les organisations peuvent désormais :

* Organisez plusieurs salles de classe virtuelles sur Zoom en même temps (par exemple, des pistes parallèles lors d’un sommet virtuel, des cohortes régionales ou des sessions de formation distinctes pour les partenaires).

* Évitez les goulots d’étranglement qui obligeaient auparavant les administrateurs à sérialiser les sessions ou à recourir à la gestion manuelle du zoom.

#### Frais généraux d’administrateur et d’auteur réduits

L’amélioration élimine :

* Création manuelle de réunions Zoom en dehors de Adobe Learning Manager.

* Copiez-collez les URL de zoom dans chaque instance de cours pour les sessions qui se chevauchent.

* Risque de liens mal configurés, de mauvaises réunions jointes ou de suivi de présence manqué.

Les administrateurs et les auteurs peuvent gérer toutes les sessions Zoom à partir de Adobe Learning Manager, à l’aide de workflows familiers.

#### Meilleur alignement avec la mise en service du zoom et les rôles d’instructeur

En associant des réunions à des comptes Zoom d’instructeur individuels :

* Chaque instructeur peut utiliser ses propres limites de licence Zoom.

* Les organisations peuvent utiliser leur modèle de provisionnement Zoom existant (un compte par formateur, par BU, etc.) tout en s’intégrant pleinement à Adobe Learning Manager.

* Cela évite le goulot d’étranglement d’un point unique lors de l’utilisation d’un utilisateur Zoom super-administrateur partagé pour toutes les sessions.

### Cas d’utilisation

#### Événements et sommets virtuels multipistes

Les équipes de formation des clients qui organisent de grands événements (par exemple, des camps d’entraînement sur les produits, des sommets de partenaires ou des semaines de certification) peuvent :

* Configurez plusieurs sessions basées sur Zoom dans le même créneau horaire (pour différentes pistes ou rubriques).

* Gérez-les tous en tant que modules VILT sous les cours et parcours d’apprentissage de Adobe Learning Manager.

* Offrez aux élèves une expérience unifiée pendant que le connecteur gère toutes les créations de réunions Zoom sous-jacentes.

#### Formation internationale des partenaires et des clients

Les organisations qui forment des clients et des partenaires dans toutes les régions peuvent :

* Organisez des sessions Zoom distinctes pour la zone EMEA, l’APAC et les Amériques à des heures qui se chevauchent pour correspondre aux heures de travail locales.

* Évitez de forcer un seul créneau horaire global ou une configuration de zoom manuelle pour les cohortes supplémentaires.

#### Activation interne

Les équipes d’activation internes (ventes, support, etc.) peuvent :

* Planifiez des sessions d’intégration parallèles ou des groupes en fonction des rôles (par exemple, des salles Zoom séparées pour les développeurs, les administrateurs et les parties prenantes de l’entreprise) dans ALM.

* Conservez toutes les sessions dans le modèle VILT d’ALM à des fins de reporting et de conformité, plutôt que de passer partiellement à des réunions Zoom non gérées.

## Afficher l&#39;auteur d&#39;origine des cours partagés dans les comptes de pairs

### Présentation

Lorsqu&#39;un cours est partagé via le catalogue avec un compte de pairs, Adobe Learning Manager nomme actuellement l&#39;auteur « Auteur externe » dans les vues Élève, Administrateur et Auteur du compte de réception. Cela peut poser des problèmes aux élèves et aux administrateurs, en particulier dans les grandes entreprises, car il devient difficile d’identifier et de contacter le propriétaire de contenu approprié lorsque des problèmes ou des questions surviennent.

L’amélioration garantit que les informations sur l’auteur sont conservées et affichées pour les cours partagés dans les comptes de pairs, plutôt que remplacées par un espace réservé générique.

### Nouveautés

Afficher le nom réel de l&#39;auteur pour les cours partagés dans les comptes de pairs

Pour les cours partagés via des catalogues externes ou de pairs, le nom de l’auteur d’origine du compte source s’affiche désormais dans le compte de réception au lieu de « Auteur externe ».

Cela s’applique :

* Application de l’élève (carte de cours ou détails du cours).

* Vues Administrateur et Auteur lors de la prévisualisation en tant qu’élève.

### Principaux avantages

#### Visibilité directe du propriétaire pour le contenu partagé

Les élèves et les administrateurs des comptes de pairs peuvent désormais :

* Découvrez qui a créé le cours, même lorsqu&#39;il est acquis via un catalogue partagé.

* Évitez l’étiquette générique et inutile « Auteur externe ».

#### Expérience multi-locataires et compte de pairs plus cohérente

Pour les clients exécutant des scénarios multi-locataires ou d’entreprise étendue :

* Le même cours apparaît avec une image de marque cohérente de l’auteur sur tous les comptes.

* L’expérience de l’élève correspond aux attentes du compte principal (par exemple, voir le nom de l’auteur du compte source au lieu de « Auteur externe »).

### Cas d’utilisation

#### Grande entreprise avec comptes de pairs

L’entreprise utilise ALM avec :

* Un compte principal qui possède les cours canoniques, et

* Comptes de pairs qui acquièrent du contenu via des catalogues partagés.

Les élèves des comptes de pairs doivent savoir quelle équipe d&#39;entreprise a créé un cours pour acheminer correctement les questions ou les suggestions d&#39;amélioration.

Grâce à cette amélioration :

* Les cours partagés affichent désormais le nom d’auteur d’entreprise correct dans les comptes de pairs.

* La charge de support interne de l’entreprise est réduite, car les élèves et les administrateurs locaux savent qui contacter.

#### Partage multi-BU interne

Lorsqu’une unité commerciale organise l’apprentissage pour d’autres :

* La BU propriétaire peut être identifiée dans le champ Auteur sur tous les comptes consommateurs.

* Les administrateurs L&amp;D locaux peuvent rapidement voir si un cours est maintenu localement ou par une autre entité organisationnelle, et collaborer en conséquence.

## Exposer la date d&#39;expiration de l&#39;objet d&#39;apprentissage (retrait automatique) dans les API des élèves

### Présentation

Cette amélioration rend la date de retrait automatique d&#39;un objet d&#39;apprentissage (LO) disponible directement via les API de Adobe Learning Manager destinées aux élèves. Lorsqu’un cours, un parcours d’apprentissage ou une certification est configuré avec une date d’expiration ou de retrait automatique, ces informations font désormais partie des données d’objet d’apprentissage renvoyées par les points de terminaison clés de l’élève.

### Nouveautés

#### Nouveau champ d’expiration/retrait automatique dans les API de l’objet d’apprentissage de l’élève

* Les API d’objet d’apprentissage de l’élève (par exemple, les points de terminaison qui renvoient des objets d’apprentissage à l’expérience de l’élève et à des plateformes externes) incluent désormais la date d’expiration de l’objet d’apprentissage (date de retrait automatique configurée pour cet objet d’apprentissage).

* Ce champ est renvoyé comme faisant partie de l’entité objet d’apprentissage dans les réponses telles que :

   * Obtenir l’objet d’apprentissage (détails LO).

   * Données d’objet d’apprentissage utilisées pour remplir la page d’accueil de l’élève, le catalogue et les résultats de recherche.

* Le champ complète l’échéance d’achèvement existante qui existe déjà au niveau de l’instance ; le nouveau champ est spécifiquement la date de retrait automatique au niveau de l’objet d’apprentissage.

#### Disponibilité dans les expériences d’élève basées sur la recherche

La date d’expiration étant affichée dans le cadre de la représentation d’objet d’apprentissage soutenue par la recherche, elle est désormais disponible partout où ALM ou une plate-forme externe utilise :

* rechercher des API ou

* catalogues et suggestions basés sur la recherche pour construire des vues d’élève.

**Portée et exclusions**

L’amélioration s’applique uniquement aux API des élèves.

### Principaux avantages

#### Expérience d’élève avec expiration dans les LXP personnalisés

Pour les grandes et moyennes entreprises, leur LXP personnalisé peut désormais obtenir des informations d’expiration d’objet d’apprentissage directement auprès d’ALM, ce qui leur permet de :

* Afficher les étiquettes « Expiration le {date} » ou « Bientôt expirée » sur les cartes de cours et les pages de détails.

* Communiquez avec l&#39;urgence plus clairement, afin que les élèves donnent la priorité à la formation qui est sur le point de prendre sa retraite.

Cela est particulièrement important pour la conformité ou la formation produit limitée dans le temps, où les objets d’apprentissage sont régulièrement actualisés et les versions plus anciennes sont retirées.

#### De meilleurs conseils pour les élèves sur les formations à suivre dès maintenant

En exposant l’expiration de l’objet d’apprentissage, l’expérience de l’élève peut :

* Mettez en surbrillance les cours qui sont toujours valides et ceux qui sont sur le point d’être retirés.

* Aidez les élèves à éviter de s&#39;inscrire à des formations qui ne seront plus disponibles ou valides dans un proche avenir.

#### Cohérence avec les données d’échéance d’achèvement existantes

Auparavant, les API de l’élève affichaient déjà le délai d’achèvement au niveau de l’instance, mais pas la date de retrait automatique au niveau de l’objet d’apprentissage. Avec cette modification :

Les aspects suivants d’une formation sont disponibles :

* « Quand dois-je terminer cette instance ? » (échéance d’achèvement).

* « Jusqu&#39;à quand cette formation est-elle offerte ? » (date de retrait automatique/d’expiration).

### Cas d’utilisation

#### Une entreprise mondiale avec une gestion stricte du cycle de vie des cours

Les entreprises qui retirent et remplacent régulièrement des cours (par exemple, des mises à jour réglementaires, de produits ou de méthodologies) peuvent :

* Évitez toute confusion chez l’élève quant à la suppression progressive d’une formation.

* Dirigez les élèves vers les offres les plus récentes et les plus durables.

Leurs portails personnalisés et leurs outils internes peuvent désormais lire la date d’expiration directement à partir d’ALM via les API des élèves.

#### Académies clients ou partenaires externes

Pour la formation des clients et des partenaires, les pages marketing et les portails mettent souvent l’accent sur la formation la plus récente.

La présence de dates d’expiration dans l’API LO permet aux créateurs d’expérience :

* Masquez ou atténuez l’accent mis sur le contenu qui est proche de la retraite.

* Créez des campagnes « Dernière chance de terminer ».

## Définir une restriction sur l&#39;heure de début du module

### Présentation

L’amélioration permet aux auteurs et aux administrateurs de Adobe Learning Manager de définir une fenêtre temporelle pendant laquelle les élèves sont autorisés à démarrer un module. En dehors de la fenêtre de début/fin configurée, le module reste visible dans la structure du cours, mais les élèves ne peuvent pas le lancer.

Cette fonctionnalité est essentielle pour les utilisateurs qui ont besoin d’un contrôle plus strict sur le moment où certains contenus deviennent disponibles ou doivent cesser d’être initiés, par exemple, dans le cadre de programmes à durée déterminée, de formations en cohorte ou d’exercices à durée déterminée.

### Nouveautés

Les auteurs peuvent désormais configurer, au niveau du module dans un cours, une date/heure de début et une date/heure de fin qui régissent le moment où les élèves sont autorisés à lancer ce module. Dans cette fenêtre, le module se comporte comme d&#39;habitude : avant l&#39;heure de début ou après l&#39;heure de fin, l&#39;élève voit le module dans l&#39;aperçu du cours mais ne peut pas le démarrer.

La configuration apparaît dans l&#39;interface utilisateur de création de cours sous forme de commandes de planification supplémentaires pour des types de module spécifiques, tels que le contenu d&#39;auto-apprentissage, les quiz ou les activités. Les administrateurs peuvent utiliser ces commandes pour créer des modules qui s’ouvrent par phases ou pour empêcher les démarrages tardifs dans les programmes où le contenu doit être consommé dans un délai défini.

#### Principaux avantages

Le principal avantage est la possibilité de contrôler quand les modules sont accessibles. Les équipes de formation peuvent synchroniser la disponibilité des modules avec des événements réels, tels que les lancements de nouveaux produits, les délais réglementaires et les programmes internes. Cela garantit que les élèves terminent le contenu prérequis avant de pouvoir accéder aux modules suivants.

Par exemple, la cohorte 1 peut accéder au module 2 uniquement au cours de la semaine 2, tandis que le module 3 reste verrouillé jusqu’à la semaine 3, éliminant ainsi la nécessité de masquer et d’afficher manuellement le contenu ou de créer des versions de cours distinctes.

Cela améliore l’expérience de l’élève : au lieu de faire face à des modules qui sont techniquement accessibles mais qui ne devraient pas l’être à ce moment-là (ou qui devraient déjà être terminés), les élèves voient une structure de cours où les modules qu’ils sont autorisés à commencer sont clairement alignés sur le calendrier prévu.

#### Cas d’utilisation

* **Programme d&#39;accompagnement par cohorte** : dans ce programme, chaque semaine ouvre un nouveau module. Le contenu de la semaine 1 est disponible immédiatement, tandis que la semaine 2 est visible, mais ne peut pas être démarrée avant une date spécifiée. La semaine 3 suit le même processus de contrôle. Les élèves peuvent voir l’intégralité du parcours d’apprentissage, mais le système contrôle à quel moment ils peuvent réellement commencer chaque étape.

* **Formation sur un produit ou une campagne limitée dans le temps** : les équipes marketing ou produit peuvent créer un module de formation qui n’est accessible que lorsqu’une campagne est active ou lorsqu’une version spécifique d’un produit est toujours disponible. Cette fenêtre de début désignée permet de s&#39;assurer que les élèves ne commencent pas un module sur une version de produit retirée après l&#39;heure de fin spécifiée.

* **Environnements d’évaluation ou d’examen** : les organisations peuvent ouvrir un module (tel qu’un test) pendant une courte période bien définie (par exemple, « vous pouvez commencer l’examen à tout moment entre 9:00 et 12:00 à une date donnée »). Les élèves ne peuvent pas commencer l&#39;examen en dehors de cette fenêtre, ce qui permet un planning équitable entre les fuseaux horaires et les cohortes.

## Contrôle du langage du lecteur via le paramètre LTI personnalisé

### Présentation

L’amélioration permet aux plateformes externes utilisant LTI (Learning Tools Interoperability) de spécifier la langue du contenu Adobe Learning Manager au moment du lancement. Au lieu de dépendre de l&#39;élève pour changer la langue dans le lecteur Fluidic, le consommateur LTI peut envoyer un code de langue via un paramètre LTI personnalisé. Adobe Learning Manager utilisera ensuite ce code pour sélectionner la variante de langue appropriée.

### Nouveautés

Les plateformes externes qui agissent comme des consommateurs LTI peuvent désormais transmettre un paramètre de langue personnalisé (et les paramètres de lecteur associés) lors du lancement du contenu ALM. ALM lit ce paramètre et :

* Définit la langue du lecteur en conséquence.

* Lance la variante de langue correspondante du module, lorsque du contenu multilingue est configuré.

Cela signifie qu’un nouvel élève, qui sélectionne Français sur la plateforme externe, verra le lecteur et le module ALM se lancer directement en français, sans avoir à ajuster quoi que ce soit à l’intérieur d’ALM.

L’amélioration s’adapte également aux scénarios dans lesquels la plateforme externe traite ALM comme un lecteur de contenu sans en-tête. Par exemple, il permet de masquer les éléments de navigation et la table des matières (TDM) en envoyant des paramètres personnalisés supplémentaires pour ajuster certains paramètres de l’interface utilisateur. Ces paramètres fonctionnent en conjonction avec le paramètre de langue, ce qui permet à la plate-forme externe de fournir une expérience de marque fluide tout en utilisant ALM pour la lecture et le suivi.

### Principaux avantages

* **Expérience linguistique cohérente entre les systèmes** : lorsqu&#39;un élève sélectionne une langue dans le portail externe, ce choix est immédiatement reflété dans ALM. Cela garantit que les élèves ne sont confrontés à aucune incompatibilité entre la langue du portail et le cours. Par conséquent, ils n’auront pas besoin de rechercher un changement de langue dans le lecteur.

* **Rapports spécifiques à la langue** : dans leur plateforme, la sélection de la langue est cohérente avec ALM, ce qui améliore la précision de leurs analyses et le suivi des élèves. Cet alignement prend également en charge les configurations dans lesquelles les commandes de langue propres à ALM sont intentionnellement désactivées ou masquées dans le lecteur Fluidic pour des cours spécifiques. Dans ces cas, la plateforme externe sert de source unique de vérité pour le langage.

### Cas d’utilisation

* Un cas d’utilisation important implique les grandes entreprises qui utilisent des intégrations LTI. Les élèves s&#39;inscrivent et sélectionnent d&#39;abord une langue sur la plateforme. Ils lancent ensuite des sessions de formation ALM via LTI. Grâce à cette amélioration, lorsqu’un élève sélectionne l’espagnol, le module ALM s’ouvre automatiquement en espagnol. Cela signifie que les élèves n’ont pas besoin d’ajuster les paramètres de langue dans ALM. En outre, les rapports basés sur la langue restent cohérents avec ce que les élèves voient et expérimentent dans ALM.

* Une autre application est la fourniture d’expériences de cours sans interface utilisateur au sein d’un portail client ou partenaire. Dans cette configuration, le portail peut incorporer du contenu ALM à l’aide d’un iframe, tandis que toutes les expériences utilisateur de navigation et de langue (UX) sont gérées en dehors d’ALM. En utilisant des paramètres LTI personnalisés, le portail peut s&#39;assurer que le lecteur ALM est affiché dans la langue appropriée et que tous les éléments inutiles de l&#39;interface utilisateur (tels que la table des matières et les boutons de navigation) sont masqués. Cela permet aux élèves de percevoir une application unique et cohérente plutôt qu’une collection d’outils disparate.

* Ceci est avantageux pour les organisations qui effectuent une formation à grande échelle dans plusieurs langues à l’aide d’un autre LMS ou d’une plate-forme d’apprentissage. Ils peuvent standardiser leur utilisation de cette plateforme pour gérer les profils d’élèves, sélectionner des paramètres régionaux et présenter des catalogues. Dans le même temps, ALM sert de moteur de contenu et de suivi fiable, respectant les préférences linguistiques et les interactions utilisateur spécifiées par le système externe lors de chaque lancement LTI.

## Pondération des questions de la liste de contrôle pour les évaluations des instructeurs

### Présentation

L’amélioration introduit des listes de contrôle pondérées, permettant aux instructeurs et aux responsables d’évaluer les élèves à l’aide d’échelles notées et de scores totaux, plutôt que de traiter chaque question de liste de contrôle comme étant égale. L&#39;objectif est de faciliter la création de listes de contrôle en mettant en œuvre des évaluations pondérées des questions, ce qui permet de refléter l&#39;importance relative des différentes actions ou compétences dans une seule liste de contrôle.

### Nouveautés

Les listes de contrôle prennent en charge les types suivants :

1. Oui/Non
Le comportement reste le même qu&#39;aujourd&#39;hui : chaque question est Oui/Non et les critères de réussite sont basés sur le nombre de réponses « Oui ».

2. Questions de même poids

   * Les questions sont notées sur une échelle numérique (de 0 à 10 par défaut), où :

      * Les valeurs max/min de l’échelle sont personnalisables au niveau de la liste de contrôle.

      * L’échelle peut désormais commencer à 0 (le score minimum précédent était de 1).

   * Toutes les questions partagent le même score maximum, la liste de contrôle se comporte donc comme une échelle de notation uniforme pour chaque question.

3. Questions de poids différent

   * Chaque question a son propre score maximum (poids).

   * Les critères de réussite dépendent du pourcentage du score total possible que l’élève obtient sur la liste de contrôle (par exemple, « réussite si l’élève obtient ≥ 70 % du score total disponible »).

Pour tous les types de listes de contrôle :

* Le **réviseur** (instructeur ou responsable) évalue l’élève en fonction du type de liste de contrôle configuré :

   * Sélectionnez Oui/Non.

   * Sélectionnez des scores sur l’échelle définie.

* Le rapport **Liste de contrôle** est mis à jour pour inclure, pour les questions avec une pondération différente :

   * Score maximal pour chaque question.

   * Score obtenu par chaque élève pour cette question.

Cela permet d’analyser les performances globales et les performances spécifiques aux questions en fonction des pondérations prévues.

### Principaux avantages

* **Évaluations plus riches et plus réalistes** : les instructeurs peuvent refléter les priorités du monde réel en accordant plus de points aux comportements critiques et moins de points aux comportements mineurs, tout en utilisant un workflow de liste de contrôle adapté aux tâches observées ou pratiques.

* **Réussite/échec total basé sur le score** : les évaluations peuvent être basées sur le score total en pourcentage, et pas seulement sur le nombre de questions qui dépassent un seuil, en s&#39;alignant plus étroitement sur les schémas de compétence ou de notation types.

* **Amélioration des rapports** : les rapports de liste de contrôle mis à jour exposent le score maximal et le score obtenu par question, ce qui permet aux propriétaires du programme et aux équipes qualité d’identifier les points faibles spécifiques et d’affiner les conseils de formation ou d’évaluation.

### Cas d’utilisation

* **Évaluations des compétences de l’entreprise** : les ingénieurs sont évalués via des listes de contrôle pratiques basées sur des scénarios, où certaines étapes de diagnostic ou de communication doivent avoir plus de poids que les étapes cosmétiques ou à faible risque. Les questions pondérées et les critères de réussite du score total rendent ces évaluations plus crédibles et prédictives du rendement réel.

* **Observations de sécurité et de conformité** : dans le secteur de la santé, de la fabrication ou de l&#39;assistance sur site, les étapes de sécurité critiques peuvent obtenir des scores maximaux plus élevés, ce qui garantit que le fait de ne pas effectuer une action critique de sécurité a un impact plus important sur le score total que le fait de ne pas effectuer une étape procédurale mineure.

* **Coaching et étalonnage** : avec des scores max. et réalisés par question dans le rapport, les responsables peuvent voir exactement où les élèves sous-performent et calibrer les instructeurs sur la façon d&#39;obtenir des scores cohérents.

## Liste de contrôle avec possibilité de commentaire pour le réviseur

### Présentation

L&#39;amélioration introduit une fonction de commentaire pour les évaluations de listes de contrôle, permettant aux réviseurs, tels que les instructeurs et les gestionnaires, de fournir une rétroaction qualitative parallèlement aux notes numériques. Ce retour d’informations peut être rendu visible aux élèves si nécessaire.

L&#39;objectif est d&#39;appuyer les évaluations fondées sur des listes de contrôle où la rétroaction des mentors est aussi cruciale que le résultat numérique. Il s’agit notamment de mettre en évidence des points forts spécifiques, des points à améliorer ou de fournir le contexte pour la note donnée.

Aujourd’hui, les réviseurs peuvent :

* Évaluez une liste de contrôle pour chaque élève, question par question.

* Afficher les résultats et réévaluer les élèves qui ont échoué.

Dans des scénarios réels, comme l&#39;aviation, les formateurs sur le terrain évaluent les agents des ateliers et le personnel des aéroports. De même, les formateurs et les mentors des petites et moyennes entreprises (PME) utilisent souvent des listes de contrôle pour évaluer les performances au travail. Cependant, ces listes de contrôle ne comprennent généralement pas de section structurée pour recueillir les commentaires narratifs liés à l&#39;évaluation.

### Nouveautés

#### Options de création

Les auteurs peuvent configurer chaque liste de contrôle pour :

* Activer ou désactiver la fonctionnalité de commentaire pour les réviseurs.

* Décidez si le nom du réviseur doit être affiché aux élèves avec les commentaires.

Cela permet aux organisations d’adapter la visibilité des commentaires à leur culture et à leurs exigences de confidentialité.

#### Expérience du réviseur

Lorsque les commentaires sont activés :

* Les réviseurs (instructeurs/responsables) peuvent ajouter des commentaires facultatifs lors de l’évaluation d’une liste de contrôle.

* Ils peuvent choisir si les commentaires sont visibles par les élèves, en fonction des paramètres de la liste de contrôle.

S’ils réévaluent un élève, ils peuvent mettre à jour ou modifier les commentaires pour refléter la dernière évaluation.

#### Rapports et notifications

* Le rapport Liste de contrôle gagne une nouvelle colonne pour les remarques des réviseurs, capturant le commentaire fourni pendant l&#39;évaluation.

* Les élèves reçoivent des notifications (sur la plateforme et par e-mail) chaque fois qu’une évaluation de liste de contrôle se produit. Ces notifications comprennent :

   * Le commentaire et

   * Le nom du réviseur, s’il a été configuré pour être visible.

Cela permet de s’assurer que les commentaires sont non seulement stockés, mais également activement transmis aux élèves.

### Principaux avantages

* **Retour d&#39;informations plus riche et similaire à celui d&#39;un coach** : les scores numériques sont complétés par des remarques contextuelles, ce qui fait des listes de contrôle un outil plus efficace pour le coaching, pas seulement pour la conformité.

* **Traçabilité et auditabilité** : les organisations obtiennent un enregistrement permanent des personnes qui ont évalué qui, quand et ce qu&#39;elles ont dit, ce qui est important dans les environnements réglementés et les rôles à enjeux élevés.

* **Meilleur engagement des élèves** : les élèves reçoivent des conseils clairs liés à des évaluations spécifiques, ce qui améliore leur compréhension des attentes et des étapes ultérieures.

### Cas d’utilisation

* Les organisations dont les environnements sont réglementés peuvent utiliser les commentaires pour documenter le jugement clinique ou la rétroaction procédurale du personnel qui est observé sur le terrain.

* Les organismes d&#39;aviation et d&#39;assistance en escale peuvent joindre des notes détaillées sur le rendement opérationnel, les pratiques de sécurité et le comportement vis-à-vis des clients, transformant ainsi une liste de contrôle en un outil de compte rendu structuré.

* Dans le mentorat et l&#39;évaluation des experts, les instructeurs peuvent saisir des observations nuancées qui ne cadreraient pas avec un score seul, par exemple, « ont bien géré l&#39;escalade, mais doivent améliorer la gestion du temps » ou « un excellent flux de dépannage ; ont manqué une étape de documentation ».

## Tentatives multiples au niveau du contenu et rapports de quiz

### Présentation

>[!IMPORTANT]
>
>Notez que la fonctionnalité ne sera disponible qu’après son activation dans le compte. Contactez le support ALM.


Actuellement, ALM prend en charge plusieurs tentatives au niveau du système de gestion de l’apprentissage via la fonctionnalité de tentatives de quiz multiples (MQA) :

* Les auteurs peuvent configurer les tentatives au niveau du cours (appliqué à tous les modules du cours qui répondent au quiz) ou au niveau du module (par module de quiz).

* Les tentatives peuvent être les suivantes :

   * Un nombre spécifique (par exemple, 3 tentatives), ou

   * Tentatives infinies, contrôlées au niveau du LMS.

* Lorsqu’un élève utilise un module via le lecteur Fluidic, puis ferme le lecteur ou termine le module, cette session est traitée comme une tentative LMS unique.

* Chaque tentative de LMS est capturée dans le rapport de quiz L2 sous la forme d’une nouvelle ligne.

Cependant, si le fichier de contenu lui-même (par exemple, un quiz Articulate SCORM) implémente sa propre logique de tentatives multiples, le rapport de quiz L2 d&#39;ALM ne distingue pas ou ne suit pas correctement ces tentatives internes.

Cette amélioration introduit le suivi des tentatives multiples au niveau du contenu pour les quiz, permettant à Adobe Learning Manager de capturer avec précision chaque tentative dans le contenu lui-même dans le rapport de quiz L2. Il est conçu pour les situations où l&#39;outil de création de contenu (tel qu&#39;Articulate SCORM) gère indépendamment les tentatives de quiz. Grâce à cette fonctionnalité, les tentatives sont correctement reflétées dans les rapports ALM sans dépendre des paramètres de Tentative de quiz multiple (MQA) au niveau du LMS.

### Nouveautés

#### Indicateur Auteur pour les tentatives au niveau du contenu

* Lors du chargement de contenu dans la bibliothèque de contenu, les auteurs peuvent désormais indiquer qu’un fichier de contenu spécifique a plusieurs tentatives intégrées.

* Il s&#39;agit d&#39;un paramètre par contenu qui indique à ALM de traiter les tentatives définies dans le contenu comme source de vérité.

#### Comportement du cours/module

Lorsque ce contenu est utilisé dans un cours :

* Le module déduira ses tentatives du contenu, et non du LMS MQA.

* Les élèves ne verront qu’une seule tentative au niveau du LMS :

   * La vue de présentation du cours et du module n’affiche pas de bouton « retenter » LMS pour ce module.

   * La gestion des tentatives (par exemple, les nouvelles tentatives dans le quiz) est régie par le contenu lui-même.

#### Rapports

Le rapport de quiz L2 traite chaque tentative au niveau du contenu comme une ligne de tentative distincte :

* Chaque tentative de quiz interne configurée dans le contenu apparaît sous la forme de sa propre ligne dans le rapport de quiz L2, comme le sont les tentatives au niveau du LMS aujourd’hui.

* Le format de chaque ligne reste identique aux lignes à tentatives multiples existantes dans les rapports L2 (mêmes colonnes, structure et sémantique).

* Cela offre une expérience de reporting cohérente :

   * Que les tentatives soient contrôlées par le LMS MQA ou par le contenu, le rapport de quiz L2 affiche une ligne par tentative.

#### Principaux avantages

* Historique précis des tentatives pour les quiz SCORM où les tentatives sont contrôlées en interne par des outils comme Articulate, sans forcer la configuration MQA au niveau du LMS.

* Amélioration de l’expérience de l’élève : pour les tentatives contrôlées par le contenu, les élèves ne voient qu’un seul emplacement au niveau du LMS et n’ont pas besoin d’interagir avec les commandes de nouvelle tentative du LMS ; toutes les nouvelles tentatives sont gérées dans l’interface utilisateur de quiz qu’ils connaissent déjà.

* Architecture flexible : les utilisateurs peuvent choisir si ALM MQA ou les tentatives au niveau du contenu doivent piloter le comportement par module, en fonction de la façon dont leur contenu a été créé et de la façon dont ils préfèrent gérer les tentatives.

* Modèle de rapport cohérent : les utilisateurs en aval du rapport de quiz L2 peuvent traiter chaque ligne comme une « tentative », quelle que soit l’origine de la logique de tentative.

#### Cas d’utilisation

* Les organisations qui utilisent Articulate SCORM peuvent conserver une logique de quiz autonome dans le package SCORM tout en réalisant un reporting précis au niveau des tentatives dans ALM sans configuration LMS supplémentaire.

* Les organisations qui utilisent le contenu SCORM fourni par le fournisseur peuvent éviter d’avoir à modifier ou à mettre en œuvre une logique de tentatives et de tentatives supplémentaires avec l’authentification fondée sur les connaissances (MQA) au niveau du LMS.

## Codes QR de l&#39;instructeur pour l&#39;inscription et la présence à la session d&#39;instance

### Présentation

Cette amélioration permet aux instructeurs de générer des codes QR eux-mêmes pour :

* Inscription à l’instance de cours,

* Participation à la session, ou

* Inscription + participation ensemble

au niveau de la session. Il est conçu pour les situations où les élèves entrent dans une classe physique ou hybride et ont besoin d&#39;une option rapide et en libre-service pour s&#39;inscrire et enregistrer leur présence à l&#39;aide d&#39;un code QR.

### Nouveautés

#### Codes QR générés par l’instructeur

* Les instructeurs peuvent générer des codes QR au niveau de la session pour :

   * S’inscrire dans l’instance : les élèves scannent pour s’inscrire dans l’instance qui inclut la session actuelle.

   * Marquer la présence à la session : les élèves numérisent pendant/après la session pour enregistrer la présence pour cette session spécifique.

   * S’inscrire dans l’instance + marquer la participation à la session : un code QR combiné pour les participants qui ne sont pas encore inscrits et dont la participation doit être marquée en une étape.

* Les instructeurs peuvent exporter les codes QR dont ils ont besoin en fonction du scénario (inscription, assiduité ou les deux).

#### Packaging de code QR

Le PDF de code QR exporté comprend :

* Nom du cours

* Nom d’instance

* Nom de la session

Ils permettent aux instructeurs et aux coordinateurs d’identifier et d’imprimer facilement le code QR correct pour chaque session.

### Principaux avantages

* **Autonomie des instructeurs** : les instructeurs n’ont plus besoin d’attendre que les administrateurs créent des codes QR. Ils peuvent les générer directement pour chaque session, ce qui améliore l&#39;agilité et réduit les frais de coordination.

* **Meilleure logistique des salles de classe** : pour les audiences en salle de classe ou sur place (tels que les travailleurs sur le terrain, le personnel d&#39;atelier ou les participants externes), les instructeurs peuvent gérer l&#39;inscription et la présence sur place à l&#39;aide de codes QR.

* **Charge de travail administrative réduite** : les équipes d’administration peuvent se concentrer sur la configuration et la gouvernance au lieu de gérer les demandes de génération de code QR de routine pour chaque session.

### Cas d’utilisation

* Les organisations qui exécutent de gros volumes de sessions sur site (par exemple, la formation de professionnels sur les produits) peuvent permettre aux instructeurs d’imprimer des codes QR spécifiques à la session qui inscrivent et marquent la présence à l’aide d’une seule numérisation.

* Dans les formations sur la vente au détail, la fabrication et les soins de santé, où les élèves rejoignent souvent les sessions directement à partir de l&#39;étage ou sans pré-inscription, un code QR « Inscription + Présence » peut être placé à la porte. Cela permet aux élèves d&#39;accéder en libre-service à leur inscription et à leur assiduité via leurs téléphones.

* Les événements de formation pour les partenaires ou les clients permettent au formateur sur site de s&#39;adapter facilement aux changements de salle, aux sessions supplémentaires ou aux participants supplémentaires sans avoir à consulter l&#39;administrateur pour de nouveaux codes QR.

## Améliorations du Captivate et du lecteur ALM

### Présentation

Cette amélioration améliore l’expérience de lecture du contenu Adobe Captivate dans le lecteur Adobe Learning Manager (ALM), en particulier suite aux récentes modifications apportées à l’architecture du Captivate. L’objectif est de permettre aux élèves d’utiliser les modules de Captivate en mode natif dans ALM tout en veillant à ce que la navigation, le suivi d’achèvement et la prise de notes soient clairs, cohérents et fiables.

### Nouveautés

#### Expérience de table des matières unifiée

* Seule la table des matières ALM s’affiche sur le côté gauche du lecteur.

* La table des matières du Captivate est masquée lorsque le module est lu dans ALM.

* Cela élimine la duplication, garantit une source unique de vérité pour la navigation et libère l’espace de l’écran.

#### Commentaires sur l’achèvement visuel

* La table des matières ALM affiche des coches vertes (ou des repères visuels équivalents) indiquant que la diapositive est terminée.

* Au fur et à mesure que les élèves progressent dans les diapositives du Captivate, la table des matières ALM reflète les diapositives terminées, conformément aux attentes des élèves pour les joueurs du cours moderne.

#### Commandes de progression contextuelle

* Les commandes du lecteur s’adapteront en fonction du type de diapositive :

   * Pour les diapositives vidéo :

      * Affiche une barre de progression temporelle reflétant la lecture vidéo.

* Pour les diapositives non vidéo :

   * Afficher les commandes de navigation des diapositives (diapositive suivante/précédente, etc.) au lieu d&#39;une barre de temps non fonctionnelle.

      * Cela permet d’éviter d’afficher des commandes non pertinentes ou inopérantes sur certains types de diapositives.

#### Navigation simplifiée

* La barre de navigation du module (ALM) et la barre de navigation du cours séparées sont fusionnées en une seule barre intuitive.

* Cette navigation unifiée :

   * Distingue clairement le passage par le module Captivate du retour au niveau cours/module.

   * Réduit la confusion causée par plusieurs barres dont les objectifs se chevauchent.

#### Liaison de notes fiable

* Les annotations sont liées aux numéros des diapositives et non à la date et à l’heure.

* Cette modification :

   * Corrige les échecs d’exportation dus à des horodatages manquants ou incorrects.

   * Permet d’exporter les notes de manière cohérente en tant que PDF, avec un mappage fiable entre les notes et le contexte de diapositive auquel elles appartiennent.

### Principaux avantages

* Expérience plus propre et mono-joueur : les élèves interagissent avec une table des matières et un modèle de navigation, réduisant ainsi la confusion et la charge cognitive.

* Indications précises d’achèvement et de progression : les graduations de niveau diapositive et les contrôles contextuels aident les élèves à comprendre où ils sont et ce qui reste.

* Prise de notes et exportations plus fiables : en liant des notes aux diapositives au lieu d’horodatages fragiles, les utilisateurs retrouvent un workflow de prise de notes en PDF fiable, même avec un contenu de Captivate basé sur les diapositives.

* Workflow d’auteur préservé : les auteurs conservent la simplicité de la publication directe du Captivate vers ALM, tandis que les élèves bénéficient d’une expérience de lecture moderne et intégrée sans charges de création supplémentaires.

### Cas d’utilisation

* Les programmes d’activation qui s’appuient sur Captivate pour les simulations interactives peuvent déployer du contenu dans ALM, garantissant ainsi que la navigation, le suivi d’achèvement et les notes fonctionnent de manière cohérente pour les élèves.

* Les organisations qui utilisent Captivate comme outil principal de création de contenu peuvent maintenir la publication en un clic et éviter la confusion entre les tables des matières doubles et les contrôles non fonctionnels pour les élèves.

* Les organisations qui s’appuient sur les notes exportées à partir du contenu du Captivate dans ALM (pour le coaching, la conformité ou les enregistrements) peuvent accéder aux éléments suivants :

   * Les notes sont correctement liées aux diapositives.

   * Les PDF sont générés comme prévu.

## Amélioration du calcul du temps d’apprentissage passé dans les relevés de notes des élèves

### Présentation

Avec sa version d’avril 2026, Adobe Learning Manager a revu la façon dont il calcule le temps d’apprentissage dans les relevés de notes des élèves. Auparavant, la logique de création de rapports pouvait entraîner des temps inexacts si les élèves laissaient le lecteur ouvert sans s’engager avec le contenu, ce qui entraînait des différences. La nouvelle méthode suit désormais le temps actif en fonction de l’engagement de l’utilisateur, en particulier lorsque l’onglet est actif et lorsqu’il y a une activité de l’utilisateur. Cette modification permet d’obtenir des données plus précises.

Cette mise à jour améliore les rapports et les tableaux de bord, aidant les administrateurs à mieux garantir la conformité et à suivre les progrès des élèves. Après la publication, consultez vos relevés de notes des élèves pour voir ces améliorations.

La méthode de calcul mise à jour se concentre sur l’engagement réel, tel que la mise au point active de l’onglet et les interactions récentes de l’utilisateur, améliorant ainsi la précision des rapports de temps dans les domaines suivants :

* Relevés de notes des élèves (IU)
* Mesures du tableau de bord d’administration
* Rapports d&#39;inscription aux cours
* API et connecteurs

### Modifications

La colonne **Temps d&#39;apprentissage passé** dans les relevés de notes des élèves utilise désormais une logique améliorée pour calculer le temps avec plus de précision. Au lieu de simplement suivre les heures d&#39;ouverture/fermeture du lecteur, le système fait maintenant la distinction entre les périodes actives et inactives en fonction de l&#39;engagement de l&#39;utilisateur.

* **Temps actif** : temps pendant lequel l’élève est activement engagé (par exemple, sur l’onglet approprié, en effectuant des actions telles que le défilement ou le visionnage de vidéos).
* **Temps d&#39;inactivité** : temps pendant lequel l&#39;élève n&#39;est pas engagé (par exemple, changement d&#39;onglet, aucune activité pendant plus de 10 minutes), qui est exclu du total.

Cela s’applique à la plupart des types de module, à l’exception des modules SCORM, Captivate et XAPI, qui conservent la logique d’origine.

### Fonctionnement du logiciel

Le nouveau calcul varie selon le type de module :

* **Modules vidéo et audio** : actifs lorsque le contenu est lu, même si l’élève passe à un autre onglet. La mise au point sur la tabulation n’est pas requise pour le suivi du temps de lecture.
* **Modules statiques (PDF, PPT, Excel, etc.)** : actifs s&#39;ils se trouvent sur l&#39;onglet et exécutant des activités (déplacement de la souris, défilement, clic, saisie au clavier) au cours des 10 dernières minutes. S&#39;il n&#39;y a aucune activité pendant 10 minutes, il passe en mode inactif.
* **SCORM et Captivate** conservent la logique d&#39;ouverture/fermeture d&#39;origine.
* **xAPI** utilise désormais la détection de temps actif basée sur les onglets, où le temps est compté uniquement lorsque l&#39;onglet est actif. Notez que le contenu AICC **n&#39;est pas** pris en charge.
* **HTML, LTI et autre contenu** : peut varier. Vérifiez les relevés de notes des élèves pour plus d&#39;exactitude.

Le temps d’inactivité est soustrait, ce qui garantit que seul le temps d’engagement réel est signalé.

>[!NOTE]
>
>Si votre ordinateur portable passe en mode veille, le temps d’apprentissage peut ne pas être suivi correctement. En effet, le suivi d&#39;activité s&#39;interrompt lorsque le système est en veille et ne reprend qu&#39;au réveil de l&#39;ordinateur portable.


### Tableau récapitulatif

| **Type de module** | **Temps actif (compté)** | **Temps d’inactivité (exclu)** |
| --- | --- | --- |
| **Vidéo/Audio** | Temps de lecture | Non commencé ; terminé ; pause **\>10 min** |
| **Statique (PDF/PPT/DOC)** | Activité **et** active dans l&#39;onglet au cours des **10 dernières minutes** | Aucune activité **\>10 min** ; onglet inactif |
| **SCORM** | Heure indiquée par le runtime de contenu | Impossible de détecter l&#39;inactivité |
| **Captivate** | Durée basée sur les diapositives | Impossible de détecter l&#39;inactivité |
| **xAPI** | Onglet actif | Onglet inactif |
| **HTML** | Temps d’ouverture du lecteur avec l’onglet actif | Onglet inactif |
| **Producteur/Consommateur LTI** | Si le contenu LTI est lu dans le lecteur d&#39;ALM (c&#39;est-à-dire, qu&#39;ALM consomme du contenu LTI hébergé sur un autre LMS agissant en tant que producteur), alors cette logique de temps passé s&#39;applique.<br><br>Cependant, si le contenu est lu en dehors du LMS (c&#39;est-à-dire, que le contenu est hébergé dans ALM, alors ALM est le producteur, mais la lecture se produit dans un lecteur externe), cette partie de la logique de calcul du temps ne s&#39;applique pas.  <br>**Remarque** : le consommateur LTI n&#39;est pas pris en charge dans Adobe Learning Manager. | Onglet inactif |

**Remarque** :

* **Visites et sessions parallèles** : comptez comme actives lorsque les conditions ci-dessus sont remplies.
* **Tous les appareils, navigateurs et langues** : inclus ; une utilisation mobile hors ligne est ajoutée après la synchronisation.

### Avantages du nouveau calcul

* **Rapports précis** : élimine les durées excessives des joueurs sans assistance, offrant des durées d&#39;apprentissage réalistes.
* **Meilleure conformité** : prend en charge le suivi précis de la formation obligatoire (par exemple, l&#39;exigence mensuelle de 5 heures d&#39;une entreprise).
* **Tableaux de bord améliorés** : les graphiques d&#39;activité des utilisateurs et les rapports sur le temps passé reflètent désormais l&#39;engagement réel.
* **Données sur les élèves** : aide les administrateurs à identifier les progrès réels et à s’adresser aux élèves désengagés.

### Impact des rapports et analyses

* **Relevés de notes des élèves :** « Temps d&#39;apprentissage passé » reflète désormais **l&#39;engagement réel**.
* **Tableau de bord d&#39;administration :** les mesures qui incluent le temps (par exemple, les vignettes « temps passé », les tendances) affichent des valeurs **plus basses mais plus réalistes** dans les scénarios où le temps d&#39;inactivité a précédemment gonflé les résultats.
* **Rapports d&#39;inscription aux cours :** les champs liés au temps adoptent le **nouveau calcul** après le lancement.
* **Remarque sur la comparabilité :** étant donné que les données historiques ne sont pas recalculées, les analyses de séries temporelles qui s&#39;étendent sur la date de publication peuvent afficher un **changement d&#39;étape**. Pensez à l’annotation ou à la segmentation par date dans les outils d’analyse.

### API et connecteurs

* **Aucune modification de schéma** n&#39;est apportée aux points de terminaison/champs existants qui signalent le temps passé.
* **La sémantique de champ** est mise à jour pour refléter le _calcul du temps actif_ pour les sessions **après** le lancement de la fonctionnalité.
* **Les connecteurs et les exportations** qui consomment du temps dans les champs recevront automatiquement les valeurs mises à jour à l&#39;avenir.

### Rétrocompatibilité et migration des données

* **Sessions historiques :** non recalculées.
* **Nouvelles sessions :** utilisez le calcul du temps actif **nouveau**.
* **Périodes mixtes :** pour les audits ou les rapports longitudinaux, segmentez par **avant/après le lancement** afin d&#39;éviter les erreurs d&#39;interprétation.

### Limitations connues

* **Le contenu interactif** (SCORM/Captivate) continue de dépendre du minutage fourni par le contenu ; la détection d&#39;inactivité dans le contenu n&#39;est pas disponible.
* **Le contenu basé sur Iframe** (HTML/xAPI) limite la détection des interactions précises ; la mise au point sur l’onglet est utilisée à la place.

### Foire aux questions

**Cette mise à jour modifie-t-elle les enregistrements historiques ?**

Non. La modification s’applique uniquement aux sessions qui suivent le lancement de la fonctionnalité.

**Comment vérifier les modifications ?**

Vérifier les relevés de notes des élèves pour les modules récents ; comparer les durées aux durées attendues.

**Cela affecte-t-il tous les comptes ?**

Oui, il s’agit d’une mise à jour globale pour tous les comptes Adobe Learning Manager.

**Les élèves doivent-ils agir ?**

Non. La modification est automatique et transparente pour les élèves.

**Que se passe-t-il si les élèves laissent le contenu ouvert ?**

Le temps d&#39;inactivité est désormais exclu, ce qui évite la surdéclaration.

**Les sessions vidéo/audio sont-elles automatiquement interrompues lorsque l’onglet est inactif ?**

Non. Le comportement de lecture reste inchangé. Le temps est exclu lorsqu’il est interrompu > 10 minutes ou lorsqu’il ne joue pas activement.

**L’activité mobile hors ligne sera-t-elle reflétée ?**

Oui. L’utilisation hors ligne est incluse lors de la synchronisation du périphérique.

**Que dois-je faire si mes tableaux de bord affichent désormais des moyennes plus basses ?**

Ceci est attendu lorsque le temps d&#39;inactivité avait précédemment gonflé les résultats. Annotez les tableaux de bord et ajustez les cibles selon vos besoins.

**Existe-t-il des conditions préalables ?**

Aucune ; la modification est automatique.

## Mise à jour des rapports de relevé de notes pour les administrateurs

Nous mettons à jour les rapports du relevé de notes pour les administrateurs afin de mieux prendre en charge les évaluations basées sur des listes de contrôle et les commentaires des réviseurs.

## Qu’est-ce qui change ?

### &#x200B;1. Renommer la colonne dans le relevé de notes de l’administrateur

La colonne existante **Envoyer un commentaire** dans l&#39;apprentissage de l&#39;administrateur
La transcription est :

1. **Renommé en :** `Reviewer's remarks`

### Données affichées dans cette colonne :

* **Pour les modules d&#39;envoi :**
La colonne continue d&#39;afficher le commentaire de soumission (aucun changement de comportement).

* **Pour les modules de liste de contrôle :**
La colonne affiche maintenant le commentaire de l&#39;évaluation (les remarques de l&#39;examinateur de la liste de contrôle).

Cette modification s’applique à toutes les sources Admin LT :

* LT téléchargé depuis l’interface utilisateur d’administration
* LT obtenu via l’API de tâche
* LT généré via des connecteurs

Après cette modification, la même colonne contient : - Soumettre des commentaires pour les modules de soumission

* Commentaires d’évaluation pour les modules de liste de contrôle

Sous le nouveau nom d&#39;en-tête **Remarques du réviseur**.

### &#x200B;2. Nouvelle colonne dans les exportations de relevés de notes d’apprentissage basés sur des connecteurs

Pour les relevés de notes d’apprentissage exportés par le connecteur :

* Une nouvelle colonne nommée **Remarques du réviseur** est ajoutée à la fin du rapport.
* Cette colonne contient les commentaires du réviseur, alignés sur le comportement décrit ci-dessus :
   * Commentaires de soumission pour les modules de soumission
   * Commentaires d’évaluation pour les modules de liste de contrôle

## Impact sur les intégrations et automatisations existantes

Si vous utilisez des rapports de relevé de notes dans des intégrations personnalisées, des automatisations ou des outils de rapport externes, passez en revue les scénarios suivants :

| Scénario | Impact | Action requise |
|----------|--------|----------------|
| Vous identifiez les champs dans Admin LT par nom de colonne (par exemple, « Commentaire de soumission ») | L’en-tête de colonne se transforme en remarques du réviseur. | Oui. Mettez à jour toutes les mises en correspondance ou logiques qui font référence au commentaire de soumission pour utiliser les remarques du réviseur. |
| Vous identifiez les champs dans Admin LT par position de colonne uniquement (basée sur l’index) | La position de cette colonne reste la même dans Admin LT. | Habituellement, aucune action. Si votre logique ne dépend pas du texte de l’en-tête, aucune modification n’est nécessaire pour Admin LT, modifiez simplement le nom de la colonne si la colonne actuellement « Commentaires de soumission » est utilisée. |
| Vous utilisez un LT exporté par connecteur et comptez sur un nombre de colonnes fixe ou une position de dernière colonne spécifique | Une nouvelle colonne est ajoutée à la fin du rapport. | Oui. Ajustez la logique d&#39;analyse ou de validation pour tenir compte d&#39;une colonne supplémentaire à la fin du fichier. |
| Vous utilisez le LT exporté par connecteur et le mappage par nom de colonne | Une nouvelle colonne intitulée Remarques du réviseur est disponible. | Facultatif. Aucune modification n’est requise, sauf si vous souhaitez utiliser les nouvelles données de commentaires du réviseur/de la liste de contrôle. |

**Que faire**

* Examinez les scripts, les tâches ETL, les tableaux de bord ou les intégrations qui utilisent les rapports de relevé de notes d’apprentissage de l’administrateur.
* Si vous faites référence à l&#39;ancien nom de colonne _Soumettre un commentaire_, mettez à jour votre configuration ou votre code pour utiliser le nouveau nom de colonne Remarques du réviseur.
* Si vous utilisez des exportations LT basées sur des connecteurs et que vous supposez un nombre fixe de colonnes ou une dernière colonne fixe, mettez à jour votre logique pour gérer une colonne supplémentaire à la fin de l’exportation.

Si votre implémentation actuelle repose uniquement sur les positions de colonnes dans Admin LT et n’est pas validée ou ne dépend pas du texte de l’en-tête de colonne, aucune modification n’est requise pour Admin LT lui-même. Seules les exportations de connecteurs nécessitent une attention particulière lorsque vous dépendez d’une disposition fixe.


## Expérience hors connexion dans Experience Builder

L’expérience hors connexion dans Experience Builder permet aux organisations d’afficher leur contenu d’apprentissage et leurs pages de portail à tous les visiteurs, y compris ceux qui ne sont pas connectés. Cette fonctionnalité est conçue pour attirer, informer et impliquer les élèves potentiels en offrant un aperçu fluide et de marque de vos offres de formation avant qu’ils ne soient tenus de se connecter ou de s’inscrire.

Cette fonctionnalité vous permet de créer et de personnaliser des pages accessibles au public à l’aide de la même interface conviviale de glisser-déposer que celle d’Experience Builder standard. Vous pouvez présenter les catalogues de cours, les catégories, les parcours et le contenu statique enrichi, y compris les images, le texte, le HTML et les iframes intégrés, à toute personne visitant votre portail. Il est ainsi plus simple de mettre en évidence vos programmes d&#39;apprentissage, de promouvoir de nouveaux cours et de fournir des informations essentielles à un public plus large.

Les visiteurs peuvent parcourir le catalogue, afficher des détails sur les cours et les instances, et utiliser la recherche globale pour explorer les possibilités de formation disponibles. Cependant, les actions qui nécessitent l’identité d’un utilisateur, telles que l’inscription à un cours, l’accès à des fonctionnalités personnalisées (comme Calendrier, Conformité, Tableau des scores ou Apprentissage par les réseaux sociaux) ou la consommation d’une formation, invitent le visiteur à se connecter. Cette approche garantit que les informations sensibles et personnalisées restent sécurisées tout en permettant une expérience d’aperçu complète.

Les administrateurs peuvent configurer les pages et widgets visibles pour les utilisateurs qui ne sont pas connectés, en s’assurant que seul le contenu approprié est affiché. Les pages peuvent être définies pour être accessibles aux utilisateurs connectés et non connectés, ou exclusivement pour l’un de ces groupes. Experience Builder offre un mode d’aperçu, qui vous permet de voir exactement comment vos pages apparaîtront aux visiteurs avant leur publication.

Pour activer cette fonctionnalité, votre administrateur d’intégration ALM doit activer le connecteur d’accès aux données de formation. Ce connecteur garantit que les métadonnées de cours sont accessibles au public.

L’image de marque et la localisation sont entièrement prises en charge, ce qui vous permet de personnaliser les titres de page, les icônes et les paramètres linguistiques pour les aligner sur l’identité de votre organisation et répondre aux besoins de votre public. Dans le cadre de la transition vers cette expérience améliorée, la fonctionnalité héritée de la page d’accueil pour les utilisateurs non connectés sera obsolète. Par conséquent, tout nouveau contenu public doit être créé à l’aide d’Experience Builder.

### Objectif de la fonctionnalité

L’expérience hors connexion dans Experience Builder permet aux organisations de présenter publiquement leur contenu d’apprentissage et leurs pages de portail à quiconque, sans exiger que les utilisateurs se connectent. Cela permet d’attirer, d’informer et d’impliquer les élèves potentiels en fournissant un aperçu des formations et des ressources disponibles avant que l’inscription ou l’authentification ne soient nécessaires.

### Cas d’utilisation réels sur une expérience non connectée

* **Marketing et sensibilisation** : les organisations peuvent promouvoir leurs programmes de formation auprès de publics externes, tels que les clients potentiels, les partenaires ou les candidats à un emploi, en rendant les catalogues de cours et les détails du programme accessibles au public.
* **Exploration avant inscription** : les élèves peuvent parcourir les cours disponibles, afficher des aperçus et explorer les catégories avant de décider de s&#39;inscrire ou de se connecter, ce qui les aide à prendre des décisions éclairées en matière d&#39;inscription.
* **Portails de formation d’entreprise** : les entreprises peuvent fournir un portail public pour les informations de conformité ou d’intégration, ce qui permet aux nouveaux embauchés ou sous-traitants de voir quelle formation est disponible avant de recevoir des informations d’identification.
* **Pages de destination des événements ou des campagnes** : les organisations qui mènent des campagnes d’apprentissage ou des événements peuvent créer des pages publiques dédiées pour mettre en évidence les cours, calendriers ou ressources en vedette, ce qui augmente la visibilité et l’engagement.
* **SEO et découvrabilité** : en rendant publiques certaines pages et certains catalogues, les organisations améliorent la visibilité de leurs moteurs de recherche, aidant ainsi les utilisateurs à découvrir leurs offres d’apprentissage en ligne.

### Concepts clés de l’expérience hors connexion

L’expérience hors connexion d’Experience Builder vous permet de présenter publiquement du contenu d’apprentissage et des pages de portail, ce qui permet aux visiteurs de parcourir le site sans se connecter.

* **Créer des pages et des menus publics** : vous configurez des pages et un menu unique auxquels tout le monde peut accéder, quel que soit le statut de connexion.
* **Ajouter uniquement les widgets pris en charge** : vous incluez des widgets qui n’ont pas besoin du contexte utilisateur (catégories, cours et parcours d’apprentissage, zone de contenu, HTML, iframe), tandis que le système masque les widgets spécifiques à l’utilisateur.
* **Configurer le comportement de page adaptatif** : vous décidez si une page apparaît pour les utilisateurs connectés et non connectés, et si le système adapte les widgets et le contenu visibles en fonction de l&#39;état de connexion.
* **Prévisualiser les deux expériences** : vous utilisez les options d&#39;aperçu pour voir à quoi ressemblent les pages pour les utilisateurs connectés et non connectés, avec des différences de visibilité et de contenu du widget.
* **Activer la recherche globale** : les visiteurs recherchent des cours et du contenu, mais n&#39;obtiennent que des fonctionnalités de recherche de base sans intégration avancée de l&#39;IA.
* **Autoriser les visiteurs à parcourir les aperçus de catalogue et de cours** : les visiteurs explorent les pages de catalogue, les détails de cours et les instances, mais doivent se connecter pour s&#39;inscrire ou accéder à des fonctionnalités personnalisées.
* **Personnalisation de l&#39;image de marque et de la localisation** : vous définissez des favicons et des paramètres de langue pour répondre aux besoins de votre organisation en matière d&#39;image de marque et d&#39;accessibilité.
* **Activer le connecteur d&#39;accès aux données de formation** : vous activez ce connecteur pour exporter les métadonnées du cours pour un affichage public, en conservant les pages non connectées à jour.
* **Gérer un trafic élevé avec une infrastructure partagée** : le système gère de gros volumes de visiteurs anonymes à l&#39;aide de ressources partagées et de la limitation de débit.
* **Optimiser pour le référencement** : la plateforme prépare des pages publiques pour l&#39;indexation des moteurs de recherche, ce qui simplifie la recherche de votre contenu d&#39;apprentissage.

### Conditions préalables pour l’expérience hors connexion

* Vous devez activer le Connecteur d’accès aux données de formation dans l’administrateur d’intégration avant de pouvoir utiliser l’expérience hors connexion.
* Le connecteur exporte les métadonnées du cours vers un référentiel public, qui met à jour les pages non connectées.

#### Initialisation du connecteur Training Data Access

Le connecteur Training Data Access (TDA) est un prérequis essentiel à l’activation de la nouvelle fonctionnalité du créateur d’expérience hors connexion dans ALM. Ce connecteur facilite l’exportation des métadonnées de formation, ce qui permet à votre portail d’afficher des informations sur les cours pour les utilisateurs qui ne sont pas connectés.

* **Activation du connecteur** : vous devez activer le connecteur TDA à partir du panneau d&#39;administration de l&#39;intégration. Cette étape active la fonctionnalité du créateur d’expérience non connectée et rend les options d’interface utilisateur pertinentes visibles dans votre interface d’administration.
* **Exportation de métadonnées** : une fois activé, le connecteur exporte les métadonnées de formation essentielles (telles que le nom du cours, la description, la présentation, l’évaluation, la durée et les compétences) d’ALM vers un référentiel public. Ces données sont utilisées pour remplir les pages et les widgets non connectés.
* **Planification et synchronisation** : le processus d&#39;exportation peut être planifié (par exemple, quotidiennement) pour s&#39;assurer que votre portail reflète les dernières mises à jour de cours. Les modifications apportées dans ALM apparaîtront sur vos pages non connectées après le prochain cycle d’exportation, sous réserve de la mise en cache et de la fréquence d’exportation.
* **Disponibilité des fonctionnalités** : les fonctionnalités du créateur d’expérience non connectées, y compris la création de menus, la prise en charge des widgets et la visibilité des catalogues, ne sont accessibles qu’après l’initialisation du connecteur TDA. Si le connecteur n’est pas activé, votre Experience Builder restera limité aux scénarios d’utilisateur connecté.
* **Migration et prise en charge** : pour les comptes en transition à partir des fonctionnalités héritées de la page d’accueil non connectées, l’initialisation du connecteur TDA est la première étape vers la migration. Cela vous permet d’utiliser la flexibilité et les fonctionnalités améliorées du nouveau créateur d’expérience.


### Ce que les visiteurs peuvent faire sans se connecter

Sur un site Experience Builder non connecté, les visiteurs peuvent parcourir le catalogue de formation en ouvrant la page du catalogue pour les catalogues publics. Ils peuvent utiliser des filtres tels que le catalogue, le produit, le rôle, le type, les compétences et les balises, selon la façon dont vous avez configuré le site. Les visiteurs peuvent également rechercher des formations à l’aide de la barre de recherche globale dans l’en-tête (si activée) et afficher les résultats de la recherche directement sur la page du catalogue.

Les visiteurs peuvent afficher les détails de la formation en ouvrant des pages de présentation pour les cours, les parcours d’apprentissage et les certifications. Ces pages affichent les métadonnées clés, notamment le titre, la description, l’auteur, la durée, le format, les balises et les compétences.

De plus, les visiteurs peuvent explorer le contenu statique et promotionnel. Ils peuvent lire des blocs de texte et de contenu enrichi, afficher des bannières et des vignettes d’image, et interagir avec des iframes intégrés tels que des microsites externes, des vidéos ou des outils.

Si un visiteur clique sur S’inscrire ou tente de commencer la formation, le système l’invite à se connecter ou à s’inscrire. Une fois la connexion réussie, le visiteur est redirigé vers la page appropriée, qu’il s’agisse de la page d’accueil, d’une page personnalisée ou de la formation spécifique qu’il a sélectionnée.

### Éléments non disponibles sans connexion

Sur un site Experience Builder non connecté, les visiteurs ne peuvent pas accéder aux fonctionnalités ou au contenu qui nécessitent l’authentification de l’utilisateur. Ils ne peuvent pas s’inscrire à des formations, commencer ou suivre des cours, ni accéder à des widgets personnalisés tels que Mon apprentissage, Calendrier, Conformité, Tableau des scores ou Apprentissage par les réseaux sociaux. Ces widgets dépendent de données spécifiques à l’utilisateur et ne sont disponibles qu’après la connexion.

Les visiteurs ne peuvent pas non plus effectuer d&#39;actions telles que l&#39;inscription à un cours ou l&#39;accès à un contenu qui nécessite un suivi de la progression ou du contexte utilisateur. Si vous tentez de vous inscrire ou de démarrer une formation, le visiteur est invité à se connecter ou à s’inscrire avant de continuer.

### Widgets pris en charge en mode hors connexion

En mode non connecté, seuls les widgets qui ne nécessitent pas de données spécifiques à l’utilisateur sont pris en charge. Il s’agit notamment :

* le widget Catégories, qui affiche les catégories de formation disponibles.
* Widget Cours et parcours, qui affiche les cours et parcours d’apprentissage du catalogue public.
* Zone de contenu, pour ajouter du texte statique, des images ou du contenu promotionnel.
* widget de HTML, pour l’incorporation de contenu de HTML personnalisé.
* Widget Iframe, pour afficher des sites externes, des vidéos ou des outils dans la page.
* Les widgets qui nécessitent un contexte utilisateur, tels que Mon apprentissage, Calendrier, Conformité, Tableau des scores et Apprentissage par les réseaux sociaux, ne sont pas disponibles en mode non connecté.

### Pages et menus en mode hors connexion

* Un seul menu hors connexion est pris en charge, visible par tous les visiteurs sans authentification.
* Les pages peuvent être ajoutées aux menus connectés et non connectés ; si une page est connectée aux deux, elle adapte ses widgets et son contenu en fonction de l’état de connexion de l’utilisateur.
* Les menus hors connexion n’ont pas de ciblage d’audience ni de personnalisation. Tout le monde voit le même ensemble de pages.
* Les widgets non pris en charge en mode hors connexion sont masqués automatiquement ; la mise en page s’ajuste pour remplir les espaces.
* La gestion des menus et des pages (ajout, prévisualisation, suppression) est similaire au mode connecté, mais avec des adaptations pour les contraintes non connectées.

### Comportement de recherche et de catalogue

En mode hors connexion, les utilisateurs peuvent accéder à la page du catalogue et utiliser la recherche pour parcourir les cours et parcours d’apprentissage disponibles. La page du catalogue affiche tous les cours publics, ainsi que les filtres et la fonctionnalité de recherche, en suivant les mêmes paramètres de compte que ceux du mode connecté. Lorsqu&#39;un utilisateur effectue une recherche, les résultats s&#39;affichent sur la page du catalogue et les utilisateurs peuvent afficher les pages de présentation des cours et des instances sans se connecter. Cependant, les actions telles que l’inscription nécessitent une connexion.

Si un utilisateur tente de s’inscrire, le système exige qu’il se connecte d’abord. La recherche d’utilisateurs non connectés est plus simple que celle d’utilisateurs connectés et n’inclut pas de fonctionnalités avancées telles que l’intégration de l’assistant AI.

### Mise en œuvre technique

#### Configuration du connecteur d&#39;accès aux données de formation

Vous devez activer le connecteur d’accès aux données de formation dans le panneau d’administration de l’intégration avant de pouvoir utiliser la fonctionnalité du créateur d’expérience non connecté. Ce connecteur exporte les métadonnées de formation d’ALM vers un référentiel public, ce qui les rend accessibles via des API pour vos pages non connectées. La configuration du connecteur est un prérequis pour l’activation de la fonctionnalité et garantit que votre portail affiche des informations de formation à jour.

#### Exportation et synchronisation des métadonnées

Le connecteur exporte des champs de métadonnées clés tels que le nom du cours, la présentation, la description, l’évaluation, la durée et les compétences. Vous pouvez planifier des exportations (par exemple, quotidiennes) pour que votre portail reste synchronisé avec ALM. Tous les champs de métadonnées ne peuvent pas être inclus ; consultez les ingénieurs pour obtenir une liste complète. Les données exportées sont utilisées pour remplir les pages non connectées, et les modifications dans ALM apparaîtront après le prochain cycle d’exportation.

#### Mise en cache et exportation de la fréquence

Le système utilise la fréquence d&#39;exportation du serveur principal et la mise en cache du serveur principal pour gérer les mises à jour des données. Les modifications apportées dans ALM sont répercutées sur votre portail après l’exportation planifiée et l’actualisation du cache. Certaines mises à jour peuvent ne pas apparaître immédiatement en raison de ces mécanismes. Si vous avez besoin de mises à jour plus rapides, ajustez la planification de l’exportation ou videz le cache selon vos besoins.

#### Prise en charge de la personnalisation CSS/JS

Vous pouvez appliquer des feuilles de style CSS et JavaScript personnalisées aux pages connectées et non connectées à l’aide de l’onglet Personnalisation. Cela vous permet de maintenir une image de marque cohérente, d’ajouter des éléments d’interface utilisateur personnalisés et d’améliorer l’expérience utilisateur sur votre portail. Toutes les personnalisations sont appliquées globalement, garantissant un aspect unifié.

#### Différences d’URL et identité visuelle (icône favorite, titre de la page)

Les pages non connectées et connectées peuvent avoir des URL différentes pour distinguer les états de l’utilisateur. Vous pouvez personnaliser l’icône favorite et le titre de la page pour votre portail, ce qui contribue à renforcer votre identité de marque. Ces fonctionnalités sont disponibles dans le créateur d’expérience ; consultez les ingénieurs pour connaître le dernier statut de la prise en charge hors connexion.

### Performances et évolutivité

#### Pile partagée et pile Premium

La pile partagée permet à plusieurs clients d’utiliser le créateur d’expérience hors connexion sur l’infrastructure commune, prenant en charge les niveaux de trafic standard. La pile Premium est une option payante qui fournit des ressources dédiées, des fonctionnalités en temps réel et des limites de places plus élevées pour les clients ayant des besoins avancés. Sélectionnez la pile en fonction de votre trafic et de vos exigences professionnelles attendus.

#### Limites de trafic et limitation du débit

La pile partagée applique des limites de trafic pour garantir une utilisation équitable entre les clients. L’ingénierie mettra en œuvre une limitation de débit pour empêcher un seul client de consommer toutes les ressources. Si vous planifiez des campagnes marketing ou prévoyez un trafic élevé, coordonnez-vous avec les ingénieurs pour comprendre vos limites et éviter les interruptions de service. La limitation de débit permet de maintenir la stabilité du système et les performances pour tous les utilisateurs.

#### Considérations relatives au multi-location et au référencement

La plateforme prend en charge le multi-location, permettant à plusieurs clients d’héberger leurs portails sur des infrastructures partagées. Les pages non connectées sont SEO-friendly, ainsi que sitemap.xml et robots.txt pour optimiser la visibilité des moteurs de recherche. Cela garantit que votre portail est détectable et indexé de manière appropriée par les moteurs de recherche.

### Migration et dépréciation

#### Transition depuis la page d’accueil existante sans connexion

Vous devez recréer votre page d’accueil à l’aide du nouveau créateur d’expérience pour bénéficier d’une flexibilité, d’une prise en charge des widgets et d’une expérience utilisateur améliorées. Le plan de transition assure une interruption minimale et un soutien continu.

#### Plan de communication

Les clients qui utilisent la page d’accueil héritée recevront une communication claire sur le calendrier d’obsolescence et les étapes de migration. Une assistance sera fournie pour vous aider à déplacer votre page d’accueil vers la nouvelle plateforme experience builder, afin que vous puissiez bénéficier des nouvelles fonctionnalités et des mises à jour continues.

### Prise en charge de la localisation et de la connexion

#### Logique de secours des paramètres régionaux

Le système affiche les pages dans les paramètres régionaux dans lesquels elles ont été créées. Si les paramètres régionaux d’un utilisateur ne sont pas disponibles, le système utilise une logique de secours pour sélectionner les meilleurs paramètres régionaux disponibles suivants. Cela garantit que les utilisateurs voient toujours le contenu dans une langue prise en charge, améliorant ainsi l’accessibilité et la satisfaction des utilisateurs.

#### Types de connexion pris en charge

L’expérience hors connexion prend en charge tous les types de connexion disponibles dans ALM, y compris l’authentification unique et la connexion standard. Les utilisateurs peuvent parcourir le contenu sans se connecter et seront invités à se connecter si nécessaire, comme pour s&#39;inscrire à un cours ou accéder à des fonctionnalités personnalisées. Cela permet une transition en douceur de la navigation à l’engagement.


### API non connectées

#### API de l’objet d’apprentissage d’administrateur

Les pages Experience Builder non connectées et les portails sans tête organisent ou filtrent souvent les cours en fonction du produit et du rôle. L’API Admin LO a été améliorée pour garantir que ces associations sont accessibles de manière cohérente pour les intégrations back-end et headless, ainsi que pour le connecteur TDA.

**Point de terminaison et comportement**

Vous continuez à utiliser le point de terminaison Admin LO existant :

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Où :

* loId est l&#39;ID de l&#39;objet d&#39;apprentissage (par exemple, course:12345).
* forcedFields[learningObject] indique à l&#39;API d&#39;inclure explicitement des produits et des rôles pour cet objet d&#39;apprentissage.

Pour ce faire, assurez-vous que les associations de produit et de rôle de l’objet d’apprentissage sont présentes dans la réponse lorsque celle-ci est demandée par l’intermédiaire des champs appliqués. La réponse contient ensuite, dans les attributs, les métadonnées de produit et de rôle nécessaires pour calculer ou afficher les produits recommandés (rec\_products) et les rôles (rec\_roles) pour Experience Builder et les autres clients.

Un appel typique d’un administrateur ou d’une intégration se présente comme suit :

```
url -X GET \
 "https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json
```

Le fichier JSON LO renvoyé est la même structure de base qu’auparavant, mais vous pouvez désormais compter sur la présence de champs de produit/rôle lorsque vous les demandez avec forcedFields. Les intégrations qui n’utilisent pas forcément forcées continuent de se comporter comme auparavant.

#### Liste des objets d’apprentissage - Prise en charge de JobAid dans le filtre Date de modification effective

**Objectif**

Le connecteur TDA (Training Data Access) et les implémentations sans tête doivent souvent effectuer une synchronisation incrémentielle, en fonction de la **date de modification effective** des objets d&#39;apprentissage. Jusqu&#39;à cette version, les assistances à la tâche (assistance à la tâche de type objet d&#39;apprentissage) n&#39;étaient pas correctement gérées lorsqu&#39;elles étaient combinées avec les filtres effectiveModifiedDate. Cette version corrige ce problème afin que les assistances à la tâche puissent être synchronisées de manière incrémentielle comme les cours et les parcours d’apprentissage.

**Point de terminaison et comportement**

Vous utilisez le point de terminaison de liste d’objet d’apprentissage existant avec les filtres de date et le type d’objet d’apprentissage :

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z
 &filter.loTypes=jobAid
```

Auparavant, lorsque filter.loTypes=jobAid était combiné à une plage effectiveModifiedDate, le filtre excluait effectivement les assistances à la tâche et l&#39;appel se comportait comme si les assistances à la tâche n&#39;étaient pas prises en charge.

À partir de cette mise à jour, l&#39;appel retourne uniquement les objets d&#39;apprentissage JobAid dont la date effectiveModifiedDate est comprise dans la fenêtre spécifiée.

```
{
 "links": {
 "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"
 },
 "data": [
 {
 "id": "jobAid:144968",
 "type": "learningObject",
 "attributes": {
 "authorNames": ["Author"],
 "dateCreated": "2026-01-20T08:48:55.000Z",
 "datePublished": "2026-01-20T08:48:55.000Z",
 "dateUpdated": "2026-01-20T08:48:55.000Z",
 "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",
 "loType": "jobAid",
 "loFormat": "Content",
 "loResourceType": "Content",
 "localizedMetadata": [
 {
 "description": "Link jobAid new",
 "locale": "en-US",
 "name": "Link jobAid new"
 },
 {
 "description": "Link jobAid new fre",
 "locale": "fr-FR",
 "name": "Link jobAid new fre"
 }
 ],
 "relationships": {
 "authors": {
 "data": [
 { "id": "13385176", "type": "user" }
 ]
 },
 "instances": {
 "data": [
 { "id": "jobAid:144891\_-1", "type": "learningObjectInstance" }
 ]
 }
 }
 }
 }
 ]
}
```

Cela signifie que vous pouvez désormais implémenter en toute sécurité des synchronisations d&#39;assistance à la tâche incrémentielles basées sur effectiveModifiedDate, comme vous le faites déjà pour les autres types.

Si vous omettez filter.loTypes=jobAid, le comportement des autres types d&#39;objet d&#39;apprentissage reste inchangé ; la modification n&#39;affecte que la combinaison de JobAid avec ce filtre.

#### **API de menu : filtre de menu non connecté**

**Objectif**

Experience Builder et les frontends sans tête ont besoin d’un moyen simple de récupérer le **menu hors connexion** , celui qui définit la navigation pour les visiteurs publics. Avant cette version, vous deviez récupérer tous les menus, puis appliquer une logique personnalisée pour identifier celui qui représentait la navigation hors connexion. Cette version ajoute un filtre côté serveur simple.

**Point de terminaison et comportement**

Vous utilisez le point de terminaison de liste Menu existant avec un nouveau paramètre de requête :

```
GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true
```

Les points clés :

* include=pages,subMenus.pages est facultatif, mais recommandé lorsque vous avez besoin des détails de la page et du sous-menu dans la même réponse.
* isNonLoggedIn=true est une nouvelle version de cette version et indique au serveur de renvoyer uniquement les menus marqués comme non connectés.

Sans le paramètre isNonLoggedIn, le point de terminaison se comporte exactement comme auparavant et renvoie des menus en fonction du comportement par défaut existant. Avec isNonLoggedIn=true, il renvoie généralement le menu unique utilisé par l’expérience hors connexion pour votre compte (puisqu’il y a normalement un menu hors connexion par compte).

En pratique, un client peut désormais émettre :

```
curl -X GET \
 "https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json"
```

et récupérez la structure de navigation hors connexion en un seul appel, avec toutes les pages qui devraient être visibles par les visiteurs anonymes.

Cela est particulièrement utile lorsque vous créez un site sans en-tête non connecté et que vous souhaitez refléter la même navigation qu’Experience Builder utilise, ou lorsque vous déboguez si le menu hors connexion a été configuré correctement.

### Autoriser la liste de domaines personnalisés

La pile non connectée se compose des éléments suivants :

* Domaine CDN public (par exemple cpcontents.adobe.com ou yourdomain.example.com) qui sert les mises en page, la configuration JSON et les actifs statiques.
* Point de terminaison d&#39;Elasticsearch public (ES) qui fournit des données de catalogue et de recherche, mais uniquement si la demande provient d&#39;un **domaine autorisé** pour ce compte ALM.

Lorsque vous introduisez un domaine personnalisé, il fonctionne de manière transparente sans effort supplémentaire suivant le processus existant pour ajouter un domaine personnalisé.

#### Conditions préalables

Avant de mettre un domaine personnalisé en liste blanche pour les utilisateurs non connectés :

1. Le domaine personnalisé est configuré pour votre compte ALM (par exemple, DNS pour academy.yourcompany.com pointe vers Adobe / Akamai et des certificats sont fournis).
2. Le connecteur **Training Data Access (TDA)** est activé pour le compte.
3. La fonctionnalité **Experience Builder** non connecté est activée (côté Adobe).

Ces étapes garantissent que :

* Votre compte a un **compte JSON** non connecté (souvent référencé sous le nom de accountConfig / experienceBuilderConfig), qui inclut des champs tels que cpDomain, almDomain, almCdnBaseUrl, esBaseUrl et des domaines inscrits dans la liste autorisée.
* La pile non connectée sait où servir les données et à partir de quels domaines elle doit accepter les demandes.

#### Fonctionnement de la liste autorisée

La liste autorisée est stockée dans la configuration exportée par TDA et lue par la pile non connectée. Cette configuration comprend :

* Domaines ALM (cpDomain, almDomain).
* **URL de base CDN** pour le contenu non connecté (almCdnBaseUrl).
* **URL de base de recherche publique** (esBaseUrl).
* Liste des domaines autorisés à effectuer des appels publics non connectés pour ce compte.

Pour qu’Experience Builder non connecté fonctionne sur un domaine personnalisé :

* Le navigateur doit charger le HTML non connecté à partir de ce domaine personnalisé (ou du domaine CDN ALM non connecté, selon votre configuration).
* Les appels de ce domaine vers les points de terminaison ES et CDN publics doivent être acceptés. Cela se produit uniquement si le domaine est présent dans la liste autorisée.

Cette version ajoute un nouveau domaine CDN non connecté, cpcontents.adobe.com, et spécifie qu&#39;il doit être placé dans les **domaines autorisés** dans le connecteur TDA. Pour les utilisateurs natifs existants non connectés, une mise à jour est nécessaire.

#### Autoriser la liste d’un domaine personnalisé

**Configuration du domaine personnalisé dans ALM**

Travaillez avec Adobe pour enregistrer votre domaine, par exemple academy.yourcompany.com, en tant que domaine personnalisé pour votre compte ALM. Vous mettez à jour DNS pour pointer vers l&#39;Adobe Akamai comme indiqué et attendez que le protocole SSL et le routage se terminent.

À ce stade, le trafic connecté et non connecté peut atteindre ALM via ce domaine, mais les appels de recherche et de catalogue non connectés peuvent toujours être bloqués si le domaine n’est pas autorisé.

**Activer TDA et Experience Builder hors connexion**

Assurez-vous que :

* Le **connecteur Training Data Access** est activé.
* La fonctionnalité **Experience Builder** non connecté est activée pour le compte.

L’activation de TDA crée ou met à jour le compte non connecté JSON. Pour les nouveaux comptes, le processus autorise également le nouveau domaine CDN non connecté (cpcontent.adobe.com) par défaut, de sorte que le point de terminaison ES public attend des appels de ce domaine.

Pour les comptes qui utilisaient déjà l’ancienne pile non connectée, les connecteurs existants doivent être supprimés et recréés pour récupérer le nouveau domaine.

**Ajouter le domaine personnalisé à la liste autorisée**

La partie critique indique à la pile ES non connectée que academy.yourcompany.com est une origine approuvée. Il existe deux chemins communs.

1. **Réactivez le connecteur TDA (simple, en libre-service)**

Les utilisateurs natifs non connectés existants devront supprimer et réactiver la connexion TDA afin que le nouveau domaine soit automatiquement autorisé à figurer dans la liste. Cela permet d’atteindre deux objectifs :

1. Le compte JSON non connecté est régénéré.
2. Les domaines de la liste autorisée sont mis à jour pour inclure le nouveau domaine CDN non connecté et votre domaine personnalisé.

Cette option est recommandée lorsque vous disposez d&#39;un petit nombre de comptes et que vous tolérez la désactivation et la réactivation temporaires du connecteur.

1. **Vérifiez que le domaine est bien autorisé**

Après la liste autorisée, ouvrez votre site non connecté sur le domaine personnalisé et inspectez les appels réseau du navigateur.

Vous voulez voir :

* Demandes à almCdnBaseUrl (par exemple <https://cpcontent.adobe.com/>...) avec 200/304.
* Demandes à esBaseUrl (API de recherche publique, par exemple <https://primeapps.adobe.com/almsearch/api/v1/>...) opération réussie, retour de JSON avec les données de recherche/catalogue.

Si ces appels retournent 4xx ou des erreurs explicites suggérant « domaine non approuvé » ou « origine non autorisée », la liste autorisée est incomplète ou mal configurée et le support doit l’ajuster.

Le LLD hors connexion note également que la configuration du compte peut contenir une valeur de domaine attendue. Lors de l’exécution, le site vérifie que le domaine dans l’URL correspond à ce qui est défini dans la configuration. Si ce n’est pas le cas, l’utilisateur peut être redirigé vers une page d’erreur. Cela vous protège contre l’accès à la configuration d’un client via le domaine d’un autre client.

### Utilisation des recommandations dans Experience Builder non connecté

L’Experience Builder non connecté vous permet de créer des pages d’apprentissage publiques où les visiteurs peuvent parcourir votre catalogue et voir le contenu mis en évidence avant de se connecter. Même si ces visiteurs sont anonymes, vous pouvez toujours présenter des formations recommandées en utilisant des métadonnées et des widgets.

Dans l’application de l’élève connecté, les recommandations peuvent être personnalisées : elles peuvent dépendre du profil, de l’historique, des compétences et de la progression de l’élève. Dans l&#39;expérience **hors connexion**, il n&#39;y a pas encore d&#39;identité d&#39;élève, la plateforme ne peut donc pas personnaliser par utilisateur.

Par conséquent, Recommendations en mode hors connexion est :

* **Sélectionné ou basé sur des règles** : basé sur le catalogue, le produit, le rôle, les libellés, les balises et d&#39;autres métadonnées.
* **Orienté segment** : « recommandé pour les développeurs », « recommandé pour les partenaires », « recommandé pour les débutants ».
* **Axé sur le marketing** : utilisé pour attirer et guider les visiteurs pour qu&#39;ils s&#39;inscrivent une fois qu&#39;ils se connectent.

### Métadonnées et API prenant en charge les recommandations

En coulisse, les pages non connectées utilisent :

* Le **connecteur TDA** pour exporter les métadonnées des objets d&#39;apprentissage (cours, parcours, certifications, assistances à la tâche) vers un index de recherche public.
* La **pile de recherche publique** pour répondre aux requêtes des widgets non connectés (catalogue, recherche, cours et parcours, catégories).
* L&#39;**API Admin Learning Objects** pour exposer les métadonnées de produit et de rôle qui peuvent être utilisées pour les règles de recommandation.

Dans cette version, l’API Admin LO a été étendue afin que les associations de produits et de rôles soient disponibles de manière fiable :

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Cela permet aux widgets et aux intégrations sans en-tête de créer des recommandations basées sur des règles à l’aide de produits, de rôles, d’étiquettes de catalogue, de balises et d’autres champs de manière cohérente.

### Conception de sections de recommandation avec les widgets Experience Builder

Vous créez des sections de recommandation sur des pages non connectées en combinant des **widgets Experience Builder** avec des filtres de métadonnées.

#### Widget **Cours et parcours**

Utilisez le widget **Cours et parcours** pour afficher une ligne ou une grille d&#39;éléments recommandés. Dans sa configuration, vous pouvez choisir :

* À partir de quels catalogues extraire.
* Étiquettes, produits, rôles ou balises de catalogue à utiliser comme filtres.
* Indique s’il faut afficher des cours, des parcours, des certifications, des assistances à la tâche ou un mixage.
* Tri et nombre maximal d’éléments.

Par exemple, vous pouvez créer :

* « Recommandé pour les développeurs » : filtrez en fonction d’un produit ou d’un rôle que vous utilisez pour le contenu développeur.
* « Commencer ici » : filtrez par un libellé tel que « Démarrer » ou « Intégration ».
* « En vedette ce trimestre » : filtrez par un libellé limité dans le temps comme en vedette-t3-2026.

Le widget n’apprend pas à tirer des leçons du comportement ; il affiche tout ce qui correspond aux règles de métadonnées que vous définissez. Du point de vue du visiteur, cependant, cela ressemble à une bande de recommandation.

#### Widget **Catégories**

Utilisez le widget **Catégories** pour aider les visiteurs à naviguer dans les ensembles de contenu « recommandés », même s&#39;ils ne connaissent pas les noms de vos produits.

Vous pouvez configurer des vignettes qui représentent chacune un segment, par exemple :

* « Pour les administrateurs »
* « Pour les équipes commerciales »
* « Pour les partenaires »
* « Par gamme de produits »

Chaque vignette peut être liée à :

* Une page de catalogue filtrée (par exemple, le catalogue filtré par certains produits ou étiquettes).
* Une page dédiée non connectée qui utilise des cours et des chemins préconfigurés pour ce segment.

Cela vous offre une expérience « chemins recommandés par segment » sans personnalisation.

### Élaboration de recommandations par segment

Étant donné que les visiteurs non connectés n&#39;ont pas encore de profil ALM, il est utile de concevoir des recommandations **par segment** et de laisser les visiteurs choisir eux-mêmes.

1. Utilisez une **page d&#39;accueil non connectée** qui explique brièvement à qui votre académie est destinée et affiche un petit nombre de points d&#39;entrée de segment (par exemple, « Développeurs », « Marketing », « Partenaires », « Nouveaux employés »). Pour ce faire, utilisez un widget Catégories ou une simple zone de contenu ou une section de HTML avec des boutons.
2. Pour chaque segment, créez une **page non connectée dédiée** dans Experience Builder. Sur cette page, utilisez un ou plusieurs widgets Cours et parcours configurés avec des filtres qui représentent ce qui est « recommandé » pour ce groupe. Par exemple, pour « Développeurs », vous pouvez filtrer sur :
   1. Catalogue = « Formation publique »
   2. Produit = « Adobe Experience Manager »
   3. Balises = « Principes de base du développeur »
3. Utilisez ces pages de segment comme destination de vos campagnes marketing et comme cible des vignettes de la page d’accueil non connectée.

Les visiteurs perçoivent qu&#39;ils voient des recommandations adaptées à leur situation, même si la logique est définie au moment de la conception via des métadonnées.

### Transition des utilisateurs non connectés aux recommandations personnalisées

Les recommandations hors connexion concernent principalement la **découvrabilité** et la **conversion**. Une fois que les visiteurs décident de s’inscrire ou de commencer une formation, ils se connectent et deviennent des élèves à part entière avec un profil et un historique.

Le flux habituel est :

1. Un visiteur découvre du contenu via vos sections de recommandation non connectées (recommandations d’accueil, pages de destination des segments, lignes en vedette).
2. Ils cliquent sur une vue d’ensemble de cours ou de parcours et choisissent de s’inscrire ou de commencer.
3. ALM les invite à s’inscrire ou à se connecter.
4. Une fois qu’ils se sont connectés, l’expérience d’élève standard connectée prend le relais, notamment :
   1. « Mon apprentissage »
   2. Catalogue connecté avec progression personnelle
   3. Tous les systèmes de recommandation internes que vous utilisez pour les élèves existants.

En d’autres termes, les recommandations connectées les aident à décider de ce qu’il faut faire ensuite et à continuer.

### Comment les assistances à la tâche peuvent être utilisées dans le nouvel Experience Builder non connecté

Sur l&#39;**interface utilisateur**, les assistances à la tâche participent à des expériences non connectées, principalement via les widgets qui peuvent afficher des objets d&#39;apprentissage :

1. Widget **Cours et parcours**
Ce widget peut afficher plusieurs types d’objet d’apprentissage, y compris des assistances à la tâche. Dans les pages non connectées, vous pouvez le configurer pour :
   1. Inclure ou exclure explicitement les assistances à la tâche.
   2. Filtrez les assistances à la tâche par catalogue, produit, rôle, étiquettes, balises et autres métadonnées.
   3. Présentez-les en même temps que des cours et des parcours ou sous la forme d’une bande « Ressources » distincte.

Par exemple, sur une page de destination publique, vous pouvez configurer une bande intitulée « Ressources utiles » qui affiche uniquement les assistances à la tâche, et une autre bande intitulée « Cours recommandés » qui affiche les cours et les parcours.

1. **Page de catalogue et recherche**
Les surfaces **catalogue** et **recherche** non connectées utilisent l&#39;index de recherche publique (alimenté par le connecteur Training Data Access). Cet index prend désormais correctement en charge les assistances à la tâche.
   1. Les résultats de recherche hors connexion peuvent inclure des assistances à la tâche.
   2. Filtres de catalogue non connectés (par type, produit, balises, etc.) peut inclure des assistances à la tâche tant que la configuration de votre compte et les widgets sont configurés pour les afficher.
2. Pages de présentation **LO**
Lorsqu&#39;un visiteur clique sur une assistance à la tâche à partir d&#39;un widget ou du catalogue, il accède à une **page de présentation LO** pour cette assistance à la tâche en mode non connecté. De là, ils peuvent lire sa description et ses métadonnées. Le téléchargement ou la consommation réels nécessitent généralement toujours une connexion, mais la présence et la découvrabilité de l&#39;assistance à la tâche elle-même sont gérées par l&#39;expérience hors connexion.

### Affichage des assistances à la tâche via des API non connectées

Du côté **API**, les assistances à la tâche sont prises en charge par :

1. Connecteur d&#39;accès aux données de formation **et recherche publique**
TDA exporte les métadonnées des assistances à la tâche ainsi que d’autres types d’objet d’apprentissage vers l’index de recherche public qui sert aux requêtes de recherche et de catalogue non connectées. C’est ce sur quoi reposent Experience Builder et les frontends sans tête.
2. La liste **Objets d’apprentissage avec effectiveModifiedDate**
Dans cette version, le point de terminaison de liste LO a été corrigé afin que les assistances à la tâche fonctionnent correctement avec le filtre effectiveModifiedDate. Vous pouvez désormais appeler :

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z
 &filter.loTypes=jobAid
```

Avant cette modification, la combinaison effectiveModifiedDate avec loTypes=jobAid ne renvoyait pas d&#39;assistances à la tâche de manière fiable. Cela signifie :

1. Vos tâches TDA ou ETL peuvent **synchroniser de manière incrémentielle les assistances à la tâche** pour les expériences non connectées, de la même manière qu’ils le font pour les cours et les parcours.
2. Toute implémentation sans en-tête qui crée un répertoire d&#39;assistance à la tâche public peut interroger les modifications en fonction de effectiveModifiedDate et loType=jobAid.

**Remarque** :

Dans l’état non connecté :

* Les assistances à la tâche sont principalement **détectables** : les visiteurs peuvent voir qu&#39;elles existent, lire les descriptions et comprendre comment elles prennent en charge les sujets ou les cours.
* La **consommation** réelle (téléchargement ou ouverture du contenu de l&#39;assistance à la tâche) nécessite généralement toujours la connexion, en particulier si les assistances à la tâche sont considérées comme faisant partie du contenu sous licence ou interne.

### Modifications apportées à la brève description dans la recherche d’objet d’apprentissage (non connecté)

Dans la pile non connectée, la recherche et la liste des objets d’apprentissage sont optimisées par le connecteur TDA (Training Data Access) et un index d’Elasticsearch publics. Historiquement, cette pile utilisait un seul champ de présentation/description pour chaque objet d’apprentissage. Les clients qui créent des portails sans en-tête non connectés voulaient afficher la même brève description sur les vignettes d’objet d’apprentissage que celle de l’interface utilisateur des élèves connectés, plutôt que la seule vue d’ensemble longue.

La modification introduit la prise en charge de l&#39;objet d&#39;apprentissage **brève description** dans les API de recherche et de liste non connectées :

* Pour **cours**, la sémantique de l’interface utilisateur existante est la suivante :
* Les cartes connectées affichent une brève description (champ de 140 caractères), le cas échéant ; sinon, elles se limitent à la longue présentation détaillée.
* Pour les **parcours d’apprentissage**, l’interface utilisateur connectée utilise le champ Avantages comme brève description, si elle est définie, et revient à la vue d’ensemble dans les autres cas.
* Pour les **certifications**, une brève description est utilisée, avec une présentation de certification plus longue comme solution de secours.
* Pour les **assistances à la tâche**, le champ de description principal est utilisé.

### Autres modifications

#### Restriction selon laquelle deux comptes ne peuvent pas partager le même domaine personnalisé

Dans les architectures non connectées et connectées de Adobe Learning Manager, un **domaine personnalisé** (par exemple, academy.example.com) est traité comme une clé unique au niveau mondial qui doit être mappée à exactement un compte ALM. La plateforme applique donc une restriction stricte selon laquelle **aucun compte ne peut partager le même domaine personnalisé**. Ceci est requis pour la sécurité, le routage et le référencement : la couche de routage et la pile non connectée utilisent le domaine pour rechercher la configuration de compte correcte (y compris son compte non connecté JSON, les menus Experience Builder, le branding et les points d’entrée TDA/search),

Autoriser le même domaine personnalisé sur deux comptes rendrait impossible de garantir les données du compte retournées, pourrait provoquer des fuites entre locataires et corromprait également les artefacts générés tels que sitemap.xml et robots.txt qui sont produits par compte mais découverts par les moteurs de recherche par hôte. Sur le plan opérationnel, cela signifie que lorsque vous attribuez ou déplacez un domaine personnalisé, vous devez d&#39;abord vous assurer qu&#39;il n&#39;est pas associé à un autre compte (ou l&#39;y radier), et l&#39;outillage interne d&#39;Adobe rejettera les tentatives de liaison du même domaine à plusieurs comptes.

#### Mise en cache des ressources du navigateur dans l’expérience hors connexion

Dans l’expérience hors connexion de Adobe Learning Manager, la mise en cache des ressources dans le navigateur est un élément essentiel de la stratégie de performances et d’évolutivité, car les pages publiques doivent gérer un trafic marketing important et parfois chargé avec une faible latence et une charge d’origine minimale. Les actifs statiques et semi-statiques tels que le shell de HTML non connecté (par exemple, index.html/guest.html), la configuration au niveau du compte JSON (account.json ou config.json), la mise en page JSON Experience Builder (menus, mises en page de widgets, paramètres de carte), CSS, JS, les images et les favicons sont servis à partir d’un CDN Akamai (cpcontents.adobe.com / cpcontent.adobe.com) avec des en-têtes de cache qui encouragent la réutilisation côté CDN et côté navigateur, de sorte qu’après le chargement de la première page, le navigateur peut effectuer le rendu des pages non connectées suivantes en grande partie à partir de son cache, en les revalidant uniquement lorsque nécessaire via ETag ou Last-Modified.

## Assistances à la tâche multilingues

### Introduction

Les assistances à la tâche multilingues dans Adobe Learning Manager (ALM) permettent aux auteurs et aux administrateurs de fournir des documents d’accompagnement, des guides ou des ressources dans plusieurs langues dans une seule entrée d’assistance à la tâche. Les élèves de différentes régions peuvent accéder aux documents pertinents dans leur langue préférée, ce qui améliore la compréhension, la conformité et l&#39;expérience utilisateur.

### Comportement précédent

Auparavant, les assistances à la tâche dans ALM ne prenaient en charge qu’un seul fichier de contenu par assistance à la tâche, même lorsque le nom et la description pouvaient être localisés. Pour fournir la même ressource dans plusieurs langues, les auteurs devaient créer des assistances à la tâche distinctes pour chaque langue. Cela a entraîné des dédoublements, de la confusion et une augmentation des frais généraux administratifs. Il n&#39;existait pas de moyen unifié de gérer les ressources multilingues, ce qui rendait difficile la cohérence et le suivi de l&#39;utilisation.

### Cas d’utilisation

* **Activation du personnel à l&#39;échelle mondiale** : fournissez des manuels de sécurité, des guides de processus ou des documents de référence dans plusieurs langues à un personnel diversifié.
* **Conformité à la réglementation** : assurez-vous que tous les employés reçoivent la même documentation sur la conformité dans leur langue maternelle.
* **Intégration cohérente** : fournissez des listes de contrôle d’intégration ou des FAQ dans les langues locales pour les nouvelles recrues du monde entier.
* **Réduction de la duplication** : gérez toutes les versions linguistiques d&#39;une assistance à la tâche en une seule entrée, ce qui simplifie les mises à jour et la création de rapports.

### Fonctionnalités clés

* **Prise en charge de plusieurs langues** : joignez un fichier ou une URL unique pour chaque langue prise en charge dans une seule assistance à la tâche.
* **Nom et description localisés** : entrez le nom et la description de l&#39;assistance à la tâche dans chaque langue.
* **Gestion unifiée** : modifiez, mettez à jour et générez des rapports sur toutes les versions linguistiques à partir d&#39;un seul endroit.
* **Rétrocompatibilité** : les assistances à la tâche unilingues existantes sont automatiquement répliquées dans toutes les langues ajoutées jusqu’à ce que de nouveaux fichiers soient chargés.

### Création d’une assistance à la tâche multilingue

1. Accédez au rôle Auteur et sélectionnez **Assistances à la tâche**.
2. Sélectionnez **Créer une assistance à la tâche**.
3. Entrez le nom et la description de l’assistance à la tâche dans la langue par défaut.
4. Ajoutez le fichier de contenu principal ou l’URL de la langue par défaut.
5. Enregistrez l’assistance à la tâche.

### Ajout de langues supplémentaires

1. Dans l&#39;éditeur d&#39;assistance à la tâche, sélectionnez **Ajouter une langue**.
2. Sélectionnez la ou les langues souhaitées dans la liste.
3. Pour chaque langue ajoutée :
   * Entrez le nom et la description traduits.
   * Chargez le fichier de contenu correspondant ou fournissez une URL spécifique à la langue.
4. Répétez l’opération pour toutes les langues requises.

### Modifier et gérer les langues

1. Pour mettre à jour un fichier ou une description pour une langue spécifique, sélectionnez l’onglet de langue et apportez les modifications nécessaires.
2. Si une langue est ajoutée après la publication de l’assistance à la tâche, le fichier d’origine est automatiquement affecté à la nouvelle langue jusqu’à ce qu’un fichier unique soit chargé.
3. Supprimez ou remplacez les fichiers pour n’importe quelle langue selon vos besoins.

### Publish et expérience de l’élève

1. Une fois toutes les langues et tous les fichiers ajoutés, publiez l’assistance à la tâche.
2. Les élèves voient l’assistance à la tâche dans la langue de contenu sélectionnée, avec le fichier ou l’URL approprié.
3. Si la langue d’un élève n’est pas disponible, le fichier de langue par défaut est affiché.

### Rapports

1. Téléchargez les rapports d’assistance à la tâche pour afficher les détails de tous les fichiers et langues associés à chaque assistance à la tâche.
2. Les rapports incluent la langue, le nom du fichier et les données d’utilisation pour le suivi.

### Bonnes pratiques

* Fournissez des traductions précises pour les noms, les descriptions et les fichiers de contenu.
* Révisez et mettez à jour les fichiers régulièrement pour assurer la cohérence entre les langues.
* Utilisez des conventions de dénomination claires pour distinguer les fichiers pour différentes langues.
* Testez l’expérience de l’élève en changeant de langue de contenu pour vérifier que les fichiers sont correctement distribués.

### Dépannage

* **Fichier manquant pour une langue** : le fichier par défaut est affiché. Vérifiez que le fichier correct est chargé dans toutes les langues.
* **Assistances à la tâche héritées** : ajoutez de nouveaux fichiers de langue pour remplacer les originaux répliqués automatiquement.
* **Langue affichée incorrecte** : vérifiez les paramètres de langue du contenu de l&#39;élève et la configuration de langue de l&#39;assistance à la tâche.

Les assistances à la tâche multilingues vous permettent de fournir des ressources de support à un public mondial en une seule entrée, de réduire les doublons et de vous assurer que chaque élève reçoit les bonnes informations dans sa langue préférée. Cette fonctionnalité améliore l’accessibilité, la conformité et l’efficacité administrative dans Adobe Learning Manager.

## Obtenez des réponses avec l’assistant AI pour les élèves

L’assistant AI pour les élèves est un assistant conversationnel basé sur l’IA au sein de Adobe Learning Manager conçu pour vous guider vers les informations dont vous avez besoin plus rapidement. En posant des questions en langage naturel, vous pouvez obtenir des explications contextuelles, faire apparaître des cours pertinents et récupérer des informations à partir du contenu d’apprentissage, sans parcourir manuellement les catalogues.

### Capacités

* **Réponse intelligente aux questions :** gère les conversations à tour unique et à tour multiple, ce qui vous permet de poser des questions naturellement. Les réponses sont dérivées des cours, des parcours d’apprentissage, des certifications et des assistances à la tâche.
* **Réponses basées sur le contenu avec des citations :** extrait les informations directement du matériel d&#39;apprentissage et inclut des citations qui renvoient au cours, module ou ressource d&#39;origine.
* **Compatibilité étendue du contenu :** prend en charge un large éventail de formats, notamment des documents, des présentations, des vidéos, des fichiers audio, du contenu de HTML et des modules SCORM (Sharable Content Object Reference Model).
* **Expérience utilisateur transparente :** disponible sous forme de panneau latéral sur les pages de l’élève, conservant l’historique de conversation basé sur la session pour assurer la continuité.
* **Contrôles administrateur performants :** les administrateurs peuvent activer ou désactiver l&#39;assistant, limiter l&#39;accès par groupes d&#39;utilisateurs et choisir les catalogues internes à utiliser comme source pour les réponses générées par l&#39;IA.

### Avantages

* **Accès plus rapide aux connaissances :** vous recevez des réponses instantanées à vos questions, ce qui élimine la nécessité de parcourir plusieurs cours ou documents.
* **Engagement supérieur :** les interactions conversationnelles rendent l&#39;expérience d&#39;apprentissage plus naturelle, intuitive et accessible.
* **Meilleure compréhension :** vous pouvez poser des questions de suivi pour clarifier les concepts et explorer les sujets plus en profondeur.
* **Prise en charge de l’apprentissage évolutif :** les réponses automatisées et basées sur l’IA réduisent la dépendance à l’égard des experts et des équipes de support.

En savoir plus sur [l&#39;Assistant IA pour les élèves](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

## Prise en charge des pistes de texte vidéo multilingues (VTT)

La prise en charge des pistes de texte vidéo multilingues (VTT) dans Adobe Learning Manager permet aux auteurs de fournir des sous-titres et des légendes pour le contenu vidéo et audio dans plusieurs langues. Cette fonctionnalité rationalise la localisation, rend la formation accessible à un public international et garantit la conformité aux normes d’accessibilité. Les auteurs peuvent générer, traduire, réviser et modifier automatiquement les fichiers VTT directement sur la plateforme.

### Cas d’utilisation

* **Formation globale :** proposez du contenu vidéo avec sous-titres dans plusieurs langues pour atteindre des élèves internationaux.
* **Conformité à l’accessibilité :** indiquez les sous-titres aux utilisateurs malentendants dans leur langue préférée.
* **Localisation plus rapide :** réduisez les efforts manuels et accélérez le déploiement de contenu en générant et en traduisant automatiquement les fichiers VTT.
* **Expérience cohérente :** assurez-vous que tous les élèves reçoivent les mêmes informations, quelle que soit la langue.

### Fonctionnalités clés

* **Génération VTT automatique :** chargez un fichier vidéo ou audio et générez automatiquement des légendes VTT dans la langue d&#39;origine.
* **Traduction multilingue :** traduisez les sous-titres dans l’une des 39 langues non anglophones prises en charge.
* **Révision et modification dans l’application :** révisez, modifiez et téléchargez les fichiers VTT avant de les publier.
* **Notifications :** recevez des notifications dans l&#39;application lorsque la génération et la traduction VTT sont terminées.
* **Publication fluide :** légendes finalisées Publish auxquelles les élèves peuvent accéder dans la langue de leur choix.

### Chargement de contenu et génération de VTT

1. Accédez à la bibliothèque de contenu et sélectionnez **Ajouter du contenu**.
2. Chargez votre fichier MP3 ou MP4.
3. Dans la boîte de dialogue de téléchargement, sélectionnez l&#39;option **Générer la traduction**.
4. Sélectionnez la langue du contenu d’origine (la langue par défaut est celle du fichier).
5. Sélectionnez d’autres langues cibles pour la traduction (jusqu’à 39 prises en charge).
6. Sélectionnez **Enregistrer**. Le système commence à générer et à traduire des fichiers VTT.

### Suivi de la progression

1. Après l’enregistrement, la nouvelle entrée de contenu apparaît dans la bibliothèque de contenu.
2. Un indicateur de progression affiche l’état de la génération et de la traduction VTT.
3. Vous recevez une notification dans l’application une fois le processus terminé.

### Révision et modification de fichiers VTT

1. Dans la bibliothèque de contenu, ouvrez le contenu en mode **Modifier**.
2. Pour chaque langue, sélectionnez le lien **Révision** en regard du fichier VTT.
3. Une fenêtre contextuelle affiche les légendes pour cette langue.
4. Modifiez les sous-titres directement dans la fenêtre contextuelle ou téléchargez le fichier VTT pour le modifier hors ligne.
5. Après avoir apporté des modifications, téléchargez ou collez de nouveau les légendes révisées dans la fenêtre contextuelle.
6. Enregistrez vos modifications.

### Sous-titres Publish

1. Une fois satisfait de toutes les légendes de langue, publiez le contenu.
2. Les élèves voient les options de sous-titre dans toutes les langues publiées lorsqu’ils visionnent la vidéo.

### Informations supplémentaires

* **Langues prises en charge :** les 39 langues autres que l&#39;anglais sont prises en charge par Adobe Learning Manager.
* **Notifications :** les auteurs sont avertis lorsque la génération et la traduction VTT sont terminées.
* **Flexibilité de modification :** les sous-titres peuvent être modifiés dans l&#39;application ou hors ligne et rechargés.
* **Évolutivité :** conçue pour les besoins de localisation et d&#39;accessibilité à l&#39;échelle de l&#39;entreprise.
* **Pas besoin de chargement VTT manuel :** le système peut générer des fichiers VTT à partir de zéro à l&#39;aide de la vidéo/audio chargée.

### Bonnes pratiques

* Vérifiez toujours l’exactitude des sous-titres générés automatiquement avant de publier.
* Fournir des traductions pour tous les principaux groupes d&#39;élèves afin de maximiser l&#39;accessibilité.
* Utilisez le système de notification pour rester informé du statut du traitement.
* Mettez régulièrement à jour les sous-titres si le contenu vidéo change.

### Dépannage

* Si la génération VTT échoue, assurez-vous que votre fichier est dans un format pris en charge (MP3/MP4).
* Pour les langues manquantes, vérifiez qu’elles sont prises en charge et sélectionnées pendant le téléchargement.
* Si les sous-titres ne sont pas synchronisés, utilisez l’éditeur intégré à l’application pour ajuster la durée.

La prise en charge de la VTT multilingue vous permet de proposer efficacement des expériences d’apprentissage vidéo accessibles et localisées. En utilisant la génération automatique, la traduction et l’édition intégrée à l’application, vous pouvez vous assurer que votre contenu atteint et prend en charge tous les élèves, quelle que soit la langue.

## Création de certificats personnalisés

Les certificats personnalisés dans Adobe Learning Manager (ALM) permettent aux administrateurs et aux auteurs de concevoir, gérer et émettre des certificats personnalisés pour les élèves. La fonctionnalité comprend un éditeur par glisser-déposer, des champs dynamiques, une prise en charge multilingue et des arrière-plans générés par l’IA afin que les organisations puissent créer des certificats de marque sans expertise technique.

### Comportement précédent

Auparavant, la création de certificats dans ALM était limitée par la rigidité du modèle, le manque de personnalisation et les obstacles techniques (tels que l’édition de HTML). Les clients demandaient des moyens plus simples de concevoir des certificats, d’ajouter des champs dynamiques (comme le nom de l’élève ou celui de l’instructeur) et de prendre en charge plusieurs langues, tout en conservant la cohérence de la marque et l’attrait visuel.

### Cas d’utilisation

* **Reconnaissance de la marque** : émettez des certificats avec les logos, les couleurs et les polices de l’entreprise à des fins de conformité, de formation ou de réussite.
* **Personnalisation dynamique** : renseignez automatiquement les noms des élèves, des instructeurs et d’autres champs actifs.
* **Diffusion multilingue** : fournissez des certificats dans plusieurs langues aux élèves du monde entier.
* **Conception flexible** : créez des certificats de type paysage ou portrait, utilisez des arrière-plans générés par l’IA et prévisualisez avant de publier.

### Accès aux certificats personnalisés

1. Accédez à la section **Réalisations** dans la page d&#39;accueil de l&#39;administrateur (auparavant appelée **Badges**).
2. Sélectionnez **Certificats** pour afficher, créer ou gérer les modèles de certificats.

### Création d’un certificat

1. Sélectionnez **Créer un certificat**.
2. Sélectionnez l’orientation Portrait ou Paysage.
3. Sélectionnez un modèle existant ou commencez à partir d’une zone de travail vierge.
4. Entrez un nom de certificat et une langue par défaut.
5. Utilisez l’éditeur glisser-déposer pour ajouter :
   * Champs de texte (avec options de police, de couleur et de positionnement)
   * Images (logos, icônes, etc.)
   * Champs dynamiques (nom de l’élève, nom de l’instructeur, etc.)
   * Arrière-plans de certificat (couleur unie, image téléchargée ou image générée par l’IA)
6. Pour les arrière-plans générés par l’IA : entrez une invite (par exemple, « étudiants dans une salle de classe ») pour générer des arrière-plans à l’aide de l’IA.

### Ajouter des champs dynamiques

Les champs dynamiques dans les certificats personnalisés de Adobe Learning Manager sont des espaces réservés qui renseignent automatiquement les informations pertinentes, telles que le nom de l’élève, le nom de l’instructeur ou d’autres données spécifiques au compte. Lors de la génération du certificat, ils permettent d’obtenir des certificats personnalisés et contextuels sans modification manuelle.

1. Insérez des variables dynamiques telles que le nom de l’élève, le nom du formateur ou d’autres champs actifs.
2. Les champs sont renseignés automatiquement lorsque le certificat est émis.

### Prise en charge multilingue

1. Ajoutez de nouvelles langues (par exemple, français, allemand) au certificat.
2. Entrez le texte traduit pour chaque langue.
3. Gérez les traductions et prévisualisez les certificats dans chaque langue.

### Aperçu et publication

1. Utilisez la fonction d’aperçu pour voir comment le certificat apparaît aux élèves.
2. Téléchargez ou imprimez l’aperçu pour révision.
3. Enregistrez-le en tant que brouillon pour poursuivre les modifications ultérieurement ou publiez-le lorsqu’il sera prêt.

### Application de certificats

1. Les administrateurs peuvent définir des certificats par défaut pour le compte.
2. Les auteurs peuvent joindre des certificats à des instances d’objets d’apprentissage spécifiques (cours, parcours, etc.).
3. Sélectionnez différents certificats au niveau de l’instance selon vos besoins.

### Gestion des certificats

1. Affichez les certificats publiés et les brouillons dans la bibliothèque.
2. Modifiez, mettez à jour ou supprimez des modèles selon vos besoins.
3. Les certificats peuvent être réutilisés sur plusieurs instances.

Les certificats personnalisés dans ALM offrent un moyen flexible de concevoir et d’émettre des certificats personnalisés, de marque et multilingues. La fonctionnalité simplifie la gestion des certificats, améliore la reconnaissance des élèves et prend en charge les besoins mondiaux en matière de conformité et de branding.

## Assistances à la tâche multilingues

Les assistances à la tâche multilingues dans Adobe Learning Manager (ALM) permettent aux auteurs et aux administrateurs de fournir des documents d’accompagnement, des guides ou des ressources dans plusieurs langues dans une seule entrée d’assistance à la tâche. Les élèves de différentes régions peuvent accéder aux documents pertinents dans leur langue préférée, ce qui améliore l’accessibilité, la conformité et l’expérience utilisateur.

### Comportement précédent

Auparavant, ALM n’autorisait qu’un seul fichier de contenu par assistance à la tâche, même si le nom et la description pouvaient être localisés. Pour fournir la même ressource dans plusieurs langues, les auteurs devaient créer des assistances à la tâche distinctes pour chaque langue. Cela a entraîné des dédoublements, de la confusion et un effort administratif accru. Il n&#39;existait pas de moyen unifié de gérer les ressources multilingues, ce qui rendait difficile la cohérence et le suivi de l&#39;utilisation.

### Cas d’utilisation

* **Activation du personnel à l&#39;échelle mondiale** : fournissez des manuels de sécurité, des guides de processus ou des documents de référence dans plusieurs langues à un personnel diversifié.
* **Conformité à la réglementation** : assurez-vous que tous les employés reçoivent la même documentation sur la conformité dans leur langue maternelle.
* **Intégration cohérente** : fournissez des listes de contrôle d’intégration ou des FAQ dans les langues locales pour les nouvelles recrues du monde entier.
* **Réduction de la duplication** : gérez toutes les versions linguistiques d&#39;une assistance à la tâche en une seule entrée, ce qui simplifie les mises à jour et la création de rapports.

### Création d’une assistance à la tâche multilingue

1. Accédez au rôle Auteur et sélectionnez **Assistances à la tâche**.
2. Sélectionnez **Créer une assistance à la tâche**.
3. Entrez le nom et la description de l’assistance à la tâche dans la langue par défaut.
4. Chargez le fichier de contenu principal ou fournissez une URL pour la langue par défaut.
5. Enregistrez l’assistance à la tâche.

### Ajout de langues supplémentaires

1. Dans l&#39;éditeur d&#39;assistance à la tâche, sélectionnez **Ajouter une langue**.
2. Sélectionnez la ou les langues souhaitées dans la liste.
3. Pour chaque langue ajoutée :
   * Entrez le nom et la description traduits.
   * Chargez le fichier de contenu correspondant ou fournissez une URL spécifique à la langue.
4. Répétez l’opération pour toutes les langues requises.

### Modifier et gérer les langues

1. Pour mettre à jour un fichier ou une description pour une langue spécifique, sélectionnez l’onglet de langue et apportez les modifications nécessaires.
2. Si une langue est ajoutée après la publication de l’assistance à la tâche, le fichier d’origine est automatiquement affecté à la nouvelle langue jusqu’à ce qu’un fichier unique soit chargé.
3. Supprimez ou remplacez les fichiers pour n’importe quelle langue selon vos besoins.

### Publish et expérience de l’élève

1. Une fois toutes les langues et tous les fichiers ajoutés, publiez l’assistance à la tâche.
2. Les élèves voient l’assistance à la tâche dans la langue de contenu sélectionnée, avec le fichier ou l’URL approprié.
3. Si la langue d’un élève n’est pas disponible, le fichier de langue par défaut est affiché.

### Rapports

1. Téléchargez les rapports d’assistance à la tâche pour afficher les détails de tous les fichiers et langues associés à chaque assistance à la tâche.
2. Les rapports incluent la langue, le nom du fichier et les données d’utilisation pour le suivi.

Les assistances à la tâche multilingues dans ALM vous permettent de fournir des ressources de support à un public mondial en une seule entrée, de réduire la duplication et de vous assurer que chaque élève reçoit les bonnes informations dans sa langue préférée. Cette fonctionnalité améliore l’accessibilité, la conformité et l’efficacité administrative dans Adobe Learning Manager.

## Améliorations de la lecture pour les cours générés par Captivate

La mise à jour améliore considérablement l’expérience de lecture du contenu Adobe Captivate dans ALM en introduisant une interface unifiée et rationalisée.

Le lecteur ALM affiche désormais une seule table des matières consolidée, masquant la table des matières du Captivate, et fournit des indicateurs d’achèvement clairs au niveau des diapositives, y compris des coches vertes pour le suivi visuel de la progression.

Le système simplifie la navigation en fusionnant les commandes de module et de cours dans une barre intuitive, réduisant ainsi la confusion de l&#39;élève.

Les commandes de progression contextuelle améliorent la convivialité en affichant les barres de progression vidéo uniquement sur les diapositives vidéo et les commandes de navigation dans les diapositives non vidéo.

En outre, le système associe désormais les notes aux numéros des diapositives plutôt qu’aux horodatages, ce qui garantit la fiabilité des exportations de PDF et la résolution des incohérences de format antérieures.

## Améliorations de la liste de contrôle

### Prise en charge multilingue de la liste de contrôle

Cette fonctionnalité vous permet de créer et de gérer des modules de liste de contrôle dans plusieurs langues. Chaque question de liste de contrôle, instruction et critère d&#39;évaluation peuvent être traduits afin que les réviseurs et les élèves interagissent avec la liste de contrôle dans leur langue préférée. Le système affiche la liste de contrôle dans la langue de contenu sélectionnée par l’utilisateur, ce qui améliore l’accessibilité et la conformité pour les équipes mondiales.

1. Ajoutez ou modifiez un module de liste de contrôle dans votre cours.
2. Sélectionnez toutes les langues que vous souhaitez prendre en charge dans les options de langue.
3. Pour chaque langue, saisissez des traductions pour chaque question de la liste de contrôle, instruction et critère d&#39;évaluation.
4. Enregistrez vos modifications. La liste de contrôle s’affiche dans la langue de contenu sélectionnée par le réviseur ou l’élève.
5. Si vous ajoutez une nouvelle langue ultérieurement, fournissez des traductions pour toutes les questions et tous les critères avant la publication.
6. Lors du téléchargement des rapports de liste de contrôle, sélectionnez la langue de votre choix pour afficher le rapport dans cette langue.

### Pondération des questions de la liste de contrôle pour les évaluations des instructeurs

Cette fonctionnalité vous permet d’attribuer différents scores maximaux (pondération) à chaque question de liste de contrôle. Vous pouvez refléter l&#39;importance ou la difficulté variable de chaque question, ce qui favorise des évaluations plus précises et plus significatives. Le système calcule le score total en fonction de vos entrées et détermine si l’élève réussit ou échoue selon les critères que vous définissez.

1. Lorsque vous ajoutez un module de liste de contrôle, sélectionnez **Score personnalisé**.
2. Pour chaque question de la liste de contrôle, définissez une note maximale unique qui reflète son importance.
3. Définissez la note de passage globale pour la liste de contrôle.
4. Enregistrez et publiez la liste de contrôle.
5. En tant qu’instructeur ou réviseur, évaluez chaque élève en attribuant un score pour chaque question (jusqu’au maximum que vous définissez).
6. Le système calcule le score total et détermine le statut Réussite/Échec.
7. Téléchargez les rapports de liste de contrôle pour afficher les scores atteints et maximum pour chaque question et le score total.

### Liste de contrôle avec possibilité de commentaire pour le réviseur

Cette fonctionnalité permet aux réviseurs d’ajouter des commentaires pendant l’évaluation des listes de contrôle. Vous pouvez fournir des commentaires personnalisés et exploitables pour chaque élève. Vous pouvez également choisir d’afficher votre nom avec vos commentaires pour plus de transparence. Toutes les remarques sont enregistrées dans le relevé de notes de l’élève et incluses dans les rapports de liste de contrôle.

1. Lors de la configuration de la liste de contrôle, activez **Remarques du réviseur**.
2. Vous pouvez éventuellement activer **Afficher le nom du réviseur à l&#39;élève** si vous souhaitez que votre nom apparaisse avec vos commentaires.
3. Pendant l’évaluation, saisissez des commentaires ou des retours d’informations pour l’élève dans le champ de remarques fourni.
4. Indiquez si vos commentaires doivent être visibles pour l’élève.
5. Soumettez votre évaluation. Si cette option est activée, l’élève voit vos remarques et votre nom avec leurs résultats.
6. Tous les commentaires sont enregistrés dans le relevé de notes de l’élève et inclus dans les rapports de liste de contrôle pour référence ultérieure.

## Améliorations de la recherche avancée

Cette version inclut une amélioration de la recherche dans le contenu en affichant les cours dont le contenu correspond à une requête de rang supérieur. En outre, les assistances à la tâche sont désormais incluses dans le classement de recherche avancée.

## Équivalents et substituts

### Présentation

Dans de nombreuses organisations, les apprenants se trouvent dans des situations de formation où différents cours peuvent légitimement satisfaire la même exigence ? par exemple, lorsqu&#39;un nouveau cours remplace un ancien, lorsqu&#39;un cours plus complet peut remplacer un plus court ou lorsqu&#39;un cours de remplacement spécial doit être proposé.

La fonctionnalité Cours alternatifs ou parcours d’apprentissage donne à ALM un moyen formel de dire :

« Si l’élève a terminé cette formation, traitez-le comme ayant satisfait à cette exigence de formation connexe. »

La fonctionnalité fonctionne dans tous les cours et parcours d’apprentissage, garantit que les exigences en aval telles que les conditions préalables et les règles de conformité sont respectées, et le fait sans forcer les élèves à passer par du contenu redondant. Il permet également de garder les rapports exacts en enregistrant ce qui a été rempli directement par rapport à ce qui a été satisfait par l&#39;intermédiaire d&#39;un autre système.

Au cœur de la fonctionnalité, le concept d’une autre fin de formation : un état d’achèvement spécial créé automatiquement lorsqu’un élève termine une formation source configurée qui est prise en compte dans une autre formation cible.

### Équivalence et variantes

Certaines relations de formation sont bidirectionnelles, ce qui signifie que chaque cours peut répondre aux exigences de l&#39;autre. Il s&#39;agit en fait d&#39;un scénario dans lequel deux formations sont considérées comme mutuellement substituables. En revanche, les relations unidirectionnelles permettent à une formation de satisfaire à une autre exigence, mais pas l&#39;inverse. ALM modélise les deux scénarios en utilisant le même mécanisme d&#39;achèvement alternatif sous-jacent.

* **Relation bidirectionnelle :** terminer l&#39;une ou l&#39;autre formation satisfait aux exigences de l&#39;autre.
* **Relation unidirectionnelle :** terminer la formation A satisfait la formation B, mais terminer B ne satisfait pas A. Cela se produit généralement lorsqu’une version plus récente ou plus complète doit être prise en compte dans une ancienne exigence, mais pas l’inverse.

Les variantes sont le plus souvent utilisées dans les scénarios **unidirectionnels** ?par exemple, lorsqu&#39;un cours sur-ensemble plus complet couvre tout dans un cours de sous-ensemble plus simple. Le fait de remplir le sur-ensemble doit satisfaire aux exigences du sous-ensemble, mais pas nécessairement l&#39;inverse.

* Un cours plus récent et plus développé qui devrait être pris en compte dans une ancienne exigence.
* Cours conçu pour un public spécifique (par exemple, une variante régionale ou adaptée à l&#39;accessibilité) qui satisfait toujours aux mêmes exigences que le cours principal.
* Nouvelle version améliorée d&#39;un cours que l&#39;organisation souhaite compter pour une ancienne exigence, mais l&#39;ancienne version ne doit pas être prise en compte pour la nouvelle exigence.

Dans les variantes, la relation est normalement **unidirectionnelle**. Si le cours A est un cours alternatif au cours B, terminer A peut répondre aux exigences de B, mais terminer B ne répond pas nécessairement à A.

L’équivalence et le remplacement partagent le même mécanisme sous-jacent dans ALM : lorsqu’une formation source configurée est terminée, ALM produit automatiquement un remplacement pour une ou plusieurs formations cibles.

### Quels problèmes cela résout-il ?

Sans alternatives et équivalences, les administrateurs et les élèves sont confrontés à plusieurs problèmes récurrents :

* Les élèves sont fréquemment invités à répéter des cours qui couvrent le contenu qu&#39;ils ont déjà terminé dans une version ou un format différent.
* La mise à jour des programmes de conformité est plus simple, car les administrateurs peuvent remplacer ou restructurer les formations sans forcer les élèves qui ont terminé les anciennes versions à reprendre le contenu équivalent ou remplacé.
* La logique prérequise est rigide. Si un parcours nécessite un cours particulier comme condition préalable, il n&#39;existe aucun moyen propre de reconnaître qu&#39;une autre formation est suffisante.
* Les rapports et les audits sont plus difficiles. Il n&#39;y a pas de signal formel indiquant qu&#39;une exigence a été satisfaite au moyen d&#39;une autre exécution et il n&#39;y a pas de moyen simple de retracer la source du crédit.

La fonctionnalité Variantes et équivalences aborde ces problèmes en procédant comme suit :

* Empêcher les efforts en double pour les élèves lorsque les alternatives sont valides.
* Autoriser les administrateurs à modifier les structures de formation (par exemple, échanger un cours à l’intérieur d’un parcours) sans interrompre les achèvements pour les élèves qui ont suivi la version antérieure.
* Permettre aux conditions préalables et aux contrôles de conformité de respecter à la fois les finalisations directes et les finalisations alternatives ou équivalentes.
* Indiquer clairement, dans les transcriptions et les rapports, si une formation a été suivie directement ou si elle a été suivie par une autre relation, avec laquelle la formation a servi de source.

### Fonctionnement conceptuel de la fonctionnalité

La fonctionnalité repose sur trois idées principales : **relations**, **achèvement alternatif** et **comportement en aval**.

#### Relations entre les formations

Les administrateurs définissent les relations entre les cours et les parcours d’apprentissage. Pour chaque relation, ils choisissent une **source** et une ou plusieurs **cibles**. Un cours peut avoir jusqu’à 30 objectifs en fonction du nombre de formations antérieures ou connexes qu’il doit satisfaire.

Pour l&#39;équivalence, les administrateurs peuvent rendre la relation **bidirectionnelle** s&#39;ils souhaitent que les deux formations se satisfassent mutuellement. Pour les variantes, les administrateurs conservent normalement le sens une fois pour indiquer que seules certaines substitutions sont autorisées.

Ces relations sont stockées au niveau de la formation, pas au niveau de l’élève. Une fois configurés et activés, ils s’appliquent à toutes les terminaisons actuelles et futures de la formation source, sous réserve des paramètres au niveau du compte*tels que l’activation ou non de l’achèvement rétroactif.

### Autre achèvement

Lorsqu&#39;un élève termine une formation source, ALM examine toutes les relations alternatives ou équivalentes configurées et, pour chaque formation cible pertinente, crée un **enregistrement d&#39;achèvement alternatif**. Cet enregistrement est différent d’une fin normale :

* Elle marque la formation cible pour l’élève, mais assure le suivi pour s’assurer qu’elle a été terminée via une alternative ou une équivalence plutôt que directement.
* Il enregistre quelle formation source a été utilisée pour satisfaire la cible.
* Il est stocké dans une structure dédiée afin que les rapports puissent faire la distinction entre les finalisations directes et alternatives.

Les élèves verront une autre réalisation même s’ils ne sont pas inscrits. Le rapport Relevé de notes de l’élève (LT) inclut uniquement les enregistrements des formations auxquelles l’élève est inscrit.

### Expérience de l’application de l’élève pour des achèvements alternatifs et équivalents

Les achèvements alternatifs et équivalents apparaissent distinctement dans l’application de l’élève afin que celui-ci puisse clairement comprendre comment une exigence de formation a été satisfaite, tout en conservant la cohérence avec les relevés de notes et les rapports.

#### Comportement de la carte LO

#### Autre état d’achèvement

Lorsqu&#39;un élève termine une formation via une autre relation ou une relation équivalente, la carte d&#39;objet d&#39;apprentissage affiche un statut distinct tel que **Terminé via une autre relation**.\
Cette distinction visuelle aide les élèves à différencier les achèvements directs des achèvements accordés via des relations configurées.

#### Indicateur de méthode d’achèvement

La carte objet d&#39;apprentissage inclut un indicateur de méthode d&#39;achèvement (par exemple, une étiquette ou une icône) pour montrer que l&#39;achèvement a été atteint via une **alternative**.\
Si une autre fin est révoquée ultérieurement en raison de modifications telles que l&#39;inachèvement rétroactif ou la suppression de la formation source, la carte objet d&#39;apprentissage est mise à jour pour refléter la **variante (révoquée)**.

#### Transparence et détails d’audit

Les élèves peuvent ouvrir la carte objet d’apprentissage pour afficher des détails supplémentaires, notamment :

* Cours ou parcours d’apprentissage source qui a accordé l’autre achèvement
* Date d’achèvement associée à la formation source

Cela garantit la transparence et prend en charge les audits et les examens de conformité.

#### Filtrage et vues

#### Filtre Méthode d’achèvement

L’application de l’élève fournit un filtre qui permet aux élèves de distinguer entre :

* Achèvements **directs**
* **Autres** finalisations
* **Toutes les** finalisations

Cela permet aux élèves de comprendre rapidement comment leurs exigences d’apprentissage ont été remplies.

#### Vues de transcription et de progression

Le filtre de méthode d&#39;achèvement est disponible dans les vues en regard de learner*faces telles que :

* Relevés de notes d’apprentissage
* Sections de suivi de la progression et de l’achèvement

Ces points de vue indiquent clairement quelles formations ont été complétées directement et lesquelles ont été satisfaites par des suppléants ou des équivalences.

#### Alignement des rapports

La logique de filtrage dans l&#39;application de l&#39;élève s&#39;aligne sur la colonne **Méthode d&#39;achèvement** utilisée dans les rapports.\
Cela garantit la cohérence entre ce que les élèves voient dans l’interface utilisateur et ce que les administrateurs voient dans les exportations et les rapports de conformité.

#### Fin *à* fin du flux

#### Pour les élèves

1. Accédez à **Mon apprentissage** ou **Cours terminés** dans l’application de l’élève.
2. Passez en revue les cartes d&#39;objet d&#39;apprentissage pour identifier les formations marquées comme **Terminées via un autre**.
3. Ouvrez une carte objet d’apprentissage pour afficher les détails sur la formation source et la date d’achèvement.
4. Utilisez le menu de filtre dans les vues de transcription ou de liste de cours pour sélectionner **Direct**, **Alternatif** ou **Tous**.
5. Passez en revue la liste mise à jour en fonction de la méthode d’achèvement sélectionnée.

#### Pour les administrateurs et auteurs

1. Configurez des relations équivalentes ou alternatives entre les cours ou les parcours d’apprentissage dans l’interface d’administration.
2. Vérifiez que les autres achèvements sont correctement reflétés sur les cartes d&#39;objet d&#39;apprentissage et dans les filtres en regard de l&#39;élève.
3. Utilisez les vues et les rapports des élèves pour confirmer la cohérence entre l’interface utilisateur et les données exportées.
4. Si une formation source est retirée ou supprimée, vérifiez que les cartes LO affectées sont mises à jour en conséquence (par exemple, en affichant **Autre (Révoqué)** le cas échéant).

## Comportement d’achèvement et d’inachèvement rétroactif

ALM prend en charge l’achèvement rétroactif et l’inachèvement rétroactif pour garantir que les relations alternatives et équivalentes restent exactes au fil du temps, même lorsque des relations sont créées, modifiées ou supprimées une fois que les élèves ont déjà terminé la formation.

### Achèvement rétroactif

#### Définition

Lorsque l’achèvement rétroactif est activé, les élèves qui ont terminé un cours source dans le passé reçoivent automatiquement un autre achèvement pour le cours cible si une relation équivalente ou alternative est créée ultérieurement.\
Cela garantit que l’apprentissage de l’histoire est respecté sans exiger des élèves qu’ils reprennent la formation.

#### Fonctionnement du logiciel

1. Un administrateur active la saisie semi-automatique rétroactive au niveau du compte.
2. L’administrateur définit une relation équivalente ou alternative entre une formation source et une formation cible.
3. Le système analyse les enregistrements d’achèvement historiques pour la formation source.
4. Les élèves éligibles se voient attribuer une autre fin pour la formation cible.
5. Ces enregistrements apparaissent comme **Terminés via un autre** dans les relevés de notes et les rapports des élèves.

### Inachèvement rétroactif

#### Définition

Lorsque l’inachèvement rétroactif est activé, les autres fins de production sont révoquées si la relation équivalente ou alternative sous-jacente est supprimée ou si la formation source est supprimée.\
Cela garantit que le système reflète les relations de formation actuelles et valides.

#### Fonctionnement du logiciel

1. Un administrateur active l’inachèvement rétroactif au niveau du compte.
2. L’administrateur supprime une autre relation ou une relation équivalente, ou supprime la formation source.
3. Le système identifie les élèves qui ont reçu un autre achèvement par le biais de la relation affectée.
4. Les autres enregistrements d&#39;achèvement correspondants sont révoqués.
5. Les enregistrements révoqués sont marqués comme **Alternatif (révoqué)** dans les transcriptions et les rapports pour la visibilité de l’audit.

### Impact sur les conditions préalables

Les achèvements alternatifs (y compris ceux accordés rétroactivement) sont considérés comme des achèvements valides lors de l&#39;évaluation des conditions préalables.\
Si un élève a **Terminé via une autre**, il est autorisé à poursuivre les cours qui nécessitent la formation cible.

Si une autre fin est révoquée ultérieurement par inachèvement rétroactif, l’élève peut perdre son éligibilité aux cours qui dépendaient de cette condition préalable.

### Impact sur les parcours d’apprentissage et les certifications

Les autres achèvements contribuent à la progression et à l’achèvement des parcours d’apprentissage et des certifications.\
Les élèves peuvent progresser ou terminer ces programmes lorsque les formations requises sont satisfaites via des relations alternatives ou équivalentes.

Si une autre achèvement est révoqué, les parcours d’apprentissage ou certifications concernés peuvent perdre leur progression ou l’état d’achèvement jusqu’à ce que l’exigence soit remplie via une achèvement valide.

### Fin *à* fin du workflow

#### Activation de l&#39;achèvement ou de l&#39;inachèvement rétroactif

1. Les administrateurs accèdent aux paramètres du compte et activent l’achèvement et/ou l’inachèvement rétroactifs.
2. Les administrateurs créent, modifient ou suppriment des relations équivalentes ou alternatives entre les formations.

#### Actions système

* **Pour l&#39;achèvement rétroactif :**\
  Le système attribue d&#39;autres déclarations de production en fonction des déclarations de production d&#39;origine historiques.
* **Pour inachèvement rétroactif :**\
  Le système révoque les autres achèvements lorsque des relations sont supprimées ou des formations sources supprimées.

#### Expérience des élèves

Les élèves voient les états d’achèvement mis à jour sur les cartes d’objet d’apprentissage et dans les relevés de notes, tels que :

* **Terminé via un autre**
* **Alternative (Révoquée)**

Les vérifications de prérequis, la progression du parcours d’apprentissage et l’état de certification se mettent à jour de manière dynamique en fonction de l’état d’achèvement actuel.

#### Rapports et audit

Toutes les modifications rétroactives sont reflétées dans le rapport Relevé de notes de l’apprentissage (LT).\
Les rapports font clairement la distinction entre les déclarations de production directes, les déclarations de production alternatives et les déclarations de production alternatives révoquées pour prendre en charge la conformité, les enquêtes et les audits.

### Comportement d’achèvement et d’inachèvement rétroactif

ALM prend en charge l’achèvement rétroactif et l’inachèvement rétroactif pour garantir que les relations alternatives et équivalentes restent exactes au fil du temps, même lorsque des relations sont créées, modifiées ou supprimées une fois que les élèves ont déjà terminé la formation.

#### Achèvement rétroactif

#### Définition

Lorsque l’achèvement rétroactif est activé, les élèves qui ont terminé un cours source dans le passé reçoivent automatiquement un autre achèvement pour le cours cible si une relation équivalente ou alternative est créée ultérieurement.\
Cela garantit que l’apprentissage de l’histoire est respecté sans exiger des élèves qu’ils reprennent la formation.

#### Fonctionnement du logiciel

1. Un administrateur active la saisie semi-automatique rétroactive au niveau du compte.
2. L’administrateur définit une relation équivalente ou alternative entre une formation source et une formation cible.
3. Le système analyse les enregistrements d’achèvement historiques pour la formation source.
4. Les élèves éligibles se voient attribuer une autre fin pour la formation cible.
5. Ces enregistrements apparaissent comme **Terminés via un autre** dans les relevés de notes et les rapports des élèves.

#### Inachèvement rétroactif

#### Définition

Lorsque l’inachèvement rétroactif est activé, les autres fins de production sont révoquées si la relation équivalente ou alternative sous-jacente est supprimée ou si la formation source est supprimée.\
Cela garantit que le système reflète les relations de formation actuelles et valides.

#### Fonctionnement du logiciel

1. Un administrateur active l’inachèvement rétroactif au niveau du compte.
2. L’administrateur supprime une autre relation ou une relation équivalente, ou supprime la formation source.
3. Le système identifie les élèves qui ont reçu un autre achèvement par le biais de la relation affectée.
4. Les autres enregistrements d&#39;achèvement correspondants sont révoqués.
5. Les enregistrements révoqués sont marqués comme **Alternatif (révoqué)** dans les transcriptions et les rapports pour la visibilité de l’audit.

#### Impact sur les conditions préalables

Les achèvements alternatifs (y compris ceux accordés rétroactivement) sont considérés comme des achèvements valides lors de l&#39;évaluation des conditions préalables.\
Si un élève a **Terminé via une autre**, il est autorisé à poursuivre les cours qui nécessitent la formation cible.

Si une autre fin est révoquée ultérieurement par inachèvement rétroactif, l’élève peut perdre son éligibilité aux cours qui dépendaient de cette condition préalable.

#### Impact sur les parcours d’apprentissage et les certifications

Les autres achèvements contribuent à la progression et à l’achèvement des parcours d’apprentissage et des certifications.\
Les élèves peuvent progresser ou terminer ces programmes lorsque les formations requises sont satisfaites via des relations alternatives ou équivalentes.

Si une autre achèvement est révoqué, les parcours d’apprentissage ou certifications concernés peuvent perdre leur progression ou l’état d’achèvement jusqu’à ce que l’exigence soit remplie via une achèvement valide.

#### Fin *à* fin du workflow

#### Activation de l&#39;achèvement ou de l&#39;inachèvement rétroactif

1. Les administrateurs accèdent aux paramètres du compte et activent l’achèvement et/ou l’inachèvement rétroactifs.
2. Les administrateurs créent, modifient ou suppriment des relations équivalentes ou alternatives entre les formations.

#### Actions système

* **Pour l&#39;achèvement rétroactif :**\
  Le système attribue d&#39;autres déclarations de production en fonction des déclarations de production d&#39;origine historiques.
* **Pour inachèvement rétroactif :**\
  Le système révoque les autres achèvements lorsque des relations sont supprimées ou des formations sources supprimées.

#### Expérience des élèves

Les élèves voient les états d’achèvement mis à jour sur les cartes d’objet d’apprentissage et dans les relevés de notes, tels que :

* **Terminé via un autre**
* **Alternative (Révoquée)**

Les vérifications de prérequis, la progression du parcours d’apprentissage et l’état de certification se mettent à jour de manière dynamique en fonction de l’état d’achèvement actuel.

#### Rapports et audit

Toutes les modifications rétroactives sont reflétées dans le rapport Relevé de notes de l’apprentissage (LT).\
Les rapports font clairement la distinction entre les déclarations de production directes, les déclarations de production alternatives et les déclarations de production alternatives révoquées pour prendre en charge la conformité, les enquêtes et les audits.

### Webhooks pour les équivalents et les variantes

ALM fournit des événements de webhook dédiés pour des achèvements équivalents et alternatifs afin de prendre en charge l’automatisation, les intégrations et la synchronisation avec des systèmes externes.

Ces événements permettent aux consommateurs externes de faire une distinction fiable entre les compléments directs et les compléments accordés par le biais de relations alternatives ou équivalentes.

#### Présentation

Lorsqu’un élève termine un cours via une relation alternative ou équivalente, ALM déclenche un événement webhook distinct du webhook d’achèvement de cours standard.\
Cela garantit que les intégrations peuvent répondre différemment aux autres finalisations si nécessaire.

Les événements de webhook sont également déclenchés en cas d’achèvement rétroactif ou d’inachèvement rétroactif, couvrant les mises à jour historiques ainsi que les modifications de relation.

#### Comportement d’événement Webhook

* Un événement webhook distinct est déclenché lorsqu’un élève reçoit l’état **Terminé via un autre statut** pour un cours cible.
* L’événement est généré lorsque l’élève termine un cours source configuré qui satisfait la cible via une relation équivalente ou alternative.
* Ce webhook n’est pas déclenché pour les terminaisons de cours directes.
* Lorsque l’achèvement rétroactif ou l’inachèvement rétroactif est activé, des événements webhook sont émis pour chaque élève affecté et chaque cours cible.

#### Détails de la payload du webhook

La payload du webhook d’achèvement secondaire inclut les attributs clés suivants :

* **ID d’élève**\
  Identifie l’élève qui a reçu l’autre achèvement.

* **Cours source**\
  Cours ou parcours d’apprentissage que l’élève a suivi directement.

* **Cours cible**\
  Cours marqué comme terminé via la relation alternative ou équivalente.

* **Méthode d&#39;achèvement**\
  Indique que la méthode d&#39;achèvement est **alternative**.

* **Date d’achèvement**\
  Dérivé de la date de fin du cours source.

* **Type de relation**\
  Spécifie si la relation est **équivalente** ou **alternative**.

Pour les scénarios d’inachèvement rétroactifs, les événements de webhook indiquent qu’un autre achèvement existant a été révoqué.

#### Considérations relatives à l’intégration

Les systèmes externes peuvent utiliser ces événements de webhook pour :

* Mettre à jour les enregistrements d’élève
* Synchronisation de l’état d’achèvement
* Déclencher des notifications ou des workflows en aval
* Gestion des pistes d’audit à des fins de conformité

Les utilisateurs de webhook doivent explicitement différencier les terminaisons **directes** et **alternatives**.\
Les autres achèvements n&#39;accordent pas de récompenses de compétences, de badges ou de ludification et devraient être traités en conséquence dans les systèmes en aval.

### Impact du retrait et de la suppression de la formation source dans les équivalents et les suppléants

L&#39;état du cycle de vie d&#39;une formation source (retirée ou supprimée) affecte directement la façon dont les autres achèvements et les achèvements équivalents sont conservés pour les élèves. ALM traite ces scénarios différemment pour préserver la précision historique tout en s’assurant que les relations actuelles restent valides.

#### Retrait de la formation source

##### Définition

Le retrait d’un cours le rend indisponible pour les nouvelles inscriptions tout en le conservant dans le système à des fins de référence historique, de création de rapports et d’audit.

##### Impact

* Les autres achèvements existants accordés dans le cadre du cours source retiré demeurent valides.
* Les élèves qui ont précédemment terminé le cours source conservent une autre fin pour le cours cible.
* Aucune autre achèvement n&#39;est généré à partir du cours retiré, car il ne peut pas être terminé par de nouveaux élèves.
* Les relevés de notes et les rapports des élèves continuent d&#39;afficher **Terminé(e) via un autre** pour les élèves concernés.

#### Suppression de la formation source

#### Définition

La suppression d&#39;un cours le supprime entièrement du système, y compris ses enregistrements d&#39;achèvement et ses relations configurées.

#### Impact

* Si l’inachèvement rétroactif est activé, toutes les autres achèvements accordés via le cours source supprimé sont révoqués.
* Les relevés de notes et les rapports des élèves sont mis à jour pour afficher **Alternative (Révoquée)** pour la visibilité de l&#39;audit et de la conformité.
* Les élèves peuvent perdre l’état de progression ou d’achèvement dans les parcours d’apprentissage, les certifications ou les conditions préalables qui dépendaient de l’autre achèvement révoqué.
* Aucune autre achèvement alternatif ne peut être accordé à partir du cours supprimé.

#### Workflow

1. Un administrateur retire ou supprime le cours source à l’aide de l’interface d’administration.
2. Le système évalue toutes les terminaisons alternatives et équivalentes dérivées du cours source.
3. L’état d’achèvement est mis à jour en fonction de l’état du cours :
   * **Retiré :** les autres fins de production existantes restent inchangées.
   * **Supprimé :** les autres terminaisons sont révoquées si l&#39;inachèvement rétroactif est activé.
4. Les relevés de notes et les rapports des élèves reflètent l’état mis à jour pour prendre en charge les exigences de conformité et d’audit.

### Aucun enchaînement de relations

ALM ne prend pas en charge l’enchaînement de relations alternatives ou équivalentes. Les autres achèvements sont accordés uniquement pour les relations directement configurées et ne se répercutent pas sur plusieurs niveaux de cours.

#### Concept : pas d’enchaînement des relations

#### Définition

Le chaînage fait référence à la possibilité de propagation de relations alternatives ou équivalentes entre plusieurs cours.\
Par exemple, si le cours A est un cours alternatif au cours B et que le cours B est un cours alternatif au cours C, l’enchaînement impliquerait que terminer le cours A permet de terminer le cours C.

#### Politique

Le chaînage n&#39;est pas pris en charge.\
Les relations alternatives et équivalentes sont évaluées uniquement à un seul niveau. Le fait de terminer un cours source permet d’obtenir une autre fin uniquement pour son ou ses cours cibles immédiats, et non pour des cibles en aval.

#### Workflow

#### Paramétrage des relations

Un administrateur définit des relations alternatives ou équivalentes entre les cours, telles que :

* Cours A → Cours B
* Cours B → Cours C

#### Événement d’achèvement

Un élève termine le cours A directement.

#### Action système

* Le système accorde une autre fin pour le cours B, si la relation A → B est définie.
* Le système n’accorde pas d’autre achèvement pour le cours C, même s’il existe une relation B → C.

#### Exigence d’achèvement direct

Pour être remplacé dans le cours C, l’élève doit :

* Terminer directement le cours B, ou
* Terminer un cours explicitement configuré comme alternative directe ou équivalent pour le cours C.

### Implications

#### Aucun avantage indirect

Les élèves ne peuvent pas recevoir de crédit d’achèvement pour les cours situés plus bas dans une chaîne de relations à moins que chaque cours (ou son alternative directe) ne soit terminé.\
Cela garantit que les exigences d’apprentissage sont satisfaites de manière explicite et prévisible.

#### Audit et reporting simplifiés

Les rapports et les relevés de notes des élèves affichent des déclarations de fin alternatives uniquement pour les relations directes.\
Cela évite les pistes d’audit complexes à sauts multiples et garantit la clarté lors de la révision de la manière dont une achèvement a été accordée.

### Partage de catalogue avec des comptes de pairs : relations non partagées

Le partage de catalogue permet de partager des objets d’apprentissage entre comptes de pairs, mais les relations alternatives et équivalentes sont gérées indépendamment au sein de chaque compte et ne sont pas partagées.

#### Concept : partage de catalogue et relations

#### Partage de catalogue

Les comptes peuvent partager des catalogues avec des comptes de pairs pour fournir un accès aux cours, aux parcours d’apprentissage et à d’autres objets d’apprentissage entre les comptes.

#### Relations non partagées

Les relations d’achèvement alternatives, équivalentes et alternatives configurées dans le compte source ne sont pas partagées ou répliquées lorsqu’un catalogue est partagé.\
Chaque compte gère et évalue ses propres relations indépendamment.

### Workflow

#### Partage de catalogue

Un administrateur du **compte A** partage un catalogue contenant des objets d&#39;apprentissage avec le **compte B**.

#### Configuration de la relation

Le compte A peut avoir des relations alternatives ou équivalentes définies parmi les objets d’apprentissage dans le catalogue partagé.

#### Accès au compte de pairs

Le compte B reçoit l’accès aux objets d’apprentissage partagés, mais n’hérite d’aucune autre relation ou relation équivalente configurée dans le compte A.

#### Gestion indépendante

Si le compte B requiert un comportement alternatif ou équivalent similaire, un administrateur du compte B doit configurer manuellement les relations au sein de ce compte.

#### Implications

#### Aucune propagation automatique des relations

Les relations alternatives et équivalentes ne sont pas automatiquement disponibles dans les comptes de pairs via le partage de catalogue.

#### Configuration manuelle requise

Chaque compte de pairs est responsable de la définition et de la gestion de ses propres relations pour les objets d’apprentissage partagés.

#### Considérations de cohérence

Le comportement d’achèvement, la satisfaction des conditions préalables et le reporting peuvent différer d’un compte à l’autre, sauf si les relations sont alignées intentionnellement via une configuration manuelle.


### Comportement en aval

Une fois qu’une autre fin existe pour une formation cible, ALM l’utilise dans les vérifications en aval :

* Si la formation cible est un **prérequis** pour d’autres formations, l’élève devient éligible à ces formations comme s’il avait terminé la cible.
* Si la cible est un **cours obligatoire dans un parcours d’apprentissage**, la logique d’achèvement du parcours peut traiter l’élève comme ayant terminé cette partie et marquer le parcours comme terminé lorsque d’autres conditions sont remplies.
* Les tableaux de bord de conformité et autres, tels que Tableau de bord de réussite de groupe, qui dépendent du respect d’une exigence de formation peuvent inclure des élèves qui n’ont que d’autres achèvements.

Le système fait la distinction entre l&#39;achèvement réel et l&#39;achèvement alternatif de sorte que :

* Si l’élève suit directement la formation cible et la termine ultérieurement, cette achèvement direct peut remplacer le besoin de l’autre achèvement.
* Si la relation entre la source et la cible est supprimée ou modifiée, ALM peut supprimer ou ajuster les autres finalisations sans toucher aux finalisations authentiques, à condition que les finalisations rétroactives soient activées pour le compte.

Les autres achèvements sont conçus pour ne pas interférer avec l’activité réelle de l’élève sur la formation cible. Elles agissent comme une superposition qui peut être révisée si les relations changent.

## Modifications apportées au rapport Relevés de notes de l’apprentissage dans cette version

### Colonne Méthode d’achèvement

La colonne Méthode d’achèvement indique comment chaque enregistrement du relevé de notes de l’élève de l’administrateur a été terminé.

Valeurs :

* Direct (pour les fins de production directes)
* Variante (pour les réalisations obtenues via d&#39;autres relations)
* Remplacement révoqué (lorsque toutes les autres déclarations de production sont révoquées en raison d&#39;une inachèvement rétroactive et de la suppression de la relation)

>[!NOTE]
>
>Cette colonne n’est pas visible dans le LT de l’élève ; elle est uniquement disponible dans le LT de l’administrateur à des fins de reporting et de suivi.

#### Impact

Active des pistes d’audit claires, le suivi de la conformité et la transparence pour les administrateurs concernant la façon dont un cours a été terminé.

### Autre suivi de l’achèvement dans les relevés de notes des élèves

Les autres achèvements permettent aux élèves de recevoir un crédit d’achèvement pour un cours ou un parcours d’apprentissage cible lorsqu’ils ont terminé un cours ou un parcours source équivalent, en fonction des relations établies.

Dans le relevé de notes de l’élève, les autres achèvements ont un impact sur trois colonnes existantes : statut, date d’achèvement et source d’achèvement :

* **État** : l’état peut être Terminé même si l’élève n’a pas directement terminé le cours/parcours cible, en raison d’une autre achèvement. Les autres statuts (Non démarré, En cours, Non inscrit) ne sont pas affectés par les variantes. Seule la fonctionnalité Terminé est affectée par les alternatives.
* **Date d’achèvement** : la date d’achèvement d’une variante d’achèvement est héritée du cours/chemin source qui a déclenché la variante d’achèvement. Si l’élève termine directement la cible ultérieurement, la date est mise à jour pour refléter l’achèvement direct.
* **Source de l&#39;achèvement** : cette colonne capture les ID de formation du ou des cours ou parcours source qui ont fourni l&#39;autre achèvement. Si plusieurs sources sont actives, tous les ID pertinents sont répertoriés ; si les sources sont révoquées (avec l’option d’inachèvement rétroactif activée), seules les sources actives sont conservées. La colonne Source d’achèvement répertorie tous les ID de formation source actifs (séparés par des virgules). S’il existe plusieurs sources, la date d’achèvement la plus ancienne est utilisée.

#### Impact

Les autres achèvements réduisent le rapprochement manuel, automatisent le suivi de la progression dans les parcours d’apprentissage et les certifications, et prennent en charge les exigences de conformité.

>[!NOTE]
>
>Les relevés de notes des élèves n’affichent pas la colonne Méthode d’achèvement ; elle est uniquement disponible dans le LT administrateur.

### Logique de la date d&#39;achèvement pour les suppléants

La colonne Date d’achèvement du relevé de notes de l’élève est un champ existant utilisé pour enregistrer le moment où un élève termine un cours ou un parcours d’apprentissage, que ce soit par des moyens directs ou alternatifs. Pour les autres achèvements, la date d&#39;achèvement est héritée du cours ou du chemin source qui a déclenché l&#39;autre achèvement. Cela signifie que la date reflète la date à laquelle l’élève a terminé la source, et non la cible.

Si un élève termine ultérieurement le cours ou le parcours cible directement, la date d’achèvement est mise à jour à la date d’achèvement direct, en remplacement de la date d’achèvement secondaire précédente.

Aucune nouvelle colonne n&#39;est ajoutée pour les autres dates de fin. La colonne Date de fin existante est utilisée pour les fins de production directes et alternatives. Dans les cas où plusieurs origines peuvent fournir une autre date d&#39;achèvement pour une cible, la date d&#39;achèvement alternative la plus ancienne parmi les origines est utilisée. Si une origine est révoquée (avec l&#39;option d&#39;inachèvement rétroactif activée), la date d&#39;achèvement est mise à jour vers l&#39;origine active la plus récente suivante ou est effacée s&#39;il ne reste aucune origine active.

#### Impact

La logique de la date d&#39;achèvement garantit un suivi historique précis et la cohérence des rapports, en particulier lorsque les autres déclarations de production sont révoquées ou mises à jour.

### Autres déclarations de production révoquées

Les autres achèvements révoqués se produisent lorsqu’un autre achèvement d’un élève pour un cours ou un parcours d’apprentissage cible est supprimé en raison de la révocation de toutes les relations sources, à condition que l’inachèvement rétroactif soit activé dans le compte.

#### Conditions de déclenchement

* L&#39;inachèvement rétroactif doit être activé pour le compte. Sinon, la suppression des relations source ne révoque pas les autres achèvements.
* La révocation ne se produit que lorsque toutes les relations source actives d’une cible sont supprimées. S&#39;il reste au moins une source, l&#39;autre achèvement persiste et la colonne source d&#39;achèvement est mise à jour pour refléter uniquement les autres origines actives.

#### Impact

* Statut : si toutes les autres finalisations sont révoquées et qu&#39;il n&#39;y a pas d&#39;achèvement direct, le statut est mis à jour (par exemple, de Terminé à Non commencé ou En cours selon le cas).
* Date d’achèvement : la date d’achèvement est effacée s’il ne reste aucune source active et que l’élève n’a pas directement terminé la cible.
* Source d&#39;achèvement : La colonne Source d&#39;achèvement est mise à jour pour supprimer la ou les sources révoquées ; si toutes sont révoquées, elle est effacée.

Si l’élève a une fin directe, la révocation des remplacements n’affecte pas le statut terminé ou la date d’achèvement.

**Remarque** :

1. Si plusieurs origines ont fourni une autre fin de production et que seules certaines sont révoquées, le LT reflète les origines actives restantes et leur date d&#39;achèvement la plus ancienne.
2. Si toutes les sources sont révoquées et qu’il n’y a pas d’achèvement direct, l’élève perd l’état d’achèvement pour la cible.

### Rapport amélioré pour les remarques des réviseurs de listes de contrôle

Les commentaires des réviseurs des modules de liste de contrôle sont désormais inclus dans les relevés de notes des élèves (LT) sous une colonne renommée : **Remarques du réviseur** (auparavant Commentaire d&#39;envoi).

#### Impact

Les élèves et les administrateurs peuvent afficher les commentaires des réviseurs consolidés et clairement étiquetés dans les exportations LT (IU, API de tâche et connecteurs), ce qui améliore la transparence, l’auditabilité et prend en charge une évaluation et un coaching des performances plus précis.

#### Quels sont les changements apportés

**Colonnes renommées**

| Zone | Ancien nom de colonne | Nom de la nouvelle colonne | Annotations |
| --------------------------- | ------------------ | ------------------ | --------------------------------------------------------- |
| Relevés de notes des élèves (administrateur) | Commentaire de soumission | Remarques de l’évaluateur | S’applique à toutes les sources LT d’administration : interface utilisateur, API de tâche, connecteurs, le cas échéant. |

Cette modification s’applique uniformément à toutes les sources LT d’administration (exportations d’interface utilisateur, rapports d’API de tâche et exportations basées sur un connecteur, le cas échéant). LT exporté par connecteur affichera les remarques du réviseur dans une colonne dédiée à la fin (pour les connecteurs qui n’exposaient pas précédemment le commentaire de soumission), ce qui garantit que les intégrations en aval peuvent distinguer le retour du réviseur des autres commentaires.

>[!NOTE]
>
>Pour les relevés de notes des élèves, la colonne précédemment intitulée « Commentaire de soumission » est désormais renommée « Remarques du réviseur » et remplie avec le commentaire du réviseur de la liste de contrôle lorsqu’elle est activée.



### Amélioration du calcul du temps d’apprentissage

Le rapport LT utilise désormais une logique raffinée pour distinguer le temps actif et le temps inactif consacrés aux modules d’apprentissage, en fonction de l’activité de l’utilisateur et du focus de l’onglet.

#### Impact

Fournit une mesure plus précise des engagements d’apprentissage, prenant en charge la conformité et les analyses.