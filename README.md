# Azure VM + Docker Nginx Container Deployment 🚀

## Project Overview

This project demonstrates the deployment of an Nginx web server inside a Docker container running on an Azure Ubuntu Virtual Machine.

The goal of this project was to understand how Cloud Engineers deploy, manage, monitor, and troubleshoot containerized applications on cloud infrastructure.

---

## Architecture

```
Azure Virtual Machine
        |
        |
Ubuntu Linux Operating System
        |
        |
Docker Engine
        |
        |
Nginx Docker Image
        |
        |
Nginx Container
        |
        |
Web Server
```

---

## Technologies Used

* Microsoft Azure VM
* Ubuntu Linux
* Docker
* Docker Hub
* Nginx Web Server
* Linux Commands
* Azure Network Security Group (NSG)

---

## Implementation Steps

### 1. Azure VM Setup

Created an Ubuntu Virtual Machine on Microsoft Azure to provide cloud infrastructure for hosting the application.

---

### 2. Docker Installation Verification

Checked Docker installation:

```bash
docker --version
```

Tested Docker:

```bash
sudo docker run hello-world
```

---

### 3. Downloaded Nginx Docker Image

Command:

```bash
sudo docker pull nginx
```

Purpose:

Downloaded the official Nginx image from Docker Hub.

---

### 4. Created Nginx Container

Command:

```bash
sudo docker run -d -p 8080:80 --name my-nginx nginx
```

Explanation:

* `-d` → Run container in background
* `-p 8080:80` → Map Azure VM port 8080 to container port 80
* `--name my-nginx` → Assign container name
* `nginx` → Use Nginx image

---

### 5. Container Verification

Checked running containers:

```bash
sudo docker ps
```

Checked all containers:

```bash
sudo docker ps -a
```

---

### 6. Troubleshooting

Checked container logs:

```bash
sudo docker logs my-nginx
```

Restarted container:

```bash
sudo docker start my-nginx
```

---

### 7. Monitoring Container Resources

Command:

```bash
sudo docker stats my-nginx
```

Monitored:

* CPU usage
* Memory usage
* Network traffic

---

### 8. Container Reliability Configuration

Enabled automatic restart:

```bash
sudo docker update --restart always my-nginx
```

This ensures the container automatically starts after failure or VM restart.

---

### 9. Resource Management

Applied memory limitation:

```bash
--memory="200m"
```

This prevents the container from consuming excessive system memory.

---

## Troubleshooting Experience

During deployment, the container stopped unexpectedly.

Troubleshooting steps:

1. Checked container status
2. Reviewed container logs
3. Restarted the container
4. Verified Nginx response using curl

Testing command:

```bash
curl localhost:8080
```

Successful output:

```
Welcome to nginx!
```

---

## Skills Learned

* Azure Virtual Machine Deployment
* Linux Server Management
* Docker Container Deployment
* Nginx Web Server Configuration
* Port Mapping
* Container Monitoring
* Troubleshooting
* Cloud Infrastructure Management

---

## Interview Explanation

I deployed an Nginx web server inside a Docker container on an Azure Ubuntu Virtual Machine. I configured container networking, restart policies, resource limits, monitoring, and troubleshooting using Docker commands.

---

## Future Improvements

* Docker Compose implementation
* HTTPS/SSL configuration
* CI/CD pipeline integration
* Kubernetes deployment
* Container orchestration

```
```
# azure-vm-docker-nginx-deployment
Deployed an Nginx web server inside a Docker container on an Azure Ubuntu Virtual Machine. This project covers Docker container management, networking, monitoring, troubleshooting, and cloud deployment practices.
