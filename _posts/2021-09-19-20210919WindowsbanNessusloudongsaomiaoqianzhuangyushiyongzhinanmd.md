---
layout: post
title: "Windows版Nessus漏洞扫描器安装与使用指南"
date:   2023-06-05
tags: [Nessus,安装,插件,Windows,路径]
comments: true
author: admin
---
# Windows版Nessus漏洞扫描器安装与使用指南

本仓库提供了一个资源文件，用于Windows版Nessus漏洞扫描器的安装与使用。Nessus是一款广泛使用的系统漏洞扫描与分析软件，能够帮助用户快速检测和解决网络中的安全漏洞。

## 资源文件内容

- **Nessus版本**: 8.13.1
- **适用系统**: Windows 10 64位
- **插件版本**: all_2.0_20220618.tar

## 安装步骤

1. **下载资源文件**: 从本仓库下载Nessus安装包及相关插件。
2. **安装Nessus**:
   - 双击安装包，点击“Next”。
   - 选择安装路径（建议自定义路径），点击“Install”。
   - 安装完成后，点击“Finish”。
3. **配置Nessus**:
   - 安装完成后，浏览器会自动访问Nessus管理界面（https://localhost:8834/）。
   - 选择“Connect via SSL”，然后选择“Managed Scanner”。
   - 继续操作，注册账号并输入用户名和密码。
4. **加载插件**:
   - 等待插件加载完成，完成后即可开始使用Nessus进行漏洞扫描。

## 破解步骤（可选）

1. **停止Nessus服务**: 以管理员身份打开命令提示符，输入`net stop "Tenable Nessus"`。
2. **更改文件属性**: 输入以下命令更改文件属性：
   ```
   attrib -s -r -h "安装路径\Nessus\nessus\plugins\*"
   attrib -s -r -h "安装路径\Nessus\nessus\plugin_feed_info.inc"
   ```
3. **更新插件**: 将下载的插件文件复制到Nessus安装目录下，然后输入以下命令更新插件：
   ```
   nessuscli.exe update all_2.0_20220618.tar.gz
   ```
4. **复制文件**: 将`plugin_feed_info.inc`文件复制到`plugins`目录下。
5. **更改文件属性**: 输入以下命令恢复文件属性：
   ```
   attrib +s +r +h "安装路径\Nessus\nessus\plugins\*"
   attrib +s +r +h "安装路径\Nessus\nessus\plugin_feed_info.inc"
   ```
6. **启动Nessus服务**: 输入`net start "Tenable Nessus"`启动服务。
7. **登录Nessus**: 打开浏览器访问`https://localhost:8834/`，输入账号密码登录，完成破解。

## 使用说明

- 安装完成后，可以通过Nessus管理界面进行漏洞扫描。
- 扫描结果可以导出为PDF格式，方便后续分析和处理。

## 注意事项

- 安装路径中不要包含中文，否则可能导致插件加载失败。
- 破解步骤仅供学习使用，请勿用于商业用途。

通过本指南，您可以顺利完成Windows版Nessus漏洞扫描器的安装与使用，帮助您更好地进行网络安全检测。

## 下载链接

[Windows版Nessus漏洞扫描器安装与使用指南](https://pan.quark.cn/s/f3f2d022e525)