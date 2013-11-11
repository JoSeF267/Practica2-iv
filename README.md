Practica2-iv
============
Mis objetivos para realizar esta practica seran los siguiente
- 1. Instalar debian en un directorio local
- 2. Instalar joomla sobre este directorio
- 3. Ejecutar mi propio modulo de joomla dentro de la maquina

Primero lo que vamos a hacer es montar un sistemas dentro de un directorio especifico:

```
sudo debootstrap --arch=amd64 wheezy /home/josef267/Escritorio/IV/fedora-debian http://ftp.uk.debian.org/debian/

```
Una vez instalado la maquina me dispongo a instalar los paquetes necesarios para poder instalar el joomla.

```
apt-get install apache2
apt-get install mysql-server
apt-get install joe
sudo aptitude install php5 libapache2-mod-php5
```
He tenido que isntalar basntates librerias adiccionales pongo algunos ejemplos:
```
apt-get install php5-mysql php5-curl php5-gd php5-idn php-pear php5-imagick php5-imap php5-mcrypt 
php5-memcache php5-ming php5-ps php5-pspell php5-recode php5-snmp php5-sqlite php5-tidy php5-xmlrpc php5-xsl

```


Con esto ya configurado me dispongo a instalar joomla dentro de la maquina creada.

```
wget http://joomlacode.org/gf/download/frsrelease/17715/77260/Joomla_2.5.8-Stable-Full_Package.tar.bz2
```
Descomprimimos joomla dentro de la carpeta /var/www/

```
tar xvjf Joomla_2.5.8-Stable-Full_Package.tar.bz2
```
Despues de crar la base de datos y instalar joomla ya lo tenemos todo listo:
Para poder acceder a joomla cualquier usuario necesitaremos saber la ip hacemos un ifconfig
```
ifconfig
```
![captura 1] (https://dl.dropbox.com/s/979fibr4dg5u8ci/2.png?m)

Despues podemos ver como he modificado el fichero ports.conf para saber que estoy en la jaula y le he puesto el puerto 9090

![captura 2] (https://dl.dropbox.com/s/nqu9cn8pl8f0s25/5.png)

en la siguiente captura podemos ver ya joomla funcionando

![captura 3] (https://dl.dropbox.com/s/33o42r13axjuvhe/1.png)

Despues de acceder al menu de joomla instalo mi modulo de ejemplo y lo vemos funcionando en la pantalla principal.Llamando a la ip de la maqunina y el puerto 9090 aparecera nuestro joomla

![captura 4] (https://dl.dropbox.com/s/ygisim7sw7cxa1c/6.png)

y con esto ya tendriamos el joomla funcinando en una jaula con acceso a cualquier usuario.
