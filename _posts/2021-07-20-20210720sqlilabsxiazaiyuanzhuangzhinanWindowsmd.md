---
layout: post
title: "sqlilabs 下载与安装指南Windows"
date:   2023-08-27
tags: [labs,sqli,安装,MySQL,Windows]
comments: true
author: admin
---
# sqli-labs 下载与安装指南（Windows）

## 简介
sqli-labs 是一个由印度程序员开发的 SQL 注入学习工具，它以闯关游戏的形式帮助用户学习和实践 SQL 注入技术。本资源文件提供了 sqli-labs 在 Windows 系统下的下载与安装指南。

## 环境要求
- Apache + MySQL + PHP
- Windows 系统下可以使用 phpstudy、wamp 等集成环境进行安装

## 安装步骤

### 1. 下载 sqli-labs
从提供的资源文件中下载 sqli-labs 的压缩包。

### 2. 安装 phpstudy
- 下载并安装 phpstudy，确保 Apache 和 MySQL 服务正常运行。
- 将 phpstudy 的 PHP 版本设置为 5.x 以上，7.x 以下。

### 3. 解压 sqli-labs
将下载的 sqli-labs 压缩包解压到 phpstudy 的 WWW 目录下。

### 4. 配置 sqli-labs
- 打开解压后的 sqli-labs 文件夹，找到 `db-creds.inc` 文件。
- 根据需要修改数据库连接信息。

### 5. 启动 phpstudy
确保 Apache 和 MySQL 服务均为绿灯状态，表示服务正常运行。

### 6. 访问 sqli-labs
- 在浏览器中输入 `http://localhost/sqli-labs-master` 访问 sqli-labs。
- 点击 `setup/reset database for labs` 安装数据库。
- 安装成功后，返回上一页，点击 `SQLi-LABS Page-1`，看到页面显示则表示安装成功。

## 常见问题
- 如果之前安装了 MySQL，可能会导致数据库安装不成功。解决办法是关闭之前的 MySQL 服务，确保 phpstudy 的 MySQL 服务正常运行。
- 如果遇到其他问题，可以参考提供的文章中的详细步骤进行排查。

## 总结
通过以上步骤，你可以在 Windows 系统下成功安装并运行 sqli-labs，开始学习和实践 SQL 注入技术。

## 下载链接

[sqli-labs下载与安装指南Windows分享](https://pan.quark.cn/s/bb88a26738ae)