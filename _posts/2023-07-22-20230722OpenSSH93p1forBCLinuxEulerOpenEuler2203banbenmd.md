---
layout: post
title: "OpenSSH 93p1 for BCLinux Euler  OpenEuler 2203 版本"
date:   2022-11-08
tags: [OpenSSH,9.3,p1,sshd,SSH]
comments: true
author: admin
---
# OpenSSH 9.3p1 for BCLinux Euler & OpenEuler 22.03 版本

---

**资源说明：**

本仓库提供了OpenSSH 9.3p1的安装包，专为BCLinux Euler和OpenEuler 22.03操作系统版本设计。此更新旨在增强系统的安全性和兼容性。通过本资源，用户可以方便地升级系统中的OpenSSH客户端与服务器组件至最新稳定版。

**升级步骤：**

1. **备份原配置**：首先，确保您的原有SSH配置得到妥善保存，执行命令`cp /etc/ssh/sshd_config /etc/ssh/sshd_config.20230509`来创建备份。

2. **本地安装新版本**：利用以下yum命令进行升级：
   ```
   yum localinstall -y openssh-clients-9.3p1-1.x86_64.rpm openssh-9.3p1-1.x86_64.rpm openssh-server-9.3p1-1.x86_64.rpm
   ```

3. **解决升级问题**：在某些情况下，升级过程中可能会遇到第159行配置相关的问题，具体表现为与GSSAPI相关的Kex Algorithms不兼容。您需要手动编辑`/etc/ssh/sshd_config`，找到如下行并将其注释：
   ```
   #GSSAPIKexAlgorithms gss-group14-sha256,gss-group16-sha512,gss-curve25519-sha256
   ```
   使用`#`符号在行首添加注释以禁用这一项。

4. **验证配置**：如果需要验证修改的行数是否正确，可以通过`cat -n /etc/ssh/sshd_config | grep GSSAPIKexAlgorithms`来定位相关配置的位置和内容。

5. **重启SSH服务**：完成上述步骤后，务必重启SSH服务以使更改生效：
   ```
   systemctl restart sshd
   ```

**注意事项：**
- 在执行任何升级操作之前，请确保对重要数据进行了备份。
- 监控系统日志以确认SSH服务启动无误，并保持系统的稳定性。

这个过程确保了向新OpenSSH版本平滑过渡，同时解决了可能影响服务运行的潜在问题。如果您在升级过程中遇到其他问题，建议查阅OpenSSH官方文档或寻求社区支持。

## 下载链接

[OpenSSH9.3p1forBCLinuxEulerOpenEuler22.03版本](https://pan.quark.cn/s/a9554bfe6df4)