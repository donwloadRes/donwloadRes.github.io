---
layout: post
title: "Zabbix 60 离线安装指南附RPM包"
date:   2021-01-02
tags: [mysql,Zabbix,RPM,mysqld,安装]
comments: true
author: admin
---
# Zabbix 6.0 离线安装指南（附RPM包）

## 简介
本资源文件提供了Zabbix 6.0的离线安装方法，并附带了所需的RPM包。适用于在没有互联网连接的环境中进行Zabbix服务器的安装和配置。

## 安装步骤

### 1. 准备工作
- 虚拟环境软件：VMware Workstation 17 pro
- 镜像：CentOS-7-x86_64-DVD-2009.iso

### 2. 离线安装Zabbix-server
1. 拷入RPM包并解压。
2. 安装MySQL：
   ```bash
   cd /opt/package/mysql
   rpm -ivh mysql-community-* --force --nodeps
   ```
3. 创建存储目录：
   ```bash
   mkdir -p /data/mysql
   chown mysql:mysql /data/mysql
   ```
4. 编辑配置文件：
   ```bash
   vim /etc/my.cnf
   ```
   配置内容如下：
   ```ini
   [mysqld]
   datadir=/data/mysql
   socket=/var/lib/mysql/mysql.sock
   log-error=/var/log/mysqld.log
   pid-file=/var/run/mysqld/mysqld.pid
   character-set-server=utf8mb4
   collation-server=utf8mb4_general_ci
   port=3306
   lower_case_table_names=1
   ```

### 3. 安装Zabbix
按照文章中的详细步骤进行Zabbix的安装和配置。

## 注意事项
- 确保所有依赖包已正确安装。
- 配置文件中的路径和参数需根据实际环境进行调整。

## 参考资料
- Zabbix官方文档
- CentOS官方文档

## 联系我们
如有任何问题或建议，请联系我们。

## 下载链接

[Zabbix6.0离线安装指南附RPM包](https://pan.quark.cn/s/13882c5ca200)