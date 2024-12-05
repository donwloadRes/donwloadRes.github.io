---
layout: post
title: "Windows Server 2019 .NET Framework 3.5 安装包"
date:   2023-02-28
tags: [安装,Windows,Server,2019,NET]
comments: true
author: admin
---
# Windows Server 2019 .NET Framework 3.5 安装包

## 简介

本仓库提供了一个用于Windows Server 2019的.NET Framework 2.0和3.5的安装包。该安装包专为在Windows Server 2019上安装.NET Framework 2.0和3.5时遇到问题的用户设计。通过使用本仓库提供的资源文件，您可以顺利完成.NET Framework 2.0和3.5的安装。

## 使用说明

1. **下载资源文件**：
   - 点击仓库中的资源文件进行下载。

2. **安装步骤**：
   - 将下载的资源文件放置在Windows Server 2019的合适位置。
   - 打开命令提示符（以管理员身份运行）。
   - 使用以下命令进行安装：
     ```shell
     dism /online /enable-feature /featurename:NetFx3 /All /Source:C:\路径\到\资源文件 /LimitAccess
     ```
   - 请将`C:\路径\到\资源文件`替换为您实际存放资源文件的路径。

3. **验证安装**：
   - 安装完成后，您可以通过以下命令验证.NET Framework 3.5是否成功安装：
     ```shell
    dism /online /get-features | findstr NetFx3
     ```
   - 如果显示`State : Enabled`，则表示安装成功。

## 注意事项

- 请确保您以管理员权限运行命令提示符。
- 如果安装过程中遇到任何问题，请参考Windows Server 2019的官方文档或联系技术支持。

## 贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[WindowsServer2019.NETFramework3.5安装包](https://pan.quark.cn/s/d44c14ece589)