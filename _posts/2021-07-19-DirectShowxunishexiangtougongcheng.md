---
layout: post
title: "DirectShow虚拟摄像头工程"
date:   2020-09-23
tags: [DirectShow,摄像头,虚拟,工程,bin]
comments: true
author: admin
---
# DirectShow虚拟摄像头工程

## 项目描述

这是一个基于DirectShow的虚拟摄像头驱动源代码工程。该工程采用从零开发的方式，实现了COM基础组件和IBaseFilter、IPin等接口功能。与传统的DirectShow开发不同，本工程不依赖于DSHOW的SDK库即可编译运行。代码工程使用VS2015进行编译。

如果你对DirectShow的工作原理不感兴趣，或者不想深入了解其内部机制，那么这个工程可能并不适合你。你可以选择不下载这份代码，以免给你带来不必要的困扰。

## 目录结构

- **source**: 工程源代码目录。
- **bin**: 已经编译好的dll文件。

## 使用方法

1. **注册虚拟摄像头**: 在bin目录下，运行`register.bat`文件进行注册。
2. **注销虚拟摄像头**: 在bin目录下，运行`unregister.bat`文件进行注销。

注册成功后，使用DirectShow框架的程序（如QQ、amcap等）就可以发现并访问这个虚拟摄像头。

## 详细原理介绍

关于本工程的详细原理介绍，请参考相关技术博客文章。

## 作者

Fanxiushu 2018

---

希望这份README能够帮助你更好地理解和使用这个DirectShow虚拟摄像头工程。

## 下载链接

[DirectShow虚拟摄像头工程](https://pan.quark.cn/s/5d9db8907667)