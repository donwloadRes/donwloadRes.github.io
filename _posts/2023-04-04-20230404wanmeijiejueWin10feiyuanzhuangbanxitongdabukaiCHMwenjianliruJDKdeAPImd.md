---
layout: post
title: "完美解决Win10非原装版系统打不开CHM文件（例如JDK的API）"
date:   2021-05-08
tags: [文件,CHM,Windows,hh,exe]
comments: true
author: admin
---
# 完美解决Win10非原装版系统打不开CHM文件（例如JDK的API）

## 简介

本资源文件旨在帮助用户解决在Windows 10非原装版系统中无法打开CHM文件的问题，特别是针对JDK的API文档。通过本资源文件，您可以轻松配置系统，使其能够正常打开CHM文件。

## 问题背景

在某些Windows 10系统中，尤其是非原装版或Ghost系统，用户可能会遇到无法打开CHM文件的情况。这通常是由于系统缺少必要的hh.exe文件及其相关组件导致的。

## 解决方案

### 1. 下载资源文件

本资源文件包含以下必要文件：
- hh.exe
- hhctrl.ocx
- itss.dll

### 2. 安装步骤

1. **解压资源文件**：将下载的压缩包解压到任意目录。
2. **复制文件**：
   - 将`hh.exe`文件放置在`C:\Windows`目录下。
   - 将`hhctrl.ocx`和`itss.dll`文件放置在`C:\Windows\System32`目录下。
   - 将`hh.exe`、`hhctrl.ocx`和`itss.dll`文件放置在`C:\Windows\SysWOW64`目录下。
3. **注册组件**：
   - 以管理员身份打开命令提示符（cmd）。
   - 输入以下命令并回车：
     ```
     regsvr32 hhctrl.ocx
     regsvr32 itss.dll
     ```
   - 如果命令执行成功，会显示注册成功的提示。
4. **关联CHM文件**：
   - 右击任意CHM文件，选择“打开方式” -> “选择其他应用” -> “更多应用” -> “在这台电脑上查找其他应用”。
   - 找到`C:\Windows\SysWOW64`目录下的`hh.exe`文件，点击打开。
5. **配置注册表**（可选）：
   - 如果仍然无法打开CHM文件，可以尝试以下操作：
   - 按`Win + R`打开运行，输入`regedit`进入注册表。
   - 依次进入：`HKEY-LOCAL-MACHINE` -> `SOFTWARE` -> `Classes` -> `chm.file` -> `shell` -> `open` -> `command`。
   - 将其值改为`"C:\Windows\SysWOW64\hh.exe" %1`。

## 注意事项

- 请确保以管理员身份执行所有命令。
- 如果系统中已有这些文件，请先备份原文件再进行替换。

通过以上步骤，您应该能够成功解决Windows 10非原装版系统无法打开CHM文件的问题。

## 下载链接

[完美解决Win10非原装版系统打不开CHM文件例如JDK的API分享](https://pan.quark.cn/s/674cb172bff4)