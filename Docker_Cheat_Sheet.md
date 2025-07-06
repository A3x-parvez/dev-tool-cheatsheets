# 🐳 Docker Commands Cheat Sheet

## Getting Started
- **`docker --version`**: Check installed Docker version.
- **`docker info`**: Display Docker system-wide information.
- **`docker help`**: List all available Docker commands.

## Images
- **`docker pull <image>`**: Download an image from Docker Hub.
- **`docker images`**: List all downloaded images.
- **`docker rmi <image_id>`**: Remove an image by ID or name.

## Containers
- **`docker run <image>`**: Run a container from an image.
- **`docker run -it <image>`**: Run container in interactive mode.
- **`docker run -d <image>`**: Run container in detached mode.
- **`docker ps`**: List running containers.
- **`docker ps -a`**: List all containers (including stopped).
- **`docker start <container_id>`**: Start an existing container.
- **`docker stop <container_id>`**: Stop a running container.
- **`docker restart <container_id>`**: Restart a container.
- **`docker rm <container_id>`**: Remove a stopped container.
- **`docker exec -it <container_id> bash`**: Access running container shell.

## Building and Tagging
- **`docker build -t <tagname> .`**: Build an image from a Dockerfile in current directory.
- **`docker tag <image_id> <repo>:<tag>`**: Tag an image for repository.

## Volumes
- **`docker volume create <name>`**: Create a volume.
- **`docker volume ls`**: List all volumes.
- **`docker volume rm <name>`**: Remove a volume.
- **`docker run -v <volume>:/path <image>`**: Mount a volume to a container.

## Networks
- **`docker network ls`**: List all networks.
- **`docker network create <name>`**: Create a new network.
- **`docker network rm <name>`**: Remove a network.

## Logs & Monitoring
- **`docker logs <container_id>`**: Show logs of a container.
- **`docker top <container_id>`**: Display running processes inside container.
- **`docker stats`**: Live container resource usage statistics.

## Clean Up
- **`docker system prune`**: Remove unused data (containers, networks, images).
- **`docker container prune`**: Remove all stopped containers.
- **`docker image prune`**: Remove unused images.

---
