---
layout: post
title: "使用Nuitka打包Python代码为EXE可执行程序"
date:   2023-05-01
tags: [Python,--,EXE,打包,Nuitka]
comments: true
author: admin
---
# 使用Nuitka打包Python代码为EXE可执行程序

本文介绍了如何使用Nuitka工具将Python代码打包为EXE可执行程序。Nuitka是一个将Python代码转换为C代码并编译成可执行文件的工具，适用于在没有Python环境的Windows系统上运行Python程序。

## 一、Nuitka简介

Nuitka是一个将Python代码打包为EXE可执行文件的工具。其原理是将部分Python代码（自己编写的部分）转换成C代码，以提高运行速度。导入的第三方包不进行编译，而是在运行时通过一个`python3x.dll`的动态链接库执行第三方包的Python代码，从而减少EXE包的大小。

## 二、Nuitka打包流程

### 1. 环境准备

- **Python环境**: 使用conda 4.7.12，Python 3.6.13，numpy 1.16.4，pyqt5 5.15.4。
- **C编译器**: 下载并安装MinGW64 8.1，并添加到系统环境变量中。

### 2. 下载Nuitka

使用pip或conda安装Nuitka：
```bash
pip install nuitka
```
或
```bash
conda install nuitka
```

### 3. 使用Nuitka打包Python代码

#### 简单打包

1. 新建一个简单的Python文件，确保其可以正常运行。
2. 使用以下命令进行打包：
   ```bash
   nuitka xxx.py
   ```
3. 根据提示下载所需的包，并手动解压到指定文件夹中。
4. 重新执行打包命令，直到打包成功。

#### 打包PyQt5项目

使用以下命令打包包含PyQt5的项目：
```bash
nuitka --standalone --mingw64 --show-progress --show-memory --nofollow-imports --plugin-enable=qt-plugins --include-qt-plugins=sensible,styles --output-dir=out --windows-icon-from-ico=favicon.ico start.py
```

### 4. 调试与优化

- **调试**: 在打包后的目录中运行EXE文件，根据报错信息逐步添加缺少的第三方包和自定义包。
- **优化**: 正式打包时，可以添加`--windows-disable-console`参数，避免显示CMD控制窗口。

### 5. 移植与分发

- **移植**: 确保所有依赖包都复制到EXE文件的同一目录下，避免路径问题。
- **分发**: 可以使用Inno Setup等工具将EXE文件封装成安装包，方便用户安装。

## 三、常见问题与解决方案

- **第三方包导入问题**: 使用`--plugin-enable=qt-plugins`等参数确保PyQt5等库正确导入。
- **路径问题**: 使用绝对路径或相对路径处理资源文件，避免打包后找不到资源。
- **移植问题**: 确保所有依赖的DLL文件都复制到目标电脑的EXE文件目录下。

通过以上步骤，您可以成功使用Nuitka将Python代码打包为EXE可执行文件，方便在没有Python环境的Windows系统上运行。

## 下载链接

[使用Nuitka打包Python代码为EXE可执行程序](https://pan.quark.cn/s/dd2f542cf843)