---
layout: post
title: "WPS VBA 支持库及插件问题解决方案"
date:   2022-01-24
tags: [WPS,VBA,插件,安装,Axmath]
comments: true
author: admin
---
# WPS VBA 支持库及插件问题解决方案

本仓库提供了解决 WPS 中常见问题的资源文件，包括未安装 VBA 支持库、Axmath 或 AxGraph 无反应、不显示 AxMath 插件、Zotero 插件无法使用以及 WPS 登录功能限制等问题。

## 问题列表

1. **WPS：未安装 VBA 支持库，无法运行文档中的宏**
   - 解决步骤：
     1. 下载 VBA 支持库。
     2. 关闭所有正在运行的 WPS，再安装 VBA 支持库。

2. **WPS 中点击 Axmath 或 AxGraph 无反应**
   - 解决步骤：
     1. 确认安装 AxMath 时，安装的组件【MS-Office Addins】已勾选。
     2. 关闭所有正在运行的 WPS，拷贝 Axmath.dotm 到指定目录。
     3. 运行 WPS，检查【加载项】中是否已加载，没有就【添加】。

3. **WPS 中不显示 AxMath 插件**
   - 解决步骤：
     1. 确认安装 AxMath 时，安装的组件【MS-Office Addins】已勾选。
     2. 关闭所有正在运行的 WPS，拷贝 Axmath.dotm 到指定目录。
     3. 运行 WPS，检查【加载项】中是否已加载，没有就【添加】。

4. **WPS 中 Zotero 插件无法使用**
   - 原因：
     1. 缺少 Python3 环境支持。
     2. 缺少 VBA 支持库。
     3. WPS 中新旧版本 Zotero 扩展冲突。
   - 解决方法：
     1. 下载并安装 Python3。
     2. 安装 VBA 支持库。
     3. 卸载 WPS 中旧版 Zotero 扩展。

5. **WPS 登录功能限制**
   - 解除方法：
     1. 修改注册表或使用小程序。

## 使用说明

1. 下载本仓库中的资源文件。
2. 根据具体问题，按照上述解决步骤进行操作。
3. 重启 WPS，检查问题是否解决。

## 注意事项

- 在安装或修改任何文件之前，请确保已备份重要数据。
- 如果遇到问题，请参考相关文档或联系技术支持。

希望本仓库的资源能够帮助您解决 WPS 中的常见问题。

## 下载链接

[WPSVBA支持库及插件问题解决方案](https://pan.quark.cn/s/3d7da1d1006e)