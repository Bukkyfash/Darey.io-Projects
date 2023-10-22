# Web Stack Implementationm(LEMP Stack)

Launching Git Bash With the following command

`ssh -i <Your-private-key.pem> ubuntu@<EC2-Public-IP-address>`

![Alt text](<Images/Project 2 Step 0.png>)

## Step 1: Installing the Nginx Server

We need to update our server package index and install Ngnix using these commands

`$ sudo apt update`
`$ sudo apt install nginx`

When prompted, enter `Y` to confirm you want to install Nginx

![Alt text](<Images/Project 2 step 1a.png>)

![Alt text](<Images/Project 2 Step 1b.png>)

## Step 2: Installing MySQL 

To install, log in as root user and run a security script that comes pre-installed with MySQL and Exit MySQL, use the following commands

`$ sudo apt install mysql-server`

`$ sudo mysql`

`ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

`mysql> exit`

![Alt text](<Images/Project 2 Step 2a.png>)

![Alt text](<Images/Project 2 Step 2c.png>)

![Alt text](<Images/Project 2 Step 2b.png>)

## Step 3: Installing PHP

Run this command to install PHP

`$ sudo apt install php-fpm php-mysql`

Press `Y` and `Enter` when prompted

![Alt text](<Images/Project 2 Step 3a.png>)

## Step 4: Configuring Nginx to Use PHP Processor

When configuring Nginx to use PHP Processor, you will use commands like

`$ sudo mkdir /var/www/projectLEMP`

`$ sudo chown -R $USER:$USER /var/www/projectLEMP`

`#/etc/nginx/sites-available/projectLEMP`

`$ sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/`

`$ sudo nginx -t`

`sudo unlink /etc/nginx/sites-enabled/default`
`
`$ sudo systemctl reload nginx`

`sudo echo 'Hello LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectLEMP/index.html`

Then, go to your browser and open your websit URL using IP address

![Alt text](<Images/Project 2 Step 4a.png>)

![Alt text](<Images/Project 2 step 4b.png>)

## Step 5: Testing PHP with Ngnix

Use the commands below

Open a New file called `info.php` using your text editor with this command

`$ nano /var/www/projectLEMP/info.php`
write the lines below in your file

`<?php
phpinfo();`

Paste `http://server_domain_or_IP`/info.php` in your browser to see the PHP page

![Alt text](<Images/Project 2 Step 5.png>)

## Step 6: Retrieving data from MySQL database with PHP

We we create a database named "example_database" and a user named "example_user", before doing that, we will connect to our MySQL console using the root command

`$ sudo mysql`

Create a new database by running the following commands in the MySQL console

`mysql> CREATE DATABASE `example_database`;`

Create a new user with full privileges on the database created using this command

`mysql>  CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';`

`mysql> GRANT ALL ON example_database.* TO 'example_user'@'%';`

Exit MySQL shell with this command

`mysql> exit`

Run `mysql> SHOW DATABASES;`

![Alt text](<Images/Project 2 Step 6a.png>)

To create a Todo_list from the MySQL console, run

`CREATE TABLE example_database.todo_list (item_id INT AUTO_INCREMENT,content VARCHAR(255),PRIMARY KEY(item_id));`

Insert a few rows of content in the test table

`mysql> INSERT INTO example_database.todo_list (content) VALUES ("My first important item");`

![Alt text](<Images/Project 2 step 6b.png>)

![Alt text](<Images/Project 2 Step 6c.png>)

Exit MySQL using `mysql> exit`

Create a PHP script that will connect to MYSQL and query for your content, creat a new PHP file using this text editor command

`$ nano /var/www/projectLEMP/todo_list.php`

copy some texts into the todo_list.php, save and close when done

Now access this page in your web browser by visiting the domain name or public IP address configured for your website, followed by `/todo_list.php:`

`http://<Public_domain_or_IP>/todo_list.php`

![Alt text](<Images/Project 2 Step 6d.png>)


















