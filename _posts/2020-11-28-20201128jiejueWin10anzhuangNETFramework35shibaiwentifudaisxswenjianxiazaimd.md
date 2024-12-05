---
layout: post
title: "解决Win10安装NET Framework 35失败问题附带sxs文件下载"
date:   2023-03-16
tags: [sxs,Win10,安装包,NET,Framework]
comments: true
author: admin
---
# 解决Win10安装.NET Framework 3.5失败问题（附带sxs文件下载）

## 简介

本仓库提供了一个解决方案，帮助用户解决在Windows 10系统中安装.NET Framework 3.5时遇到的问题。该问题通常表现为安装失败，错误代码为87。本仓库包含了一个必要的sxs文件，用户可以通过该文件进行离线安装，从而成功启用.NET Framework 3.5功能。

## 使用方法

1. **下载sxs文件**：
   - 从本仓库下载提供的sxs文件。

2. **准备Win10安装包**：
   - 如果用户没有Win10安装包，可以参考相关教程下载。
   - 如果用户已经拥有Win10安装包，可以从安装包中提取sxs文件。

3. **拷贝sxs文件**：
   - 将下载或提取的sxs文件拷贝到E盘根目录下。

4. **执行命令**：
   - 打开命令提示符（以管理员身份运行）。
   - 输入以下命令并执行：
     ```
     dism.exe /online /enable-feature /featurename:NetFX3 /Source:E:\sxs
     ```

5. **开启.NET Framework 3.5功能**：
   - 执行完上述命令后，系统将自动开启.NET Framework 3.5功能。

## 常见问题

- **错误87**：如果在执行过程中遇到错误87，请按照以下步骤解决：
  1. 关闭所有杀毒软件及电脑管理管家（如360安全卫士）。
  2. 打开服务中的Windows Update自动更新。
  3. 关闭.NET Framework 4.6高级服务。
  4. 将NetFx3.cab的离线安装包拷贝到Win10系统盘C:\Windows文件夹里。
  5. 以管理员身份运行命令提示符，输入以下命令：
     ```
     dism.exe /online /add-package /packagepath:C:\WINDOWS\netfx3.cab
     ```
  6. 看到进度条并有释放空间字样，即表示成功。

## 注意事项

- 请确保在执行命令时，系统盘C:\Windows文件夹中有足够的空间。
- 如果用户没有Win10安装包，建议先下载安装包，再进行sxs文件的提取和安装。

## 贡献

欢迎用户反馈问题和提出改进建议。如果有任何疑问或需要帮助，请在仓库中提交Issue。

## 许可证

本仓库内容遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[解决Win10安装.NETFramework3.5失败问题附带sxs文件下载](https://pan.quark.cn/s/ea9bbf854fb3)