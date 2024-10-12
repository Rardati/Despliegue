##Tarea DNS

-**Comandos Utilizados** :

- sudo apt-get install bind9 -> Instalamos bind9 

![InstalacionBind9.jpg](InstalacionBind9.jpg)

- sudo mkdir /etc/bind/zones -> Crear directorio

![mkdir.jpg](mkdir.jpg)

- sudo systemctl status bind9 -> Comprobar que está bien creado.
- sudo cd /etc/bind -> Ir al directorio
![doscomandos.jpg](doscomandos.jpg)

- sudo apt-get install tree 
![installtree.jpg](installtree.jpg)

-  tree
![tree.jpg](tree.jpg)

- sudo cp db.local /etc/bind/zones/prueba.com.zone
![cpdblocal.jpg](cpdblocal.jpg)

- sudo nano /etc/bind/named.conf.local 
![archivo.jpg](archivo.jpg)

- sudo nano /etc/bind/zones/prueba.com.zone
![nanocambiado.jpg](nanocambiado.jpg)

- sudo systemctl restart bind9
- dig @localhost prueba.com
![final.jpg](final.jpg)

Todo esto es siguiendo el video.


