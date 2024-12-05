---
layout: post
title: "PowerBuilder 105下通过福晰ocx控件实现PDF文件浏览和打印"
date:   2021-06-23
tags: [PDF,控件,PowerBuilder,浏览,ocx]
comments: true
author: admin
---
# PowerBuilder 10.5下通过福晰ocx控件实现PDF文件浏览和打印

## 背景

在单位中，原本使用BS方式通过浏览器调阅服务器上的PDF文件。然而，由于单位内同时存在XP、Win7和Win10操作系统，浏览器调用PDF文件时经常出现误报本地未安装PDF阅读器的情况。为了解决这一问题，我尝试通过本地的PDF控件实现直接调阅功能。经过几天的研究和实践，终于在PowerBuilder 10.5下成功实现了这一功能。

## 描述

本资源文件提供了一个在PowerBuilder 10.5下实现PDF文件浏览和打印功能的解决方案。通过使用福晰的ocx控件`FoxitPDFSDK_AX_Pro.ocx`，可以实现PDF文件的浏览和打印功能。PDF浏览界面可以根据需求进行定制，通过代码可以对阅读器的按钮进行隐藏和显示。虽然本示例基于PowerBuilder 10.5，但对于其他版本的PowerBuilder，实现方式应该大同小异。

## 资源内容

- **PowerBuilder 10.5源代码**：包含实现PDF文件浏览和打印功能的源代码。
- **FoxitPDFSDK_AX_Pro.ocx控件**：福晰提供的ocx控件，用于实现PDF文件的浏览和打印。
- **控件API文档**：一份可以参考的控件API文档，帮助你更好地理解和使用该控件。

## 使用说明

1. **下载资源**：下载本仓库中的所有文件。
2. **导入控件**：将`FoxitPDFSDK_AX_Pro.ocx`控件导入到你的PowerBuilder项目中。
3. **运行代码**：打开PowerBuilder 10.5，导入提供的源代码，运行程序即可实现PDF文件的浏览和打印功能。
4. **定制界面**：根据需求，通过代码对PDF浏览界面进行定制，隐藏或显示相关按钮。

## 参考文章

如果你希望更详细地了解如何在PowerBuilder 10.5下实现PDF文件的浏览和打印功能，可以参考我的另一篇原创文章《PowerBuilder 10 下调用FoxitPDFSDK_AX_Pro.ocx浏览打印PDF文件》。

希望这个资源对你有所帮助！

## 下载链接

[PowerBuilder10.5下通过福晰ocx控件实现PDF文件浏览和打印](https://pan.quark.cn/s/7cf2cf8b4319)