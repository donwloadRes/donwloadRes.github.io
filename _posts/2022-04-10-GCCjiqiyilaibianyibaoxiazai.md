---
layout: post
title: "GCC及其依赖编译包下载"
date:   2022-01-03
tags: [x86,64,rpm,el7,GCC]
comments: true
author: admin
---
# GCC及其依赖编译包下载

## 资源描述

本仓库提供了一系列用于编译和运行GCC（GNU Compiler Collection）所需的依赖包。这些RPM包适用于CentOS 7系统，支持x86_64架构。以下是资源文件的详细列表：

- `cpp-4.8.5-28.el7.x86_64.rpm`
- `gcc-4.8.5-28.el7.x86_64.rpm`
- `glibc-devel-2.17-222.el7.x86_64.rpm`
- `glibc-headers-2.17-222.el7.x86_64.rpm`
- `kernel-headers-3.10.0-862.el7.x86_64.rpm`
- `libmpc-1.0.1-3.el7.x86_64.rpm`
- `mpfr-3.1.1-4.el7.x86_64.rpm`

## 使用说明

1. **下载资源**：
   您可以直接从本仓库下载上述列出的RPM包。

2. **安装依赖**：
   在CentOS 7系统上，您可以使用以下命令安装这些RPM包：
   ```bash
   sudo rpm -ivh cpp-4.8.5-28.el7.x86_64.rpm gcc-4.8.5-28.el7.x86_64.rpm glibc-devel-2.17-222.el7.x86_64.rpm glibc-headers-2.17-222.el7.x86_64.rpm kernel-headers-3.10.0-862.el7.x86_64.rpm libmpc-1.0.1-3.el7.x86_64.rpm mpfr-3.1.1-4.el7.x86_64.rpm
   ```

3. **验证安装**：
   安装完成后，您可以使用以下命令验证GCC是否成功安装：
   ```bash
   gcc --version
   ```

## 注意事项

- 请确保您的系统是CentOS 7，并且架构为x86_64。
- 在安装这些RPM包之前，建议先备份您的系统配置文件。
- 如果系统中已经存在相同版本的软件包，可能会导致冲突，请谨慎操作。

## 联系我们

如果您在使用过程中遇到任何问题或有任何建议，欢迎通过GitHub Issues联系我们。

## 下载链接

[GCC及其依赖编译包下载](https://pan.quark.cn/s/9c83fda9cd71)