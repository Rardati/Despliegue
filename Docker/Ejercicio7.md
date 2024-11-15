## VOLÚMENES ##

Iniciamos aqui el tema de la persistencia de datos:

1. Crear los siguientes volúmenes con la orden docker volume: volumen_datos y volumen_web
Usamos los comandos:
- sudo docker volume create volumen_datos
![volume1.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio7/volume1.png)

- sudo docker volume create volumen_web
![volume2.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio7/volume2.png)


2. Una vez creados estos contenedores:
    - Arrancar un contenedor llamado c1 sobre la imagen php:7.4-apache que monte el volumen_web en la ruta ***/var/www/html***
    - Contenedor c1 (PHP/Apache):  Comando utilizado 
    - sudo docker run -d --name c1 \
        -p 8080:80 \
        -v volumen_web:/var/www/html \
        php:7.4-apache

![c1.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio7/c1.png)    



2. (b) Arrancar un contenedor llamado c2 sobre la imagen mariadb que monte el volumen_datos en la ruta ***/var/lib/mysql*** y cuya contraseña de root sea admin.
    - Contenedor c2 (MariaDB): Comando utilizado
    - sudo docker run -d --name c2 \
        -e MYSQL_ROOT_PASSWORD=admin \
        -v volumen_datos:/var/lib/mysql \
        mariadb

![c2.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio7/c2.png)           




3. Parar y borrar el contenedor c2 y tras ello borrar el volumen volumen_datos.
- Parar el contenedor c2:  sudo docker stop c2
- Eliminar el contenedor c2: sudo docker rm c2
- Eliminar el volumen volumen_datos: sudo docker volume rm volumen_datos

![Paso3.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio7/Paso3.png)

