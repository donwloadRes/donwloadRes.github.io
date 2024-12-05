---
layout: post
title: "乌班图Ubuntu开启root远程登录权限指南"
date:   2023-09-23
tags: [root,Ubuntu,SSH,登录,bash]
comments: true
author: admin
---
# 乌班图Ubuntu开启root远程登录权限指南

## 概览

在使用Ubuntu系统时，有时因管理需求需启用root账户进行远程访问。本资源提供了详细步骤，指导如何安全地配置Ubuntu以允许root用户通过SSH远程登录。此过程涉及设置root密码和修改SSH服务器配置。

## 步骤详解

### 1. 设置root账户密码

首先，确保你的Ubuntu系统已安装完毕。若要启用root登录功能，你需要为root账户设置密码。打开终端并执行以下命令：

```bash
sudo passwd root
```

按照提示，输入你希望设定的root密码，并再次确认。完成这一步后，root账户就有了密码。

### 2. 开启SSH服务并允许root登录

接下来，我们将配置SSH以接受root用户的连接。

- **切换到root用户** (如果你之前没有使用sudo -i或者直接作为root登录的话)：

```bash
sudo su -
```
或直接使用`sudo`执行后续命令。

- **编辑SSH配置文件**：

```bash
nano /etc/ssh/sshd_config
```

- 在该文件中找到这一行：
  
  ```
  #PermitRootLogin prohibit-password
  ```

  将其取消注释（去掉前面的`#`），并修改为允许root登录：

  ```
  PermitRootLogin yes
  ```

- 保存更改并退出编辑器。在nano中，可以通过按`Ctrl + X`，然后按`Y`来确认保存，最后按回车键。

- **重启SSH服务** 使更改生效：

```bash
systemctl restart sshd
```

或者，在某些版本的Ubuntu上，可能是：

```bash
service ssh restart
```

至此，你已经成功配置了Ubuntu系统，使其允许root用户通过SSH进行远程登录。请确保你的网络环境安全，以避免潜在的安全风险。

---

请注意，启用root远程登录虽然方便，但也有一定的安全风险，建议仅在必要时使用，并且应采取其他安全措施，如使用强壮的密码、开启公钥认证等，以保护系统安全。

## 下载链接

[乌班图Ubuntu开启root远程登录权限指南分享](https://pan.quark.cn/s/9fa15d91939f)