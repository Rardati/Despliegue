## Instalar y configurar MediaWiki en un entorno debian utilizando Docker Compose. ##

**Crea una página de prueba en tu MediaWiki.**
**Reinicia los contenedores y verifica que los datos persisten**

- Comandos utilizados para docker compose:

- sudo apt update
- sudo apt upgrade
![Paso1.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso1.jpg)

- sudo apt install docker.io docker-compose -y
![Paso2.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso2.jpg)

- docker --version
- docker-compose --version
![Paso3.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso3.jpg)

- mkdir /home/raquel/mediawiki
- cd /home/raquel/mediawiki
![Paso4.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso4.jpg)

- nano docker-compose.yml
![Paso5.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso5.jpg)
![nanoCompose.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/nanoCompose.jpg)

- nano Dockerfile
![Paso6.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso6.jpg)
![nanoDockerfile.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/nanoDockerfile.jpg)


- nano mySqlScript.
![Paso7.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso7.jpg)
![nanoSQL.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/nanoSQL.jpg)


- docker-compose up -d
![Paso8a.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso8a.jpg)

- docker ps ---> Aqui ya me deniega el acceso
![Paso9.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso9.jpg)


- Da error, asi que lo vuelvo hacer con otros comandos.
- sudo docker-compose up -d
![SolErrPaso10.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/SolErrPaso10.jpg)

- sudo usermod -aG docker raquel
![Paso11.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso11.jpg)

- newgrp docker
- docker-compose up -d
- docker ps 
![Paso11a.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso11a.jpg)

- docker-compose down
- docker-compose up -d
![Paso12.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Paso12.jpg)

- docker ps
![Final.jpg](https://github.com/Rardati/Despliegue/blob/main/DockerCompose/DockerCompose/Final.jpg)

