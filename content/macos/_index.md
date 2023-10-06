---
title: "HEP on macOS"
excerpt: "HEP on macOS"
last_modified_at: 2020-10-12
permalink: /macos
---

The easiest way to get HEP software development started on macOS is with these two tools:

- [Docker](macos/docker)
- [Visual Studio Code](editors-and-ides/vscode)

Docker will allow you to run an isolated environment for any Linux distribution (e.g. CentOS is popular within HEP).
Visual Studio Code is a very versatile IDE, which will help you with using development tools and coding.

If you want to develop directly on macOS instead of via Docker, you will also need to install XCode and the command line developer tools:

- install XCode via the AppStore
- install command line developer tools by opening the terminal and executing

```bash
xcode-select --install
```

Optionally, you might also want to configure [CVMFS on macOS](macos/cvmfs) if you want to access HEP software on your machine.
