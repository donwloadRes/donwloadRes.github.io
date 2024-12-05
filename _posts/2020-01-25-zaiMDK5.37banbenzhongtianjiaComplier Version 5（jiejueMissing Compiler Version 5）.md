---
layout: post
title: "在MDK5.37版本中添加Complier Version 5（解决Missing Compiler Version 5）"
date:   2022-06-15
tags: [Version,Compiler,ARM,编译器,MDK5.37]
comments: true
author: admin
---
# 在MDK5.37版本中添加Complier Version 5（解决Missing Compiler Version 5）

## 简介
本资源文件旨在帮助用户在MDK5.37版本中添加Complier Version 5，以解决“Missing Compiler Version 5”的问题。通过本资源文件，用户可以顺利地将ARM Compiler Version 5集成到Keil MDK5.37中，从而确保旧版本工程文件的正常编译。

## 问题描述
在升级到MDK5.37版本后，由于编译器版本不匹配，用户在编译旧版本工程文件时可能会遇到“Missing Compiler Version 5”的错误。这是因为MDK5.37默认使用的是Version 6版本的编译器，而旧版本工程文件需要使用Version 5版本的编译器。

## 解决方案
1. **下载ARM Compiler Version 5**：首先，用户需要下载ARM Compiler Version 5的编译器。
2. **解压并复制到Keil安装目录**：将下载的ARM Compiler Version 5解压，并将其复制到Keil MDK的ARM文件夹中。
3. **配置Keil**：打开Keil软件，进入“File Extension, Books and Environment”设置，选择“Folders/Extensions”，点击“Use ARM Compiler”方框中的选项，添加刚刚下载的ARM Compiler Version 5。
4. **验证配置**：再次打开“Options”选项，确认Version 5的编译器已经成功安装并配置。

## 使用说明
1. 下载本资源文件中的ARM Compiler Version 5。
2. 按照上述解决方案中的步骤进行操作。
3. 确保所有步骤正确无误后，重新编译旧版本工程文件，问题应得到解决。

## 注意事项
- 请确保下载的ARM Compiler Version 5与您的Keil MDK版本兼容。
- 在配置过程中，请仔细检查路径设置，确保编译器文件正确放置。

通过以上步骤，用户可以顺利解决“Missing Compiler Version 5”的问题，确保工程文件的正常编译。

## 下载链接

[在MDK5.37版本中添加ComplierVersion5解决MissingCompilerVersion5](https://pan.quark.cn/s/466f5b509034)