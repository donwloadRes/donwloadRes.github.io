---
layout: post
title: "Ubuntu系统的Docker离线安装包"
date:   2023-06-29
tags: [docker,Docker,安装包,sudo,bash]
comments: true
author: admin
---
# Ubuntu系统的Docker离线安装包

## 介绍
本仓库提供了一个适用于Ubuntu系统的Docker离线安装包，该安装包已经经过测试，确保能够有效安装Docker。

## 安装步骤
1. 使用以下命令安装`containerd.io`：
   ```bash
   sudo dpkg -i containerd.io_1.4.6-1_amd64.deb
   ```
2. 使用以下命令安装`docker-ce-cli`：
   ```bash
   sudo dpkg -i docker-ce-cli_20.10.7_3-0_ubuntu-xenial_amd64.deb
   ```
3. 使用以下命令安装`docker-ce`：
   ```bash
   sudo dpkg -i docker-ce_20.10.7_3-0_ubuntu-xenial_amd64.deb
   ```

## 查看Docker版本
安装完成后，可以通过以下命令查看Docker的版本：
```bash
sudo docker --version
```

## 配置免sudo执行Docker命令
如果希望在使用Docker命令时无需每次都加`sudo`，可以执行以下命令将当前用户添加到`docker`用户组：
```bash
sudo usermod -aG docker 登录账号
```
请将`登录账号`替换为实际的用户名。

## 注意事项
- 确保在执行安装命令前已下载相应的`.deb`安装包。
- 安装过程中可能需要根据提示解决依赖问题。
- 添加用户到`docker`组后，需要重新登录或重启系统才能生效。

希望这个安装包能帮助您顺利安装Docker！

## 下载链接

[Ubuntu系统的Docker离线安装包](https://pan.quark.cn/s/8b5d1515b40a)