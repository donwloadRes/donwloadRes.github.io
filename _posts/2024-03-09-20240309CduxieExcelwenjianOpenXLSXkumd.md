---
layout: post
title: "C读写Excel文件  OpenXLSX库
date   20220429
tags ExcelOpenXLSX文件xlsx示例
comments true
author admin

 C读写Excel文件  OpenXLSX库

 简介

OpenXLSX是一套开源的C库专门用于读取写入创建和修改Excel文件格式xlsx本仓库提供了OpenXLSX的源代码以及相关的示例程序帮助开发者快速上手并集成到自己的项目中

 功能特点

 读取Excel文件支持读取xlsx格式的Excel文件并提取其中的数据
 写入Excel文件可以将数据写入到xlsx格式的Excel文件中支持创建新的文件或修改现有文件
 创建Excel文件可以创建新的xlsx格式的Excel文件并设置初始内容
 修改Excel文件支持对现有xlsx格式的Excel文件进行修改包括添加删除和更新单元格数据

 使用方法

1 下载源码
    克隆本仓库到本地
     bash
     git clone httpsgithubcomyourrepourlgit
     

2 编译与运行
    进入项目目录
     bash
     cd OpenXLSX
     
    根据项目提供的编译脚本或使用CMake进行编译
     bash
     mkdir build
     cd build
     cmake 
     make
     
    运行示例程序
     bash
     examplesexampleprogram
     

3 集成到项目
    将OpenXLSX的源码文件添加到你的项目中并根据需要进行编译和链接
    参考示例程序了解如何使用OpenXLSX库进行Excel文件的读写操作

 示例代码

以下是一个简单的示例代码展示了如何使用OpenXLSX库创建一个新的Excel文件并写入数据

cpp
include OpenXLSXhpp"
date:   2022-04-29
tags: [Excel,OpenXLSX,文件,xlsx,示例]
comments: true
author: admin
---
# C++读写Excel文件 - OpenXLSX库

## 简介

OpenXLSX是一套开源的C++库，专门用于读取、写入、创建和修改Excel文件（格式：xlsx）。本仓库提供了OpenXLSX的源代码以及相关的示例程序，帮助开发者快速上手并集成到自己的项目中。

## 功能特点

- **读取Excel文件**：支持读取xlsx格式的Excel文件，并提取其中的数据。
- **写入Excel文件**：可以将数据写入到xlsx格式的Excel文件中，支持创建新的文件或修改现有文件。
- **创建Excel文件**：可以创建新的xlsx格式的Excel文件，并设置初始内容。
- **修改Excel文件**：支持对现有xlsx格式的Excel文件进行修改，包括添加、删除和更新单元格数据。

## 使用方法

1. **下载源码**：
   - 克隆本仓库到本地：
     ```bash
     git clone https://github.com/your-repo-url.git
     ```

2. **编译与运行**：
   - 进入项目目录：
     ```bash
     cd OpenXLSX
     ```
   - 根据项目提供的编译脚本或使用CMake进行编译：
     ```bash
     mkdir build
     cd build
     cmake ..
     make
     ```
   - 运行示例程序：
     ```bash
     ./examples/example_program
     ```

3. **集成到项目**：
   - 将OpenXLSX的源码文件添加到你的项目中，并根据需要进行编译和链接。
   - 参考示例程序，了解如何使用OpenXLSX库进行Excel文件的读写操作。

## 示例代码

以下是一个简单的示例代码，展示了如何使用OpenXLSX库创建一个新的Excel文件并写入数据：

```cpp
#include "OpenXLSX.hpp"

int main() {
    // 创建一个新的Excel文件
    OpenXLSX::XLDocument doc;
    doc.create("example.xlsx");

    // 获取工作表
    auto wks = doc.workbook().worksheet("Sheet1");

    // 写入数据
    wks.cell("A1").value() = "Hello, OpenXLSX!";
    wks.cell("B1").value() = 42;

    // 保存文件
    doc.save();

    return 0;
}
```

## 依赖项

- OpenXLSX库本身不依赖于其他第三方库，但需要C++11或更高版本的标准库支持。

## 贡献

欢迎开发者为本项目贡献代码、提交问题或提出改进建议。请参考[贡献指南](CONTRIBUTING.md)进行操作。

## 许可证

本项目采用MIT许可证，详情请参阅[LICENSE](LICENSE)文件。

## 联系

如有任何问题或建议，请通过[GitHub Issues](https://github.com/your-repo-url/issues)联系我们。

---

希望OpenXLSX库能够帮助你轻松处理Excel文件的读写操作！

## 下载链接

[C读写Excel文件-OpenXLSX库](https://pan.quark.cn/s/c680feded075)