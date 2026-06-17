---
jcr-language: en_us
title: Application de groupes par et d’agrégations dans Report Builder
description: Synthétiser les données de l’état Adobe Learning Manager selon un champ choisi et calculer les nombres, les totaux et les pourcentages sur les lignes groupées.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---


# Application de groupes par et d’agrégations dans Report Builder

Regrouper par et agréger vous permet de produire des rapports récapitulatifs, tels que le nombre total d&#39;achèvements par instructeur, le nombre d&#39;inscriptions par catalogue ou le pourcentage de conformité par région.

## Quand utiliser l’option Regrouper par

Utilisez l’option Regrouper par lorsque vous souhaitez une ligne par catégorie plutôt qu’une ligne par enregistrement. Par exemple :

* Une ligne par instructeur, indiquant le nombre de sessions enseignées
* Une ligne par catalogue, affichant le nombre total d’inscriptions
* Une ligne par groupe d’utilisateurs, avec pourcentage de conformité

Si vous souhaitez afficher des enregistrements d&#39;élève individuels ou des lignes d&#39;inscription individuelles, n&#39;appliquez pas l&#39;option Regrouper par.

Lorsque vous appliquez l&#39;option Regrouper par à une colonne, une fonction d&#39;agrégation doit être appliquée à toutes les autres colonnes du rapport. Vous ne pouvez pas afficher une valeur de champ brute à côté d’une colonne groupée, mais uniquement une valeur calculée (nombre, somme, moyenne, etc.).

Par exemple, si vous regroupez par **Nom de l&#39;instructeur**, vous ne pouvez pas afficher les valeurs individuelles de **Nom de la session** à côté. À la place, vous appliqueriez **Nombre** au champ **ID de session** pour afficher le nombre de sessions enseignées par chaque instructeur.

## Application de groupes par et d’agrégations

Dans cet exemple, vous allez comparer la progression de l&#39;inscription entre les élèves. Utilisez ce rapport pour comprendre les performances des différents responsables en termes de progression et d’achèvement de l’inscription.

### Sélectionner des colonnes

1. Lancez **Report Builder** et sélectionnez **Créer un rapport**.
2. Saisissez le nom et la description du rapport :
a. **Nom :** comparez la progression de l&#39;inscription entre les utilisateurs
b. **Description :** ce rapport regroupe les élèves par responsable et calcule des mesures récapitulatives telles que le nombre total d&#39;élèves, la progression moyenne et le nombre d&#39;achèvements pour l&#39;état d&#39;inscription=COMPLETED
3. Sélectionnez les colonnes suivantes : `<dataset>:<column name>`
a. Nom d’utilisateur\de responsable
b. User\Name
c. Inscription\État
d. Inscription\Pourcentage de progression
e. Objet d’apprentissage\Nombre d’achèvements

### Sélectionner Regrouper par colonnes

1. Sélectionnez les colonnes suivantes dans la section **Regrouper par** :
a. Inscription\Statut
b. Nom de l’utilisateur\du responsable
   ![](assets/image020.jpg)
2. Sélectionnez **Appliquer**.

### Sélection des colonnes à agréger

Les fonctions d&#39;agrégation résument les performances d&#39;inscription des élèves par responsable et statut d&#39;inscription, en montrant des nombres d&#39;élèves distincts, des pourcentages moyens de progression de la formation et des nombres moyens d&#39;achèvements d&#39;objets d&#39;apprentissage dans les enregistrements de formation groupés.

1. Sélectionnez **Nombre distinct** pour Utilisateur\Nom.
2. Sélectionnez **Moyenne** pour Inscription\Pourcentage de progression.
3. Sélectionnez **Moyenne** pour Objet d’apprentissage\Nombre d’achèvements.
   ![](assets/image021.png)

### Appliquer des filtres

Appliquez des filtres pour inclure uniquement les inscriptions terminées et exclure les enregistrements avec des noms de responsable manquants, en veillant à ce que le rapport analyse les données d’élève valides pour une progression de la formation précise à l’échelle du responsable et des informations sur l’achèvement.

1. Appliquez un filtre où _État-Inscription_ équivaut à _Terminé_.
2. Appliquez un deuxième filtre où _Nom du gestionnaire d&#39;utilisateurs_ n&#39;est pas vide.
3. Combinez les deux filtres en utilisant la condition AND pour inclure uniquement les enregistrements valides des élèves terminés.

### Enregistrement et téléchargement du rapport

Sélectionnez **Enregistrer le rapport** et sélectionnez **Actions** > **Télécharger** pour télécharger le rapport. Vous recevrez une notification pour télécharger le rapport au format .csv une fois qu’il sera prêt.

Le fichier CSV contient un résumé des inscriptions d’élèves terminées et de la progression de la formation à l’échelle du responsable. Chaque ligne représente un responsable et inclut le nombre d&#39;élèves, le statut d&#39;inscription, le pourcentage de progression moyen et le nombre d&#39;achèvements moyens.

Globalement, le rapport compare l’achèvement de la formation et l’activité d’apprentissage entre les responsables, mettant en évidence les différences dans l’engagement des élèves et le nombre d’objets d’apprentissage terminés.
