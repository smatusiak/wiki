---
title: WTF is Docker?
layout: page
parent: Infrastructure
---

# WTF is Docker?

## Overview

1. What is Docker?
2. How does Docker work?
3. Docker in Serverless Cloud Services
4. Installing Docker on Windows
5. Running Docker on Windows
6. Docker Licenses and Corporate Use

Now, let's explore the world of Docker!

## 1. What is Docker?

Docker is an open-source platform that automates the deployment, scaling, and management of applications. It does this by encapsulating applications into containers. A Docker container is a standalone, executable package that includes everything needed to run an application: the code, a runtime, libraries, environment variables, and config files.

> Note: Containers are similar to virtual machines, but they are more portable and efficient because they share the host system's kernel and do not require a full operating system.

## 2. How Does Docker Work?

Docker uses a client-server architecture. The Docker client communicates with the Docker daemon, which builds, runs, and manages Docker containers. The Docker client and daemon can run on the same host, or they can communicate over a network.

A Docker container is created from a Docker image, which is a read-only template with instructions for creating a Docker container. Docker images are created with the `build` command, and they'll produce a container when started with `run`.

| Command | Description |
|---------|-------------|
| `docker build` | Create a Docker image from a Dockerfile |
| `docker run` | Start a Docker container from a Docker image |

## 3. Docker in Serverless Cloud Services

Serverless computing is a cloud-computing model where the cloud provider dynamically manages the allocation of machine resources. Docker plays a crucial role in serverless computing because Docker containers provide a consistent, reproducible environment that can be easily scaled up or down.

Many cloud service providers, like AWS, Google Cloud, and Microsoft Azure, offer serverless services that leverage Docker. These services allow developers to focus on their code, leaving the infrastructure management to the cloud provider.

## 4. Installing Docker on Windows

To install Docker Desktop on Windows:

1. Visit the [Docker Desktop for Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows/) download page.
2. Click on "Get Docker Desktop for Windows (stable)".
3. After the installer is downloaded, double-click `Docker Desktop Installer.exe` to start the installation.

> Note: Docker Desktop requires Windows 10 Pro or Enterprise version 15063 to run.

## 5. Running Docker on Windows

Once Docker Desktop is installed, you can start using Docker. Open a command prompt and run:

```bash
docker run hello-world
```

This command will download a test image and run it in a container. If everything is correctly installed, it should print a welcome message.

## 6. Docker Licenses and Corporate Use

Docker is released under the Apache 2.0 open-source license. However, Docker Desktop for Windows, the version designed for enterprise use, is released under a different license and requires a paid subscription for use in a corporate environment. 

> Note: Always ensure you are in compliance with the licensing terms when using Docker in a corporate environment.

| Command | Description |
|---------|-------------|
| `docker run hello-world` | Run a test Docker container |

Congratulations! You now have a basic understanding of Docker, its benefits, and how to use it. Now you're ready to start exploring the world of containerization!