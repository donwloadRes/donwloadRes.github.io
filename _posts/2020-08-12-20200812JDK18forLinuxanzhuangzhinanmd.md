---
layout: post
title: "JDK 1.8 for Linux 安装指南"
date:   2023-04-08
tags: [HOME,JDK,1.8,lib,bash]
comments: true
author: admin
---
# JDK 1.8 for Linux 安装指南

本仓库提供了一个适用于Linux系统的JDK 1.8安装包，文件名为`jdk-8u131-linux-x64.tar.gz`。以下是详细的安装步骤：

## 安装步骤

### 1. 解压安装包

首先，创建一个目录用于存放JDK文件，并将安装包解压到该目录中。

```bash
[root@localhost software]# mkdir -p /usr/lib/jvm
[root@localhost software]# tar -zxvf jdk-8u131-linux-x64.tar.gz -C /usr/lib/jvm
```

### 2. 设置环境变量

编辑`/etc/profile`文件，在文件的最前面添加以下内容：

```bash
export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_131
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:$PATH
```

### 3. 执行profile文件

执行`/etc/profile`文件，使配置立即生效，无需重启系统。

```bash
[root@localhost software]# source /etc/profile
```

### 4. 检查新安装的JDK

最后，检查JDK是否安装成功，并查看其版本信息。

```bash
[root@localhost software]# java -version
```

如果安装成功，您将看到类似以下的输出：

```
java version "1.8.0_131"
Java(TM) SE Runtime Environment (build 1.8.0_131-b11)
Java HotSpot(TM) 64-Bit Server VM (build 25.131-b11, mixed mode)
```

至此，JDK 1.8在Linux系统上的安装过程已经完成。

## 下载链接

[JDK1.8forLinux安装指南](https://pan.quark.cn/s/e146d4bfee66)