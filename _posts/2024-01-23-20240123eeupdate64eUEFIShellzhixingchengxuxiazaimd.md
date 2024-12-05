---
layout: post
title: "eeupdate64e UEFI Shell 执行程序下载"
date:   2024-09-30
tags: [MAC,eeupdate64e,UEFI,Shell,NIC]
comments: true
author: admin
---
# eeupdate64e UEFI Shell 执行程序下载

## 资源文件介绍

本仓库提供了一个名为 `eeupdate64e.zip` 的资源文件下载。该文件是一个在 UEFI Shell 下执行的程序，主要用于更新网络接口卡（NIC）的 MAC 地址。

## 使用说明

1. **下载与解压缩**  
   下载 `eeupdate64e.zip` 文件后，请先将其解压缩。解压缩后，您将获得 `eeupdate64e.efi` 文件。

2. **进入 UEFI Shell**  
   在 UEFI Shell 环境下，导航到解压缩后的文件所在目录。

3. **执行命令**  
   在 UEFI Shell 中执行以下命令来更新 NIC 的 MAC 地址：
   ```
   eeupdate64e.efi /NIC=1 /MAC=xxxxxxxxx
   ```
   其中，`xxxxxxxxx` 是您希望设置的新 MAC 地址。

4. **注意事项**  
   - 某些主板可能需要关闭 BIOS 写保护才能成功写入新的 MAC 地址。
   - 请务必参考主板的 BIOS 升级指导书，以确保操作的安全性和正确性。

## 其他说明

- 本资源文件仅供学习和研究使用，请勿用于非法用途。
- 如果在使用过程中遇到任何问题，请参考相关文档或联系技术支持。

希望这个资源文件能帮助您顺利完成 NIC 的 MAC 地址更新。

## 下载链接

[eeupdate64eUEFIShell执行程序下载](https://pan.quark.cn/s/235b59a6fced)