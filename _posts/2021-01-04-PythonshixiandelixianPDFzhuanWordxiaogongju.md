---
layout: post
title: "Python实现的离线PDF转Word小工具"
date:   2021-09-03
tags: [Python,源码,PDF,Word,离线]
comments: true
author: admin
---
# Python实现的离线PDF转Word小工具

## 简介

本仓库提供了一个离线的PDF转Word小工具，无需网络即可使用。该工具使用Python编写，基于PyQt5实现了一个简单的图形用户界面，并集成了pdf2docx第三方包来完成PDF到Word的转换。为了在前端界面中打印更多的日志信息，我们对pdf2docx包中的Converter类进行了改进，增加了回调函数功能，使得转换过程中的信息可以直接反馈到前端界面。

## 功能特点

- **离线使用**：无需网络连接，随时随地进行PDF到Word的转换。
- **图形界面**：使用PyQt5实现了一个简单易用的图形用户界面，方便用户操作。
- **日志输出**：在转换过程中，程序会输出详细的日志信息，方便用户了解转换进度和状态。
- **源码开放**：提供了完整的源码，用户可以根据自己的需求进行修改和定制。

## 使用说明

1. **下载资源**：
   - 源码文件：`源码.zip`
   - 可执行程序：`PDF2Word.exe`
   - 修改后的三方处理文件：`converter.py`

2. **运行程序**：
   - 如果你有Python环境，可以直接解压`源码.zip`，运行其中的Python脚本。
   - 如果你没有Python环境，可以直接运行`PDF2Word.exe`，这是一个编译后的可执行文件，无需安装Python即可使用。

3. **自定义配置**：
   - 如果你需要自定义转换过程中的日志输出，可以修改`src/PDFTool`目录下的代码：
     ```python
     cv = Converter(self.pdf, func=self.func)   # 打印过程信息
     # cv = Converter(self.pdf)   # 不打印过程信息
     ```
   - 根据你的需求选择是否打印转换过程中的详细信息。

## 目录结构

- `源码.zip`：包含所有源码文件。
- `PDF2Word.exe`：编译后的可执行程序，无需Python环境即可运行。
- `converter.py`：修改后的pdf2docx处理文件，增加了回调函数功能。

## 注意事项

- 该工具依赖于pdf2docx第三方包，如果你需要重新编译程序，请确保安装了所有依赖项。
- 如果你在使用过程中遇到任何问题，欢迎在仓库中提交Issue，我们会尽快回复并解决问题。

## 贡献

如果你对该项目有任何改进建议或发现了bug，欢迎提交Pull Request或Issue。我们非常欢迎社区的贡献！

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[Python实现的离线PDF转Word小工具](https://pan.quark.cn/s/5542c350d1de)