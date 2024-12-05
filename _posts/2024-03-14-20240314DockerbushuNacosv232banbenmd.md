---
layout: post
title: "Docker 部署 Nacos v232 版本"
date:   2021-06-28
tags: [nacos,Nacos,Docker,v2.3,部署]
comments: true
author: admin
---
# Docker 部署 Nacos v2.3.2 版本

本文档提供了使用 Docker 部署 Nacos v2.3.2 版本的详细步骤和配置说明。Nacos 是一个开源的动态服务发现、配置和服务管理平台，适用于构建云原生应用。

## 目录

1. [环境准备](#环境准备)
2. [下载 Nacos 镜像](#下载-nacos-镜像)
3. [配置 Nacos](#配置-nacos)
4. [启动 Nacos](#启动-nacos)
5. [验证部署](#验证部署)

## 环境准备

在开始部署之前，请确保您的系统已经安装了 Docker 和 Docker Compose。

## 下载 Nacos 镜像

首先，从 Docker Hub 下载 Nacos v2.3.2 版本的镜像：

```bash
docker pull nacos/nacos-server:v2.3.2
```

## 配置 Nacos

创建一个目录用于存放 Nacos 的配置文件和数据：

```bash
mkdir nacos && cd nacos
mkdir data logs
```

## 启动 Nacos

使用以下命令启动 Nacos 容器：

```bash
docker run --name nacos \
-e MODE=standalone \
-p 8848:8848 \
-d nacos/nacos-server:v2.3.2
```

## 验证部署

启动成功后，您可以通过浏览器访问 `http://<您的IP地址>:8848/nacos` 来验证 Nacos 是否正常运行。默认的用户名和密码为 `admin/nacos`。

## 注意事项

- 如果您的网络环境无法直接访问 Docker Hub，可以使用提供的镜像文件下载链接进行离线下载。
- 本文档未配置 MySQL 数据库，配置数据保存在 `data/config-data` 目录下。
- 开启鉴权功能后，需要验证登录账号与密码（默认 `admin/nacos`）。

通过以上步骤，您可以成功在 Docker 环境中部署 Nacos v2.3.2 版本，并开始使用其服务发现和配置管理功能。

## 下载链接

[Docker部署Nacosv2.3.2版本](https://pan.quark.cn/s/6d37f1e0bf9f)