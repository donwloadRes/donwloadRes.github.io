---
layout: post
title: "PCB Logo Creator 使用指南"
date:   2022-10-21
tags: [PCB,logo,Altium,Designer,脚本]
comments: true
author: admin
---
# PCB Logo Creator 使用指南

## 概述
PCB Logo Creator 是一款专为Altium Designer用户设计的脚本工具，用于方便地将您的logo嵌入到PCB设计中。如果您希望在电路板上添加企业或项目标志，本工具将是您不可或缺的好帮手。通过简单的几步操作，即可将黑白位图转换成PCB兼容格式并放置于指定的PCB层上。

## 使用步骤

### 步骤1: 准备Logo图像
- 将您的logo转化为单色BMP格式。最简便的方式是利用Windows自带的“画图”工具。编辑好后，保存时选择“单色.bmp”。

### 步骤2: 运行脚本
1. 启动Altium Designer。
2. 点击顶部菜单的“DXP” -> 选择“Run...”命令。
3. 在弹出的对话框点击“Browse”，导航至安装目录下的示例路径（如：`D:\Program Files\Altium Designer 10\Examples\`），找到`CBLogoCreator.PRJSCR`脚本文件并打开。请注意根据实际安装位置调整路径。

### 步骤3: 导入Logo
- 在脚本运行界面，按照提示导入步骤1准备的单色logo BMP图像。
- 设置导入层为“Top Overlay”（顶层丝印层）或其他适合的层，以及是否需要镜像处理。
- 点击“Load”加载图片，然后“Convert”进行转换。转换可能需要一些时间。

### 步骤4: 完成转换
- 脚本执行完毕后，会自动生成一个包含转换后logo的新PCB文件。
- 此时，您可以将logo复制粘贴到您的设计项目中了。

## 注意事项
- 请确保您的系统中已经安装有支持该脚本版本的Altium Designer软件。
- 若电脑未安装上述脚本，您可通过附件下载`PCB Logo Creator.rar`文件进行安装。
- 确保logo的清晰度和简洁性，以保证在实际PCB上的可读性和美观度。

通过遵循上述步骤，您就能轻松将个性化logo融入到产品设计之中，增添产品的独特魅力。祝设计顺利！

## 下载链接

[PCBLogoCreator使用指南](https://pan.quark.cn/s/b50e4fdbfe6f)