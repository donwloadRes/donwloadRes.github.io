---
layout: post
title: "Windows 安装压缩版 PostgreSQL 指南"
date:   2020-10-21
tags: [PostgreSQL,Windows,数据库,bin,压缩包]
comments: true
author: admin
---
# Windows 安装压缩版 PostgreSQL 指南

本资源文件提供了一个详细的指南，帮助用户在 Windows 系统上安装压缩版的 PostgreSQL 数据库。通过本指南，您可以轻松地完成 PostgreSQL 的安装和配置，无需复杂的步骤和额外的工具。

## 内容概述

1. **下载 PostgreSQL 压缩包**
   - 从官方网站或百度网盘下载 PostgreSQL 的压缩包。

2. **解压安装**
   - 将下载的压缩包解压到指定目录，并进行初始化数据库的操作。

3. **启动 PostgreSQL 服务**
   - 使用命令行启动 PostgreSQL 服务，并了解如何关闭和重启服务。

4. **配置远程访问**
   - 配置 PostgreSQL 以允许远程访问，确保数据库的安全性和可用性。

5. **注册为 Windows 服务**
   - 将 PostgreSQL 注册为 Windows 服务，确保系统重启后服务自动启动。

6. **使用自带客户端连接到 PostgreSQL**
   - 使用 PostgreSQL 自带的客户端工具连接到数据库，进行基本的数据库操作。

## 使用步骤

### 1. 下载
- 从 [PostgreSQL 官方网站](https://www.postgresql.org/download/windows/) 下载适用于 Windows 的压缩包。
- 或者从百度网盘下载：链接：[百度网盘下载链接] 提取码：dzyy

### 2. 解压安装
- 将下载的压缩包解压到 D 盘或其他指定目录。
- 使用命令行初始化数据库：
  ```
  bin\initdb -D data -U postgres -A password -E utf8 --locale=C -W
  ```

### 3. 启动服务
- 启动 PostgreSQL 服务：
  ```
  bin\pg_ctl -D data start
  ```
- 关闭服务：
  ```
  bin\pg_ctl -D data stop
  ```
- 重启服务：
  ```
  bin\pg_ctl -D data restart
  ```

### 4. 配置远程访问
- 修改配置文件以监听所有 IP 地址。
- 允许任意客户端 IP 连接。
- 重新启动 PostgreSQL 服务。

### 5. 注册为 Windows 服务
- 使用管理员权限打开命令提示符，切换到 PostgreSQL 目录，执行以下命令：
  ```
  bin\pg_ctl.exe register -N pgsql -D "d:\pgsql\data" -S auto
  ```

### 6. 连接到 PostgreSQL
- 使用自带客户端连接到数据库：
  ```
  bin\psql.exe -h localhost -p 5432 -U postgres
  ```

## 注意事项
- 确保系统满足 PostgreSQL 的最低要求。
- 在配置远程访问时，注意网络安全，避免不必要的安全风险。

通过本指南，您可以轻松地在 Windows 系统上安装和配置 PostgreSQL 数据库，享受高效的数据库管理体验。

## 下载链接

[Windows安装压缩版PostgreSQL指南](https://pan.quark.cn/s/67e0754b1fe5)