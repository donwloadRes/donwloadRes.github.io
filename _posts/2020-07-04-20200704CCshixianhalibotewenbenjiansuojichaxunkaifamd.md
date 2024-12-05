---
layout: post
title: "C-C++ 实现哈利波特文本检索及查询开发"
date:   2020-04-07
tags: [查询,哈利波,读取,文本,结果]
comments: true
author: admin
---
# C/C++ 实现哈利波特文本检索及查询开发

## 项目简介

本项目是一个基于C/C++语言的简单实现，旨在提供哈利波特系列小说的文本检索及查询功能。通过读取哈利波特系列小说的文本文件，用户可以输入人名或地名，系统将显示查询结果，并提供查询结果所在位置前后的一段文字。

## 功能特点

1. **文本读取与存储**：
   - 支持读取哈利波特系列小说的文本文件（txt格式）。
   - 使用`fstream`头文件进行文本操作，按行读取文本内容。
   - 使用`deque`双端队列存储读取到的文本信息，便于后续查询。

2. **查询功能**：
   - 用户输入人名或地名后，系统将显示查找到的相关信息，包括出现的页码、章节和书名。
   - 查询结果按页码顺序显示，并提供每个查询结果的序号。

3. **结果展示**：
   - 用户可以选择查询结果的序号，系统将显示该结果所在位置前后的一段文字。

## 使用方法

1. **下载资源文件**：
   - 下载本仓库中的资源文件，包含哈利波特系列小说的文本文件。

2. **编译与运行**：
   - 使用C/C++编译器编译项目源代码。
   - 运行编译后的可执行文件，按照提示输入查询内容。

3. **查询操作**：
   - 输入要查询的人名或地名，系统将显示相关查询结果。
   - 选择查询结果的序号，查看详细内容。

## 注意事项

- 本项目仅支持英文文本的读取和查询，中文文本可能会导致读取错误。
- 查询结果的准确性依赖于文本文件的格式和内容。

## 贡献与反馈

欢迎对本项目提出改进建议或贡献代码。如有任何问题，请在项目仓库中提交Issue。

## 许可证

本项目遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[CC实现哈利波特文本检索及查询开发](https://pan.quark.cn/s/0db3e91e8929)