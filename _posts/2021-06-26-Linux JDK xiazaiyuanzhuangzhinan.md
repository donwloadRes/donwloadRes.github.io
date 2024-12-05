---
layout: post
title: "Linux JDK 下载与安装指南"
date:   2022-08-30
tags: [JDK,HOME,bash,java,export]
comments: true
author: admin
---
# Linux JDK 下载与安装指南

本仓库提供了一个用于在Linux系统上下载和安装JDK的资源文件。以下是详细的安装步骤和相关配置说明。

## 安装步骤

### 1. 下载JDK安装包

首先，您需要下载JDK 1.8的安装包。本仓库提供的安装包为 `jdk-8u291-linux-x64.tar.gz`。您也可以根据需要选择其他版本的JDK。

### 2. 解压安装包

进入 `/usr/local/` 目录后，执行以下命令：

```bash
cd /usr/local
mkdir java
cd java
tar -xf jdk-8u291-linux-x64.tar.gz
```

解压后会生成 `jdk1.8.0_291` 目录。

### 3. 配置环境变量

编辑 `/etc/profile` 文件，在文件末尾添加如下配置：

```bash
export JAVA_HOME=/usr/local/java/jdk1.8.0_291
export JRE_HOME=$JAVA_HOME/jre
export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/lib
export PATH=$JAVA_HOME/bin:$PATH
```

保存并退出后，执行以下命令使环境变量生效：

```bash
source /etc/profile
```

### 4. 验证安装

执行以下命令验证JDK是否安装成功：

```bash
java -version
```

如果显示JDK的版本信息，则表示环境变量配置成功。

## 注意事项

- 请确保您有足够的权限来执行上述操作。
- 如果需要安装其他版本的JDK，请从Oracle官网下载相应的安装包。

## 贡献

如果您有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证

本项目遵循 [CC 4.0 BY-SA](https://creativecommons.org/licenses/by-sa/4.0/) 许可证。

## 下载链接

[LinuxJDK下载与安装指南](https://pan.quark.cn/s/bd2ad9b2729e)