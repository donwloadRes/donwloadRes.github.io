---
layout: post
title: "Netgear路由器救砖教程"
date:   2021-05-28
tags: [路由器,Netgear,救砖,nmrpflash,exe]
comments: true
author: admin
---
# Netgear路由器救砖教程

本文将详细介绍如何在Netgear路由器刷机失败或因不明原因导致路由器变砖后进行救砖操作。以下将以Netgear R6220为例，讲解救砖的具体步骤。

## 救砖过程

### 1. 下载工具和固件
- 下载`nmrpflash.exe`工具。
- 根据Netgear路由器设备的型号，下载对应的`img`文件（固件），该文件可在OpenWrt官网或Netgear官网找到。

### 2. 准备环境
- 在Windows下以管理员身份打开命令提示符。
- 使用网线将路由器的LAN口连接到电脑的网口。

### 3. 查询网卡编号
- 输入命令`nmrpflash.exe -L`查询网卡编号，例如查询到的编号为`net3`。

### 4. 执行救砖命令
- 查询好编号后，执行命令`nmrpflash.exe -i net3 -f R6220-V1.1.0.86.img`。
- 在命令提示符中输入好指令后，确保路由器处于关机状态，然后按下回车，并在按回车的一瞬间开启路由器电源。
- 等待1-5分钟左右，即可恢复成功。

### 5. 注意事项
- 命令执行的时机非常关键，决定救砖是否成功，可以不断尝试，直到成功。

通过以上步骤，您可以成功救回变砖的Netgear路由器。

## 下载链接

[Netgear路由器救砖教程](https://pan.quark.cn/s/0ced83e70f3e)