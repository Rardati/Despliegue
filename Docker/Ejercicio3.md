## ARRANCAR UN CONTENEDOR ##

-**Comandos Utilizados para esta actividad**

## Arrancar el contenedor:
- sudo docker run-it --name ubuntu ubunto:18.04
Para salir de él presionando Ctrl + D.

![arrancar1.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio3/Arrancar1.png)

## Comprobar que se ha parado:
-  sudo docker run-it --name ubuntu ubunto:18.04
- sudo docker ps -a

![2.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio3/2.png)


## Rearrancar el contenedor:
- sudo docker start ubuntu

![3.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio3/3.png)


## Comprobar que el contenedor está funcionando:
- sudo docker ps

![4.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio3/4.png)


## Mostrar el fichero /etc/os-release sin entrar en el contenedor:
-sudo docker exec ubuntu cat 7etc/os-release

![5.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio3/5.png)