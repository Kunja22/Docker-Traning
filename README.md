# Docker-Traning

## Docker Introduction

Docker is an open-source platform that enables developers to build, package, and run applications inside lightweight containers. Containers include everything needed to run the application, such as code, runtime, libraries, and dependencies, ensuring that the application works consistently across different environments.

Docker helps solve the common problem of “it works on my machine but not on another system.” By using containers, applications become portable, scalable, and easy to deploy.

Key Features

Containerization – Package applications and dependencies together.

Portability – Run containers on any system that supports Docker.

Isolation – Each container runs independently.

Scalability – Easily scale applications using container orchestration tools.

Consistency – Same environment in development, testing, and production.

How Docker Works

Docker uses a client-server architecture:

Docker Client – Command-line tool used to interact with Docker.

Docker Daemon – Background service that builds and runs containers.

Docker Images – Templates used to create containers.

Docker Containers – Running instances of Docker images.

Basic Docker Workflow

Write a Dockerfile to define the application environment.

Build a Docker Image using the Dockerfile.

Run a Docker Container from the image.

Deploy and manage containers easily across environments.

Common Docker Commands
# Check docker version
docker --version

# Pull image from Docker Hub
docker pull nginx

# Build docker image
docker build -t myapp .

# Run container
docker run -d -p 80:80 myapp

# List running containers
docker ps
Benefits of Docker

Faster application deployment

Consistent development environments

Improved resource utilization

Simplified CI/CD integration

Docker Architecture

Docker follows a client-server architecture that allows users to build, run, and manage containers efficiently. It consists of several key components that work together to enable containerization.

Main Components
1. Docker Client

The Docker Client is the command-line interface (CLI) that users interact with to communicate with Docker. Commands such as docker build, docker pull, and docker run are executed through the Docker Client.

Example:

docker run nginx

The client sends these commands to the Docker Daemon.

2. Docker Daemon (dockerd)

The Docker Daemon is the background service that runs on the host machine. It is responsible for:

Building Docker images

Running Docker containers

Managing Docker networks

Managing Docker volumes

The daemon listens for Docker API requests from the Docker Client and processes them.

3. Docker Images

A Docker Image is a read-only template used to create containers. It includes everything needed to run an application, such as:

Application code

Runtime environment

System libraries

Dependencies

Images are built using a Dockerfile.

Example:

docker build -t myapp .
4. Docker Containers

A Docker Container is a running instance of a Docker image. Containers are lightweight and isolated environments where applications run.

Key features:

Fast startup time

Resource-efficient

Portable across environments

Example:

docker run -d -p 80:80 nginx
5. Docker Registry

A Docker Registry is a storage location where Docker images are stored and shared.

Common registries:

Docker Hub (public registry)

Amazon ECR

Google Container Registry

Private registries

Example:

docker pull nginx
Docker Architecture Flow

The Docker Client sends a command to the Docker Daemon.

The Docker Daemon processes the request.

If an image is needed, Docker pulls it from the Docker Registry.

The Docker Daemon creates and runs a Container from the image.

Simple Architecture Diagram (Concept)
Developer
   |
   v
Docker Client (CLI)
   |
   v
Docker Daemon (dockerd)
   |
   |---- Docker Images
   |---- Docker Containers
   |
   v
Docker Registry (Docker Hub / Private Registry)

Basic Docker Commands
1. Check Docker Version

Check if Docker is installed and verify the version.

docker --version
2. Pull an Image from Docker Hub

Download an image from the Docker registry.

docker pull nginx
3. List Docker Images

Show all images available on the system.

docker images
4. Create and Run a Container

Run a container from an image.

docker run nginx

Run container in detached mode with port mapping:

docker run -d -p 80:80 nginx

-d → Run container in background

-p → Map host port to container port

5. List Running Containers
docker ps

Show all containers (running + stopped):

docker ps -a
6. Stop a Container
docker stop <container_id>

Example:

docker stop 4f3c2d1
7. Remove a Container
docker rm <container_id>
Commands to Create Docker Images
1. Create a Dockerfile

Example Dockerfile:

FROM nginx
COPY . /usr/share/nginx/html
2. Build Docker Image
docker build -t myapp .

-t → Tag name for the image

. → Current directory

3. Run Container from Created Image
docker run -d -p 8080:80 myapp
Useful Docker Commands
Remove Image
docker rmi <image_id>
View Container Logs
docker logs <container_id>
Execute Command Inside Container
docker exec -it <container_id> /bin/bash
