---
layout: post
title: "Ubuntu 18.04 离线安装 SSH 指南"
date:   2023-03-10
tags: [SSH,deb,ssh,安装,bash]
comments: true
author: admin
---
# Ubuntu 18.04 离线安装 SSH 指南

本仓库提供了在 Ubuntu 18.04 系统上离线安装 SSH 所需的步骤和 deb 安装包。通过本指南，您可以在没有网络连接的环境中成功安装和配置 SSH 服务。

## 资源文件内容

本资源文件包含了以下内容：
1. **SSH 安装包**：包括 `openssh-client`、`openssh-server` 等必要的 deb 安装包。
2. **安装步骤**：详细的安装步骤，指导您如何在离线环境中完成 SSH 的安装。

## 安装步骤

### 1. 下载并解压安装包

将本仓库中的 `ssh.tar.gz` 文件上传到您的 Ubuntu 18.04 服务器，并解压：
```bash
tar -xzvf ssh.tar.gz
```

### 2. 进入解压后的目录并安装

进入解压后的目录，并执行以下命令进行安装：
```bash
cd ssh
chmod +x install.sh
sh install.sh
```

### 3. 安装依赖包

依次运行以下命令安装所需的依赖包：
```bash
sudo dpkg -i openssh-client_1%3a7.6p1-4ubuntu0.6_amd64.deb
sudo dpkg -i ncurses-term_6.1-1ubuntu1.18.04_all.deb
sudo dpkg -i openssh-sftp-server_1%3a7.6p1-4ubuntu0.6_amd64.deb
sudo dpkg -i openssh-server_1%3a7.6p1-4ubuntu0.6_amd64.deb
sudo dpkg -i ssh-import-id_5.7-0ubuntu1.1_all.deb
```

### 4. 修改 SSH 配置文件权限

进入 `/etc/ssh/` 目录，并修改 `sshd_config` 文件权限：
```bash
cd /etc/ssh/
chmod 777 sshd_config
```

### 5. 编辑 SSH 配置文件

使用 `vi` 编辑器编辑 `sshd_config` 文件，找到 `permitRootLogin` 并将其修改为 `yes`：
```bash
vi sshd_config
```

### 6. 启动 SSH 服务

安装完成后，启动 SSH 服务：
```bash
sudo systemctl start ssh
```

### 7. 设置 SSH 开机自启动

如果需要 SSH 服务在系统启动时自动启动，可以执行以下命令：
```bash
sudo systemctl enable ssh
```

## 注意事项

- 请确保在执行安装步骤前，已经将所有必要的 deb 安装包上传到服务器。
- 如果在安装过程中遇到依赖问题，请手动安装缺失的依赖包。

通过以上步骤，您可以在 Ubuntu 18.04 系统上成功离线安装 SSH 服务。

## 下载链接

[Ubuntu18.04离线安装SSH指南分享](https://pan.quark.cn/s/7fedbd0c7a4f)