---
layout: post
title: "国标GBT27930报文解析工具"
date:   2024-02-07
tags: [报文,文件,工具,GBT27930,Git]
comments: true
author: admin
---
# 国标GBT27930报文解析工具

## 简介

本仓库提供了一个用于解析国标GBT27930报文的工具。该工具可以通过宏定义进行修改，以适应多种工具生成的CAN报文。工具使用awk脚本实现，适用于Windows系统上的Git Bash环境。

## 使用方法

1. **下载工具**：
   - 克隆或下载本仓库中的脚本文件。

2. **准备输入文件**：
   - 确保你有一个包含CAN报文的输入文件。

3. **运行脚本**：
   - 在Git Bash中运行以下命令：
     ```bash
     ./parse_27930_for_ZCANPRO.sh [输入文件路径] > [输出文件路径]
     ```
   - 例如：
     ```bash
     ./parse_27930_for_ZCANPRO.sh input.log > output.log
     ```

4. **查看输出**：
   - 解析后的报文将输出到指定的输出文件中。

## 注意事项

- 确保在Windows系统上安装了Git Bash，以便能够运行bash脚本。
- 输入文件路径和输出文件路径可以是相对路径或绝对路径。

## 贡献

欢迎提交问题和改进建议。如果你有更好的实现方式或功能扩展，欢迎提交Pull Request。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 下载链接

[国标GBT27930报文解析工具](https://pan.quark.cn/s/6b72c1f4e796)