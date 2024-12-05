---
layout: post
title: "Windows MySQL 80 忘记密码后重置密码亲测可用"
date:   2020-07-20
tags: [MySQL,密码,命令提示符,8.0,bash]
comments: true
author: admin
---
# Windows MySQL 8.0 忘记密码后重置密码（亲测可用）

当您忘记了 Windows 上 MySQL 8.0 的密码时，可以按照以下步骤进行找回：

## 步骤一：停止 MySQL 服务

首先，您需要停止 MySQL 服务。打开命令提示符（以管理员身份），然后输入以下命令：

```bash
net stop MySQL80
```

## 步骤二：以不检查密码的方式启动 MySQL

接下来，您需要以不检查密码的方式启动 MySQL。在命令提示符中输入以下命令：

```bash
C:\Program Files\MySQL\MySQL Server 8.0\bin\mysqld.exe --skip-grant-tables --skip-networking
```

## 步骤三：登录 MySQL

在命令提示符中，尝试登录 MySQL：

```bash
mysql -u root
```

## 步骤四：重设密码

在 MySQL 提示符下，执行以下命令来重设 root 用户的密码：

```sql
ALTER USER root@localhost IDENTIFIED BY 'YourNewPassword';
```

请将 `YourNewPassword` 替换为您想要设置的新密码。

## 步骤五：刷新权限

最后，刷新权限以确保更改生效：

```sql
FLUSH PRIVILEGES;
```

完成以上步骤后，您应该能够使用新密码登录 MySQL。

---

**注意**：在进行这些操作时，请确保您有管理员权限，并且在操作过程中不要关闭命令提示符窗口，以免影响 MySQL 的正常运行。

## 下载链接

[WindowsMySQL8.0忘记密码后重置密码亲测可用分享](https://pan.quark.cn/s/742fafa97c4f)