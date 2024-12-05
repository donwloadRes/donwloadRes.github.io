---
layout: post
title: "Aspose Excel 转 PDF 依赖的 Jar 包"
date:   2023-02-11
tags: [Jar,Excel,PDF,aspose,Aspose]
comments: true
author: admin
---
# Aspose Excel 转 PDF 依赖的 Jar 包

本仓库提供了一个用于将 Excel 文件转换为 PDF 格式的依赖 Jar 包。该资源文件包含了两个关键的 Jar 包：`aspose-cells-8.5.2.jar` 和 `aspose-words-15.8.0.jar`。

## 资源文件描述

- **aspose-cells-8.5.2.jar**: 该 Jar 包是 Aspose Cells 库的一部分，用于处理 Excel 文件的读取、写入和转换操作。通过该库，您可以将 Excel 文件转换为 PDF 格式。
  
- **aspose-words-15.8.0.jar**: 该 Jar 包是 Aspose Words 库的一部分，用于处理 Word 文档的读取、写入和转换操作。虽然主要用于 Word 文档，但在某些情况下，它也可以辅助 Excel 文件的转换。

## 使用说明

1. **下载 Jar 包**: 您可以直接从本仓库下载 `aspose-cells-8.5.2.jar` 和 `aspose-words-15.8.0.jar`。

2. **集成到项目中**: 将下载的 Jar 包添加到您的 Java 项目中。您可以通过以下方式将其添加到项目的构建路径中：
   - 对于 Maven 项目，可以将 Jar 包安装到本地 Maven 仓库，然后在 `pom.xml` 中添加依赖。
   - 对于非 Maven 项目，可以直接将 Jar 包添加到项目的 `lib` 目录中，并在构建路径中引用。

3. **编写代码**: 使用 Aspose Cells 库提供的 API 将 Excel 文件转换为 PDF 格式。以下是一个简单的示例代码：

   ```java
   import com.aspose.cells.*;

   public class ExcelToPdfConverter {
       public static void main(String[] args) throws Exception {
           // 加载 Excel 文件
           Workbook workbook = new Workbook("input.xlsx");

           // 保存为 PDF 格式
           workbook.save("output.pdf", SaveFormat.PDF);

           System.out.println("Excel 文件已成功转换为 PDF 格式。");
       }
   }
   ```

4. **运行程序**: 编译并运行您的 Java 程序，确保 Excel 文件已成功转换为 PDF 格式。

## 注意事项

- 请确保您已获得 Aspose 库的合法授权，以避免任何潜在的法律问题。
- 在使用 Aspose 库时，请参考官方文档以获取更多详细信息和示例代码。

## 联系我们

如果您在使用过程中遇到任何问题或有任何疑问，请随时联系我们。我们将尽力为您提供帮助。

## 下载链接

[AsposeExcel转PDF依赖的Jar包](https://pan.quark.cn/s/8673d00017ee)