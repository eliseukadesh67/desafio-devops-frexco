# Desafio DevOps
 
## 1. Introdução
 
Nesse desafio, como sugerido, o foco foi no deploy e na infraestrutura, e a aplicação foi totalmente baseada na aplicação básica da documentação do ReactJS.
 
## 2. Como utilizar
 
### Pré-requisitos
 
- docker >= 20.10.10;
- docker-compose >= 1.29.2;
- make >= 4.2.1;
 
### Subindo o container
 
Inicialize a aplicação utilizando o script do Make
 
    make run

Caso queira parar o container e limpar tudo

    make clean
 
Também é possível subir apenas utilizando o docker-compose
 
    docker-compose up --build
 
Veja a aplicação rodando acessando 'http://localhost:80/'
 
## 3. Detalhes da infra-estrutura

Nesta aplicação, as configurações de portas e ambiente foram descritas no Dockerfile e no docker-compose.yml, além disso, foi utilizado uma imagem docker do Nginx para ser usado como proxy e redirecionar requisições realizadas na porta 80 para a porta exposta do container da aplicação.