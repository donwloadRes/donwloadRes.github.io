---
layout: post
title: "Qt mingw release版异常结束 crash信息捕捉和跟踪含测试代码"
date:   2022-07-01
tags: [异常,release,Qt,crash,捕捉]
comments: true
author: admin
---
# Qt mingw release版异常结束 crash信息捕捉和跟踪(含测试代码)

## 简介

在开发Qt应用程序时，经常会遇到程序在debug模式下运行正常，但在release模式下却异常结束的情况。特别是在程序发布后，客户反馈程序崩溃，但开发者自己却无法复现问题。这种情况下，如果能捕获到异常时的相关信息，将有助于快速定位和解决问题。

本资源文件提供了Qt mingw编译程序crash信息捕捉和跟踪的方法说明，并附带了测试程序代码，帮助开发者更好地处理release版程序的异常结束问题。

## 资源内容

1. **Qt mingw编译程序crash信息捕捉和跟踪方法说明**：详细介绍了如何在Qt mingw环境下捕捉和跟踪程序的异常崩溃信息。

2. **测试程序代码**：包含了一个简单的测试程序，用于演示如何在release版中捕捉和记录异常信息。

## 使用步骤

1. **修改.pro文件**：在项目文件（.pro）中添加调试信息，以便在生成release版时保留必要的调试符号。

2. **添加ccrashstack类**：在项目中添加ccrashstack类，用于捕捉和记录异常信息。

3. **在main函数中添加异常处理**：在main函数中添加`SetUnhandledExceptionFilter(callback);`，以捕获未处理的异常。

4. **生成exe并反汇编**：使用`objdump -S xxx.exe > aaa.asm`命令生成exe文件的反汇编代码，以便在异常发生时查找异常地址对应的代码位置。

5. **分析crash.log**：从生成的crash.log文件中获取异常地址，并结合反汇编代码定位问题所在。

## 注意事项

- 确保在release版中保留足够的调试信息，以便在异常发生时能够准确定位问题。
- 在发布程序时，建议保留一份反汇编代码，以便在客户反馈异常时能够快速定位问题。

通过以上步骤，开发者可以有效地捕捉和跟踪Qt mingw编译程序在release版中的异常崩溃信息，从而更快地解决问题，提升程序的稳定性和用户体验。

## 下载链接

[Qtmingwrelease版异常结束crash信息捕捉和跟踪含测试代码](https://pan.quark.cn/s/a497cf153039)