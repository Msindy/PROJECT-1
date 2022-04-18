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

`php -v`
![apache running](./images/php%20version.PNG)
