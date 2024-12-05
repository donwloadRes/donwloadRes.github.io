---
layout: post
title: "基于Cortex-A53内核Linux系统gec6818开发板的电子自助点餐设计"
date:   2024-03-14
tags: [文件,开发板,菜品,编译,点餐]
comments: true
author: admin
---
# 基于Cortex-A53内核Linux系统gec6818开发板的电子自助点餐设计

## 项目简介

本项目基于Cortex-A53内核的Linux系统，使用gec6818开发板实现了一个电子自助点餐系统。该系统旨在提供一个便捷、高效的点餐体验，适用于各种餐饮场景。

## 功能特点

1. **菜品展示**：系统能够展示所有菜品的照片以及桌面背景图片，用户可以通过触摸屏浏览菜品。
2. **菜品选择**：用户可以通过触摸屏选择菜品，并进行数量的增减操作。
3. **结算功能**：用户点餐完毕后，系统会自动计算总价，并提供结算功能。
4. **多文件编译**：项目涉及多个文件和链接库，通过Makefile脚本文件方便用户进行多文件编译。
5. **底层支持**：系统使用了提供的底层文件和库文件，确保系统的稳定性和高效性。

## 文件结构

- **picture目录**：存放菜品的照片以及桌面背景图片。
- **common.c / common.h、font.h、input.h、input-event-codes.h、jconfig.h、jerror.h、jmorecfg.h、jpeglib.h、lcd.c、lcd.h**：提供的底层文件，直接使用即可。
- **libfont.a、libjpeg.so、libjpeg.so.8、libjpeg.so.8.3.0**：库文件，需要上传到开发板中。
- **main**：在Ubuntu系统下生成的可执行文件，需使用arm-linux-gcc编译。
- **Makefile**：脚本文件，方便用户多文件编译时命令过于冗长。
- **opendir.c**：检索目录下所有的.jpg文件，并将它们的名字存放到链表中。
- **double_link.c**：双向循环链表。
- **test.c**：main文件，里面的函数都有功能介绍，有兴趣的读者可以自行下载查看。

## 使用说明

1. **环境配置**：确保开发板和Ubuntu系统环境配置正确，库文件已上传到开发板。
2. **编译运行**：使用arm-linux-gcc编译main文件，并将生成的可执行文件上传到开发板运行。
3. **操作流程**：用户通过触摸屏浏览菜品，选择菜品并进行数量调整，点餐完毕后进行结算。

## 注意事项

- 由于是多文件下编译，涉及的文件很多，还有链接库，发源代码读者也不能编译运行，因此不将源代码下发打印。
- 所有的文件压缩成包，放到百度网盘上，有简陋功能展示视频（可直接扫描二维码）。

## 联系我们

如有任何问题或建议，请联系项目开发者。

## 下载链接

[基于Cortex-A53内核Linux系统gec6818开发板的电子自助点餐设计](https://pan.quark.cn/s/35a6e66e8e20)