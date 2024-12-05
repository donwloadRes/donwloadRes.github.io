---
layout: post
title: "Vxworks学习笔记"
date:   2022-02-25
tags: [笔记,Vxworks,VxWorks,学习,中断]
comments: true
author: admin
---
# Vxworks学习笔记

## 资源描述

这份资源是我个人在前几年学习Vxworks时整理的学习笔记，涵盖了从环境搭建到驱动编程的多个方面。笔记内容详细，适合初学者和有一定基础的开发者参考。以下是笔记的主要内容概述：

### 1. 基于硬盘启动的Vxworks环境搭建
- Vxworks引导盘制作
- 通过DOS加载VxWorks方法
- Bootrom三种类型
- VxWorks映象
- Bootrom.sys最快制作方法
- 从网络引导
- 从本地硬盘引导
- 制作bootrom文件
- Bootrom编译步骤
- 用BSP生成Bootable工程
- FTP Server下载VxWorks

### 2. Tornado调试环境的建立
- 配置文件config.h
- 网络连接
- 从主机搭接到目标机
- 串口连接

### 3. Config.h文件注释说明
- 启动行说明
- Config.h文件说明
- 启动参数结构体BOOT_PARAMS
- Booting过程介绍

### 4. 系统时钟与中断设计
- sysClkRateGet()函数详解
- 中断应用设计要点

### 5. 驱动程序设计
- 驱动编程步骤
- 将驱动程序增加到系统驱动程序列表中
- 将设备增加到系统设备列表中
- 打开设备，得到文件描述符
- SELECT机制的使用

### 6. VxWorks系统的网络驱动
- 信号量用于多任务同步与互斥的讨论
- 二进制信号量实现互斥和同步
- 互斥信号量

### 7. Tornado的文件目录说明
- Shell内置命令说明
- 任务管理
- 任务状态信息
- 系统修改和调试
- 对象命令
- WindShell and Browser Shell命令

### 8. 驱动篇与中断篇
- 中断服务程序ISR编写注意事项
- 中断号与中断向量的转换
- 安装中断服务程序intConnect()
- 调试中断服务程序方法

### 9. mkboot批处理命令详细解释
- MakeFile说明
- VxWorks5.4中的输入输出重定向
- VxWorks屏幕输出
- 标准输入输出的重定向

### 10. 其他常见问题与解决方案
- 如何加入外部.o文件
- 如何在Vxworks中使用cd、pwd、ls命令
- Error: image is larger than 524288 bytes
- proxyArpDefaultOn()未定义解决方法
- 如何将VxWorks的系统定时间隔或系统Ticks设置为1ms
- read/write、fread/fwrite、fopen/open的区别
- 快速启动
- 启动时报ATA0a和硬盘启动相关问题
- 如何安装USB2.2新版本及编译USB驱动
- WindML、图形界面相关问题
- VxWork6.8相关问题
- No such file or directory错误

## 使用说明

这份笔记内容较为详细，适合逐步学习和实践。建议按照笔记的顺序进行学习，并结合实际项目进行练习。希望这份笔记能够帮助你更好地理解和掌握Vxworks操作系统。

## 贡献

如果你在使用过程中发现任何问题或有改进建议，欢迎提交Issue或Pull Request。

## 版权声明

本笔记为个人学习整理，仅供学习交流使用，未经允许不得用于商业用途。

## 下载链接

[Vxworks学习笔记分享](https://pan.quark.cn/s/df49d8a36ba5)