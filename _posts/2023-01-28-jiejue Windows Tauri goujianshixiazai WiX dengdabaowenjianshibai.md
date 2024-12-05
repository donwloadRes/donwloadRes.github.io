---
layout: post
title: "解决 Windows Tauri 构建时下载 WiX 等打包文件失败"
date:   2020-02-26
tags: [文件,下载,Tauri,WiX,复制到]
comments: true
author: admin
---
# 解决 Windows Tauri 构建时下载 WiX 等打包文件失败

## 简介

在 Windows 环境下使用 Tauri 构建应用程序时，可能会遇到下载 WiX 等打包文件失败的问题。本文提供了一个解决方案，帮助开发者顺利完成 Tauri 应用程序的构建。

## 解决方案

1. **WiX 工具包下载失败**：
   - 手动下载 `wix311-binaries.zip` 文件。
   - 创建一个名为 `WixTools` 的文件夹，并将解压后的文件复制到该文件夹中。

2. **NSIS 工具包下载失败**：
   - 手动下载 `nsis-3.zip` 文件。
   - 在 Tauri 项目目录下新建一个名为 `NSIS` 的文件夹，并将解压后的文件复制到该文件夹中。
   - 下载 `NSIS-ApplicationID` 插件，将解压后的文件复制到 `Plugins` 目录下。
   - 将 `ReleaseUnicode` 目录下的 `applicationid.dll` 文件复制到 `x86-unicode` 目录。
   - 将 `nsis_tauri_utils.dll` 文件也复制到 `x86-unicode` 目录。

## 注意事项

- 新建文件夹时注意大小写。
- 确保所有文件正确放置在指定目录中，以避免构建过程中的错误。

通过以上步骤，可以有效解决 Windows 环境下 Tauri 构建时下载 WiX 等打包文件失败的问题。

## 下载链接

[解决WindowsTauri构建时下载WiX等打包文件失败](https://pan.quark.cn/s/4f9c73f15b58)