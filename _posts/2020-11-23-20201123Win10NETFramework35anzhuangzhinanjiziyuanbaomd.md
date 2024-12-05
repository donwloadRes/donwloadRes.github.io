---
layout: post
title: "Win10 NET Framework 35 安装指南及资源包"
date:   2023-08-12
tags: [版本,Win10,NetFx3,NET,Framework]
comments: true
author: admin
---
# Win10 .NET Framework 3.5 安装指南及资源包

## 简介
本仓库提供了一个用于Windows 10系统中安装.NET Framework 3.5的详细指南，并附带了Win10 1909版本的安装包资源。该资源包可以帮助用户在没有互联网连接的情况下，轻松安装所需的.NET Framework 3.5版本，以确保应用程序的正常运行。

## 安装步骤

### 1. 获取NetFx3.cab包
- **Win10 1909版本**：
  - 下载并解压Win10 1909版本的ISO镜像文件。
  - 在解压后的文件夹中，找到并复制`\sources\sxs`目录下的`NetFx3.cab`包。

- **其他版本**：
  - 在系统设置中查看系统版本。
  - 下载对应版本的ISO镜像文件并解压。
  - 在解压后的文件夹中，找到并复制`\sources\sxs`目录下的`NetFx3.cab`包。

### 2. 安装.NET Framework 3.5
- 将复制的`NetFx3.cab`包放到`C:\Windows`目录下。
- 以管理员身份打开命令提示符。
- 输入以下命令并按回车执行：
  ```
  dism /online /Enable-Feature /FeatureName:NetFx3 /Source:"%windir%" /LimitAccess
  ```
- 等待进度条加载完毕，安装完成。

## 注意事项
- 确保系统版本与下载的ISO镜像文件版本一致，否则可能导致安装失败。
- 在执行命令时，确保命令提示符是以管理员身份运行。

## 资源包内容
- `NetFx3.cab`：用于离线安装.NET Framework 3.5的CAB包。

## 参考资料
- 更多详细信息和操作步骤，请参考[CSDN博客文章](https://blog.csdn.net/weixin_43869135/article/details/110452007)。

## 贡献
欢迎提交问题和改进建议，帮助我们完善本仓库的内容。

## 许可证
本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[Win10.NETFramework3.5安装指南及资源包分享](https://pan.quark.cn/s/ddb3dfde7cf3)