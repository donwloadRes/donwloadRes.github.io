---
layout: post
title: "关于BI Publisher Desktop在Word中无显示问题的解决方案"
date:   2024-10-14
tags: [BI,Publisher,Word,Desktop,文件夹]
comments: true
author: admin
---
# 关于BI Publisher Desktop在Word中无显示问题的解决方案

## 简介

本资源文件旨在解决在使用Oracle BI Publisher Desktop时，Word中无法显示BI Publisher插件的问题。该问题通常出现在安装BI Publisher Desktop后，Word中没有显示相应的插件，导致无法正常使用BI Publisher功能。

## 问题描述

在使用Oracle BI Publisher Desktop时，用户可能会遇到以下问题：
- 安装BI Publisher Desktop后，Word中没有显示BI Publisher插件。
- 无法在Word中使用BI Publisher功能。

## 解决方案

### 步骤一：检查加载项

1. 打开Word，点击“文件”菜单，选择“选项”。
2. 在弹出的窗口中，选择“加载项”。
3. 在“管理”下拉菜单中选择“COM加载项”，然后点击“转到”。
4. 检查是否存在“BI Publisher Template Builder for Word 64bit”的COM加载项，并确保其已勾选。

### 步骤二：修改注册表

1. 如果上一步勾选后依然没有显示，或者根本没有这个选项，请打开注册表编辑器。
2. 导航到以下路径：`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Word\Addins`。
3. 在Addins文件夹中添加一个新的文件夹，命名为`TBAddin64`。
4. 在`TBAddin64`文件夹中添加以下字符串值：
   - `Manifest`：指向BI Publisher Desktop安装路径中的`DotNet2007`文件夹。

### 步骤三：重新启动Word

1. 完成上述步骤后，重新启动Word。
2. 进入“加载项”中，检查是否已显示BI Publisher插件。

## 注意事项

- 确保BI Publisher Desktop安装路径中存在`DotNet2007`文件夹。
- 如果缺少该文件夹，请从提供的资源文件中解压并放置到正确的路径。

## 结论

通过以上步骤，您应该能够解决BI Publisher Desktop在Word中无显示的问题，并顺利使用BI Publisher功能。如果仍有问题，请参考相关文档或联系技术支持。

## 下载链接

[关于BIPublisherDesktop在Word中无显示问题的解决方案分享](https://pan.quark.cn/s/039d895ea7c4)