---
title: "Docker on Linux"
permalink: /linux/docker/
excerpt: "How to install Docker on Linux"
last_modified_at: 2020-10-16
redirect_from:
  - /Linux-docker/
resources:
  - name: "docker_install"
    src: "install_docker_linux.png"
    title: "Download Docker Desktop for Linux"
  - name: "docker_ps_hello_world"
    src: "docker_ps_hello_world.png"
    title: "Test Docker installation"
---

Docker is a useful tool to create specific, isolated enviroments on your machine. 
As most HEP software is currently written for the CentOS distribution, Docker can provide a matching environment independent of your current Linux distribution.
Most Linux distributions should be able to install Docker as long as they have a kernel version qual or newer than 3.10.

## Installing Docker

To install Docker, head to the [Docker docs](https://docs.docker.com/engine/install/) and follow the instructions for your Linux distribution.
It is recommended you install the latest stable version of Docker. To keep it up to date, follow the instructions using the package manager for your distribution.

{{<img name="docker_install" size="origin">}}

## Checking the installation

In order to verify, open your terminal and type

```bash
docker ps

docker run hello-world
```

You should see something similar to:

{{<img name="docker_ps_hello_world" size="origin">}}
![Docker PS and hello world output](../static/windows/docker_ps_hello_world.png)
