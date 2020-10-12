---
title: "HEP on Linux"
excerpt: "HEP on Linux"
last_modified_at: 2020-10-12
---

The easiest way to get HEP software development started on Linux is with these two tools:

- [Docker](linux/docker)
- [Visual Studio Code](editors-and-ides/vscode)

Docker will allow you to run an isolated environment for any Linux distribution (e.g. CentOS is popular within HEP).
Visual Studio Code is a very versatile IDE, which will help you with using development tools and coding.

If you want to develop directly on Linux instead of via Docker, you will also need to install the compiler (e.g. GCC) and git via
yoru distributions package manager (e.g. `apt` or `yum`).

```bash
# example for Debian based systems (e.g. Ubuntu)
sudo apt-get update
sudo apt-get install build-essential gdb
```

Optionally, you might also want to configure [CVMFS on Linux](linux/cvmfs) if you want to access HEP software on your machine.
