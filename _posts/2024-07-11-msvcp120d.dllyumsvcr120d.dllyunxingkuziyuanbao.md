---
layout: post
title: "msvcp120d.dll与msvcr120d.dll运行库资源包"
date:   2023-10-15
tags: [dll,msvcp120d,msvcr120d,Visual,DLL]
comments: true
author: admin
---
# msvcp120d.dll与msvcr120d.dll运行库资源包

## 概述

当您在尝试使用Visual Studio 2015进行项目开发，特别是集成OpenCV等库时，可能会遇到缺少msvcp120d.dll和msvcr120d.dll运行时库的问题。这两个DLL文件是Microsoft Visual C++ 2013的调试版本动态链接库，对于开发环境至关重要。本仓库提供了这两种DLL文件的完整套装，包含32位与64位版本，以帮助解决因缺失这些依赖而引发的运行错误。

## 文件说明及安装步骤

- **msvcp120d.dll**：Microsoft Visual C++ 2013调试版运行时库文件。
- **msvcr120d.dll**：同样属于Visual C++ 2013调试版的重要组件。

### 安装指引：

#### 对于32位系统：
将32位的`msvcp120d.dll`和`msvcr120d.dll`复制到：
```
C:\Windows\SysWOW64\
```

#### 对于64位系统：
64位系统的用户应将对应的`msvcp120d.dll`和`msvcr120d.dll`文件放置于：
```
C:\Windows\System32\
```

**重要提示**：确保您的操作符合系统架构（32位或64位），以避免不兼容问题。此外，放置这些文件时可能需要管理员权限。

## 注意事项

- 在安装这些DLL之前，建议备份原有的文件以防万一。
- 如果是在开发环境中遇到问题，考虑通过Visual Studio的安装程序添加缺失的组件也是一个解决方案。
- 仅适用于开发环境下遇到的特定错误，如果应用发布后还依赖这些调试库，需转换到相应的release版本库。

## 结语

本资源旨在为开发者快速解决开发过程中遇到的特定依赖问题，希望对您有所帮助。正确安装这些DLL文件后，应该能顺利解决由于缺失这两款运行时库而导致的编译或运行错误。如果您在使用过程中还有其他技术难题，推荐查阅官方文档或社区寻求更广泛的帮助。

## 下载链接

[msvcp120d.dll与msvcr120d.dll运行库资源包](https://pan.quark.cn/s/37ff9d01169d)