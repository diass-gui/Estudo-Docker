# Anotações sobre estudos - Docker

Repositório criado para armazenar estudos e práticas relacionadas ao **Docker** e **Docker Compose**.

Durante os estudos, foram trabalhados conceitos como:

* Criação de imagens através de `Dockerfile`;
* Criação e execução de containers;
* Utilização de variáveis de ambiente;
* Portas e redes;
* Criação de imagens personalizadas;
* Publicação de imagens no Docker Hub;
* Utilização do Docker Compose.

## Como executar o Dockerfile

O projeto Node.js utilizado para os estudos está localizado em:

```text
exemplo-estudo-docker/
```

### 1. Criar a imagem

A partir da raiz do projeto, execute:

```bash
docker build -t app-node-estudo-docker:1.0 ./exemplo-estudo-docker
```

### 2. Executar o container

Depois de criar a imagem:

```bash
docker run -d --name app-node-estudo-docker -p 3000:6000 app-node-estudo-docker:1.0
```

A aplicação poderá ser acessada em:

```text
http://localhost:3000
```

### 3. Parar e remover o container

Para parar:

```bash
docker stop app-node-estudo-docker
```

Para remover:

```bash
docker rm app-node-estudo-docker
```

---

## Como executar com Docker Compose

O arquivo `docker-compose.yml` está localizado em:

```text
ymls/docker-compose.yml
```

Entre na pasta:

```bash
cd ymls
```

### 1. Subir o projeto

Execute:

```bash
docker compose up -d
```

O Compose utilizará a imagem definida no arquivo:

```text
bigasgui20/app-node-estudo-docker:1.0
```

A aplicação ficará disponível em:

```text
http://localhost:3000
```

### 2. Parar os containers

Para parar os serviços:

```bash
docker compose down
```
