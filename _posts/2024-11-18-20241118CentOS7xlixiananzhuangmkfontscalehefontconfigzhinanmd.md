---
layout: post
title: "CentOS 7x 离线安装mkfontscale和fontconfig指南"
date:   2021-02-13
tags: [rpm,mkfontscale,字体,fontconfig,离线]
comments: true
author: admin
---
# CentOS 7.x 离线安装mkfontscale和fontconfig指南

## 文档概述

本文旨在指导您在无网络连接的CentOS 7环境下，如何离线安装mkfontscale和fontconfig组件，进而解决可能遇到的截图乱码问题。通过本指南，您将学会手动下载所需的rpm包，并完成本地安装流程，确保您的Linux系统能够正确显示中文和其他字体。

### 步骤概览

1. **准备工作**：确认您有一台可以连接互联网的辅助Linux机器。
2. **下载依赖包**：使用`yumdownloader`工具下载`mkfontscale`和`fontconfig`及相关依赖包。
3. **转移至目标机器**：将下载的rpm包传送到离线环境的目标CentOS 7系统。
4. **安装mkfontscale和fontconfig**：在目标机器上执行特定命令安装rpm包。
5. **配置字体**：创建字体目录，安装字体，并更新字体缓存。

### 具体步骤

#### 1. 在有网环境中下载rpm包

- 安装`yum-utils`：确保您可以使用`yumdownloader`命令。
  ```
  yum install -y yum-utils
  ```

- 下载所需软件包至指定目录，例如 `/root/font_rpm`。
  ```
  yumdownloader --resolve --destdir=/root/font_rpm mkfontscale fontconfig
  ```

#### 2. 文件传输

使用FTP、SCP或其他文件传输工具，将`/root/font_rpm`目录下的所有rpm包传输到离线CentOS 7系统的相应位置。

#### 3. 在目标机器上安装

- 切换到含有rpm包的目录，然后执行安装命令。如果遇到依赖冲突，可以使用以下命令强制安装。
  ```
  rpm -ivh *.rpm --nodeps --force
  ```

#### 4. 安装字体

- 创建字体存储目录：
  ```
  mkdir -p /usr/share/fonts
  ```
  
- 将您的字体文件复制到 `/usr/share/fonts`。
  
- 更新字体索引和缓存：
  ```
  cd /usr/share/fonts/
  mkfontscale
  mkfontdir
  fc-cache -fv
  ```

### 结论

通过以上步骤，您可以在CentOS 7离线环境中成功安装mkfontscale和fontconfig，有效解决屏幕截图等场景中的字体乱码问题。这有助于优化Linux系统中字体的管理和显示效果，提高用户体验。

## 下载链接

[CentOS7.x离线安装mkfontscale和fontconfig指南](https://pan.quark.cn/s/b04609e2602f)