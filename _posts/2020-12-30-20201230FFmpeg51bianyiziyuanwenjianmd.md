---
layout: post
title: "FFmpeg 51 编译资源文件"
date:   2024-05-06
tags: [编译,FFmpeg,文件,代码生成,资源]
comments: true
author: admin
---
# FFmpeg 5.1 编译资源文件

本仓库提供了一个已经预编译好的 FFmpeg 5.1 资源文件，可以直接使用 Visual Studio 2019 进行编译。该资源文件已经支持 GPU 加速、H.264、H.265 等功能，并且成功编译出了静态库（lib）与动态库（dll）。

## 资源文件描述

- **编译环境**：Visual Studio 2019
- **支持功能**：GPU 加速、H.264、H.265 等
- **编译结果**：静态库（lib）与动态库（dll）

## 使用说明

1. **代码生成设置**：
   - 该资源文件的代码生成设置依赖于 VC 运行库。如果需要修改代码生成选项，请将所有工程文件的代码生成选项修改为 `MTd` 或 `MT`。

2. **依赖项安装**：
   - 使用提供的脚本安装 YASM 与 NASM：
     - 运行 `VSNASM\install_script.bat`
     - 运行 `VSYASM\install_script.bat`

3. **编译步骤**：
   - 打开 Visual Studio 2019，加载项目文件 `projects\FFmpeg\SMP\ffmpeg_deps.sln`。
   - 编译项目，生成的文件将位于 `msvc` 目录下。

## 其他说明

- 原项目地址：[ShiftMediaProject/FFmpeg](https://github.com/ShiftMediaProject/FFmpeg)
- 参考文章：[知乎专栏文章](https://zhuanlan.zhihu.com/p/64442121)

## 注意事项

- 该资源文件已经下载了所有依赖项，可以直接使用。
- 如果需要进一步修改或自定义编译选项，请参考相关文档进行操作。

---

希望这个资源文件能够帮助你顺利进行 FFmpeg 5.1 的编译和使用！

## 下载链接

[FFmpeg5.1编译资源文件](https://pan.quark.cn/s/51a973ed32fd)