---
layout: post
title: "ubuntu安装draw.io指南"
date:   2020-06-19
tags: [draw,io,drawio,fish,AppImage]
comments: true
author: admin
---
# ubuntu安装draw.io指南

## 概述

本文档为您提供了一份详尽的指南，旨在帮助您在Ubuntu操作系统上顺利安装draw.io这一强大的绘图软件。draw.io是一款优秀的跨平台图形设计工具，支持绘制包括思维导图、UML图、流程图在内的多种图表，且完全免费并开源。无论是专业的技术文档绘制，还是日常的工作学习需求，draw.io都能满足您的需求。

## 安装步骤

### 获取安装包

访问draw.io的GitHub释放页面或通过社区分享的链接下载适用于Ubuntu的安装包。推荐选择`.deb`包以利用Ubuntu的默认软件管理机制，或选择`.AppImage`文件，后者直接运行即可，无需安装。

#### 使用DEB包：
1. 下载最新版本的`.deb`文件。
2. 双击文件或在终端使用命令安装：
   ```
   sudo dpkg -i drawio-amd64-版本号.deb
   ```

#### 使用AppImage包：
1. 下载`.AppImage`文件。
2. 给予执行权限：
   ```
   chmod a+x drawio-x86_64-版本号.AppImage
   ```
3. 直接运行执行文件启动draw.io。

### 创建快捷方式

为了便于使用，您可以创建一个桌面快捷方式和命令行alias：

#### 桌面快捷方式
1. 创建一个新的`.desktop`文件，如`drawio.desktop`，并放置于`/usr/share/applications`目录（可能需管理员权限）：
   ```
   sudo touch /usr/share/applications/drawio.desktop
   sudo nano /usr/share/applications/drawio.desktop
   ```
2. 编辑此文件，填入如下内容：
   ```
   [Desktop Entry]
   Encoding=UTF-8
   Name=draw.io
   Comment=draw.io 图形编辑器
   Exec=/path/to/your/drawio.AppImage 或者 /opt/drawio/drawio
   Icon=/path/to/icon.xpm
   Terminal=false
   StartupNotify=true
   Type=Application
   Categories=Office;
   ```

#### 命令行Alias
对于快速命令行启动，可以在用户配置文件中添加alias：
- 对于bash用户，在`~/.bashrc`或`~/.profile`中加入：
  ```
  alias drawio="/path/to/your/drawio.AppImage"
  ```
- 对于fish用户，则在`~/.config/fish/config.fish`中添加相似指令。

记得替换上述路径为您实际的draw.io可执行文件路径，并执行`source ~/.bashrc`或`fish -c 'source ~/.config/fish/config.fish'`使alias生效。

## 结论

按照以上步骤操作后，您应该能够成功安装并在Ubuntu系统上启动draw.io。享受高效便捷的图形设计体验，无论是复杂的IT架构图还是简单的流程草图，draw.io都将助您一臂之力。

## 下载链接

[ubuntu安装draw.io指南分享](https://pan.quark.cn/s/5e0bd1baf2e8)