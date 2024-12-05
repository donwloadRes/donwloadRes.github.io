---
layout: post
title: "Charles安装与简单使用指南"
date:   2020-09-12
tags: [Charles,网络,请求,安装,截取]
comments: true
author: admin
---
# Charles安装与简单使用指南

## 简介
Charles是一款在Mac/PC下常用的网络封包截取工具，广泛应用于移动开发中，用于调试与服务器端的网络通讯协议。通过将Charles设置成系统的网络访问代理服务器，所有的网络访问请求都会通过它来完成，从而实现了网络封包的截取和分析。

## 主要功能
- **截取HTTP和HTTPS网络封包**：Charles能够截取并分析HTTP和HTTPS协议的网络请求。
- **重发网络请求**：方便后端调试，支持重复发送网络请求。
- **修改网络请求参数**：支持动态修改网络请求的参数。
- **模拟慢速网络**：支持模拟慢速网络环境，帮助测试应用在不同网络条件下的表现。

## 安装步骤
1. **下载Charles**：从Charles官网下载最新版本的安装包。
2. **安装Charles**：双击安装包，按照提示完成安装。
3. **破解Charles**：下载破解工具，将破解文件复制到Charles安装目录下的`/jre/lib`目录中，覆盖原有的`charles.jar`文件。
4. **验证破解**：打开Charles，点击`Help` -> `About Charles`，确认显示“Registered to: 破解 By 小宇殿下”字样。

## 简单使用
1. **设置系统代理**：打开Charles，点击`Proxy` -> `Windows Proxy`，将Charles设置为系统代理。
2. **手机连接代理**：在手机上设置代理服务器为主机IP地址，端口号为8888。
3. **开始抓包**：手机开始请求网络，Charles会弹出确认框，点击同意开始抓包。

## 查看封包
Charles提供两种视图：
- **Structure视图**：按访问的域名分类显示网络请求。
- **Sequence视图**：按访问的时间排序显示网络请求。

## 截取HTTPS通讯信息
1. **安装证书**：在电脑上安装Charles的CA证书，点击`Help` -> `SSL Proxy` -> `Install Charles Root Certificate`。
2. **手机安装证书**：在手机浏览器中访问`http://chls.pro/ssl`，安装证书。
3. **启用SSL代理**：在要截取的网络请求上右击，选择`SSL proxy`菜单项。

## 总结
通过以上步骤，您可以成功安装并使用Charles进行网络封包的截取和分析。Charles不仅适用于移动开发中的调试，还可以用于分析第三方应用的通讯协议。

## 下载链接

[Charles安装与简单使用指南分享](https://pan.quark.cn/s/d0ef23aac9aa)