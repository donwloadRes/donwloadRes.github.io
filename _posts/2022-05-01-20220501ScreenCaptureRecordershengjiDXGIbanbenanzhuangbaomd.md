---
layout: post
title: "ScreenCaptureRecorder 升级 DXGI 版本安装包"
date:   2024-03-03
tags: [安装包,DXGI,screen,capture,Windows]
comments: true
author: admin
---
# Screen-Capture-Recorder 升级 DXGI 版本安装包

## 简介

本仓库提供了一个名为 **screen-capture-recorder 升级 DXGI 版本安装包** 的资源文件下载。该安装包旨在帮助用户轻松安装并注册 screen-capture-recorder.dll，使其支持高帧率（120帧）和低CPU占有率，适用于Windows 10系统。

## 资源描述

**screen-capture-recorder.dll** 是一款优秀的录屏 dshow filter，也被称为虚拟摄像头。它能够将桌面虚拟为一个 dshow 源 filter，打开这个虚拟摄像头就相当于捕获了桌面数据。然而，由于该工具最初是为 XP 系统设计的，其抓屏技术为 GDI，无法满足 Windows 10 下高帧率（DXGI）的需求。

为了解决这一问题，我们对源码进行了修改和升级，生成了 **screen-capture-dxgi.dll**。该升级版本支持高达 120 帧的高帧率，并且具备以下特性：

- **支持有无鼠标**：用户可以选择是否捕获鼠标。
- **捕获方式**：支持 GDI 或 DXGI 两种捕获方式。
- **颜色空间**：支持多种颜色空间输出，如 nv12、yv12、argb、yuv2 等。
- **图像翻转**：支持图像翻转功能。
- **完美解决鼠标问题**：新版本解决了鼠标捕获的问题。
- **支持不同分辨率和DPI**：能够适应不同分辨率和 DPI 的主屏幕和副屏幕。
- **增加 GDI 模式下的主副屏采集**：在 GDI 模式下也能采集主副屏幕。
- **支持 32 位和 64 位系统**：兼容 32 位和 64 位 Windows 系统。

## 安装说明

为了方便用户测试和使用，我们制作了一个安装包，用户只需下载并运行该安装包，即可自动完成注册过程，省去了手动注册的繁琐步骤。

## 注意事项

- 本安装包适用于 Windows 10 系统，建议在安装前备份重要数据。
- 安装过程中请确保系统权限足够，避免因权限问题导致安装失败。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过仓库的 Issues 页面进行反馈。我们非常乐意听取您的意见，并不断改进和优化该工具。

感谢您的使用！

## 下载链接

[Screen-Capture-Recorder升级DXGI版本安装包](https://pan.quark.cn/s/2b87d47cbbaf)