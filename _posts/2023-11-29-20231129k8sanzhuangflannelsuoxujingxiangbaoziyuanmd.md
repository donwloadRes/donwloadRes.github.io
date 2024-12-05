---
layout: post
title: "k8s 安装 flannel 所需镜像包资源"
date:   2024-10-21
tags: [flannel,Kubernetes,镜像,插件,集群]
comments: true
author: admin
---
# k8s 安装 flannel 所需镜像包资源

本仓库提供了一个用于安装 Kubernetes (k8s) 网络插件 flannel 的必要镜像包资源。该资源包包含了以下内容：

1. **flannel-cni-plugin:v1.1.2**
2. **flannel:v0.21.5**
3. **kube-flannel.yaml** 文件

## 资源描述

- **flannel-cni-plugin:v1.1.2**: 这是 flannel 的 CNI 插件镜像，用于 Kubernetes 集群中的网络配置。
- **flannel:v0.21.5**: 这是 flannel 的核心镜像，负责在 Kubernetes 集群中提供网络覆盖。
- **kube-flannel.yaml**: 这是一个 Kubernetes 的配置文件，用于部署 flannel 网络插件。

## 使用方法

1. 下载本仓库中的资源文件。
2. 根据你的 Kubernetes 集群配置，使用 `kube-flannel.yaml` 文件部署 flannel 网络插件。
3. 确保你的 Kubernetes 集群能够正确拉取 `flannel-cni-plugin:v1.1.2` 和 `flannel:v0.21.5` 镜像。

## 注意事项

- 请确保你的 Kubernetes 集群版本与 flannel 插件版本兼容。
- 如果你在私有环境中使用这些镜像，请确保你有相应的镜像仓库权限。

## 贡献

如果你有任何改进建议或发现了问题，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的资源文件遵循开源许可证，具体请参考 LICENSE 文件。

---

有兴趣的朋友可以自行下载使用。

## 下载链接

[k8s安装flannel所需镜像包资源](https://pan.quark.cn/s/c9aec8dbc1f5)