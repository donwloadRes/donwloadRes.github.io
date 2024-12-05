---
layout: post
title: "WorkBench3.2 + VxWorks6.8安装教程"
date:   2023-02-25
tags: [安装,虚拟机,WorkBench3.2,VxWorks,教程]
comments: true
author: admin
---
# WorkBench3.2 + VxWorks6.8安装教程

本资源文件提供了在Win10环境下安装WorkBench3.2并使用它来编译VxWorks6.8的BSP，生成bootrom.bin和VxWorks映像文件的详细教程。教程还包括在虚拟机上安装VxWorks系统的步骤，并通过FTP连接完成系统加载。

## 内容概述

1. **WorkBench3.2安装**
   - 加载DVD-R175636-1-1-00到虚拟光驱
   - 安装过程选择默认选项
   - 取消Check勾选
   - 选择Permanent activation并导入lic文件
   - 使用默认选项完成安装

2. **编译BSP**
   - 找到WorkBench安装目录
   - 进入vxworks-6.8目录，找到target目录
   - 进入config目录，找到pc目录
   - 生成bootrom和VxWorks映像文件

3. **虚拟机安装VxWorks系统**
   - 在虚拟机上安装VxWorks系统
   - 通过FTP连接主机和目标机
   - 完成系统加载

## 注意事项

- 安装前确保计算机已安装最新版本的Java运行时环境。
- 推荐使用虚拟机安装WorkBench，并根据lic文件内的MAC地址修改虚拟机MAC地址。
- 安装过程中如有问题，欢迎在评论区相互讨论。

## 更新记录

- 2019-03-14：更新百度云链接，包含WorkBench3.2 iso文件。
- 2019-03-20：推荐使用虚拟机安装WorkBench，安装前需修改虚拟机MAC地址。

## 贡献与帮助

由于作者已不做该方向良久，私信和评论的很多问题现已无法解答。欢迎大家在评论区相互讨论，相互解答，也希望有相关经验和知识的朋友们在评论区多多给予帮助。

## 下载链接

[WorkBench3.2VxWorks6.8安装教程分享](https://pan.quark.cn/s/ec0a5ba98903)