## INSTALCION DE DOCKER ##

-**COMANDOS UTILIZADOS**

- sudo apt-get update
![PrimerPaso.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio1/PrimerPaso.png)



- sudo apt-get install ca-certificates curl
![SegundoPaso.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio1/SegundoPaso.png)

- sudo install -m 0755 -d /etc/apt/keyrings
- sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
- sudo chmod a+r /etc/apt/keyrings/docker.asc

![Paso3.png](https://github.com/Rardati/Despliegue/blob/main/Docker/Ejercicio1/Paso3.png)

Lo hago en cmd del oredandor:

- sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
![5.png](5.png)



- sudo chmod a+r /etc/apt/keyrings/docker.asc
![daError6.png](daError6.png)

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
![deNuevo7.png](deNuevo7.png)

- sudo apt-get update
![]()

- (. /etc/os-release && echo "$VERSION_CODENAME")


![]()

- sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
![9.png](9.png)



- sudo docker run hello-world
![Final10.png](Final10.png)