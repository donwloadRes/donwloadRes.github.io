---
layout: post
title: "Eclipse 添加 JDeclipse 反编译插件"
date:   2020-06-14
tags: [插件,Eclipse,反编译,JD,eclipse]
comments: true
author: admin
---
# Eclipse 添加 JD-eclipse 反编译插件

## 简介

本资源文件提供了在Eclipse中添加JD-eclipse反编译插件的详细步骤。通过安装该插件，用户可以在Eclipse中直接查看第三方或其他Jar文件的源代码，无需手动反编译。

## 安装步骤

### 1. 下载文件

首先，需要下载JD-eclipse反编译插件的相关文件。可以从官方网站或提供的网盘链接下载。

### 2. 安装插件

1. 打开Eclipse，进入菜单栏的 `Help` 选项。
2. 选择 `Install New Software`。
3. 点击 `Add` 按钮，添加下载的插件文件。
4. 等待安装进度条加载完成，安装过程中可能需要一些时间。

### 3. 查看安装是否成功

1. 安装完成后，进入 `Window` -> `Preferences`。
2. 在 `Java` 选项下找到 `Decompiler`。
3. 如果 `Decompiler` 选项存在，说明安装成功。

### 4. 关联文件

1. 在 `Preferences` 中，进入 `General` -> `Editors` -> `File Associations`。
2. 找到 `*.class` 和 `*.class without source` 文件类型。
3. 如果没有这些文件类型，点击 `Add` 按钮进行添加。
4. 选中 `Class File Editor`，点击 `Default`，然后点击 `OK`。

### 5. 删除插件

如果不再需要该插件，可以在 `Help` -> `About Eclipse` -> `Installation Details` 中找到并卸载。

## 注意事项

- 安装过程中可能会遇到运行缓慢的情况，请耐心等待。
- 安装完成后，部分功能可能需要重启Eclipse才能生效。

通过以上步骤，您可以在Eclipse中轻松添加并使用JD-eclipse反编译插件，方便地查看和分析Java类文件的源代码。

## 下载链接

[Eclipse添加JD-eclipse反编译插件](https://pan.quark.cn/s/37182f8c1970)