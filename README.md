RVCM is a revival of the Kirjuri project by Antti Kurittu. The intention is to update the code to be compatible with newer version of PHP and to maintain the project. The older code works with PHP 7, if you would like to test it out you can find it on Antti's github https://github.com/AnttiKurittu/kirjuri please see security update below taken from his github page.

# Project UPDATE (25 June 2022)

RVCM should be working with the most recent version of PHP. 

# Project UPDATE (22 June 2022)

Requirements (so far)
* httpd
* php
* mysql
* php-mysql

You should only have to allow port 80.

To test if you're web server is running you can navigate to your web servers IP in a browser.

Your apache install should have created a directory in /var/www/html/ make a new directory in the html directory this will be the root of your instance of RVCM. You'll need to change permissions in a few directories after cloning. Example below if you're running the web server as www-data. You can also change the permissions of the whole directory (you might actually need to do this anyway). 

Permissions below were set for testing!

sudo chown –R <user":www-data conf 

sudo chown –R <user>:www-data cache 

sudo chown –R <user>:www-data logs 

Might also need to change the write permissions. 

sudo chmod -R 777 <directory>

Once these changes have been made you should be able to start the install process. Open a browser and navigate to the IP of your web server and name of the directory you created in html. i.e. x.x.x.x/rvcm/install.php

MySQL

You'll have to create a database user before proceeding with the next step.

CREATE USER '<username>'@'%' IDENTIFIED BY 'password';
<strong>To change password</strong> ALTER USER 'rv'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON *.* TO 'rv'@'%';
FLUSH PRIVILEGES;


# SECURITY UPDATE (7.5.2021)

As this project has been inactive for years, it was inevitable that some of the dependencies will become out of date. There are several security vulnerabilities in the dependencies involved, and some of the dependencies, like Twig, don't play nice with the newest version of PHP. IF you wish to install and use Kirjuri, please update the dependencies manually & make sure you install it in a safe environment. The original advice was to install in an [air-gapped environment](https://en.wikipedia.org/wiki/Air_gap_(networking) and this advice still stands.

As always, I can not guarantee the security of this software, and any users will be solely responsible of configuring it securely before using. There have been several attempts by well-meaning individuals to develop this project further, but they have all been deterred from it by the quality of the code and the lack of proper commenting.

**Use Kirjuri at your own risk.**

# Kirjuri

Kirjuri is a simple php/mysql web application for managing physical forensic evidence items. It is intended to be used as a workflow tool from receiving, booking, note-taking and possibly reporting findings. It simplifies and helps in case management when dealing with a large (or small!) number of devices submitted for forensic analysis. Kirjuri requires PHP7.