---
layout: post
title: "libyuv 安卓 Android 编译好的 SO 库文件及源代码"
date:   2022-09-21
tags: [libyuv,文件,SO,源代码,编译]
comments: true
author: admin
---
# libyuv 安卓 Android 编译好的 SO 库文件及源代码

本仓库提供最新版 libyuv 的编译好的 SO 库文件及源代码，适用于安卓平台。具体包括以下内容：

- **arm64-v8a** 平台的动态库文件
- **armeabi-v7a** 平台的动态库文件
- **x86** 平台的动态库文件
- **x86_64** 平台的动态库文件

这些库文件可以直接在安卓项目中使用，无需额外编译。libyuv 是一个高效的 YUV 转 RGB 库，其转换效率远高于 ffmpeg 的 swscale，推荐在需要高性能 YUV 转 RGB 的场景中使用。

## 使用说明

1. **下载库文件**：从本仓库中下载对应平台的 SO 库文件。
2. **集成到项目**：将下载的 SO 库文件放置到安卓项目的 `libs` 目录下。
3. **配置 build.gradle**：在项目的 `build.gradle` 文件中添加以下配置，确保库文件被正确加载：

   ```groovy
   android {
       ...
       sourceSets {
           main {
               jniLibs.srcDirs = ['libs']
           }
       }
   }
   ```

4. **使用 libyuv**：在你的代码中直接调用 libyuv 提供的接口进行 YUV 到 RGB 的转换。

## 注意事项

- 本仓库提供的库文件已经过编译，无需额外编译步骤。
- 请根据你的目标平台选择合适的 SO 库文件。
- 如果你需要修改或自定义 libyuv 的源代码，可以参考本仓库提供的源代码进行二次开发。

## 支持的平台

- **arm64-v8a**
- **armeabi-v7a**
- **x86**
- **x86_64**

## 推荐使用

libyuv 在 YUV 转 RGB 的性能上表现优异，尤其是在处理大量图像数据时，其效率远高于 ffmpeg 的 swscale。推荐在需要高性能图像处理的安卓项目中使用。

## 联系我们

如果你在使用过程中遇到任何问题或有任何建议，欢迎通过 GitHub 的 Issues 功能联系我们。

## 下载链接

[libyuv安卓Android编译好的SO库文件及源代码](https://pan.quark.cn/s/190bd7a4a0ec)