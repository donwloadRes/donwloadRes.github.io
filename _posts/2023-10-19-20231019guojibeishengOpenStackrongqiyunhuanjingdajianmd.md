---
layout: post
title: "国基北盛OpenStack容器云环境搭建"
date:   2023-09-05
tags: [节点,OpenStack,搭建,环境,部署]
comments: true
author: admin
---
# 国基北盛-OpenStack-容器云-环境搭建

## 简介
本资源文件提供了国基北盛OpenStack容器云环境搭建的详细步骤和相关配置文件。通过本资源，用户可以快速搭建一个基于OpenStack的容器云环境，并进行Kubernetes集群的部署和管理。

## 内容概述
1. **实验环境**：
   - 系统说明：利用OpenStack私有云部分所搭建的环境，创建两台云主机进行部署K8s集群环境。
   - 运行环境：CentOS 7.5，内核版本>=3.10。
   - Docker版本：docker-ce-19.03.13。
   - Kubernetes版本：1.18.1。

2. **节点角色**：
   - Master节点：8G内存，100G硬盘，IP地址为192.168.58.6。
   - Worker节点：8G内存，100G硬盘，IP地址为192.168.58.11。

3. **基础环境部署**：
   - 安装CentOS 7.5操作系统。
   - 将官方提供的chinaskills_cloud_paas.iso镜像文件上传到Master节点，并将基础系统镜像挂载到Master节点。

4. **系统初始化配置**：
   - 修改主机名。
   - 配置主机名映射。
   - 关闭防火墙和SElinux。
   - 配置yum源。

5. **部署Harbor仓库**：
   - 使用脚本k8s_harbor_install.sh自动化部署Harbor仓库。

6. **上传镜像到Harbor仓库**：
   - 使用脚本k8s_image_push.sh将paas中准备好的镜像全部推送到Harbor仓库。

7. **部署Kubernetes集群**：
   - 执行脚本k8s_master_install.sh自动化部署K8s集群。

8. **将Node节点加入集群**：
   - 将脚本上传到Node节点上，并执行脚本k8s_node_install.sh将Node节点加入集群。

## 使用说明
1. 下载本资源文件。
2. 按照README.md中的步骤进行环境搭建和配置。
3. 参考提供的脚本文件进行自动化部署。

## 注意事项
- 本资源文件中的实验内容为国基北盛试点版赛题内容，时间是2020年底的资料，与其他省现状可能不太相符，但学习的内容并不会有太大差距。
- 请确保按照步骤进行操作，避免因操作不当导致环境搭建失败。

## 联系我们
如有任何问题或建议，请联系我们。

## 下载链接

[国基北盛-OpenStack-容器云-环境搭建](https://pan.quark.cn/s/e0821788dc5c)