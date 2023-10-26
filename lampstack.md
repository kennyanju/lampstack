Create VM
<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/425e9b9e-44a2-45d7-b285-7b79fe419293">
<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/290185fa-3680-4b03-a01a-60e45bf168bc">

SSH into vm
<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/73801154-1a8c-4096-980b-7aa6ceb0a09e">

Update and upgrade VM
azureuser@lampstackimplementation:~$ sudo apt update
```
sudo apt upgrade
```
Install Apache and Enable Apache
```
sudo apt install apache2
sudo systemctl enable apache2
```
Install and enable firewall
```
sudo apt install ufw
sudo ufw enable
sudo ufw allow in "Apache Full"
sudo systemctl status apache2
```
Browse to IP address
Install Mysql
```
sudo apt install mysql-server
```
Secure mysql
Check sql status
Login to SQL server
```
sudo mysql -u root
```
Install PHP
```
sudo apt install php libapache2-mod-php php-mysql
```
Install PHP addons
```
sudo apt install php-cli php-fpm php-json php-common php-mysql php-zip php-gd php-mbstring php-curl php-xml php-pear php-bcmath
```
Install Nano
```
sudo apt install nano
```
Configure Apache to Handle PHP
```
sudo nano /etc/apache2/mods-enabled/dir.conf
```
Test the webserver
```
sudo nano /var/www/html/info.php
```
Display page in the browser
