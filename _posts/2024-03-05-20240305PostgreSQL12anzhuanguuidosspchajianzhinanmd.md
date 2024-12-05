---
layout: post
title: "PostgreSQL 12 安装 uuid-ossp 插件指南"
date:   2020-08-13
tags: [插件,uuid,ossp,PostgreSQL,安装]
comments: true
author: admin
---
# PostgreSQL 12 安装 uuid-ossp 插件指南

本仓库提供了一个资源文件，用于在 PostgreSQL 12 中安装 `uuid-ossp` 插件。`uuid-ossp` 插件允许您在 PostgreSQL 数据库中生成 UUID（通用唯一标识符），这对于需要唯一标识符的应用程序非常有用。

## 资源文件内容

- `uuid-ossp.so` 文件：这是 `uuid-ossp` 插件的核心文件，需要将其放置在 PostgreSQL 的库目录中。
- 其他相关文件：这些文件用于扩展 `uuid-ossp` 插件的功能，需要放置在 PostgreSQL 的扩展目录中。

## 安装步骤

1. **上传文件到 PostgreSQL 服务器**
   - 将 `uuid-ossp.so` 文件上传到 `/usr/local/pgsql/lib` 目录下，并赋予执行权限。
   - 将其他相关文件上传到 `/usr/local/pgsql/share/extension` 目录下。

2. **检查插件是否可用**
   - 执行以下 SQL 命令，检查 `uuid-ossp` 插件是否可用：
     ```sql
     SELECT * FROM pg_available_extensions WHERE name LIKE '%uuid%';
     ```

3. **安装 uuid-ossp 插件**
   - 执行以下 SQL 命令安装 `uuid-ossp` 插件：
     ```sql
     CREATE EXTENSION IF NOT EXISTS "uuid-ossp";
     ```

4. **验证安装**
   - 安装完成后，可以通过以下 SQL 命令查看插件是否安装成功：
     ```sql
     SELECT * FROM pg_extension;
     ```

5. **使用插件**
   - 安装成功后，可以使用 `uuid_generate_v4()` 函数生成 UUID：
     ```sql
     SELECT uuid_generate_v4();
     ```

## 注意事项

- 如果是主从架构，需要在主库和从库上都上传相关文件，但只需在主库执行 `CREATE EXTENSION` 命令，它会自动同步到从库上。
- 在从库上手动执行 `CREATE EXTENSION` 命令会报错。
- 需要切换到业务库执行 `CREATE EXTENSION` 命令，否则用户在 `pg_extension` 中查不到该插件，并且无法使用该插件。

## 参考资料

本指南参考了以下文章：
- [PostgreSQL 12 安装 uuid-ossp 插件](https://blog.csdn.net/yabignshi/article/details/134252306)

通过以上步骤，您可以成功在 PostgreSQL 12 中安装并使用 `uuid-ossp` 插件。

## 下载链接

[PostgreSQL12安装uuid-ossp插件教程](https://pan.quark.cn/s/2eb581ddc0ef)