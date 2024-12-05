---
layout: post
title: "CentOS 7 安装 Oracle 11R2 最全依赖包"
date:   2024-05-15
tags: [安装,devel,依赖,RPM,CentOS]
comments: true
author: admin
---
# CentOS 7 安装 Oracle 11R2 最全依赖包

## 资源描述

本仓库提供了一个资源文件，包含了在 CentOS 7 上安装 Oracle 11R2 所需的最全依赖包。这些依赖包可以帮助解决在安装过程中可能遇到的各种依赖问题，特别是以下错误：

```
Exception in thread "main" java.lang.UnsatisfiedLinkError: /app/oracle/product/11.2.0/jdk/jre/lib/amd64/xawt/libmawt.so: libXext.so.6: cannot open shared object file: No such file or directory
```

## 包含的依赖包

以下是资源文件中包含的依赖包列表：

- binutils
- compat-libstdc++
- elfutils-libelf-devel
- gcc-c++
- glibc
- glibc-devel
- ksh
- libaio
- libaio-devel
- libgcc
- libstdc++
- libX11
- libX11-common
- libXau
- libxcb
- libXext
- libXp
- libXp-devel
- numactl-devel
- unixODBC
- zlib-devel

## 解决步骤

1. **上传所有 RPM 文件到服务器**：将本仓库中的所有 RPM 文件上传到你的 CentOS 7 服务器。

2. **进入服务器 RPM 文件路径**：使用 `cd` 命令进入你上传 RPM 文件的目录。

3. **执行安装命令**：在终端中执行以下命令来安装所有依赖包：

   ```bash
   rpm -ivh *.rpm --force --nodeps
   ```

   该命令会强制安装所有 RPM 文件，并忽略依赖关系。

## 注意事项

- 请确保在执行安装命令之前，已经备份了重要的数据和配置文件。
- 安装过程中可能会覆盖系统中已有的某些软件包，请谨慎操作。
- 如果在安装过程中遇到其他问题，请参考 Oracle 官方文档或社区支持。

通过以上步骤，你应该能够顺利解决在 CentOS 7 上安装 Oracle 11R2 时遇到的依赖问题。

## 下载链接

[CentOS7安装Oracle11R2最全依赖包](https://pan.quark.cn/s/1e3d9f22b8fb)