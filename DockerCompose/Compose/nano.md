version: '3.7'

services:
  db:
    image: mariadb:10.5
    container_name: mediawiki-db
    environment:
      MYSQL_ROOT_PASSWORD: example
      MYSQL_DATABASE: mediawiki
    volumes:
      - mediawiki-db-data:/var/lib/mysql
    networks:
      - mediawiki-net

  mediawiki:
    image: mediawiki:latest
    container_name: mediawiki
    ports:
      - "8080:80"  # Cambia este puerto si 8080 está ocupado
    environment:
      - MEDIAWIKI_DB_HOST=db:3306
      - MEDIAWIKI_DB_NAME=mediawiki
      - MEDIAWIKI_DB_USER=root
      - MEDIAWIKI_DB_PASSWORD=example
    volumes:
      - mediawiki-data:/var/www/html
    networks:
      - mediawiki-net
    depends_on:
      - db

volumes:
  mediawiki-db-data:
  mediawiki-data:

networks:
  mediawiki-net:
    driver: bridge