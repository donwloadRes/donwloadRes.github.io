---
layout: post
title: "Landsat 7 ETM影像条带修复ENVI补丁"
date:   2024-05-13
tags: [补丁,ENVI,条带,影像,Landsat]
comments: true
author: admin
---
# Landsat 7 ETM+影像条带修复ENVI补丁

## 简介

本资源文件提供了一个用于修复Landsat 7 ETM+影像条带的ENVI补丁。Landsat 7 ETM+卫星在2003年5月31日之后由于机载扫描行校正器(SLC)故障，导致获取的影像数据出现了条带丢失问题。该补丁旨在帮助用户修复这些条带，恢复影像的完整性。

## 使用方法

1. **下载补丁文件**：从本仓库下载所需的补丁文件。
2. **安装补丁**：
   - 将补丁文件放置到ENVI程序安装目录的`save_add`文件夹下。例如，在ENVI 4.7版本中，路径为`D:\Program Files\ITT\IDL71\products\envi47\save_add`。
3. **启动ENVI**：打开ENVI软件，补丁将自动加载。
4. **使用补丁**：
   - 在ENVI中，导航到`Basic Tools -> Preprocessing -> Data-Specific Utilities -> Landsat TM -> Landsat gapfill`。
   - 选择需要修复的影像文件，按照提示进行操作。

## 补丁类型

本资源文件包含两个常用的Landsat 7 ETM+影像条带修复补丁：

1. **landsat_gapfill.sav**：
   - 提供单文件条带修复和借助辅助文件的条带修复两类方法。
   - 下载地址：[landsat_gapfill.sav](此处省略下载地址)

2. **tm_destripe.sav**：
   - 使用地址：`Basic Tools -> Preprocessing -> General Purpose Utilities -> TM6去条带(改进)`。
   - 下载地址：[tm_destripe.sav](此处省略下载地址)

## 注意事项

- 确保补丁文件放置在正确的目录下，否则可能无法正常使用。
- 在使用补丁修复影像时，建议备份原始影像文件，以防数据丢失。

## 参考资料

有关该补丁的更多详细信息和使用教程，请参考[Landsat 7 ETM+影像条带修复ENVI补丁](此处省略文章链接)。

## 贡献

如果您有任何改进建议或发现了问题，欢迎提交Issue或Pull Request。

## 许可证

本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处声明。

## 下载链接

[Landsat7ETM影像条带修复ENVI补丁分享](https://pan.quark.cn/s/c5466adfdbdc)