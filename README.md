webadmin
========

forked from https://gist.github.com/nic-o/1219610


This is a simple PHP script to manage files on a web server. 

Requirements: PHP, MySQL, Windows/Linux 


There are a lot of changes and functionalities added with regards to the original webadmin script. These are listed below:

1. Admin user: The user has complete access to the files on the system. He can grant access to read write and execute permissions to users on per file, per user basis.
2. User management: Users can register to the site. They need approval from the site admin to access the contents of the site.
3. File/Folder access management: Generally, new users are limited to read permission. Write and Execute permissions can be demanded to the admin. This is notified via email to the admin that contains the links for accepting and denying the request.
4. Functionalities: Copy, Move, Zip, Delete, Create Shortcut, Directory Listing, Creating Symlinks etc.


FILES
-----

1. webadmin.ini
This is the basic configuration read by webadmin.php


   ;;; database configurations
   [db]
   user = dbuser
   password = pass
   host = localhost
   port = 3306
   dbname = webadmin

   ;;; site specific configurations
   [site]
   base_url = http://localhost/proj/webadmin.php

   ;;; this is the site owner's email
   admin_mail = coderpurple@gmail.com

   ;;; this is site owner's password
   admin_password = paword

The webadmin.php script is coded to search for webadmin.ini in a folder above the webadmin.php
E.g. If webadmin is located in /var/www/project/webadmin.php, then the ini file needs to be located at /var/www/webadmin.ini

2. db.sql
MySQL database used for the project.

3. webadmin.php


Notes: 

1. For mail sending functionality, I presume that the machine is installed with Postfix or Sendmail utilities.
2. Please rename the webadmin.ini.template file to webadmin.ini in the appropriate directory.

