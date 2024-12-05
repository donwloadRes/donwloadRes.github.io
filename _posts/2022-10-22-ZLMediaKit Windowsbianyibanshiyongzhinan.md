---
layout: post
title: "ZLMediaKit Windows编译版使用指南"
date:   2024-04-25
tags: [ZLMediaKit,Windows,调试,OpenSSL,HTTP]
comments: true
author: admin
---
# ZLMediaKit Windows编译版使用指南

## 资源文件描述

本仓库提供了一个在Windows x64平台上编译的ZLMediaKit版本，方便用户在Windows系统上快速部署和使用ZLMediaKit。

## 使用步骤

1. **安装OpenSSL**  
   双击运行`Win64OpenSSL_Light-3_2_1.exe`，按照提示完成OpenSSL的安装。

2. **启动ZLMediaKit**  
   双击`MediaServer.exe`启动ZLMediaKit项目。默认情况下，HTTP端口为8099。如果端口冲突，可以自行修改`config.ini`文件中的HTTP端口配置。

3. **接口调试**  
   将提供的两个JSON文件导入Postman，即可进行接口调试。

## 注意事项

- 请确保在安装OpenSSL时按照提示正确完成安装。
- 如果遇到端口冲突问题，请在`config.ini`文件中修改HTTP端口配置。
- 导入Postman的JSON文件包含了常用的接口配置，方便用户进行接口调试。

通过以上步骤，您可以快速在Windows系统上部署和使用ZLMediaKit，进行流媒体服务的开发和调试。

## 下载链接

[ZLMediaKitWindows编译版使用指南](https://pan.quark.cn/s/1fcddd2fe5b5)