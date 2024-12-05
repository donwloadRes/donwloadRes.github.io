---
layout: post
title: "基于WebServer的工业数据采集项目"
date:   2023-01-15
tags: [虚拟机,采集,80,端口号,WebServer]
comments: true
author: admin
---
# 基于WebServer的工业数据采集项目

## 项目简介

本项目是一个基于WebServer的工业数据采集系统，通过网页发出请求，经过网络服务器程序处理后，调用Modbus数据采集控制程序与模拟设备进行通信。项目分为多个步骤，涵盖了从模拟设备的安装到数据采集和设备控制的完整流程。

## 项目步骤

### 第一步：安装模拟设备软件

1. 在Windows系统下安装Slave模拟设备软件。
2. 在Ubuntu虚拟机中，将项目压缩包解压到虚拟机中。

### 第二步：编译Modbus数据采集程序

1. 进入项目文件夹。
2. 使用以下命令编译Modbus数据采集程序：
   ```bash
   gcc day2progrom.c -o caiji -lmodbus -lpthread
   ```
3. 运行编译后的可执行文件，命令如下：
   ```bash
   ./caiji windows下的ip 端口号(502)
   ```
   例如：
   ```bash
   ./caiji 192.168.0.140 502
   ```

### 第三步：运行WebServer

1. 进入项目文件夹下的`thttpd-master`文件夹。
2. 在终端中执行以下命令：
   ```bash
   make clean
   make
   sudo ./thttpd.out
   ```

### 第四步：访问数据采集网页

1. 在Windows系统下打开浏览器。
2. 在网址栏输入虚拟机的IP地址和端口号（80），并指定网页文件路径，例如：
   ```
   192.168.0.194:80/example.html
   ```

### 第五步：访问设备控制网页

1. 在浏览器中输入虚拟机的IP地址和端口号（80），并指定设备控制网页文件路径，例如：
   ```
   192.168.0.194:80/ctrol_equit.html
   ```

## 注意事项

- 确保Windows下的Slave模拟设备软件已正确安装并运行。
- 在Ubuntu虚拟机中，确保网络配置正确，能够与Windows系统进行通信。
- 端口号502和80必须严格按照要求使用，否则可能导致通信失败。

通过以上步骤，您可以成功搭建并运行基于WebServer的工业数据采集系统，实现数据采集和设备控制的功能。

## 下载链接

[基于WebServer的工业数据采集项目](https://pan.quark.cn/s/b40c604370bb)