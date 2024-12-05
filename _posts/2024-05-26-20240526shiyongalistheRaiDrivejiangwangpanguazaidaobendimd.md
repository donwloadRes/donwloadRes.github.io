---
layout: post
title: "使用alist和RaiDrive将网盘挂载到本地"
date:   2024-11-06
tags: [alist,网盘,本地,文件,挂载]
comments: true
author: admin
---
# 使用alist和RaiDrive将网盘挂载到本地

本文介绍了如何通过alist挂载百度网盘，并配置RaiDrive以实现webDav连接，同时提供自启动设置和缓存目录管理，以便于本地文件操作和多设备同步。

## 说明

本方案的意义在于记录经过实践检验的方案，同时分享操作中的细节和踩坑。本方案不一定完美，大家可以尝试其他的工具和解决方案。思路是通过alist挂载网盘，然后通过RaiDrive将网盘内容映射到本地。

本套方案只是将网盘的内容挂载到本地，可以进行一些常见的文件增删改查的操作，以及文件的查看，和使用本地播放器播放远程的视频内容。不可视为本地硬盘，因为查看网盘文件时会将数据缓存到本地，数据的加载速度取决于网络的质量，远没有本地磁盘的加载速度快。有助于多个设备异地访问网盘保持时时最新。

## 软件分享

- alist
- RaiDrive（windows x64版本）

## alist初始化

从官网或者分享的连接中获取对应的alist版本（本质就是一个exe文件），然后创建一个alist目录，将解压后的alist.exe文件放入其中。运行alist，在当前目录路径中的最前面输入cmd然后敲回车键进入终端，使用alist --help可以查看alist的相关命令。

## 挂载网盘（某度为例）

访问ip:5244或者自定义的访问端口，登录admin用户，打开管理界面（底部有管理）。打开存储的添加页面，选择百度网盘进行挂载配置。首先在浏览器登录百度网盘，然后打开官方百度网盘挂载说明文档，在刷新令牌部分点击连接，获取刷新令牌，然后再alist配置界面进行配置（请一定先登录网盘，然后点击连接获取刷新令牌）。

## alist自启动设置

在alist目录下创建alist_start.VBS文件，然后编辑文件内容如下：
```vbs
Set ws = CreateObject("Wscript.Shell")
ws.run "cmd /c alist.exe server", vbhide
```
有坑注意：如果设置脚本文件的默认打开方式，使用Microsoft Windows Based Script Host。如果使用记事本，重启之后直接打开脚本文件，而不是执行文件的内容。右键创建快捷方式，然后win+r输入shell:startup，将快捷方式放入到启动目录。

## RaiDrive配置

无脑双击安装，然后打开软件，点击添加配置webdav连接配置。

## 缓存目录设置

最终效果：可以使用本地的播放器播放视频资料，随意调节播放相关的设置，文件资料也可以在使用本地应用编辑。

## 下载链接

[使用alist和RaiDrive将网盘挂载到本地](https://pan.quark.cn/s/372934d7627b)