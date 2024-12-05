---
layout: post
title: "小白指南：MySQL 5.7 非安装版配置教程与资源分享"
date:   2020-11-27
tags: [MySQL,5.7,mysql,---,ini]
comments: true
author: admin
---
# 小白指南：MySQL 5.7 非安装版配置教程与资源分享

---

## 概述

本资源为MySQL 5.7非安装版的详细配置教程，特别适合初次接触MySQL的新手。通过本教程，您可以轻松地在Windows系统上设置好MySQL环境，无需经历复杂的安装流程。同时，我们提供了百度云资源链接，方便您快速下载MySQL 5.7的压缩包。

---

## 文档版本对应教程

- **教程来源**: [CSDN博客文章](https://blog.csdn.net/weidong_y/article/details/81660958)
- **适用版本**: MySQL 5.7.x

---

## 教程步骤概览

### 1. 下载MySQL 5.7非安装版

- **官方下载**：可选择直接从MySQL官方网站下载。
- **百度云分享**：[提取码：dsn](https://pan.baidu.com/s/11ZgLj5cAwOyhv-C32iW1Gg)

### 2. 解压与目录结构

- 将下载的ZIP文件解压至希望的路径，例如`C:\Program Files\mysql-5.7.23-winx64`。
- 在该目录下创建`my.ini`配置文件，并填入相应的配置内容。

### 3. 配置my.ini

基础配置示例：
```ini
[mysql]
default-character-set=utf8

[mysqld]
port = 3306
basedir=C:\Program Files\mysql-5.7.23-winx64
datadir=C:\Program Files\mysql-5.7.23-winx64\data
max_connections=20
character-set-server=utf8
default-storage-engine=INNODB
```

### 4. 启动MySQL服务

1. 以管理员身份打开CMD。
2. 转至MySQL的bin目录执行安装命令：`mysqld install`，随后启动服务：`net start mysql`。

### 5. 初始密码配置

- 首次启动可能无初始密码，通过编辑`my.ini`解锁登录限制，重启服务。
- 登录MySQL (`mysql -u root -p`)，无密码直接回车，然后更新root用户的密码。

### 6. 更改密码与权限刷新

```sql
UPDATE USER SET authentication_string=PASSWORD("你的新密码") WHERE USER='root';
FLUSH PRIVILEGES;
```

记得完成后重新注释或删除`my.ini`中的`skip-grant-tables`。

---

## 注意事项

- 在操作过程中，请确保所有步骤严格按照教程指导进行。
- 完成配置后，建议移除或安全锁定`my.ini`中的敏感配置。
- 定期备份数据，保证数据安全性。

通过以上步骤，即便是新手也能顺利搭建起本地的MySQL 5.7数据库环境，开启你的数据库管理之旅！

---

此文档旨在提供简明清晰的指引，帮助大家快速上手。祝您的学习与工作顺利！

## 下载链接

[小白指南MySQL5.7非安装版配置教程与资源分享指南](https://pan.quark.cn/s/5c3c6f0041ac)