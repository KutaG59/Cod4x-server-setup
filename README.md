# Cod4x-server-setup
This is just a repository for Cod4x (Cod4 PC client) to help setup a server. Click on the "server.cfg" above README.md or below. All settings are there besides some modes I believe. 

Any questions/issues feel free to contact me on discord as I rarely look at github Discord: Kutag9


I will soon add a server setup guide for Linux, I use Fedora 39, keep that in mind if you are waiting for a guide, as all commands will use dnf and such. Or follow the guide on Cod4x Github if you are experienced with Linux.


IMPORTANT NOTES: server token is needed to make your server show on the masterlist, you have to link your steam in order to do this. Open [This](http://cod4master.cod4x.ovh/) website and click get a token. Paste the token into set sv_authtoken on Line 15

Set IP/Port  (same as the IP/port in the notepad from step 1) in the cfg file as well.

IF YOU FOUND THIS BY SEARCH, MY GUIDE IS JUST BELOW.




I recently set up a server with the help of [-MAD_DAD-'s](https://botsofwar.forumotion.com/t563-guide-to-setting-up-your-own-cod4-dedicated-server#1558) guide, It is straight to the point, but misses some things that I think should be included for new server hosters/People who arent Tech Savvy and its the only complete guide I can find (might be blind). All credit goes to -MAD_DAD- as without his guide, I would've faulted. This guide is more lengthy, so if you are Tech Savvy and know how to port forward / setup servers, please follow his instead.

1. IP/Port. (If using Hamachi/Radmin or anything, just copy IP from that. port forwarding is still recommended/needed. If you cant port forward, try using default 28960)
**First**  we need your IP and Port to setup your server to let others join. Open CMD on windows, type ipconfig , look for your ipv4 address. Copy (ctrl+shift+c) and paste into notepad for later. 
**Next** is port forwarding, It is very misguided that you should use port 28960. DO NOT USE THIS PORT (Unless absolutely needed). Type any random numbers 4-5 chars long but make sure its between 0 and 65535, like 27491 (dont use) and set as TCP/UDP protocol also paste this port in your notepad.

 (if you do not know how to port forward, First check if your provider has an app for your phone/Panel on their website, if not follow this [guide](https://www.hellotech.com/guide/for/how-to-port-forward)  or this [guide](https://www.noip.com/support/knowledgebase/general-port-forwarding-guide) if the first one doesn't work. If neither of those work, you will have to contact your provider for further assistance.
Once you get to the Port Forwarding screen ignore anything else and, come back to this, and follow what I said above)  In the end, you should have a new port with TDP/UDP on your router/pc.

2. Server Setup.
**First** we need a copy of your game, so copy and paste (or re-extract) your game to a new folder separate from your [Cod4 folder](https://imgur.com/a/W71oVjn). Then we will download the [server files](https://cod4x.ovh/uploads/short-url/kDLPuAqzAQvrQHSbLtCnl9EE9Ec.zip) for windows. (guide may become out of date, if any issue arises first make sure server files are most recently released V21.2 is current as of 12/1/2023)
**Once** the server files are downloaded, open with Winrar/7zip, go into the folders until you see Main/Zone Folder and other loose files. [Drag the loose files](https://imgur.com/a/92Ar1LJ), into the root directory of your server then copy the files inside of the Main/Zone folder from the rar, into the Main/Zone folder of the server.
**After** this has been done, make a shortcut of cod4x18_dederun.exe inside the server folder, we will use this to set "Launch options" like steam.
Right click the shortcut, click properties, and where Target is. Go all the way right with your arrow key, after the " make a space and Paste whats below with the ipv4 and port set to what is pasted in your notepad from Step 1. 

> +set dedicated 2 +set net_ip 000.000.000.000 +set net_port 28700 +set modstats 0 +set rcon_password "Password" +set sv_maxclients 32 +exec server.cfg

**IMPORTANT:** Change the rcon_password, make sure its longer than 6 characters. Its up to you what it is. **DO NOT SHARE, AND DO NOT PASTE THIS OR PUT IT ANY CFG FILE, IT STAYS IN THE SHORTCUT!!!**

**Once** this is set, hit apply, if there is an error, make sure it was fully pasted. There is a character limit, so make sure your folders don't have super long names (ex D:\My Games\Call Of Duty 4 Modern Warfare\Cod Server\) try to keep it short.
If it says cannot apply/invalid/something, delete the shortcut, make a new one, and try it again.  **NOW** Run the server once to get needed folders/files generated for later steps. (it wont work, that is fine)

3. We will now set up the server settings. If you want to do this from scratch (fun but hard) use this [template](https://github.com/CodeBreakerRU/cod4-server-cfg/blob/master/config.cfg) from Cod4x, or you can use [mine](https://github.com/KutaG59/Cod4x-server-setup/blob/main/server.cfg) (I've made it so all maps rotate, with voting enabled, Everything else is default) Once you have a template ready, make a Text file in your server folder. Paste the template in the folder, Click on file in the top left, save/save all and close the Text file. Rename this file to "server.cfg" and move it to the "Main" Folder
**(go through the template if you use mine, you will have to set a host name and such)**

Once that is all done, your folder structure for your server should look like [this](https://imgur.com/a/myEbMCv) or very similar

Launch the shortcut, the server should open and run. Once the console stops spamming logs you should see **"Gameserver is not VAC Secure!"** and following it should be heartbeats from your IP/Port to the masterserver, then following should say **"Server is registered on the master server"** that should be all! Open Cod4x.

Now open the console with **`** (next to 1) and type "connect IP:PORT" (replace ip and port with yours from Step 1) and if you want to have it be private to friends. You can set a password. 
**Open server.cfg in the Main folder**, Line 48 "**set g_password " "**" put your password inside the parenthesis. Now to connect with a password set use command "connect IP:PORT; password Password" (replace 2nd password)

IF YOU NEED ANY HELP, FEEL FREE TO ASK BELOW, IF YOU NEED HELP ASAP, IM TYPICALLY FREE TO HELP // Discord: kutag9

If this is not allowed on the forum for some reason, please tell me where I could post this for other new users to easily find!
Now open the console with **`** (next to 1) and type "connect IP:PORT" (replace ip and port with yours from Step 1) and if you want to have it be private to friends. You can set a password. 
**Open server.cfg in the Main folder**, Line 48 "**set g_password " "**" put your password inside the parenthesis. Now to connect with a password set use command "connect IP:PORT; password Password" (replace 2nd password)

IF YOU NEED ANY HELP, FEEL FREE TO ASK BELOW, IF YOU NEED HELP ASAP, IM TYPICALLY FREE TO HELP // Discord: kutag9
