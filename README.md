# BetterBan
BetterBan will SteamId ban a user when they are IP rejected from the server.

Banning a Steam client from your server will just allow the user to change account and continue playing on the server. BetterBan will ban the client and also for a specified amount of time ("bb_ip_banlength") will ban every user that attempt to connect using the same IP address.

You might be thinking, why dont I just ban their IP? Well this will work but wouldn't you like to ban their second account or third account (and so on) that try to connect but are IP rejected? This is the functionality of this plugin. 

The only case that this plugin is inneffective is if the client changes their IP address before connect with a new SteamID.

#Installation
Drag betterban.smx into your Sourcemod plugins folder and restart your server or type "sm plugins load betterban" into the server console.


#Usage
betterban <clientid> <(Optional) Message to user>
Hint:

1. The clientid can be retrieved by typing status and use the second userid digit. 
As highlighted in this image - ![Alt text](http://puu.sh/tcQLn/61d6bcb848.png "Status Output")

2. Message needs to be quoted

example: betterban 1 "You have been banned for wallhacking"
