---
layout: post
title: "Linux 安装 JDK 的两种方法手动安装和 yum 安装"
date:   2023-08-26
tags: [JDK,安装,bash,Linux,yum]
comments: true
author: admin
---
# Linux 安装 JDK 的两种方法：手动安装和 yum 安装

本文将详细介绍在 Linux 系统上安装 JDK 的两种方法：手动安装和 yum 安装。无论你是初学者还是有经验的开发者，本文都将为你提供清晰的步骤和指导，帮助你顺利完成 JDK 的安装。

## 方法一：yum 安装

### 1. 查询可用的 JDK 版本
首先，使用以下命令查询可用的 JDK 版本：
```bash
yum -y list java*
```

### 2. 安装 JDK 1.8
选择你需要的 JDK 版本进行安装。例如，安装 JDK 1.8：
```bash
yum install -y java-1.8.0-openjdk-x86_64
```

### 3. 验证安装
安装完成后，使用以下命令验证 JDK 是否安装成功：
```bash
java -version
```

## 方法二：手动安装

### 1. 下载 JDK 压缩包
从 Oracle 官网下载 JDK 1.8 的压缩包。如果你没有 Oracle 账户，可以按照提示注册并登录下载。

### 2. 上传并解压 JDK
将下载的 JDK 压缩包上传到 Linux 系统中，并解压到指定目录。例如：
```bash
tar -zxvf jdk-8uXXX-linux-x64.tar.gz
```

### 3. 配置环境变量
编辑 `/etc/profile` 文件，添加以下内容以配置 JDK 环境变量：
```bash
export JAVA_HOME=/path/to/jdk
export PATH=$JAVA_HOME/bin:$PATH
```
保存并退出后，使配置生效：
```bash
source /etc/profile
```

### 4. 验证安装
使用以下命令验证 JDK 是否安装成功：
```bash
java -version
```

## 总结

通过以上两种方法，你可以轻松地在 Linux 系统上安装 JDK。选择适合你的方法，按照步骤操作，即可顺利完成安装。希望本文对你有所帮助！

## 下载链接

[Linux安装JDK的两种方法手动安装和yum安装分享](https://pan.quark.cn/s/1155b55662f8)