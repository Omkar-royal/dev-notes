# Dockerfile Guide

A `Dockerfile` is a script containing instructions on how to build a Docker image.

---

## 🧾 Basic Structure

```Dockerfile
# Base image
FROM node:18

# Working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Expose port
EXPOSE 3000

# Start the app
CMD ["node", "index.js"]
```

---

## 🔍 Key Instructions

* **FROM**: Defines the base image
* **WORKDIR**: Sets the working directory inside the container
* **COPY**: Copies files from host to container
* **RUN**: Executes commands (e.g., install dependencies)
* **EXPOSE**: Indicates the port the container listens on
* **CMD**: Specifies the command to run when the container starts

---

## 💡 Tips

* Use `.dockerignore` to avoid copying unnecessary files
* Keep layers minimal to optimize image size
* Use multi-stage builds for production readiness

---

## 📦 Build & Run Example

```bash
# Build the image
docker build -t my-node-app .

# Run the container
docker run -p 3000:3000 my-node-app
```
