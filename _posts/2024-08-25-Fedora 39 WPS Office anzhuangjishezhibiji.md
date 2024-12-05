---
layout: post
title: "Fedora 39 WPS Office 安装及设置笔记"
date:   2020-12-16
tags: [WPS,安装,Office,bash,wps]
comments: true
author: admin
---
# Fedora 39 WPS Office 安装及设置笔记

本文详细介绍了在 Fedora 39 系统上安装 WPS Office 的步骤，包括下载 RPM 包、执行安装、处理字体问题以及切换到中文界面的操作。

## 1. WPS Office 下载

首先，从 WPS Office 的官方网站下载适用于 Linux 的 RPM 版本软件包。

## 2. 安装 WPS Office

使用以下命令安装下载的 RPM 包：

```bash
sudo dnf install wps-office-11.1.0.11708.XA-1.x86_64.rpm
```

等待安装完成即可。

## 3. 解决字体问题

安装完成后，可能会遇到字体缺失的问题。可以通过以下步骤解决：

1. 从 GitHub 下载 WPS 字体包：

```bash
git clone https://github.com/IamDH4/ttf-wps-fonts.git && cd ttf-wps-fonts
```

2. 安装字体：

```bash
sudo sh install.sh
```

## 4. 切换到中文界面

如果需要将 WPS Office 切换到中文界面，可以按照以下步骤操作：

1. 删除原有的字体文件：

```bash
cd /opt/kingsoft/wps-office/office6/mui
ls
```

2. 下载并解压中文界面文件（mui），然后将其复制到指定目录：

```bash
sudo cp -r mui /opt/kingsoft/wps-office/office6/
ls
```

确保只保留 `default` 和 `zh_CN` 文件夹。

通过以上步骤，您可以在 Fedora 39 系统上成功安装并配置 WPS Office，并解决可能遇到的字体问题。

## 下载链接

[Fedora39WPSOffice安装及设置笔记](https://pan.quark.cn/s/919e52a89078)