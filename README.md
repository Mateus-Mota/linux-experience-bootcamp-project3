# linux-experience-bootcamp-project3

3° projeto do bootcamp Linux Experience.

<br>

## Objetivo

Implementar uma estrutura de Microsserviços com as melhores práticas do mercado internacional gerando independência entre aplicações e infraestrutura.

<br>

## Tecnologias

- Git
- Php
- Docker
- MySQL
- Nginx

<br>

## Passo a Passo

### Clone o repositório e entre no diretório do projeto
~~~shell
git clone https://github.com/Mateus-Mota/linux-experience-bootcamp-project3.git
cd linux-experience-bootcamp-project3
~~~

<br>

### Coloque o endereço IP do seu servidor de banco de dados no arquivo index.php na linha 17
~~~php
$servername = "0.0.0.0";
~~~

<br>

### :warning: Ainda em desenvolvimento :warning:
### Caso não tenha um servidor de banco de dados disponível, você poderar usar o docker compose para criação do banco de dados e do servidor web
~~~shell
docker-compose up -d
~~~

<br>

### Caso queira iniciar um único containner para o Servidor Web 
~~~shell
docker run --name web-server-php -dt -p 80:80 --mount type=volume,src=app,dst=/app/ webdevops/php-apache:alpine-php7
~~~

<br>

### Caso queria iniciar múltiplos containers para o Servidor Web utilizando o Docker Swarm
~~~shell
docker service create --name web-server-php --replicas 3 -dt -p 80:80 --mount type=volume,src=app,dst=/app/ webdevops/php-apache:alpine-php7
~~~
