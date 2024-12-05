---
layout: post
title: "2020版FME安装与激活指南"
date:   2023-09-26
tags: [FME,安装,License,文件,2020]
comments: true
author: admin
---
# 2020版FME安装与激活指南

本指南提供FME（特征操纵引擎）2020版的安装和激活的详细步骤。FME是加拿大Safe Software公司开发的地理空间数据转换处理**资源**，广泛应用于地理信息系统（GIS）领域。

## 概述

FME是一个全面的空间ETL解决方案，基于OpenGIS组织提出的数据转换新理念“语义转换”。它提供数据重构功能，实现超过250种不同空间数据格式（模型）之间的转换，提供快速、高质量、多用途的数据转换应用，高效且可靠。

## 安装流程

1. **下载安装包**：
   - 下载FME2020（64位）安装包，提取码：s7h8。

2. **安装FlexNET Floating License Manager**：
   - 双击`fme-flexnet-win-x64.msi`进行安装，生成txt文件，将文件中的HostName及HostID粘贴进`dummy.txt`文件中。
   - 笔记本电脑会生成两个HostID，用引号和空格隔开，只需要粘贴一个。台式机生成一个，在后面空一格加上端口号（27001~27009），避免与ArcGIS冲突。

3. **生成License文件**：
   - 双击`makekey.bat`生成`safe.lic`文件，将其放入FlexServer目录。

4. **启动License Server**：
   - 双击`Imtools.exe`文件，切换到“Start/Stop/Reread”选项卡，点击“Start Server”读取license，显示启动成功即可。
   - 如果启动失败，可能是`safe.lic`文件有误，检查内容和大小（超过5KB需要重新生成）。然后停止Server并重新读取License。

5. **安装FME Desktop**：
   - 安装`fme-desktop-2020.0-b20200-win-x64.msi`，完成后打开FME workbench，安装完成。

6. **安装汉化版（可选）**：
   - 点击`FME_2020_Chinese_x64.msi`安装汉化版。

## 常见问题

- **系统兼容性**：确保操作系统与FME版本兼容，旧版本可能不支持新操作系统。
- **License问题**：无法连接license时，重新生成`safe.lic`文件并按照步骤重新读取license。
- **ArcGIS冲突**：ArcGIS处理大数据时频繁报错，可能是因为与FME位数不兼容。建议重装FME解决问题。

## 总结

FME提供了强大的空间数据转换能力，在Arcgis处理受限时，可作为补充工具。本指南详细阐述了FME2020的安装和激活步骤，帮助用户顺利安装和使用FME，进行高效的数据转换。

## 下载链接

[2020版FME安装与激活指南](https://pan.quark.cn/s/192d0cc21560)