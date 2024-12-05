---
layout: post
title: "删除Xftp后WindowsInstall弹出Xftp安装窗口的解决办法"
date:   2021-01-28
tags: [Xftp,卸载,安装,删除,软件]
comments: true
author: admin
---
# 删除Xftp后，WindowsInstall弹出Xftp安装窗口的解决办法

## 简介

在使用Xftp过程中，如果直接删除Xftp的安装文件夹，可能会导致Windows系统在启动其他软件或系统时弹出Xftp的安装提示窗口。这是因为删除Xftp时，部分路径临时文件仍然存在，导致系统误以为需要重新安装Xftp。

## 问题描述

非正规卸载Xftp后，点击某些软件会使软件不能正常运行，而弹出要求安装msi文件的提示框。

## 解决方案

1. **下次一定要去卸载中心卸载软件**：确保使用系统的卸载程序来彻底移除软件。
2. **使用Windows Install Clean Up工具**：
   - 下载并安装`msicuu.exe`工具。
   - 以管理员模式运行安装。
   - 运行后打开工具，找到Xftp软件的名字并移除。

## 注意事项

- 确保在卸载软件时使用正规的卸载程序，避免直接删除安装文件夹。
- 使用Windows Install Clean Up工具时，务必以管理员身份运行，以确保操作的有效性。

通过以上步骤，可以有效解决删除Xftp后弹出安装提示的问题。

## 下载链接

[删除Xftp后WindowsInstall弹出Xftp安装窗口的解决办法分享](https://pan.quark.cn/s/cfa7ed315302)