---
layout: post
title: "CentOS 7 解决 yum 命令报错 There are no enabled repos
date   20210422
tags yumreporepos命令CentOS
comments true
author admin

 CentOS 7 解决 yum 命令报错 There are no enabled repos"
date:   2021-04-22
tags: [yum,repo,repos,命令,CentOS]
comments: true
author: admin
---
# CentOS 7 解决 yum 命令报错 "There are no enabled repos"

## 简介

本资源文件旨在帮助解决在 CentOS 7 系统中使用 `yum` 命令时遇到的报错：“There are no enabled repos”。该错误通常发生在 `yum repolist` 命令返回 0 个仓库，而 `yum list` 命令正常工作的情况下。

## 问题描述

在使用 `yum` 命令时，可能会遇到以下错误信息：

```
There are no enabled repos.
```

尽管 `yum list` 命令可以正常列出软件包，但 `yum repolist` 命令显示仓库数量为 0。这通常是由于 `repo` 文件配置错误或缺失导致的。

## 解决方法

### 1. 检查 yum 工具是否已安装

首先，确保系统中已安装 `yum` 工具。可以使用以下命令检查：

```bash
rpm -qa | grep yum
```

如果没有安装，请参考相关文档进行安装。

### 2. 备份并替换 repo 文件

进入 `/etc/yum.repos.d/` 目录，备份现有的 `repo` 文件：

```bash
cd /etc/yum.repos.d/
mv CentOS-Base.repo CentOS-Base.repo.backup
```

然后，下载对应版本的 `repo` 文件并放入 `/etc/yum.repos.d/` 目录中。可以使用以下命令下载：

```bash
wget -O /etc/yum.repos.d/CentOS-Base.repo http://mirrors.163.com/.help/CentOS7-Base-163.repo
```

### 3. 生成缓存

下载并替换 `repo` 文件后，运行以下命令生成缓存：

```bash
yum clean all
yum makecache
```

### 4. 验证问题是否解决

最后，使用以下命令验证问题是否已解决：

```bash
yum repolist
```

如果命令返回的仓库数量大于 0，则问题已成功解决。

## 总结

通过以上步骤，您可以解决 CentOS 7 系统中 `yum` 命令报错 "There are no enabled repos" 的问题。确保正确配置 `repo` 文件并生成缓存后，`yum` 命令将恢复正常使用。

## 下载链接

[CentOS7解决yum命令报错Therearenoenabledrepos](https://pan.quark.cn/s/9dee1f4e6175)