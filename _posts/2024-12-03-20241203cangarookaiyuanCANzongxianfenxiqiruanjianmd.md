---
layout: post
title: "cangaroo 开源CAN总线分析器软件"
date:   2024-08-09
tags: [总线,Cangaroo,开源,dev,软件]
comments: true
author: admin
---
# cangaroo 开源CAN总线分析器软件

袋鼠(Cangaroo)是一款专为CAN总线设计的开源分析工具，由Hubert Denkmair创建。该软件致力于简化CAN总线数据的监控、分析和理解过程，特别适合嵌入式系统开发者、汽车电子工程师以及其他对CAN协议有需求的用户。

## 系统要求与安装指南

### 在Linux环境下的安装步骤：
1. **确保环境**：推荐在Ubuntu 16.04上操作。
2. **安装必要软件包**：打开终端并执行以下命令以安装必要的开发工具和依赖项。
   ```
   sudo apt-get install build-essential git qt5-qmake qtbase5-dev libnl-3-dev libnl-route-3-dev
   ```
3. **项目克隆与编译**：
   - 使用git克隆Cangaroo项目到本地。
   - 进入项目目录，执行`qmake -qt=qt5`准备编译环境。
   - 随后输入`make`进行编译。

### 在Windows环境下的搭建说明：
- 对于Windows用户，推荐使用Qt Creator（社区版已足够）作为开发环境，因为它包含了大部分所需的开发工具。
- **PCAN库的配置**：需要额外获取PCAN基本API库，并将其解压缩至项目的特定路径，即`src/driver/PeakCanDriver/pcan-basic-api`。
- 确保在运行Cangaroo之前，Windows系统路径中包含`PCANBasic.dll`。通常，可以从`pcan-basic-api/Win32`目录中的“普通”32位版本找到此DLL文件，并将其放置在可执行文件同一目录下。

## 注意事项
- 对于不同操作系统，确保遵循相应的开发和配置指导，以避免兼容性问题。
- 软件的持续更新和改进可能要求查阅最新的文档或项目仓库信息。
- 开发与维护开源软件需要社区的支持，鼓励贡献代码、报告问题和提出建议。

通过以上步骤，您可以成功地设置和使用Cangaroo进行CAN总线的数据分析工作，助力您的项目开发和故障排查。

## 下载链接

[cangaroo开源CAN总线分析器软件](https://pan.quark.cn/s/ff1cb6f63e05)