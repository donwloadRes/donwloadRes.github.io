---
layout: post
title: "WPS for Linux 中文界面设置指南"
date:   2024-03-19
tags: [WPS,Linux,中文,语言包,mui]
comments: true
author: admin
---
# WPS for Linux 中文界面设置指南

本仓库提供了一个资源文件，用于将WPS for Linux的界面语言从默认的英文切换为中文。由于WPS for Linux默认情况下可能没有提供语言切换的图标或选项，因此本资源文件提供了一种通过命令行替换语言包的方法。

## 使用方法

1. **下载WPS for Linux**：
   首先，从WPS官方网站下载适用于Linux的WPS Office安装包。

2. **删除官方自带语言包**：
   进入WPS的安装目录，通常位于 `/opt/kingsoft/wps-office/office6/mui`，删除该目录下的所有文件和文件夹。

   ```bash
   cd /opt/kingsoft/wps-office/office6/mui
   rm -rf *
   ```

3. **下载中文汉化包**：
   从本仓库下载中文汉化包，并解压到本地。

4. **替换原语言包**：
   将解压后的 `mui` 文件夹复制到WPS的安装目录下。

   ```bash
   sudo cp -r mui /opt/kingsoft/wps-office/office6/
   ```

5. **确认替换**：
   确认替换成功后，重新启动WPS for Linux，界面语言应已切换为中文。

## 注意事项

- 请确保在执行替换操作前备份原有语言包，以防出现问题时可以恢复。
- 本方法适用于大多数Linux发行版，但具体路径可能因系统不同而有所差异。

## 贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交Issue或Pull Request。

## 许可证

本资源文件遵循MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[WPSforLinux中文界面设置指南](https://pan.quark.cn/s/db8028363ccb)