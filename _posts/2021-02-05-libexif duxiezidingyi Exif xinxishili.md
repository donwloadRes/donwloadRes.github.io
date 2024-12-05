---
layout: post
title: "libexif 读写自定义 Exif 信息实例"
date:   2021-06-15
tags: [libexif,test,exif,Exif,bash]
comments: true
author: admin
---
# libexif 读写自定义 Exif 信息实例

本仓库提供了一个名为 `libexif-master.tar.gz` 的资源文件，该文件包含了 libexif 库的源代码以及相关示例代码，用于读写自定义的 Exif 信息。详细的使用说明请参见 `MyReadme.txt` 文件。

## 资源文件内容

- **libexif-master.tar.gz**: 包含 libexif 库的源代码及相关示例代码。

## 使用说明

### 1. 编译库

1. 解压 `libexif-master.tar.gz` 文件。
2. 进入解压后的 `libexif-master` 文件夹。
3. 运行 `mybuild_ubuntu.sh` 脚本进行编译。

```bash
cd libexif-master
./mybuild_ubuntu.sh
```

编译完成后，当前目录下的 `build` 文件夹中会生成编译后的文件。

```bash
ls build/
# 输出: include  lib  share
```

### 2. 编译示例 Demo

进入 `contrib/examples/` 目录，运行 `compile_example.sh` 脚本编译示例代码。

```bash
cd contrib/examples/
./compile_example.sh
```

### 3. 测试示例

#### 写入自定义 Exif 信息

使用 Windows 自带的画图软件生成一个 JPG 文件，或者使用自带的 `test.jpg` 文件。然后运行 `test_jpeg_exif_new` 程序写入自定义 Exif 信息。

```bash
./test_jpeg_exif_new test.jpg test_exif.jpg
```

如果操作成功，会有如下输出：

```bash
Add customer exif info for test.jpg ok!
```

#### 读取写入的 Exif 信息

运行 `read_jpeg_exif` 程序读取写入的 Exif 信息。

```bash
./read_jpeg_exif test_exif.jpg
```

输出示例：

```bash
-------------->ExifInfo:test_exif.jps Start<--------------
======IFD: 0 0======
X-Resolution: 72
Y-Resolution: 72
Resolution Unit: Inch
======IFD: 1 1======
============IFD: 2 EXIF======
Exposure Time: 1/18 sec.
F-Number: f/4.0
ISO Speed Ratings: 60
Exposure Bias: 0.00 EV
Maximum Aperture Value: 4.00 EV (f/4.0)
Subject Distance: 0.0 m
Metering Mode: Pattern
Flash: Flash fired
Focal Length: 35.0 mm
Flash Energy: 65535
Exif Version: Exif Version 2.1
FlashPixVersion: FlashPix Version 1.0
Color Space: Uncalibrated
======IFD: 3 GPS======
North or South Latitude: W
Latitude: 38.0 132897/0 0/0 0/0 0/0 0/0 0/0 0/0
East or West Longitude: N
Longitude: 9.0 132833/0 0/0 0/0 0/0 0/0 0/0 0/0
======IFD: 4 Interoperability======
-------------->ExifInfo:test_exif.jps End<--------------
```

## 注意事项

- 确保系统中已安装必要的编译工具和依赖库。
- 示例代码中的路径和文件名可能需要根据实际情况进行调整。

## 其他说明

更多详细信息请参见 `MyReadme.txt` 文件。

## 下载链接

[libexif读写自定义Exif信息实例](https://pan.quark.cn/s/f8394f5856c0)