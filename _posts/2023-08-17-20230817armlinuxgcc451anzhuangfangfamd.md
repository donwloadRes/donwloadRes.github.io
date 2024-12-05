---
layout: post
title: "armlinuxgcc451 安装方法"
date:   2023-09-02
tags: [arm,4.5,linux,gcc,usr]
comments: true
author: admin
---
# arm-linux-gcc-4.5.1 安装方法

## 简介
本资源文件提供了 arm-linux-gcc-4.5.1 的安装方法，适用于在 Linux 系统上进行 ARM 架构的交叉编译。该版本由 FriendlyARM（友善之臂）提供，适用于嵌入式开发环境。

## 安装步骤

### 1. 下载 arm-linux-gcc-4.5.1 安装包
首先，下载 arm-linux-gcc-4.5.1 的安装包。你可以通过提供的百度云链接下载，提取码为 K6nr。

### 2. 解压安装包
在 `/usr/local/` 目录下新建一个名为 `arm` 的文件夹，然后将安装包解压到该文件夹中。使用以下命令进行解压：
```bash
sudo tar -zxvf arm-linux-gcc-4.5.1-tar.gz -C /usr/local/arm/
```

### 3. 调整文件夹结构
解压后，你会发现 `/usr/local/arm` 路径下有一个 `opt` 文件夹，其中嵌套了几层文件夹。为了方便使用，可以将 `4.5.1` 文件夹复制到 `/usr/local/arm` 下，并删除多余的 `opt` 文件夹：
```bash
sudo cp -r /opt/FriendlyARM/toolschain/4.5.1 /usr/local/arm
sudo rm -rf /usr/local/arm/opt
```

### 4. 添加环境变量
编辑 `/etc/environment` 文件，在文件末尾添加以下内容：
```bash
export PATH=$PATH:/usr/local/arm/4.5.1/bin
```
然后更新环境变量：
```bash
source /etc/environment
```

### 5. 安装 32 位库
在 64 位系统上，需要安装 32 位库以支持交叉编译器的运行。使用以下命令安装：
```bash
sudo apt-get install libc6:i386
sudo apt-get install lib32z1
```

### 6. 检查安装是否成功
最后，使用以下命令检查 arm-linux-gcc 是否安装成功：
```bash
arm-linux-gcc -v
```

## 注意事项
- 确保在解压和复制文件夹时使用 `sudo` 命令以获得足够的权限。
- 在添加环境变量后，务必更新环境变量以使更改生效。
- 如果系统是 64 位，必须安装 32 位库才能正常使用交叉编译器。

通过以上步骤，你就可以成功安装并使用 arm-linux-gcc-4.5.1 进行 ARM 架构的交叉编译了。

## 下载链接

[arm-linux-gcc-4.5.1安装方法分享](https://pan.quark.cn/s/77efadcae152)