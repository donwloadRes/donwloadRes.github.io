---
layout: post
title: "Windows 系统添加 VirtIO 驱动指南"
date:   2022-12-03
tags: [Windows,ISO,镜像,驱动,VirtIO]
comments: true
author: admin
---
# Windows 系统添加 VirtIO 驱动指南

本资源文件提供了在Windows ISO安装镜像中添加VirtIO驱动的详细步骤。通过集成VirtIO驱动，可以解决在KVM虚拟化环境中安装Windows时找不到硬盘的问题。

## 背景介绍

在KVM虚拟化环境中，Windows自带的驱动可能不支持KVM的硬盘控制器，导致在安装过程中无法识别硬盘。为了解决这一问题，可以将VirtIO驱动集成到Windows的ISO安装镜像中，从而在安装过程中自动加载驱动。

## 主要步骤

1. **准备工作**
   - 下载Windows原版ISO镜像
   - 获取UltraISO软件
   - 下载Windows AIK工具包
   - 获取VirtIO驱动

2. **安装WAIK工具包**
   - 验证系统是否已自带工具包
   - 使用UltraISO挂载WAIK的ISO镜像
   - 运行WAIKAMD64安装工具包

3. **准备WIM映像文件**
   - 使用UltraISO挂载Windows ISO镜像
   - 复制或提取boot.wim和install.wim文件

4. **添加驱动**
   - 创建文件夹用于挂载WIM映像
   - 使用UltraISO挂载VirtIO驱动ISO镜像
   - 以管理员身份运行cmd或PowerShell
   - 使用Dism工具挂载WIM映像并添加驱动
   - 查看驱动情况并保存WIM映像

5. **封装新的ISO镜像**
   - 使用UltraISO打开原Windows ISO安装盘镜像
   - 替换sources文件夹下的boot.wim和install.wim
   - 保存为新的ISO镜像

## 注意事项

- 确保所有操作在管理员权限下进行。
- 驱动添加过程中，注意驱动的路径和版本匹配。
- 在封装新的ISO镜像时，确保不丢失ISO的引导数据。

通过以上步骤，您可以成功在Windows ISO安装镜像中集成VirtIO驱动，从而在KVM虚拟化环境中顺利安装Windows系统。

## 下载链接

[Windows系统添加VirtIO驱动指南分享](https://pan.quark.cn/s/10d701033a1a)