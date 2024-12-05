---
layout: post
title: "Linux中文字体包语言包"
date:   2020-06-05
tags: [字体,bash,Linux,mkfontscale,生效]
comments: true
author: admin
---
# Linux中文字体包语言包

## 简介

本仓库提供了一个用于解决Linux环境下Java应用生成图片乱码问题的中文字体包语言包。该资源文件包含了必要的字体文件，通过简单的安装步骤即可使字体在系统中生效，从而解决乱码问题。

## 使用方法

1. **下载资源文件**：
   - 下载本仓库中的字体包文件。

2. **解压文件**：
   - 将下载的字体包文件解压至 `/usr/share/fonts` 目录下。

3. **执行字体索引命令**：
   - 依次执行以下命令以使字体生效：
     ```bash
     mkfontscale
     mkfontdir
     fc-cache
     ```

4. **检查字体是否生效**：
   - 如果字体未生效，可以尝试重启服务器或执行以下命令：
     ```bash
     source /etc/profile
     ```

5. **安装缺失的工具**：
   - 如果提示没有 `mkfontscale` 或 `fontconfig`，请执行以下命令进行安装：
     ```bash
     yum install mkfontscale
     yum install fontconfig
     ```

6. **验证字体安装**：
   - 进入 `/usr/share/fonts` 目录，分别执行以下命令：
     ```bash
     mkfontscale
     mkfontdir
     fc-cache
     ```
   - 查看黑体常规字体是否安装成功：
     ```bash
     fc-list :lang=zh
     ```

## 注意事项

- 确保在执行命令时具有足够的权限。
- 如果字体仍未生效，建议重启服务器以确保所有更改生效。

通过以上步骤，您应该能够成功解决Linux环境下Java应用生成图片乱码的问题。

## 下载链接

[Linux中文字体包语言包](https://pan.quark.cn/s/d74f5c528ac7)