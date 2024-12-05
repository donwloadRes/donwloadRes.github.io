---
layout: post
title: "CentOS 76 安装 Git 指南"
date:   2021-02-13
tags: [Git,git,usr,local,bash]
comments: true
author: admin
---
# CentOS 7.6 安装 Git 指南

本仓库提供了一个详细的指南，帮助你在CentOS 7.6系统上安装Git。Git是一个开源的分布式版本控制系统，广泛用于软件开发项目中。

## 安装步骤

### 1. 解压gz包
首先，进入`/usr/local`目录，并创建一个名为`git`的目录。将下载的gz包放入该目录中，然后解压gz包。

```bash
cd /usr/local
mkdir git
tar -zxvf git-2.33.1.tar.gz
```

### 2. 配置环境变量
编辑`/etc/profile`文件，添加以下配置信息：

```bash
make prefix=/usr/local/git all
make prefix=/usr/local/git install
export PATH=/usr/local/git/bin:$PATH
```

保存并退出后，使环境变量生效：

```bash
source /etc/profile
```

### 3. 校验安装
运行以下命令，检查Git是否安装成功：

```bash
git --version
```

如果显示Git的版本信息，表示安装成功。

## 注意事项
- 确保系统已连接到互联网，以便下载必要的依赖包。
- 如果遇到任何问题，请参考[CSDN博客文章](https://blog.csdn.net/lzc2644481789/article/details/124888525)获取更多帮助。

通过以上步骤，你应该能够在CentOS 7.6系统上成功安装Git。

## 下载链接

[CentOS7.6安装Git指南](https://pan.quark.cn/s/8e9e3e4bc078)