---
layout: post
title: "Unity TMPTextMesh Pro中文输入问题解决方案"
date:   2021-09-17
tags: [字体,中文,Unity,TMP,资源]
comments: true
author: admin
---
# Unity TMP(TextMesh Pro)中文输入问题解决方案

本资源文件旨在解决Unity中使用TextMesh Pro（TMP）组件时遇到的中文输入问题。通过本资源，您可以学习如何配置TMP以支持中文输入，并解决常见的乱码和不显示问题。

## 内容概述

1. **问题描述**：
   - 默认情况下，Unity的TextMesh Pro组件可能无法正确显示中文，导致出现乱码或“口口”字符。

2. **解决方法**：
   - **创建字体资源**：
     1. 打开`Window -> TextMeshPro -> Font Asset Creator`。
     2. 设置`Source Font File`为包含中文字体的文件（如Windows系统字体目录中的字体）。
     3. 设置`Character Set`为`Characters from File`，并创建一个包含常用中文字符的文本文件。
     4. 点击`Generate Font Atlas`生成新的字体资源。
   - **解决字体资源生成错误**：
     1. 如果生成字体资源时报错`Error Code [Invalid_File_Format]`，可能是因为字体文件类型不兼容。
     2. 使用`FontCreator`软件修改字体文件的名称和类型，确保Unity能够正确识别。
   - **解决字体烘焙丢失问题**：
     1. 检查文本文件的编码格式，确保为`Unicode`。
     2. 重新生成字体资源，确保所有字符都被正确烘焙。

3. **使用说明**：
   - 将生成的字体资源拖入TMP的`Font Asset`中，即可在项目中使用该字体显示中文。

## 注意事项

- 确保字体文件路径不包含中文，以避免潜在的字体丢失问题。
- 如果遇到其他问题，请参考文章中的详细步骤进行排查。

通过本资源文件，您可以轻松解决Unity TMP中中文输入的相关问题，提升项目中的文本显示效果。

## 下载链接

[UnityTMPTextMeshPro中文输入问题解决方案](https://pan.quark.cn/s/7a985b56aac7)