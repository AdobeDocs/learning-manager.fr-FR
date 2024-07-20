---
jcr-language: en_us
title: Prise en charge du domaine personnalisé
description: Les domaines personnalisés ne sont pas pris en charge dans une instance Azure de Learning Manager.
contentowner: saghosh
exl-id: 162ce268-48e3-4c7e-acb1-5181cebbb18d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 67%

---

# Prise en charge du domaine personnalisé

Les domaines personnalisés ne sont pas pris en charge dans une instance Azure de Learning Manager.

## Vue d’ensemble {#overview}

La prise en charge du domaine personnalisé permet aux clients d’avoir un contrôle total sur le nom de domaine qu’ils peuvent utiliser pour leur compte dans Learning Manager. Un client doit acheter le domaine personnalisé séparément et collaborer avec l’équipe Adobe pour le configurer comme URL de connexion pour sa plate-forme d’apprentissage.

Cela permet au client de valider la connexion et l’expérience d’accès, de sorte que les utilisateurs ne constatent aucune présence d’Adobe ou d’Adobe Learning Manager.

Par exemple, vous souhaitez personnaliser votre domaine afin que vos utilisateurs bénéficient de la même expérience que s’ils se trouvaient dans le domaine Adobe. Si ABC Inc souhaite former ses clients, elle souhaite qu’ils accèdent à un domaine appelé `abc.com/mylearning`, au lieu de `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>Comme condition préalable, vous devez enregistrer le domaine, puis l’Adobe vous guidera dans la personnalisation de l’url.


La fonctionnalité de domaine personnalisé est disponible moyennant des frais supplémentaires. Pour plus d’informations, contactez votre gestionnaire de succès client.

* Pour le rôle d’élève, le domaine commencera par `https://cdn.<customer_custom_domain>/`. Par exemple, `https://cdn.elearningstage1.cpdomaintest.in/`
* Pour tous les autres rôles, le domaine commencera par `https://<customer_custom_domain>/`. Par exemple, `https://elearningstage1.cpdomaintest.in/`

`<customer_custom_domain>` est la partie personnalisable.

## Comment configurer un domaine personnalisé sur un compte {#howtosetupacustomdomainonanaccount}

Comme condition préalable, un client doit posséder un nom de domaine et acheter le domaine auprès d’un fournisseur.

Par exemple, imaginons qu’un client possède un domaine fictif, **acme.com**. Le client souhaite que le contenu Learning Manager soit distribué à partir de **learning.acme.com**.

Suivez les étapes ci-dessous pour configurer un domaine personnalisé.

1. Le client doit **ajouter trois enregistrements CNAME** dans le domaine :

   * **learning.acme.com:** point de terminaison public ALB de Learning Manager partagé par l&#39;Adobe
   * **lrs.learning.acme.com:** point de terminaison public ALB pointé par learning.acme.com
   * **cdn.learning.acme.com:** point de terminaison CDN partagé par Adobe

1. Le client doit fournir des certificats SSL pour ces domaines :

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe téléchargera ces certificats SSL vers AWS ALB afin de transmettre les demandes aux domaines.
1. Adobe ajoutera learning.acme.com dans son certificat SAN.
1. Adobe générera les métadonnées SP pour le client, car ces métadonnées contiendront les URL des domaines personnalisées.

   * Si le client souhaite disposer d’un compte de réseau social, Adobe doit inclure les modèles d’URL de redirection des sites de réseaux sociaux dans la liste des URL autorisées.
   * Si le client a activé l’authentification unique (SSO), le client doit contacter son fournisseur d’identités pour inclure ses domaines dans les URL de redirection. Le client doit transmettre le fichier XML des métadonnées du fournisseur à Adobe. Adobe doit alors mettre à jour les paramètres d’authentification unique du compte du client.

1. Adobe modifiera ensuite les règles S3 CORS afin d&#39;inclure le domaine du client.
