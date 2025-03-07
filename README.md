# 🐳 Docker Cheatsheet 🐳

## 🔹 Basic Commands
```sh
docker --version                  # Check Docker version
docker info                        # Display system-wide information
docker help                        # List all commands
docker COMMAND --help              # Get help for a specific command
```

---

## 🔹 Container Management
```sh
docker ps                          # List running containers
docker ps -a                       # List all containers (including stopped ones)
docker start <container_id>        # Start a stopped container
docker stop <container_id>         # Stop a running container
docker restart <container_id>      # Restart a container
docker rm <container_id>           # Remove a stopped container
docker logs <container_id>         # Show container logs
docker inspect <container_id>      # Show container details
docker exec -it <container_id> bash  # Access container shell
```

---

## 🔹 Image Management
```sh
docker images                      # List available images
docker pull <image_name>           # Download an image from Docker Hub
docker build -t <image_name> .     # Build an image from Dockerfile
docker rmi <image_id>              # Remove an image
docker tag <image> <new_image>     # Rename/tag an image
docker history <image_id>          # Show image history
```

---

## 🔹 Running Containers
```sh
docker run -it <image_name> bash   # Run a container interactively
docker run -d <image_name>         # Run a container in detached mode
docker run -p 8080:80 <image>      # Run container and expose ports (host:container)
docker run --name <name> <image>   # Run with a specific name
docker run --rm <image>            # Run and remove container after exit
```

---

## 🔹 Docker Compose
```sh
docker-compose up -d               # Start services in the background
docker-compose down                # Stop and remove containers
docker-compose build               # Build/rebuild services
docker-compose ps                  # List running services
docker-compose logs -f              # View logs
```

---

## 🔹 Volumes & Networks
```sh
docker volume ls                   # List volumes
docker volume rm <volume_name>      # Remove a volume
docker network ls                   # List networks
docker network inspect <network>    # Inspect a network
docker network rm <network_name>    # Remove a network
```

---

## 🔹 Cleanup Unused Data
```sh
docker system prune                 # Remove all unused containers, networks, and images
docker system prune -a               # Remove all unused images as well
docker volume prune                  # Remove all unused volumes
docker rmi $(docker images -q)       # Remove all images
docker rm $(docker ps -aq)           # Remove all containers
```

