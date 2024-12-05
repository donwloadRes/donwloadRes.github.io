---
layout: post
title: "OpenSSH 74p1 升级到 OpenSSH 96p1 离线包"
date:   2020-11-07
tags: [rpm,el7,x86,64,4.8]
comments: true
author: admin
---
# OpenSSH 7.4p1 升级到 OpenSSH 9.6p1 离线包

## 简介

本仓库提供了一个用于将 OpenSSH 7.4p1 升级到 OpenSSH 9.6p1 所需的离线包资源。该资源文件包含了升级过程中所需的命令包和依赖库，适用于无法连接互联网的环境。

## 资源内容

### 主要包含以下内容：

1. **命令包**：
   - gcc
   - openssl-devel
   - pam-devel
   - rpm-build
   - zlib

2. **离线包**：
   - openssh-9.6p1.tar.gz
   - openssl-1.1.1t.tar.gz

### 各个版本的详细信息：

- **gcc**：4.8.5
- **openssl**：1.1.1
- **pam**：1.1.8
- **zlib**：1.2.7

## 文件列表

```
openssh-update/
├── boost-serialization-1.53.0-28.el7.x86_64.rpm
├── boost-system-1.53.0-28.el7.x86_64.rpm
├── boost-thread-1.53.0-28.el7.x86_64.rpm
├── cpp-4.8.5-44.el7.x86_64.rpm
├── gcc-4.8.5-44.el7.x86_64.rpm
├── gcc-c++-4.8.5-44.el7.x86_64.rpm
├── gcc-gfortran-4.8.5-44.el7.x86_64.rpm
├── gcc-gnat-4.8.5-44.el7.x86_64.rpm
├── gcc-objc-4.8.5-44.el7.x86_64.rpm
├── gcc-objc++-4.8.5-44.el7.x86_64.rpm
├── glibc-2.17-326.el7_9.x86_64.rpm
├── glibc-common-2.17-326.el7_9.x86_64.rpm
├── glibc-devel-2.17-326.el7_9.x86_64.rpm
├── glibc-headers-2.17-326.el7_9.x86_64.rpm
├── glibc-static-2.17-326.el7_9.x86_64.rpm
├── glibc-utils-2.17-326.el7_9.x86_64.rpm
├── kernel-headers-3.10.0-1160.el7.x86_64.rpm
├── libgcc-4.8.5-44.el7.x86_64.rpm
├── libstdc++-4.8.5-44.el7.x86_64.rpm
├── libstdc++-devel-4.8.5-44.el7.x86_64.rpm
├── libtool-ltdl-2.4.2-22.el7_3.x86_64.rpm
├── mpfr-3.1.1-4.el7.x86_64.rpm
├── openssh-9.6p1.tar.gz
├── openssl-1.1.1t.tar.gz
├── pcre-8.32-17.el7.x86_64.rpm
├── zlib-1.2.7-18.el7.x86_64.rpm
└── zlib-devel-1.2.7-18.el7.x86_64.rpm
```

## 使用说明

1. **下载资源**：
   将本仓库中的所有文件下载到本地。

2. **安装依赖**：
   在目标服务器上，使用 `rpm` 命令安装所需的依赖包。例如：
   ```bash
   rpm -ivh gcc-4.8.5-44.el7.x86_64.rpm
   ```

3. **解压并编译 OpenSSH**：
   解压 `openssh-9.6p1.tar.gz` 和 `openssl-1.1.1t.tar.gz`，并按照官方文档进行编译和安装。

4. **配置与启动**：
   完成编译后，配置 OpenSSH 并启动服务。

## 注意事项

- 请确保在升级前备份现有配置文件和数据。
- 升级过程中可能会遇到依赖冲突或其他问题，建议在测试环境中先行测试。

## 联系我们

如有任何问题或建议，请通过以下方式联系我们：
- 邮箱：support@example.com
- 电话：+86 123-4567-8901

---

**感谢使用本资源，祝您升级顺利！**

## 下载链接

[OpenSSH7.4p1升级到OpenSSH9.6p1离线包](https://pan.quark.cn/s/993b0fff50e8)