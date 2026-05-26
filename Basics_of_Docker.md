# Basics of Docker

Basic Docker commands and features are important for developers because they help in deployment and project management.

Learning Docker basics makes application setup faster and easier.

---

# What is Docker?

Docker is a tool used to run applications inside **containers**.

A container is a lightweight environment that contains:
- application code
- dependencies
- libraries
- configuration files

This helps applications run the same way on every system.

---

# Docker vs Virtual Machine

Docker is different from a Virtual Machine (VM).

## Virtual Machine

A Virtual Machine contains:
- its own operating system
- RAM
- storage
- virtual hardware

Because of this, VMs are heavier and slower.

---
## Docker

Docker does not create a full operating system.

It works on top of the host operating system.

This makes Docker:
- lightweight
- faster
- efficient

---

# Containers

Containers are isolated environments used to run applications independently.

This isolation prevents:
- software conflicts
- dependency issues
- version mismatch problems

Multiple containers can run on the same machine safely.

---

# Advantages of Docker

## Easy Setup : 

Docker makes application installation simple.

Developers do not need to manually install all dependencies.

---

## Faster Development

Pre-configured Docker images help quickly create environments.

This saves:
- time
- effort

---

## Better Performance

Containers use fewer resources compared to virtual machines.

This improves:
- speed
- scalability
- performance

---

## Application Isolation

Each container runs separately.

If one container crashes, others continue running.

This improves:
- security
- stability

---

# Host Machine and Containers

The main computer system is called the **Host Machine**.

Docker containers run inside the host machine.

Example:

```txt
Host Machine
│
├── Docker
│   ├── Container 1
│   ├── Container 2
│   └── Container 3
```

---

# Port Mapping

Applications inside containers use ports.

Docker maps container ports to host machine ports.

Example:

```bash
docker run -p 8080:80 nginx
```

## Meaning

- `8080` → Host machine port
- `80` → Container port

Opening:

```txt
http://localhost:8080
```

will open the application running inside the container.

---

# Important Docker Commands

## Show Running Containers

```bash
docker ps
```

Meaning:
Shows currently running containers.

---

## Show All Containers

```bash
docker ps -a
```

Meaning:
Shows all containers including stopped containers.

---

## Start a Container

```bash
docker start container_name
```

Meaning:
Starts an existing container.

---

## Stop a Container

```bash
docker stop container_name
```

Meaning:
Stops a running container.

---

## Remove a Container

```bash
docker rm container_name
```

Meaning:
Deletes a container.

---

# Access Container Terminal

```bash
docker exec -it container_name bash
```

## Meaning

- `exec` → run command inside container
- `-it` → interactive terminal
- `bash` → open bash shell

This command allows direct access inside the container.

---

# Copy Files From Container

```bash
docker cp container_name:/path/file.txt .
```

Meaning:
Copies files from the container to the host machine.

Useful for:
- backups
- debugging
- file management

---

# Docker Images

A Docker image is a blueprint used to create containers.

Images contain:
- application code
- dependencies
- configurations

Containers are created from images.



