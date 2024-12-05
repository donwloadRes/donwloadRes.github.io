---
layout: post
title: "Linux 安装nginx 1.24.0 亲测有效指南"
date:   2023-10-17
tags: [nginx,bash,安装,Linux,1.24]
comments: true
author: admin
---
# Linux 安装nginx 1.24.0 亲测有效指南

## 概述

本文档为您提供了一份详尽的步骤指导，以帮助您在Linux环境中顺利安装nginx 1.24.0版本。本教程经过实践验证，确保每个步骤都清晰易懂，适合Linux初学者以及有一定基础的用户。

## 安装步骤

### 准备工作

1. **创建目录**：首先，在`/usr/local/`下创建一个用于存放nginx的文件夹。
   ```bash
   mkdir /usr/local/nginx
   ```

2. **下载安装包**：通过提供的百度网盘链接下载nginx-1.24.0.tar.gz，提取码为`s8k6`。您也可以从nginx官方或其他可靠的源下载最新的源代码包。

3. **上传文件**：使用rz命令或FTP客户端将下载的文件上传到服务器的相应目录。

### 安装过程

4. **安装依赖**：确保系统已安装必要的开发工具及依赖库，如gcc、zlib、pcre、openssl。
   ```bash
   yum -y install gcc zlib zlib-devel pcre-devel openssl openssl-devel
   ```

5. **解压文件**：
   ```bash
   tar -zxvf nginx-1.24.0.tar.gz
   ```

6. **配置编译**：
   进入解压后的目录，配置安装路径及其它选项。
   ```bash
   cd nginx-1.24.0
   ./configure --prefix=/usr/local/nginx
   ```

7. **编译与安装**：
   执行编译与安装命令。
   ```bash
   make
   make install
   ```

8. **启动nginx**：
   进入sbin目录，并启动nginx服务。
   ```bash
   cd /usr/local/nginx/sbin/
   ./nginx -c /usr/local/nginx/conf/nginx.conf
   ```

### 配置与管理

9. **防火墙设置**：如果使用防火墙，打开80端口。
   ```bash
   firewall-cmd --add-port=80/tcp --permanent
   firewall-cmd --reload
   ```

10. **开机自启配置**：
    创建systemd服务文件以实现开机启动。
    ```bash
    sudo vim /etc/systemd/system/nginx.service
    ```
    写入相应的服务配置，并保存。

11. **启用与测试**：
    启动服务并检查状态。
    ```bash
    sudo systemctl start nginx
    sudo systemctl enable nginx
    sudo systemctl status nginx
    ```

## 注意事项

- 确保每一步执行无误，特别是配置文件的路径和参数。
- 在生产环境中，推荐使用非root用户权限进行编译安装以提升安全性。
- 根据实际系统类型，可能需要调整依赖库的安装方法，例如在Debian系Linux上可能会使用`apt-get`而不是`yum`。

此指南旨在快速引导您完成nginx的安装，具体操作时还需根据实际情况灵活调整。祝您安装顺利！

## 下载链接

[Linux安装nginx1.24.0亲测有效指南](https://pan.quark.cn/s/e31575569d1b)