# LAMP STACK IMPLEMENTATION

## Step 1 : Installing Apache and Updating Firewall

Apache 2 Installed by running

'sudo apt install apache'

![Alt text](<Images/Project 1 Step 1.png>)

Running URL in the brouser

![Alt text](<Images/Project 1 Step 1b.png>)

## Step 2 : Installing MYSQL

Mysql installed by running

'sudo mysql_secure_installation'

![Alt text](<Images/Project 1 step 2 (2).png>)

## Step 3 : Installing PHP 

Running this command

'sudo apt install php libapache2-mod-php php-mysql'

![Alt text](<Images/Project 1 Step 3.png>)

## Step 4 :  Creating a Virtual Host for Your Website Using Apache

Opening a new configuration file in Apache using vi or vim running this command

'sudo vi /etc/apache2/sites-available/projectlamp.conf'

![Alt text](<Images/Project 1 Step 4a.png>)

![Alt text](<Images/Project 1 Step 4b.png>)

## Step 5 : Enabling PHP on the Website 

Created a PHP Script to test that PHP is correctly installed using

'vim /var/www/projectlamp/index.php'

![Alt text](<Images/Project 1 Step 5a.png>)









