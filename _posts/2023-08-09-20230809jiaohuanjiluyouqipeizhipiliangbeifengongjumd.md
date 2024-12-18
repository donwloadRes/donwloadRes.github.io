---
layout: post
title: "交换机路由器配置批量备份工具"
date:   2023-08-06
tags: [备份,日志,批量,路由器,多线程]
comments: true
author: admin
---
# 交换机路由器配置批量备份工具

## 简介
本仓库提供了一个强大的工具，用于通过SSH和Telnet协议批量获取交换机和路由器的配置日志。该工具不仅支持前台版和后台版的批量自动备份配置，还能自动删除过期的日志文件，并且支持多线程运行，极大地提高了备份效率。

## 功能特点
- **批量备份**：支持通过SSH和Telnet协议批量获取交换机和路由器的配置日志。
- **自动备份**：提供前台版和后台版两种模式，满足不同场景下的自动备份需求。
- **自动清理**：自动删除过期的日志文件，保持系统整洁。
- **多线程支持**：支持多线程运行，大幅提升备份速度。
- **版本更新**：当前版本为1.6，持续优化和更新中。

## 使用说明
1. **安装与配置**：下载并解压工具包，根据提供的配置文件模板进行相关参数的设置。
2. **运行工具**：根据需求选择前台版或后台版运行工具，启动批量备份任务。
3. **查看日志**：备份完成后，可以在指定目录下查看备份的配置日志文件。
4. **自动清理**：工具会自动删除过期的日志文件，无需手动干预。

## 注意事项
- 请确保交换机和路由器的SSH/Telnet服务已开启，并且具备相应的访问权限。
- 在多线程运行时，请根据设备性能合理设置线程数，避免资源占用过高。
- 定期检查工具的版本更新，以获取最新的功能和优化。

## 反馈与支持
如果在使用过程中遇到任何问题或有任何建议，欢迎通过仓库的Issues功能进行反馈。我们将尽快回复并提供支持。

感谢您的使用！

## 下载链接

[交换机路由器配置批量备份工具](https://pan.quark.cn/s/186d39907726)