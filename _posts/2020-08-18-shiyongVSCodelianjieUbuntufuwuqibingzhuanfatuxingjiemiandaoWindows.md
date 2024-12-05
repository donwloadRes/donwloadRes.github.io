---
layout: post
title: "使用VSCode连接Ubuntu服务器并转发图形界面到Windows"
date:   2023-08-24
tags: [VSCode,图形界面,Xming,Windows,SSH]
comments: true
author: admin
---
# 使用VSCode连接Ubuntu服务器并转发图形界面到Windows

本文将介绍如何在Windows系统下使用VSCode连接Ubuntu服务器，并通过Xming将Ubuntu服务器端的图形界面转发到Windows系统中。通过这种方法，您可以在Windows环境下方便地进行远程开发和调试。

## 步骤概览

1. **安装VSCode和相关插件**
   - 在Windows系统中安装VSCode。
   - 安装Remote - SSH插件，以便通过SSH连接到远程服务器。

2. **配置SSH连接**
   - 在VSCode中配置SSH连接，输入Ubuntu服务器的IP地址和用户名。
   - 使用SSH密钥或密码进行身份验证。

3. **安装Xming**
   - 在Windows系统中下载并安装Xming，用于显示远程服务器的图形界面。

4. **配置Xming和VSCode**
   - 启动Xming并确保其正常运行。
   - 在VSCode中配置环境变量，指定Xming作为图形界面的显示工具。

5. **启动图形界面应用**
   - 在VSCode中打开远程服务器的终端。
   - 运行需要图形界面的应用程序，Xming将自动显示该应用程序的界面。

## 详细步骤

### 1. 安装VSCode和相关插件

首先，在Windows系统中下载并安装VSCode。安装完成后，打开VSCode并进入扩展市场，搜索并安装“Remote - SSH”插件。该插件允许您通过SSH连接到远程服务器。

### 2. 配置SSH连接

在VSCode中，按下`Ctrl+Shift+P`打开命令面板，输入“Remote-SSH: Connect to Host”并选择“Add New SSH Host”。输入Ubuntu服务器的IP地址和用户名，例如：

```
ssh user@192.168.1.100
```

保存配置后，选择该配置并进行连接。您可能需要输入SSH密钥或密码进行身份验证。

### 3. 安装Xming

在Windows系统中，访问Xming的官方网站并下载安装包。安装过程中，确保选择“XLaunch”选项以便配置Xming的启动参数。

### 4. 配置Xming和VSCode

启动Xming并确保其正常运行。在VSCode中，打开远程服务器的终端，并设置环境变量以指定Xming作为图形界面的显示工具。您可以通过以下命令设置环境变量：

```bash
export DISPLAY=localhost:0.0
```

### 5. 启动图形界面应用

在VSCode的远程终端中，运行需要图形界面的应用程序。例如，运行一个简单的图形界面工具：

```bash
xeyes
```

Xming将自动显示该应用程序的界面，您可以在Windows系统中看到Ubuntu服务器上的图形界面。

## 总结

通过以上步骤，您可以在Windows系统下使用VSCode连接到Ubuntu服务器，并通过Xming将服务器端的图形界面转发到Windows系统中。这种方法适用于远程开发、调试和图形界面应用的测试。

## 下载链接

[使用VSCode连接Ubuntu服务器并转发图形界面到Windows](https://pan.quark.cn/s/26ac57ad1a4b)