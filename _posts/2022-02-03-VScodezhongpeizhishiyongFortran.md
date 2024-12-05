---
layout: post
title: "VScode中配置使用Fortran"
date:   2024-02-09
tags: [Fortran,VScode,安装,gfortran,代码]
comments: true
author: admin
---
# VScode中配置使用Fortran

本文将详细介绍如何在VScode中配置和使用Fortran编程语言。通过本文的指导，您将能够轻松地在VScode中设置Fortran开发环境，并开始编写和调试Fortran代码。

## 配置步骤

### 1. 安装VScode
首先，确保您已经安装了最新版本的VScode。如果尚未安装，请访问VScode官方网站下载并安装。

### 2. 安装Fortran扩展
在VScode中，打开扩展视图（快捷键：Ctrl+Shift+X），搜索并安装以下扩展：
- **Modern Fortran**：提供Fortran语言支持，包括语法高亮、代码补全等功能。
- **Code Runner**：用于运行Fortran代码。

### 3. 安装Fortran编译器
为了在VScode中编译和运行Fortran代码，您需要安装一个Fortran编译器。推荐使用GNU Fortran编译器（gfortran）。

#### 在Windows上安装gfortran
1. 下载并安装MinGW（Minimalist GNU for Windows）。
2. 在MinGW安装过程中，确保选择安装gfortran。
3. 将MinGW的bin目录添加到系统的环境变量PATH中。

#### 在Linux上安装gfortran
打开终端并运行以下命令：
```bash
sudo apt-get install gfortran
```

#### 在macOS上安装gfortran
使用Homebrew安装gfortran：
```bash
brew install gcc
```

### 4. 配置VScode
在VScode中，打开设置（快捷键：Ctrl+,），搜索`code-runner.executorMap`，找到并编辑该设置，添加以下内容：
```json
"code-runner.executorMap": {
    "fortran": "cd $dir && gfortran $fileName -o $fileNameWithoutExt && $dir$fileNameWithoutExt"
}
```

### 5. 编写和运行Fortran代码
1. 在VScode中创建一个新的Fortran文件（扩展名为`.f90`）。
2. 编写您的Fortran代码。
3. 使用Code Runner扩展运行代码（快捷键：Ctrl+Alt+N）。

## 总结
通过以上步骤，您已经成功在VScode中配置了Fortran开发环境。现在，您可以开始编写、调试和运行Fortran代码了。希望本文对您有所帮助！

## 下载链接

[VScode中配置使用Fortran](https://pan.quark.cn/s/8f4ef6ec5c0e)