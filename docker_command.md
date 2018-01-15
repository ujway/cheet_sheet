# Docker command cheetsheet

## Overview
Docker, including docker-compse command cheet sheet for everyday use..

## Docker
- `docker run -it -p 8080:8080 --rm -v 'pwd':/src --name test test`
  - `--rm` destroy container after running docker..
  - `--name` provides name.
- `docker exec -it {container_name} bash`
  - allocate tty with bush.
- `docker run -it -p 8080:8080 test-image bash`
  - `-p` port forwarding guest:host IPs.
  - `-i` send a command to container with bash, etc..
  - `-t` connects stdout on container and stdout.
- `docker build --no-cache=true -t test`
  - `-t` provides image name.
  - `--no-cache=true` indicates no cache

## Docker Compose
- `docker-compose build`
  - build images and containers.
  - `--no-cache` option uses no cache.

- `docker-compose pull`
  - pull images defined in docker-compose.yml
- `docker-compose up`
  - start or restart a docker service defined in docker-compose.yml
  - `-d` is a detach option. docker-compose up.
  - `--build` provides with bulding docker image.
- `docker-compose down`
  - stop service removing container and network
  - `-v --rmi all` option indicates removing volumes and docker images.
- `docker-compose exec {container_name} bash`
  - allocate tty with bush
