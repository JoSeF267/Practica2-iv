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

```
Con esto ya configurado me dispongo a instalar joomla dentro de la maquina creada.
