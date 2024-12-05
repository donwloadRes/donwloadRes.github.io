---
layout: post
title: "麒麟v10系统arm64架构自制openssh9.5p1的rpm包"
date:   2022-02-25
tags: [OpenSSH,p1,arm64,RPM,架构]
comments: true
author: admin
---
# 麒麟v10系统arm64架构自制openssh9.5p1的rpm包

## 资源描述

本仓库提供了一个适用于麒麟v10系统arm64架构的自制OpenSSH 9.5p1的RPM包。该RPM包理论上适用于所有arm64架构（aarch64）的系统。

### 系统信息
- 系统架构：arm64（aarch64）
- 内核版本：4.19.90-17.ky10.aarch64
- 系统类型：aarch64 GNU/Linux

### 使用说明
1. **升级前备份**：在升级OpenSSH之前，请务必备份以下文件和目录：
   - `/etc/ssh`
   - `/etc/pam.d`

2. **开启Telnet**：为了防止升级过程中出现SSH连接中断的情况，建议在升级前开启Telnet服务，以便在升级过程中能够通过Telnet进行远程操作。

3. **安装RPM包**：下载本仓库提供的RPM包，并使用以下命令进行安装：
   ```bash
   sudo rpm -ivh openssh-9.5p1-1.aarch64.rpm
   ```

4. **确认升级成功**：升级完成后，使用以下命令确认OpenSSH版本：
   ```bash
   ssh -V
   ```
   输出应为：`OpenSSH_9.5p1`。

5. **关闭Telnet**：确认OpenSSH升级成功且功能正常后，关闭Telnet服务。

### 注意事项
- 原系统中的OpenSSH版本为：`OpenSSH_7.8p1 OpenSSL 1.1.1d  10 Sep 2019`。
- 执行`yum update`后，OpenSSH版本为：`OpenSSH_8.2p1 OpenSSL 1.1.1f`。
- 本RPM包中的OpenSSH显示的OpenSSL版本为1.1.1f。如果系统中的OpenSSL版本与此不一致，安装后可能会影响`ssh -V`命令的版本显示，但不会影响OpenSSH的正常使用。

### 备注
- 本RPM包是基于麒麟v10系统arm64架构制作的，适用于相同架构的系统。
- 如果在其他系统上使用，请根据实际情况进行测试和调整。

---

希望本资源能够帮助您顺利升级OpenSSH，并确保系统的安全性和稳定性。如有任何问题，请随时联系。

## 下载链接

[麒麟v10系统arm64架构自制openssh9.5p1的rpm包](https://pan.quark.cn/s/1efdbdb522a2)