---
layout: post
title: "CentOS 79 SSH 97p1 和 SSL 111w RPM 升级加固脚本"
date:   2020-09-06
tags: [OpenSSH,OpenSSL,升级,p1,1.1]
comments: true
author: admin
---
# CentOS 7.9 SSH 9.7p1 和 SSL 1.1.1w RPM 升级加固脚本

## 简介

本仓库提供了一个用于升级和加固 CentOS 7.9 系统中 OpenSSH 和 OpenSSL 的脚本。该脚本采用 RPM 包形式，能够一键快速升级版本，无需每台服务器单独进行编译。升级后，系统将同时拥有 OpenSSH 9.7p1 和 OpenSSL 1.1.1w 版本，并进行了默认的安全加固。

## 特点

1. **同时升级 OpenSSH 和 OpenSSL**：采用 RPM 包形式，一键快速升级版本，无需每台服务器单独进行编译。
2. **隐藏 OpenSSH 版本号**：升级后，OpenSSH 的版本号将被隐藏，增加安全性。
3. **保留关键命令**：升级过程中保留 `scp` 和 `ssh-copy-id` 命令，确保日常操作不受影响。
4. **默认安全加固**：脚本已包含默认的安全加固配置，已有配置将跳过。

## 安装步骤

1. **下载脚本**：从本仓库下载 `upgrade_ssl_ssh.sh` 脚本。
2. **执行安装**：在目标服务器上执行以下命令进行安装：
   ```bash
   bash upgrade_ssl_ssh.sh
   ```
3. **验证安装**：安装完成后，请新开终端进行验证测试。

## 验证版本

- **验证 OpenSSL 版本**：
  ```bash
  openssl version
  ```
  预期输出：
  ```
  OpenSSL 1.1.1w  11 Sep 2023
  ```

- **验证 OpenSSH 版本**：
  ```bash
  ssh -V
  ```
  预期输出：
  ```
  OpenSSH_9.7p1 OpenSSL 1.1.1w  11 Sep 2023
  ```

## 注意事项

- 升级安装后，请确保 `sshd` 服务正常运行，并新开终端进行验证测试。
- 若需获取最新版本或更多信息，请参考相关文章。

## 更新日志

- **2023-09-11**：初始版本发布，支持 OpenSSH 9.7p1 和 OpenSSL 1.1.1w 升级。

## 贡献

欢迎提交 Issue 或 Pull Request 来改进本脚本。

## 许可证

本项目采用 MIT 许可证，详情请参阅 [LICENSE](LICENSE) 文件。

## 下载链接

[CentOS7.9SSH9.7p1和SSL1.1.1wRPM升级加固脚本](https://pan.quark.cn/s/e94619c531d0)