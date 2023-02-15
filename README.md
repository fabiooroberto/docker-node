# Iniciar o projeto

## Passos

### 1 - Para rodar o projeto tenha o Docker Desktop instalado na máquina.
Execute o seguinte comando na raiz, aonde se encontra o arquivo Dockerfile
``` powershell
docker build -t my-project .
```
Este comando irá criar uma imagem do seu projeto com o Tag my-project

### 2 - Criar um container devivado da imagem

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