---
layout: post
title: "Qt6.5.0 MySQL驱动文件已编译版本"
date:   2023-11-24
tags: [qsqlmysql,lib,驱动,文件,dll]
comments: true
author: admin
---
# Qt6.5.0 MySQL驱动文件已编译版本

本仓库提供了一个已经编译好的Qt6.5.0 MySQL驱动文件，可以直接拷贝到相应的驱动文件夹中使用，无需进行繁琐的编译过程。以下是资源文件的树状结构：

```
├─mingw_64QMySQL驱动文件
│      qsqlmysql.debug
│      qsqlmysql.dll
├─msvc2019_64QMySQL驱动文件
│      qsqlmysql.dll
│      qsqlmysql.exp
│      qsqlmysql.lib
│      qsqlmysql.pdb
│      qsqlmysqld.dll
│      qsqlmysqld.exp
│      qsqlmysqld.lib
│      qsqlmysqld.pdb
└─MySQL_lib文件
        libmysql.dll
        libmysql.lib
```

## 使用方法

1. 根据你的Qt版本和编译器类型，选择相应的驱动文件夹（`mingw_64` 或 `msvc2019_64`）。
2. 将驱动文件夹中的所有文件拷贝到你的Qt安装目录下的 `plugins/sqldrivers` 文件夹中。
3. 将 `MySQL_lib` 文件夹中的 `libmysql.dll` 和 `libmysql.lib` 文件拷贝到你的项目目录或系统路径中。

## 注意事项

- 确保你的Qt版本为6.5.0，否则可能无法正常使用这些驱动文件。
- 如果你使用的是其他编译器或Qt版本，可能需要重新编译驱动文件。

## 贡献

欢迎提交问题和改进建议，帮助我们完善这个资源。如果你有更好的编译版本或改进方法，也欢迎提交PR。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。

## 下载链接

[Qt6.5.0MySQL驱动文件已编译版本](https://pan.quark.cn/s/ec746032e6a2)