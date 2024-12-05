---
layout: post
title: "windows10安装openssl环境并命令行调用openssl（快速免编译安装指南）"
date:   2020-06-13
tags: [openssl,环境变量,安装,OpenSSL,Perl]
comments: true
author: admin
---
# windows10安装openssl环境并命令行调用openssl（快速免编译安装指南）

## 概述

本文档为您提供一个简易教程，指导您如何在Windows 10操作系统上安装OpenSSL环境，并在命令行下直接调用openssl命令，整个过程无需编译openssl源代码，适合不想深入编译过程的用户。

## 步骤概览

### 1. 安装Perl（可选）
- 对于某些特定情况，Perl可能是必需的。您可以从[Activestate](https://www.activestate.com/activeperl/downloads/)下载Perl。安装后，可能需要重启计算机以确保Perl命令能在命令行中正常使用。

### 2. OpenSSL安装
- 访问[OpenSSL官方下载页面](http://slproweb.com/products/Win32OpenSSL.html)，根据您的系统选择对应的64位或32位exe安装包。
- 完成安装，默认安装路径通常为`C:\Program Files\OpenSSL Win64`。
- 设置环境变量，将`openssl`的bin目录加入到系统PATH环境变量中，例如`C:\Program Files\OpenSSL-Win64\bin`。
- 重启电脑以确保环境变量生效。

### 3. 配置环境（解决警告问题）
- 若遇到“WARNING: can't open config file”错误，手动设置`OPENSSL_CONF`环境变量指向正确的openssl.cfg位置，例如`set OPENSSL_CONF=C:\Program Files\OpenSSL-Win64\bin\openssl.cfg`。

### 4. 命令行调用openssl
- 重启电脑后，以管理员权限打开命令提示符，现在您可以输入openssl命令了，如生成RSA密钥对：
  ```
  openssl genrsa -aes256 -out rsa-key.pem 2048
  ```
- 上述命令将在指定路径生成一个包含RSA密钥对的.pem文件。

## 注意事项
- 安装Perl和配置环境变量后，强烈建议重启电脑，以免环境变量未正确生效。
- 确保所有步骤都遵循指南，以避免环境配置不当导致的问题。

通过遵循这些简单的步骤，您可以在Windows 10上快速地准备好openssl的使用环境，以便在命令行中执行加密相关的任务。

## 下载链接

[windows10安装openssl环境并命令行调用openssl快速免编译安装指南](https://pan.quark.cn/s/bbcd1c3f5007)