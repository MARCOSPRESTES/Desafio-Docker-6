#DESAFIO DOCKER  :rocket:

##Questão 06 -

Agora vamos aumentar mais a complexidade das coisas, chegou a hora de executaruma aplicação baseada em arquitetura de microsserviços. Essa aplicação é formada por 3 repositórios: Aplicação Web (<https://github.com/KubeDev/rotten-potatoes-ms>), Microsserviço de Filmes (<https://github.com/KubeDev/movie>), Microsserviço de Avaliação (<https://github.com/KubeDev/review>). Montar o ambiente com Docker compose baseado em arquivos de enviroment.*





# Serviço de Reviews

Esse projeto é um serviço de cadastro de reviews. Ele trabalha cadastrando o review de qualquer elemento.

## Estrutura do projeto

Esse projeto trabalha com uma base de dados Postgree 

![Diagrama](./img/diagrama.png)

## Configuração

É preciso determinar a connection string pra que ele acesse o banco de dados Postgree. Isso pode ser feito alterando o arquivo src/Review.Web/appsettings.json ou definindo como variável de ambiente (ConnectionStrings__MyConnection)

Exemplo:

ConnectionStrings__MyConnection: Host=localhost;Database=pguser;Username=pguser;Password=Pg@123;
