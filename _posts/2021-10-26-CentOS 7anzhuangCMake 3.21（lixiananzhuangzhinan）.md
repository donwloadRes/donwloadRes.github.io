---
layout: post
title: "CentOS 7安装CMake 3.21（离线安装指南）"
date:   2020-06-14
tags: [安装,tar,CMake,3.21,离线]
comments: true
author: admin
---
# CentOS 7安装CMake 3.21（离线安装指南）

---

**简介**

本资源提供了在CentOS 7系统下离线安装CMake 3.21的详细步骤。对于没有稳定互联网连接的环境，这篇指南尤为实用。通过遵循以下步骤，您可以在您的CentOS 7机器上成功安装CMake 3.21版本，确保您能够本地编译和管理软件项目。

**离线安装包获取**

离线安装所需的CMake 3.21源码包及其依赖（如gcc-c++和openssl）已经预先准备。您需手动下载这些文件，并通过FTP、SSH等方式传输至目标CentOS 7系统。

**安装步骤**

1. **文件上传**
   - 将`cmake-3.21.0-rc2.tar.gz`, `gcc-c++-4.8.5-44.el7.tar.gz`, 和 `openssl-1.0.2k-21.el7.tar.gz` 文件上传至CentOS 7服务器的适当位置。

2. **解压文件**
   ```bash
   tar -zxvf cmake-3.21.0-rc2.tar.gz
   tar -zxvf gcc-c++-4.8.5-44.el7.tar.gz
   tar -zxvf openssl-1.0.2k-21.el7.tar.gz
   ```

3. **安装依赖**
   - 使用YUM安装gcc-c++（注意：此处实际应使用上传的gcc-c++包替代标准YUM安装步骤）
   - 解压后的gcc-c++包，找到rpm文件并执行安装。
   - 类似地处理openssl安装，使用上传的openssl rpm包进行安装。

4. **验证安装**
   - 安装完成后，检查gcc和openssl的版本以确认正确安装。

5. **源码安装CMake**
   - 进入CMake解压目录，执行以下命令：
     ```bash
     ./bootstrap
     make
     make install
     ```
   
6. **完成安装验证**
   - 运行`cmake --version`，屏幕上应显示CMake 3.21.0的版本信息，标志着安装成功。

**注意事项**

- 确保在执行./bootstrap之前，所有必要的依赖都已经安装或编译完毕。
- 如果在安装过程中遇到任何问题，比如缺少依赖，需手动查找对应的离线安装包进行补充安装。
- 操作每一步都建议在具有足够权限的账户下进行，通常需要sudo或者作为root用户。

通过以上步骤，您应该能在离线环境中顺利在CentOS 7系统上搭建起CMake 3.21的开发环境。

## 下载链接

[CentOS7安装CMake3.21离线安装指南](https://pan.quark.cn/s/8ac944e2e5d8)