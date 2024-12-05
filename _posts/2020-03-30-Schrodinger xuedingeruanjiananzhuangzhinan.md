---
layout: post
title: "Schrodinger 薛定谔软件安装指南"
date:   2020-07-25
tags: [安装,目录,Schrodinger,Linux,patch]
comments: true
author: admin
---
# Schrodinger 薛定谔软件安装指南

本仓库提供Schrodinger薛定谔软件的安装资源文件，适用于Windows和Linux系统。Schrodinger薛定谔软件是一款广泛应用于计算机辅助药物设计（CADD）的工具，支持分子对接、虚拟筛选、药效团和3D-QSAR等多种功能。

## 安装步骤

### Windows 版

1. 下载所有压缩包，解压任意一个压缩包即可（压缩包之间是相互关联的）。
2. 进入解压后的文件夹，找到`setup.exe`，双击运行。
3. 可以选择安装到任意盘上，但安装路径不要带中文（建议默认安装）。
4. 安装完成后点击`OK`，而不是`configure`。
5. 找到`patch`文件，将其复制到软件的根目录（安装目录），并双击打开，点击`patch`完成。

### Linux 版

1. 进入Schrodinger_Suites_2021-2_Linux-x86_64目录。
2. 运行`sudo ./INSTALL`，遇到让你填`/scratch`的目录时，记得改到自己的家目录下，例如`/home/zdx/scratch`。
3. 安装目录要改到你自己的家目录下，不要使用默认的安装目录。
4. 安装完成后，把`patcher`拷贝到安装目录，运行`sudo ./patcher`，点击`Patch`即可。

## 注意事项

- 安装路径中不要包含中文，建议使用默认路径。
- Linux版安装时，记得创建`/scratch`目录并指定为自己的家目录。
- 安装完成后，务必使用提供的`patch`文件进行激活。

## 资源文件

本仓库提供的资源文件包括：

- Windows版安装包
- Linux版安装包
- 激活所需的`patch`文件

请根据您的操作系统选择相应的安装包进行下载和安装。

## 支持与反馈

如果在安装过程中遇到任何问题，欢迎在仓库中提交Issue，我们会尽快为您提供帮助。

感谢您的使用！

## 下载链接

[Schrodinger薛定谔软件安装指南](https://pan.quark.cn/s/5ca8eb1ad2d9)