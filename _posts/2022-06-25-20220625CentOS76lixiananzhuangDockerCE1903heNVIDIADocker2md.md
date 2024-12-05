---
layout: post
title: "CentOS 76 离线安装 Docker CE 1903 和 NVIDIA Docker 2"
date:   2020-07-04
tags: [Docker,docker,bash,安装,CE]
comments: true
author: admin
---
# CentOS 7.6 离线安装 Docker CE 19.03 和 NVIDIA Docker 2

## 资源描述

本仓库提供了一个在 CentOS 7.6 系统上离线安装 Docker CE 19.03 和 NVIDIA Docker 2 的资源文件。资源文件包括以下内容：

- `docker-local.tar`：包含 Docker CE 19.03 的 RPM 包。
- `nvidia-docker2.zip`：包含 NVIDIA Docker 2.4 的 RPM 包。

## 安装流程

### 1. 安装 Docker CE 19.03

1. 进入 `docker-local` 目录：
   ```bash
   cd docker-local
   ```

2. 安装 Docker CE 19.03：
   ```bash
   rpm -Uvh *.rpm --nodeps --force
   ```

3. 启用并启动 Docker 服务：
   ```bash
   systemctl enable docker && systemctl start docker
   ```

4. 验证 Docker 是否安装成功：
   ```bash
   docker images
   ```

### 2. 安装 NVIDIA Docker 2

1. 进入 `nvidia-docker2` 目录：
   ```bash
   cd nvidia-docker2
   ```

2. 安装 NVIDIA Docker 2：
   ```bash
   rpm -Uvh *.rpm --nodeps --force
   ```

### 3. 修改配置文件并重启 Docker

1. 使用 `daemon.json` 替换 `/etc/docker/daemon.json` 文件。请注意，将 `/data/docker` 替换为你需要安装的路径。

2. 重新加载并重启 Docker 服务：
   ```bash
   systemctl daemon-reload && systemctl restart docker
   ```

## 注意事项

- 请确保在执行安装步骤前，系统已经正确配置并满足安装要求。
- 在替换 `daemon.json` 文件时，请根据实际需求修改路径。

通过以上步骤，你可以在 CentOS 7.6 系统上成功离线安装 Docker CE 19.03 和 NVIDIA Docker 2。

## 下载链接

[CentOS7.6离线安装DockerCE19.03和NVIDIADocker2](https://pan.quark.cn/s/c97c7c737efd)