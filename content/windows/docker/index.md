---
title: "Docker on Windows"
permalink: /windows/docker/
excerpt: "How to install Docker on Windows"
last_modified_at: 2020-10-08
redirect_from:
  - /windows-docker/
resources:
  - name: "download"
    src: "docker_download.png"
    title: "Download Docker Desktop for Windows"
  - name: "docker_install"
    src: "docker_install.png"
    title: "Install Docker Desktop for Windows"
  - name: "docker_ps_hello_world"
    src: "docker_ps_hello_world.png"
    title: "Test Docker installation"
---

Docker is a useful tool to create specific, isolated enviroments on your machine.
On Windows 10, Docker can run within the [WSL 2](wsl) setup thus providing you with a solid Docker-on-Linux experience.
The latter means it is easy to share files and ports between the Linux OS and the Docker images.
It also allows you to make full use of all the Docker image and Docker Compose examples (i.e. no special Windows treatment).

## Installing Docker

To install Docker, head to the [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-windows/) to download
the latest Community Edition of Docker (stable version).

{{<img name="download" size="origin">}}

You will need at least Docker version 2.3.0.2 and Windows 10 version 2004 or higher for all the features discussed on these pages. Please make sure to install WSL 2 _before_ installing Docker. If everything is setup correctly, you should see the following during the Docker installation:

{{<img name="docker_install" size="origin">}}


Additional installation help as well as OS requirements for the install are detailed on the [Windows Docker pages](https://docs.docker.com/docker-for-windows/install/).

**Note**: You will be required to log out of Windows to complete the installation.

## Checking the installation

In order to verify, open your Ubuntu WSL 2 terminal and type

```bash
docker ps

docker run hello-world
```

You should see something similar to:

{{<img name="docker_ps_hello_world" size="origin">}}
