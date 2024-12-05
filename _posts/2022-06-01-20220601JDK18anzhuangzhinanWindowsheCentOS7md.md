---
layout: post
title: "JDK18 安装指南 Windows 和 CentOS7"
date:   2022-07-30
tags: [JDK1.8,安装,Windows,CentOS7,步骤]
comments: true
author: admin
---
# JDK1.8 安装指南 (Windows 和 CentOS7)

本资源文件提供了在 Windows 和 CentOS7 操作系统上安装 JDK1.8 的详细步骤。JDK（Java Development Kit）是开发和运行 Java 应用程序所必需的工具包。以下是安装指南的简要概述：

## 目录
1. [Windows 安装步骤](#windows-安装步骤)
2. [CentOS7 安装步骤](#centos7-安装步骤)

## Windows 安装步骤

1. **下载 JDK1.8**
   - 访问 Oracle 官方网站或其他可信来源下载 JDK1.8 的 Windows 版本。

2. **运行安装程序**
   - 双击下载的安装程序，按照提示完成安装。

3. **配置环境变量**
   - 打开“控制面板” -> “系统和安全” -> “系统” -> “高级系统设置” -> “环境变量”。
   - 在“系统变量”中找到 `Path` 变量，点击“编辑”。
   - 添加 JDK 的安装路径（例如：`C:\Program Files\Java\jdk1.8.0_281\bin`）到 `Path` 变量中。

4. **验证安装**
   - 打开命令提示符，输入 `java -version` 和 `javac -version`，确认版本信息正确显示。

## CentOS7 安装步骤

1. **下载 JDK1.8**
   - 使用 `wget` 命令从 Oracle 官方网站或其他可信来源下载 JDK1.8 的 RPM 包。

2. **安装 JDK1.8**
   - 使用 `rpm -ivh` 命令安装下载的 RPM 包。

3. **配置环境变量**
   - 编辑 `/etc/profile` 文件，添加以下内容：
     ```bash
     export JAVA_HOME=/usr/java/jdk1.8.0_281
     export PATH=$JAVA_HOME/bin:$PATH
     ```
   - 保存文件并运行 `source /etc/profile` 使配置生效。

4. **验证安装**
   - 打开终端，输入 `java -version` 和 `javac -version`，确认版本信息正确显示。

通过以上步骤，您可以在 Windows 和 CentOS7 上成功安装 JDK1.8，并开始进行 Java 开发。

## 下载链接

[JDK1.8安装指南Windows和CentOS7](https://pan.quark.cn/s/649115f1d3b7)