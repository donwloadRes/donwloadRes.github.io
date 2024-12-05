---
layout: post
title: "CoreDNS v184 镜像及 YAML 文件下载"
date:   2023-10-04
tags: [镜像,CoreDNS,coredns,文件,导入]
comments: true
author: admin
---
# CoreDNS v1.8.4 镜像及 YAML 文件下载

本仓库提供 CoreDNS v1.8.4 镜像以及相应的 YAML 文件，帮助您在 Kubernetes 集群搭建过程中避免因 Calico 镜像无法下载而导致的部署问题。

## 资源文件说明

- **coredns.tar**: CoreDNS v1.8.4 的 Docker 镜像文件。
- **coredns.yaml**: CoreDNS 的 Kubernetes 部署 YAML 文件。

## 使用方法

1. **下载资源文件**: 下载本仓库中的 `coredns.tar` 和 `coredns.yaml` 文件。

2. **导入镜像**: 将 `coredns.tar` 文件解压到您的 Linux 本地，然后使用以下命令导入镜像：
   ```bash
   docker load -i coredns.tar
   ```

3. **查看导入的镜像**: 使用以下命令查看已导入的 CoreDNS 镜像：
   ```bash
   docker images
   ```

4. **部署 CoreDNS**: 使用 `coredns.yaml` 文件在 Kubernetes 集群中部署 CoreDNS：
   ```bash
   kubectl apply -f coredns.yaml
   ```

## 注意事项

- 请确保您的 Kubernetes 集群环境已正确配置，并且 Docker 服务已启动。
- 在导入镜像之前，请确保您的 Docker 版本与镜像兼容。

通过以上步骤，您可以顺利完成 CoreDNS 的部署，避免因镜像下载问题导致的集群搭建失败。

## 下载链接

[CoreDNSv1.8.4镜像及YAML文件下载](https://pan.quark.cn/s/619b722287d8)