---
layout: post
title: "在Linux系统中离线安装PostgreSQL和PostGIS亲测可用"
date:   2023-10-12
tags: [usr,local,--,bash,postgresql]
comments: true
author: admin
---
# 在Linux系统中离线安装PostgreSQL和PostGIS亲测可用

## 简介
本资源文件提供了一个详细的指南，帮助用户在Linux系统中离线安装PostgreSQL和PostGIS。通过遵循本指南，用户可以在没有互联网连接的环境中成功安装和配置这两个强大的数据库工具。

## 安装步骤

### 1. 准备工作
- **关闭防火墙**：为了方便连接数据库，建议关闭防火墙。
  ```bash
  systemctl stop firewalld
  ```

### 2. 安装PostgreSQL
- **上传文件**：将PostgreSQL的安装文件上传到`/usr/local`目录下。
- **安装依赖**：确保安装了必要的编译工具（如gcc和g++）。
  ```bash
  rpm -Uvh * rpm --nodeps --force
  ```
- **解压并安装**：
  ```bash
  tar -zxvf postgresql-9.5.7.tar.gz
  cd postgresql-9.5.7
  ./configure --prefix=/usr/local/postgresql --with-libxml
  gmake
  gmake install
  ```
- **创建用户和目录**：
  ```bash
  useradd postgres
  cd /usr/local/postgresql
  mkdir data
  chown -R postgres:postgres data
  ```
- **设置环境变量**：
  ```bash
  vi /etc/profile
  export PGDATA=/usr/local/postgresql/data
  export PGHOME=/usr/local/postgresql
  export PATH=$PGHOME/bin:$PATH
  source /etc/profile
  ```
- **初始化数据库**：
  ```bash
  su postgres
  initdb
  pg_ctl -D /usr/local/postgresql/data -l logfile start
  psql
  alter user postgres with password '密码'
  \q
  ```

### 3. 安装PostGIS
- **安装依赖**：确保安装了必要的依赖包，如bzip2、gcc、g++、gdal、geos、libxml2、proj、json-c等。
- **解压并安装**：
  ```bash
  tar -zxvf postgis-2.5.1.tar.gz -C /opt
  cd /opt/postgis-2.5.1
  ./configure --prefix=/usr/local/postgis \
  --with-pgconfig=/usr/local/postgresql/bin/pg_config \
  --with-xml2config=/usr/local/libxml2-2.9.1/bin/xml2-config \
  --with-geosconfig=/usr/local/geos-3.6.3/bin/geos-config \
  --with-gdalconfig=/usr/local/gdal-2.0.0/bin/gdal-config \
  --with-projdir=/usr/local/proj-5.2.0
  make
  make install
  ```
- **创建扩展**：
  ```bash
  su postgres
  psql
  create database postgis
  \c postgis
  create extension postgis
  ```

## 注意事项
- 确保所有依赖包都已正确安装，否则可能会导致安装失败。
- 在安装过程中，如果遇到缺少共享对象文件的错误，可以通过复制相应文件到PostgreSQL的lib目录下解决。

## 结语
通过本指南，您可以在Linux系统中成功离线安装PostgreSQL和PostGIS。希望这个资源对您有所帮助！

## 下载链接

[在Linux系统中离线安装PostgreSQL和PostGIS亲测可用分享](https://pan.quark.cn/s/e5922108b98a)