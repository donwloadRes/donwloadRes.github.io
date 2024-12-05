---
layout: post
title: "Android super.img 镜像解包工具"
date:   2023-04-30
tags: [解包,img,super,镜像文件,image]
comments: true
author: admin
---
# Android super.img 镜像解包工具

本仓库提供了一个用于解包 Android super.img 镜像文件的工具。super.img 是 Android 10 及更高版本中引入的动态分区镜像文件，包含了系统、供应商、产品等多个分区的镜像。通过本工具，您可以轻松地将 super.img 解包为各个分区的镜像文件，以便进行进一步的定制和修改。

## 工具介绍

### 主要工具
- **simg2img**: 用于将 Android sparse image 转换为 raw image。
- **lpunpack**: 用于从 raw image 中解包出各个分区的镜像文件。

### 使用步骤
1. **编译 lpunpack 工具**:
   - 按照以下命令编译 lpunpack 工具：
     ```
     source build/envsetup.sh
     make lpunpack
     ```
   - 生成的文件位于 `out/host/linux-x86/bin` 目录下。

2. **将 super.img 从 Android sparse image 转换为 raw image**:
   - 使用 simg2img 工具进行转换：
     ```
     simg2img super.img super_ext4.img
     ```

3. **从 raw image 解包出分区镜像文件**:
   - 使用 lpunpack 工具解包：
     ```
     lpunpack super_ext4.img output_dir
     ```
   - 解包后的文件将存储在 `output_dir` 目录下。

## 注意事项
- 解包和打包操作需要在 Linux 环境下进行。
- 请确保工具和依赖库是配套使用的，避免混搭工具和库文件。
- 解包后的镜像文件可以进行挂载和修改，修改完成后可以重新打包为新的 super.img。

## 参考资料
- 更多详细信息和操作步骤，请参考 [CSDN 博客文章](https://blog.csdn.net/u012045061/article/details/119383397)。

## 贡献
欢迎提交问题和改进建议，帮助我们完善这个工具。

## 许可证
本项目遵循 [CC 4.0 BY-SA 版权协议](https://creativecommons.org/licenses/by-sa/4.0/)，转载请附上原文出处链接和本声明。

## 下载链接

[Androidsuper.img镜像解包工具](https://pan.quark.cn/s/7ecfc7f2029b)