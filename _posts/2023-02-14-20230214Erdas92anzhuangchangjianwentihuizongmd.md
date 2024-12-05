---
layout: post
title: "Erdas92安装常见问题汇总"
date:   2022-09-16
tags: [安装,Erdas9.2,ERDAS,软件,常见问题]
comments: true
author: admin
---
# Erdas9.2安装常见问题汇总

本文旨在为Erdas9.2的安装过程中可能遇到的问题提供详细的解决方案。Erdas9.2是一款广泛应用于地理信息系统（GIS）和遥感领域的专业软件，安装过程中可能会遇到各种技术问题。通过本文，您可以找到针对这些问题的有效解决方法。

## 主要内容

### 1. 许可管理的配置问题
- **license.dat文件中的计算机名替换**：确保将“SERVER this host ANY”中的"this host"替换为您的计算机名。
- **LMTOOLS配置细节**：在LMTOOLS的config service菜单下，确保第一个Browse打开的是lmgrd.exe而不是ERDAS.exe。
- **许可管理冲突**：如果电脑中同时安装了ArcGIS、ERDAS、ENVI等软件，可能会造成许可管理冲突，需特别注意。

### 2. 打开软件弹窗问题
- **首次打开软件的弹窗处理**：通常选中第一个选项，输入“localhost”或本机计算机名后单击continue即可打开。
- **服务被占用问题**：如果服务被ArcGIS或ENVI占用，需结束相应进程后启动ERDAS服务。

### 3. 安装过程中的问题及建议
- **安装路径中的中文问题**：建议安装路径中不要出现中文，以避免潜在的兼容性问题。
- **Error 1935错误**：这是由于缺少Microsoft Visual C++ 2005 Redistributable所致，需下载并安装相应的运行库。

## 总结

本文总结了Erdas9.2安装过程中常见的问题及其解决方法，希望能帮助用户顺利完成安装并开始使用这款强大的遥感图像处理软件。

## 下载链接

[Erdas9.2安装常见问题汇总分享](https://pan.quark.cn/s/f68ae435c06f)