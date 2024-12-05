---
layout: post
title: "pkm与png的相互转化工具"
date:   2020-11-08
tags: [pkm,png,格式,转换,工具]
comments: true
author: admin
---
# pkm与png的相互转化工具

## 简介

本资源文件提供了一个用于将pkm格式与png格式相互转化的工具。该工具基于Mali Texture Compression Tool开发，适用于Windows平台。通过该工具，用户可以轻松地将png图片转换为pkm格式，或将pkm格式的图片转换回png格式。

## 功能特点

1. **png转pkm**：
   - 支持批量转换png图片为pkm格式。
   - 生成的pkm文件包含RGB和Alpha通道。
   - 提供快速转换选项，可根据需求选择是否包含Alpha通道。

2. **pkm转png**：
   - 支持将pkm格式的图片转换回png格式。
   - 提供快速转换选项，可根据需求选择是否包含Alpha通道。

## 使用方法

1. **下载与安装**：
   - 从官网下载Mali Texture Compression Tool，或使用提供的百度云盘链接进行下载。
   - 安装完成后，将工具放置在指定目录下。

2. **png转pkm**：
   - 编写一个Windows脚本，放置在工具的bin目录下。
   - 脚本示例：
     ```batch
     @echo off
     @echo start getList
     set /p a=please input png dictionary:
     DIR %a% /B >list.txt
     for /f "delims=[" %%i in (list.txt) do etcpack.exe %a%/%%i %a%_pkm -c etc1 -s slow -as -ext PNG
     @echo pkm successful make
     del list.txt
     pause
     ```
   - 运行脚本，输入png图片所在的目录，即可在该目录下生成对应的pkm文件。

3. **pkm转png**：
   - 编写一个类似的Windows脚本，使用以下命令：
     ```batch
     etcpack [input pkm] [outputdir] -ext PNG
     ```
   - 运行脚本，输入pkm文件所在的目录，即可在该目录下生成对应的png文件。

## 注意事项

- 转换过程中，输入文件的路径应为绝对路径，否则可能会导致找不到文件。
- 如果转换速度较慢，可以去掉`-s slow`选项以加快转换速度。
- 如果不希望生成Alpha通道，可以去掉`-as`选项。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个工具。

## 许可证

本工具遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[pkm与png的相互转化工具分享](https://pan.quark.cn/s/6431e732128f)