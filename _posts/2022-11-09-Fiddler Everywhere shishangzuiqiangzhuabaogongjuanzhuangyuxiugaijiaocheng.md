---
layout: post
title: "Fiddler Everywhere 史上最强抓包工具安装与修改教程"
date:   2022-04-09
tags: [Fiddler,Everywhere,安装,Users,XXX]
comments: true
author: admin
---
# Fiddler Everywhere 史上最强抓包工具安装与修改教程

## 简介
Fiddler Everywhere 是一款跨平台的 Web 调试代理工具，适用于 macOS、Windows 和 Linux。它能够记录计算机与互联网之间的所有 HTTP(S) 通信，支持检查、编辑通信内容，并具备 Mock 请求和修改响应返回的能力。相比传统的 Fiddler 版本，Fiddler Everywhere 功能更加丰富，界面也更加美观。

## 版本下载
由于最新的版本可能存在安装问题，本仓库提供了一个可安装的版本（Fiddler Everywhere 3.3.1）。请确保只使用此版本，其他版本概不负责。

## 安装步骤
1. 下载资源文件后，直接默认下一步进行安装。
2. 安装完成后，打开 Fiddler Everywhere。
3. 如果没有账号，请先注册。注册方式简单，按照提示操作即可。
4. 登录后，会看到付费提示，关闭 Fiddler Everywhere。

## 修改步骤
1. 替换以下目录中的两个 DLL 文件：
   - `C:\Users\XXX\AppData\Local\Programs\Fiddler Everywhere\resources\app\out\WebServer\FiddlerBackendSDK.dll`
   - `C:\Users\XXX\AppData\Local\Programs\Fiddler Everywhere\resources\app\out\WebServer\Fiddler.WebUi.dll`
2. 将 `main.3f983221e4e1aade.js` 复制到以下目录中，替换原文件：
   - `C:\Users\XXX\AppData\Local\Programs\Fiddler Everywhere\resources\app\out\WebServer\ClientApp\dist`
3. 将 `main.js` 复制到以下目录中，替换原文件：
   - `C:\Users\XXX\AppData\Local\Programs\Fiddler Everywhere\resources\app\out`

## 替换文件下载
本仓库提供了所需的替换文件，请下载并按照上述步骤进行操作。

## 注意事项
- 请确保只使用提供的版本进行安装和修改。
- 操作过程中请仔细阅读每一步的说明，避免误操作。

通过以上步骤，您可以成功安装并修改 Fiddler Everywhere，享受其强大的抓包和调试功能。

## 下载链接

[FiddlerEverywhere史上最强抓包工具安装与修改教程](https://pan.quark.cn/s/81c2edfb1035)