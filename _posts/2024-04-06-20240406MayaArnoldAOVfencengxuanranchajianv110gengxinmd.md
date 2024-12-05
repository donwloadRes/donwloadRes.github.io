---
layout: post
title: "Maya Arnold AOV 分层渲染插件 v1.1.0 更新"
date:   2023-12-27
tags: [ID,分层,Arnold,渲染,插件]
comments: true
author: admin
---
# Maya Arnold AOV 分层渲染插件 v1.1.0 更新

## 简介

本资源文件提供了一个用于Maya的Arnold AOV分层渲染插件的最新版本v1.1.0。该插件旨在帮助用户更方便地管理和创建Arnold渲染器的分层渲染通道，特别适用于需要处理大量镜头和复杂场景的动画制作。

## 主要功能

- **更直观的分层渲染面板**：提供预设保存功能，方便用户快速管理分层选项。
- **新增分层类型**：包括物体ID、材质ID、Rim边缘光、物体的AO和Occ、线框效果等自定义通道输出。
- **物体组ID和材质ID创建功能**：优化了整体UI面板结构，将层操作加到右键快捷菜单中，操作更加简洁方便。
- **快速渲染分层批量创建**：支持快速创建、关闭、开启、反选、删除通道等操作。
- **运动模糊层设置**：提供Motion Vector快速摄像机设置开关和恢复工具。
- **自定义边缘发光层**：新增Rim物体自定义边缘发光层，使用Sample Info节点。
- **物体ID层创建方式**：使用aiUserDataFloat节点，自定义浮点变量arnold专有变量objectID，确保ID的唯一性。
- **灰度材质ID层方式**：选择材质节点，设置一个ID灰度，创建即可，提供Nuke提取方法。

## 安装方法

1. **解压安装**：将压缩包解压到非中文路径下，直接将tjh_Arnold_AOV_creator_Main.mel拖入Maya窗口即可弹出界面。
2. **手动安装**：解压目录中的文件到Maya的用户script目录中，注意不包含原有解压的父目录，将mel和dll文件夹直接放到script下，之后重新启动Maya，在命令行输入tjh_Arnold_AOV_creator_Main。

## 使用教程

详细的使用教程请参考[CSDN博客文章](https://blog.csdn.net/tian0000hai/article/details/107474387)。

## 更新历史

- **v1.1.0**：更直观的分层渲染面板，新增分层类型，优化UI面板结构。
- **v1.0.5**：增加最新Arnold 3.1.1版新aovs pass层的支持，主菜单增加preset reset功能。
- **v1.0.1**：增加快速渲染分层批量创建、运动模糊层设置、自定义边缘发光层、物体ID层创建方式、灰度材质ID层方式。

## 版权声明

本插件为原创作品，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

---

希望这个README.md文件能够帮助你更好地了解和使用这个Maya Arnold AOV分层渲染插件。如果有任何问题或建议，欢迎联系我们。

## 下载链接

[MayaArnoldAOV分层渲染插件v1.1.0更新分享](https://pan.quark.cn/s/2727b584d4b5)