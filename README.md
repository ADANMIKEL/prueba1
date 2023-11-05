# prueba1
Caso de Automatización con Linux 
1) Iniciar sesión en KillerCoda
2) Levantar un Distro Ubuntu
3) Instalar los requerimientos del Proyecto
   - Git
   - Apache
   - MariaBD
   - PHP
```
apt-get update

sudo apt install git -y

sudo apt install -y mariadb-server
sudo systemctl start mariadb
sudo systemctl enable mariadb

sudo apt install apache2 -y
sudo apt install -y php libapache2-mod-php php-mysql
sudo systemctl start apache2 
sudo systemctl enable apache2 

```
4) Validamos la habilitación del Puerto 80 (Traffic and Ports)
5) Clonamos el repostorio donde se encuentra
```
git clone -b clase2-linux-bash https://github.com/roxsross/bootcamp-devops-2023.git
```
6) Validamos la estructura de Carpertas

```
 ffff  git clone https://github.com/roxsross/The-DevOps-Journey-101.git



-- funciono
mv /var/www/html/index.html /var/www/html/index.html.bkp

cp -r bootcamp-devops-2023/app-295devops-travel/* /var/www/html/

```


sudo systemctl start apache2 

sudo systemctl reload apache2 

ubuntu $ ls
bootcamp-devops-2023  filesystem
ubuntu $ cd ^C
ubuntu $ cd bootcamp-devops-2023
ubuntu $ ls
README.md             app-ecommerce  recursos         vagrant
app-295devops-travel  app-tetris     scripts-example
ubuntu $ cd app-295devops-travel
ubuntu $ ls
README.md  config.php   gallery.php    index.php  logout.php    registration.php  vendor
assets     confirm.php  header-bg.jpg  info.php   packages.php  script.js         videos
book.php   database     images         login.php  pdf.php       style.css
ubuntu $ cd database
ubuntu $ ls
devopstravel.sql
ubuntu $ mysql
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 37
Server version: 10.3.38-MariaDB-0ubuntu0.20.04.1 Ubuntu 20.04

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> CREATE DATABASE devopstravel;
Query OK, 1 row affected (0.000 sec)

MariaDB [(none)]> CREATE USER 'codeuser'@'localhost' IDENTIFIED BY 'codepass';
Query OK, 0 rows affected (0.001 sec)

MariaDB [(none)]> GRANT ALL PRIVILEGES ON *.* TO 'codeuser'@'localhost';
Query OK, 0 rows affected (0.000 sec)

MariaDB [(none)]> 
MariaDB [(none)]> MariaDB [(none)]> 
    -> FLUSH PRIVILEGES;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'MariaDB [(none)]> 
FLUSH PRIVILEGES' at line 1
MariaDB [(none)]> FLUS PRIVILEGES;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'FLUS PRIVILEGES' at line 1
MariaDB [(none)]> FLUSH PRIVILEGES;
Query OK, 0 rows affected (0.000 sec)

MariaDB [(none)]> mysql < devepstravel.sql
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'mysql < devepstravel.sql' at line 1
MariaDB [(none)]> mysql < devepstravel.sql;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version for the right syntax to use near 'mysql < devepstravel.sql' at line 1
MariaDB [(none)]> exit;
Bye
ubuntu $ mysql < devopstravel.sql
ubuntu $ ls
devopstravel.sql
ubuntu $ mysql
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 39
Server version: 10.3.38-MariaDB-0ubuntu0.20.04.1 Ubuntu 20.04

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> use devopstravel;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
MariaDB [devopstravel]> show tables;
+------------------------+
| Tables_in_devopstravel |
+------------------------+
| booking                |
| package                |
| user                   |
+------------------------+
3 rows in set (0.000 sec)

MariaDB [devopstravel]> 
