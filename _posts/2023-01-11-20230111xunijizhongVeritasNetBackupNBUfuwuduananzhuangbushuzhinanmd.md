---
layout: post
title: "虚拟机中Veritas NetBackupNBU服务端安装部署指南"
date:   2020-08-19
tags: [NBU,服务端,bash,安装,NetBackup]
comments: true
author: admin
---
# 虚拟机中Veritas NetBackup（NBU）服务端安装部署指南

## 简介
本资源文件提供了在虚拟机环境中安装和部署Veritas NetBackup（NBU）服务端的详细步骤。NBU是一款广泛使用的企业级备份软件，适用于多种操作系统。通过本指南，您可以在虚拟机中轻松完成NBU服务端的安装和配置。

## 安装环境
- **操作系统**: RHEL 7
- **虚拟化软件**: VirtualBox 或 Parallels Desktop
- **内存**: 4GB
- **磁盘**: 50GB
- **IP地址**: 10.211.55.111

## 安装步骤

### 1. 下载并上传安装包
首先，下载NBU服务端的安装包，并将其上传至Linux主机。

### 2. 关闭防火墙和SELinux
为了确保安装过程顺利，需要关闭防火墙和SELinux。

```bash
systemctl stop firewalld
systemctl disable firewalld
sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config
```

### 3. 创建用户和组
安装NBU服务端需要创建特定的用户和组。

```bash
mkdir /usr/openv -p
groupadd nbwebgrp
useradd -g nbwebgrp -c 'NetBackup Web Services account' -d /usr/openv/wmc nbwebsvc
```

### 4. 配置内核参数
NBU安装需要配置一些内核参数。

```bash
echo 300 307200 32 1024 > /proc/sys/kernel/sem
echo "kernel.sem = 300 307200 32 1024" >> /etc/sysctl.conf
sysctl -p
```

### 5. 配置ulimit
配置ulimit以避免安装过程中出现错误。

```bash
ulimit -f unlimited
ulimit -n 8000
```

### 6. 配置环境变量
为了方便使用NBU命令，配置环境变量。

```bash
cat <<EOF >> /root/.bash_profile
export NBU_HOME=/usr/openv/netbackup
export PATH=\$NBU_HOME/bin:\$PATH
export PS1="[\`whoami\`@\`hostname\`:"'\w]# '
EOF
```

### 7. 解压并安装NBU
进入安装包目录，解压并执行安装。

```bash
tar -xf NetBackup_8.1.1_LinuxR_x86_64.tar.gz
cd NetBackup_8.1.1_LinuxR_x86_64
./install
```

### 8. 初始化NBU服务端
安装完成后，进行初始化设置。

1. **创建存储卷**: 在主机上创建一个目录作为存储卷。
2. **创建Token**: 配置客户端连接所需的Token。

## 注意事项
- 确保所有配置完成后，重启主机并检查SELinux是否已关闭。
- 安装过程中请按照提示输入正确的许可证密钥。

通过以上步骤，您可以在虚拟机中成功安装和配置Veritas NetBackup（NBU）服务端，开始使用NBU进行数据备份。

## 下载链接

[虚拟机中VeritasNetBackupNBU服务端安装部署指南](https://pan.quark.cn/s/2e2a33ba738a)