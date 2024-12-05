---
layout: post
title: "Windows下简易安装NCL指南"
date:   2020-11-30
tags: [NCL,Cygwin,安装,ncl,Terminal]
comments: true
author: admin
---
# Windows下简易安装NCL指南

本文提供了一种简便的方法在Windows 10上安装NCL（NCAR Command Language）。通过使用预编译的NCL安装包和Cygwin，步骤包括下载Cygwin安装包和NCL文件、修改环境变量，并在Cygwin Terminal中运行测试以验证安装。此教程特别适合多次安装失败或希望简化安装过程的用户。

## 安装步骤

### 1. 下载Cygwin安装包

下载Cygwin安装包并解压后，将“cygwin”整个文件夹移到所要安装的路径（如D盘或E盘根目录下）。

### 2. 下载预编译的NCL安装包

下载预编译的NCL安装包（如6.4版本），并将其解压至`E:/cygwin/app/ncl`或`D:/cygwin/app/ncl`目录下。确保ncl文件夹已创建。

### 3. 修改环境变量

打开Cygwin Terminal，输入以下命令来修改环境变量：

```bash
vi ~/.bashrc
```

在文件末尾添加以下内容：

```bash
# for ncl
export NCARG_ROOT=/app/ncl
export PATH=$NCARG_ROOT/bin:$PATH
export DISPLAY=:0.0
```

保存并退出编辑器，然后执行以下命令使更改生效：

```bash
source ~/.bashrc
```

### 4. 运行测试

重新打开Cygwin Terminal，输入以下命令以验证NCL安装是否成功：

```bash
ncl
```

如果显示出正确版本信息，即表示安装完成。

## 注意事项

- 如果安装路径在E盘而非D盘，需在Cygwin Terminal快捷方式的属性中将目标路径中的D盘改为E盘。
- 安装完成后，每次使用NCL时均需从Cygwin Terminal打开。

通过以上步骤，您可以在Windows系统上轻松安装并使用NCL。

## 下载链接

[Windows下简易安装NCL指南](https://pan.quark.cn/s/54da6927e2bc)