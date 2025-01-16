## Exercise 3.1 Creating an executable bash script 
**Parte1**

-Capturas:

![Captura1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura1.png)
![Captura2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura2.png)
![Captura3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura3.png)

**Parte2**
No es buena idea utilizar chmod 777 porque da todos los permisos, lectura, escritura y ejecución tanto al usuario como a los grupos.
Eso significa que cualquier persona podría leer, modificar y ejecutar el archivo o el directorio.

Es mejor utilizar chmod 744 porque permite a todos, tanto usuario como grupos leer, pero la parte de escritura y de ejecucion solo podría hacerlo el usuario.
Así el usuario tendría más seguridad con sus archivos y directorios.

## Exercise 3.2 Creating new users 
**username: bob, password: bob**
![Captura4.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura4.jpg)
![Captura4a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura4a.jpg)

**username: smith, password: smith**
![Captura5.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura5.jpg)

## Exercise 3.3 Creating a shared executable script 

**Create a publically readable and writeable directory with the path /home/ncs with the appropriate directory permissions**
![Captura6.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura6.jpg)
![Captura6a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura6a.jpg)

**Create a bash script in this directory called hello.sh which should print a message saying “HelloWorld”**
![Captura7.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura7.jpg)
![Captura7a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura7a.jpg)

**Execute thisscript**
![Captura7b.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura7b.jpg)

**Note down the owner/group ownerships and the file permissions of this script**
![Captura7c.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura7c.jpg)


## Exercise 3.4 Accessing files from different user accounts 
**a) Press [Ctrl] + [Alt] + [F2] and log in as bob**
1. Navigate to the directory /home/ncs. 
Se ve que me salte algún paso anterior, he tenido que volver hacerlo.


![Captura8.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura8.jpg)

2. Execute ./hello.sh. Doesitsucceed? Why (not)?
Funciona porque le puse de permiso chmod 777
![Captura8a.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura8a.jpg)

3. Create a script called bob.sh, which should print the message “Hello this is Bob” when executed.
![Captura8b.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura8b.jpg)


4. Execute ./bob.sh and explain the result you get.
![Captura8c.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura8c.jpg)

Permite ver “Hello this is Bob” porque tiene permiso de ejecucion sobre el script.

**What do you see in this directory?**
![ls-l.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/ls-l.jpg)



**b) Press [Ctrl] + [Alt] + [F3] and log in as smith.**
1. Navigate to the directory /home/ncs. What do you see in this directory?
2. Execute ./hello.sh and ./bob.sh. Explain the results you get.
![Captura9.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/Capturas/Captura9.jpg)

