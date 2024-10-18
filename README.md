# sshmount
Script para hacer un montaje sshfs

## Requisitos
Se necesitará tener instalado el paquete ***sshfs***
### Debian:
***apt install sshfs***
### Archlinux:
***pacman -S sshfs***

## Uso
El uso de este script será como sigue:
~~~
sshmount [-p puerto] [usuario@]host
~~~
Este script comprobará la existencia de la carpeta
~~~
$HOME/mnt/host
~~~
Si no existe esta carpeta la crea y nos hará un montaje ssh del $HOME del usuario en el host indicado en la carpeta $HOME/mnt/host
## Características
Este script lee el fichero ***.ssh/config*** y los ficheros *.conf que haya en ***/etc/ssh/ssh-config.d*** y lee si hay alguna entrada del **host** y lee las propiedades de **user**, **port** y  **hostname**
