---
layout: post
title: "Centos 72747678 升级 OpenSSH 96 方法和详解脚本一键升级
date   20230714
tags sshdetcsshconfig升级
comments true
author admin

 Centos 72747678 升级 OpenSSH 96 方法和详解脚本一键升级

本仓库提供了一个用于将 CentOS 727476 和 78 系统中的 OpenSSH 升级到 96 版本的脚本该脚本支持一键升级并提供了必要的备份和恢复机制以确保在升级过程中出现问题时能够快速恢复

 脚本内容及使用方法

以下是脚本的内容及详细说明

bash
binbash

 备份 sshdconfig 配置文件及 sshdpam 文件
echo 备份 sshdconfig 配置文件及 sshdpam 文件
cp etcsshsshdconfig etcsshsshdconfig74p1bak
cp etcpamdsshd etcsshsshd74p1pambak

 升级 OpenSSH
echo 升级 OpenSSH
rpm Uvh opensshrpm

 设置权限
echo 设置权限
chmod 0600 etcsshsshhostkeys

 修改 sshdconfig 配置文件
echo 修改 sshdconfig 配置文件
sed i sUsePAM noUsePAM yesg etcsshsshdconfig
sed i sPermitRootLogin prohibitpasswordPermitRootLogin yesg etcsshsshdconfig

 重启 sshd 服务
echo 重启 sshd 服务"
date:   2023-07-14
tags: [sshd,etc,ssh,config,升级]
comments: true
author: admin
---
# Centos 7.2/7.4/7.6/7.8 升级 OpenSSH 9.6 方法和详解（脚本一键升级）

本仓库提供了一个用于将 CentOS 7.2、7.4、7.6 和 7.8 系统中的 OpenSSH 升级到 9.6 版本的脚本。该脚本支持一键升级，并提供了必要的备份和恢复机制，以确保在升级过程中出现问题时能够快速恢复。

## 脚本内容及使用方法

以下是脚本的内容及详细说明：

```bash
#!/bin/bash

# 备份 sshd_config 配置文件及 sshd_pam 文件
echo "备份 sshd_config 配置文件及 sshd_pam 文件"
cp /etc/ssh/sshd_config /etc/ssh/sshd_config_7.4p1_bak
cp /etc/pam.d/sshd /etc/ssh/sshd_7.4p1_pam_bak

# 升级 OpenSSH
echo "升级 OpenSSH"
rpm -Uvh openssh-*.rpm

# 设置权限
echo "设置权限"
chmod 0600 /etc/ssh/ssh_host_*_keys

# 修改 sshd_config 配置文件
echo "修改 sshd_config 配置文件"
sed -i 's/#UsePAM no/UsePAM yes/g' /etc/ssh/sshd_config
sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config

# 重启 sshd 服务
echo "重启 sshd 服务"
systemctl restart sshd
```

### 注意事项

1. **备份重要文件**：脚本会自动备份 `/etc/ssh/sshd_config` 和 `/etc/pam.d/sshd` 文件，以防止升级过程中出现问题。
2. **恢复机制**：如果升级后无法通过 SSH 登录，可以使用以下命令恢复 `/etc/pam.d/sshd` 文件：
   ```bash
   cp /etc/ssh/sshd_7.4p1_pam_bak /etc/pam.d/sshd
   ```
3. **权限设置**：脚本会自动设置 `/etc/ssh/ssh_host_*_keys` 文件的权限为 `0600`，以确保安全性。
4. **配置修改**：脚本会自动修改 `/etc/ssh/sshd_config` 文件中的 `UsePAM` 和 `PermitRootLogin` 配置项。

## 使用步骤

1. **下载脚本**：将上述脚本内容保存为 `upgrade_openssh.sh` 文件。
2. **准备 RPM 包**：确保 `openssh-*.rpm` 文件已下载并放置在当前目录中。
3. **执行脚本**：在终端中执行以下命令：
   ```bash
   bash upgrade_openssh.sh
   ```
4. **验证升级**：升级完成后，使用 `ssh -V` 命令验证 OpenSSH 版本是否已成功升级到 9.6。

## 常见问题及解决方法

- **无法登录 SSH**：如果升级后无法通过 SSH 登录，请按照上述恢复机制进行恢复操作。
- **权限问题**：确保 `/etc/ssh/ssh_host_*_keys` 文件的权限为 `0600`，否则可能会导致 SSH 服务无法启动。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 下载链接

[Centos7.27.47.67.8升级OpenSSH9.6方法和详解脚本一键升级](https://pan.quark.cn/s/fd14a3aa08e4)