---
layout: post
title: "银河麒麟系统arrch64架构安装达梦数据库指南"
date:   2020-02-07
tags: [dmdba,bash,数据库,data,dm8]
comments: true
author: admin
---
# 银河麒麟系统arrch64架构安装达梦数据库指南

本资源文件提供了在银河麒麟系统（arrch64架构）上安装达梦数据库的详细步骤和配置说明。通过本指南，您可以顺利完成达梦数据库的安装和初始化设置。

## 安装步骤概览

1. **系统环境检查**
   - 确认操作系统版本和架构
   - 检查磁盘空间和网络环境

2. **创建dmdba用户**
   - 创建用户组和用户
   - 设置用户密码和文件打开最大数

3. **创建数据库安装目录**
   - 创建并授权安装路径
   - 上传达梦数据库安装文件

4. **数据库安装**
   - 切换用户并执行安装命令
   - 创建DmAPService服务

5. **配置环境变量**
   - 编辑bash_profile文件
   - 初始化数据库实例

6. **注册数据库服务**
   - 使用root用户注册服务
   - 设置数据库服务开机自启

7. **防火墙配置**
   - 检查并配置防火墙
   - 确保数据库端口开放

## 详细步骤

### 1. 系统环境检查

- **操作系统**：银河麒麟V10
- **CPU架构**：Arrch64
- **系统版本**：4.19.90-52.19.v2207.ky10.aarch64

### 2. 创建dmdba用户

```bash
groupadd dinstall
useradd -g dinstall -m -d /home/dmdba -s /bin/bash dmdba
passwd dmdba
vi /etc/security/limits.conf
```

在limits.conf文件中添加以下内容：

```bash
dmdba hard nofile 65536
dmdba soft nofile 65536
dmdba hard stack 32768
dmdba soft stack 16384
```

### 3. 创建数据库安装目录

```bash
mkdir /data/dm8 -p
chown dmdba:dinstall -R /data/dm8
chmod -R 755 /data/dm8
chown dmdba:dinstall /data/dm8/DMInstall.bin
chmod 755 /data/dm8/DMInstall.bin
```

### 4. 数据库安装

```bash
su dmdba
cd /data/dm8
./DMInstall.bin -i
```

### 5. 配置环境变量

```bash
su dmdba
vim .bash_profile
```

在.bash_profile文件中添加：

```bash
export PATH=$PATH:$DM_HOME/bin:$DM_HOME/tool
```

### 6. 注册数据库服务

```bash
cd /data/dm8/dmdbms/script/root
./dm_service_installer.sh -t dmserver -dm_ini /data/dm8/dmdata/DAMENG/dm.ini -p DMSERVER
```

### 7. 防火墙配置

```bash
systemctl enable DmServiceDMSERVER.service
systemctl start DmServiceDMSERVER.service
```

## 注意事项

- 安装过程中请确保网络环境正常。
- 安装路径建议选择非系统盘，以避免磁盘空间不足。
- 安装完成后，请检查防火墙设置，确保数据库端口开放。

通过以上步骤，您可以在银河麒麟系统上成功安装并配置达梦数据库。