---
layout: post
title: "CentOS 76 Docker 部署 EMQX 教程本地镜像导入指南"
date:   2024-02-06
tags: [EMQX,Docker,sudo,docker,镜像]
comments: true
author: admin
---
# CentOS 7.6 Docker 部署 EMQX 教程：本地镜像导入指南

本资源包含一份详尽的教程，专为那些在云服务器环境中因网络限制而难以直接从Docker Hub拉取EMQX镜像的用户设计。EMQX是一款强大的物联网MQTT消息服务器，适合处理大规模设备连接与消息传输。以下是手动导入EMQX Docker镜像并在CentOS 7.6系统上部署的步骤概要。

## 快速入门

### 镜像下载
首先，您需要下载EMQX的预编译Docker镜像tar包。镜像文件可通过特定渠道获得，确保您已拥有该文件，或者参照原始资源链接指引获取。

### 部署步骤

#### 1. 镜像导入
- 将下载的`EMQX-latest.tar`文件上传至服务器，推荐位置`/usr/local`。
- 通过命令行执行 `sudo docker load -i /usr/local/EMQX-latest.tar` 导入镜像。

#### 2. 创建数据卷
- 运行 `sudo docker volume create EMQX_data` 创建专用数据卷，保证数据持久性。

#### 3. 部署与配置
- 根据需求决定是否使EMQX随Docker服务自动启动：
    - 不自动启动：`sudo docker run -d --name emqx -p 1883:1883 -p 8883:8883 ... emqx/emqx:latest`
    - 自动启动：增加`--restart=always`参数。

#### 4. 开启防火墙端口
- 确保服务器防火墙允许MQTT及相关端口（1883, 8883, 8083, 8084, 18083）通信，并更新云服务商的安全组规则。

#### 5. 验证与启动
- 使用 `sudo docker restart emqx` 重启服务，通过 `sudo docker ps` 确认运行状态。
- 浏览器访问 `http://your_server_ip:18083/` 检查EMQX控制台是否正常工作。

## 注意事项
- 确保Docker服务已在服务器上正确安装并启用。
- 云服务器需配置相应的安全组规则，以允许外部访问EMQX的服务端口。
- 对于首次使用，记得在成功部署后修改默认管理员密码。

此教程旨在简化EMQX在受限网络环境下的部署流程，确保您的物联网项目顺利推进。遵循上述步骤，即使在网络条件不佳的环境下，也能顺利完成EMQX的部署。

## 下载链接

[CentOS7.6Docker部署EMQX教程本地镜像导入指南](https://pan.quark.cn/s/4b370f9dece5)