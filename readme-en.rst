Minecraft Server On DotCloud
============================

This is a port of the Minecraft game server for running on dotCloud. The server is vanilla, it has no plugins installed. Using these files you should be able to get the server is up and running instantly.

How Does it work ?
-------------------

It downloads the jar file directly from Minecraft, to ensure it is up-to-date, and configures the Minecraft server within the constraints allowed by dotCloud via scripts.

How do I use it ?
--------------------

Clone the repo to your computer, install the dotcloud CLI tool and push it

	dotcloud push applicationname 

When the application has been deployed, the server address and port to use for the Minecraft client will be displayed.

How to administer the Minecraft server ?
------------------------------------------

The server Minecraft is started on a screen so that you can control it. First you connect to your dotCloud app via SSH:

	dotcloud ssh applicationname.minecraft

Once you are connected: 

-All file-server-specific Minecraft logs in ~/minecraftserver:

	$cd ~/minecraftserver

-To access the Minecraft console:

	$screen -x MCServer

To exit a screen ``CTRL + A`` then ``CTRL + D`` . NEVER press ``CTRL + C`` because it will stop the process of screen and then unavoidably the Minecraft server.
