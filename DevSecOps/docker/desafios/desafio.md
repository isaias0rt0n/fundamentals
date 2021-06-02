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
### Dicas:
- Ao executar o container Mysql usar a variável "-e" para:
  * MYSQL_RANDOM_ROOT__PASSWORD=yes

- Executar ```$ docker container logs``` para localizar a senha randômica criada para o container MySQL
- Remover todos os containers ao final do exercicio
  * usar ```$ docker container ls -a``` para verificar
