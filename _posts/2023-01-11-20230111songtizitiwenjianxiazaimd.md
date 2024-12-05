---
layout: post
title: "宋体字体文件下载"
date:   2020-05-04
tags: [字体,宋体,文件,Docker,容器]
comments: true
author: admin
---
# 宋体字体文件下载

## 资源介绍

本仓库提供宋体（SimSun）字体的ttf和ttc文件下载，适用于CentOS系统和Docker容器环境。这些字体文件可以帮助你在各种Linux环境下正常显示和使用宋体字体。

## 文件说明

- **simsun.ttf**: 宋体的TrueType字体文件。
- **simsun.ttc**: 宋体的TrueType Collection字体文件。

## 适用环境

- **CentOS系统**: 适用于CentOS操作系统的字体安装。
- **Docker容器**: 适用于Docker容器内的字体配置。

## 使用方法

1. **下载文件**: 点击仓库中的文件链接，下载所需的ttf或ttc文件。
2. **安装字体**:
   - 在CentOS系统中，将下载的字体文件复制到`/usr/share/fonts/`目录下，然后运行`fc-cache -fv`命令刷新字体缓存。
   - 在Docker容器中，将字体文件复制到容器的`/usr/share/fonts/`目录下，并执行`fc-cache -fv`命令。

## 注意事项

- 请确保你有权限将字体文件复制到系统字体目录。
- 在Docker容器中使用时，请确保容器内有`fc-cache`工具。

## 支持与反馈

如果你在使用过程中遇到任何问题或有任何建议，欢迎在仓库中提交Issue，我们会尽快回复并提供帮助。

## 下载链接

[宋体字体文件下载](https://pan.quark.cn/s/c74627ed7e76)