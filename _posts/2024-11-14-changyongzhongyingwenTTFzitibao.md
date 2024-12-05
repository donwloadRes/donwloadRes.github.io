---
layout: post
title: "常用中英文TTF字体包"
date:   2021-03-22
tags: [ttf,字体,bash,fonts,usr]
comments: true
author: admin
---
# 常用中英文TTF字体包

## 描述

本资源文件包含了常用的中英文TTF字体包，涵盖了多种字体风格，包括手写字体。具体字体列表如下：

- Times New Roman
- 中山行书百年纪念版
- Calibri
- Christopherhand
- DejaVuSansMono
- 方正兰亭黑
- James Fajardo
- Monaco
- 微软雅黑
- 仿宋
- 黑体
- 楷体
- 宋体
- yahei_mono
- 仿宋_GB2312
- 楷体_GB2312
- 迷你简行楷碑

## 文件列表

- bb1550.ttf
- calibri.ttf
- calibrib.ttf
- calibrii.ttf
- calibriz.ttf
- comesinhandy.ttf
- DejaVuSansMono-Bold.ttf
- DejaVuSansMono-BoldOblique.ttf
- DejaVuSansMono-Oblique.ttf
- DejaVuSansMono.ttf
- DroidSansFallback.ttf
- James_Fajardo.ttf
- Monaco.ttf
- msyh.ttf
- msyhbd.ttf
- simfang.ttf
- simhei.ttf
- simkai.ttf
- simsun.ttc
- times.ttf
- timesbd.ttf
- timesbi.ttf
- timesi.ttf
- yahei_mono.ttf
- 仿宋_GB2312.ttf
- 使用方法.txt
- 楷体_GB2312.ttf
- 迷你简行楷碑.TTF

## 使用方法

### Windows

将所有的TTF文件拷贝到系统所在分区的 `C:\Windows\Fonts` 目录下即可。

### Linux

1. 解压缩下载的字体压缩包：
   ```bash
   tar xvzf utf8.tar.gz
   ```
   或
   ```bash
   tar xvjf arial.tar.bz2
   ```

2. 创建一个新的字体目录：
   ```bash
   mkdir /usr/share/fonts/truetype
   ```

3. 将解压缩后的字体文件移动到新创建的字体目录：
   ```bash
   mv *.ttf /usr/share/fonts/truetype
   ```

4. 导航到字体目录：
   ```bash
   cd /usr/share/fonts/truetype
   ```

5. 创建 `fonts.scale` 和 `fonts.dir` 文件：
   ```bash
   mkfontscale && mkfontdir
   fc-cache
   ```

6. 将新字体目录添加到X11字体路径：
   ```bash
   chkfontpath --add /usr/share/fonts/truetype
   ```

7. 重启X字体服务器：
   ```bash
   /etc/rc.d/init.d/xfs restart
   ```

   你可以通过运行 `chkfontpath` 命令或查看 `/etc/X11/XF86Config` 文件来验证新路径是否成功添加。

   如果没有root权限，可以将 `*.ttf` 文件复制到 `~/.fonts` 目录下。

### 使X11字体对Java可用

1. 打开 `/etc/profile` 文件，并添加一个新的环境变量：
   ```bash
   JAVA_FONTS=/usr/share/fonts/truetype
   export JAVA_FONTS
   ```

2. 打开 `jre/lib` 目录下的 `font.properties` 文件，取消注释并设置为适当的字体目录：
   ```bash
   appendedfontpath=/usr/share/fonts/truetype
   ```

## 注意事项

- 确保在安装字体时遵循操作系统的权限要求。
- 对于Linux系统，确保字体路径正确配置，以便应用程序能够正确识别和使用这些字体。

## 下载链接

[常用中英文TTF字体包](https://pan.quark.cn/s/35977db86049)