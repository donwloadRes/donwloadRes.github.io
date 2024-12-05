---
layout: post
title: "Liunx服务器安装SVN（安装包版）"
date:   2024-05-08
tags: [SVN,usr,local,bash,安装包]
comments: true
author: admin
---
# Liunx服务器安装SVN（安装包版）

本资源文件提供了在Liunx服务器上安装SVN（Subversion）的详细步骤和所需安装包。通过本资源，您可以轻松地在Liunx服务器上部署SVN，并进行版本控制管理。

## 资源内容

1. **SVN安装包**：包含了最新版本的SVN客户端安装包，适用于Liunx操作系统。
2. **依赖包**：提供了安装SVN所需的依赖包，确保安装过程顺利进行。

## 安装步骤

### 1. 下载SVN安装包

通过提供的下载链接，获取SVN安装包并将其上传至Liunx服务器。

### 2. 安装依赖包

在安装SVN之前，需要先安装相关的依赖包。具体步骤如下：

- 解压依赖包：
  ```bash
  tar -zxvf apr-1.4.5.tar.gz
  ```
- 安装依赖包：
  ```bash
  cd apr-1.4.5
  ./configure --prefix=/usr/local/apr
  make && make install
  ```

### 3. 安装SVN

- 解压SVN安装包：
  ```bash
  tar -zxvf subversion-1.14.2.tar.gz
  ```
- 配置并安装SVN：
  ```bash
  cd subversion-1.14.2
  ./configure --prefix=/usr/local/svn --with-apr=/usr/local/apr --with-apr-util=/usr/local/apr-util --with-sqlite=/usr/local/sqlite/sqlite-autoconf-3080800 --with-utf8proc=internal --with-lz4=internal
  make && make install
  ```

### 4. 配置SVN

- 创建版本库：
  ```bash
  svnadmin create /usr/local/svn/svndata
  ```
- 修改配置文件：
  ```bash
  vim /usr/local/svn/svndata/conf/svnserve.conf
  ```
  添加以下配置：
  ```ini
  [general]
  anon-access = none
  auth-access = write
  password-db = passwd
  authz-db = authz
  realm = /usr/local/svn/svndata
  ```
- 设置用户密码：
  ```bash
  vim /usr/local/svn/svndata/conf/passwd
  ```
  添加用户账号和密码：
  ```ini
  user1 = passwd1
  user2 = passwd2
  ```
- 配置用户权限：
  ```bash
  vim /usr/local/svn/svndata/conf/authz
  ```
  配置用户的读写权限：
  ```ini
  [groups]
  admin = user1,user2
  developer = user3,user4

  [/]
  @admin = rw
  @developer = r
  ```

### 5. 启动SVN服务

```bash
svnserve -d -r /usr/local/svn/svndata/
```

### 6. 验证SVN是否启动成功

```bash
ps -ef|grep svnserve
```

## 注意事项

- 确保服务器有足够的磁盘空间和内存资源。
- 在安装过程中，如果遇到依赖包缺失的情况，请根据提示安装相应的依赖包。

通过以上步骤，您可以在Liunx服务器上成功安装并配置SVN，实现版本控制管理。

## 下载链接

[Liunx服务器安装SVN安装包版分享](https://pan.quark.cn/s/9153682d35b7)