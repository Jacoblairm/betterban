# BetterBan
BetterBan will SteamId ban a user when they are IP rejected from the server.

Banning a Steam client from your server will just allow the user to change account and continue playing on the server. BetterBan will ban the client and also for a specified amount of time `bb_ip_banlength` will ban every user that attempt to connect using the same IP address.

You might be thinking, why dont I just ban their IP? Well this will work but wouldn't you like to ban their second account or third account (and so on) that try to connect but are IP rejected? This is the functionality of this plugin. 

The only case that this plugin is inneffective is if the client changes their IP address before connect with a new SteamID.

#Installation
Drag betterban.smx into your Sourcemod plugins folder and restart your server or type "sm plugins load betterban" into the server console.

#Usage
`betterban <clientid> [Message to user]`

Hint:

* The clientid can be retrieved by typing status and using the second userid digit, as highlighted in this image ![Alt text](http://puu.sh/tcQLn/61d6bcb848.png "Status Output")

* Message is optional and needs to be quoted.
example: 

`betterban 1 "You have been banned for wallhacking"`

Each entry of IP addresses (along with a EPOCH timestamp) are stored line by line in addons/sourcemod/configs/iplist.cfg

ConVar `bb_ip_banlength` determines the time (in seconds) that the IP addresses will ban a client, after this time the IP addresses will be removed from the iplist.cfg file. The default time is 432000 (5 days).
