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
    - Arrancar un contenedor llamado c2 sobre la imagen mariadb que monte el volumen_datos en la ruta ***/var/lib/mysql*** y cuya contraseña de root sea admin.




3. Parar y borrar el contenedor c2 y tras ello borrar el volumen volumen_datos.
