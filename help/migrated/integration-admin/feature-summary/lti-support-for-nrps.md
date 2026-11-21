---
description: Découvrez comment Adobe Learning Manager utilise NRPS pour synchroniser des attributs d’élève personnalisés d’une plateforme LTI 1.3 dans les profils d’élève en tant que champs actifs
jcr-language: en_us
title: Prise en charge LTI pour NRPS
exl-id: 4c972319-b8ce-4f2d-9ccb-1b93c6cc6ac0
source-git-commit: 92be9eb8ece6d083efe595894a492540cd96eead
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%
---

# Prise en charge LTI pour NRPS

## Présentation

Adobe Learning Manager prend en charge la spécification NRPS (Names and Role Provisioning Services) lorsqu’il agit comme un outil LTI (Learning Tools Interoperability) 1.3. Lorsqu’un élève lance Learning Manager à partir d’un système de gestion de l’apprentissage externe (la plateforme), Learning Manager récupère l’enregistrement d’abonnement de l’élève à partir de la plateforme. Ensuite, il copie les attributs personnalisés de cet enregistrement, tels que l’ID du service ou de l’employé, dans le profil de l’élève en tant que champs actifs.

## Cas d’utilisation

* **Enrichir automatiquement les profils des élèves.** Importez des attributs tels que le service, l’ID d’employé ou des métadonnées personnalisées de votre plateforme dans Learning Manager sans saisie manuelle des données ni importations séparées.
* **Analysez d’où viennent vos élèves.** Capturez les attributs d’emplacement, tels que le pays et la ville, pour créer une image des zones géographiques d’où proviennent vos élèves. Utilisez les champs de profil résultants pour l’analyse dans Learning Manager.
* **Alignez les données de profil sur la plateforme source.** La plateforme reste la source de la vérité. Learning Manager actualise les valeurs à chaque démarrage d’un élève.
* **Prenez en charge plusieurs plateformes dans un seul compte.** Les préfixes d&#39;espace de noms séparent les attributs de différentes plates-formes, même si celles-ci utilisent le même nom d&#39;attribut.

Avec la synchronisation des champs personnalisés NRPS, Learning Manager effectue les opérations suivantes au lancement :

1. Détecte que la plateforme prend en charge NRPS.
2. Demande l’enregistrement d’abonnement de l’élève de lancement à partir de la plateforme.
3. Extrait les attributs personnalisés de cet enregistrement.
4. Écrit les attributs dans le profil de l’élève en tant que champs actifs. Chaque nom de champ porte un préfixe `<namespace>`, de sorte que les attributs de différentes plateformes ne soient pas en conflit.
5. Learning Manager réutilise le jeton d’informations d’identification du client OAuth 2.0 qu’il utilise déjà pour les services d’affectations et de grades (AGS). Vous n’avez pas besoin de configurer un nouveau point de terminaison de jeton.

>[!NOTE]
>
>NRPS est une spécification facultative dans LTI Advantage. La prise en charge du NRPS et des attributs personnalisés varie selon la plate-forme. Assurez-vous que votre plate-forme expose NRPS 2.0 avant d’envisager d’utiliser cette fonctionnalité.

## Fonctionnalités clés

* **Prise en charge des revendications NRPS :** Learning Manager vérifie chaque lancement de LTI 1.3 pour la revendication NRPS. Si la revendication est absente, le lancement se poursuit normalement sans erreur et sans impact sur l’élève.
  * Cette revendication fournit les informations suivantes :
    * **Point de terminaison d&#39;abonnement :** `context_memberships_url `identifie l&#39;URL de service pour le cours ou le contexte d&#39;apprentissage à partir duquel l&#39;élève a lancé ALM.
    * **Versions prises en charge :** `service_versions` répertorie les versions NRPS disponibles sur ce point de terminaison.
      Cette fonctionnalité prend en charge NRPS 2.0.
  * **Infrastructure de jetons partagés :** Learning Manager ajoute la portée NRPS à sa demande de jeton AGS existante et réutilise le cache de jeton par inscription existant.
