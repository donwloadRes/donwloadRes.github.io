---
layout: post
title: "SPI Flash W25Q128 驱动函数"
date:   2023-05-13
tags: [擦除,写入,SPI,Page,多页]
comments: true
author: admin
---
# SPI Flash W25Q128 驱动函数

## 描述
本仓库提供了一个针对 W25Q128 SPI Flash 的驱动函数库。该库包含了多个常用的操作函数，如块擦除、扇区擦除、页写入、多页写入、页读取和多页读取等。所有函数均已调试通过，可以直接在项目中使用。

## 功能列表
- **块擦除 (Block Erase)**: 擦除指定块的数据。
- **扇区擦除 (Sector Erase)**: 擦除指定扇区的数据。
- **页写入 (Page Write)**: 将数据写入指定页。
- **多页写入 (Multi-Page Write)**: 将数据连续写入多个页。
- **页读取 (Page Read)**: 从指定页读取数据。
- **多页读取 (Multi-Page Read)**: 从多个页连续读取数据。

## 使用说明
1. **下载资源**: 下载本仓库中的资源文件。
2. **集成到项目**: 将下载的驱动函数库集成到你的项目中。
3. **调用函数**: 根据需要调用相应的函数进行 SPI Flash 的操作。

## 注意事项
- 在使用前请确保硬件连接正确，SPI 接口配置无误。
- 在进行擦除或写入操作时，请注意数据的完整性和一致性。

## 贡献
如果你有任何改进建议或发现了问题，欢迎提交 Issue 或 Pull Request。

## 许可证
本项目采用 MIT 许可证，详情请参阅 LICENSE 文件。

## 下载链接

[SPIFlashW25Q128驱动函数](https://pan.quark.cn/s/14bea84d868c)