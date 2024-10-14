##Tarea DNS

-**Comandos Utilizados** :

Siguiendo el video:

- sudo apt-get install bind9 -> Instalamos bind9 

![InstalacionBind9.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\InstalacionBind9.jpg)

- sudo mkdir /etc/bind/zones -> Crear directorio

![mkdir.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\mkdir.jpg)

- sudo systemctl status bind9 -> Comprobar que está bien creado.
- sudo cd /etc/bind -> Ir al directorio
![doscomandos.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\doscomandos.jpg)

- sudo apt-get install tree 
![installtree.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\installtree.jpg)

-  tree
![tree.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\tree.jpg)

- sudo cp db.local /etc/bind/zones/prueba.com.zone
![cpdblocal.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\cpdblocal.jpg)

- sudo nano /etc/bind/named.conf.local 
![archivo.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\archivo.jpg)

- sudo nano /etc/bind/zones/prueba.com.zone
![nanocambiado.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\nanocambiado.jpg)

- sudo systemctl restart bind9
- dig @localhost prueba.com
![final.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\final.jpg)




Ahora siguiendo los apuntes:

- sudo nano /etc/bind/named.conf.options
![1.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\1.jpg)
![1cambiado.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\1cambiado.jpg)


- sudo nano /etc/bind/named.conf.local
![local.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\local.jpg)

- sudo cp /etc/bind/db.local /etc/bind/db.prueba.com
![cp.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\cp.jpg)

- sudo nano /etc/bind/db.prueba.com
![nano2.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\nano2.jpg)
![nano2cambiado.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\nano2cambiado.jpg)

- sudo nano /etc/resolv.conf
![resolv.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\resolv.jpg)

- sudo systemctl restart bind9
- dig @localhost prueba.com
![dig.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\dig.jpg)

- nslookup prueba.com localhost
- nslookup prueba.com 10.0.2.15
![nslookup.jpg](C:\Users\Raquel\Documents\GitHub\Despliegue\DNS\DNSserver\Imagen\nslookup.jpg)