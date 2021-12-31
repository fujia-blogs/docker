# docker compose

## 安装

1，window 和 Mac 在安装了 docker desktop 之后，docker-compose 是绑定安装的

```sh
docker-compose -v
# Docker Compose version v2.2.1
```

2，在 Linux 中需要手动安装，建议使用 Python 的 pip 安装，参考：https://github.com/docker/compose/releases

```sh
pip install docker-compose
```

## 使用

1，基本结构

```yml
version: '3.8'

services: # container
  [serviceName]: # service name, also can be used as DNS name in the inner bridge network
    image: [imageName] # image name
    command: [commandList] # optional, if is set, it'll cover default CMD commands in mirror
    environment: # optional, amount to the arguments --env in docker run
    volumes: # optional, amount to the arguments -v in docker run
    networks: # optional, it's equivalent to to the arguments --network in docker run
    ports: # optional, amount to the arguments -p in docker run

volumes: # optional, amount to exec: docker volume create

networks: # optional, amount to exec: docker network create
```

2，需要制定 docker-compose 的版本，它的语法是在不断改进的

## 参考资料

1，语法：https://docs.docker.com/compose/compose-file/
