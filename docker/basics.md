# Docker Basics

Docker is a platform for developing, shipping, and running applications using containerization. Containers allow developers to package up an application with all the parts it needs, such as libraries and other dependencies, and ship it all out as one package.

---

## 🧱 What is Docker?

* Docker is an open-source tool for automating the deployment of applications inside lightweight, portable containers.
* Containers run on any machine that has Docker installed, regardless of the underlying operating system.

## 🛠️ Key Components

* **Docker Engine**: Core component that runs and manages containers.
* **Docker Images**: Read-only templates used to create containers.
* **Docker Containers**: Runnable instances of Docker images.
* **Dockerfile**: Script to build Docker images.
* **Docker Hub**: Cloud-based registry service for sharing images.

## 📦 Why Use Docker?

* Consistency across environments
* Lightweight compared to virtual machines
* Fast deployment and rollback
* Easy scaling and integration with CI/CD

## 🔄 Common Workflow

1. Write `Dockerfile`
2. Build image using `docker build`
3. Run container using `docker run`
4. Share image via Docker Hub or private registry

---

## 🧪 Example

```bash
# Build image from Dockerfile
docker build -t myapp .

# Run container
docker run -p 8080:80 myapp
```
