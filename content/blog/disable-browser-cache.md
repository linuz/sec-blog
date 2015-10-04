Title: Disabling Browser Cache in Apache
Date: 2015-10-04 01:40
Tags: Apache

Since I plan on blogging fairly often, it might be a good idea to configure apache to inform browsers not to cache the site. That fixes the problem of readers not always seeing new blog posts right away. I am running Apache Web Server so here is what I did to disable caching:

First, enable the **headers** apache module

	sudo a2enmod headers

Next, add the following lines to your **.htaccess** file, or create one if it does not exist:

	<FilesMatch "\.(html|htm)">
		FileETag None
		Header unset ETag
		Header set Cache-Control "max-age=0, no-cache, no-store, must-revalidate"
		Header set Pragma "no-cache"
		Header set Expires "Tue, 1 Jan 1980 01:00:00 GMT"
	</FilesMatch>

