---
layout: post
title: "Win10离线安装Framework 3.5及解决DISM找不到源文件的方法"
date:   2022-01-12
tags: [源文件,离线,DISM,安装,Framework]
comments: true
author: admin
---
# Win10离线安装Framework 3.5及解决DISM找不到源文件的方法

本文档提供了一个资源文件，用于在Windows 10系统中离线安装.NET Framework 3.5，并解决在使用DISM命令时可能遇到的“找不到源文件”问题。该方法已经过测试，证明有效。

## 资源文件内容

该资源文件包含了以下内容：
- .NET Framework 3.5的离线安装包
- 解决DISM找不到源文件的详细步骤和命令

## 使用方法

1. **下载资源文件**：
   - 下载本仓库中的资源文件，并解压缩到本地目录。

2. **离线安装.NET Framework 3.5**：
   - 打开命令提示符（以管理员身份运行）。
   - 输入以下命令：
     ```
     dism /online /enable-feature /featurename:NetFx3 /All /Source:D:\路径\到\解压后的文件夹\sxs /LimitAccess
     ```
   - 等待安装完成。

3. **解决DISM找不到源文件的问题**：
   - 如果遇到“找不到源文件”的错误，请确保已将解压后的`sxs`文件夹放置在C盘根目录下。
   - 重新运行上述命令，确保路径正确。

## 注意事项

- 在安装过程中，请保持电脑联网状态，因为安装过程中可能需要从网络上下载一些必要的文件。
- 如果安装过程中遇到其他问题，请参考CSDN博客文章中的详细步骤和解决方案。

## 参考资料

- 该资源文件的详细使用方法和解决方案参考自CSDN博客文章。

通过以上步骤，您应该能够成功在Windows 10系统中离线安装.NET Framework 3.5，并解决DISM找不到源文件的问题。

## 下载链接

[Win10离线安装Framework3.5及解决DISM找不到源文件的方法](https://pan.quark.cn/s/2a71ec832c78)