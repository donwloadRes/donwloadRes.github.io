---
layout: post
title: "编译OpenCV时，xfeatures2d模块下载boostdesc_bgm.i等文件超时问题解决方案"
date:   2022-05-11
tags: [OpenCV,编译,xfeatures2d,下载,文件]
comments: true
author: admin
---
# 编译OpenCV时，xfeatures2d模块下载boostdesc_bgm.i等文件超时问题解决方案

在编译OpenCV的过程中，许多用户可能会遇到因网络问题导致xfeatures2d子模块无法成功下载boostdesc_bgm.i等重要文件的情况，这会直接阻碍编译进程。为了帮助大家顺利绕过这一难题，我们提供了本资源包和简易步骤指南，旨在通过本地文件替换的方式，确保OpenCV编译顺利完成。

## 解决步骤：

1. **资源复制**：
   下载本压缩包后，将其内容解压，并将得到的文件复制到OpenCV的指定源代码目录中。具体路径是`opencv_contrib/modules/xfeatures2d/src/`。如果您的项目结构已经创建好，这样做可以直接覆盖所需文件，避免下载超时的问题。

2. **修改下载脚本**：
   接下来，需要手动编辑位于`opencv_contrib/modules/xfeatures2d/cmake/download_boostdesc.cmake`文件。请使用文本编辑器（如记事本）打开此文件。找到负责从远程服务器下载文件的命令，原样通常是HTTP或HTTPS开头的URL地址。
   
   将这些下载指令中的URL替换为本地路径协议，格式如下：
   ```
   file://F://temp/boostdesc_bgm.i
   ```
   注意，这里的`F://temp/`应替换为您实际存储下载文件的本地路径。确保所有需要的文件都放在这个指定的本地目录中。

完成上述两步操作后，您就可以继续编译OpenCV了，这次xfeatures2d模块应当能够正确编译，不再受远程服务器响应时间的限制。

### 注意事项：
- 确保你有正确的OpenCV和opencv_contrib版本匹配。
- 路径名称对Windows用户来说可能有所不同，如果是Linux或macOS用户，路径将遵循各自的文件系统规则（如使用 `/` 作为路径分隔符）。
- 修改CMake脚本时，需谨慎操作，避免引入语法错误。

借助本指南及提供的资源，希望你的OpenCV编译之旅能更加顺畅！

## 下载链接

[编译OpenCV时xfeatures2d模块下载boostdesc_bgm.i等文件超时问题解决方案](https://pan.quark.cn/s/08f5f8ad47ec)