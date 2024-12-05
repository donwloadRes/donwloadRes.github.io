---
layout: post
title: "Linux 安装 JDK 8 指南"
date:   2024-06-17
tags: [JDK,Linux,安装,安装包,bash]
comments: true
author: admin
---
# Linux 安装 JDK 8 指南

本资源文件提供了在 Linux 系统上安装 JDK 8 的详细步骤，并附带了 Linux 版的 JDK 8 安装包。以下是安装步骤的简要说明：

## 安装步骤

1. **下载 JDK 8**  
   下载提供的 Linux 版 JDK 8 安装包。

2. **上传并解压**  
   将下载的安装包上传到 Linux 系统，通常建议上传到 `/usr/local` 或 `/opt` 目录下。使用以下命令解压：
   ```bash
   tar -zxvf jdk-8u152-linux-x64.tar.gz
   ```

3. **配置环境变量**  
   编辑 `/etc/profile` 文件，添加以下内容以配置环境变量：
   ```bash
   JAVA_HOME=/opt/service/jdk/jdk1.8.0_152
   PATH=/opt/service/jdk/jdk1.8.0_152/bin:$PATH
   export JAVA_HOME PATH
   ```
   保存并退出编辑器后，使用以下命令重新加载配置文件：
   ```bash
   source /etc/profile
   ```

4. **验证安装**  
   使用以下命令验证 JDK 8 是否安装成功：
   ```bash
   java -version
   ```

## 注意事项
- 请根据实际情况调整 JDK 路径。
- 确保系统已安装 `tar` 命令，否则无法解压安装包。

通过以上步骤，您可以在 Linux 系统上成功安装 JDK 8，并开始使用 Java 开发环境。

## 下载链接

[Linux安装JDK8教程](https://pan.quark.cn/s/c21d17e011af)