---
layout: post
title: "彻底删除 MySQL 和 MySQL Connector Net 的详细指南"
date:   2021-11-01
tags: [MySQL,卸载,注册表,Connector,Net]
comments: true
author: admin
---
# 彻底删除 MySQL 和 MySQL Connector Net 的详细指南

本文详细介绍了如何彻底删除 MySQL 和 MySQL Connector Net，包括卸载不掉或不能更新的问题。文章涵盖了停止服务、删除相关文件夹、清理注册表以及处理无法卸载的 MySQL Connector Net 问题。

## 主要步骤

1. **卸载原有的 MySQL 软件**
   - 先停掉 MySQL 的服务：右键我的电脑找到管理。
   - 在管理面板中找到服务，然后禁用掉所有 MySQL 的服务。
   - 在计算机的控制面板中找到卸载程序，将所有 MySQL 有关程序全部卸载。

2. **删除跟原来的 MySQL 有关的数据（文件夹）**
   - 删除 MySQL 的安装路径的 MySQL 文件，默认为两种路径：
     - C:\Program Files (x86)\MySQL 或 C:\Program Files\MySQL
     - C:\ProgramData\MySQL（ProgramData 文件夹一般是隐藏的）

3. **清理注册表**
   - 按 window+R 打开运行，输入 regedit 打开注册表。
   - 删除以下注册表文件夹：
     - HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\Eventlog\Application\MySQL
     - HKEY_LOCAL_MACHINE\SYSTEM\ControlSet002\Services\Eventlog\Application\MySQL
     - HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Eventlog\Application\MySQL

4. **处理无法卸载的 MySQL Connector Net 问题**
   - 使用微软疑难解答工具来解决无法卸载的问题。
   - 下载并运行疑难解答工具，选择卸载，然后找到需要卸载的选项（即 MySQL Connector Net），然后等待。

## 注意事项

- 确保所有 MySQL 相关服务和程序都已停止和卸载。
- 删除文件夹时注意检查隐藏文件夹。
- 清理注册表时要小心，避免误删其他重要注册表项。

通过以上步骤，您可以彻底删除 MySQL 和 MySQL Connector Net，解决卸载不掉或不能更新的问题。

## 下载链接

[彻底删除MySQL和MySQLConnectorNet的详细指南](https://pan.quark.cn/s/b2ba13a557df)