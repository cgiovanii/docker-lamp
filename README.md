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

Criei três ficheiros para poder correr o stack:

- Dockerfile = Serve para gerar um novo container com as alterações que necessito.
- docker-composer.yml = para fazer o build e correr o container.
- ./compose/docker-compose.yml = Ficheiro com as configurações para correr o Lamp (apache, php, mysql e phpmyadmin).

#### Para correr o buid tem que executar o comando:

`$ docker-compose -f "docke-compose.yml" -d --build`

O Docker criará um container php7.2-apache personalizado com as libs que faltavam, e depois é só executar o comando `$ docker-compose down` para parar os containers.

Depois basta substituir o ficheiro **docker-composer.yml** pelo que está na pasta **./compose/** e eliminar do **Dockerfile.**

Sempre que executar o comando `$ docker-compose up -d` o stack vai rodar com os 3 containers.
