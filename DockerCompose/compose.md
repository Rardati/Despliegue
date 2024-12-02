## Instalar y configurar MediaWiki en un entorno debian utilizando Docker Compose ##

- Crea una página de prueba en tu MediaWiki.

- Comandos utilizados:


- sudo apt update
- sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
- curl -fsSL https://get.docker.com -o get-docker.sh
- sudo sh get-docker.sh
- sudo usermod -aG docker raquel


- sudo apt install -y python3-pip
- sudo pip3 install docker-compose ----- Aqui me da error 

- Utilizo los siguientes comandos:(C5)




Otros comandos:(C7)
- mkdir /home/raquel/mediawiki-docker
- cd /home/raquel/mediawiki-docker


- nano docker-compose.yml



- sudo docker-compose up -d
- sudo docker ps





- Reinicia los contenedores y verifica que los datos persisten
