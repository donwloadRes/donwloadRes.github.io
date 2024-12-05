---
layout: post
title: "Xcode10：library not found for -lstdc++.6.0.9 临时解决方法"
date:   2024-02-17
tags: [c++,6.0,Xcode,libstd,lib]
comments: true
author: admin
---
# Xcode10：library not found for -lstdc++.6.0.9 临时解决方法

当您在使用Xcode 10进行iOS应用开发时，可能会遇到“library not found for -lstdc++.6.0.9”的编译错误。这是由于Xcode 10移除了libstdc++.6.0.9库，转而支持更新的libc++库。本资源提供了针对此问题的一个临时解决方案，帮助那些仍然依赖于libstdc++.6.0.9库的老项目能够继续运行。

## 解决步骤：

1. **下载资源**：首先，您需要下载libstdc++.6.0.9的兼容文件。请注意，由于原始链接可能过期，您应该寻找当前有效的资源下载地址。

2. **真机与模拟器库文件**：
   - **真机运行**：打开路径`/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS.sdk/usr/lib`，如果您安装在非默认位置，请相应调整路径。
   - **模拟器运行**：对于模拟器，路径为`/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs/iPhoneSimulator.sdk/usr/lib`。

3. **文件替换**：解压缩下载的zip文件，得到`libstdc++.6.0.9.tbd`文件。将此文件复制到上述两个目录中，分别对应真实设备和模拟器的运行环境。

4. **重启Xcode**：完成文件替换后，重启Xcode使改动生效。

5. **替代方案考虑**：虽然此方法能立即解决问题，但从长期角度考虑，建议升级您的项目以适应最新的库要求，比如切换到使用libc++，这将确保项目的可持续发展和兼容性。

通过遵循上述步骤，您可以快速解决在Xcode 10环境中遇到的关于libstdc++.6.0.9的编译错误，让您的开发工作流畅进行。记得在处理完紧急情况后，考虑对项目进行必要的现代化改造，以避免将来再次遇到类似兼容性问题。

## 下载链接

[Xcode10librarynotfoundfor-lstdc.6.0.9临时解决方法分享](https://pan.quark.cn/s/be55879b8fd4)