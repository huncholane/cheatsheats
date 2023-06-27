# Docker Cheat Sheet

## Table of Contents
- [Basic Commands](#basic-commands)
- [Images](#images)
- [Containers](#containers)
- [Volumes](#volumes)
- [Networking](#networking)
- [Docker Compose](#docker-compose)
- [Dockerfile](#dockerfile)
- [Miscellaneous](#miscellaneous)

## Basic Commands

### Build an image
```bash
docker build -t <image_name> .
```

### Run a container
```bash
docker run <image_name>
```

### List running containers
```bash
docker ps
```

### Stop a running container
```bash
docker stop <container_id>
```

### Remove a container
```bash
docker rm <container_id>
```

### List Docker images
```bash
docker images
```

### Remove an image
```bash
docker rmi <image_id>
```

## Images

### Pull an image from Docker Hub
```bash
docker pull <image_name>
```

### Push an image to Docker Hub
```bash
docker push <image_name>
```

### Tag an image
```bash
docker tag <source_image> <target_image>
```

## Containers

### Start a stopped container
```bash
docker start <container_id>
```

### Attach to a running container
```bash
docker attach <container_id>
```

### Execute a command in a running container
```bash
docker exec <container_id> <command>
```

### Copy files between host and container
```bash
docker cp <source_path> <container_id>:<target_path>
docker cp <container_id>:<source_path> <target_path>
```

### Inspect container details
```bash
docker inspect <container_id>
```

## Volumes

### Create a named volume
```bash
docker volume create <volume_name>
```

### Mount a volume in a container
```bash
docker run -v <volume_name>:<container_path> <image_name>
```

### Mount a host directory in a container
```bash
docker run -v <host_path>:<container_path> <image_name>
```

### List Docker volumes
```bash
docker volume ls
```

### Remove a volume
```bash
docker volume rm <volume_name>
```

## Networking

### Create a user-defined network
```bash
docker network create <network_name>
```

### Run a container on a specific network
```bash
docker run --network <network_name> <image_name>
```

### Connect a container to a network
```bash
docker network connect <network_name> <container_name>
```

### Disconnect a container from a network
```bash
docker network disconnect <network_name> <container_name>
```

### List Docker networks
```bash
docker network ls
```

## Docker Compose

### Start services defined in a Compose file
```bash
docker-compose up
```

### Start services in the background
```bash
docker-compose up -d
```

### Stop services defined in a Compose file
```bash
docker-compose down
```

### Scale services
```bash
docker-compose up --scale <service_name>=<count>
```

## Dockerfile

### Specify a base image
```Dockerfile
FROM <base_image>
```

### Set the working directory
```Dockerfile
WORKDIR /app
```

### Copy files to the image
```Dockerfile
COPY <source_path> <target_path>
```



### Run commands in the image
```Dockerfile
RUN <command>
```

### Expose a port
```Dockerfile
EXPOSE <port>
```

## Miscellaneous

### Monitor resource usage of containers
```bash
docker stats
```

### Remove all stopped containers
```bash
docker container prune
```

### Remove all unused images
```bash
docker image prune
```

### Remove all unused volumes
```bash
docker volume prune
```

### Remove all unused networks
```bash
docker network prune
```

### View logs of a container
```bash
docker logs <container_id>
```

### Clean up Docker resources
```bash
docker system prune
```

```
