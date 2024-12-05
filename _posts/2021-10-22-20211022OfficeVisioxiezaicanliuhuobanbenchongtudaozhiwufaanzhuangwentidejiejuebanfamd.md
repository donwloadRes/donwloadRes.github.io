---
layout: post
title: "OfficeVisio卸载残留或版本冲突导致无法安装问题的解决办法"
date:   2021-12-20
tags: [Office,Visio,版本,安装,卸载]
comments: true
author: admin
---
# Office/Visio卸载残留或版本冲突导致无法安装问题的解决办法

## 简介
本资源文件旨在帮助用户解决在卸载旧版本Office或Visio后，由于卸载残留或版本冲突导致无法安装新版本的问题。通过本文提供的解决方案，用户可以彻底清理旧版本的残留文件和注册表项，确保新版本的顺利安装。

## 常见问题
1. **网络连接问题或硬盘空间不足**：在确认网络无问题、硬盘空间足够的情况下，安装程序仍然提示网络连接问题或硬盘空间不足。
2. **32/64位版本冲突**：旧版本的Office与新版本的Office位数不一致，导致安装冲突。
3. **Office/Visio冲突**：Office 2016/2019的安装技术是即点即用（click-to-run），而Visio 2016的安装技术是windows installer，两者在先后安装时会提示冲突。

## 解决办法
### 利用软件完全卸载旧版本
推荐使用微软官方推荐的Office卸载工具，如SetupProd_OffScrub.exe或o15-ctrremove.diagcab，彻底卸载旧版本Office或Visio。

### 手动修改注册表
1. **32/64位版本冲突**：
   - 打开注册表编辑器（regedit）。
   - 定位到HKEY_CLASSES_ROOT\Installer\Products。
   - 删除以“00006”开头的注册表键值。

2. **Office/Visio冲突**：
   - 打开注册表编辑器（regedit）。
   - 定位到HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall\Office16\VISPRO。
   - 删除Office16\VISPRO相关的注册表值。

### 通过微软官方Office Deployment Tool解决问题
1. 下载并解压Office Deployment Tool。
2. 修改配置文件，指定安装路径和版本。
3. 运行命令行，执行安装命令。

## 总结
通过上述方法，用户可以有效解决Office或Visio卸载残留或版本冲突导致的安装问题，确保新版本的顺利安装。

## 下载链接

[OfficeVisio卸载残留或版本冲突导致无法安装问题的解决办法分享](https://pan.quark.cn/s/c2df928346c2)