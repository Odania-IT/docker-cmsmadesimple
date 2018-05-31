# CMS Made Simple

This Docker Image provides cms made simple served by apache.

At the first start you need to setup the CMS. Run it with:

	docker run -ti -p 8080:80 -v /tmp/config.php:/var/www/html/config.php odaniait/cmsmadesimple

You need to set the following environment variable:

	MYSQL_HOST
	MYSQL_USER
	MYSQL_PASSWORD
	MYSQL_DATABASE
	REMOVE_INSTALL_FOLDER <- If this is set to any value, the install folder will be deleted

For persisting uploaded data you should mount the volumes:

	/var/www/html/uploads
	/var/www/html/modules
