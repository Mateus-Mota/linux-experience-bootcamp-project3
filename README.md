# linux-experience-bootcamp-project3

3° projeto do bootcamp Linux Experience.

## Objetivo

Implementar uma estrutura de Microsserviços com as melhores práticas do mercado internacional gerando independência entre aplicações e infraestrutura.

<br>

## Passo a Passo

## Caso queira rodar um único containner
~~~shell
docker run --name web-server -dt -p 80:80 --mount type=volume,src=app,dst=/app/ webdevops/php-apache:alpine-php7
~~~

## Caso queria inciar múltiplos containners com Docker Swarm
~~~shell
docker service create --name web-server --replicas 3 -dt -p 80:80 --mount type=volume,src=app,dst=/app/ webdevops/php-apache:alpine-php7
~~~
