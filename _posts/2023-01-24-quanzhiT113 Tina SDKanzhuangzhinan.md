---
layout: post
title: "全志T113 Tina SDK安装指南"
date:   2024-06-01
tags: [Tina,SDK,tar,bash,dev]
comments: true
author: admin
---
# 全志T113 Tina SDK安装指南

本仓库提供了一个资源文件，用于全志T113平台的Tina SDK安装。Tina SDK是全志科技基于Linux内核开发的针对智能硬件类产品的嵌入式软件系统，包含了Linux系统开发用到的内核源码、驱动、工具、系统中间件与应用程序包。

## 资源文件内容

- **Tina SDK安装包**：包含了Tina SDK的安装文件，用户可以通过解压并按照步骤进行安装。
- **补丁文件**：用于修复和更新Tina SDK中的某些组件。
- **依赖库安装脚本**：提供了在Ubuntu 18.04系统上安装Tina SDK所需依赖库的脚本。

## 安装步骤

1. **解压SDK**：
   ```bash
   tar -zxvf Tina-Linux-20220815.tar.gz
   cd Tina-Linux
   ```

2. **安装补丁**：
   ```bash
   wget http://dl.mangopi.org/tina/prebuilt.tar.gz
   tar xzvf prebuilt.tar.gz
   wget http://dl.mangopi.org/tina/dl.tar
   tar xvf dl.tar
   ```

3. **安装依赖库**：
   ```bash
   sudo apt-get install build-essential subversion git-core libncurses5-dev zlib1g-dev gawk flex quilt libssl-dev xsltproc libxml-parser-perl mercurial bzr ecj cvs unzip lib32z1 lib32z1-dev lib32stdc++6 libstdc++6 libmpc-dev libgmp-dev -y
   ```

4. **编译**：
   ```bash
   source build/envsetup.sh
   lunch 7:t113_mq_r-tina
   make
   ```

5. **编译uboot**：
   ```bash
   mboot
   ```

6. **打包镜像**：
   ```bash
   pack
   ```

## 常见问题

- **打包镜像报错**：如果遇到`mbr failed`错误，请检查分区设置，确保boot分区配置正确。

## 参考资料

- 更多详细信息和操作步骤，请参考[全志T113 Tina SDK安装](https://blog.csdn.net/linkkeee/article/details/136695042)。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个资源文件。

## 许可证

本资源文件遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接和本声明。

## 下载链接

[全志T113TinaSDK安装指南](https://pan.quark.cn/s/435b153e8c0d)