---
layout: post
title: "Veritas NetBackup 101 Windows管理控制台管理指南"
date:   2024-09-10
tags: [控制台,安装,NetBackup,Windows,管理]
comments: true
author: admin
---
# Veritas NetBackup 10.1 Windows管理控制台管理指南

本文档提供了关于如何在Windows环境中安装和配置Veritas NetBackup 10.1的管理控制台的详细步骤。内容包括Java控制台的安装、汉化包的应用以及Web控制台的访问。

## 目录
1. [前言](#前言)
2. [Java管理控制台安装](#java管理控制台安装)
3. [控制台登录](#控制台登录)
4. [控制台安装中文包](#控制台安装中文包)
5. [Web控制台](#web控制台)

## 前言
本文是Veritas NetBackup 10.1安装系列中Windows管理控制台配置部分。本文包括控制台异地管理的安装、汉化包安装及Web控制台。仅提供安装步骤及思路，相关许可密钥请至官方正版购买颁发，严厉打击侵权行为。

## Java管理控制台安装
1. 下载链接: NetBackup_10.0.0.1_Win
2. 提取码：rfag
3. 下载完毕解压提取Addons文件夹到对应需要安装Java管理控制台的Windows服务器上。
4. 文件夹内为Java console控制台安装程序。
5. 运行SETUP安装JAVA控制台。
6. 接受授权，选择经典安装模式。
7. 确认安装细节后，自动执行安装程序等待安装完成。

## 控制台登录
1. 以异地控制台为例，master server本地控制台同理。
2. 打开NetBackup 10.0.0.1 Administration Console.exe控制台程序。
3. 填写hostname为master server服务器hostname。
4. 账号hostname\Administrator，密码为服务器用户密码。
5. 第二种登录为AD域登录，第三种基于单点登录、证书或智能卡的认证访问WEB控制台。

## 控制台安装中文包
1. 下载链接: NetBackup_10.0.0.1_ZH
2. 提取码：2q0o
3. 下载汉化包，运行browser汉化程序。
4. 选择netbackup汉化安装。
5. 默认下一步，自动执行安装程序。
6. 安装后再打开控制台程序，汉化完毕。

## Web控制台
1. 打开JAVA控制台可以找到web控制台网址，输入网址，打开web控制台（支持异地管理）。
2. 与JAVA控制台一样，输入hostname\administrator用户名，密码。
3. 登录进入web管理页面。

---

通过以上步骤，您可以在Windows环境中成功安装和配置Veritas NetBackup 10.1的管理控制台，并实现汉化和Web控制台的访问。

## 下载链接

[VeritasNetBackup10.1Windows管理控制台管理指南](https://pan.quark.cn/s/0265f4c0b754)