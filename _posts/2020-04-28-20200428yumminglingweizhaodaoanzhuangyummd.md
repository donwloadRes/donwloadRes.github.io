---
layout: post
title: "yum命令未找到安装yum"
date:   2022-02-19
tags: [rpm,yum,x86,64,centos]
comments: true
author: admin
---
# yum命令未找到，安装yum

在某些CentOS系统或类似RHEL环境中，你可能会遇到“yum命令未找到”的情况，这通常是因为系统未预装或已移除了yum包。此仓库提供了适用于CentOS 4的yum及相关依赖包，帮助快速解决这一问题，让你能够重新使用yum进行软件包管理。

## 资源包含的rpm包如下：

1. **centos-yumconf-4-4.5.noarch.rpm** - CentOS特有配置，确保yum工作的环境配置。
2. **python-elementtree-1.2.6-5.el4.centos.x86_64.rpm** - Python的ElementTree模块，yum依赖项之一。
3. **python-sqlite-1.1.7-1.2.1.x86_64.rpm** - Python对SQLite数据库的支持库。
4. **python-urlgrabber-2.9.8-2.noarch.rpm** - yum使用的下载工具模块。
5. **sqlite-3.3.6-2.x86_64.rpm** - SQLite数据库引擎。
6. **sqlite-devel-3.3.6-2.x86_64.rpm** - SQLite的开发文件，用于编译需要SQLite接口的软件。
7. **yum-2.4.3-4.el4.centos.noarch.rpm** - 主要的yum包，实现包管理和更新功能。
8. **yum-metadata-parser-1.0-8.el4.centos.x86_64.rpm** - 解析yum元数据的解析器，提升性能和稳定性。

## 安装步骤：

1. 下载上述所有列出的`.rpm`文件到同一目录下。
2. 打开终端，导航至存放这些rpm文件的目录。
3. 依次安装每个rpm文件，可以使用以下命令序列（每个文件名用实际文件名替换）：
   ```bash
   rpm -ivh python-elementtree-1.2.6-5.el4.centos.x86_64.rpm
   rpm -ivh sqlite-3.3.6-2.x86_64.rpm
   rpm -ivh sqlite-devel-3.3.6-2.x86_64.rpm
   rpm -ivh python-urlgrabber-2.9.8-2.noarch.rpm
   rpm -ivh centos-yumconf-4-4.5.noarch.rpm
   rpm -ivh yum-2.4.3-4.el4.centos.noarch.rpm
   rpm -ivh yum-metadata-parser-1.0-8.el4.centos.x86_64.rpm
   # 注意：如果之前安装过旧版本的任何这些包，可能需要先使用'rpm -e 包名'卸载它们
   ```
4. 完成以上步骤后，你应该已经成功安装了yum。可以通过输入`yum`来验证是否成功安装，系统应该会显示yum的相关命令选项。

请注意，这个解决方案针对的是较老的CentOS 4系统，对于更现代的Linux发行版，推荐使用dnf作为默认的包管理器。此外，直接安装这些特定版本的rpm包可能在新一些的系统上不兼容。务必根据你的具体操作系统版本选择合适的包进行安装。

## 下载链接

[yum命令未找到安装yum](https://pan.quark.cn/s/b5c59cf2a04f)