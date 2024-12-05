---
layout: post
title: "Mac 安装 PrettyZoo 指南"
date:   2021-02-02
tags: [PrettyZoo,Mac,macOS,安装,安全策略]
comments: true
author: admin
---
# Mac 安装 PrettyZoo 指南

## 概述
PrettyZoo 是一款免费开源的 Zookeeper 客户端工具，支持 Mac、Linux 和 Windows 平台。本指南主要介绍如何在 Mac 平台上安装 PrettyZoo，并解决安装过程中可能遇到的安全策略问题。

## 环境描述
- macOS 版本：macOS Ventura 13.2.1
- PrettyZoo 版本：2.1.1

## 下载
从 PrettyZoo 的官方 GitHub 发布页面下载适用于 Mac 系统的 `.dmg` 安装包。下载地址为：https://github.com/vran-dev/PrettyZoo/releases

## 安装
1. 下载完成后，双击安装包，将 PrettyZoo 拖动到 `/Applications` 文件夹中。
2. 在程序坞中找到安装的 PrettyZoo，单击打开。

## 解决安装受限问题
由于 macOS 的安全策略，可能会提示“文件已损坏，无法打开”。这是因为 PrettyZoo 没有加入 Apple 的平台签名。可以通过以下步骤解决：

1. 打开终端，执行以下命令以解除 macOS 的安全策略限制：
   ```bash
   sudo spctl --master-disable
   ```
2. 输入系统密码，再次执行上述命令。
3. 打开 Mac 的“设置” > “隐私与安全”，找到“安全性”选项，可以看到已自动勾选了“任何来源”选项。
4. 如果之前在程序坞中已经有了 PrettyZoo，需要先将其移除，然后继续执行以下命令：
   ```bash
   xattr -rc /Applications/prettyZoo.app
   ```
5. 在程序坞中再次打开 PrettyZoo，即可成功打开。

## 安装完成后
安装完成后，别忘了将 macOS 的安全策略重新开启：
```bash
sudo spctl --master-enable
```

## 总结
通过以上步骤，您可以在 Mac 上成功安装并使用 PrettyZoo 客户端工具。如果在安装过程中遇到任何问题，可以参考 PrettyZoo 的 GitHub 页面上的相关 issue 进行解决。

## 下载链接

[Mac安装PrettyZoo指南](https://pan.quark.cn/s/c510504252e4)