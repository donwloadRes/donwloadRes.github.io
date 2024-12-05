---
layout: post
title: "将Windows环境中的.exe可执行文件设置为后台服务"
date:   2022-12-12
tags: [exe,Windows,MyService,服务,srvany]
comments: true
author: admin
---
# 将Windows环境中的.exe可执行文件设置为后台服务

本资源文件提供了一个详细的指南，帮助用户在Windows环境中将.exe可执行文件设置为后台服务。通过使用`instsrv.exe`和`srvany.exe`这两个工具，用户可以将任何的exe应用程序作为Windows服务运行，使其在系统启动时自动启动，从而隐藏不必要的窗口。

## 主要步骤

### 1. 下载instsrv和srvany
- `instsrv.exe`和`srvany.exe`是Microsoft Windows Resource Kits工具集中的两个实用工具，配合使用可以将任何的exe应用程序作为Windows服务运行。
- `srvany.exe`是注册程序的服务外壳，可以通过它让应用程序以system账号启动，使应用程序作为Windows的服务随机器启动而自动启动。

### 2. 安装
- 将`instsrv.exe`和`srvany.exe`拷贝到系统目录下（64位系统为`C:\WINDOWS\SysWOW64`，32位系统为`C:\WINDOWS\system32`）。
- 在系统目录下打开命令提示符（cmd），运行以下命令：
  ```
  instsrv MyService C:\WINDOWS\SysWOW64\srvany.exe
  ```
  或
  ```
  instsrv MyService C:\WINDOWS\system32\srvany.exe
  ```
  其中，`MyService`是自定义的服务名称，可以根据应用程序名称任意更改。

### 3. 配置
- 打开注册表编辑器（regedit），搜索自定义的服务名称（如`MyService`）。
- 右击`MyService`，新建项，名称为`Parameters`。
- 在`Parameters`中新建几个字符串值：
  - `Application`：值为你要作为服务运行的程序地址。
  - `AppDirectory`：值为你要作为服务运行的程序所在文件夹路径。
  - `AppParameters`：值为你要作为服务运行的程序启动所需要的参数。

### 4. 操作服务
- 启动服务：`net start MyService`
- 停止服务：`net stop MyService`
- 删除服务：`sc delete "MyService"`

通过以上步骤，用户可以轻松地将任何exe应用程序设置为Windows后台服务，使其在系统启动时自动运行，无需用户手动开启。

## 下载链接

[将Windows环境中的.exe可执行文件设置为后台服务](https://pan.quark.cn/s/e7ae3c2c1e64)