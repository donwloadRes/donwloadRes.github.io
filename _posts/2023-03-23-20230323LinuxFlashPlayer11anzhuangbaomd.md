---
layout: post
title: "Linux Flash Player 11 安装包"
date:   2021-07-19
tags: [插件,Flash,11,Linux,64]
comments: true
author: admin
---
# Linux Flash Player 11 安装包

## 简介

本仓库提供了一个适用于Linux系统的Flash Player 11安装包，文件名为`install-flash-player-11-linux.x86-64.tar.gz`。该安装包主要用于在Linux系统上的火狐浏览器中安装Flash插件，以便启动和登录OEM企业管理器。

## 文件描述

- **文件名**: `install-flash-player-11-linux.x86-64.tar.gz`
- **适用系统**: Linux x86-64
- **用途**: 在火狐浏览器中安装Flash插件，用于启动和登录OEM企业管理器

## 安装步骤

1. **下载文件**: 从本仓库下载`install-flash-player-11-linux.x86-64.tar.gz`文件。
2. **解压缩**: 使用以下命令解压缩文件：
   ```bash
   tar -xzvf install-flash-player-11-linux.x86-64.tar.gz
   ```
3. **安装插件**: 将解压后的文件复制到火狐浏览器的插件目录中。通常情况下，插件目录位于`/usr/lib/mozilla/plugins/`或`~/.mozilla/plugins/`。
   ```bash
   sudo cp libflashplayer.so /usr/lib/mozilla/plugins/
   ```
4. **重启浏览器**: 重启火狐浏览器，确保Flash插件已正确加载。

## 注意事项

- 请确保您的系统是64位的Linux系统。
- 安装前请备份重要数据，以防意外情况发生。
- 如果遇到任何问题，请参考官方文档或寻求技术支持。

## 更新日志

- **版本**: Flash Player 11
- **发布日期**: [请填写发布日期]
- **更新内容**: 初始版本发布

## 联系我们

如有任何问题或建议，请通过[联系方式]与我们联系。

---

希望这个安装包能够帮助您顺利在Linux系统上使用Flash插件，并成功启动和登录OEM企业管理器。

## 下载链接

[LinuxFlashPlayer11安装包](https://pan.quark.cn/s/1650ade1c436)