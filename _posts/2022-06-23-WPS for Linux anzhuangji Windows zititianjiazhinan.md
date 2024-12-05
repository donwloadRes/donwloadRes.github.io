---
layout: post
title: "WPS for Linux 安装及 Windows 字体添加指南"
date:   2022-12-26
tags: [字体,ttf,WPS,Linux,Windows]
comments: true
author: admin
---
# WPS for Linux 安装及 Windows 字体添加指南

本资源文件提供了在 Linux 系统上安装 WPS Office 的详细步骤，并指导用户如何添加 Windows 字体以确保文档的正确显示。以下是具体操作步骤：

## 安装 WPS Office

1. **下载安装包**：
   - 从 WPS 官网下载适用于 Linux 的安装包。

2. **安装 WPS Office**：
   - 使用命令 `sudo dpkg -i wps-office_版本号_i386.deb` 安装下载的安装包。

## 添加 Windows 字体

1. **准备字体文件**：
   - 从 Windows 系统中复制所需字体文件到 Linux 系统。常见的字体包括：
     - 宋体：`simsunb.ttf` 和 `simsun.ttc`
     - 微软雅黑：`msyhbd.ttf`
     - Courier New：`courbd.ttf`、`courbi.ttf`、`couri.ttf` 和 `cour.ttf`
     - WPS Office 所需字体：`wingding.ttf`、`webdings.ttf`、`symbol.ttf`、`WINGDNG3.TTF`、`WINGDNG2.TTF`、`MTExtra.ttf`

2. **创建字体存放目录**：
   - 在 `/usr/share/fonts/truetype/` 目录下创建一个新的目录，例如 `windows-font`。

3. **复制字体文件**：
   - 将复制的字体文件复制到新建的 `windows-font` 目录中。

4. **修改权限并更新字体缓存**：
   - 修改字体目录权限：`sudo chmod -R 777 /usr/share/fonts/truetype/windows-font`
   - 更新字体缓存：
     ```bash
     cd /usr/share/fonts/truetype/windows-font
     sudo mkfontscale
     sudo mkfontdir
     sudo fc-cache -fv
     ```

5. **重启系统**：
   - 重启系统以确保字体更改生效。

通过以上步骤，您可以在 Linux 系统上成功安装 WPS Office 并添加 Windows 字体，确保文档的正确显示。

## 下载链接

[WPSforLinux安装及Windows字体添加指南分享](https://pan.quark.cn/s/6787e140b6d1)