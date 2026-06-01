# Nginx Basics

## What is Nginx?

Nginx is a web server used to:
- host websites
- serve static files
- handle traffic
- work as a reverse proxy
- balance load between servers

Nginx is very fast and lightweight.

It is widely used in modern web development.

---
# Why Nginx is Popular?

Nginx is popular because it:
- handles many users efficiently
- uses less memory
- is fast
- works well with Docker
- is easy to configure

---

# What Nginx Can Do

Nginx can:
- serve HTML websites
- host APIs
- run as reverse proxy
- handle SSL certificates
- distribute traffic
- cache content

---

# Nginx Architecture

Example:

```txt
Client Browser
       │
       ▼
     Nginx
       │
 ┌─────┴─────┐
 │           │
App 1      App 2
```

Nginx receives requests from users and forwards them to applications.

---

# Install Nginx Using Docker

## Pull Nginx Image

```bash
docker pull nginx
```

Meaning:
Downloads nginx image from Docker Hub.

---

# Run Nginx Container

```bash
docker run -d -p 8080:80 nginx
```

## Explanation

- `-d` → run in background
- `-p` → port mapping
- `8080` → host machine port
- `80` → nginx container port

---

# Access Nginx in Browser

Open:

```txt
http://localhost:8080
```

You will see the default Nginx welcome page.

---

# Show Running Containers

```bash
docker ps
```

Meaning:
Displays running Docker containers.

---

# Stop Nginx Container

```bash
docker stop container_id
```

Meaning:
Stops the running nginx container.

---

# Start Nginx Container Again

```bash
docker start container_id
```

Meaning:
Starts stopped container again.

---

# Remove Nginx Container

```bash
docker rm container_id
```

Meaning:
Deletes the container.

---

# Access Nginx Container Terminal

```bash
docker exec -it container_id bash
```

Meaning:
Opens terminal inside nginx container.

---

# Important Nginx Folder

Inside container:

```txt
/etc/nginx
```

This folder contains nginx configuration files.

---

# Main Nginx Configuration File

```txt
/etc/nginx/nginx.conf
```

This file controls:
- server settings
- ports
- request handling
- performance settings

---

# Default Website Files Location

```txt
/usr/share/nginx/html
```

This folder contains website files.

Example:
- HTML
- CSS
- JavaScript

---

# Create Custom HTML Page

## Example

```html
<h1>Hello Nginx</h1>
```

Save as:

```txt
index.html
```

---

# Copy HTML File Into Nginx Container

```bash
docker cp index.html container_id:/usr/share/nginx/html/
```

Meaning:
Copies local HTML file into nginx container.

---

# Restart Nginx Container

```bash
docker restart container_id
```

Meaning:
Restarts nginx container.

---

# Reverse Proxy

A reverse proxy forwards requests from users to backend applications.

Example:

```txt
User → Nginx → Node.js / PHP / Python App
```

Benefits:
- better security
- load balancing
- SSL handling
- faster performance

---

# Nginx With PHP

Nginx is commonly used with:
- PHP
- Laravel
- CodeIgniter

Nginx forwards PHP requests to PHP-FPM.

---

# Nginx With Docker

Nginx works very well with Docker containers.

Common setup:

```txt
Nginx Container
PHP Container
MySQL Container
```

This setup is widely used in modern web applications.

---

# Advantages of Nginx

## Fast Performance

Handles many users efficiently.

---

## Low Memory Usage

Uses fewer system resources.

---

## Scalability

Can handle large traffic easily.

---

## Security

Works well with SSL and reverse proxy setups.

---

# Docker + Nginx Workflow

Example workflow:

```txt
Docker
   │
   ├── Nginx Container
   ├── PHP Container
   └── MySQL Container
```
Each service runs independently.

