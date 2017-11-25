# KadesGDPS-2.13. Gdps version: 2.11
This is the amazing guide to making the new 2.11 gdps
# Souce Use
This source is ment for people to learn how to make a gdps not to copy mine xD
# How to install a gdps on your linux apache2 server
# Requirements
 Need a apache2 server
 Use debian/Ubuntu
 Mysql Server
 Phpmyadmin (optinal)
# Installing
This is very simple first you start out with installing apache2 (duh)
`sudo apt-get install apache2`
Then We Need Mysql Install it by using `sudo apt-get install mysql-server`
Then Go into root `sudo su` then navigate to `/var/www/html/` with `cd /var/www/html/` if your not
root then you cant modify files in there (unless you give your self the www-data group)
Now do `git clone -b permsDashboardUpdate https://github.com/Cvolton/GMDprivateServer.git` We use cvoltons server as a base (do `sudo apt-get install git`
if its not a command). Now if you want to you could install phpmyadmin which i think you should but thats your prefence
im not gonna use the mysql term. `sudo apt-get install phpmyadmin` `sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf` `sudo ln -s /usr/share/phpmyadmin /var/www/html/` `sudo a2enconf phpmyadmin` `sudo service apache2 reload`
after that navigate into http://(your_vps_ip)/phpmyadmin then type the user detials you set in the install of phpmyadmin. Then download https://codeload.github.com/Cvolton/GMDprivateServer/zip/permsDashboardUpdate then make a database named geometrydash. then take the .db in the zip and upload it into that database. 
# Config
right that was alot but now is the hard part for most people. we have to go into the files of the git you put in your /var/www/html/ folder and then rename the folder to database then go into it then go to /config/connection.php it should look like this
```
<?php
$servername = "127.0.0.1";
$username = "root";
$password = "";
$dbname = "geometrydash";
?>
```
heres what you do. for `$servername = "127.0.0.1";` keep it the same. for `$username = "root";` enter your mysql user (the same as your phpmyadmin user) for `$password = "";` enter your password to your phpmyadmin(mysql) keep `$dbname = "geometrydash";` the same.
now you must be thinking alright im done right? nope your not, Now go to http://www.freenom.com/ and make a account and then register a free domain name thats matches http://www.boomlings.com in chars like this:
```
kadesgdpsdatabasegdps.tk
http://www.boomlings.com
```
then after that go register https://www.cloudflare.com/ if you havent then register that domain then when it ask you for dns put your vps ip in your ipv4. Then go download http://bit.ly/2otfCPU (this is from http://keenlos.ueuo.com) its the cracked gd then extract it into a folder then get hxd https://mh-nexus.de/en/downloads.php?product=HxD . then rename geometrydash.exe to (anything).exe cant be geometrydash.exe tho. 
# Making The GDPS Connect
go to https://www.base64encode.org/ and encode 
http://www.boomlings.com and your domain then go into hxd and replace http://www.boomlings.com with your domain then, http://www.boomlings.com encoded domain. Now if you run it you should be able to register with a fake email and it should work!
If not post in Issues.
# How to use the gdps
First you can add roles in the roles table
go to insert and you will see a bunch of new stuff.
the perms will look simple but there is some stuff
Quote cvolton:
```
with the most recent version of the gdps source, modBadgeLevel and actionRequestMod accept values 0-2 (0=not a mod, 1=normal mod, 2=elder mod) and modBadgeLevel must be at least 1 for colored comments to work.

Also I recommend creating a normal user role that has isDefault set to 1 (leave it at 0 for all other roles, otherwise the GDPS might get confused and could make all people mods)

Also priority exists because you can assign multiple roles to 1 person, the GDPS always goes from the top to the bottom when checking permissions - setting a permission to 0 means "check if a lower priority role has the permission and if the user requesting it has that lower priority role"

I hope I didn't make this explaination too confusing. I plan to make a role manager in the dashboard later on, but I'm currently focusing on updating the GDPS to 2.11 and getting the system to actually work, since commands for example still depend on the old isAdmin variable instead of the permissions system
```
And really thats it. For 2.11 atleast
## What if i want robtops color
Change your account id in accounts and change your extid in users to 71
