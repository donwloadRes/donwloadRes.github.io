---
layout: post
title: "Windows环境下Erlang下载与安装指南"
date:   2022-07-27
tags: [Erlang,Windows,安装,下载,22.3]
comments: true
author: admin
---
# Windows环境下Erlang下载与安装指南

本仓库提供了一个资源文件，用于在Windows环境下下载和安装Erlang。Erlang是一种通用的面向并发的编程语言，广泛用于构建分布式、实时软并行计算系统。

## 资源文件内容

- **Erlang OTP 22.3 Windows 64位二进制文件**：适用于Windows 64位系统的Erlang OTP（开放电信平台）22.3版本。
- **Microdoft DLL**：如果您的开发环境是.NET，建议勾选此选项。

## 安装步骤

1. **下载资源文件**：从本仓库下载提供的Erlang安装包。
2. **运行安装程序**：双击下载的安装包，按照向导完成安装。
3. **配置环境变量**：
   - 右键点击“我的电脑”，选择“属性”。
   - 点击“高级系统设置”，然后选择“环境变量”。
   - 在“系统变量”中新建一个变量，变量名为`ERLANG_HOME`，变量值为Erlang安装路径（例如`C:\Program Files\erl-22.3`）。
   - 在“系统变量”中找到`PATH`，点击“编辑”，然后新建一个条目，输入`%ERLANG_HOME%\bin`。
4. **验证安装**：
   - 打开命令提示符，输入`erl -version`。
   - 如果显示版本号，说明安装成功。

## 注意事项

- 确保您的系统是64位Windows。
- 安装过程中如有任何问题，请参考[CSDN博客文章](https://blog.csdn.net/weixin_40822435/article/details/105738375)获取更多帮助。

通过以上步骤，您可以在Windows环境下成功安装Erlang，并开始使用它进行开发。

## 下载链接

[Windows环境下Erlang下载与安装指南](https://pan.quark.cn/s/d68b19f1ef3b)