---
layout: post
title: "CentOS 7.x OpenSSH 与 OpenSSL 1.1.x 自定义版本 RPM 包构建脚本"
date:   2021-01-29
tags: [OpenSSH,版本,OpenSSL,RPM,脚本]
comments: true
author: admin
---
# CentOS 7.x OpenSSH 与 OpenSSL 1.1.x 自定义版本 RPM 包构建脚本

## 资源描述

本仓库提供了一个用于在 CentOS 7.x 系统上构建自定义版本的 OpenSSH 和 OpenSSL 1.1.x 的 RPM 包的脚本。该脚本具有以下特点：

1. **同时升级 OpenSSH 与 OpenSSL**：采用 RPM 包形式，一键快速升级版本，无需每台服务器单独进行编译。
2. **隐藏 OpenSSH 版本号**：对于 OpenSSH 9.8p1 之前的版本，可以隐藏版本号。（OpenSSH 9.8p1 及之后的版本暂时无法隐藏版本号）
3. **保留关键命令**：升级过程中保留 `scp` 和 `ssh-copy-id` 命令，确保日常操作不受影响。

## 注意事项

- CentOS 7.x 默认使用的 OpenSSL 版本为 1.1.1x，但该版本已经停止维护。建议使用 OpenSSL 3.0.x 或更高版本的 TLS 长期支持版本来构建 RPM 包。
- 本脚本适用于需要快速升级 OpenSSH 和 OpenSSL 版本，并且希望以 RPM 包形式进行部署的场景。

## 使用方法

1. 下载本仓库中的脚本文件。
2. 根据脚本中的说明，配置所需的 OpenSSH 和 OpenSSL 版本。
3. 运行脚本，自动构建 RPM 包。
4. 将生成的 RPM 包分发到目标服务器，并进行安装。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。我们非常乐意与您一起完善这个脚本。

---

希望这个脚本能帮助您快速、安全地升级您的 OpenSSH 和 OpenSSL 版本！

## 下载链接

[CentOS7.xOpenSSH与OpenSSL1.1.x自定义版本RPM包构建脚本](https://pan.quark.cn/s/d2939558b0c5)