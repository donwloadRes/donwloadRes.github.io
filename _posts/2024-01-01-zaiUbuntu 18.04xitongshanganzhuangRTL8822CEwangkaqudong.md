---
layout: post
title: "在Ubuntu 18.04系统上安装RTL8822CE网卡驱动"
date:   2020-01-15
tags: [网卡,RTL8822CE,WiFi,rtl88x2ce,sudo]
comments: true
author: admin
---
# 在Ubuntu 18.04系统上安装RTL8822CE网卡驱动

## 简介
本资源文件提供了在Ubuntu 18.04系统上安装RTL8822CE网卡驱动的详细步骤和方法。通过本指南，您可以解决在安装或升级系统后无法连接WiFi的问题。

## 背景
在使用Ubuntu 18.04系统时，可能会遇到无法连接WiFi的问题，尤其是在系统升级后。这通常是由于WiFi驱动与系统不匹配导致的。本指南将帮助您正确安装RTL8822CE网卡驱动，以恢复WiFi功能。

## 安装步骤

### 1. 查看系统硬件信息
在终端中输入以下命令，查看计算机的有线网卡和无线网卡信息：
```bash
lspci
```

### 2. 下载驱动
下载RTL8822CE网卡驱动，并将其放置在合适的文件夹中。

### 3. 解压并手动更新
进入驱动文件夹，依次执行以下命令：
```bash
sudo cp rtl88x2ce-dkms/rtw88_blacklist.conf /etc/modprobe.d/rtw88_blacklist.conf
sudo mkdir /usr/src/rtl88x2ce-35403
sudo cp -Rv rtl88x2ce-dkms/* /usr/src/rtl88x2ce-35403/
sudo dkms add -m rtl88x2ce -v 35403
sudo dkms build -m rtl88x2ce -v 35403
sudo dkms install -m rtl88x2ce -v 35403
```

### 4. 重启系统
执行完上述步骤后，重启系统。进入网络管理界面，您应该可以看到无线网络选项，并可以正常连接WiFi。

## 后记
感谢GitHub上的开发者提供的Linux RTL8822CE网卡驱动，帮助解决了许多用户的WiFi连接问题。如果在BIOS升级后再次遇到WiFi无法连接的问题，请确保在BIOS设置中将Secure Boot设置为Disable。

## 补充说明
如果在安装过程中遇到任何问题，请参考原始文章中的详细步骤和说明，以确保正确安装驱动。

## 下载链接

[在Ubuntu18.04系统上安装RTL8822CE网卡驱动分享](https://pan.quark.cn/s/0f6acc9f1e87)

## 下载链接

[在Ubuntu18.04系统上安装RTL8822CE网卡驱动分享](https://pan.quark.cn/s/4a1fea68049a)