# Docker Lamp Stack

## Para que foi criado este stack?

Criei este stack porque precisava de ter um container php:7.2-apache para fazer um curso de reciclagem em php7 com as seguintes libs:

* gd
* mcrypt
* mysqli

Para facilitar e criar um Lamp completo adicionei mais dois containers que são:

* mysql:5.7
* phpmyadmin:latest

## Ficheiros

Criei três ficheiros para poder correr o stack que são eles:

- Dockerfile = Serve para gerar um novo container com as alterações que quero.
- docker-composer.yml = para fazer o build e correr o container criado
- ./compose/docker-compose.yml = Ficheiro com as configurações para correr o apache com php, mysql e phpmyadmin.

** para correr o buid tem que executar o comando:

' docker-compose -f "docke-compose.yml" -d --build
' que ele cria a imagem personalizada, depois e só dar o comando 'docker-compose down' para parar os containers.

Depois basta substituir o ficheiro docker-composer.yml pelo que está na pasta ./compose/ e eliminar do Dockerfile

E executar sempre o 'docker-compose up -d' e o stack vai rodar sempre com os 3 containers.
