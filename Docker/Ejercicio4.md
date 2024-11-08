## EJECUCIÓN DE SERVICIOS DESDE CONTENEDORES ##

-**Comandos Utilizados  para realizar la tarea**

- Arranca un contenedor que ejecute una instancia de la imagen php:7.3-apache, que se llame web y que sea accesible desde tu equipo en el puerto 8181.

Para ello primero he de descargar la imagen
- sudo docker pull php:7.3-apache

![Imagenphp.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio4/Imagenphp.png)

Ejecuta el siguiente comando para crear y arrancar el contenedor:
- sudo docker run --name web -p 8181:80 -d php:7.3-apache
![dockerRun.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio4/dockerRun.png)

Podemos verificar si el contenedor se está ejecutando correctamente con el siguiente comando:
- sudo docker ps
![dockerps.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio4/dockerps.png)

Acceder al contenedor:
- sudo docker exec -it web /bin/bash
![exec.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio4/exec.png)

Crear archivo:
- echo "<h1>HOLA SOY TU NOMBRE Y APELLIDOS</h1>" > /var/www/html/index.html
![echo.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio4/echo.png)


- Colocar en ese mismo directorio raíz un archivo llamado index.php con el siguiente contenido: &lt;?php phpinfo(); ?>




- Arrancar un contenedor que se llame bbdd y que ejecute una instancia de la imagen mariadb para que sea accesible desde el puerto 3336.





- Antes de arrancarlo visitar la página del contenedor en Docker Hub (https://hub.docker.com/_/mariadb) y establecer las variables de entorno necesarias para que:
    - La contraseña de root sea root.
    - Crear una base de datos automáticamente al arrancar que se llame prueba.
    - Crear el usuario invitado con la contraseña invitado.



    