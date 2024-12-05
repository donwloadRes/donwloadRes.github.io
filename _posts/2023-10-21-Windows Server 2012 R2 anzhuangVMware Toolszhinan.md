---
layout: post
title: "Windows Server 2012 R2 安装VMware Tools指南"
date:   2021-10-07
tags: [虚拟机,安装,VMware,Tools,Windows]
comments: true
author: admin
---
# Windows Server 2012 R2 安装VMware Tools指南

本资源文件提供了在Windows Server 2012 R2虚拟机中安装VMware Tools的详细步骤，帮助用户实现物理机与虚拟机之间的文件互传。通过安装VMware Tools，用户可以轻松地将文件从物理机拖拽到虚拟机中，大大简化了文件传输的过程。

## 安装步骤

1. **打开虚拟机**：启动VMware Workstation Pro，并打开Windows Server 2012 R2虚拟机。

2. **安装VMware Tools**：
   - 在虚拟机菜单中，点击“虚拟机”选项。
   - 选择“安装VMware Tools”。

3. **运行安装程序**：
   - 在虚拟机中打开“运行”对话框。
   - 输入命令 `D:\setup.exe` 并点击“确定”。

4. **安装更新程序**：
   - 如果安装过程中提示缺少更新程序，请下载并安装以下两个更新程序：
     - KB2975061
     - KB2919355
   - 安装顺序：先安装KB2975061，再安装KB2919355。

5. **重启虚拟机**：安装完成后，重启虚拟机。

6. **完成安装**：重启后，VMware Tools安装完成。此时，用户可以将物理机上的文件直接拖拽到虚拟机中，实现文件互传。

## 注意事项

- 确保虚拟机和物理机之间的网络连接正常。
- 安装过程中可能需要管理员权限。
- 安装完成后，建议重启虚拟机以确保VMware Tools正常运行。

通过以上步骤，用户可以顺利在Windows Server 2012 R2虚拟机中安装VMware Tools，并实现物理机与虚拟机之间的文件互传。

## 下载链接

[WindowsServer2012R2安装VMwareTools指南](https://pan.quark.cn/s/1185e6741df2)