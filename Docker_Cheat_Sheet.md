# 🐳 Docker Commands Cheat Sheet

---

### 👤 Author: Rijwanool Karim  
🔗 Linkdin - [Rijwanool karim](https://www.linkedin.com/in/rijwanool-karim)  
💻 Github - [A3x-parvez](https://github.com/rijwanoolkarim)

---

## Getting Started
- **`docker --version`**: Check installed Docker version.
- **`docker info`**: Display Docker system-wide information.
- **`docker help`**: List all available Docker commands.

## Images
- **`docker pull <image>`**: Download an image from Docker Hub.
- **`docker images`**: List all downloaded images.
- **`docker rmi <image_id>`**: Remove an image by ID or name.
- **`docker build -t <name>`**: Build image from Dockerfile (tagged with <name>).
- **`docker tag <img_name> <username>/<img_name>:<version>`**: Tag image (e.g., repo/image:tag).

## Containers
- **`docker ps`**: List running containers.
- **`docker ps -a`**: List all containers (including stopped).
- **`docker run <image>`**: Run a container from an image.
- **`docker run -d <image>`**: Run container in detached mode.
- **`docker run -it <image>`**: Run container in interactive mode.
- **`docker run -p 5000:5000 <image>`**: Map container port to host port'
- **`docker start <container_id>`**: Start an existing container.
- **`docker stop <container_id>`**: Stop a running container.
- **`docker restart <container_id>`**: Restart a container.
- **`docker rm <container_id>`**: Remove a stopped container.
- **`docker logs <id>`**: View logs of a container.
- **`docker exec -it <id> sh`**: Access running container (bash/sh shell).
- **`docker exec -it <container_id> bash`**: Access running container shell.

## Building and Tagging
- **`docker build -t <tagname> .`**: Build an image from a Dockerfile in current directory.
- **`docker tag <image_id> <repo>:<tag>`**: Tag an image for repository.

## Volumes
- **`docker volume ls`**: List all volumes.
- **`docker volume create <name>`**: Create a volume.
- **`docker volume rm <name>`**: Remove a volume.
- **`docker volume inspect <name>`**: Inspect volume details.
- **`docker run -v <volume>:/path <image>`**: Mount a volume to a container.

## Networks
- **`docker network ls`**: List all networks.
- **`docker network create <name>`**: Create a new network.
- **`docker network inspect <name>`**: Inspect network details.
- **`docker network connect <net> <id>`**: Connect container to network.
- **`docker network disconnect <net> <id>`**: Disconnect container.
- **`docker network rm <name>`**: Remove a network.

## Logs & Monitoring
- **`docker logs <container_id>`**: Show logs of a container.
- **`docker top <container_id>`**: Display running processes inside container.
- **`docker stats`**: Live container resource usage statistics.

## Clean Up
- **`docker system df`**: Show disk usage.
- **`docker system prune`**: Remove unused data (containers, networks, images).
- **`docker container prune`**: Remove all stopped containers.
- **`docker image prune`**: Remove unused (dangling) images.
- **`docker volume prune`**: Remove unused volumes.

## Docker Compose (Multi-container apps)
- **`docker-compose up`**: Start services from docker-compose.yml.
- **`docker-compose up -d`**: Start in detached mode.
- **`docker-compose down`**: Stop and remove services.
- **`docker-compose ps`**: List containers in Compose project.
- **`docker-compose logs`**: View logs from services.
---
