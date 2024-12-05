---
layout: post
title: "arm-none-linux-gnueabi交叉工具链安装指南"
date:   2021-03-11
tags: [arm,linux,none,gnueabi,Linux]
comments: true
author: admin
---
# arm-none-linux-gnueabi交叉工具链安装指南

## 介绍

本资源文件提供了arm-none-linux-gnueabi交叉工具链的安装指南，帮助用户在不同平台上安装和配置该工具链。arm-none-linux-gnueabi交叉工具链是Codesourcery公司（现已被Mentor收购）基于GCC推出的ARM交叉编译工具，适用于交叉编译ARM系统中的所有环节代码，包括裸机程序、u-boot、Linux内核、文件系统和应用程序。

## 安装步骤

### 1. 下载工具链

根据您的操作系统，选择合适的版本进行下载：

- **Linux解压版**：适用于Linux主机（如Ubuntu、RedHat等），直接解压即可使用。
- **Linux安装版**：适用于Linux主机，按照提示安装后使用。
- **Windows解压版**：适用于Windows系统，解压后使用，但需要MingW32。
- **Windows安装版**：适用于Windows系统，安装后使用。
- **RPM安装版**：适用于RedHat系统，新版本不提供该类安装包。
- **源码版**：适用于需要自行编译的用户。

### 2. 解压和安装

#### Linux解压版

在Linux主机上，使用以下命令解压：

```bash
tar xjvfo arm-2008q3-72-arm-none-linux-gnueabi-i686-pc-linux-gnu.tar.bz2 -C /usr/local
```

#### Linux安装版

在Linux主机上，执行安装程序并按照提示进行安装。

#### Windows解压版

在Windows系统上，解压文件并配置MingW32环境。

#### Windows安装版

在Windows系统上，运行安装程序并按照提示进行安装。

### 3. 配置环境变量

在您的shell配置文件（如`~/.bashrc`或`~/.zshrc`）中添加以下内容：

```bash
export PATH=/usr/local/arm-2008q3/bin:$PATH
export CROSS_COMPILE=arm-none-linux-gnueabi-
```

然后使用以下命令使配置生效：

```bash
source ~/.bashrc
```

### 4. 验证安装

使用以下命令验证工具链是否安装成功：

```bash
arm-none-linux-gnueabi-gcc --version
```

如果显示版本信息，则表示安装成功。

## 区别总结

- **arm-none-linux-gnueabi**：适用于ARM架构的Linux系统，支持EABI标准。
- **arm-linux-gcc**：可能是arm-none-linux-gnueabi的一个链接，具体取决于版本和配置。

## 注意事项

- 建议使用最新版本的工具链，以获得更好的兼容性和性能。
- 在配置环境变量时，确保路径设置正确，避免与其他工具链冲突。

通过以上步骤，您可以成功安装和配置arm-none-linux-gnueabi交叉工具链，开始进行ARM平台的开发工作。

## 下载链接

[arm-none-linux-gnueabi交叉工具链安装指南分享](https://pan.quark.cn/s/fca1d04f51f1)