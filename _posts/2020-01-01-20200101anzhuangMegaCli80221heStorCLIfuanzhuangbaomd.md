---
layout: post
title: "安装MegaCli-8.02.21和StorCLI(附安装包)"
date:   2021-08-10
tags: [MegaCli,StorCLI,安装,RAID,rpm]
comments: true
author: admin
---
# 安装MegaCli-8.02.21和StorCLI(附安装包)

## 文档简介

本文档旨在为Linux系统管理员提供详细步骤，用于安装MegaCli和StorCLI工具。这些工具对于管理和监控基于LSI和Broadcom的RAID控制器至关重要，允许用户进行RAID配置、查询驱动器状态、监控健康情况等操作。下面的指南基于[CSDN博客](https://blog.csdn.net/qq_26884501/article/details/112307407)上的分享，简化了下载和安装流程，确保新手也能顺利完成安装。

## 下载资源

- **MegaCli-8.02.21**: 提供稳定版本的MegaCli工具包。
- **StorCLI**: 作为MegaCli的继承者，提供了更统一的跨平台RAID管理体验。

请访问提供的链接获取最新版本的安装包，提取码分别为2fe1（MegaCli）和tgvo（StorCLI），以确保与您的系统兼容性。

## 安装步骤

### MegaCli 安装

1. **下载并解压**：首先下载MegaCli的tar.gz文件并解压。
2. **安装依赖**：运行以下命令安装必需的库`rpm -ivh Lib_Utils-1.00-09.noarch.rpm`。
3. **继续安装MegaCli**：接着安装MegaCli RPM包`rpm -ivh MegaCli-8.02.21-1.noarch.rpm`。
4. **环境配置**：确保MegaCli命令全局可访问，通过命令`ln -s /opt/MegaRAID/MegaCli/MegaCli64 /usr/local/bin/MegaCli`添加软链接。
5. **验证安装**：使用命令`MegaCli -v`检查安装是否成功。

### StorCLI 安装

1. **解压StorCLI包**。
2. **安装RPM**：使用`rpm -ivh <StorCLI-x.xx-x.noarch.rpm>`命令安装StorCLI。
3. **创建符号链接**，确保命令在系统路径中可用，分别向`/bin`和`/sbin`添加软链接。

### 使用示例

安装完成后，您可以利用以下命令进行基本的RAID管理和监控：

- 查询MegaCli版本：`MegaCli -v`
- 查看所有RAID控制器信息：`MegaCli -AdpAllInfo -aALL`
- 对于StorCLI，常用的命令如：`/opt/MegaRAID/storcli/storcli64 /call show all`。

## 注意事项

- 在进行任何RAID配置变更之前，请确保数据已备份，以防不可预料的数据丢失。
- 根据具体的Linux发行版，可能需要调整安装命令或处理依赖关系。
- 定期检查官方更新，以获得新功能和安全修复。

通过遵循上述步骤，您能够有效地在您的Linux环境中部署这两款强大的RAID管理工具。记得，正确地管理和监控RAID阵列对于维护数据的完整性和系统稳定性至关重要。

## 下载链接

[安装MegaCli-8.02.21和StorCLI附安装包分享](https://pan.quark.cn/s/856c687761ed)