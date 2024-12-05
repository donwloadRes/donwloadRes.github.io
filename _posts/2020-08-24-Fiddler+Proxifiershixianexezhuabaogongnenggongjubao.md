---
layout: post
title: "Fiddler+Proxifier实现exe抓包功能工具包"
date:   2022-07-13
tags: [Proxifier,Fiddler,exe,抓取,抓包]
comments: true
author: admin
---
# Fiddler+Proxifier实现exe抓包功能工具包

## 简介
本资源文件提供了一个完整的工具包，用于实现通过Fiddler和Proxifier抓取exe程序的网络请求。通常情况下，Fiddler只能抓取浏览器发出的请求，但通过结合Proxifier，我们可以扩展其功能，使其能够同时抓取通过exe程序发出的网络请求。

## 内容概述
- **Fiddler**：一个强大的Web调试工具，广泛用于抓取和分析HTTP/HTTPS流量。
- **Proxifier**：一个代理工具，允许所有网络流量通过指定的代理服务器，从而实现对非浏览器应用的抓包。
- **配置使用说明**：详细的配置步骤和使用指南，帮助用户快速上手并实现exe程序的抓包功能。

## 使用说明
1. **安装Fiddler**：首先安装并配置Fiddler，确保其能够正常抓取浏览器请求。
2. **安装Proxifier**：下载并安装Proxifier，并根据配置说明进行设置。
3. **配置Proxifier**：将Proxifier配置为通过Fiddler代理所有网络流量。
4. **启动抓包**：启动需要抓包的exe程序，Fiddler将能够捕获该程序的所有网络请求。

## 注意事项
- 请确保Fiddler和Proxifier的版本兼容。
- 配置过程中可能需要管理员权限。
- 使用完毕后，建议恢复Proxifier的默认设置，以免影响其他网络应用的正常使用。

## 适用场景
- 开发人员在调试网络应用时，需要抓取exe程序的网络请求。
- 安全研究人员在分析恶意软件或网络攻击时，需要捕获非浏览器应用的网络流量。

通过本工具包，您可以轻松实现对exe程序的网络请求抓包，提升开发和安全分析的效率。

## 下载链接

[FiddlerProxifier实现exe抓包功能工具包](https://pan.quark.cn/s/90ae45bb3b96)