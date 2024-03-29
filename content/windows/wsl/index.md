---
title: "Windows Subsystem for Linux 2"
excerpt: "How to install Windows Subsystem for Linux 2 on Windows 10"
last_modified_at: 2020-10-08
permalink: /windows/wsl/
resources:
  - name: "powershell"
    src: "powershell_admin_annotated.png"
    title: "How to start Powershell with admin rights"
  - name: "WSL Explorer"
    src: "wsl_explorer.png"
    title: "Access files in WSL 2 from Windows Explorer"
---

## Installation

Since the Windows 10 build version 1903 or higher the Windows Subsystem for Linux 2 (WSL 2) is available.
The most important improvement for HEP is the FUSE support which allows us to mount the global file system, CVMFS.
Full installation instructions can be found on the [Official Microsoft Pages](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

The installation consists of four parts:

1. Open Powershell with admin rights:

{{<img name="powershell" size="medium" lazy=false >}}


2. Install the Windows Subsystem for Linux:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

3. Enable "Virtual MAchine Platform"

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

4. Set WSL 2 as your default version:

```powershell
wsl --set-default-version 2
```

After this is done, you need to install your Linux distribution of choice: Ubuntu 20.04 is recommended.
This can be done via the [Microsoft Store](https://www.microsoft.com/en-us/p/ubuntu-2004-lts/9n6svws3rx71?activetab=pivot:overviewtab).

**Note**: CentOS 7 exists in the Microsoft Store, but is not free. Instead, we will use the Ubunutu distribution in combination with Docker to provide any OS available as docker image (includes CentOS 6-8).


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