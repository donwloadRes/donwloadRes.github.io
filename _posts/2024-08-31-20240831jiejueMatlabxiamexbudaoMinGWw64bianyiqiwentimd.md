---
layout: post
title: "解决Matlab下mex不到 MinGWw64 编译器问题"
date:   2021-03-03
tags: [MinGW,w64,编译器,Matlab,mex]
comments: true
author: admin
---
# 解决Matlab下mex不到 MinGW-w64 编译器问题

## 简介
本资源文件旨在帮助用户解决在Matlab中使用mex命令时，无法检测到MinGW-w64编译器的问题。通过本资源文件，您可以顺利配置MinGW-w64编译器，使其能够在Matlab中正常使用。

## 问题描述
在使用Matlab进行C/C++代码编译时，用户可能会遇到以下错误提示：
```
错误使用 mex
未找到支持的编译器或 SDK。您可以安装免费提供的 MinGW-w64 C/C++ 编译器。
```
即使已经安装了MinGW-w64编译器，Matlab仍然无法检测到它，导致mex命令无法正常运行。

## 解决方案
以下是解决该问题的详细步骤：

### 1. 安装MinGW-w64编译器
首先，确保您已经正确安装了MinGW-w64编译器。可以从官方网站或其他可靠来源下载并安装。

### 2. 设置环境变量
安装完成后，需要设置系统的环境变量，以便Matlab能够找到MinGW-w64编译器。

- 打开“文件资源管理器”，右键点击“此电脑”或“计算机”，选择“属性”。
- 点击“高级系统设置”，然后选择“环境变量”。
- 在“系统变量”中，找到并编辑“Path”变量，添加MinGW-w64的bin目录路径。
- 新建一个系统变量，变量名为`MW_MINGW64_LOC`，变量值为MinGW-w64的安装路径。

### 3. 验证安装
在命令提示符（cmd）中输入以下命令，验证MinGW-w64编译器是否安装成功：
```
gcc -v
```
如果显示gcc的版本信息，则表示安装成功。

### 4. 配置Matlab
打开Matlab，输入以下命令：
```
mex -setup
```
如果仍然提示找不到MinGW-w64编译器，可以尝试以下步骤：

- 检查Matlab安装路径下的`bin/win64/mexopts`文件夹，确保其中包含`mingw64.xml`和`mingw64_g++.xml`文件。
- 如果没有这些文件，可以从本资源文件中提供的链接下载并放置到上述路径中。

### 5. 重新运行mex命令
完成上述配置后，再次运行`mex -setup`命令，Matlab应该能够正确检测到MinGW-w64编译器。

## 注意事项
- 确保Matlab版本与MinGW-w64编译器版本兼容。
- 如果遇到其他问题，可以参考资源文件中的详细描述文章进行排查。

通过以上步骤，您应该能够成功解决Matlab下mex不到MinGW-w64编译器的问题，顺利进行C/C++代码的编译工作。

## 下载链接

[解决Matlab下mex不到MinGW-w64编译器问题](https://pan.quark.cn/s/7b87a32940e7)