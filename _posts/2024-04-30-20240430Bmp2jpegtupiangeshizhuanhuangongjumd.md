---
layout: post
title: "Bmp2jpeg图片格式转换工具
date   20230729
tags BMPJPEGCBmp2Jpeg转换格式
comments true
author admin

 Bmp2jpeg图片格式转换工具

 简介

本仓库提供了一个C代码资源用于将BMP格式的图片转换为JPEG格式代码已经封装成一个名为CBmp2Jpeg的C类用户可以直接调用该类进行图片格式转换

 功能描述

 BMP转JPEG支持将BMP格式的图片文件转换为JPEG格式
 封装好的类代码已经封装成CBmp2Jpeg类用户只需实例化该类并调用相应的方法即可完成转换

 使用示例

以下是一个简单的使用示例展示了如何使用CBmp2Jpeg类将BMP图片转换为JPEG格式

cpp
include CBmp2Jpegh"
date:   2023-07-29
tags: [BMP,JPEG,CBmp2Jpeg,转换,格式]
comments: true
author: admin
---
# Bmp2jpeg图片格式转换工具

## 简介

本仓库提供了一个C++代码资源，用于将BMP格式的图片转换为JPEG格式。代码已经封装成一个名为`CBmp2Jpeg`的C++类，用户可以直接调用该类进行图片格式转换。

## 功能描述

- **BMP转JPEG**：支持将BMP格式的图片文件转换为JPEG格式。
- **封装好的类**：代码已经封装成`CBmp2Jpeg`类，用户只需实例化该类并调用相应的方法即可完成转换。

## 使用示例

以下是一个简单的使用示例，展示了如何使用`CBmp2Jpeg`类将BMP图片转换为JPEG格式：

```cpp
#include "CBmp2Jpeg.h"
#include <iostream>

int main() {
    CBmp2Jpeg bmp;
    bmp.Bmp2Jpeg("111_24.bmp", "lena.jpg");
    std::cout << "转换成功！" << std::endl;
    std::cin.get();
    return 0;
}
```

## 注意事项

- 请确保输入的BMP文件路径和输出的JPEG文件路径正确。
- 该代码适用于24位BMP图片的转换。

## 贡献

欢迎大家提出改进建议或提交PR，共同完善这个工具。

## 许可证

本项目采用MIT许可证，详情请参阅LICENSE文件。

## 下载链接

[Bmp2jpeg图片格式转换工具](https://pan.quark.cn/s/4e5702555ad6)