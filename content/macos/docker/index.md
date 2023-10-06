---
title: "Docker on MacOS"
permalink: /macos/docker/
excerpt: "How to install Docker on MacOS"
last_modified_at: 2020-10-08
redirect_from:
  - /macos-docker/
resources:
  - name: "docker_download"
    src: "docker_download.png"
    title: "Download Docker Desktop for MacOS"
  - name: "docker_ps_hello_world"
    src: "docker_ps_hello_world.png"
    title: "Test Docker installation"
---

Docker is a useful tool to create specific, isolated enviroments on your machine.

## Installing Docker

To install Docker, head to the [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-mac/) to download
the latest Community Edition of Docker (stable version).

{{<img name="docker_download" size="origin">}}

Additional installation help as well as OS requirements for the install are detailed on the [MacOS Docker pages](https://docs.docker.com/docker-for-mac/install/).

## Checking the installation

In order to verify, open your terminal and type

```bash
docker ps

docker run hello-world
```

You should see something similar to:

{{<img name="docker_ps_hello_world" size="origin">}}
