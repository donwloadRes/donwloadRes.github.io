---
layout: post
title: "Delphi7 Indy HTTPS 访问所需的 OpenSSL 版本"
date:   2024-09-29
tags: [dll,Indy,OpenSSL,版本,文件]
comments: true
author: admin
---
# Delphi7 Indy HTTPS 访问所需的 OpenSSL 版本

## 资源描述

本仓库提供 Delphi7 自带 Indy 组件访问 HTTPS 所需的 OpenSSL 对应版本，包含 `libeay32.dll` 和 `ssleay32.dll` 两个文件。经过实际测试，使用 `IdHttp1.get` 方法可以正常获取 HTTPS 内容。

## 使用方法

1. 将 `libeay32.dll` 和 `ssleay32.dll` 文件拷贝到您的可执行文件（exe）所在的目录下。
2. 在 Delphi 中，设置 `IdSSLIOHandlerSocket1` 属性面板中的 `SSLOption` 的 `Method` 为 `sslvSSLv23`。
3. 在代码中，只需进行以下设置：
   ```delphi
   IdHttp1.IOHandler := IdSSLIOHandlerSocket1;
   memo1.text := IdHttp1.get(furl);
   ```

## 注意事项

- 确保 `libeay32.dll` 和 `ssleay32.dll` 文件与您的可执行文件在同一目录下，以确保 Indy 组件能够正确加载 OpenSSL 库。
- 如果您在其他环境中使用这些文件，请确保它们与您的 Delphi 版本和 Indy 版本兼容。

## 贡献

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 许可证

本仓库中的文件遵循相应的开源许可证，具体请参考文件中的许可证信息。

## 下载链接

[Delphi7IndyHTTPS访问所需的OpenSSL版本](https://pan.quark.cn/s/55b33c22425e)