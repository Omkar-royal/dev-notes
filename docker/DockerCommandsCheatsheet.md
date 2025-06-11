# Docker Commands Cheatsheet

Quick reference for commonly used Docker CLI commands.

---

## 📦 Images

```bash
# List images
docker images

# Build image from Dockerfile
docker build -t <image_name> .

# Remove an image
docker rmi <image_id>
```

## 🧱 Containers

```bash
# List running containers
docker ps

# List all containers (including stopped)
docker ps -a

# Run a container
docker run -d -p 8080:80 --name mycontainer <image_name>

# Stop a container
docker stop <container_id>

# Start a container
docker start <container_id>

# Remove a container
docker rm <container_id>
```

## 🔍 Logs & Exec

```bash
# View container logs
docker logs <container_id>

# Access container shell
docker exec -it <container_id> bash
```

## 📂 Volumes & Networks

```bash
# List volumes
docker volume ls

# Create volume
docker volume create <volume_name>

# List networks
docker network ls
```

## 🧹 Cleanup

```bash
# Remove all stopped containers
docker container prune

# Remove all unused images
docker image prune -a
```

---

## ✅ Tip

Use `docker system df` to check disk usage and `docker system prune` to clean up all unused data.
