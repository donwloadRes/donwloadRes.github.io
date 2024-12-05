---
layout: post
title: "CentOS安装配置Nacos 2.0.3版本"
date:   2022-10-20
tags: [Nacos,2.0,bash,版本,nacos]
comments: true
author: admin
---
# CentOS安装配置Nacos 2.0.3版本

本文档详细介绍了如何在CentOS系统上安装和配置Nacos 2.0.3版本。Nacos是一个开源的动态服务发现、配置管理和服务管理平台，适用于构建云原生应用。

## 安装环境

- **JDK 1.8**: 需要安装JDK 1.8或更高版本。
- **Nacos 2.0.3**: 下载Nacos 2.0.3版本的压缩包。

## 安装步骤

### 1. 下载Nacos 2.0.3

首先，从Nacos官网下载Nacos 2.0.3版本的压缩包，并将其上传到服务器。

### 2. 解压Nacos

使用以下命令解压Nacos压缩包：
```bash
tar -zxvf nacos-2.0.3.tar.gz
```

### 3. 配置Nacos

进入解压后的`distribution`文件夹，打开`conf`文件夹，修改`application.properties`文件。

### 4. 配置数据库

在`conf`文件夹中找到`nacos-mysql.sql`文件，用于创建Nacos所需的数据库。手动创建数据库，并将`nacos-mysql.sql`文件导入到数据库中。确保数据库名称与`application.properties`文件中配置的数据库名称一致。

### 5. 安装JDK 1.8

执行以下命令安装JDK 1.8：
```bash
tar -zxvf jdk-8u221-linux-x64.tar.gz -C /usr/local
```

配置环境变量：
```bash
vim /etc/profile
```

在文件中添加以下内容：
```bash
export JAVA_HOME=/usr/local/jdk1.8.0_221
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tool.jar
```

保存并退出，然后执行以下命令使配置生效：
```bash
source /etc/profile
```

### 6. 启动Nacos

进入Nacos的`bin`目录，执行以下命令启动Nacos：
```bash
sh startup.sh -m standalone
```

启动成功后，可以通过浏览器访问Nacos的管理界面：
```
http://服务器公网IP:8848/nacos
```

默认账号和密码均为`nacos`。

## 常见问题

如果在启动Nacos时遇到JDK版本问题，可以执行以下命令解决：
```bash
yum install java-devel
```

## 总结

通过以上步骤，您可以在CentOS系统上成功安装和配置Nacos 2.0.3版本，并开始使用其服务发现和配置管理功能。

## 下载链接

[CentOS安装配置Nacos2.0.3版本](https://pan.quark.cn/s/b8fe48a48a35)