---
layout: post
title: "CentOS 7 下 CM631  CDH632 安装部署指南"
date:   2020-01-05
tags: [安装,指南,CM,CM6.3,CentOS]
comments: true
author: admin
---
# CentOS 7 下 CM6.3.1 + CDH6.3.2 安装部署指南

本仓库提供了一个详细的安装部署指南，帮助用户在CentOS 7系统上安装Cloudera Manager 6.3.1（CM6.3.1）和Cloudera Distribution Including Apache Hadoop 6.3.2（CDH6.3.2）。

## 内容概述

本指南涵盖了从基础环境准备到最终安装完成的整个过程，包括以下主要步骤：

1. **基础环境准备**
   - 修改主机名
   - 关闭防火墙
   - 关闭SELinux
   - 添加内网映射
   - 安装JDK并设置环境变量
   - 配置免密登录
   - NTP时间同步

2. **关系型数据库安装**
   - 卸载MariaDB
   - 安装MySQL 5.7
   - 创建数据库并授权
   - 配置JDBC

3. **CM安装**
   - 布置CM安装包
   - 配置CM包yum源
   - 分发包
   - 安装CM server
   - 初始化CM的数据库

4. **CDH安装**
   - 下载CDH相关包
   - 配置本地parcel存储库
   - 生成sha文件

## 使用说明

1. **下载资源文件**：请从本仓库下载所需的资源文件。
2. **参考指南**：按照指南中的步骤进行操作，确保每一步都正确执行。
3. **问题排查**：如果在安装过程中遇到问题，请参考指南中的问题排查部分。

## 注意事项

- 请确保所有节点的基础环境配置一致。
- 在安装过程中，务必按照指南中的顺序进行操作。
- 如果遇到网络问题，建议使用本地下载后再上传到服务器的方式。

通过本指南，您将能够顺利在CentOS 7系统上完成CM6.3.1和CDH6.3.2的安装部署。

## 下载链接

[CentOS7下CM6.3.1CDH6.3.2安装部署指南](https://pan.quark.cn/s/8f0d9fb97a67)