# Docker no linux

## Instalação 
```powershell
sudo apt install docker.io docker-compose
```

## Iniciar junto com o sistema
```powershell
sudo systemctl enable --now docker ocker.socker containerd
```

## Helper
```powershell
docker --help
```
-- Iniciar o ambiente em modo admin do usuário
sudo su

-- Baixar ultima imagem do wordpress do dockerhub
docker pull wordpress

-- Listar todas as images baixadas no sistema
docker images

-- Container é uma imagem em execução

-- Name (Nome do container que será criado) wordpress (indica qual imagem está sendo usada para criar o container)
docker run --name meu_wordpress -p 8080:80 -d wordpress

-- Imagem do ubuntu
docker pull ubuntu

-- -it (interativo com o terminal)
docker run -it ubuntu

docker stop 81c4 (inicias do Id do container)
docker start 81c4
docker restart 81c4
docker rm 81c4
-- remover uma imagem
docker rmi ubuntu

-- c# (Criar imagem baseada no dockerfile)
docker build -t docker-aspnet-yb -f DockerAspNet.API/Dockerfile .
-- criar container baseado na imagem
docker run -d -p 5000:80 docker-demo-yb docker-aspnet-yb


# Iniciar o projeto

## Passos

### 1 - Para rodar o projeto tenha o Docker Desktop instalado na máquina.
Execute o seguinte comando na raiz, aonde se encontra o arquivo Dockerfile
``` powershell
docker build -t my-project .
```
Este comando irá criar uma imagem do seu projeto com o Tag my-project

### 2 - Criar um container derivado da imagem

``` powershell
docker run -d -p 3000:3000 -n project-docker my-project
```

-d => irá rodar o container desacoplado do terminal

-p => vai rodar na porta 3000 e expor a porta 3000 definida no arquivo index.js

-n => será o nome do container

### Verificar se o container foi iniciado.

``` powershell
docker ps
```
