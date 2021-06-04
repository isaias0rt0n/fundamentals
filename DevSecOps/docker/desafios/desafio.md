## Desafio 01
#### Executar os seguintes containers:
- Nginx
- MySQL
- HTTPD (Apache)
#### Regras:
- Executa-los em modo "Detach" e com nomes "--name"
- Executar os containers nas seguintes portas:
  * Nginx (80:80)   
  * httpd (8080:80)
  * MySQL (3306:3306)
### Dicas:
- Ao executar o container Mysql usar a variável "-e" para:
  * MYSQL_RANDOM_ROOT__PASSWORD=yes

- Executar ```$ docker container logs``` para localizar a senha randômica criada para o container MySQL
- Remover todos os containers ao final do exercicio
  * usar ```$ docker container ls -a``` para verificar

## 🔗[Resolução](https://www.notion.so/estudostack/Resolu-o-Desafios-7be503df8c6e475a8c677c61c167c61a)

## Desafio 02 - Parte 1
#### Baixar as imagens:
- mysql/mysql-server:5.7
- zabbix/zabbix-server-mysql
- zabbix/zabbix-web-nginx-mysql

#### Realizar tag das imagens:
- zabbix/zabbix-server-mysql isaiasorton/zabbix-mysql
- zabbix/zabbix-web-nginx-mysql isaiasorton/zabbix-nginx

## Desafio 02 - Parte 2
#### Iniciar o container mysql-server:
- Declarar o nome mysql-server
- Declarar a variável MYSQL_DATABASE="zabbix"
- Declarar a variável MYSQL_USER="zabbix"
- Declarar a variável MYSQL_PASSWORD="zabbix_pwd"
- Declarar a variável MYSQL_ROOT_PASSWORD="root_pwd"
- Ultilizar a imagem mysql:5.7
- Ultilizar a formatação abaixo:
    * --character-set-server=utf8 --collation-server=utf8_bin

## Desafio 02 - Parte 3
#### iniciar o container zabbix:
- Declarar o nome zabbix
- Declarar a variável DB_SERVER_HOST="mysql-server"
- Declarar a variável MYSQL_DATABASE="zabbix"
- Declarar a variável MYSQL_USER="zabbix"
- Declarar a variável MYSQL_PASSWORD="zabbix_pwd"
- Declarar a variável MYSQL_ROOT_PASSWORD="root_pwd"
- Criar o link para o container mysql-server:mysql
- Expor a porta 10051:10051
- Ultilizar a imagem tag (isaiasorton/zabbix-mysql)

## Desafio 02 - Parte 4
#### iniciar o container nginx:
- Declarar o nome nginx
- Declarar a variável DB_SERVER_HOST="mysql-server"
- Declarar a variável MYSQL_DATABASE="zabbix"
- Declarar a variável MYSQL_USER="zabbix"
- Declarar a variável MYSQL_PASSWORD="zabbix_pwd"
- Declarar a variável MYSQL_ROOT_PASSWORD="root_pwd"
- Criar o link para o container mysql-server:mysql
- Criar o link para o container zabbix
- Expor a porta 80:80
- Ultilizar a imagem tag (isaiasorton/zabbix-nginx)

## Desafio 02 - Parte 5
#### Criar um repositório chamadao treinaweb
- Realizar o upload da imagem isaiasorton/zabbix-mysql
- Realizar o upload da imagem isaiasorton/zabbix-nginx

## Dicas:
- Fazer login no docker hub com o comando ```$ docker login```
- É necessário uma base de dados para executar o Zabbix
- Assegurar que as portas estejam abertas para comunicação

