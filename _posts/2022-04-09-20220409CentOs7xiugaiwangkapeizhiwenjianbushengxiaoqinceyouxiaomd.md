---
layout: post
title: "CentOs7修改网卡配置文件不生效亲测有效"
date:   2020-08-25
tags: [网卡,配置文件,eth0,nmcli,虚拟机]
comments: true
author: admin
---
# CentOs7修改网卡配置文件不生效-亲测有效

在CentOS 7系统中，有时修改网卡配置文件后发现配置并未生效，这可能会导致网络连接问题。本文将介绍一种亲测有效的方法，通过使用`nmcli`命令来修改网卡配置，并确保配置生效。

## 问题描述

在CentOS 7中，修改网卡配置文件（如`/etc/sysconfig/network-scripts/ifcfg-eth0`）后，重启网络服务或虚拟机，发现配置并未生效。这通常是因为虚拟机启动时获取IP地址的配置文件不是`eth0`，而是其他网卡配置文件。

## 解决方案

### 1. 使用`nmcli`命令修改网卡配置

首先，使用`nmcli`命令来修改网卡配置。`nmcli`是NetworkManager的命令行工具，可以方便地管理网络配置。

例如，修改`eth0`的IP地址和子网掩码：

```bash
nmcli connection modify eth0 ipv4.addresses 192.168.1.100/24
nmcli connection modify eth0 ipv4.gateway 192.168.1.1
nmcli connection modify eth0 ipv4.dns 8.8.8.8
nmcli connection modify eth0 ipv4.method manual
```

### 2. 重启虚拟机

修改完成后，重启虚拟机以使配置生效。

```bash
reboot
```

### 3. 检查配置是否生效

重启后，使用`ip addr`或`ifconfig`命令检查`eth0`的IP地址是否已正确配置。

```bash
ip addr show eth0
```

### 4. 处理其他网卡配置文件

如果配置仍未生效，说明虚拟机启动时获取IP地址的配置文件不是`eth0`。此时，需要检查并处理其他网卡配置文件。

1. 列出所有网卡配置文件：

   ```bash
   ls /etc/sysconfig/network-scripts/ifcfg-*
   ```

2. 找到其他网卡配置文件（如`ifcfg-eth1`、`ifcfg-ens33`等），并将其修改或删除。

3. 再次重启虚拟机，确保配置生效。

## 总结

通过使用`nmcli`命令修改网卡配置，并确保虚拟机启动时获取IP地址的配置文件正确，可以有效解决CentOS 7中修改网卡配置文件不生效的问题。希望本文的方法能帮助你顺利解决网络配置问题。

## 下载链接

[CentOs7修改网卡配置文件不生效-亲测有效分享](https://pan.quark.cn/s/fa80d60b9344)