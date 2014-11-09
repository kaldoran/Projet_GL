##Prise d'idée et de note

####Idee :
- Gestionnaire FTP
- Application emploi du temps 
- Mini ent

####Idee retenue :
- Gestionnaire FTP a avec Client - Serveur

####Langage : 
Java et Mysql

####Nom logiciel :
Kould Not Share

####Cible :
Tout public 

####Serveur :
- Partie Doit :
	- Doit pouvoir partager des fichier par le protocol ftp ( port 21 - 22 )
	- Doit avoir une interface graphique
	- Doit avoir un fichier public qui contient des informations
- Les comptes :
	- l'administrateur peut crée des comptes utilisateurs
	- chaque compte donne acces à certain fichier
	- l'administrateur doit pouvoir parametrer les acces aux fichiers pour chaque compte
- Partie Devrait :
	- Devrait pouvoir changer le port
	- Devrait pouvoir fixer la taille maximum des fichier qui peuvent etre envoyé
	- Devrait pouvoir fixer le nombre maximum de téléchargement d'un fichier
	- Devrait pouvoir fixer les heures de téléchargement
	- Devrait faire des stats
	- Devrait pouvoir filter les fichiers ( extension ) 
	- Devrait pouvoir etre accessible en ligne de commande ( sans interface graphique )
	- Devrait pouvoir bannir une personne / ip / compte
	- Brider le taux de transfere par utilisateur 
	- Crypter un envoi de fichier
	- Devrait pouvoir, voir en temps réel qui est connecté ( ce qu'il télécharge ) , heure de début, heure de fin
	- Crée des utilisateurs temporaire

####Client :
- Devrait pouvoir limiter le taux de transfere
- Doit pouvoir changer sont mot de passe
- Devrait gérer les bookmarks
	


##Partie du DSE

####CLIENT
- Interface graphique (à definir la prochaine reunion)
- Authentification (client vers serveur)==Nico
- Gestionnaire de marque-page == KB
- Creation de statistiques Client == KL
- limitation == KB
	- Brider le taux de transfere de manière général
	- pouvoir definir des tranches horaire de téléchargement (exemple : de 0H00 à 7h00 )
- Download == KL
- Upload == KL

####SERVEUR
- Interface graphique(à definir la prochaine reunion)
- Authentification administrateur (machine local) : pour faire des modif, l'admin doit s'authentifier == Nico
- partage de fichier (l'administrateur choisit quel fichier/dossier il veut partager) == Nico
- Gestion des utilisateurs == NIC0
	- Creation de compte utilisateur
	- Création des utilisateurs temporaire
	- stockage login et password
	- droit au téléchargement sur les fichiers
	- Attribution d'un espace pour chaque utilisateur
	- Pouvoir bannir une personne / ip / compte
- Creation de statistiques Serveur == KL
- limitation  == KB
	- Brider le taux de transfere par utilisateur
	- pouvoir definir des tranches horaire de téléchargement (exemple : de 0H00 à 7h00 )
	- pouvoir filter les fichiers ( extension )
- avoir un fichier public qui contient des informations == KL
- Creation de fichier log (savoir qui est connecté, à quel heure, les propriétaire de fichier) == KL
- Download == KL
- Upload   == KL

####COMMUN
- Communication/réseau == KL
- Utilisation des dossiers (chaque utilisateur à un dossier)==KB
- Download (établir une connexion entre client/serveur) == KL
- Upload == KL
- Cryptage Décryptage un envoi de fichier == KB

####USE CASE
![Use case client](https://raw.githubusercontent.com/kaldoran/Projet_GL/dev/Document_des_exigences/Ressources/Client.png "Use case client")

![Use case serveur](https://raw.githubusercontent.com/kaldoran/Projet_GL/dev/Document_des_exigences/Ressources/Serveur.png "Use case serveur")

## DSE, Voir pour une V2.0
##DSE, exigences à modifier:

####Procédure d'initialisation de la communication ( 3.1.1.5.1.3 & 3.1.1.5.1.4)
- On ne doit pas clore la communication sur le port 21 elle servira a fournir les dossiers qui existent.
- Pourquoi un port perso ? il y a le 21 et 20 a utiliser c'est tout me semble

####Marque-pages 
- Modifier liste de nom vers liste de bouton de connexion.
- Ajouter methode enregistrement.

####Limitations
- préciser methode plannification.

####Bannissement 
- Changer les numéro ( subparagraph de gestion de compte) 

####Utilisation des dossiers
- rennomage des fichiers et dossiers.

##Divers
- exemple de fichier de gestion de droits: Nicolas:password@/home/Dossier_de_Nicolas/
	




