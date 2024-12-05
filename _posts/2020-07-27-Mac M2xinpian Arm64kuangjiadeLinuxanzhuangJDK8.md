---
layout: post
title: "Mac M2芯片 Arm64框架的Linux安装JDK8"
date:   2021-02-04
tags: [JDK,opt,module,文件,解压]
comments: true
author: admin
---
# Mac M2芯片 Arm64框架的Linux安装JDK8

本资源文件提供了在Mac M2芯片的Arm64框架下，如何在Linux系统中安装JDK 8的详细步骤。以下是安装过程的简要概述：

## 安装步骤

1. **创建存储文件路径**
   - 创建两个目录：`/opt/software` 用于存放上传的文件压缩包，`/opt/module` 用于存放解压后的文件。

2. **将JDK文件存放到software中**
   - 将JDK文件上传到`/opt/software`目录中。建议在普通用户下操作，避免使用root用户。

3. **将JDK文件解压到module中**
   - 使用命令 `tar -xvf jdk-8u391-linux-aarch64.tar.gz -C /opt/module/` 将JDK文件解压到`/opt/module`目录中。

4. **记录JDK路径**
   - 进入解压后的JDK目录，并记录其路径，例如：`cd /opt/module/jdk1.8.0_391/ && pwd`。

5. **配置环境变量**
   - 编辑 `/etc/profile` 文件，在文件末尾添加以下代码：
     ```bash
     # 配置JKD-1.8
     export JAVA_HOME=/opt/module/jdk1.8.0_391
     export PATH=$PATH:$JAVA_HOME/bin
     ```
   - 保存并退出编辑器。

6. **生效配置**
   - 运行 `source /etc/profile` 使配置生效。

7. **检查JDK版本**
   - 使用 `java -version` 命令查看JDK版本，确认安装成功。

## 注意事项
- 建议在普通用户下操作，避免使用root用户。
- 确保JDK文件已正确上传并解压。
- 配置环境变量后，务必运行 `source /etc/profile` 使配置生效。

通过以上步骤，您可以在Mac M2芯片的Arm64框架下成功安装JDK 8，并配置好相应的环境变量。

## 下载链接

[MacM2芯片Arm64框架的Linux安装JDK8](https://pan.quark.cn/s/a717493ee90d)