---
layout: post
title: "联想Thinklife SSD ST600 120G变satafirms11修复步骤亲测心得20231006"
date:   2024-09-13
tags: [硬盘,固态,修复,固件,步骤]
comments: true
author: admin
---
# 联想Thinklife SSD ST600 120G变satafirms11修复步骤（亲测心得2023.10.06）

## 简介

本资源文件提供了联想Thinklife SSD ST600 120G固态硬盘变satafirms11状态的修复步骤。该修复步骤经过亲测，适用于大多数采用PHISON-PS3111-S11-13群联主控的固态硬盘。修复过程中需要注意，重新修复后的硬盘数据将无法找回，因此仅适用于数据不重要的硬盘。

## 所需工具及文件资源

1. 查看固态硬盘芯片的Phison flash id
2. 群联固态解锁软件Unlocker
3. 修复固态岛软件repairPhison
4. S11 firmware flasher v2
5. 自己硬盘对应的固件包

以上所需工具及文件资源在群联PHISON S11的官方固态资源库中基本可以找到，部分型号的固件包可能需要用户自行另找。

## 具体步骤

1. **连接固态硬盘**：将需要修复的固态SSD连接至PC端的SATA接口上，通过U盘启动进入winPE系统下。
2. **获取硬盘固件详细信息**：下载并运行Phison flash id工具，获取固态硬盘的固件详细信息。
3. **下载对应固件**：根据获取的固件信息，下载对应的硬盘固件。
4. **解锁固态硬盘**：使用Phison S11 unlocker工具解锁固态硬盘。
5. **修复或重新刷写固件**：使用repairS11修复固态或用Phison S11 firmware flasher v2重新刷写固件。
6. **重启电脑**：修复成功后，关闭电脑断电30秒，再开机进入BIOS，固态硬盘应恢复正常显示。

## 注意事项

- 修复过程中，硬盘数据将无法找回，请确保数据不重要时再进行修复。
- 修复成功后，建议通过Windows操作系统对固态硬盘进行重新分区。

## 参考资料

本修复步骤参考了CSDN博客文章《联想Thinklife SSD（固态硬盘） ST600 120G变satafirms11修复步骤（亲测心得2023.10.06）》，详细步骤和工具使用方法可参考该文章。

## 致谢

感谢CSDN博主元气满满@每一天提供的详细修复步骤和工具资源。

## 下载链接

[联想ThinklifeSSDST600120G变satafirms11修复步骤亲测心得2023.10.06](https://pan.quark.cn/s/39f0a3ca7434)