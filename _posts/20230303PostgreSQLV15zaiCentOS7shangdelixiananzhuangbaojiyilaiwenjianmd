---
layout: post
title: "PostgreSQL V15 在 CentOS7 上的离线安装包及依赖文件"
date:   2023-07-15
tags: [rpm,PostgreSQL,x86,64,15]
comments: true
author: admin
---
# PostgreSQL V15 在 CentOS7 上的离线安装包及依赖文件

本仓库提供了在 CentOS7 操作系统上离线安装 PostgreSQL V15 所需的完整软件包集合。如果您因为网络限制或安全策略需要在没有互联网连接的环境下部署 PostgreSQL 15，这些资源将是您的理想选择。此套资源包含了 PostgreSQL 15 的核心组件以及必要的依赖库，确保您能顺利进行离线安装和运行。

## 包含文件列表：

- `libzstd-1.5.5-1.el7.x86_64.rpm` - 提供了 Zstandard 压缩算法的支持。
- `libicu-50.2-4.el7_7.x86_64.rpm` - 国际化和本地化支持库，PostgreSQL 需要它来处理各种字符集和全球化数据。
- `postgresql15-15.3-1PGDG.rhel7.x86_64.rpm` - PostgreSQL 15 主程序包。
- `postgresql15-libs-15.3-1PGDG.rhel7.x86_64.rpm` - PostgreSQL 15 必需的共享库。
- `postgresql15-server-15.3-1PGDG.rhel7.x86_64.rpm` - PostgreSQL 服务器组件，用于搭建数据库服务。

## 安装指南：

1. **下载资源**：首先，您需要将本仓库中的所有列出的 `.rpm` 文件下载到您的 CentOS7 系统中。
   
2. **安装依赖包**：使用 `rpm` 命令依次安装 `libzstd-1.5.5-1.el7.x86_64.rpm` 和 `libicu-50.2-4.el7_7.x86_64.rpm`，确保系统满足 PostgreSQL 的依赖要求。
   ```bash
   rpm -ivh libzstd-1.5.5-1.el7.x86_64.rpm
   rpm -ivh libicu-50.2-4.el7_7.x86_64.rpm
   ```

3. **安装 PostgreSQL**：接下来，安装 PostgreSQL 本身及其相关的包。
   ```bash
   rpm -ivh postgresql15-libs-15.3-1PGDG.rhel7.x86_64.rpm
   rpm -ivh postgresql15-server-15.3-1PGDG.rhel7.x86_64.rpm
   ```

4. **初始化数据库**：安装完毕后，初始化 PostgreSQL 数据库实例。
   ```bash
   sudo /usr/pgsql-15/bin/postgresql-15-setup initdb
   ```

5. **启动 PostgreSQL 服务**：
   ```bash
   sudo systemctl start postgresql-15.service
   ```
   若要设置开机自启：
   ```bash
   sudo systemctl enable postgresql-15.service
   ```

至此，您已经在 CentOS7 系统上成功地离线安装了 PostgreSQL V15。您可以按照 PostgreSQL 的官方文档进一步配置和管理您的数据库系统。

请注意，保持操作系统和软件包的更新对于维护系统的安全性至关重要，但在这个特定场景下，请确保在有网络访问时手动检查并更新相关软件以获取最新的安全修复和改进。

## 下载链接

[PostgreSQLV15在CentOS7上的离线安装包及依赖文件](https://pan.quark.cn/s/692127df9ae7)