---
layout: post
title: "【CentOS】CentOS安装yum教程概述"
date:   2021-10-27
tags: [yum,rpm,el7,--,CentOS]
comments: true
author: admin
---
# 【CentOS】CentOS安装yum教程概述

本文档旨在为遇到CentOS系统中yum包管理器缺失或损坏的用户提供详细指导，以帮助您重新安装并配置yum。当您的系统因操作不当或其他原因导致yum不可用时，通过此教程，您可以逐步恢复系统的基本软件包管理能力。

## 教程概览

### 准备工作

- **适用环境**：本教程主要面向CentOS 7用户，部分步骤同样适用于CentOS 8及之前的版本。
- **问题场景**：如果您已经不慎卸载了yum或者遇到了yum无法使用的错误。

### 步骤分解

#### 1. 下载必要包

- 从可靠的源，例如[镜像站点](http://mirrors.163.com/centos/7/os/x86_64/Packages/)，下载以下五个关键的rpm包：
  - `python-2.7.5-89.el7.x86_64.rpm`
  - `python-iniparse-0.4-9.el7.noarch.rpm`
  - `yum-metadata-parser-1.1.4-10.el7.x86_64.rpm`
  - `yum-3.4.3-168.el7.centos.noarch.rpm`
  - `yum-plugin-fastestmirror-1.1.31-54.el7_8.noarch.rpm`

或使用分享的网盘链接获取这些文件。

#### 2. 安装包

- 通过终端命令安装这些包，可能需要使用`--nodeps`和`--force`选项来强制安装，以绕过可能的依赖关系检查问题：
  ```bash
  rpm -ivh python-2.7.5-89.el7.x86_64.rpm python-iniparse-0.4-9.el7.noarch.rpm --nodeps --force
  rpm -ivh yum-metadata-parser-1.1.4-10.el7.x86_64.rpm --nodeps --force
  rpm -ivh yum-3.4.3-168.el7.centos.noarch.rpm yum-plugin-fastestmirror-1.1.31-54.el7_8.noarch.rpm --nodeps --force
  ```

#### 3. 更改yum源

- 下载并替换默认的yum源文件，通常推荐使用稳定且速度较快的国内镜像，如网易163或阿里云的CentOS镜像站，并将它们放置于`/etc/yum.repos.d/`目录下。

#### 4. 清理与更新缓存

- 清除现有缓存以避免冲突：
  ```bash
  yum clean all
  ```
- 紧接着刷新缓存以确保最新信息：
  ```bash
  yum makecache
  ```

### 测试与验证

- 完成上述步骤后，通过运行`yum list`或尝试安装一个小软件来确认yum是否已正确安装并能够正常工作。

### 注意事项

- 在执行任何破坏性操作之前，确保重要数据的安全。
- 仔细阅读每个命令的意义，避免不必要的系统故障。
- 对于复杂的依赖问题，有时重装Python和yum是最直接有效的解决方案。

通过跟随这个教程，您应能成功恢复或安装CentOS中的yum包管理器，从而顺利地进行软件的安装和管理。

## 下载链接

[CentOSCentOS安装yum教程概述](https://pan.quark.cn/s/12e7b61c8708)