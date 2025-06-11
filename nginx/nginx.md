# Nginx Setup Guide

Nginx is a high-performance web server and reverse proxy used to serve static content, load balance, and manage API traffic.

---

## 🚀 What is Nginx?

* Web server
* Reverse proxy
* Load balancer
* Caching and compression support

---

## ⚙️ Basic Installation (Ubuntu)

```bash
sudo apt update
sudo apt install nginx
```

Check service status:

```bash
sudo systemctl status nginx
```

---

## 🪟 Installation on Windows

### Option 1: Using WSL (Recommended)

1. Enable Windows Subsystem for Linux
2. Install Ubuntu from Microsoft Store
3. Launch Ubuntu and run:

```bash
sudo apt update
sudo apt install nginx
```

4. Start Nginx with:

```bash
sudo service nginx start
```

5. Open browser and go to `http://localhost:80`

### Option 2: Native Windows (Less Common)

1. Download precompiled binaries from [https://nginx.org/en/download.html](https://nginx.org/en/download.html)
2. Extract the ZIP file
3. Open `cmd` and navigate to the folder
4. Start Nginx:

```cmd
start nginx
```

5. Stop Nginx:

```cmd
nginx -s stop
```

---

## 📁 Default File Paths

* Config: `/etc/nginx/nginx.conf`
* Site Configs: `/etc/nginx/sites-available/`
* Enabled Sites: `/etc/nginx/sites-enabled/`
* Logs: `/var/log/nginx/`

---

## 🌐 Basic Site Configuration

```nginx
server {
    listen 80;
    server_name example.com;

    location / {
        root /var/www/html;
        index index.html;
    }
}
```

Enable config:

```bash
sudo ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx
```

---

## 🐳 Nginx with Docker

```bash
# Run a basic Nginx container
docker run --name nginx-server -d -p 8080:80 nginx

# Mount local config and html
docker run -d -p 8080:80 \
  -v /path/to/html:/usr/share/nginx/html \
  -v /path/to/nginx.conf:/etc/nginx/nginx.conf \
  nginx
```

---

## ✅ Tip

Use Nginx as a reverse proxy in front of Node.js, Laravel, or any backend API to enhance performance and security.
