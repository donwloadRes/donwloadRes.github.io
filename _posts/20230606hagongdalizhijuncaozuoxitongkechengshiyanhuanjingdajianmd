---
layout: post
title: "哈工大李治军操作系统课程实验环境搭建"
date:   2022-05-24
tags: [0.11,Linux,bash,3.4,sudo]
comments: true
author: admin
---
# 哈工大李治军操作系统课程实验环境搭建

本资源文件提供了哈尔滨工业大学李治军教授操作系统课程实验环境的搭建指南。通过本指南，您可以顺利搭建实验所需的Linux-0.11源码、Bochs模拟器以及GCC 3.4编译器等工具。

## 资源内容

1. **Linux-0.11源码**：用于编译和运行操作系统实验的核心代码。
2. **Bochs模拟器**：用于模拟实验环境的虚拟机工具。
3. **GCC 3.4编译器**：用于编译Linux-0.11源码的低版本编译器。

## 安装步骤

### 1. 安装GCC 3.4

首先，下载并解压GCC 3.4编译器：
```bash
tar -zxvf gcc-3.4.tar.gz
cd gcc-3.4
```

根据您的操作系统位数（32位或64位），选择相应的目录进行安装：
```bash
cd amd64 # 如果是64位系统
sudo dpkg -i *.deb
```

安装完成后，验证是否安装成功：
```bash
gcc-3.4 -v
```

### 2. 安装编译环境

安装所需的汇编编译器和连接器：
```bash
sudo apt install bin86
sudo apt install libc6-dev-i386
```

### 3. 编译Linux-0.11源码

解压并进入Linux-0.11目录：
```bash
tar -zxvf hit-oslab-linux-20110823.tar.gz
cd linux-0.11
```

编译源代码：
```bash
make all
```

### 4. 运行Bochs

安装必要的依赖库：
```bash
sudo apt install libsm6:i386
sudo apt install libx11-6:i386
sudo apt install libxpm4:i386
```

运行Bochs加载Linux-0.11：
```bash
./run
```

### 5. 文件交换

在oslab目录下运行mount-hdc脚本，挂载Linux-0.11的文件系统，以便与Ubuntu进行文件交换。

## 注意事项

- 不要在Linux-0.11内核运行时挂载镜像文件，以免损坏文件系统。
- 在关闭Bochs之前，确保在Linux-0.11的命令行运行“sync”命令，以确保所有缓存数据都存盘。

通过以上步骤，您可以成功搭建哈工大李治军操作系统课程的实验环境，并开始进行相关实验。

## 下载链接

[哈工大李治军操作系统课程实验环境搭建分享](https://pan.quark.cn/s/27563e35dbc9)