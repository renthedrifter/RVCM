# Project UPDATE (22.6.2022)

Working on getting DrifterCM to work with most recent version of PHP (8.1.2).

Requirements (so far)
* httpd
* php
* mysql
* php-mysql

You should only have to allow port 80.

To test if you're web server is running you can navigate to your web servers IP in a browser.

Your apache install should have created a directory in /var/www/html/ make a new directory in the html directory this will be the root of your instance of DrifterCM. You'll need to change permissions in a few directories after cloning. If you're running the web server as www-data.

sudo chown –R www-data:www-data conf 

sudo chown –R www-data:www-data cache 

sudo chown –R www-data:www-data logs 

Once these changes have been made you should be able to start the install process. Open a browser and navigate to the IP of your web server and name of the directory you created in html. i.e. x.x.x.x/DrifterCM/install.php

MySQL

You'll have to create a database user before proceeding with the next step.

# Project UPDATE (21.6.2022)

Intentions for this project is to update and maintain a case management system based off of Kirjuri a project originally created by Antti Kurittu. 

# SECURITY UPDATE (7.5.2021)

As this project has been inactive for years, it was inevitable that some of the dependencies will become out of date. There are several security vulnerabilities in the dependencies involved, and some of the dependencies, like Twig, don't play nice with the newest version of PHP. IF you wish to install and use Kirjuri, please update the dependencies manually & make sure you install it in a safe environment. The original advice was to install in an [air-gapped environment](https://en.wikipedia.org/wiki/Air_gap_(networking) and this advice still stands.

As always, I can not guarantee the security of this software, and any users will be solely responsible of configuring it securely before using. There have been several attempts by well-meaning individuals to develop this project further, but they have all been deterred from it by the quality of the code and the lack of proper commenting.

**Use Kirjuri at your own risk.**

# Kirjuri

Kirjuri is a simple php/mysql web application for managing physical forensic evidence items. It is intended to be used as a workflow tool from receiving, booking, note-taking and possibly reporting findings. It simplifies and helps in case management when dealing with a large (or small!) number of devices submitted for forensic analysis. Kirjuri requires PHP7.

[See the official Kirjuri home page for more details.](https://kurittu.org/2018/06/kirjuri/)

NOTICE: Kirjuri is no longer actively developed since 09/2017, as I don't have time for this project anymore. If you are interested in developing this tool further, please contact me.

OVERVIEW & LICENSE
------------

Kirjuri is developed by Antti Kurittu. It was started at the Helsinki Police Department as an internal tool. Original development released under the MIT license. Some components are distributed with their own licenses, please see folders & help for details.

CHANGELOG
------------

see [CHANGELOG.md](CHANGELOG.md)

LOOKING TO PARTICIPATE?
------------
* Everyone interested is encouraged to submit code and enhancements. If you don't feel confident submitting code, you can submit lanugage files and localized lists of devices etc. These will gladly be accepted.

SCREENSHOTS
------------

![1](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/1.png)
![2](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/2.png)
![3](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/3.png)
![4](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/4.png)
![5](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/5.png)
![6](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/6.png)
![7](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/7.png)
![8](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/8.png)
![9](https://github.com/AnttiKurittu/kirjuri/blob/master/extra/screenshots/9.png)
