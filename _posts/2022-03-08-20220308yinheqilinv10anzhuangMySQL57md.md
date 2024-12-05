---
layout: post
title: "银河麒麟v10安装MySQL57"
date:   2023-08-29
tags: [MySQL,mysql,5.7,安装,命令]
comments: true
author: admin
---
# 银河麒麟v10安装MySQL5.7

## 简介

本资源文件提供了在银河麒麟v10操作系统上安装MySQL 5.7的详细步骤和所需文件。通过本资源，您可以轻松地在银河麒麟v10系统上完成MySQL 5.7的安装和配置。

## 安装步骤

### 1. 环境准备

- **查看操作系统版本**：使用命令 `nkvers` 查看当前操作系统的版本。
- **下载安装包**：下载提供的MySQL 5.7安装包。

### 2. 安装前准备

- **检查是否已安装MySQL**：使用命令 `rpm -qa | grep mysql` 检查系统中是否已安装MySQL。
- **卸载旧版本**：如果存在旧版本的MySQL，使用命令 `rpm -e --nodeps` 卸载。
- **删除残余文件**：使用命令 `whereis mysql` 查找并删除所有残余的MySQL文件。

### 3. 开始安装

- **拷贝安装包**：将下载的MySQL 5.7安装包拷贝到服务器上。
- **执行安装命令**：使用命令 `rpm -ivh mysql-5.7.27-1.el7.aarch64.rpm` 进行安装。
- **配置my.cnf**：将提供的 `my.cnf` 文件拷贝到 `/etc/` 目录下。
- **解压数据文件**：在 `/usr/local/mysql/` 目录下创建 `data` 文件夹，并将数据文件解压到该目录。
- **创建日志文件**：在 `/usr/local/mysql/` 目录下创建 `log` 文件夹，并创建 `mysql-error.log` 和 `mysqld.pid` 文件。
- **授权文件**：使用命令 `chown -R mysql:mysql /usr/local/mysql/` 对MySQL目录进行授权。
- **添加环境变量**：编辑 `/etc/profile` 文件，添加以下内容：
  ```bash
  export MYSQL_HOME=/usr/local/mysql
  export PATH=$PATH:$MYSQL_HOME/bin
  ```
- **使环境变量生效**：使用命令 `source /etc/profile` 使环境变量生效。

### 4. 启动MySQL服务

- **启动服务**：使用命令 `service mysql start` 启动MySQL服务。
- **登录数据库**：使用命令 `mysql -u root -p` 登录MySQL，默认密码为 `123456`。
- **修改密码**：登录后使用命令 `set password for root = password('新密码')` 修改密码。

## 注意事项

- 确保系统满足MySQL 5.7的安装要求。
- 在执行安装和配置步骤时，请仔细阅读每一步的说明，避免操作失误。

## 参考资料

- 更多详细信息请参考提供的描述文章。

---

通过以上步骤，您可以在银河麒麟v10系统上成功安装并配置MySQL 5.7。如果在安装过程中遇到任何问题，请参考相关文档或寻求技术支持。