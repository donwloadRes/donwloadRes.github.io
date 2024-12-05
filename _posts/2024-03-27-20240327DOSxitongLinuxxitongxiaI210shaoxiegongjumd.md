---
layout: post
title: "DOS系统Linux系统下I210烧写工具"
date:   2022-09-10
tags: [烧写,DOS,Linux,I210,eeupdate]
comments: true
author: admin
---
# DOS系统、Linux系统下I210烧写工具

本仓库提供了一个用于在DOS系统和Linux系统下烧写I210网卡的工具及相关资源文件。以下是资源文件的详细介绍：

## 资源文件列表

1. **dos.zip**
   - 包含DOS系统下的相关烧写工具及烧写配置文件。
   - 主要工具：`eeupdate.exe`
   - 使用方法：
     - 查看MAC地址：`eeupdate.exe /nic=1 /mac_dump`
     - 修改MAC地址：`eeupdate.exe /nic=1 /mac=xxxxxxxxxxxx`
     - 烧写invm配置信息：`eeupdate.exe /nic=1 /invmupdate /file=<config_file>`

2. **eepromaccesstool-0-8-0.zip**
   - 包含Linux系统下的烧写工具源码，支持mips和x86架构的交叉编译。
   - 主要工具：`EepromAccessTool`
   - 使用方法：
     - 运行命令：`[root@test ~]# ./EepromAccessTool -nic=1 -f=I210_Invm_SerDesKX_NoAPM_v0.6.HEX -mac=887766231301`

3. **配置文件及mac烧写.txt**
   - 包含烧写相关的说明文档，详细介绍了如何在DOS和Linux系统下进行烧写操作。

## 使用说明

### DOS系统下使用
1. 解压`dos.zip`文件。
2. 根据需要使用`eeupdate.exe`工具进行MAC地址查看、修改或烧写invm配置信息。

### Linux系统下使用
1. 解压`eepromaccesstool-0-8-0.zip`文件。
2. 根据需要编译并运行`EepromAccessTool`工具进行烧写操作。

## 注意事项
- 请确保在操作前备份重要数据，避免因操作失误导致数据丢失。
- 操作过程中请严格按照说明文档进行，避免错误操作。

希望本资源文件能帮助您顺利完成I210网卡的烧写工作。如有任何问题，欢迎反馈。

## 下载链接

[DOS系统Linux系统下I210烧写工具](https://pan.quark.cn/s/97b10c0765ba)