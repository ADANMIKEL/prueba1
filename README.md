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
