## BIND MOUNTS ##

Seguimos con el tema de la persistencia de datos:

1. Crea una carpeta llamada saludo y dentro de ella crea un fichero llamado index.html con el siguiente contenido:
&lt;h1>HOLA SOY XXXXXX&lt;/h1>. Deberás sustituir ese XXXXX por tu nombre.
- Comandos utilizados: 
- Crear la carpeta "saludo": sudo mkdir saludo
- Crear el archivo index.html: sudo touch saludo/index.html

![Paso1.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso1.png)


- Editar el contenido del archivo index.html: sudo nano saludo/index.html ---- <h1>HOLA SOY TU_NOMBRE_AQUÍ</h1>
![Paso1b.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso1b.png)

- Ver si se ha creado: sudo cat saludo/index.html
![Paso1c.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso1c.png)
![Paso1Final.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso1Final.png)



2. Una vez hecho esto arrancar dos contenedores basados en la imagen php:7.4-apache que hagan un **bind mount** de la carpeta saludo en la carpeta /var/www/html del contenedor.
- usamos el comando:sudo docker run -d --name c2 -p 8181:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache
- usuamos el comando: sudo docker run -d --name c3 -p 8282:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache
![Paso2.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso2.png)


- Me daba algun que otro conflicto, pero al final funciona
![Paso3.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso3.png)
![Paso3b.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio8/Paso3b.png)


