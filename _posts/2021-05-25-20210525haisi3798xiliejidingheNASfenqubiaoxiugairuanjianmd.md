---
layout: post
title: "海思3798系列机顶盒NAS分区表修改软件"
date:   2020-01-10
tags: [分区,backup,gz,分区表,挂载]
comments: true
author: admin
---
# 海思3798系列机顶盒NAS分区表修改软件

## 简介

本仓库提供了一个名为 `makebootargs.exe` 的资源文件，该软件专为海思3798系列机顶盒设计，主要用于修改机顶盒的分区表。通过该软件，用户可以灵活调整分区大小，修改启动项，甚至设置机顶盒从U盘或TF卡启动。

## 功能特点

- **分区表修改**：支持对海思3798系列机顶盒的分区表进行修改，包括分区大小的调整。
- **启动项设置**：可以修改机顶盒的启动项，支持从U盘、TF卡等多种设备启动。
- **系统恢复**：提供了从 `/dev/mmcblk0p8` 分区中提取重置恢复系统文件 `backup.gz` 的方法，方便用户进行系统恢复操作。

## 使用方法

### 1. 提取重置恢复系统文件

1. **创建挂载点**：首先创建一个用于挂载的分区目录。
   ```bash
   mkdir /mnt/mm8
   ```

2. **挂载分区**：将分区挂载到创建的目录中，并查看挂载目录中的重置恢复系统文件名称。
   ```bash
   mount /dev/mmcblk0p8 /mnt/mm8
   ls /mnt/mm8
   ```

3. **拷贝文件**：将 `backup.gz`（可能是 `backup-32.gz` 或 `backup-64.gz`）拷贝到你的系统任意分区。
   ```bash
   cp /mnt/mm8/backup-32.gz /home/ubuntu
   ```

4. **解压文件**：使用 `gunzip` 命令解压 `backup.gz` 文件。
   ```bash
   cd /home/ubuntu
   gunzip backup-32.gz
   ```

### 2. 修改U盘分区

1. **卸载挂载分区**：如果U盘分区被自动挂载，则先卸载挂载分区。
   ```bash
   lsblk -m -a -f
   umount /dev/sda1
   ```

2. **分区操作**：使用 `fdisk` 命令对U盘进行分区操作（具体分区过程省略）。
   ```bash
   fdisk /dev/sda
   ```

## 注意事项

- 在进行分区表修改和启动项设置时，请务必谨慎操作，避免误操作导致数据丢失或系统无法启动。
- 建议在操作前备份重要数据，并确保对操作步骤有充分理解。

## 支持与反馈

如果在使用过程中遇到任何问题或有任何建议，欢迎通过仓库的 Issues 功能进行反馈。我们将尽力提供帮助。

## 下载链接

[海思3798系列机顶盒NAS分区表修改软件](https://pan.quark.cn/s/9d59ec94220b)