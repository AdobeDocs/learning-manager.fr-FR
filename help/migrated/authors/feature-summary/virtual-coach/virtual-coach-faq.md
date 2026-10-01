---
description: Trouvez des réponses aux questions courantes sur la création, l’octroi de licences, la sécurité, la confidentialité des données, le score et l’expérience de l’élève pour Virtual Coach
jcr-language: en_us
title: FAQ sur Virtual Coach
exl-id: b8955b04-4655-413a-b570-a05b1f76285c
source-git-commit: 449f25df93867bf4d5ec11af057f8da7c405a09f
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 0%
---

# FAQ sur Virtual Coach

## Création

Obtenez des réponses aux questions courantes sur la création, la configuration et le dépannage d&#39;un jeu de rôle Virtual Coach.

1. **Pourquoi mon jeu de rôle a-t-il obtenu un score nul alors que j’ai couvert la plupart des sujets ?**
Vérifiez si l&#39;une de vos rubriques a l&#39;option **Créer ou interrompre** activée. Si un élève n’aborde pas du tout un sujet « Make or Break » au cours de la conversation, le score final de la simulation est de 0, indépendamment de ses performances sur tout le reste. Réservez le Make or Break à un ou deux sujets véritablement non négociables pour éviter que cela ne se produise dans un délai raisonnable. Pour la configuration complète, voir [Créer et publier un jeu de rôle Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

2. **Combien de personnages un jeu de rôle à plusieurs personnages peut-il inclure ?**
Jusqu&#39;à quatre personnalités dans un seul scénario, chacune configurée individuellement avec ses propres **rôle**, **personnalité** et **préoccupations personnelles**. Utilisez cette option lorsqu’un élève doit faire défiler plusieurs parties prenantes dans la même conversation, comme une présentation au comité d’achat ou une révision par un comité de direction.

3. **Comment choisir entre la voix, le chat et la vidéo pour un jeu de rôle ?**
Cela dépend du type de personnage que vous sélectionnez. **Les personnages système** prennent en charge **la voix et la vidéo** (un avatar animé avec une voix parlée) ou **la voix** uniquement. Les **personnages personnalisés** prennent en charge l&#39;interaction vocale et vous pouvez activer l&#39;**avatar vidéo** séparément pour les personnages qui prennent en charge le mode vocal et vidéo. Choisissez Voix et vidéo pour la simulation la plus réaliste, ou Voix uniquement pour les scénarios dans lesquels un avatar visuel n’est pas nécessaire, comme une formation par téléphone.

4. **Comment rédiger une bonne invite pour l’assistant de co-création d’IA ?**
Saisissez une brève description qui décrit le scénario, par exemple `Handling price objections in enterprise sales` ou `Pitching our new product to a buying committee`. L&#39;assistant AI pose ensuite des questions de suivi pour vous aider à créer la présentation, le personnage IA et les rubriques d&#39;évaluation. Fournissez autant de contexte que possible sur la situation, le rôle et les préoccupations de la personne, et la façon dont vous souhaitez mesurer le succès. Plus de détails dans votre description initiale signifie moins de va-et-vient dans le chat. Voir [Rassembler des matériaux pour un jeu de rôle d&#39;entraîneur virtuel](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) pour un modèle d&#39;invite plus complet.

5. **Puis-je modifier un jeu de rôle après sa publication ?**
Oui. Les modifications apportées aux paramètres des personas, aux rubriques et à d’autres configurations prennent effet immédiatement pour tout jeu de rôle non publié. Si un jeu de rôles est déjà publié et attribué aux élèves, republiez-le après avoir apporté des modifications afin que les élèves puissent voir la dernière version.

Pour des questions générales sur les produits, les licences et l’administration, consultez la [FAQ sur Adobe Learning Manager Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/virtual-coach-faq.md).

## Formation et conformité

1. **Comment Virtual Coach protège-t-il les données des clients et des élèves ?**
Les données client sont stockées à l’aide du chiffrement AES-256, sécurisées en transit à l’aide de TLS 1.3+ et logiquement séparées par des identifiants client uniques pour assurer l’isolement entre les environnements client. Ces contrôles sont validés par des tests annuels de pénétration réalisés par des tiers.

