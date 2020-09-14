# High-Energy Physics (Doftware) Development Documentation (HEP-DEV-DOCS)

High-Energy Physics (Doftware) Development Documentation (HEP-DEV-DOCS) are hosted on [kreczko.github.io/hep-dev-docs](https://kreczko.github.io/hep-dev-docs/) and are meant as an overview to get started with software development in HEP.
While most HEP software is written for CentOS (6, 7, 8) with a large set of common depenencies, its development, given a set of tools, can happen on almost any Operating System. This documenatation describes how to install this set of tools to simplify the software setup on Windows, Mac OS and Linux machines.

At the moment of writing, these tools include

- Windows Subsystem for Linux 2 (Windows 10 only) for FUSE support and a Linux environment
- Docker for running CentOS on any OS
- CVMFS for access to most HEP depenencies via FUSE + HTTP
- Anaconda for Python environments (recommended for Python-only code)

Note that depending on the experiment you are on, you might prefer CVMFS installations of compilers and build tools,
instead of the ones provided by a Docker container or OS.

If you find mistakes or want to contribute to the documentation, please submit a pull request on [our GitHub repository](https://github.com/kreczko/hep-dev-docs).
