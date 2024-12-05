---
layout: post
title: "Ubuntu安装中文字体及Python Matplotlib绘图显示中文指南"
date:   2024-07-25
tags: [字体,Matplotlib,中文字体,Ubuntu,Python]
comments: true
author: admin
---
# Ubuntu安装中文字体及Python Matplotlib绘图显示中文指南

本资源文件提供了在Ubuntu系统上安装中文字体，并配置Python的Matplotlib库以支持中文显示的详细步骤。通过本指南，您将能够解决在Matplotlib绘图中无法正确显示中文的问题。

## 内容概述

1. **下载中文字体**：提供了SimHei和SimKai字体的下载方法。
2. **上传字体到服务器**：指导如何将下载的字体文件上传到Ubuntu服务器。
3. **安装字体**：详细说明了如何将字体文件复制到指定目录并进行安装。
4. **配置Matplotlib**：提供了在Python脚本中配置Matplotlib以使用中文字体的代码示例。

## 使用步骤

### 1. 下载字体

首先，您需要下载SimHei和SimKai字体文件。这些字体文件可以在Windows系统的`C:/Windows/Fonts`目录中找到，或者通过提供的链接下载。

### 2. 上传字体到服务器

使用工具（如WinSCP）将下载的字体文件上传到Ubuntu服务器的指定目录，例如`/home/wzg/Downloads/fonts/`。

### 3. 安装字体

将字体文件复制到系统的字体目录中，例如`/usr/share/fonts/truetype/noto/`，并执行以下命令：

```bash
cd /home/wzg/Downloads/fonts
sudo cp -i simhei.ttf /usr/share/fonts/truetype/noto/
sudo cp -i simkai.ttf /usr/share/fonts/truetype/noto/
```

### 4. 配置Matplotlib

在您的Python脚本中添加以下代码，以确保Matplotlib使用中文字体：

```python
import matplotlib
matplotlib.rcParams['font.sans-serif'] = ['SimHei']  # 或者使用'KaiTi'
matplotlib.rcParams['axes.unicode_minus'] = False  # 解决负号显示问题
```

## 注意事项

- 确保字体文件正确上传并复制到指定目录。
- 在配置Matplotlib时，确保字体名称正确无误。

通过以上步骤，您应该能够在Ubuntu系统上成功安装中文字体，并在Python的Matplotlib绘图中正确显示中文。

## 下载链接

[Ubuntu安装中文字体及PythonMatplotlib绘图显示中文指南](https://pan.quark.cn/s/8da1d5ae1486)