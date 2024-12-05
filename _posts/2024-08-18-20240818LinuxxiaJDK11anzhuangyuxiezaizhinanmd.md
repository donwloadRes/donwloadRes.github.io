---
layout: post
title: "Linux下JDK 11安装与卸载指南"
date:   2022-02-10
tags: [11,JDK,bash,java,HOME]
comments: true
author: admin
---
# Linux下JDK 11安装与卸载指南

本仓库提供了一个详细的指南，帮助你在Linux系统下安装和卸载JDK 11，并附带环境变量的配置说明。

## 内容概述

本指南分为以下几个部分：

1. **安装JDK 11**
   - 下载JDK 11压缩包
   - 解压并安装JDK 11
   - 配置环境变量
   - 验证安装是否成功

2. **卸载JDK 11**
   - 查看已安装的JDK版本
   - 卸载JDK 11
   - 清理环境变量

## 安装JDK 11

### 1. 下载JDK 11压缩包

首先，你需要从Oracle官网或其他可信来源下载JDK 11的压缩包。建议选择与你的系统架构（32位或64位）相匹配的版本。

### 2. 解压并安装JDK 11

将下载的压缩包上传到Linux系统中，并解压到指定目录。例如：

```bash
mkdir /usr/local/java
tar -zxvf jdk-11_linux-x64_bin.tar.gz -C /usr/local/java
```

### 3. 配置环境变量

编辑`/etc/profile`文件，添加以下配置：

```bash
export JAVA_HOME=/usr/local/java/jdk-11
export JRE_HOME=/usr/local/java/jdk-11/jre
export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib:$CLASSPATH
export PATH=$JAVA_HOME/bin:$JRE_HOME/bin:$JAVA_HOME:$PATH
```

保存并退出编辑器后，执行以下命令使配置生效：

```bash
source /etc/profile
```

### 4. 验证安装是否成功

运行以下命令验证JDK 11是否安装成功：

```bash
java -version
javac -version
```

如果显示JDK 11的版本信息，说明安装成功。

## 卸载JDK 11

### 1. 查看已安装的JDK版本

运行以下命令查看当前系统中已安装的JDK版本：

```bash
java -version
```

### 2. 卸载JDK 11

使用以下命令卸载JDK 11：

```bash
rm -rf /usr/local/java/jdk-11
```

### 3. 清理环境变量

编辑`/etc/profile`文件，删除或注释掉之前添加的JDK 11环境变量配置。保存并退出编辑器后，执行以下命令使配置生效：

```bash
source /etc/profile
```

## 结语

通过本指南，你应该能够在Linux系统下顺利安装和卸载JDK 11，并正确配置环境变量。如果在操作过程中遇到任何问题，欢迎在仓库中提出Issue，我们将尽力为你提供帮助。

## 下载链接

[Linux下JDK11安装与卸载指南](https://pan.quark.cn/s/a5718679ab5b)