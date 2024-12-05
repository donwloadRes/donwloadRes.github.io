---
layout: post
title: "Ubuntu 18.04 离线安装配置 FTP (vsftpd) 步骤及所需 deb 安装包"
date:   2021-04-20
tags: [vsftpd,bash,安装包,deb,laogao]
comments: true
author: admin
---
# Ubuntu 18.04 离线安装配置 FTP (vsftpd) 步骤及所需 deb 安装包

本仓库提供了一个资源文件，用于在 Ubuntu 18.04 系统上离线安装和配置 FTP 服务器 (vsftpd)。以下是详细的安装步骤和所需的 deb 安装包。

## 安装步骤

1. **解压安装包**  
   将 `vsftpd.tar.gz` 上传到服务器后，进行解压安装：
   ```bash
   tar -zxvf vsftpd.tar.gz
   cd vsftpd
   sh install.sh
   ```

2. **上传配置文件**  
   将 `vsftpd.chroot_list`、`vsftpd.conf`、`vsftpd.user_list` 上传至 `/etc` 目录中，替换原有文件。

3. **创建用户目录**  
   在 `/opt` 目录下创建 FTP 用户目录：
   ```bash
   cd /opt
   mkdir ftp
   cd ftp
   mkdir laogao
   mkdir xiaozhou
   ```

4. **新建 FTP 用户组**  
   创建一个新的用户组 `ftpgroup`：
   ```bash
   groupadd ftpgroup
   ```

5. **添加用户并设置密码**  
   添加用户 `laogao` 和 `xiaozhou`，并设置密码：
   ```bash
   useradd -g ftpgroup -d /opt/ftp -s /bin/bash laogao
   passwd laogao
   useradd -g ftpgroup -d /opt/ftp -s /bin/bash xiaozhou
   passwd xiaozhou
   ```

6. **设置权限**  
   设置用户目录的权限，确保用户只能对其自己的目录进行读写操作：
   ```bash
   chown laogao laogao
   chown xiaozhou xiaozhou
   ```

7. **配置用户列表**  
   将新建的用户名添加到 vsftpd 的用户配置文档中：
   ```bash
   vim /etc/vsftpd.user_list
   ```

8. **重启服务**  
   重启 vsftpd 服务以应用配置：
   ```bash
   service vsftpd restart
   ```

## 所需 deb 安装包

本仓库中包含了以下 deb 安装包，用于离线安装 vsftpd：

- `vsftpd_3.0.3-3ubuntu2_amd64.deb`

请确保在执行安装步骤前，将这些 deb 安装包上传到服务器并解压。

## 注意事项

- 在第6步骤中，根据需求设置相应的权限。样例中权限为：用户只能对用户自己的文件夹进行读写操作，其他权限需要使用 `chmod` 命令设置自定义权限。
- 如有问题，可以留言或者私信。

---

希望本资源能帮助你在 Ubuntu 18.04 系统上顺利安装和配置 FTP 服务器。

## 下载链接

[Ubuntu18.04离线安装配置FTPvsftpd步骤及所需deb安装包分享](https://pan.quark.cn/s/79c955984a27)