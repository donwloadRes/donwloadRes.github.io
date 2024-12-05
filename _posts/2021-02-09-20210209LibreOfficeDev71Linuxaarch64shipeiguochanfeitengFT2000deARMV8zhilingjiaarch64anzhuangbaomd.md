---
layout: post
title: "LibreOfficeDev-7.1-Linux-aarch64 适配国产飞腾FT2000的ARMV8指令集aarch64安装包"
date:   2023-12-01
tags: [安装包,aarch64,FT2000,ARMV8,--]
comments: true
author: admin
---
# LibreOfficeDev-7.1-Linux-aarch64 适配国产飞腾FT2000的ARMV8指令集aarch64安装包

## 简介

本仓库提供了一个专为国产飞腾FT2000服务器适配的LibreOfficeDev 7.1版本安装包。该安装包基于ARMV8指令集的aarch64架构，适用于Linux系统。由于飞腾FT2000服务器的yum源中缺少LibreOffice的安装包，且网上ARM架构的资源较为稀缺，因此本仓库特别提供了这一资源，方便大家使用。

## 资源文件说明

- **文件名**: LibreOfficeDev-7.1-Linux-aarch64适配国产飞腾FT2000的ARMV8指令集aarch64安装包
- **文件类型**: RPM安装包
- **适用平台**: 飞腾FT2000服务器，ARMV8指令集aarch64架构

## 安装步骤

1. **下载安装包**: 从本仓库下载所有RPM安装包。
2. **安装RPM包**: 进入RPM目录，执行以下命令安装所有RPM包：
   ```bash
   yum install *.rpm
   ```
3. **启动LibreOffice**: 安装完成后，可以通过以下命令启动LibreOffice：
   ```bash
   /opt/libreoffice6.3/program/soffice --headless --accept="socket,host=127.0.0.1,port=8100;urp;" --nofirststartwizard &
   ```
4. **文件预览命令**: 使用以下命令将文件转换为PDF格式进行预览：
   ```bash
   /opt/libreoffice6.3/program/soffice --headless --invisible --convert-to pdf 文件名
   ```

## 注意事项

- 本安装包为ARMV8指令集aarch64架构专用，不适用于其他架构。
- 安装过程中请确保系统已配置好yum源，以便顺利安装依赖包。
- 启动LibreOffice时，请根据实际需求调整命令中的参数。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交Issue或Pull Request。感谢您的支持与贡献！

## 下载链接

[LibreOfficeDev-7.1-Linux-aarch64适配国产飞腾FT2000的ARMV8指令集aarch64安装包](https://pan.quark.cn/s/efd7a81f20bc)