# arkmanager
Multi-ARK-Manager – linux script with autoupdate and watchdog

Multi-ARK-Manager, linux script that can manage multiple instances of ARK survival evolved server with autoupdates and keep them running. With small adjustments, you can keep all the servers published via Steam up and running. The particular thing is that it is designed for n instances, so you can manage multiple servers and only need one config file per server.

usage: arkmanager < ArkServerNumber > < start|wipestart|stop|kill|runcheck|restart|install|update|broadcast|backup|restore > [broadcast text]

The following commands are implemented:

Start - self explanatory
Wipestart - start with redistribution of the untamed dinos in the world
Stop - stops the server via RCON (regular stop)
Kill - stops the server via screen (abort)
Runcheck - checks if the server is running and restarts it if necessary
Restart - self explanatory
Install - installs the server files at a given location
Update - check if new server version is available with controlled update
Broadcast - fast way to send a message to the server (chat)
Backup - copies all World, Tribe and Player files to a given location
Restore - copies all World, Tribe and Player files back from the backup location


With the help of the crontab you can do update check (update) hourly, in which the users are warned in time, the server is stoped, updated and restarted. 
It is also possible to check every x minutes whether the server is still running (runcheck) and, if necessary, restart it.
