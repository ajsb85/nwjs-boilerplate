## NW.js Boilerplate

#### Canaima Popular 4.1

Corriendo NW.js en Canaima nos da el error de la librería en C

Para solucionar este problema debemos añadir unos repositorios experimentales y hacer una actualización de la librería libc.so.6. Primero abrimos una terminal y editamos los repositorios

  # sudo nano /etc/apt/sources.list

deb http://ftp.debian.org/debian experimental main
deb http://ftp.debian.org/debian sid main

Este repositorio lo tendremos de forma temporal hasta que hagamos la actualización.

sudo apt-get update

Ahora hacemos la actulizacion de la libreria libc.so.6

sudo apt-get -t experimental install libc6-dev

Por ultimo eliminamos los repositorios agregados y ejecutamos ./nw
