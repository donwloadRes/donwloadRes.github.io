---
layout: post
title: "Linux 系统缺失字体解决方案"
date:   2022-03-01
tags: [字体,Linux,WPS,Office,Wingdings]
comments: true
author: admin
---
# Linux 系统缺失字体解决方案

## 简介

本仓库提供了一个资源文件，用于解决Linux系统中WPS Office无法正确显示某些符号（公式）的问题。具体来说，WPS Office在Linux系统中可能会提示缺失以下字体：

- Symbol
- Wingdings
- Wingdings 2
- Wingdings 3
- Webdings
- MT Extra

这些字体缺失会导致WPS Office无法正确显示文档中的某些符号和公式，影响文档的阅读和编辑体验。

## 解决方案

通过下载并安装本仓库提供的字体文件，可以解决上述问题，确保WPS Office在Linux系统中能够正确显示所有符号和公式。

## 使用方法

1. **下载字体文件**：
   - 从本仓库下载字体文件压缩包。

2. **安装字体**：
   - 解压下载的字体文件压缩包。
   - 将解压后的字体文件复制到Linux系统的字体目录中，通常为 `/usr/share/fonts/`。

3. **更新字体缓存**：
   - 打开终端，运行以下命令更新字体缓存：
     ```bash
     sudo fc-cache -vf
     ```

4. **重启WPS Office**：
   - 重新启动WPS Office，检查是否能够正确显示所有符号和公式。

## 注意事项

- 确保字体文件具有正确的权限，通常需要设置为 `644` 权限。
- 如果系统中已经存在同名字体文件，建议先备份原有字体文件，再进行替换。

## 参考资料

有关更多详细信息和操作步骤，请参考以下文章：
- [Linux 系统缺失字体：Symbol､Wingdings､Wingdings 2､Wingdings 3､Webdings､MT Extra,WPS无法正确地显示某些符号(公式)！](https://blog.csdn.net/u013669912/article/details/139678684)

通过以上步骤，您可以轻松解决WPS Office在Linux系统中缺失字体的问题，提升文档编辑和阅读的体验。

## 下载链接

[Linux系统缺失字体解决方案](https://pan.quark.cn/s/e3510fb9370f)