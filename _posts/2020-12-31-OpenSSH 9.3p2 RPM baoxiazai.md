---
layout: post
title: "OpenSSH 9.3p2 RPM 包下载"
date:   2022-05-17
tags: [OpenSSH,9.3,p2,RPM,openEuler]
comments: true
author: admin
---
# OpenSSH 9.3p2 RPM 包下载

本仓库提供了一个适用于 openEuler 20.03 (LTS-SP2) Linux 环境的 OpenSSH 9.3p2 版本的 RPM 包下载。该 RPM 包旨在帮助用户修复 OpenSSH 低版本中的漏洞。

## 资源文件信息

- **文件名**: openssh-9.3p2-1.x86_64.rpm
- **描述**: 基于 openEuler 20.03 (LTS-SP2) Linux 环境制作的 OpenSSH 9.3p2 版本的 RPM 包，适用于 OpenSSH 低版本漏洞修复。

## 使用说明

1. **下载文件**: 点击仓库中的 `openssh-9.3p2-1.x86_64.rpm` 文件进行下载。
2. **安装 RPM 包**: 在 openEuler 20.03 (LTS-SP2) 系统中，使用以下命令安装 RPM 包：
   ```bash
   sudo rpm -ivh openssh-9.3p2-1.x86_64.rpm
   ```
3. **验证安装**: 安装完成后，可以使用以下命令验证 OpenSSH 版本：
   ```bash
   ssh -V
   ```
   输出应显示 `OpenSSH_9.3p2`。

## 注意事项

- 请确保在安装前备份重要数据，以防意外情况发生。
- 该 RPM 包仅适用于 openEuler 20.03 (LTS-SP2) 系统，其他系统版本可能无法正常使用。

## 联系我们

如有任何问题或建议，请通过仓库的 Issues 页面进行反馈。

## 下载链接

[OpenSSH9.3p2RPM包下载](https://pan.quark.cn/s/06d825f4efb5)