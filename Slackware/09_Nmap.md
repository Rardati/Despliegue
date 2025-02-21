## Nmap 

Primero instalaremos los paquetes que nos hacen falta

- Nmap
![Captura1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Captura1.png)

- Router (net-tools)
![Captura2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Captura2.png)

- Finger
![CapturaFinger.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/CapturaFinger.png)


**Exercise 9.1**

![Captura3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Captura3.png)
![nano1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/nano1.png)
![Captura6.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Captura6.png)




**Exercise 10.1 User and system information**

- Parte 1, ¿Cuántos intentos de inicio de sesión (exitosos y fallidos) ocurrieron en las últimas 48 horas?
- Usar el comando last para obtener los registros de inicio de sesión -> last -x | grep -E 'still logged in|shutdown'
![CapturaParte1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/CapturaParte1.png)

- Parte 2, ¿Cuántos reinicios del sistema ocurrieron en las últimas 48 horas?
- Ver los reinicios -> last reboot
![CapturaParte2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/CapturaParte2.png)




**Exercise 10.2 Symbolic and hard links**

- Parte 1
![Parte1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte1.png)
![Parte1a.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte1a.png)



- Parte 2:
- Se puede ver el contenido del archivo.
![Parte2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte2.png)

Se puede ver el contenido del archivo.


-Parte 3
![Parte3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte3.png)
Cuando mueves extra_file, el enlace simbólico extra_file_link se rompe.


![Parte3a.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte3a.png)
Cuando mueves extra_file de vuelta a su ubicación original, el enlace simbólico extra_file_link comienza a funcionar nuevamente, 
mostrando el contenido del archivo como antes.

- Parte 4
![Parte4.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte4.png)
El archivo extra_file no se ve afectado al eliminar el enlace simbólico. 
El archivo original sigue existiendo y se puede ver sin problemas. El enlace simbólico solo es un "acceso directo", no afecta al archivo original.


- Parte 5
![Parte5.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte5.png)
Apunta a un archivo que ya no existe, por lo que cuando intentas abrirlo con cat, dice que el fichero no existe.


- Parte 6
![Parte6.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte6.png)
![Parte6b.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/Nmap/Parte6b.png)


