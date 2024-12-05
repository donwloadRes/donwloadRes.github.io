---
layout: post
title: "QT5生成PDF方案"
date:   2022-05-14
tags: [PDF,生成,QT5,文件,pdf]
comments: true
author: admin
---
# QT5生成PDF方案

本仓库提供了一个使用QT5生成PDF的资源文件，详细介绍了如何通过QT5的QPdfWriter方式生成PDF文件。该方案包含了两种不同的实现方式，分别展示了如何生成纯文字版的PDF以及如何创建包含页眉、页脚和内容排版的PDF报告。

## 方案描述

### 1. pdfWriter1()
- **功能**：使用QpdfWriter和QPainter进行纯文字版的PDF生成和绘制，并进行了分页显示。
- **输出文件**：生成的PDF文件保存在当前目录下，文件名为`pdf_test.pdf`。

### 2. pdfWriter2()
- **功能**：使用QPdfwriter和QPainter创建包含页眉、页脚和内容排版的PDF报告。
  - **页眉**：左上角为图片logo，右边为页数提示。
  - **页脚**：包含生成报告的时间和公司logo布局。
  - **图像缩放**：图像的缩放不采用scale，而是直接使用Rect来缩放，例如缩小原图的一半，只需设置`image.width/2`。
- **输出文件**：生成的PDF文件保存在当前目录下，文件名为`Report.pdf`。

## 使用方法

1. 下载本仓库的资源文件。
2. 在QT5环境中打开项目。
3. 在MainWindow中通过调用`pdfWriter1()`或`pdfWriter2()`方法来生成不同类型的PDF文件。
4. 生成的PDF文件将保存在当前目录下，文件名分别为`pdf_test.pdf`和`Report.pdf`。

## 注意事项

- 本方案适用于需要在QT5环境中生成PDF文件的开发者。
- 生成的PDF文件将直接保存在当前目录下，请确保有足够的权限进行文件写入操作。
- 图像缩放部分采用了Rect方式，适用于需要精确控制图像尺寸的场景。

通过本方案，您可以轻松地在QT5项目中实现PDF文件的生成，并根据需求进行自定义排版和内容布局。

## 下载链接

[QT5生成PDF方案](https://pan.quark.cn/s/b1f66a9312ac)