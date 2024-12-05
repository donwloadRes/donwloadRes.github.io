---
layout: post
title: "plsql以及instantclient下载安装配置使用指南"
date:   2020-02-04
tags: [Oracle,Instant,Client,数据库,PL]
comments: true
author: admin
---
# plsql以及instantclient下载安装配置使用指南

本文档提供了详细的步骤，帮助您下载、安装配置PL/SQL Developer与Oracle Instant Client，以便于远程连接和管理Oracle数据库。以下是整个流程的概览：

## 下载资源

- **PL/SQL Developer**: 是一款强大的Oracle数据库管理与开发工具。
- **Oracle Instant Client**: 是Oracle提供的轻量级客户端，支持数据库的基本连接，无需安装完整的Oracle数据库客户端。

### 直接下载链接已失效，请自行访问官方网站或可信源获取最新版。

## 安装步骤

### PL/SQL Developer安装

1. 下载PL/SQL Developer的安装包，并进行默认安装。
2. 完成安装后，应用永久注册码：
   - **Product Code**: 4t46t6vydkvsxekkvf3fjnpzy5wbuhphqz
   - **Serial Number**: 601769
   - **Password**: xs374ca

### Oracle Instant Client配置

1. 下载Oracle Instant Client基本包并解压至适当位置（如`D:\instantclient_11_2`）。
2. 在解压目录下创建`NETWORK\ADMIN`文件夹，并在此内创建`tnsnames.ora`文件，配置示例：
   ```
   NC611 = (DESCRIPTION = (ADDRESS_LIST = (ADDRESS = (PROTOCOL = TCP)(HOST = 数据库IP地址)(PORT = 1521)) ) (CONNECT_DATA = (SERVICE_NAME = 数据库服务名) ) )
   ```
   
3. **环境变量配置**:
   - 设置`NLS_LANG=AMERICAN_AMERICA.AL32UTF8` 或根据需要设定语言编码。
   - 设定`TNS_ADMIN`为Instant Client的网络配置目录路径（如`D:\instantclient_11_2\network\admin`）。

### 配合PL/SQL Developer使用

1. **环境配置**: 在PL/SQL Developer中配置。
   - 进入`Configure -> Preferences -> Connection`。
   - 设置`Oracle Home`为你Instant Client的路径。
   - 设置`OCI Library`为oci.dll的路径，通常位于Instant Client根目录下。
   
2. 保存配置后，重新启动PL/SQL Developer，输入在`tnsnames.ora`中定义的Database名进行连接。

## 注意事项

- 确保Oracle数据库服务端已正确配置并运行。
- 对于操作系统特定的环境变量设置，参照相应操作系统指南。
- 若遇到连接问题，请检查网络连接、防火墙设置以及数据库监听器状态。

本指南基于旧有的资源链接编写，实际操作时请使用最新的软件版本，并参照其官方文档或更新的教程进行操作。

## 下载链接

[plsql以及instantclient下载安装配置使用指南](https://pan.quark.cn/s/e3e557cd2ca4)