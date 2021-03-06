# Starting with Docker

## Executar docker sem o sudo - (Princípio do menor privilégio)
- Adicionando o usuário ao grupo docker
```
$ sudo usermod -aG docker ${USER}
```
- Para aplicar a nova associação ao grupo, saia do servidor e entre novamente
```
$ su - ${USER}
```
- Confirme se o seu usuário foi adicionado ao grupo docker digitando:
```
$ id -nG
```
```
Saída
${USER} sudo docker
```

## Comandos Docker
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
#### Interagingo com container usando bash
```docker
$ docker exec -it <name_container> bash
```
***
#### :link:[Desafio 01](https://github.com/isaias0rt0n/fundamentals/blob/main/DevSecOps/docker/desafios/desafio.md)

## Docker images
#### Histórico de uma imagem (versão e variações)
```
$ docker image history <imagem:version>
```
#### Ver várias informações (low-level) de uma image
```
$ docker image inspect <image:version>
```
#### Baixando image ou repositório de um registro (docker hub)
```
$ docker pull image
```
#### Criando tag que referencia uma image
```
$ docker image tag <TARGET_IMAGE> <SOURCE_IMAGE>
```
#### Fazendo push para um remositório no [docker hub](https://hub.docker.com/)
```
$ docker login
username:
password:
$ docker image push <repositorio>
```
