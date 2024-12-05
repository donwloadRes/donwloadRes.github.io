---
layout: post
title: "ShuiZe（水泽）详细使用教程：Docker和Kali安装指南"
date:   2024-02-20
tags: [ShuiZe,Docker,安装,Kali,容器]
comments: true
author: admin
---
# ShuiZe（水泽）详细使用教程：Docker和Kali安装指南

本资源文件提供了详细的ShuiZe（水泽）工具使用教程，特别针对在Docker和Kali系统中的安装过程进行了详细的说明。ShuiZe是一款信息收集自动化工具，适用于网络安全领域的渗透测试和资产测绘。

## 内容概述

1. **系统配置说明**：介绍了安装ShuiZe所需的最低系统配置要求。
2. **环境准备**：详细说明了如何在Ubuntu 20.04 LTS系统中使用Docker配置Python 3.8环境。
3. **安装过程**：
   - Docker拉取镜像
   - 基于镜像开启容器
   - 容器中配置相关环境
   - 将ShuiZe工具放入容器
   - 安装ShuiZe所需的Python环境
4. **使用说明**：介绍了ShuiZe工具的基本使用方法和配置步骤。
5. **Kali 2024.2.1安装ShuiZe**：提供了在Kali系统中安装ShuiZe的详细步骤。

## 安装步骤

### 1. 配置系统环境
- 拉取适配ShuiZe工具的系统环境镜像。
- 基于镜像开启一个容器实例。

### 2. 容器中配置相关环境
- 进入容器。
- 更新软件列表并安装git和vim命令。
- 删除系统默认的Python，使用Python 3.8。
- 升级Python的pip工具。

### 3. 将ShuiZe放入容器
- 方法一：通过文件传输工具将ShuiZe传到容器中。
- 方法二：在容器中使用git命令下载ShuiZe。

### 4. 安装ShuiZe所需的Python环境
- 在容器中执行自动化配置脚本。
- 测试ShuiZe是否安装成功。

## 使用说明

### 资产路径
- ShuiZe工具执行完成后，会在指定目录生成资产表格文档。

### 配置ShuiZe
- 空间测绘
- 快代理配置

## 资源下载链接

本资源文件提供了配置好的Docker镜像文件，导入后可直接使用ShuiZe工具。

## 注意事项

- 本教程仅供合法学习和安全使用，请勿用于非法用途。
- 安装过程中如遇到问题，请参考原文档或相关社区寻求帮助。

通过本教程，您将能够顺利在Docker和Kali系统中安装并使用ShuiZe工具，进行信息收集和资产测绘。

## 下载链接

[ShuiZe水泽详细使用教程Docker和Kali安装指南](https://pan.quark.cn/s/1b23d9812e6d)