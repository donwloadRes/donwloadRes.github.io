---
layout: post
title: "PostgreSQL 11 在 Ubuntu 2204 离线安装包"
date:   2022-10-22
tags: [11,PostgreSQL,离线,安装,Ubuntu]
comments: true
author: admin
---
# PostgreSQL 11 在 Ubuntu 22.04 离线安装包

## 概览

本仓库提供 PostgreSQL 11 的 Ubuntu 22.04 专用离线安装包。以 deb 包的形式分发，便于在没有网络连接的环境中快速部署这款高性能的关系型数据库管理系统。通过简单的步骤，您可以在 Ubuntu 22.04 系统上实现 PostgreSQL 11 的一键安装。

## 特点

- **版本**：专为 PostgreSQL 11 设计。
- **系统兼容性**：确保与 Ubuntu 22.04 LTS（长期支持版）完美兼容。
- **安装便捷**：包含 `install.sh` 脚本，执行即可自动完成安装过程。
- **离线安装**：适合那些无法直接访问互联网的服务器或环境。

## 安装步骤

1. **下载资源**：首先从本仓库下载压缩包。
2. **上传至目标机器**：通过FTP、SSH或其他方式将下载好的离线安装包上传到您的Ubuntu 22.04服务器上。
3. **解压**：使用命令行工具，如终端，进入存放压缩包的目录并解压。例如：
   ```shell
   tar -zxvf postgresql-11_ubuntu22.04_offline.tar.gz
   ```
4. **执行安装脚本**：切换到解压后的目录，然后作为根用户运行 `install.sh` 脚本：
   ```shell
   sudo ./install.sh
   ```
5. **等待安装完成**：安装过程中会自动处理依赖项，并配置必要的服务。
6. **启动和验证**：安装成功后，您可以启动 PostgreSQL 并进行基本的配置检查。

```shell
sudo systemctl start postgresql@11-main
sudo systemctl status postgresql@11-main
```

## 注意事项

- 在执行安装之前，请确保您有足够的权限来安装系统级别的软件（通常需要 root 权限）。
- 若系统有其他版本的 PostgreSQL 运行，请先妥善处理，以免冲突。
- 安装完毕后，建议查阅官方文档进行进一步的配置和安全设置。

## 结语

此离线安装包旨在简化 PostgreSQL 11 在特定环境下部署的复杂度，帮助开发者和系统管理员高效工作。如有任何问题或反馈，欢迎贡献您的宝贵意见。

---

以上就是 PostgreSQL 11 在 Ubuntu 22.04 上离线安装的简要指南。祝您安装顺利！

## 下载链接

[PostgreSQL11在Ubuntu22.04离线安装包](https://pan.quark.cn/s/0b822d887bf3)