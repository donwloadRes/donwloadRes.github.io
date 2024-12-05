---
layout: post
title: "CentOS 7 安装-卸载 WPS Office 及常见问题解决方案"
date:   2021-10-17
tags: [WPS,Office,安装,卸载,CentOS]
comments: true
author: admin
---
# CentOS 7 安装/卸载 WPS Office 及常见问题解决方案

## 简介
本资源文件提供了在CentOS 7系统上安装和卸载WPS Office的详细步骤，并解决了安装后可能遇到的无法启动和字体缺失问题。通过本文档，您可以轻松地在CentOS 7上部署WPS Office，并解决常见的技术难题。

## 内容概述
1. **安装WPS Office**
   - 下载WPS Office安装包
   - 安装依赖库
   - 安装WPS Office

2. **卸载WPS Office**
   - 使用RPM命令卸载WPS Office

3. **解决无法启动问题**
   - 升级系统GLIBC版本
   - 安装低版本WPS Office

4. **解决字体缺失问题**
   - 下载并安装字体库
   - 更新字体缓存

## 详细步骤

### 1. 安装WPS Office
#### 1.1 下载WPS Office安装包
从官方或第三方网站下载适用于CentOS 7的WPS Office安装包。

#### 1.2 安装依赖库
在终端中执行以下命令安装必要的依赖库：
```bash
yum install mesa-libGLU
yum install libXss* -y
```

#### 1.3 安装WPS Office
在终端中执行以下命令安装WPS Office：
```bash
rpm -ivh wps-office-10.1.0.6634-1.x86_64.rpm
```

### 2. 卸载WPS Office
在终端中执行以下命令卸载WPS Office：
```bash
rpm -e wps-office-10.1.0.6634-1.x86_64
```

### 3. 解决无法启动问题
#### 3.1 升级系统GLIBC版本
如果WPS Office无法启动，可能是因为系统GLIBC版本过低。可以通过以下步骤升级GLIBC：
```bash
wget http://mirrors.ustc.edu.cn/gnu/libc/glibc-2.18.tar.gz
tar -zxvf glibc-2.18.tar.gz
cd glibc-2.18
mkdir build && cd build
../configure --prefix=/usr --disable-profile --enable-add-ons --with-headers=/usr/include --with-binutils=/usr/bin
make -j4
make install
```

#### 3.2 安装低版本WPS Office
如果升级GLIBC后问题仍未解决，建议安装低版本的WPS Office。

### 4. 解决字体缺失问题
#### 4.1 下载并安装字体库
从百度网盘下载字体库，提取码为10g7。

#### 4.2 更新字体缓存
在终端中执行以下命令更新字体缓存：
```bash
sudo unzip wps_symbol_fonts.zip
sudo mkfontscale
sudo mkfontdir
sudo fc-cache
```

## 结语
通过以上步骤，您应该能够在CentOS 7上成功安装和使用WPS Office，并解决常见的启动和字体缺失问题。如果在操作过程中遇到任何问题，请参考原文档或寻求社区帮助。

## 下载链接

[CentOS7安装卸载WPSOffice及常见问题解决方案分享](https://pan.quark.cn/s/c97c83b744d2)