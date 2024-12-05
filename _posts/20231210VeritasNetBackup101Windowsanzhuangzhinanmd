---
layout: post
title: "Veritas NetBackup 10.1 Windows 安装指南"
date:   2022-01-30
tags: [安装,Veritas,NetBackup,Windows,10.1]
comments: true
author: admin
---
# Veritas NetBackup 10.1 Windows 安装指南

本资源文件提供了关于如何在Windows系统上安装Veritas NetBackup 10.1的详细步骤和指南。Veritas NetBackup是一款功能强大的企业级备份和恢复解决方案，适用于各种规模的企业。

## 内容概述

1. **前言**  
   本文是Veritas NetBackup 10.1安装系列中关于Windows安装的部分。本文仅提供安装步骤及思路，相关许可密钥请至官方正版购买颁发，严厉打击侵权行为。

2. **创建账户及分配权限**  
   由于Veritas 8以后版本添加了CA认证，master server会包括一个网络服务器，在提供的用户和组别账户下运行，所以需要提前创建对应组及用户，分配相关权限。

3. **下载分析安装包**  
   下载并解压安装包到需要安装master server的Windows服务器上，分析对应软件和功能。

4. **执行安装**  
   运行安装程序，选择安装类型，输入正版license key，创建相关用户并分配权限，确认相关信息后开始自动安装。

## 安装步骤

### 1. 创建账户及分配权限

- **创建本地用户帐户**：  
  `C:\>net user nbwebsvc <StrongPassword> /add`

- **创建本地组**：  
  `C:\>net localgroup nbwebgrp /add`

- **使用户成为组成员**：  
  `C:\>net localgroup nbwebgrp nbwebsvc /add`

### 2. 下载分析安装包

- 下载链接: `NetBackup_10.0.0.1_Win`  
- 提取码：`rfag`

### 3. 执行安装

- 运行安装程序，选择安装类型，输入正版license key。
- 创建相关用户并分配权限。
- 确认相关信息后开始自动安装。

## 注意事项

- 安装前请详细阅读readme文件。
- 安装过程中需要相关许可支持，请提前备好NBU10.1的密钥许可代码以及customer-registration-key的注册文件。

## 结语

本指南旨在帮助用户顺利完成Veritas NetBackup 10.1在Windows系统上的安装。如需更多详细信息，请参考官方文档或联系技术支持。

## 下载链接

[VeritasNetBackup10.1Windows安装指南](https://pan.quark.cn/s/db1a0c7898be)