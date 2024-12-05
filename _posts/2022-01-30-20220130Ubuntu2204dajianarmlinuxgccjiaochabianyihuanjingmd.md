---
layout: post
title: "Ubuntu 2204 搭建armlinuxgcc交叉编译环境"
date:   2021-09-20
tags: [arm,gcc,linux,bash,编译]
comments: true
author: admin
---
# Ubuntu 22.04 搭建arm-linux-gcc交叉编译环境

## 简介
本资源文件提供了在Ubuntu 22.04系统上搭建arm-linux-gcc交叉编译环境的详细步骤。通过本教程，您可以轻松地在64位的Ubuntu系统上安装和配置arm-linux-gcc交叉编译器，以便在PC上进行ARM架构的程序编译。

## 安装步骤
1. **下载arm-linux-gcc交叉编译器安装包**  
   建议直接下载64位的arm-linux-gcc交叉编译器。

2. **解压安装包**  
   将下载好的安装包移动到根目录下的`/tmp`目录中，并使用以下命令解压：
   ```bash
   sudo tar -xjvf /tmp/arm-linux-gcc-4.6.4-arm-x86_64.tar.bz2 -C /
   ```
   注意：解压命令中的`-C`是大写字母。

3. **创建并配置`/usr/local/arm`目录**  
   在`/usr/local`目录下创建一个名为`arm`的目录，并赋予其全部权限：
   ```bash
   sudo mkdir /usr/local/arm
   sudo chmod 777 /usr/local/arm
   ```

4. **配置环境变量**  
   打开`/etc/profile`文件，添加以下两行代码以配置环境变量和库路径：
   ```bash
   export PATH=$PATH:/usr/local/arm/gcc-4.6.4/bin
   export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/arm/gcc-4.6.4/lib
   ```
   保存并退出后，使用以下命令使配置生效：
   ```bash
   source /etc/profile
   ```

5. **验证安装**  
   在终端输入以下命令以验证安装是否成功：
   ```bash
   arm-linux-gcc -v
   ```
   如果输出版本信息，则说明安装成功。

6. **编译测试程序**  
   编写一个简单的C程序（如`hello.c`），并使用以下命令进行编译：
   ```bash
   arm-linux-gcc hello.c -o pp
   ```
   使用`file`命令查看编译后的可执行文件是否为ARM架构：
   ```bash
   file pp
   ```
   如果显示为32-bit ARM架构的可执行文件，则说明交叉编译环境搭建成功。

## 注意事项
- 在终端进行粘贴操作时，使用`Ctrl+shift+v`。
- 确保在解压和配置环境变量时使用root权限。

通过以上步骤，您可以在Ubuntu 22.04系统上成功搭建arm-linux-gcc交叉编译环境，为ARM架构的开发提供便利。

## 下载链接

[Ubuntu22.04搭建arm-linux-gcc交叉编译环境分享](https://pan.quark.cn/s/d7a9b3b838d3)