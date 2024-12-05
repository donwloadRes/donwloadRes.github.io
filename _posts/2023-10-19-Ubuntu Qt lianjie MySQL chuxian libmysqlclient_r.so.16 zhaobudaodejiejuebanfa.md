---
layout: post
title: "Ubuntu Qt 连接 MySQL 出现 libmysqlclient_r.so.16 找不到的解决办法"
date:   2022-10-15
tags: [libmysqlclient,so.16,MySQL,文件,下载]
comments: true
author: admin
---
# Ubuntu Qt 连接 MySQL 出现 libmysqlclient_r.so.16 找不到的解决办法

## 简介

本资源文件提供了在 Ubuntu 系统上使用 Qt 连接 MySQL 数据库时，遇到 `libmysqlclient_r.so.16` 文件找不到的问题的解决办法。该问题通常出现在尝试加载 MySQL 驱动时，系统无法找到所需的动态链接库文件。

## 问题描述

在使用 Qt 开发的应用程序中，尝试连接 MySQL 数据库时，可能会遇到以下错误信息：

```
libmysqlclient_r.so.16: cannot open shared object file: No such file or directory
```

这表明系统无法找到 `libmysqlclient_r.so.16` 文件，导致 MySQL 驱动无法加载。

## 解决步骤

### 1. 确认文件缺失

首先，确认系统中确实缺少 `libmysqlclient_r.so.16` 文件。可以通过以下命令检查：

```bash
find / -name libmysqlclient_r.so.16
```

如果命令返回空结果，说明文件确实缺失。

### 2. 下载并安装缺失的文件

根据系统架构（32位或64位），下载对应的 `libmysqlclient_r.so.16` 文件。

- 64位系统下载链接：[下载链接]
- 32位系统下载链接：[下载链接]

下载完成后，将文件移动到 `/usr/lib/i386-linux-gnu` 目录下：

```bash
mv 下载的文件路径 /usr/lib/i386-linux-gnu
```

### 3. 测试动态库是否加载成功

重新测试动态库是否已经加载成功：

```bash
ldd /opt/Qt5.4.0/5.4/gcc/plugins/sqldrivers/libqsqlmysql.so
```

如果命令输出中不再显示 `libmysqlclient_r.so.16` 找不到的错误，说明问题已解决。

### 4. 重启应用程序

如果上述步骤完成后问题仍未解决，可以尝试重启应用程序或系统，确保更改生效。

## 注意事项

- 确保下载的文件与系统架构匹配。
- 如果问题仍然存在，可能需要检查其他依赖库是否缺失或版本不匹配。

## 参考资料

有关该问题的详细描述和解决步骤，请参考 [CSDN博客文章](https://blog.csdn.net/jiacheng1991/article/details/82597922)。

## 贡献

如果您有更好的解决办法或发现了其他相关问题，欢迎提交贡献。

## 许可证

本资源文件遵循 [CC 4.0 BY-SA 版权协议](https://creativecommons.org/licenses/by-sa/4.0/)，转载请附上原文出处链接和本声明。

## 下载链接

[UbuntuQt连接MySQL出现libmysqlclient_r.so.16找不到的解决办法分享](https://pan.quark.cn/s/5197da6f7c3d)