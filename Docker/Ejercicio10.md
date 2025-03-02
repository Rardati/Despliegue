## DOCKERFILE ##

## 1a Parte

1. Arrancar un contenedor sobre la imagen ubuntu:20.04 y sobre él realizar las siguientes operaciones:

    - Instalación del editor nano (apt install nano).
    - Instalación del editor vim (apt install vim).
    - Instalación de las herramientas de red (apt install inetutils-tools).
    - Instalación de las herramientas dns (apt install dnsutils).
    - Creación del usuario usuario con contraseña usuario (adduser usuario)


- Comandos utilizados:
    - sudo docker run -it --name ubuntu_container ubuntu:20.04 /bin/bash

![Paso1a.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso1a.png)

Una vez dentro del contenedor, actualizamos los paquetes: 
- apt update && apt upgrade -y

![Paso1b.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso1b.png)

Ahora instalamos los paquetes requeridos: 
- apt install nano vim inetutils-tools dnsutils -y
![Paso1c.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso1c.png)



Instalamos el paquete adduser y luego creamos el usuario:
- apt install adduser -y
- adduser usuario

![Paso1d.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso1d.png)






2. Tras realizar dichas instalaciones y utilizando la orden docker commit crear una imagen que se llame de la siguiente manera: TuNombreUsuarioDockerHub/a61 y subirla a DockerHub utilizanzo la orden docker push. Recordad que antes tendréis que hacer docker login.

- Comandos utilizados:
- sudo docker login
![Paso2a.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso2a.png)


- sudo docker commit ubuntu_container rardati/a61
- sudo docker push rardati/a61
![Paso2b.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso2b.png)



-  Como nos da error repetimos el proceso.Comandos Utilizados
- sudo groupadd docker
- sudo usermod -aG docker raquel
- newgrp docker
- docker push rardati/a61:2.0

![Paso2c.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Paso2c.png)



## 2a Parte

1. Partiendo de la imagen php:7.4-apache construir un Dockerfile que realice lo siguiente:
    - Instalar nano (apt install -y nano)
    - Instalar git (apt install -y git)
    - Colocar en el directorio raíz del servidor apache (/var/www/html) dos ficheros:
        - index.html que contenga HOLA SOY XXXXXX sustituyendo XXXXX por tu nombre
        - info.php que contengo el siguiente código &lt;? php phpinfo(); ?>



- Descargamos la imagen
![Imagenphp.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/Imagenphp.png)

- mkdir imagen-php
- cd imagen-php

![imagen1.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/imagen1.png)


- nano Dockerfile:

![nano.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/nano.png)




2. Una vez creado dicho Dockerfile construir la imagen, que se deberá llamar TuNombreUsarioDockerHub/a62.

- docker build -t rardati/a62 .


![dockerbuild.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/dockerbuild.png)

- docker images


![dockerImages.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/dockerImages.png)

- docker Login


![DLogin.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/DLogin.png)

- docker push rardati/a62


![push.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio10/push.png)