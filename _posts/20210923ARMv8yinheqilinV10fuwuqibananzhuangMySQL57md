---
layout: post
title: "ARMv8 银河麒麟V10服务器版安装 MySQL5.7"
date:   2022-01-18
tags: [mysql,usr,MySQL,local,bash]
comments: true
author: admin
---
# ARMv8 银河麒麟V10服务器版安装 MySQL5.7

本文档详细介绍了如何在ARMv8架构的银河麒麟V10服务器版上安装MySQL 5.7。以下是安装步骤的简要概述：

## 安装步骤

1. **下载 MySQL 5.7 安装包**  
   下载适用于ARMv8架构的MySQL 5.7安装包，并将其上传到服务器。

2. **解压安装包**  
   使用以下命令解压安装包：
   ```bash
   tar xzvf mysql-5.7.27-aarch64.tar.gz -C /usr/local/
   ```

3. **配置MySQL**  
   将解压后的文件夹重命名为`mysql`，并进行相关配置：
   ```bash
   mv /usr/local/mysql-5.7.27-aarch64 /usr/local/mysql
   mkdir -p /usr/local/mysql/logs
   chown -R mysql:mysql /usr/local/mysql
   ln -sf /usr/local/mysql/my.cnf /etc/my.cnf
   cp -rf /usr/local/mysql/extra/lib* /usr/lib64/
   mv /usr/lib64/libstdc++.so.6 /usr/lib64/libstdc++.so.6.old
   ln -s /usr/lib64/libstdc++.so.6.0.24 /usr/lib64/libstdc++.so.6
   ```

4. **设置开机启动**  
   将MySQL服务设置为开机启动：
   ```bash
   cp -rf /usr/local/mysql/support-files/mysql.server /etc/init.d/mysqld
   chmod +x /etc/init.d/mysqld
   systemctl enable mysqld
   ```

5. **添加环境变量**  
   编辑`/etc/profile`文件，添加以下内容：
   ```bash
   export MYSQL_HOME=/usr/local/mysql
   export PATH=$PATH:$MYSQL_HOME/bin
   ```
   然后使环境变量生效：
   ```bash
   source /etc/profile
   ```

6. **初始化并启动MySQL**  
   初始化MySQL并启动服务：
   ```bash
   mysqld --initialize-insecure --user=mysql --basedir=/usr/local/mysql --datadir=/usr/local/mysql/data
   systemctl start mysqld
   ```

7. **查看MySQL状态**  
   使用以下命令查看MySQL服务状态：
   ```bash
   systemctl status mysqld
   ```

8. **登录MySQL**  
   使用以下命令登录MySQL：
   ```bash
   mysql -u root
   ```

9. **设置MySQL用户**  
   在MySQL中删除已有root用户并添加新的root用户：
   ```sql
   delete from mysql.user where user='root';
   grant all privileges on *.* to 'root'@'%' identified by 'rootpwd';
   flush privileges;
   ```

## 注意事项
- 确保服务器已获得root权限。
- 安装过程中可能需要根据实际情况调整配置文件。
- 安装完成后，建议进行安全配置以保护MySQL数据库。

通过以上步骤，您可以在ARMv8架构的银河麒麟V10服务器版上成功安装并配置MySQL 5.7。

## 下载链接

[ARMv8银河麒麟V10服务器版安装MySQL5.7](https://pan.quark.cn/s/b5687cf7c5e5)