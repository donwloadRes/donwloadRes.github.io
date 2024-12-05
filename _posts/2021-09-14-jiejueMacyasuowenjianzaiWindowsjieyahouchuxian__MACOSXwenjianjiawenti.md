---
layout: post
title: "解决Mac压缩文件在Windows解压后出现__MACOSX文件夹问题"
date:   2022-09-02
tags: [Windows,解压,文件夹,__,MACOSX]
comments: true
author: admin
---
# 解决Mac压缩文件在Windows解压后出现__MACOSX文件夹问题

## 简介

在使用Mac系统压缩文件后，在Windows系统上解压时，经常会发现多出一个名为`__MACOSX`的文件夹。这个文件夹通常包含一些Mac系统特有的元数据信息，对于Windows用户来说，这些信息是无用的。本资源文件旨在提供解决方案，帮助用户在Mac上压缩文件时避免生成`__MACOSX`文件夹，从而在Windows上解压时不会出现多余的文件夹。

## 解决方案

### 方法一：使用CleanArchiver软件进行压缩

1. 下载并安装CleanArchiver软件。
2. 打开CleanArchiver，选择要压缩的文件或文件夹。
3. 点击顶部菜单中的`File` -> `Compress`，选择要压缩的文件，然后进行压缩。

### 方法二：在Windows下使用命令行解压

在Windows系统下，可以使用以下命令解压文件，避免解压出`__MACOSX`文件夹：

```bash
unzip 文件名.zip -x __MACOSX/*
```

## 注意事项

- 使用CleanArchiver压缩文件时，确保选择正确的压缩格式，以避免在Windows上解压时出现问题。
- 在Windows上使用命令行解压时，确保已安装`unzip`工具。

## 总结

通过上述方法，您可以有效避免在Mac上压缩文件后，在Windows上解压时出现多余的`__MACOSX`文件夹，从而提高文件传输和共享的效率。

## 下载链接

[解决Mac压缩文件在Windows解压后出现__MACOSX文件夹问题分享](https://pan.quark.cn/s/e5cdfd7a66ab)