Minecraft Server On DotCloud
============================

C'est un portage de serveur de jeu Minecraft pour dotCloud.
Le serveur est nu, c'est à dire qu'il n'a aucun plugins tel que CraftBukkit. Lors du déploiement, le serveur est fonctionnel instantanément.

Comment ça marche ?
-------------------

Il récupère le fichier jar directement sur le site Minecraft pour assurer la pérennité et configure le serveur Minecraft selon les contraintes imposées par dotCloud via des scripts.

Comment l'utiliser ?
--------------------

Utiliser la méthode du Clone-And-DotCloud-Push:

	dotcloud push applicationname 

A la fin de ce push, l'adresse du serveur et son port à utiliser pour les clients Minecraft seront affichés.

Comment administrer le serveur Minecraft ?
------------------------------------------

Le serveur Minecraft est lancé dans un screen, pour garder la possibilité de l'administrer.
Tout d'abord connectez vous en SSH sur votre service dotCloud:

	dotcloud ssh applicationname.minecraft

Une fois le sheel démarré:

-Tous les fichiers propres au serveur Minecraft se loge dans ~/minecraftserver:

	$cd ~/minecraftserver

-Pour accéder dans la console Minecraft:

	$screen -x MCServer

Et pour quitter un screen ``CTRL + A`` puis ``CTRL + D``. Surtout ne JAMAIS faire un ``CTRL + S`` car ça arrêtera le processus de screen et donc inévitablement le serveur Minecraft.

