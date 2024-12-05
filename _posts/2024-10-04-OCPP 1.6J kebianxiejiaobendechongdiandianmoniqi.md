---
layout: post
title: "OCPP 1.6J 可编写脚本的充电点模拟器"
date:   2021-08-13
tags: [OCPP,1.6,模拟器,支持,JavaScript]
comments: true
author: admin
---
# OCPP 1.6J 可编写脚本的充电点模拟器

## 介绍

`scriptable-ocpp-chargepoint-simulator` 是一个用于 OCPP 1.6J 的可编写脚本的充电点模拟器。该模拟器支持多种功能，包括带有 JSON 的 OCPP 1.6（和安全性）、带有 HTML 前端的 REST API、基于文件的批处理模式、完全可以用 JavaScript 编写脚本、FTP 和 CSR 操作、ws:// 和 wss://（带有客户端证书）等。

## 主要功能

- **OCPP 1.6 支持**：支持 OCPP 1.6 协议，并带有安全性支持。
- **REST API**：提供带有 HTML 前端的 REST API，方便用户进行操作和监控。
- **批处理模式**：支持基于文件的批处理模式，方便进行大规模操作。
- **JavaScript 脚本**：完全可以用 JavaScript 编写脚本，灵活性高。
- **FTP 和 CSR 操作**：支持 FTP 和 CSR 操作，方便进行文件传输和证书管理。
- **WebSocket 支持**：支持 ws:// 和 wss:// 协议，并带有客户端证书支持。

## 主要开发注意事项

该工具的设计初衷是为了帮助用户学习和理解 OCPP 协议，因此它不会隐藏任何细节，而是使这些细节更易于掌握。该模拟器是一个全基于的项目，具有服务器端支持的基于的服务器和基于 HTML 客户端，具有超级简单的无转换器设置。

## 待办事项

- OCPP 代码也应在浏览器中运行。

## 许可证

该软件已获得开源许可证。请参阅相关文件以获取更多信息。

## 安装和构建

确保已安装 npm。批量操作将使用 JavaScript 的逻辑放入文件（例如 `custom.js`）。您的文件需要使用一个参数导出异步功能。此参数将传递 `connect(url: string): Chargepoi`。

## 下载链接

[OCPP1.6J可编写脚本的充电点模拟器](https://pan.quark.cn/s/c0ae996ec2ae)