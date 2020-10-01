# Lucimar

Lucimar is restaurant management application

## Prerequisites
Make sure you have installed all of the following prerequisites on your development machine:
* Git - [Download & Install Git](https://git-scm.com/downloads). 
* Docker - [Download & Install Docker](https://www.docker.com/products/docker-desktop).

### Cloning The GitHub Repository

```bash
$ git clone https://gitlab.com/decode.repositorio/lucimar.git
```

## Deployment with Docker

Navigate to the project folder

```bash
$ cd lucimar
```

* Deployment with compose:

```bash
$ docker-compose up
```

* Deployment with just Docker:

```bash
$ docker network create lucimar-network
```

```bash
docker image build -t lucimar-db ./db
```

```bash
docker image build -t lucimar-app ./app
```

```bash
docker container run --name lucimar-db --network lucimar-network -d lucimar-db
```

```bash
docker container run --name lucimar-app --network lucimar-network  -p 8080:8080 -d lucimar-app
```