* **Synchronisation des paramètres personnalisés avec les profils d’élève**
  * **Champs actifs préfixés par un espace de noms :** chaque attribut personnalisé est mappé à un champ actif nommé `<namespace>_<field_name>`.
  * **Création automatique de champ :** s&#39;il n&#39;existe aucun champ actif correspondant, Learning Manager en crée un avec le type **Texte** et l&#39;état **Actif**.
  * **Plateforme comme source de vérité :** Learning Manager remplace les valeurs de profil existantes par les dernières valeurs de la plateforme. Les élèves et les administrateurs ne peuvent pas modifier ces champs.
  * **Comportement non bloquant :** les erreurs NRPS n&#39;empêchent pas les élèves de lancer le contenu d&#39;apprentissage.
  * **Sources multiples pour les attributs personnalisés :** Learning Manager peut lire les attributs personnalisés à partir du point de terminaison NRPS et des paramètres personnalisés dans le jeton de lancement LTI. En savoir plus sur les [attributs personnalisés dans le jeton de lancement](#custom-attributes-in-the-launch-token).

## Configurations prises en charge

| Élément | Assistance |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| Rôle Learning Manager | Outil LTI 1.3 |
| Version LTI | LTI 1.3 |
| Version du service NRPS | 2.0 |
| Plates-formes (format de champ personnalisé conforme aux spécifications) | Moodle, D2L Brightspace, Blackboard (Anthologie), Sakai |
| Type de champ personnalisé | Texte |
| Déclencheur | Chaque lancement LTI 1.3 |

La prise en charge de la plate-forme dépend du modèle de sérialisation de champ personnalisé utilisé dans l&#39;enregistrement de membre NRPS. Plusieurs modèles peuvent coexister, mais Learning Manager ne traite que les modèles pris en charge dans la version active.

## Fonctionnement du logiciel

### Flux de lancement

1. Un élève lance Learning Manager à partir de la plateforme.
2. Learning Manager lit la revendication NRPS dans le jeton de lancement LTI 1.3. Si la revendication répertorie le service NRPS version 2.0, Learning Manager stocke l&#39;élément `context_memberships_url` pour la session et pour le contexte LTI (cours).
3. Learning Manager demande un jeton d&#39;accès qui inclut l&#39;étendue NRPS `https://purl.imsglobal.org/spec/lti-nrps/scope/contextmembership.readonly`.
4. Learning Manager appelle `context_memberships_url?rlid=<lti_user_id>` avec le jeton de support pour récupérer l’enregistrement de l’élève qui lance l’application. Si la plateforme ignore le filtre `rlid` et renvoie la liste complète, Learning Manager trouve l’élève avant le `user_id`.
5. Learning Manager extrait les champs personnalisés de l’enregistrement.
6. Learning Manager mappe chaque champ personnalisé à un champ actif et écrit les valeurs dans le profil de l’élève.
7. Sinon, ALM prend également en charge l&#39;extraction des paramètres personnalisés à synchroniser avec le profil de l&#39;élève pendant le lancement de l&#39;outil, si les paramètres personnalisés sont préfixés avec le champ identifiable ALM `ALMfield`.

### Format de champ personnalisé

La spécification NRPS 2.0 définit les données personnalisées comme un tableau `message` dans l&#39;enregistrement de membre. Learning Manager lit les données personnalisées de la revendication personnalisée LTI dans cette baie. Pour cette version, Learning Manager prend en charge la représentation S du motif conforme à la spécification.

```json
{
  "user_id": "abc123",
  "message": [
    {
      "https://purl.imsglobal.org/spec/lti/claim/custom": {
        "department": "Engineering",
        "employee_id": "E4567"
      }
    }
  ]
}
```

### Attributs personnalisés dans le jeton de lancement

Les plateformes peuvent également envoyer des attributs personnalisés en tant que paramètres personnalisés dans le jeton de lancement LTI. Learning Manager collecte les attributs à la fois du jeton de lancement et du point de terminaison NRPS et les stocke dans le profil de l’élève.

Pour les attributs du jeton de lancement, le nom du paramètre doit commencer par le préfixe `almfield-` requis par Learning Manager. Sans le préfixe, Learning Manager ne peut pas distinguer ces paramètres des autres paramètres personnalisés et ne les importe pas. Les attributs récupérés à partir du point de terminaison NRPS n&#39;ont pas besoin de ce préfixe. Ce préfixe n&#39;est requis que si des paramètres personnalisés sont importés dans le jeton de lancement pour ALM afin d&#39;identifier le champ qu&#39;il doit synchroniser avec les champs actifs de l&#39;élève.

>[!NOTE]
>
>Confirmez le préfixe exact requis auprès de votre représentant Learning Manager avant de configurer les paramètres personnalisés sur la plateforme.

### Nommage et mappage des champs actifs

Learning Manager crée le nom du champ actif en tant que `<namespace>_<field_name>`. Par exemple, le champ `department` dans l&#39;espace de noms `https://purl.imsglobal.org/spec/lti/claim/custom` devient `https://purl.imsglobal.org/spec/lti/claim/custom_department`.

Learning Manager applique les règles suivantes :

* **Longueur du nom :** si le nom dépasse la limite de caractères du nom de champ actif, Learning Manager raccourcit d&#39;abord la partie espace de noms et conserve le nom du champ.
* **Conflits de noms :** après le raccourcissement, Learning Manager recherche les conflits avec les champs actifs existants d’une autre source. En cas de conflit, il ajuste la longueur du raccourcissement jusqu’à ce qu’il trouve un nom unique. S’il ne trouve pas de nom unique, il ignore le champ et consigne une erreur.
* **Correspondance :** la correspondance des noms de champs n&#39;est pas sensible à la casse.
* **Champ existant et activé :** Learning Manager écrit la valeur dans le profil de l’élève.
* **Champ existant et désactivé :** Learning Manager ignore le champ sans enregistrer d&#39;erreur.
* **Aucun champ existant :** Learning Manager crée un champ **Texte** avec l’état **Actif**.

### Écriture de valeurs dans le profil

* À chaque lancement où Learning Manager récupère les données NRPS, il écrit toutes les valeurs de champ personnalisé résolues dans le profil de l’élève qui lance le programme. Aucun autre profil d’élève n’est modifié.
* Si un champ a déjà une valeur, Learning Manager l’écrase avec la dernière valeur de la plateforme.
* Si la valeur de la plate-forme est vide ou nulle, Learning Manager conserve la valeur de profil existante.
* L’échec de l’écriture d’un champ ne bloque pas le lancement ni les écritures des autres champs.
* Learning Manager applique les mises à jour de champ dans la même transaction de lancement, si possible.
* Les élèves ne peuvent pas modifier les champs NRPS sur leur page de profil, et les administrateurs ne peuvent pas modifier ces valeurs au nom d’un élève.

## Configuration de la synchronisation des champs personnalisés NRPS

### Conditions préalables

* Votre plateforme est enregistrée auprès de Learning Manager en tant qu’outil LTI 1.3. Cette fonctionnalité ne prend pas en charge LTI 1.1 ou LTI 1.2.
* Votre plate-forme prend en charge le service NRPS version 2.0 et expose des attributs personnalisés au format `message` conforme aux spécifications.
* Le jeton de lancement LTI contient la revendication `namesroleservice`.
* La revendication fournit `context_memberships_url`, qui identifie le point de terminaison NRPS spécifique au cours.
* La valeur `service_versions` de la revendication inclut `2.0`.
* Vous disposez d’un accès administrateur à l’enregistrement des outils de la plateforme.

### Octroyer la portée NRPS à Learning Manager

Les nouveaux enregistrements qui incluent la portée NRPS ne nécessitent aucune configuration supplémentaire dans Learning Manager.

Les nouvelles inscriptions qui incluent la portée NRPS fonctionnent sans modifications supplémentaires dans Learning Manager. Pour une inscription existante, l’administrateur de la plate-forme doit mettre à jour l’inscription de l’outil côté plate-forme.

>[!NOTE]
>
>Vous n’avez pas besoin de modifier le point de terminaison du jeton, l’ID client ou la clé privée dans Learning Manager. La configuration AGS existante est réutilisée. Si la plate-forme n’accorde pas la portée NRPS, Learning Manager l’ignore sans affecter AGS ou le lancement.

### Exposer les attributs de l’élève sur la plateforme

La plateforme contrôle les attributs d’élève qu’elle partage. Les étapes exactes dépendent de la plate-forme. Par exemple, dans Moodle :

1. Ajoutez Learning Manager en tant qu’outil externe à l’aide de LTI 1.3.
2. Activez les paramètres de confidentialité qui permettent à la plateforme de partager les informations des élèves avec l’outil.
3. Définissez les attributs personnalisés que vous souhaitez envoyer. Vous pouvez utiliser des variables de plate-forme ou des valeurs prédéfinies.
4. Si vous envoyez également des attributs en tant que paramètres personnalisés dans le jeton de lancement, ajoutez le préfixe requis par Learning Manager à chaque nom de paramètre.

>[!NOTE]
>
>Exposez uniquement les attributs requis pour le cas d’utilisation de formation. Learning Manager traite la plate-forme comme une source de vérité et n’offre pas de consentement distinct ni de contrôles de confidentialité dans cette version.

### Vérification de la synchronisation

1. Lancez Learning Manager à partir de la plateforme en tant qu’élève de test.
2. Vérifiez que le lancement se termine normalement.
3. Dans l’application d’administration Learning Manager, ouvrez la page des champs actifs.
4. Confirmez que les champs apparaissent avec le préfixe d&#39;espace de noms, avec le type **Texte** et l&#39;état **Actif**.
5. Ouvrez le profil de l’élève participant au test et confirmez que les valeurs correspondent à la plateforme.
6. Confirmez que les champs sources NRPS sont en lecture seule. Ni l’élève ni un administrateur ne peuvent modifier manuellement les valeurs synchronisées.
7. Relancez l’application après avoir modifié une valeur source non vide et vérifiez que Learning Manager remplace la valeur de profil existante par la dernière valeur NRPS.

>[!TIP]
>
>Si un champ existe mais est désactivé, Learning Manager n’y écrit pas. Activez le champ si vous souhaitez qu’il soit renseigné.

## Gestion des erreurs et journalisation

Learning Manager ne bloque jamais un élève en raison d’un problème NRPS. Il ne réessaie pas. Il consigne l’échec et ignore la synchronisation NRPS pour ce lancement. Le prochain lancement tente à nouveau.

| Condition | Résultat |
|------------------------------------------------------------------|-------------------------------------------------------|
| La revendication NRPS est absente du jeton de lancement | NRPS est ignoré. Le lancement se poursuit. |
| Seul le service NRPS version 1.0 est présent | NRPS est ignoré. Le lancement se poursuit. |
| La demande de jeton échoue ou la plateforme n’accorde pas la portée NRPS | NRPS est ignoré. AGS et le lancement ne sont pas affectés. |
| Échec de l’appel NRPS (temporisation, 4xx ou 5xx) | L’erreur est consignée. Le lancement se poursuit. |
| L’élève n’est pas trouvé dans la réponse NRPS | La synchronisation des champs est ignorée. Le lancement se poursuit. |
| Aucun champ personnalisé dans la réponse NRPS | La synchronisation des champs est ignorée sans erreur. |
| Impossible de résoudre un conflit de nom de champ | Le champ est ignoré et une erreur est consignée. |
| Échec de l’écriture d’un seul champ | D&#39;autres champs sont encore écrits. Le lancement se poursuit. |

Chaque entrée de journal inclut l’horodatage, l’ID d’inscription de la plateforme, l’ID de l’élève et le motif de l’échec. Les administrateurs système de Learning Manager peuvent accéder aux journaux.

## Notes

* Seul l’enregistrement de l’élève qui lance est synchronisé. Learning Manager ne synchronise pas la liste complète des cours.
* Seul le service NRPS version 2.0 est pris en charge.
* Tous les champs synchronisés sont de type **Texte**. Learning Manager ne déduit pas les types des valeurs. Les types de champ de numéro, de date et de Booléen ne sont pas pris en charge.
* Learning Manager fait office d’outil LTI. Il n’agit pas comme une plateforme NRPS et ne fournit pas de point de terminaison de liste à d’autres outils.
* La synchronisation des champs personnalisés se produit lors du lancement LTI.
