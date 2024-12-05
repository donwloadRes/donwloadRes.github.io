---
layout: post
title: "CentOS 7 安装 Harbor 指南"
date:   2021-06-11
tags: [harbor,Harbor,Docker,安装,sudo]
comments: true
author: admin
---
# CentOS 7 安装 Harbor 指南

本仓库提供了一个资源文件，用于在 CentOS 7 系统上安装 Harbor。Harbor 是一个企业级的 Docker Registry，支持安全的镜像管理和分发。

## 资源文件内容

- **harbor-offline-installer-v2.10.0.tgz**: 这是 Harbor 的离线安装包，适用于无法直接访问互联网的环境。

## 安装步骤

1. **前提条件**:
   - 已安装 Docker 和 Docker Compose。

2. **下载离线包**:
   - 将 `harbor-offline-installer-v2.10.0.tgz` 下载到本地。

3. **安装 Harbor**:
   - 创建目录 `/opt/harbor`。
   - 将离线包上传到 `/opt/harbor` 目录。
   - 解压离线包：`sudo tar xf harbor-offline-installer-v2.10.0.tgz`。
   - 复制配置文件：`sudo scp -r harbor.yml.tmpl harbor.yml`。
   - 编辑配置文件 `harbor.yml`，根据需要修改 `hostname` 和 `http` 端口。
   - 运行安装脚本：`sudo ./install.sh`。
   - 查看容器信息：`sudo docker ps -a`。

4. **访问 Harbor**:
   - 访问地址：`http://<hostname>:18080`。
   - 默认账号：`admin`，默认密码：`Harbor12345`。

5. **开机自启**:
   - 进入目录 `/opt/harbor/harbor`。
   - 编辑启动脚本 `start.sh`，添加启动命令。
   - 赋予执行权限：`sudo chmod +x /opt/harbor/harbor/start.sh`。
   - 编辑 `/etc/rc.d/rc.local`，添加启动脚本路径。
   - 赋予 `/etc/rc.d/rc.local` 执行权限。

6. **推送镜像**:
   - 在本地安装 Docker 并配置可接受 HTTP。
   - 编写 Dockerfile 并构建镜像。
   - 重命名镜像并推送至 Harbor。

## 注意事项

- 安装过程中请确保 Docker 和 Docker Compose 已正确安装。
- 配置文件 `harbor.yml` 中的 `hostname` 和 `http` 端口需要根据实际情况进行修改。
- 如果需要使用 HTTPS，请在配置文件中启用并配置相关证书。

## 参考文档

- 更多详细信息请参考 [CSDN 博客文章](https://blog.csdn.net/qq_32088869/article/details/135461169)。

---

通过以上步骤，您可以在 CentOS 7 系统上成功安装并配置 Harbor，实现企业级的 Docker 镜像管理。

## 下载链接

[CentOS7安装Harbor指南](https://pan.quark.cn/s/231a28dbc6d0)