2. **Où sont stockées et traitées les données de Virtual Coach ?**
Les données client sont stockées dans les centres de données de l’UE, conformément aux exigences européennes en matière de confidentialité.

3. **Combien de temps Virtual Coach conserve-t-il les données des clients et des élèves, et peut-il être supprimé ?**
Les données de session peuvent être conservées pendant la durée du contrat de service et les clients peuvent configurer des politiques de conservation spécifiques à l’entreprise. Les utilisateurs individuels peuvent supprimer leurs propres enregistrements, les administrateurs peuvent effectuer des suppressions en bloc et les données peuvent être exportées avant la suppression. Les mécanismes de suppression automatique et la journalisation des audits sont également pris en charge.

4. **Le contenu chargé par le client est-il utilisé à d’autres fins que la génération du jeu de rôle, telles que la formation à l’IA ou l’amélioration du produit ?**
Non, les données client ne sont pas utilisées pour la formation à l’IA.

5. **Comment Virtual Coach utilise-t-il l’IA et quelles garanties sont en place pour les réponses générées par l’IA ?**
Virtual Coach utilise l’IA générative pour créer des expériences de jeu de rôle interactives. Plusieurs garanties sont en place, notamment des filtres de contenu Azure OpenAI pour des catégories telles que la violence, les discours de haine, le contenu sexuel et l’automutilation, des garde-fous au niveau des invites et des contrôles contextuels qui maintiennent l’IA axée sur l’apprentissage et le développement des cas d’utilisation. Des tests de sécurité de l&#39;IA sont également effectués et des mesures de protection telles que la transformation rapide basée sur la sécurité et le comportement de clarification puis de refus sont utilisées pour les demandes sensibles. En outre, les engagements contractuels exigent la divulgation des extrants générés par l&#39;IA et le respect des réglementations applicables en matière d&#39;IA.

6. **Quelles sont les normes de confidentialité et de conformité prises en charge par Virtual Coach ?**
Virtual Coach prend en charge les protections de confidentialité liées au RGPD, les contrôles de rétention configurables, la journalisation d’audit, les fonctionnalités de suppression des utilisateurs et l’hébergement de données basé en UE. L’accord contractuel exige également le respect des lois et réglementations applicables, notamment la loi sur l’IA dans l’Union européenne et la loi californienne sur la transparence de l’IA (SB-942).

7. **À qui appartient le contenu chargé sur Virtual Coach et le contenu généré pendant une session ?**
Le client est propriétaire du contenu chargé sur Virtual Coach et du contenu généré au cours d’une session.

8. **Où se trouvent les données de Virtual Coach, dans Adobe Learning Manager ou avec le fournisseur de services Virtual Coach ?**
Les données de jeu de rôle sont stockées dans l&#39;infrastructure cloud du fournisseur de services Virtual Coach et hébergées dans les centres de données de l&#39;UE.

## Produit

