---
layout: post
title: "Ubuntu 2004 安装 Qt512 指南"
date:   2022-01-18
tags: [Qt5.12,QtCreator,安装,sudo,opt]
comments: true
author: admin
---
# Ubuntu 20.04 安装 Qt5.12 指南

本资源文件提供了在 Ubuntu 20.04 系统上安装 Qt5.12 的详细步骤。Qt 是一个跨平台的 C++ 应用程序框架，广泛用于开发图形用户界面（GUI）程序。以下是安装过程的简要说明：

## 安装步骤

### 第一步：下载 Qt5.12 安装包
1. 使用清华镜像进行下载。
2. 也可以通过百度云链接下载，提取码为 `t5jt`。

### 第二步：安装 Qt
1. 进入安装包路径：`cd ~/下载`。
2. 赋予安装包执行权限：`sudo chmod +x qt-opensource-linux-x64-5.12.9.run`。
3. 断开无线网，开始安装：`sudo ./qt-opensource-linux-x64-5.12.9.run`。
4. 一路默认选择安装内容，Qt 默认安装在 `/opt/Qt5.12.9`。

### 第三步：配置 Qt
1. 安装 g++：`sudo apt-get install g++`。
2. 安装 OpenGL 库：`sudo apt-get install mesa-common-dev`。
3. 添加环境路径：编辑 `~/.bashrc` 文件，添加以下内容：
   ```bash
   export PATH=/opt/Qt5.12.9/Tools/QtCreator/bin:$PATH
   ```

### 第四步：运行与测试
1. 打开终端，运行 `qtcreator`。
2. 正常打开后，界面如下。
3. 可以进行测试，确保安装成功。

### 第五步：创建快捷方式
1. 创建快捷方式文件：`sudo gedit /usr/share/applications/QtCreator.desktop`。
2. 写入以下内容：
   ```ini
   Type=Application
   Name=QtCreator
   GenericName=QtCreator
   Exec=/opt/Qt5.12.9/Tools/QtCreator/bin/qtcreator
   Icon=/opt/Qt5.12.9/Tools/QtCreator/share/qtcreator/qbs/share/qbs/examples/cocoa-application/CocoaApplication/CocoaApplication.xcassets/AppIcon.appiconset/icon_512x512.png
   Terminal=false
   Categories=Development;Qt;
   ```
3. 在启动项中可以搜索到 QtCreator，并添加到侧边栏。

通过以上步骤，您可以在 Ubuntu 20.04 系统上成功安装并配置 Qt5.12。

## 下载链接

[Ubuntu20.04安装Qt5.12指南分享](https://pan.quark.cn/s/368eb4dc98f7)