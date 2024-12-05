---
layout: post
title: "QT 624 自编译 WebEngine 版本"
date:   2024-09-24
tags: [编译,QT,WebEngine,Python,--]
comments: true
author: admin
---
# QT 6.2.4 自编译 WebEngine 版本

## 特性说明：
此资源提供了QT 6.2.4版本的自编译包，特别增强了QWebEngineview组件的功能，使其能够支持MP4等视频格式的直接播放。这解决了QT默认配置下WebEngine对多媒体播放支持不足的问题。为了实现这一增强功能，编译过程中特别包括并启用了专有编解码器的支持。

## 系统需求与编译环境：
- **Python 2.7.5或更高**：请注意，WebEngine部分要求使用Python 2.7系列，Python 3不兼容。
- Bison & Flex 3：解析工具的必需版本。
- GPerf：用于性能分析的工具。
- Perl & Ruby：脚本语言，编译过程中的辅助工具。
- **Node.js v12或以上**：用于处理某些前端构建任务。
- **Visual Studio 2019**：推荐使用的IDE，自带Windows 10 SDK（version 10.0.19041或以上）。
- **Python 3.8或更高**：用于编译QT源代码本身。
- Ninja构建系统：提高编译速度。
  
### 配置与编译命令示例：
在满足上述环境后，执行以下步骤进行编译：
```sh
configure -prefix C:\x64release -release -force-debug-info -platform win32-msvc -opensource -confirm-license -opengl es2 -webengine-proprietary-codecs
cmake --build . --parallel
cmake --install .
```
**重要提示：**
- 编译本资源需占用大量系统资源。确保硬盘空间至少50GB+，内存建议16GB+，以及高性能的计算平台。在资源有限的环境下（如虚拟机），编译过程可能极为缓慢，实际耗时一周的情况表明这是个资源密集型任务。
- 编译前请仔细检查依赖，正确安装所有必需工具，以避免编译错误或不完全的编译结果。

## 使用须知：
本资源旨在方便那些需要在Qt应用中集成网页视图及媒体播放能力的开发者。请注意，自行编译的库可能不包含官方发布的所有更新和修复，使用时请根据项目需求谨慎评估。

通过下载使用此自编译版QT，您将能快速启用QWebEngineview的高级功能，无需手动处理复杂的编译配置，极大加速您的开发进程。

## 下载链接

[QT6.2.4自编译WebEngine版本](https://pan.quark.cn/s/fe46ade4bc73)