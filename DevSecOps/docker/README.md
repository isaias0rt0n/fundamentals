# Starting with Docker

#### Iniciando primeito container - (nginx)
```
$ docker container run --publish 80:80 nginx
```
#### Listando todos containers (parados e em execução)
```
$ docker container ls -a
```
#### Criando container apartir de uma imagem - (ngix)
```
$ docker container run --name <nome_nova_image> -d --publish 81:80 nginx
```
#### Parando/Executando um container
```
$ docker container stop <id_container>
```
```
$ docker container start <id_container>
```
#### Baixando uma image do docker pull e adiconar ela na biblioteca - (Apache)
```
$ docker pull httpd
```
#### Monitorando logs de um container 
```
$ docker container logs <name_container>
```
#### Encontrando o processo de um certo container(PID)
```
$ docker container top <name_container>
```
#### Removendo um container
```
$ docker container rm <id_container>
```
