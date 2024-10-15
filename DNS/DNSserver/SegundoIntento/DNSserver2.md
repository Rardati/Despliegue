## TAREA DNS SERVER ##

## Comandos Utilizados

-**Comando:** sudo apt update

![1a.jpg](1a.jpg)

-**Comando:** sudo apt upgrade

![1b.jpg](1b.jpg)

-**Comando:** sudo apt install bind9 bind9utils bind9-doc -y

![1c.jpg](1c.jpg)

-**Comando:** sudo systemctl restart networking
-**Comando:** sudo nano /etc/bind/named.conf.options 

![2.jpg](2.jpg)

-**Sin modificar:**

![2a.jpg](2a.jpg)

-**Modificada:**

![2b.jpg](2b.jpg)

-**Comando:** sudo nano /etc/bind/named.conf.options

![3.jpg](3.jpg)
![3a.jpg](3a.jpg)

-**Comando:** sudo cp /etc/bind/db.local /etc/bind/db.prueba.com

![4.jpg](4.jpg)

-**Comando:** sudo nano /etc/bind/db.prueba.com

![5.jpg](5.jpg)

-**Sin modificar:** cambiamos localhost por prueba.com.

![5a.jpg](5a.jpg)

-**Modificada:** lo guardamos y salimos.

![5b.jpg](5b.jpg)


-**Comando:** sudo nano /etc/resolv.conf

![6.jpg](6.jpg)

-**Sin modificar:** cambiamos el nameserver 10.0.2.3 por 10.0.2.15

![6a.jpg](6a.jpg)

-**Modificada:** guardamos y salimos.

![6b.jpg](6b.jpg)

-**Comando:** sudo systemctl restart bind9
-**Comando:** sudo systemctl status bind9

![systemctl.jpg](systemctl.jpg)


-**Comando:** nslookup prueba.com

![7a.jpg](7a.jpg)

-**Comando:** dig @localhost prueba.com
-**Comando:** dig @localhost www.prueba.com

![dig.jpg](dig.jpg)


