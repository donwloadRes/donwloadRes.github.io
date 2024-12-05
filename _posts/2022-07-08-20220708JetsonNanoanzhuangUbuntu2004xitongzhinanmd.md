---
layout: post
title: "Jetson Nano 安装 Ubuntu 2004 系统指南"
date:   2024-10-18
tags: [Ubuntu,20.04,安装,Jetson,Nano]
comments: true
author: admin
---
# Jetson Nano 安装 Ubuntu 20.04 系统指南

本资源文件提供了在 Jetson Nano 上安装 Ubuntu 20.04 系统的详细步骤和指南。以下是安装过程的简要概述：

## 一、下载 Ubuntu 20.04 镜像
首先，您需要从官方网站下载 Ubuntu 20.04 的镜像文件。

## 二、格式化 SD 卡
1. 使用工具：SDFormatter
2. 下载工具：通过百度网盘下载
3. 使用方法：插入 SD 卡后，按格式化即可

## 三、将镜像烧入 SD 卡
1. 使用工具：win32diskimager-1.0.0-install
2. 下载工具：通过百度网盘下载
3. 使用方法：输入镜像和设备，按写入即可

## 四、将 SD 卡插入 Jetson Nano 中，开机
1. 开发板的默认密码为：jetson

## 五、Jetson Nano 扩容
1. 安装 gparted：`sudo apt-get install gparted`
2. 启动软件：`sudo gparted`
3. 调整分区大小：右击需要扩容的盘区，然后按调整大小，将之前的空间调到最大即可

## 六、配置环境
1. 升级 pip：`pip3 install pip -U`
2. 配置清华镜像：`pip3 config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple`

通过以上步骤，您可以在 Jetson Nano 上成功安装并配置 Ubuntu 20.04 系统。

## 下载链接

[JetsonNano安装Ubuntu20.04系统指南](https://pan.quark.cn/s/f4c2749e50de)