---
jcr-language: en_us
title: Credly
description: Découvrez l’intégration de Credly à ALM pour gérer et partager des badges externes à partir de la plateforme sur divers canaux de médias sociaux.
contentowner: chandrum
exl-id: 168f7ff8-51f5-4962-bf76-af909fc5565b
source-git-commit: f3a0ec693e1a2e75cdad24f91f22a0290d62740d
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Credly

[Credly](https://info.credly.com/) est une plateforme d’identification numérique qui permet aux élèves et aux organisations d’obtenir, de partager et de vérifier des réalisations professionnelles, telles que des badges ou des certifications. Les élèves peuvent gérer et partager des badges via leur profil Credly sur les réseaux sociaux et d’autres endroits.

## Prérequis

Configurez un compte Creative Cloud pour votre organisation. Ajoutez des élèves à Credly à l’aide de leurs ID de messagerie dans Adobe Learning Manager. Cela permettra aux élèves de voir les badges sur Credly et Adobe Learning Manager.

## Ajout du Credly Connector à Adobe Learning Manager

Procédez comme suit pour ajouter le connecteur Credly à Adobe Learning Manager :

1. Connectez-vous en tant qu&#39;**[!UICONTROL administrateur d&#39;intégration]**.
2. Sélectionnez **[!UICONTROL Credly]** > **Connect** pour ajouter le connecteur **[!UICONTROL Credly]** à Adobe Learning Manager.

   ![](assets/connector-credly.png)
   _Ajouter un connecteur Credly_

3. Tapez le **[!UICONTROL nom de la connexion]**.
4. Tapez l&#39;**[!UICONTROL ID d&#39;organisation]** et le **[!UICONTROL jeton d&#39;autorisation]**.

   >[!NOTE]
   >
   >Chaque badge de Credy est fourni avec un ID d’organisation et un jeton d’autorisation. Copiez ces valeurs de Credly.

5. Saisissez **[!UICONTROL Nom d&#39;hôte]** et sélectionnez **[!UICONTROL Se connecter]**.

## Migrer des badges depuis Credly

Le fichier badge.csv de Adobe Learning Manager vous permet de migrer des badges à partir du LMS ou de systèmes externes existants. Le fichier badge.csv a été mis à jour avec deux nouvelles colonnes :

* externalBadgeId
* externalBadgeProvider

L’ID de badge externe fait référence à l’ID de modèle de badge dans la plateforme Credly, et le fournisseur de badge externe est Credly. Ajoutez ces valeurs dans badge.csv et suivez les étapes mentionnées dans le [manuel de migration](https://experienceleague.adobe.com/fr/docs/learning-manager/using/integration/migration-manual#migrationprocedure) pour migrer le fichier csv.

## Créer une compétence - Administrateur

Une fois le badge importé dans Adobe Learning Manager, l’administrateur peut le créer en tant que compétence. Pour savoir comment créer une compétence, voir [Créer et modifier des compétences](https://experienceleague.adobe.com/fr/docs/learning-manager/using/admin/skills-levels).

### Attribuer la compétence/le badge à l’objet d’apprentissage - Auteur

L’auteur/l’administrateur peut affecter ces badges ALM importés avec Credly à un cours, un parcours d’apprentissage ou une certification (pas seulement des compétences). Sur la consommation de ces objets d’apprentissage, le badge sera obtenu et peut être consulté sur Credly et l’application ALM.

Les élèves peuvent se connecter à Credly et voir les badges dans la plateforme Credly. Depuis Credly, ils peuvent partager les badges sur des plateformes externes comme LinkedIn et d’autres réseaux sociaux.
