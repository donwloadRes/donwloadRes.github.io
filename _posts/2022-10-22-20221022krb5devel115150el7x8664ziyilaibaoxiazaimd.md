---
layout: post
title: "krb5-devel-1.15.1-50.el7.x86_64 子依赖包下载"
date:   2021-02-05
tags: [devel,x86,64,rpm,el7]
comments: true
author: admin
---
# krb5-devel-1.15.1-50.el7.x86_64 子依赖包下载

本仓库提供了在安装 `krb5-devel-1.15.1-50.el7.x86_64` 时可能缺失的子依赖包。这些依赖包是确保 `krb5-devel` 能够正常安装和运行的关键组件。以下是具体的依赖包列表：

1. **keyutils-libs-devel-1.5.8-3.el7.x86_64.rpm**
2. **libcom_err-devel-1.42.9-19.el7.x86_64.rpm**
3. **libkadm5-1.15.1-50.el7.x86_64.rpm**
4. **libselinux-devel-2.5-15.el7.x86_64.rpm**
5. **libverto-devel-0.2.5-4.el7.x86_64.rpm**

## 使用说明

1. **下载依赖包**：
   您可以直接从本仓库下载上述列出的所有依赖包。

2. **安装依赖包**：
   下载完成后，使用以下命令安装这些依赖包：
   ```bash
   sudo rpm -ivh keyutils-libs-devel-1.5.8-3.el7.x86_64.rpm
   sudo rpm -ivh libcom_err-devel-1.42.9-19.el7.x86_64.rpm
   sudo rpm -ivh libkadm5-1.15.1-50.el7.x86_64.rpm
   sudo rpm -ivh libselinux-devel-2.5-15.el7.x86_64.rpm
   sudo rpm -ivh libverto-devel-0.2.5-4.el7.x86_64.rpm
   ```

3. **安装 krb5-devel**：
   在安装完所有依赖包后，您可以继续安装 `krb5-devel-1.15.1-50.el7.x86_64`。

## 注意事项

- 请确保您下载的依赖包与您的操作系统版本和架构（x86_64）相匹配。
- 如果在安装过程中遇到其他依赖问题，请参考相关文档或联系技术支持。

希望这些依赖包能够帮助您顺利完成 `krb5-devel` 的安装。如果有任何问题，欢迎在仓库中提出。

## 下载链接

[krb5-devel-1.15.1-50.el7.x86_64子依赖包下载](https://pan.quark.cn/s/ee8c8ae77e27)