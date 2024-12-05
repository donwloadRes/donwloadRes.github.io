---
layout: post
title: "Unity强力配置插件LubanNext最新版本部署指南"
date:   2024-07-16
tags: [Luban,Unity,插件,项目,Next]
comments: true
author: admin
---
# Unity强力配置插件Luban【Next最新版本】部署指南

## 简介
Luban是一个强大、易用、优雅、稳定的游戏配置解决方案，旨在满足从小型到超大型游戏项目，从简单到复杂的游戏配置工作流需求。在2023年下半年，Luban项目进行了重构，旧版本命名为Classic版，新版本为Next版。如果追求稳定性，建议使用Classic版；如果需要更简化的流程和模块化功能，推荐使用Next版。

## 准备工作
1. **安装dotnet SDK 8.0或更高版本**：确保你的开发环境支持dotnet SDK 8.0或更高版本。
2. **下载luban_examples项目**：获取Luban的示例项目，以便参考和学习。
3. **准备一个Unity项目**：确保你有一个正在开发的Unity项目，用于集成Luban插件。

## 快速配置
### 1. Luban配置
- 在目标工程中新建一个名为`Luban`的文件夹。
- 将下载的示例项目中的`MiniTemplate`和`Tools`文件夹拷贝到`Luban`文件夹中。
- 运行`gen.bat`文件，生成配置文件。

### 2. Unity配置
- 下载并解压Luban Unity插件，将其放置在Unity项目的`Assets`文件夹中。
- 在Unity的`PlayerSettings`中开启`unsafe`选项。
- 修改`gen.bat`文件，设置数据生成的路径，并添加代码生成的路径。

### 3. Unity内加载
- 在Unity场景中添加一个脚本，用于加载Luban生成的配置数据。
- 运行Unity项目，验证配置数据是否正确加载并打印信息。

## 优化整理
- 删除`Luban\DesignerConfigs\Datas`目录下无用的文件，只保留必要的配置文件。
- 根据项目需求，添加自定义的类型转换脚本，如`ExternalTypeUtil`。
- 移除不需要的脚本文件，如`gen.sh`，并调整`gen.bat`文件的路径设置。

## 总结
通过以上步骤，你可以快速上手并部署Luban Next版插件，实现游戏配置的自动化生成和管理。Luban的强大功能和易用性将极大地提升你的开发效率，帮助你更好地管理和优化游戏配置。

## 下载链接

[Unity强力配置插件LubanNext最新版本部署指南](https://pan.quark.cn/s/80bb620f928e)