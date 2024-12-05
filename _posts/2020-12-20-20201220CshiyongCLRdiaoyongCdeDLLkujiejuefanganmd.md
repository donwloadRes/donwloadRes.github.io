---
layout: post
title: "C#使用CLR调用C++的DLL库解决方案"
date:   2023-08-18
tags: [C++,DLL,CLR,类库,C#]
comments: true
author: admin
---
# C#使用CLR调用C++的DLL库解决方案

本仓库提供了一个完整的解决方案，展示了如何在C#中使用CLR（Common Language Runtime）调用C++编写的DLL库。该解决方案包含三个工程，分别对应C++的DLL、C++的CLR类库以及C#的可执行文件。

## 解决方案结构

1. **工程一：C++的DLL**
   - 该工程使用C++编写，生成了一个DLL库。该DLL库包含了需要在C#中调用的函数和类。

2. **工程二：C++的CLR的类库**
   - 该工程使用C++/CLI（C++ Language Integrated）编写，生成了一个CLR类库。该类库作为桥梁，将C++的DLL库中的函数和类暴露给C#。

3. **工程三：C#的exe**
   - 该工程使用C#编写，生成了一个可执行文件。该可执行文件通过调用C++的CLR类库，间接调用了C++的DLL库中的函数和类。

## 使用说明

1. **编译C++的DLL**
   - 首先，打开工程一，编译生成C++的DLL库。确保DLL库生成成功，并将其放置在合适的路径下。

2. **编译C++的CLR类库**
   - 接着，打开工程二，编译生成C++的CLR类库。确保CLR类库生成成功，并将其放置在合适的路径下。

3. **编译C#的可执行文件**
   - 最后，打开工程三，编译生成C#的可执行文件。在C#项目中，通过引用C++的CLR类库，调用C++的DLL库中的函数和类。

## 注意事项

- 确保所有工程的编译选项和依赖项配置正确，特别是C++的CLR类库需要正确引用C++的DLL库。
- 在C#项目中，确保正确引用C++的CLR类库，并按照CLR类库的接口进行调用。

通过本解决方案，您可以轻松地在C#中调用C++编写的DLL库，实现跨语言的互操作。

## 下载链接

[C使用CLR调用C的DLL库解决方案](https://pan.quark.cn/s/8a4c691290ba)