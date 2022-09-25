## How To Set Up Password Authentication with Apache on Ubuntu 14.04, 16.04 & 18.04

### Prerequisites

I followed this [guide](https://www.digitalocean.com/community/tutorials/how-to-set-up-password-authentication-with-apache-on-ubuntu-16-04) for my Ubuntu 18.04 server and opted the virtual host method (there are two methods to setup Apache auth, one is Virtual Host Definition and other one requires `.htaccess` file), I opted the first one namely the **Virtual Host Definition.** I followed the guide but config file in the guide didn’t worked for me so I had to improvise :). This is my config file that worked for me.

<VirtualHost \*:80>  
     ServerAdmin <your-admin>  
     DocumentRoot <your-root>  
     ServerName <your-server-name>

<Directory project-root-directory-path/>  
        Options +FollowSymlinks  
        AllowOverride All  
        Require all granted  
     </Directory>

<Directory "project-root-directory-path">  
        AuthType Basic  
        AuthName "Restricted Content"  
        AuthUserFile /etc/apache2/.htpasswd  
        Require valid-user  
 </Directory>

</VirtualHost>

Checkout this [link](https://websiteforstudents.com/protect-directories-with-apache2-http-basic-authentication-on-ubuntu-16-04-lts/) for more.