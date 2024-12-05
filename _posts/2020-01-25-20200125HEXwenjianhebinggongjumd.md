---
layout: post
title: "HEX文件合并工具"
date:   2021-09-15
tags: [文件,HEX,mergeHEX,批处理,exe]
comments: true
author: admin
---
# HEX文件合并工具

## 简介

`mergeHEX.zip` 是一个用于合并HEX文件的小工具，通过批处理脚本调用传参，在MDK中可以在魔术棒的User选项卡设置编译后调用批处理脚本，使用起来非常方便。

## 文件说明

1. **main.c**  
   - 这是 `mergeHEX.exe` 的源码文件。

2. **mergeHEX.exe**  
   - 这是由 `main.c` 生成的可执行文件，可以直接使用。

3. **merge_hex.bat**  
   - 这是一个批处理文件，用于调用 `mergeHEX.exe` 并传入文件路径参数。需要注意的是，文件路径只能使用相对路径，且总路径长度不能大于2048个字节。

## 使用方法

1. 在MDK中，打开魔术棒选项卡。
2. 在User选项卡中设置编译后调用 `merge_hex.bat` 批处理脚本。
3. 编译完成后，批处理脚本会自动调用 `mergeHEX.exe` 并传入相应的文件路径参数，完成HEX文件的合并。

## 注意事项

- 文件路径只能使用相对路径。
- 总路径长度不能大于2048个字节。

通过以上步骤，您可以方便地使用该工具进行HEX文件的合并操作。

## 下载链接

[HEX文件合并工具](https://pan.quark.cn/s/5c4541fe1cf1)