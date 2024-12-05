---
layout: post
title: "AWS虚拟机pem密钥使用指南"
date:   2021-09-21
tags: [pem,AWS,EC2,your,实例]
comments: true
author: admin
---
# AWS虚拟机pem密钥使用指南

在进行AWS（Amazon Web Services）的EC2实例管理时，特别是对于Linux系统的实例，安全地通过SSH登录是日常操作的重要部分。AWS提供了`.pem`格式的私钥文件，用于无密码登录到您的虚拟机。下面将介绍如何在不同操作系统上利用这些密钥安全地登录到您的AWS EC2实例。

## Linux系统下的登录方法

1. **确保您已经下载了`.pem`文件**，通常在创建EC2实例时提供。
   
2. **修改权限**：为了安全，应该限制对`.pem`文件的访问权限。
   ```bash
   chmod 400 your-key-pair.pem
   ```
   这里`your-key-pair.pem`替换为实际的`.pem`文件名。

3. **使用SSH登录**：
   ```bash
   ssh -i your-key-pair.pem ec2-user@your-instance-public-ip
   ```
   `ec2-user`通常是Amazon Linux AMI的默认用户，如果您使用的是Ubuntu，则可能是`ubuntu`，而`your-instance-public-ip`需要替换为您EC2实例的公共IP地址。

## Windows系统下的登录方法

Windows用户由于不直接支持`.pem`文件，可以采用以下步骤：

1. **转换`.pem`文件为PuTTY格式(.ppk)**:
    - 下载并安装[Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)和[PuTTYgen]。
    - 打开PuTTYgen，选择“Load”，然后浏览并选择您的`.pem`文件。 PuTTYgen会自动加载密钥。
    - 单击“Save private key”，保存成`.ppk`格式。

2. **使用PuTTY登录**:
    - 启动PuTTY，输入您的EC2实例的公网IP地址作为“Host Name”。
    - 在“Category”树中，导航至“Connection -> SSH -> Auth”。点击“Browse...”，找到并选择之前生成的`.ppk`文件。
    - 回到顶层菜单，点击“Session”，并保存此会话配置以供未来使用。
    - 最后，点击“Open”以启动SSH连接。

通过以上步骤，无论您使用的是Linux还是Windows系统，都可以顺利地使用`.pem`密钥来安全地登录您的AWS EC2虚拟机。记得始终遵循最佳安全实践，妥善保管您的私钥文件。

## 下载链接

[AWS虚拟机pem密钥使用指南分享](https://pan.quark.cn/s/7a06339b2bd3)