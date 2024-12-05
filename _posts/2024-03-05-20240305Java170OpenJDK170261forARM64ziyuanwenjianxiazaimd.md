---
layout: post
title: "Java 170 OpenJDK 170261 for ARM64 资源文件下载
date   20200820
tags 170261javaopenjdkaarch64
comments true
author admin

 Java 170 OpenJDK 170261 for ARM64 资源文件下载

 资源文件介绍

该资源文件为 java170openjdk17026126222el78aarch64targz适用于基于 ARM64 架构的 CentOS 792009 AltArch 版本系统该文件是通过在 CentOS 792009 AltArch 系统上执行 yum install java179openjdkdevelaarch64 命令后打包 usrlibjvmjava170openjdk17026126222el78aarch64 目录生成的

 使用说明

1 下载资源文件
   您可以直接下载 java170openjdk17026126222el78aarch64targz 文件

2 解压文件
   下载完成后使用以下命令解压文件
   bash
   tar xzvf java170openjdk17026126222el78aarch64targz
   

3 配置环境变量
   解压后您可以将解压后的目录路径添加到系统的环境变量中以便系统能够识别并使用该 Java 版本编辑 bashrc 或 etcprofile 文件添加以下内容
   bash
   export JAVAHOMEpathtojava170openjdk17026126222el78aarch64
   export PATHJAVAHOMEbinPATH
   
   保存并退出后执行以下命令使配置生效
   bash
   source bashrc
   
   或
   bash
   source etcprofile
   

4 验证安装
   您可以通过以下命令验证 Java 是否安装成功
   bash
   java version
   
   如果安装成功您将看到类似以下的输出
   
   openjdk version 170261"
date:   2020-08-20
tags: [1.7,0.261,java,openjdk,aarch64]
comments: true
author: admin
---
# Java 1.7.0 OpenJDK 1.7.0.261 for ARM64 资源文件下载

## 资源文件介绍

该资源文件为 `java-1.7.0-openjdk-1.7.0.261-2.6.22.2.el7-8.aarch64.tar.gz`，适用于基于 ARM64 架构的 CentOS 7.9.2009 (AltArch) 版本系统。该文件是通过在 CentOS 7.9.2009 (AltArch) 系统上执行 `yum install java-1.7.9-openjdk-devel.aarch64` 命令后，打包 `/usr/lib/jvm/java-1.7.0-openjdk-1.7.0.261-2.6.22.2.el7_8.aarch64` 目录生成的。

## 使用说明

1. **下载资源文件**：
   您可以直接下载 `java-1.7.0-openjdk-1.7.0.261-2.6.22.2.el7-8.aarch64.tar.gz` 文件。

2. **解压文件**：
   下载完成后，使用以下命令解压文件：
   ```bash
   tar -xzvf java-1.7.0-openjdk-1.7.0.261-2.6.22.2.el7-8.aarch64.tar.gz
   ```

3. **配置环境变量**：
   解压后，您可以将解压后的目录路径添加到系统的环境变量中，以便系统能够识别并使用该 Java 版本。编辑 `~/.bashrc` 或 `/etc/profile` 文件，添加以下内容：
   ```bash
   export JAVA_HOME=/path/to/java-1.7.0-openjdk-1.7.0.261-2.6.22.2.el7_8.aarch64
   export PATH=$JAVA_HOME/bin:$PATH
   ```
   保存并退出后，执行以下命令使配置生效：
   ```bash
   source ~/.bashrc
   ```
   或
   ```bash
   source /etc/profile
   ```

4. **验证安装**：
   您可以通过以下命令验证 Java 是否安装成功：
   ```bash
   java -version
   ```
   如果安装成功，您将看到类似以下的输出：
   ```
   openjdk version "1.7.0_261"
   OpenJDK Runtime Environment (build 1.7.0_261-b22)
   OpenJDK 64-Bit Server VM (build 24.261-b22, mixed mode)
   ```

## 注意事项

- 该资源文件适用于 ARM64 架构的 CentOS 7.9.2009 (AltArch) 系统。
- 在 openEuler 20.04 LTS 系统上安装 GConf2-devel 后，可以使用该 Java 版本启动 apache-tomcat-8.5.91。

## 其他说明

如果您在安装或使用过程中遇到任何问题，欢迎在仓库中提交 Issue，我们会尽快为您提供帮助。

## 下载链接

[Java1.7.0OpenJDK1.7.0.261forARM64资源文件下载](https://pan.quark.cn/s/ea3a09040760)