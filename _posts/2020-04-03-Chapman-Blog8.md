---
layout: post
title: "Blog 8"
---
Install WordPress with Ubuntu
-----------------------------

WordPress is the most popular open-source blogging system and CMS on the Web. It is based on PHP and MySQL. Its features can be extended with thousands of free plugins and themes.

What you need before you get started:

	Ubuntu 16.04
	Apache2 server running


### Intsall WordPress
Use the following command:

	$ sudo apt update
	$ sudo apt install wordpress php libapache2-mod-php mysql-server php-mysql

### Configure Apache for WordPress
Create Apache site for WordPress. Create
	/etc/apache2/sites-available/wordpress.conf
with following:

	Alias /blog /usr/share/wordpress
	<Directory /usr/share/wordpress>
		Options FollowSymLinks
		AllowOverride Limit Options FileInfo
		DirectoryIndex index.php
		Order allow,deny
		Allow from all
	</Directory>
	<Directory /usr/share/wordpress/wp-content>
		Options FollowSymLinks
		Order allow,deny
		Allow from all
	</Directory>

Then, enable this site with:

	$ sudo a2ensite wordpress

Next, enable URL rewriting with:

	$ sudo a2enmod rewrite

Then, reload apache2 with:

	$ sudo service apache2 reload

### Configure database
To configure WordPress, a MySQL database must be created.

	$ sudo mysql -u root

	mysql> CREATE DATABASE wordpress;
	Query OK, 1 row affected (0,00 sec)

	mysql> GRANT SELECT,INSERT,UPDATE,DELETE,CREATE,DROP,ALTER
		-> ON wordpress.*
		-> TO wordpress@localhost
		-> IDENTIFIED BY '<your-password>';
	Query OK, 1 row affected (0,00 sec)

	mysql> FLUSH PRIVILEGES;
	Query OK, 1 row affected (0,00 sec)

	mysql> quit

Configure WordPress to use this database. Open /etc/wordpress/config-localhost.php and write:

	<?php
	define('DB_NAME', 'wordpress');
	define('DB_USER', 'wordpress');
	define('DB_PASSWORD', '<your-password>');
	define('DB_HOST', 'localhost');
	define('DB_COLLATE', 'utf8_general_ci');
	define('WP_CONTENT_DIR', '/usr/share/wordpress/wp-content');
	?>

Enable MySQL with:

	$ sudo service mysql start

### Configure WordPress
Open localhost/blog in your browser. You will be asked for title of your new site, username, password and address e-mail. You can choose if you want to make your site indexed by search engines.

You can now login under localhost/blog/wp-login.php. In Dashboard, you will see bunch of icons and options. Don’t worry, it’s easy!
