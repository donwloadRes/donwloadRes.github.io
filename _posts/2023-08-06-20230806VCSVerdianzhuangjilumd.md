---
layout: post
title: "VCSVerdi安装记录"
date:   2023-03-20
tags: [安装,VCS,Verdi,Synopsys,synopsys]
comments: true
author: admin
---
# VCS、Verdi安装记录

本仓库提供了一个详细的安装记录，帮助用户在Ubuntu 16.04系统上安装Synopsys VCS、Verdi和SCL。以下是安装步骤的简要概述：

## 安装步骤

1. **下载相关文件**：
   - 从百度网盘下载所需的安装文件，包括synopsys_installer、vcs_2016、verdi_2016、scl_v11.9和scl_keygen。

2. **创建安装目录**：
   - 在Linux系统中创建安装目录，例如`/home/***/synopsys/`，并在该目录下创建子目录`vcs_2016.06`、`verdi_2016.06-1`和`scl_11.9`。

3. **运行安装脚本**：
   - 运行`SynopsysInstaller_v3.3.run`脚本，按照提示进行安装。选择合适的安装路径，并根据系统选择64位版本。

4. **破解许可证**：
   - 在Windows系统中运行`scl_keygen.exe`，修改HOST ID、HOSTNAME和截止日期，生成`Synopsys.dat`文件。
   - 将生成的`Synopsys.dat`文件拷贝到`/home/***/synopsys/vcs_2016.06/license`和`/home/***/synopsys/verdi_2016.06-1/license`目录下。

5. **添加环境变量**：
   - 编辑`~/.bashrc`文件，添加VCS、Verdi和SCL的环境变量，并激活配置。

6. **激活软件**：
   - 安装`lsb-core`包，并运行`lmg_vcs`命令激活软件。

## 注意事项

- 安装过程中可能会遇到权限问题，请确保有足够的权限进行操作。
- 安装路径和环境变量需要根据实际安装情况进行调整。

通过以上步骤，您应该能够在Ubuntu 16.04系统上成功安装并配置Synopsys VCS、Verdi和SCL。

## 下载链接

[VCSVerdi安装记录](https://pan.quark.cn/s/69cd609a2364)