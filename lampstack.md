# LAMP Stack Setup

This document explains how to set up a LAMP stack on Ubuntu.

## What is a LAMP stack?

LAMP stands for:

- **L**inux - Operating system (Ubuntu)
- **A**pache - Web server
- **M**ySQL - Database management system 
- **P**HP - Scripting language

It is a popular open-source web stack to deploy web applications and websites.

## Installation 

### Step 1 - Install Apache

```bash
sudo apt update
sudo apt install apache2
```

### Step 2 - Install MySQL

```bash
sudo apt install MySQL-server
# Set root password when prompted
```

### Step 3 - Install PHP

```bash 
sudo apt install php libapache2-mod-php PHP-MySQL
```

### Step 4 - Create info.php

To verify PHP is working:

```bash
echo "<?php phpinfo(); ?>" > /var/www/html/info.php
```

## Usage

- Place your PHP application code in `/var/www/html`
- Access it via http://your_server_ip/app_name

### Create VM

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/425e9b9e-44a2-45d7-b285-7b79fe419293">
<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/290185fa-3680-4b03-a01a-60e45bf168bc">


### SSH into VM

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/a6dcde00-140c-442b-934f-fb0d95f0d153">

### Update and upgrade VM OS
azureuser@lampstackimplementation:~$ sudo apt update

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/291ca094-c9dc-4362-a006-0ec0e1da0805">

```bash
sudo apt upgrade
```

### Install Apache and Enable Apache

```bash
sudo apt install apache2
sudo systemctl enable apache2
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/d6580102-a9e0-4412-8875-f6cc23dfcd30">

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/907b23ff-ce59-48ee-86da-1b8770919544">


### Install and enable firewall

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/613fd0b9-175f-4bfe-8c0c-d39a92957889">

```bash
sudo apt install ufw
sudo ufw enable
sudo ufw allow in "Apache Full"
sudo systemctl status apache2
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/2682c2f8-4f23-4f4d-be16-91bae12e2cfa">

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/aced484c-33d2-48cb-9edb-ff3b4d3c6821">

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/99bd6582-d8f0-4603-bf88-8dab4844c8b5">


### Browse to IP address

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/486b0d4e-cf5f-426b-9383-6e5c52787329">


### Install Mysql

```bash
sudo apt install mysql-server
```
<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/d013871a-15f3-457a-bcfb-673d1a4206a8">

### Secure MySQL

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/e4794727-bd85-425d-b308-12ad0296fee6">


### Check SQL status

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/2f5b7e77-db50-487f-8b7c-506a7309e4be">


### Login to SQL server

```bash
sudo mysql -u root
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/07730a20-dadc-48d7-8fe9-2954160847cf">


### Install PHP

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/19dbab0f-ee88-45c5-bcf7-22d31d018789">

```bash
sudo apt install php libapache2-mod-php php-mysql
```

### Install PHP addons

```bash
sudo apt install php-cli php-fpm php-json php-common php-mysql php-zip php-gd php-mbstring php-curl php-xml php-pear php-bcmath
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/ee483db5-827e-430c-82dc-b53a7b9ba46b">


### Install Nano

```bash
sudo apt install nano
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/3191f5d8-c955-448c-820c-7765ce7d3e37">


### Configure Apache to Handle PHP

```bash
sudo nano /etc/apache2/mods-enabled/dir.conf
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/bd084e81-75f8-449e-a774-9141c55a48a4">


### Test the webserver

```bash
sudo nano /var/www/html/info.php
```

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/60aa3ae9-6111-4640-b2a8-2e3ed50035ca">


### Display page in the browser

<img width="452" alt="image" src="https://github.com/kennyanju/lampstack/assets/10983149/ffd4238c-7972-40c4-9098-e376b2efabc4">

