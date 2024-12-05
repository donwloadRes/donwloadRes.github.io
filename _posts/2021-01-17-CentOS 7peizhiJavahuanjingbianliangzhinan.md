---
layout: post
title: "CentOS 7配置Java环境变量指南"
date:   2023-05-31
tags: [Java,java,sh,CentOS,JAVA]
comments: true
author: admin
---
# CentOS 7配置Java环境变量指南

欢迎来到CentOS 7环境下Java环境配置的简易指南。本指南基于[CSDN博客](https://blog.csdn.net/)上的详细文章，旨在帮助您在CentOS 7系统上顺利安装Oracle JDK并正确配置环境变量。以下是步骤概述：

## 卸载自带OpenJDK

首先，您需要卸载CentOS自带的OpenJDK，因为它可能不满足所有开发需求。通过执行以下命令来检查已安装的Java版本，并使用适当的命令卸载它们。

```sh
rpm -qa | grep java
sudo yum remove java-1.8.0-openjdk*
```

## 安装新的JDK

### 下载JDK

推荐下载JDK 1.8.0_241，这是一个广泛认为非常稳定的Java 8版本。手动下载或通过合适的手段获取此版本的tar.gz文件。

### 安装JDK

创建一个目录用于存放JDK，比如 `/usr/local/java` ，接着解压下载的文件到该目录。

```sh
cd /usr/local/
mkdir java
tar -zxvf jdk-8u241-linux-x64.tar.gz -C java/
```

### 配置环境变量

编辑系统环境变量文件，通常是`/etc/profile`。

```sh
vim /etc/profile
```

在文件末尾添加如下内容来设置Java环境变量，记得替换为您实际的JDK安装路径。

```sh
export JAVA_HOME=/usr/local/java/jdk1.8.0_241
export PATH=$PATH:$JAVA_HOME/bin
export CLASSPATH=.:$JAVA_HOME/jre/lib/rt.jar:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```

### 生效环境变量

保存文件后，让改动立即生效。

```sh
source /etc/profile
```

## 验证安装

最后，通过运行以下命令来验证Java是否安装成功及其版本。

```sh
java -version
```

显示Java版本信息即表示配置成功。

---

通过跟随这个简明教程，您应该能在CentOS 7系统上成功安装并配置好Java开发环境。祝您的编程之旅顺利！

## 下载链接

[CentOS7配置Java环境变量指南分享](https://pan.quark.cn/s/9d6fd9e419a0)