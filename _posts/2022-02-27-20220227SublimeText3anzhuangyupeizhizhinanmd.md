---
layout: post
title: "Sublime Text 3 安装与配置指南"
date:   2024-09-29
tags: [安装,Sublime,Text,Package,Control]
comments: true
author: admin
---
# Sublime Text 3 安装与配置指南

本仓库提供了一个详细的指南，帮助用户在Windows 10（64位）操作系统下安装和配置Sublime Text 3。内容包括软件的下载、安装、Package Control的手动安装及配置，以及插件的安装（以汉化包ChineseLocalizations为例）。

## 目录

1. [下载Sublime Text 3](#下载sublime-text-3)
2. [安装Sublime Text 3](#安装sublime-text-3)
3. [手动安装Package Control](#手动安装package-control)
4. [更改配置](#更改配置)
5. [安装插件（以汉化包ChineseLocalizations为例）](#安装插件)

## 下载Sublime Text 3

- 官方网站：[Sublime Text 3](http://www.sublimetext.com/3)
- 官方网站中文版：[Sublime Text 3 中文版](http://www.sublimetext.cn/3)

## 安装Sublime Text 3

双击Setup.exe安装包，根据提示进行安装。若勾选“Add to explorer context menu”，Sublime Text可以被添加到右键打开方式中，在右键单击文件时，可以选择使用Sublime Text打开。

## 手动安装Package Control

1. 访问[Package Control 安装页面](https://packagecontrol.io/installation)，点击界面中用红框标识的部分进行下载。
2. 点击软件中菜单栏Preferences > Browse Packages。
3. 在打开的面板中返回上一级目录，双击文件夹Installed Packages，将下载好的Package Control.sublime-package复制至其下。
4. 重启Sublime Text，菜单栏Preferences最下方显示Package Settings和Package Control两项，说明已成功安装。

## 更改配置

如果安装Package Control时报错，可能是因为网址被墙。解决方案是将软件需要使用的channel_v3.json文件保存至本地，并在软件中进行配置。

## 安装插件（以汉化包ChineseLocalizations为例）

在Package Control中输入插件名称，按下回车进行安装。这里以安装语言包为例，输入ChineseLocalizations并回车，在软件左下方会显示安装过程相关信息。待安装结束后，重启软件，菜单栏Help > Language > 简体中文，即可切换至中文界面。

---

通过本指南，您可以顺利完成Sublime Text 3的安装与配置，并根据需要安装其他插件。希望本指南能为您带来帮助。

## 下载链接

[SublimeText3安装与配置指南](https://pan.quark.cn/s/d77b95b09603)