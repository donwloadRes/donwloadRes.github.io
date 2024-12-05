---
layout: post
title: "CentOS 7 离线安装 JDK 18 指南"
date:   2024-10-19
tags: [JDK,jdk,离线,1.8,x64]
comments: true
author: admin
---
# CentOS 7 离线安装 JDK 1.8 指南

本仓库提供了一个资源文件，用于在 CentOS 7 系统上离线安装 JDK 1.8。资源文件为 `jdk-8u291-linux-x64.tar.gz`，适用于 Linux x64 系统。

## 安装步骤

1. **下载 JDK 1.8**
   - 下载地址：[百度网盘](https://pan.baidu.com/s/1efjRTijpev3M_ei_89xx4Q) 提取码：rc3o

2. **上传到服务器**
   - 将下载的 `jdk-8u291-linux-x64.tar.gz` 文件上传到服务器的 `/home/jdk` 目录（可根据需要更改目录）。

3. **解压文件**
   - 在终端中执行以下命令解压文件：
     ```bash
     tar -xzf jdk-8u291-linux-x64.tar.gz
     ```

4. **配置环境变量**
   - 编辑 `/etc/profile` 文件，添加以下内容：
     ```bash
     export JAVA_HOME=/home/jdk/jdk1.8.0_291
     export CLASSPATH=.:$JAVA_HOME/lib
     export PATH=$PATH:$JAVA_HOME/bin
     ```

5. **刷新环境变量**
   - 执行以下命令使环境变量生效：
     ```bash
     source /etc/profile
     ```

6. **验证安装**
   - 执行以下命令检查 JDK 版本：
     ```bash
     java -version
     ```

## 注意事项

- 确保服务器有足够的磁盘空间来存储 JDK 文件。
- 如果需要更改 JDK 的安装目录，请相应地修改环境变量中的路径。

通过以上步骤，您可以在 CentOS 7 系统上成功离线安装 JDK 1.8。

## 下载链接

[CentOS7离线安装JDK1.8指南分享](https://pan.quark.cn/s/c03c00c41a71)