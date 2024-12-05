---
layout: post
title: "Delphi XE10 实现带 SSL 的 idHttp 发送 HTTPS POST 请求示例"
date:   2021-10-13
tags: [示例,Delphi,idHttp,dll,HTTPS]
comments: true
author: admin
---
# Delphi XE10 实现带 SSL 的 idHttp 发送 HTTPS POST 请求示例

本资源文件提供了一个在 Delphi XE10 环境下，使用 `idHttp` 组件通过 HTTPS 协议发送 JSON 数据的示例程序。该示例程序解决了在 HTTPS 环境下使用 `idHttp` 进行 POST 请求时可能遇到的常见问题。

## 描述

在现代 Web 开发中，使用 `idHttp` 组件发送 JSON 数据到某个 URL 已经非常普遍。然而，当目标 URL 是 HTTPS 时，直接使用 `idHttp` 进行 POST 请求可能会遇到错误或无法成功发送数据的情况。这是因为 HTTPS 协议需要 SSL/TLS 加密支持，而 `idHttp` 默认情况下并不具备这一功能。

为了解决这个问题，本示例程序使用了 `IdSSLIOHandlerSocketOpenSSL` 控件，并依赖于两个关键的 DLL 文件：`libeay32.dll` 和 `ssleay32.dll`。这两个 DLL 文件需要放置在程序的执行目录下，或者放置在系统的 `system32` 目录（对于 64 位程序，则放置在 `systemWOW64` 目录）。

需要注意的是，Delphi XE 和 Delphi 2007 及以下版本使用的 `libeay32.dll` 和 `ssleay32.dll` 文件虽然名称相同，但内容是不同的。本示例程序是基于 Delphi XE10 开发的，因此适用于 XE 及以上版本。

## 使用说明

1. **下载资源文件**：下载本仓库中的示例程序及相关 DLL 文件。
2. **放置 DLL 文件**：将 `libeay32.dll` 和 `ssleay32.dll` 文件放置在程序的执行目录下，或者放置在系统的 `system32` 或 `systemWOW64` 目录中。
3. **运行示例程序**：打开 Delphi XE10，加载并运行示例程序。程序将演示如何使用 `idHttp` 组件通过 HTTPS 协议发送 JSON 数据。

## 注意事项

- 确保使用的 `libeay32.dll` 和 `ssleay32.dll` 文件与 Delphi 版本匹配。
- 如果程序运行在 64 位系统上，请确保将 DLL 文件放置在 `systemWOW64` 目录中。
- 本示例程序适用于 Delphi XE 及以上版本，低版本 Delphi 可能需要使用不同的 DLL 文件。

通过本示例程序，您可以轻松地在 Delphi XE10 中实现带 SSL 的 HTTPS POST 请求，解决常见的网络通信问题。

## 下载链接

[DelphiXE10实现带SSL的idHttp发送HTTPSPOST请求示例](https://pan.quark.cn/s/4ccbad1d6527)