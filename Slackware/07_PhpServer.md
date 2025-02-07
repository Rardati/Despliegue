## PHP SERVER

**Exercise 7.1 Configuring Apache** 

- sudo apt install apache2
![CInstall.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/CInstall.png)

- sudo apt install php8.2 libapache2-mod-php8.2
![Cinstall2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/Cinstall2.png)

- sudo a2enmod php8.2
![Cinstall3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/Cinstall3.png)

- sudo nano /etc/apache2/apache2.conf 
- sudo nano /etc/apache2/sites-available/000-default.conf 
![ConfNano.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/ConfNano.png)
![nano.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/nano.png)
![NanoModificado.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/NanoModificado.png)


- sudo systemctl restart apache2
![restartApa.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/restartApa.png)

- grep -i "DocumentRoot" /etc/apache2/*
- grep -i "ServerName" /etc/apache2/*
![DocumentServer.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/DocumentServer.png)

**Exercise 7.2 Running Apache**

**Parte 1**

**¿Por qué necesitamos reiniciar httpd cuando hacemos cambios en la configuración?**
El servidor Apache necesita reiniciarse después de modificar su configuración porque:

Apache carga toda su configuración en memoria durante el arranque inicial
Los cambios en los archivos de configuración no se reflejan automáticamente en la memoria
Un reinicio asegura que el proceso lea y aplique la nueva configuración
Es una forma garantizada de aplicar todas las modificaciones simultáneamente

**Parte 2**
**A. ¿Qué hace el comando ps aux? ¿Y el comando grep httpd? ¿Qué significa el símbolo “|”? Entonces, explica qué hace el comando ps aux | grep httpd**


- ps aux: Este comando muestra información sobre todos los procesos que están en ejecución en el sistema. 
- a significa "todos los usuarios", 
- u significa que se mostrará información sobre el usuario que ejecuta el proceso, 
- x indica que se mostrarán procesos que no están asociados a una terminal. 
El resultado incluye detalles como el ID de proceso (PID), el uso de la CPU y la memoria, 
el tiempo de ejecución, entre otros.

- grep httpd: El comando grep busca patrones en un texto o flujo de datos. 
En este caso, busca la cadena de texto httpd en el flujo de datos que recibe como entrada. 
httpd es el nombre del servicio de Apache (servidor web). Este comando filtra las líneas que contienen la palabra httpd.

- | (pipe): El símbolo de barra vertical | es un operador que toma la salida del comando de la izquierda y la pasa como entrada al comando de la derecha. 
En este caso, la salida del comando ps aux se pasa como entrada al comando grep httpd.

Entonces, ps aux | grep httpd: Este comando muestra todos los procesos en ejecución en el sistema y filtra aquellos que contienen la palabra httpd. 
Es útil para ver si el servidor Apache está funcionando.

**B.  ¿Qué esperarías ver como resultado del comando ps aux | grep httpd si httpd está en ejecución? ¿Y si no está en ejecución? Intenta ambos casos y anota los resultados.**

- Si httpd está en ejecución: Verás varias líneas de salida que contienen información sobre el proceso de httpd

- Si httpd no está en ejecución: Si no hay procesos de httpd en ejecución, no verás ninguna salida, 
o solo verás la línea que contiene el propio comando grep, ya que grep también aparecerá en la lista de procesos. 
- ps aux | grep httpd
![grephttp.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/grephttp.png)


**Parte 3**
- ps axl | egrep "httpd|PPID"
![Parte3.jpg](https://github.com/Rardati/Despliegue/blob/main/Slackware/CapApache/Parte3.jpg)


**Exercise 7.3 Creating HTMLfiles**
**¿Qué tienen de especial los archivos index.htm e index.html?**

- Son los archivos predeterminados que Apache carga cuando se accede a un directorio sin especificar un archivo.






**Exercise 7.4 Viewing HTML files using a terminalinterface**


**Exercise 7.5 Creating and viewing PHP files using a terminal interface**


**Exercise 7.6 Exploring and adding an entry to the hosts file**


**Exercise 7.7 Optional exercises**