1. **Comment Virtual Coach est-il activé pour un client Adobe Learning Manager existant ?**
Voir [Activation De Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md#activatevirtualcoach)

2. **Combien de temps l&#39;activation du Virtual Coach est-elle valide et comment est-elle renouvelée ?**
L’activation du Virtual Coach dans Adobe Learning Manager est valide pour la durée de votre contrat d’abonnement au module complémentaire. Il n&#39;est pas automatiquement perpétuel. Au lieu de cela, la validité s’aligne sur votre période d’abonnement.

   **Renouvellement :** pour continuer à utiliser Virtual Coach après la fin de la période de votre contrat, vous devez renouveler votre abonnement. Au moment de l’achat, Adobe fournit une clé d’activation, que l’administrateur de compte utilise pour activer Virtual Coach dans la section Facturation. Si vous renouvelez votre contrat, vous recevrez des instructions et une nouvelle clé d’activation si nécessaire pour conserver un accès ininterrompu.

   Des crédits d’utilisateur actif mensuels (MAU) sont également alloués pour chaque période contractuelle. Tous les crédits non utilisés à la fin du contrat deviennent caducs. Ils ne sont pas reportés dans une nouvelle période. Votre activation dure aussi longtemps que votre abonnement Virtual Coach payant est actif et est renouvelé en prolongeant votre abonnement, comme géré via votre compte d’Adobe.

3. **Qu’advient-il des documents sources chargés et des données de session générées après la création ou la fin d’un jeu de rôle ?**
Les documents sources chargés peuvent être utilisés pour créer et configurer des scénarios de jeu de rôle, des personas et des critères d’évaluation. Une fois que les élèves ont terminé un jeu de rôle, Virtual Coach génère des résultats d’évaluation, des scores, des commentaires de coaching et des informations d’achèvement pour soutenir les activités d’apprentissage et de création de rapports. Les données associées aux jeux de rôles restent disponibles en fonction du cycle de vie du contenu et des règles de rétention applicables.

4. **Les élèves peuvent-ils réessayer un jeu de rôle ?**
Oui. Les élèves peuvent répéter une session de jeux de rôles plusieurs fois pour mettre en pratique leurs compétences, appliquer le retour d&#39;informations du coaching et améliorer leurs performances. Après avoir terminé un jeu de rôle, les élèves peuvent examiner leurs commentaires et tenter à nouveau de développer leurs compétences.

## Généralités

1. **Qu&#39;est-ce que Virtual Coach ?**
Virtual Coach est une fonction de coaching et de jeu de rôle basée sur l’IA intégrée à Adobe Learning Manager. Il permet aux élèves de s&#39;entraîner à avoir des conversations en situation réelle avec un personnage d&#39;IA qui répond intelligemment en temps réel, puis de recevoir un rapport de performance instantané couvrant ce qu&#39;ils ont dit et comment ils l&#39;ont dit. Pour une explication complète, voir [Qu&#39;est-ce que Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md) ?

2. **Qui utilise Virtual Coach ?**
Les organisations utilisent Virtual Coach pour former les représentants commerciaux, les équipes de service client, les agents de centre d’appels, les responsables et les dirigeants, les nouvelles recrues, les partenaires et les employés à l’apprentissage de nouveaux produits ou processus. Virtual Coach est disponible pour tous les élèves, auteurs et administrateurs d’un compte Adobe Learning Manager dans lequel il a été activé. Les élèves accèdent aux sessions de jeux de rôles et les terminent, les auteurs créent et publient des scénarios de jeux de rôles, et les administrateurs gèrent les crédits et affichent des rapports.

3. **Virtual Coach utilise-t-il automatiquement mon contenu Adobe Learning Manager existant ?**
Non. Les auteurs doivent fournir des matériaux de référence, tels que des playbooks, des platines de vente, des transcriptions et des grilles de notation, ou une invite écrite, pour chaque jeu de rôle qu&#39;ils créent. Virtual Coach utilise ces matériaux chargés et ces définitions de personnages pour diriger la conversation ; il ne s’appuie pas automatiquement sur le contenu déjà présent dans votre bibliothèque de contenu ou dans vos cours. Voir [Rassembler des matériaux pour un jeu de rôle d&#39;entraîneur virtuel](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) pour savoir quoi préparer.

4. **Quels types de jeux de rôle sont disponibles ?**
Virtual Coach prend en charge trois domaines : l’activation des ventes, le développement du leadership et l’évaluation des compétences. Les auteurs font leur choix parmi des modèles préconfigurés couvrant des scénarios tels que les appels de découverte B2B, les appels à froid, la gestion des objections, le retour d’informations difficile et la désescalade des plaintes des clients. Les auteurs peuvent également créer des scénarios personnalisés à partir de zéro à l’aide de l’assistant AI. Voir [Créer et publier un jeu de rôle d&#39;entraîneur virtuel](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

5. **Quelles langues Virtual Coach prend-il en charge ?**
Virtual Coach est disponible en neuf langues pour l’interface et le contenu de simulation : allemand (Allemagne), espagnol (LATAM), espagnol (Espagne), français (France), italien (Italie), portugais (Portugal), portugais (Brésil), néerlandais (Pays-Bas) et anglais.

6. **Comment Virtual Coach est-il facturé et sous licence ?**
Virtual Coach est disponible sous forme d’abonnement complémentaire à Adobe Learning Manager. L’utilisation est mesurée en utilisateurs actifs mensuels (MAU). Un crédit MAU est consommé lorsqu’un élève lance un cours au cours d’un mois civil ; les sessions supplémentaires du même élève ce mois-là ne consomment pas de crédits supplémentaires. Les crédits non utilisés à la fin du contrat annuel deviennent caducs. Voir [Gérer l&#39;utilisation et la facturation du Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md).

7. **Comment le score d’un élève est-il calculé ?**
Chaque session génère un score de connaissances et un score de style. Le score de connaissances indique si l’élève a traité les sujets requis et fourni des informations précises. Le score de style reflète la manière dont l’élève a communiqué, notamment le rythme, la clarté, les mots de remplissage, la force de la phrase et l’énergie vocale. Les auteurs définissent le poids de chaque composant lors de la configuration du scénario ; une configuration commune est 70 % de connaissances et 30 % de style. Voir [Comprendre votre rapport de performances Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/understand-virtual-coach-performance-report.md).

8. **Les élèves peuvent-ils télécharger leur rapport de performances ?**
Oui. En plus de l’affichage du rapport à l’écran, les élèves peuvent le télécharger en tant que PDF à conserver pour leurs propres enregistrements ou à partager avec un responsable.

9. **Un élève peut-il réessayer un jeu de rôle ?**
Oui. Les élèves peuvent tenter un jeu de rôle autant de fois qu&#39;ils le souhaitent. Chaque tentative correspond à une nouvelle session indépendante et génère un nouveau rapport de performances. Seule la première session d’un mois civil consomme un crédit MAU.

10. **Les élèves peuvent-ils soumettre leurs sessions pour révision humaine ?**
Non.

11. **Virtual Coach est-il disponible sur mobile ?**
Virtual Coach est pris en charge par les API et sur le web mobile et sur ordinateur Adobe Learning Manager. Elle n’est pas disponible dans l’application mobile Adobe Learning Manager (iOS/Android) de la version actuelle.

12. **Les données de l’élève sont-elles utilisées pour former l’IA ?**
Non. Virtual Coach est hébergé sur une infrastructure conforme au RGPD, et aucune donnée d’élève personnelle n’est utilisée pour former les modèles d’IA.

13. **Quelle est la différence entre une assistance à la tâche et un module de cours pour Virtual Coach ?**
Une assistance à la tâche est une ressource autonome à la demande à laquelle les élèves peuvent accéder directement à partir du catalogue à tout moment sans être inscrits à un cours. Un module de cours est accessible dans le cadre d&#39;une séquence de cours structurée avec inscription, suivi de l&#39;achèvement et évaluation formelle. Le même jeu de rôle peut être publié en tant qu’outil de travail et ajouté à plusieurs cours simultanément. Voir [ajouter un jeu de rôle d&#39;entraîneur virtuel à un cours](/help/migrated/authors/feature-summary/virtual-coach/add-virtual-coach-role-play-to-course.md).

14. **Comment devrions-nous packager Virtual Coach lors du déploiement d’un nouveau processus ou produit ?**
Incluez dans un package le jeu de rôles au sein d&#39;un cours ou d&#39;un parcours d&#39;apprentissage avec le contenu de formation associé, et diffusez le lien du cours par e-mail ou d&#39;autres communications de gestion du changement. Virtual Coach est le lieu idéal pour la formation sur le dernier kilomètre : le point de contrôle une fois que les élèves ont terminé le contenu associé, où ils peuvent démontrer qu’ils peuvent l’appliquer, plutôt que comme une activité autonome.

15. **Virtual Coach est-il pris en charge sur les implémentations sans en-tête ou API ?**
Les API publiques de récupération des cours et des assistances à la tâche récupèrent également les cours Virtual Coach et les assistances à la tâche. Le filtre `jobAidType` est disponible pour récupérer les assistances à la tâche Virtual Coach spécifiquement. Le contenu Virtual Coach est pris en charge dans le lecteur sans en-tête, et les cours et assistances à la tâche contenant Virtual Coach fonctionnent dans le lecteur Fluidic.

Pour toute question sur la création et la configuration d’un jeu de rôle, consultez cette page FAQ.
