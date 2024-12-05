---
layout: post
title: "FFTW开源库文件及源码下载"
date:   2024-09-21
tags: [lib,FFTW,文件,dll,源码]
comments: true
author: admin
---
# FFTW开源库文件及源码下载

## 资源描述

本仓库提供了FFTW官方源码，以及经过编译的适用于Windows的32位和64位的lib、dll文件。FFTW是一个用于计算一维或多维离散傅里叶变换的C语言子函数库，支持实数序列和复数序列的输入。FFTW是免费软件，是各种应用中fft函数库的上佳选择。

## 资源内容

- **FFTW官方源码**：包含FFTW的完整源代码，方便用户自行编译和修改。
- **32位lib、dll文件**：适用于32位Windows系统的编译文件。
- **64位lib、dll文件**：适用于64位Windows系统的编译文件。

## 使用说明

1. **DLL文件放置**：
   - 将`libfftw3f-3.dll`、`libfftw3-3.dll`和`libfftw3l-3.dll`文件放入`C:\Windows\SysWOW64`（如果是32位系统，则放入`C:\Windows\System32`）。

2. **库文件放置**：
   - 将生成的库文件`libfftw3-3.lib`、`libfftw3f-3.lib`、`libfftw3l-3.lib`放入VC的`lib`文件夹。
   - 将`fftw3.h`文件放入VC的`include`文件夹。

3. **新建工程应用**：
   - **头文件**：在代码中添加`#include "fftw3.h"`。
   - **设置参数**：在项目属性中，配置属性 -> 链接器 -> 输入 -> 附加依赖项，添加以下三项：
     - `libfftw3-3.lib`
     - `libfftw3f-3.lib`
     - `libfftw3l-3.lib`

## 注意事项

- 请根据您的系统位数选择合适的lib和dll文件。
- 确保所有文件路径正确，以避免编译错误。

## 贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

FFTW是免费软件，遵循其官方许可证。请参考源码中的LICENSE文件获取更多信息。

## 下载链接

[FFTW开源库文件及源码下载](https://pan.quark.cn/s/b789c58b6b0a)