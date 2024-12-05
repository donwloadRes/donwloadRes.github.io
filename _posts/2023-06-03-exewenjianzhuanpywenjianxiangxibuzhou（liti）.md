---
layout: post
title: "exe文件转py文件详细步骤（例题）"
date:   2024-01-23
tags: [py,文件,解包,exe,white]
comments: true
author: admin
---
# exe文件转py文件详细步骤（例题）

本文详细介绍了如何将一个exe文件转换为py文件的过程，包括从exe文件解包为pyc文件，再将pyc文件反编译为可读的py文件。以下是详细的步骤说明。

## 1. 解包exe文件(exe > pyc)

1. 下载并安装Python解包exe项目。
2. 将解包工具移动到想要解包的文件目录下。
3. 在当前目录下打开终端，输入以下命令进行解包：
   ```
   python pyinstxtractor-ng.py white_give.exe
   ```
4. 解包后会在当前目录下生成一个名为`white_give.exe_extracted`的文件夹。
5. 进入该文件夹，会发现与解包文件相同名称的pyc文件，例如`white_give.pyc`。

## 2. 将pyc文件转为py文件(pyc > py)

1. 安装`uncompyle6`工具：
   ```
   pip install uncompyle6
   ```
2. 进入解包完成的目录，并在该目录下运行cmd，输入以下命令将pyc文件反编译为py文件：
   ```
   uncompyle6 white_give.pyc > white_give.py
   ```
3. 运行成功后，即可看到生成了`white_give.py`文件。
4. 打开`white_give.py`文件，即可查看源代码。

## 3. 算法逆向

1. 对反编译后的代码进行分析，可以进一步了解程序的逻辑和功能。
2. 通过分析代码，可以找到程序中的关键部分，例如输入验证、加密算法等。

通过以上步骤，你可以成功将一个exe文件转换为可读的py文件，并进一步分析其源代码。

## 下载链接

[exe文件转py文件详细步骤例题](https://pan.quark.cn/s/ef702a4ea982)