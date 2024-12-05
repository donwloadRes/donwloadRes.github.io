---
layout: post
title: "Visual Studio 2019 离线断网（内网安装）保姆级安装方法"
date:   2021-11-20
tags: [--,安装,文件夹,离线,Visual]
comments: true
author: admin
---
# Visual Studio 2019 离线断网（内网安装）保姆级安装方法

本仓库提供了一个详细的教程和资源文件，帮助用户在没有互联网连接的情况下（如内网环境）安装 Visual Studio 2019。以下是安装步骤的简要说明：

## 安装步骤

### 1. 下载安装包引导程序
- 首先，从微软官方网站下载 Visual Studio 2019 的安装包引导程序。

### 2. 创建文件夹
- 在本地计算机上创建一个文件夹（例如 `VS2019`），并将下载的 `.exe` 文件保存到该文件夹中。
- 在该文件夹内再创建一个名为 `installer` 的子文件夹，用于存放后续下载的离线安装包。

### 3. 下载离线安装包
- 打开命令提示符（CMD），导航到 `VS2019` 文件夹。
- 输入以下命令开始下载离线安装包：
  ```
  vs_community.exe --layout .\installer --add Microsoft.VisualStudio.Workload.NativeDesktop --add Microsoft.VisualStudio.Component.Windows10SDK.18362 --includeRecommended --lang zh-CN
  ```
  该命令将下载 C++ 桌面开发和 Windows 10 SDK 18362 组件，并包含推荐的中文语言包。

### 4. 安装 Visual Studio 2019
- 下载完成后，将整个 `VS2019` 文件夹拷贝到需要安装的计算机上。
- 双击 `vs_setup.exe` 文件开始安装。

### 5. 使用配置文件安装（可选）
- 如果之前已经安装过 Visual Studio 2019，可以通过导出配置文件（`.vsconfig`）来简化离线安装过程。
- 使用以下命令根据配置文件进行安装：
  ```
  vs_community.exe --layout c:\localVSlayout --config c:\myconfig.vsconfig --lang en-US
  ```

## 注意事项
- 本安装包仅包含 C++ 桌面开发和 Linux C++ 开发组件，安装时会自动勾选这两个组件。
- 如果需要其他组件，可以在命令中添加相应的工作负荷 ID 或组件 ID。

通过以上步骤，您可以在没有互联网连接的环境中顺利安装 Visual Studio 2019。

## 下载链接

[VisualStudio2019离线断网内网安装保姆级安装方法](https://pan.quark.cn/s/0705d7be9183)