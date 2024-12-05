---
layout: post
title: "Ubuntu离线安装Samba与配置指南"
date:   2023-03-29
tags: [Samba,samba,Ubuntu,bash,usr]
comments: true
author: admin
---
# Ubuntu离线安装Samba与配置指南

本资源文件提供了在Ubuntu系统上离线安装Samba服务器的详细步骤和配置方法。通过本文档，您可以了解如何在没有网络连接的情况下安装和配置Samba，以便在局域网内共享文件和打印机。

## 内容概述

1. **Samba离线安装**
   - 下载Samba安装包
   - 解压并安装Samba
   - 配置Samba服务

2. **配置Samba进行共享文件夹访问**
   - 添加Ubuntu用户
   - 将Ubuntu用户添加到Samba用户
   - 修改Samba配置文件

## 安装步骤

### 1. Samba离线安装

#### 1.1 下载安装包
首先，您需要下载Samba的安装包（例如：`samba-3.2.0.tar.gz`）。

#### 1.2 解压并安装Samba
将下载好的安装包传到服务器上，并在压缩包所在路径下依次执行以下命令：
```bash
tar zxvf samba-3.2.0.tar.gz
cd samba-3.2.0/source
./configure
make
make install
```

#### 1.3 配置Samba服务
安装完成后，将解压目录中的配置文件复制到指定位置：
```bash
cp /home/cqf/samba-3.2.0/examples/smb.conf.default /usr/local/samba/lib/smb.conf
```

### 2. 配置Samba进行共享文件夹访问

#### 2.1 添加Ubuntu用户
默认情况下，Samba将用户设置为安全模式，这意味着客户端必须输入共享文件夹的用户名和密码。首先，添加一个Ubuntu用户：
```bash
sudo adduser share_user
```

#### 2.2 将Ubuntu用户添加到Samba用户
将新添加的Ubuntu用户添加到Samba用户，并设置Samba密码：
```bash
/usr/local/samba/bin/smbpasswd -a share_user
```

#### 2.3 修改Samba配置文件
编辑Samba配置文件，确保工作组的值与Windows计算机的工作组设置相同：
```bash
vi /usr/local/samba/lib/smb.conf
```

## 启动Samba服务

启动Samba服务并测试是否安装成功：
```bash
/usr/local/samba/sbin/smbd -D
/usr/local/samba/sbin/nmbd -D
/usr/local/samba/bin/testparm
```

## 注意事项

- 确保配置文件中指定的路径存在，否则Windows访问时会提示错误。
- 如果Ubuntu的防火墙开启，需要开放445端口，并为Windows用户开启445访问权限。

通过以上步骤，您可以在Ubuntu系统上成功离线安装并配置Samba服务器，实现文件和打印机的共享。

## 下载链接

[Ubuntu离线安装Samba与配置指南](https://pan.quark.cn/s/5bcac851896d)