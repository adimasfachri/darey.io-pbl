# PROJECT 1: LAMP STACK IMPLEMENTATION

1. Update ubuntu & install apache with ```sudo apt update -y && sudo apt install apache2 -y```

2. Verify that apache2 service is running with ```sudo systemctl status apache2```

![service apache](https://user-images.githubusercontent.com/55023518/162229467-c3c259ee-df0e-4164-9e90-ea48dbfb90ad.jpg)

3. Because we run this on aws instance, we must open the TCP port 80 to open inbound connection through port 80

![aws tcp rule](https://user-images.githubusercontent.com/55023518/162231253-16dad47e-9ad1-451b-805b-b2e751b106a5.jpg)

4. Verify that we can access the apache web server

![apache 2](https://user-images.githubusercontent.com/55023518/162246544-5c8932e9-5246-4ad8-a3f7-0dc03a9302b6.jpg)

5. After that install mySQL database with ```sudo apt install mysql-server -y```

6. run a security script that comes pre-installed with MySQL ```sudo mysql_secure_installation```

7. verify that we can run mysql 

![mysql](https://user-images.githubusercontent.com/55023518/162248363-1cee1d9e-a88b-4b49-af91-7074c796f146.jpg)

8. Install apache with some library ```sudo apt install mysql-server -y```

9. After that we will create virtual host that allows us to have multiple websites located on a single machine

10. Create the directory for projectlamp and assign ownership for the current user

```sudo mkdir /var/www/projectlamp```
```sudo chown -R $USER:$USER /var/www/projectlamp```

11. create and open a new configuration file in Apache’s sites-available directory using your preferred command-line editor

```
<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
    </VirtualHost>
```

12. use a2ensite command to enable the new virtual host  ```sudo a2ensite projectlamp```

13. reload Apache so these changes take effect ```sudo systemctl reload apache2```

14. create some html file in /var/www/projectlamp/ and check my IP
```http://http://54.251.231.51/:80```

![lamp](https://user-images.githubusercontent.com/55023518/162252302-79e6ca7a-3a4a-4507-b0e2-65f9723b6661.jpg)

15. Enable PHP on the website and serve index.php as first order

```sudo vim /etc/apache2/mods-enabled/dir.conf```

```
<IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>
```


16. Reload Apache2 for apply out new config
```sudo systemctl reload apache2```

17. Create a PHP script to test that PHP is correctly installed and configured on your server
```vim /var/www/projectlamp/index.php```

inside the index.php

```
<?php
phpinfo();
```

18. Verify in your server that index.php in first order
![php](https://user-images.githubusercontent.com/55023518/162253868-1fa1ded4-9c17-49ac-bba8-b9024959a6e4.jpg)



