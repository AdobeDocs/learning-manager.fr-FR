---
jcr-language: en_us
title: Prise en charge du domaine personnalisé
description: Les domaines personnalisés ne sont pas pris en charge dans une instance Azure de Learning Manager.
contentowner: saghosh
source-git-commit: 8635072782253cbac3f913953797cae7c0bc5ef4
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---



# Prise en charge du domaine personnalisé

Les domaines personnalisés ne sont pas pris en charge dans une instance Azure de Learning Manager.

## Présentation {#overview}

La prise en charge du domaine personnalisé permet aux clients d’avoir un contrôle total sur le nom de domaine qu’ils peuvent utiliser pour leur compte dans Learning Manager. Un client doit acheter le domaine personnalisé séparément et travailler avec l’équipe d’Adobe pour le configurer comme URL de connexion pour sa plateforme d’apprentissage.

Cela permet au client de valider la connexion et l’expérience d’accès, de sorte que les utilisateurs ne constatent aucune présence d’Adobe ou d’Adobe Learning Manager.

Par exemple, vous souhaitez personnaliser votre domaine afin que vos utilisateurs bénéficient de la même expérience que s’ils se trouvaient dans le domaine Adobe. Si ABC Inc veut former ses clients, elle aimerait qu&#39;ils atterrissent sur un domaine appelé `abc.com/mylearning`, au lieu de `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>Comme condition préalable, vous devez enregistrer le domaine, puis l’Adobe vous guidera dans la personnalisation de l’url.


La fonctionnalité de domaine personnalisé est disponible moyennant des frais supplémentaires. Pour plus d’informations, contactez votre gestionnaire de succès client.

* Pour le rôle d’élève, le domaine commence par `https://cdn.<customer_custom_domain>/` Par exemple, `https://cdn.elearningstage1.cpdomaintest.in/`
* Pour tous les autres rôles, le domaine commence par `https://<customer_custom_domain>/`. Par exemple, `https://elearningstage1.cpdomaintest.in/`

`<customer_custom_domain>` est la partie personnalisable.

## Configuration d’un domaine personnalisé sur un compte {#howtosetupacustomdomainonanaccount}

Comme condition préalable, un client doit posséder un nom de domaine et acheter le domaine auprès d’un fournisseur.

Par exemple, considérons qu&#39;un client possède un domaine fictif, **acme.com**. Le client souhaite que le contenu Learning Manager soit servi à partir de **learning.acme.com**.

Suivez les étapes ci-dessous pour configurer un domaine personnalisé.

1. Le client doit **ajouter trois CNAME** enregistrements dans le domaine :

   * **learning.acme.com :** Point de terminaison public ALB de Learning Manager partagé par Adobe
   * **lrs.learning.acme.com :** Point de terminaison public ALB pointé par learning.acme.com
   * **cdn.learning.acme.com :** Point de terminaison CDN partagé par Adobe

1. Le client doit fournir des certificats SSL pour ces domaines :

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe téléchargera ces certificats SSL vers AWS ALB pour répondre aux demandes sur les domaines.
1. L’Adobe ajoutera learning.acme.com dans son certificat SAN.
1. Adobe génère les métadonnées du SP pour le client, car les métadonnées contiennent les URL de domaine personnalisées.

   * Si le client souhaite avoir une connexion via un réseau social, l’Adobe doit inclure les modèles d’URL de redirection des sites de réseaux sociaux dans la liste des URL autorisées.
   * Si le client a activé l’authentification unique, il doit travailler avec son FI pour inclure ses domaines dans les URL de redirection. Le client doit partager le XML des métadonnées IDP avec Adobe. L’Adobe doit ensuite mettre à jour les paramètres d’authentification unique du compte du client.

1. L’Adobe modifiera ensuite les règles S3 CORS pour inclure le domaine du client.
