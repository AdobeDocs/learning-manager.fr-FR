---
jcr-language: en_us
title: Conformité de Learning Manager au RGPD
description: Conformité de Adobe Learning Manager au RGPD
contentowner: dvenkate
exl-id: 8ea31464-b4ce-49e8-b471-5630f0216aa4
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 39%

---

# Conformité de Learning Manager au RGPD

>[!IMPORTANT]
>
>Le contenu de ce document ne constitue pas un avis juridique et ne vise pas à remplacer un avis juridique. Consultez le service juridique de votre entreprise pour obtenir des conseils concernant le RGPD.

+++ Qu’est-ce que le RGPD ?

Le RGPD est un nouveau règlement de l’Union européenne qui entre en vigueur le 25 mai 2018. Il offre un contrôle strict de la confidentialité des données et permet aux utilisateurs finaux de prendre en charge leurs propres données personnelles.

+++

+++En quoi et pourquoi s’applique-t-il à vous en tant que client Adobe Learning Manager ?

Bien que le RGPD soit un règlement de l’UE, il s’applique aux entités commerciales du monde entier, qui collectent des informations personnelles pour tout utilisateur susceptible d’être résident de l’UE.  En tant que client Learning Manager, déterminez si le RGPD s’applique à votre organisation.

+++

+++Quel rôle joue Adobe dans ce domaine en tant que fournisseur de Learning Manager ?

Conformément au RGPD, si votre entreprise fournit un produit ou un service à des résidents de l&#39;UE et détermine comment et pourquoi collecter, suivre et surveiller leurs données, vous êtes considéré comme un [responsable du traitement des données](https://gdpr-info.eu/art-24-gdpr/). En tant que client Adobe Learning Manager, si vous effectuez l’une de ces activités, vous êtes considéré comme un responsable du traitement des données.

Les entreprises qui traitent des données pour le compte de contrôleurs sont considérées comme des [processeurs de données](https://gdpr-info.eu/art-28-gdpr/). En tant que fournisseur de LMS Adobe Learning Manager hébergé dans le cloud, Adobe joue le rôle d’un responsable du traitement des données. Voici quelques détails supplémentaires sur le [RGPD et votre entreprise](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++Comment Learning Manager vous permet-il de vous conformer au RGPD ?

Learning Manager a intégré les outils et processus suivants qui vous aideront à vous conformer au RGPD. Pour prendre en charge tous les processus qui vont au-delà du produit pour être entièrement conforme à la réglementation, vous devrez peut-être encore effectuer une évaluation avec votre équipe de conformité.

**Droit à l&#39;oubli : pour joindre le contrôleur de données :** le RGPD exige que les contrôleurs de données prennent en charge une fonctionnalité de droit à l&#39;oubli pour leurs utilisateurs. Cela signifie que tout utilisateur a le droit de demander au responsable du traitement de supprimer définitivement toutes les données personnelles stockées pour cet utilisateur. Si vous recevez une demande de ce type et estimez qu’elle est valide, cette fonctionnalité est désormais fournie par Learning Manager via sa fonctionnalité [Purger les utilisateurs](../administrators/feature-summary/purge-users.md). Cette fonctionnalité permet à l’administrateur d’initier une suppression permanente de toutes les données relatives à un individu spécifique, à la demande de l’individu, auquel cas Learning Manager supprimera instantanément les données de sa base de données et purgera automatiquement les journaux de sauvegarde (destinés à la restauration du système).

**Droit à l’oubli - Joindre le sous-traitant des données :** l’utilisateur final peut également contacter Adobe indépendamment pour la suppression de ses informations personnelles. Dans ce cas, Learning Manager détectera automatiquement les comptes propriétaires des informations personnelles de cet utilisateur et Adobe informera immédiatement l’administrateur de la demande. L’administrateur peut ensuite évaluer la validité de la demande et prendre un appel sur la demande via la fonctionnalité Purger les utilisateurs.

**Droit d&#39;accès :** le RGPD accorde à l&#39;utilisateur final le droit de demander des données qu&#39;un contrôleur peut avoir stockées pour cet utilisateur final. Pour prendre en charge cette demande, Learning Manager permet à l’administrateur de générer automatiquement le relevé de notes de l’élève, qui peut être partagé avec l’utilisateur.

**Confidentialité par conception, chiffrement des données :** nous traitons les données en transit et au repos à l&#39;aide des meilleures normes de chiffrement de sa catégorie pour garantir la sécurité des données. Les algorithmes de chiffrement utilisés sont SHA-256. Cela garantit que toutes les données que vous stockez sont correctement protégées afin de ne pas tomber entre de mauvaises mains.

+++
