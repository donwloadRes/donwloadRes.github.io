---
layout: post
title: "Windows 安装 zip 命令指南"
date:   2021-07-27
tags: [zip,命令,Windows,点击,文件]
comments: true
author: admin
---
# Windows 安装 zip 命令指南

## 简介
在 Windows 系统中，`zip` 命令通常不是系统自带的，因此在尝试运行 `zip` 命令时可能会遇到“'zip' 不是内部或外部命令，也不是可运行的程序或批处理文件”的错误。本资源文件提供了一个解决方案，帮助用户在 Windows 系统中安装并配置 `zip` 命令。

## 安装步骤
1. **下载 zip 命令文件**  
   下载 `zip.exe` 和 `unzip.exe` 文件，这些文件可以从提供的资源链接中获取。

2. **保存文件**  
   将下载的 `zip.exe` 和 `unzip.exe` 文件保存在一个自定义目录中，例如 `C:\zip_command`。

3. **配置环境变量**  
   将上述自定义目录路径添加到系统的环境变量 `PATH` 中。具体步骤如下：
   - 右键点击“此电脑”或“计算机”，选择“属性”。
   - 点击“高级系统设置”。
   - 在“系统属性”窗口中，点击“环境变量”。
   - 在“系统变量”部分，找到并选择 `Path`，然后点击“编辑”。
   - 在“编辑环境变量”窗口中，点击“新建”，然后输入自定义目录的路径（例如 `C:\zip_command`）。
   - 点击“确定”保存更改。

4. **验证安装**  
   打开命令提示符（CMD），输入 `zip` 命令，如果显示了 `zip` 命令的帮助信息，说明安装成功。

## 常见问题
- **运行 `zip` 命令仍然报错**  
  如果运行 `zip` 命令后仍然报错，尝试重启电脑，然后再次运行 `zip` 命令。

## 参考资料
本指南参考了以下文章：
- [Windows 中安装 zip 命令 - ‘zip‘ 不是内部或外部命令，也不是可运行的程序 或批处理文件](https://blog.csdn.net/my_codeart/article/details/103456843)

通过以上步骤，您应该能够在 Windows 系统中成功安装并使用 `zip` 命令。

## 下载链接

[Windows安装zip命令指南](https://pan.quark.cn/s/bcd7c6e2fdfd)