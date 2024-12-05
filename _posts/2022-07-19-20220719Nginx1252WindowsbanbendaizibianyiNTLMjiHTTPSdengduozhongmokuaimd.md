---
layout: post
title: "Nginx 1252 Windows版本带自编译NTLM及HTTPS等多种模块"
date:   2023-03-11
tags: [Nginx,版本,模块,1.25,Windows]
comments: true
author: admin
---
# Nginx 1.25.2 Windows版本，带自编译NTLM及HTTPS等多种模块

本仓库提供了一个基于最新版本Nginx 1.25.2的Windows版本，该版本经过本人亲手使用MSMY2编译，并集成了多种实用模块，包括但不限于NTLM、HTTPS、流代理等。此版本已在生产环境中经过长期使用，稳定可靠。

## 资源文件描述

- **Nginx版本**: 1.25.2
- **操作系统**: Windows
- **编译工具**: MSMY2
- **集成模块**:
  - `nginx-http-flv-module-master`
  - `nginx-ntlm-module-master`
  - `ngx_http_proxy_connect_module-master`
- **功能特性**:
  - 支持域登陆代理
  - 支持HTTPS代理
  - 支持流代理

## 使用说明

1. **下载资源**: 从本仓库下载Nginx 1.25.2 Windows版本及相关配置文件。
2. **配置文件**: 下载的资源中包含了一些参考配置文件（`conf`目录下），您可以根据实际需求修改对应的IP和端口。
3. **启动Nginx**: 解压下载的文件，进入Nginx目录，运行`nginx.exe`即可启动Nginx服务。

## 注意事项

- 如果您需要集成其他模块，可以私信我，我将根据您的需求进行编译并提供相应的版本。
- 本版本已在生产环境中经过测试，但仍建议您在部署前进行充分的测试，以确保其符合您的业务需求。

## 联系我

如果您在使用过程中遇到任何问题，或有其他模块需求，欢迎通过私信联系我，我将尽力为您提供帮助。

## 下载链接

[Nginx1.25.2Windows版本带自编译NTLM及HTTPS等多种模块](https://pan.quark.cn/s/352e99135cda)