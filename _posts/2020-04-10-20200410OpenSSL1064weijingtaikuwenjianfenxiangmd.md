---
layout: post
title: "OpenSSL 10 64位静态库文件分享"
date:   2022-08-07
tags: [lib,OpenSSL,文件,1.0,64]
comments: true
author: admin
---
# OpenSSL 1.0 64位静态库文件分享

本仓库提供了一个资源文件的下载，具体为OpenSSL 1.0的64位lib静态库 `libeay64.lib` 和 `ssleay64.lib`。如果你在开发过程中需要使用这些库文件，可以直接从本仓库下载，无需再花费大量时间进行编译。

## 资源文件描述

- **文件名**: `libeay64.lib`, `ssleay64.lib`
- **版本**: OpenSSL 1.0
- **架构**: 64位

## 使用说明

如果你在项目中需要使用这些库文件，可以按照以下步骤进行配置：

1. 下载本仓库中的 `libeay64.lib` 和 `ssleay64.lib` 文件。
2. 在你的项目中包含以下头文件：
   ```c
   #include <openssl/ssl.h>
   #include <openssl/err.h>
   ```
3. 根据你的平台架构，添加相应的库文件链接：
   ```c
   #if defined _M_X64 || defined _AMD64_
   #pragma comment (lib, "libeay64.lib")
   #pragma comment (lib, "ssleay64.lib")
   #else
   #pragma comment (lib, "libeay32.lib")
   #pragma comment (lib, "ssleay32.lib")
   #endif
   ```

## 注意事项

- 本仓库提供的库文件为OpenSSL 1.0版本，适用于64位系统。
- 如果你使用的是32位系统或其他版本的OpenSSL，请自行编译或寻找相应的库文件。

## 贡献

如果你有其他版本的OpenSSL库文件或发现任何问题，欢迎提交Issue或Pull Request。

## 许可证

本仓库中的资源文件遵循OpenSSL的开源许可证。具体信息请参考OpenSSL的官方文档。

## 下载链接

[OpenSSL1.064位静态库文件分享](https://pan.quark.cn/s/1a04c111a90b)