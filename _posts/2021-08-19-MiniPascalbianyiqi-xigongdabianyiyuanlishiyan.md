---
layout: post
title: "MiniPascal编译器-西工大编译原理实验"
date:   2021-08-27
tags: [Begin,End,编译器,编译,10]
comments: true
author: admin
---
# MiniPascal编译器-西工大编译原理实验

## 项目介绍

本项目是一个MiniPascal编译器的实现，作为西北工业大学编译原理课程的实验项目。该编译器支持多种Pascal语言特性，包括但不限于：

- 消除注释
- FOR循环
- 多维数组
- 自动类型转换
- 类型检查
- 数组维数检查
- 错误提示

## 功能特性

1. **消除注释**：编译器能够自动识别并消除代码中的注释，确保代码的纯净性。
2. **FOR循环**：支持Pascal语言中的FOR循环语法，能够正确解析和执行FOR循环结构。
3. **多维数组**：实现了多维数组的定义和使用，支持数组的嵌套和复杂操作。
4. **自动类型转换**：在进行算术运算或赋值操作时，能够自动进行类型转换，确保操作的正确性。
5. **类型检查**：在编译过程中进行严格的类型检查，防止类型不匹配的错误。
6. **数组维数检查**：在数组定义和使用时，检查数组的维度是否匹配，避免维度错误。
7. **错误提示**：提供详细的错误提示信息，帮助用户快速定位和修复代码中的问题。

## 使用说明

1. **环境配置**：
   - 使用CodeBlocks作为开发环境。
   - 下载并配置Flex和Bison工具包。
   - 在CodeBlocks中设置Flex和Bison的路径，并配置编译和生成语句。

2. **编译与运行**：
   - 创建对应的`.l`和`.y`文件，并进行编译。
   - 编译完成后，可以链接运行生成的可执行文件。

3. **抽象语法树生成**：
   - 使用Graphviz工具生成抽象语法树的可视化图像。
   - 通过遍历语法树并生成描述文件，调用Graphviz工具生成图像。

## 示例代码

以下是一个简单的MiniPascal程序示例：

```pascal
Program mini1;
Var
    a, b, c, d, e : Integer;
    arr1, arr2 : Array[10, 10] Of Integer;
    arr3 : Array[10, 10] Of Real;
Begin
    e := 1;
    For a := 0 To 9 Do
    Begin
        For b := 0 To 9 Do
        Begin
            c := 1;
            While c <= 100 Do
            Begin
                If e <> 1 Then
                Begin
                    c := c * 10;
                End
                Else
                Begin
                    c := c * 20;
                    While d < (c + 2) Do
                    Begin
                        If (e <> 1) || (e <> 1) Then
                        Begin
                            c := d * 10;
                        End
                    End
                End
            End;
            arr1[a][b] := c;
            arr1[b][a] := arr1[a][b];
            arr3[b][a] := (arr1[a][b] + 1.2) * d + 2;
        End
    End
End.
```

## 总结

本项目通过实现MiniPascal编译器，帮助学生深入理解编译原理的相关知识，并提供了丰富的功能和详细的错误提示，使得编译器的使用更加便捷和高效。

## 下载链接

[MiniPascal编译器-西工大编译原理实验分享](https://pan.quark.cn/s/6c35c4103a24)