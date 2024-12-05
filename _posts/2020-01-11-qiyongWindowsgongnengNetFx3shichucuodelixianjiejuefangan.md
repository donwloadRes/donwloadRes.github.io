---
layout: post
title: "启用Windows功能NetFx3时出错的离线解决方案"
date:   2021-09-15
tags: [Windows,NetFx3,离线,安装,NET]
comments: true
author: admin
---
# 启用Windows功能NetFx3时出错的离线解决方案

## 简介

本资源文件提供了一个离线解决方案，用于解决在启用Windows功能NetFx3时出现的错误。该解决方案适用于那些无法通过在线方式安装.NET Framework 3.5的用户。通过使用本资源文件，您可以在没有互联网连接的情况下成功安装.NET Framework 3.5。

## 适用场景

- 在安装SQL Server 2012的过程中，报错“启用windows功能NetFx3时出错”。
- 在Windows Server 2016等操作系统上，默认不安装.NET Framework 3.5，需要手动安装。
- 在没有系统安装文件的情况下，通过NetFx3.cab文件进行离线安装。

## 解决方案步骤

### 方法一：有系统安装文件

1. 打开控制面板，进入“程序和应用”。
2. 选择“打开或关闭Windows功能”。
3. 在功能选项中，勾选“.NET Framework 3.5”。
4. 指定备用源路径为系统安装文件下的Sources\sxs目录。
5. 等待安装成功。

### 方法二：无系统安装文件（通过NetFx3.cab文件安装）

1. 下载NetFx3.cab文件，并将其放于C盘WINDOWS文件夹下（C:\Windows）。
2. 以管理员身份运行命令提示符，输入以下命令：
   ```
   dism.exe /online /add-package /packagepath:C:\WINDOWS\netfx3.cab
   ```
3. 等待安装成功。

## 注意事项

- 确保您有足够的权限进行系统修改。
- 在执行命令时，请确保以管理员身份运行命令提示符。
- 如果遇到其他错误，请参考相关文档或联系技术支持。

## 结论

通过本资源文件提供的离线解决方案，您可以轻松解决在启用Windows功能NetFx3时出现的错误，确保.NET Framework 3.5的顺利安装。

## 下载链接

[启用Windows功能NetFx3时出错的离线解决方案分享](https://pan.quark.cn/s/20aa85638ad0)