---
title: "Windows Subsystem for Linux"
excerpt: "How to install Windows Subsystem for Linux on Windows 11"
last_modified_at: 2025-10-17
permalink: /windows/wsl/
resources:
  - name: "powershell"
    src: "powershell_admin_annotated.png"
    title: "How to start Powershell with admin rights"
  - name: "WSL Explorer"
    src: "wsl_explorer.png"
    title: "Access files in WSL from Windows Explorer"
---

## Installation

Since the Windows 10 build version 1903 or higher the Windows Subsystem for Linux version 2 is available.
The most important improvement for HEP is the FUSE support which allows us to mount the global file system, CVMFS.
Full installation instructions can be found on the [Official Microsoft Pages](https://learn.microsoft.com/en-us/windows/wsl/install).

The installation consists of four parts:

1. Open Powershell with admin rights:

{{<img name="powershell" size="medium" lazy=false >}}


2. Install the Windows Subsystem for Linux:

```powershell
wsl --install
```

3. Optional: Change the default Linux distribution
By default, the installed Linux distribution will be Ubuntu. 
This is fine for most use-cases as you can refine your choice with containers (e.g. CentOS, RockyLinux, etc).

On how to change it, please refer to the [Microsoft Documentation - change the default Linux distribution](https://learn.microsoft.com/en-us/windows/wsl/install#change-the-default-linux-distribution-installed).

4. Start up WSL for the very first time
After the installation is complete, you need to start WSL for the first time.
You can do this by starting the installed Linux distribution from the start menu.

The first start will take a bit longer as the Linux distribution needs to be set up.
You will be asked to create a user account and password for the Linux distribution.
If you are regularly using WSL to access remote systems via SSH, it is recommended to use the same username as on the remote systems.
Please set a strong password as well.


## Accessing files from WSL inside Windows

Due to the tight integration between WSL and Windows, some windows commands are available withing WSL.
Once such command is

```shell
explorer.exe .
```
Note: The `.` is very important as it denotes the current folder.

When executed in a folder inside a WSL instance, it will open the current folder in the Windows Explorer as a network mount:
{{<img name="WSL Explorer" size="large" lazy=false >}}

Soon: [Access Linux filessystems in Windows and WSL2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/)