# Visual Studio Code Podman Box (vsc-podman)

This repository contains some IaC scripts to build a fedora based VirtualBox running podman. The box in conjunction with Visual Studio Code (VSC) is meant as a drop in solution for Docker.

## How it works

The general idea is to start the VM and use it to develop and run your applications using VSCs [Remote SSH Development](https://code.visualstudio.com/docs/remote/ssh) feature.

Due to VSC implementation, all no UI related VSC plugins will be installed on the VM as well. Only UI related plugins will be installed on the host. Therefore, it is also possible to isolate multiple development environments easily by creating multiple boxes.

## Setup

In order to setup a new box navigate to the repositories root directory and run

```bash
vagrant up
```

In order to refine the basic box to your needs, you can add your required software an configurations using ansible.

To configure VSC for development, follow their instructions: [Remote SSH Development](https://code.visualstudio.com/docs/remote/ssh)