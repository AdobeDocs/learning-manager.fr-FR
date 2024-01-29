---
title: Transition à partir du gestionnaire FTP d’Adobe
description: Adobe Learning Manager prend en charge un nouveau connecteur utilisant le protocole SFTP de la famille de transfert AWS. Vous pouvez remplacer n’importe quel client FTP open source par FTP Manager Adobe.
source-git-commit: aa8030e7e1d0ad72b76fb48a34e7b15ddf178a0b
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 0%

---


# Transition à partir du gestionnaire FTP d’Adobe

Adobe Learning Manager prend en charge un nouveau connecteur utilisant le protocole SFTP de la famille de transfert AWS.

Vous pouvez remplacer n’importe quel client FTP open source par FTP Manager Adobe.

Certains clients FTP recommandés par AWS sont répertoriés [ici](https://docs.aws.amazon.com/transfer/latest/userguide/transfer-file.html):

* FileZilla (Windows, macOS et Linux)
* OpenSSH (macOS et Linux) - Remarque : ce client ne fonctionne qu&#39;avec des serveurs activés pour le protocole SFTP (Secure Shell).
* WinSCP (Microsoft Windows uniquement)
* Cyberduck (Windows, macOS et Linux)

## Configuration du connecteur FTP AWS

Vous devez configurer le nouveau connecteur FTP basé sur AWS sur l’administrateur de l’intégration.

![image des connecteurs](assets/alm-ftp.png)
*Sélectionnez l’option FTP.*

Une fois la connexion établie, la page Détails de la connexion s’affiche.

![page de détails connecter](assets/connection-name.png)
*Affichage de la page Détails de la connexion*

Il existe trois options d’authentification :

### Créer une authentification en générant de nouvelles clés SSH

Si vous souhaitez générer la clé SSH dans votre système lui-même, vous pouvez le faire. Cliquez sur Générer la clé SSH.

La clé privée est téléchargée sur votre ordinateur et la clé publique est enregistrée dans nos services. Une fois que vous avez cliqué sur Se connecter, l’utilisateur FTP est créé avec les clés publique et privée comme authentification.

Vous avez créé une connexion FTP.

### Créer une authentification à l’aide de clés SSH existantes

Si vous disposez déjà d’une clé SSH, collez la clé publique dans le **[!UICONTROL Clé publique FTP]** , puis cliquez sur Se connecter.

![Touches SSH](assets/ssh-keys.png)
*Coller les touches*

### Créer une authentification de base à l’aide d’un mot de passe

Il s’agit du mécanisme d’authentification de base. Sélectionnez la première option. **[!UICONTROL Créer une authentification de base à l’aide d’un mot de passe]**. Saisissez le mot de passe, puis cliquez sur **[!UICONTROL Se connecter]**.

Cela crée une connexion.

## Prochaine étape

### Configuration du client FTP

Configurez la connexion sur un client FTP (recommandé dans la section précédente) avec les clés téléchargées ou les clés ou mots de passe existants.

### Exemple d’exportation de test

* Dans votre client FTP, changez l’emplacement du FTP ExaVault en nouvel emplacement FTP. Le nouveau domaine est `http://almftp.adobelearningmanager.com/`.
* Vous devez également ajouter l’adresse IP à la liste d’autorisation. `18.195.107.67`.
* Après l’authentification, vous devez charger et télécharger quelques exemples de fichiers vers et depuis le nouvel emplacement FTP à l’aide de clients FTP externes ou de scripts d’automatisation.
* Vous devez transférer les données de l’ancien emplacement vers le nouvel.
* La stratégie de rétention des données pour le connecteur reste la même. ExaVault prenait également en charge certaines politiques de conservation des données en plus de la politique officielle. Ces règles de rétention des données ne seront pas disponibles pour le nouveau connecteur. Vérifiez si votre connecteur utilise une rétention des données autre que les stratégies officiellement prises en charge.

### Qu’advient-il des projets de migration ?

| Statut | Recommandation |
|---|---|
| Nouvelle migration | Vous ne pouvez pas démarrer de nouvelles migrations à partir de l’ancien FTP. Vous devez utiliser le nouveau FTP pour les nouvelles migrations. Pour obtenir plus d’informations à ce sujet, contactez l’équipe de réussite client. |
| Migration en cours | Création d’un sprint : vous pouvez continuer à utiliser l’ancien FTP, mais nous vous recommandons d’utiliser le nouveau FTP. Contactez l’équipe de réussite client pour tout sprint existant qui ne peut pas être modifié. |
| Migration fermée | Aucune action. |

## Connexion à Adobe Learning Manager à l’aide du client FTP Filezilla

1. Se connecter au nouveau connecteur FTP ALM. Cliquez sur Se connecter.

   ![connecter une image](assets/connect-client.png)
   *Se connecter au nouveau connecteur FTP ALM*

1. Pour vous connecter via une authentification de base par mot de passe, saisissez le nom de domaine, le nom d’utilisateur FTP et configurez un mot de passe correspondant aux critères de validation du mot de passe. Cliquez sur Se connecter. La nouvelle connexion FTP sera créée et accessible via n’importe quel client SFTP.

   ![paramètres ftp](assets/connect-settings.png)
   *via l’authentification de base via mot de passe*

1. Installez n’importe quel client SFTP, par exemple, File Zilla. Lancez File Zilla et cliquez sur Open Site Manager dans le coin supérieur gauche.

   ![client SFTP](assets/sftp-client-install.png)
   *Se connecter via un client SFTP*

1. Cliquez sur **[!UICONTROL Nouveau site]** pour créer un nouveau site. Renommez le site selon vos besoins.

   ![nouveau site](assets/new-site.png)
   *Création d’un site*

1. Mappez les détails de la page d’informations d’identification du connecteur.

   * Sélectionnez le protocole « SFTP - SSH File Transfer Protocol ».
   * Hôte en tant que domaine FTP
   * Type de connexion « Demander un mot de passe »
   * Utilisateur comme nom d’utilisateur FTP

1. Cliquez sur Se connecter.

   ![informations d’identification](assets/connector-credentials.png)
   *Saisir les informations d’identification*

   >[!NOTE]
   >
   >Effectuez cette étape dans le client File Zilla.

1. Saisissez le mot de passe.

   (Facultatif) Cochez la case Mémoriser le mot de passe pour le mémoriser.

   ![mot de passe](assets/password.png)
   *Saisir un mot de passe*

   (Facultatif) Sélectionnez l’option **[!UICONTROL Toujours faire confiance à cet hôte]** case à cocher pour approuver l’hôte.

1. Cliquez sur OK.

   ![clé d&#39;hôte inconnue](assets/unknown-host-key.png)
   *Clé d’hôte*

1. Vérifiez le statut et la progression de la connexion en haut.

   La moitié gauche correspond au site local et la moitié droite au site distant.

   Pour déplacer des fichiers du local vers le distant et inversement :

   * Vous pouvez faire glisser et déposer des fichiers.
   * Double-cliquez sur le fichier.

   ![état de la connexion](assets/connection-status-progress.png)
   *Vérification de l’état de la connexion*

À tout moment, vous pouvez modifier et mettre à jour le type d’authentification.

Les autres méthodes d’authentification sont les clés SSH :

Collez votre clé publique dans la zone de texte pour utiliser les clés SSH existantes. Cliquez sur Connecter/Enregistrer.

Pour générer de nouvelles clés SSH, cliquez sur le bouton **[!UICONTROL Générer une clé SSH]** bouton. La clé privée sera téléchargée. Cliquez sur **[!UICONTROL Connecter/Enregistrer]**.

![générer la clé ssh](assets/ssh-key.png)
*Générer une clé SSH*

Mappez les détails. Sélectionnez le type de connexion en tant que fichier de clé. Sélectionnez le fichier de clé privée.

Cliquez sur **[!UICONTROL Se connecter]**.

## Que se passe-t-il une fois qu’ExaVault est obsolète ?

Une fois qu’ExaVault est obsolète, tous les projets de migration existants, qui sont en cours, sont transférés vers le nouveau FTP en tant qu’emplacement source. Vous devez ensuite configurer le nouveau connecteur FTP et poursuivre le processus de migration.

## Recommendations pour migrer des sprints

Lors de la création d’un projet de migration, Adobe vous recommande d’utiliser le nouveau connecteur SFTP d’AWS pour éviter la migration de sprint d’Exavault vers AWS à un stade ultérieur.

Si une migration est en cours, fermez le sprint actuel qui utilise Exavault comme source de données. Créez la connexion AWS SFTP, testez la configuration et contactez l’équipe de réussite client pour passer à la nouvelle source de données AWS SFTP. Après le basculement, créez un nouveau sprint dans le même projet de migration. Les dossiers sprint sont créés dans le nouvel emplacement et vous pouvez charger les fichiers CSV de migration pour poursuivre l’activité.

**Cas où un projet de migration ne peut pas être fermé**

* Le mappage d’ID de cours est effectué dans le projet actif pour les cours qui sont migrés depuis des systèmes hérités externes vers Adobe Learning Manager. Vous ne pouvez le faire que si vous souhaitez mettre à jour les mêmes cours dans le même projet. Une fois le projet fermé, vous ne pouvez plus modifier ses détails.
* Pour les projets de migration basés sur l’API, où vous ne devez pas fermer de projet.
