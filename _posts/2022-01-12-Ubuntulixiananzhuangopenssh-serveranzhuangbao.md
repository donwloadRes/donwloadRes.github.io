---
layout: post
title: "Ubuntu离线安装openssh-server安装包"
date:   2024-01-23
tags: [openssh,server,deb,安装,Ubuntu]
comments: true
author: admin
---
# Ubuntu离线安装openssh-server安装包

## 资源描述

本仓库提供了一个用于Ubuntu 20.04和Ubuntu 16.04等其他Ubuntu版本的离线安装openssh-server的安装包。通过本资源，您可以在没有网络连接的情况下，轻松完成openssh-server的安装。

## 安装步骤

1. **下载安装包**：
   - 从本仓库下载以下安装包：
     - `libssl1.0.0_1.0.2n-1ubuntu5.7_amd64.deb`
     - `openssh-client_8.4p1-6ubuntu1_amd64.deb`
     - `openssh-sftp-server_8.4p1-6ubuntu1_amd64.deb`
     - `openssh-server_8.4p1-6ubuntu1_amd64.deb`
     - `ssh_8.4p1-6ubuntu1_all.deb`

2. **安装依赖包**：
   - 在终端中依次执行以下命令，安装依赖包：
     ```bash
     sudo dpkg -i libssl1.0.0_1.0.2n-1ubuntu5.7_amd64.deb
     ```

3. **安装openssh-client**：
   - 继续执行以下命令，安装openssh-client：
     ```bash
     sudo dpkg -i openssh-client_8.4p1-6ubuntu1_amd64.deb
     ```

4. **安装openssh-sftp-server**：
   - 继续执行以下命令，安装openssh-sftp-server：
     ```bash
     sudo dpkg -i openssh-sftp-server_8.4p1-6ubuntu1_amd64.deb
     ```

5. **安装openssh-server**：
   - 继续执行以下命令，安装openssh-server：
     ```bash
     sudo dpkg -i openssh-server_8.4p1-6ubuntu1_amd64.deb
     ```

6. **安装ssh**：
   - 最后执行以下命令，安装ssh：
     ```bash
     sudo dpkg -i ssh_8.4p1-6ubuntu1_all.deb
     ```

7. **重启SSH服务**：
   - 安装完成后，执行以下命令重启SSH服务：
     ```bash
     sudo service ssh restart
     ```

## 注意事项

- 请确保在执行安装命令时，所有安装包都在当前目录下。
- 如果在安装过程中遇到依赖问题，请尝试使用`sudo apt-get install -f`命令修复依赖关系。

## 支持的Ubuntu版本

- Ubuntu 20.04
- Ubuntu 16.04
- 其他基于Ubuntu的发行版

## 贡献

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本仓库中的资源文件遵循相应的开源许可证，具体请查看每个文件的许可证信息。

## 下载链接

[Ubuntu离线安装openssh-server安装包](https://pan.quark.cn/s/b3e7d3511ea0)