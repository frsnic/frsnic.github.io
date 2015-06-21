---
layout: post
title: "Wordpress Not Found."
description: ""
category: wordpress, note
tags: [wordpress]
---
{% include JB/setup %}

If you get the same error like me
> ##Not Found
The requested URL /your_url was not found on this server.

***
Check  below
#### 1. apache defualt is disable ".htaccess", you need to manual enable it.
```
$ sudo vi /etc/apache2/sites-available/$site
<VirtualHost *:80>
		....
        <Directory "/var/www/$site">
                AllowOverride All
        </Directory>
        ...
</VirtualHost>
```
***
#### 2. apache default not load rewrite.load
```
cd /etc/apache2/mods-enabled
ln -s ../mods-available/rewrite.load
```
***
#### 3. last check your apache can write to your .htaccess
```
$ ls -l your_project/.htaccess
-rwxrwxr-- 1 www-data www-data 436  6月 21 15:20 .htaccess
```