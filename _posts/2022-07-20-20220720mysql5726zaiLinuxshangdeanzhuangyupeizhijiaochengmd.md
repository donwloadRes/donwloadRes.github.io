---
layout: post
title: "mysql-5.7.26在Linux上的安装与配置教程"
date:   2022-10-06
tags: [mysql,MySQL,5.7,26,安装]
comments: true
author: admin
---
# mysql-5.7.26在Linux上的安装与配置教程

本教程详细指导您如何在Linux操作系统上安装和配置MySQL 5.7.26版本。通过本教程，您可以顺利完成MySQL数据库的搭建，并进行基础配置。以下是详细的步骤说明：

## 准备工作

确保您的Linux环境已准备好，并具有足够的权限来安装软件。推荐使用`wget`或直接在终端下载所需的`.tar.gz`安装包。

### 下载安装包

如果您没有提前下载，可以通过以下命令下载MySQL 5.7.26的安装文件：

```bash
wget https://cdn.mysql.com//Downloads/MySQL-5.7/mysql-5.7.26-linux-glibc2.12-x86_64.tar.gz
```

## 解压与安装

1. **解压文件**:
    ```bash
    tar -zxvf mysql-5.7.26-linux-glibc2.12-x86_64.tar.gz
    ```

2. **创建安装目录和移动文件**:
    创建一个安装目录，例如`/home/develop/mysql`，并将解压后的文件移至此目录。

3. **环境配置**:
    根据需要设置环境变量，但本教程主要关注非标准路径的快速启动配置。

## 用户与组设置

- 使用`groupadd`添加MySQL组。
- 使用`useradd`添加MySQL用户，并将其关联至之前创建的组。
- 设置MySQL用户的密码。

## 初始化配置

1. **创建数据目录**并在MySQL安装路径下。
2. **配置my.cnf文件**，创建或编辑`/etc/my.cnf`以包含必要的配置信息。
3. 初始安装时，可能会生成一个临时密码，请查看日志获取。

## 初始化数据库

运行初始化脚本并留意生成的临时密码，通常位于日志文件中。按照指示，使用该密码首次登录MySQL。

```bash
cd mysql-5.7.26
./bin/mysqld --initialize --user=mysql --basedir=/path/to/your/installation --datadir=/path/to/data
```

## 启动服务与密码修改

- 使用`service mysql start`启动MySQL服务。
- 首次登录可能需使用临时密码，随后立即更改`root`用户密码。

```bash
mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED BY 'YourNewPassword';
FLUSH PRIVILEGES;
```

## 远程访问配置

允许远程连接，更新用户表中的host字段以接受任意IP（%）连接。

```bash
USE mysql;
UPDATE user SET Host='%' WHERE User='root';
FLUSH PRIVILEGES;
```

## 注意事项

- 在执行上述步骤时，根据实际情况调整路径和细节。
- 保持系统安全，避免使用过于简单的密码。
- 定期备份数据，尤其是生产环境。

通过遵循以上步骤，您可以成功地在Linux系统上安装和配置MySQL 5.7.26版本。

## 下载链接

[mysql-5.7.26在Linux上的安装与配置教程](https://pan.quark.cn/s/134aa1c34700)