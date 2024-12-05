---
layout: post
title: "Tesseract-OCR 安装与环境变量配置指南"
date:   2023-10-05
tags: [OCR,Tesseract,安装,环境变量,配置]
comments: true
author: admin
---
# Tesseract-OCR 安装与环境变量配置指南

本资源文件提供了关于Tesseract-OCR的安装与环境变量配置的详细步骤。Tesseract-OCR是一个开源的光学字符识别（OCR）引擎，广泛用于从图像中提取文本。以下是安装和配置Tesseract-OCR的步骤。

## 安装步骤

1. **下载Tesseract-OCR安装包**：
   - 访问Tesseract-OCR的官方下载页面，选择适合你操作系统的版本进行下载。
   - 如果你在下载过程中遇到困难，可以使用提供的备用下载链接。

2. **安装Tesseract-OCR**：
   - 双击下载的安装包，按照安装向导的指示进行安装。
   - 在安装过程中，确保选择安装语言包，特别是英语和数学语言包。
   - 安装完成后，记住安装路径，后续配置环境变量时会用到。

## 环境变量配置

1. **打开Tesseract-OCR的安装目录**，复制安装路径。
2. **配置系统环境变量**：
   - 右键点击“此电脑”或“我的电脑”，选择“属性”。
   - 点击“高级系统设置”，找到“环境变量”。
   - 在“系统变量”中找到“Path”，点击“编辑”。
   - 在“变量值”字段中添加Tesseract-OCR的安装路径，多个路径之间用分号隔开。
   - 点击“确定”保存更改。

3. **配置TESSDATA_PREFIX变量**：
   - 在“系统变量”中，新建一个变量名称为“TESSDATA_PREFIX”。
   - 变量值为Tesseract-OCR的安装路径加上`\tessdata`。
   - 点击“确定”保存更改。

## 测试Tesseract-OCR

1. **准备测试图片**：
   - 选择一张包含文本的图片，将其放在一个易于访问的目录中，例如`D:\photos`。

2. **打开命令提示符**：
   - 进入图片所在的目录。
   - 输入以下命令进行文字识别：
     ```
     tesseract test.jpg output_1 –l eng
     ```
   - 运行结果将生成一个名为`output_1.txt`的文件，其中包含识别出的文本。

通过以上步骤，你已经成功安装并配置了Tesseract-OCR，并进行了简单的文字识别测试。希望这个指南对你有所帮助！

## 下载链接

[Tesseract-OCR安装与环境变量配置指南分享](https://pan.quark.cn/s/7bba74eb10e8)