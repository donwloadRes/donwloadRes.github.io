---
layout: post
title: "Windows下的Memcached 1621服务安装包"
date:   2023-07-22
tags: [Windows,服务,Memcached,命令提示符,21]
comments: true
author: admin
---
# Windows下的Memcached 1.6.21服务安装包

## 描述

本仓库提供了一个在Windows下编译的最新版本Memcached 1.6.21，并将其制作为Windows服务。由于1.4.5版本以后的Memcached不再支持Windows服务，因此我们使用了第三方工具将其制作为Windows服务。

## 使用说明

1. **解压文件**：首先，请将下载的RAR文件解压到您希望安装Memcached的目录中。

2. **以管理员身份运行命令提示符**：右键点击`cmd.exe`，选择“以管理员身份运行”。

3. **执行安装脚本**：在命令提示符中，导航到解压后的目录，然后执行`service_install.bat`脚本。

4. **服务名称**：默认情况下，服务名称为`memcached`。如果您希望修改服务名称，可以在`memcached-service.xml`文件中进行修改。

## 注意事项

- 请确保在执行安装脚本时，命令提示符是以管理员身份运行的。
- 如果您修改了服务名称，请确保在`memcached-service.xml`文件中同步更新。

## 其他说明

本资源文件仅供学习和测试使用，请勿用于商业用途。如果您在使用过程中遇到任何问题，欢迎在仓库中提交Issue，我们会尽快为您解答。

## 下载链接

[Windows下的Memcached1.6.21服务安装包](https://pan.quark.cn/s/1be2c0898ca2)