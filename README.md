# KadesGDPS-2.0
This is the seccond and inproved version of kadesgdps runing on CGDPS
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
Now do `git https://github.com/Cvolton/GMDprivateServer.git` We use cvoltons server as a base (do `sudo apt-get install git`
if its not a command). Now if you want to you could install phpmyadmin which i think you should but thats your prefence
im not gonna use the mysql term. `sudo apt-get install phpmyadmin` `sudo ln -s /etc/phpmyadmin/apache.conf /etc/apache2/conf-available/phpmyadmin.conf` `sudo ln -s /usr/share/phpmyadmin /var/www/html/` `sudo a2enconf phpmyadmin` `sudo service apache2 reload`
after that navigate into http://(your_vps_ip)/phpmyadmin then type the user detials you set in the install of phpmyadmin. Then download https://codeload.github.com/Cvolton/GMDprivateServer/zip/master then make a database named geometrydash. then take the .db in the zip and upload it into that database. 
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
