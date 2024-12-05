---
layout: post
title: "vs2019+ArcEngine10.2安装教程"
date:   2024-05-09
tags: [Visual,Studio,2019,ArcGIS,安装]
comments: true
author: admin
---
# vs2019+ArcEngine10.2安装教程

## 简介
本资源文件提供了在Visual Studio 2019（vs2019）中安装ArcGIS Engine 10.2的详细教程。该教程适用于需要使用C#和ArcGIS Engine进行二次开发的用户。

## 安装环境
- **ArcGIS 10.2**
- **Visual Studio 2019**

## 安装步骤

### 1. 安装Visual Studio 2019
- 参考其他教程完成Visual Studio 2019的安装。

### 2. 安装ArcGIS Engine 10.2
1. 打开下载的ArcGIS Engine安装文件。
2. 按照安装向导的指示完成安装。
3. 安装完成后，启动许可服务器管理员（License Manager）。
4. 停止许可服务器服务。
5. 安装破解文件，覆盖原有的许可文件。

### 3. 配置Visual Studio 2019与ArcGIS Engine
1. 打开注册表编辑器。
2. 在注册表路径 `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\VisualStudio\10.0` 下新建两个字符串值：
   - `InstallDir`：设置为Visual Studio 2019的安装路径。
   - `ShellFolder`：设置为Visual Studio 2019的安装路径。
3. 完成注册表配置后，重新启动Visual Studio 2019。

### 4. 创建项目并配置
1. 在Visual Studio 2019中创建一个新的C# Windows窗体应用程序。
2. 在工具箱中添加ArcGIS Engine的工具。
3. 右键点击工具箱，选择“添加选项卡”，然后选择“项”。
4. 选择所有ArcGIS相关的工具并添加到工具箱中。

## 注意事项
- 确保所有安装步骤按照顺序进行，避免出现兼容性问题。
- 在配置注册表时，务必确认路径的正确性。

## 结语
通过本教程，您应该能够在Visual Studio 2019中成功安装并配置ArcGIS Engine 10.2，为后续的二次开发工作打下基础。

## 下载链接

[vs2019ArcEngine10.2安装教程](https://pan.quark.cn/s/6bd5c054a880)