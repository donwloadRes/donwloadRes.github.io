---
layout: post
title: "AI绘画Stable Diffusion整合包v42版本安装说明"
date:   2024-05-30
tags: [整合,启动器,v4.2,插件,AI]
comments: true
author: admin
---
# AI绘画Stable Diffusion整合包v4.2版本安装说明

## 简介
本资源文件提供了AI绘画Stable Diffusion整合包v4.2版本的安装说明。该整合包基于开源项目stabledefusingwebui，适合初学者和遇到问题的用户。整合包包含了运行Stable Diffusion所需的必要环境、预置模型和常用插件，安装简便，适合Windows 10以上系统、NVIDIA独立显卡等硬件配置。

## 整合包内容
1. **整合包升级内容**：
   - torch2
   - xformers0.0.17
   - cudnn8.8
   - 其他各种依赖版本升级
   - 预置了Tagger（图反推关键词）的模型
   - 预置了ControlNet、MultiDiffusion插件
   - 优化了一些其他设置

2. **整合包声明**：
   - 整合包基于开源项目stable defusing web ui制作，没有任何官方版一说。
   - 整合包打包了运行必须的环境，如python、git，并预制好模型，添加了一些常用插件。
   - 所有环境都在包内，随用随删，环境是独立虚拟的，不会产生任何冲突。

3. **适合人群**：
   - 零基础入门没用过AI绘画的人
   - 把原来整合包自己玩坏了的人
   - 不想动脑子的人

4. **运行所需的配置需求**：
   - 操作系统要求：Windows 10 以后
   - CPU不做强制性要求
   - 内存推荐：8GB以上
   - 显卡必须是NVIDIA独立显卡，显存最低4GB
   - 固态硬盘，空间最好200GB以上，提升模型加载速度

5. **整合包包含内容**：
   - 可选ControlNet模型（按需下载）
   - 启动器运行依赖-donet-6.0.11.exe
   - sd-webui-aki-v4.2.zip

## 安装步骤
1. 解压sd-webui-aki-v4.2.zip。
2. 如果之前没用过启动器，首先需要安装启动器的依赖：启动器运行依赖-donet-6.0.11.exe。
3. 安装完成后，进入解压后的整合包目录：sd-webui-aki-v4.2，直接双击A启动器.exe运行。
4. 点击“一键启动”按钮，启动Stable Diffusion控制台及操作界面。

## 后续版本更新
1. 点击左侧版本管理。
2. 切换到本体标签页，点击右上角“一键更新”按钮即可升级本体。
3. 切换到扩展标签页，点击右上角“一键更新”按钮即可升级扩展插件。

## 免责声明
本安装包及启动器免费提供，无任何盈利目的。

## 下载链接

[AI绘画StableDiffusion整合包v4.2版本安装说明](https://pan.quark.cn/s/70aa69767a70)