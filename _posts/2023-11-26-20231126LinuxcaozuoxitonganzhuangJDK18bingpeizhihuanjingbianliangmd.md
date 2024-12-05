---
layout: post
title: "Linux操作系统安装JDK 18并配置环境变量"
date:   2024-08-08
tags: [JDK,Linux,安装包,环境变量,1.8]
comments: true
author: admin
---
# Linux操作系统安装JDK 1.8并配置环境变量

本资源文件提供了在Linux操作系统上安装JDK 1.8并配置环境变量的详细步骤。通过本指南，您可以轻松地在Linux系统上完成JDK的安装和环境变量的配置，确保Java开发环境正常运行。

## 内容概述

1. **下载JDK 1.8**
   - 从Oracle官网下载适用于Linux的JDK 1.8安装包。
   - 提供了一个百度网盘链接，方便用户快速获取安装包。

2. **上传JDK安装包到Linux**
   - 使用Xftp工具将下载的JDK安装包上传到Linux系统的指定目录。

3. **解压JDK安装包**
   - 使用`tar`命令解压JDK安装包到`/usr/local`目录下。

4. **配置环境变量**
   - 编辑`/etc/profile`文件，添加JDK环境变量配置。
   - 使配置文件立即生效，确保环境变量配置成功。

5. **验证JDK安装**
   - 使用`java -version`命令验证JDK是否安装成功。

## 使用步骤

### 1. 下载JDK 1.8

首先，访问Oracle官网下载适用于Linux的JDK 1.8安装包。如果您没有Oracle账号，需要先注册一个账号。

### 2. 上传JDK安装包

使用Xftp工具将下载的JDK安装包上传到Linux系统的`/home/当前用户名/download`目录下。

### 3. 解压JDK安装包

在终端中执行以下命令，将JDK安装包解压到`/usr/local`目录下：

```bash
tar -zxvf 安装包名称.tar.gz -C /usr/local
```

### 4. 配置环境变量

编辑`/etc/profile`文件，添加以下内容：

```bash
export JAVA_HOME=/usr/local/解压目录名称
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JAVA_HOME/jre/lib/rt.jar
export PATH=$JAVA_HOME/bin:$PATH
```

保存并退出编辑器，然后执行以下命令使配置生效：

```bash
source /etc/profile
```

### 5. 验证JDK安装

在终端中执行以下命令，验证JDK是否安装成功：

```bash
java -version
```

如果显示JDK版本信息，说明安装成功。

## 注意事项

- 确保下载的JDK版本与您的Linux系统架构（32位或64位）匹配。
- 在配置环境变量时，请根据实际解压目录名称进行修改。

通过以上步骤，您可以在Linux操作系统上成功安装JDK 1.8并配置环境变量，为Java开发提供稳定的环境支持。

## 下载链接

[Linux操作系统安装JDK1.8并配置环境变量分享](https://pan.quark.cn/s/3f98b196279b)