---
layout: post
title: "Android MediaProjection 截屏录屏  完美适配至Android Q及以上版本"
date:   2023-04-16
tags: [Android,录屏,截屏,权限,前台]
comments: true
author: admin
---
# Android MediaProjection 截屏&录屏 - 完美适配至Android Q及以上版本

## 简介

本仓库提供了实现Android设备截屏与录屏功能的解决方案，特别针对Android Q（API级别29）引入的安全限制进行了优化。在Android Q及更高版本中，使用MediaProjection进行屏幕截图或录制视频时，开发者会遇到`java.lang.SecurityException: Media projections require a foreground service of type ServiceInfo.FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION`异常，本项目通过创建符合新要求的前台服务成功绕过了这一限制，确保了应用在目标SDK 32上也能顺利运行。

## 功能特点

- **兼容性**：确保在Android Q (API 29) 到最新版Android系统之间的完美工作。
- **安全合规**：遵循最新的隐私政策和权限管理机制。
- **前台服务适配**：通过实施前台服务策略，避免因权限变更导致的崩溃问题。
- **示例代码**：包含详实的代码示例，帮助快速集成截屏和录屏功能到您的应用中。

## 快速入门

1. **添加依赖**：确认项目支持的最低API级别，并根据需要将此项目的代码合并到你的项目中。
2. **请求权限**：在AndroidManifest.xml中添加必要的权限声明，包括录音权限（如果需要录屏带声音的话）和系统级的屏幕记录权限。
3. **创建并启动前台服务**：按照提供的模板创建一个服务类，设置其类型为`FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION`以满足Android Q以上的安全需求。
4. **用户交互**：设计UI来触发截屏或录屏操作，确保通知用户服务正在运行（这是Android系统的要求）。
5. **处理数据流**：对于录屏，正确管理和保存视频数据；对于截屏，处理生成的图像数据。

## 注意事项

- 集成前请仔细阅读Android官方文档关于MediaProjection和前台服务的最新指南，确保应用的稳定性和合规性。
- 测试应覆盖多种Android版本，以验证跨版本的兼容性。

## 示例与文档

本仓库的核心部分包含了关键代码片段和示范如何正确实施所述功能的详细步骤。为了最大化利用这些资源，请直接查看源码中的注释和示例Activity/Service，那里会有更具体的实施指导。

开始集成这个强大且适应性强的截屏和录屏模块，提升你的应用程序功能和用户体验吧！

---

这个仓库是针对那些希望在应用中无缝加入截屏与录屏功能开发者的一份宝贵资源，确保无论是在较新的还是旧版本的Android设备上都能流畅运行。

## 下载链接

[AndroidMediaProjection截屏录屏-完美适配至AndroidQ及以上版本](https://pan.quark.cn/s/3974c8fd0eb5)