---
layout: post
title: "Quartus II 13.0下载安装与Hello World教程"
date:   2023-09-06
tags: [Quartus,II,13.0,安装,仿真]
comments: true
author: admin
---
# Quartus II 13.0下载安装与Hello World教程

本仓库提供了Quartus II 13.0完整版的下载资源及其详尽的安装指南，帮助您顺利搭建FPGA开发环境。Quartus II是一款由Altera公司开发的业界领先的FPGA设计软件，广泛应用于数字逻辑电路的设计与实现。无论您是初学者还是有经验的开发者，这份教程都将引导您从下载到完成第一个“Hello World”项目的全过程。

## 安装步骤摘要：

### 1. **下载软件**
- 软件包可通过百度云等途径获得，提取码为ac9r。
- 其他辅助资料亦可在指定论坛帖子中查找。

### 2. **安装指南**
1. 解压缩下载的安装包，并双击进入“Quartus-13.0_0_156-windows”目录。
2. 使用管理员权限运行`setup.bat`开始安装。
3. 同意许可协议，选择安装路径（建议非默认，例如D:\software\altera\13.0），并选择必要的组件安装，包括主程序、仿真工具Modelsim-Altera的初学者版本等。
4. 安装完成后，首次运行软件会提示许可证安装，此时需手动处理许可证文件。

### 3. **许可证设置**
- 使用提供的“Quartus_13.0_SP1_x64许可工具”，以管理员身份运行，生成个性化license文件，并修改以匹配您的网卡号。
- 保存许可证文件至不易被误删的安全位置，并确保路径正确无误。
- 在Quartus II中指向该许可证文件，完成破解。

### 4. **器件库安装**
- 关闭Quartus II，运行Device Install程序，确保安装路径与软件路径一致，安装相应的器件库。

### 5. **创建Hello World项目**
1. 启动Quartus II，通过“File”->“New Project Wizard”开始新项目。
2. 设定项目路径、名称，以及顶层实体名。
3. 选择仿真工具为ModelSim-Altera，语言设为Verilog HDL。
4. 编写简单的Verilog HelloWorld代码，进行综合、仿真。

### 6. **编译与仿真**
- 分别进行综合、RTL视图检查、以及功能仿真。
- 确保仿真无误，输出显示“Hello World”。

## 注意事项：
- 在处理许可证文件时，确保每个步骤精确执行，特别是网卡号的正确替换。
- 硬件环境与软件兼容性，请根据个人电脑配置选择合适版本。
- 跟随具体步骤操作，避免遗漏导致安装失败。

通过遵循上述步骤，您可以成功搭建Quartus II 13.0开发环境，并开始您的FPGA开发之旅。祝您学习愉快！

## 下载链接

[QuartusII13.0下载安装与HelloWorld教程](https://pan.quark.cn/s/15f1310e7b64)