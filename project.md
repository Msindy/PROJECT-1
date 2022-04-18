# LAMP STACK IMPLEMENTATION DOCUMENTATION
## **Install Apache**

`sudo apt update`

![update packages](./images/update%20packages%20.PNG)


`sudo apt install apache2`

![install apache](./images/install%20apache2.PNG)

![install successful](./images/install%20successful.PNG)

`sudo systemctl status apache2`

![apache running](./images/apache%20running%20confirmed.PNG)

*http://54.147.77.70/*

![apache running](./images/Apache%20web%20server%20over%20the%20internet.PNG)


## **Installing MYSQL**

`sudo apt install mysql-server`
![apache running](./images/SQL%20installation.PNG)

![apache running](./images/SQL%20installation%20successful.PNG)


`sudo mysql_secure_installation`
![apache running](./images/security%20script.PNG)

![apache running](./images/sql%20password%20validation.PNG)

`mysql>exit`
![apache running](./images/sql%20exit.PNG)


## **Installing PHP**

`sudo apt install php libapache2-mod-php php-mysql`
![apache running](./images/php%20installation.PNG)

![apache running](./images/php%20installation%20successful.PNG)

`php -v `
![apache running](./images/php%20version.PNG)

## **Creating a Virtual Host**

`sudo mkdir /var/www/projectlamp`

![apache running](./images/CREATING%20A%20VIRTUAL%20HOST.PNG)

 `sudo chown -R $USER:$USER /var/www/projectlamp`
 `sudo vi /etc/apache2/sites-available/projectlamp.conf`
 `<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>`

![apache running](./images/bare%20bone%20config.PNG)

1.Hit the esc button on the keyboard

2.Type :

3.Type wq. w for write and q for quit

4.Hit ENTER to save the file

`sudo ls /etc/apache2/sites-available`

`sudo a2ensite projectlamp`

`sudo a2dissite 000-default`

`sudo apache2ctl configtest`

`sudo systemctl reload apache2`

`sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`

*Output from ip address*
![apache running](./images/website%20ip%20url.PNG)


*Output from public dns address*
![apache running](./images/public%20dns.PNG)