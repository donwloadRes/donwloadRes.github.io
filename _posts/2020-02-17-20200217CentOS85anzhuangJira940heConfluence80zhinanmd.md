---
layout: post
title: "CentOS85安装Jira 940和Confluence 80指南
date   20230403
tags bashmysql80etcusr
comments true
author admin

 CentOS85安装Jira 940和Confluence 80指南

本仓库提供了一个详细的安装指南帮助你在CentOS 85系统上安装Jira 940和Confluence 80以下是安装步骤的简要概述

 系统准备
1 关闭防火墙
   bash
   systemctl stop firewalld
   systemctl disable firewalld
   

2 关闭SELinux
   bash
   vi etcselinuxconfig
   SELINUXdisabled
   

 安装JDK
1 解压JDK
   bash
   tar zxvf jdk8u241linuxx64targz C usrlocal
   

2 配置环境变量
   bash
   vi etcprofile
   export JAVAHOMEusrlocaljava
   export CLASSPATHCLASSPATHJAVAHOMElib
   export PATHPATHJAVAHOMEbin
   source etcprofile
   

 安装MySQL 8
1 手动安装MySQL
   bash
   mkdir p usrlocalmysql
   xz d mysql8031linuxglibc212x8664tarxz
   tar xvf mysql8031linuxglibc212x8664tar C usrlocal
   ln s mysql8031linuxglibc212x8664 mysql
   

2 配置MySQL
   bash
   vi etcmycnf
   mysqld
   port3306
   basedirusrlocalmysql
   datadirdatamysqldata
   

3 初始化MySQL
   bash
   usrlocalmysqlmysql8031binmysqld defaultsfileetcmycnf initialize usermysql basedirusrlocalmysqlmysql8031 datadirdatamysqldata
   

 安装Jira
1 创建Jira用户
   bash
   useradd u 2000 jira
   

2 安装Jira
   bash
   bash atlassianjirasoftware940x64bin
   

3 配置Jira
   bash
   vi setenvsh
   export JAVAOPTSjavaagenthomejiraatlassianagentjar JAVAOPTS"
date:   2023-04-03
tags: [bash,mysql,8.0,etc,usr]
comments: true
author: admin
---
# CentOS8.5安装Jira 9.40和Confluence 8.0指南

本仓库提供了一个详细的安装指南，帮助你在CentOS 8.5系统上安装Jira 9.40和Confluence 8.0。以下是安装步骤的简要概述：

## 系统准备
1. **关闭防火墙**：
   ```bash
   systemctl stop firewalld
   systemctl disable firewalld
   ```

2. **关闭SELinux**：
   ```bash
   vi /etc/selinux/config
   SELINUX=disabled
   ```

## 安装JDK
1. **解压JDK**：
   ```bash
   tar -zxvf jdk-8u241-linux-x64.tar.gz -C /usr/local
   ```

2. **配置环境变量**：
   ```bash
   vi /etc/profile
   export JAVA_HOME=/usr/local/java
   export CLASSPATH=$:CLASSPATH:$JAVA_HOME/lib/
   export PATH=$PATH:$JAVA_HOME/bin
   source /etc/profile
   ```

## 安装MySQL 8
1. **手动安装MySQL**：
   ```bash
   mkdir -p /usr/local/mysql
   xz -d mysql-8.0.31-linux-glibc2.12-x86_64.tar.xz
   tar xvf mysql-8.0.31-linux-glibc2.12-x86_64.tar -C /usr/local/
   ln -s mysql-8.0.31-linux-glibc2.12-x86_64 mysql
   ```

2. **配置MySQL**：
   ```bash
   vi /etc/my.cnf
   [mysqld]
   port=3306
   basedir=/usr/local/mysql/
   datadir=/data/mysql/data
   ```

3. **初始化MySQL**：
   ```bash
   /usr/local/mysql/mysql-8.0.31/bin/mysqld --defaults-file=/etc/my.cnf --initialize --user=mysql --basedir=/usr/local/mysql/mysql-8.0.31 --datadir=/data/mysql/data
   ```

## 安装Jira
1. **创建Jira用户**：
   ```bash
   useradd -u 2000 jira
   ```

2. **安装Jira**：
   ```bash
   bash atlassian-jira-software-9.4.0-x64.bin
   ```

3. **配置Jira**：
   ```bash
   vi setenv.sh
   export JAVA_OPTS="-javaagent:/home/jira/atlassian-agent.jar $[JAVA_OPTS]"
   ```

## 安装Confluence
1. **创建Confluence用户**：
   ```bash
   useradd -u 3000 confluence
   ```

2. **安装Confluence**：
   ```bash
   bash atlassian-confluence-8.0.0-x64.bin
   ```

## 其他注意事项
- **关闭IPv6**：
  ```bash
  vi /etc/sysctl.conf
  net.ipv6.conf.all.disable_ipv6 = 1
  net.ipv6.conf.default.disable_ipv6 = 1
  net.ipv6.conf.lo.disable_ipv6 = 1
  sysctl -p /etc/sysctl.conf
  ```

通过以上步骤，你可以在CentOS 8.5系统上成功安装Jira 9.40和Confluence 8.0。如果在安装过程中遇到任何问题，请参考详细的文章描述或联系技术支持。

## 下载链接

[CentOS8.5安装Jira9.40和Confluence8.0指南](https://pan.quark.cn/s/40c3769f9e8f)